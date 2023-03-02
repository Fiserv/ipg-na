
# 3-D Secure Test Data

The purpose of 3DS test cards is to simulate AUTHENTICATION responses, it means that they do not automatically guarantee approved AUTHORIZATION.

Test cards should only be used for the AUTHENTICATION SCENARIO / TEST CASE they support, misusing the card for any other authentication responses will not provide the correct result. The description suggests applicable scenario, e.g. ***Frictionless Y*** test card is able to provide authentication transStatus = Y and corresponding ECI value (02 or 05).

Expiry date for all cards =  any future date
CVV = any 3digits number, e.g. 999 or 123

## Authentication Transaction Status

|*Value*|*Description*|
|----|----|
|Y|Fully Authenticated|
|N|Not Authenticated, cardholder not enrolled|
|A|Attempted Authentication|
|R|Rejected Authentication|
|U|Unable to Authenticate, ACS Not responding/Invalid 3DS Values received|


## Frictionless Flow

|*Test Case*|*IPG 3DS Response Code*|*Authentication Trans Status*|*Test Card*|
|----|----|----|----|
|Frictionless Fully Authenticated|1|Y|4147463011110083 <br/> 5239290700000028|
|Frictionless Not Authenticated|3|N|4147463011110091 <br/> 5239290700000036 <br/> 4147463011110091|
|Frictionless Attempted Authentication|4|A|4147463011110117 <br/> 5239290700000044|
|Frictionless Rejected Authentication|3|R|4147463011110042 <br/> 5239290700000051|
|Frictionless Unable to Authenticate|6|U|4147463011110067 <br/> 5239290700000069 <br/> 4147463011110125|

## Frictionless Flow + 3DSMethod

|*Test Case*|*IPG 3DS Response Code*|*Authentication TransStatus*|*Test Card Number*|
|----|----|----|----|
|Frictionless Fully Authenticated  + 3DSMethod|1|Y|4012000000012011004 <br/> 4265880000000007 <br/> 4265880000000049 <br/> 4099000000001978 <br/> 5204740000002711|
|Frictionless Not Authenticated + 3DSMethod|3|N|5426064000425117 <br/> 4012000000012011012 <br/> 5426064000425190 <br/> 4265880000000015 <br/> 4099000000001986 <br/> 5204740000002729|
|Unable to Authenticate + 3DSMethod|6|U|5426064000425216 <br/> 4012000000012011020 <br/> 4265880000000056 <br/> 4265880000000072 <br/> 4265880000000080 <br/> 5204740000002786 <br/> 4012001037167778|
|Frictionless Attempted Authentication + 3DSMethod|4|A|5426064000425208 <br/> 4149011500000519 <br/> 4265880000000023|
|Rejected Authentication + 3DSMethod|3|R|5204740000002778 <br/> 4265880000000031 <br/> 4012000000012011038|

## Challenge Flow

|*Test Case*|*IPG 3DS Response Code*|*Authentication Trans Status*|*Test Card*|
|----|----|----|----|
|Challenge - Y|1|Y|4147463011110109|
|Challenge - R|3|R|4147463011110034 <br/> 5239290700000010|
|Challenge - configurable response |1 <br/> 4 <br/> 6 <br/> 3|Y <br/> A <br/> U <br/> N/R |4147463011110059 <br/> 5239290700000002 |

## Challenge Flow + 3DSMethod

|*Test Case*|*IPG 3DS Response Code*|*Authentication Trans Status*|*Test Card*|
|----|----|----|----|
|Challenge - R|3|R|4149011500000535 <br/> 5204740000002760|
|Challenge - configurable response |1 <br/> 3 <br/> 4 <br/> 6|Y <br/> N/R <br/> A <br/> U |5204740000002745 <br/> 5544330000000235 <br/> 4099000000001960 <br/> 4149011500000527 <br/> 4265880000000064 |


## Fallback to 3DS 1.0

 |*Test Case*|*IPG 3DS Response Code*|*Authentication Trans Status*|*Test Card*|
|----|----|----|----|
|Fallback to 3DS 1.0|1|Y|4147463011110109|
|Challenge - R|3|R|4035874000424977 <br/> 5204730000001003 <br/> 5210000010001001 <br/> 2223000280000016|
||Fallback to 3DS 1.0 (not enrolled)|3|N|4000000000000002|


> [Back to 3-D Secure main page](?path=docs/3dsecure-md/3DSecure.md)
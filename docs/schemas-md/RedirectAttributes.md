
# RedirectAttributes

| *description*: | *Attributes for controlling transactions with additional parameters like dccFlow, '3ds' flows.*|
|----|----|
| challengeIndicator |    ``` string ```  <br/>  *default: 01 example: 01 * <br/> Indicates whether or not a challenge should be performed. 01 = No preference (You have no preference whether a challenge should be performed. This is the default value) 02 = No challenge requested (You prefer that no challenge should be performed) 03 = Challenge requested: 3DS Requestor Preference (You prefer that a challenge should be performed) 04 = Challenge requested: Mandate (There are local or regional mandates that mean that a challenge must be performed) <br/> Enum:[ 01, 02, 03, 04 ]|
| authenticateTransaction |    ``` string ```  <br/>  *example: true* <br/> If 3D secure should be applied.|
| threeDSEmvCoMessageCategory |    ``` string ```  <br/>  *example: 01* <br/> EmvCo Messag Category <br/> Enum:[ 01, 02, 80 ]|
| browserJavaScriptEnabled |    ``` boolean ```  <br/>  *default: false <br/> Browser Java Script Enabled flag|
| browserJavaEnabled |    ``` boolean ```  <br/>  *default: false <br/> Boolean that represents the ability of the cardholder browser to execute Java (required for 2.1, mandatory for 2.2 when browserjavaScriptEnabled=true)> ATTENTION - it is stronly recommended to be set (but optional at the moment for backward compatibility)|
| override3dsCountryExclusion |    ``` boolean ```  <br/>  *default: false <br/> Override 3ds Country Exclusion flag|
| threeDSTransactionType |    ``` string ```  <br/>  *example: 01* <br/> Secure 3D Transaction Type <br/> Enum:[ 01, 03, 10, 11, 28 ]|
| skipTRA |   SkipTRA  ``` boolean ```  <br/>  *default: false <br/> skip TRA exemption for the transaction|
| fullBypass |    ``` boolean ```  <br/>  *default: false  <br/> Full by pass flag|
| mobileMode |    ``` boolean ```  <br/>  *default: false <br/> Mobile mode flag|
| paymentMode |    ``` string ```  <br/>  *example: FULLPAY* <br/> Payment Mode <br/> Enum:[ FULLPAY, PAYONLY, PAYPLUS ]|
| language |    ``` string ```  <br/>  pattern: ^(?!\s*$).+ <br/> *example: en* <br/> Language used by client.|  




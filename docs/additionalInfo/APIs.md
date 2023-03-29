
# APIs


For server-to-server interactions with the First Data Gateway, we provide APIs that give you maximum flexibility in implementing custom business logic and full control over the look and feel of the customer journey.

This type of integration suits best for steps where no direct consumer interaction is required and no sensitive cardholder data is getting processed.

Please note that if you store or process cardholder data within your own application, you must ensure that your system components are compliant with the Data Security Standard of the Payment Card Industry (PCI DSS). Depending on your transaction volume, an assessment by a Qualified Security Assessor may be mandatory to declare your compliance status.

For tokenization of card details that you can then use for later payment transactions via API requests, please have a look at our JavaScript option for this purpose.

## API Options

|   |   |   |
|---|---|---|
|**REST API** |Simple lightweight API for the most common operations in **Card Not Present** scenarios. Covers requests and responses for payment transactions, inquiries, payment schedules, payment tokens, card verification and currency conversion.| [ REST API Reference](?path=docs/schemas-md/PaymentCardPreAuthTransaction.md)|
|**SOAP API**|	Language and platform independent API that covers both **Card Not Present and Card Present** scenarios.|[SOAP API Reference](?path=docs/additionalInfo/SOAPAPIIntegrationGuide.md)|
|**Nexo Acquirer Protocol**|ISO 20022 based standard interface for Card Present scenarios allowing interoperability between different implementations. It handles, amongst other features, the authorization, pre-authorization, refund, cancellation and rejection of card transactions.<br/>*Please note that Nexo-based integrations to our gateway require an implementation project where integration details will be mutually agreed.*|[Nexo Specification](https://www.nexo-standards.org/user?category=protocols&about=nexo-acquirer-protocol)|
||||

## Alternative Options

> [Hosted Payment Pages](?path=docs/additionalInfo/HostedPaymentPages.md)

> [Direct Post](?path=docs/additionalInfo/DirectPost.md)
---
share: true
created: 2023-10-30T14:29
updated: 2025-03-04T15:47
---
[HTTP là ngôn ngữ để trình duyệt và webserver nói chuyện với nhau](../../%F0%9F%96%A5%EF%B8%8FM%E1%BA%A1ng%20m%C3%A1y%20t%C3%ADnh/Giao%20th%E1%BB%A9c/HTTP/HTTP%20l%C3%A0%20ng%C3%B4n%20ng%E1%BB%AF%20%C4%91%E1%BB%83%20tr%C3%ACnh%20duy%E1%BB%87t%20v%C3%A0%20webserver%20n%C3%B3i%20chuy%E1%BB%87n%20v%E1%BB%9Bi%20nhau.md)
Web service là các API của các dịch vụ trên mạng, cần phải có internet mới dùng được nó. Gọi là là web API cũng được. Nhưng cần phân biệt với [web API của JS](../Ng%C3%B4n%20ng%E1%BB%AF/Ng%C3%B4n%20ng%E1%BB%AF%20l%E1%BA%ADp%20tr%C3%ACnh/Ng%C3%B4n%20ng%E1%BB%AF%20ki%E1%BB%83u%20%C4%91%E1%BB%99ng/JavaScript/M%C3%B4i%20tr%C6%B0%E1%BB%9Dng%20th%E1%BB%B1c%20thi%20(runtime)/Web%20API%20l%C3%A0%20nh%E1%BB%AFng%20API%20%C4%91%C6%B0%E1%BB%A3c%20tr%C3%ACnh%20duy%E1%BB%87t%20cung%20c%E1%BA%A5p,%20kh%C3%B4ng%20ph%E1%BA%A3i%20c%E1%BB%A7a%20%C4%91%E1%BB%99ng%20c%C6%A1.md). Nó là API của trình duyệt, chứ không phải của dịch vụ trên mạng nào. Không có internet vẫn dùng được.

## What is Web API?
- An API (Application Programming Interface) is the means by which third parties can write code that interfaces with other code.
-  A Web Service is a type of API, one that almost always operates over HTTP (though some, like SOAP, can use alternate transports, like SMTP).
- Web API is typically done as HTTP/SMTP (REST/SOAP), output can be eg: JSON/XML, input can be XML/JSON or plain data.

[![](https://sp-ao.shortpixel.ai/client/to_auto,q_glossy,ret_img,w_1134,h_1078/https://lcdung.top/wp-content/uploads/2018/07/apis-devices.jpg)](https://lcdung.top/web-services-apis/apis-devices/)

## SOAP vs REST comparison

#### Origin

|   |   |
|---|---|
|REST|SOAP|
|– REST (Representational State Transfer) was Created in 2000 by Roy Fielding in UC, Irvine.  <br>– Developed in an academic environment, this protocol embraces the philosophy of the open Web|– SOAP (Simple Object Access  <br>Protocol), was created in 1998 by Dave Winer et al in collaboration  <br>with Microsoft.  <br>– Developed by a large software company, this protocol addresses the goal of addressing the needs of the enterprise market.|

#### BASIC CONCEPT

|   |   |
|---|---|
|REST|SOAP|
|– Makes data  vailable as resources (nouns), for example “user” or “invoice”|– Makes data available as services (verb + noun), for example “getUser” or “PayInvoice”|

#### ADVANTAGES

|   |   |
|---|---|
|REST|SOAP|
|– Follows the philosophy of the Open Web  <br>– Relatively easy to implement and maintain  <br>– Clearly separates client and server implementations  <br>– Communication isn’t controlled by a single entity  <br>– Information can be stored by the client to prevent multiple calls  <br>– Can return data in multiple formats (JSON, XML etc)|– Follows a formal enterprise  <br>approach  <br>– Works on top of any communication protocol, even asynchronously  <br>– Information about objects is communicated to clients  <br>– Security and authorization are part of the protocol  <br>– Can be fully described using WSDL|

#### DISADVANTAGES

|   |   |
|---|---|
|REST|SOAP|
|– Only works on top of the HTTP  <br>protocol.  <br>– Hard to enforce authorization and security on top of it|– Spends a lot of bandwidth communicating metadata.  <br>– Hard to implement and is unpopular among Web and mobile developers.  <br>– Uses only XML.|

#### WHEN TO USE

|   |   |
|---|---|
|REST|SOAP|
|– When clients and servers operate on a Web environment  <br>– When information about objects doesn’t need to be communicated to the client|– When clients need to have access to objects available on servers  <br>– When you want to enforce a formal contract between client and server|

#### COMMON USE CASES

|   |   |
|---|---|
|REST|SOAP|
|– Social Media services  <br>– Social Networks  <br>– Web Chat services  <br>– Mobile Services  <br>– Synchronize applications|– Financial services  <br>– Payment gateways  <br>– Telecommunication services|

#### POPULAR EXAMPLES

|   |   |
|---|---|
|REST|SOAP|
|– Facebook APIs  <br>– Google APIs  <br>– YouTube APIs  <br>– Twitter APIs  <br>– LinkedIn APIs  <br>– Instagram APIs|– Salesforce SOAP API  <br>– Paypal SOAP API  <br>– Clickatell SMS SOAP API  <br>– Almost Banking Systems|

## APIs Security

- IPs Whitelist
- Authentication (Oauth, Api Key…)
- Username/Password Scenarios
- Security Tokens + Signature
- Namespaces Required
- The Header

## Caching Data

#### Why to optimize?

- Increase visitor retention/engagement and loyalty.
- Better ranking on Google Search (SEO).
- Reduce the response time.
- Improve page load time.
- Make the customer happier.
-  Reduce network throughput in some types of optimization.
- Save customer money on bandwidth (mobile network).
- Helps the environment saving energy.
- COST !!!

#### COST !!!

- Reduce resource usage (CPU/Memory/DiskIO)
- Reduce network throughput
- Reduce requests queueing
- Reduce number or size of instances
- Increase number of concurrent requests per instance

#### Cache Types

- APC Cache
- Memcache
- Files Cache
- Severs Cache (Redis, Varnish)

## Logging

#### Why to log?

- Storage any actions from users
- Tracking system problems
- Code checking
- Customer support quickly
- Logging
- Avoid legal risks

#### Logging Levels

- FATAL
- ERROR
- WARNING
- INFO
- DEBUG

## Testing

#### Why should we do API testing?

Can help find/isolate problems:

- Security
- Robustness
- Functionality
- Testing

Reduce business costs

Nguồn:: [Web services (APIs) - LCDUNG](https://lcdung.top/web-services-apis/)
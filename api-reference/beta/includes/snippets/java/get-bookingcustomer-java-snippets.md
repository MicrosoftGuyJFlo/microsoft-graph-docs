---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

GraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

BookingCustomer bookingCustomer = graphClient.bookingBusinesses("Contosolunchdelivery@contoso.onmicrosoft.com").customers("8bb19078-0f45-4efb-b2c5-da78b860f73a")
	.buildRequest()
	.get();

```
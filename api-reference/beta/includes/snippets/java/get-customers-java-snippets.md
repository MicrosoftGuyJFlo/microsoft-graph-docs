---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

GraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

BookingCustomerCollectionPage customers = graphClient.bookingBusinesses("Contosolunchdelivery@contoso.onmicrosoft.com").customers()
	.buildRequest()
	.get();

```
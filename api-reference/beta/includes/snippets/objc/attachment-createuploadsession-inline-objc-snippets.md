---
description: "Automatically generated file. DO NOT MODIFY"
---

```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/me/messages/AAMkAGUwNjQ4ZjIxLTQ3Y2YtNDViMi1iZjc4LTMA=/attachments/createUploadSession"]]];
[urlRequest setHTTPMethod:@"POST"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

NSMutableDictionary *payloadDictionary = [[NSMutableDictionary alloc] init];

MSGraphAttachmentItem *attachmentItem = [[MSGraphAttachmentItem alloc] init];
[attachmentItem setAttachmentType: [MSGraphAttachmentType file]];
[attachmentItem setName:@"scenary"];
[attachmentItem setSize: 7208534];
[attachmentItem setIsInline: true];
[attachmentItem setContentId:@"my_inline_picture"];
payloadDictionary[@"AttachmentItem"] = attachmentItem;

NSData *data = [NSJSONSerialization dataWithJSONObject:payloadDictionary options:kNilOptions error:&error];
[urlRequest setHTTPBody:data];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
	completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

		//Request Completed

}];

[meDataTask execute];

```
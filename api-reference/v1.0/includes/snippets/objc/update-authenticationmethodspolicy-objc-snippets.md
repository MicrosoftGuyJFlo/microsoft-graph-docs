---
description: "Automatically generated file. DO NOT MODIFY"
---

```objc

MSHTTPClient *httpClient = [MSClientFactory createHTTPClientWithAuthenticationProvider:authenticationProvider];

NSString *MSGraphBaseURL = @"https://graph.microsoft.com/v1.0/";
NSMutableURLRequest *urlRequest = [NSMutableURLRequest requestWithURL:[NSURL URLWithString:[MSGraphBaseURL stringByAppendingString:@"/policies/authenticationMethodsPolicy"]]];
[urlRequest setHTTPMethod:@"PATCH"];
[urlRequest setValue:@"application/json" forHTTPHeaderField:@"Content-Type"];

MSGraphAuthenticationMethodsPolicy *authenticationMethodsPolicy = [[MSGraphAuthenticationMethodsPolicy alloc] init];
MSGraphRegistrationEnforcement *registrationEnforcement = [[MSGraphRegistrationEnforcement alloc] init];
MSGraphAuthenticationMethodsRegistrationCampaign *authenticationMethodsRegistrationCampaign = [[MSGraphAuthenticationMethodsRegistrationCampaign alloc] init];
[authenticationMethodsRegistrationCampaign setSnoozeDurationInDays: 1];
[authenticationMethodsRegistrationCampaign setState: [MSGraphAdvancedConfigState enabled]];
NSMutableArray *excludeTargetsList = [[NSMutableArray alloc] init];
[authenticationMethodsRegistrationCampaign setExcludeTargets:excludeTargetsList];
NSMutableArray *includeTargetsList = [[NSMutableArray alloc] init];
MSGraphAuthenticationMethodsRegistrationCampaignIncludeTarget *includeTargets = [[MSGraphAuthenticationMethodsRegistrationCampaignIncludeTarget alloc] init];
[includeTargets setId:@"3ee3a9de-0a86-4e12-a287-9769accf1ba2"];
[includeTargets setTargetType: [MSGraphAuthenticationMethodTargetType group]];
[includeTargets setTargetedAuthenticationMethod:@"microsoftAuthenticator"];
[includeTargetsList addObject: includeTargets];
[authenticationMethodsRegistrationCampaign setIncludeTargets:includeTargetsList];
[registrationEnforcement setAuthenticationMethodsRegistrationCampaign:authenticationMethodsRegistrationCampaign];
[authenticationMethodsPolicy setRegistrationEnforcement:registrationEnforcement];
NSMutableArray *authenticationMethodConfigurationsList = [[NSMutableArray alloc] init];
MSGraphAuthenticationMethodConfiguration *authenticationMethodConfigurations = [[MSGraphAuthenticationMethodConfiguration alloc] init];
[authenticationMethodConfigurations setId:@"Fido2"];
[authenticationMethodConfigurations setState: [MSGraphAuthenticationMethodState disabled]];
[authenticationMethodConfigurations setIsSelfServiceRegistrationAllowed: false];
[authenticationMethodConfigurations setIsAttestationEnforced: false];
MSGraphFido2KeyRestrictions *keyRestrictions = [[MSGraphFido2KeyRestrictions alloc] init];
[keyRestrictions setIsEnforced: false];
[keyRestrictions setEnforcementType: [MSGraphFido2RestrictionEnforcementType block]];
NSMutableArray *aaGuidsList = [[NSMutableArray alloc] init];
[keyRestrictions setAaGuids:aaGuidsList];
[authenticationMethodConfigurations setKeyRestrictions:keyRestrictions];
[authenticationMethodConfigurationsList addObject: authenticationMethodConfigurations];
[authenticationMethodsPolicy setAuthenticationMethodConfigurations:authenticationMethodConfigurationsList];

NSError *error;
NSData *authenticationMethodsPolicyData = [authenticationMethodsPolicy getSerializedDataWithError:&error];
[urlRequest setHTTPBody:authenticationMethodsPolicyData];

MSURLSessionDataTask *meDataTask = [httpClient dataTaskWithRequest:urlRequest 
	completionHandler: ^(NSData *data, NSURLResponse *response, NSError *nserror) {

		//Request Completed

}];

[meDataTask execute];

```
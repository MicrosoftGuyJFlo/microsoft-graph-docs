---
description: "Automatically generated file. DO NOT MODIFY"
---

```javascript

const options = {
	authProvider,
};

const client = Client.init(options);

const cloudPcOnPremisesConnection = {
  '@odata.type': '#microsoft.graph.cloudPcOnPremisesConnection',
  displayName: 'test-canary-02',
  type: 'hybridAzureADJoin',
  subscriptionId: '0ac520ee-14c0-480f-b6c9-0a90c585ffff',
  subscriptionName: 'CPC customer 001 test subscription',
  adDomainName: 'contoso001.com',
  adDomainUsername: 'dcadmin',
  organizationalUnit: 'OU=Domain Controllers, DC=contoso001, DC=com',
  resourceGroupId: '/subscriptions/0ac520ee-14c0-480f-b6c9-0a90c585ad47/resourceGroups/CustomerRG',
  virtualNetworkId: '/subscriptions/0ac520ee-14c0-480f-b6c9-0a90c585ad47/resourceGroups/CustomerRG/providers/Microsoft.Network/virtualNetworks/canary01-MyVNET',
  subnetId: '/subscriptions/0ac520ee-14c0-480f-b6c9-0a90c585ad47/resourceGroups/CustomerRG/providers/Microsoft.Network/virtualNetworks/canary01-MyVNET/subnets/canary01-Subnet'
};

await client.api('/deviceManagement/virtualEndpoint/onPremisesConnections')
	.version('beta')
	.post(cloudPcOnPremisesConnection);

```
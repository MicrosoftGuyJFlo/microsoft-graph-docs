---
description: "Automatically generated file. DO NOT MODIFY"
---

```powershell

Import-Module Microsoft.Graph.Teams

$params = @{
	"@odata.type" = "#microsoft.graph.aadUserConversationMember"
	Roles = @(
		"owner"
	)
}

Update-MgTeamChannelMember -TeamId $teamId -ChannelId $channelId -ConversationMemberId $conversationMemberId -BodyParameter $params

```
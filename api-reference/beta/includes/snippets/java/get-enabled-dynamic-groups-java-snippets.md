---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

IGroupCollectionPage groups = graphClient.groups()
	.buildRequest()
	.filter("membershipRuleProcessingState eq 'On'")
	.select("id,membershipRule,membershipRuleProcessingState,membershipRuleProcessingStatus")
	.get();

```
---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var tasks = await graphClient.Me.Outlook.TaskFolders["AAMkADIyAAAhrbPWAAA="].Tasks
	.Request()
	.GetAsync();

```
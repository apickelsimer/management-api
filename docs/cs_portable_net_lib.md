# Getting started

TODO: Add Description

## How to Build

The generated code uses the Newtonsoft Json.NET NuGet Package. If the automatic NuGet package restore
is enabled, these dependencies will be installed automatically. Therefore,
you will need internet access for build.

1. Open the solution (ApigeeEdgeAPIManagement.sln) file.
2. Invoke the build process using `Ctrl+Shift+B` shortcut key or using the `Build` menu as shown below.

![Building SDK using Visual Studio](https://apidocs.io/illustration/cs?step=buildSDK&workspaceFolder=Apigee%20Edge%20API%20Management-CSharp&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagement.Tests)

## How to Use

The build process generates a portable class library, which can be used like a normal class library. The generated library is compatible with Windows Forms, Windows RT, Windows Phone 8,
Silverlight 5, Xamarin iOS, Xamarin Android and Mono. More information on how to use can be found at the [MSDN Portable Class Libraries documentation](http://msdn.microsoft.com/en-us/library/vstudio/gg597391%28v=vs.100%29.aspx).

The following section explains how to use the ApigeeEdgeAPIManagement library in a new console project.

### 1. Starting a new project

For starting a new project, right click on the current solution from the *solution explorer* and choose  ``` Add -> New Project ```.

![Add a new project in the existing solution using Visual Studio](https://apidocs.io/illustration/cs?step=addProject&workspaceFolder=Apigee%20Edge%20API%20Management-CSharp&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagement.Tests)

Next, choose "Console Application", provide a ``` TestConsoleProject ``` as the project name and click ``` OK ```.

![Create a new console project using Visual Studio](https://apidocs.io/illustration/cs?step=createProject&workspaceFolder=Apigee%20Edge%20API%20Management-CSharp&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagement.Tests)

### 2. Set as startup project

The new console project is the entry point for the eventual execution. This requires us to set the ``` TestConsoleProject ``` as the start-up project. To do this, right-click on the  ``` TestConsoleProject ``` and choose  ``` Set as StartUp Project ``` form the context menu.

![Set the new cosole project as the start up project](https://apidocs.io/illustration/cs?step=setStartup&workspaceFolder=Apigee%20Edge%20API%20Management-CSharp&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagement.Tests)

### 3. Add reference of the library project

In order to use the ApigeeEdgeAPIManagement library in the new project, first we must add a projet reference to the ``` TestConsoleProject ```. First, right click on the ``` References ``` node in the *solution explorer* and click ``` Add Reference... ```.

![Open references of the TestConsoleProject](https://apidocs.io/illustration/cs?step=addReference&workspaceFolder=Apigee%20Edge%20API%20Management-CSharp&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagement.Tests)

Next, a window will be displayed where we must set the ``` checkbox ``` on ``` ApigeeEdgeAPIManagement.Tests ``` and click ``` OK ```. By doing this, we have added a reference of the ```ApigeeEdgeAPIManagement.Tests``` project into the new ``` TestConsoleProject ```.

![Add a reference to the TestConsoleProject](https://apidocs.io/illustration/cs?step=createReference&workspaceFolder=Apigee%20Edge%20API%20Management-CSharp&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagement.Tests)

### 4. Write sample code

Once the ``` TestConsoleProject ``` is created, a file named ``` Program.cs ``` will be visible in the *solution explorer* with an empty ``` Main ``` method. This is the entry point for the execution of the entire solution.
Here, you can add code to initialize the client library and acquire the instance of a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

![Add a reference to the TestConsoleProject](https://apidocs.io/illustration/cs?step=addCode&workspaceFolder=Apigee%20Edge%20API%20Management-CSharp&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagement.Tests)

## How to Test

The generated SDK also contain one or more Tests, which are contained in the Tests project.
In order to invoke these test cases, you will need *NUnit 3.0 Test Adapter Extension for Visual Studio*.
Once the SDK is complied, the test cases should appear in the Test Explorer window.
Here, you can click *Run All* to execute these test cases.

## Initialization

### Authentication
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| basicAuthUserName | The username to use with basic authentication |
| basicAuthPassword | The password to use with basic authentication |



API client can be initialized as following.

```csharp
// Configuration parameters and credentials
string basicAuthUserName = "basicAuthUserName"; // The username to use with basic authentication
string basicAuthPassword = "basicAuthPassword"; // The password to use with basic authentication

ApigeeEdgeAPIManagementClient client = new ApigeeEdgeAPIManagementClient(basicAuthUserName, basicAuthPassword);
```



# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [DeploymentsController](#deployments_controller)
* [UserRolesController](#user_roles_controller)
* [OAuthController](#o_auth_controller)
* [KVMController](#kvm_controller)
* [PodsController](#pods_controller)
* [ServersController](#servers_controller)
* [DevelopersController](#developers_controller)
* [APIsController](#ap_is_controller)
* [CacheController](#cache_controller)
* [AuditController](#audit_controller)
* [UsersController](#users_controller)
* [ZzzOthersController](#zzz_others_controller)
* [AppsController](#apps_controller)
* [VirtualHostsController](#virtual_hosts_controller)
* [EnvironmentsController](#environments_controller)
* [DeveloperAppController](#developer_app_controller)
* [KeystoresController](#keystores_controller)
* [ProductsController](#products_controller)
* [TargetServersController](#target_servers_controller)
* [CompanyController](#company_controller)
* [OrganizationsController](#organizations_controller)

## <a name="deployments_controller"></a>![Class: ](https://apidocs.io/img/class.png "ApigeeEdgeAPIManagement.Tests.Controllers.DeploymentsController") DeploymentsController

### Get singleton instance

The singleton instance of the ``` DeploymentsController ``` class can be accessed from the API Client.

```csharp
DeploymentsController deployments = client.Deployments;
```

### <a name="list_deployments"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.DeploymentsController.ListDeployments") ListDeployments

> List Deployments


```csharp
Task ListDeployments(string authorization, string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string oRG = "ORG";

await deployments.ListDeployments(authorization, oRG);

```


### <a name="get_deployments"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.DeploymentsController.GetDeployments") GetDeployments

> Deployments


```csharp
Task GetDeployments(string authorization, string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string oRG = "ORG";

await deployments.GetDeployments(authorization, oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="user_roles_controller"></a>![Class: ](https://apidocs.io/img/class.png "ApigeeEdgeAPIManagement.Tests.Controllers.UserRolesController") UserRolesController

### Get singleton instance

The singleton instance of the ``` UserRolesController ``` class can be accessed from the API Client.

```csharp
UserRolesController userRoles = client.UserRoles;
```

### <a name="create_user_roles_update"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.UserRolesController.CreateUserRolesUpdate") CreateUserRolesUpdate

> User Roles Update


```csharp
Task CreateUserRolesUpdate(PCL.Models.UserRolesUpdateRequest body, string authorization, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string bodyValue = "{ \"role\" : [ { \"name\" : \"orgadmin\", \"organization\" : \"dev\" }, { \"name\" : \"sysadmin\" } ] }";
var body = Newtonsoft.Json.JsonConvert.DeserializeObject<PCL.Models.UserRolesUpdateRequest>(bodyValue);
string authorization = "Basic {{BASICAUTH}}";
string contentType = "application/json";

await userRoles.CreateUserRolesUpdate(body, authorization, contentType);

```


### <a name="delete_an_organization_userrole"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.UserRolesController.DeleteAnOrganizationUserrole") DeleteAnOrganizationUserrole

> Delete an organization userrole


```csharp
Task DeleteAnOrganizationUserrole(string org, string authorization, string accept)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| org |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string org = "{{ORG}}";
string authorization = "Basic {{BASICAUTH}}";
string accept = "application/json";

await userRoles.DeleteAnOrganizationUserrole(org, authorization, accept);

```


### <a name="get_permissions_for_a_role"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.UserRolesController.GetPermissionsForARole") GetPermissionsForARole

> Get permissions for a role


```csharp
Task GetPermissionsForARole(string authorization, string contentType, string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string contentType = "Content-Type";
string oRG = "ORG";

await userRoles.GetPermissionsForARole(authorization, contentType, oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="o_auth_controller"></a>![Class: ](https://apidocs.io/img/class.png "ApigeeEdgeAPIManagement.Tests.Controllers.OAuthController") OAuthController

### Get singleton instance

The singleton instance of the ``` OAuthController ``` class can be accessed from the API Client.

```csharp
OAuthController oAuth = client.OAuth;
```

### <a name="get_o_auth2_token_details_get"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.OAuthController.GetOAuth2TokenDetailsGet") GetOAuth2TokenDetailsGet

> OAuth2 Token Details Get


```csharp
Task GetOAuth2TokenDetailsGet(string authorization, string contentType, string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string contentType = "Content-Type";
string oRG = "ORG";

await oAuth.GetOAuth2TokenDetailsGet(authorization, contentType, oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="kvm_controller"></a>![Class: ](https://apidocs.io/img/class.png "ApigeeEdgeAPIManagement.Tests.Controllers.KVMController") KVMController

### Get singleton instance

The singleton instance of the ``` KVMController ``` class can be accessed from the API Client.

```csharp
KVMController kVM = client.KVM;
```

### <a name="get_kvm_get"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.KVMController.GetKVMGet") GetKVMGet

> KVM Get


```csharp
Task GetKVMGet(
        string authorization,
        string contentType,
        string oRG,
        string eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string contentType = "Content-Type";
string oRG = "ORG";
string eNV = "ENV";

await kVM.GetKVMGet(authorization, contentType, oRG, eNV);

```


### <a name="delete_kvm_delete_entire_kvm"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.KVMController.DeleteKVMDeleteEntireKVM") DeleteKVMDeleteEntireKVM

> KVM Delete (Entire KVM)


```csharp
Task DeleteKVMDeleteEntireKVM(
        string authorization,
        string contentType,
        string oRG,
        string eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string contentType = "Content-Type";
string oRG = "ORG";
string eNV = "ENV";

await kVM.DeleteKVMDeleteEntireKVM(authorization, contentType, oRG, eNV);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="pods_controller"></a>![Class: ](https://apidocs.io/img/class.png "ApigeeEdgeAPIManagement.Tests.Controllers.PodsController") PodsController

### Get singleton instance

The singleton instance of the ``` PodsController ``` class can be accessed from the API Client.

```csharp
PodsController pods = client.Pods;
```

### <a name="get_analytics_pod"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.PodsController.GetAnalyticsPod") GetAnalyticsPod

> Analytics pod


```csharp
Task GetAnalyticsPod(string pod, string authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| pod |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string pod = "analytics";
string authorization = "Basic {{BASICAUTH}}";

await pods.GetAnalyticsPod(pod, authorization);

```


### <a name="get_associated_pods"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.PodsController.GetAssociatedPods") GetAssociatedPods

> Get Associated  Pods


```csharp
Task GetAssociatedPods(string contentType, string authorization, string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string contentType = "Content-Type";
string authorization = "Authorization";
string oRG = "ORG";

await pods.GetAssociatedPods(contentType, authorization, oRG);

```


### <a name="create_disassociate_org_from_pod"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.PodsController.CreateDisassociateOrgFromPOD") CreateDisassociateOrgFromPOD

> Disassociate Org from POD


```csharp
Task CreateDisassociateOrgFromPOD(string contentType, string authorization, string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string contentType = "Content-Type";
string authorization = "Authorization";
string oRG = "ORG";

await pods.CreateDisassociateOrgFromPOD(contentType, authorization, oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="servers_controller"></a>![Class: ](https://apidocs.io/img/class.png "ApigeeEdgeAPIManagement.Tests.Controllers.ServersController") ServersController

### Get singleton instance

The singleton instance of the ``` ServersController ``` class can be accessed from the API Client.

```csharp
ServersController servers = client.Servers;
```

### <a name="create_deregister"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.ServersController.CreateDeregister") CreateDeregister

> Deregister


```csharp
Task CreateDeregister(string authorization, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Basic {{BASICAUTH}}";
string contentType = "application/x-www-form-urlencoded";

await servers.CreateDeregister(authorization, contentType);

```


### <a name="list_server_by_uuid"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.ServersController.ListServerByUUID") ListServerByUUID

> List Server by UUID


```csharp
Task ListServerByUUID(string authorization, string uuid)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| uuid |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Basic {{BASICAUTH}}";
string uuid = "uuid";

await servers.ListServerByUUID(authorization, uuid);

```


### <a name="create_set_not_reachable"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.ServersController.CreateSetNotReachable") CreateSetNotReachable

> Set not reachable


```csharp
Task CreateSetNotReachable(string reachable, string authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| reachable |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string reachable = "false";
string authorization = "Basic {{BASICAUTH}}";

await servers.CreateSetNotReachable(reachable, authorization);

```


### <a name="list_org_env_servers"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.ServersController.ListOrgEnvServers") ListOrgEnvServers

> List org/env servers


```csharp
Task ListOrgEnvServers(string authorization, string oRG, string eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string oRG = "ORG";
string eNV = "ENV";

await servers.ListOrgEnvServers(authorization, oRG, eNV);

```


### <a name="create_register_server_with_org"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.ServersController.CreateRegisterServerWithOrg") CreateRegisterServerWithOrg

> Register server with org


```csharp
Task CreateRegisterServerWithOrg(
        string authorization,
        string contentType,
        string oRG,
        string eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string contentType = "Content-Type";
string oRG = "ORG";
string eNV = "ENV";

await servers.CreateRegisterServerWithOrg(authorization, contentType, oRG, eNV);

```


### <a name="create_associate_environments_to_mp"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.ServersController.CreateAssociateEnvironmentsToMP") CreateAssociateEnvironmentsToMP

> Associate  environments to MP


```csharp
Task CreateAssociateEnvironmentsToMP(
        string authorization,
        string contentType,
        string oRG,
        string eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string contentType = "Content-Type";
string oRG = "ORG";
string eNV = "ENV";

await servers.CreateAssociateEnvironmentsToMP(authorization, contentType, oRG, eNV);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="developers_controller"></a>![Class: ](https://apidocs.io/img/class.png "ApigeeEdgeAPIManagement.Tests.Controllers.DevelopersController") DevelopersController

### Get singleton instance

The singleton instance of the ``` DevelopersController ``` class can be accessed from the API Client.

```csharp
DevelopersController developers = client.Developers;
```

### <a name="get_developers"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.DevelopersController.GetDevelopers") GetDevelopers

> Get Developers


```csharp
Task GetDevelopers(string authorization, string contentType, string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string contentType = "Content-Type";
string oRG = "ORG";

await developers.GetDevelopers(authorization, contentType, oRG);

```


### <a name="create_developer"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.DevelopersController.CreateDeveloper") CreateDeveloper

> Create Developer


```csharp
Task CreateDeveloper(
        string body,
        string authorization,
        string contentType,
        string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string body = "Body";
string authorization = "Authorization";
string contentType = "Content-Type";
string oRG = "ORG";

await developers.CreateDeveloper(body, authorization, contentType, oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="ap_is_controller"></a>![Class: ](https://apidocs.io/img/class.png "ApigeeEdgeAPIManagement.Tests.Controllers.APIsController") APIsController

### Get singleton instance

The singleton instance of the ``` APIsController ``` class can be accessed from the API Client.

```csharp
APIsController aPIs = client.APIs;
```

### <a name="get_api_list"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.APIsController.GetApiList") GetApiList

> Api list


```csharp
Task GetApiList(string authorization, string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string oRG = "ORG";

await aPIs.GetApiList(authorization, oRG);

```


### <a name="create_deploy_api"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.APIsController.CreateDeployAPI") CreateDeployAPI

> Deploy API


```csharp
Task CreateDeployAPI(
        string action,
        string name,
        string authorization,
        string contentType,
        string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| action |  ``` Required ```  | TODO: Add a parameter description |
| name |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string action = "action";
string name = "name";
string authorization = "Authorization";
string contentType = "Content-Type";
string oRG = "ORG";

await aPIs.CreateDeployAPI(action, name, authorization, contentType, oRG);

```


### <a name="delete_an_api"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.APIsController.DeleteAnAPI") DeleteAnAPI

> Delete an API


```csharp
Task DeleteAnAPI(string authorization, string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string oRG = "ORG";

await aPIs.DeleteAnAPI(authorization, oRG);

```


### <a name="create_undeploy_revisions"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.APIsController.CreateUndeployRevisions") CreateUndeployRevisions

> Undeploy Revisions


```csharp
Task CreateUndeployRevisions(
        string action,
        string env,
        string authorization,
        string contentType,
        string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| action |  ``` Required ```  | TODO: Add a parameter description |
| env |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string action = "action";
string env = "env";
string authorization = "Authorization";
string contentType = "Content-Type";
string oRG = "ORG";

await aPIs.CreateUndeployRevisions(action, env, authorization, contentType, oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="cache_controller"></a>![Class: ](https://apidocs.io/img/class.png "ApigeeEdgeAPIManagement.Tests.Controllers.CacheController") CacheController

### Get singleton instance

The singleton instance of the ``` CacheController ``` class can be accessed from the API Client.

```csharp
CacheController cache = client.Cache;
```

### <a name="list_caches"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.CacheController.ListCaches") ListCaches

> List caches


```csharp
Task ListCaches(string authorization, string oRG, string eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string oRG = "ORG";
string eNV = "ENV";

await cache.ListCaches(authorization, oRG, eNV);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="audit_controller"></a>![Class: ](https://apidocs.io/img/class.png "ApigeeEdgeAPIManagement.Tests.Controllers.AuditController") AuditController

### Get singleton instance

The singleton instance of the ``` AuditController ``` class can be accessed from the API Client.

```csharp
AuditController audit = client.Audit;
```

### <a name="get_audit"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.AuditController.GetAudit") GetAudit

> Audit


```csharp
Task GetAudit(
        bool expand,
        string timeline,
        string authorization,
        string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| expand |  ``` Required ```  | TODO: Add a parameter description |
| timeline |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
bool expand = false;
string timeline = "timeline";
string authorization = "Authorization";
string oRG = "ORG";

await audit.GetAudit(expand, timeline, authorization, oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="users_controller"></a>![Class: ](https://apidocs.io/img/class.png "ApigeeEdgeAPIManagement.Tests.Controllers.UsersController") UsersController

### Get singleton instance

The singleton instance of the ``` UsersController ``` class can be accessed from the API Client.

```csharp
UsersController users = client.Users;
```

### <a name="get_developer_details_get"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.UsersController.GetDeveloperDetailsGet") GetDeveloperDetailsGet

> Developer Details Get


```csharp
Task GetDeveloperDetailsGet(string authorization, string contentType, string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string contentType = "Content-Type";
string oRG = "ORG";

await users.GetDeveloperDetailsGet(authorization, contentType, oRG);

```


### <a name="create_user_in_org"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.UsersController.CreateUserInORG") CreateUserInORG

> Create User in ORG


```csharp
Task CreateUserInORG(
        string body,
        string authorization,
        string contentType,
        string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string body = "Body";
string authorization = "Authorization";
string contentType = "Content-Type";
string oRG = "ORG";

await users.CreateUserInORG(body, authorization, contentType, oRG);

```


### <a name="list_users"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.UsersController.ListUsers") ListUsers

> List Users


```csharp
Task ListUsers(string authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Basic {{BASICAUTH}}";

await users.ListUsers(authorization);

```


### <a name="add_user_as_orgadmin"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.UsersController.AddUserAsOrgadmin") AddUserAsOrgadmin

> Add user as Orgadmin


```csharp
Task AddUserAsOrgadmin(
        string body,
        string authorization,
        string contentType,
        string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string body = "Body";
string authorization = "Authorization";
string contentType = "Content-Type";
string oRG = "ORG";

await users.AddUserAsOrgadmin(body, authorization, contentType, oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="zzz_others_controller"></a>![Class: ](https://apidocs.io/img/class.png "ApigeeEdgeAPIManagement.Tests.Controllers.ZzzOthersController") ZzzOthersController

### Get singleton instance

The singleton instance of the ``` ZzzOthersController ``` class can be accessed from the API Client.

```csharp
ZzzOthersController zzzOthers = client.ZzzOthers;
```

### <a name="get_cluster_status"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.ZzzOthersController.GetClusterStatus") GetClusterStatus

> Cluster Status


```csharp
Task GetClusterStatus(string authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Basic {{BASICAUTH}}";

await zzzOthers.GetClusterStatus(authorization);

```


### <a name="create_enable_debug_wo_restart"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.ZzzOthersController.CreateEnableDebugWORestart") CreateEnableDebugWORestart

> Enable Debug w/o Restart 


```csharp
Task CreateEnableDebugWORestart(string session, string authorization, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| session |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string session = "logsession_name";
string authorization = "Basic {{BASICAUTH}}";
string contentType = "application/x-www-form-urlencoded";

await zzzOthers.CreateEnableDebugWORestart(session, authorization, contentType);

```


### <a name="get_classifications"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.ZzzOthersController.GetClassifications") GetClassifications

> Classifications


```csharp
Task GetClassifications(string authorization, string hOST)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string hOST = "HOST";

await zzzOthers.GetClassifications(authorization, hOST);

```


### <a name="create_company_developer"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.ZzzOthersController.CreateCompanyDeveloper") CreateCompanyDeveloper

> Create Company Developer


```csharp
Task CreateCompanyDeveloper(
        PCL.Models.CreateCompanyDeveloperRequest body,
        string contentType,
        string authorization,
        string oRG,
        string cOMPANY)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| cOMPANY |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var body = new PCL.Models.CreateCompanyDeveloperRequest();
string contentType = "Content-Type";
string authorization = "Authorization";
string oRG = "ORG";
string cOMPANY = "COMPANY";

await zzzOthers.CreateCompanyDeveloper(body, contentType, authorization, oRG, cOMPANY);

```


### <a name="get_qpid_metrics"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.ZzzOthersController.GetQPIDMetrics") GetQPIDMetrics

> QPID Metrics


```csharp
Task GetQPIDMetrics(string authorization, string hOST)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string hOST = "HOST";

await zzzOthers.GetQPIDMetrics(authorization, hOST);

```


### <a name="get_build_info"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.ZzzOthersController.GetBuildInfo") GetBuildInfo

> Build Info


```csharp
Task GetBuildInfo(string authorization, string hOST, string pORT)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |
| pORT |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string hOST = "HOST";
string pORT = "PORT";

await zzzOthers.GetBuildInfo(authorization, hOST, pORT);

```


### <a name="delete_disable_debug_wo_restart"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.ZzzOthersController.DeleteDisableDebugWORestart") DeleteDisableDebugWORestart

> Disable Debug w/o Restart


```csharp
Task DeleteDisableDebugWORestart(string authorization, string contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Basic {{BASICAUTH}}";
string contentType = "application/x-www-form-urlencoded";

await zzzOthers.DeleteDisableDebugWORestart(authorization, contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="apps_controller"></a>![Class: ](https://apidocs.io/img/class.png "ApigeeEdgeAPIManagement.Tests.Controllers.AppsController") AppsController

### Get singleton instance

The singleton instance of the ``` AppsController ``` class can be accessed from the API Client.

```csharp
AppsController apps = client.Apps;
```

### <a name="create_company_app"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.AppsController.CreateCompanyAPP") CreateCompanyAPP

> Create Company APP


```csharp
Task CreateCompanyAPP(
        string body,
        string authorization,
        string contentType,
        string oRG,
        string cOMPANY)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| cOMPANY |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string body = "Body";
string authorization = "Authorization";
string contentType = "Content-Type";
string oRG = "ORG";
string cOMPANY = "COMPANY";

await apps.CreateCompanyAPP(body, authorization, contentType, oRG, cOMPANY);

```


### <a name="add_app_credentials"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.AppsController.AddAppCredentials") AddAppCredentials

> Add app credentials


```csharp
Task AddAppCredentials(
        string body,
        string authorization,
        string contentType,
        string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string body = "Body";
string authorization = "Authorization";
string contentType = "Content-Type";
string oRG = "ORG";

await apps.AddAppCredentials(body, authorization, contentType, oRG);

```


### <a name="list_apps"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.AppsController.ListApps") ListApps

> List apps 


```csharp
Task ListApps(string authorization, string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string oRG = "ORG";

await apps.ListApps(authorization, oRG);

```


### <a name="list_app"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.AppsController.ListApp") ListApp

> List app


```csharp
Task ListApp(string authorization, string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string oRG = "ORG";

await apps.ListApp(authorization, oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="virtual_hosts_controller"></a>![Class: ](https://apidocs.io/img/class.png "ApigeeEdgeAPIManagement.Tests.Controllers.VirtualHostsController") VirtualHostsController

### Get singleton instance

The singleton instance of the ``` VirtualHostsController ``` class can be accessed from the API Client.

```csharp
VirtualHostsController virtualHosts = client.VirtualHosts;
```

### <a name="list_virtual_hosts"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.VirtualHostsController.ListVirtualHosts") ListVirtualHosts

> List VirtualHosts


```csharp
Task ListVirtualHosts(string authorization, string oRG, string eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string oRG = "ORG";
string eNV = "ENV";

await virtualHosts.ListVirtualHosts(authorization, oRG, eNV);

```


### <a name="add_virtual_host"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.VirtualHostsController.AddVirtualHost") AddVirtualHost

> Add Virtual Host


```csharp
Task AddVirtualHost(
        string body,
        string authorization,
        string contentType,
        string oRG,
        string eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string body = "Body";
string authorization = "Authorization";
string contentType = "Content-Type";
string oRG = "ORG";
string eNV = "ENV";

await virtualHosts.AddVirtualHost(body, authorization, contentType, oRG, eNV);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="environments_controller"></a>![Class: ](https://apidocs.io/img/class.png "ApigeeEdgeAPIManagement.Tests.Controllers.EnvironmentsController") EnvironmentsController

### Get singleton instance

The singleton instance of the ``` EnvironmentsController ``` class can be accessed from the API Client.

```csharp
EnvironmentsController environments = client.Environments;
```

### <a name="update_environments"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.EnvironmentsController.UpdateEnvironments") UpdateEnvironments

> Update Environments


```csharp
Task UpdateEnvironments(
        string authorization,
        string contentType,
        string oRG,
        string eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string contentType = "Content-Type";
string oRG = "ORG";
string eNV = "ENV";

await environments.UpdateEnvironments(authorization, contentType, oRG, eNV);

```


### <a name="delete_environment"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.EnvironmentsController.DeleteEnvironment") DeleteEnvironment

> Delete Environment


```csharp
Task DeleteEnvironment(string authorization, string oRG, string eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string oRG = "ORG";
string eNV = "ENV";

await environments.DeleteEnvironment(authorization, oRG, eNV);

```


### <a name="create_new_env_in_org"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.EnvironmentsController.CreateNewENVInORG") CreateNewENVInORG

> Create New ENV in ORG


```csharp
Task CreateNewENVInORG(
        string body,
        string authorization,
        string contentType,
        string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string body = "Body";
string authorization = "Authorization";
string contentType = "Content-Type";
string oRG = "ORG";

await environments.CreateNewENVInORG(body, authorization, contentType, oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="developer_app_controller"></a>![Class: ](https://apidocs.io/img/class.png "ApigeeEdgeAPIManagement.Tests.Controllers.DeveloperAppController") DeveloperAppController

### Get singleton instance

The singleton instance of the ``` DeveloperAppController ``` class can be accessed from the API Client.

```csharp
DeveloperAppController developerApp = client.DeveloperApp;
```

### <a name="get_developer_app_details_get"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.DeveloperAppController.GetDeveloperAppDetailsGet") GetDeveloperAppDetailsGet

> Developer App Details Get


```csharp
Task GetDeveloperAppDetailsGet(string authorization, string contentType, string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string contentType = "Content-Type";
string oRG = "ORG";

await developerApp.GetDeveloperAppDetailsGet(authorization, contentType, oRG);

```


### <a name="delete_app_credentials"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.DeveloperAppController.DeleteAppCredentials") DeleteAppCredentials

> Delete app credentials


```csharp
Task DeleteAppCredentials(string authorization, string accept, string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string accept = "Accept";
string oRG = "ORG";

await developerApp.DeleteAppCredentials(authorization, accept, oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="keystores_controller"></a>![Class: ](https://apidocs.io/img/class.png "ApigeeEdgeAPIManagement.Tests.Controllers.KeystoresController") KeystoresController

### Get singleton instance

The singleton instance of the ``` KeystoresController ``` class can be accessed from the API Client.

```csharp
KeystoresController keystores = client.Keystores;
```

### <a name="list_keystores"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.KeystoresController.ListKeystores") ListKeystores

> List Keystores


```csharp
Task ListKeystores(string authorization, string oRG, string eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string oRG = "ORG";
string eNV = "ENV";

await keystores.ListKeystores(authorization, oRG, eNV);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="products_controller"></a>![Class: ](https://apidocs.io/img/class.png "ApigeeEdgeAPIManagement.Tests.Controllers.ProductsController") ProductsController

### Get singleton instance

The singleton instance of the ``` ProductsController ``` class can be accessed from the API Client.

```csharp
ProductsController products = client.Products;
```

### <a name="get_api_products"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.ProductsController.GetApiProducts") GetApiProducts

> Api Products


```csharp
Task GetApiProducts(string authorization, string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string oRG = "ORG";

await products.GetApiProducts(authorization, oRG);

```


### <a name="create_ap_iproduct_creation"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.ProductsController.CreateAPIproductCreation") CreateAPIproductCreation

> APIproduct Creation


```csharp
Task CreateAPIproductCreation(
        string body,
        string authorization,
        string contentType,
        string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string body = "Body";
string authorization = "Authorization";
string contentType = "Content-Type";
string oRG = "ORG";

await products.CreateAPIproductCreation(body, authorization, contentType, oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="target_servers_controller"></a>![Class: ](https://apidocs.io/img/class.png "ApigeeEdgeAPIManagement.Tests.Controllers.TargetServersController") TargetServersController

### Get singleton instance

The singleton instance of the ``` TargetServersController ``` class can be accessed from the API Client.

```csharp
TargetServersController targetServers = client.TargetServers;
```

### <a name="list_target_servers"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.TargetServersController.ListTargetServers") ListTargetServers

> List Target Servers


```csharp
Task ListTargetServers(string authorization, string oRG, string eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Authorization";
string oRG = "ORG";
string eNV = "ENV";

await targetServers.ListTargetServers(authorization, oRG, eNV);

```


### <a name="add_target"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.TargetServersController.AddTarget") AddTarget

> Add Target


```csharp
Task AddTarget(
        PCL.Models.AddTargetRequest body,
        string contentType,
        string authorization,
        string oRG,
        string eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var body = new PCL.Models.AddTargetRequest();
string contentType = "content-type";
string authorization = "Authorization";
string oRG = "ORG";
string eNV = "ENV";

await targetServers.AddTarget(body, contentType, authorization, oRG, eNV);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="company_controller"></a>![Class: ](https://apidocs.io/img/class.png "ApigeeEdgeAPIManagement.Tests.Controllers.CompanyController") CompanyController

### Get singleton instance

The singleton instance of the ``` CompanyController ``` class can be accessed from the API Client.

```csharp
CompanyController company = client.Company;
```

### <a name="create_company"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.CompanyController.CreateCompany") CreateCompany

> Create Company


```csharp
Task CreateCompany(
        string body,
        string authorization,
        string contentType,
        string oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string body = "Body";
string authorization = "Authorization";
string contentType = "Content-Type";
string oRG = "ORG";

await company.CreateCompany(body, authorization, contentType, oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="organizations_controller"></a>![Class: ](https://apidocs.io/img/class.png "ApigeeEdgeAPIManagement.Tests.Controllers.OrganizationsController") OrganizationsController

### Get singleton instance

The singleton instance of the ``` OrganizationsController ``` class can be accessed from the API Client.

```csharp
OrganizationsController organizations = client.Organizations;
```

### <a name="list_organizations"></a>![Method: ](https://apidocs.io/img/method.png "ApigeeEdgeAPIManagement.Tests.Controllers.OrganizationsController.ListOrganizations") ListOrganizations

> List organizations


```csharp
Task ListOrganizations(string authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string authorization = "Basic {{BASICAUTH}}";

await organizations.ListOrganizations(authorization);

```


[Back to List of Controllers](#list_of_controllers)




# Getting started

TODO: Add Description

## How to Build


The generated code has dependencies over external libraries like UniRest. These dependencies are defined in the ```PodFile``` file that comes with the SDK. 
To resolve these dependencies, we use the Cocoapods package manager.
Visit https://guides.cocoapods.org/using/getting-started.html to setup Cocoapods on your system.
Open command prompt and type ```pod --version```. This should display the current version of Cocoapods installed if the installation was successful.

Using command line, navigate to the directory containing the generated files (including ```PodFile```) for the SDK. 
Run the command ```pod install```. This should install all the required dependencies and create the ```pods``` directory in your project directory.

![Installing dependencies using Cocoapods](https://apidocs.io/illustration/objc?step=AddDependencies&workspaceFolder=Apigee%20Edge%20API%20Management-ObjC&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagement&rootNamespace=ApigeeEdgeAPIManagement)

Open the project workspace using the (ApigeeEdgeAPIManagement.xcworkspace) file. Invoke the build process using `Command(⌘)+B` shortcut key or using the `Build` menu as shown below.

![Building SDK using Xcode](https://apidocs.io/illustration/objc?step=BuildSDK&workspaceFolder=Apigee%20Edge%20API%20Management-ObjC&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagement&rootNamespace=ApigeeEdgeAPIManagement)


## How to Use

The generated code is a Cocoa Touch Static Library which can be used in any iOS project. The support for these generated libraries go all the way back to iOS 6.

The following section explains how to use the ApigeeEdgeAPIManagement library in a new iOS project.     
### 1. Starting a new project
To start a new project, left-click on the ```Create a new Xcode project```.
![Create Test Project - Step 1](https://apidocs.io/illustration/objc?step=Test1&workspaceFolder=Apigee%20Edge%20API%20Management-ObjC&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagement&rootNamespace=ApigeeEdgeAPIManagement)

Next, choose **Single View Application** and click ```Next```.
![Create Test Project - Step 2](https://apidocs.io/illustration/objc?step=Test2&workspaceFolder=Apigee%20Edge%20API%20Management-ObjC&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagement&rootNamespace=ApigeeEdgeAPIManagement)

Provide **Test-Project** as the product name click ```Next```.
![Create Test Project - Step 3](https://apidocs.io/illustration/objc?step=Test3&workspaceFolder=Apigee%20Edge%20API%20Management-ObjC&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagement&rootNamespace=ApigeeEdgeAPIManagement)

Choose the desired location of your project folder and click ```Create```.
![Create Test Project - Step 4](https://apidocs.io/illustration/objc?step=Test4&workspaceFolder=Apigee%20Edge%20API%20Management-ObjC&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagement&rootNamespace=ApigeeEdgeAPIManagement)

### 2. Adding the static library dependency
To add this dependency open a terminal and navigate to your project folder. Next, input ```pod init``` and press enter.
![Add dependency - Step 1](https://apidocs.io/illustration/objc?step=Add0&workspaceFolder=Apigee%20Edge%20API%20Management-ObjC&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagement&rootNamespace=ApigeeEdgeAPIManagement)

Next, open the newly created ```PodFile``` in your favourite text editor. Add the following line : pod 'ApigeeEdgeAPIManagement', :path => 'Vendor/ApigeeEdgeAPIManagement'
![Add dependency - Step 2](https://apidocs.io/illustration/objc?step=Add1&workspaceFolder=Apigee%20Edge%20API%20Management-ObjC&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagement&rootNamespace=ApigeeEdgeAPIManagement)

Execute `pod install` from terminal to install the dependecy in your project. This would add the dependency to the newly created test project.
![Add dependency - Step 3](https://apidocs.io/illustration/objc?step=Add2&workspaceFolder=Apigee%20Edge%20API%20Management-ObjC&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagement&rootNamespace=ApigeeEdgeAPIManagement)


## How to Test

Unit tests in this SDK can be run using Xcode. 

First build the SDK as shown in the steps above and naivgate to the project directory and open the ApigeeEdgeAPIManagement.xcworkspace file.

Go to the test explorer in Xcode as shown in the picture below and click on `run tests` from the menu. 
![Run tests](https://apidocs.io/illustration/objc?step=RunTests&workspaceFolder=Apigee%20Edge%20API%20Management-ObjC&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagement&rootNamespace=ApigeeEdgeAPIManagement)


## Initialization

### Authentication
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| basicAuthUserName | The username to use with basic authentication |
| basicAuthPassword | The password to use with basic authentication |



Configuration variables can be set as following.
```Objc
// Configuration parameters and credentials
Configuration_BasicAuthUserName = "Configuration_BasicAuthUserName"; // The username to use with basic authentication
Configuration_BasicAuthPassword = "Configuration_BasicAuthPassword"; // The password to use with basic authentication

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

## <a name="deployments_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DeploymentsController") DeploymentsController

### Get singleton instance
```objc
Deployments* deployments = [[Deployments alloc]init] ;
```

### <a name="list_deployments_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".DeploymentsController.listDeploymentsAsyncWithAuthorization") listDeploymentsAsyncWithAuthorization

> List Deployments


```objc
function listDeploymentsAsyncWithAuthorization:(NSString*) authorization
                oRG:(NSString*) oRG
                completionBlock:(CompletedGetListDeployments) onCompleted(authorization oRG : oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* oRG = @"ORG";

    [self.deployments listDeploymentsAsyncWithAuthorization: authorization oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_deployments_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".DeploymentsController.getDeploymentsAsyncWithAuthorization") getDeploymentsAsyncWithAuthorization

> Deployments


```objc
function getDeploymentsAsyncWithAuthorization:(NSString*) authorization
                oRG:(NSString*) oRG
                completionBlock:(CompletedGetDeployments) onCompleted(authorization oRG : oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* oRG = @"ORG";

    [self.deployments getDeploymentsAsyncWithAuthorization: authorization oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="user_roles_controller"></a>![Class: ](https://apidocs.io/img/class.png ".UserRolesController") UserRolesController

### Get singleton instance
```objc
UserRoles* userRoles = [[UserRoles alloc]init] ;
```

### <a name="create_user_roles_update_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".UserRolesController.createUserRolesUpdateAsyncWithBody") createUserRolesUpdateAsyncWithBody

> User Roles Update


```objc
function createUserRolesUpdateAsyncWithBody:(UserRolesUpdateRequest*) body
                authorization:(NSString*) authorization
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostUserRolesUpdate) onCompleted(body authorization : authorization contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    UserRolesUpdateRequest* body = (UserRolesUpdateRequest*) [APIHelper jsonDeserialize: @"{ \"role\" : [ { \"name\" : \"orgadmin\", \"organization\" : \"dev\" }, { \"name\" : \"sysadmin\" } ] }"
                toClass: UserRolesUpdateRequest.class];
    NSString* authorization = @"Basic {{BASICAUTH}}";
    NSString* contentType = @"application/json";

    [self.userRoles createUserRolesUpdateAsyncWithBody: body authorization : authorization contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="delete_an_organization_userrole_async_with_org"></a>![Method: ](https://apidocs.io/img/method.png ".UserRolesController.deleteAnOrganizationUserroleAsyncWithOrg") deleteAnOrganizationUserroleAsyncWithOrg

> Delete an organization userrole


```objc
function deleteAnOrganizationUserroleAsyncWithOrg:(NSString*) org
                authorization:(NSString*) authorization
                accept:(NSString*) accept
                completionBlock:(CompletedDeleteAnOrganizationUserrole) onCompleted(org authorization : authorization accept : accept)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| org |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* org = @"{{ORG}}";
    NSString* authorization = @"Basic {{BASICAUTH}}";
    NSString* accept = @"application/json";

    [self.userRoles deleteAnOrganizationUserroleAsyncWithOrg: org authorization : authorization accept : accept  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_permissions_for_a_role_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".UserRolesController.getPermissionsForARoleAsyncWithAuthorization") getPermissionsForARoleAsyncWithAuthorization

> Get permissions for a role


```objc
function getPermissionsForARoleAsyncWithAuthorization:(NSString*) authorization
                contentType:(NSString*) contentType
                oRG:(NSString*) oRG
                completionBlock:(CompletedGetPermissionsForARole) onCompleted(authorization contentType : contentType oRG : oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* contentType = @"Content-Type";
    NSString* oRG = @"ORG";

    [self.userRoles getPermissionsForARoleAsyncWithAuthorization: authorization contentType : contentType oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="o_auth_controller"></a>![Class: ](https://apidocs.io/img/class.png ".OAuthController") OAuthController

### Get singleton instance
```objc
OAuth* oAuth = [[OAuth alloc]init] ;
```

### <a name="get_o_auth2_token_details_get_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".OAuthController.getOAuth2TokenDetailsGetAsyncWithAuthorization") getOAuth2TokenDetailsGetAsyncWithAuthorization

> OAuth2 Token Details Get


```objc
function getOAuth2TokenDetailsGetAsyncWithAuthorization:(NSString*) authorization
                contentType:(NSString*) contentType
                oRG:(NSString*) oRG
                completionBlock:(CompletedGetOAuth2TokenDetailsGet) onCompleted(authorization contentType : contentType oRG : oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* contentType = @"Content-Type";
    NSString* oRG = @"ORG";

    [self.oAuth getOAuth2TokenDetailsGetAsyncWithAuthorization: authorization contentType : contentType oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="kvm_controller"></a>![Class: ](https://apidocs.io/img/class.png ".KVMController") KVMController

### Get singleton instance
```objc
KVM* kVM = [[KVM alloc]init] ;
```

### <a name="get_kvm_get_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".KVMController.getKVMGetAsyncWithAuthorization") getKVMGetAsyncWithAuthorization

> KVM Get


```objc
function getKVMGetAsyncWithAuthorization:(NSString*) authorization
                contentType:(NSString*) contentType
                oRG:(NSString*) oRG
                eNV:(NSString*) eNV
                completionBlock:(CompletedGetKVMGet) onCompleted(authorization contentType : contentType oRG : oRG eNV : eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* contentType = @"Content-Type";
    NSString* oRG = @"ORG";
    NSString* eNV = @"ENV";

    [self.kVM getKVMGetAsyncWithAuthorization: authorization contentType : contentType oRG : oRG eNV : eNV  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="delete_kvm_delete_entire_kvm_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".KVMController.deleteKVMDeleteEntireKVMAsyncWithAuthorization") deleteKVMDeleteEntireKVMAsyncWithAuthorization

> KVM Delete (Entire KVM)


```objc
function deleteKVMDeleteEntireKVMAsyncWithAuthorization:(NSString*) authorization
                contentType:(NSString*) contentType
                oRG:(NSString*) oRG
                eNV:(NSString*) eNV
                completionBlock:(CompletedDeleteKVMDeleteEntireKVM) onCompleted(authorization contentType : contentType oRG : oRG eNV : eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* contentType = @"Content-Type";
    NSString* oRG = @"ORG";
    NSString* eNV = @"ENV";

    [self.kVM deleteKVMDeleteEntireKVMAsyncWithAuthorization: authorization contentType : contentType oRG : oRG eNV : eNV  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="pods_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PodsController") PodsController

### Get singleton instance
```objc
Pods* pods = [[Pods alloc]init] ;
```

### <a name="get_analytics_pod_async_with_pod"></a>![Method: ](https://apidocs.io/img/method.png ".PodsController.getAnalyticsPodAsyncWithPod") getAnalyticsPodAsyncWithPod

> Analytics pod


```objc
function getAnalyticsPodAsyncWithPod:(NSString*) pod
                authorization:(NSString*) authorization
                completionBlock:(CompletedGetAnalyticsPod) onCompleted(pod authorization : authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| pod |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* pod = @"analytics";
    NSString* authorization = @"Basic {{BASICAUTH}}";

    [self.pods getAnalyticsPodAsyncWithPod: pod authorization : authorization  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_associated_pods_async_with_content_type"></a>![Method: ](https://apidocs.io/img/method.png ".PodsController.getAssociatedPodsAsyncWithContentType") getAssociatedPodsAsyncWithContentType

> Get Associated  Pods


```objc
function getAssociatedPodsAsyncWithContentType:(NSString*) contentType
                authorization:(NSString*) authorization
                oRG:(NSString*) oRG
                completionBlock:(CompletedGetAssociatedPods) onCompleted(contentType authorization : authorization oRG : oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* contentType = @"Content-Type";
    NSString* authorization = @"Authorization";
    NSString* oRG = @"ORG";

    [self.pods getAssociatedPodsAsyncWithContentType: contentType authorization : authorization oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_disassociate_org_from_pod_async_with_content_type"></a>![Method: ](https://apidocs.io/img/method.png ".PodsController.createDisassociateOrgFromPODAsyncWithContentType") createDisassociateOrgFromPODAsyncWithContentType

> Disassociate Org from POD


```objc
function createDisassociateOrgFromPODAsyncWithContentType:(NSString*) contentType
                authorization:(NSString*) authorization
                oRG:(NSString*) oRG
                completionBlock:(CompletedPostDisassociateOrgFromPOD) onCompleted(contentType authorization : authorization oRG : oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* contentType = @"Content-Type";
    NSString* authorization = @"Authorization";
    NSString* oRG = @"ORG";

    [self.pods createDisassociateOrgFromPODAsyncWithContentType: contentType authorization : authorization oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="servers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ServersController") ServersController

### Get singleton instance
```objc
Servers* servers = [[Servers alloc]init] ;
```

### <a name="create_deregister_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.createDeregisterAsyncWithAuthorization") createDeregisterAsyncWithAuthorization

> Deregister


```objc
function createDeregisterAsyncWithAuthorization:(NSString*) authorization
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostDeregister) onCompleted(authorization contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Basic {{BASICAUTH}}";
    NSString* contentType = @"application/x-www-form-urlencoded";

    [self.servers createDeregisterAsyncWithAuthorization: authorization contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="list_server_by_uuid_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.listServerByUUIDAsyncWithAuthorization") listServerByUUIDAsyncWithAuthorization

> List Server by UUID


```objc
function listServerByUUIDAsyncWithAuthorization:(NSString*) authorization
                uuid:(NSString*) uuid
                completionBlock:(CompletedGetListServerByUUID) onCompleted(authorization uuid : uuid)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| uuid |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Basic {{BASICAUTH}}";
    NSString* uuid = @"uuid";

    [self.servers listServerByUUIDAsyncWithAuthorization: authorization uuid : uuid  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_set_not_reachable_async_with_reachable"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.createSetNotReachableAsyncWithReachable") createSetNotReachableAsyncWithReachable

> Set not reachable


```objc
function createSetNotReachableAsyncWithReachable:(NSString*) reachable
                authorization:(NSString*) authorization
                completionBlock:(CompletedPostSetNotReachable) onCompleted(reachable authorization : authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| reachable |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* reachable = @"false";
    NSString* authorization = @"Basic {{BASICAUTH}}";

    [self.servers createSetNotReachableAsyncWithReachable: reachable authorization : authorization  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="list_org_env_servers_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.listOrgEnvServersAsyncWithAuthorization") listOrgEnvServersAsyncWithAuthorization

> List org/env servers


```objc
function listOrgEnvServersAsyncWithAuthorization:(NSString*) authorization
                oRG:(NSString*) oRG
                eNV:(NSString*) eNV
                completionBlock:(CompletedGetListOrgEnvServers) onCompleted(authorization oRG : oRG eNV : eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* oRG = @"ORG";
    NSString* eNV = @"ENV";

    [self.servers listOrgEnvServersAsyncWithAuthorization: authorization oRG : oRG eNV : eNV  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_register_server_with_org_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.createRegisterServerWithOrgAsyncWithAuthorization") createRegisterServerWithOrgAsyncWithAuthorization

> Register server with org


```objc
function createRegisterServerWithOrgAsyncWithAuthorization:(NSString*) authorization
                contentType:(NSString*) contentType
                oRG:(NSString*) oRG
                eNV:(NSString*) eNV
                completionBlock:(CompletedPostRegisterServerWithOrg) onCompleted(authorization contentType : contentType oRG : oRG eNV : eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* contentType = @"Content-Type";
    NSString* oRG = @"ORG";
    NSString* eNV = @"ENV";

    [self.servers createRegisterServerWithOrgAsyncWithAuthorization: authorization contentType : contentType oRG : oRG eNV : eNV  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_associate_environments_to_mp_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.createAssociateEnvironmentsToMPAsyncWithAuthorization") createAssociateEnvironmentsToMPAsyncWithAuthorization

> Associate  environments to MP


```objc
function createAssociateEnvironmentsToMPAsyncWithAuthorization:(NSString*) authorization
                contentType:(NSString*) contentType
                oRG:(NSString*) oRG
                eNV:(NSString*) eNV
                completionBlock:(CompletedPostAssociateEnvironmentsToMP) onCompleted(authorization contentType : contentType oRG : oRG eNV : eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* contentType = @"Content-Type";
    NSString* oRG = @"ORG";
    NSString* eNV = @"ENV";

    [self.servers createAssociateEnvironmentsToMPAsyncWithAuthorization: authorization contentType : contentType oRG : oRG eNV : eNV  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="developers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DevelopersController") DevelopersController

### Get singleton instance
```objc
Developers* developers = [[Developers alloc]init] ;
```

### <a name="get_developers_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".DevelopersController.getDevelopersAsyncWithAuthorization") getDevelopersAsyncWithAuthorization

> Get Developers


```objc
function getDevelopersAsyncWithAuthorization:(NSString*) authorization
                contentType:(NSString*) contentType
                oRG:(NSString*) oRG
                completionBlock:(CompletedGetDevelopers) onCompleted(authorization contentType : contentType oRG : oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* contentType = @"Content-Type";
    NSString* oRG = @"ORG";

    [self.developers getDevelopersAsyncWithAuthorization: authorization contentType : contentType oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_developer_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".DevelopersController.createDeveloperAsyncWithBody") createDeveloperAsyncWithBody

> Create Developer


```objc
function createDeveloperAsyncWithBody:(NSString*) body
                authorization:(NSString*) authorization
                contentType:(NSString*) contentType
                oRG:(NSString*) oRG
                completionBlock:(CompletedPostCreateDeveloper) onCompleted(body authorization : authorization contentType : contentType oRG : oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* body = @"Body";
    NSString* authorization = @"Authorization";
    NSString* contentType = @"Content-Type";
    NSString* oRG = @"ORG";

    [self.developers createDeveloperAsyncWithBody: body authorization : authorization contentType : contentType oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="ap_is_controller"></a>![Class: ](https://apidocs.io/img/class.png ".APIsController") APIsController

### Get singleton instance
```objc
APIs* aPIs = [[APIs alloc]init] ;
```

### <a name="get_api_list_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.getApiListAsyncWithAuthorization") getApiListAsyncWithAuthorization

> Api list


```objc
function getApiListAsyncWithAuthorization:(NSString*) authorization
                oRG:(NSString*) oRG
                completionBlock:(CompletedGetApiList) onCompleted(authorization oRG : oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* oRG = @"ORG";

    [self.aPIs getApiListAsyncWithAuthorization: authorization oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_deploy_api_async_with_action"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.createDeployAPIAsyncWithAction") createDeployAPIAsyncWithAction

> Deploy API


```objc
function createDeployAPIAsyncWithAction:(NSString*) action
                name:(NSString*) name
                authorization:(NSString*) authorization
                contentType:(NSString*) contentType
                oRG:(NSString*) oRG
                completionBlock:(CompletedPostDeployAPI) onCompleted(action name : name authorization : authorization contentType : contentType oRG : oRG)
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

```objc
    // Parameters for the API call
    NSString* action = @"action";
    NSString* name = @"name";
    NSString* authorization = @"Authorization";
    NSString* contentType = @"Content-Type";
    NSString* oRG = @"ORG";

    [self.aPIs createDeployAPIAsyncWithAction: action name : name authorization : authorization contentType : contentType oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="delete_an_api_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.deleteAnAPIAsyncWithAuthorization") deleteAnAPIAsyncWithAuthorization

> Delete an API


```objc
function deleteAnAPIAsyncWithAuthorization:(NSString*) authorization
                oRG:(NSString*) oRG
                completionBlock:(CompletedDeleteAnAPI) onCompleted(authorization oRG : oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* oRG = @"ORG";

    [self.aPIs deleteAnAPIAsyncWithAuthorization: authorization oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_undeploy_revisions_async_with_action"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.createUndeployRevisionsAsyncWithAction") createUndeployRevisionsAsyncWithAction

> Undeploy Revisions


```objc
function createUndeployRevisionsAsyncWithAction:(NSString*) action
                env:(NSString*) env
                authorization:(NSString*) authorization
                contentType:(NSString*) contentType
                oRG:(NSString*) oRG
                completionBlock:(CompletedPostUndeployRevisions) onCompleted(action env : env authorization : authorization contentType : contentType oRG : oRG)
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

```objc
    // Parameters for the API call
    NSString* action = @"action";
    NSString* env = @"env";
    NSString* authorization = @"Authorization";
    NSString* contentType = @"Content-Type";
    NSString* oRG = @"ORG";

    [self.aPIs createUndeployRevisionsAsyncWithAction: action env : env authorization : authorization contentType : contentType oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="cache_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CacheController") CacheController

### Get singleton instance
```objc
Cache* cache = [[Cache alloc]init] ;
```

### <a name="list_caches_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".CacheController.listCachesAsyncWithAuthorization") listCachesAsyncWithAuthorization

> List caches


```objc
function listCachesAsyncWithAuthorization:(NSString*) authorization
                oRG:(NSString*) oRG
                eNV:(NSString*) eNV
                completionBlock:(CompletedGetListCaches) onCompleted(authorization oRG : oRG eNV : eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* oRG = @"ORG";
    NSString* eNV = @"ENV";

    [self.cache listCachesAsyncWithAuthorization: authorization oRG : oRG eNV : eNV  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="audit_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AuditController") AuditController

### Get singleton instance
```objc
Audit* audit = [[Audit alloc]init] ;
```

### <a name="get_audit_async_with_expand"></a>![Method: ](https://apidocs.io/img/method.png ".AuditController.getAuditAsyncWithExpand") getAuditAsyncWithExpand

> Audit


```objc
function getAuditAsyncWithExpand:(BOOL) expand
                timeline:(NSString*) timeline
                authorization:(NSString*) authorization
                oRG:(NSString*) oRG
                completionBlock:(CompletedGetAudit) onCompleted(expand timeline : timeline authorization : authorization oRG : oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| expand |  ``` Required ```  | TODO: Add a parameter description |
| timeline |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    BOOL expand = false;
    NSString* timeline = @"timeline";
    NSString* authorization = @"Authorization";
    NSString* oRG = @"ORG";

    [self.audit getAuditAsyncWithExpand: expand timeline : timeline authorization : authorization oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="users_controller"></a>![Class: ](https://apidocs.io/img/class.png ".UsersController") UsersController

### Get singleton instance
```objc
Users* users = [[Users alloc]init] ;
```

### <a name="get_developer_details_get_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.getDeveloperDetailsGetAsyncWithAuthorization") getDeveloperDetailsGetAsyncWithAuthorization

> Developer Details Get


```objc
function getDeveloperDetailsGetAsyncWithAuthorization:(NSString*) authorization
                contentType:(NSString*) contentType
                oRG:(NSString*) oRG
                completionBlock:(CompletedGetDeveloperDetailsGet) onCompleted(authorization contentType : contentType oRG : oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* contentType = @"Content-Type";
    NSString* oRG = @"ORG";

    [self.users getDeveloperDetailsGetAsyncWithAuthorization: authorization contentType : contentType oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_user_in_org_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.createUserInORGAsyncWithBody") createUserInORGAsyncWithBody

> Create User in ORG


```objc
function createUserInORGAsyncWithBody:(NSString*) body
                authorization:(NSString*) authorization
                contentType:(NSString*) contentType
                oRG:(NSString*) oRG
                completionBlock:(CompletedPostCreateUserInORG) onCompleted(body authorization : authorization contentType : contentType oRG : oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* body = @"Body";
    NSString* authorization = @"Authorization";
    NSString* contentType = @"Content-Type";
    NSString* oRG = @"ORG";

    [self.users createUserInORGAsyncWithBody: body authorization : authorization contentType : contentType oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="list_users_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.listUsersAsyncWithAuthorization") listUsersAsyncWithAuthorization

> List Users


```objc
function listUsersAsyncWithAuthorization:(NSString*) authorization
                completionBlock:(CompletedGetListUsers) onCompleted(authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Basic {{BASICAUTH}}";

    [self.users listUsersAsyncWithAuthorization: authorization  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="add_user_as_orgadmin_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.addUserAsOrgadminAsyncWithBody") addUserAsOrgadminAsyncWithBody

> Add user as Orgadmin


```objc
function addUserAsOrgadminAsyncWithBody:(NSString*) body
                authorization:(NSString*) authorization
                contentType:(NSString*) contentType
                oRG:(NSString*) oRG
                completionBlock:(CompletedPostAddUserAsOrgadmin) onCompleted(body authorization : authorization contentType : contentType oRG : oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* body = @"Body";
    NSString* authorization = @"Authorization";
    NSString* contentType = @"Content-Type";
    NSString* oRG = @"ORG";

    [self.users addUserAsOrgadminAsyncWithBody: body authorization : authorization contentType : contentType oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="zzz_others_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ZzzOthersController") ZzzOthersController

### Get singleton instance
```objc
ZzzOthers* zzzOthers = [[ZzzOthers alloc]init] ;
```

### <a name="get_cluster_status_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.getClusterStatusAsyncWithAuthorization") getClusterStatusAsyncWithAuthorization

> Cluster Status


```objc
function getClusterStatusAsyncWithAuthorization:(NSString*) authorization
                completionBlock:(CompletedGetClusterStatus) onCompleted(authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Basic {{BASICAUTH}}";

    [self.zzzOthers getClusterStatusAsyncWithAuthorization: authorization  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_enable_debug_wo_restart_async_with_session"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.createEnableDebugWORestartAsyncWithSession") createEnableDebugWORestartAsyncWithSession

> Enable Debug w/o Restart 


```objc
function createEnableDebugWORestartAsyncWithSession:(NSString*) session
                authorization:(NSString*) authorization
                contentType:(NSString*) contentType
                completionBlock:(CompletedPostEnableDebugWORestart) onCompleted(session authorization : authorization contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| session |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* session = @"logsession_name";
    NSString* authorization = @"Basic {{BASICAUTH}}";
    NSString* contentType = @"application/x-www-form-urlencoded";

    [self.zzzOthers createEnableDebugWORestartAsyncWithSession: session authorization : authorization contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_classifications_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.getClassificationsAsyncWithAuthorization") getClassificationsAsyncWithAuthorization

> Classifications


```objc
function getClassificationsAsyncWithAuthorization:(NSString*) authorization
                hOST:(NSString*) hOST
                completionBlock:(CompletedGetClassifications) onCompleted(authorization hOST : hOST)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* hOST = @"HOST";

    [self.zzzOthers getClassificationsAsyncWithAuthorization: authorization hOST : hOST  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_company_developer_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.createCompanyDeveloperAsyncWithBody") createCompanyDeveloperAsyncWithBody

> Create Company Developer


```objc
function createCompanyDeveloperAsyncWithBody:(CreateCompanyDeveloperRequest*) body
                contentType:(NSString*) contentType
                authorization:(NSString*) authorization
                oRG:(NSString*) oRG
                cOMPANY:(NSString*) cOMPANY
                completionBlock:(CompletedPostCreateCompanyDeveloper) onCompleted(body contentType : contentType authorization : authorization oRG : oRG cOMPANY : cOMPANY)
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

```objc
    // Parameters for the API call
    CreateCompanyDeveloperRequest* body = [[CreateCompanyDeveloperRequest alloc]init];
    NSString* contentType = @"Content-Type";
    NSString* authorization = @"Authorization";
    NSString* oRG = @"ORG";
    NSString* cOMPANY = @"COMPANY";

    [self.zzzOthers createCompanyDeveloperAsyncWithBody: body contentType : contentType authorization : authorization oRG : oRG cOMPANY : cOMPANY  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_qpid_metrics_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.getQPIDMetricsAsyncWithAuthorization") getQPIDMetricsAsyncWithAuthorization

> QPID Metrics


```objc
function getQPIDMetricsAsyncWithAuthorization:(NSString*) authorization
                hOST:(NSString*) hOST
                completionBlock:(CompletedGetQPIDMetrics) onCompleted(authorization hOST : hOST)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* hOST = @"HOST";

    [self.zzzOthers getQPIDMetricsAsyncWithAuthorization: authorization hOST : hOST  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_build_info_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.getBuildInfoAsyncWithAuthorization") getBuildInfoAsyncWithAuthorization

> Build Info


```objc
function getBuildInfoAsyncWithAuthorization:(NSString*) authorization
                hOST:(NSString*) hOST
                pORT:(NSString*) pORT
                completionBlock:(CompletedGetBuildInfo) onCompleted(authorization hOST : hOST pORT : pORT)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |
| pORT |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* hOST = @"HOST";
    NSString* pORT = @"PORT";

    [self.zzzOthers getBuildInfoAsyncWithAuthorization: authorization hOST : hOST pORT : pORT  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="delete_disable_debug_wo_restart_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.deleteDisableDebugWORestartAsyncWithAuthorization") deleteDisableDebugWORestartAsyncWithAuthorization

> Disable Debug w/o Restart


```objc
function deleteDisableDebugWORestartAsyncWithAuthorization:(NSString*) authorization
                contentType:(NSString*) contentType
                completionBlock:(CompletedDeleteDisableDebugWORestart) onCompleted(authorization contentType : contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Basic {{BASICAUTH}}";
    NSString* contentType = @"application/x-www-form-urlencoded";

    [self.zzzOthers deleteDisableDebugWORestartAsyncWithAuthorization: authorization contentType : contentType  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="apps_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AppsController") AppsController

### Get singleton instance
```objc
Apps* apps = [[Apps alloc]init] ;
```

### <a name="create_company_app_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.createCompanyAPPAsyncWithBody") createCompanyAPPAsyncWithBody

> Create Company APP


```objc
function createCompanyAPPAsyncWithBody:(NSString*) body
                authorization:(NSString*) authorization
                contentType:(NSString*) contentType
                oRG:(NSString*) oRG
                cOMPANY:(NSString*) cOMPANY
                completionBlock:(CompletedPostCreateCompanyAPP) onCompleted(body authorization : authorization contentType : contentType oRG : oRG cOMPANY : cOMPANY)
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

```objc
    // Parameters for the API call
    NSString* body = @"Body";
    NSString* authorization = @"Authorization";
    NSString* contentType = @"Content-Type";
    NSString* oRG = @"ORG";
    NSString* cOMPANY = @"COMPANY";

    [self.apps createCompanyAPPAsyncWithBody: body authorization : authorization contentType : contentType oRG : oRG cOMPANY : cOMPANY  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="add_app_credentials_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.addAppCredentialsAsyncWithBody") addAppCredentialsAsyncWithBody

> Add app credentials


```objc
function addAppCredentialsAsyncWithBody:(NSString*) body
                authorization:(NSString*) authorization
                contentType:(NSString*) contentType
                oRG:(NSString*) oRG
                completionBlock:(CompletedPostAddAppCredentials) onCompleted(body authorization : authorization contentType : contentType oRG : oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* body = @"Body";
    NSString* authorization = @"Authorization";
    NSString* contentType = @"Content-Type";
    NSString* oRG = @"ORG";

    [self.apps addAppCredentialsAsyncWithBody: body authorization : authorization contentType : contentType oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="list_apps_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.listAppsAsyncWithAuthorization") listAppsAsyncWithAuthorization

> List apps 


```objc
function listAppsAsyncWithAuthorization:(NSString*) authorization
                oRG:(NSString*) oRG
                completionBlock:(CompletedGetListApps) onCompleted(authorization oRG : oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* oRG = @"ORG";

    [self.apps listAppsAsyncWithAuthorization: authorization oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="list_app_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.listAppAsyncWithAuthorization") listAppAsyncWithAuthorization

> List app


```objc
function listAppAsyncWithAuthorization:(NSString*) authorization
                oRG:(NSString*) oRG
                completionBlock:(CompletedGetListApp) onCompleted(authorization oRG : oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* oRG = @"ORG";

    [self.apps listAppAsyncWithAuthorization: authorization oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="virtual_hosts_controller"></a>![Class: ](https://apidocs.io/img/class.png ".VirtualHostsController") VirtualHostsController

### Get singleton instance
```objc
VirtualHosts* virtualHosts = [[VirtualHosts alloc]init] ;
```

### <a name="list_virtual_hosts_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".VirtualHostsController.listVirtualHostsAsyncWithAuthorization") listVirtualHostsAsyncWithAuthorization

> List VirtualHosts


```objc
function listVirtualHostsAsyncWithAuthorization:(NSString*) authorization
                oRG:(NSString*) oRG
                eNV:(NSString*) eNV
                completionBlock:(CompletedGetListVirtualHosts) onCompleted(authorization oRG : oRG eNV : eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* oRG = @"ORG";
    NSString* eNV = @"ENV";

    [self.virtualHosts listVirtualHostsAsyncWithAuthorization: authorization oRG : oRG eNV : eNV  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="add_virtual_host_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".VirtualHostsController.addVirtualHostAsyncWithBody") addVirtualHostAsyncWithBody

> Add Virtual Host


```objc
function addVirtualHostAsyncWithBody:(NSString*) body
                authorization:(NSString*) authorization
                contentType:(NSString*) contentType
                oRG:(NSString*) oRG
                eNV:(NSString*) eNV
                completionBlock:(CompletedPostAddVirtualHost) onCompleted(body authorization : authorization contentType : contentType oRG : oRG eNV : eNV)
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

```objc
    // Parameters for the API call
    NSString* body = @"Body";
    NSString* authorization = @"Authorization";
    NSString* contentType = @"Content-Type";
    NSString* oRG = @"ORG";
    NSString* eNV = @"ENV";

    [self.virtualHosts addVirtualHostAsyncWithBody: body authorization : authorization contentType : contentType oRG : oRG eNV : eNV  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="environments_controller"></a>![Class: ](https://apidocs.io/img/class.png ".EnvironmentsController") EnvironmentsController

### Get singleton instance
```objc
Environments* environments = [[Environments alloc]init] ;
```

### <a name="update_environments_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".EnvironmentsController.updateEnvironmentsAsyncWithAuthorization") updateEnvironmentsAsyncWithAuthorization

> Update Environments


```objc
function updateEnvironmentsAsyncWithAuthorization:(NSString*) authorization
                contentType:(NSString*) contentType
                oRG:(NSString*) oRG
                eNV:(NSString*) eNV
                completionBlock:(CompletedPostUpdateEnvironments) onCompleted(authorization contentType : contentType oRG : oRG eNV : eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* contentType = @"Content-Type";
    NSString* oRG = @"ORG";
    NSString* eNV = @"ENV";

    [self.environments updateEnvironmentsAsyncWithAuthorization: authorization contentType : contentType oRG : oRG eNV : eNV  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="delete_environment_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".EnvironmentsController.deleteEnvironmentAsyncWithAuthorization") deleteEnvironmentAsyncWithAuthorization

> Delete Environment


```objc
function deleteEnvironmentAsyncWithAuthorization:(NSString*) authorization
                oRG:(NSString*) oRG
                eNV:(NSString*) eNV
                completionBlock:(CompletedDeleteEnvironment) onCompleted(authorization oRG : oRG eNV : eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* oRG = @"ORG";
    NSString* eNV = @"ENV";

    [self.environments deleteEnvironmentAsyncWithAuthorization: authorization oRG : oRG eNV : eNV  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_new_env_in_org_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".EnvironmentsController.createNewENVInORGAsyncWithBody") createNewENVInORGAsyncWithBody

> Create New ENV in ORG


```objc
function createNewENVInORGAsyncWithBody:(NSString*) body
                authorization:(NSString*) authorization
                contentType:(NSString*) contentType
                oRG:(NSString*) oRG
                completionBlock:(CompletedPostCreateNewENVInORG) onCompleted(body authorization : authorization contentType : contentType oRG : oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* body = @"Body";
    NSString* authorization = @"Authorization";
    NSString* contentType = @"Content-Type";
    NSString* oRG = @"ORG";

    [self.environments createNewENVInORGAsyncWithBody: body authorization : authorization contentType : contentType oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="developer_app_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DeveloperAppController") DeveloperAppController

### Get singleton instance
```objc
DeveloperApp* developerApp = [[DeveloperApp alloc]init] ;
```

### <a name="get_developer_app_details_get_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".DeveloperAppController.getDeveloperAppDetailsGetAsyncWithAuthorization") getDeveloperAppDetailsGetAsyncWithAuthorization

> Developer App Details Get


```objc
function getDeveloperAppDetailsGetAsyncWithAuthorization:(NSString*) authorization
                contentType:(NSString*) contentType
                oRG:(NSString*) oRG
                completionBlock:(CompletedGetDeveloperAppDetailsGet) onCompleted(authorization contentType : contentType oRG : oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* contentType = @"Content-Type";
    NSString* oRG = @"ORG";

    [self.developerApp getDeveloperAppDetailsGetAsyncWithAuthorization: authorization contentType : contentType oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="delete_app_credentials_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".DeveloperAppController.deleteAppCredentialsAsyncWithAuthorization") deleteAppCredentialsAsyncWithAuthorization

> Delete app credentials


```objc
function deleteAppCredentialsAsyncWithAuthorization:(NSString*) authorization
                accept:(NSString*) accept
                oRG:(NSString*) oRG
                completionBlock:(CompletedDeleteAppCredentials) onCompleted(authorization accept : accept oRG : oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* accept = @"Accept";
    NSString* oRG = @"ORG";

    [self.developerApp deleteAppCredentialsAsyncWithAuthorization: authorization accept : accept oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="keystores_controller"></a>![Class: ](https://apidocs.io/img/class.png ".KeystoresController") KeystoresController

### Get singleton instance
```objc
Keystores* keystores = [[Keystores alloc]init] ;
```

### <a name="list_keystores_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".KeystoresController.listKeystoresAsyncWithAuthorization") listKeystoresAsyncWithAuthorization

> List Keystores


```objc
function listKeystoresAsyncWithAuthorization:(NSString*) authorization
                oRG:(NSString*) oRG
                eNV:(NSString*) eNV
                completionBlock:(CompletedGetListKeystores) onCompleted(authorization oRG : oRG eNV : eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* oRG = @"ORG";
    NSString* eNV = @"ENV";

    [self.keystores listKeystoresAsyncWithAuthorization: authorization oRG : oRG eNV : eNV  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="products_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductsController") ProductsController

### Get singleton instance
```objc
Products* products = [[Products alloc]init] ;
```

### <a name="get_api_products_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.getApiProductsAsyncWithAuthorization") getApiProductsAsyncWithAuthorization

> Api Products


```objc
function getApiProductsAsyncWithAuthorization:(NSString*) authorization
                oRG:(NSString*) oRG
                completionBlock:(CompletedGetApiProducts) onCompleted(authorization oRG : oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* oRG = @"ORG";

    [self.products getApiProductsAsyncWithAuthorization: authorization oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_ap_iproduct_creation_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.createAPIproductCreationAsyncWithBody") createAPIproductCreationAsyncWithBody

> APIproduct Creation


```objc
function createAPIproductCreationAsyncWithBody:(NSString*) body
                authorization:(NSString*) authorization
                contentType:(NSString*) contentType
                oRG:(NSString*) oRG
                completionBlock:(CompletedPostAPIproductCreation) onCompleted(body authorization : authorization contentType : contentType oRG : oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* body = @"Body";
    NSString* authorization = @"Authorization";
    NSString* contentType = @"Content-Type";
    NSString* oRG = @"ORG";

    [self.products createAPIproductCreationAsyncWithBody: body authorization : authorization contentType : contentType oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="target_servers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".TargetServersController") TargetServersController

### Get singleton instance
```objc
TargetServers* targetServers = [[TargetServers alloc]init] ;
```

### <a name="list_target_servers_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".TargetServersController.listTargetServersAsyncWithAuthorization") listTargetServersAsyncWithAuthorization

> List Target Servers


```objc
function listTargetServersAsyncWithAuthorization:(NSString*) authorization
                oRG:(NSString*) oRG
                eNV:(NSString*) eNV
                completionBlock:(CompletedGetListTargetServers) onCompleted(authorization oRG : oRG eNV : eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Authorization";
    NSString* oRG = @"ORG";
    NSString* eNV = @"ENV";

    [self.targetServers listTargetServersAsyncWithAuthorization: authorization oRG : oRG eNV : eNV  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


### <a name="add_target_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".TargetServersController.addTargetAsyncWithBody") addTargetAsyncWithBody

> Add Target


```objc
function addTargetAsyncWithBody:(AddTargetRequest*) body
                contentType:(NSString*) contentType
                authorization:(NSString*) authorization
                oRG:(NSString*) oRG
                eNV:(NSString*) eNV
                completionBlock:(CompletedPostAddTarget) onCompleted(body contentType : contentType authorization : authorization oRG : oRG eNV : eNV)
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

```objc
    // Parameters for the API call
    AddTargetRequest* body = [[AddTargetRequest alloc]init];
    NSString* contentType = @"content-type";
    NSString* authorization = @"Authorization";
    NSString* oRG = @"ORG";
    NSString* eNV = @"ENV";

    [self.targetServers addTargetAsyncWithBody: body contentType : contentType authorization : authorization oRG : oRG eNV : eNV  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="company_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CompanyController") CompanyController

### Get singleton instance
```objc
Company* company = [[Company alloc]init] ;
```

### <a name="create_company_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".CompanyController.createCompanyAsyncWithBody") createCompanyAsyncWithBody

> Create Company


```objc
function createCompanyAsyncWithBody:(NSString*) body
                authorization:(NSString*) authorization
                contentType:(NSString*) contentType
                oRG:(NSString*) oRG
                completionBlock:(CompletedPostCreateCompany) onCompleted(body authorization : authorization contentType : contentType oRG : oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* body = @"Body";
    NSString* authorization = @"Authorization";
    NSString* contentType = @"Content-Type";
    NSString* oRG = @"ORG";

    [self.company createCompanyAsyncWithBody: body authorization : authorization contentType : contentType oRG : oRG  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="organizations_controller"></a>![Class: ](https://apidocs.io/img/class.png ".OrganizationsController") OrganizationsController

### Get singleton instance
```objc
Organizations* organizations = [[Organizations alloc]init] ;
```

### <a name="list_organizations_async_with_authorization"></a>![Method: ](https://apidocs.io/img/method.png ".OrganizationsController.listOrganizationsAsyncWithAuthorization") listOrganizationsAsyncWithAuthorization

> List organizations


```objc
function listOrganizationsAsyncWithAuthorization:(NSString*) authorization
                completionBlock:(CompletedGetListOrganizations) onCompleted(authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* authorization = @"Basic {{BASICAUTH}}";

    [self.organizations listOrganizationsAsyncWithAuthorization: authorization  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)




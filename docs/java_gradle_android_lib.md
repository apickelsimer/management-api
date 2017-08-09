# Getting started

TODO: Add Description

## How to Build

The generated code uses a few Gradle dependencies e.g., Jackson, Volley,
and Apache HttpClient. The reference to these dependencies is already
added in the build.gradle file will be installed automatically. Therefore,
you will need internet access for a successful build.

* In order to open the client library in Android Studio click on ``` Open an Existing Android Project ```.

![Importing SDK into Android Studio - Step 1](https://apidocs.io/illustration/android?step=import1&workspaceFolder=Apigee%20Edge%20API%20Management&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagementLib&rootNamespace=com.example)

* Browse to locate the folder containing the source code. Select the location of the ApigeeEdgeAPIManagement gradle project and click ``` Ok ```.

![Importing SDK into Android Studio - Step 2](https://apidocs.io/illustration/android?step=import2&workspaceFolder=Apigee%20Edge%20API%20Management&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagementLib&rootNamespace=com.example)

* Upon successful import, the project can be built by clicking on ``` Build > Make Project ``` or  pressing ``` Ctrl + F9 ```.

![Importing SDK into Android Studio - Step 3](https://apidocs.io/illustration/android?step=import3&workspaceFolder=Apigee%20Edge%20API%20Management&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagementLib&rootNamespace=com.example)

## How to Use

The following section explains how to use the ApigeeEdgeAPIManagement library in a new project.

### 1. Starting a new project 

For starting a new project, click on ``` Create New Android Studio Project ```.

![Add a new project in Android Studio - Step 1](https://apidocs.io/illustration/android?step=createNewProject0&workspaceFolder=Apigee%20Edge%20API%20Management&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagementLib&rootNamespace=com.example)

Here, configure the new project by adding the name, domain and location of the sample application followed by clicking ``` Next ```.

![Create a new Android Studio Project - Step 2](https://apidocs.io/illustration/android?step=createNewProject1&workspaceFolder=Apigee%20Edge%20API%20Management&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagementLib&rootNamespace=com.example)

Following this, select the ``` Phone and Tablet ```` option as shown in the illustration below and click ``` Next ```. 

![Create a new Android Studio Project - Step 3](https://apidocs.io/illustration/android?step=createNewProject2&workspaceFolder=Apigee%20Edge%20API%20Management&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagementLib&rootNamespace=com.example)

In the following step, choose ``` Empty Activity ``` as the activity type and click ``` Next ```.

![Create a new Android Studio Project - Step 4](https://apidocs.io/illustration/android?step=createNewProject3&workspaceFolder=Apigee%20Edge%20API%20Management&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagementLib&rootNamespace=com.example)

In this step, provide an ``` Activity Name ``` and ``` Layout Name ``` and click ``` Finish ```.  This would take you to the newly created project.

![Create a new Android Studio Project - Step 4](https://apidocs.io/illustration/android?step=createNewProject4&workspaceFolder=Apigee%20Edge%20API%20Management&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagementLib&rootNamespace=com.example)

### 2. Add reference of the library project

In order to add a dependency to this sample application, click on the android button shown in the project explorer on the left side as shown in the picture. Click on ``` Project ``` in the drop down that emerges.  

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/android?step=testProject0&workspaceFolder=Apigee%20Edge%20API%20Management&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagementLib&rootNamespace=com.example)

Right click the sample application in the project explorer and click on ``` New > Module ```  as shown in the picture.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/android?step=testProject1&workspaceFolder=Apigee%20Edge%20API%20Management&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagementLib&rootNamespace=com.example)

Choose ``` Import Gradle Project ``` and click ``` Next ```.

![Adding dependency to the client library - Step 3](https://apidocs.io/illustration/android?step=testProject2&workspaceFolder=Apigee%20Edge%20API%20Management&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagementLib&rootNamespace=com.example)

Click on ``` Finish ``` which would take you back to the sample application with the refernced SDK. 

![Adding dependency to the client library - Step 4](https://apidocs.io/illustration/android?step=testProject3&workspaceFolder=Apigee%20Edge%20API%20Management&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagementLib&rootNamespace=com.example)

In the following step naigate to the ``` SampleApplication >  app > build.gradle ``` file and add the following line ```compile project(path: ':ApigeeEdgeAPIManagement')``` to the dependencies section as shown in the illustration below.

![Adding dependency to the client library - Step 5](https://apidocs.io/illustration/android?step=testProject4&workspaceFolder=Apigee%20Edge%20API%20Management&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagementLib&rootNamespace=com.example)

Finally, press ``` Sync Now ``` in the warning visible as shown in the picture below.

![Adding dependency to the client library - Step 6](https://apidocs.io/illustration/android?step=testProject5&workspaceFolder=Apigee%20Edge%20API%20Management&workspaceName=ApigeeEdgeAPIManagement&projectName=ApigeeEdgeAPIManagementLib&rootNamespace=com.example)

### 3. Write sample code

Once the ``` SampleApplication ``` is created, a file named ``` SampleApplication > app > src > main > java > MainActivity ``` will be visible in the *Project Explorer* with an ``` onCreate ``` method. This is the entry point for the execution of the created project.
Here, you can add code to initialize the client library and instantiate a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

## How to Test

The generated code and the server can be tested using automatically generated test cases. 
JUnit is used as the testing framework and test runner.

In Android Studio, for running the tests do the following:

1. Right click on *SampleApplication > ApigeeEdgeAPIManagementLib > androidTest > java)* from the project explorer.
2. Select "Run All Tests" or use "Ctrl + Shift + F10" to run the Tests.

## Initialization

### Authentication
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| basicAuthUserName | The username to use with basic authentication |
| basicAuthPassword | The password to use with basic authentication |



API client can be initialized as following. The `appContext` being passed is the Android application [`Context`](https://developer.android.com/reference/android/content/Context.html).

```java
// Configuration parameters and credentials
String basicAuthUserName = "basicAuthUserName"; // The username to use with basic authentication
String basicAuthPassword = "basicAuthPassword"; // The password to use with basic authentication

com.example.Configuration.initialize(appContext);
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

## <a name="deployments_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.DeploymentsController") DeploymentsController

### Get singleton instance

The singleton instance of the ``` DeploymentsController ``` class can be accessed from the API Client.

```java
DeploymentsController deployments = client.getDeployments();
```

### <a name="list_deployments_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.DeploymentsController.listDeploymentsAsync") listDeploymentsAsync

> List Deployments


```java
void listDeploymentsAsync(
        final String authorization,
        final String oRG,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String oRG = "ORG";
// Invoking the API call with sample inputs
deployments.listDeploymentsAsync(authorization, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="get_deployments_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.DeploymentsController.getDeploymentsAsync") getDeploymentsAsync

> Deployments


```java
void getDeploymentsAsync(
        final String authorization,
        final String oRG,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String oRG = "ORG";
// Invoking the API call with sample inputs
deployments.getDeploymentsAsync(authorization, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="user_roles_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.UserRolesController") UserRolesController

### Get singleton instance

The singleton instance of the ``` UserRolesController ``` class can be accessed from the API Client.

```java
UserRolesController userRoles = client.getUserRoles();
```

### <a name="create_user_roles_update_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.UserRolesController.createUserRolesUpdateAsync") createUserRolesUpdateAsync

> User Roles Update


```java
void createUserRolesUpdateAsync(
        final UserRolesUpdateRequest body,
        final String authorization,
        final String contentType,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    String bodyValue = "{ \"role\" : [ { \"name\" : \"orgadmin\", \"organization\" : \"dev\" }, { \"name\" : \"sysadmin\" } ] }";
    UserRolesUpdateRequest body = mapper.readValue(bodyValue,new TypeReference<UserRolesUpdateRequest> (){});
    String authorization = "Basic {{BASICAUTH}}";
    String contentType = "application/json";
    // Invoking the API call with sample inputs
    userRoles.createUserRolesUpdateAsync(body, authorization, contentType, new APICallBack<void>() {
        public void onSuccess(HttpContext context, void response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    });
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


### <a name="delete_an_organization_userrole_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.UserRolesController.deleteAnOrganizationUserroleAsync") deleteAnOrganizationUserroleAsync

> Delete an organization userrole


```java
void deleteAnOrganizationUserroleAsync(
        final String org,
        final String authorization,
        final String accept,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| org |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String org = "{{ORG}}";
String authorization = "Basic {{BASICAUTH}}";
String accept = "application/json";
// Invoking the API call with sample inputs
userRoles.deleteAnOrganizationUserroleAsync(org, authorization, accept, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="get_permissions_for_a_role_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.UserRolesController.getPermissionsForARoleAsync") getPermissionsForARoleAsync

> Get permissions for a role


```java
void getPermissionsForARoleAsync(
        final String authorization,
        final String contentType,
        final String oRG,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String contentType = "Content-Type";
String oRG = "ORG";
// Invoking the API call with sample inputs
userRoles.getPermissionsForARoleAsync(authorization, contentType, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="o_auth_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.OAuthController") OAuthController

### Get singleton instance

The singleton instance of the ``` OAuthController ``` class can be accessed from the API Client.

```java
OAuthController oAuth = client.getOAuth();
```

### <a name="get_o_auth2_token_details_get_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.OAuthController.getOAuth2TokenDetailsGetAsync") getOAuth2TokenDetailsGetAsync

> OAuth2 Token Details Get


```java
void getOAuth2TokenDetailsGetAsync(
        final String authorization,
        final String contentType,
        final String oRG,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String contentType = "Content-Type";
String oRG = "ORG";
// Invoking the API call with sample inputs
oAuth.getOAuth2TokenDetailsGetAsync(authorization, contentType, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="kvm_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.KVMController") KVMController

### Get singleton instance

The singleton instance of the ``` KVMController ``` class can be accessed from the API Client.

```java
KVMController kVM = client.getKVM();
```

### <a name="get_kvm_get_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.KVMController.getKVMGetAsync") getKVMGetAsync

> KVM Get


```java
void getKVMGetAsync(
        final String authorization,
        final String contentType,
        final String oRG,
        final String eNV,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String contentType = "Content-Type";
String oRG = "ORG";
String eNV = "ENV";
// Invoking the API call with sample inputs
kVM.getKVMGetAsync(authorization, contentType, oRG, eNV, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="delete_kvm_delete_entire_kvm_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.KVMController.deleteKVMDeleteEntireKVMAsync") deleteKVMDeleteEntireKVMAsync

> KVM Delete (Entire KVM)


```java
void deleteKVMDeleteEntireKVMAsync(
        final String authorization,
        final String contentType,
        final String oRG,
        final String eNV,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String contentType = "Content-Type";
String oRG = "ORG";
String eNV = "ENV";
// Invoking the API call with sample inputs
kVM.deleteKVMDeleteEntireKVMAsync(authorization, contentType, oRG, eNV, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="pods_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.PodsController") PodsController

### Get singleton instance

The singleton instance of the ``` PodsController ``` class can be accessed from the API Client.

```java
PodsController pods = client.getPods();
```

### <a name="get_analytics_pod_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.PodsController.getAnalyticsPodAsync") getAnalyticsPodAsync

> Analytics pod


```java
void getAnalyticsPodAsync(
        final String pod,
        final String authorization,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| pod |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String pod = "analytics";
String authorization = "Basic {{BASICAUTH}}";
// Invoking the API call with sample inputs
pods.getAnalyticsPodAsync(pod, authorization, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="get_associated_pods_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.PodsController.getAssociatedPodsAsync") getAssociatedPodsAsync

> Get Associated  Pods


```java
void getAssociatedPodsAsync(
        final String contentType,
        final String authorization,
        final String oRG,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String contentType = "Content-Type";
String authorization = "Authorization";
String oRG = "ORG";
// Invoking the API call with sample inputs
pods.getAssociatedPodsAsync(contentType, authorization, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="create_disassociate_org_from_pod_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.PodsController.createDisassociateOrgFromPODAsync") createDisassociateOrgFromPODAsync

> Disassociate Org from POD


```java
void createDisassociateOrgFromPODAsync(
        final String contentType,
        final String authorization,
        final String oRG,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String contentType = "Content-Type";
String authorization = "Authorization";
String oRG = "ORG";
// Invoking the API call with sample inputs
pods.createDisassociateOrgFromPODAsync(contentType, authorization, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="servers_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.ServersController") ServersController

### Get singleton instance

The singleton instance of the ``` ServersController ``` class can be accessed from the API Client.

```java
ServersController servers = client.getServers();
```

### <a name="create_deregister_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.ServersController.createDeregisterAsync") createDeregisterAsync

> Deregister


```java
void createDeregisterAsync(
        final String authorization,
        final String contentType,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Basic {{BASICAUTH}}";
String contentType = "application/x-www-form-urlencoded";
// Invoking the API call with sample inputs
servers.createDeregisterAsync(authorization, contentType, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="list_server_by_uuid_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.ServersController.listServerByUUIDAsync") listServerByUUIDAsync

> List Server by UUID


```java
void listServerByUUIDAsync(
        final String authorization,
        final String uuid,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| uuid |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Basic {{BASICAUTH}}";
String uuid = "uuid";
// Invoking the API call with sample inputs
servers.listServerByUUIDAsync(authorization, uuid, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="create_set_not_reachable_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.ServersController.createSetNotReachableAsync") createSetNotReachableAsync

> Set not reachable


```java
void createSetNotReachableAsync(
        final String reachable,
        final String authorization,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| reachable |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String reachable = "false";
String authorization = "Basic {{BASICAUTH}}";
// Invoking the API call with sample inputs
servers.createSetNotReachableAsync(reachable, authorization, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="list_org_env_servers_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.ServersController.listOrgEnvServersAsync") listOrgEnvServersAsync

> List org/env servers


```java
void listOrgEnvServersAsync(
        final String authorization,
        final String oRG,
        final String eNV,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String oRG = "ORG";
String eNV = "ENV";
// Invoking the API call with sample inputs
servers.listOrgEnvServersAsync(authorization, oRG, eNV, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="create_register_server_with_org_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.ServersController.createRegisterServerWithOrgAsync") createRegisterServerWithOrgAsync

> Register server with org


```java
void createRegisterServerWithOrgAsync(
        final String authorization,
        final String contentType,
        final String oRG,
        final String eNV,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String contentType = "Content-Type";
String oRG = "ORG";
String eNV = "ENV";
// Invoking the API call with sample inputs
servers.createRegisterServerWithOrgAsync(authorization, contentType, oRG, eNV, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="create_associate_environments_to_mp_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.ServersController.createAssociateEnvironmentsToMPAsync") createAssociateEnvironmentsToMPAsync

> Associate  environments to MP


```java
void createAssociateEnvironmentsToMPAsync(
        final String authorization,
        final String contentType,
        final String oRG,
        final String eNV,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String contentType = "Content-Type";
String oRG = "ORG";
String eNV = "ENV";
// Invoking the API call with sample inputs
servers.createAssociateEnvironmentsToMPAsync(authorization, contentType, oRG, eNV, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="developers_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.DevelopersController") DevelopersController

### Get singleton instance

The singleton instance of the ``` DevelopersController ``` class can be accessed from the API Client.

```java
DevelopersController developers = client.getDevelopers();
```

### <a name="get_developers_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.DevelopersController.getDevelopersAsync") getDevelopersAsync

> Get Developers


```java
void getDevelopersAsync(
        final String authorization,
        final String contentType,
        final String oRG,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String contentType = "Content-Type";
String oRG = "ORG";
// Invoking the API call with sample inputs
developers.getDevelopersAsync(authorization, contentType, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="create_developer_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.DevelopersController.createDeveloperAsync") createDeveloperAsync

> Create Developer


```java
void createDeveloperAsync(
        final String body,
        final String authorization,
        final String contentType,
        final String oRG,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String body = "Body";
String authorization = "Authorization";
String contentType = "Content-Type";
String oRG = "ORG";
// Invoking the API call with sample inputs
developers.createDeveloperAsync(body, authorization, contentType, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="ap_is_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.APIsController") APIsController

### Get singleton instance

The singleton instance of the ``` APIsController ``` class can be accessed from the API Client.

```java
APIsController aPIs = client.getAPIs();
```

### <a name="get_api_list_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.APIsController.getApiListAsync") getApiListAsync

> Api list


```java
void getApiListAsync(
        final String authorization,
        final String oRG,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String oRG = "ORG";
// Invoking the API call with sample inputs
aPIs.getApiListAsync(authorization, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="create_deploy_api_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.APIsController.createDeployAPIAsync") createDeployAPIAsync

> Deploy API


```java
void createDeployAPIAsync(
        final String action,
        final String name,
        final String authorization,
        final String contentType,
        final String oRG,
        final APICallBack<Object> callBack)
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

```java
String action = "action";
String name = "name";
String authorization = "Authorization";
String contentType = "Content-Type";
String oRG = "ORG";
// Invoking the API call with sample inputs
aPIs.createDeployAPIAsync(action, name, authorization, contentType, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="delete_an_api_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.APIsController.deleteAnAPIAsync") deleteAnAPIAsync

> Delete an API


```java
void deleteAnAPIAsync(
        final String authorization,
        final String oRG,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String oRG = "ORG";
// Invoking the API call with sample inputs
aPIs.deleteAnAPIAsync(authorization, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="create_undeploy_revisions_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.APIsController.createUndeployRevisionsAsync") createUndeployRevisionsAsync

> Undeploy Revisions


```java
void createUndeployRevisionsAsync(
        final String action,
        final String env,
        final String authorization,
        final String contentType,
        final String oRG,
        final APICallBack<Object> callBack)
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

```java
String action = "action";
String env = "env";
String authorization = "Authorization";
String contentType = "Content-Type";
String oRG = "ORG";
// Invoking the API call with sample inputs
aPIs.createUndeployRevisionsAsync(action, env, authorization, contentType, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="cache_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.CacheController") CacheController

### Get singleton instance

The singleton instance of the ``` CacheController ``` class can be accessed from the API Client.

```java
CacheController cache = client.getCache();
```

### <a name="list_caches_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.CacheController.listCachesAsync") listCachesAsync

> List caches


```java
void listCachesAsync(
        final String authorization,
        final String oRG,
        final String eNV,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String oRG = "ORG";
String eNV = "ENV";
// Invoking the API call with sample inputs
cache.listCachesAsync(authorization, oRG, eNV, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="audit_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.AuditController") AuditController

### Get singleton instance

The singleton instance of the ``` AuditController ``` class can be accessed from the API Client.

```java
AuditController audit = client.getAudit();
```

### <a name="get_audit_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.AuditController.getAuditAsync") getAuditAsync

> Audit


```java
void getAuditAsync(
        final boolean expand,
        final String timeline,
        final String authorization,
        final String oRG,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| expand |  ``` Required ```  | TODO: Add a parameter description |
| timeline |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
boolean expand = false;
String timeline = "timeline";
String authorization = "Authorization";
String oRG = "ORG";
// Invoking the API call with sample inputs
audit.getAuditAsync(expand, timeline, authorization, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="users_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.UsersController") UsersController

### Get singleton instance

The singleton instance of the ``` UsersController ``` class can be accessed from the API Client.

```java
UsersController users = client.getUsers();
```

### <a name="get_developer_details_get_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.UsersController.getDeveloperDetailsGetAsync") getDeveloperDetailsGetAsync

> Developer Details Get


```java
void getDeveloperDetailsGetAsync(
        final String authorization,
        final String contentType,
        final String oRG,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String contentType = "Content-Type";
String oRG = "ORG";
// Invoking the API call with sample inputs
users.getDeveloperDetailsGetAsync(authorization, contentType, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="create_user_in_org_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.UsersController.createUserInORGAsync") createUserInORGAsync

> Create User in ORG


```java
void createUserInORGAsync(
        final String body,
        final String authorization,
        final String contentType,
        final String oRG,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String body = "Body";
String authorization = "Authorization";
String contentType = "Content-Type";
String oRG = "ORG";
// Invoking the API call with sample inputs
users.createUserInORGAsync(body, authorization, contentType, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="list_users_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.UsersController.listUsersAsync") listUsersAsync

> List Users


```java
void listUsersAsync(
        final String authorization,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Basic {{BASICAUTH}}";
// Invoking the API call with sample inputs
users.listUsersAsync(authorization, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="add_user_as_orgadmin_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.UsersController.addUserAsOrgadminAsync") addUserAsOrgadminAsync

> Add user as Orgadmin


```java
void addUserAsOrgadminAsync(
        final String body,
        final String authorization,
        final String contentType,
        final String oRG,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String body = "Body";
String authorization = "Authorization";
String contentType = "Content-Type";
String oRG = "ORG";
// Invoking the API call with sample inputs
users.addUserAsOrgadminAsync(body, authorization, contentType, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="zzz_others_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.ZzzOthersController") ZzzOthersController

### Get singleton instance

The singleton instance of the ``` ZzzOthersController ``` class can be accessed from the API Client.

```java
ZzzOthersController zzzOthers = client.getZzzOthers();
```

### <a name="get_cluster_status_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.ZzzOthersController.getClusterStatusAsync") getClusterStatusAsync

> Cluster Status


```java
void getClusterStatusAsync(
        final String authorization,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Basic {{BASICAUTH}}";
// Invoking the API call with sample inputs
zzzOthers.getClusterStatusAsync(authorization, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="create_enable_debug_wo_restart_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.ZzzOthersController.createEnableDebugWORestartAsync") createEnableDebugWORestartAsync

> Enable Debug w/o Restart 


```java
void createEnableDebugWORestartAsync(
        final String session,
        final String authorization,
        final String contentType,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| session |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String session = "logsession_name";
String authorization = "Basic {{BASICAUTH}}";
String contentType = "application/x-www-form-urlencoded";
// Invoking the API call with sample inputs
zzzOthers.createEnableDebugWORestartAsync(session, authorization, contentType, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="get_classifications_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.ZzzOthersController.getClassificationsAsync") getClassificationsAsync

> Classifications


```java
void getClassificationsAsync(
        final String authorization,
        final String hOST,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String hOST = "HOST";
// Invoking the API call with sample inputs
zzzOthers.getClassificationsAsync(authorization, hOST, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="create_company_developer_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.ZzzOthersController.createCompanyDeveloperAsync") createCompanyDeveloperAsync

> Create Company Developer


```java
void createCompanyDeveloperAsync(
        final CreateCompanyDeveloperRequest body,
        final String contentType,
        final String authorization,
        final String oRG,
        final String cOMPANY,
        final APICallBack<Object> callBack)
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

```java
try {
    CreateCompanyDeveloperRequest body = new CreateCompanyDeveloperRequest();
    String contentType = "Content-Type";
    String authorization = "Authorization";
    String oRG = "ORG";
    String cOMPANY = "COMPANY";
    // Invoking the API call with sample inputs
    zzzOthers.createCompanyDeveloperAsync(body, contentType, authorization, oRG, cOMPANY, new APICallBack<void>() {
        public void onSuccess(HttpContext context, void response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    });
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


### <a name="get_qpid_metrics_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.ZzzOthersController.getQPIDMetricsAsync") getQPIDMetricsAsync

> QPID Metrics


```java
void getQPIDMetricsAsync(
        final String authorization,
        final String hOST,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String hOST = "HOST";
// Invoking the API call with sample inputs
zzzOthers.getQPIDMetricsAsync(authorization, hOST, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="get_build_info_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.ZzzOthersController.getBuildInfoAsync") getBuildInfoAsync

> Build Info


```java
void getBuildInfoAsync(
        final String authorization,
        final String hOST,
        final String pORT,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |
| pORT |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String hOST = "HOST";
String pORT = "PORT";
// Invoking the API call with sample inputs
zzzOthers.getBuildInfoAsync(authorization, hOST, pORT, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="delete_disable_debug_wo_restart_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.ZzzOthersController.deleteDisableDebugWORestartAsync") deleteDisableDebugWORestartAsync

> Disable Debug w/o Restart


```java
void deleteDisableDebugWORestartAsync(
        final String authorization,
        final String contentType,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Basic {{BASICAUTH}}";
String contentType = "application/x-www-form-urlencoded";
// Invoking the API call with sample inputs
zzzOthers.deleteDisableDebugWORestartAsync(authorization, contentType, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="apps_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.AppsController") AppsController

### Get singleton instance

The singleton instance of the ``` AppsController ``` class can be accessed from the API Client.

```java
AppsController apps = client.getApps();
```

### <a name="create_company_app_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.AppsController.createCompanyAPPAsync") createCompanyAPPAsync

> Create Company APP


```java
void createCompanyAPPAsync(
        final String body,
        final String authorization,
        final String contentType,
        final String oRG,
        final String cOMPANY,
        final APICallBack<Object> callBack)
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

```java
String body = "Body";
String authorization = "Authorization";
String contentType = "Content-Type";
String oRG = "ORG";
String cOMPANY = "COMPANY";
// Invoking the API call with sample inputs
apps.createCompanyAPPAsync(body, authorization, contentType, oRG, cOMPANY, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="add_app_credentials_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.AppsController.addAppCredentialsAsync") addAppCredentialsAsync

> Add app credentials


```java
void addAppCredentialsAsync(
        final String body,
        final String authorization,
        final String contentType,
        final String oRG,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String body = "Body";
String authorization = "Authorization";
String contentType = "Content-Type";
String oRG = "ORG";
// Invoking the API call with sample inputs
apps.addAppCredentialsAsync(body, authorization, contentType, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="list_apps_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.AppsController.listAppsAsync") listAppsAsync

> List apps 


```java
void listAppsAsync(
        final String authorization,
        final String oRG,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String oRG = "ORG";
// Invoking the API call with sample inputs
apps.listAppsAsync(authorization, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="list_app_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.AppsController.listAppAsync") listAppAsync

> List app


```java
void listAppAsync(
        final String authorization,
        final String oRG,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String oRG = "ORG";
// Invoking the API call with sample inputs
apps.listAppAsync(authorization, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="virtual_hosts_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.VirtualHostsController") VirtualHostsController

### Get singleton instance

The singleton instance of the ``` VirtualHostsController ``` class can be accessed from the API Client.

```java
VirtualHostsController virtualHosts = client.getVirtualHosts();
```

### <a name="list_virtual_hosts_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.VirtualHostsController.listVirtualHostsAsync") listVirtualHostsAsync

> List VirtualHosts


```java
void listVirtualHostsAsync(
        final String authorization,
        final String oRG,
        final String eNV,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String oRG = "ORG";
String eNV = "ENV";
// Invoking the API call with sample inputs
virtualHosts.listVirtualHostsAsync(authorization, oRG, eNV, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="add_virtual_host_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.VirtualHostsController.addVirtualHostAsync") addVirtualHostAsync

> Add Virtual Host


```java
void addVirtualHostAsync(
        final String body,
        final String authorization,
        final String contentType,
        final String oRG,
        final String eNV,
        final APICallBack<Object> callBack)
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

```java
String body = "Body";
String authorization = "Authorization";
String contentType = "Content-Type";
String oRG = "ORG";
String eNV = "ENV";
// Invoking the API call with sample inputs
virtualHosts.addVirtualHostAsync(body, authorization, contentType, oRG, eNV, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="environments_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.EnvironmentsController") EnvironmentsController

### Get singleton instance

The singleton instance of the ``` EnvironmentsController ``` class can be accessed from the API Client.

```java
EnvironmentsController environments = client.getEnvironments();
```

### <a name="update_environments_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.EnvironmentsController.updateEnvironmentsAsync") updateEnvironmentsAsync

> Update Environments


```java
void updateEnvironmentsAsync(
        final String authorization,
        final String contentType,
        final String oRG,
        final String eNV,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String contentType = "Content-Type";
String oRG = "ORG";
String eNV = "ENV";
// Invoking the API call with sample inputs
environments.updateEnvironmentsAsync(authorization, contentType, oRG, eNV, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="delete_environment_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.EnvironmentsController.deleteEnvironmentAsync") deleteEnvironmentAsync

> Delete Environment


```java
void deleteEnvironmentAsync(
        final String authorization,
        final String oRG,
        final String eNV,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String oRG = "ORG";
String eNV = "ENV";
// Invoking the API call with sample inputs
environments.deleteEnvironmentAsync(authorization, oRG, eNV, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="create_new_env_in_org_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.EnvironmentsController.createNewENVInORGAsync") createNewENVInORGAsync

> Create New ENV in ORG


```java
void createNewENVInORGAsync(
        final String body,
        final String authorization,
        final String contentType,
        final String oRG,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String body = "Body";
String authorization = "Authorization";
String contentType = "Content-Type";
String oRG = "ORG";
// Invoking the API call with sample inputs
environments.createNewENVInORGAsync(body, authorization, contentType, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="developer_app_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.DeveloperAppController") DeveloperAppController

### Get singleton instance

The singleton instance of the ``` DeveloperAppController ``` class can be accessed from the API Client.

```java
DeveloperAppController developerApp = client.getDeveloperApp();
```

### <a name="get_developer_app_details_get_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.DeveloperAppController.getDeveloperAppDetailsGetAsync") getDeveloperAppDetailsGetAsync

> Developer App Details Get


```java
void getDeveloperAppDetailsGetAsync(
        final String authorization,
        final String contentType,
        final String oRG,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String contentType = "Content-Type";
String oRG = "ORG";
// Invoking the API call with sample inputs
developerApp.getDeveloperAppDetailsGetAsync(authorization, contentType, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="delete_app_credentials_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.DeveloperAppController.deleteAppCredentialsAsync") deleteAppCredentialsAsync

> Delete app credentials


```java
void deleteAppCredentialsAsync(
        final String authorization,
        final String accept,
        final String oRG,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String accept = "Accept";
String oRG = "ORG";
// Invoking the API call with sample inputs
developerApp.deleteAppCredentialsAsync(authorization, accept, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="keystores_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.KeystoresController") KeystoresController

### Get singleton instance

The singleton instance of the ``` KeystoresController ``` class can be accessed from the API Client.

```java
KeystoresController keystores = client.getKeystores();
```

### <a name="list_keystores_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.KeystoresController.listKeystoresAsync") listKeystoresAsync

> List Keystores


```java
void listKeystoresAsync(
        final String authorization,
        final String oRG,
        final String eNV,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String oRG = "ORG";
String eNV = "ENV";
// Invoking the API call with sample inputs
keystores.listKeystoresAsync(authorization, oRG, eNV, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="products_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.ProductsController") ProductsController

### Get singleton instance

The singleton instance of the ``` ProductsController ``` class can be accessed from the API Client.

```java
ProductsController products = client.getProducts();
```

### <a name="get_api_products_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.ProductsController.getApiProductsAsync") getApiProductsAsync

> Api Products


```java
void getApiProductsAsync(
        final String authorization,
        final String oRG,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String oRG = "ORG";
// Invoking the API call with sample inputs
products.getApiProductsAsync(authorization, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="create_ap_iproduct_creation_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.ProductsController.createAPIproductCreationAsync") createAPIproductCreationAsync

> APIproduct Creation


```java
void createAPIproductCreationAsync(
        final String body,
        final String authorization,
        final String contentType,
        final String oRG,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String body = "Body";
String authorization = "Authorization";
String contentType = "Content-Type";
String oRG = "ORG";
// Invoking the API call with sample inputs
products.createAPIproductCreationAsync(body, authorization, contentType, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="target_servers_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.TargetServersController") TargetServersController

### Get singleton instance

The singleton instance of the ``` TargetServersController ``` class can be accessed from the API Client.

```java
TargetServersController targetServers = client.getTargetServers();
```

### <a name="list_target_servers_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.TargetServersController.listTargetServersAsync") listTargetServersAsync

> List Target Servers


```java
void listTargetServersAsync(
        final String authorization,
        final String oRG,
        final String eNV,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Authorization";
String oRG = "ORG";
String eNV = "ENV";
// Invoking the API call with sample inputs
targetServers.listTargetServersAsync(authorization, oRG, eNV, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="add_target_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.TargetServersController.addTargetAsync") addTargetAsync

> Add Target


```java
void addTargetAsync(
        final AddTargetRequest body,
        final String contentType,
        final String authorization,
        final String oRG,
        final String eNV,
        final APICallBack<Object> callBack)
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

```java
try {
    AddTargetRequest body = new AddTargetRequest();
    String contentType = "content-type";
    String authorization = "Authorization";
    String oRG = "ORG";
    String eNV = "ENV";
    // Invoking the API call with sample inputs
    targetServers.addTargetAsync(body, contentType, authorization, oRG, eNV, new APICallBack<void>() {
        public void onSuccess(HttpContext context, void response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    });
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


[Back to List of Controllers](#list_of_controllers)

## <a name="company_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.CompanyController") CompanyController

### Get singleton instance

The singleton instance of the ``` CompanyController ``` class can be accessed from the API Client.

```java
CompanyController company = client.getCompany();
```

### <a name="create_company_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.CompanyController.createCompanyAsync") createCompanyAsync

> Create Company


```java
void createCompanyAsync(
        final String body,
        final String authorization,
        final String contentType,
        final String oRG,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String body = "Body";
String authorization = "Authorization";
String contentType = "Content-Type";
String oRG = "ORG";
// Invoking the API call with sample inputs
company.createCompanyAsync(body, authorization, contentType, oRG, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="organizations_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.controllers.OrganizationsController") OrganizationsController

### Get singleton instance

The singleton instance of the ``` OrganizationsController ``` class can be accessed from the API Client.

```java
OrganizationsController organizations = client.getOrganizations();
```

### <a name="list_organizations_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.controllers.OrganizationsController.listOrganizationsAsync") listOrganizationsAsync

> List organizations


```java
void listOrganizationsAsync(
        final String authorization,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String authorization = "Basic {{BASICAUTH}}";
// Invoking the API call with sample inputs
organizations.listOrganizationsAsync(authorization, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)




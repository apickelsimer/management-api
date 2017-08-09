# Getting started

TODO: Add Description

## How to Build

The generated SDK relies on [Node Package Manager](https://www.npmjs.com/) (NPM) being available to resolve dependencies. If you don't already have NPM installed, please go ahead and follow instructions to install NPM from [here](https://nodejs.org/en/download/).
The SDK also requires Node to be installed. If Node isn't already installed, please install it from [here](https://nodejs.org/en/download/)
> NPM is installed by default when Node is installed

To check if node and npm have been successfully installed, write the following commands in command prompt:

* `node --version`
* `npm -version`

![Version Check](https://apidocs.io/illustration/nodejs?step=versionCheck&workspaceFolder=Apigee%20Edge%20API%20Management-Node)

Now use npm to resolve all dependencies by running the following command in the root directory (of the SDK folder):

```bash
npm install
```

![Resolve Dependencies](https://apidocs.io/illustration/nodejs?step=resolveDependency1&workspaceFolder=Apigee%20Edge%20API%20Management-Node)

![Resolve Dependencies](https://apidocs.io/illustration/nodejs?step=resolveDependency2)

This will install all dependencies in the `node_modules` folder.

Once dependencies are resolved, you will need to move the folder `ApigeeEdgeAPIManagementLib ` in to your `node_modules` folder.

## How to Use

The following section explains how to use the library in a new project.

### 1. Open Project Folder
Open an IDE/Text Editor for JavaScript like Sublime Text. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

Click on `File` and select `Open Folder`.

![Open Folder](https://apidocs.io/illustration/nodejs?step=openFolder)

Select the folder of your SDK and click on `Select Folder` to open it up in Sublime Text. The folder will become visible in the bar on the left.

![Open Project](https://apidocs.io/illustration/nodejs?step=openProject&workspaceFolder=Apigee%20Edge%20API%20Management-Node)

### 2. Creating a Test File

Now right click on the folder name and select the `New File` option to create a new test file. Save it as `index.js` Now import the generated NodeJS library using the following lines of code:

```js
var lib = require('lib');
```

Save changes.

![Create new file](https://apidocs.io/illustration/nodejs?step=createNewFile&workspaceFolder=Apigee%20Edge%20API%20Management-Node)

![Save new file](https://apidocs.io/illustration/nodejs?step=saveNewFile&workspaceFolder=Apigee%20Edge%20API%20Management-Node)

### 3. Running The Test File

To run the `index.js` file, open up the command prompt and navigate to the Path where the SDK folder resides. Type the following command to run the file:

```
node index.js
```

![Run file](https://apidocs.io/illustration/nodejs?step=runProject&workspaceFolder=Apigee%20Edge%20API%20Management-Node)


## How to Test

These tests use Mocha framework for testing, coupled with Chai for assertions. These dependencies need to be installed for tests to run.
Tests can be run in a number of ways:

### Method 1 (Run all tests)

1. Navigate to the root directory of the SDK folder from command prompt.
2. Type `mocha --recursive` to run all the tests.

### Method 2 (Run all tests)

1. Navigate to the `../test/Controllers/` directory from command prompt.
2. Type `mocha *` to run all the tests.

### Method 3 (Run specific controller's tests)

1. Navigate to the `../test/Controllers/` directory from command prompt.
2. Type `mocha  Apigee Edge API ManagementController`  to run all the tests in that controller file.

> To increase mocha's default timeout, you can change the `TEST_TIMEOUT` parameter's value in `TestBootstrap.js`.

![Run Tests](https://apidocs.io/illustration/nodejs?step=runTests&controllerName=Apigee%20Edge%20API%20ManagementController)

## Initialization

### Authentication
In order to setup authentication in the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| basicAuthUserName | The username to use with basic authentication |
| basicAuthPassword | The password to use with basic authentication |



API client can be initialized as following:

```JavaScript
const lib = require('lib');

// Configuration parameters and credentials
lib.Configuration.basicAuthUserName = "basicAuthUserName"; // The username to use with basic authentication
lib.Configuration.basicAuthPassword = "basicAuthPassword"; // The password to use with basic authentication

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

The singleton instance of the ``` DeploymentsController ``` class can be accessed from the API Client.

```javascript
var controller = lib.DeploymentsController;
```

### <a name="list_deployments"></a>![Method: ](https://apidocs.io/img/method.png ".DeploymentsController.listDeployments") listDeployments

> List Deployments


```javascript
function listDeployments(authorization, oRG, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var oRG = 'ORG';

    controller.listDeployments(authorization, oRG, function(error, response, context) {

    
    });
```



### <a name="get_deployments"></a>![Method: ](https://apidocs.io/img/method.png ".DeploymentsController.getDeployments") getDeployments

> Deployments


```javascript
function getDeployments(authorization, oRG, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var oRG = 'ORG';

    controller.getDeployments(authorization, oRG, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="user_roles_controller"></a>![Class: ](https://apidocs.io/img/class.png ".UserRolesController") UserRolesController

### Get singleton instance

The singleton instance of the ``` UserRolesController ``` class can be accessed from the API Client.

```javascript
var controller = lib.UserRolesController;
```

### <a name="create_user_roles_update"></a>![Method: ](https://apidocs.io/img/method.png ".UserRolesController.createUserRolesUpdate") createUserRolesUpdate

> User Roles Update


```javascript
function createUserRolesUpdate(body, authorization, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new UserRolesUpdateRequest({ "role" : [ { "name" : "orgadmin", "organization" : "dev" }, { "name" : "sysadmin" } ] });
    var authorization = 'Basic {{BASICAUTH}}';
    var contentType = 'application/json';

    controller.createUserRolesUpdate(body, authorization, contentType, function(error, response, context) {

    
    });
```



### <a name="delete_an_organization_userrole"></a>![Method: ](https://apidocs.io/img/method.png ".UserRolesController.deleteAnOrganizationUserrole") deleteAnOrganizationUserrole

> Delete an organization userrole


```javascript
function deleteAnOrganizationUserrole(org, authorization, accept, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| org |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var org = '{{ORG}}';
    var authorization = 'Basic {{BASICAUTH}}';
    var accept = 'application/json';

    controller.deleteAnOrganizationUserrole(org, authorization, accept, function(error, response, context) {

    
    });
```



### <a name="get_permissions_for_a_role"></a>![Method: ](https://apidocs.io/img/method.png ".UserRolesController.getPermissionsForARole") getPermissionsForARole

> Get permissions for a role


```javascript
function getPermissionsForARole(authorization, contentType, oRG, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var contentType = 'Content-Type';
    var oRG = 'ORG';

    controller.getPermissionsForARole(authorization, contentType, oRG, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="o_auth_controller"></a>![Class: ](https://apidocs.io/img/class.png ".OAuthController") OAuthController

### Get singleton instance

The singleton instance of the ``` OAuthController ``` class can be accessed from the API Client.

```javascript
var controller = lib.OAuthController;
```

### <a name="get_o_auth2_token_details_get"></a>![Method: ](https://apidocs.io/img/method.png ".OAuthController.getOAuth2TokenDetailsGet") getOAuth2TokenDetailsGet

> OAuth2 Token Details Get


```javascript
function getOAuth2TokenDetailsGet(authorization, contentType, oRG, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var contentType = 'Content-Type';
    var oRG = 'ORG';

    controller.getOAuth2TokenDetailsGet(authorization, contentType, oRG, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="kvm_controller"></a>![Class: ](https://apidocs.io/img/class.png ".KVMController") KVMController

### Get singleton instance

The singleton instance of the ``` KVMController ``` class can be accessed from the API Client.

```javascript
var controller = lib.KVMController;
```

### <a name="get_kvm_get"></a>![Method: ](https://apidocs.io/img/method.png ".KVMController.getKVMGet") getKVMGet

> KVM Get


```javascript
function getKVMGet(authorization, contentType, oRG, eNV, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var contentType = 'Content-Type';
    var oRG = 'ORG';
    var eNV = 'ENV';

    controller.getKVMGet(authorization, contentType, oRG, eNV, function(error, response, context) {

    
    });
```



### <a name="delete_kvm_delete_entire_kvm"></a>![Method: ](https://apidocs.io/img/method.png ".KVMController.deleteKVMDeleteEntireKVM") deleteKVMDeleteEntireKVM

> KVM Delete (Entire KVM)


```javascript
function deleteKVMDeleteEntireKVM(authorization, contentType, oRG, eNV, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var contentType = 'Content-Type';
    var oRG = 'ORG';
    var eNV = 'ENV';

    controller.deleteKVMDeleteEntireKVM(authorization, contentType, oRG, eNV, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="pods_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PodsController") PodsController

### Get singleton instance

The singleton instance of the ``` PodsController ``` class can be accessed from the API Client.

```javascript
var controller = lib.PodsController;
```

### <a name="get_analytics_pod"></a>![Method: ](https://apidocs.io/img/method.png ".PodsController.getAnalyticsPod") getAnalyticsPod

> Analytics pod


```javascript
function getAnalyticsPod(pod, authorization, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| pod |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var pod = 'analytics';
    var authorization = 'Basic {{BASICAUTH}}';

    controller.getAnalyticsPod(pod, authorization, function(error, response, context) {

    
    });
```



### <a name="get_associated_pods"></a>![Method: ](https://apidocs.io/img/method.png ".PodsController.getAssociatedPods") getAssociatedPods

> Get Associated  Pods


```javascript
function getAssociatedPods(contentType, authorization, oRG, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var contentType = 'Content-Type';
    var authorization = 'Authorization';
    var oRG = 'ORG';

    controller.getAssociatedPods(contentType, authorization, oRG, function(error, response, context) {

    
    });
```



### <a name="create_disassociate_org_from_pod"></a>![Method: ](https://apidocs.io/img/method.png ".PodsController.createDisassociateOrgFromPOD") createDisassociateOrgFromPOD

> Disassociate Org from POD


```javascript
function createDisassociateOrgFromPOD(contentType, authorization, oRG, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var contentType = 'Content-Type';
    var authorization = 'Authorization';
    var oRG = 'ORG';

    controller.createDisassociateOrgFromPOD(contentType, authorization, oRG, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="servers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ServersController") ServersController

### Get singleton instance

The singleton instance of the ``` ServersController ``` class can be accessed from the API Client.

```javascript
var controller = lib.ServersController;
```

### <a name="create_deregister"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.createDeregister") createDeregister

> Deregister


```javascript
function createDeregister(authorization, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Basic {{BASICAUTH}}';
    var contentType = 'application/x-www-form-urlencoded';

    controller.createDeregister(authorization, contentType, function(error, response, context) {

    
    });
```



### <a name="list_server_by_uuid"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.listServerByUUID") listServerByUUID

> List Server by UUID


```javascript
function listServerByUUID(authorization, uuid, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| uuid |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Basic {{BASICAUTH}}';
    var uuid = 'uuid';

    controller.listServerByUUID(authorization, uuid, function(error, response, context) {

    
    });
```



### <a name="create_set_not_reachable"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.createSetNotReachable") createSetNotReachable

> Set not reachable


```javascript
function createSetNotReachable(reachable, authorization, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| reachable |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var reachable = 'false';
    var authorization = 'Basic {{BASICAUTH}}';

    controller.createSetNotReachable(reachable, authorization, function(error, response, context) {

    
    });
```



### <a name="list_org_env_servers"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.listOrgEnvServers") listOrgEnvServers

> List org/env servers


```javascript
function listOrgEnvServers(authorization, oRG, eNV, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var oRG = 'ORG';
    var eNV = 'ENV';

    controller.listOrgEnvServers(authorization, oRG, eNV, function(error, response, context) {

    
    });
```



### <a name="create_register_server_with_org"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.createRegisterServerWithOrg") createRegisterServerWithOrg

> Register server with org


```javascript
function createRegisterServerWithOrg(authorization, contentType, oRG, eNV, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var contentType = 'Content-Type';
    var oRG = 'ORG';
    var eNV = 'ENV';

    controller.createRegisterServerWithOrg(authorization, contentType, oRG, eNV, function(error, response, context) {

    
    });
```



### <a name="create_associate_environments_to_mp"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.createAssociateEnvironmentsToMP") createAssociateEnvironmentsToMP

> Associate  environments to MP


```javascript
function createAssociateEnvironmentsToMP(authorization, contentType, oRG, eNV, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var contentType = 'Content-Type';
    var oRG = 'ORG';
    var eNV = 'ENV';

    controller.createAssociateEnvironmentsToMP(authorization, contentType, oRG, eNV, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="developers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DevelopersController") DevelopersController

### Get singleton instance

The singleton instance of the ``` DevelopersController ``` class can be accessed from the API Client.

```javascript
var controller = lib.DevelopersController;
```

### <a name="get_developers"></a>![Method: ](https://apidocs.io/img/method.png ".DevelopersController.getDevelopers") getDevelopers

> Get Developers


```javascript
function getDevelopers(authorization, contentType, oRG, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var contentType = 'Content-Type';
    var oRG = 'ORG';

    controller.getDevelopers(authorization, contentType, oRG, function(error, response, context) {

    
    });
```



### <a name="create_developer"></a>![Method: ](https://apidocs.io/img/method.png ".DevelopersController.createDeveloper") createDeveloper

> Create Developer


```javascript
function createDeveloper(body, authorization, contentType, oRG, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = 'Body';
    var authorization = 'Authorization';
    var contentType = 'Content-Type';
    var oRG = 'ORG';

    controller.createDeveloper(body, authorization, contentType, oRG, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="ap_is_controller"></a>![Class: ](https://apidocs.io/img/class.png ".APIsController") APIsController

### Get singleton instance

The singleton instance of the ``` APIsController ``` class can be accessed from the API Client.

```javascript
var controller = lib.APIsController;
```

### <a name="get_api_list"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.getApiList") getApiList

> Api list


```javascript
function getApiList(authorization, oRG, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var oRG = 'ORG';

    controller.getApiList(authorization, oRG, function(error, response, context) {

    
    });
```



### <a name="create_deploy_api"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.createDeployAPI") createDeployAPI

> Deploy API


```javascript
function createDeployAPI(action, name, authorization, contentType, oRG, callback)
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

```javascript

    var action = 'action';
    var name = 'name';
    var authorization = 'Authorization';
    var contentType = 'Content-Type';
    var oRG = 'ORG';

    controller.createDeployAPI(action, name, authorization, contentType, oRG, function(error, response, context) {

    
    });
```



### <a name="delete_an_api"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.deleteAnAPI") deleteAnAPI

> Delete an API


```javascript
function deleteAnAPI(authorization, oRG, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var oRG = 'ORG';

    controller.deleteAnAPI(authorization, oRG, function(error, response, context) {

    
    });
```



### <a name="create_undeploy_revisions"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.createUndeployRevisions") createUndeployRevisions

> Undeploy Revisions


```javascript
function createUndeployRevisions(action, env, authorization, contentType, oRG, callback)
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

```javascript

    var action = 'action';
    var env = 'env';
    var authorization = 'Authorization';
    var contentType = 'Content-Type';
    var oRG = 'ORG';

    controller.createUndeployRevisions(action, env, authorization, contentType, oRG, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="cache_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CacheController") CacheController

### Get singleton instance

The singleton instance of the ``` CacheController ``` class can be accessed from the API Client.

```javascript
var controller = lib.CacheController;
```

### <a name="list_caches"></a>![Method: ](https://apidocs.io/img/method.png ".CacheController.listCaches") listCaches

> List caches


```javascript
function listCaches(authorization, oRG, eNV, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var oRG = 'ORG';
    var eNV = 'ENV';

    controller.listCaches(authorization, oRG, eNV, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="audit_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AuditController") AuditController

### Get singleton instance

The singleton instance of the ``` AuditController ``` class can be accessed from the API Client.

```javascript
var controller = lib.AuditController;
```

### <a name="get_audit"></a>![Method: ](https://apidocs.io/img/method.png ".AuditController.getAudit") getAudit

> Audit


```javascript
function getAudit(expand, timeline, authorization, oRG, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| expand |  ``` Required ```  | TODO: Add a parameter description |
| timeline |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var expand = true;
    var timeline = 'timeline';
    var authorization = 'Authorization';
    var oRG = 'ORG';

    controller.getAudit(expand, timeline, authorization, oRG, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="users_controller"></a>![Class: ](https://apidocs.io/img/class.png ".UsersController") UsersController

### Get singleton instance

The singleton instance of the ``` UsersController ``` class can be accessed from the API Client.

```javascript
var controller = lib.UsersController;
```

### <a name="get_developer_details_get"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.getDeveloperDetailsGet") getDeveloperDetailsGet

> Developer Details Get


```javascript
function getDeveloperDetailsGet(authorization, contentType, oRG, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var contentType = 'Content-Type';
    var oRG = 'ORG';

    controller.getDeveloperDetailsGet(authorization, contentType, oRG, function(error, response, context) {

    
    });
```



### <a name="create_user_in_org"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.createUserInORG") createUserInORG

> Create User in ORG


```javascript
function createUserInORG(body, authorization, contentType, oRG, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = 'Body';
    var authorization = 'Authorization';
    var contentType = 'Content-Type';
    var oRG = 'ORG';

    controller.createUserInORG(body, authorization, contentType, oRG, function(error, response, context) {

    
    });
```



### <a name="list_users"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.listUsers") listUsers

> List Users


```javascript
function listUsers(authorization, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Basic {{BASICAUTH}}';

    controller.listUsers(authorization, function(error, response, context) {

    
    });
```



### <a name="add_user_as_orgadmin"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.addUserAsOrgadmin") addUserAsOrgadmin

> Add user as Orgadmin


```javascript
function addUserAsOrgadmin(body, authorization, contentType, oRG, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = 'Body';
    var authorization = 'Authorization';
    var contentType = 'Content-Type';
    var oRG = 'ORG';

    controller.addUserAsOrgadmin(body, authorization, contentType, oRG, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="zzz_others_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ZzzOthersController") ZzzOthersController

### Get singleton instance

The singleton instance of the ``` ZzzOthersController ``` class can be accessed from the API Client.

```javascript
var controller = lib.ZzzOthersController;
```

### <a name="get_cluster_status"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.getClusterStatus") getClusterStatus

> Cluster Status


```javascript
function getClusterStatus(authorization, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Basic {{BASICAUTH}}';

    controller.getClusterStatus(authorization, function(error, response, context) {

    
    });
```



### <a name="create_enable_debug_wo_restart"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.createEnableDebugWORestart") createEnableDebugWORestart

> Enable Debug w/o Restart 


```javascript
function createEnableDebugWORestart(session, authorization, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| session |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var session = 'logsession_name';
    var authorization = 'Basic {{BASICAUTH}}';
    var contentType = 'application/x-www-form-urlencoded';

    controller.createEnableDebugWORestart(session, authorization, contentType, function(error, response, context) {

    
    });
```



### <a name="get_classifications"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.getClassifications") getClassifications

> Classifications


```javascript
function getClassifications(authorization, hOST, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var hOST = 'HOST';

    controller.getClassifications(authorization, hOST, function(error, response, context) {

    
    });
```



### <a name="create_company_developer"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.createCompanyDeveloper") createCompanyDeveloper

> Create Company Developer


```javascript
function createCompanyDeveloper(body, contentType, authorization, oRG, cOMPANY, callback)
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

```javascript

    var body = new CreateCompanyDeveloperRequest({"key":"value"});
    var contentType = 'Content-Type';
    var authorization = 'Authorization';
    var oRG = 'ORG';
    var cOMPANY = 'COMPANY';

    controller.createCompanyDeveloper(body, contentType, authorization, oRG, cOMPANY, function(error, response, context) {

    
    });
```



### <a name="get_qpid_metrics"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.getQPIDMetrics") getQPIDMetrics

> QPID Metrics


```javascript
function getQPIDMetrics(authorization, hOST, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var hOST = 'HOST';

    controller.getQPIDMetrics(authorization, hOST, function(error, response, context) {

    
    });
```



### <a name="get_build_info"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.getBuildInfo") getBuildInfo

> Build Info


```javascript
function getBuildInfo(authorization, hOST, pORT, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |
| pORT |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var hOST = 'HOST';
    var pORT = 'PORT';

    controller.getBuildInfo(authorization, hOST, pORT, function(error, response, context) {

    
    });
```



### <a name="delete_disable_debug_wo_restart"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.deleteDisableDebugWORestart") deleteDisableDebugWORestart

> Disable Debug w/o Restart


```javascript
function deleteDisableDebugWORestart(authorization, contentType, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Basic {{BASICAUTH}}';
    var contentType = 'application/x-www-form-urlencoded';

    controller.deleteDisableDebugWORestart(authorization, contentType, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="apps_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AppsController") AppsController

### Get singleton instance

The singleton instance of the ``` AppsController ``` class can be accessed from the API Client.

```javascript
var controller = lib.AppsController;
```

### <a name="create_company_app"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.createCompanyAPP") createCompanyAPP

> Create Company APP


```javascript
function createCompanyAPP(body, authorization, contentType, oRG, cOMPANY, callback)
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

```javascript

    var body = 'Body';
    var authorization = 'Authorization';
    var contentType = 'Content-Type';
    var oRG = 'ORG';
    var cOMPANY = 'COMPANY';

    controller.createCompanyAPP(body, authorization, contentType, oRG, cOMPANY, function(error, response, context) {

    
    });
```



### <a name="add_app_credentials"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.addAppCredentials") addAppCredentials

> Add app credentials


```javascript
function addAppCredentials(body, authorization, contentType, oRG, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = 'Body';
    var authorization = 'Authorization';
    var contentType = 'Content-Type';
    var oRG = 'ORG';

    controller.addAppCredentials(body, authorization, contentType, oRG, function(error, response, context) {

    
    });
```



### <a name="list_apps"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.listApps") listApps

> List apps 


```javascript
function listApps(authorization, oRG, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var oRG = 'ORG';

    controller.listApps(authorization, oRG, function(error, response, context) {

    
    });
```



### <a name="list_app"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.listApp") listApp

> List app


```javascript
function listApp(authorization, oRG, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var oRG = 'ORG';

    controller.listApp(authorization, oRG, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="virtual_hosts_controller"></a>![Class: ](https://apidocs.io/img/class.png ".VirtualHostsController") VirtualHostsController

### Get singleton instance

The singleton instance of the ``` VirtualHostsController ``` class can be accessed from the API Client.

```javascript
var controller = lib.VirtualHostsController;
```

### <a name="list_virtual_hosts"></a>![Method: ](https://apidocs.io/img/method.png ".VirtualHostsController.listVirtualHosts") listVirtualHosts

> List VirtualHosts


```javascript
function listVirtualHosts(authorization, oRG, eNV, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var oRG = 'ORG';
    var eNV = 'ENV';

    controller.listVirtualHosts(authorization, oRG, eNV, function(error, response, context) {

    
    });
```



### <a name="add_virtual_host"></a>![Method: ](https://apidocs.io/img/method.png ".VirtualHostsController.addVirtualHost") addVirtualHost

> Add Virtual Host


```javascript
function addVirtualHost(body, authorization, contentType, oRG, eNV, callback)
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

```javascript

    var body = 'Body';
    var authorization = 'Authorization';
    var contentType = 'Content-Type';
    var oRG = 'ORG';
    var eNV = 'ENV';

    controller.addVirtualHost(body, authorization, contentType, oRG, eNV, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="environments_controller"></a>![Class: ](https://apidocs.io/img/class.png ".EnvironmentsController") EnvironmentsController

### Get singleton instance

The singleton instance of the ``` EnvironmentsController ``` class can be accessed from the API Client.

```javascript
var controller = lib.EnvironmentsController;
```

### <a name="update_environments"></a>![Method: ](https://apidocs.io/img/method.png ".EnvironmentsController.updateEnvironments") updateEnvironments

> Update Environments


```javascript
function updateEnvironments(authorization, contentType, oRG, eNV, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var contentType = 'Content-Type';
    var oRG = 'ORG';
    var eNV = 'ENV';

    controller.updateEnvironments(authorization, contentType, oRG, eNV, function(error, response, context) {

    
    });
```



### <a name="delete_environment"></a>![Method: ](https://apidocs.io/img/method.png ".EnvironmentsController.deleteEnvironment") deleteEnvironment

> Delete Environment


```javascript
function deleteEnvironment(authorization, oRG, eNV, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var oRG = 'ORG';
    var eNV = 'ENV';

    controller.deleteEnvironment(authorization, oRG, eNV, function(error, response, context) {

    
    });
```



### <a name="create_new_env_in_org"></a>![Method: ](https://apidocs.io/img/method.png ".EnvironmentsController.createNewENVInORG") createNewENVInORG

> Create New ENV in ORG


```javascript
function createNewENVInORG(body, authorization, contentType, oRG, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = 'Body';
    var authorization = 'Authorization';
    var contentType = 'Content-Type';
    var oRG = 'ORG';

    controller.createNewENVInORG(body, authorization, contentType, oRG, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="developer_app_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DeveloperAppController") DeveloperAppController

### Get singleton instance

The singleton instance of the ``` DeveloperAppController ``` class can be accessed from the API Client.

```javascript
var controller = lib.DeveloperAppController;
```

### <a name="get_developer_app_details_get"></a>![Method: ](https://apidocs.io/img/method.png ".DeveloperAppController.getDeveloperAppDetailsGet") getDeveloperAppDetailsGet

> Developer App Details Get


```javascript
function getDeveloperAppDetailsGet(authorization, contentType, oRG, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var contentType = 'Content-Type';
    var oRG = 'ORG';

    controller.getDeveloperAppDetailsGet(authorization, contentType, oRG, function(error, response, context) {

    
    });
```



### <a name="delete_app_credentials"></a>![Method: ](https://apidocs.io/img/method.png ".DeveloperAppController.deleteAppCredentials") deleteAppCredentials

> Delete app credentials


```javascript
function deleteAppCredentials(authorization, accept, oRG, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var accept = 'Accept';
    var oRG = 'ORG';

    controller.deleteAppCredentials(authorization, accept, oRG, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="keystores_controller"></a>![Class: ](https://apidocs.io/img/class.png ".KeystoresController") KeystoresController

### Get singleton instance

The singleton instance of the ``` KeystoresController ``` class can be accessed from the API Client.

```javascript
var controller = lib.KeystoresController;
```

### <a name="list_keystores"></a>![Method: ](https://apidocs.io/img/method.png ".KeystoresController.listKeystores") listKeystores

> List Keystores


```javascript
function listKeystores(authorization, oRG, eNV, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var oRG = 'ORG';
    var eNV = 'ENV';

    controller.listKeystores(authorization, oRG, eNV, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="products_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductsController") ProductsController

### Get singleton instance

The singleton instance of the ``` ProductsController ``` class can be accessed from the API Client.

```javascript
var controller = lib.ProductsController;
```

### <a name="get_api_products"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.getApiProducts") getApiProducts

> Api Products


```javascript
function getApiProducts(authorization, oRG, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var oRG = 'ORG';

    controller.getApiProducts(authorization, oRG, function(error, response, context) {

    
    });
```



### <a name="create_ap_iproduct_creation"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.createAPIproductCreation") createAPIproductCreation

> APIproduct Creation


```javascript
function createAPIproductCreation(body, authorization, contentType, oRG, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = 'Body';
    var authorization = 'Authorization';
    var contentType = 'Content-Type';
    var oRG = 'ORG';

    controller.createAPIproductCreation(body, authorization, contentType, oRG, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="target_servers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".TargetServersController") TargetServersController

### Get singleton instance

The singleton instance of the ``` TargetServersController ``` class can be accessed from the API Client.

```javascript
var controller = lib.TargetServersController;
```

### <a name="list_target_servers"></a>![Method: ](https://apidocs.io/img/method.png ".TargetServersController.listTargetServers") listTargetServers

> List Target Servers


```javascript
function listTargetServers(authorization, oRG, eNV, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Authorization';
    var oRG = 'ORG';
    var eNV = 'ENV';

    controller.listTargetServers(authorization, oRG, eNV, function(error, response, context) {

    
    });
```



### <a name="add_target"></a>![Method: ](https://apidocs.io/img/method.png ".TargetServersController.addTarget") addTarget

> Add Target


```javascript
function addTarget(body, contentType, authorization, oRG, eNV, callback)
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

```javascript

    var body = new AddTargetRequest({"key":"value"});
    var contentType = 'content-type';
    var authorization = 'Authorization';
    var oRG = 'ORG';
    var eNV = 'ENV';

    controller.addTarget(body, contentType, authorization, oRG, eNV, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="company_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CompanyController") CompanyController

### Get singleton instance

The singleton instance of the ``` CompanyController ``` class can be accessed from the API Client.

```javascript
var controller = lib.CompanyController;
```

### <a name="create_company"></a>![Method: ](https://apidocs.io/img/method.png ".CompanyController.createCompany") createCompany

> Create Company


```javascript
function createCompany(body, authorization, contentType, oRG, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = 'Body';
    var authorization = 'Authorization';
    var contentType = 'Content-Type';
    var oRG = 'ORG';

    controller.createCompany(body, authorization, contentType, oRG, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="organizations_controller"></a>![Class: ](https://apidocs.io/img/class.png ".OrganizationsController") OrganizationsController

### Get singleton instance

The singleton instance of the ``` OrganizationsController ``` class can be accessed from the API Client.

```javascript
var controller = lib.OrganizationsController;
```

### <a name="list_organizations"></a>![Method: ](https://apidocs.io/img/method.png ".OrganizationsController.listOrganizations") listOrganizations

> List organizations


```javascript
function listOrganizations(authorization, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var authorization = 'Basic {{BASICAUTH}}';

    controller.listOrganizations(authorization, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)




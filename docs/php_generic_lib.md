# Getting started

TODO: Add Description

## How to Build

The generated code has dependencies over external libraries like UniRest. These dependencies are defined in the ```composer.json``` file that comes with the SDK. 
To resolve these dependencies, we use the Composer package manager which requires PHP greater than 5.3.2 installed in your system. 
Visit [https://getcomposer.org/download/](https://getcomposer.org/download/) to download the installer file for Composer and run it in your system. 
Open command prompt and type ```composer --version```. This should display the current version of the Composer installed if the installation was successful.

* Using command line, navigate to the directory containing the generated files (including ```composer.json```) for the SDK. 
* Run the command ```composer install```. This should install all the required dependencies and create the ```vendor``` directory in your project directory.

![Building SDK - Step 1](https://apidocs.io/illustration/php?step=installDependencies&workspaceFolder=Apigee%20Edge%20API%20Management-PHP)

### [For Windows Users Only] Configuring CURL Certificate Path in php.ini

CURL used to include a list of accepted CAs, but no longer bundles ANY CA certs. So by default it will reject all SSL certificates as unverifiable. You will have to get your CA's cert and point curl at it. The steps are as follows:

1. Download the certificate bundle (.pem file) from [https://curl.haxx.se/docs/caextract.html](https://curl.haxx.se/docs/caextract.html) on to your system.
2. Add curl.cainfo = "PATH_TO/cacert.pem" to your php.ini file located in your php installation. “PATH_TO” must be an absolute path containing the .pem file.

```ini
[curl]
; A default value for the CURLOPT_CAINFO option. This is required to be an
; absolute path.
;curl.cainfo =
```

## How to Use

The following section explains how to use the ApigeeEdgeAPIManagement library in a new project.

### 1. Open Project in an IDE

Open an IDE for PHP like PhpStorm. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

![Open project in PHPStorm - Step 1](https://apidocs.io/illustration/php?step=openIDE&workspaceFolder=Apigee%20Edge%20API%20Management-PHP)

Click on ```Open``` in PhpStorm to browse to your generated SDK directory and then click ```OK```.

![Open project in PHPStorm - Step 2](https://apidocs.io/illustration/php?step=openProject0&workspaceFolder=Apigee%20Edge%20API%20Management-PHP)     

### 2. Add a new Test Project

Create a new directory by right clicking on the solution name as shown below:

![Add a new project in PHPStorm - Step 1](https://apidocs.io/illustration/php?step=createDirectory&workspaceFolder=Apigee%20Edge%20API%20Management-PHP)

Name the directory as "test"

![Add a new project in PHPStorm - Step 2](https://apidocs.io/illustration/php?step=nameDirectory&workspaceFolder=Apigee%20Edge%20API%20Management-PHP)
   
Add a PHP file to this project

![Add a new project in PHPStorm - Step 3](https://apidocs.io/illustration/php?step=createFile&workspaceFolder=Apigee%20Edge%20API%20Management-PHP)

Name it "testSDK"

![Add a new project in PHPStorm - Step 4](https://apidocs.io/illustration/php?step=nameFile&workspaceFolder=Apigee%20Edge%20API%20Management-PHP)

Depending on your project setup, you might need to include composer's autoloader in your PHP code to enable auto loading of classes.

```PHP
require_once "../vendor/autoload.php";
```

It is important that the path inside require_once correctly points to the file ```autoload.php``` inside the vendor directory created during dependency installations.

![Add a new project in PHPStorm - Step 4](https://apidocs.io/illustration/php?step=projectFiles&workspaceFolder=Apigee%20Edge%20API%20Management-PHP)

After this you can add code to initialize the client library and acquire the instance of a Controller class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

### 3. Run the Test Project

To run your project you must set the Interpreter for your project. Interpreter is the PHP engine installed on your computer.

Open ```Settings``` from ```File``` menu.

![Run Test Project - Step 1](https://apidocs.io/illustration/php?step=openSettings&workspaceFolder=Apigee%20Edge%20API%20Management-PHP)

Select ```PHP``` from within ```Languages & Frameworks```

![Run Test Project - Step 2](https://apidocs.io/illustration/php?step=setInterpreter0&workspaceFolder=Apigee%20Edge%20API%20Management-PHP)

Browse for Interpreters near the ```Interpreter``` option and choose your interpreter.

![Run Test Project - Step 3](https://apidocs.io/illustration/php?step=setInterpreter1&workspaceFolder=Apigee%20Edge%20API%20Management-PHP)

Once the interpreter is selected, click ```OK```

![Run Test Project - Step 4](https://apidocs.io/illustration/php?step=setInterpreter2&workspaceFolder=Apigee%20Edge%20API%20Management-PHP)

To run your project, right click on your PHP file inside your Test project and click on ```Run```

![Run Test Project - Step 5](https://apidocs.io/illustration/php?step=runProject&workspaceFolder=Apigee%20Edge%20API%20Management-PHP)

## How to Test

Unit tests in this SDK can be run using PHPUnit. 

1. First install the dependencies using composer including the `require-dev` dependencies.
2. Run `vendor\bin\phpunit --verbose` from commandline to execute tests. If you have 
   installed PHPUnit globally, run tests using `phpunit --verbose` instead.

You can change the PHPUnit test configuration in the `phpunit.xml` file.

## Initialization

### Authentication
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| basicAuthUserName | The username to use with basic authentication |
| basicAuthPassword | The password to use with basic authentication |



API client can be initialized as following.

```php
$basicAuthUserName = 'basicAuthUserName'; // The username to use with basic authentication
$basicAuthPassword = 'basicAuthPassword'; // The password to use with basic authentication

$client = new ApigeeEdgeAPIManagementLib\ApigeeEdgeAPIManagementClient($basicAuthUserName, $basicAuthPassword);
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

```php
$deployments = $client->getDeployments();
```

### <a name="list_deployments"></a>![Method: ](https://apidocs.io/img/method.png ".DeploymentsController.listDeployments") listDeployments

> List Deployments


```php
function listDeployments(
        $authorization,
        $oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$oRG = 'ORG';

$deployments->listDeployments($authorization, $oRG);

```


### <a name="get_deployments"></a>![Method: ](https://apidocs.io/img/method.png ".DeploymentsController.getDeployments") getDeployments

> Deployments


```php
function getDeployments(
        $authorization,
        $oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$oRG = 'ORG';

$deployments->getDeployments($authorization, $oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="user_roles_controller"></a>![Class: ](https://apidocs.io/img/class.png ".UserRolesController") UserRolesController

### Get singleton instance

The singleton instance of the ``` UserRolesController ``` class can be accessed from the API Client.

```php
$userRoles = $client->getUserRoles();
```

### <a name="create_user_roles_update"></a>![Method: ](https://apidocs.io/img/method.png ".UserRolesController.createUserRolesUpdate") createUserRolesUpdate

> User Roles Update


```php
function createUserRolesUpdate(
        $body,
        $authorization,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$bodyValue = "{ \"role\" : [ { \"name\" : \"orgadmin\", \"organization\" : \"dev\" }, { \"name\" : \"sysadmin\" } ] }";
$body = APIHelper::deserialize($bodyValue);
$authorization = 'Basic {{BASICAUTH}}';
$contentType = 'application/json';

$userRoles->createUserRolesUpdate($body, $authorization, $contentType);

```


### <a name="delete_an_organization_userrole"></a>![Method: ](https://apidocs.io/img/method.png ".UserRolesController.deleteAnOrganizationUserrole") deleteAnOrganizationUserrole

> Delete an organization userrole


```php
function deleteAnOrganizationUserrole(
        $org,
        $authorization,
        $accept)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| org |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$org = '{{ORG}}';
$authorization = 'Basic {{BASICAUTH}}';
$accept = 'application/json';

$userRoles->deleteAnOrganizationUserrole($org, $authorization, $accept);

```


### <a name="get_permissions_for_a_role"></a>![Method: ](https://apidocs.io/img/method.png ".UserRolesController.getPermissionsForARole") getPermissionsForARole

> Get permissions for a role


```php
function getPermissionsForARole(
        $authorization,
        $contentType,
        $oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$contentType = 'Content-Type';
$oRG = 'ORG';

$userRoles->getPermissionsForARole($authorization, $contentType, $oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="o_auth_controller"></a>![Class: ](https://apidocs.io/img/class.png ".OAuthController") OAuthController

### Get singleton instance

The singleton instance of the ``` OAuthController ``` class can be accessed from the API Client.

```php
$oAuth = $client->getOAuth();
```

### <a name="get_o_auth2_token_details_get"></a>![Method: ](https://apidocs.io/img/method.png ".OAuthController.getOAuth2TokenDetailsGet") getOAuth2TokenDetailsGet

> OAuth2 Token Details Get


```php
function getOAuth2TokenDetailsGet(
        $authorization,
        $contentType,
        $oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$contentType = 'Content-Type';
$oRG = 'ORG';

$oAuth->getOAuth2TokenDetailsGet($authorization, $contentType, $oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="kvm_controller"></a>![Class: ](https://apidocs.io/img/class.png ".KVMController") KVMController

### Get singleton instance

The singleton instance of the ``` KVMController ``` class can be accessed from the API Client.

```php
$kVM = $client->getKVM();
```

### <a name="get_kvm_get"></a>![Method: ](https://apidocs.io/img/method.png ".KVMController.getKVMGet") getKVMGet

> KVM Get


```php
function getKVMGet(
        $authorization,
        $contentType,
        $oRG,
        $eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$contentType = 'Content-Type';
$oRG = 'ORG';
$eNV = 'ENV';

$kVM->getKVMGet($authorization, $contentType, $oRG, $eNV);

```


### <a name="delete_kvm_delete_entire_kvm"></a>![Method: ](https://apidocs.io/img/method.png ".KVMController.deleteKVMDeleteEntireKVM") deleteKVMDeleteEntireKVM

> KVM Delete (Entire KVM)


```php
function deleteKVMDeleteEntireKVM(
        $authorization,
        $contentType,
        $oRG,
        $eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$contentType = 'Content-Type';
$oRG = 'ORG';
$eNV = 'ENV';

$kVM->deleteKVMDeleteEntireKVM($authorization, $contentType, $oRG, $eNV);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="pods_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PodsController") PodsController

### Get singleton instance

The singleton instance of the ``` PodsController ``` class can be accessed from the API Client.

```php
$pods = $client->getPods();
```

### <a name="get_analytics_pod"></a>![Method: ](https://apidocs.io/img/method.png ".PodsController.getAnalyticsPod") getAnalyticsPod

> Analytics pod


```php
function getAnalyticsPod(
        $pod,
        $authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| pod |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$pod = 'analytics';
$authorization = 'Basic {{BASICAUTH}}';

$pods->getAnalyticsPod($pod, $authorization);

```


### <a name="get_associated_pods"></a>![Method: ](https://apidocs.io/img/method.png ".PodsController.getAssociatedPods") getAssociatedPods

> Get Associated  Pods


```php
function getAssociatedPods(
        $contentType,
        $authorization,
        $oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$contentType = 'Content-Type';
$authorization = 'Authorization';
$oRG = 'ORG';

$pods->getAssociatedPods($contentType, $authorization, $oRG);

```


### <a name="create_disassociate_org_from_pod"></a>![Method: ](https://apidocs.io/img/method.png ".PodsController.createDisassociateOrgFromPOD") createDisassociateOrgFromPOD

> Disassociate Org from POD


```php
function createDisassociateOrgFromPOD(
        $contentType,
        $authorization,
        $oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$contentType = 'Content-Type';
$authorization = 'Authorization';
$oRG = 'ORG';

$pods->createDisassociateOrgFromPOD($contentType, $authorization, $oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="servers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ServersController") ServersController

### Get singleton instance

The singleton instance of the ``` ServersController ``` class can be accessed from the API Client.

```php
$servers = $client->getServers();
```

### <a name="create_deregister"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.createDeregister") createDeregister

> Deregister


```php
function createDeregister(
        $authorization,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Basic {{BASICAUTH}}';
$contentType = 'application/x-www-form-urlencoded';

$servers->createDeregister($authorization, $contentType);

```


### <a name="list_server_by_uuid"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.listServerByUUID") listServerByUUID

> List Server by UUID


```php
function listServerByUUID(
        $authorization,
        $uuid)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| uuid |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Basic {{BASICAUTH}}';
$uuid = 'uuid';

$servers->listServerByUUID($authorization, $uuid);

```


### <a name="create_set_not_reachable"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.createSetNotReachable") createSetNotReachable

> Set not reachable


```php
function createSetNotReachable(
        $reachable,
        $authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| reachable |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$reachable = 'false';
$authorization = 'Basic {{BASICAUTH}}';

$servers->createSetNotReachable($reachable, $authorization);

```


### <a name="list_org_env_servers"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.listOrgEnvServers") listOrgEnvServers

> List org/env servers


```php
function listOrgEnvServers(
        $authorization,
        $oRG,
        $eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$oRG = 'ORG';
$eNV = 'ENV';

$servers->listOrgEnvServers($authorization, $oRG, $eNV);

```


### <a name="create_register_server_with_org"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.createRegisterServerWithOrg") createRegisterServerWithOrg

> Register server with org


```php
function createRegisterServerWithOrg(
        $authorization,
        $contentType,
        $oRG,
        $eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$contentType = 'Content-Type';
$oRG = 'ORG';
$eNV = 'ENV';

$servers->createRegisterServerWithOrg($authorization, $contentType, $oRG, $eNV);

```


### <a name="create_associate_environments_to_mp"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.createAssociateEnvironmentsToMP") createAssociateEnvironmentsToMP

> Associate  environments to MP


```php
function createAssociateEnvironmentsToMP(
        $authorization,
        $contentType,
        $oRG,
        $eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$contentType = 'Content-Type';
$oRG = 'ORG';
$eNV = 'ENV';

$servers->createAssociateEnvironmentsToMP($authorization, $contentType, $oRG, $eNV);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="developers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DevelopersController") DevelopersController

### Get singleton instance

The singleton instance of the ``` DevelopersController ``` class can be accessed from the API Client.

```php
$developers = $client->getDevelopers();
```

### <a name="get_developers"></a>![Method: ](https://apidocs.io/img/method.png ".DevelopersController.getDevelopers") getDevelopers

> Get Developers


```php
function getDevelopers(
        $authorization,
        $contentType,
        $oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$contentType = 'Content-Type';
$oRG = 'ORG';

$developers->getDevelopers($authorization, $contentType, $oRG);

```


### <a name="create_developer"></a>![Method: ](https://apidocs.io/img/method.png ".DevelopersController.createDeveloper") createDeveloper

> Create Developer


```php
function createDeveloper(
        $body,
        $authorization,
        $contentType,
        $oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = 'Body';
$authorization = 'Authorization';
$contentType = 'Content-Type';
$oRG = 'ORG';

$developers->createDeveloper($body, $authorization, $contentType, $oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="ap_is_controller"></a>![Class: ](https://apidocs.io/img/class.png ".APIsController") APIsController

### Get singleton instance

The singleton instance of the ``` APIsController ``` class can be accessed from the API Client.

```php
$aPIs = $client->getAPIs();
```

### <a name="get_api_list"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.getApiList") getApiList

> Api list


```php
function getApiList(
        $authorization,
        $oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$oRG = 'ORG';

$aPIs->getApiList($authorization, $oRG);

```


### <a name="create_deploy_api"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.createDeployAPI") createDeployAPI

> Deploy API


```php
function createDeployAPI(
        $action,
        $name,
        $authorization,
        $contentType,
        $oRG)
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

```php
$action = 'action';
$name = 'name';
$authorization = 'Authorization';
$contentType = 'Content-Type';
$oRG = 'ORG';

$aPIs->createDeployAPI($action, $name, $authorization, $contentType, $oRG);

```


### <a name="delete_an_api"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.deleteAnAPI") deleteAnAPI

> Delete an API


```php
function deleteAnAPI(
        $authorization,
        $oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$oRG = 'ORG';

$aPIs->deleteAnAPI($authorization, $oRG);

```


### <a name="create_undeploy_revisions"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.createUndeployRevisions") createUndeployRevisions

> Undeploy Revisions


```php
function createUndeployRevisions(
        $action,
        $env,
        $authorization,
        $contentType,
        $oRG)
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

```php
$action = 'action';
$env = 'env';
$authorization = 'Authorization';
$contentType = 'Content-Type';
$oRG = 'ORG';

$aPIs->createUndeployRevisions($action, $env, $authorization, $contentType, $oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="cache_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CacheController") CacheController

### Get singleton instance

The singleton instance of the ``` CacheController ``` class can be accessed from the API Client.

```php
$cache = $client->getCache();
```

### <a name="list_caches"></a>![Method: ](https://apidocs.io/img/method.png ".CacheController.listCaches") listCaches

> List caches


```php
function listCaches(
        $authorization,
        $oRG,
        $eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$oRG = 'ORG';
$eNV = 'ENV';

$cache->listCaches($authorization, $oRG, $eNV);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="audit_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AuditController") AuditController

### Get singleton instance

The singleton instance of the ``` AuditController ``` class can be accessed from the API Client.

```php
$audit = $client->getAudit();
```

### <a name="get_audit"></a>![Method: ](https://apidocs.io/img/method.png ".AuditController.getAudit") getAudit

> Audit


```php
function getAudit(
        $expand,
        $timeline,
        $authorization,
        $oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| expand |  ``` Required ```  | TODO: Add a parameter description |
| timeline |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$expand = true;
$timeline = 'timeline';
$authorization = 'Authorization';
$oRG = 'ORG';

$audit->getAudit($expand, $timeline, $authorization, $oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="users_controller"></a>![Class: ](https://apidocs.io/img/class.png ".UsersController") UsersController

### Get singleton instance

The singleton instance of the ``` UsersController ``` class can be accessed from the API Client.

```php
$users = $client->getUsers();
```

### <a name="get_developer_details_get"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.getDeveloperDetailsGet") getDeveloperDetailsGet

> Developer Details Get


```php
function getDeveloperDetailsGet(
        $authorization,
        $contentType,
        $oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$contentType = 'Content-Type';
$oRG = 'ORG';

$users->getDeveloperDetailsGet($authorization, $contentType, $oRG);

```


### <a name="create_user_in_org"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.createUserInORG") createUserInORG

> Create User in ORG


```php
function createUserInORG(
        $body,
        $authorization,
        $contentType,
        $oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = 'Body';
$authorization = 'Authorization';
$contentType = 'Content-Type';
$oRG = 'ORG';

$users->createUserInORG($body, $authorization, $contentType, $oRG);

```


### <a name="list_users"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.listUsers") listUsers

> List Users


```php
function listUsers($authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Basic {{BASICAUTH}}';

$users->listUsers($authorization);

```


### <a name="add_user_as_orgadmin"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.addUserAsOrgadmin") addUserAsOrgadmin

> Add user as Orgadmin


```php
function addUserAsOrgadmin(
        $body,
        $authorization,
        $contentType,
        $oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = 'Body';
$authorization = 'Authorization';
$contentType = 'Content-Type';
$oRG = 'ORG';

$users->addUserAsOrgadmin($body, $authorization, $contentType, $oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="zzz_others_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ZzzOthersController") ZzzOthersController

### Get singleton instance

The singleton instance of the ``` ZzzOthersController ``` class can be accessed from the API Client.

```php
$zzzOthers = $client->getZzzOthers();
```

### <a name="get_cluster_status"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.getClusterStatus") getClusterStatus

> Cluster Status


```php
function getClusterStatus($authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Basic {{BASICAUTH}}';

$zzzOthers->getClusterStatus($authorization);

```


### <a name="create_enable_debug_wo_restart"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.createEnableDebugWORestart") createEnableDebugWORestart

> Enable Debug w/o Restart 


```php
function createEnableDebugWORestart(
        $session,
        $authorization,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| session |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$session = 'logsession_name';
$authorization = 'Basic {{BASICAUTH}}';
$contentType = 'application/x-www-form-urlencoded';

$zzzOthers->createEnableDebugWORestart($session, $authorization, $contentType);

```


### <a name="get_classifications"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.getClassifications") getClassifications

> Classifications


```php
function getClassifications(
        $authorization,
        $hOST)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$hOST = 'HOST';

$zzzOthers->getClassifications($authorization, $hOST);

```


### <a name="create_company_developer"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.createCompanyDeveloper") createCompanyDeveloper

> Create Company Developer


```php
function createCompanyDeveloper(
        $body,
        $contentType,
        $authorization,
        $oRG,
        $cOMPANY)
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

```php
$body = new CreateCompanyDeveloperRequest();
$contentType = 'Content-Type';
$authorization = 'Authorization';
$oRG = 'ORG';
$cOMPANY = 'COMPANY';

$zzzOthers->createCompanyDeveloper($body, $contentType, $authorization, $oRG, $cOMPANY);

```


### <a name="get_qpid_metrics"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.getQPIDMetrics") getQPIDMetrics

> QPID Metrics


```php
function getQPIDMetrics(
        $authorization,
        $hOST)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$hOST = 'HOST';

$zzzOthers->getQPIDMetrics($authorization, $hOST);

```


### <a name="get_build_info"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.getBuildInfo") getBuildInfo

> Build Info


```php
function getBuildInfo(
        $authorization,
        $hOST,
        $pORT)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |
| pORT |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$hOST = 'HOST';
$pORT = 'PORT';

$zzzOthers->getBuildInfo($authorization, $hOST, $pORT);

```


### <a name="delete_disable_debug_wo_restart"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.deleteDisableDebugWORestart") deleteDisableDebugWORestart

> Disable Debug w/o Restart


```php
function deleteDisableDebugWORestart(
        $authorization,
        $contentType)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Basic {{BASICAUTH}}';
$contentType = 'application/x-www-form-urlencoded';

$zzzOthers->deleteDisableDebugWORestart($authorization, $contentType);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="apps_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AppsController") AppsController

### Get singleton instance

The singleton instance of the ``` AppsController ``` class can be accessed from the API Client.

```php
$apps = $client->getApps();
```

### <a name="create_company_app"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.createCompanyAPP") createCompanyAPP

> Create Company APP


```php
function createCompanyAPP(
        $body,
        $authorization,
        $contentType,
        $oRG,
        $cOMPANY)
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

```php
$body = 'Body';
$authorization = 'Authorization';
$contentType = 'Content-Type';
$oRG = 'ORG';
$cOMPANY = 'COMPANY';

$apps->createCompanyAPP($body, $authorization, $contentType, $oRG, $cOMPANY);

```


### <a name="add_app_credentials"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.addAppCredentials") addAppCredentials

> Add app credentials


```php
function addAppCredentials(
        $body,
        $authorization,
        $contentType,
        $oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = 'Body';
$authorization = 'Authorization';
$contentType = 'Content-Type';
$oRG = 'ORG';

$apps->addAppCredentials($body, $authorization, $contentType, $oRG);

```


### <a name="list_apps"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.listApps") listApps

> List apps 


```php
function listApps(
        $authorization,
        $oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$oRG = 'ORG';

$apps->listApps($authorization, $oRG);

```


### <a name="list_app"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.listApp") listApp

> List app


```php
function listApp(
        $authorization,
        $oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$oRG = 'ORG';

$apps->listApp($authorization, $oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="virtual_hosts_controller"></a>![Class: ](https://apidocs.io/img/class.png ".VirtualHostsController") VirtualHostsController

### Get singleton instance

The singleton instance of the ``` VirtualHostsController ``` class can be accessed from the API Client.

```php
$virtualHosts = $client->getVirtualHosts();
```

### <a name="list_virtual_hosts"></a>![Method: ](https://apidocs.io/img/method.png ".VirtualHostsController.listVirtualHosts") listVirtualHosts

> List VirtualHosts


```php
function listVirtualHosts(
        $authorization,
        $oRG,
        $eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$oRG = 'ORG';
$eNV = 'ENV';

$virtualHosts->listVirtualHosts($authorization, $oRG, $eNV);

```


### <a name="add_virtual_host"></a>![Method: ](https://apidocs.io/img/method.png ".VirtualHostsController.addVirtualHost") addVirtualHost

> Add Virtual Host


```php
function addVirtualHost(
        $body,
        $authorization,
        $contentType,
        $oRG,
        $eNV)
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

```php
$body = 'Body';
$authorization = 'Authorization';
$contentType = 'Content-Type';
$oRG = 'ORG';
$eNV = 'ENV';

$virtualHosts->addVirtualHost($body, $authorization, $contentType, $oRG, $eNV);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="environments_controller"></a>![Class: ](https://apidocs.io/img/class.png ".EnvironmentsController") EnvironmentsController

### Get singleton instance

The singleton instance of the ``` EnvironmentsController ``` class can be accessed from the API Client.

```php
$environments = $client->getEnvironments();
```

### <a name="update_environments"></a>![Method: ](https://apidocs.io/img/method.png ".EnvironmentsController.updateEnvironments") updateEnvironments

> Update Environments


```php
function updateEnvironments(
        $authorization,
        $contentType,
        $oRG,
        $eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$contentType = 'Content-Type';
$oRG = 'ORG';
$eNV = 'ENV';

$environments->updateEnvironments($authorization, $contentType, $oRG, $eNV);

```


### <a name="delete_environment"></a>![Method: ](https://apidocs.io/img/method.png ".EnvironmentsController.deleteEnvironment") deleteEnvironment

> Delete Environment


```php
function deleteEnvironment(
        $authorization,
        $oRG,
        $eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$oRG = 'ORG';
$eNV = 'ENV';

$environments->deleteEnvironment($authorization, $oRG, $eNV);

```


### <a name="create_new_env_in_org"></a>![Method: ](https://apidocs.io/img/method.png ".EnvironmentsController.createNewENVInORG") createNewENVInORG

> Create New ENV in ORG


```php
function createNewENVInORG(
        $body,
        $authorization,
        $contentType,
        $oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = 'Body';
$authorization = 'Authorization';
$contentType = 'Content-Type';
$oRG = 'ORG';

$environments->createNewENVInORG($body, $authorization, $contentType, $oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="developer_app_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DeveloperAppController") DeveloperAppController

### Get singleton instance

The singleton instance of the ``` DeveloperAppController ``` class can be accessed from the API Client.

```php
$developerApp = $client->getDeveloperApp();
```

### <a name="get_developer_app_details_get"></a>![Method: ](https://apidocs.io/img/method.png ".DeveloperAppController.getDeveloperAppDetailsGet") getDeveloperAppDetailsGet

> Developer App Details Get


```php
function getDeveloperAppDetailsGet(
        $authorization,
        $contentType,
        $oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$contentType = 'Content-Type';
$oRG = 'ORG';

$developerApp->getDeveloperAppDetailsGet($authorization, $contentType, $oRG);

```


### <a name="delete_app_credentials"></a>![Method: ](https://apidocs.io/img/method.png ".DeveloperAppController.deleteAppCredentials") deleteAppCredentials

> Delete app credentials


```php
function deleteAppCredentials(
        $authorization,
        $accept,
        $oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$accept = 'Accept';
$oRG = 'ORG';

$developerApp->deleteAppCredentials($authorization, $accept, $oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="keystores_controller"></a>![Class: ](https://apidocs.io/img/class.png ".KeystoresController") KeystoresController

### Get singleton instance

The singleton instance of the ``` KeystoresController ``` class can be accessed from the API Client.

```php
$keystores = $client->getKeystores();
```

### <a name="list_keystores"></a>![Method: ](https://apidocs.io/img/method.png ".KeystoresController.listKeystores") listKeystores

> List Keystores


```php
function listKeystores(
        $authorization,
        $oRG,
        $eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$oRG = 'ORG';
$eNV = 'ENV';

$keystores->listKeystores($authorization, $oRG, $eNV);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="products_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductsController") ProductsController

### Get singleton instance

The singleton instance of the ``` ProductsController ``` class can be accessed from the API Client.

```php
$products = $client->getProducts();
```

### <a name="get_api_products"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.getApiProducts") getApiProducts

> Api Products


```php
function getApiProducts(
        $authorization,
        $oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$oRG = 'ORG';

$products->getApiProducts($authorization, $oRG);

```


### <a name="create_ap_iproduct_creation"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.createAPIproductCreation") createAPIproductCreation

> APIproduct Creation


```php
function createAPIproductCreation(
        $body,
        $authorization,
        $contentType,
        $oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = 'Body';
$authorization = 'Authorization';
$contentType = 'Content-Type';
$oRG = 'ORG';

$products->createAPIproductCreation($body, $authorization, $contentType, $oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="target_servers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".TargetServersController") TargetServersController

### Get singleton instance

The singleton instance of the ``` TargetServersController ``` class can be accessed from the API Client.

```php
$targetServers = $client->getTargetServers();
```

### <a name="list_target_servers"></a>![Method: ](https://apidocs.io/img/method.png ".TargetServersController.listTargetServers") listTargetServers

> List Target Servers


```php
function listTargetServers(
        $authorization,
        $oRG,
        $eNV)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Authorization';
$oRG = 'ORG';
$eNV = 'ENV';

$targetServers->listTargetServers($authorization, $oRG, $eNV);

```


### <a name="add_target"></a>![Method: ](https://apidocs.io/img/method.png ".TargetServersController.addTarget") addTarget

> Add Target


```php
function addTarget(
        $body,
        $contentType,
        $authorization,
        $oRG,
        $eNV)
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

```php
$body = new AddTargetRequest();
$contentType = 'content-type';
$authorization = 'Authorization';
$oRG = 'ORG';
$eNV = 'ENV';

$targetServers->addTarget($body, $contentType, $authorization, $oRG, $eNV);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="company_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CompanyController") CompanyController

### Get singleton instance

The singleton instance of the ``` CompanyController ``` class can be accessed from the API Client.

```php
$company = $client->getCompany();
```

### <a name="create_company"></a>![Method: ](https://apidocs.io/img/method.png ".CompanyController.createCompany") createCompany

> Create Company


```php
function createCompany(
        $body,
        $authorization,
        $contentType,
        $oRG)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = 'Body';
$authorization = 'Authorization';
$contentType = 'Content-Type';
$oRG = 'ORG';

$company->createCompany($body, $authorization, $contentType, $oRG);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="organizations_controller"></a>![Class: ](https://apidocs.io/img/class.png ".OrganizationsController") OrganizationsController

### Get singleton instance

The singleton instance of the ``` OrganizationsController ``` class can be accessed from the API Client.

```php
$organizations = $client->getOrganizations();
```

### <a name="list_organizations"></a>![Method: ](https://apidocs.io/img/method.png ".OrganizationsController.listOrganizations") listOrganizations

> List organizations


```php
function listOrganizations($authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$authorization = 'Basic {{BASICAUTH}}';

$organizations->listOrganizations($authorization);

```


[Back to List of Controllers](#list_of_controllers)




# Getting started

TODO: Add Description

## How to Build

The generated SDK requires AngularJS framework to work. If you do not already have angular downloaded, please go ahead and do it from [here](https://angularjs.org/).
If any of your models have `Date` or `Datetime` type fields or your endpoints have `Date`/`Datetime` type response, you will need to download and link [angular-moment](https://cdnjs.cloudflare.com/ajax/libs/angular-moment/1.0.1/angular-moment.min.js) and [moment.js](https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.17.1/moment.min.js) with your project.

## How to Use

The following section describes how to use the generated SDK in an existing/new project.

### 1. Configure Angular and Generated SDK
Perform the following steps to configure angular and the SDK:
+ Make a `scripts` folder inside the root folder of the project. If you already have a `scripts` folder, skip to the next step.
+ Move the `angular.min.js` file inside the scripts folder. 
+ Move the `ApigeeEdgeAPIManagementLib` folder inside the scripts folder.
+ If any of the Custom Types in your API have `Date`/`Datetime` type fields or any endpoint has `Date`/`Datetime` response, you will need to download angular-moment and moment.js. Move these 2 files into the `scripts` folder as well.

![folder-structure-image](https://apidocs.io/illustration/angularjs?step=folderStructure&workspaceFolder=Apigee%20Edge%20API%20Management-Angular&projectName=ApigeeEdgeAPIManagementLib)

### 2. Open Project Folder
Open an IDE/Text Editor for JavaScript like Sublime Text. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.  
Click on `File` and select `Open Folder`

Select the folder of your SDK and click on `Select Folder` to open it up in Sublime Text. The folder will become visible in the bar on the left.

![open-folder-image](https://apidocs.io/illustration/angularjs?step=openFolder&workspaceFolder=Apigee%20Edge%20API%20Management-Angular)

### 3. Create an Angular Application
Since Angular JS is used for client-side web development, in order to use the generated library, you will have to develop an application first.
If you already have an angular application, [skip to Step 6](#6-include-sdk-references-in-html-file). Otherwise, follow these steps to create one:

+ In the IDE, click on `File` and choose `New File` to create a new file.
+ Add the following starting code in the file:
```js
var app = angular.module('myApp', []);
app.controller('testController', function($scope) 
{

});
```
+ Save it with the name `app.js` in the `scripts` folder.


### 4. Create HTML File
Skip to the next step if you are working with an existing project and already have an html file. Otherwise follow the steps to create one:
+ Inside the IDE, right click on the project folder name and select the `New File` option to create a new test file.
+ Save it with an appropriate name such as `index.html` in the root of your project folder.
`index.html` should look like this:
```html
<!DOCTYPE html>
<html>
<head>
	<title>Angular Project</title>
	<script></script>
</head>

<body>
</body>

</html>
```

![initial-html-code-image](https://apidocs.io/illustration/angularjs?step=initialCode&workspaceFolder=Apigee%20Edge%20API%20Management-Angular)

### 5. Including links to Angular in HTML file
Your HTML file needs to have a link to `angular.min.js` file to use Angular-JS. Add the link using `script` tags inside the `head` section of `index.html` like:
```html
<script src="scripts/angular.min.js" ></script>
```
If any of the Custom Types that you have defined have `Date`/`Datetime` type fields or any endpoint has `Date`/`Datetime` response, you will also need to link to angular-moment and moment.js like:
```html
<script src="scripts/angular.min.js" ></script>
<script src="scripts/moment.min.js" ></script>
<script src="scripts/angular-moment.min.js" ></script>
```

### 6. Include SDK references in HTML file
Import the reference to the generated SDK files inside your html file like:
```html
<head>
    ...
    <!-- Helper files -->
    <script src="scripts/ApigeeEdgeAPIManagementLib/Module.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Configuration.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/ModelFactory.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/ObjectMapper.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/APIHelper.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Http/Client/HttpContext.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Http/Client/RequestClient.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Http/Request/HttpRequest.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Http/Response/HttpResponse.js"></script>

    <!-- API Controllers -->
    <script src="scripts/ApigeeEdgeAPIManagementLib/Controllers/BaseController.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Controllers/DeploymentsController.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Controllers/UserRolesController.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Controllers/OAuthController.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Controllers/KVMController.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Controllers/PodsController.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Controllers/ServersController.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Controllers/DevelopersController.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Controllers/APIsController.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Controllers/CacheController.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Controllers/AuditController.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Controllers/UsersController.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Controllers/ZzzOthersController.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Controllers/AppsController.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Controllers/VirtualHostsController.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Controllers/EnvironmentsController.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Controllers/DeveloperAppController.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Controllers/KeystoresController.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Controllers/ProductsController.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Controllers/TargetServersController.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Controllers/CompanyController.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Controllers/OrganizationsController.js"></script>


    <!-- Models -->
    <script src="scripts/ApigeeEdgeAPIManagementLib/Models/BaseModel.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Models/UserRolesUpdateRequest.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Models/Role.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Models/CreateCompanyDeveloperRequest.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Models/Developer.js"></script>
    <script src="scripts/ApigeeEdgeAPIManagementLib/Models/AddTargetRequest.js"></script>

    ...
</head>
```
> The `Module.js` file should be imported before the other files. After `Module.js`, `Configuration.js` should be imported.
> The `ModelFactory.js` file is needed by `ObjectMapper.js` file. The `ObjectMapper` in turn, is needed by `BaseController.js`.

### 7. Including link to `app.js` in HTML file
Link your `app.js` file to your `index.html` file like:
```html
<head>
	...
	<script src="scripts/app.js"></script>
</head>
```
> The link to app.js needs to be included at the very end of the head tag, after the SDK references have been added

### 8. Initializing the Angular App
You need to initialize your app and the controller associated with your view inside your `index.html` file. Do so like:
+ Add ng-app directive to initialize your app inside the `body` tag.
```html
<body ng-app="myApp">
```
+ Add ng-controller directive to initialize your controller and bind it with your view (`index.html` file).
```html
...
<body ng-app="myApp">
	<div ng-controller="testController">
		...
	</div>
	...
</body>
...
```

### 9. Consuming the SDK 
In order to use the generated SDK's modules, controllers and factories, the project needs to be added as a dependency in your angular app's module. This will be done inside the `app.js` file.
Add the dependency like this:

```js
var app = angular.module('myApp', ['ApigeeEdgeAPIManagementLib']);
```
At this point, the SDK has been successfully included in your project. Further steps include using a service/factory from the generated SDK. To see working example of this, please head on [over here](#list-of-controllers) and choose any class to see its functions and example usage.  

### 10. Running The App
To run the app, simply open up the `index.html` file in a browser.

![app-running](https://apidocs.io/illustration/angularjs?step=appRunning)

## Initialization


The Angular Application can be initialized as following:
```JavaScript
var app = angular.module('myApp', [ApigeeEdgeAPIManagementLib]);
// now controllers/services can be created which import
// the factories provided by the sdk
```
### Authentication
In order to setup authentication and initialization of the Angular App, you need the following information.

| Parameter | Description |
|-----------|-------------|
| basicAuthUserName | The username to use with basic authentication |
| basicAuthPassword | The password to use with basic authentication |



```JavaScript
var app = angular.module('myApp', [ApigeeEdgeAPIManagementLib]);
app.factory('config', function($scope, Configuration) 
{
    return {
        setConfigVars: function() {
            // Configuration parameters and credentials
            Configuration.basicAuthUserName = 'basicAuthUserName'; // The username to use with basic authentication
            Configuration.basicAuthPassword = 'basicAuthPassword'; // The password to use with basic authentication
            
        }
    };
});
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

The singleton instance of the ``` DeploymentsController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, DeploymentsController){
	});
```

### <a name="list_deployments"></a>![Method: ](https://apidocs.io/img/method.png ".DeploymentsController.listDeployments") listDeployments

> List Deployments


```javascript
function listDeployments(authorization, oRG)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, DeploymentsController){
        var authorization = 'Authorization';
        var oRG = 'ORG';


		var result = DeploymentsController.listDeployments(authorization, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="get_deployments"></a>![Method: ](https://apidocs.io/img/method.png ".DeploymentsController.getDeployments") getDeployments

> Deployments


```javascript
function getDeployments(authorization, oRG)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, DeploymentsController){
        var authorization = 'Authorization';
        var oRG = 'ORG';


		var result = DeploymentsController.getDeployments(authorization, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="user_roles_controller"></a>![Class: ](https://apidocs.io/img/class.png ".UserRolesController") UserRolesController

### Get singleton instance

The singleton instance of the ``` UserRolesController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, UserRolesController){
	});
```

### <a name="create_user_roles_update"></a>![Method: ](https://apidocs.io/img/method.png ".UserRolesController.createUserRolesUpdate") createUserRolesUpdate

> User Roles Update


```javascript
function createUserRolesUpdate(body, authorization, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, UserRolesController){
        var body = new UserRolesUpdateRequest({ "role" : [ { "name" : "orgadmin", "organization" : "dev" }, { "name" : "sysadmin" } ] });
        var authorization = 'Basic {{BASICAUTH}}';
        var contentType = 'application/json';


		var result = UserRolesController.createUserRolesUpdate(body, authorization, contentType);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="delete_an_organization_userrole"></a>![Method: ](https://apidocs.io/img/method.png ".UserRolesController.deleteAnOrganizationUserrole") deleteAnOrganizationUserrole

> Delete an organization userrole


```javascript
function deleteAnOrganizationUserrole(org, authorization, accept)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| org |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, UserRolesController){
        var org = '{{ORG}}';
        var authorization = 'Basic {{BASICAUTH}}';
        var accept = 'application/json';


		var result = UserRolesController.deleteAnOrganizationUserrole(org, authorization, accept);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="get_permissions_for_a_role"></a>![Method: ](https://apidocs.io/img/method.png ".UserRolesController.getPermissionsForARole") getPermissionsForARole

> Get permissions for a role


```javascript
function getPermissionsForARole(authorization, contentType, oRG)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, UserRolesController){
        var authorization = 'Authorization';
        var contentType = 'Content-Type';
        var oRG = 'ORG';


		var result = UserRolesController.getPermissionsForARole(authorization, contentType, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="o_auth_controller"></a>![Class: ](https://apidocs.io/img/class.png ".OAuthController") OAuthController

### Get singleton instance

The singleton instance of the ``` OAuthController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, OAuthController){
	});
```

### <a name="get_o_auth2_token_details_get"></a>![Method: ](https://apidocs.io/img/method.png ".OAuthController.getOAuth2TokenDetailsGet") getOAuth2TokenDetailsGet

> OAuth2 Token Details Get


```javascript
function getOAuth2TokenDetailsGet(authorization, contentType, oRG)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, OAuthController){
        var authorization = 'Authorization';
        var contentType = 'Content-Type';
        var oRG = 'ORG';


		var result = OAuthController.getOAuth2TokenDetailsGet(authorization, contentType, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="kvm_controller"></a>![Class: ](https://apidocs.io/img/class.png ".KVMController") KVMController

### Get singleton instance

The singleton instance of the ``` KVMController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, KVMController){
	});
```

### <a name="get_kvm_get"></a>![Method: ](https://apidocs.io/img/method.png ".KVMController.getKVMGet") getKVMGet

> KVM Get


```javascript
function getKVMGet(authorization, contentType, oRG, eNV)
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


	app.controller("testController", function($scope, KVMController){
        var authorization = 'Authorization';
        var contentType = 'Content-Type';
        var oRG = 'ORG';
        var eNV = 'ENV';


		var result = KVMController.getKVMGet(authorization, contentType, oRG, eNV);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="delete_kvm_delete_entire_kvm"></a>![Method: ](https://apidocs.io/img/method.png ".KVMController.deleteKVMDeleteEntireKVM") deleteKVMDeleteEntireKVM

> KVM Delete (Entire KVM)


```javascript
function deleteKVMDeleteEntireKVM(authorization, contentType, oRG, eNV)
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


	app.controller("testController", function($scope, KVMController){
        var authorization = 'Authorization';
        var contentType = 'Content-Type';
        var oRG = 'ORG';
        var eNV = 'ENV';


		var result = KVMController.deleteKVMDeleteEntireKVM(authorization, contentType, oRG, eNV);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="pods_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PodsController") PodsController

### Get singleton instance

The singleton instance of the ``` PodsController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, PodsController){
	});
```

### <a name="get_analytics_pod"></a>![Method: ](https://apidocs.io/img/method.png ".PodsController.getAnalyticsPod") getAnalyticsPod

> Analytics pod


```javascript
function getAnalyticsPod(pod, authorization)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| pod |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, PodsController){
        var pod = 'analytics';
        var authorization = 'Basic {{BASICAUTH}}';


		var result = PodsController.getAnalyticsPod(pod, authorization);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="get_associated_pods"></a>![Method: ](https://apidocs.io/img/method.png ".PodsController.getAssociatedPods") getAssociatedPods

> Get Associated  Pods


```javascript
function getAssociatedPods(contentType, authorization, oRG)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, PodsController){
        var contentType = 'Content-Type';
        var authorization = 'Authorization';
        var oRG = 'ORG';


		var result = PodsController.getAssociatedPods(contentType, authorization, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="create_disassociate_org_from_pod"></a>![Method: ](https://apidocs.io/img/method.png ".PodsController.createDisassociateOrgFromPOD") createDisassociateOrgFromPOD

> Disassociate Org from POD


```javascript
function createDisassociateOrgFromPOD(contentType, authorization, oRG)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, PodsController){
        var contentType = 'Content-Type';
        var authorization = 'Authorization';
        var oRG = 'ORG';


		var result = PodsController.createDisassociateOrgFromPOD(contentType, authorization, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="servers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ServersController") ServersController

### Get singleton instance

The singleton instance of the ``` ServersController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, ServersController){
	});
```

### <a name="create_deregister"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.createDeregister") createDeregister

> Deregister


```javascript
function createDeregister(authorization, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, ServersController){
        var authorization = 'Basic {{BASICAUTH}}';
        var contentType = 'application/x-www-form-urlencoded';


		var result = ServersController.createDeregister(authorization, contentType);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="list_server_by_uuid"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.listServerByUUID") listServerByUUID

> List Server by UUID


```javascript
function listServerByUUID(authorization, uuid)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| uuid |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, ServersController){
        var authorization = 'Basic {{BASICAUTH}}';
        var uuid = 'uuid';


		var result = ServersController.listServerByUUID(authorization, uuid);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="create_set_not_reachable"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.createSetNotReachable") createSetNotReachable

> Set not reachable


```javascript
function createSetNotReachable(reachable, authorization)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| reachable |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, ServersController){
        var reachable = 'false';
        var authorization = 'Basic {{BASICAUTH}}';


		var result = ServersController.createSetNotReachable(reachable, authorization);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="list_org_env_servers"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.listOrgEnvServers") listOrgEnvServers

> List org/env servers


```javascript
function listOrgEnvServers(authorization, oRG, eNV)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, ServersController){
        var authorization = 'Authorization';
        var oRG = 'ORG';
        var eNV = 'ENV';


		var result = ServersController.listOrgEnvServers(authorization, oRG, eNV);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="create_register_server_with_org"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.createRegisterServerWithOrg") createRegisterServerWithOrg

> Register server with org


```javascript
function createRegisterServerWithOrg(authorization, contentType, oRG, eNV)
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


	app.controller("testController", function($scope, ServersController){
        var authorization = 'Authorization';
        var contentType = 'Content-Type';
        var oRG = 'ORG';
        var eNV = 'ENV';


		var result = ServersController.createRegisterServerWithOrg(authorization, contentType, oRG, eNV);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="create_associate_environments_to_mp"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.createAssociateEnvironmentsToMP") createAssociateEnvironmentsToMP

> Associate  environments to MP


```javascript
function createAssociateEnvironmentsToMP(authorization, contentType, oRG, eNV)
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


	app.controller("testController", function($scope, ServersController){
        var authorization = 'Authorization';
        var contentType = 'Content-Type';
        var oRG = 'ORG';
        var eNV = 'ENV';


		var result = ServersController.createAssociateEnvironmentsToMP(authorization, contentType, oRG, eNV);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="developers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DevelopersController") DevelopersController

### Get singleton instance

The singleton instance of the ``` DevelopersController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, DevelopersController){
	});
```

### <a name="get_developers"></a>![Method: ](https://apidocs.io/img/method.png ".DevelopersController.getDevelopers") getDevelopers

> Get Developers


```javascript
function getDevelopers(authorization, contentType, oRG)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, DevelopersController){
        var authorization = 'Authorization';
        var contentType = 'Content-Type';
        var oRG = 'ORG';


		var result = DevelopersController.getDevelopers(authorization, contentType, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="create_developer"></a>![Method: ](https://apidocs.io/img/method.png ".DevelopersController.createDeveloper") createDeveloper

> Create Developer


```javascript
function createDeveloper(body, authorization, contentType, oRG)
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


	app.controller("testController", function($scope, DevelopersController){
        var body = 'Body';
        var authorization = 'Authorization';
        var contentType = 'Content-Type';
        var oRG = 'ORG';


		var result = DevelopersController.createDeveloper(body, authorization, contentType, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="ap_is_controller"></a>![Class: ](https://apidocs.io/img/class.png ".APIsController") APIsController

### Get singleton instance

The singleton instance of the ``` APIsController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, APIsController){
	});
```

### <a name="get_api_list"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.getApiList") getApiList

> Api list


```javascript
function getApiList(authorization, oRG)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, APIsController){
        var authorization = 'Authorization';
        var oRG = 'ORG';


		var result = APIsController.getApiList(authorization, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="create_deploy_api"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.createDeployAPI") createDeployAPI

> Deploy API


```javascript
function createDeployAPI(action, name, authorization, contentType, oRG)
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


	app.controller("testController", function($scope, APIsController){
        var action = 'action';
        var name = 'name';
        var authorization = 'Authorization';
        var contentType = 'Content-Type';
        var oRG = 'ORG';


		var result = APIsController.createDeployAPI(action, name, authorization, contentType, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="delete_an_api"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.deleteAnAPI") deleteAnAPI

> Delete an API


```javascript
function deleteAnAPI(authorization, oRG)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, APIsController){
        var authorization = 'Authorization';
        var oRG = 'ORG';


		var result = APIsController.deleteAnAPI(authorization, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="create_undeploy_revisions"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.createUndeployRevisions") createUndeployRevisions

> Undeploy Revisions


```javascript
function createUndeployRevisions(action, env, authorization, contentType, oRG)
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


	app.controller("testController", function($scope, APIsController){
        var action = 'action';
        var env = 'env';
        var authorization = 'Authorization';
        var contentType = 'Content-Type';
        var oRG = 'ORG';


		var result = APIsController.createUndeployRevisions(action, env, authorization, contentType, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="cache_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CacheController") CacheController

### Get singleton instance

The singleton instance of the ``` CacheController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, CacheController){
	});
```

### <a name="list_caches"></a>![Method: ](https://apidocs.io/img/method.png ".CacheController.listCaches") listCaches

> List caches


```javascript
function listCaches(authorization, oRG, eNV)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, CacheController){
        var authorization = 'Authorization';
        var oRG = 'ORG';
        var eNV = 'ENV';


		var result = CacheController.listCaches(authorization, oRG, eNV);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="audit_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AuditController") AuditController

### Get singleton instance

The singleton instance of the ``` AuditController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, AuditController){
	});
```

### <a name="get_audit"></a>![Method: ](https://apidocs.io/img/method.png ".AuditController.getAudit") getAudit

> Audit


```javascript
function getAudit(expand, timeline, authorization, oRG)
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


	app.controller("testController", function($scope, AuditController){
        var expand = true;
        var timeline = 'timeline';
        var authorization = 'Authorization';
        var oRG = 'ORG';


		var result = AuditController.getAudit(expand, timeline, authorization, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="users_controller"></a>![Class: ](https://apidocs.io/img/class.png ".UsersController") UsersController

### Get singleton instance

The singleton instance of the ``` UsersController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, UsersController){
	});
```

### <a name="get_developer_details_get"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.getDeveloperDetailsGet") getDeveloperDetailsGet

> Developer Details Get


```javascript
function getDeveloperDetailsGet(authorization, contentType, oRG)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, UsersController){
        var authorization = 'Authorization';
        var contentType = 'Content-Type';
        var oRG = 'ORG';


		var result = UsersController.getDeveloperDetailsGet(authorization, contentType, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="create_user_in_org"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.createUserInORG") createUserInORG

> Create User in ORG


```javascript
function createUserInORG(body, authorization, contentType, oRG)
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


	app.controller("testController", function($scope, UsersController){
        var body = 'Body';
        var authorization = 'Authorization';
        var contentType = 'Content-Type';
        var oRG = 'ORG';


		var result = UsersController.createUserInORG(body, authorization, contentType, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="list_users"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.listUsers") listUsers

> List Users


```javascript
function listUsers(authorization)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, UsersController){
        var authorization = 'Basic {{BASICAUTH}}';


		var result = UsersController.listUsers(authorization);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="add_user_as_orgadmin"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.addUserAsOrgadmin") addUserAsOrgadmin

> Add user as Orgadmin


```javascript
function addUserAsOrgadmin(body, authorization, contentType, oRG)
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


	app.controller("testController", function($scope, UsersController){
        var body = 'Body';
        var authorization = 'Authorization';
        var contentType = 'Content-Type';
        var oRG = 'ORG';


		var result = UsersController.addUserAsOrgadmin(body, authorization, contentType, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="zzz_others_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ZzzOthersController") ZzzOthersController

### Get singleton instance

The singleton instance of the ``` ZzzOthersController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, ZzzOthersController){
	});
```

### <a name="get_cluster_status"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.getClusterStatus") getClusterStatus

> Cluster Status


```javascript
function getClusterStatus(authorization)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, ZzzOthersController){
        var authorization = 'Basic {{BASICAUTH}}';


		var result = ZzzOthersController.getClusterStatus(authorization);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="create_enable_debug_wo_restart"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.createEnableDebugWORestart") createEnableDebugWORestart

> Enable Debug w/o Restart 


```javascript
function createEnableDebugWORestart(session, authorization, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| session |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, ZzzOthersController){
        var session = 'logsession_name';
        var authorization = 'Basic {{BASICAUTH}}';
        var contentType = 'application/x-www-form-urlencoded';


		var result = ZzzOthersController.createEnableDebugWORestart(session, authorization, contentType);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="get_classifications"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.getClassifications") getClassifications

> Classifications


```javascript
function getClassifications(authorization, hOST)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, ZzzOthersController){
        var authorization = 'Authorization';
        var hOST = 'HOST';


		var result = ZzzOthersController.getClassifications(authorization, hOST);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="create_company_developer"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.createCompanyDeveloper") createCompanyDeveloper

> Create Company Developer


```javascript
function createCompanyDeveloper(body, contentType, authorization, oRG, cOMPANY)
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


	app.controller("testController", function($scope, ZzzOthersController){
        var body = new CreateCompanyDeveloperRequest({"key":"value"});
        var contentType = 'Content-Type';
        var authorization = 'Authorization';
        var oRG = 'ORG';
        var cOMPANY = 'COMPANY';


		var result = ZzzOthersController.createCompanyDeveloper(body, contentType, authorization, oRG, cOMPANY);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="get_qpid_metrics"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.getQPIDMetrics") getQPIDMetrics

> QPID Metrics


```javascript
function getQPIDMetrics(authorization, hOST)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, ZzzOthersController){
        var authorization = 'Authorization';
        var hOST = 'HOST';


		var result = ZzzOthersController.getQPIDMetrics(authorization, hOST);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="get_build_info"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.getBuildInfo") getBuildInfo

> Build Info


```javascript
function getBuildInfo(authorization, hOST, pORT)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |
| pORT |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, ZzzOthersController){
        var authorization = 'Authorization';
        var hOST = 'HOST';
        var pORT = 'PORT';


		var result = ZzzOthersController.getBuildInfo(authorization, hOST, pORT);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="delete_disable_debug_wo_restart"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.deleteDisableDebugWORestart") deleteDisableDebugWORestart

> Disable Debug w/o Restart


```javascript
function deleteDisableDebugWORestart(authorization, contentType)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, ZzzOthersController){
        var authorization = 'Basic {{BASICAUTH}}';
        var contentType = 'application/x-www-form-urlencoded';


		var result = ZzzOthersController.deleteDisableDebugWORestart(authorization, contentType);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="apps_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AppsController") AppsController

### Get singleton instance

The singleton instance of the ``` AppsController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, AppsController){
	});
```

### <a name="create_company_app"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.createCompanyAPP") createCompanyAPP

> Create Company APP


```javascript
function createCompanyAPP(body, authorization, contentType, oRG, cOMPANY)
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


	app.controller("testController", function($scope, AppsController){
        var body = 'Body';
        var authorization = 'Authorization';
        var contentType = 'Content-Type';
        var oRG = 'ORG';
        var cOMPANY = 'COMPANY';


		var result = AppsController.createCompanyAPP(body, authorization, contentType, oRG, cOMPANY);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="add_app_credentials"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.addAppCredentials") addAppCredentials

> Add app credentials


```javascript
function addAppCredentials(body, authorization, contentType, oRG)
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


	app.controller("testController", function($scope, AppsController){
        var body = 'Body';
        var authorization = 'Authorization';
        var contentType = 'Content-Type';
        var oRG = 'ORG';


		var result = AppsController.addAppCredentials(body, authorization, contentType, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="list_apps"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.listApps") listApps

> List apps 


```javascript
function listApps(authorization, oRG)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, AppsController){
        var authorization = 'Authorization';
        var oRG = 'ORG';


		var result = AppsController.listApps(authorization, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="list_app"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.listApp") listApp

> List app


```javascript
function listApp(authorization, oRG)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, AppsController){
        var authorization = 'Authorization';
        var oRG = 'ORG';


		var result = AppsController.listApp(authorization, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="virtual_hosts_controller"></a>![Class: ](https://apidocs.io/img/class.png ".VirtualHostsController") VirtualHostsController

### Get singleton instance

The singleton instance of the ``` VirtualHostsController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, VirtualHostsController){
	});
```

### <a name="list_virtual_hosts"></a>![Method: ](https://apidocs.io/img/method.png ".VirtualHostsController.listVirtualHosts") listVirtualHosts

> List VirtualHosts


```javascript
function listVirtualHosts(authorization, oRG, eNV)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, VirtualHostsController){
        var authorization = 'Authorization';
        var oRG = 'ORG';
        var eNV = 'ENV';


		var result = VirtualHostsController.listVirtualHosts(authorization, oRG, eNV);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="add_virtual_host"></a>![Method: ](https://apidocs.io/img/method.png ".VirtualHostsController.addVirtualHost") addVirtualHost

> Add Virtual Host


```javascript
function addVirtualHost(body, authorization, contentType, oRG, eNV)
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


	app.controller("testController", function($scope, VirtualHostsController){
        var body = 'Body';
        var authorization = 'Authorization';
        var contentType = 'Content-Type';
        var oRG = 'ORG';
        var eNV = 'ENV';


		var result = VirtualHostsController.addVirtualHost(body, authorization, contentType, oRG, eNV);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="environments_controller"></a>![Class: ](https://apidocs.io/img/class.png ".EnvironmentsController") EnvironmentsController

### Get singleton instance

The singleton instance of the ``` EnvironmentsController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, EnvironmentsController){
	});
```

### <a name="update_environments"></a>![Method: ](https://apidocs.io/img/method.png ".EnvironmentsController.updateEnvironments") updateEnvironments

> Update Environments


```javascript
function updateEnvironments(authorization, contentType, oRG, eNV)
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


	app.controller("testController", function($scope, EnvironmentsController){
        var authorization = 'Authorization';
        var contentType = 'Content-Type';
        var oRG = 'ORG';
        var eNV = 'ENV';


		var result = EnvironmentsController.updateEnvironments(authorization, contentType, oRG, eNV);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="delete_environment"></a>![Method: ](https://apidocs.io/img/method.png ".EnvironmentsController.deleteEnvironment") deleteEnvironment

> Delete Environment


```javascript
function deleteEnvironment(authorization, oRG, eNV)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, EnvironmentsController){
        var authorization = 'Authorization';
        var oRG = 'ORG';
        var eNV = 'ENV';


		var result = EnvironmentsController.deleteEnvironment(authorization, oRG, eNV);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="create_new_env_in_org"></a>![Method: ](https://apidocs.io/img/method.png ".EnvironmentsController.createNewENVInORG") createNewENVInORG

> Create New ENV in ORG


```javascript
function createNewENVInORG(body, authorization, contentType, oRG)
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


	app.controller("testController", function($scope, EnvironmentsController){
        var body = 'Body';
        var authorization = 'Authorization';
        var contentType = 'Content-Type';
        var oRG = 'ORG';


		var result = EnvironmentsController.createNewENVInORG(body, authorization, contentType, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="developer_app_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DeveloperAppController") DeveloperAppController

### Get singleton instance

The singleton instance of the ``` DeveloperAppController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, DeveloperAppController){
	});
```

### <a name="get_developer_app_details_get"></a>![Method: ](https://apidocs.io/img/method.png ".DeveloperAppController.getDeveloperAppDetailsGet") getDeveloperAppDetailsGet

> Developer App Details Get


```javascript
function getDeveloperAppDetailsGet(authorization, contentType, oRG)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, DeveloperAppController){
        var authorization = 'Authorization';
        var contentType = 'Content-Type';
        var oRG = 'ORG';


		var result = DeveloperAppController.getDeveloperAppDetailsGet(authorization, contentType, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="delete_app_credentials"></a>![Method: ](https://apidocs.io/img/method.png ".DeveloperAppController.deleteAppCredentials") deleteAppCredentials

> Delete app credentials


```javascript
function deleteAppCredentials(authorization, accept, oRG)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, DeveloperAppController){
        var authorization = 'Authorization';
        var accept = 'Accept';
        var oRG = 'ORG';


		var result = DeveloperAppController.deleteAppCredentials(authorization, accept, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="keystores_controller"></a>![Class: ](https://apidocs.io/img/class.png ".KeystoresController") KeystoresController

### Get singleton instance

The singleton instance of the ``` KeystoresController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, KeystoresController){
	});
```

### <a name="list_keystores"></a>![Method: ](https://apidocs.io/img/method.png ".KeystoresController.listKeystores") listKeystores

> List Keystores


```javascript
function listKeystores(authorization, oRG, eNV)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, KeystoresController){
        var authorization = 'Authorization';
        var oRG = 'ORG';
        var eNV = 'ENV';


		var result = KeystoresController.listKeystores(authorization, oRG, eNV);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="products_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductsController") ProductsController

### Get singleton instance

The singleton instance of the ``` ProductsController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, ProductsController){
	});
```

### <a name="get_api_products"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.getApiProducts") getApiProducts

> Api Products


```javascript
function getApiProducts(authorization, oRG)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, ProductsController){
        var authorization = 'Authorization';
        var oRG = 'ORG';


		var result = ProductsController.getApiProducts(authorization, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="create_ap_iproduct_creation"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.createAPIproductCreation") createAPIproductCreation

> APIproduct Creation


```javascript
function createAPIproductCreation(body, authorization, contentType, oRG)
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


	app.controller("testController", function($scope, ProductsController){
        var body = 'Body';
        var authorization = 'Authorization';
        var contentType = 'Content-Type';
        var oRG = 'ORG';


		var result = ProductsController.createAPIproductCreation(body, authorization, contentType, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="target_servers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".TargetServersController") TargetServersController

### Get singleton instance

The singleton instance of the ``` TargetServersController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, TargetServersController){
	});
```

### <a name="list_target_servers"></a>![Method: ](https://apidocs.io/img/method.png ".TargetServersController.listTargetServers") listTargetServers

> List Target Servers


```javascript
function listTargetServers(authorization, oRG, eNV)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, TargetServersController){
        var authorization = 'Authorization';
        var oRG = 'ORG';
        var eNV = 'ENV';


		var result = TargetServersController.listTargetServers(authorization, oRG, eNV);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="add_target"></a>![Method: ](https://apidocs.io/img/method.png ".TargetServersController.addTarget") addTarget

> Add Target


```javascript
function addTarget(body, contentType, authorization, oRG, eNV)
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


	app.controller("testController", function($scope, TargetServersController){
        var body = new AddTargetRequest({"key":"value"});
        var contentType = 'content-type';
        var authorization = 'Authorization';
        var oRG = 'ORG';
        var eNV = 'ENV';


		var result = TargetServersController.addTarget(body, contentType, authorization, oRG, eNV);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="company_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CompanyController") CompanyController

### Get singleton instance

The singleton instance of the ``` CompanyController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, CompanyController){
	});
```

### <a name="create_company"></a>![Method: ](https://apidocs.io/img/method.png ".CompanyController.createCompany") createCompany

> Create Company


```javascript
function createCompany(body, authorization, contentType, oRG)
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


	app.controller("testController", function($scope, CompanyController){
        var body = 'Body';
        var authorization = 'Authorization';
        var contentType = 'Content-Type';
        var oRG = 'ORG';


		var result = CompanyController.createCompany(body, authorization, contentType, oRG);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="organizations_controller"></a>![Class: ](https://apidocs.io/img/class.png ".OrganizationsController") OrganizationsController

### Get singleton instance

The singleton instance of the ``` OrganizationsController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, OrganizationsController){
	});
```

### <a name="list_organizations"></a>![Method: ](https://apidocs.io/img/method.png ".OrganizationsController.listOrganizations") listOrganizations

> List organizations


```javascript
function listOrganizations(authorization)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, OrganizationsController){
        var authorization = 'Basic {{BASICAUTH}}';


		var result = OrganizationsController.listOrganizations(authorization);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)




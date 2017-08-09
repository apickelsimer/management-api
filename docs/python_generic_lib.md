# Getting started

TODO: Add Description

## How to Build


You must have Python 2 >=2.7.9 or Python 3 >=3.4 installed on your system to install and run this SDK. This SDK package depends on other Python packages like nose, jsonpickle etc. 
These dependencies are defined in the ```requirements.txt``` file that comes with the SDK.
To resolve these dependencies, you can use the PIP Dependency manager. Install it by following steps at [https://pip.pypa.io/en/stable/installing/](https://pip.pypa.io/en/stable/installing/).

Python and PIP executables should be defined in your PATH. Open command prompt and type ```pip --version```.
This should display the version of the PIP Dependency Manager installed if your installation was successful and the paths are properly defined.

* Using command line, navigate to the directory containing the generated files (including ```requirements.txt```) for the SDK.
* Run the command ```pip install -r requirements.txt```. This should install all the required dependencies.

![Building SDK - Step 1](https://apidocs.io/illustration/python?step=installDependencies&workspaceFolder=Apigee%20Edge%20API%20Management-Python)


## How to Use

The following section explains how to use the Apigeeedgeapimanagement SDK package in a new project.

### 1. Open Project in an IDE

Open up a Python IDE like PyCharm. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

![Open project in PyCharm - Step 1](https://apidocs.io/illustration/python?step=pyCharm)

Click on ```Open``` in PyCharm to browse to your generated SDK directory and then click ```OK```.

![Open project in PyCharm - Step 2](https://apidocs.io/illustration/python?step=openProject0&workspaceFolder=Apigee%20Edge%20API%20Management-Python)     

The project files will be displayed in the side bar as follows:

![Open project in PyCharm - Step 3](https://apidocs.io/illustration/python?step=openProject1&workspaceFolder=Apigee%20Edge%20API%20Management-Python&projectName=apigeeedgeapimanagement)     

### 2. Add a new Test Project

Create a new directory by right clicking on the solution name as shown below:

![Add a new project in PyCharm - Step 1](https://apidocs.io/illustration/python?step=createDirectory&workspaceFolder=Apigee%20Edge%20API%20Management-Python&projectName=apigeeedgeapimanagement)

Name the directory as "test"

![Add a new project in PyCharm - Step 2](https://apidocs.io/illustration/python?step=nameDirectory)
   
Add a python file to this project with the name "testsdk"

![Add a new project in PyCharm - Step 3](https://apidocs.io/illustration/python?step=createFile&workspaceFolder=Apigee%20Edge%20API%20Management-Python&projectName=apigeeedgeapimanagement)

Name it "testsdk"

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?step=nameFile)

In your python file you will be required to import the generated python library using the following code lines

```Python
from apigeeedgeapimanagement.apigeeedgeapimanagement_client import ApigeeedgeapimanagementClient
```

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?step=projectFiles&workspaceFolder=Apigee%20Edge%20API%20Management-Python&libraryName=apigeeedgeapimanagement.apigeeedgeapimanagement_client&projectName=apigeeedgeapimanagement)

After this you can write code to instantiate an API client object, get a controller object and  make API calls. Sample code is given in the subsequent sections.

### 3. Run the Test Project

To run the file within your test project, right click on your Python file inside your Test project and click on ```Run```

![Run Test Project - Step 1](https://apidocs.io/illustration/python?step=runProject&workspaceFolder=Apigee%20Edge%20API%20Management-Python&libraryName=apigeeedgeapimanagement.apigeeedgeapimanagement_client&projectName=apigeeedgeapimanagement)


## How to Test

You can test the generated SDK and the server with automatically generated test
cases. unittest is used as the testing framework and nose is used as the test
runner. You can run the tests as follows:

  1. From terminal/cmd navigate to the root directory of the SDK.
  2. Invoke 'pip install -r test-requirements.txt'
  3. Invoke 'nosetests'

## Initialization

### Authentication
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| basic_auth_user_name | The username to use with basic authentication |
| basic_auth_password | The password to use with basic authentication |



API client can be initialized as following.

```python
# Configuration parameters and credentials
basic_auth_user_name = 'basic_auth_user_name' # The username to use with basic authentication
basic_auth_password = 'basic_auth_password' # The password to use with basic authentication

client = ApigeeedgeapimanagementClient(basic_auth_user_name, basic_auth_password)
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

### Get controller instance

An instance of the ``` DeploymentsController ``` class can be accessed from the API Client.

```python
 deployments_client = client.deployments
```

### <a name="list_deployments"></a>![Method: ](https://apidocs.io/img/method.png ".DeploymentsController.list_deployments") list_deployments

> List Deployments

```python
def list_deployments(self,
                         authorization,
                         org)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
org = 'ORG'

deployments_client.list_deployments(authorization, org)

```


### <a name="get_deployments"></a>![Method: ](https://apidocs.io/img/method.png ".DeploymentsController.get_deployments") get_deployments

> Deployments

```python
def get_deployments(self,
                        authorization,
                        org)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
org = 'ORG'

deployments_client.get_deployments(authorization, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="user_roles_controller"></a>![Class: ](https://apidocs.io/img/class.png ".UserRolesController") UserRolesController

### Get controller instance

An instance of the ``` UserRolesController ``` class can be accessed from the API Client.

```python
 user_roles_client = client.user_roles
```

### <a name="create_user_roles_update"></a>![Method: ](https://apidocs.io/img/method.png ".UserRolesController.create_user_roles_update") create_user_roles_update

> User Roles Update

```python
def create_user_roles_update(self,
                                 body,
                                 authorization,
                                 content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body_value = "{ \"role\" : [ { \"name\" : \"orgadmin\", \"organization\" : \"dev\" }, { \"name\" : \"sysadmin\" } ] }"
body = json.loads(body_value)
authorization = 'Basic {{BASICAUTH}}'
content_type = 'application/json'

user_roles_client.create_user_roles_update(body, authorization, content_type)

```


### <a name="delete_an_organization_userrole"></a>![Method: ](https://apidocs.io/img/method.png ".UserRolesController.delete_an_organization_userrole") delete_an_organization_userrole

> Delete an organization userrole

```python
def delete_an_organization_userrole(self,
                                        org,
                                        authorization,
                                        accept)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| org |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
org = '{{ORG}}'
authorization = 'Basic {{BASICAUTH}}'
accept = 'application/json'

user_roles_client.delete_an_organization_userrole(org, authorization, accept)

```


### <a name="get_permissions_for_a_role"></a>![Method: ](https://apidocs.io/img/method.png ".UserRolesController.get_permissions_for_a_role") get_permissions_for_a_role

> Get permissions for a role

```python
def get_permissions_for_a_role(self,
                                   authorization,
                                   content_type,
                                   org)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

user_roles_client.get_permissions_for_a_role(authorization, content_type, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="o_auth_controller"></a>![Class: ](https://apidocs.io/img/class.png ".OAuthController") OAuthController

### Get controller instance

An instance of the ``` OAuthController ``` class can be accessed from the API Client.

```python
 o_auth_client = client.o_auth
```

### <a name="get_o_auth_2_token_details_get"></a>![Method: ](https://apidocs.io/img/method.png ".OAuthController.get_o_auth_2_token_details_get") get_o_auth_2_token_details_get

> OAuth2 Token Details Get

```python
def get_o_auth_2_token_details_get(self,
                                       authorization,
                                       content_type,
                                       org)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

o_auth_client.get_o_auth_2_token_details_get(authorization, content_type, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="kvm_controller"></a>![Class: ](https://apidocs.io/img/class.png ".KVMController") KVMController

### Get controller instance

An instance of the ``` KVMController ``` class can be accessed from the API Client.

```python
 kvm_client = client.kvm
```

### <a name="get_kvm_get"></a>![Method: ](https://apidocs.io/img/method.png ".KVMController.get_kvm_get") get_kvm_get

> KVM Get

```python
def get_kvm_get(self,
                    authorization,
                    content_type,
                    org,
                    env)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'
env = 'ENV'

kvm_client.get_kvm_get(authorization, content_type, org, env)

```


### <a name="delete_kvm_delete_entire_kvm"></a>![Method: ](https://apidocs.io/img/method.png ".KVMController.delete_kvm_delete_entire_kvm") delete_kvm_delete_entire_kvm

> KVM Delete (Entire KVM)

```python
def delete_kvm_delete_entire_kvm(self,
                                     authorization,
                                     content_type,
                                     org,
                                     env)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'
env = 'ENV'

kvm_client.delete_kvm_delete_entire_kvm(authorization, content_type, org, env)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="pods_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PodsController") PodsController

### Get controller instance

An instance of the ``` PodsController ``` class can be accessed from the API Client.

```python
 pods_client = client.pods
```

### <a name="get_analytics_pod"></a>![Method: ](https://apidocs.io/img/method.png ".PodsController.get_analytics_pod") get_analytics_pod

> Analytics pod

```python
def get_analytics_pod(self,
                          pod,
                          authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| pod |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
pod = 'analytics'
authorization = 'Basic {{BASICAUTH}}'

pods_client.get_analytics_pod(pod, authorization)

```


### <a name="get_associated_pods"></a>![Method: ](https://apidocs.io/img/method.png ".PodsController.get_associated_pods") get_associated_pods

> Get Associated  Pods

```python
def get_associated_pods(self,
                            content_type,
                            authorization,
                            org)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
content_type = 'Content-Type'
authorization = 'Authorization'
org = 'ORG'

pods_client.get_associated_pods(content_type, authorization, org)

```


### <a name="create_disassociate_org_from_pod"></a>![Method: ](https://apidocs.io/img/method.png ".PodsController.create_disassociate_org_from_pod") create_disassociate_org_from_pod

> Disassociate Org from POD

```python
def create_disassociate_org_from_pod(self,
                                         content_type,
                                         authorization,
                                         org)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
content_type = 'Content-Type'
authorization = 'Authorization'
org = 'ORG'

pods_client.create_disassociate_org_from_pod(content_type, authorization, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="servers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ServersController") ServersController

### Get controller instance

An instance of the ``` ServersController ``` class can be accessed from the API Client.

```python
 servers_client = client.servers
```

### <a name="create_deregister"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.create_deregister") create_deregister

> Deregister

```python
def create_deregister(self,
                          authorization,
                          content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Basic {{BASICAUTH}}'
content_type = 'application/x-www-form-urlencoded'

servers_client.create_deregister(authorization, content_type)

```


### <a name="list_server_by_uuid"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.list_server_by_uuid") list_server_by_uuid

> List Server by UUID

```python
def list_server_by_uuid(self,
                            authorization,
                            uuid)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| uuid |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Basic {{BASICAUTH}}'
uuid = 'uuid'

servers_client.list_server_by_uuid(authorization, uuid)

```


### <a name="create_set_not_reachable"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.create_set_not_reachable") create_set_not_reachable

> Set not reachable

```python
def create_set_not_reachable(self,
                                 reachable,
                                 authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| reachable |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
reachable = 'false'
authorization = 'Basic {{BASICAUTH}}'

servers_client.create_set_not_reachable(reachable, authorization)

```


### <a name="list_org_env_servers"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.list_org_env_servers") list_org_env_servers

> List org/env servers

```python
def list_org_env_servers(self,
                             authorization,
                             org,
                             env)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
org = 'ORG'
env = 'ENV'

servers_client.list_org_env_servers(authorization, org, env)

```


### <a name="create_register_server_with_org"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.create_register_server_with_org") create_register_server_with_org

> Register server with org

```python
def create_register_server_with_org(self,
                                        authorization,
                                        content_type,
                                        org,
                                        env)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'
env = 'ENV'

servers_client.create_register_server_with_org(authorization, content_type, org, env)

```


### <a name="create_associate_environments_to_mp"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.create_associate_environments_to_mp") create_associate_environments_to_mp

> Associate  environments to MP

```python
def create_associate_environments_to_mp(self,
                                            authorization,
                                            content_type,
                                            org,
                                            env)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'
env = 'ENV'

servers_client.create_associate_environments_to_mp(authorization, content_type, org, env)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="developers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DevelopersController") DevelopersController

### Get controller instance

An instance of the ``` DevelopersController ``` class can be accessed from the API Client.

```python
 developers_client = client.developers
```

### <a name="get_developers"></a>![Method: ](https://apidocs.io/img/method.png ".DevelopersController.get_developers") get_developers

> Get Developers

```python
def get_developers(self,
                       authorization,
                       content_type,
                       org)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

developers_client.get_developers(authorization, content_type, org)

```


### <a name="create_developer"></a>![Method: ](https://apidocs.io/img/method.png ".DevelopersController.create_developer") create_developer

> Create Developer

```python
def create_developer(self,
                         body,
                         authorization,
                         content_type,
                         org)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = 'Body'
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

developers_client.create_developer(body, authorization, content_type, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="ap_is_controller"></a>![Class: ](https://apidocs.io/img/class.png ".APIsController") APIsController

### Get controller instance

An instance of the ``` APIsController ``` class can be accessed from the API Client.

```python
 ap_is_client = client.ap_is
```

### <a name="get_api_list"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.get_api_list") get_api_list

> Api list

```python
def get_api_list(self,
                     authorization,
                     org)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
org = 'ORG'

ap_is_client.get_api_list(authorization, org)

```


### <a name="create_deploy_api"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.create_deploy_api") create_deploy_api

> Deploy API

```python
def create_deploy_api(self,
                          action,
                          name,
                          authorization,
                          content_type,
                          org)
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

```python
action = 'action'
name = 'name'
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

ap_is_client.create_deploy_api(action, name, authorization, content_type, org)

```


### <a name="delete_an_api"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.delete_an_api") delete_an_api

> Delete an API

```python
def delete_an_api(self,
                      authorization,
                      org)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
org = 'ORG'

ap_is_client.delete_an_api(authorization, org)

```


### <a name="create_undeploy_revisions"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.create_undeploy_revisions") create_undeploy_revisions

> Undeploy Revisions

```python
def create_undeploy_revisions(self,
                                  action,
                                  env,
                                  authorization,
                                  content_type,
                                  org)
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

```python
action = 'action'
env = 'env'
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

ap_is_client.create_undeploy_revisions(action, env, authorization, content_type, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="cache_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CacheController") CacheController

### Get controller instance

An instance of the ``` CacheController ``` class can be accessed from the API Client.

```python
 cache_client = client.cache
```

### <a name="list_caches"></a>![Method: ](https://apidocs.io/img/method.png ".CacheController.list_caches") list_caches

> List caches

```python
def list_caches(self,
                    authorization,
                    org,
                    env)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
org = 'ORG'
env = 'ENV'

cache_client.list_caches(authorization, org, env)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="audit_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AuditController") AuditController

### Get controller instance

An instance of the ``` AuditController ``` class can be accessed from the API Client.

```python
 audit_client = client.audit
```

### <a name="get_audit"></a>![Method: ](https://apidocs.io/img/method.png ".AuditController.get_audit") get_audit

> Audit

```python
def get_audit(self,
                  expand,
                  timeline,
                  authorization,
                  org)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| expand |  ``` Required ```  | TODO: Add a parameter description |
| timeline |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
expand = True
timeline = 'timeline'
authorization = 'Authorization'
org = 'ORG'

audit_client.get_audit(expand, timeline, authorization, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="users_controller"></a>![Class: ](https://apidocs.io/img/class.png ".UsersController") UsersController

### Get controller instance

An instance of the ``` UsersController ``` class can be accessed from the API Client.

```python
 users_client = client.users
```

### <a name="get_developer_details_get"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.get_developer_details_get") get_developer_details_get

> Developer Details Get

```python
def get_developer_details_get(self,
                                  authorization,
                                  content_type,
                                  org)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

users_client.get_developer_details_get(authorization, content_type, org)

```


### <a name="create_user_in_org"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.create_user_in_org") create_user_in_org

> Create User in ORG

```python
def create_user_in_org(self,
                           body,
                           authorization,
                           content_type,
                           org)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = 'Body'
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

users_client.create_user_in_org(body, authorization, content_type, org)

```


### <a name="list_users"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.list_users") list_users

> List Users

```python
def list_users(self,
                   authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Basic {{BASICAUTH}}'

users_client.list_users(authorization)

```


### <a name="add_user_as_orgadmin"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.add_user_as_orgadmin") add_user_as_orgadmin

> Add user as Orgadmin

```python
def add_user_as_orgadmin(self,
                             body,
                             authorization,
                             content_type,
                             org)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = 'Body'
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

users_client.add_user_as_orgadmin(body, authorization, content_type, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="zzz_others_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ZzzOthersController") ZzzOthersController

### Get controller instance

An instance of the ``` ZzzOthersController ``` class can be accessed from the API Client.

```python
 zzz_others_client = client.zzz_others
```

### <a name="get_cluster_status"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.get_cluster_status") get_cluster_status

> Cluster Status

```python
def get_cluster_status(self,
                           authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Basic {{BASICAUTH}}'

zzz_others_client.get_cluster_status(authorization)

```


### <a name="create_enable_debug_w_o_restart"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.create_enable_debug_w_o_restart") create_enable_debug_w_o_restart

> Enable Debug w/o Restart 

```python
def create_enable_debug_w_o_restart(self,
                                        session,
                                        authorization,
                                        content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| session |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
session = 'logsession_name'
authorization = 'Basic {{BASICAUTH}}'
content_type = 'application/x-www-form-urlencoded'

zzz_others_client.create_enable_debug_w_o_restart(session, authorization, content_type)

```


### <a name="get_classifications"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.get_classifications") get_classifications

> Classifications

```python
def get_classifications(self,
                            authorization,
                            host)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
host = 'HOST'

zzz_others_client.get_classifications(authorization, host)

```


### <a name="create_company_developer"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.create_company_developer") create_company_developer

> Create Company Developer

```python
def create_company_developer(self,
                                 body,
                                 content_type,
                                 authorization,
                                 org,
                                 company)
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

```python
body = CreateCompanyDeveloperRequest()
content_type = 'Content-Type'
authorization = 'Authorization'
org = 'ORG'
company = 'COMPANY'

zzz_others_client.create_company_developer(body, content_type, authorization, org, company)

```


### <a name="get_qpid_metrics"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.get_qpid_metrics") get_qpid_metrics

> QPID Metrics

```python
def get_qpid_metrics(self,
                         authorization,
                         host)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
host = 'HOST'

zzz_others_client.get_qpid_metrics(authorization, host)

```


### <a name="get_build_info"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.get_build_info") get_build_info

> Build Info

```python
def get_build_info(self,
                       authorization,
                       host,
                       port)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |
| pORT |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
host = 'HOST'
port = 'PORT'

zzz_others_client.get_build_info(authorization, host, port)

```


### <a name="delete_disable_debug_w_o_restart"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.delete_disable_debug_w_o_restart") delete_disable_debug_w_o_restart

> Disable Debug w/o Restart

```python
def delete_disable_debug_w_o_restart(self,
                                         authorization,
                                         content_type)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Basic {{BASICAUTH}}'
content_type = 'application/x-www-form-urlencoded'

zzz_others_client.delete_disable_debug_w_o_restart(authorization, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="apps_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AppsController") AppsController

### Get controller instance

An instance of the ``` AppsController ``` class can be accessed from the API Client.

```python
 apps_client = client.apps
```

### <a name="create_company_app"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.create_company_app") create_company_app

> Create Company APP

```python
def create_company_app(self,
                           body,
                           authorization,
                           content_type,
                           org,
                           company)
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

```python
body = 'Body'
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'
company = 'COMPANY'

apps_client.create_company_app(body, authorization, content_type, org, company)

```


### <a name="add_app_credentials"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.add_app_credentials") add_app_credentials

> Add app credentials

```python
def add_app_credentials(self,
                            body,
                            authorization,
                            content_type,
                            org)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = 'Body'
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

apps_client.add_app_credentials(body, authorization, content_type, org)

```


### <a name="list_apps"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.list_apps") list_apps

> List apps 

```python
def list_apps(self,
                  authorization,
                  org)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
org = 'ORG'

apps_client.list_apps(authorization, org)

```


### <a name="list_app"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.list_app") list_app

> List app

```python
def list_app(self,
                 authorization,
                 org)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
org = 'ORG'

apps_client.list_app(authorization, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="virtual_hosts_controller"></a>![Class: ](https://apidocs.io/img/class.png ".VirtualHostsController") VirtualHostsController

### Get controller instance

An instance of the ``` VirtualHostsController ``` class can be accessed from the API Client.

```python
 virtual_hosts_client = client.virtual_hosts
```

### <a name="list_virtual_hosts"></a>![Method: ](https://apidocs.io/img/method.png ".VirtualHostsController.list_virtual_hosts") list_virtual_hosts

> List VirtualHosts

```python
def list_virtual_hosts(self,
                           authorization,
                           org,
                           env)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
org = 'ORG'
env = 'ENV'

virtual_hosts_client.list_virtual_hosts(authorization, org, env)

```


### <a name="add_virtual_host"></a>![Method: ](https://apidocs.io/img/method.png ".VirtualHostsController.add_virtual_host") add_virtual_host

> Add Virtual Host

```python
def add_virtual_host(self,
                         body,
                         authorization,
                         content_type,
                         org,
                         env)
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

```python
body = 'Body'
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'
env = 'ENV'

virtual_hosts_client.add_virtual_host(body, authorization, content_type, org, env)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="environments_controller"></a>![Class: ](https://apidocs.io/img/class.png ".EnvironmentsController") EnvironmentsController

### Get controller instance

An instance of the ``` EnvironmentsController ``` class can be accessed from the API Client.

```python
 environments_client = client.environments
```

### <a name="update_environments"></a>![Method: ](https://apidocs.io/img/method.png ".EnvironmentsController.update_environments") update_environments

> Update Environments

```python
def update_environments(self,
                            authorization,
                            content_type,
                            org,
                            env)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'
env = 'ENV'

environments_client.update_environments(authorization, content_type, org, env)

```


### <a name="delete_environment"></a>![Method: ](https://apidocs.io/img/method.png ".EnvironmentsController.delete_environment") delete_environment

> Delete Environment

```python
def delete_environment(self,
                           authorization,
                           org,
                           env)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
org = 'ORG'
env = 'ENV'

environments_client.delete_environment(authorization, org, env)

```


### <a name="create_new_env_in_org"></a>![Method: ](https://apidocs.io/img/method.png ".EnvironmentsController.create_new_env_in_org") create_new_env_in_org

> Create New ENV in ORG

```python
def create_new_env_in_org(self,
                              body,
                              authorization,
                              content_type,
                              org)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = 'Body'
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

environments_client.create_new_env_in_org(body, authorization, content_type, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="developer_app_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DeveloperAppController") DeveloperAppController

### Get controller instance

An instance of the ``` DeveloperAppController ``` class can be accessed from the API Client.

```python
 developer_app_client = client.developer_app
```

### <a name="get_developer_app_details_get"></a>![Method: ](https://apidocs.io/img/method.png ".DeveloperAppController.get_developer_app_details_get") get_developer_app_details_get

> Developer App Details Get

```python
def get_developer_app_details_get(self,
                                      authorization,
                                      content_type,
                                      org)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

developer_app_client.get_developer_app_details_get(authorization, content_type, org)

```


### <a name="delete_app_credentials"></a>![Method: ](https://apidocs.io/img/method.png ".DeveloperAppController.delete_app_credentials") delete_app_credentials

> Delete app credentials

```python
def delete_app_credentials(self,
                               authorization,
                               accept,
                               org)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
accept = 'Accept'
org = 'ORG'

developer_app_client.delete_app_credentials(authorization, accept, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="keystores_controller"></a>![Class: ](https://apidocs.io/img/class.png ".KeystoresController") KeystoresController

### Get controller instance

An instance of the ``` KeystoresController ``` class can be accessed from the API Client.

```python
 keystores_client = client.keystores
```

### <a name="list_keystores"></a>![Method: ](https://apidocs.io/img/method.png ".KeystoresController.list_keystores") list_keystores

> List Keystores

```python
def list_keystores(self,
                       authorization,
                       org,
                       env)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
org = 'ORG'
env = 'ENV'

keystores_client.list_keystores(authorization, org, env)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="products_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductsController") ProductsController

### Get controller instance

An instance of the ``` ProductsController ``` class can be accessed from the API Client.

```python
 products_client = client.products
```

### <a name="get_api_products"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.get_api_products") get_api_products

> Api Products

```python
def get_api_products(self,
                         authorization,
                         org)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
org = 'ORG'

products_client.get_api_products(authorization, org)

```


### <a name="create_ap_iproduct_creation"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.create_ap_iproduct_creation") create_ap_iproduct_creation

> APIproduct Creation

```python
def create_ap_iproduct_creation(self,
                                    body,
                                    authorization,
                                    content_type,
                                    org)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = 'Body'
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

products_client.create_ap_iproduct_creation(body, authorization, content_type, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="target_servers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".TargetServersController") TargetServersController

### Get controller instance

An instance of the ``` TargetServersController ``` class can be accessed from the API Client.

```python
 target_servers_client = client.target_servers
```

### <a name="list_target_servers"></a>![Method: ](https://apidocs.io/img/method.png ".TargetServersController.list_target_servers") list_target_servers

> List Target Servers

```python
def list_target_servers(self,
                            authorization,
                            org,
                            env)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Authorization'
org = 'ORG'
env = 'ENV'

target_servers_client.list_target_servers(authorization, org, env)

```


### <a name="add_target"></a>![Method: ](https://apidocs.io/img/method.png ".TargetServersController.add_target") add_target

> Add Target

```python
def add_target(self,
                   body,
                   content_type,
                   authorization,
                   org,
                   env)
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

```python
body = AddTargetRequest()
content_type = 'content-type'
authorization = 'Authorization'
org = 'ORG'
env = 'ENV'

target_servers_client.add_target(body, content_type, authorization, org, env)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="company_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CompanyController") CompanyController

### Get controller instance

An instance of the ``` CompanyController ``` class can be accessed from the API Client.

```python
 company_client = client.company
```

### <a name="create_company"></a>![Method: ](https://apidocs.io/img/method.png ".CompanyController.create_company") create_company

> Create Company

```python
def create_company(self,
                       body,
                       authorization,
                       content_type,
                       org)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = 'Body'
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

company_client.create_company(body, authorization, content_type, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="organizations_controller"></a>![Class: ](https://apidocs.io/img/class.png ".OrganizationsController") OrganizationsController

### Get controller instance

An instance of the ``` OrganizationsController ``` class can be accessed from the API Client.

```python
 organizations_client = client.organizations
```

### <a name="list_organizations"></a>![Method: ](https://apidocs.io/img/method.png ".OrganizationsController.list_organizations") list_organizations

> List organizations

```python
def list_organizations(self,
                           authorization)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
authorization = 'Basic {{BASICAUTH}}'

organizations_client.list_organizations(authorization)

```


[Back to List of Controllers](#list_of_controllers)




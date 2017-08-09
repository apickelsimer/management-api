# Getting started

TODO: Add Description

## How to Build

This client library is a Ruby gem which can be compiled and used in your Ruby and Ruby on Rails project. This library requires a few gems from the RubyGems repository.

1. Open the command line interface or the terminal and navigate to the folder containing the source code.
2. Run ``` gem build apigee_edge_api_management.gemspec ``` to build the gem.
3. Once built, the gem can be installed on the current work environment using ``` gem install apigee_edge_api_management-1.0.0.gem ```

![Building Gem](https://apidocs.io/illustration/ruby?step=buildSDK&workspaceFolder=Apigee%20Edge%20API%20Management-Ruby&workspaceName=Apigee%20Edge%20API%20Management-Ruby&projectName=apigee_edge_api_management&gemName=apigee_edge_api_management&gemVer=1.0.0)

## How to Use

The following section explains how to use the ApigeeEdgeApiManagement Ruby Gem in a new Rails project using RubyMine&trade;. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

### 1. Starting a new project

Close any existing projects in RubyMine&trade; by selecting ``` File -> Close Project ```. Next, click on ``` Create New Project ``` to create a new project from scratch.

![Create a new project in RubyMine](https://apidocs.io/illustration/ruby?step=createNewProject0&workspaceFolder=Apigee%20Edge%20API%20Management-Ruby&workspaceName=ApigeeEdgeApiManagement&projectName=apigee_edge_api_management&gemName=apigee_edge_api_management&gemVer=1.0.0)

Next, provide ``` TestApp ``` as the project name, choose ``` Rails Application ``` as the project type, and click ``` OK ```.

![Create a new Rails Application in RubyMine - step 1](https://apidocs.io/illustration/ruby?step=createNewProject1&workspaceFolder=Apigee%20Edge%20API%20Management-Ruby&workspaceName=ApigeeEdgeApiManagement&projectName=apigee_edge_api_management&gemName=apigee_edge_api_management&gemVer=1.0.0)

In the next dialog make sure that correct *Ruby SDK* is being used (minimum 2.0.0) and click ``` OK ```.

![Create a new Rails Application in RubyMine - step 2](https://apidocs.io/illustration/ruby?step=createNewProject2&workspaceFolder=Apigee%20Edge%20API%20Management-Ruby&workspaceName=ApigeeEdgeApiManagement&projectName=apigee_edge_api_management&gemName=apigee_edge_api_management&gemVer=1.0.0)

This will create a new Rails Application project with an existing set of files and folder.

### 2. Add reference of the gem

In order to use the ApigeeEdgeApiManagement gem in the new project we must add a gem reference. Locate the ```Gemfile``` in the *Project Explorer* window under the ``` TestApp ``` project node. The file contains references to all gems being used in the project. Here, add the reference to the library gem by adding the following line: ``` gem 'apigee_edge_api_management', '~> 1.0.0' ```

![Add references of the Gemfile](https://apidocs.io/illustration/ruby?step=addReference&workspaceFolder=Apigee%20Edge%20API%20Management-Ruby&workspaceName=ApigeeEdgeApiManagement&projectName=apigee_edge_api_management&gemName=apigee_edge_api_management&gemVer=1.0.0)

### 3. Adding a new Rails Controller

Once the ``` TestApp ``` project is created, a folder named ``` controllers ``` will be visible in the *Project Explorer* under the following path: ``` TestApp > app > controllers ```. Right click on this folder and select ``` New -> Run Rails Generator... ```.

![Run Rails Generator on Controllers Folder](https://apidocs.io/illustration/ruby?step=addCode0&workspaceFolder=Apigee%20Edge%20API%20Management-Ruby&workspaceName=ApigeeEdgeApiManagement&projectName=apigee_edge_api_management&gemName=apigee_edge_api_management&gemVer=1.0.0)

Selecting the said option will popup a small window where the generator names are displayed. Here, select the ``` controller ``` template.

![Create a new Controller](https://apidocs.io/illustration/ruby?step=addCode1&workspaceFolder=Apigee%20Edge%20API%20Management-Ruby&workspaceName=ApigeeEdgeApiManagement&projectName=apigee_edge_api_management&gemName=apigee_edge_api_management&gemVer=1.0.0)

Next, a popup window will ask you for a Controller name and included Actions. For controller name provide ``` Hello ``` and include an action named ``` Index ``` and click ``` OK ```.

![Add a new Controller](https://apidocs.io/illustration/ruby?step=addCode2&workspaceFolder=Apigee%20Edge%20API%20Management-Ruby&workspaceName=ApigeeEdgeApiManagement&projectName=apigee_edge_api_management&gemName=apigee_edge_api_management&gemVer=1.0.0)

A new controller class anmed ``` HelloController ``` will be created in a file named ``` hello_controller.rb ``` containing a method named ``` Index ```. In this method, add code for initialization and a sample for its usage.

![Initialize the library](https://apidocs.io/illustration/ruby?step=addCode3&workspaceFolder=Apigee%20Edge%20API%20Management-Ruby&workspaceName=ApigeeEdgeApiManagement&projectName=apigee_edge_api_management&gemName=apigee_edge_api_management&gemVer=1.0.0)

## How to Test

You can test the generated SDK and the server with automatically generated test
cases as follows:

  1. From terminal/cmd navigate to the root directory of the SDK.
  2. Invoke: `bundle exec rake`

## Initialization

### Authentication
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| basic_auth_user_name | The username to use with basic authentication |
| basic_auth_password | The password to use with basic authentication |



API client can be initialized as following.

```ruby
# Configuration parameters and credentials
basic_auth_user_name = 'basic_auth_user_name' # The username to use with basic authentication
basic_auth_password = 'basic_auth_password' # The password to use with basic authentication

client = ApigeeEdgeApiManagement::ApigeeEdgeApiManagementClient.new(
  basic_auth_user_name: basic_auth_user_name,
  basic_auth_password: basic_auth_password
)
```

The added initlization code can be debugged by putting a breakpoint in the ``` Index ``` method and running the project in debug mode by selecting ``` Run -> Debug 'Development: TestApp' ```.

![Debug the TestApp](https://apidocs.io/illustration/ruby?step=addCode4&workspaceFolder=Apigee%20Edge%20API%20Management-Ruby&workspaceName=ApigeeEdgeApiManagement&projectName=apigee_edge_api_management&gemName=apigee_edge_api_management&gemVer=1.0.0&initLine=client%2520%253D%2520ApigeeEdgeApiManagementClient.new%2528%2527basic_auth_user_name%2527%252C%2520%2527basic_auth_password%2527%2529)



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

```ruby
deployments = client.deployments
```

### <a name="list_deployments"></a>![Method: ](https://apidocs.io/img/method.png ".DeploymentsController.list_deployments") list_deployments

> List Deployments


```ruby
def list_deployments(authorization,
                         org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
org = 'ORG'

deployments.list_deployments(authorization, org)

```


### <a name="get_deployments"></a>![Method: ](https://apidocs.io/img/method.png ".DeploymentsController.get_deployments") get_deployments

> Deployments


```ruby
def get_deployments(authorization,
                        org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
org = 'ORG'

deployments.get_deployments(authorization, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="user_roles_controller"></a>![Class: ](https://apidocs.io/img/class.png ".UserRolesController") UserRolesController

### Get singleton instance

The singleton instance of the ``` UserRolesController ``` class can be accessed from the API Client.

```ruby
userRoles = client.user_roles
```

### <a name="create_user_roles_update"></a>![Method: ](https://apidocs.io/img/method.png ".UserRolesController.create_user_roles_update") create_user_roles_update

> User Roles Update


```ruby
def create_user_roles_update(body,
                                 authorization,
                                 content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body_value = "{ \"role\" : [ { \"name\" : \"orgadmin\", \"organization\" : \"dev\" }, { \"name\" : \"sysadmin\" } ] }";
body = JSON.parse(body_value);
authorization = 'Basic {{BASICAUTH}}'
content_type = 'application/json'

userRoles.create_user_roles_update(body, authorization, content_type)

```


### <a name="delete_an_organization_userrole"></a>![Method: ](https://apidocs.io/img/method.png ".UserRolesController.delete_an_organization_userrole") delete_an_organization_userrole

> Delete an organization userrole


```ruby
def delete_an_organization_userrole(org,
                                        authorization,
                                        accept); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| org |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
org = '{{ORG}}'
authorization = 'Basic {{BASICAUTH}}'
accept = 'application/json'

userRoles.delete_an_organization_userrole(org, authorization, accept)

```


### <a name="get_permissions_for_a_role"></a>![Method: ](https://apidocs.io/img/method.png ".UserRolesController.get_permissions_for_a_role") get_permissions_for_a_role

> Get permissions for a role


```ruby
def get_permissions_for_a_role(authorization,
                                   content_type,
                                   org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

userRoles.get_permissions_for_a_role(authorization, content_type, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="o_auth_controller"></a>![Class: ](https://apidocs.io/img/class.png ".OAuthController") OAuthController

### Get singleton instance

The singleton instance of the ``` OAuthController ``` class can be accessed from the API Client.

```ruby
oAuth = client.o_auth
```

### <a name="get_o_auth_2_token_details_get"></a>![Method: ](https://apidocs.io/img/method.png ".OAuthController.get_o_auth_2_token_details_get") get_o_auth_2_token_details_get

> OAuth2 Token Details Get


```ruby
def get_o_auth_2_token_details_get(authorization,
                                       content_type,
                                       org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

oAuth.get_o_auth_2_token_details_get(authorization, content_type, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="kvm_controller"></a>![Class: ](https://apidocs.io/img/class.png ".KVMController") KVMController

### Get singleton instance

The singleton instance of the ``` KVMController ``` class can be accessed from the API Client.

```ruby
kVM = client.kvm
```

### <a name="get_kvm_get"></a>![Method: ](https://apidocs.io/img/method.png ".KVMController.get_kvm_get") get_kvm_get

> KVM Get


```ruby
def get_kvm_get(authorization,
                    content_type,
                    org,
                    env); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |
| env |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'
env = 'ENV'

kVM.get_kvm_get(authorization, content_type, org, env)

```


### <a name="delete_kvm_delete_entire_kvm"></a>![Method: ](https://apidocs.io/img/method.png ".KVMController.delete_kvm_delete_entire_kvm") delete_kvm_delete_entire_kvm

> KVM Delete (Entire KVM)


```ruby
def delete_kvm_delete_entire_kvm(authorization,
                                     content_type,
                                     org,
                                     env); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |
| env |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'
env = 'ENV'

kVM.delete_kvm_delete_entire_kvm(authorization, content_type, org, env)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="pods_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PodsController") PodsController

### Get singleton instance

The singleton instance of the ``` PodsController ``` class can be accessed from the API Client.

```ruby
pods = client.pods
```

### <a name="get_analytics_pod"></a>![Method: ](https://apidocs.io/img/method.png ".PodsController.get_analytics_pod") get_analytics_pod

> Analytics pod


```ruby
def get_analytics_pod(pod,
                          authorization); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| pod |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
pod = 'analytics'
authorization = 'Basic {{BASICAUTH}}'

pods.get_analytics_pod(pod, authorization)

```


### <a name="get_associated_pods"></a>![Method: ](https://apidocs.io/img/method.png ".PodsController.get_associated_pods") get_associated_pods

> Get Associated  Pods


```ruby
def get_associated_pods(content_type,
                            authorization,
                            org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
content_type = 'Content-Type'
authorization = 'Authorization'
org = 'ORG'

pods.get_associated_pods(content_type, authorization, org)

```


### <a name="create_disassociate_org_from_pod"></a>![Method: ](https://apidocs.io/img/method.png ".PodsController.create_disassociate_org_from_pod") create_disassociate_org_from_pod

> Disassociate Org from POD


```ruby
def create_disassociate_org_from_pod(content_type,
                                         authorization,
                                         org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
content_type = 'Content-Type'
authorization = 'Authorization'
org = 'ORG'

pods.create_disassociate_org_from_pod(content_type, authorization, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="servers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ServersController") ServersController

### Get singleton instance

The singleton instance of the ``` ServersController ``` class can be accessed from the API Client.

```ruby
servers = client.servers
```

### <a name="create_deregister"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.create_deregister") create_deregister

> Deregister


```ruby
def create_deregister(authorization,
                          content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Basic {{BASICAUTH}}'
content_type = 'application/x-www-form-urlencoded'

servers.create_deregister(authorization, content_type)

```


### <a name="list_server_by_uuid"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.list_server_by_uuid") list_server_by_uuid

> List Server by UUID


```ruby
def list_server_by_uuid(authorization,
                            uuid); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| uuid |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Basic {{BASICAUTH}}'
uuid = 'uuid'

servers.list_server_by_uuid(authorization, uuid)

```


### <a name="create_set_not_reachable"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.create_set_not_reachable") create_set_not_reachable

> Set not reachable


```ruby
def create_set_not_reachable(reachable,
                                 authorization); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| reachable |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
reachable = 'false'
authorization = 'Basic {{BASICAUTH}}'

servers.create_set_not_reachable(reachable, authorization)

```


### <a name="list_org_env_servers"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.list_org_env_servers") list_org_env_servers

> List org/env servers


```ruby
def list_org_env_servers(authorization,
                             org,
                             env); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |
| env |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
org = 'ORG'
env = 'ENV'

servers.list_org_env_servers(authorization, org, env)

```


### <a name="create_register_server_with_org"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.create_register_server_with_org") create_register_server_with_org

> Register server with org


```ruby
def create_register_server_with_org(authorization,
                                        content_type,
                                        org,
                                        env); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |
| env |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'
env = 'ENV'

servers.create_register_server_with_org(authorization, content_type, org, env)

```


### <a name="create_associate_environments_to_mp"></a>![Method: ](https://apidocs.io/img/method.png ".ServersController.create_associate_environments_to_mp") create_associate_environments_to_mp

> Associate  environments to MP


```ruby
def create_associate_environments_to_mp(authorization,
                                            content_type,
                                            org,
                                            env); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |
| env |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'
env = 'ENV'

servers.create_associate_environments_to_mp(authorization, content_type, org, env)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="developers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DevelopersController") DevelopersController

### Get singleton instance

The singleton instance of the ``` DevelopersController ``` class can be accessed from the API Client.

```ruby
developers = client.developers
```

### <a name="get_developers"></a>![Method: ](https://apidocs.io/img/method.png ".DevelopersController.get_developers") get_developers

> Get Developers


```ruby
def get_developers(authorization,
                       content_type,
                       org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

developers.get_developers(authorization, content_type, org)

```


### <a name="create_developer"></a>![Method: ](https://apidocs.io/img/method.png ".DevelopersController.create_developer") create_developer

> Create Developer


```ruby
def create_developer(body,
                         authorization,
                         content_type,
                         org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = 'Body'
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

developers.create_developer(body, authorization, content_type, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="ap_is_controller"></a>![Class: ](https://apidocs.io/img/class.png ".APIsController") APIsController

### Get singleton instance

The singleton instance of the ``` APIsController ``` class can be accessed from the API Client.

```ruby
aPIs = client.ap_is
```

### <a name="get_api_list"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.get_api_list") get_api_list

> Api list


```ruby
def get_api_list(authorization,
                     org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
org = 'ORG'

aPIs.get_api_list(authorization, org)

```


### <a name="create_deploy_api"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.create_deploy_api") create_deploy_api

> Deploy API


```ruby
def create_deploy_api(action,
                          name,
                          authorization,
                          content_type,
                          org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| action |  ``` Required ```  | TODO: Add a parameter description |
| name |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
action = 'action'
name = 'name'
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

aPIs.create_deploy_api(action, name, authorization, content_type, org)

```


### <a name="delete_an_api"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.delete_an_api") delete_an_api

> Delete an API


```ruby
def delete_an_api(authorization,
                      org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
org = 'ORG'

aPIs.delete_an_api(authorization, org)

```


### <a name="create_undeploy_revisions"></a>![Method: ](https://apidocs.io/img/method.png ".APIsController.create_undeploy_revisions") create_undeploy_revisions

> Undeploy Revisions


```ruby
def create_undeploy_revisions(action,
                                  env,
                                  authorization,
                                  content_type,
                                  org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| action |  ``` Required ```  | TODO: Add a parameter description |
| env |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
action = 'action'
env = 'env'
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

aPIs.create_undeploy_revisions(action, env, authorization, content_type, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="cache_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CacheController") CacheController

### Get singleton instance

The singleton instance of the ``` CacheController ``` class can be accessed from the API Client.

```ruby
cache = client.cache
```

### <a name="list_caches"></a>![Method: ](https://apidocs.io/img/method.png ".CacheController.list_caches") list_caches

> List caches


```ruby
def list_caches(authorization,
                    org,
                    env); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |
| env |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
org = 'ORG'
env = 'ENV'

cache.list_caches(authorization, org, env)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="audit_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AuditController") AuditController

### Get singleton instance

The singleton instance of the ``` AuditController ``` class can be accessed from the API Client.

```ruby
audit = client.audit
```

### <a name="get_audit"></a>![Method: ](https://apidocs.io/img/method.png ".AuditController.get_audit") get_audit

> Audit


```ruby
def get_audit(expand,
                  timeline,
                  authorization,
                  org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| expand |  ``` Required ```  | TODO: Add a parameter description |
| timeline |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
expand = true
timeline = 'timeline'
authorization = 'Authorization'
org = 'ORG'

audit.get_audit(expand, timeline, authorization, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="users_controller"></a>![Class: ](https://apidocs.io/img/class.png ".UsersController") UsersController

### Get singleton instance

The singleton instance of the ``` UsersController ``` class can be accessed from the API Client.

```ruby
users = client.users
```

### <a name="get_developer_details_get"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.get_developer_details_get") get_developer_details_get

> Developer Details Get


```ruby
def get_developer_details_get(authorization,
                                  content_type,
                                  org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

users.get_developer_details_get(authorization, content_type, org)

```


### <a name="create_user_in_org"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.create_user_in_org") create_user_in_org

> Create User in ORG


```ruby
def create_user_in_org(body,
                           authorization,
                           content_type,
                           org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = 'Body'
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

users.create_user_in_org(body, authorization, content_type, org)

```


### <a name="list_users"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.list_users") list_users

> List Users


```ruby
def list_users(authorization); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Basic {{BASICAUTH}}'

users.list_users(authorization)

```


### <a name="add_user_as_orgadmin"></a>![Method: ](https://apidocs.io/img/method.png ".UsersController.add_user_as_orgadmin") add_user_as_orgadmin

> Add user as Orgadmin


```ruby
def add_user_as_orgadmin(body,
                             authorization,
                             content_type,
                             org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = 'Body'
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

users.add_user_as_orgadmin(body, authorization, content_type, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="zzz_others_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ZzzOthersController") ZzzOthersController

### Get singleton instance

The singleton instance of the ``` ZzzOthersController ``` class can be accessed from the API Client.

```ruby
zzzOthers = client.zzz_others
```

### <a name="get_cluster_status"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.get_cluster_status") get_cluster_status

> Cluster Status


```ruby
def get_cluster_status(authorization); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Basic {{BASICAUTH}}'

zzzOthers.get_cluster_status(authorization)

```


### <a name="create_enable_debug_w_o_restart"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.create_enable_debug_w_o_restart") create_enable_debug_w_o_restart

> Enable Debug w/o Restart 


```ruby
def create_enable_debug_w_o_restart(session,
                                        authorization,
                                        content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| session |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
session = 'logsession_name'
authorization = 'Basic {{BASICAUTH}}'
content_type = 'application/x-www-form-urlencoded'

zzzOthers.create_enable_debug_w_o_restart(session, authorization, content_type)

```


### <a name="get_classifications"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.get_classifications") get_classifications

> Classifications


```ruby
def get_classifications(authorization,
                            host); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| host |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
host = 'HOST'

zzzOthers.get_classifications(authorization, host)

```


### <a name="create_company_developer"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.create_company_developer") create_company_developer

> Create Company Developer


```ruby
def create_company_developer(body,
                                 content_type,
                                 authorization,
                                 org,
                                 company); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |
| company |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = CreateCompanyDeveloperRequest.new
content_type = 'Content-Type'
authorization = 'Authorization'
org = 'ORG'
company = 'COMPANY'

zzzOthers.create_company_developer(body, content_type, authorization, org, company)

```


### <a name="get_qpid_metrics"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.get_qpid_metrics") get_qpid_metrics

> QPID Metrics


```ruby
def get_qpid_metrics(authorization,
                         host); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| host |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
host = 'HOST'

zzzOthers.get_qpid_metrics(authorization, host)

```


### <a name="get_build_info"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.get_build_info") get_build_info

> Build Info


```ruby
def get_build_info(authorization,
                       host,
                       port); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| host |  ``` Required ```  | TODO: Add a parameter description |
| port |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
host = 'HOST'
port = 'PORT'

zzzOthers.get_build_info(authorization, host, port)

```


### <a name="delete_disable_debug_w_o_restart"></a>![Method: ](https://apidocs.io/img/method.png ".ZzzOthersController.delete_disable_debug_w_o_restart") delete_disable_debug_w_o_restart

> Disable Debug w/o Restart


```ruby
def delete_disable_debug_w_o_restart(authorization,
                                         content_type); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Basic {{BASICAUTH}}'
content_type = 'application/x-www-form-urlencoded'

zzzOthers.delete_disable_debug_w_o_restart(authorization, content_type)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="apps_controller"></a>![Class: ](https://apidocs.io/img/class.png ".AppsController") AppsController

### Get singleton instance

The singleton instance of the ``` AppsController ``` class can be accessed from the API Client.

```ruby
apps = client.apps
```

### <a name="create_company_app"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.create_company_app") create_company_app

> Create Company APP


```ruby
def create_company_app(body,
                           authorization,
                           content_type,
                           org,
                           company); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |
| company |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = 'Body'
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'
company = 'COMPANY'

apps.create_company_app(body, authorization, content_type, org, company)

```


### <a name="add_app_credentials"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.add_app_credentials") add_app_credentials

> Add app credentials


```ruby
def add_app_credentials(body,
                            authorization,
                            content_type,
                            org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = 'Body'
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

apps.add_app_credentials(body, authorization, content_type, org)

```


### <a name="list_apps"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.list_apps") list_apps

> List apps 


```ruby
def list_apps(authorization,
                  org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
org = 'ORG'

apps.list_apps(authorization, org)

```


### <a name="list_app"></a>![Method: ](https://apidocs.io/img/method.png ".AppsController.list_app") list_app

> List app


```ruby
def list_app(authorization,
                 org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
org = 'ORG'

apps.list_app(authorization, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="virtual_hosts_controller"></a>![Class: ](https://apidocs.io/img/class.png ".VirtualHostsController") VirtualHostsController

### Get singleton instance

The singleton instance of the ``` VirtualHostsController ``` class can be accessed from the API Client.

```ruby
virtualHosts = client.virtual_hosts
```

### <a name="list_virtual_hosts"></a>![Method: ](https://apidocs.io/img/method.png ".VirtualHostsController.list_virtual_hosts") list_virtual_hosts

> List VirtualHosts


```ruby
def list_virtual_hosts(authorization,
                           org,
                           env); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |
| env |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
org = 'ORG'
env = 'ENV'

virtualHosts.list_virtual_hosts(authorization, org, env)

```


### <a name="add_virtual_host"></a>![Method: ](https://apidocs.io/img/method.png ".VirtualHostsController.add_virtual_host") add_virtual_host

> Add Virtual Host


```ruby
def add_virtual_host(body,
                         authorization,
                         content_type,
                         org,
                         env); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |
| env |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = 'Body'
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'
env = 'ENV'

virtualHosts.add_virtual_host(body, authorization, content_type, org, env)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="environments_controller"></a>![Class: ](https://apidocs.io/img/class.png ".EnvironmentsController") EnvironmentsController

### Get singleton instance

The singleton instance of the ``` EnvironmentsController ``` class can be accessed from the API Client.

```ruby
environments = client.environments
```

### <a name="update_environments"></a>![Method: ](https://apidocs.io/img/method.png ".EnvironmentsController.update_environments") update_environments

> Update Environments


```ruby
def update_environments(authorization,
                            content_type,
                            org,
                            env); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |
| env |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'
env = 'ENV'

environments.update_environments(authorization, content_type, org, env)

```


### <a name="delete_environment"></a>![Method: ](https://apidocs.io/img/method.png ".EnvironmentsController.delete_environment") delete_environment

> Delete Environment


```ruby
def delete_environment(authorization,
                           org,
                           env); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |
| env |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
org = 'ORG'
env = 'ENV'

environments.delete_environment(authorization, org, env)

```


### <a name="create_new_env_in_org"></a>![Method: ](https://apidocs.io/img/method.png ".EnvironmentsController.create_new_env_in_org") create_new_env_in_org

> Create New ENV in ORG


```ruby
def create_new_env_in_org(body,
                              authorization,
                              content_type,
                              org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = 'Body'
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

environments.create_new_env_in_org(body, authorization, content_type, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="developer_app_controller"></a>![Class: ](https://apidocs.io/img/class.png ".DeveloperAppController") DeveloperAppController

### Get singleton instance

The singleton instance of the ``` DeveloperAppController ``` class can be accessed from the API Client.

```ruby
developerApp = client.developer_app
```

### <a name="get_developer_app_details_get"></a>![Method: ](https://apidocs.io/img/method.png ".DeveloperAppController.get_developer_app_details_get") get_developer_app_details_get

> Developer App Details Get


```ruby
def get_developer_app_details_get(authorization,
                                      content_type,
                                      org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

developerApp.get_developer_app_details_get(authorization, content_type, org)

```


### <a name="delete_app_credentials"></a>![Method: ](https://apidocs.io/img/method.png ".DeveloperAppController.delete_app_credentials") delete_app_credentials

> Delete app credentials


```ruby
def delete_app_credentials(authorization,
                               accept,
                               org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
accept = 'Accept'
org = 'ORG'

developerApp.delete_app_credentials(authorization, accept, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="keystores_controller"></a>![Class: ](https://apidocs.io/img/class.png ".KeystoresController") KeystoresController

### Get singleton instance

The singleton instance of the ``` KeystoresController ``` class can be accessed from the API Client.

```ruby
keystores = client.keystores
```

### <a name="list_keystores"></a>![Method: ](https://apidocs.io/img/method.png ".KeystoresController.list_keystores") list_keystores

> List Keystores


```ruby
def list_keystores(authorization,
                       org,
                       env); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |
| env |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
org = 'ORG'
env = 'ENV'

keystores.list_keystores(authorization, org, env)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="products_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductsController") ProductsController

### Get singleton instance

The singleton instance of the ``` ProductsController ``` class can be accessed from the API Client.

```ruby
products = client.products
```

### <a name="get_api_products"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.get_api_products") get_api_products

> Api Products


```ruby
def get_api_products(authorization,
                         org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
org = 'ORG'

products.get_api_products(authorization, org)

```


### <a name="create_ap_iproduct_creation"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.create_ap_iproduct_creation") create_ap_iproduct_creation

> APIproduct Creation


```ruby
def create_ap_iproduct_creation(body,
                                    authorization,
                                    content_type,
                                    org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = 'Body'
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

products.create_ap_iproduct_creation(body, authorization, content_type, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="target_servers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".TargetServersController") TargetServersController

### Get singleton instance

The singleton instance of the ``` TargetServersController ``` class can be accessed from the API Client.

```ruby
targetServers = client.target_servers
```

### <a name="list_target_servers"></a>![Method: ](https://apidocs.io/img/method.png ".TargetServersController.list_target_servers") list_target_servers

> List Target Servers


```ruby
def list_target_servers(authorization,
                            org,
                            env); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |
| env |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Authorization'
org = 'ORG'
env = 'ENV'

targetServers.list_target_servers(authorization, org, env)

```


### <a name="add_target"></a>![Method: ](https://apidocs.io/img/method.png ".TargetServersController.add_target") add_target

> Add Target


```ruby
def add_target(body,
                   content_type,
                   authorization,
                   org,
                   env); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |
| env |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = AddTargetRequest.new
content_type = 'content-type'
authorization = 'Authorization'
org = 'ORG'
env = 'ENV'

targetServers.add_target(body, content_type, authorization, org, env)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="company_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CompanyController") CompanyController

### Get singleton instance

The singleton instance of the ``` CompanyController ``` class can be accessed from the API Client.

```ruby
company = client.company
```

### <a name="create_company"></a>![Method: ](https://apidocs.io/img/method.png ".CompanyController.create_company") create_company

> Create Company


```ruby
def create_company(body,
                       authorization,
                       content_type,
                       org); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| content_type |  ``` Required ```  | TODO: Add a parameter description |
| org |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = 'Body'
authorization = 'Authorization'
content_type = 'Content-Type'
org = 'ORG'

company.create_company(body, authorization, content_type, org)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="organizations_controller"></a>![Class: ](https://apidocs.io/img/class.png ".OrganizationsController") OrganizationsController

### Get singleton instance

The singleton instance of the ``` OrganizationsController ``` class can be accessed from the API Client.

```ruby
organizations = client.organizations
```

### <a name="list_organizations"></a>![Method: ](https://apidocs.io/img/method.png ".OrganizationsController.list_organizations") list_organizations

> List organizations


```ruby
def list_organizations(authorization); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
authorization = 'Basic {{BASICAUTH}}'

organizations.list_organizations(authorization)

```


[Back to List of Controllers](#list_of_controllers)




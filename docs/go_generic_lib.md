# Getting started

TODO: Add Description

## How to Build


* In order to successfully build and run your SDK files, you are required to have the following setup in your system:
    * **Go**  (Visit [https://golang.org/doc/install](https://golang.org/doc/install) for more details on how to install Go)
    * **Java VM** Version 8 or later
    * **Eclipse 4.6 (Neon)** or later ([http://www.eclipse.org/neon/](http://www.eclipse.org/neon/))
    * **GoClipse** setup within above installed Eclipse (Follow the instructions at [this link](https://github.com/GoClipse/goclipse/blob/latest/documentation/Installation.md#instructions) to setup GoClipse)
* Ensure that ```GOPATH``` environment variable is set in the system variables. If not, set it to your workspace directory where you will be adding your Go projects.
* The generated code uses unirest-go http library. Therefore, you will need internet access to resolve this dependency. If Go is properly installed and configured, run the following command to pull the dependency:

```Go
go get github.com/apimatic/unirest-go
```

This will install unirest-go in the ```GOPATH``` you specified in the system variables.

Now follow the steps mentioned below to build your SDK:

1. Open eclipse in the Go language perspective and click on the ```Import``` option in ```File``` menu.

![Importing SDK into Eclipse - Step 1](https://apidocs.io/illustration/go?step=import0)

2. Select ```General -> Existing Projects into Workspace``` option from the tree list.

![Importing SDK into Eclipse - Step 2](https://apidocs.io/illustration/go?step=import1)

3. In ```Select root directory```, provide path to the unzipped archive for the generated code. Once the path is set and the Project becomes visible under ```Projects``` click ```Finish```

![Importing SDK into Eclipse - Step 3](https://apidocs.io/illustration/go?step=import2&workspaceFolder=Apigee%20Edge%20API%20Management-GoLang&projectName=apigeeedgeapimanagement_lib)

4. The Go library will be imported and its files will be visible in the Project Explorer

![Importing SDK into Eclipse - Step 4](https://apidocs.io/illustration/go?step=import3&projectName=apigeeedgeapimanagement_lib)

## How to Use

The following section explains how to use the ApigeeedgeapimanagementLib library in a new project.

### 1. Add a new Test Project

Create a new project in Eclipse by ```File``` -> ```New``` -> ```Go Project```

![Add a new project in Eclipse](https://apidocs.io/illustration/go?step=createNewProject0)

Name the Project as ```Test``` and click ```Finish```

![Create a new Maven Project - Step 1](https://apidocs.io/illustration/go?step=createNewProject1)

Create a new directory in the ```src``` directory of this project

![Create a new Maven Project - Step 2](https://apidocs.io/illustration/go?step=createNewProject2&projectName=apigeeedgeapimanagement_lib)

Name it ```test.com```

![Create a new Maven Project - Step 3](https://apidocs.io/illustration/go?step=createNewProject3&projectName=apigeeedgeapimanagement_lib)

Now create a new file inside ```src/test.com```

![Create a new Maven Project - Step 4](https://apidocs.io/illustration/go?step=createNewProject4&projectName=apigeeedgeapimanagement_lib)

Name it ```testsdk.go```

![Create a new Maven Project - Step 5](https://apidocs.io/illustration/go?step=createNewProject5&projectName=apigeeedgeapimanagement_lib)

In this Go file, you can start adding code to initialize the client library. Sample code to initialize the client library and using its methods is given in the subsequent sections.

### 2. Configure the Test Project

You need to import your generated library in this project in order to make use of its functions. In order to import the library, you can add its path in the ```GOPATH``` for this project. Follow the below steps:

Right click on the project name and click on ```Properties```

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/go?step=testProject0&projectName=apigeeedgeapimanagement_lib)

Choose ```Go Compiler``` from the side menu. Check ```Use project specific settings``` and uncheck ```Use same value as the GOPATH environment variable.```. By default, the GOPATH value from the environment variables will be visible in ```Eclipse GOPATH```. Do not remove this as this points to the unirest dependency.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/go?step=testProject1)

Append the library path to this GOPATH

![Adding dependency to the client library - Step 3](https://apidocs.io/illustration/go?step=testProject2&workspaceFolder=Apigee%20Edge%20API%20Management-GoLang)

Once the path is appended, click on ```OK```

### 3. Build the Test Project

Right click on the project name and click on ```Build Project```

![Build Project](https://apidocs.io/illustration/go?step=buildProject&projectName=apigeeedgeapimanagement_lib)

### 4. Run the Test Project

If the build is successful, right click on your Go file and click on ```Run As``` -> ```Go Application```

![Run Project](https://apidocs.io/illustration/go?step=runProject&projectName=apigeeedgeapimanagement_lib)

## Initialization

### Authentication
In order to setup authentication of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| basicAuthUserName | The username to use with basic authentication |
| basicAuthPassword | The password to use with basic authentication |


To configure these for your generated code, open the file "Configuration.go" and edit it's contents.


# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [deployments_pkg](#deployments_pkg)
* [userroles_pkg](#userroles_pkg)
* [oauth_pkg](#oauth_pkg)
* [kvm_pkg](#kvm_pkg)
* [pods_pkg](#pods_pkg)
* [servers_pkg](#servers_pkg)
* [developers_pkg](#developers_pkg)
* [apis_pkg](#apis_pkg)
* [cache_pkg](#cache_pkg)
* [audit_pkg](#audit_pkg)
* [users_pkg](#users_pkg)
* [zzzothers_pkg](#zzzothers_pkg)
* [apps_pkg](#apps_pkg)
* [virtualhosts_pkg](#virtualhosts_pkg)
* [environments_pkg](#environments_pkg)
* [developerapp_pkg](#developerapp_pkg)
* [keystores_pkg](#keystores_pkg)
* [products_pkg](#products_pkg)
* [targetservers_pkg](#targetservers_pkg)
* [company_pkg](#company_pkg)
* [organizations_pkg](#organizations_pkg)

## <a name="deployments_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".deployments_pkg") deployments_pkg

### Get instance

Factory for the ``` DEPLOYMENTS ``` interface can be accessed from the package deployments_pkg.

```go
deployments := deployments_pkg.NewDEPLOYMENTS()
```

### <a name="list_deployments"></a>![Method: ](https://apidocs.io/img/method.png ".deployments_pkg.ListDeployments") ListDeployments

> List Deployments


```go
func (me *DEPLOYMENTS_IMPL) ListDeployments(
            authorization string,
            oRG string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
oRG := "ORG"

var result 
result,_ = deployments.ListDeployments(authorization, oRG)

```


### <a name="get_deployments"></a>![Method: ](https://apidocs.io/img/method.png ".deployments_pkg.GetDeployments") GetDeployments

> Deployments


```go
func (me *DEPLOYMENTS_IMPL) GetDeployments(
            authorization string,
            oRG string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
oRG := "ORG"

var result 
result,_ = deployments.GetDeployments(authorization, oRG)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="userroles_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".userroles_pkg") userroles_pkg

### Get instance

Factory for the ``` USERROLES ``` interface can be accessed from the package userroles_pkg.

```go
userRoles := userroles_pkg.NewUSERROLES()
```

### <a name="create_user_roles_update"></a>![Method: ](https://apidocs.io/img/method.png ".userroles_pkg.CreateUserRolesUpdate") CreateUserRolesUpdate

> User Roles Update


```go
func (me *USERROLES_IMPL) CreateUserRolesUpdate(
            body *models_pkg.UserRolesUpdateRequest,
            authorization string,
            contentType string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
bodyValue := []byte("{ \"role\" : [ { \"name\" : \"orgadmin\", \"organization\" : \"dev\" }, { \"name\" : \"sysadmin\" } ] }")
var body *models_pkg.UserRolesUpdateRequest
json.Unmarshal(bodyValue,&body)
authorization := "Basic {{BASICAUTH}}"
contentType := "application/json"

var result 
result,_ = userRoles.CreateUserRolesUpdate(body, authorization, contentType)

```


### <a name="delete_an_organization_userrole"></a>![Method: ](https://apidocs.io/img/method.png ".userroles_pkg.DeleteAnOrganizationUserrole") DeleteAnOrganizationUserrole

> Delete an organization userrole


```go
func (me *USERROLES_IMPL) DeleteAnOrganizationUserrole(
            org string,
            authorization string,
            accept string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| org |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
org := "{{ORG}}"
authorization := "Basic {{BASICAUTH}}"
accept := "application/json"

var result 
result,_ = userRoles.DeleteAnOrganizationUserrole(org, authorization, accept)

```


### <a name="get_permissions_for_a_role"></a>![Method: ](https://apidocs.io/img/method.png ".userroles_pkg.GetPermissionsForARole") GetPermissionsForARole

> Get permissions for a role


```go
func (me *USERROLES_IMPL) GetPermissionsForARole(
            authorization string,
            contentType string,
            oRG string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
contentType := "Content-Type"
oRG := "ORG"

var result 
result,_ = userRoles.GetPermissionsForARole(authorization, contentType, oRG)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="oauth_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".oauth_pkg") oauth_pkg

### Get instance

Factory for the ``` OAUTH ``` interface can be accessed from the package oauth_pkg.

```go
oAuth := oauth_pkg.NewOAUTH()
```

### <a name="get_o_auth2_token_details_get"></a>![Method: ](https://apidocs.io/img/method.png ".oauth_pkg.GetOAuth2TokenDetailsGet") GetOAuth2TokenDetailsGet

> OAuth2 Token Details Get


```go
func (me *OAUTH_IMPL) GetOAuth2TokenDetailsGet(
            authorization string,
            contentType string,
            oRG string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
contentType := "Content-Type"
oRG := "ORG"

var result 
result,_ = oAuth.GetOAuth2TokenDetailsGet(authorization, contentType, oRG)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="kvm_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".kvm_pkg") kvm_pkg

### Get instance

Factory for the ``` KVM ``` interface can be accessed from the package kvm_pkg.

```go
kVM := kvm_pkg.NewKVM()
```

### <a name="get_kvm_get"></a>![Method: ](https://apidocs.io/img/method.png ".kvm_pkg.GetKVMGet") GetKVMGet

> KVM Get


```go
func (me *KVM_IMPL) GetKVMGet(
            authorization string,
            contentType string,
            oRG string,
            eNV string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
contentType := "Content-Type"
oRG := "ORG"
eNV := "ENV"

var result 
result,_ = kVM.GetKVMGet(authorization, contentType, oRG, eNV)

```


### <a name="delete_kvm_delete_entire_kvm"></a>![Method: ](https://apidocs.io/img/method.png ".kvm_pkg.DeleteKVMDeleteEntireKVM") DeleteKVMDeleteEntireKVM

> KVM Delete (Entire KVM)


```go
func (me *KVM_IMPL) DeleteKVMDeleteEntireKVM(
            authorization string,
            contentType string,
            oRG string,
            eNV string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
contentType := "Content-Type"
oRG := "ORG"
eNV := "ENV"

var result 
result,_ = kVM.DeleteKVMDeleteEntireKVM(authorization, contentType, oRG, eNV)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="pods_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".pods_pkg") pods_pkg

### Get instance

Factory for the ``` PODS ``` interface can be accessed from the package pods_pkg.

```go
pods := pods_pkg.NewPODS()
```

### <a name="get_analytics_pod"></a>![Method: ](https://apidocs.io/img/method.png ".pods_pkg.GetAnalyticsPod") GetAnalyticsPod

> Analytics pod


```go
func (me *PODS_IMPL) GetAnalyticsPod(
            pod string,
            authorization string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| pod |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
pod := "analytics"
authorization := "Basic {{BASICAUTH}}"

var result 
result,_ = pods.GetAnalyticsPod(pod, authorization)

```


### <a name="get_associated_pods"></a>![Method: ](https://apidocs.io/img/method.png ".pods_pkg.GetAssociatedPods") GetAssociatedPods

> Get Associated  Pods


```go
func (me *PODS_IMPL) GetAssociatedPods(
            contentType string,
            authorization string,
            oRG string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
contentType := "Content-Type"
authorization := "Authorization"
oRG := "ORG"

var result 
result,_ = pods.GetAssociatedPods(contentType, authorization, oRG)

```


### <a name="create_disassociate_org_from_pod"></a>![Method: ](https://apidocs.io/img/method.png ".pods_pkg.CreateDisassociateOrgFromPOD") CreateDisassociateOrgFromPOD

> Disassociate Org from POD


```go
func (me *PODS_IMPL) CreateDisassociateOrgFromPOD(
            contentType string,
            authorization string,
            oRG string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
contentType := "Content-Type"
authorization := "Authorization"
oRG := "ORG"

var result 
result,_ = pods.CreateDisassociateOrgFromPOD(contentType, authorization, oRG)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="servers_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".servers_pkg") servers_pkg

### Get instance

Factory for the ``` SERVERS ``` interface can be accessed from the package servers_pkg.

```go
servers := servers_pkg.NewSERVERS()
```

### <a name="create_deregister"></a>![Method: ](https://apidocs.io/img/method.png ".servers_pkg.CreateDeregister") CreateDeregister

> Deregister


```go
func (me *SERVERS_IMPL) CreateDeregister(
            authorization string,
            contentType string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Basic {{BASICAUTH}}"
contentType := "application/x-www-form-urlencoded"

var result 
result,_ = servers.CreateDeregister(authorization, contentType)

```


### <a name="list_server_by_uuid"></a>![Method: ](https://apidocs.io/img/method.png ".servers_pkg.ListServerByUUID") ListServerByUUID

> List Server by UUID


```go
func (me *SERVERS_IMPL) ListServerByUUID(
            authorization string,
            muuid string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| muuid |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Basic {{BASICAUTH}}"
muuid := "uuid"

var result 
result,_ = servers.ListServerByUUID(authorization, muuid)

```


### <a name="create_set_not_reachable"></a>![Method: ](https://apidocs.io/img/method.png ".servers_pkg.CreateSetNotReachable") CreateSetNotReachable

> Set not reachable


```go
func (me *SERVERS_IMPL) CreateSetNotReachable(
            reachable string,
            authorization string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| reachable |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
reachable := "false"
authorization := "Basic {{BASICAUTH}}"

var result 
result,_ = servers.CreateSetNotReachable(reachable, authorization)

```


### <a name="list_org_env_servers"></a>![Method: ](https://apidocs.io/img/method.png ".servers_pkg.ListOrgEnvServers") ListOrgEnvServers

> List org/env servers


```go
func (me *SERVERS_IMPL) ListOrgEnvServers(
            authorization string,
            oRG string,
            eNV string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
oRG := "ORG"
eNV := "ENV"

var result 
result,_ = servers.ListOrgEnvServers(authorization, oRG, eNV)

```


### <a name="create_register_server_with_org"></a>![Method: ](https://apidocs.io/img/method.png ".servers_pkg.CreateRegisterServerWithOrg") CreateRegisterServerWithOrg

> Register server with org


```go
func (me *SERVERS_IMPL) CreateRegisterServerWithOrg(
            authorization string,
            contentType string,
            oRG string,
            eNV string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
contentType := "Content-Type"
oRG := "ORG"
eNV := "ENV"

var result 
result,_ = servers.CreateRegisterServerWithOrg(authorization, contentType, oRG, eNV)

```


### <a name="create_associate_environments_to_mp"></a>![Method: ](https://apidocs.io/img/method.png ".servers_pkg.CreateAssociateEnvironmentsToMP") CreateAssociateEnvironmentsToMP

> Associate  environments to MP


```go
func (me *SERVERS_IMPL) CreateAssociateEnvironmentsToMP(
            authorization string,
            contentType string,
            oRG string,
            eNV string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
contentType := "Content-Type"
oRG := "ORG"
eNV := "ENV"

var result 
result,_ = servers.CreateAssociateEnvironmentsToMP(authorization, contentType, oRG, eNV)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="developers_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".developers_pkg") developers_pkg

### Get instance

Factory for the ``` DEVELOPERS ``` interface can be accessed from the package developers_pkg.

```go
developers := developers_pkg.NewDEVELOPERS()
```

### <a name="get_developers"></a>![Method: ](https://apidocs.io/img/method.png ".developers_pkg.GetDevelopers") GetDevelopers

> Get Developers


```go
func (me *DEVELOPERS_IMPL) GetDevelopers(
            authorization string,
            contentType string,
            oRG string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
contentType := "Content-Type"
oRG := "ORG"

var result 
result,_ = developers.GetDevelopers(authorization, contentType, oRG)

```


### <a name="create_developer"></a>![Method: ](https://apidocs.io/img/method.png ".developers_pkg.CreateDeveloper") CreateDeveloper

> Create Developer


```go
func (me *DEVELOPERS_IMPL) CreateDeveloper(
            body string,
            authorization string,
            contentType string,
            oRG string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
body := "Body"
authorization := "Authorization"
contentType := "Content-Type"
oRG := "ORG"

var result 
result,_ = developers.CreateDeveloper(body, authorization, contentType, oRG)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="apis_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".apis_pkg") apis_pkg

### Get instance

Factory for the ``` APIS ``` interface can be accessed from the package apis_pkg.

```go
aPIs := apis_pkg.NewAPIS()
```

### <a name="get_api_list"></a>![Method: ](https://apidocs.io/img/method.png ".apis_pkg.GetApiList") GetApiList

> Api list


```go
func (me *APIS_IMPL) GetApiList(
            authorization string,
            oRG string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
oRG := "ORG"

var result 
result,_ = aPIs.GetApiList(authorization, oRG)

```


### <a name="create_deploy_api"></a>![Method: ](https://apidocs.io/img/method.png ".apis_pkg.CreateDeployAPI") CreateDeployAPI

> Deploy API


```go
func (me *APIS_IMPL) CreateDeployAPI(
            action string,
            name string,
            authorization string,
            contentType string,
            oRG string)(,error)
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

```go
action := "action"
name := "name"
authorization := "Authorization"
contentType := "Content-Type"
oRG := "ORG"

var result 
result,_ = aPIs.CreateDeployAPI(action, name, authorization, contentType, oRG)

```


### <a name="delete_an_api"></a>![Method: ](https://apidocs.io/img/method.png ".apis_pkg.DeleteAnAPI") DeleteAnAPI

> Delete an API


```go
func (me *APIS_IMPL) DeleteAnAPI(
            authorization string,
            oRG string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
oRG := "ORG"

var result 
result,_ = aPIs.DeleteAnAPI(authorization, oRG)

```


### <a name="create_undeploy_revisions"></a>![Method: ](https://apidocs.io/img/method.png ".apis_pkg.CreateUndeployRevisions") CreateUndeployRevisions

> Undeploy Revisions


```go
func (me *APIS_IMPL) CreateUndeployRevisions(
            action string,
            env string,
            authorization string,
            contentType string,
            oRG string)(,error)
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

```go
action := "action"
env := "env"
authorization := "Authorization"
contentType := "Content-Type"
oRG := "ORG"

var result 
result,_ = aPIs.CreateUndeployRevisions(action, env, authorization, contentType, oRG)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="cache_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".cache_pkg") cache_pkg

### Get instance

Factory for the ``` CACHE ``` interface can be accessed from the package cache_pkg.

```go
cache := cache_pkg.NewCACHE()
```

### <a name="list_caches"></a>![Method: ](https://apidocs.io/img/method.png ".cache_pkg.ListCaches") ListCaches

> List caches


```go
func (me *CACHE_IMPL) ListCaches(
            authorization string,
            oRG string,
            eNV string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
oRG := "ORG"
eNV := "ENV"

var result 
result,_ = cache.ListCaches(authorization, oRG, eNV)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="audit_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".audit_pkg") audit_pkg

### Get instance

Factory for the ``` AUDIT ``` interface can be accessed from the package audit_pkg.

```go
audit := audit_pkg.NewAUDIT()
```

### <a name="get_audit"></a>![Method: ](https://apidocs.io/img/method.png ".audit_pkg.GetAudit") GetAudit

> Audit


```go
func (me *AUDIT_IMPL) GetAudit(
            expand bool,
            timeline string,
            authorization string,
            oRG string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| expand |  ``` Required ```  | TODO: Add a parameter description |
| timeline |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
expand := false
timeline := "timeline"
authorization := "Authorization"
oRG := "ORG"

var result 
result,_ = audit.GetAudit(expand, timeline, authorization, oRG)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="users_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".users_pkg") users_pkg

### Get instance

Factory for the ``` USERS ``` interface can be accessed from the package users_pkg.

```go
users := users_pkg.NewUSERS()
```

### <a name="get_developer_details_get"></a>![Method: ](https://apidocs.io/img/method.png ".users_pkg.GetDeveloperDetailsGet") GetDeveloperDetailsGet

> Developer Details Get


```go
func (me *USERS_IMPL) GetDeveloperDetailsGet(
            authorization string,
            contentType string,
            oRG string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
contentType := "Content-Type"
oRG := "ORG"

var result 
result,_ = users.GetDeveloperDetailsGet(authorization, contentType, oRG)

```


### <a name="create_user_in_org"></a>![Method: ](https://apidocs.io/img/method.png ".users_pkg.CreateUserInORG") CreateUserInORG

> Create User in ORG


```go
func (me *USERS_IMPL) CreateUserInORG(
            body string,
            authorization string,
            contentType string,
            oRG string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
body := "Body"
authorization := "Authorization"
contentType := "Content-Type"
oRG := "ORG"

var result 
result,_ = users.CreateUserInORG(body, authorization, contentType, oRG)

```


### <a name="list_users"></a>![Method: ](https://apidocs.io/img/method.png ".users_pkg.ListUsers") ListUsers

> List Users


```go
func (me *USERS_IMPL) ListUsers(authorization string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Basic {{BASICAUTH}}"

var result 
result,_ = users.ListUsers(authorization)

```


### <a name="add_user_as_orgadmin"></a>![Method: ](https://apidocs.io/img/method.png ".users_pkg.AddUserAsOrgadmin") AddUserAsOrgadmin

> Add user as Orgadmin


```go
func (me *USERS_IMPL) AddUserAsOrgadmin(
            body string,
            authorization string,
            contentType string,
            oRG string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
body := "Body"
authorization := "Authorization"
contentType := "Content-Type"
oRG := "ORG"

var result 
result,_ = users.AddUserAsOrgadmin(body, authorization, contentType, oRG)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="zzzothers_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".zzzothers_pkg") zzzothers_pkg

### Get instance

Factory for the ``` ZZZOTHERS ``` interface can be accessed from the package zzzothers_pkg.

```go
zzzOthers := zzzothers_pkg.NewZZZOTHERS()
```

### <a name="get_cluster_status"></a>![Method: ](https://apidocs.io/img/method.png ".zzzothers_pkg.GetClusterStatus") GetClusterStatus

> Cluster Status


```go
func (me *ZZZOTHERS_IMPL) GetClusterStatus(authorization string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Basic {{BASICAUTH}}"

var result 
result,_ = zzzOthers.GetClusterStatus(authorization)

```


### <a name="create_enable_debug_wo_restart"></a>![Method: ](https://apidocs.io/img/method.png ".zzzothers_pkg.CreateEnableDebugWORestart") CreateEnableDebugWORestart

> Enable Debug w/o Restart 


```go
func (me *ZZZOTHERS_IMPL) CreateEnableDebugWORestart(
            session string,
            authorization string,
            contentType string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| session |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
session := "logsession_name"
authorization := "Basic {{BASICAUTH}}"
contentType := "application/x-www-form-urlencoded"

var result 
result,_ = zzzOthers.CreateEnableDebugWORestart(session, authorization, contentType)

```


### <a name="get_classifications"></a>![Method: ](https://apidocs.io/img/method.png ".zzzothers_pkg.GetClassifications") GetClassifications

> Classifications


```go
func (me *ZZZOTHERS_IMPL) GetClassifications(
            authorization string,
            hOST string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
hOST := "HOST"

var result 
result,_ = zzzOthers.GetClassifications(authorization, hOST)

```


### <a name="create_company_developer"></a>![Method: ](https://apidocs.io/img/method.png ".zzzothers_pkg.CreateCompanyDeveloper") CreateCompanyDeveloper

> Create Company Developer


```go
func (me *ZZZOTHERS_IMPL) CreateCompanyDeveloper(
            body *models_pkg.CreateCompanyDeveloperRequest,
            contentType string,
            authorization string,
            oRG string,
            cOMPANY string)(,error)
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

```go
var body *models_pkg.CreateCompanyDeveloperRequest
contentType := "Content-Type"
authorization := "Authorization"
oRG := "ORG"
cOMPANY := "COMPANY"

var result 
result,_ = zzzOthers.CreateCompanyDeveloper(body, contentType, authorization, oRG, cOMPANY)

```


### <a name="get_qpid_metrics"></a>![Method: ](https://apidocs.io/img/method.png ".zzzothers_pkg.GetQPIDMetrics") GetQPIDMetrics

> QPID Metrics


```go
func (me *ZZZOTHERS_IMPL) GetQPIDMetrics(
            authorization string,
            hOST string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
hOST := "HOST"

var result 
result,_ = zzzOthers.GetQPIDMetrics(authorization, hOST)

```


### <a name="get_build_info"></a>![Method: ](https://apidocs.io/img/method.png ".zzzothers_pkg.GetBuildInfo") GetBuildInfo

> Build Info


```go
func (me *ZZZOTHERS_IMPL) GetBuildInfo(
            authorization string,
            hOST string,
            pORT string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| hOST |  ``` Required ```  | TODO: Add a parameter description |
| pORT |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
hOST := "HOST"
pORT := "PORT"

var result 
result,_ = zzzOthers.GetBuildInfo(authorization, hOST, pORT)

```


### <a name="delete_disable_debug_wo_restart"></a>![Method: ](https://apidocs.io/img/method.png ".zzzothers_pkg.DeleteDisableDebugWORestart") DeleteDisableDebugWORestart

> Disable Debug w/o Restart


```go
func (me *ZZZOTHERS_IMPL) DeleteDisableDebugWORestart(
            authorization string,
            contentType string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Basic {{BASICAUTH}}"
contentType := "application/x-www-form-urlencoded"

var result 
result,_ = zzzOthers.DeleteDisableDebugWORestart(authorization, contentType)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="apps_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".apps_pkg") apps_pkg

### Get instance

Factory for the ``` APPS ``` interface can be accessed from the package apps_pkg.

```go
apps := apps_pkg.NewAPPS()
```

### <a name="create_company_app"></a>![Method: ](https://apidocs.io/img/method.png ".apps_pkg.CreateCompanyAPP") CreateCompanyAPP

> Create Company APP


```go
func (me *APPS_IMPL) CreateCompanyAPP(
            body string,
            authorization string,
            contentType string,
            oRG string,
            cOMPANY string)(,error)
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

```go
body := "Body"
authorization := "Authorization"
contentType := "Content-Type"
oRG := "ORG"
cOMPANY := "COMPANY"

var result 
result,_ = apps.CreateCompanyAPP(body, authorization, contentType, oRG, cOMPANY)

```


### <a name="add_app_credentials"></a>![Method: ](https://apidocs.io/img/method.png ".apps_pkg.AddAppCredentials") AddAppCredentials

> Add app credentials


```go
func (me *APPS_IMPL) AddAppCredentials(
            body string,
            authorization string,
            contentType string,
            oRG string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
body := "Body"
authorization := "Authorization"
contentType := "Content-Type"
oRG := "ORG"

var result 
result,_ = apps.AddAppCredentials(body, authorization, contentType, oRG)

```


### <a name="list_apps"></a>![Method: ](https://apidocs.io/img/method.png ".apps_pkg.ListApps") ListApps

> List apps 


```go
func (me *APPS_IMPL) ListApps(
            authorization string,
            oRG string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
oRG := "ORG"

var result 
result,_ = apps.ListApps(authorization, oRG)

```


### <a name="list_app"></a>![Method: ](https://apidocs.io/img/method.png ".apps_pkg.ListApp") ListApp

> List app


```go
func (me *APPS_IMPL) ListApp(
            authorization string,
            oRG string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
oRG := "ORG"

var result 
result,_ = apps.ListApp(authorization, oRG)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="virtualhosts_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".virtualhosts_pkg") virtualhosts_pkg

### Get instance

Factory for the ``` VIRTUALHOSTS ``` interface can be accessed from the package virtualhosts_pkg.

```go
virtualHosts := virtualhosts_pkg.NewVIRTUALHOSTS()
```

### <a name="list_virtual_hosts"></a>![Method: ](https://apidocs.io/img/method.png ".virtualhosts_pkg.ListVirtualHosts") ListVirtualHosts

> List VirtualHosts


```go
func (me *VIRTUALHOSTS_IMPL) ListVirtualHosts(
            authorization string,
            oRG string,
            eNV string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
oRG := "ORG"
eNV := "ENV"

var result 
result,_ = virtualHosts.ListVirtualHosts(authorization, oRG, eNV)

```


### <a name="add_virtual_host"></a>![Method: ](https://apidocs.io/img/method.png ".virtualhosts_pkg.AddVirtualHost") AddVirtualHost

> Add Virtual Host


```go
func (me *VIRTUALHOSTS_IMPL) AddVirtualHost(
            body string,
            authorization string,
            contentType string,
            oRG string,
            eNV string)(,error)
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

```go
body := "Body"
authorization := "Authorization"
contentType := "Content-Type"
oRG := "ORG"
eNV := "ENV"

var result 
result,_ = virtualHosts.AddVirtualHost(body, authorization, contentType, oRG, eNV)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="environments_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".environments_pkg") environments_pkg

### Get instance

Factory for the ``` ENVIRONMENTS ``` interface can be accessed from the package environments_pkg.

```go
environments := environments_pkg.NewENVIRONMENTS()
```

### <a name="update_environments"></a>![Method: ](https://apidocs.io/img/method.png ".environments_pkg.UpdateEnvironments") UpdateEnvironments

> Update Environments


```go
func (me *ENVIRONMENTS_IMPL) UpdateEnvironments(
            authorization string,
            contentType string,
            oRG string,
            eNV string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
contentType := "Content-Type"
oRG := "ORG"
eNV := "ENV"

var result 
result,_ = environments.UpdateEnvironments(authorization, contentType, oRG, eNV)

```


### <a name="delete_environment"></a>![Method: ](https://apidocs.io/img/method.png ".environments_pkg.DeleteEnvironment") DeleteEnvironment

> Delete Environment


```go
func (me *ENVIRONMENTS_IMPL) DeleteEnvironment(
            authorization string,
            oRG string,
            eNV string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
oRG := "ORG"
eNV := "ENV"

var result 
result,_ = environments.DeleteEnvironment(authorization, oRG, eNV)

```


### <a name="create_new_env_in_org"></a>![Method: ](https://apidocs.io/img/method.png ".environments_pkg.CreateNewENVInORG") CreateNewENVInORG

> Create New ENV in ORG


```go
func (me *ENVIRONMENTS_IMPL) CreateNewENVInORG(
            body string,
            authorization string,
            contentType string,
            oRG string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
body := "Body"
authorization := "Authorization"
contentType := "Content-Type"
oRG := "ORG"

var result 
result,_ = environments.CreateNewENVInORG(body, authorization, contentType, oRG)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="developerapp_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".developerapp_pkg") developerapp_pkg

### Get instance

Factory for the ``` DEVELOPERAPP ``` interface can be accessed from the package developerapp_pkg.

```go
developerApp := developerapp_pkg.NewDEVELOPERAPP()
```

### <a name="get_developer_app_details_get"></a>![Method: ](https://apidocs.io/img/method.png ".developerapp_pkg.GetDeveloperAppDetailsGet") GetDeveloperAppDetailsGet

> Developer App Details Get


```go
func (me *DEVELOPERAPP_IMPL) GetDeveloperAppDetailsGet(
            authorization string,
            contentType string,
            oRG string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
contentType := "Content-Type"
oRG := "ORG"

var result 
result,_ = developerApp.GetDeveloperAppDetailsGet(authorization, contentType, oRG)

```


### <a name="delete_app_credentials"></a>![Method: ](https://apidocs.io/img/method.png ".developerapp_pkg.DeleteAppCredentials") DeleteAppCredentials

> Delete app credentials


```go
func (me *DEVELOPERAPP_IMPL) DeleteAppCredentials(
            authorization string,
            accept string,
            oRG string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| accept |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
accept := "Accept"
oRG := "ORG"

var result 
result,_ = developerApp.DeleteAppCredentials(authorization, accept, oRG)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="keystores_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".keystores_pkg") keystores_pkg

### Get instance

Factory for the ``` KEYSTORES ``` interface can be accessed from the package keystores_pkg.

```go
keystores := keystores_pkg.NewKEYSTORES()
```

### <a name="list_keystores"></a>![Method: ](https://apidocs.io/img/method.png ".keystores_pkg.ListKeystores") ListKeystores

> List Keystores


```go
func (me *KEYSTORES_IMPL) ListKeystores(
            authorization string,
            oRG string,
            eNV string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
oRG := "ORG"
eNV := "ENV"

var result 
result,_ = keystores.ListKeystores(authorization, oRG, eNV)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="products_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".products_pkg") products_pkg

### Get instance

Factory for the ``` PRODUCTS ``` interface can be accessed from the package products_pkg.

```go
products := products_pkg.NewPRODUCTS()
```

### <a name="get_api_products"></a>![Method: ](https://apidocs.io/img/method.png ".products_pkg.GetApiProducts") GetApiProducts

> Api Products


```go
func (me *PRODUCTS_IMPL) GetApiProducts(
            authorization string,
            oRG string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
oRG := "ORG"

var result 
result,_ = products.GetApiProducts(authorization, oRG)

```


### <a name="create_ap_iproduct_creation"></a>![Method: ](https://apidocs.io/img/method.png ".products_pkg.CreateAPIproductCreation") CreateAPIproductCreation

> APIproduct Creation


```go
func (me *PRODUCTS_IMPL) CreateAPIproductCreation(
            body string,
            authorization string,
            contentType string,
            oRG string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
body := "Body"
authorization := "Authorization"
contentType := "Content-Type"
oRG := "ORG"

var result 
result,_ = products.CreateAPIproductCreation(body, authorization, contentType, oRG)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="targetservers_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".targetservers_pkg") targetservers_pkg

### Get instance

Factory for the ``` TARGETSERVERS ``` interface can be accessed from the package targetservers_pkg.

```go
targetServers := targetservers_pkg.NewTARGETSERVERS()
```

### <a name="list_target_servers"></a>![Method: ](https://apidocs.io/img/method.png ".targetservers_pkg.ListTargetServers") ListTargetServers

> List Target Servers


```go
func (me *TARGETSERVERS_IMPL) ListTargetServers(
            authorization string,
            oRG string,
            eNV string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |
| eNV |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Authorization"
oRG := "ORG"
eNV := "ENV"

var result 
result,_ = targetServers.ListTargetServers(authorization, oRG, eNV)

```


### <a name="add_target"></a>![Method: ](https://apidocs.io/img/method.png ".targetservers_pkg.AddTarget") AddTarget

> Add Target


```go
func (me *TARGETSERVERS_IMPL) AddTarget(
            body *models_pkg.AddTargetRequest,
            contentType string,
            authorization string,
            oRG string,
            eNV string)(,error)
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

```go
var body *models_pkg.AddTargetRequest
contentType := "content-type"
authorization := "Authorization"
oRG := "ORG"
eNV := "ENV"

var result 
result,_ = targetServers.AddTarget(body, contentType, authorization, oRG, eNV)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="company_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".company_pkg") company_pkg

### Get instance

Factory for the ``` COMPANY ``` interface can be accessed from the package company_pkg.

```go
company := company_pkg.NewCOMPANY()
```

### <a name="create_company"></a>![Method: ](https://apidocs.io/img/method.png ".company_pkg.CreateCompany") CreateCompany

> Create Company


```go
func (me *COMPANY_IMPL) CreateCompany(
            body string,
            authorization string,
            contentType string,
            oRG string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| authorization |  ``` Required ```  | TODO: Add a parameter description |
| contentType |  ``` Required ```  | TODO: Add a parameter description |
| oRG |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
body := "Body"
authorization := "Authorization"
contentType := "Content-Type"
oRG := "ORG"

var result 
result,_ = company.CreateCompany(body, authorization, contentType, oRG)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="organizations_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".organizations_pkg") organizations_pkg

### Get instance

Factory for the ``` ORGANIZATIONS ``` interface can be accessed from the package organizations_pkg.

```go
organizations := organizations_pkg.NewORGANIZATIONS()
```

### <a name="list_organizations"></a>![Method: ](https://apidocs.io/img/method.png ".organizations_pkg.ListOrganizations") ListOrganizations

> List organizations


```go
func (me *ORGANIZATIONS_IMPL) ListOrganizations(authorization string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| authorization |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
authorization := "Basic {{BASICAUTH}}"

var result 
result,_ = organizations.ListOrganizations(authorization)

```


[Back to List of Controllers](#list_of_controllers)




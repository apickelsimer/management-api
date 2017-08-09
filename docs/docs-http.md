# 

TODO: Add Description



## Base URL

The Base URL for this API is `http://example.com/`



## Authentication
The type of authentication used by this API is: `Basic Authentication`



# <a name="api_reference"></a>API Reference

* [Deployments](#deployments)
* [User Roles](#user_roles)
* [OAuth](#o_auth)
* [KVM](#kvm)
* [Pods](#pods)
* [Servers](#servers)
* [Developers](#developers)
* [APIs](#ap_is)
* [Cache](#cache)
* [Audit](#audit)
* [Users](#users)
* [zzzOthers](#zzz_others)
* [Apps](#apps)
* [VirtualHosts](#virtual_hosts)
* [Environments](#environments)
* [Developer App](#developer_app)
* [Keystores](#keystores)
* [Products](#products)
* [TargetServers](#target_servers)
* [Company](#company)
* [Organizations](#organizations)

## <a name="deployments"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Deployments") Deployments


### <a name="list_deployments"></a>![Endpoint: ](https://apidocs.io/img/method.png "List Deployments") List Deployments


**`GET`** `/v1/organizations/{ORG}/deployments`

> List Deployments



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Request Headers
>Authorization="Authorization";

#### Responses
**200**


### <a name="deployments"></a>![Endpoint: ](https://apidocs.io/img/method.png "Deployments") Deployments


**`GET`** `/v1/o/{ORG}/apis/_api_/revisions/_revision_/deployments`

> Deployments



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Request Headers
>Authorization="Authorization";

#### Responses
**200**


[Back to API Reference](#api_reference)

## <a name="user_roles"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "User Roles") User Roles


### <a name="user_roles_update"></a>![Endpoint: ](https://apidocs.io/img/method.png "User Roles Update") User Roles Update


**`POST`** `/v1/users/_email_/userroles`

> User Roles Update



#### Request Headers
>Accept=application/json;
>Content-Type=application/json;
>Authorization=Basic {{BASICAUTH}};

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| `user roles updaterequest` |  ``` Required ```  | TODO: Add a parameter description | 

 Example 
``` 
{
  "role": [
    {
      "name": "orgadmin",
      "organization": "dev"
    },
    {
      "name": "sysadmin"
    }
  ]
}
``` 

#### Responses
**200**


### <a name="delete_an_organization_userrole"></a>![Endpoint: ](https://apidocs.io/img/method.png "Delete an organization userrole") Delete an organization userrole


**`DELETE`** `/v1/users/_devemail_/userroles/user`

> Delete an organization userrole



#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| org | `string` |  ``` Required ```  | TODO: Add a parameter description | `{{ORG}}` | 

#### Request Headers
>Authorization=Basic {{BASICAUTH}};
>Accept=application/json;

#### Responses
**200**


### <a name="get_permissions_for_a_role"></a>![Endpoint: ](https://apidocs.io/img/method.png "Get permissions for a role") Get permissions for a role


**`GET`** `/v1/o/{ORG}/userroles/user/permissions`

> Get permissions for a role



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Request Headers
>Authorization="Authorization";
>Content-Type="Content-Type";

#### Responses
**200**


[Back to API Reference](#api_reference)

## <a name="o_auth"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "OAuth") OAuth


### <a name="o_auth2_token_details_get"></a>![Endpoint: ](https://apidocs.io/img/method.png "OAuth2 Token Details Get") OAuth2 Token Details Get


**`GET`** `/v1/o/{ORG}/oauth2/accesstokens/_tokenid_`

> OAuth2 Token Details Get



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Request Headers
>Authorization="Authorization";
>Content-Type="Content-Type";

#### Responses
**200**


[Back to API Reference](#api_reference)

## <a name="kvm"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "KVM") KVM


### <a name="kvm_get"></a>![Endpoint: ](https://apidocs.io/img/method.png "KVM Get") KVM Get


**`GET`** `/v1/o/{ORG}/e/{ENV}/keyvaluemaps/_kvm_`

> KVM Get



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 
| ENV | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ENV"` | 

#### Request Headers
>Authorization="Authorization";
>Content-Type="Content-Type";

#### Responses
**200**


### <a name="kvm_delete_(entire_kvm)"></a>![Endpoint: ](https://apidocs.io/img/method.png "KVM Delete (Entire KVM)") KVM Delete (Entire KVM)


**`DELETE`** `/v1/o/{ORG}/e/{ENV}/keyvaluemaps/_kvm_`

> KVM Delete (Entire KVM)



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 
| ENV | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ENV"` | 

#### Request Headers
>Authorization="Authorization";
>Content-Type="Content-Type";

#### Responses
**200**


[Back to API Reference](#api_reference)

## <a name="pods"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Pods") Pods


### <a name="analytics_pod"></a>![Endpoint: ](https://apidocs.io/img/method.png "Analytics pod") Analytics pod


**`GET`** `/v1/servers`

> Analytics pod



#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| pod | `string` |  ``` Required ```  | TODO: Add a parameter description | `analytics` | 

#### Request Headers
>Authorization=Basic {{BASICAUTH}};

#### Responses
**200**


### <a name="get_associated__pods"></a>![Endpoint: ](https://apidocs.io/img/method.png "Get Associated  Pods") Get Associated  Pods


**`GET`** `/v1/organizations/{ORG}/pods`

> Get Associated  Pods



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Request Headers
>Content-Type="Content-Type";
>Authorization="Authorization";

#### Responses
**200**


### <a name="disassociate_org_from_pod"></a>![Endpoint: ](https://apidocs.io/img/method.png "Disassociate Org from POD") Disassociate Org from POD


**`POST`** `/v1/organizations/{ORG}/pods`

> Disassociate Org from POD



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Request Headers
>Content-Type="Content-Type";
>Authorization="Authorization";

#### Responses
**200**


[Back to API Reference](#api_reference)

## <a name="servers"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Servers") Servers


### <a name="deregister"></a>![Endpoint: ](https://apidocs.io/img/method.png "Deregister") Deregister


**`POST`** `/v1/servers`

> Deregister



#### Request Headers
>Authorization=Basic {{BASICAUTH}};
>Content-Type=application/x-www-form-urlencoded;

#### Responses
**200**


### <a name="list_server_by_uuid"></a>![Endpoint: ](https://apidocs.io/img/method.png "List Server by UUID") List Server by UUID


**`GET`** `/v1/servers/{uuid}`

> List Server by UUID



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| uuid | `string` |  ``` Required ```  | TODO: Add a parameter description | `"uuid"` | 

#### Request Headers
>Authorization=Basic {{BASICAUTH}};

#### Responses
**200**


### <a name="set_not_reachable"></a>![Endpoint: ](https://apidocs.io/img/method.png "Set not reachable") Set not reachable


**`POST`** `/v1/servers/35553ca7-9b49-4b1e-94d0-bda583836c6d`

> Set not reachable



#### Request Headers
>Content-Type=application/x-www-form-urlencoded;
>Authorization=Basic {{BASICAUTH}};

#### Request Body
Url Encoded

| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| reachable | `string` |  ``` Required ```  | TODO: Add a parameter description | `false` | 

#### Responses
**200**


### <a name="list_org/env_servers"></a>![Endpoint: ](https://apidocs.io/img/method.png "List org/env servers") List org/env servers


**`GET`** `/v1/o/{ORG}/e/{ENV}/servers`

> List org/env servers



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 
| ENV | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ENV"` | 

#### Request Headers
>Authorization="Authorization";

#### Responses
**200**


### <a name="register_server_with_org"></a>![Endpoint: ](https://apidocs.io/img/method.png "Register server with org") Register server with org


**`POST`** `/v1/o/{ORG}/e/{ENV}/servers`

> Register server with org



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 
| ENV | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ENV"` | 

#### Request Headers
>Authorization="Authorization";
>Content-Type="Content-Type";

#### Responses
**200**


### <a name="associate__environments_to_mp"></a>![Endpoint: ](https://apidocs.io/img/method.png "Associate  environments to MP") Associate  environments to MP


**`POST`** `/v1/organizations/{ORG}/environments/{ENV}/servers`

> Associate  environments to MP



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 
| ENV | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ENV"` | 

#### Request Headers
>Authorization="Authorization";
>Content-Type="Content-Type";

#### Responses
**200**


[Back to API Reference](#api_reference)

## <a name="developers"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Developers") Developers


### <a name="get_developers"></a>![Endpoint: ](https://apidocs.io/img/method.png "Get Developers") Get Developers


**`GET`** `/v1/organizations/{ORG}/developers`

> Get Developers



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Request Headers
>Authorization="Authorization";
>Content-Type="Content-Type";

#### Responses
**200**


### <a name="create_developer"></a>![Endpoint: ](https://apidocs.io/img/method.png "Create Developer") Create Developer


**`POST`** `/v1/organizations/{ORG}/developers`

> Create Developer



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Request Headers
>Authorization="Authorization";
>Content-Type="Content-Type";

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| `string` |  ``` Required ```  | TODO: Add a parameter description | 

 Example 
``` 
"Body"
``` 

#### Responses
**200**


[Back to API Reference](#api_reference)

## <a name="ap_is"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "APIs") APIs


### <a name="api_list"></a>![Endpoint: ](https://apidocs.io/img/method.png "Api list") Api list


**`GET`** `/v1/o/{ORG}/apis`

> Api list



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Request Headers
>Authorization="Authorization";

#### Responses
**200**


### <a name="deploy_api"></a>![Endpoint: ](https://apidocs.io/img/method.png "Deploy API") Deploy API


**`POST`** `/v1/o/{ORG}/apis`

> Deploy API



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| action | `string` |  ``` Required ```  | TODO: Add a parameter description | `"action"` | 
| name | `string` |  ``` Required ```  | TODO: Add a parameter description | `"name"` | 

#### Request Headers
>Authorization="Authorization";
>Content-Type="Content-Type";

#### Responses
**200**


### <a name="delete_an_api"></a>![Endpoint: ](https://apidocs.io/img/method.png "Delete an API") Delete an API


**`DELETE`** `/v1/o/{ORG}/apis/testing`

> Delete an API



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Request Headers
>Authorization="Authorization";

#### Responses
**200**


### <a name="undeploy_revisions"></a>![Endpoint: ](https://apidocs.io/img/method.png "Undeploy Revisions") Undeploy Revisions


**`POST`** `/v1/o/{ORG}/apis/_API_/revisions/_revision_/deployments`

> Undeploy Revisions



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| action | `string` |  ``` Required ```  | TODO: Add a parameter description | `"action"` | 
| env | `string` |  ``` Required ```  | TODO: Add a parameter description | `"env"` | 

#### Request Headers
>Authorization="Authorization";
>Content-Type="Content-Type";

#### Responses
**200**


[Back to API Reference](#api_reference)

## <a name="cache"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Cache") Cache


### <a name="list_caches"></a>![Endpoint: ](https://apidocs.io/img/method.png "List caches") List caches


**`GET`** `/v1/o/{ORG}/e/{ENV}/caches`

> List caches



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 
| ENV | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ENV"` | 

#### Request Headers
>Authorization="Authorization";

#### Responses
**200**


[Back to API Reference](#api_reference)

## <a name="audit"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Audit") Audit


### <a name="audit"></a>![Endpoint: ](https://apidocs.io/img/method.png "Audit") Audit


**`GET`** `/v1/audits/o/{ORG}/companies`

> Audit



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| expand | `boolean` |  ``` Required ```  | TODO: Add a parameter description | `true` | 
| timeline | `string` |  ``` Required ```  | TODO: Add a parameter description | `"timeline"` | 

#### Request Headers
>Authorization="Authorization";

#### Responses
**200**


[Back to API Reference](#api_reference)

## <a name="users"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Users") Users


### <a name="developer_details_get"></a>![Endpoint: ](https://apidocs.io/img/method.png "Developer Details Get") Developer Details Get


**`GET`** `/v1/o/{ORG}/developers/_devemail_`

> Developer Details Get



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Request Headers
>Authorization="Authorization";
>Content-Type="Content-Type";

#### Responses
**200**


### <a name="create_user_in_org"></a>![Endpoint: ](https://apidocs.io/img/method.png "Create User in ORG") Create User in ORG


**`POST`** `/v1/organizations/{ORG}/users`

> Create User in ORG



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Request Headers
>Authorization="Authorization";
>Content-Type="Content-Type";

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| `string` |  ``` Required ```  | TODO: Add a parameter description | 

 Example 
``` 
"Body"
``` 

#### Responses
**200**


### <a name="list_users"></a>![Endpoint: ](https://apidocs.io/img/method.png "List Users") List Users


**`GET`** `/v1/users`

> List Users



#### Request Headers
>Authorization=Basic {{BASICAUTH}};

#### Responses
**200**


### <a name="add_user_as_orgadmin"></a>![Endpoint: ](https://apidocs.io/img/method.png "Add user as Orgadmin") Add user as Orgadmin


**`POST`** `/v1/organizations/{ORG}/users/shezze@ab.com/userroles/`

> Add user as Orgadmin



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Request Headers
>Authorization="Authorization";
>Content-Type="Content-Type";

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| `string` |  ``` Required ```  | TODO: Add a parameter description | 

 Example 
``` 
"Body"
``` 

#### Responses
**200**


[Back to API Reference](#api_reference)

## <a name="zzz_others"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "zzzOthers") zzzOthers


### <a name="cluster_status"></a>![Endpoint: ](https://apidocs.io/img/method.png "Cluster Status") Cluster Status


**`GET`** `/v1/cluster`

> Cluster Status



#### Request Headers
>Authorization=Basic {{BASICAUTH}};

#### Responses
**200**


### <a name="enable_debug_w/o_restart_"></a>![Endpoint: ](https://apidocs.io/img/method.png "Enable Debug w/o Restart ") Enable Debug w/o Restart 


**`POST`** `/v1/logsessions`

> Enable Debug w/o Restart 



#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| session | `string` |  ``` Required ```  | TODO: Add a parameter description | `logsession_name` | 

#### Request Headers
>Authorization=Basic {{BASICAUTH}};
>Content-Type=application/x-www-form-urlencoded;

#### Responses
**200**


### <a name="classifications"></a>![Endpoint: ](https://apidocs.io/img/method.png "Classifications") Classifications


**`GET`** `/://{HOST}:8081/v1/classification/tree`

> Classifications



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| HOST | `string` |  ``` Required ```  | TODO: Add a parameter description | `"HOST"` | 

#### Request Headers
>Authorization="Authorization";

#### Responses
**200**


### <a name="create_company_developer"></a>![Endpoint: ](https://apidocs.io/img/method.png "Create Company Developer") Create Company Developer


**`POST`** `/v1/organizations/{ORG}/companies/{COMPANY}/developers`

> Create Company Developer



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 
| COMPANY | `string` |  ``` Required ```  | TODO: Add a parameter description | `"COMPANY"` | 

#### Request Headers
>Accept=application/json;
>Content-Type=application/json;
>Authorization="Authorization";

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| `create company developerrequest` |  ``` Required ```  | TODO: Add a parameter description | 

 Example 
``` 
{
  "developer": [
    {
      "email": "email",
      "role": "role"
    }
  ]
}
``` 

#### Responses
**200**


### <a name="qpid_metrics"></a>![Endpoint: ](https://apidocs.io/img/method.png "QPID Metrics") QPID Metrics


**`GET`** `/://{HOST}:8080/v1/runtime/metrics/QPID-CLIENT`

> QPID Metrics



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| HOST | `string` |  ``` Required ```  | TODO: Add a parameter description | `"HOST"` | 

#### Request Headers
>Authorization="Authorization";

#### Responses
**200**


### <a name="build_info"></a>![Endpoint: ](https://apidocs.io/img/method.png "Build Info") Build Info


**`GET`** `/://{HOST}:{PORT}/v1/buildinfo`

> Build Info



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| HOST | `string` |  ``` Required ```  | TODO: Add a parameter description | `"HOST"` | 
| PORT | `string` |  ``` Required ```  | TODO: Add a parameter description | `"PORT"` | 

#### Request Headers
>Authorization="Authorization";

#### Responses
**200**


### <a name="disable_debug_w/o_restart"></a>![Endpoint: ](https://apidocs.io/img/method.png "Disable Debug w/o Restart") Disable Debug w/o Restart


**`DELETE`** `/v1/logsessions/logsession_name`

> Disable Debug w/o Restart



#### Request Headers
>Authorization=Basic {{BASICAUTH}};
>Content-Type=application/x-www-form-urlencoded;

#### Responses
**200**


[Back to API Reference](#api_reference)

## <a name="apps"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Apps") Apps


### <a name="create_company_app"></a>![Endpoint: ](https://apidocs.io/img/method.png "Create Company APP") Create Company APP


**`POST`** `/v1/organizations/{ORG}/companies/{COMPANY}/apps`

> Create Company APP



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 
| COMPANY | `string` |  ``` Required ```  | TODO: Add a parameter description | `"COMPANY"` | 

#### Request Headers
>Authorization="Authorization";
>Content-Type="Content-Type";

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| `string` |  ``` Required ```  | TODO: Add a parameter description | 

 Example 
``` 
"Body"
``` 

#### Responses
**200**


### <a name="add_app_credentials"></a>![Endpoint: ](https://apidocs.io/img/method.png "Add app credentials") Add app credentials


**`POST`** `/v1/organizations/{ORG}/developers/_devemail_/apps/_appname_/keys/create`

> Add app credentials



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Request Headers
>Authorization="Authorization";
>Content-Type="Content-Type";

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| `string` |  ``` Required ```  | TODO: Add a parameter description | 

 Example 
``` 
"Body"
``` 

#### Responses
**200**


### <a name="list_apps_"></a>![Endpoint: ](https://apidocs.io/img/method.png "List apps ") List apps 


**`GET`** `/v1/o/{ORG}/apps`

> List apps 



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Request Headers
>Authorization="Authorization";

#### Responses
**200**


### <a name="list_app"></a>![Endpoint: ](https://apidocs.io/img/method.png "List app") List app


**`GET`** `/v1/o/{ORG}/apps/_appid_`

> List app



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Request Headers
>Authorization="Authorization";

#### Responses
**200**


[Back to API Reference](#api_reference)

## <a name="virtual_hosts"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "VirtualHosts") VirtualHosts


### <a name="list_virtual_hosts"></a>![Endpoint: ](https://apidocs.io/img/method.png "List VirtualHosts") List VirtualHosts


**`GET`** `/v1/organizations/{ORG}/environments/{ENV}/virtualhosts`

> List VirtualHosts



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 
| ENV | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ENV"` | 

#### Request Headers
>Authorization="Authorization";

#### Responses
**200**


### <a name="add_virtual_host"></a>![Endpoint: ](https://apidocs.io/img/method.png "Add Virtual Host") Add Virtual Host


**`POST`** `/v1/organizations/{ORG}/environments/{ENV}/virtualhosts`

> Add Virtual Host



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 
| ENV | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ENV"` | 

#### Request Headers
>Authorization="Authorization";
>Content-Type="Content-Type";

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| `string` |  ``` Required ```  | TODO: Add a parameter description | 

 Example 
``` 
"Body"
``` 

#### Responses
**200**


[Back to API Reference](#api_reference)

## <a name="environments"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Environments") Environments


### <a name="update_environments"></a>![Endpoint: ](https://apidocs.io/img/method.png "Update Environments") Update Environments


**`POST`** `/v1/organizations/{ORG}/environments/{ENV}`

> Update Environments



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 
| ENV | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ENV"` | 

#### Request Headers
>Authorization="Authorization";
>Content-Type="Content-Type";

#### Responses
**200**


### <a name="delete_environment"></a>![Endpoint: ](https://apidocs.io/img/method.png "Delete Environment") Delete Environment


**`DELETE`** `/v1/organizations/{ORG}/environments/{ENV}`

> Delete Environment



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 
| ENV | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ENV"` | 

#### Request Headers
>Authorization="Authorization";

#### Responses
**200**


### <a name="create_new_env_in_org"></a>![Endpoint: ](https://apidocs.io/img/method.png "Create New ENV in ORG") Create New ENV in ORG


**`POST`** `/v1/organizations/{ORG}/environments`

> Create New ENV in ORG



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Request Headers
>Authorization="Authorization";
>Content-Type="Content-Type";

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| `string` |  ``` Required ```  | TODO: Add a parameter description | 

 Example 
``` 
"Body"
``` 

#### Responses
**200**


[Back to API Reference](#api_reference)

## <a name="developer_app"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Developer App") Developer App


### <a name="developer_app_details_get"></a>![Endpoint: ](https://apidocs.io/img/method.png "Developer App Details Get") Developer App Details Get


**`GET`** `/v1/o/{ORG}/developers/_devemail_/apps/_app_`

> Developer App Details Get



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Request Headers
>Authorization="Authorization";
>Content-Type="Content-Type";

#### Responses
**200**


### <a name="delete_app_credentials"></a>![Endpoint: ](https://apidocs.io/img/method.png "Delete app credentials") Delete app credentials


**`DELETE`** `/v1/organizations/{ORG}/developers/_devemail_/apps/_appname_/keys/_key_`

> Delete app credentials



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Request Headers
>Authorization="Authorization";
>Accept="Accept";

#### Responses
**200**


[Back to API Reference](#api_reference)

## <a name="keystores"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Keystores") Keystores


### <a name="list_keystores"></a>![Endpoint: ](https://apidocs.io/img/method.png "List Keystores") List Keystores


**`GET`** `/v1/o/{ORG}/e/{ENV}/keystores`

> List Keystores



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 
| ENV | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ENV"` | 

#### Request Headers
>Authorization="Authorization";

#### Responses
**200**


[Back to API Reference](#api_reference)

## <a name="products"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Products") Products


### <a name="api_products"></a>![Endpoint: ](https://apidocs.io/img/method.png "Api Products") Api Products


**`GET`** `/v1/o/{ORG}/apiproducts`

> Api Products



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Request Headers
>Authorization="Authorization";

#### Responses
**200**


### <a name="ap_iproduct_creation"></a>![Endpoint: ](https://apidocs.io/img/method.png "APIproduct Creation") APIproduct Creation


**`POST`** `/v1/organizations/{ORG}/apiproducts`

> APIproduct Creation



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Request Headers
>Authorization="Authorization";
>Content-Type="Content-Type";

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| `string` |  ``` Required ```  | TODO: Add a parameter description | 

 Example 
``` 
"Body"
``` 

#### Responses
**200**


[Back to API Reference](#api_reference)

## <a name="target_servers"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "TargetServers") TargetServers


### <a name="list_target_servers"></a>![Endpoint: ](https://apidocs.io/img/method.png "List Target Servers") List Target Servers


**`GET`** `/v1/o/{ORG}/e/{ENV}/targetservers`

> List Target Servers



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 
| ENV | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ENV"` | 

#### Request Headers
>Authorization="Authorization";

#### Responses
**200**


### <a name="add_target"></a>![Endpoint: ](https://apidocs.io/img/method.png "Add Target") Add Target


**`POST`** `/v1/o/{ORG}/e/{ENV}/targetservers`

> Add Target



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 
| ENV | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ENV"` | 

#### Request Headers
>Accept=application/json;
>Content-Type=application/json;
>content-type="content-type";
>Authorization="Authorization";

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| `add targetrequest` |  ``` Required ```  | TODO: Add a parameter description | 

 Example 
``` 
{
  "host": "host",
  "isEnabled": true,
  "name": "name",
  "port": 230
}
``` 

#### Responses
**200**


[Back to API Reference](#api_reference)

## <a name="company"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Company") Company


### <a name="create_company"></a>![Endpoint: ](https://apidocs.io/img/method.png "Create Company") Create Company


**`POST`** `/v1/organizations/{ORG}/companies`

> Create Company



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| ORG | `string` |  ``` Required ```  | TODO: Add a parameter description | `"ORG"` | 

#### Request Headers
>Authorization="Authorization";
>Content-Type="Content-Type";

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| `string` |  ``` Required ```  | TODO: Add a parameter description | 

 Example 
``` 
"Body"
``` 

#### Responses
**200**


[Back to API Reference](#api_reference)

## <a name="organizations"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Organizations") Organizations


### <a name="list_organizations"></a>![Endpoint: ](https://apidocs.io/img/method.png "List organizations") List organizations


**`GET`** `/v1/organizations`

> List organizations



#### Request Headers
>Authorization=Basic {{BASICAUTH}};

#### Responses
**200**


[Back to API Reference](#api_reference)


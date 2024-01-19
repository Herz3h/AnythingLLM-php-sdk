# Swagger\Client\AdminApi

All URIs are relative to *https://raw.githubusercontent.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1AdminInviteIdDelete**](AdminApi.md#v1admininviteiddelete) | **DELETE** /v1/admin/invite/{id} | 
[**v1AdminInviteNewPost**](AdminApi.md#v1admininvitenewpost) | **POST** /v1/admin/invite/new | 
[**v1AdminInvitesGet**](AdminApi.md#v1admininvitesget) | **GET** /v1/admin/invites | 
[**v1AdminIsMultiUserModeGet**](AdminApi.md#v1adminismultiusermodeget) | **GET** /v1/admin/is-multi-user-mode | 
[**v1AdminPreferencesGet**](AdminApi.md#v1adminpreferencesget) | **GET** /v1/admin/preferences | 
[**v1AdminPreferencesPost**](AdminApi.md#v1adminpreferencespost) | **POST** /v1/admin/preferences | 
[**v1AdminUsersGet**](AdminApi.md#v1adminusersget) | **GET** /v1/admin/users | 
[**v1AdminUsersIdDelete**](AdminApi.md#v1adminusersiddelete) | **DELETE** /v1/admin/users/{id} | 
[**v1AdminUsersIdPost**](AdminApi.md#v1adminusersidpost) | **POST** /v1/admin/users/{id} | 
[**v1AdminUsersNewPost**](AdminApi.md#v1adminusersnewpost) | **POST** /v1/admin/users/new | 
[**v1AdminWorkspaceChatsPost**](AdminApi.md#v1adminworkspacechatspost) | **POST** /v1/admin/workspace-chats | 
[**v1AdminWorkspacesWorkspaceIdUpdateUsersPost**](AdminApi.md#v1adminworkspacesworkspaceidupdateuserspost) | **POST** /v1/admin/workspaces/{workspaceId}/update-users | 

# **v1AdminInviteIdDelete**
> object v1AdminInviteIdDelete($id, $authorization)



Deactivates (soft-delete) invite by id. Methods are disabled until multi user mode is enabled via the UI.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\AdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | id of the invite in the database.
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1AdminInviteIdDelete($id, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdminApi->v1AdminInviteIdDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| id of the invite in the database. |
 **authorization** | **string**|  | [optional]

### Return type

**object**

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1AdminInviteNewPost**
> object v1AdminInviteNewPost($authorization)



Create a new invite code for someone to use to register with instance. Methods are disabled until multi user mode is enabled via the UI.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\AdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1AdminInviteNewPost($authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdminApi->v1AdminInviteNewPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **string**|  | [optional]

### Return type

**object**

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1AdminInvitesGet**
> object v1AdminInvitesGet($authorization)



List all existing invitations to instance regardless of status. Methods are disabled until multi user mode is enabled via the UI.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\AdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1AdminInvitesGet($authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdminApi->v1AdminInvitesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **string**|  | [optional]

### Return type

**object**

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1AdminIsMultiUserModeGet**
> object v1AdminIsMultiUserModeGet($authorization)



Check to see if the instance is in multi-user-mode first. Methods are disabled until multi user mode is enabled via the UI.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\AdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1AdminIsMultiUserModeGet($authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdminApi->v1AdminIsMultiUserModeGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **string**|  | [optional]

### Return type

**object**

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1AdminPreferencesGet**
> object v1AdminPreferencesGet($authorization)



Show all multi-user preferences for instance. Methods are disabled until multi user mode is enabled via the UI.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\AdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1AdminPreferencesGet($authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdminApi->v1AdminPreferencesGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **string**|  | [optional]

### Return type

**object**

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1AdminPreferencesPost**
> object v1AdminPreferencesPost($authorization)



Update multi-user preferences for instance. Methods are disabled until multi user mode is enabled via the UI.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\AdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1AdminPreferencesPost($authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdminApi->v1AdminPreferencesPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **string**|  | [optional]

### Return type

**object**

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1AdminUsersGet**
> object v1AdminUsersGet($authorization)



Check to see if the instance is in multi-user-mode first. Methods are disabled until multi user mode is enabled via the UI.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\AdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1AdminUsersGet($authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdminApi->v1AdminUsersGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **string**|  | [optional]

### Return type

**object**

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1AdminUsersIdDelete**
> object v1AdminUsersIdDelete($id, $authorization)



Delete existing user by id. Methods are disabled until multi user mode is enabled via the UI.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\AdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | id of the user in the database.
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1AdminUsersIdDelete($id, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdminApi->v1AdminUsersIdDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| id of the user in the database. |
 **authorization** | **string**|  | [optional]

### Return type

**object**

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1AdminUsersIdPost**
> object v1AdminUsersIdPost($id, $authorization)



Update existing user settings. Methods are disabled until multi user mode is enabled via the UI.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\AdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = "id_example"; // string | id of the user in the database.
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1AdminUsersIdPost($id, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdminApi->v1AdminUsersIdPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**| id of the user in the database. |
 **authorization** | **string**|  | [optional]

### Return type

**object**

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1AdminUsersNewPost**
> object v1AdminUsersNewPost($authorization)



Create a new user with username and password. Methods are disabled until multi user mode is enabled via the UI.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\AdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1AdminUsersNewPost($authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdminApi->v1AdminUsersNewPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **string**|  | [optional]

### Return type

**object**

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1AdminWorkspaceChatsPost**
> object v1AdminWorkspaceChatsPost($authorization)



All chats in the system ordered by most recent. Methods are disabled until multi user mode is enabled via the UI.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\AdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1AdminWorkspaceChatsPost($authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdminApi->v1AdminWorkspaceChatsPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **string**|  | [optional]

### Return type

**object**

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1AdminWorkspacesWorkspaceIdUpdateUsersPost**
> object v1AdminWorkspacesWorkspaceIdUpdateUsersPost($workspace_id, $authorization)



Overwrite workspace permissions to only be accessible by the given user ids and admins. Methods are disabled until multi user mode is enabled via the UI.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\AdminApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$workspace_id = "workspace_id_example"; // string | id of the workspace in the database.
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1AdminWorkspacesWorkspaceIdUpdateUsersPost($workspace_id, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdminApi->v1AdminWorkspacesWorkspaceIdUpdateUsersPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_id** | **string**| id of the workspace in the database. |
 **authorization** | **string**|  | [optional]

### Return type

**object**

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)


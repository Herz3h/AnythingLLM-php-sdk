# Swagger\Client\WorkspacesApi

All URIs are relative to *https://raw.githubusercontent.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1WorkspaceNewPost**](WorkspacesApi.md#v1workspacenewpost) | **POST** /v1/workspace/new | 
[**v1WorkspaceSlugChatPost**](WorkspacesApi.md#v1workspaceslugchatpost) | **POST** /v1/workspace/{slug}/chat | 
[**v1WorkspaceSlugChatsGet**](WorkspacesApi.md#v1workspaceslugchatsget) | **GET** /v1/workspace/{slug}/chats | 
[**v1WorkspaceSlugDelete**](WorkspacesApi.md#v1workspaceslugdelete) | **DELETE** /v1/workspace/{slug} | 
[**v1WorkspaceSlugGet**](WorkspacesApi.md#v1workspaceslugget) | **GET** /v1/workspace/{slug} | 
[**v1WorkspaceSlugStreamChatPost**](WorkspacesApi.md#v1workspaceslugstreamchatpost) | **POST** /v1/workspace/{slug}/stream-chat | 
[**v1WorkspaceSlugUpdateEmbeddingsPost**](WorkspacesApi.md#v1workspaceslugupdateembeddingspost) | **POST** /v1/workspace/{slug}/update-embeddings | 
[**v1WorkspaceSlugUpdatePost**](WorkspacesApi.md#v1workspaceslugupdatepost) | **POST** /v1/workspace/{slug}/update | 
[**v1WorkspacesGet**](WorkspacesApi.md#v1workspacesget) | **GET** /v1/workspaces | 

# **v1WorkspaceNewPost**
> object v1WorkspaceNewPost($authorization)



Create a new workspace

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1WorkspaceNewPost($authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->v1WorkspaceNewPost: ', $e->getMessage(), PHP_EOL;
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

# **v1WorkspaceSlugChatPost**
> object v1WorkspaceSlugChatPost($slug, $authorization)



Execute a chat with a workspace

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$slug = "slug_example"; // string | 
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1WorkspaceSlugChatPost($slug, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->v1WorkspaceSlugChatPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **slug** | **string**|  |
 **authorization** | **string**|  | [optional]

### Return type

**object**

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1WorkspaceSlugChatsGet**
> object v1WorkspaceSlugChatsGet($slug, $authorization)



Get a workspaces chats regardless of user by its unique slug.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$slug = "slug_example"; // string | Unique slug of workspace to find
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1WorkspaceSlugChatsGet($slug, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->v1WorkspaceSlugChatsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **slug** | **string**| Unique slug of workspace to find |
 **authorization** | **string**|  | [optional]

### Return type

**object**

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1WorkspaceSlugDelete**
> v1WorkspaceSlugDelete($slug, $authorization)



Deletes a workspace by its slug.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$slug = "slug_example"; // string | Unique slug of workspace to delete
$authorization = "authorization_example"; // string | 

try {
    $apiInstance->v1WorkspaceSlugDelete($slug, $authorization);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->v1WorkspaceSlugDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **slug** | **string**| Unique slug of workspace to delete |
 **authorization** | **string**|  | [optional]

### Return type

void (empty response body)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1WorkspaceSlugGet**
> object v1WorkspaceSlugGet($slug, $authorization)



Get a workspace by its unique slug.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$slug = "slug_example"; // string | Unique slug of workspace to find
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1WorkspaceSlugGet($slug, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->v1WorkspaceSlugGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **slug** | **string**| Unique slug of workspace to find |
 **authorization** | **string**|  | [optional]

### Return type

**object**

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1WorkspaceSlugStreamChatPost**
> array v1WorkspaceSlugStreamChatPost($slug, $authorization)



Execute a streamable chat with a workspace

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$slug = "slug_example"; // string | 
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1WorkspaceSlugStreamChatPost($slug, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->v1WorkspaceSlugStreamChatPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **slug** | **string**|  |
 **authorization** | **string**|  | [optional]

### Return type

[**array**](../Model/array.md)

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: text/event-stream, application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1WorkspaceSlugUpdateEmbeddingsPost**
> object v1WorkspaceSlugUpdateEmbeddingsPost($slug, $authorization)



Add or remove documents from a workspace by its unique slug.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$slug = "slug_example"; // string | Unique slug of workspace to find
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1WorkspaceSlugUpdateEmbeddingsPost($slug, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->v1WorkspaceSlugUpdateEmbeddingsPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **slug** | **string**| Unique slug of workspace to find |
 **authorization** | **string**|  | [optional]

### Return type

**object**

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1WorkspaceSlugUpdatePost**
> object v1WorkspaceSlugUpdatePost($slug, $authorization)



Update workspace settings by its unique slug.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$slug = "slug_example"; // string | Unique slug of workspace to find
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1WorkspaceSlugUpdatePost($slug, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->v1WorkspaceSlugUpdatePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **slug** | **string**| Unique slug of workspace to find |
 **authorization** | **string**|  | [optional]

### Return type

**object**

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1WorkspacesGet**
> object v1WorkspacesGet($authorization)



List all current workspaces

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\WorkspacesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1WorkspacesGet($authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkspacesApi->v1WorkspacesGet: ', $e->getMessage(), PHP_EOL;
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


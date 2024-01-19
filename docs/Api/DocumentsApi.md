# Swagger\Client\DocumentsApi

All URIs are relative to *https://raw.githubusercontent.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**v1DocumentAcceptedFileTypesGet**](DocumentsApi.md#v1documentacceptedfiletypesget) | **GET** /v1/document/accepted-file-types | 
[**v1DocumentDocNameGet**](DocumentsApi.md#v1documentdocnameget) | **GET** /v1/document/{docName} | 
[**v1DocumentUploadLinkPost**](DocumentsApi.md#v1documentuploadlinkpost) | **POST** /v1/document/upload-link | 
[**v1DocumentUploadPost**](DocumentsApi.md#v1documentuploadpost) | **POST** /v1/document/upload | 
[**v1DocumentsGet**](DocumentsApi.md#v1documentsget) | **GET** /v1/documents | 

# **v1DocumentAcceptedFileTypesGet**
> object v1DocumentAcceptedFileTypesGet($authorization)



Check available filetypes and MIMEs that can be uploaded.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1DocumentAcceptedFileTypesGet($authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->v1DocumentAcceptedFileTypesGet: ', $e->getMessage(), PHP_EOL;
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

# **v1DocumentDocNameGet**
> object v1DocumentDocNameGet($doc_name, $authorization)



Get a single document by its unique AnythingLLM document name

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$doc_name = "doc_name_example"; // string | Unique document name to find (name in /documents)
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1DocumentDocNameGet($doc_name, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->v1DocumentDocNameGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **doc_name** | **string**| Unique document name to find (name in /documents) |
 **authorization** | **string**|  | [optional]

### Return type

**object**

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1DocumentUploadLinkPost**
> object v1DocumentUploadLinkPost($body, $authorization)



Upload a valid URL for AnythingLLM to scrape and prepare for embedding.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \stdClass; // object | Link of web address to be scraped.
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1DocumentUploadLinkPost($body, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->v1DocumentUploadLinkPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**object**](../Model/object.md)| Link of web address to be scraped. |
 **authorization** | **string**|  | [optional]

### Return type

**object**

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1DocumentUploadPost**
> object v1DocumentUploadPost($file, $authorization)



Upload a new file to AnythingLLM to be parsed and prepared for embedding.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file = "file_example"; // string | 
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1DocumentUploadPost($file, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->v1DocumentUploadPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **string****string**|  |
 **authorization** | **string**|  | [optional]

### Return type

**object**

### Authorization

[BearerAuth](../../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json, application/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **v1DocumentsGet**
> object v1DocumentsGet($authorization)



List of all locally-stored documents in instance

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
    // Configure HTTP bearer authorization: BearerAuth
    $config = Swagger\Client\Configuration::getDefaultConfiguration()
    ->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Swagger\Client\Api\DocumentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$authorization = "authorization_example"; // string | 

try {
    $result = $apiInstance->v1DocumentsGet($authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DocumentsApi->v1DocumentsGet: ', $e->getMessage(), PHP_EOL;
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


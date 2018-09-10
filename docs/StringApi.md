# StringApi

All URIs are relative to */api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getStringsByName**](StringApi.md#getStringsByName) | **GET** /strings/{name} | Get Strings (formatted)


## **getStringsByName**

Get Strings (formatted)

Get Strings (formatted)

### Example
```bash
radiomanager-cli getStringsByName name=value  full_model=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string** | Name of Strings **(Required)** |
 **fullModel** | **boolean** | Full model or content only **(Required)** | [default to true]

### Return type

[**TextString**](TextString.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


# ContactApi

All URIs are relative to */api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createContact**](ContactApi.md#createContact) | **POST** /contacts | Create contact.
[**deleteContactById**](ContactApi.md#deleteContactById) | **DELETE** /contacts/{id} | Delete contact by id
[**getContactById**](ContactApi.md#getContactById) | **GET** /contacts/{id} | Get contact by id
[**listContacts**](ContactApi.md#listContacts) | **GET** /contacts | Get all contacts.
[**updateContactByID**](ContactApi.md#updateContactByID) | **PATCH** /contacts/{id} | Update contact by id


## **createContact**

Create contact.

Create contact.

### Example
```bash
radiomanager-cli createContact
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **data** | [**ContactDataInput**](ContactDataInput.md) | Data **(Required)** |

### Return type

[**PostSuccess**](PostSuccess.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **deleteContactById**

Delete contact by id

Delete contact by id

### Example
```bash
radiomanager-cli deleteContactById id=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of Contact **(Required)** |

### Return type

[**Success**](Success.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **getContactById**

Get contact by id

Get contact by id

### Example
```bash
radiomanager-cli getContactById id=value  _external_station_id=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of Contact **(Required)** |
 **externalStationId** | **integer** | Query on a different (content providing) station *(Optional)* | [optional]

### Return type

[**ContactResult**](ContactResult.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **listContacts**

Get all contacts.

List all contacts.

### Example
```bash
radiomanager-cli listContacts  page=value  item_id=value  model_type_id=value  tag_id=value  limit=value  order-by=value  order-direction=value  _external_station_id=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **integer** | Current page *(Optional)* | [optional] [default to 1]
 **itemId** | **integer** | Search on Item ID *(Optional)* '(Relation)' | [optional]
 **modelTypeId** | **integer** | Search on ModelType ID *(Optional)* '(Relation)' | [optional]
 **tagId** | **integer** | Search on Tag ID *(Optional)* '(Relation)' | [optional]
 **limit** | **integer** | Results per page *(Optional)* | [optional]
 **orderBy** | **string** | Field to order the results *(Optional)* | [optional]
 **orderDirection** | **string** | Direction of ordering *(Optional)* | [optional]
 **externalStationId** | **integer** | Query on a different (content providing) station *(Optional)* | [optional]

### Return type

[**ContactResults**](ContactResults.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **updateContactByID**

Update contact by id

Update contact by id

### Example
```bash
radiomanager-cli updateContactByID id=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of Contact **(Required)** |
 **data** | [**ContactDataInput**](ContactDataInput.md) | Data *(Optional)* | [optional]

### Return type

[**Success**](Success.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


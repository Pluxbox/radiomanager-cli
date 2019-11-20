# ModelTypeApi

All URIs are relative to */api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getModelTypeById**](ModelTypeApi.md#getModelTypeById) | **GET** /model_types/{id} | Get modelType by id
[**listModelTypes**](ModelTypeApi.md#listModelTypes) | **GET** /model_types | Get all modelTypes.


## **getModelTypeById**

Get modelType by id

Get modelType by id

### Example
```bash
radiomanager-cli getModelTypeById id=value  _external_station_id=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of ModelType **(Required)** |
 **externalStationId** | **integer** | Query on a different (content providing) station *(Optional)* | [optional]

### Return type

[**ModelTypeResult**](ModelTypeResult.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **listModelTypes**

Get all modelTypes.

List all modelTypes.

### Example
```bash
radiomanager-cli listModelTypes  page=value  program_id=value  broadcast_id=value  item_id=value  campaign_id=value  presenter_id=value  contact_id=value  model=value  limit=value  order-by=value  order-direction=value  _external_station_id=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **integer** | Current page *(Optional)* | [optional]
 **programId** | **integer** | Search on Program ID *(Optional)* | [optional]
 **broadcastId** | **integer** | Search on Broadcast ID *(Optional)* | [optional]
 **itemId** | **integer** | Search on Item ID *(Optional)* | [optional]
 **campaignId** | **integer** | Search on Campaign ID *(Optional)* | [optional]
 **presenterId** | **integer** | Search on Presenter ID *(Optional)* | [optional]
 **contactId** | **integer** | Search on Contact ID *(Optional)* | [optional]
 **model** | **string** | Search Modeltypes for certain Model *(Optional)* | [optional]
 **limit** | **integer** | Results per page *(Optional)* | [optional]
 **orderBy** | **string** | Field to order the results *(Optional)* | [optional]
 **orderDirection** | **string** | Direction of ordering *(Optional)* | [optional]
 **externalStationId** | **integer** | Query on a different (content providing) station *(Optional)* | [optional]

### Return type

[**ModelTypeResults**](ModelTypeResults.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


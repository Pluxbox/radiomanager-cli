# ModelTypeApi

All URIs are relative to */api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getModelTypeById**](ModelTypeApi.md#getModelTypeById) | **GET** /model_types/{id} | Get modelType by id
[**listModelTypes**](ModelTypeApi.md#listModelTypes) | **GET** /model_types | Get all modelTypes.



## getModelTypeById

Get modelType by id

Get modelType by id

### Example

```bash
radiomanager-cli getModelTypeById id=value  order-direction=value  _external_station_id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of ModelType **(Required)** | [default to null]
 **orderDirection** | **string** | Direction of ordering *(Optional)* | [optional] [default to null]
 **externalStationId** | **integer** | Query on a different (content providing) station *(Optional)* | [optional] [default to null]

### Return type

[**ModelTypeResult**](ModelTypeResult.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## listModelTypes

Get all modelTypes.

List all modelTypes.

### Example

```bash
radiomanager-cli listModelTypes  program_id=value  broadcast_id=value  item_id=value  campaign_id=value  presenter_id=value  contact_id=value  model=value  order-direction=value  _external_station_id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **programId** | **integer** | Search on Program ID *(Optional)* | [optional] [default to null]
 **broadcastId** | **integer** | Search on Broadcast ID *(Optional)* | [optional] [default to null]
 **itemId** | **integer** | Search on Item ID *(Optional)* | [optional] [default to null]
 **campaignId** | **integer** | Search on Campaign ID *(Optional)* | [optional] [default to null]
 **presenterId** | **integer** | Search on Presenter ID *(Optional)* | [optional] [default to null]
 **contactId** | **integer** | Search on Contact ID *(Optional)* | [optional] [default to null]
 **model** | **string** | Search Modeltypes for certain Model *(Optional)* | [optional] [default to null]
 **orderDirection** | **string** | Direction of ordering *(Optional)* | [optional] [default to null]
 **externalStationId** | **integer** | Query on a different (content providing) station *(Optional)* | [optional] [default to null]

### Return type

[**InlineResponse2009**](InlineResponse2009.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


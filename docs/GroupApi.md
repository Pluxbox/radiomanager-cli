# GroupApi

All URIs are relative to */api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getGroupById**](GroupApi.md#getGroupById) | **GET** /groups/{id} | Get group by id
[**listGroups**](GroupApi.md#listGroups) | **GET** /groups | Get all groups.



## getGroupById

Get group by id

Get group by id

### Example

```bash
radiomanager-cli getGroupById id=value  _external_station_id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | id of Group | [default to null]
 **externalStationId** | **integer** | Query on a different (content providing) station *(Optional)* | [optional] [default to null]

### Return type

[**GroupResult**](GroupResult.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## listGroups

Get all groups.

List all groups.

### Example

```bash
radiomanager-cli listGroups  broadcast_id=value  program_id=value  user_id=value  page=value  limit=value  order-by=value  order-direction=value  _external_station_id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **broadcastId** | **integer** | Search on Broadcast ID *(Optional)* '(Relation)' | [optional] [default to null]
 **programId** | **integer** | Search on Program ID *(Optional)* '(Relation)' | [optional] [default to null]
 **userId** | **integer** | Search on User ID *(Optional)* '(Relation)' | [optional] [default to null]
 **page** | **integer** | Current page *(Optional)* | [optional] [default to 1]
 **limit** | **integer** | Results per page *(Optional)* | [optional] [default to null]
 **orderBy** | **string** | Field to order the results *(Optional)* | [optional] [default to null]
 **orderDirection** | **string** | Direction of ordering *(Optional)* | [optional] [default to null]
 **externalStationId** | **integer** | Query on a different (content providing) station *(Optional)* | [optional] [default to null]

### Return type

[**InlineResponse2007**](InlineResponse2007.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


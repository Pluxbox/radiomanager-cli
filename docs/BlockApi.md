# BlockApi

All URIs are relative to */api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getBlockById**](BlockApi.md#getBlockById) | **GET** /blocks/{id} | Get block by id
[**getCurrentBlock**](BlockApi.md#getCurrentBlock) | **GET** /blocks/current | Get current Block
[**getNextBlock**](BlockApi.md#getNextBlock) | **GET** /blocks/next | Get upcoming Block
[**listBlocks**](BlockApi.md#listBlocks) | **GET** /blocks | Get a list of all blocks currently in your station.



## getBlockById

Get block by id

Get block by id

### Example

```bash
radiomanager-cli getBlockById id=value  _external_station_id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of Block **(Required)** | [default to null]
 **externalStationId** | **integer** | Query on a different (content providing) station *(Optional)* | [optional] [default to null]

### Return type

[**BlockResult**](BlockResult.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getCurrentBlock

Get current Block

Get currently playing Block

### Example

```bash
radiomanager-cli getCurrentBlock
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**BlockResult**](BlockResult.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getNextBlock

Get upcoming Block

Get currently upcoming Block

### Example

```bash
radiomanager-cli getNextBlock
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**BlockResult**](BlockResult.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## listBlocks

Get a list of all blocks currently in your station.

Get a list of all blocks currently in your station. This feature supports pagination and will give a maximum of 50 blocks back.

### Example

```bash
radiomanager-cli listBlocks  broadcast_id=value  item_id=value  program_id=value  start-min=value  start-max=value  page=value  limit=value  order-by=value  order-direction=value  _external_station_id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **broadcastId** | **integer** | Search on Broadcast ID *(Optional)* '(Relation)' | [optional] [default to null]
 **itemId** | **integer** | Search on Item ID *(Optional)* '(Relation)' | [optional] [default to null]
 **programId** | **integer** | Search on Program ID *(Optional)* '(Relation)' | [optional] [default to null]
 **startMin** | **string** | Minimum start date *(Optional)* | [optional] [default to null]
 **startMax** | **string** | Maximum start date *(Optional)* | [optional] [default to null]
 **page** | **integer** | Current page *(Optional)* | [optional] [default to 1]
 **limit** | **integer** | Results per page *(Optional)* | [optional] [default to null]
 **orderBy** | **string** | Field to order the results *(Optional)* | [optional] [default to null]
 **orderDirection** | **string** | Direction of ordering *(Optional)* | [optional] [default to null]
 **externalStationId** | **integer** | Query on a different (content providing) station *(Optional)* | [optional] [default to null]

### Return type

[**InlineResponse200**](InlineResponse200.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


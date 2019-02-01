# ItemApi

All URIs are relative to */api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createItem**](ItemApi.md#createItem) | **POST** /items | Create an new item.
[**currentItemPostStructure**](ItemApi.md#currentItemPostStructure) | **POST** /items/current/structure | Post a current playing item, keep structure
[**currentItemPostTiming**](ItemApi.md#currentItemPostTiming) | **POST** /items/current/timing | Post a current playing item
[**deleteItemById**](ItemApi.md#deleteItemById) | **DELETE** /items/{id} | Delete item by ID.
[**getCurrentItem**](ItemApi.md#getCurrentItem) | **GET** /items/current | Get current Item
[**getItemById**](ItemApi.md#getItemById) | **GET** /items/{id} | Get extended item details by ID.
[**listItems**](ItemApi.md#listItems) | **GET** /items | Get a list of all the items currently in your station.
[**playlistPostMerge**](ItemApi.md#playlistPostMerge) | **POST** /items/playlist/merge | Post a playlist, do not remove previously imported items
[**playlistPostStructure**](ItemApi.md#playlistPostStructure) | **POST** /items/playlist/structure | Post a playlist, keep current structure
[**playlistPostTiming**](ItemApi.md#playlistPostTiming) | **POST** /items/playlist/timing | Post a playlist
[**stopCurrentItem**](ItemApi.md#stopCurrentItem) | **POST** /items/stopcurrent | Stop an Item
[**updateItemById**](ItemApi.md#updateItemById) | **PATCH** /items/{id} | Update extended item details by ID.


## **createItem**

Create an new item.

Create item.

### Example
```bash
radiomanager-cli createItem
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **data** | [**ItemDataInput**](ItemDataInput.md) | Data *(Optional)* | [optional]

### Return type

[**PostSuccess**](PostSuccess.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **currentItemPostStructure**

Post a current playing item, keep structure

Post a current playing item, keep structure

### Example
```bash
radiomanager-cli currentItemPostStructure
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **data** | [**ImportItem**](ImportItem.md) | Data *(Optional)* | [optional]

### Return type

[**Success**](Success.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **currentItemPostTiming**

Post a current playing item

Post a current playing item

### Example
```bash
radiomanager-cli currentItemPostTiming
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **data** | [**ImportItem**](ImportItem.md) | Data *(Optional)* | [optional]

### Return type

[**Success**](Success.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **deleteItemById**

Delete item by ID.

Delete item by id.

### Example
```bash
radiomanager-cli deleteItemById id=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of Item **(Required)** |

### Return type

[**Success**](Success.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **getCurrentItem**

Get current Item

Get current Item

### Example
```bash
radiomanager-cli getCurrentItem  lastplayed=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **lastplayed** | **boolean** | Show last played item if there is no current item*(Optional)* | [optional]

### Return type

[**ItemResult**](ItemResult.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **getItemById**

Get extended item details by ID.

Read item by id.

### Example
```bash
radiomanager-cli getItemById id=value  _external_station_id=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of Item **(Required)** |
 **externalStationId** | **integer** | Query on a different (content providing) station *(Optional)* | [optional]

### Return type

[**ItemResult**](ItemResult.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **listItems**

Get a list of all the items currently in your station.

Get a list of all the items currently in your station. This feature supports pagination and will give a maximum results of 50 items back.

### Example
```bash
radiomanager-cli listItems  page=value  block_id=value  broadcast_id=value  model_type_id=value  tag_id=value  campaign_id=value  contact_id=value  program_draft_id=value  user_draft_id=value  station_draft_id=value  program_id=value  external_id=value  start-min=value  start-max=value  duration-min=value  duration-max=value  status=value  limit=value  order-by=value  order-direction=value  _external_station_id=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **integer** | Current page *(Optional)* | [optional]
 **blockId** | **integer** | Search on Block ID *(Optional)* '(Relation)' | [optional]
 **broadcastId** | **integer** | Search on Broadcast ID *(Optional)* '(Relation)' | [optional]
 **modelTypeId** | **integer** | Search on ModelType ID *(Optional)* '(Relation)' | [optional]
 **tagId** | **integer** | Search on Tag ID *(Optional)* '(Relation)' | [optional]
 **campaignId** | **integer** | Search on Campaign ID *(Optional)* '(Relation)' | [optional]
 **contactId** | **integer** | Search on Contact ID *(Optional)* '(Relation)' | [optional]
 **programDraftId** | **integer** | Search on Program Draft ID *(Optional)* | [optional]
 **userDraftId** | **integer** | Search on User Draft ID *(Optional)* | [optional]
 **stationDraftId** | **integer** | Search on Station Draft ID *(Optional)* | [optional]
 **programId** | **integer** | Search on Program ID *(Optional)* '(Relation)' | [optional]
 **externalId** | **string** | Search on External ID *(Optional)* | [optional]
 **startMin** | **string** | Minimum start date *(Optional)* | [optional]
 **startMax** | **string** | Maximum start date *(Optional)* | [optional]
 **durationMin** | **integer** | Minimum duration (seconds) *(Optional)* | [optional]
 **durationMax** | **integer** | Maximum duration (seconds) *(Optional)* | [optional]
 **status** | **string** | Play Status of item *(Optional)* | [optional]
 **limit** | **integer** | Results per page *(Optional)* | [optional]
 **orderBy** | **string** | Field to order the results *(Optional)* | [optional]
 **orderDirection** | **string** | Direction of ordering *(Optional)* | [optional]
 **externalStationId** | **integer** | Query on a different (content providing) station *(Optional)* | [optional]

### Return type

[**ItemResults**](ItemResults.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **playlistPostMerge**

Post a playlist, do not remove previously imported items

Post a playlist, do not remove previously imported items

### Example
```bash
radiomanager-cli playlistPostMerge
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **data** | [**Data_2**](Data_2.md) | Data *(Optional)* | [optional]

### Return type

[**Inline_response_202**](Inline_response_202.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **playlistPostStructure**

Post a playlist, keep current structure

Post a playlist, keep current structure

### Example
```bash
radiomanager-cli playlistPostStructure
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **data** | [**Data_1**](Data_1.md) | Data *(Optional)* | [optional]

### Return type

[**Inline_response_202**](Inline_response_202.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **playlistPostTiming**

Post a playlist

Post a playlist

### Example
```bash
radiomanager-cli playlistPostTiming
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **data** | [**Data**](Data.md) | Data *(Optional)* | [optional]

### Return type

[**Inline_response_202**](Inline_response_202.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **stopCurrentItem**

Stop an Item

Set a current playing or specific item on played

### Example
```bash
radiomanager-cli stopCurrentItem
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **data** | [**Data_3**](Data_3.md) | Data *(Optional)* | [optional]

### Return type

[**Success**](Success.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **updateItemById**

Update extended item details by ID.

Update item by id.

### Example
```bash
radiomanager-cli updateItemById id=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of Item **(Required)** |
 **data** | [**ItemDataInput**](ItemDataInput.md) | Data *(Optional)* | [optional]

### Return type

[**Success**](Success.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


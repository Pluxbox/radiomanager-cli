# ItemApi

All URIs are relative to */api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createItem**](ItemApi.md#createItem) | **POST** /items | Create an new item.
[**currentItemPostStructure**](ItemApi.md#currentItemPostStructure) | **POST** /items/current/structure | Post a current playing item, keep structure
[**currentItemPostTiming**](ItemApi.md#currentItemPostTiming) | **POST** /items/current/timing | Post current playing Item
[**deleteItemById**](ItemApi.md#deleteItemById) | **DELETE** /items/{id} | Delete item by ID.
[**getCurrentItem**](ItemApi.md#getCurrentItem) | **GET** /items/current | Get current Item
[**getItemById**](ItemApi.md#getItemById) | **GET** /items/{id} | Get extended item details by ID.
[**listItems**](ItemApi.md#listItems) | **GET** /items | Get a list of all the items currently in your station.
[**playlistPostMerge**](ItemApi.md#playlistPostMerge) | **POST** /items/playlist/merge | Post a playlist, do not remove previously imported items
[**playlistPostStructure**](ItemApi.md#playlistPostStructure) | **POST** /items/playlist/structure | Post a playlist, keep current structure
[**playlistPostTiming**](ItemApi.md#playlistPostTiming) | **POST** /items/playlist/timing | Post a playlist
[**stopCurrentItem**](ItemApi.md#stopCurrentItem) | **POST** /items/stopcurrent | Stop an Item
[**updateItemById**](ItemApi.md#updateItemById) | **PATCH** /items/{id} | Update extended item details by ID.



## createItem

Create an new item.

Create item.

### Example

```bash
radiomanager-cli createItem
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **itemDataInput** | [**ItemDataInput**](ItemDataInput.md) | Data **(Required)** |

### Return type

[**InlineResponse2002**](InlineResponse2002.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## currentItemPostStructure

Post a current playing item, keep structure

Post current playing Item. Can be existing Item referenced by external_id. When Items are moved, this function **will attempt to** keep Items' ModelType structure in rundown.

### Example

```bash
radiomanager-cli currentItemPostStructure
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **importItem** | [**ImportItem**](ImportItem.md) | Data **(Required)** |

### Return type

[**ItemResult**](ItemResult.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## currentItemPostTiming

Post current playing Item

Post current playing Item. Can be existing Item referenced by external_id. When Items are moved, this function **will not keep** Items' ModelType structure in rundown.

### Example

```bash
radiomanager-cli currentItemPostTiming
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **importItem** | [**ImportItem**](ImportItem.md) | Data **(Required)** |

### Return type

[**ItemResult**](ItemResult.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## deleteItemById

Delete item by ID.

Delete item by id.

### Example

```bash
radiomanager-cli deleteItemById id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of Item **(Required)** | [default to null]

### Return type

(empty response body)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getCurrentItem

Get current Item

Get current Item

### Example

```bash
radiomanager-cli getCurrentItem  lastplayed=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **lastplayed** | **boolean** | Show last played item if there is no current item*(Optional)* | [optional] [default to null]

### Return type

[**ItemResult**](ItemResult.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getItemById

Get extended item details by ID.

Read item by id.

### Example

```bash
radiomanager-cli getItemById id=value  _external_station_id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of Item **(Required)** | [default to null]
 **externalStationId** | **integer** | Query on a different (content providing) station *(Optional)* | [optional] [default to null]

### Return type

[**ItemResult**](ItemResult.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## listItems

Get a list of all the items currently in your station.

Get a list of all the items currently in your station. This feature supports pagination and will give a maximum results of 50 items back.

### Example

```bash
radiomanager-cli listItems  block_id=value  broadcast_id=value  model_type_id=value  tag_id=value  campaign_id=value  contact_id=value  program_draft_id=value  user_draft_id=value  station_draft_id=value  program_id=value  external_id=value  duration-min=value  duration-max=value  status=value  start-min=value  start-max=value  page=value  limit=value  order-by=value  order-direction=value  _external_station_id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **blockId** | **integer** | Search on Block ID *(Optional)* '(Relation)' | [optional] [default to null]
 **broadcastId** | **integer** | Search on Broadcast ID *(Optional)* '(Relation)' | [optional] [default to null]
 **modelTypeId** | **integer** | Search on ModelType ID *(Optional)* '(Relation)' | [optional] [default to null]
 **tagId** | **integer** | Search on Tag ID *(Optional)* '(Relation)' | [optional] [default to null]
 **campaignId** | **integer** | Search on Campaign ID *(Optional)* '(Relation)' | [optional] [default to null]
 **contactId** | **integer** | Search on Contact ID *(Optional)* '(Relation)' | [optional] [default to null]
 **programDraftId** | **integer** | Search on Program Draft ID *(Optional)* | [optional] [default to null]
 **userDraftId** | **integer** | Search on User Draft ID *(Optional)* | [optional] [default to null]
 **stationDraftId** | **integer** | Search on Station Draft ID *(Optional)* | [optional] [default to null]
 **programId** | **integer** | Search on Program ID *(Optional)* '(Relation)' | [optional] [default to null]
 **externalId** | **string** | Search on External ID *(Optional)* | [optional] [default to null]
 **durationMin** | **integer** | Minimum duration (seconds) *(Optional)* | [optional] [default to null]
 **durationMax** | **integer** | Maximum duration (seconds) *(Optional)* | [optional] [default to null]
 **status** | **string** | Play Status of item *(Optional)* | [optional] [default to null]
 **startMin** | **string** | Minimum start date *(Optional)* | [optional] [default to null]
 **startMax** | **string** | Maximum start date *(Optional)* | [optional] [default to null]
 **page** | **integer** | Current page *(Optional)* | [optional] [default to 1]
 **limit** | **integer** | Results per page *(Optional)* | [optional] [default to null]
 **orderBy** | **string** | Field to order the results *(Optional)* | [optional] [default to null]
 **orderDirection** | **string** | Direction of ordering *(Optional)* | [optional] [default to null]
 **externalStationId** | **integer** | Query on a different (content providing) station *(Optional)* | [optional] [default to null]

### Return type

[**InlineResponse2008**](InlineResponse2008.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## playlistPostMerge

Post a playlist, do not remove previously imported items

Post a playlist with 'keep structure' method, but do not remove previously imported items

### Example

```bash
radiomanager-cli playlistPostMerge
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **playlistMergeBody** | [**PlaylistMergeBody**](PlaylistMergeBody.md) | Data *(Required)* |

### Return type

[**InlineResponse2021**](InlineResponse2021.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## playlistPostStructure

Post a playlist, keep current structure

Post a playlist for a block. Existing Items can referenced by external_id. When Items are moved, this function **will attempt to** keep Items' ModelType structure in rundown.

### Example

```bash
radiomanager-cli playlistPostStructure
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **playlistStructureBody** | [**PlaylistStructureBody**](PlaylistStructureBody.md) | Data *(Required)* |

### Return type

[**InlineResponse2021**](InlineResponse2021.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## playlistPostTiming

Post a playlist

Post a playlist for a block. Existing Items can referenced by external_id. When Items are moved, this function **will not** keep Items' ModelType structure in rundown.

### Example

```bash
radiomanager-cli playlistPostTiming
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **playlistTimingBody** | [**PlaylistTimingBody**](PlaylistTimingBody.md) | Data *(Required)* |

### Return type

[**InlineResponse2021**](InlineResponse2021.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## stopCurrentItem

Stop an Item

Set a current playing or specific item on played

### Example

```bash
radiomanager-cli stopCurrentItem
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **itemsStopcurrentBody** | [**ItemsStopcurrentBody**](ItemsStopcurrentBody.md) | Data *(Optional)* | [optional]

### Return type

[**InlineResponse202**](InlineResponse202.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## updateItemById

Update extended item details by ID.

Update item by id.

### Example

```bash
radiomanager-cli updateItemById id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of Item **(Required)** | [default to null]
 **itemDataInput** | [**ItemDataInput**](ItemDataInput.md) | Data *(Optional)* |

### Return type

[**InlineResponse202**](InlineResponse202.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


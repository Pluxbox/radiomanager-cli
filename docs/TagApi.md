# TagApi

All URIs are relative to */api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createTag**](TagApi.md#createTag) | **POST** /tags | Create tag.
[**deleteTagById**](TagApi.md#deleteTagById) | **DELETE** /tags/{id} | Delete tag by id
[**getTagById**](TagApi.md#getTagById) | **GET** /tags/{id} | Get tags by id
[**listTags**](TagApi.md#listTags) | **GET** /tags | Get a list of all the tags currently in your station.
[**updateTagByID**](TagApi.md#updateTagByID) | **PATCH** /tags/{id} | Update tag by id



## createTag

Create tag.

Create tag.

### Example

```bash
radiomanager-cli createTag
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tagDataInput** | [**TagDataInput**](TagDataInput.md) | Data **(Required)** |

### Return type

[**InlineResponse2002**](InlineResponse2002.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## deleteTagById

Delete tag by id

Delete tag by id

### Example

```bash
radiomanager-cli deleteTagById id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of Tag **(Required)** | [default to null]

### Return type

[**InlineResponse202**](InlineResponse202.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getTagById

Get tags by id

Get tags by id

### Example

```bash
radiomanager-cli getTagById id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of Tag **(Required)** | [default to null]

### Return type

[**TagResult**](TagResult.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## listTags

Get a list of all the tags currently in your station.

Get a list of all the tags currently in your station. This feature supports pagination and will give a maximum results of 50 tags back.

### Example

```bash
radiomanager-cli listTags  program_id=value  item_id=value  broadcast_id=value  contact_id=value  page=value  limit=value  order-by=value  order-direction=value  _external_station_id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **programId** | **integer** | Search on Program ID *(Optional)* '(Relation)' | [optional] [default to null]
 **itemId** | **integer** | Search on Item ID *(Optional)* '(Relation)' | [optional] [default to null]
 **broadcastId** | **integer** | Search on Broadcast ID *(Optional)* '(Relation)' | [optional] [default to null]
 **contactId** | **integer** | Search on Contact ID *(Optional)* '(Relation)' | [optional] [default to null]
 **page** | **integer** | Current page *(Optional)* | [optional] [default to 1]
 **limit** | **integer** | Results per page *(Optional)* | [optional] [default to null]
 **orderBy** | **string** | Field to order the results *(Optional)* | [optional] [default to null]
 **orderDirection** | **string** | Direction of ordering *(Optional)* | [optional] [default to null]
 **externalStationId** | **integer** | Query on a different (content providing) station *(Optional)* | [optional] [default to null]

### Return type

[**InlineResponse20012**](InlineResponse20012.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## updateTagByID

Update tag by id

Update tag by id

### Example

```bash
radiomanager-cli updateTagByID id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of Tag **(Required)** | [default to null]
 **tagDataInput** | [**TagDataInput**](TagDataInput.md) | Data *(Optional)* |

### Return type

[**InlineResponse202**](InlineResponse202.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


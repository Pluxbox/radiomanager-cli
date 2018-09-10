# StoryApi

All URIs are relative to */api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createStory**](StoryApi.md#createStory) | **POST** /stories | Create story.
[**deleteStoryById**](StoryApi.md#deleteStoryById) | **DELETE** /stories/{id} | Delete story by id
[**getStoryById**](StoryApi.md#getStoryById) | **GET** /stories/{id} | Get story by id
[**listStories**](StoryApi.md#listStories) | **GET** /stories | Get all stories.
[**updateStoryByID**](StoryApi.md#updateStoryByID) | **PATCH** /stories/{id} | Update story by id


## **createStory**

Create story.

Create story.

### Example
```bash
radiomanager-cli createStory
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **data** | [**StoryDataInput**](StoryDataInput.md) | Data **(Required)** |

### Return type

[**PostSuccess**](PostSuccess.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **deleteStoryById**

Delete story by id

Delete story by id

### Example
```bash
radiomanager-cli deleteStoryById id=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of Story **(Required)** |

### Return type

[**Success**](Success.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **getStoryById**

Get story by id

Get story by id

### Example
```bash
radiomanager-cli getStoryById id=value  _external_station_id=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of Story **(Required)** |
 **externalStationId** | **integer** | Query on a different (content providing) station *(Optional)* | [optional]

### Return type

[**StoryResult**](StoryResult.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **listStories**

Get all stories.

List all stories.

### Example
```bash
radiomanager-cli listStories  page=value  item_id=value  model_type_id=value  tag_id=value  limit=value  order-by=value  order-direction=value  _external_station_id=value
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

[**StoryResults**](StoryResults.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **updateStoryByID**

Update story by id

Update story by id

### Example
```bash
radiomanager-cli updateStoryByID id=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of Story **(Required)** |
 **data** | [**StoryDataInput**](StoryDataInput.md) | Data *(Optional)* | [optional]

### Return type

[**Success**](Success.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


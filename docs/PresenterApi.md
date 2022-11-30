# PresenterApi

All URIs are relative to */api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createPresenter**](PresenterApi.md#createPresenter) | **POST** /presenters | Create presenter.
[**deletePresenterById**](PresenterApi.md#deletePresenterById) | **DELETE** /presenters/{id} | Delete presenter by id
[**getPresenterById**](PresenterApi.md#getPresenterById) | **GET** /presenters/{id} | Get presenter by id
[**listPresenters**](PresenterApi.md#listPresenters) | **GET** /presenters | Get all presenters.
[**updatePresenterByID**](PresenterApi.md#updatePresenterByID) | **PATCH** /presenters/{id} | Update presenter by id



## createPresenter

Create presenter.

Create presenter.

### Example

```bash
radiomanager-cli createPresenter
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **presenterDataInput** | [**PresenterDataInput**](PresenterDataInput.md) | Data **(Required)** |

### Return type

[**InlineResponse2002**](InlineResponse2002.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## deletePresenterById

Delete presenter by id

Delete presenter by id

### Example

```bash
radiomanager-cli deletePresenterById id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | id of presenter | [default to null]

### Return type

[**InlineResponse202**](InlineResponse202.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getPresenterById

Get presenter by id

Get presenter by id

### Example

```bash
radiomanager-cli getPresenterById id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | id of Presenter | [default to null]

### Return type

[**PresenterResult**](PresenterResult.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## listPresenters

Get all presenters.

List all presenters.

### Example

```bash
radiomanager-cli listPresenters  program_id=value  broadcast_id=value  model_type_id=value  page=value  limit=value  order-by=value  order-direction=value  _external_station_id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **programId** | **integer** | Search on Program ID *(Optional)* '(Relation)' | [optional] [default to null]
 **broadcastId** | **integer** | Search on Broadcast ID *(Optional)* '(Relation)' | [optional] [default to null]
 **modelTypeId** | **integer** | Search on ModelType ID (Optional) | [optional] [default to null]
 **page** | **integer** | Current page *(Optional)* | [optional] [default to 1]
 **limit** | **integer** | Results per page *(Optional)* | [optional] [default to null]
 **orderBy** | **string** | Field to order the results *(Optional)* | [optional] [default to null]
 **orderDirection** | **string** | Direction of ordering *(Optional)* | [optional] [default to null]
 **externalStationId** | **integer** | Query on a different (content providing) station *(Optional)* | [optional] [default to null]

### Return type

[**InlineResponse20010**](InlineResponse20010.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## updatePresenterByID

Update presenter by id

Update presenter by id

### Example

```bash
radiomanager-cli updatePresenterByID id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | id of Presenter | [default to null]
 **presenterDataInput** | [**PresenterDataInput**](PresenterDataInput.md) | Data *(Optional)* |

### Return type

[**InlineResponse202**](InlineResponse202.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


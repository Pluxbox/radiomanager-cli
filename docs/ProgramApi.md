# ProgramApi

All URIs are relative to */api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createProgram**](ProgramApi.md#createProgram) | **POST** /programs | Create program.
[**deleteProgramById**](ProgramApi.md#deleteProgramById) | **DELETE** /programs/{id} | Delete program by id
[**getProgramById**](ProgramApi.md#getProgramById) | **GET** /programs/{id} | Get program by id
[**listPrograms**](ProgramApi.md#listPrograms) | **GET** /programs | Get all programs.
[**updateProgramByID**](ProgramApi.md#updateProgramByID) | **PATCH** /programs/{id} | Update program by id



## createProgram

Create program.

Create program.

### Example

```bash
radiomanager-cli createProgram
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **programDataInput** | [**ProgramDataInput**](ProgramDataInput.md) | Data **(Required)** |

### Return type

[**InlineResponse2002**](InlineResponse2002.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## deleteProgramById

Delete program by id

Delete program by id

### Example

```bash
radiomanager-cli deleteProgramById id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of program **(Required)** | [default to null]

### Return type

[**InlineResponse202**](InlineResponse202.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getProgramById

Get program by id

Get program by id

### Example

```bash
radiomanager-cli getProgramById id=value  _external_station_id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of Program **(Required)** | [default to null]
 **externalStationId** | **integer** | Query on a different (content providing) station *(Optional)* | [optional] [default to null]

### Return type

[**ProgramResult**](ProgramResult.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## listPrograms

Get all programs.

List all programs.

### Example

```bash
radiomanager-cli listPrograms  broadcast_id=value  model_type_id=value  tag_id=value  presenter_id=value  genre_id=value  group_id=value  block_id=value  item_id=value  disabled=value  page=value  limit=value  order-by=value  order-direction=value  _external_station_id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **broadcastId** | **integer** | Search on Broadcast ID *(Optional)* '(Relation)' | [optional] [default to null]
 **modelTypeId** | **integer** | Search on ModelType ID *(Optional)* '(Relation)' | [optional] [default to null]
 **tagId** | **integer** | Search on Tag ID *(Optional)* '(Relation)' | [optional] [default to null]
 **presenterId** | **integer** | Search on Presenter ID *(Optional)* '(Relation)' | [optional] [default to null]
 **genreId** | **integer** | Search on Genre ID *(Optional)* | [optional] [default to null]
 **groupId** | **integer** | Search on Group ID *(Optional)* | [optional] [default to null]
 **blockId** | **integer** | Search on Block ID *(Optional)* '(Relation)' | [optional] [default to null]
 **itemId** | **integer** | Search on Item ID *(Optional)* '(Relation)' | [optional] [default to null]
 **disabled** | **integer** | Search on Disabled status *(Optional)* | [optional] [default to null]
 **page** | **integer** | Current page *(Optional)* | [optional] [default to 1]
 **limit** | **integer** | Results per page *(Optional)* | [optional] [default to null]
 **orderBy** | **string** | Field to order the results *(Optional)* | [optional] [default to null]
 **orderDirection** | **string** | Direction of ordering *(Optional)* | [optional] [default to null]
 **externalStationId** | **integer** | Query on a different (content providing) station *(Optional)* | [optional] [default to null]

### Return type

[**InlineResponse20011**](InlineResponse20011.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## updateProgramByID

Update program by id

Update program by id

### Example

```bash
radiomanager-cli updateProgramByID id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of Program **(Required)** | [default to null]
 **programDataInput** | [**ProgramDataInput**](ProgramDataInput.md) | Data *(Optional)* |

### Return type

[**InlineResponse202**](InlineResponse202.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


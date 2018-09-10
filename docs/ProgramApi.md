# ProgramApi

All URIs are relative to */api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createProgram**](ProgramApi.md#createProgram) | **POST** /programs | Create program.
[**deleteProgramById**](ProgramApi.md#deleteProgramById) | **DELETE** /programs/{id} | Delete program by id
[**getProgramById**](ProgramApi.md#getProgramById) | **GET** /programs/{id} | Get program by id
[**listPrograms**](ProgramApi.md#listPrograms) | **GET** /programs | Get all programs.
[**updateProgramByID**](ProgramApi.md#updateProgramByID) | **PATCH** /programs/{id} | Update program by id


## **createProgram**

Create program.

Create program.

### Example
```bash
radiomanager-cli createProgram
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **data** | [**ProgramDataInput**](ProgramDataInput.md) | Data **(Required)** |

### Return type

[**PostSuccess**](PostSuccess.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **deleteProgramById**

Delete program by id

Delete program by id

### Example
```bash
radiomanager-cli deleteProgramById id=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of program **(Required)** |

### Return type

[**Success**](Success.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **getProgramById**

Get program by id

Get program by id

### Example
```bash
radiomanager-cli getProgramById id=value  _external_station_id=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of Program **(Required)** |
 **externalStationId** | **integer** | Query on a different (content providing) station *(Optional)* | [optional]

### Return type

[**ProgramResult**](ProgramResult.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **listPrograms**

Get all programs.

List all programs.

### Example
```bash
radiomanager-cli listPrograms  page=value  broadcast_id=value  model_type_id=value  tag_id=value  presenter_id=value  genre_id=value  block_id=value  item_id=value  limit=value  order-by=value  order-direction=value  _external_station_id=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **integer** | Current page *(Optional)* | [optional]
 **broadcastId** | **integer** | Search on Broadcast ID *(Optional)* '(Relation)' | [optional]
 **modelTypeId** | **integer** | Search on ModelType ID *(Optional)* '(Relation)' | [optional]
 **tagId** | **integer** | Search on Tag ID *(Optional)* '(Relation)' | [optional]
 **presenterId** | **integer** | Search on Presenter ID *(Optional)* '(Relation)' | [optional]
 **genreId** | **integer** | Search on Genre ID *(Optional)* | [optional]
 **blockId** | **integer** | Search on Block ID *(Optional)* '(Relation)' | [optional]
 **itemId** | **integer** | Search on Item ID *(Optional)* '(Relation)' | [optional]
 **limit** | **integer** | Results per page *(Optional)* | [optional]
 **orderBy** | **string** | Field to order the results *(Optional)* | [optional]
 **orderDirection** | **string** | Direction of ordering *(Optional)* | [optional]
 **externalStationId** | **integer** | Query on a different (content providing) station *(Optional)* | [optional]

### Return type

[**ProgramResults**](ProgramResults.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

## **updateProgramByID**

Update program by id

Update program by id

### Example
```bash
radiomanager-cli updateProgramByID id=value
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of Program **(Required)** |
 **data** | [**ProgramDataInput**](ProgramDataInput.md) | Data *(Optional)* | [optional]

### Return type

[**Success**](Success.md)

### Authorization

[API Key](../README.md#API Key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


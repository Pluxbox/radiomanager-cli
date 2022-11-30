# CampaignApi

All URIs are relative to */api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createCampaign**](CampaignApi.md#createCampaign) | **POST** /campaigns | Create campaign.
[**deleteCampaignById**](CampaignApi.md#deleteCampaignById) | **DELETE** /campaigns/{id} | Delete campaign by id
[**getCampaignById**](CampaignApi.md#getCampaignById) | **GET** /campaigns/{id} | Get campaign by id
[**listCampaigns**](CampaignApi.md#listCampaigns) | **GET** /campaigns | Get all campaigns.
[**updateCampaignByID**](CampaignApi.md#updateCampaignByID) | **PATCH** /campaigns/{id} | Update campaign by id



## createCampaign

Create campaign.

Create campaign.

### Example

```bash
radiomanager-cli createCampaign
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **campaignDataInput** | [**CampaignDataInput**](CampaignDataInput.md) | Data **(Required)** |

### Return type

[**InlineResponse2002**](InlineResponse2002.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## deleteCampaignById

Delete campaign by id

Delete campaign by id

### Example

```bash
radiomanager-cli deleteCampaignById id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of Campaign **(Required)** | [default to null]

### Return type

[**InlineResponse202**](InlineResponse202.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getCampaignById

Get campaign by id

Get campaign by id

### Example

```bash
radiomanager-cli getCampaignById id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of Campaign **(Required)** | [default to null]

### Return type

[**CampaignResult**](CampaignResult.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## listCampaigns

Get all campaigns.

List all campaigns.

### Example

```bash
radiomanager-cli listCampaigns  item_id=value  model_type_id=value  start-min=value  start-max=value  page=value  limit=value  order-by=value  order-direction=value  _external_station_id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **itemId** | **integer** | Search on Item ID *(Optional)* '(Relation)' | [optional] [default to null]
 **modelTypeId** | **integer** | Search on ModelType ID *(Optional)* '(Relation)' | [optional] [default to null]
 **startMin** | **string** | Minimum start date *(Optional)* | [optional] [default to null]
 **startMax** | **string** | Maximum start date *(Optional)* | [optional] [default to null]
 **page** | **integer** | Current page *(Optional)* | [optional] [default to 1]
 **limit** | **integer** | Results per page *(Optional)* | [optional] [default to null]
 **orderBy** | **string** | Field to order the results *(Optional)* | [optional] [default to null]
 **orderDirection** | **string** | Direction of ordering *(Optional)* | [optional] [default to null]
 **externalStationId** | **integer** | Query on a different (content providing) station *(Optional)* | [optional] [default to null]

### Return type

[**InlineResponse2004**](InlineResponse2004.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## updateCampaignByID

Update campaign by id

Update campaign by id

### Example

```bash
radiomanager-cli updateCampaignByID id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of Campaign **(Required)** | [default to null]
 **campaignDataInput** | [**CampaignDataInput**](CampaignDataInput.md) | Data **(Optional)** |

### Return type

[**InlineResponse202**](InlineResponse202.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


# UserApi

All URIs are relative to */api/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteUserById**](UserApi.md#deleteUserById) | **DELETE** /users/{id} | Remove User from station by Id
[**getUserById**](UserApi.md#getUserById) | **GET** /users/{id} | Get user by id
[**inviteUserByMail**](UserApi.md#inviteUserByMail) | **POST** /users/invite | Invite user by mail
[**listUsers**](UserApi.md#listUsers) | **GET** /users | Get all users.



## deleteUserById

Remove User from station by Id

Remove User from station by Id, will not actually delete a User record

### Example

```bash
radiomanager-cli deleteUserById id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | ID of User **(Required)** | [default to null]

### Return type

[**InlineResponse202**](InlineResponse202.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## getUserById

Get user by id

Get user by id

### Example

```bash
radiomanager-cli getUserById id=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **integer** | id of User | [default to null]

### Return type

[**UserResult**](UserResult.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## inviteUserByMail

Invite user by mail

Invite user by mail

### Example

```bash
radiomanager-cli inviteUserByMail
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inviteUserData** | [**InviteUserData**](InviteUserData.md) | Data *(Required)* |

### Return type

[**InlineResponse202**](InlineResponse202.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## listUsers

Get all users.

List all users.

### Example

```bash
radiomanager-cli listUsers  role_id=value  group_id=value  page=value  limit=value  order-by=value  order-direction=value
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **roleId** | **integer** | Search on Role ID *(Optional)* | [optional] [default to null]
 **groupId** | **integer** | Search on Group ID *(Optional)* | [optional] [default to null]
 **page** | **integer** | Current page *(Optional)* | [optional] [default to 1]
 **limit** | **integer** | Results per page *(Optional)* | [optional] [default to null]
 **orderBy** | **string** | Field to order the results *(Optional)* | [optional] [default to null]
 **orderDirection** | **string** | Direction of ordering *(Optional)* | [optional] [default to null]

### Return type

[**InlineResponse20013**](InlineResponse20013.md)

### Authorization

[API-Key](../README.md#API-Key)

### HTTP request headers

- **Content-Type**: Not Applicable
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


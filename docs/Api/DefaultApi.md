# EpicKitty\Ras\DefaultApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**chatRoomPrivateGet()**](DefaultApi.md#chatRoomPrivateGet) | **GET** /chat/room/private | List all private AIM chat rooms |
| [**chatRoomPublicGet()**](DefaultApi.md#chatRoomPublicGet) | **GET** /chat/room/public | List all public AIM chat rooms |
| [**chatRoomPublicPost()**](DefaultApi.md#chatRoomPublicPost) | **POST** /chat/room/public | Create a new public chat room |
| [**directoryCategoryGet()**](DefaultApi.md#directoryCategoryGet) | **GET** /directory/category | Get all keyword categories |
| [**directoryCategoryIdDelete()**](DefaultApi.md#directoryCategoryIdDelete) | **DELETE** /directory/category/{id} | Delete a keyword category |
| [**directoryCategoryIdKeywordGet()**](DefaultApi.md#directoryCategoryIdKeywordGet) | **GET** /directory/category/{id}/keyword | Get all keywords in a category |
| [**directoryCategoryPost()**](DefaultApi.md#directoryCategoryPost) | **POST** /directory/category | Create a new keyword category |
| [**directoryKeywordIdDelete()**](DefaultApi.md#directoryKeywordIdDelete) | **DELETE** /directory/keyword/{id} | Delete a keyword |
| [**directoryKeywordPost()**](DefaultApi.md#directoryKeywordPost) | **POST** /directory/keyword | Create a new keyword. |
| [**instantMessagePost()**](DefaultApi.md#instantMessagePost) | **POST** /instant-message | Send an instant message |
| [**sessionGet()**](DefaultApi.md#sessionGet) | **GET** /session | Get active sessions |
| [**sessionScreennameDelete()**](DefaultApi.md#sessionScreennameDelete) | **DELETE** /session/{screenname} | Delete active sessions for a given screen name or UIN. |
| [**sessionScreennameGet()**](DefaultApi.md#sessionScreennameGet) | **GET** /session/{screenname} | Get active sessions for a given screen name or UIN. |
| [**userDelete()**](DefaultApi.md#userDelete) | **DELETE** /user | Delete a user |
| [**userGet()**](DefaultApi.md#userGet) | **GET** /user | Get all users |
| [**userPasswordPut()**](DefaultApi.md#userPasswordPut) | **PUT** /user/password | Set a user&#39;s password |
| [**userPost()**](DefaultApi.md#userPost) | **POST** /user | Create a new user |
| [**userScreennameAccountGet()**](DefaultApi.md#userScreennameAccountGet) | **GET** /user/{screenname}/account | Get account details for a specific screen name. |
| [**userScreennameAccountPatch()**](DefaultApi.md#userScreennameAccountPatch) | **PATCH** /user/{screenname}/account | Update a user account |
| [**userScreennameIconGet()**](DefaultApi.md#userScreennameIconGet) | **GET** /user/{screenname}/icon | Get AIM buddy icon for a screen name |
| [**versionGet()**](DefaultApi.md#versionGet) | **GET** /version | Get build information of RAS. |


## `chatRoomPrivateGet()`

```php
chatRoomPrivateGet(): \EpicKitty\Ras\Model\ChatRoomPrivateGet200ResponseInner[]
```

List all private AIM chat rooms

Retrieve a list of all private AIM chat rooms in exchange 4.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EpicKitty\Ras\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->chatRoomPrivateGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->chatRoomPrivateGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\EpicKitty\Ras\Model\ChatRoomPrivateGet200ResponseInner[]**](../Model/ChatRoomPrivateGet200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `chatRoomPublicGet()`

```php
chatRoomPublicGet(): \EpicKitty\Ras\Model\ChatRoomPublicGet200ResponseInner[]
```

List all public AIM chat rooms

Retrieve a list of all public AIM chat rooms in exchange 5.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EpicKitty\Ras\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->chatRoomPublicGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->chatRoomPublicGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\EpicKitty\Ras\Model\ChatRoomPublicGet200ResponseInner[]**](../Model/ChatRoomPublicGet200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `chatRoomPublicPost()`

```php
chatRoomPublicPost($chatRoomPublicPostRequest)
```

Create a new public chat room

Create a new public chat room in exchange 5.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EpicKitty\Ras\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$chatRoomPublicPostRequest = new \EpicKitty\Ras\Model\ChatRoomPublicPostRequest(); // \EpicKitty\Ras\Model\ChatRoomPublicPostRequest

try {
    $apiInstance->chatRoomPublicPost($chatRoomPublicPostRequest);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->chatRoomPublicPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **chatRoomPublicPostRequest** | [**\EpicKitty\Ras\Model\ChatRoomPublicPostRequest**](../Model/ChatRoomPublicPostRequest.md)|  | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryCategoryGet()`

```php
directoryCategoryGet(): \EpicKitty\Ras\Model\DirectoryCategoryGet200ResponseInner[]
```

Get all keyword categories

Retrieve a list of all keyword categories.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EpicKitty\Ras\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->directoryCategoryGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->directoryCategoryGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\EpicKitty\Ras\Model\DirectoryCategoryGet200ResponseInner[]**](../Model/DirectoryCategoryGet200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryCategoryIdDelete()`

```php
directoryCategoryIdDelete($id)
```

Delete a keyword category

Delete a keyword category specified by its ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EpicKitty\Ras\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 56; // int | The ID of the keyword category.

try {
    $apiInstance->directoryCategoryIdDelete($id);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->directoryCategoryIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| The ID of the keyword category. | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryCategoryIdKeywordGet()`

```php
directoryCategoryIdKeywordGet($id): \EpicKitty\Ras\Model\DirectoryCategoryIdKeywordGet200ResponseInner[]
```

Get all keywords in a category

Retrieve a list of all keywords in the specified category.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EpicKitty\Ras\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 56; // int | The ID of the keyword category.

try {
    $result = $apiInstance->directoryCategoryIdKeywordGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->directoryCategoryIdKeywordGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| The ID of the keyword category. | |

### Return type

[**\EpicKitty\Ras\Model\DirectoryCategoryIdKeywordGet200ResponseInner[]**](../Model/DirectoryCategoryIdKeywordGet200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryCategoryPost()`

```php
directoryCategoryPost($directoryCategoryPostRequest): \EpicKitty\Ras\Model\DirectoryCategoryPost201Response
```

Create a new keyword category

Create a new keyword category.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EpicKitty\Ras\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$directoryCategoryPostRequest = new \EpicKitty\Ras\Model\DirectoryCategoryPostRequest(); // \EpicKitty\Ras\Model\DirectoryCategoryPostRequest

try {
    $result = $apiInstance->directoryCategoryPost($directoryCategoryPostRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->directoryCategoryPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **directoryCategoryPostRequest** | [**\EpicKitty\Ras\Model\DirectoryCategoryPostRequest**](../Model/DirectoryCategoryPostRequest.md)|  | |

### Return type

[**\EpicKitty\Ras\Model\DirectoryCategoryPost201Response**](../Model/DirectoryCategoryPost201Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryKeywordIdDelete()`

```php
directoryKeywordIdDelete($id)
```

Delete a keyword

Delete a keyword specified by its ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EpicKitty\Ras\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 56; // int | The ID of the keyword.

try {
    $apiInstance->directoryKeywordIdDelete($id);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->directoryKeywordIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| The ID of the keyword. | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `directoryKeywordPost()`

```php
directoryKeywordPost($directoryKeywordPostRequest): \EpicKitty\Ras\Model\DirectoryKeywordPost201Response
```

Create a new keyword.

Create a new keyword in a category.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EpicKitty\Ras\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$directoryKeywordPostRequest = new \EpicKitty\Ras\Model\DirectoryKeywordPostRequest(); // \EpicKitty\Ras\Model\DirectoryKeywordPostRequest

try {
    $result = $apiInstance->directoryKeywordPost($directoryKeywordPostRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->directoryKeywordPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **directoryKeywordPostRequest** | [**\EpicKitty\Ras\Model\DirectoryKeywordPostRequest**](../Model/DirectoryKeywordPostRequest.md)|  | |

### Return type

[**\EpicKitty\Ras\Model\DirectoryKeywordPost201Response**](../Model/DirectoryKeywordPost201Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `instantMessagePost()`

```php
instantMessagePost($instantMessagePostRequest)
```

Send an instant message

Send an instant message from one user to another. No error is raised if the recipient does not exist or the user is offline. The sender screen name does not need to exist.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EpicKitty\Ras\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$instantMessagePostRequest = new \EpicKitty\Ras\Model\InstantMessagePostRequest(); // \EpicKitty\Ras\Model\InstantMessagePostRequest

try {
    $apiInstance->instantMessagePost($instantMessagePostRequest);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->instantMessagePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **instantMessagePostRequest** | [**\EpicKitty\Ras\Model\InstantMessagePostRequest**](../Model/InstantMessagePostRequest.md)|  | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `sessionGet()`

```php
sessionGet(): \EpicKitty\Ras\Model\SessionGet200Response
```

Get active sessions

Retrieve a list of active sessions of logged in users.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EpicKitty\Ras\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->sessionGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->sessionGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\EpicKitty\Ras\Model\SessionGet200Response**](../Model/SessionGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `sessionScreennameDelete()`

```php
sessionScreennameDelete($screenname)
```

Delete active sessions for a given screen name or UIN.

Disconnect any active sessions of a specific logged in user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EpicKitty\Ras\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$screenname = 'screenname_example'; // string | User's AIM screen name or ICQ UIN.

try {
    $apiInstance->sessionScreennameDelete($screenname);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->sessionScreennameDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **screenname** | **string**| User&#39;s AIM screen name or ICQ UIN. | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `sessionScreennameGet()`

```php
sessionScreennameGet($screenname): \EpicKitty\Ras\Model\SessionGet200Response
```

Get active sessions for a given screen name or UIN.

Retrieve a list of active sessions of a specific logged in user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EpicKitty\Ras\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$screenname = 'screenname_example'; // string | User's AIM screen name or ICQ UIN.

try {
    $result = $apiInstance->sessionScreennameGet($screenname);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->sessionScreennameGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **screenname** | **string**| User&#39;s AIM screen name or ICQ UIN. | |

### Return type

[**\EpicKitty\Ras\Model\SessionGet200Response**](../Model/SessionGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `userDelete()`

```php
userDelete($userDeleteRequest)
```

Delete a user

Delete a user account specified by their screen name.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EpicKitty\Ras\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$userDeleteRequest = new \EpicKitty\Ras\Model\UserDeleteRequest(); // \EpicKitty\Ras\Model\UserDeleteRequest

try {
    $apiInstance->userDelete($userDeleteRequest);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->userDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **userDeleteRequest** | [**\EpicKitty\Ras\Model\UserDeleteRequest**](../Model/UserDeleteRequest.md)|  | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `userGet()`

```php
userGet(): \EpicKitty\Ras\Model\UserGet200ResponseInner[]
```

Get all users

Retrieve a list of all user accounts.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EpicKitty\Ras\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->userGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->userGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\EpicKitty\Ras\Model\UserGet200ResponseInner[]**](../Model/UserGet200ResponseInner.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `userPasswordPut()`

```php
userPasswordPut($userPasswordPutRequest)
```

Set a user's password

Update the password for a user specified by their screen name or ICQ UIN.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EpicKitty\Ras\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$userPasswordPutRequest = new \EpicKitty\Ras\Model\UserPasswordPutRequest(); // \EpicKitty\Ras\Model\UserPasswordPutRequest

try {
    $apiInstance->userPasswordPut($userPasswordPutRequest);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->userPasswordPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **userPasswordPutRequest** | [**\EpicKitty\Ras\Model\UserPasswordPutRequest**](../Model/UserPasswordPutRequest.md)|  | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `userPost()`

```php
userPost($userPostRequest)
```

Create a new user

Create a new AIM or ICQ user account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EpicKitty\Ras\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$userPostRequest = new \EpicKitty\Ras\Model\UserPostRequest(); // \EpicKitty\Ras\Model\UserPostRequest

try {
    $apiInstance->userPost($userPostRequest);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->userPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **userPostRequest** | [**\EpicKitty\Ras\Model\UserPostRequest**](../Model/UserPostRequest.md)|  | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `userScreennameAccountGet()`

```php
userScreennameAccountGet($screenname): \EpicKitty\Ras\Model\UserScreennameAccountGet200Response
```

Get account details for a specific screen name.

Retrieve account details for a specific screen name.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EpicKitty\Ras\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$screenname = 'screenname_example'; // string | User's AIM screen name or ICQ UIN.

try {
    $result = $apiInstance->userScreennameAccountGet($screenname);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->userScreennameAccountGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **screenname** | **string**| User&#39;s AIM screen name or ICQ UIN. | |

### Return type

[**\EpicKitty\Ras\Model\UserScreennameAccountGet200Response**](../Model/UserScreennameAccountGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `userScreennameAccountPatch()`

```php
userScreennameAccountPatch($screenname, $userScreennameAccountPatchRequest)
```

Update a user account

Update attributes for a user account

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EpicKitty\Ras\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$screenname = 'screenname_example'; // string | User's AIM screen name or ICQ UIN.
$userScreennameAccountPatchRequest = new \EpicKitty\Ras\Model\UserScreennameAccountPatchRequest(); // \EpicKitty\Ras\Model\UserScreennameAccountPatchRequest

try {
    $apiInstance->userScreennameAccountPatch($screenname, $userScreennameAccountPatchRequest);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->userScreennameAccountPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **screenname** | **string**| User&#39;s AIM screen name or ICQ UIN. | |
| **userScreennameAccountPatchRequest** | [**\EpicKitty\Ras\Model\UserScreennameAccountPatchRequest**](../Model/UserScreennameAccountPatchRequest.md)|  | |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `userScreennameIconGet()`

```php
userScreennameIconGet($screenname): \SplFileObject
```

Get AIM buddy icon for a screen name

Retrieve account buddy icon for a specific screen name.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EpicKitty\Ras\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$screenname = 'screenname_example'; // string | User's AIM screen name or ICQ UIN.

try {
    $result = $apiInstance->userScreennameIconGet($screenname);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->userScreennameIconGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **screenname** | **string**| User&#39;s AIM screen name or ICQ UIN. | |

### Return type

**\SplFileObject**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `image/gif`, `image/jpeg`, `image/png`, `application/octet-stream`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `versionGet()`

```php
versionGet(): \EpicKitty\Ras\Model\VersionGet200Response
```

Get build information of RAS.

Retrieve the build version, git commit, and build date of the running RAS binary.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new EpicKitty\Ras\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->versionGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->versionGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\EpicKitty\Ras\Model\VersionGet200Response**](../Model/VersionGet200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

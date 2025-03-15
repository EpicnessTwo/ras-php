# RAS-PHP

API that provides management functionality for Retro AIM Server operators.


## Installation & Usage

### Requirements

PHP 8.1 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/epicnesstwo/ras-php.git"
    }
  ],
  "require": {
    "epicnesstwo/ras-php": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/RAS-PHP/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DefaultApi* | [**chatRoomPrivateGet**](docs/Api/DefaultApi.md#chatroomprivateget) | **GET** /chat/room/private | List all private AIM chat rooms
*DefaultApi* | [**chatRoomPublicGet**](docs/Api/DefaultApi.md#chatroompublicget) | **GET** /chat/room/public | List all public AIM chat rooms
*DefaultApi* | [**chatRoomPublicPost**](docs/Api/DefaultApi.md#chatroompublicpost) | **POST** /chat/room/public | Create a new public chat room
*DefaultApi* | [**directoryCategoryGet**](docs/Api/DefaultApi.md#directorycategoryget) | **GET** /directory/category | Get all keyword categories
*DefaultApi* | [**directoryCategoryIdDelete**](docs/Api/DefaultApi.md#directorycategoryiddelete) | **DELETE** /directory/category/{id} | Delete a keyword category
*DefaultApi* | [**directoryCategoryIdKeywordGet**](docs/Api/DefaultApi.md#directorycategoryidkeywordget) | **GET** /directory/category/{id}/keyword | Get all keywords in a category
*DefaultApi* | [**directoryCategoryPost**](docs/Api/DefaultApi.md#directorycategorypost) | **POST** /directory/category | Create a new keyword category
*DefaultApi* | [**directoryKeywordIdDelete**](docs/Api/DefaultApi.md#directorykeywordiddelete) | **DELETE** /directory/keyword/{id} | Delete a keyword
*DefaultApi* | [**directoryKeywordPost**](docs/Api/DefaultApi.md#directorykeywordpost) | **POST** /directory/keyword | Create a new keyword.
*DefaultApi* | [**instantMessagePost**](docs/Api/DefaultApi.md#instantmessagepost) | **POST** /instant-message | Send an instant message
*DefaultApi* | [**sessionGet**](docs/Api/DefaultApi.md#sessionget) | **GET** /session | Get active sessions
*DefaultApi* | [**sessionScreennameDelete**](docs/Api/DefaultApi.md#sessionscreennamedelete) | **DELETE** /session/{screenname} | Delete active sessions for a given screen name or UIN.
*DefaultApi* | [**sessionScreennameGet**](docs/Api/DefaultApi.md#sessionscreennameget) | **GET** /session/{screenname} | Get active sessions for a given screen name or UIN.
*DefaultApi* | [**userDelete**](docs/Api/DefaultApi.md#userdelete) | **DELETE** /user | Delete a user
*DefaultApi* | [**userGet**](docs/Api/DefaultApi.md#userget) | **GET** /user | Get all users
*DefaultApi* | [**userPasswordPut**](docs/Api/DefaultApi.md#userpasswordput) | **PUT** /user/password | Set a user&#39;s password
*DefaultApi* | [**userPost**](docs/Api/DefaultApi.md#userpost) | **POST** /user | Create a new user
*DefaultApi* | [**userScreennameAccountGet**](docs/Api/DefaultApi.md#userscreennameaccountget) | **GET** /user/{screenname}/account | Get account details for a specific screen name.
*DefaultApi* | [**userScreennameAccountPatch**](docs/Api/DefaultApi.md#userscreennameaccountpatch) | **PATCH** /user/{screenname}/account | Update a user account
*DefaultApi* | [**userScreennameIconGet**](docs/Api/DefaultApi.md#userscreennameiconget) | **GET** /user/{screenname}/icon | Get AIM buddy icon for a screen name
*DefaultApi* | [**versionGet**](docs/Api/DefaultApi.md#versionget) | **GET** /version | Get build information of RAS.

## Models

- [ChatRoomPrivateGet200ResponseInner](docs/Model/ChatRoomPrivateGet200ResponseInner.md)
- [ChatRoomPublicGet200ResponseInner](docs/Model/ChatRoomPublicGet200ResponseInner.md)
- [ChatRoomPublicGet200ResponseInnerParticipantsInner](docs/Model/ChatRoomPublicGet200ResponseInnerParticipantsInner.md)
- [ChatRoomPublicPostRequest](docs/Model/ChatRoomPublicPostRequest.md)
- [DirectoryCategoryGet200ResponseInner](docs/Model/DirectoryCategoryGet200ResponseInner.md)
- [DirectoryCategoryIdKeywordGet200ResponseInner](docs/Model/DirectoryCategoryIdKeywordGet200ResponseInner.md)
- [DirectoryCategoryPost201Response](docs/Model/DirectoryCategoryPost201Response.md)
- [DirectoryCategoryPost400Response](docs/Model/DirectoryCategoryPost400Response.md)
- [DirectoryCategoryPostRequest](docs/Model/DirectoryCategoryPostRequest.md)
- [DirectoryKeywordPost201Response](docs/Model/DirectoryKeywordPost201Response.md)
- [DirectoryKeywordPostRequest](docs/Model/DirectoryKeywordPostRequest.md)
- [InstantMessagePostRequest](docs/Model/InstantMessagePostRequest.md)
- [SessionGet200Response](docs/Model/SessionGet200Response.md)
- [SessionGet200ResponseSessionsInner](docs/Model/SessionGet200ResponseSessionsInner.md)
- [UserDeleteRequest](docs/Model/UserDeleteRequest.md)
- [UserGet200ResponseInner](docs/Model/UserGet200ResponseInner.md)
- [UserPasswordPutRequest](docs/Model/UserPasswordPutRequest.md)
- [UserPostRequest](docs/Model/UserPostRequest.md)
- [UserScreennameAccountGet200Response](docs/Model/UserScreennameAccountGet200Response.md)
- [UserScreennameAccountPatchRequest](docs/Model/UserScreennameAccountPatchRequest.md)
- [VersionGet200Response](docs/Model/VersionGet200Response.md)

## Authorization
All endpoints do not require authorization.
## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.0.0`
    - Package version: `0.15.3`
    - Generator version: `7.11.0-SNAPSHOT`
- Build package: `org.openapitools.codegen.languages.PhpNextgenClientCodegen`

# API

```csharp
APIController aPIController = client.APIController;
```

## Class Name

`APIController`

## Methods

* [Get Users](../../doc/controllers/api.md#get-users)
* [Create a New User](../../doc/controllers/api.md#create-a-new-user)


# Get Users

Returns a list of users, optionally filtered by search.

```csharp
GetUsersAsync(
    string search = null,
    int? limit = null)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `search` | `string` | Query, Optional | Filter users by search term |
| `limit` | `int?` | Query, Optional | Limit the number of users returned |

## Response Type

[`Task<List<Models.UsersResponse>>`](../../doc/models/users-response.md)

## Example Usage

```csharp
try
{
    List<UsersResponse> result = await aPIController.GetUsersAsync();
}
catch (ApiException e)
{
    // TODO: Handle exception here
    Console.WriteLine(e.Message);
}
```


# Create a New User

Creates a user with default values if not provided.

```csharp
CreateANewUserAsync(
    Models.UsersRequest body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`UsersRequest`](../../doc/models/users-request.md) | Body, Required | - |

## Response Type

[`Task<Models.UsersResponse1>`](../../doc/models/users-response-1.md)

## Example Usage

```csharp
UsersRequest body = new UsersRequest
{
    Username = "test",
    Rating = 0,
};

try
{
    UsersResponse1 result = await aPIController.CreateANewUserAsync(body);
}
catch (ApiException e)
{
    // TODO: Handle exception here
    Console.WriteLine(e.Message);
}
```


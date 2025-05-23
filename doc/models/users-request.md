
# Users Request

## Structure

`UsersRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Username` | `string` | Optional | User's username<br><br>**Default**: `"test"` |
| `Age` | `int?` | Optional | User's age |
| `IsActive` | `bool?` | Optional | Whether the user is active |
| `Rating` | `double?` | Optional | User's rating<br><br>**Default**: `0` |
| `SignupDate` | `DateTime?` | Optional | Signup date |

## Example (as JSON)

```json
{
  "username": "test",
  "rating": 0.0,
  "age": 82,
  "isActive": false,
  "signupDate": "2016-03-13"
}
```


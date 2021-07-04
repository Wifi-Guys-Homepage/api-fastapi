# Api Spec

| Endpoint | Verb | Parameters | Request Body | Response Body | Requires Auth | 
| --- | --- | --- | --- | --- | --- |
| /steam/{user_page} | GET | - | - | [Steam Get Response Body](#steam-get-response-body) | No |
| /user | POST | - | [User Post Request Body](#user-post-request-body) | [User Post Request Body](#user-post-response-body) | Yes |
| /user/{user_id} | GET | - |  - |  [User get Response Body](#user-get-response-body) | Yes |
| /user/{user_id} | PATCH | - | [User Patch Request Body](#user-patch-request-body) | [User Patch Response Body](#user-patch-response-body) | Yes |
| /user/{user_id} | DELETE | - | [User Delete Request Body](#user-delete-request-body) | [User Delete Response Body](#user-delete-response-body) | Yes |
| /appinfo | GET | - | - | [Appinfo Get Response Body](#appinfo-get-response-body) | No |
| /healthcheck | GET | - | - | [Healthcheck Get Response Body](#healthcheck-get-response-body) | No |
  
# Request Bodies

## User Post Request Body
```json
{
  "username": str,
  "password": str, 
  "email": str
}
```

## User Patch Request Body
```json
{
  "user_id": str
  "password": Optional[str],
  "email": Optional[str]
}
```

## User Delete Request Body
```json
{
  "user_id": str
}
```

# Response Bodies

## Steam Get Response Body
```json 
{
    "user_id": str,
    "current_game": str
}
```

## User Post Response Body 
```json
{
  "user_id": str,
  "username": str,
  "email": str
}
```

## User Get Response Body
```json
{
  "user_id": str,
  "username": str,
  "email": str
}
```

## User Patch Response Body
```json
{
  "user_id": str,
  "username": str,
  "email": str
}
```

## User Delete Response Body 
```json
{
  "user_id": str,
  "username": str
}
```

## Appinfo Get Response Body
```json
{
  "version": str,
  "git_branch": str,
  "code_hash": str,
  "build_time": str,
  "deploy_time": str
}
```

## Healthcheck Get Response Body
```json
{
  "status": "ok"
}
```
--- 

title: Yodaa 

language_tabs: 
  - shell
  - python
  - javascript

toc_footers: 
   - <a href='#'>Sign Up for a Developer Key</a> 
   - <a href='https://github.com/lavkumarv'>Documentation Powered by lav</a> 

includes: 
   - errors 

search: true 

--- 

# Introduction 

API documentation for Yodaa http://yodaa.club/ 

**Version:** 1.0.0 

# Authentication 

|apiKey|*API Key*|
|---|---| 

|oauth2|*OAuth 2.0*|
|---|---| 

# Get Active Batch
## ***GET*** 

**Summary:** fetches information for the active user batches

**Description:** 

### HTTP Request 
`GET /getactivebatch` 

**Responses**

| Code | Description |
| ---- | ----------- |
| default | 200 successful operation |

# Create new User
## ***POST*** 

**Summary:** Creates new User

**Description:** 

### HTTP Request 
`POST /users/` 

```shell
curl --location --request POST 'https://stagebeta5.com/api//users/' \
--header 'Content-Type: application/json' \
--data-raw '{
	"phone_number":"917471182501",
	"usertype":"parent"
}'
```

```python
import requests

url = "https://stagebeta5.com/api//users/"

payload = "{\n\t\"phone_number\":\"917471182501\",\n\t\"usertype\":\"parent\"\n}"
headers = {
  'Content-Type': 'application/json'
}

response = requests.request("POST", url, headers=headers, data = payload)

print(response.text.encode('utf8'))
```
```javascript
var myHeaders = new Headers();
myHeaders.append("Content-Type", "application/json");

var raw = JSON.stringify({"phone_number":"917471182501","usertype":"parent"});

var requestOptions = {
  method: 'POST',
  headers: myHeaders,
  body: raw,
  redirect: 'follow'
};

fetch("https://stagebeta5.com/api//users/", requestOptions)
  .then(response => response.text())
  .then(result => console.log(result))
  .catch(error => console.log('error', error));
```

```json
{
    "status": "success",
    "details": {
        "id": "NTM4",
        "cust_id": "YOD0000021A",
        "first_name": "",
        "last_name": "",
        "email": null,
        "instagram_handle": null,
        "snapchat_handle": null,
        "physical_card_order_status": null,
        "card_pin_set": false,
        "usertype": "parent",
        "phone_number": "917471182501",
        "father_name": null,
        "plan_status": null,
        "welcome_bonus": null,
        "invited_relationship": null,
        "gender": null,
        "physical_card_theme": null,
        "joining_status": "accepted",
        "prepaid_card_masked": null,
        "date_of_birth": null,
        "pan_card_number": null,
        "phone_verified": null,
        "email_verified": null,
        "biometric_preference": false,
        "firebase_ref_id": null,
        "user_image_url": null,
        "pin_code": null,
        "own_ref": null,
        "level": "",
        "nps_datetime": null,
        "ref_by_id": null,
        "kyc_status": null,
        "requested_datetime": null,
        "row_created": "2020-10-29T12:14:21.130626Z",
        "user_since": "2020-10-29T12:14:21.130626Z",
        "onboarding_state": null,
        "is_set_password": false
    }
}
```

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body | List of user object | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Successfully created User|
| 400 | Bad request|
| 500 | Internal server error|

# /USERS/{USERID}/
## ***PUT*** 

**Summary:** Verify phone OTP

**Description:** This can only be done by the logged in user.

### HTTP Request 
`***PUT*** /users/{userid}/` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| userid | path | name that need to be updated | Yes | string |
| body | body | Updated user object | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 400 | Invalid user supplied |
| 405 | Not Allowed |

## ***DELETE*** 

**Summary:** Delete user

**Description:** This can only be done by the logged in user.

### HTTP Request 
`***DELETE*** /users/{userid}/` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| userid | path | The name that needs to be deleted | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 400 | Invalid username supplied |
| 404 | User not found |

# /USER/LOGIN
## ***GET*** 

**Summary:** Logs user into the system

**Description:** 

### HTTP Request 
`***GET*** /user/login` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| username | query | The user name for login | Yes | string |
| password | query | The password for login in clear text | Yes | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid username/password supplied |

# /USER/LOGOUT
## ***GET*** 

**Summary:** Logs out current logged in user session

**Description:** 

### HTTP Request 
`***GET*** /user/logout` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |

**Responses**

| Code | Description |
| ---- | ----------- |
| default | successful operation |

# /USER
## ***POST*** 

**Summary:** Create user

**Description:** This can only be done by the logged in user.

### HTTP Request 
`***POST*** /user` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body | Created user object | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| default | successful operation |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->

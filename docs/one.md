FORMAT: 1A
HOST: http://localhost/api

# Sample API
テストですよ。  
2行目。

# Group ユーザ
ユーザ系

## 挨拶 [GET /hello]
テキストを返す

+ Response 200 (text/plain)
    + Body
        ```
        Hello World!
        ```


## ユーザ登録 [POST /users]
新規ユーザを登録する

+ Request (application/json)
    + Attributes
        + name: `ararenorimaki` (string, required) - ユーザ名
        + email: `arare@example.com` (string, required) - email
        + password: `hoge` (string, required) - パスワード

+ Response 200 (application/json)
    + Attributes
        + result: `true` (boolean) - 登録の成否
        + name: `arare` (string) - ユーザ名
        + emali: `arare@example.com` (string) - email
        + message: `User creation succeeded.` (string) - メッセージ


## トークン発行 [POST /login]
JWT認証用のトークンを発行する

+ Request (application/json)
    + Attributes
        + email: `arare@example.com` (string, required)
        + password: `hoge` (string, required)

+ Response 200 (application/json)
    + Attributes
        + access_token: `{token}` (string)
        + token_type: `bearer` (string)
        + expire_in: `60` (number) - 有効期限(分)

+ Response 401 (application/json)
    + Body
        ```
        {
            "error": "Unauthorized"
        }
        ```

## ユーザ情報取得 [GET /user]
自分自身のアカウント情報を取得する

+ Request
    + Headers
        ```
        Authorization: Bearer {token}
        ```

+ Response 200 (application/json)
    + Body
        ```
        {
            "id": 1,
            "name": "arare",
            "email": "arare@example.com",
            "email_verified_at": null,
            "created_at": "2019-05-29 11:12:13",
            "updated_at": "2019-05-29 11:12:13"
        }
        ```


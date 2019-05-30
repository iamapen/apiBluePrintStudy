## ユーザ一覧を取得する [GET /users/{userId}/{?offset,limit}{#var}]
+ Parameters
    + userId: 1 (number, required) - ユーザID
    + offset: 0 (number, optional) - offset
    + limit: 10 (number, optional) - limit

+ Request (application/json)
    + Attributes
        + firstName: Arare (string, required) - 名
        + lastName: Norimaki (string, required) - 姓

+ Request (application/xml)
    + Attributes
        + fullName: Arare Norimaki (string, required) - fullname

+ Response 200 (application/json)
    + Attributes (array[User]) 

+ Response 400


## Hoge [POST /hoge/{id}/{bbb}]
+ parameters
    + id (enum[string])

        Id of a Post

        + Members
            + A
            + B
            + C

    + bbb: `1001` (number, optional)
        + deault: 20
          
+ response 200


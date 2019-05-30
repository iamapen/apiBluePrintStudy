# Data Structures

#  User (object) - ユーザ
+ id: 1 (number, required) - ユーザID
+ firstName: Arare (string, required) - 名
+ lastName: Norimaki (string, required) - 姓
+ gender (Gender, required) - 性別
+ birthday (object, optional) - 生年月日
    + year: 1988 (number, required) - 西暦
    + month: 2 (number, required) - 月
    + day: 18 (number, required) - 日

# Gender (enum, fixed) - 性別
## Members
+ Male - 男性
+ Female - 女性


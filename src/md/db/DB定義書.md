# DB定義書
## ER図
[ER図はこちら](https://github.com/Aso2001407/2021sys-design/blob/main/ER.md "ER図はこちら")

# DBテーブルカラム詳細一覧

# データベース詳細

**購入テーブル**

|属性名|型|PK|NN|FK|デフォルト|備考|
|:---|:---|:---|:---|:---|:---|:---|
|order_id|bigint(20)|○|○||||
|customer_code|varchar(50)||○||||
|purchase_date|date||○||||
|total_price|int(11)||○||||

**購入テーブル詳細**

|属性名|型|PK|NN|FK|デフォルト|備考|
|:---|:---|:---|:---|:---|:---|:---|
|detail_id|bigint(20)|○|○|||
|order_id|bigint(20)|○|○||0|
|item_code|int(11)||○|||
|price|int(11)||○|||
|num|int(11)||○|||

**カテゴリテーブル**

|属性名|型|PK|NN|FK|デフォルト|備考|
|:---|:---|:---|:---|:---|:---|:---|
|category_id|int(11)|○|○|||
|name|varchar(20)||○|||
|reg_date|date||○|||

**ユーザー（顧客）テーブル**

|属性名|型|PK|NN|FK|デフォルト|備考|
|:---|:---|:---|:---|:---|:---|:---|
|customer_code|varchar(50)|○|○||||
|pass|varchar(50)||○||||
|name|varchar(20)||○||||
|address|varchar(100)||○||||
|tel|varchar(20)||○||||
|mail|varchar(100)||○||||
|del_flag|int(1)||||null||
|reg_date|date||○||||

**商品テーブル**

|属性名|型|PK|NN|FK|デフォルト|備考|
|:---|:---|:---|:---|:---|:---|:---|
|item_code|int(11)|○|○||0||
|item_name|varchar(50)||○|||
|price|int(11)||○||||
|category_id|int(11)||○|○||参照先 カテゴリテーブル(category_id)|
|image|varchar(200)||○|||
|detail|varchar(500)||||null|
|reg_date|date||○|||

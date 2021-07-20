# DB定義書
## ER図
[ER図はこちら](https://github.com/Aso2001407/2021sys-design/blob/main/ER.md "ER図はこちら")

# DBテーブルカラム詳細一覧

# データベース詳細

**購入テーブル（d_purchase）**

|和名|属性名（カラム名）|型|PK|NN|FK|デフォルト|備考|
|:---|:---|:---|:---|:---|:---|:---|:---|
|オーダーID|order_id|bigint(20)|○|○||||
|顧客コード|customer_code|varchar(50)||○||||
|購入日|purchase_date|date||○||||
|総額|total_price|int(11)||○||||

**購入詳細テーブル(d_purchase_detai1）**

|和名|属性名（カラム名）|型|PK|NN|FK|デフォルト|備考|
|:---|:---|:---|:---|:---|:---|:---|:---|
|オーダー詳細ID|detail_id|bigint(20)|○|○|||
|オーダーID|order_id|bigint(20)|○|○||0|
|商品コード|item_code|int(11)||○|||
|価格|price|int(11)||○|||
|数量|num|int(11)||○|||

**カテゴリマスタ（m_category）**

|和名|属性名（カラム名）|型|PK|NN|FK|デフォルト|備考|
|:---|:---|:---|:---|:---|:---|:---|:---|
|カテゴリID|category_id|int(11)|○|○|||
|カテゴリ名|name|varchar(20)||○|||
|登録日|reg_date|date||○|||

**顧客マスタ（m_customers）**

|和名|属性名（カラム名）|型|PK|NN|FK|デフォルト|備考|
|:---|:---|:---|:---|:---|:---|:---|:---|
|顧客コード|customer_code|varchar(50)|○|○||||
|パスワード|pass|varchar(50)||○||||
|氏名|name|varchar(20)||○||||
|住所|address|varchar(100)||○||||
|電話番号|tel|varchar(20)||○||||
|メールアドレス|mail|varchar(100)||○||||
|削除フラグ|del_flag|int(1)||||null||
|登録日|reg_date|date||○||||

**商品マスタ（m_items）**

|和名|属性名|型|PK|NN|FK|デフォルト|備考|
|:---|:---|:---|:---|:---|:---|:---|:---|
|商品コード|item_code|int(11)|○|○||0||
|商品名|item_name|varchar(50)||○|||
|価格|price|int(11)||○||||
|カテゴリID|category_id|int(11)||○|○||参照先 カテゴリテーブル(category_id)|
|画像ファイル名|image|varchar(200)||○|||
|商品詳細説明|detail|varchar(500)||||null|
|登録日|reg_date|date||○|||

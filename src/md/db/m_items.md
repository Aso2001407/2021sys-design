**商品テーブル**

|属性名|型|PK|NN|FK|デフォルト|備考|
|:---|:---|:---|:---|:---|:---|:---|
|item_code|int(11)|○|○||0||
|item_name|varchar(50)||○|||
|price|int(11)||○||||
|category_id|int(11)||○|○||参照先m_category(category_id)|
|image|varchar(200)||○|||
|detail|varchar(500)||||null|
|reg_date|date||○|||

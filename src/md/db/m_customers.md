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

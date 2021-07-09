# DB定義書
## ER図
[ER図]（http://www.plantuml.com/plantuml/png/fPLVJnj74C3VxrDipGEf6jTOIlyaGYX0gOHIGmL-gQhgjFKjvihzSVVE0WkGkBsMG00r3GAQqbBIXc8W65JJbYWk_J3BsUuJNw6xUsOv9xQ2b7bOx-xCpivlPcvzrt4XTlEceN19T2e019jbwfNEJm-fjrlRBDKEbgZt2_KsnVWD9KNgbwa_JyblZT4xgFqyLr_yWtgFAH76n6CUc2knMGeUhWIBAnULXQ3qOtNj-AAoICaZDg-TxR4hgBT2lJD-Tewm8-EkctFk918v0reyhdSpjfdu2YQS2TtAGGnDfJEXA6zfQ4ot44ZrZgO7HjHKxyWzjN_ua-4HC8oXbKL0MgH7UeT6U_lJWyD3KREF4CgDJXJwZ3nIb4vAZgc_H_txrAzGyZVrTpcZjyQe6L6mVH8yN00TKrFngQd8rOD3wi1GUZ3z6UX8wPRRZn4quodTSGiZjeCQsHHEroXXtW-ely0omk1ZaWPa3EWuCPQ7Ul6GvOHw6p8RdFGbGp2j02QTOOtg_dBryP7OwOEPYIosyvRMRnis1gEMFHarhMvjXtOsrX0ERVeCTYWqelu-zPyrqvTOh4BRYx4z6JqogoWvzWjPdcC3_PJyISbJnXO3q06idRB8LPs2uoAp4Qv811VgRr7od99_-Kt-l1ZNUMB88v2YSnvp8kfGfkGlIevaC5oV1jJRfnvlcVgJOhtuGyFdHUNxwlhzu723gyaYY9sVleWnsoBrba0iE5lbYpDsiBgnK_tfMNr_YpST8Sn3lR8OV7TKz_y9NR5qYmcoNDqjWDX_JtQ3qgyoPe6NoJkkRI8CkatrSkxqWExkrCrNUh6dH_27yeuygcPi3O7FFxttXLJ6utAQOrMM2mkQI2wWfc4KKRh8a7CJwbSB3Hdgc06pSWEZhAf1DtGrsmnPBrU2RtUYnH2Sear0jwRcyZWp3Xt46TCtMtzD33JwDKIXXHzLrzhoThoSbuyZTfUNo-X3SDk5Xfh3UaOIjK2gxvLh9yUjmLGDkInZKRx6rfjY0W4QqOHkXQfz2dGNcItm9Q8GAs-sn0tMveDLhwbDXKE7zwYONAy_PH1j0nKMqPwK4SfQiZfbRLnWlCqekWcpqZ1ColKRjfcNaWFnntCY7gq8jRoTWr_EhySUYRijlG1l6-6iVEyZpvfNejvJyMmjK_A0BSD7fxh-l5fUY_pPVQthBXJ_T6OUmmbewd7JJ8ZQ9MvbtklIahTltOOVVfdiwag-ZyO-21CI5y8cTv9oFJCZrW1Q6h0jem2kLBPGTG4RHpRZqtpJX5RXoeNOId8xqyO8t4YUlzWvFttmzfMdQUc9dmGtkYuj5EgjKh9ClMtg5MkdlrFl89A19KK-dw7Cs0rd8Fo25342AJCpZN10qtUhH1UY01nSjgYZY158cRKlzRBGB8C66dFvbi6AYFNiE5zWNG7vdB1almhGx4bBTAZDIjoPQ14_rbz7WFLhCcZswoWCz0g7aBl8qlAcyJy0 "ER図はこちら"）
# DBテーブルカラム詳細一覧
## データベース詳細

### 購入テーブル (d_purchase)
|和名|属性名（カラム）|型|PK|NN|FK|
|:---|:---|:---|:---|:---|:---|
|オーダーID|order_id|bigint(20)|〇|〇||
|顧客コード|customer_code|bigint(50)||〇||
|購入日|purchase|date||〇||
|総額|total_price|int(11)||〇||


### 購入詳細 (d_purchase_detail)
|和名|属性名（カラム）|型|PK|NN|FK|
|-----|------|--|--|--|--|
|オーダー詳細ID|detail_id|bigint(20)|〇|〇||
|オーダーID|order_id|bigint(20)|〇|〇||
|商品コード|item_code|int(11)||〇||
|価格|price|int(11)||〇||
|数量|num|int(11)||〇||


### 顧客マスタ (m_customers)
|和名|属性名（カラム）|型|PK|NN|FK|
|----|------|--|--|--|--|
|顧客コード|customer_code|varchar(50)|〇|〇||
|パスワード|pass|varchar(50)||〇||
|氏名|name|varchar(20)||〇||
|住所|address|varchar(100)||〇||
|電話番号|tel|varchar(20)||〇||
|メールアドレス|mail|varchar(100)||〇||
|削除フラグ|del_flag|int(1)||||
|登録日|reg_date|date||〇||


### カテゴリマスタ (m_category)
|和名|属性名（カラム）|型|PK|NN|FK|
|---|------|--|--|--|--|
|カテゴリID|category_id|int(11)|〇|〇||
|氏名|name|varchar(20)||〇||
|登録日|reg_date|date||〇||


### 商品マスタ
|和名|属性名（カラム）|型|PK|NN|FK|
|----|------|--|--|--|--|
|商品コード|item_code|int(11)|〇|〇||
|商品名|item_name|varchar(50)||〇||
|価格|price|int(11)||〇||
|カテゴリID|category_id|int(11)||〇|〇|
|画像ファイル名|image|varchar(200)||〇||
|商品詳細説明|detail|varchar(500)||〇||
|削除フラグ|del_flag|int(11)||〇||
|登録日|reg_date|date||〇||

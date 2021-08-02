### BD設計

## 購入テーブル
|和名|属性名（カラム）|型|PK|NN|FK|
|----|----------------|-|--|--|--|
|オーダーID|order_id|bigint(20)|〇|〇||
|顧客番号|customer_code|bigint(50)||〇||
|購入日|day|date||〇||
|合計金額|total|int(11)||〇||

## 購入詳細
|和名|属性名（カラム）|型|PK|NN|FK|
|-|-|-|--|-|-|
|オーダー詳細|detail_id|bigint(20)|〇|〇||
|価格|price|int(11)||〇||
|数量|num|int(11)||〇||
|支払い方法|charge|int(1)||〇||

## 顧客情報
|和名|属性名（カラム）|型|PK|NN|FK|
|-|-|-|-|-|-|
|ログインemail|email|varchar(50)||〇||
|パスワード|pass|varchar(20)||〇||
|氏名|name|varchar(100)||〇||
|住所|address|varchar(100)||〇||
|削除|del|int(1)||〇||
|登録日|reg|date||〇||

## 商品カテゴリ
|和名|属性名（カラム）|型|PK|NN|FK|
|-|-|-|-|-|-|
|カテゴリID|category_id|int(1)|〇|〇||
|商品名|item_name|varchar(20)||〇||

## 商品マスタ
|和名|属性名（カラム）|型|PK|NN|FK|
|-|-|-|-|-|-|
|商品コード|item_code|int(11)|〇|〇||
|商品名|item_name|varchar(50)||〇||
|価格|price|int(11)||〇||
|カテゴリID|category_id|iny(11)||〇||
|画像ファイル|image|varchar(200)||〇||
|商品詳細説明|detail|varchar(500)||〇||
|削除|del|int(11)||〇||
|登録日|reg|date||〇||

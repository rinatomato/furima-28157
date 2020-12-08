# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

＃テーブル設計
|------|----|-------|
＃users
nickname | string |  null:false |
email | string | null: false, unique: true
encrypted_password | string | null: false
first_name | string | null: false
family_name | string | null: false
first_name_kana | string | null: false
family_name_kana | string | null: false
birthday | date | null: false

＃items
item_name | string| null: false
explanation | text | null: false
category_id | integer | null: false
condition_id | integer | null: false
delibary_charge_id | integer | null: false
delibary_day_id | integer | null: false
delibary_way_id | integer | null: false
area_id | active_hash | null: false
price_id | integer | null: false
user_id | integer |null:false

#images
image| string | null: false

＃adress
country | string | null:false
prefecture | active_hash | null:false
city | string | null:false
number | string | null:false
building | string | 
user_id | references |null:false

user_id | integer | null: false
first_name | string | null: false
family_name | string | null: false
first_name_kane | string | null: false
family_name_kana | string | null: false
post_code | string | null: false
prefecture | string | null: false
city | string | null: false
address | string | null: false

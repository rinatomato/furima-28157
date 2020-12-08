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
has_many:items
belongs_to:addresses
has_many:buyer

＃items
item_name | string| null: false
explanation | text | null: false
category_id | integer | null: false
condition_id | integer | null: false
delibary_charge_id | integer | null: false
delibary_day_id | integer | null: false
delibary_way_id | integer | null: false
area_id | integer | null: false
price_id | integer | null: false
user_id | integer |null:false foreign_key: true
belongs_to:users
belongs_to:buyer


＃addresses
country | string | null:false
prefecture | active_hash | null:false
city | string | null:false
number | string | null:false
belongs_to:users

＃buyer
user_id | integer | null: false
item_id | integer | null: false
belongs_to:users
belongs_to:items

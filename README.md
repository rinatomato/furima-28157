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
mail adress | string | null: false, unique: true
password | string | null: false
first_name | string | null: false
family_name | string | null: false
first_name_kana | string | null: false
family_name_kana | string | null: false
birthday_yy | string | null: false
birthday_mm | string | null: false
birthday_dd | string | null: false

＃items
item_name | string| null: false
images| string | null: false
explanation | string | null: false
category| references | null: false
condition | references | null: false
delibary_charge | references| null: false
delibary_day | references | null: false
delibary_way| references | null: false
area| string | null: false
price | integer | null: false
user_id|refrences|null:false

＃comments
user_id | references | null:false
comment | string | null:false

＃likes
user_id | references | null:false
like | string | null:false

＃cards
card_number | integer | null:false
name | string | null:false
user_id | references | null:false

＃adress
country | string | null:false
prefecture | string | null:false
city | string | null:false
number | string | null:false
building | string | null:false
user_id | references |null:false

＃images
item_image | string | null:false

＃category
item_category | string | null:false

＃condition
item_condition | string | null:false

＃delibary_charge
charge | string | null:false

＃delibary_day
day | integer | null:false

＃delibary_way
way | string | null:false

＃area
area | string | null:false
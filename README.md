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
encrypted_password | string | null: false
first_name | string | null: false
family_name | string | null: false
first_name_kana | string | null: false
family_name_kana | string | null: false
birthday | date | null: false

＃items
item_name | string| null: false
explanation | text | null: false
category| references | null: false
condition | references | null: false
delibary_charge | references| null: false
delibary_day | references | null: false
delibary_way| references | null: false
area| active_hash | null: false
price | integer | null: false
user_id|refrences|null:false

#images
image| string | null: false

＃adress
country | string | null:false
prefecture | active_hash | null:false
city | string | null:false
number | string | null:false
building | string | 
user_id | references |null:false

＃images
item_image | string | null:false

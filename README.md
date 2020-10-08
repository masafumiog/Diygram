# README

##　users テーブル

| Column    | Type     | Options     |
| --------  | -------- | ----------- |
| profile   | string   | null: false |
| name_sei  | string   | null: false |
| name_mai  | stirng   | null: false |
| kana_sei  | string   | null: false |
| kana_mei  | string   | null: false |
| email     | string   | null: false |
| password  | string   | null: false |
| birthday  | date     | null: false |
| profile_image_id | integer | null:false |



### Association
- has_many :tweets
- has_many :comments

## tweets テーブル

| Column       | Type      | Options     | 
| --------     | --------- | ----------- |
| name         | string    | null: false |
| text         | text      | null: false |
| category_id  | integer   | null: false |
| user_id      | integer   | foreign_key:true ,null: false|

### Association
- belongs_to : user
- belongs_to : comment

## comments テーブル

| Column       | Type      | Options     | 
| --------     | --------- | ----------- |
| text         | text      | null: false |
| tweets_id    | integer   | foreign_key:true ,null: false|
| user_id      | integer   | foreign_key:true ,null: false|

### Association

-belongs_to : user
-belongs_to : tweet


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

<!-- # README

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

* ... -->

# freemarket_ample_66a DB設計


## images table

|Column|Type|Options|
|------|----|-------|
|image|text|null: false|
|item_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :item


## main_categories table

|Column|Type|Options|
|------|----|-------|
|main_category|string|
|item_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :item
- has_many :sub_category


## sub_categories table

|Column|Type|Options|
|------|----|-------|
|sub_category|string|
|main_category_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :main_category
- has_many :sub2_category


## sub2_categories table

|Column|Type|Options|
|------|----|-------|
|sub2_category|string|
|sub_category_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :sub_category
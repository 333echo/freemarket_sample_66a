# README


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
- has_many :sub_categories


## sub_categories table

|Column|Type|Options|
|------|----|-------|
|sub_category|string|
|main_category_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :main_category
- has_many :sub2_categories


## sub2_categories table

|Column|Type|Options|
|------|----|-------|
|sub2_category|string|
|sub_category_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :sub_category
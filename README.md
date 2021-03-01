# テーブル設計

## usersテーブル

| Column   | Type   | Options     |
| -------- | ------ | ----------- |
| nickname | string | null: false |
| email    | string | null: false |
| password | string | null: false |
| profile  | text   | null: false |
| phone    | string | null: false |

### Association
- has_many :animals
- has_many :blogs


## animalsテーブル

| Column      | Type       | Options                        |
| ----------- | ---------- | ------------------------------ |
| type        | boolean    | null: false                    |
| name        | string     | null: false                    |
| age         | integer    | null: false                    |
| explanation | text       | null: false                    |
| user        | references | null: false, foreign_key: true |

### Association
- belongs_to :user


## blogsテーブル

| Column  | Type       | Options                        |
| ------- | ---------- | ------------------------------ |
| tittle  | string     | null: false                    |
| content | text       | null: false                    |
| user    | references | null: false, foreign_key: true |


### Association
- belongs_to :user
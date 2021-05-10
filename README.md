## usersテーブル

| Column             | Type   | Options                   |
| ------------------ | ------ | ------------------------- |
| email              | string | null: false, unique: true |
| encrypted-password | string | null: false               |
| user_name          | string | null: false               |
| user_desc          | text   | null: false               |

### Association

- has_many :contents



## contentsテーブル

| Column     | Type   | Options     |
| ---------- | ------ | ----------- |
| main_title | string | null: false |
| main_desc  | text   | null: false |

### Association

- belongs_to :user
- has_many :processes
- has_many :comments



## processesテーブル

| Column    | Type   | Options     |
| --------- | ------ | ----------- |
| sub_title | string | null: false |
| sub_desc  | text   | null: false |

### Association

- belongs_to :contents



## commentsテーブル

| Column | Type | Options     |
| ------ | ---- | ----------- | 
| text   | text | null: false |

### Association

- belongs_to :content
- belongs_to :user
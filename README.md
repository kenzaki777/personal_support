## users テーブル

| Column           | Type  | Options                        |
| ------           | ------| ------------------------------ |
|nickname          |string | null:false                     |
|email             |string | null: false,unique: true       |
|encrypted_password|string | null: false                    |

### association
has_many :personal_data

## personal_data テーブル
| Column              | Type     | Options                        |
| ------              | ------   | ------------------------------ |
|user                 |references|null: false,foreign_key: true   |
|name                 |string    | null: false                    |
|name_kana            |string    | null: false                    |
|birth_day            |date      |                                |
|hobby                |text      |                                |
|favorite_food        |text      |                                |
|not_good             |text      |                                |
|others               |text      |                                |

### association
belongs_to :user
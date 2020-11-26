## users テーブル

| Column            | Type      | Options                        |
| ------------------| ----------| -------------------------------|
| nickname          | string    | null: false                    |
| e-mail            | string    | null: false                    |
| password          | string    | null: false                    |

### Association

- has_many :movies
- has_many :lists

## movies　テーブル

| Column            | Type      | Options                        |
| ------------------| ----------| -------------------------------|
| title             | string    | null: false                    |
| description       | string    | null: false                    |
| release_year      | date      | null: false                    |

### Association

- belongs_to :user
- has_many :lists

## lists　テーブル

| Column            | Type       | Options                        |
| ------------------| -----------| -------------------------------|
| user_id           | references | null: false, foreign_key: true |
| movie_id          | references | null: false, foreign_key: true |

### Association

- belongs_to :user
- belongs_to :list

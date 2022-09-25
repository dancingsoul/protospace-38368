# README

## Usersテーブル

| Column    | Type    | Options       |
| --------- | --------| --------------|
| email     | string  | Null: false   |
| password  | string  | Null: false   |
| name      | string  | Null: false   |
| profile   | text    | Null: false   |
| occupation| text    | Null: false   |
| position  | text    | Null: false   |

## Association

has_many: prototypes
has_many: comments


## Prototypesテーブル

| Column     | Type          | Options      |
| ---------  | ------------- | ------------ |
| title      | string        | Null: false  |
| catch_copy | text          | Null: false  | 
| concept    | text          | Null: false  |
| user       | references    |              |

## Association

has_many: comments
belongs_to: users


## Commentsテーブル

| Column     | Type         | Options       |
| -----------| -------------|-------------- |
| text       | text         | Null: false   |
| user       | references   |               |
| prototype  | references   |               |

## Association

belongs_to: users
belongs_to: prototypes

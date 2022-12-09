# Assessment for Laravel Junior Developer

To create FIFA World Cup 2022 competition API!

### Goals
- [ ] Setup Group and Team List for World Cup 2022
- [ ] Develop Fixtures CRUD functionalities
- [ ] Develop Team Listing by group

<hr>

### Prerequisites
Base the groups migration file in the following table:
```mysql
mysql> show columns from groups;
+-------------------+-----------------+------+-----+---------+----------------+
| Field             | Type            | Null | Key | Default | Extra          |
+-------------------+-----------------+------+-----+---------+----------------+
| id                | bigint unsigned | NO   | PRI | NULL    | auto_increment |
| name              | varchar(255)    | NO   |     | NULL    |                |
| created_at        | timestamp       | YES  |     | NULL    |                |
| updated_at        | timestamp       | YES  |     | NULL    |                |
+-------------------+-----------------+------+-----+---------+----------------+
```

Base the teams migration file in the following table:
```mysql
mysql> show columns from teams;
+-------------------+-----------------+------+-----+---------+----------------+
| Field             | Type            | Null | Key | Default | Extra          |
+-------------------+-----------------+------+-----+---------+----------------+
| id                | bigint unsigned | NO   | PRI |         | auto_increment |
| group_id          | bigint unsigned | NO   |     |         |                |
| name              | varchar(255)    | NO   |     |         |                |
| created_at        | timestamp       | YES  |     | NULL    |                |
| updated_at        | timestamp       | YES  |     | NULL    |                |
+-------------------+-----------------+------+-----+---------+----------------+
```

Base the fixtures migration file in the following table:
```mysql
mysql> show columns from fixtures;
+-------------------+-----------------+------+-----+---------+----------------+
| Field             | Type            | Null | Key | Default | Extra          |
+-------------------+-----------------+------+-----+---------+----------------+
| id                | bigint unsigned | NO   | PRI |         | auto_increment |
| home_team_id      | bigint unsigned | NO   |     |         |                |
| away_team_id      | bigint unsigned | NO   |     |         |                |
| home_goal         | int unsigned    | YES  |     | NULL    |                |
| away_goal         | int unsigned    | YES  |     | NULL    |                |
| date              | datetime        | NO   |     |         |                |
| status            | varchar(255)    | NO   |     | pending |                |
| created_at        | timestamp       | YES  |     | NULL    |                |
| updated_at        | timestamp       | YES  |     | NULL    |                |
+-------------------+-----------------+------+-----+---------+----------------+
```

<hr>

### ℹ️ Instructions
1. Start a project in Laravel 9
2. Create group list seeder.
3. Create team list seeder.
4. Add a **CREATE fixture API**
5. Add a **UPDATE fixture API**
6. Add a **DELETE fixture API**
7. Add a **GET fixture listing API**
8. Add a **GET team listing by group API**

<hr>

### 📝 Notes
- You can get groups and teams data from https://github.com/openfootball/worldcup.json/blob/master/2022/worldcup.groups.json.
- You can get matches data from https://github.com/openfootball/worldcup.json/blob/master/2022/worldcup.json.

<hr>

### ⭐ Bonus
- All routes implement the `public api token` middleware.

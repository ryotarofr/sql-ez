ユーザーデーブル
| id | name | age | gender | memo | create_time |
| -------------- | --------- | ---------------- | ----------------------------- | -- | -- |
|1| 山田太郎| 25 |1| 今日もいい天気 |2022-09-19 18:47:28|
|2| 佐藤花子| 24 |2| NULL |2022-09-19 18:47:28|
|3| 田中次郎| 39 |1| hello YouTube |2022-09-19 18:47:28|
|4| 高橋よしこ| 34| 2| 水曜日は不在 |2022-09-19 18:49:42|
|5| 鈴木裕貴| 18 |1 |NULL |2022-09-19 18:50:43|
|6| 山本もんじゃ| 3 |0| 柴犬 |2022-09-19 18:51:13|
|7| 小林マイク |29 |1| 来月イギリス帰国 |2022-09-19 18:51:13|
|8| 山本ハツ江 |89 |2| NULL| 2022-09-19 18:53:51|
|9| 松本幸太郎 |54 |1| 日中は携帯へ。 |2022-09-19 18:54:47|
|10| 木村アリサ| 17| 2| NULL| 2022-09-19 18:56:01|

```bash
SELECT * FROM users;
```

id 指定

```bash
SELECT * FROM users where id=1;
```

複数の id を指定

```bash
SELECT * FROM users where id in(1,2,4);
```

`memo`カラムの`NULL`を取得

```bash
SELECT * FROM users where memo IS NULL;
```

NULL じゃないもの

```bash
SELECT * FROM users where memo IS NOT NULL;
```

部分一致

```bash
SELECT * FROM users WHERE name LIKE '%木%';
```

前方一致(木ではじまる name)

```bash
SELECT * FROM users WHERE name LIKE '木%';
```

後方一致(木で終わる name)

```bash
SELECT * FROM users WHERE name LIKE '%木';
```

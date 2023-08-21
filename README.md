# Horse Race Common Info Db

競馬の情報分析に必要なデータを集めたデータベースとそのデータを取集する環境。

## Getting Started

```
❯❯ !(git:main) ~/dev/horse_race_common_info_db/main
❯ docker-compose up -d
```

- 初回起動時に実行されること
  - データベースの作成
  - テーブルの作成
  - マスター系データの Insert

## データの登録

データ登録は batch コンテナ内で実行。

引数には競馬の開催日を指定する。
フォーマットは yymmdd (年の下2桁 + 月(2桁) + 日(2桁))。

```
[root@75398904e938 scripts]# pwd
/app/scripts
[root@75398904e938 scripts]# ./download_and_convert.sh 230812
```
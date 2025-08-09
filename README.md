# 発表資料

![スライド1](information/スライド1.png)

![スライド2](information/スライド2.png)

![スライド3](information/スライド3.png)

![スライド4](information/スライド4.png)

![スライド5](information/スライド5.png)

![スライド6](information/スライド6.png)

![スライド7](information/スライド7.png)

![スライド8](information/スライド8.png)

![スライド9](information/スライド9.png)

![スライド10](information/スライド10.png)

---

<img width="712" alt="スクリーンショット 2025-04-18 17 21 57" src="https://github.com/user-attachments/assets/a9a2076f-3f74-4a29-8796-2e63c4a8a12b" />

### PC から CloudSQL の PostgreSQL に接続する方法

1. Google Cloud SDK をインストールする
   https://cloud.google.com/sdk?hl=ja
1. postgresql をインストールする
   https://www.postgresql.jp/download

1. ログインする
   ```
   gcloud auth application-default login
   ```
1. Cloud SQL Auth Proxy を起動する

   - Windows の場合

   ```
   cloud-sql-proxy.exe gabaithon202502saga2:asia-northeast1:gabaithon202502saga2 --port 5432 --debug-logs --run-connection-test
   ```

   - Mac の場合

   ```
   ./cloud-sql-proxy gabaithon202502saga2:asia-northeast1:gabaithon202502saga2 --port 5432 --debug-logs --run-connection-test
   ```

   を実行する

1. DB に接続する

   別ターミナルで以下のコマンドを実行する

   ```
   psql -h 127.0.0.1 -d postgres -U postgres
   ```

   Password for user postgres:

   ```
   postgres
   ```

   接続完了、SQL 文を実行できる

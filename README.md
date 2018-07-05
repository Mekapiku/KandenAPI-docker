# KandenAPI-docker
## これは何？
[KandenAPI](https://github.com/Mekapiku/KandenAPI)をDockerで動かすやつです．

## 使い方
### Command
```
docker build -t kanden/kanden .
docker run --rm -e KANDEN_LOGIN_ID="login_id" -e KANDEN_LOGIN_PASS="login_pass" -v /tmp:/tmp --name kanden kanden/kanden
```

### Result
```
{
    "kanden": {
        "date":"2018-06-01"
        "this_month": 8966,
        "diff_last_month": -1109,
        "diff_last_year": 110
    }
}
```

## 環境変数
`KANDEN_LOGIN_ID` はぴeみる電ログイン用の会員ID
`KANDEN_LOGIN_PASS` はぴeみる電ログイン用のパスワード
`OUTPUT_DIR` 結果の出力先：デフォルト`/tmp/kanden.json`

## その他
[json-server](https://github.com/typicode/json-server)との併用が便利です。

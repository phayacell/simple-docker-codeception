Simple docker-codeception
=========

Docker で、いろんなサイトを Codeception を使った受け入れテストを実行できます。
本レジストリは、その最小構成です。

Quick Start
-----------

テスト実行。

```bash
docker-compose run --rm codecept run -d example
```

テスト結果は `tests/_output` に吐き出されます。

Setup
-----

ベースとなる URL は `tests/example.suite.yml` で書き換えることができます。

```yaml
modules:
    config:
        WebDriver:
            url: http://my-domain.com/
```

Usage
-----

VNC で画面を見ながらデバッグしたい場合、Mac だったら以下のコマンドを叩くと開きます。

```bash
open vnc://localhost:5900
```

パスワードは `secret` です。


Codeception の詳しい使い方は `codecept --help` を実行するか、[documentation](http://codeception.com/docs/) をご確認ください。

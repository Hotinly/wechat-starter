# wechat-starter

Template for developing wechat in rails.

### Screenshots

<img src="http://i.imgur.com/oFs1AzQ.png" width="240">
<img src="http://i.imgur.com/urwmWZv.png" width="240">
<img src="http://i.imgur.com/UPw6FRc.png" width="240">

### Features

* Integerate gem [Eric-Guo/wechat](https://github.com/Eric-Guo/wechat)

* Integerate gem [jasl/wx_pay](https://github.com/jasl/wx_pay)

### Requirements

* Mysql

* Configure "服务器地址" as `http://your-domain.com/wechat`

* Configure "测试授权目录" as `http://your-domain.com/`

### Usage

* Create your new project and add this repo as template

```
mkdir your_app
cd your_app
git init
git remote add template https://github.com/goofansu/wechat-starter.git
git fetch template
git checkout -b master template/master
bundle install
rake db:create
rake db:migrate
```

* Create `config/application.yml` and config following information:

``` yaml
wechat_app_id: "AppID"
wechat_secret: "AppSecret"
wechat_token:  "Token"
wechat_encoding_aes_key: "EncodingAESKey"

# following is optional if you don't need wechat pay
wechat_pay_mch_id: "merchant id"
wechat_pay_api_key: "32 bits api key configured in pay.weixin.qq.com"
wechat_pay_notify_url: "url to accept pay result notification"
```

* Start server

`rails s`

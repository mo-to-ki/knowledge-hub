# aws-command
- [aws-command](#aws-command)
  - [config](#config)


## config
* 認証情報の管理  
awsは以下のディレクトリで認証情報を管理している。
```
└── .aws
    ├── .config
    └── .credentials
```

* 認証情報の設定方法  
以下のコマンドで {profile-name} というプロフィール名の認証情報を設定している。  
```shell
aws configure --profile {profile-name}
```

* .config  
.configファイルで、以下のように認証情報を管理している。
```shell:.config
[profile hoge]
output = json
region = {リージョン}

[profile fuga]
output = json
region = {リージョン}

[default]
output = json
region = {リージョン}
```
* .credentials  
.credentialsファイルで、以下のように認証情報を管理している。
```shell:.credentials
[hoge]
aws_access_key_id = {アクセスキー}
aws_secret_access_key = {シークレットキー}

[fuga]
aws_access_key_id = {アクセスキー}
aws_secret_access_key = {シークレットキー}

[default]
aws_access_key_id = {アクセスキー}
aws_secret_access_key = {シークレットキー}
```

* 認証情報の使い分け
```shell
aws {command} --profile {profile}
```

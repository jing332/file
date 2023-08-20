# Build

### Android Studio:
在项目根目录下新建文件 `local.properties` 并写入如下内容：
```
KEY_PATH=E\:\\Android\\key\\sign.jks (签名文件)
KEY_PASSWORD= 密码
ALIAS_NAME= 别名
ALIAS_PASSWORD= 别名密码
```

### Github Actions:
> 详见 https://www.cnblogs.com/jing332/p/17452492.html

使用 Git Bash 对签名文件进行无换行Base64编码: `openssl base64 < key.jks | tr -d '\r\n' | tee key.jks.base64.txt`

分别添加如下四个私有变量 (Repository secrets):
> 前往以下链接：https://github.com/你的用户名/tts-server-android/settings/secrets/actions
* `ALIAS_NAME` 别名
* `ALIAS_PASSWORD` 别名密码
* `KEY_PASSWORD` 密码
* `KEY_STORE` 前面生成的 sign.jks.base64.txt 内容

---
---

# Build

### Android Studio:
Create a new file `local.properties` in the project's root directory and write the following content:
```
KEY_PATH=E\:\\Android\\key\\sign.jks (Keystore file)
KEY_PASSWORD= Password
ALIAS_NAME= Alias
ALIAS_PASSWORD= Alias Password
```

### Github Actions:
> See https://www.cnblogs.com/jing332/p/17452492.html for details

Use Git Bash to perform newline-free Base64 encoding on the keystore file: `openssl base64 < key.jks | tr -d '\r\n' | tee key.jks.base64.txt`

Add the following four private variables as Repository secrets:
> Go to the following link: https://github.com/your-username/tts-server-android/settings/secrets/actions
* `ALIAS_NAME` Alias
* `ALIAS_PASSWORD` Alias Password
* `KEY_PASSWORD` Password
* `KEY_STORE` Content of the previously generated sign.jks.base64.txt file

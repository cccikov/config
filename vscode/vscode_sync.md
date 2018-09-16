# vscode同步设置 (Settings Sync)

## 上传配置

1. 进入个人github设置，从GitHub获取个人访问令牌（token）

    `Settings / Developer settings / Personal access tokens / Generate New Token`

2. 从范围中选择`Gist`。点击`Generate token`生成令牌（token）。将token保存起来供将来使用，因为刷新页面，token将消失。值得注意的事，一个token只能一个设备使用

    `5552492801162ccbf187072feebb6325f45956f3`

3. ctrl + shift + p，`Upload Settings`会提示输入token，输入好后会自动上传设置，并在控制输入上传信息

    ``` bash
        # CODE SETTINGS SYNC UPLOAD SUMMARY
        # Version: 2.9.0
        # --------------------
        # GitHub Token: d0dbe1fc95fcc633ebb36061999bb4e246770cc3
        # GitHub Gist: 9f615cd27bac8443877e5a89ce11861a
        # GitHub Gist Type: Secret
        # ...
        # ...
        # ...
        # ...
    ```

    其中`GitHub Gist`就是`GitHub Gist ID` 即系 `9f615cd27bac8443877e5a89ce11861a`

    * `9f615cd27bac8443877e5a89ce11861a` home

            GitHub Token: 5552492801162ccbf187072feebb6325f45956f3
            GitHub Gist: 9f615cd27bac8443877e5a89ce11861a
            GitHub Gist Type: Secret

    [https://gist.github.com/cccikov/9f615cd27bac8443877e5a89ce11861a](https://gist.github.com/cccikov/9f615cd27bac8443877e5a89ce11861a)可以浏览配置（好像要翻墙才可以访问）

## 下载配置

1. ctrl + shift + p，输入`Downlaod Settings`会分别提示输入 `token` 和 `GitHub Gist ID`，输入好后会自动下载设置

2. 如果输出错误，可以通过 ctrl + shift + p 输入`Reset Extension Settings` 重新设置


## 实际发现

就算token删除，重新配置一个新的token，直接下载配置用新的token旧的Gist ID也是可以的

token和Gist ID是毫无关联的

而且只要下载配置过后，下次上传也是按照下载时输入的Gist ID
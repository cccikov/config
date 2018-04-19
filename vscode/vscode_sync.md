# vscode同步设置

## 上传配置

1. 进入个人github设置，从GitHub获取个人访问令牌（token）

    `Settings / Developer settings / Personal access tokens / Generate New Token`

2. 从范围中选择`Gist`。点击`Generate token`生成令牌（token）。将token保存起来供将来使用，因为刷新页面，token将消失

    `8d71ae52d45af696316e6ea49c9205ffbd12bf48`

3. ctrl + shift + p，`Upload Settings`会提示输入token，输入好后会自动上传设置，并在控制输入上传信息

    ``` bash
        # CODE SETTINGS SYNC UPLOAD SUMMARY
        # Version: 2.9.0
        # --------------------
        # GitHub Token: 8d71ae52d45af696316e6ea49c9205ffbd12bf48
        # GitHub Gist: ba6177381ca10c759bac910de257c867
        # GitHub Gist Type: Secret
        # ...
        # ...
        # ...
        # ...
    ```

    其中`GitHub Gist`就是`GitHub Gist ID`

    [https://gist.github.com/cccikov/ba6177381ca10c759bac910de257c867](https://gist.github.com/cccikov/ba6177381ca10c759bac910de257c867)可以浏览配置（好像要翻墙才可以访问）

## 下载配置

1. ctrl + shift + p，输入`Downlaod Settings`会分别提示输入 `token` 和 `GitHub Gist ID`，输入好后会自动下载设置

2. 如果输出错误，可以通过 ctrl + shift + p 输入`Reset Extension Settings` 重新设置
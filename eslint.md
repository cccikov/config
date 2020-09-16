# eslint

* 初始化

    ```
    eslint --init
    ```
    自动创建 `.eslintrc` 文件

* 配置

    [配置文档](https://eslint.bootcss.com/docs/user-guide/configuring)

    - extends 属性值可以是：
        + 指定配置的字符串(配置文件的路径、可共享配置的名称、eslint:recommended 或 eslint:all)
        + 字符串数组：每个配置继承它前面的配置

        extends: ['plugin:vue/recommended', 'eslint:recommended']

        `eslint:recommended` 是eslint推荐的规则 https://eslint.bootcss.com/docs/rules/

        `plugin:vue/recommended` 是vue项目推荐的规则 https://github.com/vuejs/eslint-plugin-vue/blob/v6.2.2/docs/user-guide/README.md


    - rules 属性可以做下面的任何事情以扩展（或覆盖）规则：
        + 启用额外的规则
        + 改变继承的规则级别而不改变它的选项
            * 基础配置："eqeqeq": ["error", "allow-null"]
            * 派生的配置："eqeqeq": "warn"
            * 最后生成的配置："eqeqeq": ["warn", "allow-null"]
        + 覆盖基础配置中的规则的选项
            * 基础配置："quotes": ["error", "single", "avoid-escape"]
            * 派生的配置："quotes": ["error", "single"]
            * 最后生成的配置："quotes": ["error", "single"]


* rules 规则

    基本语法
    ```
    "rules": {
        "semi": ["error", "always"],
        "quotes": ["error", "double"]
    }
    ```

    第一个值是错误级别，可以使下面的值之一
    ```
    "off" or 0 - 关闭规则
    "warn" or 1 - 将规则视为一个警告（不会影响退出码）
    "error" or 2 - 将规则视为一个错误 (退出码为1)
    ```

    [规则文档](https://eslint.bootcss.com/docs/rules/)

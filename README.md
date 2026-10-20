# zhiban-ai-config · 配置空模板

知办AI 的配置字段参考。仅包含空模板，不包含真实环境配置、账号、密钥、签名证书或原配置仓库的 Git 历史。

## 社区版如何启动

社区默认使用主代码仓库的 deploy/community，不需要这个模板仓库。先按主仓库的 docs/INSTALL.md 完成 Docker Compose、初始化管理员和 Mock 对话。模型配置、数据库和对象存储以当前社区部署文件为准。

## 模板怎么用

1. 按 development、test、production 选择环境及组件目录。
2. 将需要的文件复制一份，删除文件名末尾的 .example。例如 dart-defines.env.example → dart-defines.env、bus.yaml.example → bus.yaml、.env.example → .env。
3. 按组件的配置说明填写自己的地址、口令及路径。字符串为空、数字为 0、布尔值为 false 均为占位，不代表推荐默认值；列表保留形状参考，使用前自行调整。
4. 真实文件留在本地，当前忽略规则只允许 environments 下的 .example 和 README.md 入库。提交前检查暂存内容，真实配置不要改名为 .example。

## 目录范围

development 包含服务端、示例、消息服务与相关组件的字段骨架；test 包含服务端和客户端参考；production 包含客户端编译、运行时与签名参数参考。部分字段属于私有部署或历史组件，仅作字段参考，不代表社区版包含对应产品能力。目录中的 production 是用途分类，不代表已经通过生产验收。

移动端、支付证书、真实签名资产、运行日志、迁移快照、私有部署脚本不随本模板提供。签名参数需要自行生成证书并填写本地路径。所有值由部署者提供，空模板不能直接启动服务，不应以测试值代替生产值。

## 公开方式

请从此目录新建独立 Git 历史后发布为 zhiban-ai-config。不要将原真实配置仓库改成公开，也不要将原仓库历史、分支或标签导入本目录。

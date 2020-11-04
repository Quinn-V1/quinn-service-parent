# quinn-service-parent
quinn-service-parent是Quinn-Service系列的顶层父项目，用于统一外部依赖。  
**目前V1.1.0版本因为模块分布不够科学，准备停更。感兴趣的可以参照V2**  
  
## Quinn-Service系列 项目目标  
- 快速搭建科学合理的项目骨架（分层-分模块）
- 细粒度、多中可替换实现方案的通用模块可插拔集成
- 最大限度地追求“高内聚、低耦合”
- 最大限度地追求应用的灵活性和可扩展性

## 目前实现的功能包括
### 工具层
主要包括一些静态工具库，通用模型、枚举、常量，通用抽象。以quinn-service-util为groupId，根据不同的功能边界又做一下细分
artifactId|名称|描述
-- | -- | --
quinn-util-base|基础工具类|例如字符串操作、数字操作、文件操作、枚举、常量等等
quinn-util-database|数据库（JDBC）具类|直接操作JDBC、Datasource、Connection等等
quinn-util-freemarker|Freemark工具类|添加Freemark引用然后简单封装
quinn-util-generate|代码自动生成工具|可选择不同数据源，自定义模版

### 框架层
主要包括一些通用业务接口、基类实现、启动增强、系统安全、数据源增强第三方应用集成等，以quinn-service-framework为groupId，根据不同的功能边界做以下细分
artifactId|名称|描述
-- | -- | --
quinn-service-api|通用业务接口、模型类|例如缓存操作接口、文件操作接口、策略操作接口；通用模型基础实体等等

### 核心层
主要包括权限控制、数据增强、配置增强、系统功能、消息功能

### 业务层
比如BPM，CMS等具有较强的专业性和企业资产性质，不便公开

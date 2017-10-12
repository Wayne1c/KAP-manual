## KAP 2.5 发布声明

近期我们发布了KAP v2.5，在该版本中，配备了全新的多级权限系统。**项目级权限**支持基于角色的权限管控，**行列级权限**支持更细粒度的访问隔离。同时，KAP v2.5提供了智能化的建模体验，**模型顾问**支持通过SQL自动生成模型，Cube优化器引进**多种优化策略**，**SQL验证**支持快速检验模型、Cube是否可用。



#### 企业级安全增强

**多层级权限管控**

简洁而完整的权限系统，从粗粒度到细粒度的访问权限都可以得到差异化的管控。

**项目级与表级权限**

项目级别的访问权限，可以基于用户角色进行不同程度的管控。在同一项目中，增加了表级权限控制，方便用户对源表的访问权限进行差异化的配置。作为企业级的多用户数据库，项目级和表级权限管控满足了同一系统下的多个子公司、职能部门、业务群体的统一而灵活的权限需求。

**行列级权限**

在表级权限下，支持细粒度的行列级权限管控，将权限配置细化到单元格级别，满足了企业用户对业务数据，客户个人信息等进行隔离的需求。



#### **智能化的建模体验**

**模型顾问**

支持通过SQL自动生成模型。导入源表后，用户只需指定事实表，即可通过输入SQL自动创建模型。模型顾问无需用户动手创建复杂模型，实现了从SQL到模型的一键生成。

**快速验证SQL**

无需构建Cube，模型或Cube在设计保存后，快速验证SQL查询是否能被回答，方便用户不断修改模型或Cube并及时获得反馈。

**多种Cube优化策略**

Cube优化器提供了多种优化策略，既可以支持对灵活查询的模型优先策略，也可以通过业务优先的策略定向加速查询SQL，满足了多种优化场景。



**其他更新与改进还包括**

提供更丰富的样例数据，流式数据模型与cube，方便快速验证与流式数据源的集成

KyAnalyzer无需单独提供许可证，可直接读取KAP的许可证



#### Hadoop发行版支持

  产品认证：

  	Cloudera CDH 5.7+
  	
  	MapR 5.2.1

  兼容性测试：

  	Apache Hadoop 2.2+，HBase 0.98+，Hive 0.14+

  	Hortonworks HDP 2.2+

  	Azure HDInsight 3.4~3.6 

  	AWS EMR 5.1~5.7

  	华为 FusionInsight C50/C60+



#### **产品下载**

KAP v2.5已经开放下载试用，更多产品信息请见[KAP产品页面](http://account.kyligence.io)。
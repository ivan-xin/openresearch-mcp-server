MCP工具设计原则：
├── 单一职责原则
│   ├── 每个工具只做一件事
│   ├── 功能边界清晰
│   ├── 易于测试和维护
│   └── 可复用性强
├── 数据导向原则
│   ├── 返回结构化数据
│   ├── 避免预设解读
│   ├── 保持数据完整性
│   └── 支持多种视角分析
├── 组合性原则
│   ├── 工具间可以组合使用
│   ├── 输出可作为其他工具输入
│   ├── 支持复杂工作流
│   └── 避免功能重复
└── 性能优先原则
    ├── 快速响应
    ├── 资源高效利用
    ├── 支持并发调用
    └── 优雅降级


基础数据工具：
├── search_papers
│   ├── 输入：查询条件、过滤器、分页参数
│   ├── 处理：调用Go搜索API
│   ├── 输出：论文列表、元数据、统计信息
│   └── AI增强：无（由Agent处理）
├── get_paper_details
│   ├── 输入：论文ID列表
│   ├── 处理：批量获取论文详情
│   ├── 输出：完整论文信息
│   └── AI增强：无
├── get_citation_network
│   ├── 输入：论文ID、网络深度、方向
│   ├── 处理：调用Go图分析API
│   ├── 输出：节点、边、网络统计
│   └── AI增强：无
└── get_research_trends
    ├── 输入：领域、时间范围、指标类型
    ├── 处理：调用Go分析API
    ├── 输出：时序数据、统计指标
    └── AI增强：无


计算增强工具：
├── calculate_similarity
│   ├── 输入：文本列表、相似度算法
│   ├── 处理：向量化 + 相似度计算
│   ├── 输出：相似度矩阵
│   └── AI增强：语义向量化
├── extract_keywords
│   ├── 输入：文本内容、提取数量
│   ├── 处理：关键词提取算法
│   ├── 输出：关键词列表、权重
│   └── AI增强：语义关键词提取
├── generate_embeddings
│   ├── 输入：文本列表
│   ├── 处理：调用嵌入模型
│   ├── 输出：向量表示
│   └── AI增强：多模型嵌入
└── cluster_documents
    ├── 输入：文档向量、聚类参数
    ├── 处理：聚类算法
    ├── 输出：聚类结果、中心点
    └── AI增强：智能聚类数选择
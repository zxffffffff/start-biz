# Jena
免费开源 Java 框架 for building Semantic Web and Linked Data applications.

## 简介
- https://jena.apache.org/
- https://github.com/apache/jena
- Java
- Apache-2.0 license 
- Jena是一种基于Java的RDF框架，提供了一套完整的API和工具，用于处理和管理RDF数据和Linked Data，支持SPARQL查询、RDF数据模型、RDF存储和推理等功能。

## 1、RDF(Resource Description Framework)
- W3C Web3.0 中的标准

### RDF API
- 与核心 API 交互以创建和读取资源描述框架(RDF) 图。使用RDF/XML或Turtle等流行格式序列化您的三元组。

### ARQ (SPARQL)
- 自动查询请求
- 使用符合SPARQL 1.1的引擎 ARQ 查询 RDF 数据。ARQ 支持远程联合查询和自由文本搜索。

## 2、Triple store

### TDB
- 使用 TDB（一种本机高性能三重存储）保存您的数据。TDB 支持全系列的 Jena API。

### Fuseki
- 将您的三元组公开为可通过 HTTP 访问的 SPARQL 端点。Fuseki 提供与 RDF 数据的 REST 风格交互。

## 3、OWL(Web Ontology Language)

### Ontology API
- 使用模型、RDFS 和Web Ontology Language (OWL) 为您的 RDF 数据添加额外的语义。

### Inference API
- 推理您的数据以扩展和检查您的三元组存储的内容。配置您自己的推理规则或使用内置的 OWL 和 RDFS推理器。


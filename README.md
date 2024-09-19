# o1 思维过程模拟器

这是一个模拟gpt-4o1思维过程的项目,基于 [bklieger-groq 的 g1-prototype](https://github.com/bklieger-groq/g1-prototype) 进行改进和扩展。项目包含两个主要部分:Streamlit应用和Cloudflare Worker。

## 项目简介

本项目旨在创建一个灵活的思维过程模拟器,可以使用各种大型语言模型实现多步推理,提高输出的准确性和可解释性。

## Streamlit 应用

### 主要特性

- 支持多种大型语言模型,如Llama-3.1 70b等
- 兼容不同的API端点服务商
- 实现多步思考过程,每一步都有标题和详细内容
- 基于Streamlit构建的交互式Web界面
- 支持自定义API配置

### 使用方法

1. 运行应用:
   ```
   streamlit run app.py
   ```

2. 在浏览器中打开显示的本地URL

3. 在侧边栏中配置API端点、密钥和模型选择

4. 在主界面输入您的问题,然后观察生成的多步思考过程

### 注意事项

- 需要有效的API密钥(取决于所选择的服务商)
- 当前版本限制了最多25个推理步骤
- 项目支持多种模型和API端点,请根据需要进行配置

## Cloudflare Worker

### 主要特性

- 使用JavaScript/TypeScript实现,可部署为Cloudflare Worker
- 保留了Streamlit应用的核心功能
- 提供简单的HTML界面用于输入参数和显示结果
- 支持流式响应,实时显示思考步骤
- 错误重试机制,提高稳定性

### 使用方法

1. 将`worker.js`文件部署到Cloudflare Worker

2. 访问Worker的URL,您将看到一个Web界面

3. 在界面中填写API URL、API Key、模型和查询

4. 提交查询后,结果将逐步显示在页面上

### 注意事项

- 需要有Cloudflare账户并了解如何部署Worker
- API密钥等敏感信息应通过Cloudflare的环境变量功能进行管理
- 可能需要根据具体需求调整Worker的资源限制

## 贡献

欢迎提交问题报告、改进建议或直接贡献代码!

## 试用链接

[streamlit](https://o1s.leez.tech)
[cloudfare worker](https://o1.leez.tech)

## 致谢

特别感谢 [bklieger-groq](https://github.com/bklieger-groq) 提供的原始g1-prototype项目,为本项目的开发提供了基础。

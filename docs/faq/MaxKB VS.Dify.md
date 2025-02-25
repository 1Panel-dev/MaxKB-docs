!!! Abstract ""

    MaxKB 和 Dify 都是基于大语言模型技术的开源项目，两者在产品定位以及能力上存在差异：

    - 产品定位不同：Dify 定位于大模型应用的开发平台，属于中间件范畴；MaxKB 定位于基于大模型和 RAG 的智能问答助手，属于开箱即用的最终应用。
    - 产品能力对比：以下表格是 Dify 官方提供的与 LangChain、Flowise 等产品的能力对比；MaxKB 是基于LangChain构建的应用，并补齐了 LangChain 在 Workflow 和 SSO 等企业级功能上面的空白。

    <table style="width: 100%;height: 80%;">
      <tr>
        <th align="center">功能</th>
        <th align="center">Dify.AI</th>
        <th align="center">LangChain</th>
        <th align="center">Flowise</th>
        <th align="center">OpenAI Assistant API</th>
        <th align="center">MaxKB(Built on LangChain)</th>
      </tr>
      <tr>
        <td align="center">编程方法</td>
        <td align="center">API + 应用程序导向</td>
        <td align="center">Python 代码</td>
        <td align="center">应用程序导向</td>
        <td align="center">API 导向</td>
        <td align="center">API + 应用程序导向</td>
      </tr>
      <tr>
        <td align="center">支持的 LLMs</td>
        <td align="center">丰富多样</td>
        <td align="center">丰富多样</td>
        <td align="center">丰富多样</td>
        <td align="center">仅限 OpenAI</td>
        <td align="center">丰富多样</td>
      </tr>
      <tr>
        <td align="center">RAG引擎</td>
        <td align="center">✅</td>
        <td align="center">✅</td>
        <td align="center">✅</td>
        <td align="center">✅</td>
        <td align="center">✅</td>
      </tr>
      <tr>
        <td align="center">Agent</td>
        <td align="center">✅</td>
        <td align="center">✅</td>
        <td align="center">❌</td>
        <td align="center">✅</td>
        <td align="center">✅</td>
      </tr>
      <tr>
        <td align="center">工作流</td>
        <td align="center">✅</td>
        <td align="center">❌</td>
        <td align="center">✅</td>
        <td align="center">❌</td>
        <td align="center">✅</td>
      </tr>
      <tr>
        <td align="center">可观测性</td>
        <td align="center">✅</td>
        <td align="center">✅</td>
        <td align="center">❌</td>
        <td align="center">❌</td>
        <td align="center">✅</td>
      </tr>
      <tr>
        <td align="center">企业功能（SSO/访问控制）</td>
        <td align="center">✅</td>
        <td align="center">❌</td>
        <td align="center">❌</td>
        <td align="center">❌</td>
        <td align="center">✅</td>
      </tr>
      <tr>
        <td align="center">本地部署</td>
        <td align="center">✅</td>
        <td align="center">✅</td>
        <td align="center">✅</td>
        <td align="center">❌</td>
        <td align="center">✅</td>
      </tr>
    </table>
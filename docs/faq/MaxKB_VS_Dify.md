!!! Abstract ""

    MaxKB and Dify are both open-source projects based on large language model technology, with differences in product positioning and capabilities:

    - Different product positioning: Dify is positioned as a development platform for large model applications, falling into the middleware category; MaxKB is positioned as an intelligent Q&A assistant based on large models and RAG, serving as an out-of-the-box final application.
    - Product capability comparison: The following table is a capability comparison with LangChain, Flowise and other products provided by Dify's official documentation; MaxKB is an application built on LangChain that fills the gaps in enterprise-level features such as Workflow and SSO that LangChain lacks.

    <table style="width: 100%;height: 80%;">
      <tr>
        <th align="center">Features</th>
        <th align="center">Dify.AI</th>
        <th align="center">LangChain</th>
        <th align="center">Flowise</th>
        <th align="center">OpenAI Assistant API</th>
        <th align="center">MaxKB(Built on LangChain)</th>
      </tr>
      <tr>
        <td align="center">Programming Method</td>
        <td align="center">API + Application-oriented</td>
        <td align="center">Python Code</td>
        <td align="center">Application-oriented</td>
        <td align="center">API-oriented</td>
        <td align="center">API + Application-oriented</td>
      </tr>
      <tr>
        <td align="center">Supported LLMs</td>
        <td align="center">Rich variety</td>
        <td align="center">Rich variety</td>
        <td align="center">Rich variety</td>
        <td align="center">OpenAI only</td>
        <td align="center">Rich variety</td>
      </tr>
      <tr>
        <td align="center">RAG Engine</td>
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
        <td align="center">Workflow</td>
        <td align="center">✅</td>
        <td align="center">❌</td>
        <td align="center">✅</td>
        <td align="center">❌</td>
        <td align="center">✅</td>
      </tr>
      <tr>
        <td align="center">Observability</td>
        <td align="center">✅</td>
        <td align="center">✅</td>
        <td align="center">❌</td>
        <td align="center">❌</td>
        <td align="center">✅</td>
      </tr>
      <tr>
        <td align="center">Enterprise Features (SSO/Access Control)</td>
        <td align="center">✅</td>
        <td align="center">❌</td>
        <td align="center">❌</td>
        <td align="center">❌</td>
        <td align="center">✅</td>
      </tr>
      <tr>
        <td align="center">Self-hosted Deployment</td>
        <td align="center">✅</td>
        <td align="center">✅</td>
        <td align="center">✅</td>
        <td align="center">❌</td>
        <td align="center">✅</td>
      </tr>
    </table>

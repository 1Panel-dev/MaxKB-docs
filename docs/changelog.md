## 1 版本说明

!!! Abstract ""
    **版本号说明：** 像其它优秀开源项目一样，MaxKB 将保持每月发布一个新的功能版本，功能版本中如遇较为紧急或严重的 Bug，将及时推出 Bug 修复的小版本。           
    **MaxKB 版本号命名规则为：** v 大版本.功能版本. Bug 修复版本，示例如下：

    - v2.0.1 是 v2.0.0 之后的 Bug 修复版本
    - v2.1.0 是 v2.0.0 之后的功能版本

## 2 更新内容
### v2.0.0

2025 年 7 月 17 日

<table>
	<tr>
		<td bgcolor="#4B60FC" align="middle" style="font-weight:bold;color: white;width: 150px">模块</td>
        <td bgcolor="#4B60FC" align="middle" style="font-weight:bold;color: white;width: 150px">功能项</td>
		<td bgcolor="#4B60FC" align="middle" style="font-weight:bold;color: white;width: 750px">功能描述</td>
	</tr>
	<tr>
		<td rowspan="21">应用</td>
        <td rowspan="4">应用管理</td>
		<td>支持创建简单应用、高级编排应用</td>
    </tr>
    <tr>
		<td>支持以多级目录的方式分类管理应用</td>
    </tr>
    <tr>
        <td>支持控制应用访问行为，例如允许公开访问、禁止公开访问</td>
	</tr>
    <tr>
        <td>支持应用的导入与导出</td>
	</tr>
	<tr>
        <td rowspan="10">高级编排</td>
		<td>支持创建简单应用、高级编排应用</td>
    </tr>
    <tr>
        <td>
			工作流编排应用支持 AI 对话、知识库检索、问题优化、判断、指定回复、文档内容总结、文本转语音、语音转文本、图片理解、图片生成、表单收集、MCP 等节点	
		</td>
	</tr>
    <tr>
        <td>支持提问时上传文本、图片、语音等类型文件</td>
	</tr>
    <tr>
        <td>支持在工作流中引用工具</td>
	</tr>
    <tr>
        <td>支持在工作流中嵌套其它应用</td>
	</tr>
    <tr>
        <td>支持多出多进和并行执行</td>
	</tr>
    <tr>
        <td>支持全局变量</td>
	</tr>
    <tr>
        <td>支持自动保存以及恢复历史版本</td>
	</tr>
    <tr>
        <td>支持语音输入自动发送和自动播放</td>
	</tr>
    <tr>
        <td>支持自定义思考过程的标签，配置是否输出思考过程</td>
	</tr>
    <tr>
        <td rowspan="1">问答嵌入</td>
		<td>支持问答嵌入第三方应用</td>
    </tr>
    <tr>
        <td rowspan="2">访问限制</td>
		<td>支持按客户端限制每天提问次数限制</td>
    </tr>
    <tr>
        <td>支持嵌入第三方访问白名单设置</td>
	</tr>
    <tr>
        <td rowspan="2">显示设置</td>
		<td>支持提问时显示知识来源</td>
    </tr>
    <tr>
        <td>支持设置中问答页面的语言设置</td>
	</tr>
    <tr>
        <td rowspan="2">统计看板</td>
		<td>支持按时间统计用户数、提问次数、Tokens 总数、用户满意度</td>
    </tr>
    <tr>
        <td>支持用户数、提问次数、Tokens 总数和用户满意度指标的趋势统计</td>
	</tr>
    <tr>
		<td rowspan="12">知识库</td>
        <td rowspan="1">知识库管理</td>
		<td>支持通用型文件知识库，Web 站点文档知识库</td>
    </tr>
    <tr>
        <td rowspan="6">文档管理</td>
		<td>支持上传文本文件文档，包括 Markdown、TXT、DOCX、PDF、HTML、XLSX、XLS、CSV 格式</td>
    </tr>
    <tr>
        <td>支持上传 QA 问答对，并提供 QA 问答对模板</td>
	</tr>
    <tr>
        <td>支持文本文件和离线图片 ZIP 格式的上传和导出</td>
	</tr>
    <tr>
        <td>支持知识库文档的启用状态调整，开启或关闭文档</td>
	</tr>
    <tr>
        <td>支持知识库文档的命令处理方式，如模型优化、直接回答</td>
	</tr>
    <tr>
        <td>支持知识库导出文档</td>
	</tr>
    <tr>
        <td rowspan="3">文档分段</td>
		<td>支持文档智能分段、高级分段方式</td>
    </tr>
    <tr>
        <td>支持自定义正则表达式分段</td>
	</tr>
    <tr>
        <td>支持知识库文档分段迁移</td>
	</tr>
    <tr>
        <td rowspan="2">问题管理</td>
		<td>支持问题和文档分段关联</td>
    </tr>
    <tr>
        <td>支持知识库自动生成关联问题</td>
	</tr>
    <tr>
		<td rowspan="4">工具</td>
        <td rowspan="4">工具管理</td>
		<td>支持通过 Python 函数，自定义工具</td>
    </tr>
    <tr>
        <td>支持从工具商店中导入创建</td>
	</tr>
    <tr>
        <td>支持工具多级目录分类管理</td>
	</tr>
    <tr>
        <td>支持工具的导出和导入</td>
	</tr>
    <tr>
		<td rowspan="4">模型</td>
        <td rowspan="4">模型供应商对接</td>
		<td>支持对接主流的大模型，包括包括本地私有大模型（Llama 3 / Qwen 2 等）、国内公共大模型（通义千问 / 智谱 AI / 百度千帆 / Kimi / DeepSeek 等）和国外公共大模型（OpenAI / Azure OpenAI / Gemini 等）</td>
    </tr>
    <tr>
        <td>支持大语言模型、向量化模型、重排模型、语音识别、语音合成、图片理解和图片生成模型</td>
	</tr>
    <tr>
        <td>支持自定义模型参数设置</td>
	</tr>
    <tr>
        <td>支持模型的权限</td>
	</tr>
    <tr>
		<td rowspan="20">系统管理</td>
        <td rowspan="1">系统语言</td>
        <td>支持简体中文、繁体中文和英文三种语言</td>
    </tr>
    <tr>
        <td rowspan="3">用户管理</td>
        <td>支持用户创建/删除、启用/禁止、密码修改</td>
    </tr>
    <tr>
        <td>支持 LDAP、CAS、OIDC 、OAuth2 对接（X-Pack）</td>
	</tr>
    <tr>
        <td>支持企业微信、钉钉、飞书扫码登录（X-Pack）</td>
	</tr>
    <tr>
        <td rowspan="1">工作空间</td>
        <td>支持按工作空间方式对用户、资源进行独立管理（X-Pack）</td>
    </tr>
    <tr>
        <td rowspan="2">角色管理</td>
        <td>支持系统管理员、工作空间管理员、普通用户内置角色</td>
    </tr>
    <tr>
        <td>支持自定义角色并关联权限控制以及用户成员（X-Pack）</td>
	</tr>
    <tr>
        <td rowspan="1">资源管理</td>
        <td>支持查看应用、知识库、工具和模型等所有系统资源（X-Pack）</td>
    </tr>
    <tr>
        <td rowspan="1">资源授权</td>
        <td>支持对应用、知识库、工具和模型等所有系统资源按角色或自定义授权</td>
    </tr>
    <tr>
        <td rowspan="1">共享资源</td>
        <td>支持创建和管理知识库、工具、模型等共享资源（X-Pack）</td>
    </tr>
    <tr>
        <td rowspan="3">对话用户</td>
        <td>支持创建和同步对话用户（X-Pack）</td>
    </tr>
    <tr>
        <td>支持对话用户组的创建和成员管理（X-Pack）</td>
	</tr>
    <tr>
        <td>支持通过 LDAP、CAS、OIDC、OAuth2 等方式进行对话用户的登录认证（X-Pack）</td>
	</tr>
    <tr>
        <td rowspan="3">系统设置</td>
        <td>支持对接邮箱</td>
    </tr>
    <tr>
        <td>支持自定义系统 Logo 、登录 Logo、主题配色、登录背景图、系统名称和欢迎语以及系统帮助链接（X-Pack）</td>
    </tr>
    <tr>
        <td>支持通过 LDAP、CAS、OIDC、OAuth2、扫码登录等方式进行登录认证（X-Pack）</td>
    </tr>
    <tr>
        <td rowspan="1">操作日志</td>
        <td>支持查看所有用户的操作详情（X-Pack）</td>
    </tr>
</table> 
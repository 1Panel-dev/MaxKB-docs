## 1 Adding a Model

!!! Abstract ""
    Select the model provider as `Amazon Bedrock` and enter the following necessary information in the model addition dialog:

    * Model Name: Custom model name in MaxKB.
    * Permission: Divided into private and public permissions. Private models are only available to the current user, while public models can be used by all users within the system, but other users cannot edit or delete them.
    * Model Type: Large language model/Vector large model.
    * Base Model: The names of LLM models supported by Amazon Bedrock. The drop-down option includes commonly used large language model names and supports custom input.
    * Region Name: The region where the model is activated.
    * Access Key ID/Secret Access Key: The Access Key ID and Secret Access Key are credentials used to authenticate programmatic access to AWS services, including Amazon Bedrock.

## 2 Configuration Example

!!! Abstract ""
    Example of Amazon Bedrock - Large Language Model configuration:

![AWS LLM Model](../../img/model/AWS_LLM.png){ width="500px" }

!!! Abstract ""
    Example of Amazon Bedrock - Vector Model configuration:

![AWS Vector Model](../../img/model/aws_embed.png){ width="500px" }

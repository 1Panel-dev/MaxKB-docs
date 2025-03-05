## 1 Adding a Model

!!! Abstract ""
    Before adding an Azure OpenAI large model, you need to register in [Azure AI Studio](https://ai.azure.com/) and obtain information regarding the API domain, API Key, deployment details, etc. Refer to the image below:

![Azure OpenAI Key](<../../img/model/Azure_APIKey.png>)
![Azure OpenAI Deployment Info](<../../img/model/Azure_deployInfo.png>)

!!! Abstract ""
    Select the model provider as `Azure OpenAI` and enter the following necessary information in the model addition dialog:

    * Model Name: Custom model name in MaxKB.
    * Permission: Divided into private and public permissions. Private models are only available to the current user, while public models can be used by all users within the system, but other users cannot edit or delete them.
    * Model Type: Large language model/Vector model/Speech recognition/Speech synthesis/Image understanding/Image generation.
    * Base Model: The specific base model is determined by the deployment name, as shown in the above image.
    * API Version: Model version.
    * API Domain: The URL of the API service for the Azure OpenAI project, as shown in the above image.
    * API Key: The authentication information for the Azure OpenAI project API service, as shown in the above image.
    * Deployment Name: The deployment name of the model in Azure AI Studio's project playground.

## 2 Configuration Example

!!! Abstract ""
    Example of Azure OpenAI - Large Language Model configuration:

![Azure Large Language Model](../../img/model/azure_model.png)

## 1 Adding a Model

!!! Abstract ""
    Before adding a Gemini large model, you need to create an API Key in [Google AI Studio](https://aistudio.google.com/).
![Gemini API Key](../../img/model/gemini_key.png)

!!! Abstract ""
    Select the model provider as `Gemini` and enter the following necessary information in the model addition dialog:

    * Model Name: Custom model name in MaxKB.
    * Permission: Divided into private and public permissions. Private models are only available to the current user, while public models can be used by all users within the system, but other users cannot edit or delete them.
    * Model Type: Large language model/Vector model/Speech recognition/Image understanding.
    * Base Model: The name of the base model under different types, with a drop-down option for some commonly used base model names, and supports custom input.
    * API Key: Obtain the API Key.

    **Note:** To use the Gemini API, ensure that the server where the program is located is in a [region supported by Gemini API](https://ai.google.dev/gemini-api/docs/available-regions?hl=en), otherwise you cannot call the API and access Google AI Studio.

## 2 Configuration Example

!!! Abstract ""
    Example of Gemini - Large Language Model configuration:

![Gemini Large Language Model](../../img/model/gemini_llm.png){ width="500px" }

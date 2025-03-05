## 1 Download the Model

!!! Abstract ""
    **Prerequisite:** Download the model to the server and mount it to the MaxKB container. Using a vector model as an example, the detailed explanation is as follows.

    (1) Download the vector model to the local server.
    ```
    # Recommended model download website
    https://huggingface.co/models?other=text-embedding
    # After downloading, store it in the /opt/maxkb/model/local_embedding directory
    ```
    (2) Use -v to mount the host model path inside the MaxKB container.
    ```
    -v /opt/maxkb/model/local_embedding:/opt/maxkb/model/local_embedding
    # Note: v Host model directory: MaxKB container internal directory
    ```

## 2 Add the Model

!!! Abstract ""
    In the model management, click on the supplier [Local Model] to directly proceed to the next step and fill out the form for the local model.

    * Model Name: Custom model name in MaxKB.
    * Permission: Divided into private and public permissions. Private models are only available to the current user, while public models can be used by all users within the system, but other users cannot edit or delete them.
    * Model Type: Vector model/Reranker model.
    * Base Model: The absolute path of the model in the MaxKB container.
    * Model Directory: The directory of the model (this takes effect when the base model is a name; if the base model has an absolute path, this parameter does not take effect, and it's recommended to match it with the base model).

## 3 Configuration Example

!!! Abstract ""
    Example of configuration for a local model - Vector Model:
![Local Vector Model](../../img/model/local_embed.png){ width="500px" }

!!! Abstract ""
    Example of configuration for a local model - Reranker Model:
![Local Reranker Model](../../img/model/local_reranker.png){ width="500px" }

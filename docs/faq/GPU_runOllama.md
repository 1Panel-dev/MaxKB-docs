# How to Run LLM Models on Ollama Using GPU

!!! Abstract ""
    Using NVIDIA as an example, this guide explains the specific steps to run large models on Ollama in GPU mode.

## 1 Install NVIDIA Container Toolkit

!!! Abstract ""
    Using Ubuntu 22.04 as an example (for other systems, please refer to the [NVIDIA official documentation](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/arch-overview.html))

    - Configure the apt source
    ```
    curl -fsSL https://nvidia.github.io/libnvidia-container/gpgkey | sudo gpg --dearmor -o /usr/share/keyrings/nvidia-container-toolkit-keyring.gpg \
    && curl -s -L https://nvidia.github.io/libnvidia-container/stable/deb/nvidia-container-toolkit.list | \
        sed 's#deb https://#deb [signed-by=/usr/share/keyrings/nvidia-container-toolkit-keyring.gpg] https://#g' | \
        sudo tee /etc/apt/sources.list.d/nvidia-container-toolkit.list
    ```
    - Update the source
    ```
    sudo apt-get update
    ```
    - Install the toolkit
    ```
    sudo apt-get install -y nvidia-container-toolkit
    ```

## 2 Run Ollama Using GPU

!!! Abstract ""
    ```
    # Run the Ollama container in the background mode and allow the container to access all available NVIDIA GPUs on the host
    docker run --gpus all -d -v /opt/ai/ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
    ```

## 3 Download Models Using Ollama

!!! Abstract ""
    ```
    # Download and run models online
    docker exec -it ollama ollama run qwen:7b
    ```

## 4 Add Ollama Models in MaxKB

!!! Abstract ""
    Once the models are downloaded and the model service is running, you can add the corresponding models in MaxKB and use them.
![Add Model](../img/FAQ/addmodel.png)

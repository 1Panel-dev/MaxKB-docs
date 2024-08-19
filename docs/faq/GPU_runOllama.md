# 如何让Ollama使用GPU运行LLM模型

!!! Abstract ""
    说明：以 GPU 模式运行 Ollama 需要有 NVIDIA 显卡支持。

## 1 安装英伟达容器安装包

!!! Abstract ""
    我们以 Ubuntu22.04 为例（其他系统请参考：[英伟达官方文档](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/arch-overview.html)）

    - 配置apt源
    ```
    curl -fsSL https://nvidia.github.io/libnvidia-container/gpgkey | sudo gpg --dearmor -o /usr/share/keyrings/nvidia-container-toolkit-keyring.gpg \
    && curl -s -L https://nvidia.github.io/libnvidia-container/stable/deb/nvidia-container-toolkit.list | \
        sed 's#deb https://#deb [signed-by=/usr/share/keyrings/nvidia-container-toolkit-keyring.gpg] https://#g' | \
        sudo tee /etc/apt/sources.list.d/nvidia-container-toolkit.list
    ```
    - 更新源
    ```
    sudo apt-get update
    ```
    - 安装工具包
    ```
    sudo apt-get install -y nvidia-container-toolkit
    ```
## 2 使用 GPU 运行 Ollama

!!! Abstract ""
    ```
    docker run --gpus all -d -v /opt/ai/ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
    ```

## 3 使用 Ollama 下载模型

!!! Abstract ""
    ```
    docker exec -it ollama ollama run qwen:7b
    ```

## 4 在 MaxKB 的模型设置中添加模型进行对接

![添加模型](../img/FAQ/addmodel.png)
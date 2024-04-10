
# Ziya-LLaMA-13B

## 环境按照

模型下载

Ziya-LLaMA-13B-v1.1 和 llama2 13B下载

https://huggingface.co/IDEA-CCNL/Ziya-LLaMA-13B-v1.1

## python虚拟环境搭建

```bash
> cd /opt/Data/PythonVenv
> python3 -m venv ZiyaLLaMA13B
> source /opt/Data/PythonVenv/ZiyaLLaMA13B/bin/activate
> pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple
> pip install transformers==4.31.0 protobuf accelerate llama2-wrapper -i https://pypi.tuna.tsinghua.edu.cn/simple
> 
```

## 模型合并

```bash
> python3 -m apply_delta.py --base ~/model_weights/llama-13b --target ~/model_weights/Ziya-LLaMA-13B --delta ~/model_weights/Ziya-LLaMA-13B-v1
>
> python3 fengshen/utils/apply_delta.py --base /opt/Data/ModelWeight/meta/llama1.hf/llama1-13b-hf --target /opt/Data/ModelWeight/IDEA-CCNL/Ziya-LLaMA-13B --delta /opt/Data/ModelWeight/IDEA-CCNL/Ziya-LLaMA-13B-v1
>
```

启动jupyter
```bash
> jupyter notebook --no-browser --port 7001 --ip=192.168.2.199
> jupyter notebook --no-browser --port 7000 --ip=192.168.2.200
```

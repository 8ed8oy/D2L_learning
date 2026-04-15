### 环境配置
```shell
conda create -n d2l python=3.9 -y
conda activate d2l
conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia
pip install d2l==1.0.3
conda install jupyter notebook
```

ssh时选择内核需要安装ipykernel
```shell
# 激活你的环境
conda activate d2l

# 安装内核工具
conda install ipykernel -y

# 将该环境注册到 Jupyter 的 kernels 列表中
# --name 后面是环境名，--display-name 后面是在 VS Code 里看到的名称
python -m ipykernel install --user --name d2l --display-name "Python (d2l)"
```
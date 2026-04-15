# 深度学习计算 - 常用操作

本章聚焦PyTorch常用操作的核心概念与关键代码。

---

## 目录导航

| 文件 | 主题 | 核心内容 |
|------|------|---------|
| [01_模型设计](./01_模型设计.md) | 层和块、自定义层 | Sequential、Module、自定义层实现 |
| [02_参数管理](./02_参数管理.md) | 参数访问与初始化 | 参数访问、初始化策略、延迟初始化 |
| [03_模型持久化](./03_模型持久化.md) | 模型读写 | 张量存储、模型参数保存/加载 |
| [04_计算优化](./04_计算优化.md) | GPU加速 | 设备管理、GPU计算、多GPU支持 |

---

## 与其他章节的关联

### 前置知识
- 3.线性神经网络 - 基础模型架构
- 4.多层感知机 - 完整网络设计

### 后续应用
- 6.卷积神经网络 - 使用自定义层和参数共享
- 7.递归神经网络 - 延迟初始化和参数绑定
- 8.注意力机制 - 复杂块组合
- 所有高级模型 - 参数管理和模型持久化

---

## 快速查阅

### 核心概念表

| 概念 | 定义 | 常用方法 |
|------|------|---------|
| Module | PyTorch神经网络基类 | `nn.Module` |
| Sequential | 顺序执行层的容器 | `nn.Sequential()` |
| Layer | 具有参数的计算单元 | `nn.Linear`, `nn.Conv2d` |
| Parameter | 可训练的权重/偏置 | `nn.Parameter()` |
| State Dict | 模型参数字典 | `state_dict()`, `load_state_dict()` |
| Device | 计算设备 | `torch.device('cpu')`, `torch.device('cuda')` |

### 常用操作速查

| 操作 | 代码示例 |
|------|---------|
| 创建顺序模型 | `nn.Sequential(nn.Linear(10, 20), nn.ReLU())` |
| 自定义层 | `class MyLayer(nn.Module): ...` |
| 访问参数 | `net[0].weight`, `net.named_parameters()` |
| 初始化参数 | `nn.init.xavier_uniform_(param)` |
| 保存模型 | `torch.save(net.state_dict(), 'model.pt')` |
| 加载模型 | `net.load_state_dict(torch.load('model.pt'))` |
| 指定GPU | `net.to(torch.device('cuda:0'))` |

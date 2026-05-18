# 基于奇函数与正则化的对抗攻击方法

## 项目说明

本项目实现了一种基于奇函数与正则化的对抗攻击方法（Unified Odd Descent with Regularization, UODR）。该方法通过结合奇函数特性和正则化技术，对深度神经网络进行对抗攻击研究。

### 核心技术

- **奇函数优化**：利用奇函数的对称性质进行梯度优化
- **正则化方法**：通过正则化技术提高攻击的稳定性和有效性
- **对抗攻击**：实现 PGD（Projected Gradient Descent）等经典对抗攻击算法
- **梯度优化**：支持多种优化器（Adam, Adagrad, RMSprop）

### 应用场景

- 深度学习模型安全性评估
- 对抗样本生成与研究
- 模型鲁棒性分析

## 项目目录结构

```
Unified-Odd-Descent/
├── README.md                    # 项目说明文档
├── UODR.ipynb                   # 主实验 Notebook
├── helpers.py                   # 辅助函数（优化算法、数据处理）
├── helpers1.py                  # 辅助函数扩展
├── models.py                    # 神经网络模型定义（CNN, FCNN）
├── install.sh                   # 环境安装脚本
├── configs/                     # 配置文件目录
│   ├── adv_MNIST_clean_config.py    # MNIST 干净模型配置
│   └── adv_MNIST_pgd_config.py      # MNIST PGD 攻击配置
├── data/                        # 数据集目录
│   └── MNIST/                   # MNIST 数据集
└── models/                      # 预训练模型目录
    ├── mnist_clean_epochs_20                # 干净模型
    └── mnist_pgd_epsilon_0.25_steps_20_epochs_20  # PGD 对抗训练模型
```

## 项目声明

| 项目信息 | 详情 |
|---------|------|
| **项目名称** | 基于奇函数与正则化的对抗攻击方法 |
| **项目作者** | Zheng-Sen Zhou |
| **作者单位** | 暨南大学网络空间安全学院 |
| **开发语言** | Python |
| **深度学习框架** | PyTorch |
| **核心技术** | 奇函数优化、正则化、对抗攻击（PGD）、梯度优化 |

## 环境配置

### 依赖环境

- Python 3.7.15
- PyTorch 1.13.0+cu116
- torchvision 0.14.0+cu116
- scipy 1.7.3
- torchattacks 3.3.0
- numpy 1.21.6

### 安装步骤

```bash
# 使用 conda 创建环境
conda create --name UODRGD python=3.7.15 -y
conda activate UODRGD

# 安装 PyTorch（CUDA 11.6）
pip install torch==1.13.0+cu116 torchvision==0.14.0+cu116 torchaudio==0.13.0 --extra-index-url https://download.pytorch.org/whl/cu116

# 安装其他依赖
pip install scipy==1.7.3 torchattacks==3.3.0 numpy==1.21.6
```

或者直接运行安装脚本：

```bash
bash install.sh
```

## 使用方法

1. 克隆仓库
```bash
git clone https://github.com/your-username/Unified-Odd-Descent.git
cd Unified-Odd-Descent
```

2. 配置环境
```bash
bash install.sh
```

3. 运行实验
```bash
jupyter notebook UODR.ipynb
```

## 代码统计

| 文件类型 | 文件数 | 代码行数 |
|---------|-------|---------|
| Python (.py) | 6 | 1,231 |
| Jupyter Notebook (.ipynb) | 1 | 894 |
| Shell 脚本 (.sh) | 1 | 4 |
| **总计** | **8** | **2,165** |

## 许可证

本项目仅供学术研究使用。

## 联系方式

如有问题，请联系项目作者：Zheng-Sen Zhou（暨南大学网络空间安全学院）

# Reproducibility-PIRBN

本仓库基于 PaddlePaddle/PaddleScience 复现论文中提出的 PIRBN 模型，包含在多个设置下的实验、对比 PINN 基线，并提供完整的 Jupyter Notebook、代码和结果。

## 环境依赖

- Python 3.8  
- Conda 环境：`pirbn_paddle`  
- 安装依赖：
  ```bash
  conda activate pirbn_paddle
  pip install paddlepaddle==2.6.0 -i https://pypi.tuna.tsinghua.edu.cn/simple
  pip install paddlesci -i https://pypi.tuna.tsinghua.edu.cn/simple
  conda install -c conda-forge notebook ipykernel jupyterlab -y

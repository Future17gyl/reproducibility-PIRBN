# Reproducibility-PIRBN

基于 PaddlePaddle/PaddleScience 复现论文中提出的 PIRBN 模型，包含 Baseline 实验、多频扩展实验及与 PINN 的对比研究。

### 团队成员
- ZY2406436 – 郭奕朗  
- ZY2406438 – 贾旭明  

---

## 环境依赖

- 创建并激活 Conda 环境  
  - conda create -n pirbn_paddle python=3.8 -y
  -  conda activate pirbn_paddle
- 安装核心库  
  - pip install paddlepaddle==2.6.0 paddlesci numpy matplotlib -i https://pypi.tuna.tsinghua.edu.cn/simple
- 安装 Notebook 支持  
  - conda install -c conda-forge notebook ipykernel jupyterlab -y 

---

## 项目结构

- reproducibility-PIRBN/  
  - README.md  
  - notebooks/  
    - 01_run_baseline.ipynb 论文中 µ=4,8；right_by=0,100 的 4 组默认实验  
    - 02_additional_runs.ipynb µ=2,16 两组额外频率扩展实验  
    - 03_compare_pinn.ipynb PIRBN vs 单隐藏层 PINN 对比实验  
  - src/  
    - PIRBN/ 官方示例源码（main.py、train.py 等）  
  - data/ （可选）数据或中间结果文件  

---

## 使用步骤

1. 克隆仓库并进入  
   git clone https://github.com/Future17gyl/reproducibility-PIRBN.git  
   cd reproducibility-PIRBN
2. 启动 JupyterLab  
   conda activate pirbn_paddle
   jupyter lab
3. 依次打开并运行以下 Notebook  
   - 01_run_baseline.ipynb
   - 02_additional_runs.ipynb
   - 03_compare_pinn.ipynb
4. 查看输出  
   - 训练日志  
   - Loss 曲线  
   - 预测与真实值对比图  

---

## 实验摘要

- **Baseline** µ=4, 8 × right_by=0, 100  
- **多频扩展** µ=2, 16  
- **对比实验** PIRBN final loss ≈ 0.136 vs PINN final loss ≈ 0.593  

详细结果和图表请查看对应 Notebook。
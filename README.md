# The code for DBPINN!

## Environmental requirements
- tensorflow == 1.15.0
- python == 3.6.15 
- numpy == 1.19.5
- sqlite == 3.39.0 

## How to run 
Using the Allen-Cahn equation as an example
`python AC_DB.py or  nohup python -u AC_DB.py > AC_DB.log 2>&1 &`.

## Citing DBPINN
- This section will be updated immediately once our paper is accepted.

If you have any questions, please feel free to raise "issues" for discussion.

## Abstract
```
近年来,物理信息神经网络(Physics-Informed Neural Networks, PINNs)在求解非线性偏微分方程(Partial Differential Equations, PDEs)中得到了大量应用. PINNs将物理信息作为正则化约束加入神经网络损失函数,可以减少传统神经网络方法对训练数据的大量依赖.然而,PINNs 无法根据数据变化动态调整损失函数中各个损失项的权重,导致其在求解非线性 PDEs 时存在求解误差较大的问题.为此,本文提出了一种动态平衡物理信息神经网络(Dynamic Balanced PINNs, DBPINN).首先,DBPINN 为 PINNs 损失函数的各个损失项设计了一种动态权重系数,并使用随机函数对该系数进行动态更新,使得 PINNs 各损失项的梯度下降速度得以平衡. 其次, DBPINN 为 PNNNs 损失函数的各个损失项之间建立了一种平衡求和方法,该方法考虑了各损失项之间的竞争关系,使得 PINNs 各损失项朝着有利于收敛的方向进行优化. DBPINN 通过动态权重系数和平衡求和方法使得 PINNs 各损失项可以更好地进行优化,进而解决了 PINNs 在实际应用中求解误差较大的问题.本文选择了科学机器学习领域中四个经典的非线性 PDEs 对 DBPINN 进行了数值验证和分析.实验结果表明,相比于 PINN, DBPINN 在 Schrodinger 和 Allen-Cahn 方程上误差分别降低了46\%和64\%. DBPINN 在求解 Navier-Stokes 方程时将系数 $\lambda_{1}$ 和系数 $\lambda_{2}$ 的误差分别降低了1至2个数量级和约50%. DBPINN 在 KdV 方程中能够在多项系数中将误差降低1个数量级.最后,本文在多种形式的 Burgers 方程和Allen-Cahn方程上进行性能和参数消融验证,结果表明 DBPINN 不仅能够提升模型性能、处理小数据量以及拟合不同时间状态下的方程的能力,而且DBPINN相比于PINN具有更好的稳定性、准确率以及收敛性}. DBPINN 可以取代 PINNs 被应用于各种非线性 PDEs 的高精度求解,源代码见于:https://github.com/Xiaojiuwo168/DBPINN/.
```

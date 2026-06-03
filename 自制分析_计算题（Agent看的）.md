计算题:

·数字图像的存储空间（例：一幅空间分辨率为 1024 像素×768 像素的真彩色图像，无压缩存储时至少占用多大的存储空间？如果为标准 4K 分辨率 4096 像素×2160 像素，又至少占用多大的存储空间？）

![](https://cdn-mineru.openxlab.org.cn/result/2026-06-03/e326ace8-17ea-4903-b612-d88d81f915c6/25ae9954067b2cb7e7253c9bde7e61c719f77e16bfee1c1bdff7c094137e2ac0.png)

·数字图像中像素间的空间关系（例：假设我们有一个3x3的二值图像区域，其中像素值为1表示白色，像素值为0表示黑色。判断4邻接、8邻接、m邻接关系）

·击中击不中运算（例：给一幅简单的5x5二值图像和2x2的结构元素 B。算进行击中击不中变换结果。如果是5x5的图像，结果会是4x4的图）。公式： $\left(A\ominus B_{1}\right)\cap \left(A^{c}\ominus B_{2}\right)$ （但其实对做题没有什么用，本质上对拼图游戏）

·直方图均匀化（例：使用公式 $s_{k}=T\left(r_{k}\right)=(L-1)\sum_{j=0}^{k}p\left(r_{j}\right) \quad$ 如下图灰度等级L=10，像素数量n=64。根据公式只举例s0、s8、s9。记得要四舍五入，其他的是一个道理：

$$
s_{0}=9\times 2/64=0.2813,近似取0
$$

$$
\begin{matrix}s_{8}&=9\times (2/64+2/64+3/64+5/64+16/64+14/64+13/64+5/64+\\&2/64)=8.7188(近似取9)\end{matrix}
$$

$$
\begin{matrix}s_{9}&=9\times (2/64+2/64+3/64+5/64+16/64+14/64+13/64+5/64+\\&2/64+2/64)=9\end{matrix}
$$

）

<table><thead><tr><th><p>灰度级</p></th><th><p>0</p></th><th><p>1</p></th><th><p>2</p></th><th><p>3</p></th><th><p>4</p></th><th><p>5</p></th><th><p>6</p></th><th><p>7</p></th><th><p>8</p></th><th><p>9</p></th></tr><tr><th><p>像素个数</p></th><th><p>2</p></th><th><p>2</p></th><th><p>3</p></th><th><p>5</p></th><th><p>16</p></th><th><p>14</p></th><th><p>13</p></th><th><p>5</p></th><th><p>2</p></th><th><p>2</p></th></tr></thead></table>

·深度学习的评价指标，需要掌握计算精确率（Precision）、召回率（Recall）、准确率（Accuracy）、错误率（Error Rate）、F1值（F-measure）

<table><thead><tr><th><p><strong>实际值\预测值</strong></p></th><th><p><strong>预测为正样本</strong></p></th><th><p><strong>预测为负样本</strong></p></th></tr></thead><tbody><tr><td><p>实际为正样本</p></td><td><p>TP</p></td><td><p>FN</p></td></tr><tr><td><p>实际为负样本</p></td><td><p>FP</p></td><td><p>TN</p></td></tr></tbody></table>

$$
ErrorRate=\frac{FP+FN}{TP+FP+FN+TN}
$$

$$
Accuracy=\frac{TP+TN}{TP+FP+FN+TN}
$$

$$
Recall=\frac{TP}{TP+FN}
$$

$$
Precision=\frac{TP}{TP+FP}
$$

$$
F1=\frac{2*Precision*Recall}{Precision+Recall}
$$
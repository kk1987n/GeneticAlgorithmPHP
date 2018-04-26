# PHP版遗传算法-步骤
### ①初始化一个种群
包含16个扇贝，每个扇贝包含32*32个像素点，每个像素点包含4个通道，rgb-a。每个扇贝的适应度计算出来作为扇贝的属性。
### ②淘汰2个扇贝
通过冒泡排序（16个扇贝，就不考虑效率了），淘汰适应度最差的2个扇贝。
### ③交叉生成2个新扇贝
上步剩余的14个扇贝，前7个后7个各随机挑出来1个进行交叉。
### ④交叉基因算法
新扇贝从(0,0)到(32,32)，每个点对半概率从扇贝1和扇贝2中得到基因，此时获取到了一个50%概率父母各一半基因的新扇贝。
### ⑤变异新扇贝
新扇贝上随机取出2个坐标点，随机其颜色值
### ⑥重建种群
把新生成的2个扇贝加入到14个扇贝中组成新的一代
### ⑦计算本代适应度总和
本步骤与GA没有太大关系，计算这一代16个扇贝的适应度总和（跟求平均值一个意思），这样可以用来画适应度曲线图。



1. ### 背景 

实验心理学中的典型现象—— 斯特鲁普效应。

### 概述

​        这个效应展示了人们对事物认知过程已是一个自动化的历程。当有一个新的刺激出现时，如果它的特征和原先的刺激相似或符合一致，便会加速人们的认知；反之，若新的刺激特征与原先的刺激不相同，则会干扰人们的认知，使人们的所需的反应时间，在心理学中，斯特鲁普效应是干扰对处理任务时反应时间的论证。

​        在一个 Stroop （斯特鲁普）任务中，参与者得到了一列文字，每个文字都用一种油墨颜色展示。参与者的任务是将文字的打印颜色大声说出来。这项任务有两个条件：一致文字条件，和不一致文字条件。在一致文字条件中，显示的文字是与它们的打印颜色匹配的颜色词。在不一致文字条件中，显示的文字是与它们的打印颜色不匹配的颜色词。在每个情况中，我们将计量说出同等大小的列表中的墨色名称的时间。每位参与者必须全部完成并记录每种条件下使用的时间。

### 分析

#### 1 数据来源

由课程内容方提供，[斯普鲁斯效应的实验数据来源](https://d17h27t6h515a5.cloudfront.net/topher/2016/September/57ce3363_stroopdata/stroopdata.csv) 

#### 2 因变量

说出同等大小的列表中的墨色名称的时间。

####3 处理措施

文字条件，一致文字条件和不一致文字条件

#### 4 样本数据分析
![](http://images.cronusliang.me/ML/statistics/sample_data_1.png)  
Incongruent情况下所用时间均大于Congruent情况

![](http://images.cronusliang.me/ML/statistics/sample_data_3.png)
#### 5 假设和检验方法

虽然这个数据来自某个样本，但是我们假设它代表了整个总体情况，所以 “一致”情况的总体均值 μ<sub>con</sub> ;不一致情况的总体均值μ<sub>incon</sub> 

- 设立假设

 null -> H<sub>0</sub> (零假设): “一致”情况和“不一致”情况说出同等大小的列表中的墨色名称的时间没有显著差异(μ<sub>con</sub> = μ<sub>incon</sub>)   

 ALL ->  H<sub>a</sub> (对立假设)：“一致”情况和“不一致”情况说出同等大小的列表中的墨色名称的时间有显著差异
(μ<sub>con</sub> ≠ μ<sub>incon</sub>)  

- 检验类型    


	实验是同一批参与者在不同条件下的试验，所以是相依样本  
	因为只有样本数据，而不清楚总体的情况，所以用t检验  
	因为试验考虑两种情况下，事件是否有差异，所以没有方向，为双尾检验

- 检验的前提条件分析  
   t检验的前提条件是，即正态性和方差齐性。

   对两个样本的分析，其均表现出类似正态分布（如下图所示）。且样本为随机样本，故可以合理推测其总体是正态分布。

![](http://images.cronusliang.me/ML/statistics/congruent.png)

![](http://images.cronusliang.me/ML/statistics/Incongruent.png)

   因为是让同一个受试者参与两组条件稍有不同（但其它变量受控）所得出的两个样本数据，可以合理推测其总体方差相似。  


- 假设从受试的样本得知 n = 24  
    则自由度 df = n-1 = 23   

- α水平等于0.05时的临界值  
  ​	
     因为是双尾检验 查t表得： ± 2.069

- 根据样本数据算出 
  ​	
  μ<sub>incon</sub> - μ<sub>con</sub> =  22.02 -14.05= 7.97

- 标准偏差
  根据样本数据算出 s = 4.86

- 标准误差

    s<sub>em</sub> = s/√n = 4.86 /√24 = 0.99

- t统计量  

    t= (μ<sub>incon</sub> - μ<sub>con</sub>)/(s/√n) = 7.97/0.99 = 8.05

- t临界值   
   根据t分布图 t位于临界区
   ![](http://images.cronusliang.me/ML/statistics/t%28project%291.png)


    p<.05 这些结果具有统计显著性。因为p值小于0.05也就是说我们拒绝了零假设。

- cohen's d 

    d = （μ<sub>incon</sub> - μ<sub>con</sub>）/s = 7.97/4.86 = 1.63

- 效应量 r<sup>2</sup>   
    r<sup>2</sup> = t<sup>2</sup>/(t<sup>2</sup> + df) = (8.05)^2/((-8.05)^2 + 23) = .74

- 置信区间

    CI:M<sub>D</sub> ± t<sub>critical</sub>(s/√n) = (5.92,10.02)

### 结论

  通过计算，t统计值大于t临界值且P值远小于.05，可以拒绝零假设。说明两种情况下所使用的时间，有统计上的显著差异,该结果与期望一致。


### 参考

[样本数据](https://docs.google.com/spreadsheets/d/1fqvG4N3_ZqfQAqvRbesTL6QuE7CwArLFrU5t4LNpPc0/edit#gid=0 "样本数据")  
[t表](http://www.sjsu.edu/faculty/gerstman/StatPrimer/t-table.pdf "t表")  
[斯特鲁普](https://zh.wikipedia.org/wiki/%E6%96%AF%E7%89%B9%E9%B2%81%E6%99%AE%E6%95%88%E5%BA%94 "斯特鲁普")  
[直方图制作](http://www.shodor.org/interactivate/activities/Histogram/ "直方图制作")













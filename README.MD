# 美年健康预测比赛
给如一批体检人员的常规体检数据和基因数据，预测他们的血压和血脂等成分．预防医学的一种．
* 健康预测说明
一切按照说明文档提交,如有不理解，欢迎联系我．我花了三天时间做这个初赛，提交次数也就个位数, 是个遵纪守法的队员o_o．
自己运行过一遍，虽然设置了随机数种子，但是运行结果好像和提交结果不一样．然后用xgboost测试了一下，效果还好0.0283，训练测试过程见main.ipynb中的历史记录.

* 解题思路
1.肉眼观察数据,删掉缺失值过多数据，然后清洗了剩余数据．
2.手动确认了一些数值特征和一些无关特征．大部分特征都是程序抽取的．
3.xgboost和lightgbm训练后做融合，简单相加即可．
4.小trick,估计前面的人都用了．对待训练数据做log(x+1)的转换.

# 鲁棒性

## 攻击
### 黑盒
1. T.DiNoia, D.Malitesta, and F.A.Merra. 2020. TAaMR: Targeted Adversarial Attack against Multimedia Recommender Systems. In the 50th Annual IEEE/IFIP International Conference on Dependable Systems and Networks Workshops (DSN-DSML’20). 
	- http://sisinflab.poliba.it/publications/2020/DMM20/PID6442119.pdf 

### 白盒

## 防御

# 多样性

## Selection Bias评估指标

1. X. Wang, M. Bendersky, D. Metzler, and M. Najork, “Learning to rank with selection bias in personal search,” in SIGIR, 2016, pp. 115–124. 
	- https://storage.googleapis.com/pub-tools-public-publication-data/pdf/45286.pdf

2. Z. Ovaisi, R. Ahsan, Y. Zhang, K. Vasilaky, and E. Zheleva, “Correcting for selection bias in learning-to-rank systems,” in Proceedings of The Web Conference 2020, 2020, pp. 1863–1873. 
	- https://arxiv.org/pdf/2001.11358.pdf


## Exposure Bias评估指标
**Definition:** *Exposure bias happens as users are only exposed to a part of specific items so that unobserved interactions do not always represent negative preference.* 


## Position Bias评估指标

1. T. Joachims, A. Swaminathan, and T. Schnabel. 2017. Unbiased Learning-to-Rank with Biased Feedback. In WSDM. 
	- https://arxiv.org/pdf/1608.04468.pdf
	- 使用点击模型，从显式和隐式交互中估计基于位置的点击概率
	- P (ei(y) = 1| rank(y|y ̄)) · P (ci(y) = 1| ri(y), ei(y) = 1). 

2. Xuanhui Wang, Nadav Golbandi, Michael Bendersky, Donald Metzler, and Marc Najork. 2018. Position bias estimation for unbiased learning to rank in personal search. In WSDM. ACM. 
	- https://storage.googleapis.com/pub-tools-public-publication-data/pdf/3bace79f9bcead0b20dec31e2a0878346ad2fb0d.pdf

3. .	A. Agarwal, I. Zaitsev, Xuanhui Wang, Cheng Li, M. Najork, and T. Joachims. 2019. Estimating Position Bias Without Intrusive Interventions. In WSDM.
	- https://arxiv.org/pdf/1812.05161.pdf

4. Zhichong Fang, A. Agarwal, and T. Joachims. 2019. Intervention Harvesting for Context-Dependent Examination-Bias Estimation. In SIGIR. 
	- https://arxiv.org/pdf/1811.01802.pdf
	- Accurate estimates of **examination bias** are crucial for unbiased learning-to-rank from implicit feedback in search engines and recommender systems.
	- 将有关用户和查询的上下文特征合并到基于神经网络的倾向模型中，用于预测任何新查询和排名的位置偏差。
	- Pr(C = 1|q,d,k) = Pr(E = 1|k)rel(q,d)
	- Pr(C = 1|x,d,k) = Pr(E = 1|k,x)rel(x,d)  


## Fairness指标

1. Fairness Trough Unawareness
2. Individual Fairness
3. Counter-factual Fairness
4. Group Fairness

# 可解释性
- Explainable Recommendation: A Survey and New Perspectives 

1. 可解释的推荐系统，推荐系统模型自带解释模块
2. 事后解释 




# Methods for Evaluating News Recommendation System

## Purpose & Scope

Evaluation models, methods and metrics for news recommendation system.  

As news recommendation system is a specific application of recommendation system,  the evaluation method on general recommendation system can be applied while some features specified on news can also be considered

**Overall**

* evaluation "recommendation system"
  * A Survey of Accuracy Evaluation Metrics of Recommendation Tasks [JMLR'09](https://www.jmlr.org/papers/volume10/gunawardana09a/gunawardana09a.pdf)
  * Evaluating Recommendation Systems [link]()
  * Dimensions and Metrics for Evaluating Recommendation Systems [link](2014_Book_RecommendationSystemsInSoftware)
* evaluation "news recommendation system"
   * News Recommendation Systems - Accomplishments, Challenges & Future Directions [link](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=8963698)
     	* dataset/ evaluation method

## Datasets



## Environments/Experimental Settings

### Offline

### Online

**Simulator**： how human interact with in the news recommendation system

## Criteria

1. User Preference

2. Prediction Accuracy/Correctness 

3. Coverage(想让他看到)：  catalog coverage (item-space coverage) or prediction coverage (user-space coverage) 

   * Semantics
   * 

4. Confidence

5. Trust

6. Novelty

7. Serendipity: To what extent has the system succeeded in providing surprising yet
   beneficial recommendations?

8. Diversity:  How diverse (dissimilar) are the recommended items in a list?
   $$
   diversity(c_1,...,c_n) = \frac{2}{n(n-1)}\sum_{i=1}^n\sum_{j=1}^n(1-similarity(c_i,c_j))
   $$

   * Bias

9. Utility

10. Risk

11. Robustness:  How tolerant is the recommendation system to bias or false information?

    * Adversarial Robustness

12. Privacy

13. Adaptivity

14. Scalability

15. Learning rate: How fast can the system incorporate new information to update its recommendation list?

16. Usability: How usable is the recommendation system? Will it be easy for users to adopt it in an appropriate way?

*Notes: consider more on 1) deep learning method involve new evaluation aspects; 2) news recommendation*

17. Fairness? (user/item)



# 鲁棒性

## 攻击
### 黑盒
1. T.DiNoia, D.Malitesta, and F.A.Merra. 2020. TAaMR: Targeted Adversarial Attack against Multimedia Recommender Systems. In the 50th Annual IEEE/IFIP International Conference on Dependable Systems and Networks Workshops (DSN-DSML’20). 
	- http://sisinflab.poliba.it/publications/2020/DMM20/PID6442119.pdf

2. Mingdan Si and Qingshan Li. Shilling attacks against collaborative recommender systems: a review. Artificial Intelligence Review, pages 1–29, 2018.  

### 白盒

## 防御

### Shilling Attack Detection Algorithms

1. Jun Zou and Faramarz Fekri. A belief propagation approach for detecting shilling attacks in collaborative filtering. In Proceedings of the 22nd ACM international conference on Information & Knowledge Management, pages 1837–1840. ACM, 2013.  

2. Zhihai Yang, Lin Xu, Zhongmin Cai, and Zongben Xu. Re-scale adaboost for attack detection in collaborative filtering recommender systems. Knowledge-Based Systems, 100:74–88, 2016.  
3. Runa Bhaumik, Bamshad Mobasher, and Robin Burke. A clustering approach to unsupervised attack detection in collaborative recommender systems. In Proceedings of the International Conference on Data Mining, page 1. Citeseer, 2011.  
 
### Robustness of Recommender Systems 

1. Santiago Alonso, Jesús Bobadilla, Fernando Ortega, and Ricardo Moya. Robust model-based reliability approach to tackle shilling attacks in collaborative filtering recommender systems. IEEE Access, 7:41782–41798, 2019.  

2. Fuzhi Zhang, Yuanli Lu, Jianmin Chen, Shaoshuai Liu, and Zhoujun Ling. Robust collaborative filtering based on non-negative matrix factorization and r1-norm. Knowledge-based systems, 118:177–190, 2017.  
3. Hongtao Yu, Ruibo Gao, Kun Wang, and Fuzhi Zhang. A novel robust recommendation method based on kernel matrix factorization. Journal of Intelligent & Fuzzy Systems, 32(3):2101–2109, 2017.  
4. Xiangnan He, Zhankui He, Xiaoyu Du, and TatSeng Chua. Adversarial personalized ranking for recommendation. In The 41st International ACM SIGIR Conference on Research & Development in Information Retrieval, pages 355–364. ACM, 2018.  



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




# References of Risk Management

This file contains a broad list of industrial and academic articles related to detecting and mitigating risks for information systems & platforms. Currently, these articles can be grouped into several interrelated sub-topics:

- **Anomaly Detection**. Usually an indicator of risk is anomaly. So detecting anomaly can be the first step of risk management.
- **Malicious Item Detection**. Sometime we more or less know what bad items (e.g., fraud transactions, fake accounts, bot accounts) look like. So in addition to anomaly signals, we can also add domain-specific signals to detect the bad stuff.
- **Risk Mitigation and Prevention**. After detection the defender needs to act in the right way to mitigate the risk. This is not easy, because the defender has many constraints, like growth, usability, etc.
- **Risk Management System / Infrastructure**. Risk management systems are challenging to build because they need to process huge amount of data to find a few bad things with high accuracy and fast response time. 

Hope you find this reference list helpful!

Lanugage: Chinese / English

## 2019

[Characterizing and Detecting Malicious Accounts in Privacy-Centric Mobile Social Networks: A Case Study](https://dl.acm.org/citation.cfm?id=3330702)

[反欺诈之被丢掉的黄金数据](https://zhuanlan.zhihu.com/p/69694663)
- Very good feature engineering.

[数字化风控——图计算八个应用场景](https://www.iyiou.com/p/107367.html), [Part 2](http://www.sohu.com/a/331895665_467315)

## 2018

[Automated Fake Account Detection at LinkedIn](https://engineering.linkedin.com/blog/2018/09/automated-fake-account-detection-at-linkedin)

- Score everything.
- Defense in depth and in redundancy.

[Marketing "Dirty Tinder" on Twitter](https://labsblog.f-secure.com/2018/03/16/marketing-dirty-tinder-on-twitter/)
- Network analysis

[Facebook Crackdown on Fake Accounts Isn’t Solving the Problem for Everyone](https://medium.com/thewashingtonpost/facebook-crackdown-on-fake-accounts-isnt-solving-the-problem-for-everyone-fb30b0f36d4b?qHa=true)
- High quality article on the fake & impersonating account problem on Facbeook. Facebook uses facial recognition which seems not effective.

[LOBO – Evaluation of Generalization Deficiencies in Twi er Bot Classifiers](https://www.researchgate.net/profile/Gianluca_Stringhini/publication/329422016_LOBO_Evaluation_of_Generalization_Deficiencies_in_Twitter_Bot_Classifiers/links/5c0c51a3299bf139c7499d27/LOBO-Evaluation-of-Generalization-Deficiencies-in-Twitter-Bot-Classifiers.pdf)
- Found that Twitter bot classifiers do not generalize well to unseen bots.
- But the features used by external researchers and internal spam fighters are very different.

[Implementing Model-Agnosticism in Uber’s Real-Time Anomaly Detection Platform](https://eng.uber.com/anomaly-detection/)

[Anomaly Detection: Algorithms, Explanations, Applications](https://www.microsoft.com/en-us/research/video/anomaly-detection-algorithms-explanations-applications/)

- An overview of Thomas Dietterich's research on anomaly detection benchmarking, theory, and applications.

[Netflix Cloud Security: Detecting Credential Compromise in AWS](https://medium.com/netflix-techblog/netflix-cloud-security-detecting-credential-compromise-in-aws-9493d6fd373a)

- If my understanding is correct they use the trust on first use principle: if the IP of AssumedRole call is different from the first known IP of that role the call is likely from an outside IP and therefore related to compromised credential.
- They have a follow up article: [Netflix Information Security: Preventing Credential Compromise in AWS](https://medium.com/netflix-techblog/netflix-information-security-preventing-credential-compromise-in-aws-41b112c15179).

[卷积神经网络在个人信贷风险管理中的应用](https://mp.weixin.qq.com/s/kpqYRAYiePZscC-tyLtzYw)

- The main decision making model is linear and they do NOT recommend to directly use more complex machine learning models as the decision making model.
- They propose CNN as a way of ehnancing feature engineering. Particularly, CNN explores many possible feature combinations and pick promising ones. But ultimately we need human to analyze these candidates and find ones that make sense.


[腾讯交易反欺诈](https://mp.weixin.qq.com/s/uqa9zY4oUfaEMdnEmP6glg)

[信用评分模型的理解和学习](https://zhuanlan.zhihu.com/p/36263276)

## 2017

*** [Exploring New Machine Learning Models for Account Security, Uber](https://medium.com/uber-security-privacy/uber-machine-learning-account-security-3aaadef11e45)
- Semi-supervied model: use PCA + clustering to get labels of IP.
- Unsupervised model: use LSTM and word2vec to discover common travel sequences between cities.

*** [Mastermind: Using Uber Engineering to Combat Fraud in Real Time, Uber](https://eng.uber.com/mastermind/)
- Very good insights on building a global rule-based fraud prevention engine.

[Time Series Anomaly Detection: Detection of Anomalous Drops with Limited Features and Sparse Examples in Noisy Highly Periodic Data](https://arxiv.org/pdf/1708.03665.pdf)

- Two-stage architecture: predictor and anomaly-detector / comparator.
- For the predictor they used Deep Learning models like DNN, RNN, LSTM.

[Twilio Verify: The best phone verification solution](https://www.youtube.com/watch?v=ekv6Xh_Im5c)

- Twilio argues that phone verification is a good way to prevent fake account creation.

[【反欺诈专栏】互联网黑产剖析——虚假号码](https://zhuanlan.zhihu.com/p/25474128)

[外卖订单量预测异常报警模型实践](https://tech.meituan.com/order-holtwinter.html)

[互联网业务风险控制的重要性](https://www.jianshu.com/p/bd6eb2d2b91b)

[互联网公司的风险控制](https://yq.aliyun.com/articles/136434)

[评分卡模型开发-基于逻辑回归的标准评分卡实现 - Erin的博客 - CSDN博客](https://blog.csdn.net/lll1528238733/article/details/76601897)

[用图计算做黑名单测试 京东金融准确率超90%](http://stock.xinhua08.com/a/20170919/1727030.shtml)

[图模型在欺诈检测应用一点看法](https://blog.csdn.net/hero_fantao/article/details/78745263)

## 2016

[Suspicious behavior detection: Current trends and future directions](http://media.cs.tsinghua.edu.cn/~multimedia/cuipeng/papers/suspicious%20behavior-survey.pdf)
- A very good survey of related work.

[Debot: Real-Time Bot Detection via Activity Correlation](https://www.cs.unm.edu/~chavoshi/debot/)

- Based on account activity time series, particularly correlation.
- Several papers published.

[Detecting outliers and anomalies in realtime at Datadog](https://www.youtube.com/watch?v=mG4ZpEhRKHA) ([Blog](https://www.datadoghq.com/blog/outlier-detection-algorithms-at-datadog))

- Time-series; Outlier detection: MAD, DBSCAN; Anomaly detection: agnostic online learning;
- Some discussions on signal processing based techniques: [FFT](https://en.wikipedia.org/wiki/Fast_Fourier_transform), [Wavelet Transform](https://en.wikipedia.org/wiki/Wavelet_transform), [Time–frequency analysis](https://en.wikipedia.org/wiki/Time–frequency_analysis).

[Disinformation on the web: Impact, characteristics, and detection of wikipedia hoaxes](http://infolab.stanford.edu/~west1/pubs/Kumar-West-Leskovec_WWW-16.pdf)

[京东基于 Spark 的风控系统架构实践和技术细节](https://www.infoq.cn/article/jingdong-risk-control-system-architecture-based-on-spark)

[美团风险控制系统综述](https://tech.meituan.com/online-risk-control.html) 

[搭建风控系统道路上踩过的坑——一个CPO的心得分享](http://bigsec.com/bigsec-news/wechat-161010-CPOfenxiang)

[LBSNShield: Malicious Account Detection in Location-Based Social Networks](https://pdfs.semanticscholar.org/3f5f/1b61fa856a2512afa9afe79b66b274dad59e.pdf)

## 2015

[Mastermind: Using Uber Engineering to Combat Fraud in Real Time](https://eng.uber.com/mastermind/)
- Rule-based engine

[Anomaly Detection for Airbnb’s Payment Platform](https://medium.com/airbnb-engineering/anomaly-detection-for-airbnb-s-payment-platform-e3b0ec513199)

[Identifying Outages with Argos, Uber Engineering’s Real-Time Monitoring and Root-Cause Exploration Tool](https://eng.uber.com/argos/)

[EVILCOHORT: Detecting Communities of Malicious Accounts on Online Services](http://www0.cs.ucl.ac.uk/staff/G.Stringhini/papers/evilcohort-usenix2015.pdf)

- Detect malicious account based on account-IP mapping
- Bipartite network projection, clustering / community detection

[Detecting Clusters of Fake Accounts in Online Social Networks](http://theory.stanford.edu/~dfreeman/papers/clustering.pdf)

- The main technique is a supervised machine learning pipeline for classifying an entire cluster of accounts as malicious or legitimate
- The key features used in the model are statistics on fields of user-generated text.


[RAD — Outlier Detection on Big Data](https://medium.com/netflix-techblog/rad-outlier-detection-on-big-data-d6b0494371cc)

- Robust PCA; [project source code](https://github.com/Netflix/Surus);

[Tracking down the Villains: Outlier Detection at Netflix](https://medium.com/netflix-techblog/tracking-down-the-villains-outlier-detection-at-netflix-40360b31732)

- DBSCAN clustering.

[luminol: a light weight python library for anomaly detection and correlation of time series](https://github.com/linkedin/luminol)

- The default anomaly detection method is based on the 2005 "Assumption-Free" paper.
- One limitation, if I understand correctly, is that detection_delay = future_window_size, which can be rather big if one wants to account for periodicity.

## 2014

[Fighting spam with BotMaker](https://blog.twitter.com/engineering/en_us/a/2014/fighting-spam-with-botmaker.html)
- Rule-based; low-latency so that it can run on write path.

[敢付敢赔背后的互联网实时风控技术](http://www.infoq.com/cn/presentations/internet-real-time-wind-control-technology)

[阿里巴巴的风控相比较传统银行的风控有何区别？会更有优势吗？](https://www.zhihu.com/question/23184094)

[Online Social Spammer Detection](http://www.public.asu.edu/~huanliu/papers/aaai2014.pdf)
- One key contribution is to combine content and network to detect fast evolving spammers. The basic idea is to represent the content, network, and labels as matrices. Then they find a low-rank user representation by finding a matrix factorization that minimizes a loss function. This low-rank representation becomes the feature vectors for classifier.
- Also the model can be updated online.

[Uncovering Large Groups of Active Malicious Accounts in Online Social Networks](https://users.cs.duke.edu/~xwy/publications/SynchroTrap-ccs14.pdf)

- Detect malicious accounts based on synchronized actions.
- Single-linkage hierarchical clustering.

[Nikunj Oza: "Data-driven Anomaly Detection" | Talks at Google](https://www.youtube.com/watch?v=5mBiac_dhbs&t=1175s)

- Air traffic; One-class SVM; [Multiple Kernel Learning based Heterogeneous Algorithm (MKAD)](https://c3.nasa.gov/dashlink/projects/34/);

[Systems and methods for troubleshooting errors within computing tasks using models of log files](https://patents.google.com/patent/US9552249B1/en)

- Model normal machine as a Finite-State Machine (FSM), and compare logs against the FSM.

## 2013

[Spotting Opinion Spammers using Behavioral Footprints](https://www.cs.uic.edu/~liub/publications/KDD-2013-Arjun-spam.pdf)
- Formulate the review spam problem in Bayesian framework / graphical model. The model is generative and can be viewed as a soft clustering system.
- Two key latent variables are author spamicity and review spam cluster. Author spamicity is in [0,1] and used as the parameter of Bernoulli distribution for review spam cluster (\pi). \pi, then together with a few other latent variables, generate observable variables.

## 2012

[Scammers and VoIP: What you need to know about illegal phone scams](https://www.voipreview.org/blog/scammers-and-voip-what-you-need-know-about-illegal-phone-scams

[Sms spam detection using noncontent features](http://www.cse.ust.hk/~qyang/Docs/2012/ieee_intelligent_sys_SMS-Spam_Detection.pdf)

## 2010

[Detecting and characterizing social spam campaigns](http://conferences.sigcomm.org/imc/2010/papers/p35.pdf)
- Group wall posts by textual similarities and URLs. They build similarity graph to find clusters.
- Then use two assumptions to find malicious clusters from benign ones.
- Interesting empirical results. For example, 97% of accounts used for spam campaign are compromised.

## 2008

[Determining Wether a Response from a Participant is Contradictory in an Objective Manner](http://pdfpiw.uspto.gov/.piw?PageNum=0&docid=08396718&IDKey=69A698AB1EBA%0D%0A&HomeUrl=http%3A%2F%2Fpatft.uspto.gov%2Fnetacgi%2Fnph-Parser%3FSect1%3DPTO1%2526Sect2%3DHITOFF%2526d%3DPALL%2526p%3D1%2526u%3D%25252Fnetahtml%25252FPTO%25252Fsrchnum.htm%2526r%3D1%2526f%3DG%2526l%3D50%2526s1%3D8396718.PN.%2526OS%3DPN%2F8396718%2526RS%3DPN%2F8396718)

- The basic idea is to compare a user's response with the authoritive response or community response via contingency matrix. If the difference is large one will consider the user's response as fradulent.

## 2005

[Assumption-Free Anomaly Detection in Time Series](http://www.cs.ucr.edu/~wli/publications/WeiL_AnomalyDetection.doc)

- A quite interesting 2D representation of time series. But it is hard to see why we need this representation and the proposed anomaly detection method.

[Unsupervised Anomaly Detection in Network Intrusion Detection Using Clusters](https://adiwijaya.staff.telkomuniversity.ac.id/files/2014/02/Unsupervised-Anomaly-Detection-in-Network-Intrusion-Detection.pdf)

- Grid-based clustering: CLIQUE, pMAFIA

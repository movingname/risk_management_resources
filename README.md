# Resources of *Risk Management* / *风险控制系统* / *Anomaly Detection* / *Malicious Account Detection*

Lanugage: Chinese / English

## 2018

[Implementing Model-Agnosticism in Uber’s Real-Time Anomaly Detection Platform](https://eng.uber.com/anomaly-detection/)

[Anomaly Detection: Algorithms, Explanations, Applications](https://www.microsoft.com/en-us/research/video/anomaly-detection-algorithms-explanations-applications/)

- An overview of Thomas Dietterich's research on anomaly detection benchmarking, theory, and applications.

## 2017

[Time Series Anomaly Detection: Detection of Anomalous Drops with Limited Features and Sparse Examples in Noisy Highly Periodic Data](https://arxiv.org/pdf/1708.03665.pdf)

- Two-stage architecture: predictor and anomaly-detector / comparator.
- For the predictor they used Deep Learning models like DNN, RNN, LSTM.

[Meituan] [外卖订单量预测异常报警模型实践](https://tech.meituan.com/order-holtwinter.html)

[互联网业务风险控制的重要性](https://www.jianshu.com/p/bd6eb2d2b91b)

[互联网公司的风险控制](https://yq.aliyun.com/articles/136434)

## 2016

[Detecting outliers and anomalies in realtime at Datadog](https://www.youtube.com/watch?v=mG4ZpEhRKHA) ([Blog](https://www.datadoghq.com/blog/outlier-detection-algorithms-at-datadog))

- Time-series; Outlier detection: MAD, DBSCAN; Anomaly detection: agnostic online learning;
- Some discussions on signal processing based techniques: [FFT](https://en.wikipedia.org/wiki/Fast_Fourier_transform), [Wavelet Transform](https://en.wikipedia.org/wiki/Wavelet_transform), [Time–frequency analysis](https://en.wikipedia.org/wiki/Time–frequency_analysis).

[Meituan] [美团风险控制系统综述](https://tech.meituan.com/online-risk-control.html) 

[搭建风控系统道路上踩过的坑——一个CPO的心得分享](http://bigsec.com/bigsec-news/wechat-161010-CPOfenxiang)

[LBSNShield: Malicious Account Detection in Location-Based Social Networks](https://pdfs.semanticscholar.org/3f5f/1b61fa856a2512afa9afe79b66b274dad59e.pdf)

## 2015

[Anomaly Detection for Airbnb’s Payment Platform](https://medium.com/airbnb-engineering/anomaly-detection-for-airbnb-s-payment-platform-e3b0ec513199)

[Identifying Outages with Argos, Uber Engineering’s Real-Time Monitoring and Root-Cause Exploration Tool](https://eng.uber.com/argos/)

[EVILCOHORT: Detecting Communities of Malicious Accounts on Online Services](http://www0.cs.ucl.ac.uk/staff/G.Stringhini/papers/evilcohort-usenix2015.pdf)

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

[Uncovering Large Groups of Active Malicious Accounts in Online Social Networks](https://users.cs.duke.edu/~xwy/publications/SynchroTrap-ccs14.pdf)

[Nikunj Oza: "Data-driven Anomaly Detection" | Talks at Google](https://www.youtube.com/watch?v=5mBiac_dhbs&t=1175s)

- Air traffic; One-class SVM; [Multiple Kernel Learning based Heterogeneous Algorithm (MKAD)](https://c3.nasa.gov/dashlink/projects/34/);

[Systems and methods for troubleshooting errors within computing tasks using models of log files](https://patents.google.com/patent/US9552249B1/en)

- Model normal machine as a Finite-State Machine (FSM), and compare logs against the FSM.

## 2005

[Assumption-Free Anomaly Detection in Time Series](http://www.cs.ucr.edu/~wli/publications/WeiL_AnomalyDetection.doc)

- A quite interesting 2D representation of time series. But it is hard to see why we need this representation and the proposed anomaly detection method.

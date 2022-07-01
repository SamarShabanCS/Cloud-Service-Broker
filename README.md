# Cloud-Service-Broker
## Domain Background

The Cloud computing is a computing model, wherever a large pool of resources is connected in private or public networks, to produce dynamically scalable infrastructure for application, data and file storage. The allowed software, development platforms and other hardware resources are provisioned to end users/consumers over the Internet in “as-a-service” models whenever and wherever consumers want. With the appearance of this technology, the cost of computation, application hosting, content storage and delivery are decreased significantly (1).

Cloud computing is a practical model that has a safe immediate cost benefits, and has the ability to convert a data center from a capital-intensive set up to a variably priced environment (1).

The cloud computing idea is based on reusability of IT capabilities. The enterprises as well as  individuals  can consumed these Cloud-based services as  an  agile  solution  to  their  operational  and  business  problems. The cloud providers manage the software, development platforms and hardware resources in an easy, on-demand and scalable accessible provisioned way. An online  marketplaces  to  facilitate  the  publication  and  searching  of  different types of cloud services in a more suitable way have been built by The leading cloud computing providers(Google, Microsoft, Amazon, E-Bay, IBM, etc). The marketplaces provide services on demand, paying  per  usage  and  managing  automatic  service  elasticity  to  meet  users’  requirements (2).

## Problem Statement
The Cloud consumer usually needs to use Cloud services as a partial solution to his requirements. So, the appropriate Cloud services have been composed and provided as a single virtual service to the Cloud consumers.

Compared to traditional service composition, cloud service composition is usually long-term based and economically driven. Traditional quality-based composition techniques usually consider the qualities at the time of the composition (3). For example, which composite service has the best performance at present?
This is fundamentally diﬀerent in cloud environments where the cloud service composition should last for a long period. For example, which composite cloud service performs best in the next few years; despite it may not be the best one at present?

The pay-as-you-go feature of the Cloud computing technology enables the service providers to offer their services with different configuration according to the service level agreement (SLA) (4). Therefore, Cloud consumers will face a challenge to select proper services from a huge number of the variations of the same services offered at different quality of service (QoS) levels. So, the Cloud service composition models become urgent.

## Datasets and Inputs
•	A synthetic dataset will be used to represent the cloud consumer preferences  or his requirements which are his preferred weights for response time, throughput, availability and cost for the required service : 
It will be a historical time series data follow Gaussian distribution. It will be generated using the TimeSynth open source library (https://github.com/TimeSynth/TimeSynth ). 

•	The cloud providers’ data set will be represented using a real cloud service data (5) which is updated in (6). It contains 5 historical time series for 100 cloud service providers collected through 6 months as 28 time slots as follows: 1. Availability 2. Max Response time 3. Min Response time 4. Avg. Response time 5. Throughput.
It is available here:
(https://github.com/SamarShabanCS/Math_for_ML/tree/master/time%20series%20data%20QoS)

## Solution Statement
The cloud environment has four actors: End Users, Composer, SaaS (Software as a Service) Providers and IaaS (Infrastructure as a Service) Providers. Platform as a Service (PaaS) layer is omitted as we assume that it is included in the IaaS layer. End Users are usually large companies and organizations, e.g., universities, governments. The composer represents the proposed composition framework. The composer acts on behave of the end users to form composite services that contains services from multiple SaaS providers and IaaS providers. It should select the accurately or optimal cloud providers to contract with in the future to reduce his cost (budget).

## Benchmark Model
According to my research, the nearest and closest paper to the mentioned problem is “Long-Term QoS-Aware Cloud Service Composition Using Multivariate Time Series Analysis” (7). So, it will be used as the benchmark model. It propose a multiple QoS prediction model (MQPM) by using the Arima model to predict the QoS values then compose the services that match cloud consumer requirements by using the Euclidian distance.

## Evaluation Metrics
To compare with the benchmark results; the following metrics will be use: RMSE, Precision, Recall, accuracy and f-measure.

## Project Design
The first phase: I will build prediction model to predict the future QoS provisioned values by the providers also the cloud consumer requirements using LSTM model. This prediction phase will help in accurately composing the cloud services.
The second phase: use the particle swarm optimization algorithm (PSO) to select the best services.
Third phase (optional):  applying a reduction technique such as principle component analysis (PCA) or autoencoder (AE) before the prediction phase to select the important features before the prediction also to reduce the prediction time cost.
### References:

1. M. Nazir, P. Tiwari, S. D. Tiwari, and R. G. Mishra. , Book Chapter of Cloud Computing: Reviews, Surveys, Tools, Techniques and Applications-An Open-Access eBook published by HCTL Open, 2015. 
2. Cloud services. [Online] , http://www.webopedia.com/TERM/C/cloud_services.html.
3. QoS-aware middleware for web services composition. L. Zeng, B. Benatallah, A. Ngu, M. Dumas, J. Kalagnanam and H. Chang. 5, May 2004, IEEE Transactions on Software Engineering, Vol. 30, pp. 311–327.
4. Frontiers in information and software as services. K. S. Candan, W.-S. Li, T. Phan and M. Zhou. Shanghai, China : s.n., 2009. Proc. Data Engineering, 2009. ICDE '09. IEEE 25th International Conference on. pp. 1761-1768.
5. Large-scale longitudinal analysis of soap-based and restful web services. W. Jiang, D. Lee and S. Hu. Honolulu, HI, USA : the 2012 IEEE 19th International Conference on Web Services, 2012. Proc. Web Services (ICWS), 2012 IEEE 19th International Conference on. pp. 218–225.
6. Haytamy S.S., Kholidy H.A., Omara F.A. (2018) ICSD: Integrated Cloud Services Dataset. In: Yang A. et al. (eds) Services – SERVICES 2018. SERVICES 2018. Lecture Notes in Computer Science, vol 10975. Springer, Cham.
7. Z. Ye, S. Mistry, A. Bouguettaya and H. Dong. Long-Term QoS-Aware Cloud Service Composition Using Multivariate Time Series Analysis. IEEE Transactions on Services Computing. june 2016, Vol. 9, 3, pp. 382-393. doi: 10.1109/TSC.2014.2373366.




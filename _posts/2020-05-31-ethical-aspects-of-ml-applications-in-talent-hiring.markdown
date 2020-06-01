---
layout: post
title: Ethical Aspects of ML Applications in Talent Hiring
cover: cover.jpg
date:   2020-05-31 12:00:03
categories: posts
---

This is the third article out of four posts in the _Machine Learning in Talent Hiring_ series. The [first post](https://donyeun.github.io/posts/2020/05/31/introduction.html) discusses the introduction of machine learning capability to be applied to the employee recruitment process within a company, as well as the motivation behind it. The [second post](https://donyeun.github.io/posts/2020/05/31/examples-of-ml-projects-in-talent-hiring.html) talks about several machine learning applications throughout the hiring process. The [last post](https://donyeun.github.io/posts/2020/05/31/summary.html) will talk about the summary of why we should implement machine learning applications in the recruitment sector, as well as the summary of algorithms, applications and several caveats that need to be taken into consideration when building the machine learning systems.

In this post, we will discuss several warnings, especially in relating to ethical aspects of applying machine learning techniques within the talent hiring process. Several examples of potential ethical issues and things that need to take into consideration will also be discussed.
 
---

While we know that machine learning can help in automation and faster decision making, it should be worth noting that human does responsible for supplying the data to the machine learning algorithms. Within the data compilation and generation, as well as the labelling process, there are potential biases carry over from the process. There are also some other aspects in the context of responsible AI that needs to be appropriately addressed. This includes aspects such as privacy and fairness of the decision given by the system.

## Privacy matters
It is undeniable that machine learning applications help elevate society. There have been many useful applications of machine learning being implemented in real-life. On the other hand, with the abundance of data being collected, we also need to discuss the side effects from the privacy perspective.

In the context of talent hiring, for instance, the transparency of how the applicants’ data will be stored and used is necessary. For instance, the CV and peer review comments are highly sensitive and are not intended for public consumption -does the human and the system aware of this? It is also essential to be transparent about what kind of data being used as a training set and how personally identifiable information (PII) is being handled for the machine learning algorithms. It is required that a machine learning system adheres to privacy regulation. For example, to comply with the European Union’s General Data Protection Regulation (GDPR), the tool should ask for approval to the applicants regarding what kinds of data and what are they being used for (Bersin & Chamorro-Premuzic, 2018).

Another example that can be mentioned is the use of external data (e.g. social media accounts) on assessing job seekers that are being used without consent (Wall Street Journal, 2018) (Dattner, Buchband & Schettler, 2019). There have been numerous researches being conducted in demographic inference by using social media data. Protected attributes such as gender (Vicente, Batista & Carvalho, 2019) and even socioeconomic status (Ghazouani et al., 2019) of a Twitter user can be inferred from the contents provided. This can be problematic if the user does not know that the company also take these additional data into account. In other contexts outside of hiring field, the unintentional leakage of identifiable personal attributes can result in unfair decisions by human or computer authorities, such as discrimination based on gender (Mitchell & Martin, 2018) or bias against certain ethnicities (Farkas, 2003). 

## Fairness and Human Bias
One of the definitions of fairness is the prohibition of discriminative action of any individuals based on protected attributes such as gender, race, sexual orientation, physical or mental disability and religion. Unfortunately, simply removing these protected attributes in the training data is not sufficient, as there is still a chance of indirect discrimination, such as inferring protected attributes from the language style of a candidate, to the use of implicit features within the dataset (Zafar et al., 2019).

Machine learning can also suffer from bias. There is a possibility of human bias at each machine learning steps in the pipeline, from defining the problem, data collection, to the training process and deployment of the product itself (Tensorflow, 2020). One case study is Amazon’s ML system; wherein 2017 they discarded their AI recruiting tool as it was gender bias due to discrimination against female candidates by giving them lower score (Dastin, 2018) (Heilweil, 2019). This happened due to female demography within their training dataset was underrepresented when creating the model.

Another gender bias that might not necessarily be created on purpose is described in the research done by (Datta, Tschantz & Datta, 2015), where they revealed that Google returned fewer results on high-paying job advertisements to its female audience.

These bias problems are not necessarily exclusively marked as machine learning problems; they are, in fact, a social problem as well, that can potentially be carried over in the data that will be fed into machine learning models. Some examples of unconscious biases that can happen during the hiring process are confirmation bias and expectation anchor bias. Confirmation bias happens when someone has a verdict settled in the first few moments of interviewing with the candidate, and he/she favours information confirming this initial decision. Something similar to that is expectation anchor bias, which happens when we anchor ourselves into one information about a candidate and use that information only to make a decision (Mujtaba & Mahapatra, 2019).

## Interpretability: Understanding Machine Learning Outcome
How can machine learning algorithms justify its output that comes from the black box algorithm? How can we explain why person A gets the job, while person B does not? How can we make sure that the algorithms do not suffer from any biases?

Interpretability is an essential part in order to trust the machine learning algorithms. It is, however, worth noting that interpretability is not necessarily an easy thing to be done by either machines or human beings. Even for a human expert such as an oncologist, the verdict of a patient having cancer might start from intuition, that is then followed up by a series of tests to establish the diagnosis.

In the context of machine learning algorithms, there are some easy to use machine learning libraries that can lead to interpretable results, which can be incorporated within the end products. These libraries are Lime (Ribeiro, Singh & Guestrin, 2016) and SHAP (Lundberg & Lee, 2017) to name a few. These platforms enable the user to be provided with both global and local interpretable verdict from a machine learning system. Global interpretability is the high-level reasoning and feature importance behind a model in general, whereas local explainability is defined as the result explanation of each case.

## Bias Mitigation
As described by (Mujtaba & Mahapatra, 2019), being aware of any biases is vital. This is in order to mitigate the likeliness of bias being present at each process in the hiring pipeline. Several actions can be incorporated as attempts to avoid bias in the hiring process. Adapted from (Mujtaba & Mahapatra, 2019), those actions are the following:

1. Data preprocessing

   In the case of cleaning data, other than removing the protected attributes, we can also incorporate other techniques such as reweighting of the attributes to take into account the fairness across applicants (Bellamy et al., 2018).
   
2. Tweaking the classifiers

   We can introduce additional rules to achieve the definition of fairness during the model creation.

3. Post-processing

   In this alternative, fairness can be achieved by altering the outcome, either by tweaking the threshold of the outcome given by the classifier, or providing explanations of the outcome, so the candidate can get feedback as to how they performed during the selection process. As a bonus, an outcome explanation can potentially help the candidates to gain feedback as to what can be improved had they are unable to proceed to the next step.


## Summary
In this post, we have learned about several key points of responsible AI, such as privacy and interpretability. While it is helpful to use machine learning as a tool to solve some hiring problems, it is also worth noting that humans involve within the system should aware of many potential biases that can happen. Just like the case of Amazon who discarded their machine learning recruitment tool in 2017, many potential ethical issues underlie them, such as discrimination against protected attributes, or privacy concern regarding the use of data during and after a hiring process, and the explainability of the outcome given by the algorithms. 

## Reference:
Bellamy, R.K.E., Dey, K., Hind, M., Hoffman, S.C., et al. (2018) AI Fairness 360: An extensible toolkit for detecting, understanding, and mitigating unwanted algorithmic bias. arXiv preprint arXiv:1810.01943.

Bersin, J. & Chamorro-Premuzic, T. (2018) New Ways to Gauge Talent and Potential. [Online]. 2018. Available from: https://sloanreview.mit.edu/article/new-ways-to-gauge-talent-and-potential/ [Accessed: 21 March 2020].

Dastin, J. (2018) Amazon scraps secret AI recruiting tool that showed bias against women. [Online]. 2018. Available from: https://www.reuters.com/article/us-amazon-com-jobs-automation-insight/amazon-scraps-secret-ai-recruiting-tool-that-showed-bias-against-women-idUSKCN1MK08G [Accessed: 21 March 2020].

Dattner, B., Buchband, T.C.-P.R. & Schettler, L. (2019) The Legal and Ethical Implications of Using AI in Hiring. [Online] Available from: https://hbr.org/2019/04/the-legal-and-ethical-implications-of-using-ai-in-hiring [Accessed: 21 March 2020].

Heilweil, R. (2019) Artificial intelligence will help determine if you get your next job. [Online]. 2019. Available from: https://www.vox.com/recode/2019/12/12/20993665/artificial-intelligence-ai-job-screen [Accessed: 21 March 2020].

Lundberg, S.M. & Lee, S.-I. (2017) A Unified Approach to Interpreting Model Predictions. In: I Guyon, U V Luxburg, S Bengio, H Wallach, et al. (eds.). Advances in Neural Information Processing Systems 30. [Online]. Curran Associates, Inc. pp. 4765–4774. Available from: http://papers.nips.cc/paper/7062-a-unified-approach-to-interpreting-model-predictions.pdf.

Mujtaba, D.F. & Mahapatra, N.R. (2019) Ethical Considerations in AI-Based Recruitment. In: 2019 IEEE International Symposium on Technology and Society (ISTAS). [Online]. November 2019 pp. 1–7. Available from: doi:10.1109/ISTAS48451.2019.8937920.

Ribeiro, M.T., Singh, S. & Guestrin, C. (2016) ‘Why should i trust you?’ Explaining the predictions of any classifier. In: Proceedings of the 22nd ACM SIGKDD international conference on knowledge discovery and data mining. 2016 pp. 1135–1144.

Tensorflow (2020) Responsible AI with TensorFlow (TF Dev Summit ’20). [Online]. 2020. Available from: https://www.youtube.com/watch?v=UEECKh6PLhI&t=238s [Accessed: 21 March 2020].

Wall Street Journal (2018) Artificial Intelligence: The Robots Are Now Hiring Moving Upstream. [Online]. 2018. Available from: https://www.youtube.com/watch?v=8QEK7B9GUhM [Accessed: 21 March 2020].

Zafar, M.B., Valera, I., Gomez-Rodriguez, M. & Gummadi, K.P. (2019) Fairness Constraints: A Flexible Approach for Fair Classification. Journal of Machine Learning Research. 20 (75), 1–42.

Datta, A., Tschantz, M.C. & Datta, A. (2015) Automated experiments on ad privacy settings: A tale of opacity, choice, and discrimination. Proceedings on privacy enhancing technologies. 2015 (1), 92–112.

Farkas, G. (2003) Racial disparities and discrimination in education: What do we know, how do we know it, and what do we need to know? Teachers College Record. 105 (6), 1119–1146.

Ghazouani, D., Lancieri, L., Ounelli, H. & Jebari, C. (2019) Assessing Socioeconomic Status of Twitter Users: A Survey. In: Recent Advances in Natural Language Processing (RANLP 2019). 2019 p.

Mitchell, K.M.W. & Martin, J. (2018) Gender Bias in Student Evaluations. PS: Political Science&amp; Politics. [Online] 51 (3), 648–652. Available from: doi:10.1017/S104909651800001X.

Vicente, M., Batista, F. & Carvalho, J.P. (2019) Gender detection of Twitter users based on multiple information sources. In: Interactions Between Computational Intelligence and Mathematics Part 2. Springer. pp. 39–54.

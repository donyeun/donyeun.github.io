This article is the second out of four posts of the _Machine Learning in Talent Hiring_ series. The [first post](https://donyeun.github.io/2020/05/31/introduction/) discusses a little bit about what motivates applying machine learning in the hiring process. The [third post](https://donyeun.github.io/2020/05/31/ethical-aspects-of-machine-learning-applications-in-talent-hiring/) in the series talks about several takeaways and ethical aspects of applying machine learning techniques within the recruitment field. The [last post](https://donyeun.github.io/2020/05/31/summary/) will talk about the summary of why we should implement machine learning applications in the recruitment sector, as well as the summary of algorithms, applications and several caveats that need to be taken into consideration when building the machine learning systems.

This blog post is dedicated to discussing several examples of ML applications of each significant subtask in the recruitment pipeline. Amongst others, the first application that will be discussed is the paper from LinkedIn, on getting better talent searching by considering engagement between candidate and recruiter.

## Better talent searching and mutual interest between candidate and recruiter

One new paper to look in the talent searching task is the one written by researchers from the most extensive professional social networking website in the world, LinkedIn. Focus on the initial step within hiring pipeline; this paper presents a deep learning approach as well as its representation learning for talent searching within LinkedIn Recruiter product environment (Ramanath et al., 2018). What is interesting is that the paper does not only mentioned the background theories that underlie the LinkedIn Recruiter platform, but also mentioned about the technical challenges and practical considerations when publishing the model into production. 

This paper does not only talk about the reachability of a job posting but what is more important is the mutual interest and the engagement about the particular job posting between two parties (both candidates and recruiters). When a recruiter seeks for candidates for a specific position by typing a query into LinkedIn Recruiter, the ideal interaction of mutual interest would be, when candidate showed is related to the query, and when the recruiter decided to contact the candidate, the candidate would also show the same interest for that particular job opportunity.

Unlike the previous works, this paper takes complex feature interactions relationships into account. Their contributions written in the papers are creating sparse entities semantic representation in the domain of candidate searching. Their network leverage LinkedIn Economic Graph, and take LinkedIn attributes as features, such as candidate IDs, skill entity IDs, and recruiter IDs. Another contribution in the paper is the deep model that will be trained to learn the relation between recruiter engagement within the platform, along with the followed candidate response.


## More capacity on the initial resume-based interview with a chatbot
A work by (Aquino et al., 2014) resulted in Interbot, a conversational agent (chatbot) that aims at minimising the time and cost required on interviewing candidates. The solution that this chatbot offers is by minimising hiring team’s involvement during initial resume-based interview verification that some companies perform during their hiring process. This chatbot can verify the candidate by assigning similarity score between what is written in resume paper and the candidate’s answers during a conversation with a chatbot.

The conversational agent was evaluated not only by its accuracy on doing its primary job but also the naturalness of Interbot dialogue was also being evaluated by human annotators.

## Screening and interviewing candidates 
A paper from CVPR 2017 ChaLearn Job Candidate Screening Coopetition (Kaya, Gurpinar & Salah, 2017) tries to tackle the challenge of candidate screening by using video CV. By using video as the input, this paper determines the personality traits along with other desirable features that can determine whether the candidate is a good fit. This system is also able to determine whether a candidate will continue to the next phase of the interview. The researchers aimed for an explainable result as the output from the system. 
In terms of architecture,  the system is based on decision trees operating in an ensembled way that responsible for giving an output of the quantitative stage. The ensemble trees are then followed by a series of rule-based algorithm and a single decision tree responsible for giving the final verdict as well as to give explainable results of the outcome. The features from video CV are extracted by using a deep convolutional neural network (CNN).

## Accessing emotional intelligence of candidates through social media data
Work was done by (Menon & Rahulnath, 2016) on trying to automate the preliminary check of candidates during the hiring process. This work focuses on accessing the candidate’s Big Five personality as well as accessing his/her emotional intelligence. What seems to be uncommon is that they make use of a candidate’s social media data, where the talent was being asked to provide his/her Twitter account handle during the recruitment process. 

When discussing the ethical aspect of this application, it was written that the actual contents of the tweets are not being taken as attributes. Instead, they take meta attributes as the parameters to determine the compatibility score of a candidate (Menon & Rahulnath, 2016).¬ These meta attributes are the average length of texts, average word length, and some interesting features such as the numbers of exclamation marks and number of followers.




## Summary
In this post, we discussed several examples of machine learning applications that can be incorporated at many subtasks within a talent-hiring pipeline. It is interesting to see the fact that many subtasks can be automated, allowing the hiring team to focus on the things that matter, by minimising (or getting rid of) human involvements in less exciting and repetitive tasks. By looking at Interbot, we can see that the hiring team can increase their initial resume-based interview capacity by leveraging chatbot and NLP into the process. The paper from LinkedIn makes us understand that the importance of job posting is not just reachability, but also mutual engagement between a recruiter and the candidate responding to that job posting. 

The work by Kaya, Gurpinar, and Salah on automating the outcome and predicting the personality on video CV data also shows us that many applications focused on the first part of the hiring funnel, where the highest volume of applicants happen. While it needs to be evaluated from the ethical perspective, but the work by Menon and Rahulnath on accessing the emotional intelligence of candidates through their social media data is also a unique application. This can perhaps be implemented on seeking and hiring the right social media influencer for a brand, where social media data do matters and are being used as a promotional platform.

## Reference
Aquino, A.G., Bayona, K.R., Gonzales, K.D., Reyes, G.D., et al. (2014) Interbot: A credential verification chatbot using an enhanced example based dialog model. International Journal of Future Computer and Communication. 3 (4), 252.

Kaya, H., Gurpinar, F. & Salah, A.A. (2017) Multi-modal Score Fusion and Decision Trees for Explainable Automatic Job Candidate Screening from Video CVs. IEEE Computer Society Conference on Computer Vision and Pattern Recognition Workshops. [Online] 2017-July, 1651–1659. Available from: doi:10.1109/CVPRW.2017.210.

Lewis, G. (2017) How Sutherland Is Using a Chatbot to Improve Candidate Experience. [Online]. 2017. Available from: https://business.linkedin.com/talent-solutions/blog/talent-on-tap/2017/meet-tasha-the-chatbot-that-improves-candidate-experience [Accessed: 23 March 2020].

Menon, V.M. & Rahulnath, H.A. (2016) A novel approach to evaluate and rank candidates in a recruitment process by estimating emotional intelligence through social media data. In: 2016 International Conference on Next Generation Intelligent Systems (ICNGIS). 2016 pp. 1–6.

Ramanath, R., Inan, H., Polatkan, G., Hu, B., et al. (2018) Towards deep and representation learning for talent search at LinkedIn. International Conference on Information and Knowledge Management, Proceedings. [Online] 2253–2262. Available from: doi:10.1145/3269206.3272030.


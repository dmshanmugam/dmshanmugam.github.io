---
layout: default
--- 

Hi! I am a postdoc with Emma Pierson, based at Cornell Tech. I completed my Ph.D. in the [Clinical and Applied Machine Learning](https://caml.csail.mit.edu/) group at MIT, where I was lucky to be advised by John Guttag. 
Before, I was at MIT for undergrad, where I majored in computer science with a concentration in South Asian studies. 

I work on machine learning for healthcare. My current research (often) falls into one or more of these categories:

**<mark style="background-color: #ADD9F450;"> Measuring human behavior in health datasets:</mark>**  I believe that we can improve healthcare not just
by training better predictive models, but also by building better *descriptive* models of how care is delivered today. To what extent are diseases under-diagnosed? 
How do financial incentives shape treatment decisions? These are questions that machine learning methods I develop, in combination with large health datasets, can answer. 

<!-- Datasets used in machine learning for healthcare are shaped by a complex system of human interaction and financial incentives.
I like thinking about how we can develop machine learning methods to measure processes that shape observable data, in order to:
(1) better understand the ways in which observable data differs from the data we wish to observe and 
(2) reason about the behavior of machine learning models trained on this data. -->

<!-- I've thought about this in the context of *underdiagnosis* (of intimate partner violence (NWH 2024), and in ongoing work, genetic disease and cardiovascular outcomes),
*patterns of health access* (heart failure), and most recently, *overtreatment*. -->

**<mark style="background-color: #ADD9F450;">  Updating and evaluating machine learning models:</mark>** I am interested in issues that arise *after* training a model. We are great at training models -- see the immense number of trained models available on HuggingFace -- but we have a lot of room to improve the ways we update, evaluate, and select models. I work on new methods to update models using test-time augmentation, and new methods to evaluate machine learning models under domain-specific constraints.

<!-- One powerful way to update a trained classifier is test-time augmentation [1, 2, 3, 4], a method that generates an ensemble of predictions using a single classifier by perturbing the input data. Test-time augmentation has several nice properties, all for the cost of multiple forward passes; I've looked at the effects of TTA on accuracy, robustness, and uncertainty estimation: 

I'm also interested in questions on model evaluation. The standard approach to model evaluation is to use a large labeled dataset, an expensive-at-best and impossible-at-worst procedure. I've thought about the implications of race data on assessments of algorithmic fairness, and how we can evaluate models with limited labeled data (under review). -->


**<mark style="background-color: #ADD9F450;"> Promoting health equity:</mark>** Can we use AI to characterize and mitigate persistent health inequalities? I (and many of my co-authors) would [say yes](https://arxiv.org/abs/2312.14804)! 
I am especially committed to translating advances in machine learning to women's health. A number of open technical questions here motivate my current work,
including the scarcity of ground truth labels, and the role of predictive models in case management, particularly in the context of intimate partner violence and fertility.

Sometimes I describe my interests as "everything but model training". This is partially because I am impatient, but it is <ins>also</ins> because I believe the road from messy to clean data and the road from trained model to deployment raise important unanswered questions. 

<!-- If you are a student interested in collaborating on these topics, do reach out! -->

<!-- Future:
    EHR underdiagnosis, genetic underdiagnosis
    -->

<!-- Future:
    Birth Control Switches
    Birth prediction -->
<!-- There is increased interest in reducing, reusing, and recycling machine learning models, particularly in downstream applications.  -->

<!-- I also use the intersection of machine learning and healthcare as a "model organism" for the interface between practitioners and machine learning researchers.  -->
<!-- There are fundamental questions about updating and evaluating models that challenge us today. -->


<!-- (1) Building better *descriptive* models of how care is delivered today. To what extent are diseases under-diagnosed? 
How do financial incentives shape treatment decisions? These are questions that machine learning methods I develop, in combination with large health datasets, can answer.

(2) Building better methods to update and evaluate machine learning models for context-specific tasks. 

(3) Using machine learning to *promote* health equity.  -->


<!-- - How can we use test-time augmentation to update a model to be more accurate? (ICCV 2021,  ICML UDL Workshop 2023)
- How can we use test-time augmentation to be more robust to out-of-distribution examples? (ICML UDL Workshop 2022)
- How do we update a model to produce more reliable uncertainty estimates? (under review) -->

<!-- - What are the risks of using coarse race data to evaluate clinical risk scores? (MLHC 23)
- How can we facilitate semantically-grounded, context-specific evaluation (CHI 23)
- How can we best evaluate classifiers in the absence of abundant labeled data? (under review) -->
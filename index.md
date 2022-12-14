---
title: Causal Claims   
---
### Causal Claims Identification and PIO Frame Extraction  
The 17th International Workshop on Semantic Evaluation


## Motivation 
Identification and automatic verification of medical claims from unstructured user-generated text data is an onerous but essential step for various decision-making processes. Some day-to-day tasks that can benefit from automatic claim identification are content moderation, insurance claim identification, and hypothesis generation from clinical notes. 

Towards building this capability and motivating further research in this direction, we propose the following shared subtasks. 

## Task description:  

SemEval-2023 task 8 consists of two two sub-tasks. Subtask 1 focuses on the identification of causal claims, experience, etc. in a provided multi (or single) sentence text snippet and subtask 2 focuses on the extraction of the PIO frame related to identified causal claim in the provided text snippet. More details on each subtask are provided below.  


### Subtask 1: Causal claim identification:  

For the provided snippet of text, the first subtask aims to identify the span of text that is either a claim, experience, experience_based_claim or a question. These four categories can be defined as follow:  
- Claim: Commmunicates a causal interaction between an intervention and an outcome. 
- Experience: Relates a specific outcome/symptom to an intervention or population based on someone's experience. 
- Experience based claim: A claim based on someone's experince. 
- Question: Poses a question. 

<!-- 
In experience, the post communicated something an individual's experience but is not making a claim yet. Whereas in experience_based_claim, the post makes a claim based on an individual's experience. And in Claim category, the post makes a general claims.  -->

<!-- Following in an example for each category. 
- **Experince**: " I am left with headache after taking drug-B."
- **Experince_based_claim**: " I am left with headache after taking drug-B and I recently read few posts mentioning the same."
- **Claim**: " I have read literature reporting that Drug-A doesn't work for Condition-B." -->

Participants can work on it at sentence level and try to classify sentences in one of the given classes but many times claim (or other class) is just a part of the sentence. But this maybe only a baseline as in many examples only a part of sentence is annotated as one of these category. Please check the  image below for more clarity.   

![Subtask-1](subtask-1.png)   

----- 
### Subtask 2: PIO frame extraction:  

In this subtask, for a given multi (or single) sentence text snippet and identified claim in that snippet, the task is to extract related Population (P), Intervention (I), and Outcome (O) frame. While it is rare, it may be the case that there is more than one claim in any given post. In that case, we want to identify PIO elements for a given claim. This can be framed as a sequence tagging task.  


![Subtask-2](subtask-2.png)    

## Dataset details: 
We are currently providing a sample dataset and will be releasing the full training data soon. Our dataset is built from Reddit posts and to respect the users' privacy we are not releasing the dataset directly. Instead, we are only providing Reddit post ids, annotations, and a script. Participants can use the script to obtain the data and merge it with the provided annotations. If users choose to delete their post, the script won't be able to get it. 


### Sample dataset
For this task, we are providing reddit post ids, our annotations and a script to obtain the datset from reddit. Please go through following link to obtain the dataset: 
- [Sample training and test data](https://drive.google.com/drive/folders/1cN20UanW8GmrDo1YkeMP5_AGTZ_QOtlG?usp=sharing) for both the stage 
- [Python script](https://drive.google.com/file/d/10D5VKvdKcIJvtC47vE7IcQQl_2f9qvG4/view?usp=sharing) to download the actual posts 
- [Medium article](https://towardsdatascience.com/scraping-reddit-data-1c0af3040768) if you need help with reddit crediational require in the script   
 
 The dataset provided here is same as the dataset in Codalab page but participants will need to register to access the competition leatherboard.  

## CodaLab competition details: 
Visit our [Codalab](https://codalab.lisn.upsaclay.fr/competitions/6948?secret_key=0eb18fd8-c847-4738-956c-f0f19fe3692e) website for detailed instruction. The main task along with evalution leatherboard will be hosted on codaLab. Each participant will need to sign in and register for the task.   

### Evaluation 
We will evaluate submissions on class-wise F1 scores (macro-averaged for leaderboard).



### Submission  
We plan to open the submission system in December 2022. 

### Important dates for task participants

- [x] Training data ready and available on our [CodaLab task page](https://codalab.lisn.upsaclay.fr/competitions/6948?secret_key=0eb18fd8-c847-4738-956c-f0f19fe3692e)
- [ ] Evaluation start 10 January 2023 (we are deciding on a possible earlier date)
- [ ] Evaluation end by 31 January 2023 
- [ ] Paper submission due February 2023 - each team will submit a [system paper](https://semeval.github.io/system-paper-template.html)
- [ ] Notification to authors March 2023
- [ ] Camera ready paper due April 2023
- [ ] SemEval workshop Summer 2023 

All deadlines are 23:59 UTC-12 (["anywhere on Earth"](https://en.wikipedia.org/wiki/Anywhere_on_Earth)).

### Related resouces
- [Frequenty Asked Questions](https://semeval.github.io/faq.html)
- [Paper Submission Requirements](https://semeval.github.io/paper-requirements.html)
- [Guidelines for SemEval System Paper](https://semeval.github.io/system-paper-template.html)

## Organizers
Contact us on:

- Google group and mailing list: *causal_claims@googlegroups.com*
- Email us: *semeval23.causalclaims@proton.me* 



<!---
some commented files - we can add our new md files and hyperlink here if needed
### Resources

- [Frequently Asked Questions about SemEval](/faq.html)
- [Paper Submission Requirements](/paper-requirements.html)
- [Guidelines for Writing Papers](/system-paper-template.html)
- [SemEval-2023 call for task proposals (archival)](cft)
--->

<!-- ### Sponsorship

SemEval is sponsored by the [SIGLEX](http://alt.qcri.org/siglex/) Special Interest Group on the Lexicon of the Association for Computational Linguistics.

 -->
 
<!-- __Contact:__ <semevalorganizers@gmail.com> -->
<!--- Most questions not answered by the above resources should be directed to organizers of specific [tasks](tasks.html).
General questions about SemEval organization should be directed to <semevalorganizers@gmail.com>.--->

## Anti-Harassment policy

SemEval highly values the open exchange of ideas, freedom of thought and expression, and respectful scientific debate.
We support and uphold the [ACL Anti-Harassment policy](https://www.aclweb.org/adminwiki/index.php?title=Anti-Harassment_Policy).
Participants are encouraged to send any concerns or questions to the [Professional Conduct Committee](https://www.aclweb.org/adminwiki/index.php?title=Professional_Conduct_Committee),
[Priscilla Rasmussen](mailto:acl@aclweb.org) and/or the workshop organizers.

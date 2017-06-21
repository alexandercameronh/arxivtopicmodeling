# Topic Modeling of arXiv.org


# Table of Contents

[1. Introduction](#section-a)  
[2. Action](#section-b)  


## <a name="section-a"></a>1.  Introduction

[ArXiv.org](https://www.arxiv.org) is an e-print repository of scientific publications owned by Cornell University. Fields 
covered on the website include: mathematics, physics, computer science, statistics, and so forth. All papers on arXiv 
are for PDF download and other formats (depending on the submission format). I first stumbled upon arXiv when I read a
 [paper](https://arxiv.org/abs/1610.06918) on adversarial neural networks by two computer scientists at Google. The 
 paper was extremely thought-provoking and interesting - I wanted to learn more. Or at least, I wanted to read about 
 similar topics.
 
 The problem with arXiv is that they do not have any sort of recommender products in their system. A unique keyword search
 has to be done every time you want to look for something. This was annoying. I wanted to cluster the academic papers
 into more general topics. That specific paper that I previously mentioned was filed under 'Computer Science: 
 Cryptography and Security'. Rightfully so.
 
 But what if I had two papers: one written about NMF (non-negative matrix factorization) which may be filed under
 a 'mathematics' or 'linear algebra' label, and another written about LDA (latent dirichlet allocation), which may be 
 filed under a 'statistics'. But both papers are actually talking about how those math concepts can be applied to natural 
 language processing. NLP is the sort of "general topic" that I would hope to cluster both of these papers to.
 
 
 
## <a name="section-a"></a>2. Action

Step 1. Use Python API wrapper to pull data from arXiv
Step 2. Transfer data into MongoDB (hosted on an Amazon Web Services instance)
Step 3. Apply NMF and LDA to the paper abstracts and for topic modeling
# <center> Deep Bidirectional Language-Knowledge Graph Pretraining </center>

### Abstract:
- #### What is the task they are trying to solve
  - This a QA task. Model is trained to answer questions.
- #### How do they solve it?
  - They designed two self-supervised tasks: Masked LM and Link prediction. Then pretrain the GreaseLM on Bookcorpus and ConceptNet KG. Finally, fine-tune the model on QA tasks on QA datasets.
- #### What is the main contribution?
  - DRAGON outperforms existing language model (LM) and LM+KG models on diverse downstream tasks including question answering across general and biomedical domains, 
  - DRAGON achieves strong performance on complex reasoning about language and knowledge and low-resource QA , and new state-of-the-art results on various BioNLP tasks.

### Methodology:
- #### What is the method they use to solve the problem?
  - two self-supervised tasks: Masked LM and Link prediction.
- #### Illustrations of the method
 ![DRAGON](https://github.com/michiyasunaga/dragon/raw/main/figs/dragon.png "DRAGON")


  
### Conclusion:
- #### What is the conclusion of their experiment?
  - Their deep bidirectional self-supervision over text and KG produces significantly improved language-knowledge representations compared to existing models.
- #### What is the limitation of their method?
  - Can not generate text.

### My comments:
- #### What is my conclusion? What can i learn from this paper?
  - Self-supervised learning is a good way to pretrain a model.

  
### Links:
- #### [Paper link](https://arxiv.org/pdf/2210.09338.pdf)
- #### [Code link](https://github.com/michiyasunaga/dragon)


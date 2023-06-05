# <center> Deep Bidirectional Language-Knowledge Graph Pretraining </center>

### Abstract:
- #### What is the task they are trying to solve?
The authors propose a self-supervised method to pretrain a deeply joint language-knowledge foundation model from text and knowledge graph (KG) at scale.

- #### How do they solve it?
They introduce DRAGON (Deep Bidirectional Language-Knowledge Graph Pretraining), which takes pairs of text segments and relevant KG subgraphs as input and bidirectionally fuses information from both modalities. They pretrain this model by unifying two self-supervised reasoning tasks, masked language modeling and KG link prediction.

- #### What is the main contribution?
DRAGON outperforms existing language model (LM) and LM+KG models on diverse downstream tasks including question answering across general and biomedical domains, with +5% absolute gain on average. In particular, DRAGON achieves strong performance on complex reasoning about language and knowledge (+10% on questions involving long contexts or multi-step reasoning) and low-resource QA (+8% on OBQA and RiddleSense), and new state-of-the-art results on various BioNLP tasks.

### Methodology:
- #### What is the method they use to solve the problem?
The authors use a cross-modal encoder that bidirectionally exchanges information between text and KG to produce fused text token and KG node representations. They pretrain this model by unifying two self-supervised reasoning tasks: masked language modeling, which masks some tokens in the input text and then predicts them, and link prediction, which holds out some edges from the input KG and then predicts them.

### Results:
- #### What is the result of the paper?
DRAGON outperforms existing LM and LM+KG models on diverse downstream tasks including question answering across general and biomedical domains, with +5% absolute gain on average. In particular, DRAGON achieves strong performance on complex reasoning about language and knowledge (+10% on questions involving long contexts or multi-step reasoning) and low-resource QA (+8% on OBQA and RiddleSense), and new state-of-the-art results on various BioNLP tasks.

### Datasets:
- #### What datasets do they use?
The authors pretrain DRAGON in two domains: a general domain, using the Book corpus and ConceptNet KG, and a biomedical domain, using the PubMed corpus and UMLS KG.

### Conclusion:
- #### What is the conclusion of their experiment?
The authors conclude that their deep bidirectional self-supervision over text and KG produces significantly improved language-knowledge representations compared to existing models.

- #### What is the limitation of their method?
The authors do not mention any limitations of their method in the abstract.

### My comments:
- #### How can it help in my research?
This paper presents a novel approach to pretraining a joint language-knowledge foundation model that could be useful for improving performance on downstream tasks such as question answering.

- #### Can I improve their method?
It would be interesting to explore how this approach could be extended or adapted to other modalities or types of data.

- #### What is my conclusion? What can I learn from this paper?
This paper presents a promising approach to pretraining a joint language-knowledge foundation model that achieves strong performance on a variety of downstream tasks. It provides valuable insights into how text and knowledge graphs can be effectively combined for improved reasoning abilities.
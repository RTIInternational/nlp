# NLP Tasks

Overview of common NLP tasks and their relevance to RTI.

Much of this content is subjective and based on the opinions of the contributors

| Task | Summary | Purpose | [Stage†](https://www.annualreviews.org/doi/full/10.1146/annurev-polisci-053119-015921) | Requirements | Example RTI application | Relevance to RTI |
|---|---|---|---|---|---|---|
| Fill-Mask (Word Prediction) | Use the context words surrounding a mask token to predict the mask token | Fine tune a model to domain-specific language | | Pretrained model, domain-specific texts | Improve performance on a NLP task using a pretrained model with esoteric, domain-specific language, e.g. language related to a specific health problem | Medium |
| Question Answering | Automatically answer questions posed by humans in a natural language | Convenient interface for information retrieval | | Iterative data labeling process, usually a deep learning model | Tool to help client expore a knowledge base | Low |
| Summarization | Produce a shorter version of one or several documents that preserves most of the input’s meaning | Quickly process document content and/or identify relevant documents | | Model evaluation can be difficult | Tool to summarize proposals, RFAs, or research papers | Medium |
| Table Question Answering | Query a relational database using natural language | Convenient interface for database queries | |Data must be in relational database format | Feature of a web app for data exploration | Medium |
| Text Classification | Classify documents into known categories | Solve a classification problem with text data | Measurement, Prediction | Requires labeled data | Relevance modeling - is a document relvant to a given research question | High |
| Text Generation | Predict the next word given a series of previous words (often repeatedly) | Generate natural language given a prompt | | Large deep learning model needed for best performance | Applied indirectly in conversational projects | Low |
| Text2Text Generation (Paraphrasing) | Generate an output sentence that preserves the meaning of the input sentence but contains variations in word choice and grammar | Paraphrases can be useful for generating training data, query systems, translation evaluation, etc. | | Model evaluation can be difficult | Generate additional training data | High |
| Token Classification (NER) | Tag entities in text with their corresponding type, typically using BIO notation | Extract keywords or known entities from texts | Discovery, Measurement | Requires labeled data; BIO labeling is intensive | Extract a domain-specific entity (e.g. drugs) from social media posts | High |
| Translation | Translate a document in a source langauge to a different target language | Translate text with less time and expense than human translation | | Large deep learning model needed for best performance | Translate survey input in multiple languages to a single target language | Low |
| Zero-Shot Classification | Classify documents without explicitly training the model on the classification task | Solve a classifciation problem without labeled data | Measurement, Prediction | Deep learning model, can be computationally expensive | Any classification problem where labeled data is not available / prohibitive | Medium |
| Semantic Similarity | Determine how similar two documents/sentences/words are | Find documents similar to a target document | Discovery | Generate embeddings or use pre-trained embeddings | Find proposal texts similar to a target RFA (e.g. Rfpro) | Medium |
| Conversational | Engage in conversation with a human in natural language | Resolve human questions/requests through conversation | | Iterative data labeling process, deep learning model | Build a chatbot to converse with a target population, e.g. victims of burglary | High |
| Feature Extraction (Embeddings) | Generate numeric representations of the meaning of documents/sentences/words | Many tasks rely on embedding representations | Discovery | Full document texts for training | Cluster terms based on similarity of meaning | High |

† We use the term "stage" to replace what the authors describe as "task" to avoid collision with our concept of a NLP task.
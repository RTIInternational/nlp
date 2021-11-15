# NLP Tools

Collection of useful open-source NLP tools and their applications.

| Tool | Summary | Applications |
| --- | --- | --- |
| [spaCy](https://spacy.io/) | Broad NLP library with a wide variety of uses and a huge ecosystem | Often a good starting point for NLP tasks. Useful for processing raw text and converting it to a corpus of documents via tokenization, lemmatizing, tagging, parsing, etc. Pretrained models can be used for a wide variety of tasks. Recently, spaCy has expanded to include transformer-based models.
| [Gensim](https://radimrehurek.com/gensim/) | Focused on topic modeling, generating embeddings, and semantic similarity | Very good for generating word/sentence embeddings
| [Hugging Face](https://huggingface.co/) | Easy access to a wide variety of cutting-edge deep learning models for NLP | Easy access to deep learning models through Model Hub and the `transformers` package. Can also store your own models on the Model Hub.
| [gobbli](https://github.com/RTIInternational/gobbli) | RTI-developed library designed to provide a uniform interface to various deep learning models for text | Abstracts away much of the complexity of using deep learning models for NLP. A good starting point for trying out deep learning on a NLP task.
| [scattertext](https://github.com/JasonKessler/scattertext) | Find and visualize terms that distinguish corpora | A purpose-built tool for the specific task of finding out what terms distinguish one corpus from another
| [textaCy](https://github.com/chartbeat-labs/textacy) | Extend spaCy's functionality with a variety of tasks that often come before an after a spaCy pipeline | Preprocess text before processing it with spaCy; extract structured information from processed documents, including n-grams, entities, acronyms, keyterms, and SVO triples
| [BERT](https://github.com/google-research/bert) | Deep learning model from Google which smashed benchmarks in 2018 and ushered in a new era of deep learning for NLP | The bidirectional transformer architecture introduced by BERT underlies most state of the art NLP models. This alone does not always make BERT the best tool for the job, but it's worth understanding how it works.
| [NLTK](https://www.nltk.org/) | General purpose NLP library, less robust than spaCy but great for learning | Venerable NLP library for Python. A bit outdated and less suited for production use than spaCy, but the accompanying [NLTK book](https://www.nltk.org/book/) makes it a great learning tool.
| [OpenNMT](https://opennmt.net/) | Pretrained models and API for neural machine translation | Deep learning models trained for sequence-to-sequence tasks
| [Rasa](https://rasa.com/) | Chatbot platform | Feature-rich platform for training and deploying conversational models
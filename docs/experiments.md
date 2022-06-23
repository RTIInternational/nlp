# Experiments/Experiences
The purpose of this page is to document uses of different NLP tools across projects to get a better understanding of which approaches did or did not work on given data.

## Contextual Topic Models
**Motivation for Experiment**: Embeddings + Clustering gives good results, but the clusters are uninterpretable or need manual review to provide a label
**Outcome**: Didn't work 
**Hypotheses for Outcome**: 
- Might not work with longer data (I used the mean sentence embedding from each doc's full title and selftext)
- Might still struggle with smaller corpus sizes
**Evidence**: Didn't separate out meaningful clusters from 1234 reddit posts about fentanyl overdose (in comparison to embeddings and DBSCAN)
**Other notes**: [Package](https://github.com/MilaNLProc/contextualized-topic-models/) seems to work great and was updated. 



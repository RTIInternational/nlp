# Experiments/Experiences
The purpose of this page is to document uses of different NLP tools across projects to get a better understanding of which approaches did or did not work on given data.

## Template
**Motivation for Experiment**:

**Outcome**:

**Hypotheses for Outcome**:

**Evidence**:

**Other notes**:

## Contextual Topic Models
**Motivation for Experiment**: Embeddings + Clustering gives good results, but the clusters are uninterpretable or need manual review to provide a label

**Outcome**: Didn't work 

**Hypotheses for Outcome**: 
- Might not work with longer data (I used the mean sentence embedding from each doc's full title and selftext)
- Might still struggle with smaller corpus sizes

**Evidence**: Didn't separate out meaningful clusters from 1234 reddit posts about fentanyl overdose (in comparison to embeddings and DBSCAN)

**Other notes**: [Package](https://github.com/MilaNLProc/contextualized-topic-models/) seems to work great and was updated. 

## Text cluster characterization
**Motivation for Experiment**: Embeddings + Clustering requires manual review; how can we give reviewers a summary of the cluster?

**Approaches**:
- Build a simple app to sample document texts from the cluster
- Most common n-grams in cluster (remove stopwords)
- N-grams in cluster with highest TF-IDF value
    - Could also treat all docs in each cluster as a single doc, and calculate TF-IDF at this cluster-doc level (haven't tried this)
- Chi-squared for top n-grams to find n-grams which are most unique to the cluster
    - 2x2 table comparing docs in cluster containing n-grams to docs in all other clusters containing n-grams
    - Allows for comparison of a cluster to all other clusters
- Scattertext package to find characteristic terms
    - Intended to compare documents from two corpuses
    - Can also frame as docs in one cluster vs another cluster, or docs in one cluster vs docs in all other clusters
- Cluster quality scores to help determine which clusters to keep/discard
    - sklearn includes lots of [cluster evaluation metrics](https://scikit-learn.org/stable/modules/clustering.html#clustering-performance-evaluation)

**Outcomes**:
- N-grams are cheap and effective, but require lots of stopword removal, and don't explicitly measure what makes a cluster unique
- Chi-squared solves that, but is expensive, and deciding which terms to calculate it for is tricky (e.g., if you calculate only for top n-grams, you might be missing terms that were less common but more unique)
- Scattertext also solves that, and is more efficient than calculating chi-squared for all terms, but includes its own overhead of making visualizations for each comparison
    - Future work might rewrite the scaled F-score in our own package, without the viz overhead
- Cluster quality scores are expensive

**Hypotheses for Outcome**: 
- No free lunch. Going beyond simple frequency to what makes a cluster unique requires a lot more computation.

**Evidence**: Survey of Earned Doctorates ProQuest project

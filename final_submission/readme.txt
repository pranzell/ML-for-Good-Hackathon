
EFFORT 1: Clustering of ProlificAcademic data for the 4 months based on "specifypositive" column

  - Jupyter notebook file name : "clustering_effort_1.ipynb"
  - Notebook with the last successful run at "https://www.kaggle.com/zenbird01/pranjalpathak-semantic-clustering-v1-0/notebook"
  - Separate clustering has been done for Adults and Parents
  - Generated 90 clusters for adults and 65 clusters for parents data

  - Iterative semantic clustering
    1. Runs contextual learning to get similar records and using this runs iterative clustering to get a final list of similar vectors.
    2. Uses 'all-distilroberta-v1' for vectorization
    3. Uses spacy for cleaning and lemmatization
    4. Uses sparse matrix multiplication for generating similar vetors
    5. Uses heuristic for number of clusters

  - Results of clustering have been saved in 2 CSVs: "df_adults_clusteredResults_26112021.csv" and "df_parent_clusteredResults_26112021.csv"

  - Although multiple clusters were generated in this method but no clear inference could be made. Data is such that multiple topics 
    are found in each data point and hence, it's tough for this algorithm to assign the data point to a specific cluster (with a high probability)

  - To run with new data, select a dataset and run the flow, keeping ::config:: updated everywhere!



EFFORT 2: Topic Modelling on clusters generated for 4 months of ProlificAcademic data on "specifypositive" column
 
  - Jupyter notebook file name alongwith last successful run: "clustering and topic modelling effort_2.ipynb"
  - New cluster were formed using a different technique in order to get more well defined boundaries
  - Uses BERTopic to cluster and model topics each row of "specifypositive" column for 4 months
  - Finds 15 clusters for adults' data and 13 for parents' data
  - For each cluster, main topics are then being extracted.
  - A topic is mainly represenated by top representative words form that cluster. It's upto the user to give an umbrella term to the cluster. 
  - Cluster analysis has been performed to find information for each cluster using visualizations

  - Results: 
    1) Clustering results have been saved in 2 CSVs: "df_parents_topic_allotment.csv" and "df_adults_topic_allotment.csv"
    2) Top topics and terms for each cluster has been saved in 2 CSVs: "df_parents_topic_details.csv" and "df_adults_topic_details.csv"

  - Clusters formed have better separation than the previous effort. Cluster analysis show that top terms in a cluster belong under a similar umbrella.
    Some of the important clusters are about "health", "family", "homeschooling", "anxiety". Each row from "specifypositive" column have been assigned 
    to one of the many clusters found.
	


Effort 3: Keywords & sentiments analysis

  - Notebook with the last successful run at "https://www.kaggle.com/zenbird01/pranjalpathak-semantic-clustering-v1-0/notebook". This is in continuation
    with the work done in effort 1.
  - Sentiments analysis have been done for each of parents and adults dataset. 2 columns have been used for the task: specifypositive and anything_else
  - Since "specifypositive" only talks about positive things, not a lot could be inferred by doing sentiment analysis.
  - For "anything_else" column, emotion and sentiment analysis clearly shows segregation in "fear", "sadness", "joy", "anger".
  - Using: RobertaBert_v1 emotion and sentiment
  
  - Final output excel has two sheets: 
    1) For adults' data: 
	"df_adult_clustered_01122021"  -  On specifypositive column
	"df_adult_any_01122021"  -  On anything_else column

    2) For parents' data: 
	"df_parent_clustered_01122021"  -  On specifypositive column
	"df_parent_any_01122021"  -  On anything_else column


Key resources and packages: sklearn, numpy, pandas, sklearn, networkx 

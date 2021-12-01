Code: https://www.kaggle.com/zenbird01/pranjalpathak-semantic-clustering-v1-0/notebook

Part 1: Iterative semantic clustering

1. Runs contextual learning to get similar records and using this runs iterative clustering to get a final list of similar vectors.
2. Uses 'all-distilroberta-v1' for vectorization
3. Uses spacy for cleaning and lemmatization
4. Uses sparse matrix multiplication for generating similar vetors
5. Uses heusristic for number of clusters
 
>> Select a dataset and just run the flow, keeping ::config:: updated everywhere!


Part 2: Keywords & sentiments

1. Run acc the flow
2. Using: RobertaBert_v1 emotion and sentiment
3. Download the files using given script
4. Use excel format
5. Final output excel will have two sheets: 'Detailed' with all records id wise, and 'month_wise' with analyzis across months.

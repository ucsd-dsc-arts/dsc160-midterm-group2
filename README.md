# Project Title

DSC160 Data Science and the Arts - Midterm Project Repository - Spring 2020

Project Team Members: 
- Farhood Ensan, fensan@ucsd.edu
- Rebecca Hu, reh016@ucsd.edu
- Alex Luo, ayl081@ucsd.edu
- Sharmi Mathur, s3mathur@ucsd.edu

## Abstract

(10 points) 

  Genre as we know it classifies music based on a variety of not only musical qualities but social ones. Music might be associated with each other because of their time period, the artist who produced them, their popularity, and myriad other components that may have little to do with how the music actually sounds. We decided to see if an unsupervised machine learning algorithm might spurn the biases of our social expectations of genre and cluster songs by the similarity of their audio features alone. We hypothesize that while the way people classify genres has a lot of historical and social context inherently, a machine algorithm could potentially draw unique connections between songs based purely on the audio features.

  Inspired by genre classification using an SVM in class, we instead use unsupervised learning for genre classification. We will scrape different genres of audio data from freemusicarchive.org. With the librosa library, we will use the librosa.feature functions to extract the features MFCC, CENS, and spectral contrast. We will test hierarchical density-based clustering, k-means, and affinity clustering and examine the way the grouping results interact genre conventions. Results will be presented in graphs, charts, and sonification. Because the algorithm will only intake data about what the song sounds like, we hope that it will draw novel connections between unusual songs in a potentially genre-breaking way. 


## Data

(10 points) 

The cultural data source we use in our project is an audio dataset from Free Music Archive (FMA), an online audio library containing legal music from various genres and artists. The dataset was created in 2016 and contains data that is natively digital. This open-source dataset was created by Defferrard, et al. and more information regarding the collection and curation of this dataset can be found in [their paper](https://arxiv.org/pdf/1612.01840.pdf). The specific files we used for our analysis included features of audio files extracted using the Librosa library, as well as metadata regarding each track's associated genres and artist. 


## Code

(20 points)

Data Acquisition:
- [Data Acquisition](https://github.com/ucsd-dsc-arts/dsc160-midterm-group2/blob/master/code/data_acquisition.ipynb): This notebook cleans the reorganizes the multi-indices in the <i>features.csv</i> and removes unnecessary columns to simplify our analysis. Note: Data can be downloaded from [this repository](https://github.com/mdeff/fma). 

Preprocessing:
- [Feature Extraction](https://github.com/ucsd-dsc-arts/dsc160-midterm-group2/blob/master/code/Data-Select-Feature-Extract.ipynb)

Analysis:
- [EDA](https://github.com/ucsd-dsc-arts/dsc160-midterm-group2/blob/master/code/eda.ipynb): This notebook calculates some basic statistics on the dataset to gain a general understanding of how the genres are distributed and how long the tracks are on average. It generate outputs inline within the notebook.

Generating Results:
- [Affinity Propagation](https://github.com/ucsd-dsc-arts/dsc160-midterm-group2/blob/master/code/affinity_propagation.ipynb):: Affinity propagation is a graph-based clustering method that relies on the concept of passing messages between data points. Unlike many other clustering algorithms, affinity propagation does not require an inputted parameter to specify a fixed number of clusters. 
- [Agglomerative Clustering](https://github.com/ucsd-dsc-arts/dsc160-midterm-group2/blob/master/code/Agglomerative_UMAP.ipynb): Hierarchical clustering is a general family of clustering algorithms that build nested clusters by merging or splitting them successively. Agglomerative clustering recursively merges the pair of clusters that minimally increases a given linkage distance. The linkage criteria determines the metric used for the merge strategy. We used the default ward which is a variance-minimizing approach and in this sense is similar to the k-means objective function but tackled with an agglomerative hierarchical approach.

- [DBSCAN](INSERT LINK HERE)
- [K-Means with PCA](https://github.com/ucsd-dsc-arts/dsc160-midterm-group2/blob/master/code/Kmeans_PCA.ipynb)
- [K-Means with UMAP](https://github.com/ucsd-dsc-arts/dsc160-midterm-group2/blob/master/code/UMAP.ipynb)
- [MeanShift Results](INSERT LINK HERE)

## Results

(30 points) 

This section will contain links to documentation of your results. This can include figures, sound files, videos, bitmaps, as appropriate to your domain of analysis. Each result should include a brief textual description, and all should be listed below: 

- [Affinity Propagation Results](https://github.com/ucsd-dsc-arts/dsc160-midterm-group2/blob/master/results/af_results.jpg)
- [Agglomerative Clustering with UMAP Results](https://github.com/ucsd-dsc-arts/dsc160-midterm-group2/tree/master/results/Agglomerative_UMAP)
- [DBSCAN Results]()
- [K-Means with UMAP Results]()
- [K-Means with PCA Results](https://github.com/ucsd-dsc-arts/dsc160-midterm-group2/tree/master/results/Kmeans_PCA)
- [MeanShift Results]()

Add some links to notable/example audio files here:
- [LINK]()
- [LINK]()
- [LINK]()


## Discussion

(30 points, three to five paragraphs)

The first paragraph should be a short summary describing your results.

The subsequent paragraphs could address questions including:
- Why is this culturally relevant?
- How does your computational approach differ from the traditional art historical, musicological, manuel/subjective approach to analyzing your cultural subject? 
- How do you think the original artists/musicians would respond to this type of analysis? Would it change/inform their practice in some way?
- How do your results relate to broader social, cultural, economic political, etc., issues? 
- In what future directions could you expand this work?


 The way that songs are thought to be classified into genres can be described as hierarchical in nature. There are broad buckets that most songs fit into, and then some songs can be further classified into subgenres. However, the labeled genre of a song can also be influenced by non-musical factors, like who the artist is or other cultural and societal reasons. The results of our project suggest that genres of music may be more fluid than we previously believed. We intentionally chose songs from four very distinct genres (Rock, Hip Hop, Electronic, and Folk) to see how an unsupervised algorithm would form new clusters of similar songs along novel dimensions based on Librosa-derived audio features.
 <br> Factors that go into determining a song’s genres include, but are not limited to, its audio qualities, the artist(s) that created the piece, the time period during which it was made, and its lyrics. Although there is no objectively correct way of categorizing music, generally we assume to only find music with similar audial characteristics within a particular genre. However, if an artist typically known for their rock music releases a song with heavy folk influences, it is possible that the song could lack a “folk” genre label, even if such a label would be appropriate. We sought to explore how songs might be classified into genres if only the audio features, rather than any metadata, of the music were used to determine what category each song belonged to.
 <br> [INSERT PARAGRAPH HERE: How do you think the original artists/musicians would respond to this type of analysis? Would it change/inform their practice in some way?]
 <br>[INSERT PARAGRAPH HERE: How do your results relate to broader social, cultural, economic political, etc., issues? ]
<br> Future directions for this project could include refining the resulting visualizations to include tooltips that would allow users to listen to the audio files as they scroll over each data point on the scatterplot. This would allow for a user-friendly interface to allow us to characterize the resulting clusters more efficiently. Given more time, we would have also liked to try more clustering algorithms as well as different feature selection methods.


## Team Roles

- Farhood Ensan: 
- Rebecca Hu: 
- Alex Luo: 
- Sharmi Mathur:

## Technical Notes and Dependencies

Any implementation details or notes we need to repeat your work. 
- Additional libraries you are using for this project
- Does this code require other pip packages, software, etc?
- Does this code need to run on some other (non-datahub) platform? (CoLab, etc.)

## Reference

References to any papers, techniques, repositories you used:
- Papers
- Repositories
- Blog posts
- https://arxiv.org/pdf/1612.01840.pdf
- https://github.com/mdeff/fma
- https://towardsdatascience.com/how-to-cluster-in-high-dimensions-4ef693bacc6
- https://medium.com/latinxinai/discovering-descriptive-music-genres-using-k-means-clustering-d19bdea5e443

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
- [Affinity Propagation](https://github.com/ucsd-dsc-arts/dsc160-midterm-group2/blob/master/code/affinity_propagation.ipynb)
- [Agglomerative Clustering](https://github.com/ucsd-dsc-arts/dsc160-midterm-group2/blob/master/code/Agglomerative_UMAP.ipynb)
- [DBSCAN Results](INSERT LINK HERE)
- [K-Means with UMAP](https://github.com/ucsd-dsc-arts/dsc160-midterm-group2/blob/master/code/UMAP.ipynb)
- [MeanShift Results](INSERT LINK HERE)

## Results

(30 points) 

This section will contain links to documentation of your results. This can include figures, sound files, videos, bitmaps, as appropriate to your domain of analysis. Each result should include a brief textual description, and all should be listed below: 

[Affinity Propagation Results](https://github.com/ucsd-dsc-arts/dsc160-midterm-group2/blob/master/results/af_results.jpg)
[Agglomerative Clustering Results]()
[DBSCAN Results]()
[K-Means with UMAP Results]()
[MeanShift Results]()

Add some links to notable/example audio files here:
[LINK]()
[LINK]()
[LINK]()


## Discussion

(30 points, three to five paragraphs)

The first paragraph should be a short summary describing your results.

The subsequent paragraphs could address questions including:
- Why is this culturally relevant?
- How does your computational approach differ from the traditional art historical, musicological, manuel/subjective approach to analyzing your cultural subject? 
- How do you think the original artists/musicians would respond to this type of analysis? Would it change/inform their practice in some way?
- How do your results relate to broader social, cultural, economic political, etc., issues? 
- In what future directions could you expand this work?

## Team Roles

- Farhood Ensan: 
- Rebecca Hu,: 
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

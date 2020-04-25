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

This section will describe your data and its origins. Each item should contain a name of the data source, a link to the source, and any necessary background information such as:
- What is your cultural data source? 
- When was it made? 
- Who created the works? 
- Is it digital native, or is it some kind of scan, recording, photo, etc., of an analog form? 

## Code

(20 points)

This section will link to the various code for your project (stored within this repository). Your code should be executable on datahub, should we choose to replicate your result. This includes code for: 

- data acquisition/scraping
- cleaning
- analysis
- generating results. 

Link each of your notebooks or .py files within this section, and provide a brief explanation of what the code does. Reading this section we should have a sense of how to run your code.

## Results

(30 points) 

This section will contain links to documentation of your results. This can include figures, sound files, videos, bitmaps, as appropriate to your domain of analysis. Each result should include a brief textual description, and all should be listed below: 

- image files (`.jpg`, `.png` or whatever else is appropriate)
- audio files (`.wav`, `.mp3`)
- written text as `.pdf`

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

Provide an account of individual members and their efforts/contributions to the specific tasks you accomplished.

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

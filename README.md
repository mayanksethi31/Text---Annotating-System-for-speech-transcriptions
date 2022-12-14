# Final Project 
Submission for INFO 202: Information Organization and Retrieval.

 # Text Annotation System and Comparison
Implementation of Annotation system and comparison of the same via human-coded tags. 

# Introduction


# Project Concepts
These were the concepts covered in this project(I enjoyed learning further)

# 1. Classification:
The concepst of genre is very vague and rely heavily on the feeling. I feel labelling an artist to a genre is restricting and dis-respectful to the art. The genre classification and song categorisation as binary is uncreative. The "Protoype Theory"Read more here , is really an interesting way to understanding the songs and the concept of genre. Since lot of time songs could lie in fuzziness for different genre. Like the "Bohemian Rapsody" by queens could be more towards rock in comparison to Careless whisper(it's often labelled as yatch rock), or is very less rock in comparison to "Thunderstruck" by AC/DC. Hence genre classification is more in relative terms rather than absolute hence the concepts of distance between artist and their lyrics could provide how close ther are to each other.

# 2. Web Scrapping:
I learnt the concepts of web crawling how it gather all the available information while scraping is retriving only of the relevant data. Inorder to gather lyrics data I used Genius API, and request to get details of top 100 song of artist provided and then used the list to search and then retrieve the lyrics. The whole process indeed was taxing and time consuming(sepcially Timeout Error after 20 minutes etc.), however I could gather the exact data which would be relevant for the project.

# 3. Bag of Words:
In this model the song lyrics document is divided in to words with respective frequencies (frequently used words) then to viusalise it we plotted bar graphs and word clouds for each of the artist.

# 4. Word Embedding & Document Embedding (it's implementation) :
The concept of word embedding and document embedding is based on conversion to vectors form, aslo taking into account the contextual orientation. "You Are the Average of the Company You Keep" The concept of doc2vec is context window, which slide through the paragraphs and captures the meaning of the words while continuing shift.

# 5. Model Visualisation:
It really difficult to visualised any vector with some many dimension so we need to visualise it in human underderstandable visualisations. There are many ways to do that like PCA, t-sne, UMap etc. However to ensure it's interactive, I searched about tensorboard and converted my model into an understandable .tsv file.

# Implementation:

1.Create a list of documents, where each document contains all the lyrics of an artist. 2.Clean the document and tokenize, removing stop words (eg. at, to, for, etc.) 3.Using Doc2vec trained over the list of the documents, convert every artist to a vector. 4.Visualize these vectors, to understand the closeness of different artists. 5.Visualize the artist’s word usage and frequency using a word cloud. 6.Derive insights from the visualization - (using PCA on tensorboard projector )

# Instructions to Run the project

# Conclusion


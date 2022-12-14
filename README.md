# Final Project 
Submission for INFO 202: Information Organization and Retrieval.

 # Text Annotation System and Comparison
Implementation of an Annotation system using two approaches and comparison of the same. 

# Introduction
Text annotation is of utmost importance in the field of survey analysis and qualitative analysis of large volumes of text. 
When analyzing surveys of texts, we are required to tag or give categories to the same for higher-level analysis of what's being discussed. 
Further, there could be further different types of practices to code, wherein one could be Axial, selective, or open codes.
So, to generate categories from the content mentioned, the project proposes a topic modeling approach to put focus on the words mentioned in the sentences and then formulate categories from the words in the same. This has further been benchmarked to analyze its utility for human usage as to whether it's good enough to be used or not using the Inter Annotator Agreement evaluation on the same.

# Project Concepts
These were the concepts covered in this project(I enjoyed learning further)

1. Grounded Coding:
The concept of grounded coding to analyze surveys, interviews, and text more qualitatively has been the key concept for which the system of text annotation has been developed. The whole idea of the project is to develop a better coding system for texts and evaluate its reliability.

2. Word Embeddings, Bag of Words, and Tf-IDF: 
These are techniques to represent text words in terms of vectors for the document. These are usually used for representing the document in terms of vectors and doing analysis over the same. TF-IDF on the other hand gives a weighing approach to words which might be more important for making better judgments about the content in the text document by evaluating the frequency of the words and their frequency in the whole document. These approaches are very much useful for understanding the semantics of a document and understanding the similarity between two distinct documents.

3. Stemming and Lemmatization: 
This is a technique to standardize different forms of the words giving the same sense of meaning for further content and text analysis. While doing the preprocessing, I included a stemmer and lemmatizer to convert different forms of the words to the same before generating the vector representation of the same set of texts.

4. Topic Model:  
These are probabilistic methods of extracting themes and the model used in the project is LDA, fully written as Latent Dirichlet Allocation. There are other methods also of assigning topics to texts like LSA, and CTM. It is an unsupervised method of assigning topics/themes to documents which are evaluated using the word vectors and running probability evaluation on the set of documents.

5. Inter annotator Agreement: 
This is a calculation procedure to evaluate whether a coding technique under use is reliable enough to develop and tag categories of texts which make sense to us reliably and do not cause confusion at the same time. After generating the categories through LDA, I have benchmarked this technique by evaluating this report and calculating the Kappa score to quantify the reliability against the coding done manually over a set of 30 documents selected equally from the 6 topics from the model.

# Implementation:

1. Firstly, the dataset of editorials has been fetched from Brown University which has maintained clean texts as part of the Natural Langauge Toolkit in python, which can be downloaded easily from the NLTK package.
2. The same set of texts has been put through a preprocessor function of the text, to standardize the different forms of the words using Stemmer, and Lemmatizer. Moreover, the same has been processed through the removal of stopwords like is, am are which don't add much value to the meaning of the text. 
3. Then, the cleaned set of texts has been processed to the word dictionary of NLTK having an extensive English Words dictionary. And, then using the same, I generated embeddings using Bag of Words. For comparison, I have also implemented generating the embeddings using tf-idf scores based on term frequency and inverse document frequency, which we can toggle when running the downstream process.
4. For the current pipeline, I have kept Bag of Words as the underlying technique for embeddings, and using the same, the model of LDA, which is an unsupervised learning method based on the probabilities of the words in the texts has been run over the dataset of 2700 text documents of editorials.
5. Further, I have generated 6 topics from a collection of 2700 documents to enable ease of understanding the same. 
6. Using the topic words from each of the 6 topics, I have developed tags for the categories/topics being represented using the topic words.
7. I have also generated the distribution of the documents across the 6. 
8. For the current pipeline, I have kept Bag of Words as the underlying technique for embeddings, and using the same, the model of LDA, which is an unsupervised learning method based on the probabilities of the words in the texts has been run over the dataset of 2700 text documents of editorials.  topics. 
9. Using the same set of codes, I have done grounded coding on a set of 30 documents as attached in the excel file to produce the Inter Annotator Agreement Evaluation report to benchmark whether the system is good enough over human-driven evaluation systems using the Kappa score.

Instructions to run the project

1. After loading the main code file, we import the relevant packages as mentioned in the notebook in the initial part.  
2. We load the brown university data on editorials as selected in the brown corpus of the NLTK package. 
3. Using the same LDA approach based on BOW or TF-IDF, we can generate a dataframe of the sentences, their probability scores for each topic, their dominant topic, and the corresponding name of the topic as a result.
4. The whole pipeline can be run through a single execution run over the entire code notebook. The whole notebook has no external dependency for dataset or anything as of currently. But, if there's another dataset required for generating the topics, the same can be developed and tweaked using a similar code line.

# Conclusion

After evaluating the topics of the words generated by LDA, I could get 6 topics as follows:

1. Development & Industry -  Having mentions of the development and Industry impact-related themes.
2. General Debates of People - Having themes of general discussion or talks regarding people and by people.
3. Governments & Nations - Having themes of government activities and nations.
4. People & Political Parties - Having themes of political parties and people impacted due to their activity.
5. Presidents and Politics - Themes related to people at esteemed legislative positions.
6. War & Power - Themes mentioning war and the use of power to drive or motivate them.

The above categories have been developed using the words mentioned in the code notebook for every topic.

Further, after evaluating the tagging with human-generated codes using the categories, we see that there is 70% agreement between the two approaches.
Finally, the reliability score was evaluated using the Cohen Kappa score of 0.64 which suggests that there is relatively good agreement between the two techniques being used in the project.

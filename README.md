## NLP: Topic Modelling on COVID-19 Research Papers
This project applies unsupervised machine learning techniques—specifically Latent Dirichlet Allocation (LDA)—to uncover hidden thematic structures in a collection of research papers related to COVID-19. By analyzing abstracts and titles, we aim to automatically extract key research topics from a large document corpus.

### Dataset
Source: NIH COVID-19 Portfolio

Contents: Research paper titles and abstracts

### Goal
To identify and visualize latent topics within the COVID-19 research corpus using LDA, and compare results between abstracts and titles.

### Process Overview
Text Preprocessing

Remove stopwords (NLTK + spaCy)

Build bigrams & trigrams using Gensim’s Phrases

Lemmatize using spaCy

Remove emails, special characters, punctuation

Tokenize and clean sentences

Topic Modeling with LDA

Create id2word dictionary and corpus (bag of words)

Train base LDA model using Gensim

Experiment with different alpha values

Use Mallet LDA for better topic separation

Evaluation and Correlation

Use Spearman correlation to compare topic distributions in titles vs abstracts

Visualize topics with pyLDAvis

#### Tools & Libraries
Python

Gensim (LDA, Coherence)

Mallet LDA

spaCy (en_core_web_sm)

NLTK (stopwords)

PyLDAvis (interactive visualization)

Pandas, NumPy, Matplotlib, re

#### Visualization Insights
Each bubble in PyLDAvis = 1 topic

Size = topic prevalence

Distance = topic dissimilarity

Ideal model: large, non-overlapping, well-distributed bubbles

Too many topics: small, overlapping bubbles

#### Experiments

Model Variant	Description
Base LDA Model	Default alpha and beta settings
Alpha-Tuned LDA	Adjusted alpha values to optimize coherence
Mallet LDA Model	Used Java-based Mallet toolkit via Gensim

#### Output
Top keywords per topic

Document-topic distribution

PyLDAvis HTML visualizations

Correlation charts between title-based and abstract-based topics

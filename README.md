# Machine Learning Engineer Nanodegree

# Deep Learning

## Project 2: Plaigarism Detector using AWS SageMaker

### By Vedavyas Kamath

### Goal/Aim
To build and train a plagiarism detector that examines a text file and performs binary classification by labeling that file as either *plagiarized* or *not*, depending on how similar that text file is to a provided source text. Detecting plagiarism is an active area of research with the task being non-trivial and the differences between paraphrased answers and original work are often not so obvious.

### Dataset:
For this project we used a slightly modified version of a dataset created by Paul Clough (Information Studies) and Mark Stevenson (Computer Science), at the University of Sheffield. We have a number of text files and each text file has an associated plagiarism label/category. 
The different possible labels/categories these files can be associated to are listed below:
1. `cut`: An answer is plagiarized; it is copy-pasted directly from the relevant Wikipedia source text.
2. `light`: An answer is plagiarized; it is based on the Wikipedia source text and includes some copying and paraphrasing.
3. `heavy`: An answer is plagiarized; it is based on the Wikipedia source text but expressed using different words and structure. Since this doesn't copy directly from a source text, this will likely be the most challenging kind of plagiarism to detect.
4. `non`: An answer is not plagiarized; the Wikipedia source text is not used to create this answer.
5. `orig`: This is a specific category for the original, Wikipedia source text. We will use these files only for comparison purposes.

NOTE: So, out of the submitted files, the only category that does not contain any plagiarism is `non`. <br>
You can read all about the data collection and corpus, at their university webpage [here](https://ir.shef.ac.uk/cloughie/resources/plagiarism_corpus.html#Contents)

### Project Overview
This project is broken down into three main notebooks as below with specific tasks performed in each book:

**Notebook 1: Data Exploration**
* Load in the corpus of plagiarism text data.
* Explore the existing data features and the data distribution.
* This first notebook is **not** required in your final project submission.

**Notebook 2: Feature Engineering**
* Clean and pre-process the text data.
* Define features for comparing the similarity of an answer text and a source text, and extract similarity features.
* Select "good" features, by analyzing the correlations between different features.
* Create train/test `.csv` files that hold the relevant features and class labels for train/test data points.

**Notebook 3: Train and Deploy Your Model in SageMaker**
* Upload your train/test feature data to S3.
* Define a binary classification model and a training script.
* Train your model and deploy it using SageMaker.
* Evaluate your deployed classifier.

---

### Software Requirements
This project requires **Python 3.x** and the following Python libraries installed:

- [SageMaker](https://sagemaker.readthedocs.io/en/stable/)
- [Scikit-learn](https://scikit-learn.org/stable/)
- [Pandas](https://pandas.pydata.org/)
- [NumPy](http://www.numpy.org/)

### Instructions
Please see the [README](https://github.com/udacity/ML_SageMaker_Studies/tree/master/README.md) in the root directory for instructions on setting up a SageMaker notebook and downloading the project files (as well as the other notebooks).

### Citations
- Clough, P. and Stevenson, M. Developing A Corpus of Plagiarised Short Answers, Language Resources and Evaluation: Special Issue on Plagiarism and Authorship Analysis, In Press. [Download](https://ir.shef.ac.uk/cloughie/resources/plagiarism_corpus.html)


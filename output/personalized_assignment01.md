### Assignment Title: Personalized Project - CNN for News Headline Categorization

Hi Alice,

That's an excellent project idea! Classifying news headlines into categories using Convolutional Neural Networks is a fantastic way to apply the concepts we've learned in the "Convolutional Neural Networks for Text Mining" lecture. It directly tackles a real-world NLP problem, allowing you to explore how CNNs can capture crucial semantic patterns.

### Summary of Lecture based on the provided PDF file named lecture_4.pdf

Our recent lecture introduced Convolutional Neural Networks (CNNs) as powerful tools, originally from computer vision, now widely applied in Text Mining. We began by understanding how complex text data can be transformed into numerical representations, specifically **word embeddings**, which are then fed into machine learning algorithms like CNNs for tasks such as prediction and recommendation.

We dived into **Text Classification**, a supervised learning task where a given text is mapped to a specific class, exemplified by sentiment classification. The underlying mechanism involves a **binary cross-entropy loss** function to guide the learning process.

The core of CNNs lies in their **convolutional layers**, which employ filters (kernels) to slide over input data (e.g., an image or a word embedding matrix), computing dot products to generate **feature maps**. These operations are fundamental for detecting local features like edges in images, or n-grams in text. We explored the history of CNNs, from Hubel & Wiesel's work on visual cortex to early networks like LeNet-1 and AlexNet, demonstrating their evolution and widespread success in image recognition.

Key parameters in convolutions include **stride** and **padding**, which dictate how the filter moves across the input and how spatial dimensions are preserved or altered. We discussed the formula for calculating output size based on input size, filter size, stride, and padding, and the importance of non-linear activations (like ReLU) following convolution.

**Pooling layers**, particularly max-pooling, were introduced as a second crucial component. These layers deterministically reduce the spatial size of the input, focusing on the most salient features (e.g., the highest activation) within a neighborhood, without adding learnable parameters. This is crucial for reducing computational load and preventing overfitting. A significant advantage of CNNs over traditional fully connected networks is their **parameter efficiency**, which we illustrated with a comparative example.

Finally, we transitioned to **CNNs for Text**, specifically focusing on their application in Natural Language Processing. The **Kim 2014 (EMNLP) model** for sentence classification served as a prime example, using concatenated word embeddings as input. We examined its architecture, which typically involves convolutions with various filter sizes (to capture different n-gram lengths), followed by max-over-time pooling, a fully connected layer, dropout for regularization, and a softmax output. Different **embedding strategies** were discussed, including `cnn-rand`, `cnn-static`, `cnn-nonstatic`, and `cnn-multichannel`, with a key finding being the effectiveness of pre-trained embeddings fine-tuned for the task. We also briefly touched upon **character-level CNNs**, which operate on sequences of characters rather than words, offering an alternative approach when word-level embeddings might be limiting or for languages without clear word boundaries.

### 1. Project Overview & Your Goal

Your project to build a CNN that classifies news headlines into categories like 'Technology', 'Sports', and 'Business' is an excellent application of the principles we've discussed. Your key question, "Can a simple CNN with different filter sizes effectively learn to distinguish between topics by capturing unique keywords and phrases (n-grams) specific to each category?", perfectly aligns with the core capabilities of convolutional layers in text analysis. By designing and experimenting with a CNN, you'll gain practical insight into how these networks identify and leverage localized patterns (like n-grams) within textual data to make classification decisions.

### 2. Your Tailored Assignment Path: Creative Build

For your **Creative Build**, you'll be focusing on designing, implementing, and evaluating a CNN for your chosen text classification task. This hands-on approach will allow you to explore the practical aspects of model construction, parameter tuning, and performance analysis in a domain of your interest.

### 3. Your Challenges

*   **🎯 Core Challenge:** Implement a word-level CNN classifier using Python with PyTorch or TensorFlow to categorize news headlines.
    1.  **Dataset Preparation:** Select a suitable news headline dataset with multiple categories. You may need to preprocess the text (tokenization, lowercasing).
    2.  **Embedding Strategy:** Implement at least two embedding strategies for your CNN:
        *   **Pre-trained Word Embeddings (fixed):** Initialize with pre-trained GloVe or Word2Vec embeddings and keep them non-trainable during model training (e.g., `cnn-static`).
        *   **Trainable Embeddings (initialized randomly):** Initialize word embeddings randomly and allow them to be updated during model training (e.g., `cnn-rand`).
    3.  **Varying Filter Sizes:** Experiment with at least three different filter sizes (e.g., 2, 3, 5 words) within your convolutional layer, similar to the Kim 2014 architecture.
    4.  **Evaluation:** Train your models and evaluate their performance using appropriate metrics (e.g., accuracy, F1-score) on a held-out test set. Discuss the impact of different embedding strategies and filter sizes on the classification accuracy and your ability to distinguish between categories.

*   **🚀 Stretch Challenge:** Deepen your analysis of n-gram capture and model interpretability.
    1.  **Filter Visualization/Analysis:** Devise a method to gain insight into what specific n-grams or patterns your CNN's filters are learning for different categories. This could involve identifying the top activating n-grams for a given filter or analyzing the feature maps.
    2.  **Character-level Exploration:** Briefly implement a simple character-level CNN for the same news headline classification task (you can use a subset of your data if training is computationally intensive). Compare its performance and discuss the trade-offs between word-level and character-level approaches for headline classification, especially considering your "Key Question" about unique keywords and phrases.

### 4. Recommended Resources & Next Steps

To successfully tackle this project, I recommend focusing on the following sections of our lecture material:

*   **Input Representation (Word Embeddings):** Review **Slides 43, 44, 48, and 49** for understanding how to represent text as embedding matrices and the different strategies (`cnn-rand`, `cnn-static`, `cnn-nonstatic`, `cnn-multichannel`). This is crucial for setting up your model's input.
*   **CNN Architecture for Text Classification:** Pay close attention to **Slides 45, 46, and 47**. These slides detail the architecture, including multiple filter widths and max-over-time pooling, which are central to your core challenge.
*   **Convolution Parameters:** Refer to **Slides 29-34 and 36** for a refresher on stride, padding, and the output size calculation. While `stride=1` is common for text, understanding these will aid in designing your layers.
*   **Pooling Layers:** **Slides 37 and 38** provide the intuition and purpose of pooling, especially max-over-time pooling in the context of text.
*   **Character-level CNNs:** For your stretch challenge, **Slides 53-55** offer a good overview of the character-level approach.
*   **General Model Evaluation:** Review **Slides 51 and 52** for insights into evaluating CNN performance in text classification.

You'll also find the provided `assignment_muster` useful, particularly **Part B: Applied Exercises (Programming) 1, 2, and 3** as they align well with the challenges described above.

### 5. Deliverables & Submission

Please submit the following components for your project:

1.  **Code Repository:** A link to a GitHub repository containing:
    *   Your Python code (Jupyter Notebook or `.py` scripts) for the word-level CNN and any character-level exploration. Ensure your code is well-commented and easy to follow.
    *   A `requirements.txt` file listing all necessary libraries.
2.  **Project Report:** A short report (PDF, 800-1000 words) addressing the following:
    *   **Introduction:** Briefly describe your project goal and the dataset used.
    *   **Methodology:** Detail your CNN architecture, embedding strategies implemented, filter sizes explored, and training setup.
    *   **Results & Discussion (Core Challenge):** Present your evaluation metrics (e.g., accuracy, F1-score) for the different embedding strategies and filter size combinations. Discuss your findings in relation to your "Key Question" – how effectively did the CNN capture category-specific keywords and phrases?
    *   **Stretch Challenge Findings (if attempted):** If you attempted the stretch challenge, describe your approach to filter visualization/analysis and/or the character-level CNN. Discuss any insights gained and compare performances.
    *   **Conclusion:** Summarize your main findings and reflect on the strengths and limitations of CNNs for news headline classification based on your experiments.

Good luck, Alice! I'm looking forward to seeing your insights into text classification with CNNs.
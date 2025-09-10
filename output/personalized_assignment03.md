### Assignment Title: Personalized Project - News Headline Classification with CNNs

Hi Alice,

That's an excellent project idea! Classifying news headlines into categories like 'Technology', 'Sports', or 'Business' is a fantastic real-world application and a great way to explore **Convolutional Neural Networks for Text Mining**. Your interest in how different filter sizes capture n-grams directly aligns with the core principles of CNNs in NLP. We've formalized it into the assignment plan below.

### Summary of Lecture based on the provided PDF file named lecture_4.pdf

The lecture "Convolutional Neural Networks for Text Mining" introduces CNNs, initially developed for computer vision, and their application to natural language processing tasks, particularly text classification.

**Core Concepts:**

1.  **Word Embeddings:** Text is transformed into numerical representations using word embeddings (e.g., Word2vec, GloVe), which serve as the input for the CNNs. These embeddings capture semantic meaning.
2.  **Convolutional Neural Networks (CNNs):**
    *   They are a type of partially connected feedforward network, originating from computer vision (Hubel & Wiesel, Neocognitron, LeNet-5, AlexNet).
    *   CNNs are highly parameter-efficient compared to fully connected networks.
3.  **Convolutions:**
    *   The fundamental building block. A "filter" or "kernel" (a small matrix) slides over the input (e.g., an image or a sequence of word embeddings), computing dot products to produce a "feature map."
    *   This process extracts local features like edges, blurring, or sharpening in images, and n-gram-like patterns in text.
    *   Key parameters include:
        *   **Input Dimensions:** (Image: Width x Height x Depth; Text: Sentence Length x Embedding Dimension)
        *   **Filter Dimensions:** (e.g., Fx, F, F for 3D)
        *   **Stride (S):** How many pixels/units the filter moves each step (determines output size).
        *   **Padding (P):** Adding zeros to the border of the input to control output size (e.g., preserve spatial dimensions).
        *   **Output Size Formula:** `(N - F + 2P)/S + 1`.
4.  **Pooling Layers:**
    *   Typically follow convolutional layers. They reduce the dimensionality of the feature maps.
    *   **Max Pooling** is common: it extracts the maximum value within a defined window (pool size) from the input.
    *   Pooling reduces the number of parameters in subsequent layers and captures the "strongest signal" from a local neighborhood, providing some translation invariance.
    *   Deterministic operation (no learned weights).
5.  **CNNs for Sentence Classification (Kim, 2014):**
    *   **Input Representation:** A sentence is represented as a matrix where each row is a word embedding, and columns are dimensions of the embedding (concatenated word embeddings).
    *   **Convolution Operation:** Filters slide over contiguous sequences of words (analogous to n-grams), extracting features. Multiple filter sizes (e.g., 3, 4, 5 words) are used to capture different n-gram lengths.
    *   **Max-over-time Pooling:** After convolution, a max-over-time pooling operation is applied over the *entire* feature map from each filter to select the highest output (most salient feature) for that filter.
    *   **Network Architecture:** Often consists of convolutional layers, max-over-time pooling, a fully connected layer, and a softmax output for classification.
    *   **Embedding Variants:**
        *   `cnn-rand`: Randomly initialized embeddings, trained with the model.
        *   `cnn-static`: Pre-trained embeddings (Word2Vec/GloVe), kept fixed during training.
        *   `cnn-nonstatic`: Pre-trained embeddings, fine-tuned during training.
        *   `cnn-multichannel`: Uses two sets of embeddings (one static, one fine-tuned) to preserve original information and learn task-specific features.
    *   **Regularization:** Dropout (after fully connected layer) and L2-maxnorm constraint are used to prevent overfitting.
6.  **Character-level CNNs:**
    *   An alternative approach that processes text as a sequence of characters instead of words.
    *   Learns features from scratch, ignoring the notion of words.
    *   Requires fixed-length input (padding with spaces if necessary).
    *   Can be robust to out-of-vocabulary words and typos.
7.  **Evaluation:** CNNs demonstrate strong performance in various text classification tasks, with pre-trained word embeddings generally yielding better results. The choice between static, non-static, or multichannel embeddings can vary in advantage depending on the task.

### 1. Project Overview & Your Goal
Your goal is to build a Convolutional Neural Network (CNN) that can accurately classify news headlines into predefined categories such as 'Technology', 'Sports', or 'Business'. This is a fantastic opportunity to apply the text classification concepts we discussed in the lecture, focusing on how CNNs extract meaningful patterns (like n-grams) from text. Your "Key Question" is: **Can a simple CNN with different filter sizes effectively learn to distinguish between topics by capturing unique keywords and phrases (n-grams) specific to each category?**

### 2. Your Tailored Assignment Path: Creative Build
For your **Creative Build**, you'll be focusing on the practical implementation and experimental evaluation of your CNN model. You will design, build, and train your model, then analyze its performance and specifically address your key question through your observations.

### 3. Your Challenges
*   **🎯 Core Challenge: Build and Evaluate a Multi-Filter CNN for Headline Classification**
    Implement a CNN for news headline classification. Your model should leverage **word embeddings** as input and incorporate **multiple convolutional filters of varying sizes** (e.g., 2, 3, 4, and 5 words, as discussed in the Kim 2014 model on slide 45). Follow this with a **max-over-time pooling** layer for each filter and combine their outputs for final classification. Train and evaluate your model on a suitable news headline dataset (e.g., AG News). Experiment with at least two embedding strategies:
    1.  **`cnn-static`**: Initialize with pre-trained word embeddings (e.g., Word2Vec or GloVe) and keep them fixed during training.
    2.  **`cnn-nonstatic`**: Initialize with pre-trained word embeddings but allow them to be fine-tuned during training.
    Compare the performance of these two approaches and report your classification accuracy and F1-score for each category.

*   **🚀 Stretch Challenge: Analyzing Filter Effectiveness and Exploring Character-Level Features**
    To delve deeper into your "Key Question," perform an analysis of your trained CNN:
    1.  **Filter Analysis:** Try to interpret what kind of n-gram patterns or features your filters are learning. This could involve examining the weights of highly activated filters or identifying common n-grams that frequently trigger specific filters. Discuss if different filter sizes appear to be more effective for particular types of category-specific phrases.
    2.  **Character-Level Comparison:** Implement a simple **character-level CNN** for the same classification task (as discussed on slide 53-54). Compare its performance to your word-level CNN and reflect on the trade-offs. Consider when a character-level approach might be advantageous (e.g., handling out-of-vocabulary words or misspellings in headlines).

### 4. Recommended Resources & Next Steps
To successfully complete your project, I recommend focusing on the following sections of the lecture and external resources:

*   **Lecture Slides:**
    *   **Page 2, 43:** Understanding word embeddings as input to your model.
    *   **Page 3-4:** Text classification as a supervised learning task and the binary cross-entropy loss.
    *   **Pages 17-26, 35:** How convolutions operate, especially with 3D inputs.
    *   **Pages 29-34:** The concepts of **stride** and **padding** and their effect on output dimensions – crucial for correctly designing your convolutional layers.
    *   **Pages 37-38:** The role and mechanism of **pooling layers**, particularly max-over-time pooling for text.
    *   **Page 39:** The parameter efficiency of CNNs compared to fully connected layers.
    *   **Pages 43-47:** The **Kim (2014) model architecture** for sentence classification is highly relevant to your core challenge, illustrating the use of multiple filter sizes and max-over-time pooling.
    *   **Page 48-49:** Details on **embedding strategies** (`cnn-static`, `cnn-nonstatic`, `cnn-multichannel`).
    *   **Page 53-54:** Introduction to **character-level CNNs**, relevant for your stretch challenge.
*   **Practical Guides:**
    *   Refer to PyTorch or TensorFlow tutorials on building CNNs for text classification.
    *   Explore datasets like AG News for news headline classification.

### 5. Deliverables & Submission
Please submit the following by the deadline:

1.  **Code Repository:** A link to a well-organized GitHub repository containing:
    *   Your CNN implementation (Jupyter Notebook or Python scripts) for the word-level CNN and, if attempted, the character-level CNN.
    *   Clear comments throughout your code.
    *   A `requirements.txt` file listing all dependencies.
2.  **Project Report (PDF or Markdown):** A document (approx. 700-1000 words) that includes:
    *   **Introduction:** Briefly state your project's objective.
    *   **Model Architecture:** Describe your CNN design, including filter sizes, pooling, and other hyperparameters.
    *   **Experimental Setup:** Detail the dataset used, preprocessing steps, and training procedure.
    *   **Results & Discussion:** Present your classification metrics (accuracy, F1-score per category) for both `cnn-static` and `cnn-nonstatic` embeddings.
    *   **Answering Your Key Question:** Directly address how different filter sizes capture unique keywords and phrases (n-grams) for category distinction based on your experiments and analysis.
    *   **Stretch Challenge Reflection (if attempted):** Discuss your insights from the filter analysis and the comparison with character-level CNNs.
    *   **Conclusion:** Summarize your findings and any challenges encountered.
3.  **Dataset:** If using a custom dataset, include it in your repository or provide a clear link for download.

Good luck, Alice! I'm looking forward to seeing your work!
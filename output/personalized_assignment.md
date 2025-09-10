### Assignment Title: Personalized Project - News Headline Classification with CNNs

Hi Alice,

That's an excellent project idea! Classifying news headlines into categories using Convolutional Neural Networks (CNNs) is a fantastic way to explore the capabilities of CNNs for Text Mining. Your "Key Question" – *Can a simple CNN with different filter sizes effectively learn to distinguish between topics by capturing unique keywords and phrases (n-grams) specific to each category?* – directly taps into the core strengths of CNNs in identifying local patterns (n-grams) in text. This project offers a practical and insightful application of the concepts we've covered.

### 1. Project Overview & Your Goal
Your goal is to build a CNN that can classify news headlines into relevant categories such as 'Technology', 'Sports', and 'Business'. This project will allow you to explore how CNNs, traditionally strong in image processing, can be adapted to capture contextual information in text. Your central inquiry into the effectiveness of varying filter sizes in identifying topic-specific n-grams is highly relevant to understanding the feature extraction process in text-based CNNs.

### 2. Your Tailored Assignment Path: Creative Build
For your **Creative Build**, you'll be focusing on designing, implementing, and evaluating a CNN model for your chosen text classification task. This path encourages you to experiment with architectural choices, particularly filter sizes and embedding strategies, and to critically analyze their impact on the model's ability to learn and differentiate between news categories.

### 3. Your Challenges
*   **🎯 Core Challenge:**
    Implement a word-level CNN for news headline classification. Your dataset should contain headlines labeled with at least three distinct categories (e.g., 'Technology', 'Sports', 'Business').
    1.  **Data Preprocessing:** Prepare your chosen news headline dataset, including tokenization and converting words to numerical representations using pre-trained word embeddings (e.g., Word2Vec or GloVe).
    2.  **CNN Implementation:** Build a CNN model that incorporates multiple filter sizes (e.g., 3, 4, and 5, as discussed in the lecture slides regarding n-gram capture). Each filter size should capture different lengths of n-grams. Ensure you include a max-over-time pooling layer and a fully connected layer for classification.
    3.  **Embedding Strategy:** Experiment with at least two embedding strategies:
        *   **`cnn-static`**: Use pre-trained embeddings (Word2Vec/GloVe) and keep them fixed during training.
        *   **`cnn-nonstatic`**: Initialize with pre-trained embeddings but allow them to be fine-tuned during training.
    4.  **Evaluation and Discussion:** Train your models and evaluate their performance using appropriate metrics (e.g., accuracy, F1-score). Discuss how the different filter sizes contribute to capturing distinct keywords and phrases for each category, and compare the effectiveness of `cnn-static` vs. `cnn-nonstatic` embeddings for this task.

*   **🚀 Stretch Challenge:**
    Deepen your exploration of feature learning and address your "Desired Skill" by implementing a character-level CNN for the same news headline classification task.
    1.  **Character-level CNN:** Design and implement a simple character-level CNN. You can use a subset of your data if training is computationally intensive.
    2.  **Comparative Analysis & Visualization:** Compare its performance and the types of features it learns against your best word-level CNN from the Core Challenge. Can you visualize or qualitatively describe the character-level patterns (e.g., prefixes, suffixes, specific short character sequences) that might be useful for distinguishing categories? Reflect on scenarios where a character-level approach might outperform a word-level one, and vice versa.

### 4. Recommended Resources & Next Steps
To successfully tackle this project, I recommend focusing on the following sections of the lecture material:

*   **Word Embeddings & Input Representation:** Review Slide 43, "Input representation: Concatenated word embeddings," to understand how text is fed into the CNN.
*   **Convolution Operations:** Slides 15-36 provide a detailed breakdown of convolutions, stride, and padding, which are fundamental to understanding filter mechanics.
*   **CNNs for Sentence Classification (Kim 2014):** Slides 43-47 are directly relevant, especially Slide 45 ("Network architecture") which discusses using different filter sizes (e.g., $\eta \in \{3,4,5\}$) and max-over-time pooling.
*   **Pooling Layers:** Slides 37-38 explain the intuition and utility of max pooling, crucial for reducing feature dimensionality while retaining salient information.
*   **Embedding Strategies:** Slides 48-49 detail `cnn-rand`, `cnn-static`, `cnn-nonstatic`, and `cnn-multichannel` options, which will guide your experimentation.
*   **Character-level CNNs:** For the Stretch Challenge, consult Slides 53-55, "Character level CNNs," to understand this alternative approach.
*   **Python with PyTorch/TensorFlow:** Refer to standard deep learning library documentation for implementing CNN layers, embedding layers, and training loops.

### 5. Deliverables & Submission
Please submit the following by the deadline:

1.  **Jupyter Notebook(s):** A well-commented Jupyter Notebook (.ipynb) containing all your code for both the Core and Stretch Challenges. Ensure it is executable and clearly structured.
2.  **Project Report:** A short report (approx. 700-1000 words) that addresses the following:
    *   A brief overview of your chosen dataset and preprocessing steps.
    *   A detailed discussion of your CNN architecture for the Core Challenge, including the filter sizes and embedding strategies used.
    *   Analysis of your results for the Core Challenge, directly answering your "Key Question" by discussing how different filter sizes capture n-grams and contribute to topic distinction. Compare `cnn-static` and `cnn-nonstatic` performance.
    *   For the Stretch Challenge, describe your character-level CNN implementation and provide a comparative analysis of its performance against your word-level CNN. Discuss the pros and cons of each approach for news headline classification.
    *   A reflection on any challenges encountered and insights gained during the project.
3.  **`requirements.txt`:** A file listing all necessary Python packages and their versions to reproduce your environment.

Good luck, Alice! I'm looking forward to seeing your insights.
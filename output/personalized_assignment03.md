### Assignment Title: Personalized Project - Convolutional Neural Networks for Text Classification

Hi Qasim Sefaldeen,

Deadline: 2025-09-13

### 1. Project Overview
Welcome to your personalized assignment on Convolutional Neural Networks! Your learning style, characterized by an **Objective-Practical-Independent** approach, is perfectly suited for a hands-on deep dive into how CNNs are applied to text. This project will allow you to leverage your practical inclination to implement and evaluate models, while also fostering the objective reasoning and reflection that are key to mastering this field. The goal is to build a functional understanding of CNNs for text classification, a strong application of the course material on CNNs for Text Mining.

*(A quick note on the topic: While the overarching course context mentions Transformer Models, this specific assignment is based on the provided lecture materials focusing on Convolutional Neural Networks for Text Mining, which you will find highly relevant and applicable.)*

### 2. Your Tailored Assignment Path: Objective-Practical-Independent
Given your **Objective-Practical-Independent** learning style, this assignment is structured to provide you with a clear, actionable implementation task that you can tackle autonomously. You will focus on applying the theoretical concepts of CNNs to a real-world text classification problem, objectively measuring your model's performance, and then critically reflecting on your architectural choices and experimental results. This path emphasizes direct application ("Applying methods") and analytical reasoning ("Show reasoning and reflection") through empirical evidence.

### 3. Your Challenges
*   **🎯 Core Challenge: Word-Level CNN for Sentiment Classification**
    Implement a Convolutional Neural Network (CNN) for sentiment classification using a standard text dataset (e.g., IMDB movie reviews). Your CNN architecture should incorporate word embeddings as input, a convolutional layer with multiple filter sizes (e.g., `η ∈ {3,4,5}` as discussed in the lecture, each with 100 filters), a max-over-time pooling layer, and a fully connected output layer. Your task is to:
    1.  Preprocess the text data and convert words into suitable input embeddings.
    2.  Construct and train the CNN model.
    3.  Evaluate the model's performance using objective metrics such as accuracy and F1-score on a held-out test set.
    4.  Initialize word embeddings using a pre-trained method (e.g., Word2Vec or GloVe) and keep them fixed during training (`cnn-static` variant from the lecture).

*   **🚀 Stretch Challenge: Exploring Embedding Strategies and Parameter Impact**
    Building upon your core implementation, delve deeper into the impact of different choices on CNN performance and behavior. This optional but highly recommended challenge will push your "Applying methods" and "Show reasoning and reflection" by requiring you to conduct comparative experiments:
    1.  **Embedding Strategy Comparison:** Re-run your sentiment classification task using at least two other embedding strategies discussed in the lecture (e.g., `cnn-rand` where embeddings are randomly initialized and trained, or `cnn-nonstatic` where pre-trained embeddings are fine-tuned during training). Analyze and discuss the performance differences, linking them to the nature of each embedding approach.
    2.  **Parameter Analysis:** Experiment with varying key convolutional parameters, such as different filter sizes or the number of filters per size. For example, how does changing `η` to `{2,3,4}` or increasing/decreasing the number of filters impact your model's accuracy and why? Reflect on how these changes might influence the features the CNN learns.

### 4. Recommended Resources & Next Steps
To successfully complete this assignment, I recommend focusing on the following sections of your lecture materials:

*   **For Core CNN Concepts:**
    *   **Lecture Slides 5-7:** Overview of Convolutional Neural Networks and their typical structure in Computer Vision (the principles extend to text).
    *   **Lecture Slides 15-26:** Detailed explanation of how convolutions work. Pay close attention to the visual examples.
    *   **Lecture Slide 32-34:** Understanding `stride` and `padding` for controlling output dimensions and managing feature map sizes.
    *   **Lecture Slides 37-38:** Explanation of Pooling layers, especially Max Pooling, and their purpose.
*   **For CNNs in NLP/Text Classification:**
    *   **Lecture Slides 43-46:** Illustrates how CNNs are adapted for sentence classification, including input representation, convolution operations over embeddings, and the overall network architecture.
    *   **Lecture Slides 48-49:** Details on various word embedding strategies (`cnn-rand`, `cnn-static`, `cnn-nonstatic`, `cnn-multichannel`) and their implications, crucial for your Core and Stretch challenges.
*   **For Implementation:**
    *   You are encouraged to use Python with a deep learning framework like PyTorch or TensorFlow, as outlined in the `assignment_muster.pdf`. Familiarize yourself with their convolutional layer and pooling layer implementations.
    *   Review the structure of the programming tasks in the `assignment_muster.pdf` for guidance on how to organize your implementation and experiments.

### 5. Deliverables & Submission
Please submit the following components by **2025-09-13**:

1.  **Jupyter Notebook:** A well-commented Jupyter Notebook (`.ipynb` file) containing all your code for data preprocessing, CNN model implementation, training, and evaluation for both the Core and Stretch Challenges. Ensure your code is runnable and clearly demonstrates the different experiments.
2.  **Experiment Results:** Include clear tables and/or plots within your Jupyter Notebook or a separate document summarizing the performance metrics (accuracy, F1-score) for each experiment (different embedding strategies, parameter variations).
3.  **Reflection Document:** A concise PDF or Markdown document (e.g., `reflection.md` or `reflection.pdf`) of approximately 500-750 words. In this document, critically discuss:
    *   Your design choices for the Core Challenge CNN architecture.
    *   The observed performance of your `cnn-static` model.
    *   For the Stretch Challenge, a detailed analysis of the impact of the different embedding strategies and/or parameter variations on your model's performance. Explain *why* you observed these differences, drawing connections to the lecture material and your understanding of CNN operations. This section is vital for demonstrating your "reasoning and reflection."

Good luck, Qasim! I look forward to seeing your practical applications and insightful reflections.
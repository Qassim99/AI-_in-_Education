### Assignment Title: Personalized Project - Convolutional Neural Networks for Text Classification

Hi Alice,

Deadline: 2025-09-13

### 1. Project Overview
It's great to see your proactive approach! Your interest in exploring the practical application of Convolutional Neural Networks (CNNs) for text classification aligns perfectly with our recent discussions in the "Text Mining" lecture. This project is a strong opportunity to delve into how CNNs, traditionally celebrated in computer vision, extract meaningful features from sequential text data. Your objective and practical learning style makes this a fantastic fit for a hands-on implementation and a critical analysis of its performance and underlying mechanisms.

### 2. Your Tailored Assignment Path: Practical – Independent Exploration
Given your **Objective** orientation, **Practical** knowledge preference, and **Independent** engagement style, your assignment will center around building and evaluating a CNN for text classification. This will involve hands-on coding, empirical analysis, and a structured reflection on your findings. You'll be tasked with both implementing core concepts from the lecture and pushing their boundaries through targeted experimentation.

### 3. Your Challenges
*   **🎯 Core Challenge: CNN for Sentiment Classification with Varied Embedding Strategies**
    Implement a CNN-based classifier for a text classification task (e.g., sentiment classification on a dataset like IMDB, as demonstrated in the lecture). Your primary goal here is to understand the impact of word embeddings.
    1.  **Baseline Implementation:** Build a basic CNN model for text classification.
    2.  **Embedding Exploration:** Experiment with at least three different embedding strategies:
        *   Randomly initialized, trainable embeddings (as `cnn-rand` in the lecture).
        *   Pre-trained Word2Vec or GloVe embeddings, kept static/fixed (`cnn-static`).
        *   Pre-trained Word2Vec or GloVe embeddings, fine-tuned/trainable (`cnn-nonstatic`).
    3.  **Performance Analysis:** Compare the classification accuracy and convergence behavior across these embedding setups.
    4.  **Feature Interpretation:** Reflect on how the different embedding strategies might influence the features learned by your CNN, providing insights into their strengths and weaknesses.

*   **🚀 Stretch Challenge: Character-Level CNNs and Architectural Nuances**
    Expand your investigation into more advanced CNN architectures and their properties, aligning with your desire to apply methods and show reasoning.
    1.  **Character-Level CNN:** Implement a simple character-level CNN for the same text classification task. Analyze how its performance compares to your word-level CNNs, considering the strengths of character-level models (e.g., handling OOV words, morphology).
    2.  **Architectural Impact:** Select one key convolution parameter (e.g., filter size, number of filters, or stride) and systematically vary it in your word-level CNN (using your best-performing embedding strategy from the Core Challenge). Discuss how these changes affect:
        *   The extracted features (e.g., which n-grams are captured).
        *   The overall model performance.
        *   The computational cost.
    3.  **Regularization:** Implement and evaluate the effect of L2-maxnorm regularization on one of your CNN models (as discussed on page 50 of the lecture).

### 4. Recommended Resources & Next Steps
To successfully tackle these challenges, focus on the following sections in the `lecture_4.pdf`:

*   **Understanding CNNs in CV:** Pages 5-14 provide the foundational understanding of CNNs.
*   **Convolutions in Detail:** Pages 15-29 are crucial for grasping the mechanics of convolution operations, including stride and padding, which will be essential for your architectural experiments.
*   **Pooling Layers:** Pages 37-38 will help you understand max-over-time pooling for feature aggregation.
*   **CNNs for Sentence Classification (Kim, 2014):** Pages 42-48 are directly relevant to your Core Challenge, especially regarding input representation and embedding variants.
*   **Multi-channel Embeddings & Regularization:** Pages 49-50 offer advanced techniques, particularly useful for your Stretch Challenge.
*   **Character-level CNNs:** Pages 53-54 provide the blueprint for the character-level model in your Stretch Challenge.
*   **Assignment Muster:** Refer to the "Part A: Conceptual Questions" for guidance on the depth of theoretical understanding expected, and "Part B: Applied Exercises" for structural inspiration for your practical implementation.

### 5. Deliverables & Submission
Your submission should be comprehensive and demonstrate both your practical skills and your ability to critically reflect on your work. Please submit the following:

1.  **Jupyter Notebook(s):** A clearly commented Jupyter Notebook (or a set of notebooks) containing all your code for the Core and Stretch Challenges. Ensure reproducibility and include detailed explanations of your implementation choices and experimental setup.
2.  **Project Report (PDF):** A concise report (approx. 500-750 words) structured as follows:
    *   **Introduction:** Briefly state the project's objective and your key questions.
    *   **Core Challenge Findings:** Present your comparative analysis of the different embedding strategies, including relevant metrics (accuracy, loss curves) and a discussion of the observed impact on performance and feature learning.
    *   **Stretch Challenge Findings:** Detail your results from the character-level CNN, your architectural parameter variation, and the impact of regularization.
    *   **Discussion & Reflection:** Critically analyze the trade-offs of the different CNN configurations you explored. Address your key question: "How do different CNN architectural choices (e.g., filter sizes, embedding strategies, pooling mechanisms) influence performance and feature extraction for sentiment classification, and what are their trade-offs?" Reflect on how your findings align with the theoretical concepts presented in the lecture.
    *   **Conclusion:** Summarize your main insights and suggest potential future work.
3.  **Code Repository Link:** A link to a GitHub repository (or similar) containing all your code files, models (if small enough), and your project report. Ensure the repository has a well-structured `README.md` file summarizing your project, findings, and how to run your code.

Good luck, Alice! I'm looking forward to seeing your insights and practical implementations.
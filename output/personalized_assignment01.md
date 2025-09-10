### Assignment Title: Personalized Project - Text Classification with Convolutional Neural Networks

Hi Alice,

Deadline: 2025-09-13

### 1. Project Overview
Your "Objective" and "Practical" orientation, combined with your "Independent" engagement, make you perfectly suited for a hands-on deep learning project. This assignment is designed to let you dive deep into applying Convolutional Neural Networks (CNNs) to text mining tasks, a core concept covered in our lectures. This project will allow you to not only implement these powerful methods but also to critically reflect on their performance and architectural choices, directly addressing our primary goal of showing reasoning and reflection as you apply these techniques.

### 2. Your Tailored Assignment Path: Project-Based Implementation and Analysis
Given your "Objective" and "Practical" learning style, a **Project-Based Implementation and Analysis** assignment mode is a perfect fit. This project will challenge you to apply the concepts of Convolutional Neural Networks (CNNs) directly to a text classification task, allowing you to deepen your understanding through hands-on experience and critical evaluation. You will independently design, implement, and analyze a CNN model, making it a great opportunity to demonstrate your ability to apply methods and reflect on your findings.

### 3. Your Challenges
*   **🎯 Core Challenge: Implementing and Evaluating CNNs for Text Sentiment Classification**
    *   **Task:** Develop a CNN-based classifier for sentiment analysis using a public dataset (e.g., the IMDB sentiment dataset).
    *   **Steps:**
        1.  Preprocess the text data and generate numerical representations. You should initialize your input using either pre-trained Word2Vec or GloVe embeddings (as discussed in the lecture, pages 2, 43, 48).
        2.  Construct a Convolutional Neural Network architecture suitable for text classification, incorporating convolutional layers with various filter sizes, pooling layers (specifically max-over-time pooling as shown on pages 45-47), and a fully connected output layer.
        3.  Experiment with at least two embedding strategies for your CNN:
            *   Using **pre-trained embeddings and keeping them fixed** during training (`cnn-static` variant from page 48).
            *   Using **pre-trained embeddings and allowing them to be fine-tuned/trainable** during training (`cnn-nonstatic` variant from page 48).
        4.  Train and evaluate your models on the chosen dataset, reporting standard classification metrics (e.g., accuracy, precision, recall, F1-score).

*   **🚀 Stretch Challenge: Parameter Sensitivity and Character-Level Analysis**
    *   **Task 1 (Parameter Sensitivity):** Extend your core challenge by conducting a systematic study on the impact of key CNN parameters. Vary filter sizes (e.g., 2, 3, 5 words, as mentioned in the `assignment_muster.pdf` and illustrated in the lecture on pages 45-47) and stride values (e.g., 1 and 2, as discussed on pages 29-32). Analyze and discuss how these changes affect the extracted n-gram features and the final classification results. Visualize and provide reasoning for observed trends.
    *   **Task 2 (Character-Level Exploration):** Implement a *simple* character-level CNN for the same text classification task (as introduced in the lecture, pages 53-54). Compare its performance and computational efficiency against your best-performing word-level CNN from the Core Challenge. Discuss the trade-offs and potential advantages/disadvantages of character-level versus word-level approaches for text classification, explicitly linking to concepts like handling out-of-vocabulary words and capturing sub-word information. This task directly addresses the "Show reasoning and reflection" goal, pushing you to analyze different representational paradigms.

### 4. Recommended Resources & Next Steps
To successfully complete your project, focus on the following sections of the provided materials:

*   **`lecture_4.pdf` (Text Mining):**
    *   **Word Embeddings (Pages 2, 43, 48):** Understand how to represent text input and the different embedding strategies (`cnn-rand`, `cnn-static`, `cnn-nonstatic`, `cnn-multichannel`).
    *   **Convolutional Neural Networks (Pages 5-7, 15-28):** Grasp the foundational concepts of convolutions, filters, and feature maps, initially from a computer vision perspective.
    *   **Convolutions for Text (Pages 43-44):** Specifically shows how convolutions are applied to word embeddings in text, which is crucial for your core task.
    *   **Network Architecture (Pages 45-47):** Provides a specific CNN architecture for sentence classification, including max-over-time pooling, which you can use as a starting point.
    *   **Stride and Padding (Pages 29-34):** Essential for understanding how convolutional operations affect output dimensions, especially for the stretch challenge on parameter sensitivity.
    *   **Character-level CNNs (Pages 53-54):** Key information for implementing the character-level model in the stretch challenge.
    *   **Regularization (Page 50):** Consider incorporating dropout and L2-maxnorm constraints to improve model generalization.
    *   **Evaluation (Pages 51-52, 56):** Provides context on how to evaluate models and interpret performance.

*   **`assignment_muster.pdf`:**
    *   **Part A, Q1, Q3, Q4, Q5:** These conceptual questions directly relate to the embedding strategies, stride, padding, and max pooling, which are fundamental to your implementation and analysis.
    *   **Part B, Q1, Q2, Q3:** This section provides an excellent blueprint for structuring your practical implementation, covering word-level CNNs, parameter variation, and character-level CNNs.
    *   **Part C:** The "Critical Reflection" prompts will be very useful for guiding your discussion and reasoning in your project report, helping you meet the "Show reasoning and reflection" goal.

### 5. Deliverables & Submission
Please submit your work by the deadline, packaged as follows:

1.  **Code Repository (GitHub Link):** A link to a well-organized GitHub repository containing:
    *   Your Python code (e.g., Jupyter Notebooks or `.py` files) for all implemented CNN models (word-level for Core Challenge, and if attempted, character-level and parameter sensitivity experiments for Stretch Challenge). Your code should be well-commented and clearly demonstrate each step of your process.
    *   A `requirements.txt` file listing all necessary Python libraries.
2.  **Project Report (PDF):** A concise, academic-style report (approximately 5-7 pages, excluding code printouts and appendices) with the following sections:
    *   **Introduction:** Briefly outline the sentiment classification problem and your chosen approach using CNNs.
    *   **Methodology:** Detail your CNN architectures, embedding strategies, dataset, preprocessing steps, and training configuration.
    *   **Results & Analysis (Core Challenge):** Present the evaluation metrics for your word-level CNNs (fixed vs. trainable embeddings). Discuss your findings, compare the performance of the two embedding strategies, and provide clear reasoning for any observed differences.
    *   **Results & Analysis (Stretch Challenge - if attempted):**
        *   **Parameter Sensitivity:** Analyze how varying filter sizes and stride values impacted your model's performance and feature extraction. Include relevant visualizations (e.g., t-SNE of feature maps if possible) and a discussion of the insights gained.
        *   **Character-Level CNN:** Present its performance and a detailed comparison with your best word-level CNN, including computational considerations and a critical discussion of their respective strengths and weaknesses for text classification.
    *   **Conclusion & Reflection:** Summarize your key learnings and reflect on the broader implications of your findings for text classification with CNNs. This section is crucial for demonstrating your "reasoning and reflection."

We look forward to seeing your innovative work!
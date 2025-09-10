### Assignment Title: Personalized Project - Exploring CNN Architectures for Text Classification

Hi Alice,

That's an excellent project idea! It's a great way to explore **Convolutional Neural Networks for Text Mining**, a core topic we've covered in the recent lectures. Your proposed focus on implementing and evaluating different CNN architectures for text classification tasks, particularly how architectural choices and embedding strategies impact performance and interpretability, is a strong application of the course material. It directly addresses your key question: "How do different convolutional neural network architectures and embedding strategies influence the performance and interpretability of text classification models, particularly for sentiment analysis?"

### 1. Project Overview & Your Goal
Alice, your objective-oriented and practical learning style makes this project a perfect fit for applying the concepts of CNNs to a real-world NLP challenge. Your goal will be to practically implement and thoroughly analyze various CNN configurations for text classification, demonstrating your understanding of their mechanics and their impact on model behavior and performance. This will allow you to reflect deeply on the design choices involved in building effective text mining solutions.

### 2. Your Tailored Assignment Path: Applied Project
For your **Applied Project**, you'll be focusing on building and experimenting with Convolutional Neural Networks for text classification. This will involve hands-on implementation, systematic evaluation, and a critical reflection on your findings, aligning perfectly with your independent engagement and the teacher's focus on "applying methods" and "showing reasoning and reflection."

### 3. Your Challenges
*   **🎯 Core Challenge: Comparative Analysis of Word-Level CNN Architectures**
    Implement a word-level Convolutional Neural Network for sentiment classification on a suitable dataset (e.g., IMDB sentiment dataset, as suggested in the `assignment_muster.pdf`). Design and conduct experiments to compare at least three distinct CNN configurations. This comparison should include:
    1.  **Embedding Strategies:** Evaluate the impact of (a) randomly initialized, trainable embeddings (cnn-rand/cnn-nonstatic) versus (b) pre-trained, fixed embeddings (cnn-static) (e.g., Word2Vec or GloVe, as discussed in Slide 48 of `lecture_4.pdf`).
    2.  **Filter Sizes & Counts:** Experiment with different filter sizes (e.g., 2, 3, 5, as suggested in Slide 45) and the number of filters per size.
    Analyze how these choices affect the model's accuracy, F1-score, and training efficiency. Your report should present these results clearly and discuss the reasoning behind observed performance differences, directly addressing your key question.

*   **🚀 Stretch Challenge: Exploring Character-Level CNNs and Feature Interpretation**
    Extend your core project by either:
    1.  Implementing a character-level CNN (as discussed in Slides 53-54 of `lecture_4.pdf`) for text classification on the same dataset. Compare its performance, advantages, and disadvantages against your best-performing word-level CNN. Reflect on scenarios where character-level approaches might be preferable.
    *OR*
    2.  Develop a method to visualize or interpret the features learned by your best-performing word-level CNN. For instance, identify which n-grams or sequences of words strongly activate specific filters. Discuss what insights this provides into how the CNN processes text and contributes to its classification decision, thereby enhancing your "reasoning and reflection."

### 4. Recommended Resources & Next Steps
To successfully tackle these challenges, focus on the following sections from the provided `lecture_4.pdf`:

*   **For CNN Basics and Architecture:**
    *   Slides 5-7: "Convolutional neural networks" and "CNNs in Computer Vision" for understanding the typical structure.
    *   Slides 15-27: "Convolutions" for the fundamental operation, including how filters slide over input.
    *   Slides 29-34: "Convolutions" for understanding stride and padding, which are crucial for feature map dimensions.
    *   Slides 37-38: "Pooling" and "Pooling layers" for the role of max-over-time pooling in feature extraction.
*   **For CNNs in NLP and Text-Specific Aspects:**
    *   Slides 41-42: "CNNs in NLP" and "CNNs for Sentence Classification" for the context of applying CNNs to text.
    *   Slides 43-46: "CNNs for Sentence Classification" (Input representation, Convolution operation, Network architecture) for how words are represented and convolutions are applied to text.
    *   Slides 48-49: "CNNs for Sentence Classification: Embeddings" and "Multi-channel word embeddings" for different embedding strategies, which are central to your Core Challenge.
    *   Slides 53-54: "Character level CNNs" for the Stretch Challenge option.
*   **For Implementation & Evaluation:**
    *   Refer to Part B and Part C of the `assignment_muster.pdf` for guidance on structuring your applied exercises and critical reflection.

### 5. Deliverables & Submission
Please submit the following components by the deadline:

1.  **Code Repository:** A link to a well-organized GitHub repository containing your Python code (using PyTorch or TensorFlow) for all implemented CNN models. Ensure your code is thoroughly commented and runnable, with clear instructions in a `README.md` file.
2.  **Experimental Results:** A clear presentation (e.g., tables, graphs) of the performance metrics (accuracy, F1-score) for all tested CNN configurations. This should include results for different embedding strategies and filter size variations for the Core Challenge.
3.  **Reflective Report (approx. 800-1000 words):** A detailed document (e.g., PDF or Markdown) that:
    *   Explains your experimental design and methodology.
    *   Analyzes and discusses the results from your Core Challenge, directly addressing your key question about the influence of architecture and embeddings on performance and interpretability.
    *   If you undertake the Stretch Challenge, include your implementation details, comparative analysis with word-level CNNs, and/or insights gained from feature interpretation.
    *   Conclude with a critical reflection on the strengths and limitations of CNNs for text classification based on your findings, potentially suggesting future research directions or improvements.
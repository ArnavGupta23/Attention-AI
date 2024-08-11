# Project 6: Attention - BERT Masked Word Prediction

## Overview

This project implements a BERT-based model to predict masked words in a text sequence. The model uses attention mechanisms across multiple layers and heads to understand the relationships between different words in the input sentence. The attention scores are visualized to provide insight into what BERT’s attention heads might be focusing on.

## Analysis of Attention Heads

### 1. Layer 1, Head 11: Adjective-Noun Relationship

**Example Sentences:**
- "He was a great [MASK] player."
- "The dog found a large [MASK] bone."

**Analysis:**
Layer 1, Head 11 appears to focus on the relationship between adjectives and the nouns they modify. In the sentence "He was a great [MASK] player," the attention diagram shows that this head pays significant attention to the words "great" and "player," which are directly related to the masked word. This indicates that this attention head is likely identifying and weighing the importance of descriptive words in relation to the nouns they qualify. This pattern is crucial for predicting words that describe specific qualities, such as "football" in the context of a "great player."

### 2. Layer 5, Head 3: Pronoun-Antecedent Tracking

**Example Sentences:**
- "John gave Mary the book, and [MASK] thanked him."
- "The teacher called on the student, and [MASK] answered the question."

**Analysis:**
Layer 5, Head 3 seems to focus on tracking pronouns and their antecedents within a sentence. For instance, in the sentence "John gave Mary the book, and [MASK] thanked him," this head shows strong attention linking the pronoun `[MASK]` to "Mary." This suggests that the head is particularly useful for resolving pronouns by associating them with their correct antecedents in the sentence, which is essential for understanding and predicting references in a text.

## Conclusion

This project highlights the intricate ways in which BERT’s attention heads contribute to understanding natural language. By visualizing the attention scores, we can gain insights into how different attention heads specialize in certain linguistic relationships, such as adjective-noun associations and pronoun-antecedent tracking. This understanding can inform further exploration and fine-tuning of language models for various NLP tasks.

# Embeddings
The notebook provided in this repo includes explanations and instructions that cover different types of embeddings.

# Categories of Embeddings Based on Their Generation Approach

## **Introduction**
Embeddings are essential in machine learning for representing data in dense, continuous vector spaces. Based on how they are generated, embeddings fall into three categories:
- **Static Embeddings**: Predefined, context-independent representations.
- **Contextual Embeddings**: Dynamic, context-sensitive representations.
- **Custom Embeddings**: Tailored for specific tasks or domains.

---

## **1. Static Embeddings**

### **1.1 What Are Static Embeddings?**
Static embeddings represent words or tokens with fixed vectors, regardless of their context in a sentence. These embeddings capture general semantic relationships but cannot adapt to polysemy (e.g., “bank” as a financial institution vs. a riverbank).

### **1.2 Characteristics**
- Fixed, context-independent representations.
- Pretrained on large corpora.
- Efficient and simple to use.

### **1.3 Popular Models and Tools**
- **Word2Vec**: Predicts context words or a word given its context using CBOW or Skip-Gram.
- **GloVe**: Learns word embeddings from a co-occurrence matrix.
- **FastText**: Extends Word2Vec with character-level n-grams to handle rare words or misspellings.

### **1.4 Use Cases**
- Text clustering or classification tasks.
- Semantic similarity analysis.

### **1.5 Practical Tip**
Use pretrained models like Word2Vec, GloVe, or FastText for efficiency and simplicity in general NLP tasks.

---

## **2. Contextual Embeddings**

### **2.1 What Are Contextual Embeddings?**
Contextual embeddings generate representations dynamically, adapting to the word’s meaning based on its surrounding words. These embeddings excel at handling polysemy and deep contextual understanding.

### **2.2 Characteristics**
- Context-sensitive and dynamic.
- Generated using transformer-based architectures.
- Often pretrained on large-scale corpora and fine-tuned for specific tasks.

### **2.3 Popular Models and Tools**
- **BERT (Bidirectional Encoder Representations from Transformers)**: Generates contextual embeddings by considering the bidirectional context of words.
- **GPT (Generative Pretrained Transformer)**: Produces dynamic embeddings using autoregressive transformers.
- **Sentence-BERT**: Optimized for sentence-level embeddings and tasks like semantic similarity.

### **2.4 Use Cases**
- Machine translation.
- Question answering and text summarization.
- Named entity recognition (NER).

### **2.5 Practical Tip**
Leverage pretrained transformer models like BERT or Sentence-BERT to generate contextual embeddings, and fine-tune them for domain-specific applications when needed.

---

## **3. Custom Embeddings**

### **3.1 What Are Custom Embeddings?**
Custom embeddings are task-specific or domain-specific embeddings tailored for a particular application. They can be built from scratch or fine-tuned using pretrained models.

### **3.2 Characteristics**
- Optimized for specific tasks or datasets.
- Can be either static or contextual, depending on implementation.
- Often incorporate domain knowledge.

### **3.3 Tools and Techniques**
- **Trainable Embedding Layers**:
  - `keras.layers.Embedding`: Create embeddings in TensorFlow/Keras models.
  - PyTorch’s `nn.Embedding`: Train embeddings for categorical or sequential data.
- **Fine-Tuned Transformers**:
  - Pretrained transformers like BERT can be fine-tuned for domain-specific tasks.
  - Example: Fine-tuning BERT on medical corpora to create BioBERT.
- **Recurrent Neural Networks (RNNs)**:
  - LSTMs or GRUs can be used to learn embeddings from scratch for small or specialized datasets.

### **3.4 Use Cases**
- Recommendation systems (e.g., embeddings for users and items).
- Domain-specific NLP tasks (e.g., legal or medical text analysis).
- Personalized systems (e.g., user or customer-specific embeddings).

### **3.5 Practical Tip**
Use tools like `keras.layers.Embedding` or PyTorch’s `nn.Embedding` for categorical data. For text-based custom embeddings, fine-tune pretrained transformers for better task performance. Use LSTMs when working with smaller or highly specific datasets.

---

## **4. Comparison of Embedding Categories**

| Feature               | Static Embeddings          | Contextual Embeddings      | Custom Embeddings          |
|-----------------------|---------------------------|---------------------------|----------------------------|
| **Context Sensitivity** | No                        | Yes                        | Task-specific (can be either) |
| **Pretraining**        | General corpus            | General corpus            | Domain/task-specific       |
| **Adaptability**       | Fixed                     | Dynamic                    | Adapted to specific tasks  |
| **Examples**           | Word2Vec, GloVe, FastText | BERT, GPT, Sentence-BERT   | Fine-tuned BERT, custom RNNs |

---

## **5. When to Use Each Category**

### **5.1 Static Embeddings**
- Use when:
  - Context is irrelevant or general-purpose embeddings suffice.
  - Efficiency and simplicity are priorities.
- Example: Quick semantic analysis or clustering.

### **5.2 Contextual Embeddings**
- Use when:
  - Deep contextual understanding is needed.
  - Handling polysemy or nuanced tasks.
- Example: Machine translation, summarization, or dialogue systems.

### **5.3 Custom Embeddings**
- Use when:
  - Task or domain-specific optimization is crucial.
  - Pretrained embeddings lack domain relevance.
- Example: Legal document analysis, personalized recommendation systems.

---

By understanding and leveraging these categories effectively, you can tailor embedding solutions to your data and task requirements.


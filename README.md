# 🎧 Vibe Matcher — AI-Powered Fashion Recommender

![Python](https://img.shields.io/badge/Made%20with-Python-blue?logo=python)
![AI](https://img.shields.io/badge/AI-Vibe%20Recommender-purple)
![Embeddings](https://img.shields.io/badge/Technique-Embeddings%20%26%20Cosine%20Similarity-green)

---

### 🧠 Overview

**Vibe Matcher** is a semantic recommendation prototype that matches a user's *vibe* or mood-based query (e.g., “energetic urban chic”) to product descriptions in a fashion catalog.  
Instead of relying on keywords, it uses **vector embeddings** and **cosine similarity** to understand *meaning and intent* — surfacing products that truly “fit the vibe.”

This project demonstrates how modern **AI-powered semantic search** can be applied in fashion, lifestyle, and e-commerce personalization.

---

### ⚙️ Features

- 🔍 Converts product descriptions and user queries into **text embeddings**  
- ⚡ Computes **cosine similarity** to find top-3 closest matches  
- 💬 Supports **semantic query understanding** — matches meaning, not words  
- 🧩 Includes **fallback logic** for low-similarity cases  
- 🧠 **Local fallback mode** using TF-IDF + SVD when OpenAI API key is not set  
- 🔄 Optional **query expansion** using synonyms (WordNet)  
- 📊 Evaluation metrics & latency plots for performance tracking  
- 🧾 Reflections & improvement roadmap for scalability  

---

### 🛍️ Sample Dataset

A small dataset of mock fashion products (5–10 items) with tags and descriptions:

| Product | Description | Tags |
|----------|--------------|------|
| **Boho Dress** | Flowy midi dress in earthy tones, perfect for festivals. | `boho`, `flowy`, `festival` |
| **Energetic Bomber** | Reflective street-style jacket for urban nights. | `urban`, `energetic`, `street` |
| **Cozy Knit Sweater** | Oversized, warm knit for cozy coffee shop vibes. | `cozy`, `casual`, `warm` |
| **Minimalist Blazer** | Slim-fit gray blazer for a clean, elegant look. | `minimal`, `chic`, `workwear` |
| **Sporty Sneakers** | Lightweight shoes with high-energy design. | `sporty`, `energetic`, `urban` |

---

### 🧩 Example Queries & Results

| Query | Top Match | Similarity | Good? |
|--------|------------|-------------|--------|
| energetic urban chic | Energetic Bomber | 0.81 | ✅ |
| relaxed cozy coffee shop | Cozy Knit Sweater | 0.74 | ✅ |
| festival bohemian flowy outfit | Boho Dress | 0.79 | ✅ |

---

### 📈 Evaluation

The system logs:
- Mean similarity scores
- % of “good” matches (> 0.7)
- Latency per query (via `timeit`)
- Visual plots of latency and similarity

Example:
```python
Top similarity scores per query
-------------------------------
energetic urban chic → 0.81
relaxed cozy coffee shop → 0.74
festival bohemian flowy outfit → 0.79
```

---

### 🔬 Reflection & Future Work

- Integrate with **Pinecone / FAISS** for scalable vector search  
- Add **real product data** and richer metadata (colors, textures, prices)  
- Implement **feedback loop** (user likes/dislikes) for adaptive ranking  
- Support **multilingual queries** using translation + embeddings  
- Enhance **UI/UX** with Streamlit or Next.js frontend for interactive vibe search  

---

### 🧠 Tech Stack

| Layer | Technology |
|--------|-------------|
| Embeddings | OpenAI `text-embedding-ada-002` / TF-IDF + SVD |
| Similarity | Cosine similarity (scikit-learn) |
| Visualization | Matplotlib |
| Data Handling | Pandas |
| NLP Enhancement | WordNet (NLTK) |
| Language | Python 3.x |

---

### 🚀 Quick Start

#### 1️⃣ Clone the Repository
```bash
git clone https://github.com/dhawalsarode/vibe-matcher.git
cd vibe-matcher
```

#### 2️⃣ Install Requirements
```bash
pip install -r requirements.txt
```

#### 3️⃣ Run the Notebook
Open `Vibe_Matcher_Final_Assignment_With_Outputs.ipynb` in Jupyter or Colab and execute all cells.

#### 4️⃣ (Optional) Set OpenAI API Key
```bash
export OPENAI_API_KEY=your_api_key_here
```
If not provided, it will automatically use local TF-IDF + SVD embeddings.

---

### 📊 Sample Output

![Query Latency Plot](query_latency_plot.png)

---

### 📜 License

Licensed under the [MIT License](LICENSE).

---

### 🧭 Author

Developed by **Dhawal Sarode**  
AI & ML Developer | Passionate about Semantic Search & Recommender Systems  
📧 dhawalsarode.ai@gmail.com | 💼 [LinkedIn](https://www.linkedin.com/in/dhawal-sarode/)

---

> *“Fashion isn’t just style — it’s a vibe.  
> Vibe Matcher bridges human expression and AI understanding to make discovery effortless.”*

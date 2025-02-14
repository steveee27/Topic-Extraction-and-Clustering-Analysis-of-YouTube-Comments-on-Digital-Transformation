# Topic Extraction and Clustering Analysis of Youtubes Comments on Digital Transformation

**Description:**  
This project performs scraping of YouTube comments to analyze public opinion about digital transformation in Indonesia. It employs topic modeling and clustering techniques to group comments into meaningful topics. Additionally, persona analysis is conducted to categorize comments based on distinct opinions.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Data Collection](#data-collection)
3. [Preprocessing](#preprocessing)
4. [Model Architecture](#model-architecture)
5. [Results](#results)
6. [Insights and Persona Analysis](#insights-and-persona-analysis)
7. [Conclusion](#conclusion)
8. [License](#license)

## Project Overview

This project scrapes YouTube comments from multiple videos related to digital transformation in Indonesia. It uses **unsupervised learning** techniques, particularly **topic extraction** and **clustering**, to uncover patterns in the comments. The project scrapes comments from YouTube, preprocesses the text, and applies **KMeans clustering** to group the comments. Additionally, **LDA (Latent Dirichlet Allocation)** is used for **topic modeling** to identify key themes in the comments.

## Data Collection

The data used in this project was obtained through scraping YouTube comments using the YouTube API. The following videos were used to gather comments:

1. [Motion Grafis Teknologi di Era Digital Berkembang Pesat](https://www.youtube.com/watch?v=fiuhu924--M)
2. [INDONESIA MAKIN DIGITAL](https://www.youtube.com/watch?v=UMKY_0kiwYk)
3. [Proses Percepatan Transformasi Digital di Indonesia | OOTD (08/12/20) Part 4](https://www.youtube.com/watch?v=taglTEfRt5Y)
4. [Salah Kaprah Transformasi Digital | Dharma S, Presiden Direktur Microsoft Indonesia](https://www.youtube.com/watch?v=fneZo5_pox4)
5. [Perusahaan-perusahaan di Industri ini, Wajib Transformasi Digital Sekarang Juga! - ANALISIS #2](https://www.youtube.com/watch?v=6lY4HBRgTYQ)
6. [Keterangan Pers Menkomdigi Terkait Transformasi Digital dan E-Government, Jakarta, 13 Januari 2025](https://www.youtube.com/watch?v=1BmayjFMKGc)
7. [MENOLAK PUNAH! Transformasi PT Pos Indonesia menjadi Perusahaan Digital bersama CEO Pos Indonesia](https://www.youtube.com/watch?v=kpI5ES8VEX8)
8. [Transformasi Digital Pos Indonesia](https://www.youtube.com/watch?v=gGu1XmqhI9o)
9. [Langkah Besar Transformasi Digital Indonesia](https://www.youtube.com/watch?v=8Kb3xfYXkZE)
10. [Transformasi Digital PT POS Indonesia](https://www.youtube.com/watch?v=Qntde_12uIM)

A total of 429 comments were collected across these videos.

## Preprocessing

The collected comments were preprocessed using the following steps:
1. **Text Cleaning**: Removal of URLs, emojis, special characters, and extra spaces.
2. **Stopword Removal**: Removal of common words that do not add meaningful information.
3. **Lemmatization**: Converting words to their base form using a lemmatizer.

After preprocessing, the cleaned comments were tokenized for use in text representations.

## Model Architecture

The following techniques were employed to analyze the comments:

### 1. **Text Representation**
   - **TF-IDF**: Used to vectorize the comments and represent the importance of words across all documents.
   - **Word2Vec**: A word embedding technique used to map words into high-dimensional vectors.

### 2. **Clustering**
   - **KMeans Clustering** was applied with **k = 2** for grouping comments into two clusters based on content similarity.
   - **Silhouette Score** and the **Elbow Method** were used to evaluate the optimal number of clusters.

### 3. **Topic Modeling**
   - **Latent Dirichlet Allocation (LDA)** was applied to discover **2 topics** based on the text data.

## Results

### Clustering Results:
The **KMeans clustering** produced the following clusters:

- **Cluster 0**: Focused on topics related to **Indonesia's progress** and **digital transformation**, reflecting **optimism** and **support** for the nation’s development.
- **Cluster 1**: Focused on **simple requests for permission** to use video content and **appreciation** for the videos shared.

### Topic Extraction with LDA revealed the following:

- **Topic 0**: Focused on **discussions about digital transformation** and **governmental impacts**, expressing **support** for the progress and optimism for the future of Indonesia.  

- **Topic 1**: Focused on **requests for permission to use video content** and **appreciation** for the content provided.

## Insights and Persona Analysis

### **Cluster 0 - Kemajuan dan Perhatian terhadap Indonesia**  
- Cluster 0 contains comments that focus on **Indonesia's progress**, particularly in the context of **digital transformation**. Users express their support for **President Jokowi** and **technological advancement** in Indonesia.  
  - **Persona Insight**: This cluster represents users who are **optimistic** and **supportive** of the government's role in advancing the nation’s digital infrastructure.

### **Cluster 1 - Permohonan Izin dan Apresiasi**  
- Cluster 1 primarily contains comments that are **short and polite**, focused on **requesting permission to use content** or expressing **appreciation** for the videos.  
  - **Persona Insight**: This cluster consists of users who are **respectful**, **appreciative**, and **practical** in their interactions, often utilizing content for academic or professional purposes.

### **Topic 0 - Dukungan dan Harapan untuk Kemajuan Bangsa**  
- Topic 0 contains comments filled with **national pride**, focusing on **hope for the future** and the **nation's development**. Key terms like "maju", "jokowi", "semangat", and "sehat" show **support** for the **government** and the **nation’s progress**.  
  - **Persona Insight**: Users in this topic express **optimism** and support for **digital transformation** and the **nation’s growth**.

### **Topic 1 - Permintaan Izin dan Apresiasi terhadap Konten**  
- Topic 1 is dominated by comments that **request permission** for using videos and express **gratitude**. Key terms include "video", "izin", "kak", and "tugas", showing **formal, respectful requests**.  
  - **Persona Insight**: This group represents **polite and appreciative** individuals who approach the content in a **formal and practical manner**, mainly for academic or professional purposes.

## Conclusion

This project successfully grouped YouTube comments into two clusters using **KMeans clustering** and extracted meaningful topics with **LDA**. The results provide valuable insights into public sentiment regarding **digital transformation** in Indonesia. The two clusters highlight **support for the nation’s progress** and **respectful, practical engagement with content**. The topic modeling uncovered themes related to **digital transformation** and **government policies**.

### Future Work:
- **Data Expansion**: Scraping more YouTube videos and comments can help improve the robustness of the model.
- **Fine-tuning**: Experimenting with different clustering techniques and models for improved accuracy.
- **Advanced Topic Modeling**: Exploring more sophisticated topic modeling techniques such as **BERT-based models** for better contextual understanding.

## License

This repository is licensed under the MIT License. You are free to use, modify, and distribute this project with proper attribution. For more details, refer to the [LICENSE](LICENSE) file.

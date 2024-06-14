---
title: Séance du 14 Mai 2024
date: 2024-05-14
slug: 2024-05-14
---

## Horaire et Lieu
Mardi de 18h à 20h à la MPT de Landerneau.

## Au programme
- Comment ça marche: Large Language Model (LLM): tokenizer.
  - Avec des exemples.
- BrachioGraph
  - intégration 

## Travaux Pratiques
### Exercice numéro #1
```sh
# Nous nous déplaçons dans le répertoire de travail
cd travail
# Nous créons un répertoire "llm"
mkdir llm
# Nous nous déplaçons dans ce dernier
cd llm
# Nous créons un environnement virtuel
python3 -m venv .venv
# Nous activons l'environnement virtuel
source .venv/bin/activate
# Procédons à l'installation de la bibliothèque Tiktoken
# Code source de la bibliothèque : https://github.com/openai/tiktoken
# transformer des mots en nombres pour un traitement numérique de données
pip install tiktoken
# A présent créons le fichier pour y mettre du code
touch test_tiktoken.py
# Editons ce dernier
nano test_tiktoken.py
```
#### Exercice numéro #1 - Code Source 
```py
import tiktoken
# Nous importons la bibliothèque tiktoken.

encoding_gpt2 = tiktoken.encoding_for_model("gpt-2")
# Au premier démmarage: télécharge le vocabulaire GPT-2.

print(encoding_gpt2.encode("The quick brown fox jumps over the lazy dog."))
# résultat: [464, 2068, 7586, 21831, 18045, 625, 262, 16931, 3290, 13]

print(encoding_gpt2.decode([464, 2068, 7586, 21831, 18045, 625, 262, 16931, 3290, 13]))
# résultat: The quick brown fox jumps over the lazy dog.
```
### Exercice numéro #2
```sh
# Installons la bibliothèque NumPy
pip install numpy
# Créons le fichier contenant le code Python
touch cosine_similarity_part1.py
# Editons le fichier
nano cosine_similarity_part1.py
```
#### Exercice numéro #2 - Code Source
```py
import numpy as np

# Define the vectors
Vx = np.array([0, 1, 0, 1, 0, 1, 1, 0])
Vy = np.array([0, 0, 0, 1, 1, 1, 1, 0])

# Function to calculate cosine similarity
def cosine_similarity(vector1, vector2):
  # Calculate the dot product
  dot_product = np.dot(vector1, vector2)
  # Calculate the norms of each vector
  norm1 = np.linalg.norm(vector1)
  norm2 = np.linalg.norm(vector2)
  # Calculate the cosine similarity
  cosine_sim = dot_product / (norm1 * norm2)
  return cosine_sim
  
  # Calculate and print the cosine similarity
  similarity = cosine_similarity(Vx, Vy)

print(f"Cosine similarity (Vx,Vy): {similarity}")
```

### Exercice numéro #3
```sh
# Installons la bibliothèque scikit-learn
pip install scikit-learn
# Création du fichier contenant le code source
touch cosine_similarity_part2.py
# Ouverture du fichier pour l'ajout du code
nano cosine_similarity_part2.py
```
#### Exercice numéro #3 - Code Source
```py
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.metrics.pairwise import cosine_similarity^

sentences = [
    "I am fond of reading thriller novels.",  # x
    "I prefer reading thriller novels.",      # y
    "Yesterday, I arrived late."              # z
]

# Initialize a TF-IDF Vectorizer
vectorizer = TfidfVectorizer()

# Fit and transform the sentences to a TF-IDF matrix
tfidf_matrix = vectorizer.fit_transform(sentences)

# Compute the cosine similarity matrix
cosine_sim = cosine_similarity(tfidf_matrix, tfidf_matrix)

print("Cosine Similarity Matrix:\n", cosine_sim)
```

## Références
- [Wikipedia - Large Langage Model](https://fr.wikipedia.org/wiki/Grand_mod%C3%A8le_de_langage).
- [Github - Tiktoken](https://github.com/openai/tiktoken).
- [HuggingFace - Site](https://huggingface.co/).
- [LinuxFr - Intro aux LLMs](https://linuxfr.org/users/aboulle/journaux/introduction-pratique-aux-grands-modeles-de-langage-llm).
- [GPT Tokenizer - Site](https://gpt-tokenizer.dev/).
- [HuggingFace - The Tokenizer Playground](https://huggingface.co/spaces/Xenova/the-tokenizer-playground).
- [Algebrica - Cosine Similarity](https://algebrica.org/cosine-similarity/).
- [Schoolmouv - Site](https://www.schoolmouv.fr/).
- [Github - Whisper.cpp](https://github.com/ggerganov/whisper.cpp/discussions/166) | Real-time transcription on Raspberry Pi 4.
- [Miguel Gringberg - Blog](https://blog.miguelgrinberg.com/post/how-llms-work-explained-without-math) | How LLMs work explained without math.
- [Scikit Learn - Site](https://scikit-learn.org/stable/).
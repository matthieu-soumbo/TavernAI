# 🛡️ TavernAI – IA Fantasy Conversationnelle & Narrative

> TavernAI est un projet personnel mêlant IA générative, cloud AWS, modélisation de données et narration fantasy.  
> Il a pour objectif de démontrer mes compétences de Product Owner Data / IA / Cloud à travers une interface immersive d’agent IA narratif.

---

## ✨ Pitch rapide

- 💬 Dialogue libre avec des PNJ médiéval-fantastiques riches en personnalité, mémoire, objectifs et émotions
- 🧠 Données JSON ultra enrichies (PNJ, lieux, quêtes, bestiaire, matching)
- ☁️ Infrastructure Cloud (AWS S3, IA Bedrock / OpenAI, Polly, Lambda)
- 🎮 UI simple type Streamlit ou webapp
- 📚 Projet 100% conçu, piloté et documenté comme un vrai produit tech

---

## 🎯 Objectifs du projet

- Créer un agent IA conversationnel vivant dans un univers fantasy structuré
- Structurer les données narratives sous forme de fichiers JSON exploitables
- Déployer une infrastructure IA / Cloud simple et réplicable
- Valoriser l’ensemble via une approche agile & produit documentée

---

## 🔍 Fonctionnalités

### ✅ MVP (version 1)

- Sélection d’un PNJ (avatar + fiche détaillée)
- Dialogue intelligent généré via IA (GPT / Bedrock)
- Personnalité IA cohérente (objectifs, valeurs, souvenirs, émotions…)
- Données chargées depuis fichiers JSON enrichis
- Interface utilisateur (Streamlit) simple et fonctionnelle

### 🛠️ V2 (en cours)

- Synthèse vocale via AWS Polly
- Moteur de quête dynamique avec matching PNJ ↔ lieu ↔ quête
- Personnalisation du joueur (`joueur.json`)
- Uploader les fichiers sur AWS S3

### 🔮 V3 (prévu)

- Moteur RAG narratif via LangChain ou Bedrock
- Carte interactive des lieux
- Animation vocale / faciale des PNJ
- Historique de mémoire persistante et lore étendu

---

## 📂 Données utilisées (100% générées et documentées)

| Fichier | Contenu |
|--------|---------|
| `pnj_enriched_ai_ready.json` | 100 PNJ avec objectifs, valeurs, souvenirs, peurs, secrets, phrases, avatar… |
| `lieux_enriched_with_tags_and_ambiance.json` | 100 lieux fantasy avec ambiance, climat, factions, danger, tags |
| `quetes_enriched_with_tags.json` | 250 quêtes longues avec difficulté, durée, archétype, lien lieu/PNJ |
| `bestiaire_enriched_with_tags.json` | 500 créatures fantasy avec caractéristiques, faiblesses, biomes |
| `matchmaking_rules_enriched.json` | Pondération IA pour matching PNJ ↔ lieu ↔ quête |
| `joueur.json` | (optionnel) Fiche de joueur personnalisable pour immersion |

➡️ Tous les fichiers sont disponibles dans `/data`.

---

## ☁️ Architecture AWS

- 📦 S3 : Stockage des fichiers JSON + assets (images avatars/lieux)
- 🔁 Lambda : Orchestration des appels (optionnel V2)
- 🌐 API Gateway : Endpoints publics (optionnel)
- 🧠 Bedrock / OpenAI API : Génération des dialogues IA
- 🔊 Polly : Synthèse vocale du PNJ
- 🧱 Diagramme complet dans `/docs/architecture`

---

## 🚀 Installation rapide

### 🧰 Pré-requis
- Python 3.10+
- `streamlit`, `openai`, `boto3`, `langchain` (à adapter)
- Compte AWS (facultatif pour version locale)

### ▶️ Lancer l’app localement
```bash
git clone https://github.com/ton_profil/TavernAI.git
cd TavernAI
streamlit run app.py

TavernAI/
│
├── data/
│   ├── pnj_enriched_ai_ready.json
│   ├── lieux_enriched_with_tags_and_ambiance.json
│   ├── quetes_enriched_with_tags.json
│   ├── bestiaire_enriched_with_tags.json
│   └── matchmaking_rules_enriched.json
│
├── app/
│   └── streamlit_app.py (ou équivalent)
│
├── docs/
│   └── README_confluence.md
│   └── architecture_aws.png
│
├── images/
│   └── avatars_pnj/
│   └── lieux_fantasy/
│
└── README.md

# 🎬 Movie Recommendation System Using Collaborative Filtering

---

## 📝 Project Description
This repository delivers an end-to-end recommendation engine built to solve personalized content discovery challenges using the **MovieLens (100k)** data landscape. Leveraging memory-based **User-User Collaborative Filtering**, the system constructs a massive tabular matrix intersection between consumer histories. 

By calculating directional similarity alignments through **Pairwise Cosine Distance matrices**, the algorithm isolates the single nearest behavioral neighbor for a given user, scans for items they enjoyed that the target user hasn't seen yet, and drops a list of custom movie recommendations.

---

## 📐 Recommendation Pipeline Architecture

The workflow shifts raw relational tab-separated matrices into an active item prediction engine:

| Pipeline Stage | Strategy / Function Applied | Purpose |
| :--- | :--- | :--- |
| 📥 **Data Ingestion** | Tab-Separated Parsing (`delimiter='\t'`) | Normalizes custom flat streams (`u.data`) missing standard headers |
| 🔀 **Pivot Transformation** | Matrix Reshaping (`df.pivot`) | Builds a sparse `User_ID` $\times$ `Movie_ID` ratings matrix |
| 📐 **Distance Calibration** | `pairwise_distances(metric='cosine')` | Computes geometric angular similarities between consumer profiles |
| 🔍 **Insight Filtering** | Relative Set Difference (`set(B) - set(A)`) | Isolates highly rated unseen inventory items to recommend |

---

## 🔍 Core Recommendation Methodology

The notebook applies a definitive structural logic to recommend titles for targeted users (e.g., User IDs 10, 20, 30, 50, 100):
1. **Isolate Target Profile:** Track the user's existing historical matrix interactions.
2. **Find the Top-1 Nearest Neighbor:** Scan the calculated pairwise matrix column to capture the closest statistical match (excluding self-correlation at Index 0).
3. **Discover Content Gap:** Identify highly rated movies watched by the matching neighbor that the target user has never interacted with.
4. **Map Metadata Strings:** Relate the raw `movieid` arrays back to text records inside `u.item` to print clean, readable movie name recommendations.

---

## 🛠️ Tech Stack & Libraries Used
* **Mathematical Operations:** Scikit-Learn (`sklearn.metrics.pairwise_distances`)
* **Data Frames & Arrays:** Pandas, NumPy
* **Notebook Environments:** Google Colab / VS Code Jupyter Tools
* **Dataset Used:** MovieLens 100K Layout (`u.data` & `u.item`)

---

## 🗂️ Project Repository Structure
```text
├── Data/
│   ├── u.data                          # Tab-separated user ratings ledger (100k rows)
│   └── u.item                          # Pipe

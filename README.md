Voici une version propre en **Markdown** pour ton `README.md` :

````markdown
# 🦥 Coach-fr-mistral-finetune

Fine-tuning QLoRA de **Mistral 7B** pour l’assistant coach IA de **Loodo**, spécialisé en **motivation** et **organisation personnelle** en français.

---

## Résultats

| Version | Dataset | Loss | Temps GPU |
|---------|---------|------|-----------|
| V1 | 51 exemples | 0.945 | 11m54s |
| V2 | 150 exemples | 0.487 | 14m57s |

**x3 données → loss divisée par 2, pour seulement 3 minutes de GPU supplémentaires.**

---

## Stack

- **Modèle** — `unsloth/mistral-7b-instruct-v0.3-bnb-4bit`
- **Méthode** — QLoRA 4-bit · LoRA `rank=16` · `alpha=32`
- **Framework** — Unsloth `2026.3.5` · TRL `SFTTrainer` · HuggingFace Transformers
- **GPU** — Tesla T4 · 15.6 Go VRAM (Google Colab)

---

## Utilisation

```python
from unsloth import FastLanguageModel

model, tokenizer = FastLanguageModel.from_pretrained(
    "Pirodax/loodo-mistral-7b-coach-fr",
    load_in_4bit=True,
)
````

---

## Contenu du repo

```text
├── luna_fine_tuning.ipynb   # Notebook complet commenté
├── loodo_dataset.jsonl      # Dataset V1 (51 exemples)
├── loodo_dataset_150.jsonl  # Dataset V2 (150 exemples)
└── README.md
```

---

## Documentation complète

Pour une explication détaillée du projet — concepts **QLoRA**, choix techniques, métriques GPU, comparaison avant/après et analyse des limites — consulte la documentation :

📄 **Voir la documentation complète (Word)**

Elle couvre notamment :

* Fine-tuning
* LoRA
* QLoRA
* Pipeline d’entraînement
* Résultats qualitatifs
* Analyse GPU
* Hallucinations résiduelles

---

## Modèle publié

🤗 **[Pirodax/loodo-mistral-7b-coach-v1](https://huggingface.co/Pirodax/loodo-mistral-7b-coach-v1)** sur HuggingFace Hub.

```

Je peux aussi te faire une **version encore plus stylée GitHub**, avec badges, section objectifs, limites et roadmap.
```

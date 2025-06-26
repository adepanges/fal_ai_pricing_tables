# 🧠 fal.ai Model Pricing Table

A public, community-maintained table of pricing data for models available on [fal.ai](https://fal.ai). Useful for developers, researchers, and AI builders who want to compare and calculate costs before using a model.

## 📊 What’s Inside

This repository contains:
- A `fal_models` table schema (PostgreSQL)
- Clean tabular and structured data exports
- Utilities for filtering and comparing models based on:
  - Unit price
  - Use case (e.g., Text-to-Speech, Image-to-Video)
  - Commercial-use allowance

## 🗂 Sample Fields

| Field                     | Description                                               |
|---------------------------|-----------------------------------------------------------|
| `name`                   | Human-friendly model name                                  |
| `code`                   | Unique model identifier on fal.ai                         |
| `description`            | Short description of the model                            |
| `use_case`               | Type of task the model performs (e.g., text-to-speech)    |
| `unit_price`             | Price amount (e.g., 0.06)                                  |
| `unit_quantity`          | Quantity the price covers (e.g., 1000)                     |
| `unit_label`             | Unit of measurement (e.g., characters, tokens, seconds)    |
| `price_details`          | Full pricing detail as displayed on fal.ai                |
| `is_allowed_commercial_use` | Whether it’s licensed for commercial use             |
| `created_at`             | When the data was crawled                                  |
| `updated_at`             | When the data was last updated                             |

## 🧾 Example Record

```json
{
  "name": "MiniMax Speech-02 Turbo",
  "code": "fal-ai/minimax/speech-02-turbo",
  "description": "Generate fast speech from text prompts and different voices using the MiniMax Speech-02 Turbo model.",
  "use_case": "text-to-speech",
  "unit_price": 0.06,
  "unit_quantity": 1000,
  "unit_label": "characters",
  "price_details": "Your request will cost $0.06 per 1000 character.",
  "is_allowed_commercial_use": true,
  "created_at": "2025-06-01T00:00:00Z",
  "updated_at": "2025-06-25T00:00:00Z"
}
```

## 📦 Files

- `schema.sql` – PostgreSQL schema definition
- `fal_models.csv` – Clean tabular data for easy import
- `fal_models.json` – Full data dump in JSON format
- `fal_models.md` – Human-readable Markdown version of the model pricing table

## 🧑‍💻 Contributing

Feel free to submit:
- New model entries from fal.ai
- Fixes to outdated prices
- Suggestions for improvements

Pull requests are welcome!

---

**Note:** This project is not affiliated with fal.ai. All data is for research and personal use only.

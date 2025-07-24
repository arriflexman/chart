# chart
This repository contains the JSON code for chart analysis using chart IMG and open ai

---

## 🛠 Requirements

- **n8n instance**
- **Telegram bot credentials**
- **OpenAI API Key (GPT-4o)**
- **Chart-Img API Key**
- **Gate.io API endpoint access** (public, no auth)

---

## 🔒 Secrets & Credentials

| Service      | Type       | Location                         |
|--------------|------------|----------------------------------|
| Telegram Bot | n8n creds  | `Gate io Telegram bot account`   |
| OpenAI       | n8n creds  | `OpenAi account`                 |
| Chart-Img    | API Key    | Hardcoded in HTTP Header         |

---

## 🔁 Looping & Batching

- The workflow loops over all contracts that meet the 20% rise criteria.
- Uses `SplitInBatches` to manage resource load during analysis.

---

## 📌 Notes

- Analysis is designed for 1D trend identification but charting is done on `1h` for visual clarity.
- Only one Telegram user (Chat ID `7274498508`) receives the report.
- Error-handling is minimal; nodes use `continueErrorOutput`.

---

## 🧠 Future Improvements

- Add dynamic timeframe switching.
- Include RSI or Bollinger Bands in chart studies.
- Make Telegram chat ID dynamic per user request.

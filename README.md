# India-Stocks-481-510-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 481 to 510)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-481-510-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (481 to 510)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 481 | `TARIL` | Transformers And Rectifiers (India) Ltd. | `TARIL.NS` |
| 482 | `TRIDENT` | Trident Ltd. | `TRIDENT.NS` |
| 483 | `TRITURBINE` | Triveni Turbine Ltd. | `TRITURBINE.NS` |
| 484 | `UCOBANK` | UCO Bank | `UCOBANK.NS` |
| 485 | `UNOMINDA` | UNO Minda Ltd. | `UNOMINDA.NS` |
| 486 | `UTIAMC` | UTI Asset Management Company Ltd. | `UTIAMC.NS` |
| 487 | `UBL` | United Breweries Ltd. | `UBL.NS` |
| 488 | `URBANCO` | Urban Company Ltd. | `URBANCO.NS` |
| 489 | `USHAMART` | Usha Martin Ltd. | `USHAMART.NS` |
| 490 | `VTL` | Vardhman Textiles Ltd. | `VTL.NS` |
| 491 | `VISL` | Vedanta Iron and Steel Ltd. | `VISL.NS` |
| 492 | `VOGL` | Vedanta Oil and Gas Ltd. | `VOGL.NS` |
| 493 | `VEDPOWER` | Vedanta Power Ltd. | `VEDPOWER.NS` |
| 494 | `VIJAYA` | Vijaya Diagnostic Centre Ltd. | `VIJAYA.NS` |
| 495 | `WELCORP` | Welspun Corp Ltd. | `WELCORP.NS` |
| 496 | `WELSPUNLIV` | Welspun Living Ltd. | `WELSPUNLIV.NS` |
| 497 | `WHIRLPOOL` | Whirlpool of India Ltd. | `WHIRLPOOL.NS` |
| 498 | `WOCKPHARMA` | Wockhardt Ltd. | `WOCKPHARMA.NS` |
| 499 | `ZFCVINDIA` | ZF Commercial Vehicle Control Systems India Ltd. | `ZFCVINDIA.NS` |
| 500 | `ZEEL` | Zee Entertainment Enterprises Ltd. | `ZEEL.NS` |
| 501 | `ZENTEC` | Zen Technologies Ltd. | `ZENTEC.NS` |
| 502 | `ZENSARTECH` | Zensar Technolgies Ltd. | `ZENSARTECH.NS` |
| 503 | `ZYDUSWELL` | Zydus Wellness Ltd. | `ZYDUSWELL.NS` |
| 504 | `ECLERX` | eClerx Services Ltd. | `ECLERX.NS` |
| 505 | `20MICRONS` | 20 Microns Limited | `20MICRONS.NS` |
| 506 | `21STCENMGM` | 21st Century Management Services Limited | `21STCENMGM.NS` |
| 507 | `3BBLACKBIO` | 3B Blackbio Dx Limited | `3BBLACKBIO.NS` |
| 508 | `3IINFOLTD` | 3i Infotech Limited | `3IINFOLTD.NS` |
| 509 | `3MINDIA` | 3M India Limited | `3MINDIA.NS` |
| 510 | `3PLAND` | 3P Land Holdings Limited | `3PLAND.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream TARIL 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-481-510-Historical-Data/main/TARIL/1m/2026/10/TARIL_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```

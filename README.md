# tournament-msc-2026
Tournament MLBB MSC 2026 Data Analysis using Excel & Power BI
# 🏆 Mobile Legends: Bang Bang MSC 2026

[![Esports World Cup 2026](https://img.shields.io/badge/EWC-2026-gold?style=for-the-badge&logo=trophy)](https://esportsworldcup.com/)
[![Mid Season Cup 2026](https://img.shields.io/badge/Tournament-MSC_2026-0B00A3?style=for-the-badge)]([https://liquipedia.net/mobilelegends/MSC/2026])
[![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](#-dashboard-preview--features)
[![Dataset](https://img.shields.io/badge/Format-CSV-green?style=for-the-badge)](#-repository-structure)

---

## 📌 Executive Summary

Proyek ini menyajikan **end-to-end data analytics** untuk turnamen **Mobile Legends: Bang Bang Mid Season Cup (MSC) 2026** di ajang **Esports World Cup (EWC 2026)** yang berlangsung pada **1 Juli – 1 Agustus 2026**.

Karena data mentah turnamen belum tersedia secara publik saat kompetisi berakhir, pengumpulan data dilakukan secara **manual & terstruktur** melalui ekstraksi web **Liquipedia** serta peninjauan ulang siaran pertandingan (**YouTube VODs**). Dataset yang terkumpul kemudian dibersihkan kemudian diolah dan divisualisasikan dalam **Microsoft Power BI Dashboard** interaktif.

---

## 🖼️ Dashboard Preview & Features

[MWI 2026 Dashboard Preview]
**MLBB MID SEASON CUP 2026** <img width="1322" height="742" alt="Dashboard Overall" src="https://github.com/user-attachments/assets/c8fcafb0-78a8-4f95-958a-a674c7fdd023" />


### 🎯 Fitur Utama Dashboard:
** Visualisasi *Total Presence by Name Hero*, *Win Rate by Side*, serta *Total Hero, Total Games & Avg Match Duration*
---


## 🔥 Key Insights (Temuan Utama)
1. **Balance Hero**
   - Dari total 133 hero di MLBB, hanya **76 hero** yang tersentuh di fase *Pick* maupun *Ban*. Mengingat MSC 2026 masih menerapkan format *Draft Pick* standar (non-Global Ban/Fearless Draft), perebutan hero sangat terkonsentrasi pada 76 hero *tier-S* yang paling efektif sesuai meta turnamen.

2. **Match Duration**
   - Mayoritas pertandingan berlangsung hingga fase *Mid Game*. Ini menunjukkan ketatnya pertahanan *High Ground* serta kehati-hatian tim dalam melakukan *set-up Lord* tanpa terburu-buru mengakhiri game di *Early Game*.

3. **Top 5 Contest Rate Hero**
   - **Atlas:** Hero inisiator *Moment-Maker* yang sering memicu *comeback*.
   - **Freya:** *Fleksible Hero* yang bisa megang 2 lane *Goldlane/Explane* serta kuat untuk *1 on 1* atau *teamfight*.
   - **Hirara:** Hero baru jungler dengan mobilitas yang tinggi dan susah untuk ditangkap serta kurangnya *Counter Hero*.
   - **Marcel:** *Roamer* dengan *Crowd Control* tinggi dan mobilitas luar biasa.
   - **Fanny:** Hero *Jungler* yang sulit tapi sangat overpower serta mudah untuk *Snowball*.

4. **Best Side**
   - *Win Rate* **Blue Side (First Pick)** lebih tinggi dibandingkan Red Side di MSC 2026. Tim - tim MSC banyak yang bisa memanfaatkan *First Pick* mereka untuk mengambil hero power dan memaksimalkan potensi hero tersebut sehingga tim *Second Pick* strategi *Counter-Pick* nya tidak berjalan dengan baik.
---

## 🛠️ Tech Stack & Workflow

```text
[ Liquipedia & YouTube VODs ]
            │
            ▼  (Manual Data Collection & Structuring)
[ msc_all_general_fix.csv ]
            │
            ▼  (Data Cleaning & Transformation)
[ Power BI Desktop ] ─────────► (Build MSC 2026.pbix)
            │
            ▼  (Data Modeling & DAX Calculations)

[ Interactive Visual Dashboard & Documentation ]
```

- **Data Collection:** Liquipedia Web Scraping & YouTube Tournament Review
- **Data Storage:** Flat CSV (`msc_all_general_fix`)
- **Data Visualization & Modeling:** Microsoft Power BI (`MSC 2026.pbix`)
- **Version Control & Portfolio:** GitHub

---

## 📁 Repository Structure

```text
.
├── 📄 msc_all_general_fix.csv          # Raw & Cleaned Dataset (CSV Format)
├── 📊 MSC 2026.pbix                    # Master Power BI Report File
├── 🖼️ msc_dashboard_overview.png       # Screenshot / Preview Dashboard
└── 📝 README.md                        # Project Documentation
```

---

## 📑 Data Dictionary (Schema)

Dataset `MWI_X_EWC_2026.csv` mencakup **17 kolom utama** per baris pemain:

| Nama Kolom | Tipe Data | Deskripsi |
| :--- | :--- | :--- |
| `GameID` | String | Game ID untuk tiap pertandingan |
| `Date` | Date | Tanggal pertandingan berlangsung (DD-MM-YYYY) |
| `Side` | String | Posisi tim dalam draft (`Blue` / `Red`) |
| `Win/Lose` | String | Hasil pertandingan (`Win` / `Lose`) |
| `Player` | String | Nickname pemain |
| `Role` | String | Role pemain (`Goldlane`, `EXP`, `Mid`, `Roamer`, `Jungler`) |
| `Hero` | String | Hero yang digunakan pemain |
| `Hero Ban` | String | Daftar hero yang di-ban oleh tim pada game tersebut |
| `Spell` | String | Battle Spell yang digunakan pemain |
| `Team` | String | Nama tim pemain |
| `Opponent` | String | Nama tim lawan |
| `Skor Game` | String | Skor akhir seri pertandingan (misal: 2-0, 2-1) |
| `Kill` | Integer | Jumlah Kill individu pemain |
| `Death` | Integer | Jumlah Death individu pemain |
| `Assist` | Integer | Jumlah Assist individu pemain |
| `Duration` | String | Durasi pertandingan (MM:SS) |
| `Map` | String | Map yang digunakan dalam pertandingan |
| `Stage` | String | Stage pertandingan tersebut (Group Stage & Plyaoffs) |

---

## 🚀 How to Use / Reproduce

1. **Clone Repository ini:**
   ```bash
   git clone https://github.com/xapph1re/MLBB-MSC-2026.git
   ```
2. **Eksplorasi Data Mentah:** Buka file `msc_all_general_fix.csv` menggunakan Excel, Python (Pandas), atau impor ke Database SQL.
3. **Buka Dashboard Power BI:** Buka file `MSC_2026.pbix` menggunakan **Power BI Desktop** untuk melihat interaksi visualisasi, model DAX, dan grafik.

---

## 👨‍💻 Author & Contact

**Hanif Ubaidah**  
*Aspiring Data Analyst | Esports Analytics Enthusiast*

- 💼 **LinkedIn:** [https://www.linkedin.com/in/hanifubaidah13](https://linkedin.com)
- 🐙 **GitHub:** [(https://github.com/Xapph1re)](https://github.com)
- ✉️ **Email:** hanifubaidah07@gmail.com

## 📄 License & Attribution
Dataset ini dikumpulkan dan dibersihkan secara manual untuk tujuan edukasi dan analisis portofolio.
Bebas digunakan oleh siapa saja untuk kebutuhan riset/konten, cukup cantumkan kredit ke repository ini!

---
*Dibuat dengan semangat untuk memajukan industri Esports Analytics di Indonesia. Mari berdiskusi! 🚀*

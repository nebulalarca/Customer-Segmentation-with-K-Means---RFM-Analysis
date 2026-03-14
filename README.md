# 🛒 Customer Segmentation with K-Means & RFM Analysis

![Python](https://img.shields.io/badge/Python-3.11+-blue?logo=python)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange?logo=scikit-learn)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📌 Proje Hakkında

1 milyon satır e-ticaret verisi üzerinde **RFM özellik mühendisliği** ve 
**K-Means kümeleme** kullanarak 50.000 müşteriyi 5 anlamlı segmente ayıran 
uçtan uca bir makine öğrenmesi projesi.

---

## 🗂️ Proje Yapısı
```
customer-segmentation/
│
├── notebooks/
│   └── customer_segmentation.ipynb   # Ana notebook
│
├── outputs/
│   └── customer_segments.csv         # Segment sonuçları
│
├── .gitignore
├── requirements.txt
├── LICENSE
└── README.md
```

---

## 🔍 Kullanılan Yöntemler

### Veri Ön İşleme
- Eksik değer, iade ve aykırı değer temizleme (%87.5 veri korundu)
- Log1p transform (sağa çarpık dağılım düzeltme)
- StandardScaler normalizasyon

### Özellik Mühendisliği — RFM
| Özellik | Açıklama |
|---------|----------|
| Recency | Son alışverişten geçen gün sayısı |
| Frequency | Toplam benzersiz sipariş sayısı |
| Monetary | Toplam harcama (£) |

### Model
- Elbow yöntemi + Silhouette analizi → optimal k=5
- K-Means kümeleme (n_init=10, random_state=42)
- PCA ile 2D görselleştirme

---

## 📊 Sonuçlar

| Segment | Müşteri | Gelir Payı | Strateji |
|---------|---------|------------|----------|
| 🏆 Champions | 7,645 | %20 | VIP program |
| 💚 Loyal Customers | 12,757 | %34 | Sadakat ödülü |
| ⚠️ At Risk | 8,538 | %13 | Dönüştür |
| 🌱 Promising | 14,493 | %26 | Geri kazan |
| ❌ Churned | 6,567 | %7 | Son şans |

### Model Performansı
- **Silhouette Skoru:** 0.251
- **Davies-Bouldin Index:** 1.112
- **PCA Açıklanan Varyans:** %87.9

---

## 🚀 Kurulum
```bash
git clone https://github.com/nebulalarca/Customer-Segmentation-with-K-Means---RFM-Analysis.git
cd Customer-Segmentation-with-K-Means---RFM-Analysis
pip install -r requirements.txt
jupyter notebook notebooks/customer_segmentation.ipynb
```

---

## 📚 Teknolojiler

- **Python 3.11** · **pandas** · **numpy**
- **scikit-learn** — KMeans, StandardScaler, PCA
- **matplotlib** · **seaborn**
- **Jupyter Notebook**

---

## 📄 Lisans

MIT License

# Customer Segmentation with K Means & RFM Analysis
E-ticaret müşterilerini davranışsal örüntülere göre segmentlere ayıran, K-Means kümeleme ve RFM (Recency, Frequency, Monetary) skorlamasını birleştiren uçtan uca bir makine öğrenmesi projesi.

readme = """# 🛒 Customer Segmentation with K-Means & RFM Analysis

## 📌 Proje Özeti
1 milyon satır e-ticaret verisi üzerinde RFM (Recency, Frequency, Monetary) 
özellik mühendisliği ve K-Means kümeleme kullanarak 50.000 müşteriyi 
5 anlamlı segmente ayıran uçtan uca bir veri bilimi projesi.

## 📊 Sonuçlar
| Segment         | Müşteri | Gelir Payı | Strateji     |
|-----------------|---------|------------|--------------|
| Champions       | 7,645   | %20        | VIP program  |
| Loyal Customers | 12,757  | %34        | Sadakat ödülü|
| At Risk         | 8,538   | %13        | Dönüştür     |
| Promising       | 14,493  | %26        | Geri kazan   |
| Churned         | 6,567   | %7         | Son şans     |

## 🔧 Kullanılan Teknolojiler
- Python 3.11
- pandas, numpy
- scikit-learn (KMeans, StandardScaler, PCA)
- matplotlib, seaborn

## 📁 Proje Yapısı
```
customer_segmentation/
│
├── customer_segmentation.ipynb   # Ana notebook
├── customer_segments.csv         # Segment sonuçları
└── README.md                     # Bu dosya
```

## 🚀 Nasıl Çalıştırılır?
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
jupyter notebook customer_segmentation.ipynb
```

## 📈 Model Performansı
- Silhouette Skoru : 0.251
- Davies-Bouldin   : 1.112
- Açıklanan Varyans (PCA): %87.9

## 🔮 Sonraki Adımlar
- [ ] DBSCAN ile karşılaştırma
- [ ] Streamlit dashboard
- [ ] Aylık otomatik yeniden segmentasyon
- [ ] A/B test ile strateji doğrulama
"""

with open('README.md', 'w', encoding='utf-8') as f:
    f.write(readme)
print("🔹 Loyal Customers toplam gelirin %34'ünü üretiyor")
print("🔹 Churned segment → £4.7M kurtarılabilir gelir")
print("🔹 Tech: Python, scikit-learn, pandas, seaborn")

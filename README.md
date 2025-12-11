# Maternal Health Risk Classification  
Bu proje, hamile kadınların sağlık verilerini kullanarak **düşük, orta ve yüksek risk seviyelerini** makine öğrenmesi modelleriyle tahmin etmeyi amaçlar.  
Proje iki ana aşamadan oluşur: **Veri Temizleme** ve **Model Eğitimi**.

---

## 📌 Proje İçeriği

### 1. Veri Temizleme (01_data_cleaning.ipynb)
Bu bölümde aşağıdaki işlemler yapılmıştır:

- Eksik değer analizi ve doldurma
- Aykırı değer tespiti (IQR yöntemi)
- Aykırı değerlerin sınır değerlerle veya ortalama ile düzeltilmesi
- Kategorik değişkenlerin yeniden sıralanması
- Veri setinin genel istatistiklerinin incelenmesi
- Keşifsel veri analizi (EDA)
  - Kutu grafikleri (boxplot)
  - KDE, scatter plot, line plot görselleştirmeleri

Temizlenmiş veri daha sonra **güncel_veriSeti.xlsx** olarak kaydedilmiştir.

---

### 2. Model Eğitimi (02_model_training.ipynb)
Bu bölümde aşağıdaki modeller uygulanmıştır:

#### 🔹 KNN (K-En Yakın Komşu)
- GridSearchCV ile en iyi `k` değeri seçildi
- En iyi skor: **%75.4 accuracy**

#### 🔹 MLPClassifier (Yapay Sinir Ağı)
- Çok katmanlı yapay sinir ağı
- Hiperparametre araması yapıldı (activation, solver, hidden layers, alpha)
- En iyi skor: **%78.6 accuracy**  
  🔥 *Projedeki en başarılı model*

#### 🔹 Random Forest
- Derinlik, ağaç sayısı, min_samples_split için GridSearch yapıldı
- En iyi skor: **%75.7 accuracy**

#### 🔹 LightGBM
- Learning rate, max_depth, num_leaves, subsample için tarama yapıldı
- En iyi skor: **%76 accuracy**

---

## 📊 Modellerin Performans Karşılaştırması

| Model | Accuracy |
|-------|----------|
| KNN | %75.4 |
| MLPClassifier | **%78.6** ⭐ |
| Random Forest | %75.7 |
| LightGBM | %76.0 |

---

## 🗂 Proje Yapısı

maternal-health-risk-classification
│── README.md
│── notebooks
│ ├── 01_data_cleaning.ipynb
│ └── 02_model_training.ipynb
│── data
│── images
└── models


---

## 🧠 Kullanılan Teknolojiler
- Python  
- Pandas, NumPy  
- Seaborn, Matplotlib  
- Scikit-learn  
- LightGBM  
- Jupyter Notebook  

---

## 🎯 Amaç
Gerçek dünyadaki bir veri kümesini kullanarak:

- Veri analizi
- Veri temizleme
- Makine öğrenmesi modeli eğitimi
- Model performans karşılaştırması

alanlarında deneyim kazanmaktır.

---

## ✨ Sonuç
MLPClassifier modeli diğer modellere göre en yüksek başarıyı göstermiştir.  
Bu sonuç, **yapay sinir ağlarının çok boyutlu sağlık verilerinde oldukça etkili olduğunu** göstermektedir.


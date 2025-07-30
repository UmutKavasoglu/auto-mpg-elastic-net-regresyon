# Auto MPG Veri Seti ile Elastic Net Regresyon Analizi

Bu proje, UCI Machine Learning Repository'de bulunan **Auto MPG** veri setini kullanarak bir aracın yakıt verimliliğini tahmin etmeyi amaçlamaktadır. Proje, basit bir modelleme yaklaşımının ötesine geçerek, gerçek dünya verilerinde sıkça karşılaşılan **aykırı değerler, temel regresyon varsayımlarının ihlali ve çoklu doğrusallık** gibi temel sorunlara sistematik ve istatistiksel olarak sağlam çözümler getirmektedir.

## Projenin Amacı ve Yaklaşımı

Standart bir regresyon modeli kurulduğunda, artıkların normal dağılmaması ve varyansın sabit olmaması gibi varsayım ihlalleriyle karşılaşılmıştır. Bu proje, bu sorunları adım adım ele alarak istatistiksel olarak geçerli ve yüksek tahmin gücüne sahip bir **Elastic Net regresyon modeli** inşa etme sürecini detaylandırmaktadır.

### Neden Bu Proje Önemli?
- **Sistematik Çözüm:** Sadece bir model kurmak yerine, modelin istatistiksel zayıflıklarını tespit edip bunları metodik olarak giderir.
- **Gelişmiş Teknikler:** Aykırı değer tespiti için **Local Outlier Factor (LOF)** ve varsayımları sağlamak için farklı matematiksel dönüşüm kombinasyonları uygular.
- **Tekrarlanabilirlik:** Baştan sona tüm adımlar, kod içerisinde açıkça belgelenmiş ve tekrarlanabilir bir yapıdadır.

## Temel Bulgular ve Sonuçlar

| Metrik | Başlangıç Modeli | Final Modeli | Yorum |
| :--- | :--- | :--- | :--- |
| **Eğitim R²** | 0.816 | **0.896** | Modelin veriyi açıklama gücü yaklaşık **%9.8** oranında arttı. |
| **Eğitim MAE** | 2.519 | **1.817** | Modelin tahmin hatası yaklaşık **%28** oranında azaldı. |
| **Normallik Varsayımı** | Sağlanmadı (p < 0.05) | **Sağlandı (p > 0.05)** | Normal dağılım varsayımı sağlandı. |
| **Sabit Varyanslılık Varsayımı** | Sağlanmadı (p < 0.05) | **Sağlandı (p > 0.05)** | Sabit varyanslılık varsayımı sağlandı. |

**Test Verisi Performansı:**

Nihai modelin test verisi üzerindeki performansı, modelin genellenebilirliğini doğrulamaktadır:
-   **R² Değeri:** **0.811**
-   **Ortalama Mutlak Hata (MAE):** **2.338**

**Sonuç:** Bu proje, veri ön işleme, varsayım kontrolü ve model iyileştirme adımlarının bir regresyon modelinin performansını ve güvenilirliğini ne kadar önemli ölçüde artırabildiğini göstermektedir. Geliştirilen final modeli, hem daha isabetli tahminler yapmakta hem de istatistiksel olarak sağlam temellere dayanmaktadır.

## Veri Seti

Bu çalışmada kullanılan **Auto MPG** veri seti, UCI Machine Learning Repository'den temin edilmiştir.

-   **Kaynak:** [UCI Machine Learning Repository: Auto MPG Data Set](https://archive.ics.uci.edu/dataset/9/auto+mpg)

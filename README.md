# Smart_Manufacturing_IoT_Cloud_Monitoring

# Makine Bakım Tahmini (Predictive Maintenance)
endüstriyel ekipmanların arıza süreçlerini öngörmek ve bakımı verimli planlamak için makine öğrenimi modellerinin kullanıldığı bir projedir. Bu projede, sensör verileri (sıcaklık, titreşim, nem, basınç, enerji tüketimi), makine durumu (çalışıyor/beklemede/arıza), anomali işaretleri ve arıza türü gibi çok boyutlu veriler analiz edilerek "Maintenance Required" hedef değişkeni tahmin edilir. Amaç, plansız duruşları minimize etmek, maliyetleri azaltmak ve operasyonel verimliliği artırmaktır.

# Veri Ön İşleme ve Analiz
Veri setindeki Timestamp, zaman serisi analizi için saat/gün bilgisine dönüştürülür. Machine ID, kategorik bir değişken olarak işlenebilir veya makine özelindeki eğilimleri yakalamak için kullanılır. Sensör verileri, normalizasyon veya standartlaştırma ile ölçeklenir. Anomaly Flag ve Failure Type, model için kritik ipuçları sağlar; örneğin, anomali varken "Overheating" arıza tipi, bakım ihtimalini artırabilir. Downtime Risk Score ise risk seviyesini nicelleştirir. Hedef değişkenin dengesiz olması durumunda SMOTE veya ağırlıklandırma teknikleri uygulanır.

# Model Seçimi ve Optimizasyon
Problemin doğası (binary classification) göz önüne alınarak Random Forest, XGBoost, veya Gradient Boosting gibi ensemble modelleri tercih edilebilir. Zaman serisi bağımlılığı varsa LSTM veya GRU gibi derin öğrenme modelleri denenebilir. Model performansı, F1-Score ve ROC-AUC ile değerlendirilir, çünkü dengesiz veride accuracy yanıltıcı olabilir. Bias-variance dengesi için çapraz doğrulama ve öğrenme eğrileri incelenir: Yüksek bias (underfitting) durumunda model karmaşıklığı artırılır; yüksek variance (overfitting) durumunda regularizasyon (L1/L2) veya veri artırma teknikleri uygulanır.

# Sonuç ve İş Değeri
Başarılı bir model, bakım maliyetlerini %20-30 azaltabilir ve ekipman ömrünü uzatabilir. Ancak, modelin açıklanabilirliği (SHAP/LIME ile) önemlidir, çünkü bakım ekiplerinin karar sürecine entegre edilmelidir. Sonuç olarak, bu proje veri odaklı karar destek sistemlerinin endüstriyel sürdürülebilirlikteki rolünü vurgular.

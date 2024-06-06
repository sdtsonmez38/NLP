Bu çalışma, metin sınıflandırma görevini gerçekleştirmek için BERT (Bidirectional Encoder Representations from Transformers) modelini ve çeşitli makine öğrenmesi algoritmalarını kullanmaktadır. Aşağıda adım adım sürecin açıklaması yer almaktadır:
1. Gerekli Kütüphaneleri Yükleme:
Gerekli Python kütüphaneleri yüklenir. Bu kütüphaneler arasında veri işleme (pandas, numpy), görselleştirme (matplotlib, seaborn), metin işleme (nltk), ve makine öğrenmesi (sklearn) bulunmaktadır. Hugging Face Transformers Kütüphanesi BERT modelini yüklemek için kullanılır.
2. NLTK Verilerini İndirme:
NLTK kütüphanesinin stop words (durma kelimeleri) verisi indirilir ve bu kelimeler set olarak tanımlanır.
3. Veri Setlerini Yükleme:
Eğitim ve test veri setleri CSV dosyalarından yüklenir.
4. Etiketleri Sayısallaştırma:
Etiketler (sınıflar) LabelEncoder kullanılarak sayısal değerlere dönüştürülür.
5. Metin Ön İşleme Fonksiyonu:
Metin verileri temizlenir. Bu süreçte:
Metin küçük harflere dönüştürülür.
Noktalama işaretleri ve sayılar kaldırılır.
Durma kelimeleri kaldırılır.
6. Metinleri Ön İşleme:
Ön işleme fonksiyonu kullanılarak eğitim ve test setlerindeki metinler temizlenir.
7. BERT Modelini ve Tokenizer'ı Yükleme:
BERT modeli ve tokenizer, bert-base-uncased ön eğitilmiş modeli kullanılarak yüklenir.
8. Metinleri BERT ile Dönüştürme:
Bir metin için BERT gömülmelerini elde eden bir fonksiyon tanımlanır. Bu fonksiyon, tokenizer kullanarak metni dönüştürür ve BERT modelini kullanarak gömülmeleri hesaplar.
9. Eğitim ve Test Setleri İçin BERT Gömülmelerini Elde Etme:
Eğitim ve test setlerindeki tüm metinler için BERT gömülmeleri hesaplanır.
10. Model Eğitimi ve Değerlendirme:
Çeşitli makine öğrenmesi modelleri (Logistic Regression, Random Forest, SVM) eğitilir ve test seti üzerinde değerlendirilir. Modellerin performansı accuracy (doğruluk) ve classification report (sınıflandırma raporu) kullanılarak ölçülür.
Model Sonuçları:
Logistic Regression: Accuracy: 0.847, F1-Score (0: 0.81, 1: 0.79, 2: 0.95)
Random Forest: Accuracy: 0.738, F1-Score (0: 0.72, 1: 0.66, 2: 0.83)
SVM: Accuracy: 0.847, F1-Score (0: 0.80, 1: 0.79, 2: 0.95)
Logistic Regression ve SVM modelleri, Random Forest modeline göre daha yüksek doğruluk ve f1-score değerleri elde etmiştir.
Bu sonuçlar, BERT modelinin metin sınıflandırma görevlerinde güçlü bir temsil yeteneğine sahip olduğunu ve Logistic Regression ile SVM modellerinin bu temsilleri başarılı bir şekilde kullandığını göstermektedir.

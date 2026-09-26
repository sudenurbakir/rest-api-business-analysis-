# Stakeholders

## 1. Stakeholder Listesi

| Stakeholder        | Rolü                                 | İhtiyacı                                                 |
| ------------------ | ------------------------------------ | -------------------------------------------------------- |
| Customer           | Sipariş veren kullanıcı              | Siparişinin doğru oluşturulması ve durumunu görebilmek   |
| Frontend Developer | API'yi kullanan geliştirici          | API'nin doğru endpoint ve response yapısına sahip olması |
| Backend Developer  | API'yi geliştiren geliştirici        | Gereksinimlerin ve iş kurallarının net olması            |
| Business Analyst   | İş ve teknik ihtiyaçları analiz eder | Gereksinimleri ve API davranışlarını dokümante etmek     |
| QA / Tester        | Sistemi test eder                    | Test edilebilir ve net API kuralları                     |
| Product Owner      | Ürün ihtiyaçlarından sorumlu         | Sipariş sürecinin iş gereksinimlerini karşılaması        |

## 2. Stakeholder Sorumlulukları

### Customer

* Sipariş oluşturur.
* Sipariş bilgilerini görüntüler.
* Sipariş durumunu takip eder.

### Frontend Developer

* API'ye request gönderir.
* API response'larını kullanır.
* Hata durumlarını kullanıcı arayüzüne yansıtır.

### Backend Developer

* API endpoint'lerini geliştirir.
* İş kurallarını uygular.
* Response ve hata yapılarını oluşturur.

### Business Analyst

* İş gereksinimlerini belirler.
* API gereksinimlerini dokümante eder.
* Request/response beklentilerini tanımlar.
* Geliştirme ve test ekipleri arasındaki iletişimi destekler.

### QA / Tester

* API test senaryolarını hazırlar.
* Başarılı ve hatalı request'leri test eder.
* Beklenen ve gerçekleşen sonuçları karşılaştırır.

### Product Owner

* İş ihtiyaçlarını belirler.
* Gereksinimleri önceliklendirir.
* Geliştirilen çözümün iş ihtiyacını karşılayıp karşılamadığını değerlendirir.

## 3. Basit Süreç

```text
Product Owner
      ↓
Business Analyst
      ↓
Backend Developer
      ↓
API
      ↓
Frontend Developer
      ↓
Customer

QA / Tester → API'yi test eder
```

## 4. BA Açısından Önemli Nokta

Business Analyst'in burada temel görevi **API'yi kodlamak değil**, sistemin ne yapması gerektiğini açık ve test edilebilir şekilde tanımlamaktır.

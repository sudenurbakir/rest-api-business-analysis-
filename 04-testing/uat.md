# User Acceptance Testing (UAT)

## 1. Amaç

UAT (User Acceptance Testing), geliştirilen sistemin iş gereksinimlerini karşılayıp karşılamadığını doğrulamak için yapılan kullanıcı kabul testidir.

Bu projede sipariş API'sinin temel işlevleri değerlendirilecektir.

## 2. UAT Senaryoları

| UAT ID | Senaryo                         | Beklenen Sonuç                          |
| ------ | ------------------------------- | --------------------------------------- |
| UAT-01 | Yeni sipariş oluşturma          | Sipariş başarıyla oluşturulmalı.        |
| UAT-02 | Sipariş bilgilerini görüntüleme | Doğru sipariş bilgileri gösterilmeli.   |
| UAT-03 | Sipariş durumunu takip etme     | Güncel sipariş durumu görüntülenmeli.   |
| UAT-04 | Sipariş bilgilerini güncelleme  | İzin verilen bilgiler güncellenmeli.    |
| UAT-05 | Siparişi iptal etme             | Uygun durumdaki sipariş iptal edilmeli. |

## 3. Kabul Kriterleri

* Sipariş oluşturma işlemi doğru çalışmalıdır.
* Sipariş bilgileri doğru görüntülenmelidir.
* Sipariş durumu güncel olmalıdır.
* İzin verilen güncellemeler gerçekleştirilebilmelidir.
* Sipariş iptali belirlenen iş kurallarına uygun olmalıdır.

## 4. UAT Sonuçları

| Durum   | Açıklama                                       |
| ------- | ---------------------------------------------- |
| Passed  | Senaryo başarıyla tamamlandı.                  |
| Failed  | Beklenen sonuç elde edilemedi.                 |
| Blocked | Test, bir engel nedeniyle gerçekleştirilemedi. |

## 5. BA Notu

UAT, kullanıcıların ve iş birimlerinin sistemin ihtiyaçlarını karşılayıp karşılamadığını değerlendirmesini sağlar.

API testleri teknik davranışa odaklanırken UAT, iş beklentilerine odaklanır.

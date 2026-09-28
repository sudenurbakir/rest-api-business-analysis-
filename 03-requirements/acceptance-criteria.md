# Acceptance Criteria

## 1. Amaç

Bu doküman, sipariş API'si için hazırlanan User Story'lerin kabul koşullarını tanımlar.

## 2. Acceptance Criteria

### US-01 — Sipariş Oluşturma

* Müşteri, ürün ve adet bilgileri gönderilmelidir.
* Zorunlu bilgiler eksikse sipariş oluşturulmamalıdır.
* Başarılı işlemde benzersiz bir Order ID dönmelidir.
* Yeni siparişin durumu Pending olmalıdır.

### US-02 — Sipariş Görüntüleme

* Geçerli Order ID ile sipariş bilgileri döndürülmelidir.
* Sipariş bulunamazsa 404 Not Found dönmelidir.
* Response içerisinde siparişin temel bilgileri bulunmalıdır.

### US-03 — Sipariş Durumu Görüntüleme

* Geçerli Order ID ile mevcut sipariş durumu döndürülmelidir.
* Sipariş bulunamazsa 404 Not Found dönmelidir.
* Response içerisinde siparişin güncel durumu yer almalıdır.

### US-04 — Sipariş Güncelleme

* Güncelleme için geçerli bir Order ID gönderilmelidir.
* Yalnızca izin verilen bilgiler güncellenebilmelidir.
* Başarılı işlemde güncel sipariş bilgileri döndürülmelidir.
* Geçersiz bilgiler gönderildiğinde 400 Bad Request dönmelidir.

### US-05 — Sipariş İptali

* Yalnızca Pending veya Confirmed durumundaki siparişler iptal edilebilmelidir.
* Başarılı iptal işleminde sipariş durumu Cancelled olmalıdır.
* İptal edilemeyen siparişlerde işlem reddedilmelidir.

### US-06 — Geçersiz İsteklerin Reddedilmesi

* Zorunlu alanlar kontrol edilmelidir.
* Geçersiz veriler kabul edilmemelidir.
* Hatalı isteklerde uygun HTTP status code ve hata mesajı dönmelidir.

## 3. BA Notu

Acceptance Criteria, bir User Story'nin tamamlanmış sayılması için karşılanması gereken koşullardır.

Bu koşullar, geliştirilen API'nin beklenen davranışı gösterip göstermediğini test etmek için kullanılır.

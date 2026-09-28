# API Test Scenarios

## 1. Amaç

Bu doküman, sipariş API'sinin beklenen şekilde çalışıp çalışmadığını kontrol etmek için hazırlanan temel test senaryolarını içerir.

## 2. Test Senaryoları

| Test ID | Senaryo                                     | Beklenen Sonuç  |
| ------- | ------------------------------------------- | --------------- |
| TC-01   | Geçerli bilgilerle sipariş oluşturma        | 201 Created     |
| TC-02   | Zorunlu alan eksikliğiyle sipariş oluşturma | 400 Bad Request |
| TC-03   | Geçerli Order ID ile sipariş görüntüleme    | 200 OK          |
| TC-04   | Olmayan Order ID ile sipariş görüntüleme    | 404 Not Found   |
| TC-05   | Sipariş durumunu görüntüleme                | 200 OK          |
| TC-06   | İzin verilen durumda sipariş güncelleme     | 200 OK          |
| TC-07   | Uygun durumdaki siparişi iptal etme         | 200 OK          |
| TC-08   | İptal edilemeyen siparişi iptal etme        | 400 Bad Request |

## 3. Örnek Test Senaryosu

**TC-01 — Sipariş Oluşturma**

| Alan                 | Açıklama                                   |
| -------------------- | ------------------------------------------ |
| Endpoint             | `POST /orders`                             |
| Ön koşul             | Geçerli müşteri ve ürün bulunmalı.         |
| Request              | customerId, productId, quantity            |
| Beklenen Status Code | 201 Created                                |
| Beklenen Sonuç       | Sipariş oluşturulmalı ve Order ID dönmeli. |

## 4. Test Türleri

* **Positive Testing:** Geçerli bilgilerle işlemin başarılı olduğunu kontrol eder.
* **Negative Testing:** Eksik veya geçersiz bilgilerle sistemin doğru hata verdiğini kontrol eder.

## 5. BA Notu

API test senaryoları, gereksinimlerde belirtilen davranışların doğrulanmasını sağlar. Beklenen sonuç ile gerçekleşen sonuç karşılaştırılarak testin başarılı olup olmadığı belirlenir.

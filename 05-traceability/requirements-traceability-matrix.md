# Requirements Traceability Matrix

## 1. Amaç

Requirements Traceability Matrix (RTM), gereksinimlerin User Story, Acceptance Criteria ve test senaryolarıyla bağlantısını takip etmeyi sağlar.

## 2. Traceability Matrix

| Business Requirement              | Functional Requirement | User Story | Test Case | UAT    |
| --------------------------------- | ---------------------- | ---------- | --------- | ------ |
| BR-01 Sipariş oluşturma           | FR-01/02               | US-01      | TC-01     | UAT-01 |
| BR-02 Sipariş görüntüleme         | FR-05                  | US-02      | TC-03/04  | UAT-02 |
| BR-04 Sipariş durumu takibi       | FR-07                  | US-03      | TC-05     | UAT-03 |
| BR-03 Sipariş güncelleme          | FR-06                  | US-04      | TC-06     | UAT-04 |
| BR-01/05 Geçerli sipariş kontrolü | FR-03/08               | US-06      | TC-02     | -      |
| BR-03 Sipariş iptali              | FR-06                  | US-05      | TC-07/08  | UAT-05 |

## 3. Örnek İzleme

Örneğin:

**BR-01:** Sistem yeni sipariş oluşturabilmelidir.

↓

**FR-01:** Sistem yeni bir sipariş oluşturabilmelidir.

↓

**US-01:** Müşteri olarak sipariş oluşturmak istiyorum.

↓

**Acceptance Criteria:** Zorunlu bilgiler gönderilmeli ve başarılı işlemde Order ID dönmeli.

↓

**TC-01:** Geçerli bilgilerle sipariş oluşturma.

↓

**UAT-01:** Yeni sipariş oluşturma.

Bu bağlantı sayesinde gereksinimin analizden teste kadar nasıl takip edildiği görülebilir.

## 4. BA Açısından Önemi

RTM sayesinde:

* Gereksinimlerin test edilip edilmediği görülebilir.
* Eksik testler fark edilebilir.
* Gereksinim ve test arasındaki bağlantı korunabilir.
* UAT süreci daha kontrollü yürütülebilir.

**Kısaca:** RTM, "Bu gereksinim nerede test edildi?" sorusuna cevap verir.

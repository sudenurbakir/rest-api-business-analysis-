# Business Requirements

## 1. Amaç

Sipariş işlemlerinin API üzerinden standart ve kontrollü şekilde yönetilmesi amaçlanmaktadır.

## 2. Business Requirements

| ID    | Business Requirement                                                           |
| ----- | ------------------------------------------------------------------------------ |
| BR-01 | Sistem yeni bir sipariş oluşturabilmelidir.                                    |
| BR-02 | Kullanıcı mevcut sipariş bilgilerini görüntüleyebilmelidir.                    |
| BR-03 | Sipariş bilgileri gerektiğinde güncellenebilmelidir.                           |
| BR-04 | Siparişin mevcut durumu takip edilebilmelidir.                                 |
| BR-05 | Geçersiz veya eksik sipariş bilgilerinin sisteme kaydedilmesi engellenmelidir. |
| BR-06 | API işlemleri standart bir response yapısı döndürmelidir.                      |
| BR-07 | Oluşan hatalar anlaşılır şekilde bildirilebilmelidir.                          |
| BR-08 | Sipariş işlemleri test edilebilir olmalıdır.                                   |

## 3. Öncelik

| Öncelik | Gereksinimler              |
| ------- | -------------------------- |
| High    | BR-01, BR-02, BR-04, BR-05 |
| Medium  | BR-03, BR-06, BR-07        |
| Low     | BR-08                      |

## 4. BA Notu

Business Requirement'lar **sistemin ne yapması gerektiğini** tanımlar.

Örneğin:

> BR-01: Sistem yeni bir sipariş oluşturabilmelidir.

Bu gereksinimin teknik olarak nasıl gerçekleştirileceği ise sonraki aşamalarda, **Functional Requirements** ve **API Analysis** bölümünde detaylandırılacaktır.

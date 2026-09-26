# Functional Requirements

## 1. Functional Requirements

| ID    | Functional Requirement                                              |
| ----- | ------------------------------------------------------------------- |
| FR-01 | Sistem yeni bir sipariş oluşturabilmelidir.                         |
| FR-02 | Sipariş oluşturulurken müşteri ve ürün bilgileri alınmalıdır.       |
| FR-03 | Zorunlu sipariş bilgileri kontrol edilmelidir.                      |
| FR-04 | Oluşturulan sipariş için benzersiz bir Order ID üretilmelidir.      |
| FR-05 | Mevcut sipariş Order ID kullanılarak görüntülenebilmelidir.         |
| FR-06 | Sipariş bilgileri belirlenen kurallara göre güncellenebilmelidir.   |
| FR-07 | Siparişin mevcut durumu görüntülenebilmelidir.                      |
| FR-08 | Geçersiz bilgiler gönderildiğinde sistem hata mesajı döndürmelidir. |
| FR-09 | Başarılı işlemlerde sistem uygun HTTP status code döndürmelidir.    |
| FR-10 | API response'ları standart bir JSON yapısında dönmelidir.           |

## 2. Temel Sipariş Bilgileri

Bir sipariş için temel olarak aşağıdaki bilgiler kullanılacaktır:

| Alan         | Açıklama                    |
| ------------ | --------------------------- |
| Order ID     | Siparişin benzersiz kimliği |
| Customer ID  | Müşteri kimliği             |
| Product ID   | Ürün kimliği                |
| Quantity     | Ürün adedi                  |
| Order Status | Sipariş durumu              |
| Order Date   | Sipariş tarihi              |

## 3. Sipariş Durumları

Sipariş aşağıdaki durumlardan birinde olabilir:

```text
Pending
   ↓
Confirmed
   ↓
Shipped
   ↓
Delivered
```

Sipariş iptal edilirse:

```text
Pending / Confirmed
        ↓
     Cancelled
```

## 4. BA Notu

Functional Requirement, Business Requirement'ın sistem davranışına dönüştürülmüş halidir.

Örneğin:

**Business Requirement**

> Sistem yeni bir sipariş oluşturabilmelidir.

**Functional Requirement**

> Sipariş oluşturulurken müşteri, ürün ve adet bilgileri alınmalı ve sipariş için benzersiz bir Order ID oluşturulmalıdır.

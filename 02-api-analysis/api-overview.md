# API Overview

## 1. API Nedir?

API (Application Programming Interface), farklı yazılım sistemlerinin birbiriyle iletişim kurmasını sağlayan bir arayüzdür.

Bu projede API, e-ticaret sistemi ile sipariş sistemi arasındaki iletişimi sağlar.

```text
Customer
   ↓
Frontend
   ↓
REST API
   ↓
Order System
```

## 2. REST API Nedir?

REST API, sistemler arasında HTTP üzerinden veri alışverişi yapılmasını sağlayan yaygın bir API yaklaşımıdır.

Bu projede temel olarak:

* GET
* POST
* PUT
* DELETE

HTTP methodları kullanılacaktır.

## 3. Endpoint Nedir?

Endpoint, API içerisinde belirli bir işlemi gerçekleştirmek için kullanılan adrestir.

Örneğin:

```text
GET /orders/1001
```

Burada:

* `GET` → Yapılacak işlem
* `/orders` → Sipariş kaynağı
* `1001` → Sipariş ID'si

anlamına gelir.

## 4. Temel HTTP Methodları

| Method | Kullanım                |
| ------ | ----------------------- |
| GET    | Veri görüntüleme        |
| POST   | Yeni kayıt oluşturma    |
| PUT    | Mevcut kaydı güncelleme |
| DELETE | Kayıt silme             |

Örneğin:

```text
POST /orders
```

Yeni sipariş oluşturmak için kullanılabilir.

```text
GET /orders/1001
```

1001 numaralı siparişi görüntülemek için kullanılabilir.

## 5. Request ve Response

### Request

İstemcinin API'ye gönderdiği istektir.

Örneğin yeni sipariş oluşturma isteği:

```json
{
  "customerId": 101,
  "productId": 5001,
  "quantity": 2
}
```

### Response

API'nin isteğe verdiği cevaptır.

Örneğin:

```json
{
  "orderId": 1001,
  "status": "Pending",
  "message": "Order created successfully"
}
```

## 6. BA Açısından Neden Önemli?

Business Analyst'in API konusunda kod yazması gerekmeyebilir.

Ancak BA'nın şu soruları anlayabilmesi önemlidir:

* Hangi endpoint kullanılacak?
* Hangi HTTP method kullanılacak?
* Request içerisinde hangi bilgiler gönderilecek?
* Response içerisinde hangi bilgiler dönecek?
* Hangi durumda hata oluşacak?
* Başarılı işlemde hangi status code dönecek?

Bu bilgiler geliştirici ve test ekipleriyle gereksinimlerin doğru şekilde paylaşılmasını sağlar.

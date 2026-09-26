# Request & Response

## 1. Request Nedir?

Request, istemcinin API'ye gönderdiği istektir.

Örneğin yeni sipariş oluşturmak için:

```http
POST /orders
```

Request body:

```json
{
  "customerId": 101,
  "productId": 5001,
  "quantity": 2
}
```

Bu request içerisinde:

| Alan       | Açıklama      | Zorunlu |
| ---------- | ------------- | ------- |
| customerId | Müşteri ID'si | Evet    |
| productId  | Ürün ID'si    | Evet    |
| quantity   | Ürün adedi    | Evet    |

---

## 2. Response Nedir?

Response, API'nin gönderilen request'e verdiği cevaptır.

Başarılı sipariş oluşturma örneği:

```json
{
  "orderId": 1001,
  "customerId": 101,
  "productId": 5001,
  "quantity": 2,
  "status": "Pending"
}
```

---

## 3. Başarılı Response

Sipariş başarıyla oluşturulduğunda:

**HTTP Status Code:** `201 Created`

```json
{
  "orderId": 1001,
  "status": "Pending",
  "message": "Order created successfully"
}
```

Burada:

* `orderId` → Oluşturulan siparişin ID'si
* `status` → Siparişin mevcut durumu
* `message` → İşlemin sonucunu açıklayan mesaj

---

## 4. Hatalı Request

Zorunlu bilgilerden biri gönderilmezse API hata döndürmelidir.

Örneğin:

```json
{
  "customerId": 101,
  "quantity": 2
}
```

`productId` gönderilmediği için:

**HTTP Status Code:** `400 Bad Request`

```json
{
  "error": "productId is required"
}
```

---

## 5. Sipariş Görüntüleme Response'u

```http
GET /orders/1001
```

Response:

```json
{
  "orderId": 1001,
  "customerId": 101,
  "productId": 5001,
  "quantity": 2,
  "status": "Shipped"
}
```

---

## 6. BA Açısından Request / Response

BA'nın burada temel olarak netleştirmesi gerekenler:

**Request**

* Hangi bilgiler gönderilecek?
* Hangi alanlar zorunlu?
* Veri tipleri ne olacak?

**Response**

* Hangi bilgiler dönecek?
* Başarılı işlemde ne dönecek?
* Hata durumunda ne dönecek?

Bu bilgiler geliştirici ve test ekibinin aynı beklenti üzerinden çalışmasını sağlar.

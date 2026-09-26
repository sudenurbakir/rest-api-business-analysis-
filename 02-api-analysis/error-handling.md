# Error Handling

## 1. Amaç

API'ye gönderilen hatalı veya geçersiz isteklerde sistemin anlaşılır ve standart cevaplar vermesi amaçlanmaktadır.

## 2. Temel Hata Durumları

| HTTP Status Code | Durum                 | Açıklama                                               |
| ---------------- | --------------------- | ------------------------------------------------------ |
| 400              | Bad Request           | Eksik veya geçersiz bilgi gönderildi.                  |
| 401              | Unauthorized          | Kullanıcının kimlik doğrulaması gerekli veya geçersiz. |
| 403              | Forbidden             | Kullanıcının işlemi yapma yetkisi yok.                 |
| 404              | Not Found             | İstenen sipariş bulunamadı.                            |
| 500              | Internal Server Error | Sunucu tarafında beklenmeyen hata oluştu.              |

## 3. Hata Response Örnekleri

### 400 — Bad Request

Zorunlu bir alan gönderilmediğinde:

```json id="9d6k2f"
{
  "errorCode": "INVALID_REQUEST",
  "message": "productId is required"
}
```

### 404 — Not Found

Sipariş bulunamadığında:

```json id="7z4x1m"
{
  "errorCode": "ORDER_NOT_FOUND",
  "message": "Order not found"
}
```

### 401 — Unauthorized

Kimlik doğrulama başarısız olduğunda:

```json id="v5r8q2"
{
  "errorCode": "UNAUTHORIZED",
  "message": "Authentication is required"
}
```

## 4. Hata Response Standardı

Hataların mümkün olduğunca standart bir yapıda dönmesi beklenmektedir.

Örnek:

```json id="k3p8sd"
{
  "errorCode": "ERROR_CODE",
  "message": "Error description"
}
```

Bu yapı sayesinde frontend ve test ekipleri hataları daha kolay anlayabilir ve yönetebilir.

## 5. BA Açısından Hata Analizi

BA'nın hata yönetiminde şu soruları netleştirmemiz gerekir; 

* Hangi durumda hata oluşur?
* Hangi HTTP status code dönmelidir?
* Kullanıcıya veya sisteme hangi mesaj gösterilmelidir?
* Hata response'u hangi formatta olmalıdır?
* İşlem hata aldığında veri kaydedilmeli midir?

## 6. Örnek

**Senaryo:** Kullanıcı olmayan bir siparişi görüntülemek istiyor.

```text id="2m6r8a"
GET /orders/9999
        ↓
Order bulunamadı
        ↓
404 Not Found
        ↓
{
  "errorCode": "ORDER_NOT_FOUND",
  "message": "Order not found"
}
```

Bu şekilde hata davranışı hem geliştirici hem de test ekibi için açık hale gelir.

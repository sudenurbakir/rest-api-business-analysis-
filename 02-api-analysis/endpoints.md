# API Endpoints

## 1. Endpoint Listesi

| ID     | Method | Endpoint                   | Açıklama                       |
| ------ | ------ | -------------------------- | ------------------------------ |
| API-01 | POST   | `/orders`                  | Yeni sipariş oluşturur.        |
| API-02 | GET    | `/orders/{orderId}`        | Belirli bir siparişi getirir.  |
| API-03 | PUT    | `/orders/{orderId}`        | Sipariş bilgilerini günceller. |
| API-04 | GET    | `/orders/{orderId}/status` | Sipariş durumunu getirir.      |
| API-05 | DELETE | `/orders/{orderId}`        | Siparişi iptal eder.           |

## 2. Endpoint Detayları

### API-01 — Create Order

**Method:** `POST`

**Endpoint:**

```text
/orders
```

**Amaç:** Yeni sipariş oluşturmak.

---

### API-02 — Get Order

**Method:** `GET`

**Endpoint:**

```text
/orders/{orderId}
```

**Amaç:** Belirli bir siparişin bilgilerini görüntülemek.

Örnek:

```text
GET /orders/1001
```

---

### API-03 — Update Order

**Method:** `PUT`

**Endpoint:**

```text
/orders/{orderId}
```

**Amaç:** Mevcut sipariş bilgilerinin güncellenmesini sağlamak.

---

### API-04 — Get Order Status

**Method:** `GET`

**Endpoint:**

```text
/orders/{orderId}/status
```

**Amaç:** Siparişin mevcut durumunu görüntülemek.

Örnek response:

```json
{
  "orderId": 1001,
  "status": "Shipped"
}
```

---

### API-05 — Cancel Order

**Method:** `DELETE`

**Endpoint:**

```text
/orders/{orderId}
```

**Amaç:** Siparişin iptal edilmesini sağlamak.

> Not: Gerçek sistemlerde `DELETE` her zaman fiziksel kayıt silme anlamına gelmez. Sipariş gibi iş kayıtlarında işlem, kaydı silmek yerine "Cancelled" durumuna almak şeklinde tasarlanabilir.

## 3. BA Açısından Endpoint Analizi

Bir BA endpoint tanımlarken temel olarak şunları netleştirmeliyiz;

* Hangi işlem yapılacak?
* Hangi HTTP method kullanılacak?
* Hangi bilgiler gönderilecek?
* Hangi bilgiler dönecek?
* Başarılı işlem sonucu ne olacak?
* Hata durumunda ne olacak?

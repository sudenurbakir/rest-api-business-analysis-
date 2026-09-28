# Business Rules

## 1. Amaç

Bu doküman, sipariş işlemlerinde uygulanacak temel iş kurallarını tanımlar.

## 2. İş Kuralları

| ID    | Business Rule                                                            |
| ----- | ------------------------------------------------------------------------ |
| BR-01 | Sipariş oluşturulurken müşteri, ürün ve adet bilgileri zorunludur.       |
| BR-02 | Her sipariş benzersiz bir Order ID'ye sahip olmalıdır.                   |
| BR-03 | Sipariş adedi sıfırdan büyük bir tam sayı olmalıdır.                     |
| BR-04 | Sipariş yalnızca geçerli bir müşteriye ait olmalıdır.                    |
| BR-05 | Sipariş oluşturulduğunda başlangıç durumu Pending olmalıdır.             |
| BR-06 | Sipariş bilgileri yalnızca izin verilen durumlarda güncellenebilmelidir. |
| BR-07 | Sipariş yalnızca geçerli bir Order ID ile görüntülenebilmelidir.         |
| BR-08 | Pending durumundaki sipariş Confirmed durumuna geçirilebilir.            |
| BR-09 | Confirmed durumundaki sipariş Shipped durumuna geçirilebilir.            |
| BR-10 | Shipped durumundaki sipariş Delivered durumuna geçirilebilir.            |
| BR-11 | Pending veya Confirmed durumundaki sipariş iptal edilebilir.             |
| BR-12 | İptal edilen sipariş yeniden işleme alınmamalıdır.                       |
| BR-13 | Bulunamayan siparişler için 404 Not Found hatası döndürülmelidir.        |
| BR-14 | Eksik veya geçersiz isteklerde 400 Bad Request hatası döndürülmelidir.   |

## 3. Sipariş Durum Kuralları

```text
Pending
   ├── Confirmed
   │      ├── Shipped
   │      │      └── Delivered
   │      └── Cancelled
   └── Cancelled
```

## 4. BA Notu

Business Rule, sistemin hangi koşullarda nasıl davranacağını belirler.

Örneğin, sipariş adedinin sıfırdan büyük olması bir iş kuralıdır. Bu kural, geliştiricinin uygulayacağı ve test ekibinin doğrulayacağı açık bir beklenti oluşturur.

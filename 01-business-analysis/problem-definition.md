# Problem Definition

## 1. Proje Tanımı

Bu proje, bir e-ticaret sisteminde sipariş işlemlerinin API üzerinden yönetilmesini konu alan başlangıç seviyesinde bir **Business Analysis** çalışmasıdır.

Amaç, kullanıcı tarafından oluşturulan sipariş bilgilerinin sistemler arasında güvenli ve standart bir şekilde iletilmesini sağlamaktır.

## 2. Problem

E-ticaret sisteminde sipariş işlemlerinin farklı sistemler arasında manuel veya standart olmayan yöntemlerle aktarılması;

* Sipariş bilgilerinin eksik iletilmesine,
* Veri tutarsızlıklarına,
* Sipariş durumunun takip edilememesine,
* Sistemler arasında iletişim problemlerine

neden olabilir.

Bu nedenle sipariş işlemlerinin belirli kurallar doğrultusunda bir **REST API** üzerinden yönetilmesine ihtiyaç vardır.

## 3. Çözüm

Sipariş işlemleri için standart API endpoint'leri oluşturulması planlanmaktadır.

API aracılığıyla:

* Sipariş oluşturulabilecek,
* Sipariş bilgileri görüntülenebilecek,
* Sipariş bilgileri güncellenebilecek,
* Sipariş durumu takip edilebilecek.

## 4. Proje Amaçları

* Sistemler arasında standart veri iletişimi sağlamak.
* Sipariş bilgilerinin doğru şekilde aktarılmasını sağlamak.
* Sipariş işlemlerini merkezi olarak yönetmek.
* Hatalı veya eksik istekleri kontrol etmek.
* API işlemlerinin test edilebilir olmasını sağlamak.

## 5. Proje Kapsamı

### Kapsam Dahilinde

* Sipariş oluşturma
* Sipariş görüntüleme
* Sipariş güncelleme
* Sipariş durumu
* API request/response yapısı
* Hata yönetimi
* API test senaryoları
* UAT

### Kapsam Dışında

* Ödeme işlemleri
* Kargo entegrasyonu
* Stok yönetimi
* Kullanıcı arayüzü tasarımı
* Gerçek bir API geliştirilmesi

## 6. Başarı Kriterleri

Proje sonunda:

* Sipariş işlemlerinin API üzerinden nasıl gerçekleştirileceği tanımlanmış olmalı.
* Request ve response yapıları dokümante edilmiş olmalı.
* API kuralları belirlenmiş olmalı.
* Hata durumları tanımlanmış olmalı.
* Temel API test senaryoları hazırlanmış olmalı.

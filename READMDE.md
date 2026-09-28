# REST API Business Analysis

Bu proje, bir e-ticaret sisteminde sipariş işlemlerinin **REST API** üzerinden yönetilmesini konu alan başlangıç seviyesinde bir **Business Analysis** çalışmasıdır.

Projenin amacı, sipariş sürecinin iş gereksinimlerini ve API davranışlarını analiz ederek geliştirici ve test ekiplerinin kullanabileceği temel dokümantasyonu oluşturmaktır.

## Proje Senaryosu

Bir müşteri e-ticaret sistemi üzerinden sipariş oluşturur.

```text 
Customer
   ↓
Frontend
   ↓
REST API
   ↓
Order System
```

API üzerinden temel olarak:

* Sipariş oluşturma
* Sipariş görüntüleme
* Sipariş güncelleme
* Sipariş durumu görüntüleme
* Sipariş iptali

işlemleri gerçekleştirilmektedir.

## Proje Kapsamı

* Business Requirements
* Functional Requirements
* Stakeholder Analysis
* Business Rules
* REST API Analysis
* API Endpoints
* Request / Response
* Error Handling
* User Stories
* Acceptance Criteria
* API Test Scenarios
* UAT
* Requirements Traceability Matrix

## Proje Yapısı

```text 
rest-api-business-analysis/
│
├── README.md
│
├── 01-business-analysis/
│   ├── problem-definition.md
│   ├── stakeholders.md
│   ├── business-requirements.md
│   └── functional-requirements.md
│
├── 02-api-analysis/
│   ├── api-overview.md
│   ├── endpoints.md
│   ├── request-response.md
│   └── error-handling.md
│
├── 03-requirements/
│   ├── business-rules.md
│   ├── user-stories.md
│   └── acceptance-criteria.md
│
├── 04-testing/
│   ├── api-test-scenarios.md
│   └── uat.md
│
└── 05-traceability/
    └── requirements-traceability-matrix.md
```

## Örnek API Endpoint'leri

| Method | Endpoint                   | Amaç                         |
| ------ | -------------------------- | ---------------------------- |
| POST   | `/orders`                  | Sipariş oluşturma            |
| GET    | `/orders/{orderId}`        | Sipariş görüntüleme          |
| PUT    | `/orders/{orderId}`        | Sipariş güncelleme           |
| GET    | `/orders/{orderId}/status` | Sipariş durumunu görüntüleme |
| DELETE | `/orders/{orderId}`        | Sipariş iptali               |

## Öğrenilen BA Konuları

Bu proje ile bir Business Analyst'in API süreçlerinde:

* Gereksinim toplama
* API davranışlarını tanımlama
* Request / Response analizi
* İş kuralları oluşturma
* Acceptance Criteria yazma
* API test senaryoları hazırlama
* UAT planlama
* Gereksinimlerin izlenebilirliğini sağlama

konularında nasıl çalışabileceğini konusunda kendimi geliştirmek için yapılmıştır.

## Not

Bu proje eğitim ve portföy amacıyla hazırlanmış örnek bir çalışmadır. Gerçek müşteri veya şirket verisi kullanılmamıştır.

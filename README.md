# E-Commerce Analytics Platform

Müşteri, satıcı ve yönetici rollerine sahip bir e-ticaret uygulaması. CSE 214 Advanced Application Development dersi için Yaren Erişen ve Elif Polatdemir tarafından geliştirildi.

> Bu proje bir ders ve demo çalışmasıdır, canlı kullanım için tasarlanmamıştır.

## Özellikler

- Ürün listeleme, kategori filtreleme ve sepet
- Stripe test modu ile ödeme
- JWT ile kimlik doğrulama ve rol bazlı yetkilendirme
- Yönetici, satıcı ve müşteri panelleri
- Sipariş ve mağaza yönetimi
- Veritabanı üzerinde doğal dille analiz yapan Gemini destekli sohbet asistanı (Text2SQL)
- Grafiklerle satış ve sipariş analizi

## Teknolojiler

| Katman | Teknoloji |
| --- | --- |
| Backend | Java 21, Spring Boot 3.2, Spring Security, JPA |
| Frontend | Angular 21, Chart.js, Plotly, Stripe.js |
| Veritabanı | MariaDB 10.4 |
| AI servisi | Python, FastAPI, LangChain, Gemini |

## Çalıştırma

Gereksinimler: JDK 21+, Node.js 20.19+, MariaDB ve Stripe ile Gemini API anahtarları.

Örnek veri seti repoda yer almaz. Uygulama, `ecommerce_analytics` adlı dolu bir veritabanı bekler.

1. Ayar dosyasını oluşturun ve anahtarları doldurun:

```bash
cp src/main/resources/application.properties.example src/main/resources/application.properties
```

2. Backend'i başlatın (`http://localhost:8081`):

```bash
./mvnw spring-boot:run
```

3. Frontend'i başlatın (`http://localhost:4200`):

```bash
cd ecommerce/frontend
npm install
npm start
```

## Proje yapısı

```text
src/                  Spring Boot backend
ecommerce/frontend/   Angular uygulaması
ecommerce/ai-agent/   FastAPI ve LangChain servisi (deneysel, arayüze bağlı değil)
```

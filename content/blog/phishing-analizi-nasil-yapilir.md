---
title: "Phishing E-postalarini Nasil Analiz Ederiz?"
date: 2024-02-01
tags: ["phishing", "blue team", "e-posta guvenligi"]
categories: ["Blog"]
description: "Gercek bir phishing ornegi uzerinden adim adim analiz teknikleri"
---

Phishing saldirilarinin %90'i e-posta ile baslar. Bu yazida gercek bir phishing orneği uzerinden header analizi, URL incelemesi ve IOC cikarma tekniklerini anlatacagim.

## E-posta Header Analizi

Phishing e-postasini aldiktan sonra ilk adim header'i incelemektir.

```
Received: from mail.evil-domain.ru ([192.168.1.1])
From: "PayPal Security" <security@paypa1.com>
Reply-To: attacker@gmail.com
```

Dikkat edilecek noktalar:

- **From** ile **Reply-To** farkliysa suphelenin
- **Received** header'indaki IP adresi ile gonderen alan adi eslesmiyor mu?
- SPF, DKIM, DMARC kontrollerini yap

## URL Analizi

Phishing URL'leri genellikle su ozelliklere sahiptir:

1. Marka adinin yanina ekstra kelime eklenmis: `paypal-security-alert.ru`
2. Tire ile birlestirilmis: `login-paypal-secure.com`  
3. Subdomain hilesi: `paypal.evil.com`
4. IP adresi kullaniyor: `http://192.168.1.1/paypal/login`

## IOC Cikarma

Analiz sonucunda cikarmaniz gereken Indicators of Compromise:

- Gonderen IP adresi
- Kullanilan domain
- URL pattern'leri
- E-posta konusu ve icerik benzerlikleri

## Kullanilan Araclar

- **VirusTotal** — URL ve dosya analizi
- **MXToolbox** — SPF/DKIM/DMARC kontrolu
- **URLScan.io** — URL guvenli tarama
- **PhishTool** — Otomatik phishing analizi

---

Phishing analizi pratik yapmak icin [Phishing Analyzer](/tools/phishing-analyzer.html) aracimi kullanabilirsiniz.

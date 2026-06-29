---
title: "CTF'e Nasil Baslanir? Yeni Baslayanlara Rehber"
date: 2024-03-01
tags: ["CTF", "baslangic", "ogrenme"]
categories: ["Blog"]
description: "Capture The Flag yarismalarina nasil girilir, hangi platformlar kullanilir"
---

CTF (Capture The Flag) yarismalari siber guvenlik ogrenmenin en eglenceli yollarindan biri. Bu yazida nereden baslayacaginizi anlatayyim.

## CTF Kategorileri

| Kategori | Aciklama |
|----------|----------|
| Web | SQL injection, XSS, LFI/RFI |
| Crypto | Sifreleme algoritmalarini kirma |
| Forensics | Dijital adli analiz |
| Pwn / Binary | Buffer overflow, ROP chain |
| Reverse Engineering | Zarali yazilim ve binary analizi |
| OSINT | Acik kaynak istihbarat |
| Steganography | Gizli mesaj bulmaca |

## Baslangic Platformlari

### TryHackMe
Yeni baslayanlar icin en iyi platform. Guided learning path'leri var, her seyi adim adim ogretir.

### PicoCTF
Carnegie Mellon universitesinin uretigi, baslangic seviyesi CTF arsivi. Binlerce cozulmus soru var.

### HackTheBox
Orta-ileri seviye. Gercek saldiri senaryolari. Bazi makineleri cozmek icin gerçekten iyi olmak lazim.

## Ilk CTF Icin Onerim

1. TryHackMe'de "Complete Beginner" path'ini tamamla
2. PicoCTF arsivinden Crypto ve Forensics sorularini coz
3. Linux komut satirini ogren (en az 2 hafta)
4. Python ile basit scriptler yazmay ogren
5. HackTheBox'ta "Starting Point" makineleriyle basla

## Gerekli Araclar

```bash
# Temel CTF araclari
sudo apt install nmap gobuster nikto john hashcat
pip install pwntools requests
```

---

CTF writeup'larimi [Write-ups](/writeups/) bolumunden takip edebilirsiniz.

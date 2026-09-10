# 🎯 Raspberry Pi 5 Üzerinde Gerçek Zamanlı Dost-Düşman Hedef Tespit ve Lazer Takip Sistemi

Bu proje, **Raspberry Pi 5** donanımı üzerinde çalışan; derin öğrenme tabanlı nesne tespiti, gerçek zamanlı görüntü işleme ve 2 eksenli mekanik pan-tilt yönlendirmesini bir araya getiren gömülü bir hava hedefi tespit ve takip sistemidir[cite: 1].

---

## 📌 Proje Özeti

Sistem, hava sahasındaki hedefleri (örneğin drone ve kuş) kamera aracılığıyla yakalayıp dost-düşman sınıflandırması yapar[cite: 1]. Düşman veya hedef olarak tanımlanan nesnenin merkez koordinatlarını anlık olarak hesaplayarak 2 eksenli servo motor mekanizmasıyla lazer işaretleyiciyi hedefe kilitler[cite: 1]. Eş zamanlı olarak sistem durumu ve hedef telemetri verilerini MQTT protokolü üzerinden uzak istasyona aktarır[cite: 1].

---

## 🛠️ Kullanılan Teknolojiler ve Donanım Bileşenleri

* **İşlemci Kartı:** Raspberry Pi 5 (Gömülü yapay zekâ ve kontrol birimi)[cite: 1].
* **Derin Öğrenme Modeli:** YOLO (Hedef tespit ve sınıflandırma)[cite: 1].
* **Uçta Çıkarım (Edge Inference):** NCNN kütüphanesi (ARM mimarisinde yüksek FPS ve optimize çalışma için)[cite: 1].
* **Görüntü İşleme:** OpenCV (Kamera akışı okuma, görüntü filtreleme, merkez koordinat hesaplama)[cite: 1].
* **Yönlendirme & İşaretleme:** 2 Eksenli Pan-Tilt Servo Mekanizması ve Lazer Modülü[cite: 1].
* **IoT & Haberleşme:** MQTT Protokolü (Gerçek zamanlı koordinat ve durum telemetrisi iletimi)[cite: 1].
* **Yazılım Dili & Ortam:** Python, Linux (Raspberry Pi OS)[cite: 1].

---
## ⚙️ Mühendislik Süreci ve Öne Çıkan Özellikler

* **NCNN ile Uçta Optimizasyon:** Model ağırlıkları optimize edilerek Raspberry Pi 5'in ARM Cortex-A76 işlemcisinde harici bir GPU gerekmeden gerçek zamanlı çıkarım hızlarına ulaştırılmıştır[cite: 1].
* **Kapalı Çevrim Mekanik Takip:** Hedefin görüntü merkezine olan piksel farkı ($X$ ve $Y$ ekseninde) hesaplanarak servo motorlara uygun PWM açı komutları üretilmiş ve lazer hedefe hizalanmıştır[cite: 1].
* **Telemetri ve Durum Bildirimi:** Hedef kilitlenme durumu, güven skoru ve piksel koordinatları anlık olarak MQTT broker üzerinden yayınlanmıştır[cite: 1].

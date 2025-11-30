# SAVAŞ ARACI KART OYUNU

## 👥 Proje Sahipleri
* Ömer Faruk Toycu (@omertoycu)
* Ali Berke Erenler (@aliberkerenler)

---

## 🎯 Proje Amacı
Bu proje, Java'da Nesne Yönelimli Programlama (OOP) prensipleri kullanılarak geliştirilmiş, **Kullanıcı** ve **Bilgisayar** arasında oynanan 5 turluk bir kart savaş oyunudur. Oyun, kara, hava ve deniz araçları arasındaki sınıf tabanlı avantaj mekaniklerini uygular.

## 🛠️ Teknolojiler ve Kütüphaneler
* **Dil:** Java
* **OOP Kavramları:** Kalıtım, Soyut Sınıflar, `Cloneable` Arayüzü (Kart Klonlama).

---

## 🏗️ Sınıf Hiyerarşisi (Kalıtım)
Oyunun kart sistemi, katı bir kalıtım yapısına dayanmaktadır:
1.  **`SavasAraci` (Soyut):** Tüm kartların temelini oluşturur.
2.  **`KaraAraci`, `HavaAraci`, `DenizAraci` (Soyut):** Savaş araçlarının ana tiplerini tanımlar.
3.  **Somut Kartlar:** `Ucak`, `Siha`, `Obus`, `KFS`, `Firkateyn`, `Sida`.
4.  **`Oyuncu`:** Oyuncu verilerini (skor, kart listesi) ve kart seçme/çıkarma işlevlerini yönetir.

## ✨ Temel Özellikler
* **Sınıf Avantajları:** Kartlar, karşılaştıkları rakibin tipine göre ek vuruş avantajı kazanır (örneğin: `KaraAraci`, `DenizAraci`'na karşı ek vuruş avantajı).
* **Kilitli Kart Sistemi:** Oyun başında kilitli olan **`Siha`**, **`KFS`** ve **`Sida`** kartları, bir oyuncunun skoru **20 puana** ulaştığında o oyuncunun kart havuzuna eklenir.
* **Çift Çıktı (TeeOutputStream):** Oyunun tüm logları, özel olarak tasarlanmış `TeeOutputStream` sınıfı sayesinde hem konsola hem de **`savas_sim.txt`** adlı dosyaya eşzamanlı olarak kaydedilir.
* **Puanlama:** Elenen kart için kazanan oyuncuya, kartın seviye puanı artı **10 puan** verilir.

---

## 🚀 Çalıştırma Talimatları
1. Tüm `.java` kaynak kodlarını derleyin.
2. `Oyun.java` sınıfını ana sınıf olarak çalıştırın.
3. Oyun, konsol üzerinden kullanıcıdan kart seçimi için girdi isteyecektir.

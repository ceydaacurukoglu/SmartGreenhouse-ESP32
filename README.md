# 🌱 Akıllı Sera Projesi (ESP32 - Wokwi Simülasyonu)

Bu proje, **ESP32 tabanlı bir akıllı sera kontrol sistemi** simülasyonudur.  
Wokwi platformu üzerinde geliştirilmiştir ve temel amacı, seralarda sıcaklık, nem ve ışık gibi çevresel koşulları sensörlerle izleyip aktüatörler yardımıyla otomatik kontrol etmektir.  

🔗 Projeyi doğrudan incelemek için: [Wokwi Simülasyon Linki](https://wokwi.com/projects/428389643677696001)

---

## 🎯 Projenin Amacı
Geleneksel tarımda çevresel koşulların sürekli takip edilmesi zordur. Bu proje ile:  
- Seradaki **sıcaklık ve nem değerleri** sürekli takip edilebilir.  
- Kritik eşik değerlerinde **fan, pompa ve LED ışıklar otomatik çalışır**.  
- Çiftçiye veya kullanıcıya anlık değerler **LCD ekran** üzerinden gösterilir.  
- Böylece verimlilik artar ve bitkiler için daha uygun bir mikro-iklim sağlanır.  

---

## ⚡ Özellikler
- 🌡️ **Sıcaklık ve Nem Ölçümü:** DHT22 sensörü ile ölçülür.  
- 💨 **Fan Kontrolü:** Sıcaklık eşik değeri aşıldığında fan devreye girer.  
- 💧 **Sulama Pompası:** Nem oranı düştüğünde otomatik çalışır.  
- 💡 **Aydınlatma Kontrolü:** LDR sensörüyle ortam ışığı ölçülür, yetersizse LED aydınlatma açılır.  
- 📟 **LCD Ekran:** Sensör değerlerini ve sistem durumunu anlık olarak gösterir.  
- 🔔 **Buzzer:** Kritik durumlarda kullanıcıyı uyarır.  

---

## 🛠️ Kullanılan Donanım / Yazılım
- **ESP32** (mikrodenetleyici)  
- **DHT22** (sıcaklık ve nem sensörü)  
- **LDR** (ışık sensörü)  
- **Fan** 
- **Pompa**
- **LED** 
- **LCD Ekran** (bilgilendirme için)
- **MQ-135** (Hava sensörü)
- **Wokwi Online Simulator**

## ✨ Projenin Özeti
Bu proje kapsamında geliştirilen akıllı sera sistemi, temel çevresel parametreleri izleyerek bitki gelişimini destekleyen otomatik ve kullanıcı dostu bir çözüm sunmaktadır. Sistem; sıcaklık, nem, ışık şiddeti ve CO₂ seviyelerini algılayarak fan, pompa ve aydınlatma gibi donanımları otomatik ya da manuel olarak kontrol edebilmekte, ayrıca LCD ekran ve buzzer aracılığıyla kullanıcıyı bilgilendirmektedir.

LDR sensörü sayesinde ortamdaki ışık durumu analiz edilmekte ve gün ışığı yetersizse LED aydınlatma devreye girmektedir. MQ-135 sensörü ile CO₂ seviyesi takip edilerek bitkilerin sağlıklı fotosentez yapabilmesi için gerekli havalandırma sağlanmakta, aşırı düşük CO₂ seviyelerinde sistem sesli uyarı vermektedir. DHT22 sensörü ile sıcaklık ve nem değerleri okunarak, bu değerlere bağlı olarak sulama pompası ve fan kontrolü gerçekleştirilmiştir. Tüm bu bilgiler I2C tabanlı LCD ekran üzerinde anlık olarak görüntülenmekte, bu da sistemin şeffaflığını ve kullanıcı etkileşimini artırmaktadır.

Sistem aynı zamanda düğmeler ile manuel müdahaleye izin vererek kullanıcının istediği zaman fan ya da pompayı devreye alabilmesini sağlamaktadır. Bu özellik, dış koşullara göre esnek kullanım imkânı tanımaktadır.

Sonuç olarak geliştirilen akıllı sera sistemi; çevre koşullarına duyarlı, otomasyon kabiliyetine sahip ve gerektiğinde kullanıcı müdahalesine açık bir yapıya sahiptir. Bu proje ile hem bitki sağlığı korunmakta hem de kullanıcıya zaman ve enerji açısından önemli avantajlar sunulmaktadır. Geliştirmeye açık olan sistem, sensör sayısı artırılarak veya uzaktan kontrol imkânı eklenerek daha ileri seviyelere taşınabilir.

---

## 📂 Proje Dosyaları
- `sketch.ino` → ESP32 için yazılan ana program kodu  
- `diagram.json` → Devre şemasını tanımlayan Wokwi dosyası  
- `wokwi-project.txt` → Wokwi proje ayarları  
- `libraries.txt` → Kütüphaneler
---

## 🖼️ Devre Şeması
Proje devre şeması Wokwi üzerinde oluşturulmuştur. 
<img width="834" height="666" alt="mikro" src="https://github.com/user-attachments/assets/3b620167-846a-41c0-94ce-41d93b7547c8" />


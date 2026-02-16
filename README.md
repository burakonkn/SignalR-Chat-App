# 💬 Chat | SignalR Real-Time Chat Application

Bu proje, **.NET Core SignalR** teknolojisi kullanılarak geliştirilmiş, web tabanlı ve gerçek zamanlı (real-time) bir sohbet uygulamasıdır. Mesajlaşma mantığı sunucu tarafında **In-Memory (Static Lists)** üzerinden yönetilmektedir.

[Image of SignalR Hub architecture diagram]

## 🚀 Öne Çıkan Özellikler

* **Gerçek Zamanlı İletişim:** WebSocket protokolü üzerinden anlık mesaj gönderimi ve alımı.
* **Grup/Oda Yönetimi:** Kullanıcıların özel odalar oluşturabilmesi ve bu odalara katılarak grup içi mesajlaşabilmesi.
* **Özel Mesajlaşma:** Listedeki belirli bir kullanıcıyı seçerek birebir (private) iletişim kurma imkanı.
* **Dinamik Kullanıcı Listesi:** Sisteme giren veya çıkan kullanıcıların anlık olarak tüm istemcilerde güncellenmesi.
* **Modern Arayüz:** Bootstrap 5 ile desteklenmiş, kullanıcı dostu ve duyarlı (responsive) UI.

## 🛠️ Kullanılan Teknolojiler

* **Backend:** ASP.NET Core 8.0, SignalR Hubs
* **Frontend:** HTML5, CSS3, JavaScript (jQuery), Bootstrap 5
* **Veri Yönetimi:** Static Classes & Lists (In-Memory Persistence)

## 📌 Mimari Yapı ve Klasörleme

Uygulama, Client-Server modelini takip eder ve kod organizasyonu için şu yapı kullanılmıştır:

* **/src/SignalRChatServerExample:** Hub yönetimi ve Business Logic'in bulunduğu backend projesi.
* **/src/SignalRChatClientExample:** HTML, CSS ve JavaScript dosyalarından oluşan istemci tarafı.

### Önemli Metotlar:
- **`GetNickName`**: Kullanıcıyı sisteme dahil eder ve diğer aktif kullanıcılara bildirir.
- **`SendMessageAsync`**: Hedef bazlı (kişiye özel) veya genel mesaj iletimini sağlar.
- **`AddGroup` & `AddClientToGroup`**: Dinamik grup oluşturma ve kullanıcıları odalara dahil etme işlevlerini yönetir.

## 🔧 Kurulum ve Çalıştırma

1.  **Projeyi Clone'layın:**
    ```bash
    git clone [https://github.com/burakonkn/SignalR-Chat-App.git](https://github.com/burakonkn/SignalR-Chat-App.git)
    ```
2.  **Backend'i Başlatın:** `SignalRChatServerExample.sln` dosyasını Visual Studio veya JetBrains Rider ile açıp çalıştırın. (Varsayılan: `https://localhost:7111`)
3.  **Frontend'i Açın:** `chat.html` dosyasını herhangi bir modern tarayıcıda açın.
4.  **CORS Ayarları:** Eğer frontend farklı bir adreste çalışacaksa `Program.cs` içindeki CORS politikasını güncellediğinizden emin olun.

## 🔜 Gelecek Geliştirmeler (Roadmap)

- [ ] Mesajların **PostgreSQL** veya **MSSQL** üzerine kaydedilmesi.
- [ ] Frontend tarafının **React** veya **Vue** ile modernize edilmesi.
- [ ] Mesajların uçtan uca şifrelenmesi.

---

### 👨‍💻 Hakkımda

**Burak Onkun** *Bilgisayar Programcılığı Öğrencisi*

* 📍 Bursa, Türkiye
* [LinkedIn Profilim](https://linkedin.com/in/burakonkn)
* [Diğer Projelerim](https://github.com/burakonkn)

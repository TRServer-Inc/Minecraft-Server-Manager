🎮 MC Server Manager - Ultra Core v1.2
MC Server Manager, hem Minecraft Java hem de Bedrock sunucularını tek bir panelden, ultra düşük kaynak tüketimi ve modern bir web arayüzü (HTML5/CSS3/Tailwind) ile yönetmenizi sağlayan, C# WinForms tabanlı hibrit bir sunucu yönetim panelidir.

Masaüstünün gücünü, modern web teknolojilerinin şıklığıyla birleştirir!

✨ Öne Çıkan Özellikler
🚀 Çift Platform Desteği: Tek tıkla Minecraft Java (Vanilla, PaperMC, Purpur) veya Bedrock (Dedicated, PocketMine-MP) sunucuları kurun.

📦 Akıllı Bağımlılık Yönetimi: Sistemde Java yoksa otomatik olarak algılar ve arka planda resmi OpenJDK 21 kurulumunu gerçekleştirir.

📊 Dinamik RAM Yönetimi: Sunucuyu başlatmadan önce panel üzerinden ne kadar RAM (1GB - 12GB+) atanacağını dinamik olarak seçin.

🌐 GeyserMC Entegrasyonu: Java sunucularınıza Bedrock oyuncularının da katılabilmesi için tek tıkla Geyser-Spigot veya Geyser-Velocity eklentilerini otomatik indirin.

💬 Canlı Konsol & Oyuncu Takibi: Sunucu loglarını anlık olarak panelden izleyin, komut gönderin ve oyuna giren/çıkan oyuncuları canlı listeden takip edin.

📝 Gelişmiş Konfigürasyon Editörü: server.properties dosyasını klasörler arasında kaybolmadan direkt panel üzerinden okuyun, düzenleyin ve kaydedin.

🔒 Ultra Stabilite Modu: C# arka plan thread'leri ile WebView2 arayüzü arasındaki iletişim özel kilitlenme koruması (BeginInvoke mimarisi) ile korunur; çökme veya donma yaşanmaz.

📂 Klasör Yapısı
Projenin sorunsuz çalışması için yayımlanan (Publish) klasör düzeninin aşağıdaki gibi olması gerekmektedir:

📁 MC Server Manager/
│
├── 📁 Arayuz/                 # Web arayüz bileşenleri (Kritik Klasör)
│   ├── 📄 index.html          # Ana panel yapısı
│   ├── 📄 style.css           # Özel temalandırma ve scrollbar ayarları
│   └── 📄 app.js              # C# ile köprü kuran JavaScript kodları
│
├── 📄 MC Server Manager.exe   # Ana çalıştırılabilir uygulama
├── 📄 WebView2Loader.dll      # Tarayıcı motoru yükleyicisi (Kritik Dosya)
└── 📁 runtimes/               # WebView2 için gerekli sistem mimari dosyaları

⚠️ NOT: Temiz bir görünüm için yayımlama sonrası kalabalık yapan .xml ve .pdb uzantılı dosyalar güvenle silinmiştir. Arayuz klasörü ve WebView2Loader.dll dosyalarına kesinlikle dokunulmamalıdır.

🛠️ Kurulum ve Çalıştırma
Projeyi bilgisayarınıza indirin veya Visual Studio ile derleyin (Publish).

Derlenen klasörün içinde Arayuz adında bir klasör oluşturup index.html, style.css ve app.js dosyalarını bu klasörün içine taşıyın.

MC Server Manager.exe dosyasını çift tıklayarak çalıştırın.

Panel açıldığında sisteminizdeki Java durumu otomatik kontrol edilecek ve eksikse kurulacaktır.

Sunucularınız varsayılan olarak depolama alanınızın durumuna göre otomatik olarak D:\MCEngineServers veya C:\MCEngineServers dizini altında oluşturulur.

💻 Kullanılan Teknolojiler
Backend: C# (.NET WinForms), Microsoft.Web.WebView2, System.Text.Json, HttpClient

Frontend: HTML5, Tailwind CSS, FontAwesome v6, Vanilla JavaScript

Veri Köprüsü: Asenkron PostWebMessageAsJson ve WebMessageReceived çift yönlü haberleşme hattı.

🤝 Katkıda Bulunma
Bu projeyi fork edin (git fork).

Yeni bir özellik dalı (feature branch) açın (git checkout -b yeni-ozellik).

Değişikliklerinizi commit edin (git commit -am 'Yeni özellik eklendi').

Dalınızı push edin (git push origin yeni-ozellik).

Bir Pull Request (Çekme İsteği) oluşturun.

📄 Lisans
Bu proje MIT Lisansı ile lisanslanmıştır. Detaylar için lisans dosyasına göz atabilirsiniz.

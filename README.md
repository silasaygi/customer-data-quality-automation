# Müşteri Veri Kalitesi ve Geri Bildirim Otomasyonu

Bu proje, Google Sheets'teki verileri yerel bir LLM (Ollama) ile analiz ederek, veri kalitesini otonom bir şekilde yöneten bir n8n iş akışıdır.

## Sistem Özellikleri
- **AI Analizi:** Ollama üzerinden gelen verileri inceleyerek hata tespiti yapar.
- **Kural Tabanlı Doğrulama:** JavaScript kodları ile hataları sınıflandırır.
- **Geri Bildirim Döngüsü:** Hatalı veriler için Telegram üzerinden otomatik bildirim gönderir.
- **Self-Healing:** Cron ile periyodik kontrol yaparak, düzeltilen veriler için teşekkür mesajı gönderir.

## Nasıl Kullanılır?
1. n8n kurulumunuzda "Import from File" seçeneğini kullanarak `data-quality-pipeline.json` dosyasını içe aktarın.
2. Kendi Google Sheets API ve Telegram Bot Token bilgilerinizi ilgili düğümlere tanımlayın.
3. Yerel Ollama kurulumunuzun aktif olduğundan emin olun.

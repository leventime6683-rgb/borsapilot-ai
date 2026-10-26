# BorsaPilot AI v0.3 — GitHub Pages / Samsung Tab S10 FE

Bu sürüm **statik Android PWA** olarak tasarlanmıştır. GitHub Pages ile HTTPS üzerinden açılır; Python/Termux gerekmez. **Canlı BIST verisi, otomatik haber tarama, yapay zekâ servisi, arka plan fiyat alarmı ve gerçek emir yoktur.** Üç DEMO sembolü sentetik fiyat üretir. CSV dosyası yüklenebilir. Veriler cihazın tarayıcısında tutulur.

## GitHub Pages ile yayınlama
1. GitHub hesabında `borsapilot-ai` adlı **public** repo oluştur. (GitHub Free ile Pages kullanımı için public repo gerekir; özel kalmasını istiyorsan özel erişimli barındırma seç.)
2. Bu ZIP içindeki **dosyaları** (üst klasör olmadan) repoya yükle: `index.html`, `app.js`, `sw.js`, `icon.svg`, `manifest.webmanifest`, `.nojekyll`.
3. `Settings → Pages → Build and deployment → Deploy from a branch → main → /(root) → Save`.
4. GitHub Pages adresi genellikle `https://KULLANICI.github.io/borsapilot-ai/` olur. Yayınlandığını GitHub Pages ayarından doğrula.
5. Samsung Chrome ile HTTPS adresini aç. Chrome menüsü → **Ana ekrana ekle / Uygulamayı yükle**.

## Sanal test
- Portföy başlangıcı 125.000 TL; sentetik DEMO_A, DEMO_B, DEMO_C.
- Sanal alış/satış, komisyon, RSI, EMA, ATR, işlem günlüğü ve CSV içe/dışa aktarımı.
- CSV: `date,open,high,low,close,volume` en az 60 satır, tarih artan.
- Haber düğmesi yalnızca resmî web sitelerini yeni sekmede açar; **haberleri otomatik okumaz veya puanlamaz**.
- Demo işlem algoritması gerçek piyasa performansını ölçmez.

## Güvenlik ve mahremiyet
- Banka şifresi, hesap bilgisi veya emir yetkisi istemez.
- Public GitHub repo kaynak kodunu herkese açar. Kişisel veri, API anahtarı, parola yükleme.
- GitHub Pages barındırması kişiye özel giriş kontrolü sağlamaz. Bu sürümde portföy verisi sadece aynı tarayıcıda tutulur; tarayıcı verisi temizlenirse silinir.
- Otomatik haber takibi, lisanslı BIST verisi ve bildirim için sonradan yetkili sunucu/API gerekir.

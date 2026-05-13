# ChoreClick

**Oyunlaştırılmış Ortak Ev İşleri ve Görev Yöneticisi**

ChoreClick, öğrenci evleri, paylaşımlı apartman daireleri ve aileler için ev işleri dağılımında yaşanan adaletsizlik ve tartışmaları kökünden çözen, sıkıcı sorumlulukları rekabetçi ve eğlenceli bir mobil "clicker" oyununa dönüştüren modern bir görev yönetim platformudur.

## Proje Odak Noktaları ve İşleyiş

Sistem, ev içi dinamiklerdeki angarya işleri adil bir puanlama ve ödül sistemiyle sosyalleştirmek üzerine kuruludur:

*   **Oyunlaştırılmış Görev Havuzu:** Ev arkadaşları veya aile üyeleri tarafından görülebilen ortak bir pano oluşturulur. Bulaşık yıkamak, çöpü atmak, alışveriş yapmak gibi her göreve efor/zorluk derecesine göre belirli bir puan (XP) atanır.
*   **Clicker ve Kanıt Mekanizması:** Görevi yapmak isteyen kişi butona basarak işi üzerine alır. Görev tamamlandığında (isteğe bağlı olarak fotoğraf yüklenerek) uygulama üzerinden bildirilir ve evdeki diğer üyelerin onayıyla puanlar hesaba geçer.
*   **Haftalık Liderlik Tablosu (Leaderboard):** Kullanıcıların kazandığı puanlar canlı bir liderlik tablosunda yarışa dönüşür. Haftanın sonunda en çok puanı toplayan kişi, önceden belirlenen haftalık ödülü (örneğin: kahve ısmarlanması, bir sonraki hafta bulaşıktan muafiyet) kazanır.
*   **Tartışmasız Adalet:** "Sen az yaptın, ben çok yaptım" şeklindeki ev içi tartışmalar, herkesin görebildiği şeffaf istatistikler ve oyunlaştırma (gamification) dinamikleri sayesinde eğlenceli bir rekabete bırakır.

## Mimari Yaklaşım ve Teknoloji Yığını

*   **Frontend (Mobil Uygulama):** Flutter veya React Native. Tipik bir "to-do" uygulamasından ziyade, oyun hissi veren; tatmin edici buton tıklama animasyonlarına (haptic feedback), rozetlere ve canlı bir tasarıma sahip çapraz platform bir arayüz.
*   **Backend (API ve İş Mantığı):** Node.js (Express/NestJS) veya Python (FastAPI). Haftalık puan sıfırlamaları (cron jobs), ev/grup (room) yönetimi ve puan hesaplama algoritmalarının koştuğu servis.
*   **Veritabanı ve Gerçek Zamanlılık:** Firebase Realtime Database, Firestore veya Supabase. Evde bir görev tamamlandığında veya eklendiğinde tüm ev arkadaşlarının ekranında anında (gerçek zamanlı) güncellenmesi için.
*   **Bildirim Servisi (Push Notifications):** Firebase Cloud Messaging (FCM) veya OneSignal. "Mutfak temizlendi, onayınız bekleniyor" veya "Haftanın birincisi belli oldu!" gibi sosyal motivasyon tetikleyicileri için.

---

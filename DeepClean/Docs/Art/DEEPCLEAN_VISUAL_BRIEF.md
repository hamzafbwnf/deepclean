# DEEPCLEAN — Görsel çalışma tarifi

Tarih: 5 Eylül 2026. Durum: Kullanıcı eleştirisi sonrası revizyon; görsel yön onaylanmadı. Kanonik GDD: ../DEEPCLEAN_GDD.md (0.7).

**Üretim tercihi:** Kullanıcı limit tüketimi nedeniyle görselleri başka bir yapay zekâya ürettirecek. Bu sohbet ayrıntılı İngilizce istemleri ve referans rollerini hazırlar, gelen sonuçları inceler. Yeni açık talep olmadan burada görsel üretimi yapılmaz. Beğenilen sonuçlar ayrıca kararlaştırılarak GDD'ye alınır.

## Amaç ve ilerleme

1. Görsel tarif: ilk taslak hazır.
2. Dış alan: `DEEPCLEAN_Exterior_A02.png` kullanıcı tarafından GDD'ye hazır bulunmadı. Suda asılı atıklar, nesne çeşitliliği ve fiziksel madencilik/çıkarım kimliği eksik. A01 ve A02 onaylı görsel hedef değildir. Yeni dış üretim istemi: `DEEPCLEAN_EXTERIOR_REVISION_B_PROMPT_EN.md`.
3. Aynı dış alanın temizlenmiş görünümü ve iç alan: dış görsel yön seçildikten sonra hazırlanacak.

İlk üç adımın birlikte tamamlanması GDD 0.8 eşiğidir; taslak üretmek onay anlamına gelmez.

## Korunacaklar

- Tekne: eski konseptlerdeki küçük, mavi boyalı/paslı iş teknesi; açık ahşap güverte, tek kamara, borda ve korkuluk karakteri. Gövde korunurken sondaj/numune çıkarımını anlatacak sınırlı modüler ekipman eklenebilir. Gövdeyi korumak, tekneyi işlevsel olarak değişmeden bırakmak anlamına gelmez. Eklentilerin kesin yerleşimi ve üretime kabulü açıktır.
- Çöpler: renkli içecek kutuları, plastik/cam şişeler, mevcut referanslardaki gündelik ve denizcilik eşyaları. Madencilik anlatısı bunları tek renk cevhere dönüştürmez.
- Yoğunluk: ilk anda çok iş olduğunu gösterir. Okunabilirlik yerleşim, görüş açısı, yerel ışık/biçim ayrımı ve ileride UI desteğiyle sağlanır; genel renk ve nesne çeşitliliğini azaltmak temel çözüm değildir.
- Doğal deniz tabanı korunur. Kum/çamur teknik adları temizlenebilir yabancı maddeleri temsil eder.
- Referans görüntüler modellemeye temel olmuştur. Tekne varyantları arasında uyuşmazlık varsa ilk karede kullanılan varyant kaydedilir; gerçek modelin hangi varyantı izlediği sonradan doğrulanır.

## Önerilen görsel dil

Stilize gerçekçilik: okunabilir şekiller, inandırıcı metal/plastik/ahşap ayrımı, canlı sualtı yaşamı. Subnautica 2 atmosfer ve malzeme hedefidir; birebir araç/UI kopyası hedeflenmez.

Yakın çalışma alanı seçilebilir; uzaklık arttıkça mavi/turkuaz sis şekilleri yumuşatır. Yüzey ışığı ve kostikler formu destekler. Renkli mercanlar ve atıklar korunur; ışık saçma seçili bitki vurgularında sınırlıdır. Nihai renkler henüz onaylanmamıştır.

Tanecikli yabancı birikinti: hacmi miktarı anlatır; ufalanan düzensiz kenar, doğal zeminden farklı yüzey karakteri. Balçık kıvamındaki kir: kalın merkez, incelen düzensiz leke ve akış izleri. İnce leke ile hacim aynı madde gibi birleşmelidir. Renk ve kurgu isimleri aday kalır.

Yosunlar canlı ve esnektir; 5 Eylül prototipindeki parlak yeşil sensör görünümü nihai sanat referansı değildir. HDR/SDR farkı olan video renk hedefi olarak kullanılmaz.

Atık gerekçeleri: tekneye ait eşyalar, çevreden taşınmış karışık atıklar ve iş ekipmanı. Tekrarlanan oyuncaklar gerekiyorsa açılmış paket/kasa gibi çevresel bir gerekçe ile gruplanabilir; tekne geçmişi henüz kesinleştirilmez.

## Dış kare A — üretim tarifi

**TARİHSEL / YETERSİZ BULUNDU:** Aşağıdaki A istemi ilk denemeyi belgeliyor; yeni üretimde B revizyonu kullanılmalıdır.

Oyuncu kamerası deniz tabanının biraz üstünde, küçük teknenin ön/yan tarafından bakar. Tekne su altında zemine oturur; gövde ve kamara kimliği okunur. Ön planda yakın mesafede renkli atık kümeleri, iki farklı kir davranışı ve esnek bitkiler görülür. Küçük görüş boşlukları çalışma alanlarını ayırır; sahne dolu hissettirir. HUD ve yeni silah tasarımı bu ilk çevre karesine eklenmez. Yerleşim, ölçülü level planı değil görsel araştırmadır.

Tekne biçim kaynağı: `konsept görseller/1.level/tekne/Gemini_Generated_Image_jq9mw7jq9mw7jq9m.png` (ilk kare için geçici seçilen üç çeyrek görünüş).
Çöp kaynağı: `konsept görseller/1.level/çöpler/Gemini_Generated_Image_81afd81afd81afd8.png`.

## Değerlendirme

- Tekne tanınabiliyor mu; gövde/kamara/güverte yeni bir tasarıma dönüşmüş mü?
- Yakındaki toplama nesneleri gerçek çalışma ölçeğinde mi?
- Yoğunluğu korurken temizlik yapılan alanın açılması okunabilir mi?
- İki kir türü doğal çevreden ve birbirinden ayrılıyor mu?
- Mevcut iki kişilik üretime aşırı yeni yapı/aset yükü ekliyor mu?

## Kullanılan üretim istemi

Use case: stylized-concept. Create one wide 16:9 environment concept for DEEPCLEAN, a first-person cozy underwater reclamation game. Image 1 is the boat shape reference: preserve this small rusty blue workboat, its single wheelhouse, open wooden working deck, hull proportions and railings. Image 2 is the collectible litter reference: use recognizable colorful cans and bottles from this sheet, with believable materials. Place the boat submerged on the seabed, viewed from a player's low swimming height near the front quarter, with the boat fitting into the middle distance and a detailed reachable foreground. Dense satisfying clusters of colorful litter cover patches of the foreground and hull base; retain small visual gaps between work patches. Include distinguishable granular foreign residue piles and viscous industrial sludge with raised centers merging into thin irregular stains; natural seabed remains visibly separate. Add flexible underwater plants and restrained colorful coral around the site. Stylized realism with convincing wood, worn paint, metal, plastic and glass, crisp nearby surfaces, turquoise water fading into deeper blue haze, soft sunlight caustics, cozy inviting atmosphere. Rich color variety with local readability, not uniformly desaturated. Do not enlarge the boat into a ship, add extra cabins, invent large drilling structures, add people, weapons, HUD, captions, logos, glowing debug foliage or mountains of new props. This is a plausible game-camera environmental concept, not a distant cinematic poster or isometric miniature.

Üretim yöntemi: yerleşik imagegen; ilk görsel değerlendirme taslağıdır.

### A02 düzeltme istemi

Edit this DEEPCLEAN environment concept with one strictly localized correction: remove both human diver hands, gloves and forearms from the lower corners. Reconstruct only the underlying seabed, existing litter and coral in those occluded regions. Keep the exact camera, boat geometry and position, lighting, colors, water, sludge, all other objects and composition unchanged. No hands, people, robot arms, weapons, HUD or added text. Preserve the rest of the image.

### İlk görsel değerlendirmesi

- A02 tekne kimliğini, mavi/paslı gövdeyi ve renkli atık kümelerini koruyor. Birebir geometri doğruluğu ölçülmüş değildir.
- İnsan elleri A02'de kaldırıldı; bu çevre taslağı B-404 tasarımını belirlemiyor.
- Tanecikli yabancı kir doğal zeminden yeterince ayrılmıyor; sonraki çalışma gerektiriyor.
- Çamur fazla siyah/yağ benzeri ve düz görünüyor; prototipteki hacim-leke ilişkisi daha iyi taşınmalı.
- Kare gerçekçiliğe yakın. Kullanıcının hedeflediği stilizasyon ve renk canlılığı açısından değerlendirilmeden iç mekân ve temizlenmiş varyantlara çoğaltılmamalı.
- Üzerindeki ambalaj yazıları tasarım kararı değildir; nihai özgün etiketler ayrıca hazırlanır.

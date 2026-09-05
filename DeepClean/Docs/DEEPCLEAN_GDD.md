# DEEPCLEAN - Yaşayan Oyun Tasarım Belgesi

> **Kanonik proje belgesi**  
> Sürüm: 0.7  
> Son güncelleme: 5 Eylül 2026  
> Belge sahibi: Ana GDD bakım sohbeti

Bu dosya, DEEPCLEAN'in güncel tasarım yönünü diğer proje sohbetleri için ortak ve okunabilir hâle getirir. Eski PDF ve beyin fırtınası metinleri tarihsel kaynaklardır; bundan sonraki çalışmalarda güncel kanonik kaynak bu dosyadır.

**Sürüm ilkesi:** `0.x` sürümleri konsept, tasarım ve prototip öncesi/erken prototip kararlarını temsil eder. İlk dikey dilimin gerçek üretim uygulamasına geçildiğinde ve uygulanacak kapsam kilitlendiğinde belge `1.0` sürümüne çıkarılır. `1.0`, oyunun yayıma hazır olduğu anlamına gelmez; uygulanacak ilk üretim kapsamının başlangıcıdır.

Her belge düzeltmesi sürüm artışı gerektirmez. Açıklamalar, mevcut sistem bilgilerinin düzeltilmesi ve küçük eklemeler aynı sürüm altında kaydedilir; sürüm numarası köklü tasarım eklemeleri veya önemli kapsam değişikliklerinde artırılır.

**KESİN SÜRÜM EŞİKLERİ — 5 Eylül 2026:** Bölüm 17.2'deki güncel beş adımlı planın ilk üç adımı tamamlanıp görsel yön değerlendirildiğinde `0.8`; beşinci adım tamamlandığında `0.9`; uygulama kapsamı kilitlenip üretime geçildiğinde `1.0`. İlk görsel taslağının üretilmesi tek başına sürüm artışı oluşturmaz.

## 0. Karar durumları

- **KESİN:** Kaynak GDD'den gelen veya kullanıcı tarafından açıkça belirlenmiş temel karar.
- **ÇALIŞMA KARARI:** Şu an önerilen ana yön; prototip ve kullanıcı değerlendirmesiyle değişebilir.
- **ADAY:** Değerli görülen fakat henüz oyuna kesin olarak alınmamış fikir.
- **AÇIK SORU:** Karar verilmesi veya test edilmesi gereken konu.
- **ÇIKARILDI / KAÇINILACAK:** Güncel yönle uyuşmadığı için ana tasarımda kullanılmaması önerilen unsur.

Başka sohbetler **ADAY** veya **AÇIK SORU** durumundaki maddeleri kesin özellik gibi uygulamamalıdır.

---

## 1. Yüksek konsept

### 1.1 Tek cümlelik tanım

**ÇALIŞMA KARARI:** DEEPCLEAN; emekliye ayrılmış endüstriyel geri kazanım dronu B-404 ile ilk bakışta ezici yoğunluktaki sualtı çalışma sahalarını işlediğimiz; atıkları değerli hammaddelere dönüştürdüğümüz; tek bir çok amaçlı vakum, fizik sistemleri ve dünya içi küçük işler üzerinde giderek ustalaşıp batıkları ve ekosistemleri kalıcı biçimde hayata döndürdüğümüz birinci şahıs sualtı madenciliği ve restorasyon simülasyonudur.

### 1.2 Tür

**KESİN:**

- Birinci şahıs sualtı temizlik simülasyonu.
- Fizik-bulmaca ve ekipman gelişimi içerir.
- Rahatlatıcı/cozy bir ana tona sahiptir.
- Oyuncuyu öldürmeye odaklanan klasik düşman veya çatışma yapısı ana tasarım değildir.

**KESİN YÖN:** Incremental güçlenme oyunun temel ilerleme omurgalarından biridir. Ancak bu, DEEPCLEAN'i idle/clicker oyununa veya zorunlu 15 saniyelik turlara dönüştürmez. Güçlenme; daha büyük iş sahalarını daha akıcı, daha sistemik ve daha ustaca yönetmeye hizmet eder.

### 1.3 Referans oyunlar ve görevleri

Referanslar bütün hâlinde kopyalanmayacaktır. Her oyundan yalnızca DEEPCLEAN'in belirli bir tasarım problemini çözmek için yararlanılır.

| Referans | Alınacak tasarım dersi | Alınmayacak veya sınırlandırılacak taraf |
|---|---|---|
| **Keep on Mining** | İlk anda ezici görünen nesne yoğunluğu; başlangıçtaki bilinçli hantallık; kısa aralıklarla hissedilen gelişim; kademe kademe açılan çok sayıda küçük mekanik; ileride önceki engelleri çok daha hızlı aşmanın verdiği güç ve ekranı düzene sokma hazzı | Ana oyunu 15-20 saniyelik zorunlu turlara bölmek, otomatik/idle temizleme, sürekli ödül seçimi, yalnızca sayısal artışlara dayanan mobil oyun ritmi |
| **Cozy Cleaner** | Temizlik eylemini farklı mekânlar, işler ve kısa görev modülleriyle çeşitlendirmek; bir alanı tamamladıktan sonra oyuncuya farklı ritimde bir iş vermek | Ana oyundan kopuk, yalnızca menüden açılan veya tema ile ilgisiz mini oyun koleksiyonu |
| **Subnautica 2** | Sualtı ölçeği, berrak yakın plan ile sisli uzak plan dengesi, biyom siluetleri, canlı renk ve ışık kullanımı; Unreal Engine 5 için görsel kalite hedefi | Hayatta kalma, üs kurma, kapsamlı crafting, korku ve yaratık tehdidi gibi üretim kapsamını başka bir türe taşıyan sistemler |
| **PowerWash Simulator** | Dokunsal temizlik, okunaklı kir katmanları ve görünür önce/sonra tatmini | Her işi yalnızca yüzey yüzdesi doldurmaya indirgemek |
| **Hardspace: Shipbreaker** | Her çalışma alanının fizik tabanlı, iş sırası önemli ve birden fazla çözüme açık bir sistemik problem olması | Ağır ceza, ölüm ve sürekli endüstriyel stres tonunu aynen almak |
| **DREDGE** | Kısa saha seferlerinin daha büyük keşif, yükseltme ve gizem ilerleyişine bağlanması | Korku tonunu veya zaman baskısını ana kimliğe dönüştürmek |

**Yakın pazar karşılaştırması:** Loddlenaut, sualtı temizliği, geri dönüşüm, ekosistem canlanması ve sevimli canlılar bakımından yakın bir karşılaştırmadır. DEEPCLEAN'in ayırt edici tarafı; yoğun çalışma sahaları, B-404'ün endüstriyel kimliği, hissedilir güçlenme eğrisi, küçük görev modülleri ve tek araçla sistemik fizik manipülasyonu olmalıdır.

### 1.4 Projenin mevcut aşaması

**KESİN:** Proje hâlen konsept/ön üretim aşamasındadır. Tasarım omurgası kesinleşmeden özellik sayısını artırmak hedef değildir.

**KULLANICI BEYANI - TEKNİK DENETİM YAPILMADI:** Fizik, vakum, akıntı, çamur, çöp üretimi/yerleşimi ve yosun sistemlerinin temel prototipleri oluşturulmuştur. Bu sistemler nihai tasarım kararı değil, üzerinde ilerlenebilecek teknik temel olarak ele alınmalıdır.

**ÇALIŞMA SIRASI:** Önce ana fantezi ve oynanış grameri; ardından ilerleme eğrisi ve seviye tasarımı; sonra görev modülleri/mini işler, RPG-ekonomi katmanı ve gelişmiş fizik sistemleri netleştirilecektir.

---

## 2. Tasarım sütunları

### 2.1 Dokunsal temizlik ve dönüşüm

**KESİN:** Kirli, paslı ve terk edilmiş alanlar gözle görülür biçimde berrak, renkli ve canlı hâle gelir. Temizlik kendi başına tatmin edici olmalıdır.

### 2.2 Tek araçla sistemik ustalık

**KESİN:** Oyunun merkezinde tek bir çok amaçlı vakum aleti bulunur. Derinlik, çok sayıda bağımsız silah eklemekten değil; vakumun farklı modları ile akıntı, ağırlık, yüzdürme, basınç ve malzeme özelliklerinin etkileşiminden doğar.

### 2.3 Her batık bir çalışma sahası ve fizik bulmacasıdır

**ÇALIŞMA KARARI:** Oyuncu yalnızca yüzeyleri yüzde yüz temizlemez. Kirliliğin kaynağını bulur, mekanizmaları açar, ağır parçaları taşır, hassas alanları korur ve doğru çalışma sırasını keşfeder.

### 2.4 Kalıcı ekolojik restorasyon

**ÇALIŞMA KARARI:** Oyuncunun tamamladığı işler dünyada kalıcı iz bırakır. Görüş açılır, canlılar döner, bitkiler gelişir ve yeni yollar veya etkileşimler ortaya çıkar.

### 2.5 Rahatlatıcı gizem

**KESİN:** Derinlerde nadir eşyalar, antikalar ve gizemli kalıntılar bulunur. Anlatı korku veya sürekli hayatta kalma baskısından çok merak ve keşif duygusuna dayanır.

### 2.6 Kaostan ustalığa

**KESİN:** Oyunun temel ilerleme fantezisi, ilk karşılaşmada göz korkutan kir ve nesne yoğunluğunu giderek daha yetkin araçlar, daha iyi saha bilgisi ve küçük sistemlerin birleşimiyle yönetilebilir hâle getirmektir. Oyuncu yalnızca sayaçlarının büyüdüğünü değil, çalışma yönteminin değiştiğini hissetmelidir.

**HEDEF HİS:** Erken oyunda tek tek uğraşılan bir alan, geç oyunda yaklaşık bir büyüklük mertebesi daha hızlı ve akıcı biçimde çözülebilmelidir. Bu "10 kat güç" kesin bir hasar katsayısı değil; süre, menzil, kapasite, zincirleme etki ve oyuncu bilgisinin birlikte ürettiği algılanan güçtür.

---

## 3. Oyuncu karakteri ve perspektif

### 3.1 B-404

**KESİN:**

- Oyuncu bir insan dalgıç değil, **B-404** adlı modifiye edilmiş endüstriyel geri kazanım/madencilik dronudur.
- B-404 ağır sanayi hizmetinden emekliye ayrılmış ve deniz atıklarını ekonomik hammaddelere dönüştüren sualtı geri kazanım madenciliği için yeniden donatılmıştır.
- Görsel kimlik sevimli fakat oyuncak gibi değil; kullanılan, dayanıklı ve sanayi tipi bir iş makinesi hissi vermelidir.

### 3.2 Kamera

**KESİN:** Kamera birinci şahıstır. Oyuncu B-404'ün kollarını, vakum platformunu ve takılı modülleri görür.

### 3.3 Kaynak mantığı

**ÇALIŞMA KARARI:** B-404 bir drone olduğu için oksijen kullanılmaz. Temel saha kaynağı bataryadır. Batarya yalnızca geri sayan bir seans saati olmamalı; iticiler, güçlü vakum modları, ışık ve sonar gibi işlevler arasında enerji kararı yaratmalıdır.

---

## 4. Temel oynanış döngüsü

### 4.1 Makro döngü

**ÇALIŞMA KARARI:**

1. Merkez gemide kontrat, araştırma hedefi veya restorasyon görevi seçilir.
2. Bölgenin şartlarına göre vakum modülleri ve ekipman düzeni hazırlanır.
3. Bölgeye dalış yapılır; kirlilik, enkaz, akıntı ve gömülü nesneler taranır.
4. Görünen kirlilik temizlenirken kirliliğin kaynağı ve çevresel problem araştırılır.
5. Vanalar, kapaklar, ağır nesneler, akıntılar ve hassas yüzeylerle ilgili fizik problemleri çözülür.
6. Geri dönüştürülebilir malzemeler, kayıp eşyalar ve hikâye parçaları çıkarılır.
7. Oyuncu görev hedefi tamamlandığında veya kaynakları azaldığında merkeze döner.
8. Toplananlar satılır, araştırılır veya bölge restorasyonuna ayrılır.
9. Ekipman geliştirilir; yeni derinliklere, iş türlerine ve hikâye alanlarına erişilir.

### 4.2 İç içe döngü hedefleri

| Katman | Örnek | İlk prototip süre hedefi |
|---|---|---:|
| Anlık tatmin | Tek bir nesneyi çekmek veya lekeyi sökmek | 2-5 saniye |
| Mikro problem | Bir tortu kümesini veya küçük mekanizmayı temizlemek | 20-60 saniye |
| Karşılaşma | Bir oda, boru hattı veya akıntı problemini çözmek | 3-6 dakika |
| Dalış | Kontratın anlamlı bir bölümünü tamamlamak | 8-15 dakika |
| Bölge | Büyük batık ve çevresinin restorasyonu | 45-90 dakika |

Bu değerler **prototip hedefidir**, kesin içerik süresi değildir.

### 4.3 Dalışın bitişi

**ÇALIŞMA KARARI:** Ana kampanyada 15-20 saniyelik zorunlu seanslar ve ani otomatik çıkarılma kullanılmaz. Oyuncu batarya, taşıma kapasitesi ve görev hedeflerine göre ne zaman döneceğine karar verir.

**ADAY:** Süreli veya sınırlı enerjiyle yapılan özel kontratlar ana kampanyadan ayrı challenge görevleri olabilir.

### 4.4 Yoğunluk, öğretim ve mekanik grameri

**KESİN:** Sualtına girildiğinde alan; çöp, enkaz, tortu, bitki, canlı ve etkileşimli makine bakımından zengin görünmelidir. Yoğunluk dekoratif bir gürültü değil, oyuncunun zamanla düzene dönüştüreceği okunabilir bir çalışma sahasıdır.

**ÇALIŞMA KARARI:** Oyunda çok sayıda küçük mekanik bulunabilir; ancak her biri tek başına kolay anlaşılır olmalı ve seviye seviye öğretilmelidir.

- Bir görev/bölüm, kural olarak yalnızca **bir yeni temel davranışı** güvenli bir bağlamda tanıtır.
- Aynı bölümün devamı yeni davranışı daha önce öğrenilmiş bir veya iki davranışla birleştirir.
- Sonraki bölümler eski mekanikleri yeni çevre, akıntı veya malzeme koşullarında yeniden kullanır.
- Derinlik, tekil mini sistemlerin karmaşıklığından değil, az sayıdaki okunabilir kuralın birleşmesinden doğar.
- Ekranda çok nesne olabilir; fakat görev için önemli nesneler siluet, hareket, renk değeri, sonar ve çevresel yönlendirmeyle ayırt edilmelidir.

**Mekanik grameri çalışma modeli:**

1. **Madde:** Kum, çamur, yağ, yosun, gevşek/hassas/ağır atık.
2. **Kuvvet:** Çekme, itme, kazıma, akıntı, yüzdürme, ağırlık.
3. **Makine:** Vana, pompa, kapak, filtre, türbin, taşıyıcı düzenek.
4. **Ekoloji:** Mercan, bitki, yengeç, balık sürüsü, filtreleyici canlı.
5. **Amaç:** Temizle, ayır, kurtar, onar, yönlendir veya araştır.

Bir karşılaşma bu katmanlardan iki veya üçünü bir araya getirerek üretilmelidir; her yeni fikir bağımsız bir kontrol şeması gerektirmemelidir.

### 4.5 Oynanış çeşitliliği ve görev modülleri

**KESİN YÖN:** Temizlik ana eylemdir fakat kampanyanın kesintisiz olarak yalnızca vakumlama ve yüzde doldurmadan oluşmaması gerekir. Bölümler arasında veya bölümün doğal bir aşamasında farklı ritme sahip kısa işler bulunacaktır.

**ÇALIŞMA KARARI:** Bunlara geçici olarak **görev modülü** denir. Görev modülü, bağımsız bir mobil mini oyun değil; aynı dünya, araç, fizik ve restorasyon hedefi içinde anlamlı bir iş prosedürüdür.

**KESİN DENEYİM HEDEFİ — MİNİ OYUNLARIN AYRI KEYFİ:** Kullanıcının Cozy Cleaner referansında aradığı özellik, temizlik arasında ilginç ve kendi başına keyif veren farklı işler yapmaktır. Dünya ve araçlarla bütünleşme, mini oyunun sıradan temizlikten ayırt edilememesi anlamına gelmez. Oyuncu "şimdi farklı bir şey yapıyorum" hissini almalıdır. Yalnızca farklı nesnelerin üzerindeki kiri vakumlatmak bu hedefi karşılamaz.

**ÇALIŞMA KARARI:** Her seçilen mini işin anlaşılır bir yerel amacı, temizlikten farklı bir eylem/karar ritmi ve kendine özgü görünür tamamlanma anı bulunmalıdır. Örneğin bir parçayı hizalama, yükü dengeleme veya sıkışan parçayı aşamalı çıkarma adayları aynı araçlarla farklı deneyimler sağlayabilir. Bunlar henüz seçilmiş giriş/orta bölüm mini oyunları değildir. Yakın çalışma görünümü, mekanik sesler ve bağlamsal geri bildirim farklılığı destekleyebilir; kontrol dağılımı daha sonra belirlenir.

**DEĞERLENDİRME SORUSU:** "Bu işin üzerindeki kiri kaldırsak geriye oyuncunun yapacağı ilginç bir eylem kalıyor mu?" Kalmıyorsa iş temizlik karşılaşması olarak değerlidir, fakat tek başına mini oyun çeşitliliği hedefini karşılamaz. Finalde birleşecek davranışları öğretmek faydalıdır; her mini iş yalnızca final eğitimi olmak zorunda değildir. Küçük işlerin kendi keyfi ve keşif değeri korunur.

**ADAY görev modülleri:**

- Tortudan arındırılmış bir vanayı doğru basınç sırasıyla açmak.
- Toplanan malzemeleri mıknatıslı ayırıcı veya sıkıştırıcıda sınıflandırmak.
- Kırılgan bir antikayı temizleyip parçalarını uzamsal olarak birleştirmek.
- Mercan nakli yapmak veya hasarlı bir habitatı yeniden yerleştirmek.
- Sonar yankılarıyla gömülü boru hattının güzergâhını çıkarmak.
- Yüzdürme torbalarını doğru noktalara bağlayarak enkazın dengesini kurmak.
- Bir pompa, filtre ya da türbinin kirli parçalarını sırayla açıp temizlemek.

**Ritim hedefi:** 8-15 dakikalık bir dalışta ana temizlik akışını kesmeden en az bir kısa iş değişimi veya karar yoğunluğu değişimi bulunmalıdır. Her bölüm yeni bir görev modülü eklemek zorunda değildir; güçlü modüller farklı koşullarda tekrar kullanılmalı ve birleşmelidir.

---

## 5. Vakum platformu

### 5.1 Kesin temel işlevler

**KESİN:**

- **Vakumlama:** Hafif çöpleri ve serbest maddeleri uzaktan çeker.
- **Ters itiş / fırlatma:** Tutulan ağır nesneleri iter veya fırlatır; kırılabilir engeller ve fiziksel düzeneklerde kullanılır.
- **Yakın kazıma:** Yüzeye kaynamış çamur, pas, kireç ve benzeri maddeleri yakın mesafede söker. Güçlü ses, titreşim ve malzeme geri bildirimi verir.

**KULLANICI AKTARIMI - MEVCUT PROTOTİP:** Vakum, oyuncunun önündeki geniş bir etki hacmi içinde çalışır. Ana eylem basılı tutulduğunda uygun hafif fizik nesneleri sürekli kuvvet uygulanarak silaha doğru çekilir. Ağır nesneler doğrudan emilmek yerine tutulabilir, taşınabilir ve ikincil eylemle fırlatılabilir. Kum, çamur ve gelecekteki maddelerin aynı vakum girdisine kendi kurallarıyla tepki verebilmesi için ortak bir etkileşim yapısı bulunmaktadır.

Bu özet oyuncu tarafından aktarılan mevcut davranışı kaydeder; kesin kuvvet, zamanlama, hedef önceliği ve sağ/sol tık çakışmaları mekanik denetiminde doğrulanacaktır.

### 5.2 Modül adayları

**ADAY:**

- Dar başlık: küçük alan, yüksek çekiş kuvveti.
- Geniş başlık: geniş alan, düşük çekiş kuvveti.
- Ayırıcı filtre: değerli veya hassas parçaları korur; işlem hızını düşürür.
- Aşındırıcı uç: sert kirleri hızlı söker; hassas yüzeylerde risk oluşturur.
- Halat/tether modu: ağır nesneleri bağlar ve akıntıdan yararlanarak taşır.
- Sonar filtresi: gömülü nesneleri ve kapalı mekanizmaları bulur; yüksek enerji tüketir.
- Darbeli ters basınç: pervaneleri, mekanik kolları veya sıkışmış parçaları hareket ettirir.

### 5.3 Yükseltme ilkesi

**ÇALIŞMA KARARI:** Yükseltmeler yalnızca yüzde artışı vermemelidir. Yeni davranış, yeni çözüm veya belirgin bir araç tercihi yaratmalıdır. Sayısal gelişmeler destekleyici olabilir fakat ana ilerleme bunlardan oluşmamalıdır.

Güçlenme üç eksende ilerler:

1. **Erişim:** Daha uzak, ağır, gömülü veya zor konumdaki hedeflere ulaşmak.
2. **Verim:** Menzil, alan, filtreleme, batarya ve depo sayesinde aynı işi belirgin biçimde daha hızlı yapmak.
3. **Orkestrasyon:** Akıntı, toplayıcı, makine ve ekolojik davranışları birbirine bağlayarak çok sayıda nesneyi oyuncunun başlattığı zincirleme bir süreçle yönetmek.

**Güç aşamaları ve erişim:**

- **Operatör:** Mevcut geniş vakum hacmini kullanabilir; sınırlılık zorunlu olarak menzilden değil, işleme kapasitesi, ağırlık sınırı ve maddeye müdahale seçeneklerinden gelir.
- **Uzman:** Önceki araçların geliştirmelerinin yanında, bu aşamada ilk kez erişilebilen yeni mekanik ve modüller bulunur.
- **Saha Mühendisi:** Önceki sistemlerin gelişmiş birleşimlerinin yanında, daha önce düşük güçlü bir sürümü bulunmayan aşamaya özgü sistemler de açılabilir.

Bu aşamalar karakter sınıfları veya birbirinin yalnızca sayısal olarak güçlendirilmiş kopyaları değildir. Aşama hangi seçeneklerin erişilebilir olduğunu belirler; oyuncunun seçtiği yükseltmeler ise aynı aşamada nasıl çalıştığını belirler.

Geç oyun, oyuncu girdisi olmadan ekranı silmemelidir. Oyuncu zincirleme temizliği **kurar, başlatır ve yönetir**. Böylece Keep on Mining'deki güçlenme hazzı korunurken oyunun fiziksel ustalığı geçersizleşmez.

**ADAY:** Önceden tamamlanmış erken bölgelere isteğe bağlı geri dönüş; yeni araçlarla eski, zor alanların çok daha hızlı temizlenmesini ve saklı hedeflerin açılmasını sağlar. Bu geri dönüşler zorunlu içerik tekrarı değil, güç farkını gösteren kısa ustalık kontratları olmalıdır.

### 5.4 Kontrol ve etkileşim ilkesi

**KESİN İLKE:** Mekanik sayısı arttıkça her davranış için ayrı ve seyrek kullanılan bir tuş eklenmemelidir. Az sayıda tutarlı girdi, aktif mod ve bağlama göre farklı fakat tahmin edilebilir sonuçlar üretmelidir.

**MEVCUT TEMEL:** Ana eylem vakumlamayı, ikincil eylem ise ters basınç/püskürtme ile tutulan ağır nesneyi bırakma veya fırlatma tarafını taşır. Kesin öncelik kuralları mevcut uygulama incelendiğinde belgelenmelidir.

**ÇALIŞMA KARARI - BAĞLAMSAL KAZIMA:** Oyuncu yüzeye bağlı ve kazınabilir maddeye temas mesafesinde ana eylemi sürdürdüğünde vakum başlığı otomatik olarak yakın kazıma davranışına geçebilir. Böylece seyrek kullanılacak ayrı bir kazıma tuşuna ihtiyaç duyulmaz. Başlık animasyonu, ses, titreşim ve yüzey tepkisi mod değişimini açıkça göstermelidir.

**AÇIK SORU:** Vakum odağı, başlık/mod seçimi ve gelecekteki manyetik manipülasyon için fare tekerleği, radyal seçim veya bağlamsal davranışların kesin dağılımı mekanik matrisi ve kullanılabilirlik testi sonrasında belirlenecektir.

### 5.5 Aşamaya özgü sistemler, oyuncu seçimi ve tekrar oynanabilirlik

**KESİN YÖN:** İlerleme hem mevcut mekaniklerin geliştirmelerini hem de yalnızca belirli güç aşamalarında açılan bağımsız yeni sistemleri içerir. Her ileri aşama özelliğinin erken oyunda zayıf bir sürümü bulunması gerekmez.

**DRONE ERİŞİM SINIRI:** Yardımcı robot başlangıçta verilmez. Oyuna alınırsa yalnızca Saha Mühendisi aşamasında erişilebilir; mevcut vakumun erken güçsüz sürümü gibi aşamalara dağıtılmaz. Robotun kesin davranışı, zorunlu mu isteğe bağlı mı olduğu ve demoya üretim kabulü henüz belirlenmemiştir.

**KESİN YÖN:** Oyuncu bütün geliştirmeleri önceden belirlenmiş aynı sırada almak zorunda olmamalıdır. Ortak ana ilerleyiş içinde hangi isteğe bağlı özelliklere ve geliştirmelere yatırım yapacağını kendi çalışma tarzına göre seçebilmelidir.

**TEKRAR OYNAMA HEDEFİ:** Aynı yaklaşık 30 dakikalık seviyenin ikinci veya üçüncü oynanışı yalnızca sayısal hız farkı değil; farklı iş sırası, ekipman birleşimi, yerel çözüm ve oyuncu hissi üretebilmelidir. Farklı oyuncu tarzları için sabit bir sınıf sayısı henüz kararlaştırılmamıştır.

**ÇALIŞMA KARARI:** Ana görev için vazgeçilmez yetenekler ortak erişimde kalmalı veya zorunlu engellerin farklı yatırım yollarıyla geçerli alternatif çözümleri bulunmalıdır. İsteğe bağlı yükseltme seçmeyen oyuncu ana ilerleyişte kilitlenmemelidir. Seçimlerin gerçek bir fırsat maliyeti üretmesi için kaynak/yuva sınırları değerlendirilecektir; kesin ekonomi ve modül sayısı açık karardır.

---

## 6. Madde, kirlilik ve fizik sistemleri

### 6.1 Modüler madde sistemi

**KESİN TERMİNOLOJİ AÇIKLAMASI:** Bu belgede ve prototipte kullanılan "kum" ve "çamur" adları malzeme davranışlarını anlatan teknik çalışma isimleridir. Oyuncunun doğal deniz kumunu veya doğal deniz tabanını kir kabul ederek temizlemesi amaçlanmaz. "Kum" sistemi toz/tanecikli birikinti biçimindeki temizlenebilir maddeyi; "çamur" sistemi balçık kıvamında, yayılan ve akabilen temizlenebilir maddeyi temsil eder. Nihai kurgu adları, renkleri ve malzeme görünümleri henüz seçilmemiştir. Doğal çevre ile çıkarılacak yabancı atık görsel olarak ayrıştırılmalıdır.

**KESİN / TEKNİK TEMEL:** Kum, çamur, yosun, yağ ve benzeri maddeler ortak bir madde altyapısından türeyebilir. Her madde en az şu özelliklerle ayrışabilir:

- Serbest veya yüzeye bağlı olma.
- Yoğunluk ve ağırlık.
- Vakum direnci.
- Yüzeye tutunma.
- Akıntıdan etkilenme.
- Geri dönüşüm veya araştırma değeri.
- Ekosisteme etkisi.

### 6.2 Prosedürel yığın ve destek algılama

**KESİN / TEKNİK TEMEL:**

- Biriken maddeler hücre/örnek tabanlı, performans dostu bir sistem kullanır.
- Yığınlar merkez etrafında katmanlı biçimde büyüyebilir.
- Destek kaybolduğunda madde aşağı düşer; duvara doğal olmayan şekilde yapışmaz.
- Farklı destek nesnelerindeki birikintiler istenmeden birleşmez.
- Vakum etki alanındaki hücreleri kademeli küçültür ve çekilen miktarı hesaplar.

#### 6.2.1 Kum davranışı

**KULLANICI AKTARIMI - MEVCUT PROTOTİP:**

- Oyuncu kumu yüzeylere püskürterek biriktirebilir.
- Yakın kum birikintileri birleşerek tek bir yığın hâlinde büyür.
- Yığın bulunduğu alana göre açık alan, duvar kenarı, iç köşe veya dar alan biçimine uyum sağlar.
- Altındaki destek kaybolursa kum aşağı düşer ve uygun bir alt yüzeye yerleşir; havada asılı kalmaz.
- Vakum kullanıldığında yığın kademeli olarak küçülür ve tamamen çekildiğinde yok olur.
- Birikinti boyutu içerdiği madde miktarıyla doğru orantılıdır; kalan miktar yığının küçülmesi üzerinden okunabilir.

**ADAY KULLANIMLAR:** Nesne saklama/açığa çıkarma, destek ve ağırlık dağılımıyla ilgili işlemler ileride bu altyapıdan yararlanabilir; bunlar mevcut seviyede kurulmuş ve doğrulanmış bulmacalar değildir.

#### 6.2.2 Çamur davranışı

**KULLANICI AKTARIMI - MEVCUT PROTOTİP:**

- Çamur yüzeylere tutunan, yoğun ve vakumla azaltılabilen bir kir türüdür.
- Eğimli yüzeylerde aşağı akar ve geçtiği yerde akış izi bırakır.
- Düz zemine ulaştığında birikinti oluşturur.
- Kenarlardan ve duvarlardan uygun alt yüzeylere geçebilir; havada asılı kalmaz.
- Oyuncu vakumladıkça miktarı ve görünümü azalır; kaynak birikinti tamamen temizlendiğinde ona bağlı akış izleri de kaybolur.
- Birbirine yakın ve aynı yüzeydeki uygun birikintiler birleşebilir.

**KULLANICI DEĞERLENDİRMESİ:** Kum ve çamur aynı temel altyapıyı kullanır. Mevcut etkileşim hisleri kısmen benzerdir; çamurun belirgin ek farkları akması ve daha geniş bir alana leke yaymasıdır. İki tamamen farklı çalışma yöntemi gerektirdikleri henüz varsayılmamalıdır.

Bağlamsal kazıma planı, mevcut vakumla azaltma davranışını iptal etmez. Vakum serbest/yumuşak çamuru çekebilir; yakın kazıma ise yüzeye güçlü biçimde bağlanmış veya sertleşmiş çamur varyantı için ilerleme katmanı olabilir.

#### 6.2.3 Akıntı ve dalga davranışı

**KULLANICI AKTARIMI - MEVCUT DURUM:**

- Mevcut akıntının ağırlıklı işlevi estetiktir: nesnelerin hareketiyle sualtında bulunma hissi verir.
- İlk uygulamada rüzgâr benzeri bir kuvvet altyapısından yararlanılmıştır; bu teknik tercih nihai değildir.
- Dalga sistemi bazı durumlarda çalışmayı zorlaştırabilir, fakat henüz dengelenmiş bir stratejik karar sistemi değildir.
- Akıntıyı yönlendirme, kaynakları bilinçli toplama alanına taşıma veya farklı oyuncu tarzlarını destekleme mevcut ve doğrulanmış işlevler olarak kabul edilmez.

**ADAY GELECEK YÖNÜ:** Sürekli yönsel akıntı ile aralıklı dalga kuvveti ayrı tasarım rolleri üstlenebilir. Oyuncunun hareketini, malzeme taşımasını ve saha yönetimini etkilemeleri değerlendirilebilir. Kesin aralıklar, kuvvetler ve oyuncuya etkileri uygulama/tasarım kararı olarak henüz kilitlenmemiştir.

#### 6.2.4 Hafif, ağır ve yüzen çöp davranışı

**KULLANICI AKTARIMI - MEVCUT PROTOTİP:**

- Hafif çöpler vakum kuvvetinden etkilenerek fiziksel biçimde oyuncuya doğru çekilir.
- Ağır çöpler emilmez; tutulabilir, taşınabilir ve fırlatılabilir.
- Mevcut kırılabilir ağır çöp, bir yüzeye vurularak veya fırlatılıp çarptırılarak kırılabilir. Ağır nesneyi tutma/fırlatmanın şu anki somut kullanım örneği budur; eşya taşımalı seviye bulmacaları henüz kurulmamıştır.
- Uygun çöplerin kaldırma/yüzdürme davranışı tek tek her nesnenin üzerinde çalışmak yerine bölgesel ve merkezî bir sistem tarafından yönetilir.
- Ağır çöpler otomatik kaldırma/yüzdürme davranışının dışında tutulur.

Kırılabilirliği oyuncuya öğreten seviye yönlendirmesi henüz yapılmamıştır. Kırılma sonrası parçaların toplanabilirliği ve kaynak ödülü ayrıca netleştirilmelidir; mevcut bilgi bunların işleyişini doğrulamamaktadır.

**ADAY TASARIM YÖNÜ:** Çöp yalnızca satılacak kaynak olmayabilir; ağırlık, yüzdürme elemanı, mekanizma engeli, geçici tapa, karşı ağırlık veya başka bir fizik probleminin aracı olarak kullanılabilir.

### 6.3 Kirlilik kaynağı sistemi

**ÇALIŞMA KARARI:** Kirlilik yalnızca haritaya serpiştirilmiş can puanları gibi davranmamalıdır. Bazı bölgelerde aktif kaynak bulunur:

- Sızdıran petrol veya kimyasal borusu.
- Kırık arıtma filtresi.
- Çöp taşıyan akıntı.
- Açık kalmış enkaz bölmesi.
- Tortu üreten arızalı türbin veya pompa.

Oyuncu kaynağı durdurmadan yalnızca sonucu temizlerse sınırlı ve açıklanabilir yeniden kirlenme olabilir. Kaynak durdurulduktan ve bölge tamamlandıktan sonra temizlik kalıcıdır.

### 6.4 Fiziksel problem türleri

**ADAY:**

- Akıntıyı kapaklar ve vanalarla yönlendirme.
- Batık bölmelerinde su akışını veya basıncı dengeleme.
- Yüzdürme torbalarıyla ağır parçaları kaldırma.
- Ağırlık merkezini değiştirerek enkaz parçasını döndürme.
- Kırılgan mercanların arasından çöp çıkarma.
- Kir türlerini birbirine karıştırmadan ayırma.
- Sıkışmış mekanizmaları doğru sırayla temizleyip çalıştırma.

### 6.5 Mekanik dokümantasyon standardı

**ÇALIŞMA KARARI:** Oyuncunun karşılaştığı ve üretime alınan her ana mekanik GDD'de kısa, tasarım odaklı bir özetle tanımlanmalıdır. GDD; Blueprint sınıfları, fonksiyon listeleri veya ayrıntılı algoritmalar yerine oyuncunun ne yaptığını ve sistemin hangi tasarım amacına hizmet ettiğini anlatır.

Her kabul edilmiş mekanik için gerektiği ölçüde şu bilgiler tutulur:

1. **Amaç:** Mekanik oyuna neden ekleniyor ve hangi oyuncu hissini destekliyor?
2. **Oyuncu eylemi:** Oyuncu mekaniği nasıl başlatıyor veya kontrol ediyor?
3. **Dünya tepkisi:** Sistem görünür ve işitsel olarak nasıl cevap veriyor?
4. **Temel kurallar:** Neler üzerinde çalışıyor, neler üzerinde çalışmıyor?
5. **Sınırlar ve maliyet:** Enerji, menzil, kapasite, süre, risk veya ekipman şartı var mı?
6. **Diğer sistemlerle bağ:** Akıntı, madde, fizik, ekoloji, ekonomi veya görevlerle nasıl birleşiyor?
7. **İlerleme:** Yükseltmeler davranışı veya kullanım yöntemini nasıl değiştiriyor?
8. **Başarı ve başarısızlık:** Oyuncu doğru/yanlış kullandığını nasıl anlıyor?

**Belge sınırı:** Bir mekaniğin teknik uygulama ayrıntısı büyüdüğünde ayrı bir sistem tasarım/teknik tasarım belgesine taşınır ve GDD'de yalnızca kısa özet ile ilgili belge bağlantısı kalır.

**MEVCUT DOKÜMANTASYON İHTİYACI:** Vakumlama, ters itiş/püskürtme, yakın kazıma, kum, çamur, akıntı, çöp yerleşimi ve yosun sistemleri bu şablonla sırayla belgelenmelidir. Kodda gerçekten çalışan davranışlar incelenmeden eksik ayrıntılar varsayılmamalıdır.

---

## 7. Kapasite, kaynak ve geri dönüş

### 7.1 Atık deposu

**KESİN:** Vakumlanan maddeler B-404'ün atık deposunda birikir ve daha sonra merkezde geri dönüşüme/satışa aktarılır.

**ÇALIŞMA KARARI:** Depo sistemi oyuncuyu çok sık aynı yolu yürümeye zorlayan bir angarya olmamalıdır. Doluluk, hangi malzemenin saklanacağı veya görevin ne zaman sonlandırılacağı hakkında karar yaratmalıdır.

**ADAY:** İleri aşamada bölgeye kurulabilen toplama şamandırası veya sıkıştırma modülü, tekrar yolculuklarını azaltabilir.

### 7.2 Ekonomi

**KESİN:** Plastik, paslı metal ve diğer geri dönüştürülebilir malzemeler kredi kazandırır. Krediler ekipman ve kapasite geliştirmelerinde kullanılır.

**KESİN ROL TANIMI:** Oyuncu kurgu içinde bir çöpçü değildir. Plastik, metal, elektronik parça, cam ve diğer deniz atıkları çıkarılıp ayrıştırılacak maden/hammadde damarları gibi değerlendirilir. Ekolojik temizlik bu işin görünür ve olumlu dünya sonucudur.

**ÇALIŞMA KARARI:** Ekonomi çok sayıda mobil oyun para birimine bölünmez. İlk hedef:

- **Kredi:** Satın alma ve temel ekipman geliştirmeleri.
- **Araştırma ilerlemesi:** Yeni teknoloji ve bilgi açılması; harcanabilir ikinci para birimi olmak zorunda değildir.
- **Restorasyon durumu:** Harcanan para değil, bölgenin kalıcı dünya durumudur.

### 7.3 Çıkarma ve başarısızlık

**ÇALIŞMA KARARI:** Ana kampanyada süre dolduğu için "respawn" kullanılmaz. Batarya kritik seviyeye geldiğinde güvenli geri çağırma veya oyuncunun kontrollü dönüşü gerçekleşir. Ceza, tüm ilerlemeyi silmek yerine o dalışta taşınan bazı fırsatların kaçması veya ek taşıma maliyeti olabilir.

---

## 8. Ekolojik restorasyon

### 8.1 Görsel dönüş

**KESİN:** Kirlilik azaldıkça mercanlar ve bitkiler görünür hâle gelir; balık sürüleri, yengeçler ve diğer canlılar geri döner. Oyuncu çalışmasının sonucunu anında ve kalıcı biçimde görür.

### 8.2 Sistemik ekoloji

**ADAY:** Dönen canlılar yalnızca dekorasyon değildir:

- Midye ve istiridyeler suyu filtreleyerek görüşü artırabilir.
- Küçük balıklar ilginç veya saklı nesnelere yönelerek ipucu verebilir.
- Deniz çayırları yerel akıntıyı yavaşlatabilir.
- Yengeçler uygun şekilde yönlendirildiğinde küçük atıkları kümelendirebilir.
- Sağlıklı mercanlar yeni türleri, araştırmaları veya yan görevleri açabilir.

### 8.3 Restorasyon ölçümü

**ÇALIŞMA KARARI:** Tek bir genel temizlik yüzdesi kullanılabilir fakat tek başarı ölçütü olmamalıdır. Bölge değerlendirmesi; aktif kaynaklar, geri dönüştürülen atık, habitat durumu, keşifler ve tamamlanan mekanizmaları ayrı gösterebilir.

---

## 9. Canlılar ve engeller

### 9.1 Genel ton

**KESİN:** Oyuncuyu öldürmeye çalışan klasik düşmanlar yerine işi zorlaştıran, meraklı veya yaramaz ekosistem üyeleri bulunur.

### 9.2 Sarmaşık Yengeci

**KESİN ÇEKİRDEK:** Sarmaşık Yengeci çöplere yaklaşır, sarmaşıklarıyla onları yere sabitler ve uzaktan vakumlanamaz hâle getirir. Oyuncu yaklaşıp sarmaşıkları kazıyarak nesneyi serbest bırakır.

**ÇALIŞMA KARARI:** Yengece ağır varil fırlatmak ana çözüm olmamalıdır. Cozy tonla daha uyumlu çözümler araştırılmalıdır:

- Yiyecek veya parlak nesneyle başka yere çekmek.
- Işık, ses veya akıntıyla yönlendirmek.
- Yengecin davranışını oyuncu lehine kullanmak.

Vakumun ağır nesne fırlatma işlevi çevresel bulmacalarda korunur.

### 9.3 Canlı tasarım ilkesi

**ÇALIŞMA KARARI:** Her canlı tek kullanımlık bir anahtar değil, farklı sistemlerle etkileşebilen davranış setine sahip olmalıdır. Oyuncu canlıları öldürmez; gözlemler, yönlendirir veya habitatlarını iyileştirir.

---

## 10. Görev ve dünya yapısı

### 10.1 Merkez gemi

**ADAY / GÜÇLÜ YÖN:** Menü yerine içinde hareket edilebilen küçük bir mobil atölye/geri dönüşüm gemisi:

- Kontrat ve bölge haritası.
- Ekipman tezgâhı.
- Malzeme ayrıştırma alanı.
- Kayıp eşya ve antika kataloğu.
- Temizlenen bölgelerin ekolojik verilerini gösteren araştırma bölümü.
- B-404 için görsel özelleştirme ve gövde izleri.

### 10.2 Bölge yapısı

**ÇALIŞMA KARARI:** Dünya yalnızca prosedürel çöp alanlarından oluşmaz. Her ana bölge kendine özgü görsel kimliğe, baskın madde türüne, fizik problemine ve küçük hikâye zincirine sahip tasarlanmış bir çalışma sahasıdır.

Her ana bölge mümkünse şu omurgayı taşır:

1. Uzaktan okunabilen bir **kahraman nesne**: batık tekne, türbin, istasyon veya boru düğümü.
2. İlk bakışta yoğun fakat katmanlara ayrılabilen bir kirlilik alanı.
3. Bölgenin baskın yeni mekaniğini öğreten güvenli bir cep.
4. Eski ve yeni mekanikleri birleştiren bir ana çalışma problemi.
5. Temizliğin hızını veya alanın şeklini değiştiren aktif kirlilik kaynağı.
6. Görev modülü, keşif veya anlatı temposu sağlayan kısa bir ritim değişimi.
7. Uzak mesafeden dahi fark edilen kalıcı ekolojik önce/sonra dönüşümü.

**ADAY bölge örnekleri:**

- Paslanmış araştırma istasyonu.
- Mercanların üzerine çökmüş konteyner gemisi.
- Sızdıran endüstriyel boru hattı.
- Terk edilmiş sualtı turizm tesisi.
- Akıntı türbinleriyle çevrili derin deniz madeni.
- Gizemli, şirket kayıtlarında bulunmayan eski kalıntı alanı.

### 10.3 Görev çeşitleri

**ADAY:**

- Alanı güvenli ve erişilebilir hâle getirme.
- Aktif kirlilik kaynağını bulup kapatma.
- Ağır enkazı hassas habitat üzerinden kaldırma.
- Belirli kayıp eşya zincirini tamamlama.
- Eski mekanizmayı temizleyip yeniden çalıştırma.
- Nadir numuneyi zarar vermeden çıkarma.
- Ekolojik eşikleri tamamlayarak belirli canlıyı bölgeye döndürme.
- Opsiyonel süre veya verimlilik kontratı.

### 10.4 Seviye tasarımı ve LDD yaklaşımı

**ÇALIŞMA KARARI:** Konsept ve ilk dikey dilim aşamasında ayrı bir LDD zorunlu değildir. Az sayıdaki seviye için yüksek seviye tasarım bilgisi bu GDD'nin içinde tutulabilir. Böylece ana oynanış, ilerleme ve seviye kararları erken aşamada birbirinden kopmaz.

Her tasarlanan seviye/bölge için şu kısa şablon kullanılacaktır:

1. Bölgenin adı, teması ve hikâye amacı.
2. Oyuncunun bölgeye ilk bakışta gördüğü kahraman nesne ve ana hedef.
3. Giriş, yön bulma, ana rota, yan cepler ve geri dönüş noktaları.
4. Öğretilen yeni mekanik ve tekrar kullanılan eski mekanikler.
5. Baskın madde, akıntı, fizik ve ekoloji kuralları.
6. Ana kirlilik kaynağı ve çözüm sırası.
7. Görev modülü veya tempo değişimi.
8. Sırlar, koleksiyonlar ve opsiyonel hedefler.
9. Kirli, yarı temiz ve restore edilmiş dünya durumları.
10. Erken/orta/geç ekipmanla beklenen çözüm farkı.
11. Yaklaşık süre, performans bütçesi ve oynanış testi hedefleri.

**AYIRMA EŞİĞİ:** Üç veya daha fazla ana bölge ayrıntılı üretime geçtiğinde, seviye belgeleri `Docs/LDD/` altında ayrı dosyalara taşınmalıdır. GDD dünya yapısını ve ortak kuralları tutar; her LDD yalnızca kendi seviyesinin yerleşimini, karşılaşmalarını, akışını ve içerik listesini ayrıntılandırır.

**NOT:** Bölüm 17.2'deki mekanik matrisi, güç eğrisi, seviye grameri ve gri kutu bölüm adımları ilk LDD'nin hazırlık sürecidir.

---

## 11. Anlatı ve koleksiyon

### 11.1 Dünya

**KESİN:** Fütüristik dönemde okyanus temizliği kazançlı bir "geri dönüşüm madenciliği" mesleğine dönüşmüştür. B-404, yüzeydeki şirketten topladığı malzemeler için kredi alır.

Görev dili mümkün olduğunca "çöp toplama" yerine saha taraması, kaynak çıkarımı, malzeme geri kazanımı, enkaz işleme ve bölge restorasyonu kavramlarını kullanmalıdır. Cozy temizlik hissi korunur; fakat karakterin mesleki kimliği madencilik ve endüstriyel geri kazanımdır.

### 11.2 Ana gizem

**KESİN:** Derinlere inildikçe sıradan çöplerin yanında nadir inciler, antik eşyalar ve açıklanamayan kalıntılar ortaya çıkar.

**AÇIK SORU:** Şirketin rolü yalnızca mizahi bürokrasi mi, ahlaki açıdan gri bir yapı mı, yoksa hikâyenin merkezindeki antagonistik güç mü olacak?

### 11.3 Çevresel hikâye

**ÇALIŞMA KARARI:** Temizlik aynı zamanda araştırmadır. Kir ve tortu katmanları kaldırıldıkça gemi plakaları, seri numaraları, kişisel eşyalar, kayıt cihazları ve kapalı bölmeler ortaya çıkar.

### 11.4 Kayıp eşya kataloğu

**KESİN:** Bulunan özel eşyalar kataloglanır ve hafif hikâye anlatımı sağlar.

**ADAY:** Bazı eşyalar doğrudan satılmak, araştırmaya verilmek veya bir seti tamamlamak arasında seçim yaratabilir.

---

## 12. Sanat yönetimi ve atmosfer

### 12.1 Ana estetik

**KESİN:** Rahatlatıcı, renkli ve biyolüminesan bir sualtı dünyası. Karanlık ve korkutucu ana ton değildir.

### 12.2 Görsel kontrast

**KESİN:** Canlı mercanlar ve sevimli deniz yaşamı; paslı metal, endüstriyel plastik ve kirli tortuyla güçlü biçimde karşıtlık oluşturur. Oyuncu çirkinliği kaldırarak doğanın rengini ortaya çıkarır.

### 12.3 Görüş katmanları

**ÇALIŞMA KARARI:**

- Yakın çalışma alanı berrak, keskin ve malzeme okunabilirliği yüksek olmalıdır.
- Uzak alan ışığı yutan su sisiyle derinlik ve keşif duygusu vermelidir.
- Kostikler, parçacık akışları ve doğal zemin dalgalanmaları atmosferi desteklemelidir.

### 12.4 Geri bildirim standardı

**ÇALIŞMA KARARI:** Her madde; ses, parçacık, titreşim, yüzey değişimi ve vakum tepkisiyle ayırt edilmelidir. Profesyonel his, sistem sayısından önce bu eylemlerin kalitesinden gelir.

### 12.5 Mevcut konsept görsellerin durumu

**KAYNAK:** `D:\deepclean\deepclean\konsept görseller`

**KULLANICI AÇIKLAMASI — 5 Eylül 2026:** Tekne ve çöp modelleri bu klasördeki ilgili konseptler esas alınarak, yakın biçim benzerliği hedeflenerek modellenmektedir. İlgili tekne ve çöp tasarımları mevcut üretimin biçim referansıdır; yeni konsept çalışması bunların kimliğini korur. Klasörün tamamındaki ışık, ölçek, yazı ve yerleşim ayrıntıları otomatik olarak kanonik değildir. Modellerin tamamlanması veya yeni ekran görüntülerinin gelmesi erken görsel çalışma için ön koşul değildir.

Yararlı tarafları:

- Turkuaz su, renkli mercan, paslı tekne ve yoğun çöp kontrastını hızlıca gösterir.
- Tekne, ağır atık, küçük çöp, değerli eşya, bitki ve canlı kategorileri için başlangıç çeşitliliği sunar.
- Alanların ilk anda dolu ve göz korkutucu görünmesi fikrini destekler.

Sorunları:

- Çoğu görsel ressamsı anahtar görsel niteliğindedir; birinci şahıs oynanış okunabilirliğini kanıtlamaz.
- Renk doygunluğu ve nesne yoğunluğu bazı karelerde görev hedeflerini kaybettirir.
- Nesne ölçeği, malzeme dili, tekne detayları ve stil seviyesi görseller arasında tutarlı değildir.
- Bazı çöp setleri fazla oyuncak/mobil oyun estetiğine yaklaşır; yapay zekâ kaynaklı biçim ve yazı hataları içerir.

**YENİ KONSEPT PAKETİ İÇİN HEDEF:** Mevcut üretim referanslarının biçimleri korunarak sanat dili ve oyuncu bakışı geliştirilir; aşağıdaki kontrollü set hazırlanmalıdır:

- Aynı alanın kirli, yarı temiz ve restore edilmiş birinci şahıs oynanış kareleri.
- Yakın çalışma alanı ile uzak su sisi için değer/renk hedefi.
- B-404 kolu, vakum ve HUD'un birlikte görüldüğü oynanış çerçevesi.
- Bir kahraman batığın ölçek ve dolaşım çizimleri.
- Çöp, tortu, metal, mercan ve biyolüminesans için malzeme/renk kılavuzu.
- Aynı sahnenin erken, orta ve geç oyun güç seviyelerindeki okunabilirlik karşılaştırması.

---

## 13. Arayüz ve oyuncu bilgisi

### 13.1 Temel HUD

**KESİN:** Bölge veya görev temizliği hakkında anlaşılır ilerleme bilgisi bulunur.

**ÇALIŞMA KARARI:** HUD mümkün olduğunca B-404'ün endüstriyel arayüzünün parçası gibi görünmeli; mobil oyun sayaçları ve sürekli ödül patlamaları hissinden kaçınmalıdır.

### 13.2 Gösterilecek bilgiler

**ADAY:**

- Batarya ve anlık enerji tüketimi.
- Atık deposu doluluğu ve malzeme dağılımı.
- Aktif görev hedefleri.
- Kirlilik kaynağı durumu.
- Bölgesel restorasyon özeti.
- Vakum modu ve takılı modül.

### 13.3 Madde analiz geri bildirimi

**ÇALIŞMA KARARI:** Vakumun analiz/ayrıştırma süreci, hedef üzerinde beliren kısa ve küçük beyaz bir parıltı veya ince tarama vurgusuyla okunabilir hâle getirilebilir. Geri bildirim; büyük holografik tarama çerçeveleri, yoğun mavi arayüz katmanları veya Subnautica 2'nin görsel kimliğini doğrudan çağrıştıran bir sunum kullanmamalıdır.

**KABUL EDİLEN SUNUM YÖNÜ:** Küçük beyaz malzeme doğrulama parlamasını, kaynak türüne bağlı çok kısa bir renkli parçacık vurgusu izleyebilir. Ses; bilimkurgu tarayıcı melodisinden çok endüstriyel barkod okuyucu/yazıcı gibi kısa ve mekanik olmalıdır. Nesne bütünüyle hologramla kaplanmaz; tekrarlanan ses ve parlamalar yoğun toplamada birleştirilerek görsel/işitsel yorgunluk önlenmelidir.

Nesnelerin organik fizik hareketi korunmalıdır. Aynı rota ve hızla ilerleyen katı bir kuyruk yerine serbest çekim, kısa analiz kilidi ve yalnızca silah ağzına çok yakınken kontrollü son emiş kullanılmalıdır. Kesin görsel dil prototip ve okunabilirlik testiyle belirlenecektir.

---

## 14. Kaçınılacak tasarım yönleri

**ÇIKARILDI / KAÇINILACAK:**

- Ana oyunu 15-20 saniyelik zorunlu seanslara bölmek.
- Oyuncuyu her tur sonunda otomatik olarak yüzeye ışınlamak.
- B-404 için oksijen kaynağı kullanmak.
- Her turun mutlaka yükseltmeyle bitmesi.
- İlerlemeyi ağırlıklı olarak düz yüzde artışlarından kurmak.
- Oyuncunun başlangıçta neden yavaş olduğunu açıklamadan yapay biçimde hantal kontroller kullanmak.
- Tamamlanan temizliği sebepsiz ve sürekli geri büyütmek.
- Oyuncuyu tank boşaltmak için çok sık aynı rotada gidip gelmeye zorlamak.
- Geç oyunu bütün ekranı otomatik temizleyen ve temel etkileşimi anlamsızlaştıran bir güç fantezisine dönüştürmek.
- Cozy hissi sağlamak amacıyla fizik problemlerini ve anlamlı kararları kaldırmak.
- Steam oyunu gibi görünmek adına kontrolsüz sistem, para birimi veya mini oyun eklemek.
- Ana dünya ve araç sistemlerinden kopuk, tek kullanımlık mini oyunlar üretmek.
- Her bölümde yeni bir mekanik tanıtıp öncekileri bir daha kullanmamak.
- Çok oyunculu modu yalnızca pazar beklentisi nedeniyle erken üretim kapsamına almak.

---

## 15. Açık tasarım soruları

1. Ana kampanyada batarya oyuncuyu ne kadar sınırlandırmalı; tamamen tükenen bataryanın kesin sonucu ne olmalı?
2. Merkez gemi oynanabilir fiziksel bir alan mı, hızlı ve stilize bir menü mü olacak?
3. Oyuncu aynı büyük bölgeye kaç dalışta dönmeli?
4. Temizlik, fizik bulmacası ve keşif arasındaki hedef süre dağılımı ne olmalı?
5. Hassas ekolojiye zarar verme ihtimali olacak mı; olacaksa cozy tonu bozmadan nasıl sonuçlanacak?
6. Kredi dışında ayrı bir araştırma kaynağına gerçekten ihtiyaç var mı?
7. Ana gizemin tonu mizahi, melankolik veya daha ciddi mi olacak?
8. Prosedürel madde yerleşimi ile elle tasarlanmış görev alanlarının oranı ne olmalı?
9. B-404 sessiz bir avatar mı, sesli bir karakter mi olacak?
10. Oyunun hedef kampanya süresi ve fiyat konumu nedir?
11. Erken oyundaki kısıt hissinin kabul edilebilir sınırı nedir; oyuncu hangi anda ilk büyük güç sıçramasını yaşamalı?
12. Tam oyunda tekrar kullanılacak temel görev modülleri hangileri olacak ve bunlardan kaçı ilk dikey dilimde test edilecek?
13. RPG unsurları B-404'ün teknik uzmanlaşması mı, anlatısal rol yapma seçimleri mi, yoksa ikisinin sınırlı bir birleşimi mi olacak?

---

## 16. İlk dikey dilim hedefi

**ÇALIŞMA KARARI:** Tam üretim kapsamından önce yaklaşık 30 dakikalık, tek ve kesintisiz bir batık bölümü oyunun kimliğini doğrulamalıdır:

- Bir küçük merkez/atölye alanı.
- Bir ana sualtı bölgesi ve dışı ile içi yükleme ekranı olmadan birbirine bağlı tek büyük batık.
- Vakumlama, ters itiş/fırlatma ve kazıma.
- En az üç davranış bakımından farklı madde türü.
- Bir aktif kirlilik kaynağı ve onu durduran fizik problemi.
- Sarmaşık Yengeci veya eşdeğer bir sistemik canlı.
- Bir kayıp eşya/hikâye zinciri.
- Belirgin önce/sonra ekolojik dönüşümü.
- En az üç niteliksel ekipman seçimi.
- Aynı alan içinde en az bir görev modülü veya belirgin ritim değişimi.
- Erken ve geliştirilmiş araç arasında aynı iş üzerinde açıkça hissedilen verim/strateji farkı.
- **Operatör, Uzman ve Saha Mühendisi** güç aşamalarının üçünü de gösteren sıkıştırılmış bir ilerleme eğrisi.
- Dış alanın giriş/öğretim bölümü, mekanik olarak farklı çalışan batık içi ikinci bölüm ve ilk zorlukların yeni güçlerle hızla aşıldığı final dönüşü.
- Yaklaşık 25-35 dakikalık tamamlanabilir demo/dikey dilim ritmi.

Dikey dilimin temel testi: Oyuncu yalnızca daha hızlı temizlemek istememeli; alanın nasıl çalıştığını anlamak, altında ne olduğunu görmek ve geri döndüğünde dünyanın nasıl değiştiğini merak etmelidir. Güçlenme yeni bir sayıdan ibaret kalmamalı; oyuncunun aynı yoğun sahayı ele alma biçimini görünür şekilde değiştirmelidir.

### 16.1 İlk 30 dakikanın çalışma akışı

Bu zamanlar kesin senaryo süreleri değil, prototip ritim hedefleridir. Uygulama ve oynanış testleri sırasında değiştirilebilir.

#### 0-8 dakika - Operatör / dış çalışma alanı

- Oyuncu mevcut geniş etki hacimli vakum, ters basınç/fırlatma, hafif-ağır çöp, kum ve çamur davranışlarını öğrenir.
- Alanın tamamını temizleyemeyeceği anlaşılır; sonraki güç seviyeleriyle çözülecek yoğun kümeler, ağır nesneler ve kapalı erişim noktaları erken gösterilir.
- Vakumlanan kaynaklar ilk küçük verim gelişmelerini besler. Aynı anda işlenen hedef sayısı, analiz süresi veya depo işleme kapasitesi gibi artışlar ilk dakikalarda hissedilir fark üretmelidir.
- Dış alan temizliği ve gelişim, batığın iç bölümüne erişimi açar.

#### 8-20 dakika - Uzman / batık içi ikinci bölüm

- Dışarıdaki yüksek hacimli temizliğin yerini daha dar, hassas ve sıralı bir çalışma ritmi alır; yükleme ekranı kullanılmaz.
- Devrilmiş nesneler geçişi kapatır; kum bağlantıları gizler; çamur hareketli parçaları kilitler; kablo/ağ benzeri engeller fiziksel işlemleri etkiler; hassas eşyalar seçici çalışmayı gerektirir.
- Gelişim döngüsü durmaz: oyuncu temizler, kaynak işler, küçük gelişme alır, yeni engeli aşar ve daha yoğun bir iç bölüme ulaşır.
- Dar/geniş odak, bağlamsal kazıma, gelişmiş ayrıştırma ve ağır nesneyi kontrollü yönetme bu bölüm için aday ilerleme araçlarıdır; kesin dağılım mekanik matrisinde belirlenecektir.

#### 20-27 dakika - Saha Mühendisi / birleşik prosedür

- Oyuncu yalnızca daha hızlı vakumlayan değil, öğrendiği sistemleri birlikte kullanan seviyeye ulaşır.
- **ÇALIŞMA KARARI — ANA PROSEDÜR TASLAĞI:** Sıkışmış bir numune/sondaj çekirdeğinin çıkarılması. Kum ve çamur temizliği, kilit noktalarının açılması, ters basınç, ağır parça/karşı ağırlık yönetimi ve olası manyetik manipülasyon aynı fiziksel süreçte birleşir. Ayrıntılı işleyiş aşağıdaki 16.1.1 bölümündedir; kesin teknik çözüm ve modül gereksinimleri henüz kilitlenmemiştir.
- Prosedür ayrı bir arayüz mini oyununa geçmez; mevcut araç ve dünya kuralları farklı hassasiyet ve sırada kullanılır.
- Bu bölümün ödülü, final temizliğinin ölçeğini belirgin biçimde artıran yeni bir davranış veya sistem birleşimidir. Manyetik zincirleme çıkarım ve rezonanslı kazı şu an adaydır, kesin değildir.

#### 27-30 dakika - Final güç gösterisi ve dönüşüm

- Oyuncu başlangıçta gördüğü veya kısmen temizlediği yoğun dış alana geri döner.
- Birikmiş küçük ve büyük gelişmeleri birlikte kullanarak daha önce zorlandığı alanı kendisi çok daha hızlı işler.
- Akıntı, kum, çamur, hafif/ağır çöp ve ayrıştırma mekanikleri finalde birbirini desteklemelidir; çevresel sistem oyuncunun yerine oynamamalıdır.
- Son kapalı alan veya değerli kaynak açılır; batığın hikâye sonucu ve belirgin ekolojik önce/sonra dönüşümü gösterilir.

### 16.1.1 Final mini oyunu ve tekne eklemelerinin işlevsel temeli

**ÇALIŞMA KARARI — KORUNACAK FİKİR:** Final, oyuncunun temizlediği, çevirdiği ve taşıdığı parçaların birlikte büyük bir numuneyi fiziksel olarak serbest bıraktığı dünya içi bir mini oyundur. Kendine özgü hizalama/yük yönetimi/çıkarım ritmi ve belirgin bir sonuç anı sunar; yalnızca uzun bir temizlik kontrol listesine dönüşmemelidir.

**ÖNCEKİ BİRLEŞİK AKIŞ TASLAĞI:** Aşağıdaki maddeler fikrin geçmiş birleşik hâlini korur. Güncel üç kapanış yapısında halka hizalama Uzman aşamasına, yük yönetimi ve çıkarım Saha Mühendisi aşamasına dağıtılmıştır (16.1.2); yedi adımın tamamı finalde tekrar oynatılmaz.

1. Sıkışmış noktalar görsel işaretlerle veya aday sonar yardımıyla bulunur.
2. Tanecikli birikinti ve çamur kaldırılarak kilit halkaları ile bağlantılar ortaya çıkarılır.
3. Sıkışmış çevre gevşetilir; basınçlı püskürtmenin bu işlevi adaydır, mevcut madde püskürtme davranışıyla aynı olduğu varsayılmaz.
4. Kilit halkaları hizalanır. Manyetik kavrama aday yöntemdir; ortak araçlarla geçerli çözüm ve kesin kontrol şeması açık kalır.
5. Ağır karşı ağırlık uygun kılavuza/raya taşınarak çıkarım hazırlanır. Karşı ağırlığın hangi kilidi veya yük dengesini değiştirdiği mekanik tasarımda açıklanmalıdır.
6. Numune kontrollü çekilirken çevresindeki tortu temizlenir. Zorlanma görüldüğünde başka sıkışma noktasına müdahale edilir; çekiş ve temizlik girdilerinin birlikte veya dönüşümlü kullanımı henüz kararlaştırılmamıştır.
7. Numune tüpten fiziksel olarak çıkar ve geri kazanılır. Büyük parçanın serbest kalması ayrı bir görsel/işitsel tamamlanma anıdır.

Bu sıra önceki fikri koruyan taslaktır; halka sayısı, kesin adım sırası, çekiş direnci, yük ve başarısızlık kuralları nihai değildir. Mıknatıs gibi isteğe bağlı bir modül ana görevin tek çözümü hâline getirilmez. Mevcut vakumun bütün uygun hafif nesneleri çekmesi korunur; kazıma, sonar ve manyetik manipülasyon uygulanmış sistemler gibi kabul edilmez.

**ÜÇ AŞAMAYA BAĞLANTI:** Girişte toplama ve basit fiziksel müdahaleler gelişimi besler. Orta bölümde yeni yetenekler, farklı kısa işler ve devam eden kaynak/geliştirme döngüsü bulunur. Final bu davranışları birleştirir; ardından yaklaşık 27-30 dakikada oyuncu dış alanda kişisel güç artışını kullanır. Giriş ve orta bölüm mini oyunlarının tam listesi henüz seçilmemiştir. Devrilmiş nesne, gömülü bağlantı ve sıkışmış mekanizma örnekleri otomatik olarak kesin görev yapılmaz. Finalin ödülünün güçlenmeye nasıl bağlanacağı açıktır; numune değeri sıradan kaynak toplamayı anlamsızlaştırmamalıdır.

**TEKNE KİMLİĞİ — ÇALIŞMA KARARI:** Mevcut küçük gövde, numune çıkarımı ve geri kazanım işi için ek ekipmanla donatılan tekne olarak geliştirilir. Teknenin geçmiş işinin ve oyuncunun bugünkü müdahalesinin fiziksel izleri görünür olmalıdır. Renkli gündelik atıklar, ekipman parçaları ve geri kazanılacak maddeler birlikte bulunabilir.

**ÖNCEKİ EKİPMAN FİKİRLERİ — ADAY ENVANTER:** Numune sondaj düzeneği; elektromanyetik ayırıcı; ağır yük vinci; cevher/numune depolama bölümü; endüstriyel filtreler; sıkışmış sondaj çekirdeği. Bu liste her ekipman için ayrı mini oyun veya zorunlu tamir zinciri kabul edildiği anlamına gelmez. Elektromanyetik ayırıcı bütün metal türlerini çekiyor sayılmaz.

| Finalde gereken iş | Tekne eklemesinin sağlaması gereken karşılık |
|---|---|
| Birikintiyi kaldırıp bağlantıları bulma | Kısmen gömülü kılavuz ve bağlantı yuvaları |
| Halkaları ortaya çıkarma ve hizalama | Erişilebilir hareketli kilit halkaları |
| Karşı ağırlığı taşıma | Yükün işlevini gösteren kılavuz ve mekanik bağlantı |
| Çekiş sırasında sıkışmayı çözme | Hareketle yeni müdahale noktaları açılan tüp/yatak |
| Numunenin fiziksel olarak çıkması | Çıkarım mesafesi ve parçayı karşılayacak alan |

**KAPSAM SINIRI:** Vinç bu işlevlerden birini desteklediği ölçüde eklenir; karşı ağırlığı gereksizleştirmemeli veya oyuncunun çıkarım işini tamamen devralmamalıdır. Filtre/ayırıcı/depo, giriş ve orta bölüm için aday çalışma alanlarıdır; bütün makineleri sırayla tamir etme zorunluluğu onaylanmamıştır. Teknenin ölçüleri ve iç yerleşimi doğrulanmadan bütün ekipmanın sığdığı varsayılmaz.

**GÖRSEL ÜRETİMDEN ÖNCE:** Sabit tüp, çıkan numune taşıyıcısı, kilit halkaları, kılavuz ve karşı ağırlık/yük desteğinin ilişkisi netleştirilir. Sonra kullanıcı için İngilizce görsel istemi hazırlanır. Kullanıcı görselleri harici yapay zekâda üretir; bu sohbet inceler. Yeni açık talep olmadan burada görsel üretilmez. Mevcut dış alan taslakları henüz onaylı sanat hedefi değildir.

### 16.1.2 Birbirine bağlı üç aşama kapanışı

**KESİN TASARIM İLKESİ:** Oyuncuya başlangıçta verilen ana hedefe aşamalı olarak yaklaşılır. Üç mini oyun Operatör, Uzman ve Saha Mühendisi aşamalarının kapanışlarıdır; peş peşe bağımsız işler değildir. Aralarında keşif, kaynak toplama, geliştirme seçimi ve yeni yetenek kullanımı sürer. Her kapanış sonraki aşamaya somut erişim veya mekanik hazırlık sağlar; yalnızca ek kaynak vermesi zorunlu ana hat için yeterli gerekçe değildir. Farklı yerel amaç ve eylem ritimleri korunur.

**KESİN GELİŞİM İLKESİ:** İlk kapanış başlangıç ekipmanıyla hemen çözülebilir olmamalıdır. Oyuncu engeli erken görür, dış sahadaki çalışmasıyla yeni bir işlev kazanır ve aynı engele dönerek önceden yapamadığı müdahaleyi yapar. Mevcut geniş vakum veya ağır nesne tutma işlevi yapay biçimde zayıflatılmaz. Temizlik yüzdesi, görünmez duvar veya yalnızca aşama etiketi fiziksel gerekçenin yerine geçmez. Zorunlu yeni işlev ortak ilerleme erişimindedir; isteğe bağlı geliştirme seçimleri bu erişimi kilitlemez. Yeni yeteneğin açılması mini oyunu otomatik tamamlamaz.

| Kapanış | Ana hedefle bağlantısı | Durum ve farklı his |
|---|---|---|
| Operatör: raylı bakım kızağını açma | Numune kilitlerinin servis bölümüne erişim sağlar | İşlevsel taslak; yeni yetenekle hareket ettirip sıkışma nedenini ortaya çıkarma |
| Uzman: numune kilitlerini hizalama | Numuneyi mekanik olarak serbest bırakır | KONSEPT; hizalama ve bağlantı ilişkisini çözme, kesin mekanizma açık |
| Saha Mühendisi: yük dengeli çıkarım | Numuneyi fiziksel olarak geri kazanarak ana hedefi tamamlar | KONSEPT; karşı ağırlık, kontrollü çekiş ve tortu müdahalesi, kesin mekanizma açık |

Ana hedef için "sıkışmış son numuneyi geri kazan" çalışma ifadesi kullanılır. Bu tablo son iki mini oyunun üretime hazır olduğunu belirtmez. Kişisel güç gösterisi için dış alana son dönüş korunur. Genel kaynak ekonomisi numune ödülüyle değersizleştirilmez.

#### İlk kapanış için yeni yetenek önerisi: mekanik tahrik bağlantısı

**YENİ ÇALIŞMA ÖNERİSİ — KULLANICI DEĞERLENDİRMESİ BEKLER:** Vakum platformuna takılan bağlantı ucu, standart servis yuvasına oturup makinenin miline kontrollü dönme hareketi aktarır. Mevcut serbest çekme/itmeden farklı olarak bir mekanizmayı bağlantı üzerinden çalıştırır. Bu önerinin ayrıntıları, kesin gelişim ilkesinden ayrı tutulur; mevcut uygulama değildir.

- Bakım kızağı, numune servis girişinin önünde iki ray üzerinde hareket eder. Sabit dişli kutusu ve kendinden kilitlemeli vidalı mil kızağı taşır; dışarıdan çekmek onu açmaz. Yeni uç servis milini döndürerek kızağı ilerletir. Modelde mil, somun/taşıyıcı bağlantısı ve gövde ankrajı görünür olmalıdır.
- Oyuncu başlangıçta yuvayı ve kapalı geçişi görür; olağan temizlik ve gevşek engelleri kaldırma mümkündür. Dış sahadaki normal kaynak işleme ortak temel modülün edinilmesini besler. Fiyat, teknoloji eşiği ve edinim ekranı ekonomi tasarımında belirlenecek; sonsuz çöp üretimi veya ilk kapının arkasındaki tek bir eşyaya bağımlılık kurulmayacaktır.
- Modülle dönüldüğünde yuva üzerinden kızak kısmen hareket ettirilir. Açılan servis aralığı, rayda sıkışmış ayrı metal takozu görünür ve erişilebilir kılar. Kızak biraz geri alınarak takoz üzerindeki yük boşaltılır; oyuncu bağlantıdan ayrılıp mevcut ağır nesne tutmasıyla takozu çıkarır. Yeniden bağlanıp ilerleterek geçişi açar. Takoz rastgele anahtar değildir; hareketi fiziksel olarak engeller.
- Kontrol önerisi: yakın yuvaya nişan alıp ana eylemle bağlanma; bağlıyken sol/sağ eylem ileri/geri tahrik; iki eylem bırakılınca ayrılma. Mod değişimi belirgin geri bildirim verir, hedefleme sırasında rastgele bağlanma önlenir. Kesin bağlanma süresi ve girdi öncelikleri kullanılabilirlik tasarımıdır.
- Sıkışmada motor durur, parçanın yük altında olduğu hareket/sesle anlaşılır. Ölüm, süre baskısı veya ilerleme sıfırlama önerilmez. Güçlü ekipman zorunlu engeli açabilir; mini işin içinde gözlem ve geri alma kararı yine oyuncudadır.
- Aynı standart bağlantı için iç bölüm mekanizması ve çıkarım taşıyıcısı aday sonraki kullanımlardır. Bunlar kesin mini oyun çözümü değildir. En az üç anlamlı kullanım, iki sistemle birleşim ve görünür yöntem farkı ölçütü sağlanamazsa modül tek kullanımlık bir anahtar hâline getirilmeden revize edilir.
- Modelleme taslağı: sabit çerçeve, iki ray, hareketli bakım kızağı, vidalı tahrik mili, korumalı dişli kutusu/servis yuvası, çıkarılabilir takoz ve fiziksel olarak kapatılan giriş. Ölçüler, tekne üzerindeki kesin açıklık ve yük geometrisi doğrulanmadan bitmiş aset üretimi yapılmaz. Gövdeye yeni bir delik açıldığı varsayılmaz.

Görsel istemi: `Art/DEEPCLEAN_OPERATOR_MINIGAME_PROMPT_EN.md`. İstem bu mekanizma önerisini incelenebilir kılar; görselin üretilmesi öneriyi otomatik olarak kesinleştirmez.

### 16.2 Dikey dilim ilerleme ilkesi

Üç güç aşaması yalnızca bölüm başlarında verilen üç büyük yükseltmeden oluşmamalıdır. Yaklaşık her birkaç dakikada bir küçük verim kazanımı, yeni kullanım veya daha önce görülen engeli aşma fırsatı bulunmalıdır. Bununla birlikte her kazanım yeni bir tuş veya bütünüyle bağımsız sistem değildir.

**ÇALIŞMA HEDEFİ:**

- Az sayıda ana oyuncu fiili.
- Sürekli hissedilen küçük verim artışları.
- En fazla birkaç büyük davranış açılımı.
- Yeni açılan davranış için anlamlı ve yeterli kullanım fırsatları; açıldıktan sonraki 30-60 saniyede kullanım zorunlu değildir.
- Önceki engellerin yeni güçlerle yeniden yorumlanması.
- Finalde oyuncunun seçtiği gelişmelerin güç farkını gösterebilmesi; her mekaniğin finalde kullanılması zorunlu değildir.

Yaklaşık 3-4 dakikada bir gelişim fırsatı sunulması ritim hedefidir; belirli dakikada belirli modülün herkese otomatik verilmesi anlamına gelmez. Oyuncunun yatırım seçimleri korunur. Aşamaya erişim ile isteğe bağlı yükseltme satın alma/seçme ayrı kararlardır.

---

## 17. Ön üretim karar ve doğrulama planı

### 17.1 Güncel çekirdek kimlik

**ÇALIŞMA KARARI:** DEEPCLEAN'in ayırt edici formülü:

> **Yoğun sualtı temizliği + kademeli endüstriyel ustalık + dünya içine bağlı değişken görevler + kalıcı ekolojik dönüşüm**

Yeni bir özellik bu dört parçadan en az birini güçlendirmiyor veya aralarındaki bağı derinleştirmiyorsa üretim kapsamına alınmamalıdır.

### 17.2 Tasarım sırası

**GÜNCEL ÇALIŞMA NOKTASI:** Erken görsel tasarım çalışması başlamıştır. Mekanik tanımlama/seçim matrisi bu çalışma sonrasında sürdürülecektir. Karşılaştırmalı playtestler henüz başlamamıştır. Daha önce konuşulan değerli kutulu küçük test alanı kabul edilmiş bir seviye tasarımı değildir; değerli kutu da mevcut prototip içeriği değildir.

1. **Görsel tarif:** Mevcut tekne/çöp biçimleri korunarak su, ışık, malzeme, bitki ve iki temizlenebilir madde için kısa çalışma tarifi hazırlanır.
2. **İlk dış alan konsepti:** Oyuncu bakışından tekne, yoğun atıklar, kirler ve bitkiler birlikte gösterilir; görsel yön değerlendirilir.
3. **İç alan ve dönüşüm:** Seçilen dil tekne içine taşınır; aynı dış alanın kirli ve temizlenmiş görünüşleri karşılaştırılır. Tutarlılık değerlendirildiğinde `0.8`.
4. **Mekanik ve ilerleme matrisi:** Mevcut davranış, geliştirme ve yeni sistem adayları ayrılır. Üç güç aşaması, isteğe bağlı seçimler, kontrol gereksinimleri ve alternatif yöntemler belirlenir.
5. **Bölüm, ekonomi ve kapsam:** Yaklaşık 30 dakikalık dış/iç alan akışı, kaynak kazanımı, yükseltme fırsatları, sondaj/çıkarım adayı ve final güç hissi birlikte tasarlanır. İki kişilik üretim kapsamı belirlenir; tamamlandığında `0.9`.

**UYGULAMAYA GEÇİŞ:** Kapsam kilitlenip üretime başlandığında `1.0`. Gri kutu uygulama, motor içi görünüm denemeleri ve oynanış testleri, tasarım varsayımlarını bu süreçte sınar. Konsept görselleri ölçülü mimari plan veya çalıştığı kanıtlanmış oynanış değildir.

### 17.3 Dikey dilim kabul ölçütleri

- İlk 10 saniyede oyuncu alanın durumunu, ana işi ve görsel dönüşüm vaadini anlayabilir.
- Yoğun sahne zengin görünür fakat etkileşim hedefleri kaybolmaz.
- İlk dakikalarda temel vakum eylemi kendi başına tatmin edicidir.
- Bir yükseltme oyuncunun yalnızca hızını değil, çalışma yöntemini de görünür biçimde değiştirir.
- Yaklaşık 30 dakikalık örnek seviye en az üç ana etkileşim fiili, sürekli ilerleme geri bildirimi ve bir doğal ritim değişimi içerir.
- Oyuncu kirliliğin kaynağını bulup durdurduğunda alan kalıcı olarak değişir.
- Görev modülü ana oyundan kopuk hissettirmez ve sonradan başka bir seviyede yeniden kullanılabilir.
- Prototip, oyunun "bir sonraki güç seviyesinde bu alanı nasıl temizlerdim?" merakını oluşturur.

### 17.4 Mekanik kabul ve seviye desteği ölçütleri

**KABUL EDİLEN TASARIM NOTU:** Tekrar kullanılan bir mekanik için şu üç özellik aranır:

1. Seviye boyunca en az üç anlamlı kullanım fırsatı sunması.
2. En az iki başka sistemle işlevsel biçimde birleşmesi.
3. Oyuncuya görünür bir güç veya çalışma yöntemi farkı vermesi.

Bu ölçütler oyuncuyu her seçeneği kullanmaya zorlamak için değil, üretilen mekaniğin seviye tasarımıyla desteklenmesini değerlendirmek içindir. Özellikle isteğe bağlı mekanik, onu seçen oyuncu için değerli olmalı; seçmeyen oyuncuyu yapay biçimde engellememelidir.

**ZORUNLU OLMAYAN ÖLÇÜTLER:** Açıldıktan sonraki 30-60 saniyede kullanılma ve final güç gösterisinde tekrar görünme faydalı fırsatlar olabilir; kabul koşulu değildir. Bir yeteneği açılır açılmaz denetebilmek, onu oyunun başlangıcında vermek anlamına gelmez.

Seviyeye özgü tek seferlik bir anlatı/prosedür sahnesi bu tekrar kullanılabilir mekanik ölçütlerinden ayrı değerlendirilir. Böyle bir sahne, yeni ve pahalı bağımsız sistemler yerine mevcut mekanikleri mümkün olduğunca yeniden kullanmalıdır.

## 18. Değişiklik günlüğü

### 0.7 içinde — 5 Eylül 2026

- Üç mini oyunun aşama kapanışı, ana hedefe fiziksel ilerleme ve farklı deneyim oluşturması kaydedildi; Uzman/Saha Mühendisi çözümleri konsept bırakıldı.
- İlk mini oyunun yeni yetenek edinmeden tamamlanamaması kesin gelişim ilkesi olarak eklendi. Mekanik tahrik bağlantısı bunun için yeni çalışma önerisi olarak ayrı etiketlendi.

- Mini oyunların dünya ve araçlarla bütünleşirken sıradan temizlikten farklı, ilginç ve kendi başına keyifli deneyimler sunması kabul edildi.
- Önceki final numune çıkarım taslağı ayrıntılı olarak geri kaydedildi; belirsiz mekanik ve giriş/orta bölüm görevleri aday/açık tutuldu.
- Tekne ekipman envanteri ve finalin fiziksel gereksinimleri ilişkilendirildi; bağımsız zorunlu makine tamir zinciri kabul edilmedi.
- Kullanıcının harici görsel üretimi tercihi kaydedildi. Sürüm 0.7 korundu.

- Kullanıcının onayladığı beş adımlı çalışma sırası ve `0.8 / 0.9 / 1.0` eşikleri kaydedildi; sürüm henüz artırılmadı.
- Tekne ve çöp konseptlerinin mevcut modelleme için biçim referansı olduğu netleştirildi; erken sanat çalışması için tamamlanmış model bekleme koşulu kaldırıldı.
- Görsel tasarım çalışma belgesi `Art/DEEPCLEAN_VISUAL_BRIEF.md` altında başlatıldı. Buradaki öneriler onaylanana kadar taslaktır.

### 0.7 - 4 Eylül 2026

- Aynı sürüm içi düzeltme: küçük belge eklemelerinde otomatik sürüm artırılmaması, yalnızca köklü değişikliklerde sürüm artışı yapılması açıklandı.
- "Kum/çamur" adlarının doğal deniz tabanını değil, iki temizlenebilir madde davranışını temsil eden teknik çalışma adları olduğu netleştirildi.
- Mevcut akıntının öncelikle estetik olduğu, stratejik kullanımların henüz aday kaldığı düzeltildi.
- Kırılabilir ağır çöpün darbe/fırlatma yoluyla kırılması mevcut davranış olarak eklendi; taşıma bulmacalarıyla karıştırılmaması belirtildi.
- Çalışmanın mekanik tanımlama/seçim matrisi aşamasında olduğu ve önerilen değerli kutulu test alanının kabul edilmediği kaydedildi.

- Üç güç aşaması yalnızca aynı mekaniklerin daha güçlü sürümleri olmaktan çıkarıldı; aşamaya özgü yeni sistem erişimi açıklandı.
- Yardımcı drone için başlangıçta bulunmama ve yalnızca Saha Mühendisi aşamasında erişim sınırı kaydedildi; kesin uygulama ve seçim statüsü açık bırakıldı.
- Ortak ana ilerleyiş içinde oyuncunun yükseltme seçimi ve farklı yöntemlerle tekrar oynama hedefi eklendi.
- Üç kullanım fırsatı, iki sistem bağlantısı ve görünür güç/yöntem farkı mekanik değerlendirme notları olarak eklendi.
- Hemen kullanım ve finalde tekrar kullanım zorunlulukları kaldırıldı; 3-4 dakikalık gelişim ritmi sabit modül sırasından ayrıldı.
- Küçük beyaz analiz parıltısı, kısa kaynak rengi vurgusu ve endüstriyel ayrıştırıcı sesi yönü ayrıntılandırıldı.

### 0.6 - 3 Eylül 2026

- Belge sürümleme kuralı eklendi: uygulama kapsamı kilitlenene kadar `0.x`, ilk gerçek üretim uygulamasına geçildiğinde `1.0`.
- İlk 30 dakika Operatör dış alanı, Uzman batık içi, Saha Mühendisi birleşik prosedürü ve final güç gösterisi olarak ayrıntılandırıldı.
- Gelişim döngüsünün batık içinde de devam etmesi ve yaklaşık her birkaç dakikada anlamlı bir ilerleme geri bildirimi vermesi şartı eklendi.
- Sondaj/numune çıkarımı ana prosedür adayı olarak korundu; mıknatıs ve rezonans kesin mekanik yapılmadı.
- Analiz kilidi için küçük beyaz parıltı yönü ve organik fizik hareketini koruma ilkesi eklendi; tek tip spline/kuyruk görünümünden kaçınıldı.

### 0.5 - 3 Eylül 2026

- Kullanıcı tarafından aktarılan mevcut vakum davranışı, teknik sınıf/değişken adları çıkarılarak tasarım seviyesinde kaydedildi.
- Kumun püskürtülme, birleşme, çevre biçimine uyum, destek kaybı ve vakumla küçülme davranışları eklendi.
- Çamurun yüzeye tutunma, eğimde akma, iz bırakma, uygun yüzeye düşme, birleşme ve vakumla azalması belgelendi.
- Sürekli akıntı ile aralıklı dalga kuvveti tasarım açısından ayrıldı; kesin teknik değerler kanonik karar yapılmadı.
- Hafif, ağır ve bölgesel yüzdürme yönetimine bağlı çöp davranışları kaydedildi.
- Az sayıda tutarlı girdi ilkesi ve yüzeye bağlı maddeler için bağlamsal yakın kazıma çalışma kararı eklendi.

### 0.4 - 3 Eylül 2026

- B-404'ün kurgu içindeki rolü çöpçü/temizlik görevlisi değil, deniz atıklarını ekonomik hammaddelere dönüştüren endüstriyel geri kazanım madencisi olarak netleştirildi.
- İlk dikey dilim, dış ve iç alanı yükleme ekranı olmadan birleştiren yaklaşık 30 dakikalık tek batık seviyesi olarak tanımlandı.
- Operatör, Uzman ve Saha Mühendisi güç aşamalarının tamamının bu dikey dilimde sıkıştırılmış biçimde gösterilmesi kararlaştırıldı.
- Batık içinin dış alandan mekanik ve ritmik olarak ayrışması, finalde ise oyuncunun ilk zorluklara yeni güçleriyle dönmesi şartı eklendi.

### 0.3 - 3 Eylül 2026

- Kabul edilen mekanikler için GDD'de kullanılacak kısa tasarım dokümantasyonu şablonu eklendi.
- Teknik uygulama ayrıntılarının gerektiğinde ayrı sistem/teknik tasarım belgelerine taşınacağı belirlendi.
- İlk seviyelerin GDD içinde tasarlanması, üretim büyüdüğünde ayrı `Docs/LDD/` dosyalarına ayrılması kararlaştırıldı.
- GDD'nin genel Altı Şapka değerlendirmesi ve SCAMPER dönüşüm tablosu belgenin sonuna eklendi.
- Gelecekteki fikirler için SCAMPER, Altı Şapka, prototip ve kanonik belgeye kabul sırası tanımlandı.

### 0.2 - 3 Eylül 2026

- Keep on Mining, Cozy Cleaner ve Subnautica 2 bağımsız referanslar olarak eklendi; her biri için alınacak ve alınmayacak taraflar ayrıldı.
- Incremental güçlenme destekleyici ayrıntı olmaktan çıkarılıp temel ilerleme omurgası olarak tanımlandı; zorunlu kısa tur ve idle yapıdan ayrıldı.
- Oyunun ana ilerleme fantezisi "kaostan ustalığa" olarak tanımlandı; algılanan yaklaşık 10 kat güç, erişim/verim/orkestrasyon eksenlerine bağlandı.
- Çok sayıda küçük mekaniğin bölüm bölüm öğretilmesi ve daha sonra birleştirilmesi için mekanik grameri oluşturuldu.
- Temizlik dışındaki ritim değişimleri, kopuk mini oyunlar yerine dünya içi görev modülleri olarak çerçevelendi.
- Bölgelere kahraman nesne, öğretim cebi, ana sistemik problem, görev modülü ve kalıcı dönüşüm omurgası eklendi.
- Mevcut konsept görseller incelendi; geçici ve kanonik olmayan referans statüsüne alındı, yeni konsept paketinin hedefleri belirlendi.
- Projenin konsept/ön üretim aşaması ve kullanıcı tarafından bildirilen mevcut teknik prototipler kayda geçirildi.
- Dikey dilime görev çeşitliliği ve erken/geç araç gücü karşılaştırması eklendi.
- Ön üretim tasarım sırası ve dikey dilim kabul ölçütleri eklendi.

### 0.1 - 3 Eylül 2026

- Eski PDF GDD ve sonraki tasarım konuşmaları tek yaşayan belgede birleştirildi.
- B-404, birinci şahıs kamera, tek vakum platformu, fizik-bulmaca, geri dönüşüm ekonomisi, Sarmaşık Yengeci ve derinlik gizemi korundu.
- Incremental yapı ana türden destekleyici ilerleme katmanına indirildi.
- 15-20 saniyelik zorunlu seanslar yerine iç içe geçmiş mikro problem, karşılaşma ve dalış ritmi önerildi.
- Oksijen kaldırılarak batarya temelli drone mantığına geçildi.
- Sebepsiz kirlilik geri büyümesi yerine aktif kirlilik kaynağı sistemi getirildi.
- Kalıcı ekolojik restorasyon, sistemik iş sahaları, niteliksel vakum modülleri ve merkez gemi yönleri eklendi.
- Kesin, çalışma kararı, aday, açık soru ve çıkarılmış fikirler birbirinden ayrıldı.

---

## 19. GDD'nin genel yaratıcı ve eleştirel değerlendirmesi

Bu bölüm mevcut tasarım yönünün dönemsel değerlendirmesidir. Oyundaki her mekanik için ayrı ayrı tekrarlanmaz. Ana yön önemli ölçüde değiştiğinde veya dikey dilim testlerinden sonra güncellenir.

### 19.1 Altı Şapkalı Düşünme değerlendirmesi

#### Beyaz Şapka - Bilinenler ve kanıtlanması gerekenler

- Projenin vakum, fizik, akıntı, çamur, çöp yerleşimi ve yosun alanlarında kullanıcı tarafından bildirilen çalışan temel prototipleri vardır; bunların tasarım ve teknik denetimi henüz yapılmamıştır.
- Temel vaat; yoğun ve kirli bir sualtı alanını temizleyerek okunabilir, renkli ve yaşayan bir çevreye dönüştürmektir.
- Incremental güçlenme, farklı görev ritimleri ve sualtı atmosferi ayrı referanslardan alınarak tek yapıda birleştirilmektedir.
- Oyunun henüz doğrulanmamış temel noktaları; başlangıç kısıtının kabul edilebilirliği, yoğun sahne okunabilirliği, güç sıçramasının niteliği, görev modüllerinin ana akışla uyumu ve içerik üretim maliyetidir.

#### Kırmızı Şapka - Hedeflenen duygu

- İlk bakışta "burayı nasıl temizleyeceğim?" dedirten bir alanın giderek kontrol altına alınması güçlü bir rahatlama ve yetkinlik duygusu yaratabilir.
- Kir altından renk, yaşam, mekanizma ve hikâye çıkması oyuncuda merak ve sahiplenme oluşturur.
- B-404'ün eski fakat geliştirilebilir endüstriyel yapısı, güçlenme fantezisini dünyaya doğal biçimde bağlar.
- Başlangıç hantallığı adaletsiz veya yapay hissedilirse merak hızla sıkıntıya dönüşebilir.

#### Siyah Şapka - Riskler

- Çok fazla nesne görsel gürültü, yön kaybı, erişilebilirlik sorunu ve performans maliyeti yaratabilir.
- Çok sayıda küçük mekanik ortak kurallara bağlanmazsa oyun derin değil, dağınık görünür.
- Kopuk veya tek kullanımlık mini oyunlar mobil oyun hissini güçlendirebilir.
- Yalnızca sayısal yükseltmeler oyuncuyu güçlendirirken tasarlanmış fizik problemlerini önemsizleştirebilir.
- Geç oyundaki otomasyon oyuncunun temizlik yapma hazzını ortadan kaldırabilir.
- Her seviye için tamamen yeni sistem üretmek küçük ekip/tek geliştirici kapsamını aşabilir.
- Görsel kalite hedefini Subnautica 2 ile eşitlemek, üretim kapasitesi hesaba katılmazsa gerçekçi olmayan beklenti yaratabilir.

#### Sarı Şapka - Güçlü yanlar ve fırsatlar

- Kirli ve restore edilmiş alan arasındaki büyük fark ekran görüntüsü ve fragmanda kolay anlatılan güçlü bir pazarlama vaadidir.
- Temizlik ile belirgin güçlenmenin birleşimi, cozy oyunlarda daha az kullanılan bir uzun vadeli motivasyon sunar.
- Tek vakum platformunun farklı sistemlerle etkileşmesi, sınırlı kontrol şemasıyla yüksek kombinasyon çeşitliliği üretebilir.
- Sualtı akıntısı, yüzdürme ve üç boyutlu dolaşım oyunu klasik oda temizleme oyunlarından ayırabilir.
- Kalıcı ekolojik dönüşüm, oyuncunun emeğine yalnızca para değil dünyada anlamlı bir sonuç verir.
- Mevcut teknik prototipler doğru odaklanılırsa dikey dilim için değerli bir başlangıç sağlar.

#### Yeşil Şapka - Geliştirme fırsatları

- Güçlenme Operatör, Uzman ve Saha Mühendisi aşamalarında yalnızca hız değil çözüm ölçeği değiştirebilir.
- Oyuncu geç oyunda akıntıyı yönlendirip geçici toplayıcı kurarak kendi zincirleme temizliğini tasarlayabilir.
- Eski bölgelere isteğe bağlı ustalık kontratları, önceki zorluğun yeni güçle aşılmasını görünür kılabilir.
- Her bölgenin kahraman nesnesi; mekanik, anlatı, navigasyon ve görsel dönüşümü aynı merkezde toplayabilir.
- Çöpler yalnızca para veren hedefler değil; ağırlık, yüzdürme elemanı, geçici tapa, iletken veya canlı davranışını yönlendiren nesne olabilir.
- Görev modülleri farklı kontrol ekranları yerine mevcut vakum, fizik, sonar ve hareket kurallarını yeni amaçlarla kullanabilir.

#### Mavi Şapka - Yönetim kararı

**SONUÇ:** Konsept Steam ölçeğinde bir oyun için yeterli potansiyele sahiptir; fakat profesyonel his sistem sayısından değil, sistemlerin tekrar kullanımı, seviye düzeni, geri bildirim kalitesi ve güç eğrisinin kontrollü birleşiminden doğacaktır.

Üretim odağı yeni özellik biriktirmek değil; Bölüm 17'deki sırayla çekirdek hissi, mekanik matrisini, üç aşamalı güç eğrisini ve tek bir güçlü gri kutu seviyeyi doğrulamaktır. RPG, geniş ekonomi ve büyük içerik üretimi bu doğrulamadan sonra ele alınır.

### 19.2 SCAMPER ile genel tasarım dönüşümü

| SCAMPER adımı | DEEPCLEAN için uygulama |
|---|---|
| **Substitute / Yerine koy** | 15-20 saniyelik zorunlu turların yerine kısa mikro problemler içeren 8-15 dakikalık oyuncu kontrollü dalışlar koy. Kopuk mini oyunların yerine dünya içi iş prosedürleri kullan. |
| **Combine / Birleştir** | Vakum, akıntı, madde, makine ve ekolojiyi zincirleme temizlik problemlerinde birleştir. Temizliği keşif ve çevresel hikâye anlatımıyla bağla. |
| **Adapt / Uyarla** | Keep on Mining'in büyük güç farkını, otomatik kazma yerine tekil işlemlerden saha ölçeğinde orkestrasyona geçiş olarak uyarla. Cozy Cleaner'ın ritim çeşitliliğini tekrar kullanılabilir görev modüllerine dönüştür. |
| **Modify / Değiştir-büyüt-küçült** | Oda temizliğini üç boyutlu sualtı çalışma sahasına; basit yetenek ağacını B-404 uzmanlaşma/modül sistemine; sayısal hızı yöntem değiştiren niteliksel güce dönüştür. |
| **Put to another use / Başka amaçla kullan** | Çöp, akıntı, canlı ve çevre makinelerini yalnızca engel değil bulmaca aracı, taşıma yöntemi, ipucu ve ekolojik yardımcı olarak yeniden kullan. |
| **Eliminate / Ele** | Robot için oksijen, sebepsiz kirlilik geri büyümesi, sürekli zorunlu dönüş, gereksiz para birimleri, tek kullanımlık mini oyunlar ve oyuncu girdisini yok eden otomasyonu çıkar. |
| **Reverse-Rearrange / Tersine çevir-yeniden sırala** | Bazı işlerde önce makineyi onar, sonra onun yardımıyla alanı temizle. Gelişmiş araçlarla eski alanlara dönerek önceki zorluğu tersine çevir. Temizliği yalnızca sona değil, keşif ve onarım aşamalarının arasına dağıt. |

### 19.3 Gelecekteki fikirleri değerlendirme protokolü

Yeni bir fikir için önerilen çalışma sırası:

1. **Problemi tanımla:** Hangi oyuncu ihtiyacını veya tasarım açığını çözüyoruz?
2. **SCAMPER uygula:** Tek fikre bağlanmadan alternatifler ve mevcut sistemlerle birleşimler üret.
3. **Hızlı kapsam filtresi yap:** Projenin dört parçalı çekirdek kimliğine katkısı olmayan veya üretim maliyeti aşırı olan seçenekleri ele.
4. **Altı Şapka ile değerlendir:** Bilgi, duygu, risk, fayda, yaratıcı alternatif ve yönetim kararı başlıklarında incele.
5. **Gerekirse küçük prototip kur:** Özellikle fizik, his, okunabilirlik veya performans varsayımlarını test et.
6. **Karar ver:** Fikri kabul et, revize et, beklet veya çıkar.
7. **Yalnızca kabul edilen kararı GDD'ye işle:** Sohbetteki bütün alternatifleri ve her fikrin Altı Şapka notlarını kanonik belgeye taşıma. GDD'ye mekaniğin son biçimi, amacı, ana kuralları, durum etiketi ve gerekiyorsa kısa karar gerekçesi eklenir.

Bu protokol bir zorunlu toplantı ritüeli değildir. Küçük ve geri alınabilir ayrıntılarda kısa değerlendirme yeterlidir; büyük kapsam, ilerleme, seviye yapısı veya oyuncu deneyimi kararlarında tam süreç kullanılır.

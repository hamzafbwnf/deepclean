# DEEPCLEAN - Yaşayan Oyun Tasarım Belgesi

> **Kanonik proje belgesi**  
> Sürüm: 0.3  
> Son güncelleme: 3 Eylül 2026  
> Belge sahibi: Ana GDD bakım sohbeti

Bu dosya, DEEPCLEAN'in güncel tasarım yönünü diğer proje sohbetleri için ortak ve okunabilir hâle getirir. Eski PDF ve beyin fırtınası metinleri tarihsel kaynaklardır; bundan sonraki çalışmalarda güncel kanonik kaynak bu dosyadır.

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

**ÇALIŞMA KARARI:** DEEPCLEAN; emekliye ayrılmış endüstriyel temizlik dronu B-404 ile ilk bakışta ezici yoğunluktaki sualtı çalışma sahalarını temizlediğimiz; tek bir çok amaçlı vakum, fizik sistemleri ve dünya içi küçük işler üzerinde giderek ustalaşıp batıkları ve ekosistemleri kalıcı biçimde hayata döndürdüğümüz birinci şahıs bir sualtı iş ve restorasyon simülasyonudur.

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

- Oyuncu bir insan dalgıç değil, **B-404** adlı modifiye edilmiş endüstriyel temizlik dronudur.
- B-404 ağır sanayi hizmetinden emekliye ayrılmış ve sualtı geri dönüşüm işi için yeniden donatılmıştır.
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

**Örnek güç basamakları:**

- **Operatör:** Nesneleri tek tek işler; dar menzil ve küçük depo nedeniyle öncelik belirler.
- **Uzman:** Kümeleri işler, doğru başlık ve filtre kombinasyonunu seçer, akıntıdan yararlanır.
- **Saha mühendisi:** Kirlilik kaynağını, akıntı yönünü, geçici toplayıcıları ve makineleri kurarak bütün bir alanı kontrollü biçimde çözer.

Geç oyun, oyuncu girdisi olmadan ekranı silmemelidir. Oyuncu zincirleme temizliği **kurar, başlatır ve yönetir**. Böylece Keep on Mining'deki güçlenme hazzı korunurken oyunun fiziksel ustalığı geçersizleşmez.

**ADAY:** Önceden tamamlanmış erken bölgelere isteğe bağlı geri dönüş; yeni araçlarla eski, zor alanların çok daha hızlı temizlenmesini ve saklı hedeflerin açılmasını sağlar. Bu geri dönüşler zorunlu içerik tekrarı değil, güç farkını gösteren kısa ustalık kontratları olmalıdır.

---

## 6. Madde, kirlilik ve fizik sistemleri

### 6.1 Modüler madde sistemi

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

**ÇALIŞMA KARARI:** Bu klasördeki eski yapay zekâ konseptleri kanonik üretim görseli değildir; geçici fikir ve envanter referansıdır.

Yararlı tarafları:

- Turkuaz su, renkli mercan, paslı tekne ve yoğun çöp kontrastını hızlıca gösterir.
- Tekne, ağır atık, küçük çöp, değerli eşya, bitki ve canlı kategorileri için başlangıç çeşitliliği sunar.
- Alanların ilk anda dolu ve göz korkutucu görünmesi fikrini destekler.

Sorunları:

- Çoğu görsel ressamsı anahtar görsel niteliğindedir; birinci şahıs oynanış okunabilirliğini kanıtlamaz.
- Renk doygunluğu ve nesne yoğunluğu bazı karelerde görev hedeflerini kaybettirir.
- Nesne ölçeği, malzeme dili, tekne detayları ve stil seviyesi görseller arasında tutarlı değildir.
- Bazı çöp setleri fazla oyuncak/mobil oyun estetiğine yaklaşır; yapay zekâ kaynaklı biçim ve yazı hataları içerir.

**YENİ KONSEPT PAKETİ İÇİN HEDEF:** Sanat dili kesinleştiğinde mevcut görsellerin üzerine üretim kararı verilmemeli; aşağıdaki kontrollü set hazırlanmalıdır:

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

**ÇALIŞMA KARARI:** Tam üretim kapsamından önce aşağıdaki tek bölüm oyunun kimliğini doğrulamalıdır:

- Bir küçük merkez/atölye alanı.
- Bir ana sualtı bölgesi ve tek büyük batık.
- Vakumlama, ters itiş/fırlatma ve kazıma.
- En az üç davranış bakımından farklı madde türü.
- Bir aktif kirlilik kaynağı ve onu durduran fizik problemi.
- Sarmaşık Yengeci veya eşdeğer bir sistemik canlı.
- Bir kayıp eşya/hikâye zinciri.
- Belirgin önce/sonra ekolojik dönüşümü.
- En az üç niteliksel ekipman seçimi.
- Aynı alan içinde en az bir görev modülü veya belirgin ritim değişimi.
- Erken ve geliştirilmiş araç arasında aynı iş üzerinde açıkça hissedilen verim/strateji farkı.
- Yaklaşık 8-15 dakikalık anlamlı dalış ritmi.

Dikey dilimin temel testi: Oyuncu yalnızca daha hızlı temizlemek istememeli; alanın nasıl çalıştığını anlamak, altında ne olduğunu görmek ve geri döndüğünde dünyanın nasıl değiştiğini merak etmelidir. Güçlenme yeni bir sayıdan ibaret kalmamalı; oyuncunun aynı yoğun sahayı ele alma biçimini görünür şekilde değiştirmelidir.

---

## 17. Ön üretim karar ve doğrulama planı

### 17.1 Güncel çekirdek kimlik

**ÇALIŞMA KARARI:** DEEPCLEAN'in ayırt edici formülü:

> **Yoğun sualtı temizliği + kademeli endüstriyel ustalık + dünya içine bağlı değişken görevler + kalıcı ekolojik dönüşüm**

Yeni bir özellik bu dört parçadan en az birini güçlendirmiyor veya aralarındaki bağı derinleştirmiyorsa üretim kapsamına alınmamalıdır.

### 17.2 Tasarım sırası

1. **Çekirdek vaat:** Vakum hissi, yoğunluk-okunabilirlik dengesi ve önce/sonra dönüşümü doğrulanır.
2. **Mekanik matrisi:** Mevcut madde, kuvvet, makine ve ekoloji davranışları listelenir; hangi birleşimlerin gerçekten farklı karar ürettiği test edilir.
3. **Güç eğrisi:** Aynı test sahası Operatör, Uzman ve Saha Mühendisi seviyelerinde oynatılır; yalnızca süre değil, kullanılan yöntem değişmelidir.
4. **Seviye grameri:** Öğretim cebi, ana problem, kirlilik kaynağı, görev modülü, kahraman nesne ve dönüşümden oluşan bir gri kutu bölüm kurulur.
5. **Görev modülleri:** Tam oyun için dört ila altı tekrar kullanılabilir aday belirlenir; dikey dilimde yalnızca en güçlü iki tanesi prototiplenir.
6. **İlerleme/RPG ve ekonomi:** Önceki testlerden sonra dallanma, kredi, araştırma ve uzmanlık yapısı tasarlanır.
7. **Sanat hedefi:** Oynanış kamerası ve seviye yapısı doğrulandıktan sonra tutarlı konsept paketi ve sanat kılavuzu hazırlanır.
8. **Gelişmiş üretim:** Ancak bu kapılardan sonra yeni büyük fizik sistemleri ve içerik üretimi genişletilir.

### 17.3 Dikey dilim kabul ölçütleri

- İlk 10 saniyede oyuncu alanın durumunu, ana işi ve görsel dönüşüm vaadini anlayabilir.
- Yoğun sahne zengin görünür fakat etkileşim hedefleri kaybolmaz.
- İlk dakikalarda temel vakum eylemi kendi başına tatmin edicidir.
- Bir yükseltme oyuncunun yalnızca hızını değil, çalışma yöntemini de görünür biçimde değiştirir.
- 8-15 dakikalık örnek dalış en az üç ana etkileşim fiili ve bir doğal ritim değişimi içerir.
- Oyuncu kirliliğin kaynağını bulup durdurduğunda alan kalıcı olarak değişir.
- Görev modülü ana oyundan kopuk hissettirmez ve sonradan başka bir seviyede yeniden kullanılabilir.
- Prototip, oyunun "bir sonraki güç seviyesinde bu alanı nasıl temizlerdim?" merakını oluşturur.

## 18. Değişiklik günlüğü

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

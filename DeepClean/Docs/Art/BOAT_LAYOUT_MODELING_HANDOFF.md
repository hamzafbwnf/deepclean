# Tekne — bugünkü modelleme görevi

Durum: Yerleşim ve hareket taslağı. GDD 0.7 geçerli; yeni kesin ekipman veya ölçü kararı değildir. Ayrıntılı malzeme, pas, vida ve son model üretimi bu görevin dışında.

## Amaç

Mevcut tekne gövdesi ve kamara korunarak Operatör servis erişimi, Uzman kilit mekanizması ve Saha Mühendisi numune çıkarımının aynı mekâna sığıp sığmadığını görünür kılmak. Yeni gövde deliği açılmadan önce mevcut güverte açıklığı kullanılır.

## Yerleşim A — geçici çalışma önerisi

- Orijinal referanstaki açık çalışma güvertesinde bulunan büyük dikdörtgen açıklık servis girişi adayıdır. Gerçek modeldeki karşılığı ve oyuncu geçiş hacmi doğrulanır.
- Giriş kızağı, açıklığın üzerine kapanır ve güvertenin daha uzun boşluk sunan yönüne tamamen çekilir. İskele/sancak seçimi gerçek geometriye göre yapılır; dar borda şeridine zorla sığdırılmaz.
- Açıklığın altındaki erişilebilir iç hacim, Uzman kilit mekanizmasının SERVİS TARAFI için yer ayırma alanıdır. Bu bölüm görselde aşağıda olarak etiketlenir; ikinci bir güverte makinesi gibi eklenmez.
- Numune yatağı için açık güvertenin diğer boş bölümünde, teknenin boyuna yakın doğrultuda yer ayrılır. Numunenin çıkacağı boş mesafe ayrıca gösterilir. Bu hacim ilk kızağın park alanıyla, girişle ve dolaşım yoluyla çakışamaz.
- Numune kilitlerinin iç servis tarafı ile güvertedeki yatak arasında mekanik bağlantı GÜZERGÂHI için yer ayrılır; geometrisi henüz tasarlanmış sayılmaz.
- Karşı ağırlık ve olası vinç/yük desteği, numune yatağına bağlı tek bir destek grubu olarak basit hacimle temsil edilir. Halat güzergâhı ve işlevi kesinleşmemiştir.
- Filtre, ayırıcı ve numune rafları için ancak ana çalışma hacimleri sığdıktan sonra yer ayrılır. İlk kızağın üzerindeki kutunun filtre görevi ADAYDIR; dekoratif makine olarak zorunlu değildir.

## Önce referans ölçek

Mevcut projeden B-404'ün çarpışma genişliği, yüksekliği ve gerekli dönüş alanı alınır. Bunlar hazır değilse kullanılan temsilî hacim açıkça GEÇİCİ diye işaretlenir. Kamera görüntüsünden metre tahmin edilmez.

Servis girişinin net ölçüsü oyuncu geçiş hacmi + tasarımda seçilecek pay kadar olmalıdır. Kapalı taşıyıcı açıklığı örter. Park konumunda açıklık, mil, ray, motor veya gövde tarafından kesilmez. Taşıyıcının gereken hareketi, hareket yönündeki açıklığı tamamen boşaltacak kadar olmalıdır; boş park alanı yetersizse ray yönü değiştirilir. Sığmayan sistem için gövde otomatik büyütülmez.

## Bugün oluşturulacak ayrı basit parçalar

1. Sabit çerçeve ve iki kılavuz ray.
2. Açıklığı kapatan hareketli taşıyıcı; ilk taslakta üst ekipman basit kutu olabilir.
3. Geçişin dışında kalan TEK vidalı mil ve iki sabit destek.
4. Taşıyıcıya bağlı somun bloğu; mil döndüğünde taşıyıcı doğrusal hareket eder.
5. Sabit dişli kutusu ve oyuncunun erişebileceği servis yuvası.
6. Hareketi durduran ayrı metal takoz ve temas ettiği sabit dayanak.
7. Kapalı ve açık konum dayanakları.
8. Diğer iki mini oyun için isimlendirilmiş basit yer ayırma hacimleri; detaylı model yok.

Vidalı milin gerçek diş geometrisi bu aşamada gerekli değildir; silindir yeterlidir. Hareketli ve sabit parçalar tek mesh olarak birleştirilmez. Taşıyıcının yerel hareket ekseni ve milin dönme ekseni belirgin tutulur.

## Dört kontrol pozu

A — Kapalı: oyuncu geçemez, servis yuvasına dışarıdan erişilebilir.
B — Takılmış: taşıyıcı kısmen açılmış, takoz görünür ve tutma aracının ulaşacağı aralık vardır; tam geçiş henüz yoktur.
C — Yük boşaltılmış: taşıyıcı biraz geri alınmış, takoz serbesttir ama erişim aralığı kapanmamıştır. B ve C'nin ikisi birden geometrik olarak mümkün olmalıdır.
D — Açık: takoz çıkarılmış, taşıyıcı tamamen park etmiş, oyuncu geçiş hacmi açıklıktan ve içerideki varış alanından kesintisiz geçer.

## Teslim

- Mevcut teknenin üstten ekran görüntüsü: giriş, park, numune yatağı, çıkarım boşluğu ve dolaşım gösterilsin.
- İlk mekanizmanın A/B/C/D durumlarını aynı kameradan gösteren dört görüntü.
- İç bölüm bağlantısını gösteren basit yan kesit; gizli hacim uydurmak yerine mevcut gövdeye göre çizilsin.
- Çakışan veya sığmayan yerlerin kısa listesi.

Başarı: şık görünmekten önce geçiş, erişim, hareket ve yerleşim anlaşılmalı. Bu taslak onaylanmadan nihai topoloji/malzeme üretimine başlanmaz.

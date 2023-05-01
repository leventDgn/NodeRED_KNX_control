# Node RED Tabanlı Ev Otomasyon Sistemi

KNX ev otomasyon sistemlerinde ev otomasyon sistemini internete açmak, çeşitli senaryolar oluşturmak için çeşitli firmaların geliştirmiş olduğu Touch paneller kullanılmaktadır. Bu touch paneller genelde 7 ila 10 inç büyüklüğünde bir ekrana sahip üzerinde Android ya da Linux işletim sistemleri koşan cihazlardır. Touch paneller genelde ithal ürünlerdir yine Türk markası ile piyasaya sürülen ürünlerde ODM olarak yabancı üreticiler tarafından ürettirilmektedir. Bu sebeple bu cihazlar birçok kullanıcı için ulaşılabilir değildir. Bu cihazların fiyatları 750 Eurolar mertebesinden başlamaktadır. Ayrıca üzerindeki ekran ve güçlü donanım da cihazların fiyatlarının çok yukarılara çıkmasına sebep olmaktadır. 

Bu projede önermiş olduğumuz sistemle düşük maliyetli bir ev otomasyon merkez kumandası gerçekleştirilmektedir. Bu ürünü gerçekleştirebilmek için ürün maliyetini arttıran kalemler üzerinde tek tek düşünüldü. Cihazın mevcut fonksiyonlarını azaltmadan uygun maliyetli bir ürün tasarlayabilmek için cihaz üzerindeki ekrandan feragat edildi. Bu ekran yerine zaten herkesin sahip olduğu akıllı cihazlar ile görselleştirme yoluna gidildi.

Bu projenin temel amacı, yüksek maliyetli ev otomasyon merkezi kontrol birimlerine düşük maliyetli bir alternatif sunmaktır. Bu proje ile Orange Pi Zero üzerinde koşan nodeRED tabanlı bir uygulama tasarlanacaktır. Bu uygulama akıllı evlerde kullanılan touch panellere düşük maliyetli bir alternatif oluşturacaktır. Bu ürün sayesinde ev otomasyon sistemleri insanlar için bir lüks olmaktan çıkıp daha ulaşılabilir bir hale gelecektir. Aşağıdaki resimde sistemin blok diyagramı görülmektedir.

![image](https://user-images.githubusercontent.com/35852515/235485711-d91e675e-9cc4-42dc-a9fc-bf70b39eb531.png)

 

# Proje Bileşenleri

## Orange Pi Zero
Orange Pi Zero, Raspberry Pi'ye benzeyen tek kartlı bir bilgisayardır. Ev otomasyonu, robotik ve IoT dahil olmak üzere çeşitli uygulamalar için tasarlanmıştır. Bu cihaz, düşük maliyeti, küçük boyutu ve güçlü performansı gibi bir dizi avantaj sunar.
 

Orange Pi Zero'nun ana avantajlarından biri düşük maliyetli olmasıdır. Bu cihaz, piyasadaki diğer tek kartlı bilgisayarlardan önemli ölçüde daha ucuzdur. Bu sayede düşük bütçeli projeler için uygun bir seçenek haline gelir. Ek olarak, Orange Pi Zero'nun küçük boyutu, çeşitli ortamlarda taşınmasını ve kullanılmasını kolaylaştırır. 
Orange Pi Zero'nun bir diğer avantajı da güçlü performansıdır. Küçük boyutuna rağmen, bu cihaz bir dizi uygulamayı çalıştırabilir ve karmaşık görevleri kolaylıkla yerine getirebilir. Güçlü performansı, onu yüksek performanslı tek kartlı bir bilgisayar arayanlar için ideal bir seçim haline getirir. İster bir IoT projesi geliştiriyor, ister bir robot inşa ediyor olun, Orange Pi Zero tüm bu işlerin üstesinden kolayca gelebilecek kabiliyettedir.

Detaylı Özellikler

 Özellik | #Açıklama |
--- | --- |
İşlemci |(SOC)	Alwinner H2 Dört Çekirdek Cortex A7 (H.265/HEVC 1080P)
Grafik İşlemci (GPU) |	Mali400MP2 @600 MHZ (OpenGL ES 2.0 Desteği)
Bellek (RAM)|	256 / 512 MB DDR3
Depolama	|SD Card (maks. 64 GB)
Ağ Bağlantısı	|10/100M Ethernet
Kablosuz Ağ Bağlantısı|	Alwinner XR810, 802.11 b/g/n (u.Fl anten kablosu )
Görüntü Çıkışları	| GPIO Genişleme Kartı ile.
Ses Giriş / Çıkışları |	GPIO Genişleme Kartı ile.
USB Bağlantıları |	1 x USB 2.0
Micro USB Bağlantıları	| 1 x micro USB 2.0 OTG Desteği
Dahili Sensörler	| GPIO Genişleme Kartı ile.
Sata Bağlantısı	| GPIO Genişleme Kartı ile.
Kamera Bağlantısı	| -
GPIO Geliştirici Pinleri	| 26pin (Raspberry Pi ile benzer yapıda)
13pin (2x USB, IR pin, AUDIO)
Hata Giderme (DEBUGGING)	| Seri Konsol ile UART
Buton Led ve Özellikleri	| Güç butonu.
Güç Kaynağı	| Micro USB çıkışından güç alır.
Ürün Boyutları ve Ağırlığı |	48mm x 46mm – 22gr



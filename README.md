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
GPIO Geliştirici Pinleri	| 26pin (Raspberry Pi ile benzer yapıda), 13pin (2x USB, IR pin, AUDIO) 
Hata Giderme (DEBUGGING)	| Seri Konsol ile UART
Buton Led ve Özellikleri	| Güç butonu.
Güç Kaynağı	| Micro USB çıkışından güç alır.
Ürün Boyutları ve Ağırlığı |	48mm x 46mm – 22gr


# NodeRED
Node-RED, IoT uygulamaları için tasarlanmış açık kaynaklı bir programlama aracıdır. Kullanım kolaylığı, esneklik ve çok yönlülük gibi bir dizi avantaj sunar.
Node-RED'in ana faydalarından biri kullanım kolaylığıdır. Bu programlama aracı, kullanıcı dostu olacak şekilde tasarlanmıştır ve programlama deneyimi çok az olan veya hiç olmayan kişiler tarafından kullanılabilir. Node-RED, kullanıcıların yazılım bileşenlerini sürükleyip bırakmasına izin vererek karmaşık akışlar oluşturmayı kolaylaştıran görsel bir programlama arabirimi sağlar.
Node-RED ayrıca oldukça esnek ve çok yönlüdür. Bir dizi programlama dilini destekler ve çeşitli cihaz ve hizmetleri entegre etmek için kullanılabilir. Bu, onu karmaşık IoT uygulamaları geliştirmek isteyenler için önemli bir araç haline getirir. 
Node-RED, yukarıdaki avantajların yanı sıra, aygıtları ve hizmetleri entegre etmeyi kolaylaştıran önceden oluşturulmuş çeşitli yazılım bileşenleri ve akışlar da sağlar. Ayrıca, MQTT, HTTP, TCP ve UDP gibi çoklu iletişim protokollerini de desteklemektedir.

# Geliştirme Aşamaları

## Orange Pi Zero'ya Armbian Kurulumu
Armbian, ARM tabanlı cihazlarda çalışmak üzere tasarlanmış, Debian tabanlı hafif ve verimli bir işletim sistemidir. Bu bölümde, Armbian'ı Orange Pi Zero'ya nasıl kuracağımızı anlatacağım.

## Armbian'ı İndirme
Armbian'ı Orange Pi Zero'nuza kurmanın ilk adımı, uygun görüntü dosyasını indirmektir. Orange Pi Zero için Armbian'ın en son sürümünü resmi https://www.armbian.com/orange-pi-zero/ web sitesinden indirebilirsiniz. Ben buradan Arbian 23.02 Bullseye versiyonunu indirdim.

![image](https://user-images.githubusercontent.com/35852515/235507154-2ba76057-1dd5-4630-a309-8ad735d1369a.png)

## SD Kartı Hazırlama
Armbian görüntü dosyasını indirdikten sonra, SD kartınızı hazırlamanız gerekecektir. En az 8 GB kapasiteli bir microSD karta ihtiyacınız olacak. SD kartı bilgisayarımızın kart okuyucu bölümüne takıyoruz.
Şimdi, Armbian görüntü dosyasını SD karta yazmanız gerekecek. Bunu yapmak için ben Etcher adında bir uygulama kullandım. Bu uygulamayı https://etcher.download/download-etcher/ adresinden indirebilirsiniz.
Echer uygulamasını açıyoruz. Daha sonra “Flash from file” düğmesine tıklayıp indirmiş olduğumuz Armbian imajını seçiyoruz. Yükleme yapacağımız SD kartı seçip "Flash!" butonuna basıp yazma işleminin tamamlanmasını bekliyoruz.

![image](https://user-images.githubusercontent.com/35852515/235507244-afbe57c4-d078-4b20-a43b-e3af8136196d.png)

## Orange Pi Zero'yu Başlatma
Armbian görüntüsü SD karta yazdırıldığında, artık SD kartı Orange Pi Zero'nun microSD kart yuvasına takabilirsiniz. Kartı microUSB portundan bilgisayarımıza bağlıyoruz. Bu usb portundan hem kartımızı besliyor hem de haberleşiyor olacağız.
Bilgisayarımızdan bir terminal programını açarak seri port üzerinden kartımıza bağlanıyoruz. Ben kullanım kolaylığı açısından Tera Term programını kullanmayı tercih ediyorum. Seri portu açtığımızda aşağıdaki gibi bir ekran karşımıza çıkıyor.
![image](https://user-images.githubusercontent.com/35852515/235507352-a58b05c3-b137-4bcc-97d7-95b124e58647.png)

Kurulum sürecini tamamlamak için ekrandaki talimatları izliyoruz. İlk olarak root şifresini belirlememiz gerekiyor. Daha sonra sırasıyla kullanıcı adı, kullanıcı şifresi ve sahip adı bilgilerini giriyoruz. Son olarak açılan wifi listesinden kendi ağımızı seçip ağ şifresini giriyoruz. 
![image](https://user-images.githubusercontent.com/35852515/235507415-b0154f4e-862c-430f-bcc0-25cd91064094.png)

Kurulumu tamamlamış olduk. Konsol ekranımız aşağıdaki gibi görünüyor. Artık nodered kurulumuna geçebiliriz.
![image](https://user-images.githubusercontent.com/35852515/235507479-83c7e22f-0644-4fa9-9956-ef270d3694dd.png)

# Node-RED'i Orange Pi Zero'ya Kurmak
Node-RED'i bir Orange Pi Zero'ya kurmak istiyorsanız, doğru yere geldiniz. Node-RED, cihazlarınız için kolay ve hızlı bir şekilde uygulamalar oluşturmanıza olanak tanıyan Nesnelerin İnterneti (IoT) için tasarlanmış açık kaynaklı bir programlama aracıdır. Bu yazımızda, Orange Pi Zero üzerinde Node-RED kurulum adımlarını izleyeceğiz.

## Node-RED nedir?
Node-RED, IoT uygulamaları için tasarlanmış akış tabanlı bir programlama aracıdır. Farklı görevleri gerçekleştiren önceden oluşturulmuş kod parçaları olan düğümleri bağlamayı ve yapılandırmayı kolaylaştıran web tarayıcısı tabanlı bir düzenleyici kullanır. Node-RED ile çok fazla kod yazmak zorunda kalmadan IoT cihazlarınız için hızlı bir şekilde prototip oluşturabilir ve uygulamalar geliştirebilirsiniz.

## Node-RED'i Orange Pi Zero'ya Kurmak
Node-RED'i Orange Pi Zero'ya kurmak için şu adımları izlemeniz gerekir:

1.	Öncelikle Orange Pi Zero'nuzu internete bağlamanız gerekiyor. Bunu bir ethernet kablosu bağlayarak veya bir Wi-Fi bağlantısı kurarak yapabilirsiniz.
2.	Ardından, Orange Pi Zero'nuzda bir terminal penceresi açmanız gerekir.
3.	Node-RED'i yüklemek için aşağıdaki komutu çalıştırın:
 ```
bash <(curl -sL https://raw.githubusercontent.com/node-red/linux-installers/master/deb/update-nodejs-and-nodered)
 ```

4.	Node-RED kurulduktan sonra, aşağıdaki komutu çalıştırarak başlatabilirsiniz:

 ```
node-red-start
 ```

5.	Bir web tarayıcısı açın ve Node-RED editörüne erişmek için http://YourOrangePiZeroIPAddress:1880` adresine gidin. NodeRED editörü aşağıdaki gibi açılacaktır.
![image](https://user-images.githubusercontent.com/35852515/235507645-73ab052c-e2ab-4bc5-9ac3-7e5fed78b2af.png)
 
 6.	Opi’yi resetlediğimizde nodeRED otomatik olarak başlamıyor bu problemi çözmek için aşağıdaki komutla nodeRED servisini enable etmemiz gerekiyor.
 
 ```
 sudo systemctl enable nodered.service
 ```
 # NodeRED'de KNX Kontrolü Nasıl Oluşturulur
 NodeRED, kullanıcıların farklı cihazlar ve hizmetler arasında veri akışı oluşturmasını sağlayan güçlü bir görsel programlama aracıdır. KNX ev sistemi de dahil olmak üzere bir dizi farklı donanım cihazını kontrol etmek için kullanılabilir. NodeRED üzerinde bir KNX kontrolü oluşturma adımları şunlardır:
 
## 1. Adım: KNX Kontrol Noktalarını Kurun

Node-RED üzerinde bir KNX kontrolü oluşturmanın ilk adımı, KNX kontrol noktalarını kurmaktır. Bu kontrol noktaları, kullanıcıların KNX sisteminden veri gönderip almasına izin verir. KNX kontrol noktalarını kurmak için, kullanıcılar Node-RED Palet Yöneticisine gidebilir ve "node-red-contrib-knx" için arama yapabilir.

## 2. Adım: Akışa KNX Kontrol Noktalarını Ekleyin

KNX kontrol noktalarını kurulduktan sonra, kullanıcılar bunları Node-RED akışlarına ekleyebilir. Bu, KNX kontrol noktalarını akış tuvaline sürükleyip bırakılarak yapılabilir.
 
## 3. Adım: KNX Kontrol Noktalarını Yapılandırın

Kullanıcıların, akışa eklenen KNX kontrol noktalarını KNX sistemlerine bağlanacak şekilde yapılandırması gerekmektedir. Bunu, kontrol noktalarına çift tıklayarak, grup adresi ve bağlantı detayları gibi gerekli bilgileri girerek yapabilir.

## 4. Adım: Bir Kontrol Arayüzü Oluşturun

KNX kontrol noktaları yapılandırıldıktan sonra, kullanıcılar KNX sistemleri için bir kontrol arabirimi oluşturabilir. Akış tuvaline anahtarlar, kaydırıcılar ve düğmeler gibi kontrol noktaları eklenebilir ve ardından bunlar KNX kontrol noktalarına bağlanabilirler.

## 5. Adım: Bulut bağlantısı üzerinden kontrol

Yapılandırılan akış ve oluşturulan kontrol arabirimi ile kullanıcılar akışı Node-RED sunucularına gönderebilir. Bu, KNX sistemlerini internet vasıtası aracılığıyla dünya üzerindeki herhangi bir yerden kontrol etmelerini sağlayacaktır.

# Sonuç
Orange Pi Zero, düşük maliyeti, küçük boyutu ve güçlü performansı ile güvenilir ve verimli tek kartlı bir bilgisayar arayan herkes için ideal bir seçimdir.
Armbian, Orange Pi Zero gibi ARM tabanlı cihazlarda çalışmak için güçlü ve verimli bir işletim sistemidir.
Node-RED, IoT uygulamaları geliştirmek için güçlü bir araçtır ve Orange Pi Zero'ya kurulumu kolaydır. Bu yazıda özetlenen adımları izleyerek Orange Pi Zero'nuzda Node-RED'i hızlıca kullanmaya başlayabilir ve kendi IoT uygulamalarınızı geliştirmeye başlayabilirsiniz.
Sonuç olarak, Node-RED üzerinde bir KNX kontrolü oluşturmak, evdeki bir dizi farklı cihazı otomatikleştirmenin ve kontrol etmenin kolay ve kullanışlı bir yoludur. Kullanıcılar, yukarıda anlattığım adımları takip ederek, kendi özel ihtiyaç ve gereksinimlerine göre uyarlanmış, KNX sistemlerini kolaylıkla kontrol etmelerine olanak tanıyan özel bir kontrol ara yüzünü hızlı bir şekilde oluşturabilir.

 

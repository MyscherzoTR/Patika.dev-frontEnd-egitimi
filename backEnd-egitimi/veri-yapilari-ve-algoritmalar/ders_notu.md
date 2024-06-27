# Veri Yapıları ve Algoritmalar Ders Notu

## 1. Temel Kavramlar

### A. Algoritma nedir

Algoritma belirli bir durumdan başlayıp belirli bir sonuçta biten problemlere çözüm getiren adımlar bütünüdür.

- Kaynak Siteler
    * https://tr.wikipedia.org/wiki/Algoritma
    * https://tr.khanacademy.org/computing/computer-science/algorithms
    * https://tr.khanacademy.org/computing/computer-science/algorithms/intro-to-algorithms/v/what-are-algorithms

### B. Makine Dili (0 ve 1)

İkili sayılarda bulunan **0 ve 1 rakamları (bit)**, bilgisayarın elektrik iletimi için kullandığı transistörlerin ***(elektrik akımı iletir)*** açık veya kapalı olma durumunu gösterir. Transistörlerde iki tane komut vardır, 0 (kapat, elektrik geçmiyor/yok) ve 1 (aç, elektrik geçiyor/var).

- Bytecode => **Java derleyicisinin (Java Compiler)** Java ile yazılmış kodların makine dili yerine kendine has oluşturduğu Binary (0 ve 1) dosyasıdır.

- JVM => Java Bytecode formatına derlenmiş programların çalışmasını sağlayan bir sistemdir.

- Kaynak Siteler
    * [BİL-110 Bilgisayara Giriş](https://slideplayer.biz.tr/slide/2798593/)
    * [Compiler (Derleyici) ve Interpreter (Yorumlayıcı) Nedir?](https://medium.com/@msenell/derleyi%CC%87ci%CC%87-compiler-ve-yorumlayici-interpreter-%C3%BCzeri%CC%87ne-bi%CC%87r-deneme-d8656619ef6)
    * [Java - Bytecode](https://tr.wikipedia.org/wiki/Java_bytecode)

### C. Sayı Tabanları (İkilik ve Onluk)

- [Onluk Tabanından İkilik Tabana Çevirme Kod Örneği](https://prog.asmaamir.com/e-tabancevirme)

### D. Binary Symbols - Araştır?

Sayısal olmayan verilerin bir sembol olduğunu ve 0 ve 1'lerdan oluştuğunu hep birlikte öğrendik. Binary olarak gördüğümüz ifade makine kodundan dolayı farklı bir nesneyi işaret edebilir.

### E. Bilgisayarda Verilerin Tutulması

Bilgisayar, yapısından dolayı içerisinde tutulabilecek veri miktarı sınırlıdır. Bu verilerin en küçük yapı taşları bitlerdir. *Bilgisayar hafızasında ki bir kutucuğa **1 bit** denir*. Kutucuk arttıkça bit sayısıda artar yani ***2 kutucuk varsa 2 bit*** demektir bu. bitler 0 ve 1'lerden oluşur.

Bu bitleri bir hafıza gibi düşünebiliriz. Ne kadar çok bit dolar ise boyut o kadar artar ve daha az veri depolama alanımız kalır. 8 kutucuk yan yana geldiğinde yani 8 bit olduğunda 1 Byte deniyor. ***8 bit = 1 Byte*** adlandırma ile alakalı bir şey. **Metre, Santimetre gibi düşünülebilir tamamen adlandırma.**

Peki 1 Bayt ne kadar farklı şey ifade edebiliyor. 8 kutucuk olduğu için *2^8'den 256 farklı şey ifade edebiliyor.*

Hadi gelin ***bit ve byte kavramlarını*** görsel ile örneklendirelim.
![bit ve byte kavramları](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/veri-tutulma/figures/veri-tutulma.png)

- (1 Byte = 8 bit)  demiştik. 8 bit yani 2^8 = **256 farklı şey, sembol ifade eder ve bu işimizi görmeyebilir, yetersiz kalabilir.** Bu durumda 256 sembolden daha fazla bir depolama alanı isteyebiliriz. Peki bu durum da ne yapacağız? Aslında çözüm çok basit Byte'ları yan yana koyarak depolama alanımızı arttıracağız.

Diyelim yan yana 4 Byte koyduk. Yani 4*8'den 32 bit koymuş olduk. Bu da *2^32 farklı şey, sembol ifade eder.*

***Dipnot: 4 Byte yazılımda integer(int) ifade eder.***

Hemmen bir örnek çözelim.
![bigger bit](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/veri-tutulma/figures/veri-tutulma2.png)

- Binary semboller, kullanan kişiye göre farklılık gösterebilir. Örneğin, 00 sembolü Ali'ye göre k karakterini sembolize ederken, Veli'ye göre 1 sayısını sembolize edebilir.
![Veri Sembolleri](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/veri-tutulma/figures/sembol-veri.png)

- Kaynak Siteler
    * [Bit Nedir](https://tr.wikipedia.org/wiki/Bit_(bili%C5%9Fim))
    * [Byte Nedir](https://tr.wikipedia.org/wiki/Bayt)

### F. Recursion - Araştır?

- Kaynak Siteler
    * [Youtube - Veri Yapıları Ders 8 Rekürsif Yapılar](https://www.youtube.com/watch?v=PNWOP_QoBGI&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU&index=9)
    * [Youtube - Recursive Fonksiyonlar Nasıl Çalışır ve Örnek Kodlama](https://www.youtube.com/watch?v=cv7CY8UmFL0)
    * [Youtube - Java Dersleri #43 - Recursive (Özyineli) Metotlar](https://www.youtube.com/watch?v=I3_wU5fr3Zo)
    * [Youtube - Öz Yineleme (Recursion) - Veri Yapıları Ders 02](https://www.youtube.com/watch?v=qT-Fh2kxR6s)
    * [Recursive fonksiyonlar ve Python ile Hanoi Kuleleri çözümü](https://www.youtube.com/watch?v=4GvMYiPLRtU)

<hr>

## 2. Veri Yapıları

### A. Array - Araştır?

- Kaynak Siteler
    * [Array Nedir?](https://medium.com/@denizf.b/array-nedir-d9b7afd44ca2)

### B. Linked List - Araştır?

- Linked-List (Bağlı listeler), yan yana zorunluluğu olmadan veri tutmamızı sağlayan yapılardır. Yeni gelen eleman için hafıza'da yeni bir alan açmamız gerekmez. Array'dan farklı olarak elemanlar hafıza içerisinde farklı yerlerde olabilir fakat son gelen eleman kendinden bir önceki elemana ***her zaman adresini bildirmek*** zorundadır.
![Linked-List](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/linked-list/figures/linked-list.png)

Yukarıdaki örnekte gördüğünüz üzere, her bir düğüm bir sonrakinin adresini tutar. Her bir önceki eleman bir sonraki eleman ile bağlıdır.

- Kaynak Siteler
    * [Youtube - Veri Yapıları Ders 2 Listeler](https://www.youtube.com/watch?v=hnE9_7VBKyI&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU&index=3&t=591s)
    * [Youtube - Veri Yapıları Ders 3 Bağlı Listeler (Tek Yönlü,İki Yönlü,Dairesel)](https://www.youtube.com/watch?v=7vjRwtDP0J4&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU&index=4)
    * [Linked List Nedir](http://cagataykiziltan.net/veri-yapilari-data-structures/1-linked-list-bagli-listeler/)

### C. Linked List vs Array - Farklarını Detaylı Araştır?

+Array, **Memory locality *(araştır)* için iyi.**
+Array, Veriye sabit sürede ulaşmaya ***Random Access*** denir ve Arraylerin böyle özelliği vardır.
+Linked List, **eleman ekleme ve silme Array'e göre daha kolay.**
+Linked Listlerde ilgili elemanı bulmak için tek tek sırasıyla elemanları kontrol etmek gerekir.
- ![LinkedList-vs-Array](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/linked-list-array/figures/array-vs-linkedlist-diff.png)

- Kaynak Siteler
    * [Veri Yapılarına Giriş ve Linked List Mantığı](https://ceyhuncozvelioglu.medium.com/kendime-notlar-1-veri-yap%C4%B1lar%C4%B1na-giri%C5%9F-ve-linkedlist-mant%C4%B1%C4%9F%C4%B1-5944bcbb8165)
    * [Dizi (Array) ile Bağlı Liste (Linked List) Arasındaki Farklar](https://www.ysancar.com/veri-yapilari/dizi-ile-bagli-liste-arasindaki-farklar/)

### D. Lindked List Eleman Ekleme/Silme - Detaylı Araştır?

*pointer* araştır.

- Eleman Ekleme/Çıkarma için **3 Elamanlı bir hücre oluşturduk.**
![3 Elamanlı bir hücre oluşturduk](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/linked-list-add-delete/figures/ilk-ad%C4%B1m.png)
- Eleman Ekleme
Adresi #12 olan 22 sayısını listeye eklemek istiyoruz. Yapmamız gereken 6 hücresine 22 sayısının adresini yazmak.
![Eleman Ekleme](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/linked-list-add-delete/figures/eleman-ekleme.png)
- Eleman Çıkarma
Adresi #20 olan 6 numaralı hücreyi çıkarmak/silmek istiyoruz. Linked-List'de bir önceki eleman bir sonraki elamanın hafızada ki adresini tutuyordu. Yani 7 numaralı hücrede 6 numaralı hücrenin adresi tutulmakta.
22 numaralı hücrenin adresini temp bir değişkende vb. tutuyoruz. 6 numaralı hücreyi siliyoruz sonrasında 7 numaralı hücreye 22 nin adresini yazıyoruz.
![eleman Çıkarma](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/linked-list-add-delete/figures/eleman-%C3%A7%C4%B1karma.png)

- Kaynak Siteler
    * [Doğrusal Veri Yapıları 2 - Bağlı Liste (Linked List)](https://medium.com/@tolgahan.cepel/do%C4%9Frusal-veri-yap%C4%B1lar%C4%B1-2-ba%C4%9Fl%C4%B1-liste-linked-list-8e5d3d84c41f)

### E. Stack (LIFO) - Detaylı Araştır!

Stack, LIFO (Last in First out) (En son giren en önce çıkar) mantığına dayanan, elemanlar topluluğundan oluşan bir yapıdır. Gelin hemen örneğimize geçelim. Taşınırken topladığınız koli kutusu düşünün. İçerisinde kitaplar var ve en, boy olarak koliye tam olarak koyuluyor. Mantıken kolinin altı kapalı ve üst üste koymanız gerekmektedir. Yeni taşındığınız yerde çıkartırken en üstekinden başlarsınız. İşte stack (Yığın) da aynı mantıkta çalışıyor.

Yığınlara eleman eklerken veya çıkartırken bazı methodlar uygulanır. Bunlardan biri push, diğeri ise pop. Push, yığının üzerine eleman eklemek için kullanılır (Koliye kitap koymak). Pop ise, yığından eleman çıkarmak için kullanılır.

- Örnek Push ve Pop
![Örnek Push ve Pop](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/stack/figures/stack.png)
    
    * Push: Stack'e eleman eklemek (yığının üstüne tabak koymak). Her seferinde koyulan tabak en üstteki yani son tabak olur.
    * Pop: Stack'ten eleman almak. Yığının en üstünden tabak almak. En son tabak en üstteki olduğu için yığından tabak aldığımızda üstten alırız.

- Kaynak Siteler
    * [Youtube - Veri Yapıları Ders 4 Yığıt (Stack) Yapısı]()
    * [stack-kod-örneği](https://www.baskent.edu.tr/~tkaracay/etudio/ders/prg/dataStructures/Collections/ClassStack.pdf)

### F. Queue (FIFO) - Detaylı Araştır?

Queue (Kuyruk), FIFO (First in First out) (İlk giren ilk çıkar) prensibine dayanan, girişlerde ve çıkışlarda belirli bir kurala göre çalışan yapıdır. Stack de verdiğimiz örneği kuyruğa göre uyarlayalım. Biz örnekte altı kapalı bir koli kutusunu düşünmüştük. Şimdi o koli kutusunun altı yırtılmış. Sonuç olarak ne oluyor? İlk giren ilk çıkmış oluyor.

Queue (Kuyruk)'da eleman eklemesi yaparken enqueue methodunu kullanıyoruz. Eleman silerken ise dequeue methodunu kullanıyoruz.

- Örnek engueue ve dequeue
![Örnek engueue ve dequeue](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/queue/figures/queue.png)

    * Enqueue: Yeni elemanın Kuyruğa eklenmesi (yeni birinin sıraya girmesi)
    * Dequeue: Elemanın Kuyruktan çıkarılması (sırası gelenin sıradan çıkması/işi bitenin sıradan ayrılması)
- Kaynak Siteler
    * [Youtube - Veri Yapıları Ders 5 Kuyruk Kavramı](https://www.youtube.com/watch?v=W-wCqjKSpys&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU&index=6)
    * [Doğrusal Veri Yapıları 4 - Kuyruk (Queue) Kodlu Örnek](https://medium.com/@tolgahan.cepel/do%C4%9Frusal-veri-yap%C4%B1lar%C4%B1-4-kuyruk-queue-dcbd07e8ba77)

### G. Hash Function(Karma Fonksiyonu)/ Hash Table(Karma Tablosu) - Detaylı Araştır?

- Indexleme
Arraylerde 0 bazlı bir indexleme vardır. Bazı programlama dillerin de 1 bazlı indexlemeler olsa da genel olarak 0 bazlı indexleme kullanılır. Yani 0'dan başlar index sayısı.
![Indexleme](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/hash-table/figures/Indexleme.png)
- Hash Function(Karma Fonksiyonu)/ Hash Table(Karma Tablosu)
Hash Table(Karma Tablosu), key value prensibine dayanan bir array kümesidir. Key olarak çağırdığınız elemanın değerini (value) yansıtır. 
Hash Table yerine dizileri kullanabilirdik. Fakat her ürünü ve fiyatını tek tek aramak istemediğimiz için hash table kullanıyoruz. Peki bu süreç nasıl işliyor? Hemen bir örnek yapalım. Örneğimiz bir kuru yemiş dükkanından gelecek.
![yok](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/hash-table/figures/%C3%B6rnek-ilk-k%C4%B1s%C4%B1m.png)
    
    * Bu kısımda ilk olarak bulunan ürün sayımız kadar sayısı olan bir Array oluşturduk. 8 ürün varsa 8 elemanlı bir array. ***Yukarıda ki görselde olduğu gibi;***
    * Daha sonra hash fonksiyonundan ürünleri (ürün isimlerini) geçirerek fonksiyonun sonucunda çıkan sayısal değeri **index değeri** olarak kullanacağız. ***Yukarıda ki görselde olduğu gibi;***
    * Her ürün için bir index değeri belirlenmiş oldu ve bu indexler ilk başta oluşturduğumuz Array'in indexleri. Bu indexlerde ürünlerin fiyatlarını tutacağız. ***Aşağıda ki görselde olduğu gibi;***

![yok](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/hash-table/figures/%C3%B6rnek-ikinci-k%C4%B1s%C4%B1m.png)
Şifrelendiği için artık her badem keyi gönderildiğinde 85TL, fıstık keyi gönderildiğinde ise 69 sonucu verecektir.

Özetle, elimizde var olan verileri bir fonksiyondan geçirip indexliyoruz. Bu fonksiyona hash function(karma fonksiyonu), bu fonksiyon ile birleştiğimiz dizi yapısına ise Hash Table(Karma Tablosu) diyoruz.

- Kaynak Siteler
    * [Youtube - Hash Table #13](https://www.youtube.com/watch?v=jhc-KG3htrM)
    * [Youtube - Hash Table (Karım Tablosu, Özet Tablosu) Veri Yapıları 22. Video](https://www.youtube.com/watch?v=_TCkO3DnVs4)

### H. Hash Function(Karma Fonksiyonu)

Hash Function (Karma Fonksiyonu), karma fonksiyonu olabilmesi için bazı temel şartlar vardır.Bunlar;

- Gönderdiğimiz ***anahtarlar (keys) farklı*** olmasına rağmen aynı sonuçları alıyorsak bu bir ***hash function*** değildir.
    * *Farklı girdilere farklı sonuç/çıktı vermeli!*
- Fonksiyona gönderilen ***anahtarlar aynı*** fakat sonuç farklı ise ***hash function*** değildir.
    * *Hash Function sonucu her seferinde aynı girdiye aynı sonuç/çıktı vermeli!*
- Hash Table(Karma Tablosu) için kullanılan dizinin boyutu verilen sonuçların sayısı kadar olmalıdır. Kaç key varsa o kadar elemanlı olmalı dizi(array).
    * *Hash functiondan 8 değer döndü dizinin boyutu 8 elemanlı olmalıdır.*

Fakat her zaman tutarlı olmuyor. Bazen **Collision** dediğimiz sorun ortaya çıkıyor.
- Farklı girdiye farklı sonuç veremiyor. Farklı çıktılar aynı sonuçlar doğurabiliyor.

- Kaynak Siteler
    * [Youtube - Hash Function #14](https://www.youtube.com/watch?v=ZX-1qPSYC_k)
    * [Youtube - Veri Yapıları Ders 9 / Hash Fonksiyonları 1](https://www.youtube.com/watch?v=OYiNo0BTVxQ&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU&index=10)
    * [Youtube - Veri Yapıları Ders 10 / Hash Fonksiyonları - 2](https://www.youtube.com/watch?v=jxwcjv12TG8&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU&index=11)
    * [Youtube - Veri Yapıları Ders 11 / Hash Fonksiyonları - 3](https://www.youtube.com/watch?v=Vcr3LizkCuo&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU&index=12)
    * [Youtube - Veri Yapıları Ders 12 / Hash Fonksiyonları - 4](https://www.youtube.com/watch?v=5h5mBf4k2do&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU&index=13)

### I. Hash Collision

Hash Function'da ***farklı iki değerden aynı sayı üretilirse*** bu duruma ***Collison (çarpışma)*** denir. Bu olay istediğimiz bir durum değildir.

- Hash Function'lar bazen farklı durumlar için farklı sonuçlar üretemeyebilir. *Örnek verelim;*
    * Araçları bir hash function dan geçirelim. Bu fonksiyonumuz **araçların son harflerine** göre değer atasın. Motor ve tır, bunların son harfleri ***"R"*** olduğu için fonksiyon çıktısında aynı değerler verilir ve bu **collision'a neden olur.**
- Collision sorunuyla az karşılaşabilmek için kaliteli bir hash function olmalı. Bu sayede verimli bir Hash Table elde etmiş oluyoruz.
- Çarpışma sayısı arttıkça aradığımız şeyi bulma hızı azalır.

- Kaynak Siteler
    * [Youtube - Hash Collision #15](https://www.youtube.com/watch?v=FD7nKLnrguE)

<hr>

## 3. Algoritma Analizi

### A. Algoritma Analizi Giriş

- Algoritma analizi, bir algoritmanın çalışabilmesi için gerekli koşulların sağlanıp sağlanamadığını gösteren bir parametredir.
-Algoritma analizi, var olan kaynaklara göre en uygun algoritmayı seçmek için uygulanır. Peki algoritma analizi en iyi nasıl yapılır? Kulağa karmaşık geliyor ama çok basit. Programlama dillerinden ve donanımlardan bağımsız bir şekilde Algoritma analizi yapılmalıdır. Aksi taktirde en uygun sonuç alınamayabilir.
- Donanımlar veya programlama dilleri farklı cihazlarda aynı performansı vermeyebilir. Örnek verecek olursak, cep telefonları için uygulama tasarladığımızı varsayalım. Bu uygulamanın performansı Apple telefonlar için farklı, Android telefonlar için farklı, arasında donanım farklı olanlar için ayrı olacaktır. Donanım ve diller ile algoritma analizi pek sağlıklı değildir.

- Kaynak Siteler
    * [Youtube - Algoritma Analizi #16](https://www.youtube.com/watch?v=Pi32FSu1TNg)
    * [Derinlemesine Algoritma Analizi](https://birhankarahasan.com/algoritma-analizi-nedir-zaman-karmasikligi-big-o-gosterimi)

### B. Ram Modeli

Bir algoritmayı farklı cihazlarda denemek bize pek fazla bir sonuç çıkarmıyordu. Çünkü kaynaklar değişebiliyordu. Bu probleme genel bir çözüm getirebilmek için hayalî bir cihaz düşünelim. Bu cihaz üzerinde bütün algoritmaları çalıştırdıktan sonra bize bir sonuç verecek. Kısacası; **genellenebilir bir analiz yapmak için her algoritmayı aynı bilgisayar ile test ediyor gibi düşüneceğiz.**

Bu hayalî cihaza ***RAM (Random Access Machine)*** diyoruz. Ram, algoritmalar arasındaki farkları belirlemek için kullanacağımız bir araç olacak.

- Her işlemin birim zamanı mevcuttur. Bunlara örnek;
    * Döngüler kaç defa işlem yapıyorsa (işlem sayısı * kaç kere tekrar edeceği) o kadar birim zaman alır.
    *Toplama, Çıkarma, and, or gibi *basit aritmetik/logic işlemler* 1 birim zaman alır.
    * Hafızadan her okuma işlemi 1 birim zaman alır.

- Kaynak Siteler
    * [Youtube - Ram Modeli(Random Access Machine) #17](https://www.youtube.com/watch?v=lrHoiZig3Z8)
    * [ChatGPT - RAM Modeli ve Kullanımı](https://chatgpt.com/share/5acbf049-521c-4593-90b5-44b9cc4b4b48)

### C. Time Complexity

Algoritmanın verimli olması için belli kurallar vardır. ***Örnek: Raflara kitap yerleştirmek.***

- Kitapları, gelişigüzel raflara dağıtırsak aradığımız kitabı daha fazla zamanda bulabiliriz. Aslında bu bir ***[worst case](https://bilgisayarkavramlari.com/2008/12/22/en-kotu-durum-analizi-worst-case-analysis/)***'dir. Beklenilen en kötü durum(vereceğimiz inputun algoritmamızı en yavaş/en fazla işlem yapacak şekilde çalıştırdığı durum). Kitapları filtrelememiz gerekir. Kalın olanları bir rafa, ince olanları bir rafa, küçük boyutta olanları bir rafa koyduğumuz zaman aradığımız şeyi daha rahat bulabiliriz. Algoritma, en kötü senaryoya ne kadar hazırsa, bizi o kadar memnun edebilir.
- Algoritmalar için genellikle sık kullanılan ***average case***'dir. Kısacası genel olarak beklenilen durum. Kitapların bölümüne göre kaç tane olduğunu biliyorsak average case kullanabiliriz. En büyük rafı miktarı fazla olana ayırabiliriz. Input yoksa average zordur!!!!
- Bir diğer senaryomuz ise ***best case***'dir. Beklediğimiz en iyi durum(vereceğimiz inputun algoritmamızı en hızlı şekilde çalıştırdığı durum). Kitap örneğine devam edecek olursak, bütün kitapların ayrı raflarda olması, alfabeye göre sıralanması best case olarak ifade edilebilir. Çünkü aradığımızı rahatlıkla bulabiliyoruz.

- Kaynak Siteler
    * [Youtube - Time Complexity #18](https://www.youtube.com/watch?v=Ie_Ax6KLI80)
    * [Youtube - Algoritma Analizi ve Big O (Time Complexity, Space Complexity)](https://www.youtube.com/watch?v=wMp0BrWaoz8)
    * [worst case nedir?](https://bilgisayarkavramlari.com/2008/12/22/en-kotu-durum-analizi-worst-case-analysis/)

### D. Nedir Bu “Big O Notation”?

***Bu örnekleme worst case(en kötü duruma) göre yapılan bir örneklemedir!***

1000 sayfalık bir sözlük düşünelim. **Normal bir A algoritması** 1.sayfadan başlayıp aranılan kelimeyi sayfa sayfa tarar. Bu çok fazla işlem yükü ve beraberinde zaman kaybı getirir.

Bu seferde **B algoritması** diyelim. Sözlük alfabetik olarak sıralanmıştır. Aradığımız kelime için ilk olarak sözlüğü 2'ye böleriz. ***Sol da ilk 500 sayfa sağda son 500 sayfa olarak.*** Sonra aradığımız kelimeye bakarız. Eğer ilk 500 sayfa içinde ki harflerle eşleşiyorsa sağdaki yani son 500 sayfayı eleriz. Tam tersi durumda ise sağ daki 500 sayfa ile eşleşirse bu sefer ilk 500 sayfayı eleriz. Böylece elimizde her **durumda sadece 500 sayfalık** arama yapılacak yer kalmış olur.

Şuan elimizde ***sadece 500 sayfa kaldı.*** Bu sayfalar içinde aynısını yapıyoruz. Yine 2'ye bölüyoruz. Sol ve sağ olarak yine kontrol ediyoruz. Böyle böyle yani 2'ye böle böle aramamız gereken alanı azaltıyoruz. En son elimizde aradığımız kelimeye ait sayfa kalıyor ve bu sayfada da **aynı yöntemi yaparak(bu sefer sayfayı 2'ye bölüyoruz sürekli)** kelimeyi buluyoruz.

1000 sayfalık sözlüğün tamamını teker teker aramak yerine böyle bir yöntemle çok daha az efor ve kısa zamanda aradığımız kelimeyi bulmuş oluyoruz. ***Yani problem her seferinde yarı boyutuna inmiş oluyor.***

Bu örnek 1000 sayfalık bir sözlükte yapılan bir değerlendirmeydi. Algoritmanın faydalı olup olmaması bir çok faktöre/input(sözlük boyutu, aranılan kelime vb.) bağlı olabilir. 10.000 sayfalık bir sözlükte çok daha hızlı olacaktır son sayfalardaki kelimeyi ararken.

***Worst Case örneği değil! Bir dipnot daha iyi anlaşılması için;* Fakat diyelim ki ilk sayfa da bizim aradığımız kelime. Bu durumda **normal A algoritması çok daha hızlı çalışacaktır** Çünkü 1.sayfadan taramaya başladığı için direkt bulacaktır ama B algoritması sürekli sözlüğün ortasından 2'ye böldüğü için çok daha fazla vakit ve işlem alacaktır. Buna rağmen B algoritmasının Worst Case A algoritmasının worst case'inden daha iyi olacaktır. Çünkü A algoritması için Worst Case en sonuncu sayfa artık sözlük kaç sayfa ise.

#### İşte bu noktada devreye **"Big O Notation"** girer. ***Peki nedir bu Big O Notation?;***

Bog o natation algoritmanın ne kadar sürede çalışacağını bize söylemeyecej. Bize algoritmamızın çalışma zamanının inputun boyutu ile nasıl değişeceğini söyleyece/gösterecek.

Input Boyutuna(input size), *n* diyelim. Algoritmamızın en kötü durumda n işlem yapması beklenir. Inputum n boyutunda olunca çalışma süremin de en kötü durumda n olmasını *O(n)* ile göstereceğim. Aynısı B algoritması için de geçerli *O(logn)*

Kısacası A algoritması input size göre sürekli artış gösterirken B algoritması bir süre sonra sabit zamanda işlemler(arama vb.) yaptırır.

Big O notation da yapılacak toplam işlem sayısının input size ile nasıl scale olacağına bakıyoruz. Bizim için fonksiyonun yapısı önemli. İşlem sayısı nasıl artıyor; Linear, karesi ile orantılı, logaritmik mi nasıl? Big o notaion bana bunu vermiş oluyor.

- Kaynak Siteler
    * [Youtube - Big O Notation #19](https://www.youtube.com/watch?v=AeeSlV64TOI)
    * [Nedir Bu “Big O Notation”?](https://medium.com/kodcular/nedir-bu-big-o-notation-b8b9f1416d30)
    * [Algoritma Karmaşıklığı (Big-O)](https://medium.com/algorithms-data-structures/algoritma-karma%C5%9F%C4%B1kl%C4%B1%C4%9F%C4%B1-big-o-5f14316890a4)

<hr>

## 4. Sorting (Sıralama) Algoritmaları

### A. Sorting Nedir?

Sorting, kendinden sıralama algoritmaları olarak bahsetmektedir. Sorting, bir eleman dizisini, belirli sıralama kurallarına göre sıralama yapar.

**Searcing: Elemanları en başta sıralamak, eleman aramayı hızlandırabilir.**

Sıralama algoritmaları kullanmamızdaki amaç, algoritmanın isminden de anlaşılacağı üzere sahip olduğumuz veriyi en hızlı şekilde büyükten küçüğe ya da küçükten büyüğe bir sıraya sokmak. Bunun için kullanılan bir çok sıralama algoritması vardır. Bazısı çok hızlı ama yazımı zor, bazısı az sayıda veri için çok hızlı, bazısının da yazması kolaydır.

Herhangi bir sayıdaki tip verilerin sınırlı bellek ve işlem gücü ile belirli bir sıraya göre dizilmesinin sağlanmasıdır. Burada önemli olan en optimum bellek ve performans ikilisini verecek bir algoritmanın elde edilmesidir.

- Sıralama algoritmalarının bazı kriterlere göre sınıflandırılabiliriz:
    * **Bellek Kullanımı:** Çalışırken ek bellek ihtiyacı duyan algoritmalarda kullanılabilecek bir ölçüttür buna ek olarak ayrıca da sıralama işleminin yapılması sırasında hafızanın kullanımına göre de sıralama algoritmaları; Harici sıralama (External Sort) ve Dahili Sıralama (Internal Sort).
    * **Hesaplama Karmaşıklığı:** Oluşturulmuş olan algoritmanın yaptığı işlem sayısının genel bir yapı ile ifade edilmesidir. Temel üç grup ölçek kullanılır. Bunlar en iyi (best), ortalama (average) ve en kötü (worst) durumu olarak belirtilir. İşlem yoğunluğu zaman işleyişiyle paralel olduğundan (ne kadar çok işlem yapılırsa o kadar uzun süre geçer) algoritmanın işleyiş süresini de etkiler.
    * **Yerdeğiştirmenin Karmaşıklığı:** İçerisinde ek bellek kullanmayan (in place) algoritmalarda kullanılan karşılaştırılabilmesi için önemli bir ölçüttür.
    * **Durağanlık(stability):** Algoritmanın uygulanması sırasında sıralanmış bir verinin tekrar sıralamaya tabi tutulup tutulmadığını belirten ölçektir.
    * **Rekürsiflik:** İç içe kendi kendini çağıran algoritmalarda kullanılan bir ölçüttür. Burada en önemli kriter stack dediğimiz maksimum iç içe çağırım kapasitesine dikkat edilmesi ve bu kapasitenin kullanılma sıklığıdır.
    * **Fakat en önemli kriterler**
        + Hafıza Verimliliği (Memory efficiency)
        + Zaman Verimliliği (Time efficiency)

- Aşağıda bazı sıralama algoritmaları verilmiştir:
    * Seçerek Sıralama (Selection Sort)
    * Eklemeli Sıralama (Insertion Sort)
    * Kabuk Sıralaması (Shell Sort)
    * Birleştirmeli Sıralama (Merge Sort)
    * Hızlı Sıralama (Quick Sort)
    * Kabarcık Sıralaması (Bubble Sort)

#### *Sıralama Algoritmalarının Karşılaştırılması

Sık kullanılan sıralama algoritmalarının, verinin karmaşıklığına göre gösterdiği performans:

![Sıralama Algoritmalarının Karşılaştırılması](https://www.halildurmus.com/wp-content/uploads/2021/01/593-Siralama-Algoritmalarini-Karsilastirma-1.png)

- Kaynak Siteler
    * [Youtube - Sorting #20](https://www.youtube.com/watch?v=v3Z6crtZVek)
    * [Sıralama Algoritmaları (Sorting Algorithms)](https://www.halildurmus.com/2021/02/22/siralama-algoritmalari-sorting-algorithms/)
    * [Sıralama Algoritmaları](https://serdarkuzucu.com/siralama-algoritmalari/)

### B. Insertion Sort

En basit sorting algoritmalarından biridir.

Yerleştirerek sıralama işlevi belirli bir anda dizinin belirli bir kısmını sıralı tutarak ve bu kısmı her adımda biraz daha genişleterek çalışmaktadır. Sıralı kısım işlev son bulunca dizinin tamamına ulaşmaktadır. Elemanların sırasına uygun olarak listeye tek tek eklenmesi ile gerçekleştirilen sıralamadır.

 ```python
    for i in range(1,len(arr)):
        deger = arr[i]
        j = i-1
        while(j>= 0 and deger < arr[j]):
            arr[j+1] = arr[j]
            j -= 1
        arr[j+1] = deger
 ```

 ![Eklemeli Sıralama (Insertion Sort) Nasıl Çalışır?](https://www.halildurmus.com/wp-content/uploads/2021/01/Insertion-Sort-Algorithms.gif)

 - Kaynak Siteler
    * [Youtube - 2 dakikada Insertion Sort](https://www.youtube.com/watch?v=JU767SDMDvA&list=PL9xmBV_5YoZOZSbGAXAPIq1BeUf4j20pl&index=4)
    * [Youtube - Veri Yapıları Ders 34 Insertion Sort](https://www.youtube.com/watch?v=0lpT0XUy29Q&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU&index=35)
    * [Insertion Sort Data Structure and Algorithm Tutorials](https://www.geeksforgeeks.org/insertion-sort/)

### C. Selection Sort

En basit sorting algoritmalarından biridir.

![Selection Sort](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/insertion-sort/figures/insertion-sort.png)

Verilen örüntüye ait ***en küçük elemanı buluyor ve en baştaki sayı ile yer değiştiriyor.*** Peki ya devamı? İkinci en küçük elemanı buluyor ve 2. sıra ile değiştiriyor. Baktın ki ***2.sıradaki eleman en küçük hiç dokunma!!!. Hemen 3. sıraya geç.*** 4, 5 derken dizi bitti. İşte insertion sort'un temel çalışma prensibini öğrendin.

![Selection Sort](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/insertion-sort/figures/insertion-sort.png)

- Kaynak Siteler
    * [Youtube - Insertion Sort #21(Adı yanlış yazılmış)](https://www.youtube.com/watch?v=GBXm2h4Eu-0)
    * [Youtube - 3 dakikada Selection Sort](https://www.youtube.com/watch?v=JU767SDMDvA&list=PL9xmBV_5YoZOZSbGAXAPIq1BeUf4j20pl&index=4)
    * [Youtube - Veri Yapıları Ders 32 Selection Sort](https://www.youtube.com/watch?v=Hr-cghhg-Co&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU&index=33)
    * [Youtube - Veri Yapıları Ders 33 Selection Sort Örnek 2](https://www.youtube.com/watch?v=DzgmtogFFfw&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU&index=34)
    * [Selection Sort Data Structure and Algorithm Tutorials](https://www.geeksforgeeks.org/selection-sort/)

### D. Merge Sort

Selection Sort'da, Big-O gösteriminden dolayı input'um arttığında ***n^2*** olduğunda dolayı çalışma zamanı artıyor.

Peki daha hızlı bir şekilde sıralama yapılabilir mi? Evet, Merge Sort burada yardımımıza koşuyor. Bir listeyi her adımda parçaya ayırıp tek eleman kalıncaya kadar bölüyor. Böldükten sonra sıralı bir şekilde bize sunuyor (Performans).

![Merge Sort](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/merge-sort/figures/merge-sort.png)

![Merge Sort](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/merge-sort/figures/big-o-merge.png)

Selection Sort'da, time complexity ***n^2*** olduğundan ötürü çalışma zamanımız artıyordu. Merge sort'da ise ***nlogn*** olduğu için açık ara performans olarak daha iyi diyebiliriz.

- Kaynak Siteler
  * [Youtube - Merge Sort #22](https://www.youtube.com/watch?v=Sx1VfR7EvnA)
  * [Youtube - 3 dakikada Merge Sort](https://www.youtube.com/watch?v=4VqmGXwpLqc)
  * [Youtube - Birleştirme Sıralaması (Merge Sort) ve Parçala Fethet (Divide and Conquer) (Algoritma Analizi 10)](https://www.youtube.com/watch?v=f9CNp_uuNJg)
  * [4. BİRLEŞTİRMELİ SIRALAMA (MERGE SORT)](http://cagataykiziltan.net/algoritmalar/1-siralama-algoritmalari/4-birlestirmeli-siralama/)
  * [Birleştirme Sıralaması (Merge Sort)](https://bilgisayarkavramlari.com/2008/08/09/birlestirme-siralamasi-merge-sort/)

### E. Quick Sort

Hızlı sıralama günümüzde çok yaygın olarak kullanılan bir sıralama algoritmasıdır. N tane sayıyı ***average case e göre big-o nlogn***, ***worst case e göre big-o n^2*** karmaşıklığı ile sıralanır.

![Quick Sort](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/quick-sort/figures/Quicksort.png)

İlk olarak bir pivot belirler bu pivota göre pivottan küçük ve eşitler sol kısmına, pivottan büyük ve eşitler sağ kısmına yazılır. Parçalanmış kısımlar yeni bir pivot belirlenerek parça pinçik edilir.

- Kaynak Siteler
  * [Youtube - Quick Sort #23](https://www.youtube.com/watch?v=EikA3rBMD18)
  * [Youtube - 4 dakikada Quick Sort](https://www.youtube.com/watch?v=JU767SDMDvA&list=PL9xmBV_5YoZOZSbGAXAPIq1BeUf4j20pl&index=4)
  * [Quick Sort (Hızlı Sıralama Algoritması) Veri Yapıları 13](https://www.youtube.com/watch?v=aubOM9dOy6c)
  * [Quick Sort (Hızlı Sıralama) Nedir?](https://medium.com/@turgay2317/quick-sort-h%C4%B1zl%C4%B1-s%C4%B1ralama-nedir-2d6555e5f7e2)
  * [Algoritma Dersleri – Quick Sort](https://www.mobilhanem.com/algoritma-dersleri-quick-sort/)
  * [Hızlı Sıralama Algoritması (Quick Sort Algorithm)](https://bilgisayarkavramlari.com/2008/08/09/hizli-siralama-algoritmasi-quick-sort-algorithm/)

<hr>

## 5. Searching (Arama) Algoritmaları

### A. Searching Nedir?

Günümüzde veriler gitgide artan bir hal alıyor. Her insanın bir bilgisayarı ve telefonu olduğunu düşünürsek, terabaytlarca veri ediyor. Arama algoritmaları ise istediğim özellikteki verinin elimdeki veri setlerinde aranıp, bulunup getirilmesi demek. Bunun hızlı olmasına önem gösterilir.

- Kaynak Siteler
  * [Arama Algoritmaları (Search Algorithms)](https://bilgisayarkavramlari.com/2009/11/23/arama-algoritmalari-search-algorithms/)
  * [Arama Algoritmaları (Search Algorithms) Nedir?](https://enesates03.medium.com/arama-algoritmalar%C4%B1-search-algorithms-nedir-7c8be09d541a)

### B. Linear Search

Linear search, tek tek elemanları dolandıktan sonra istediğim elemanın olup olmadığına bakmaktır. En basit arama algoritmasıdır. Örneğin;

- [20,25,46,48] veri setini ele alalım. Benim aradığım eleman 25. İlk elemana gidiyorum ve değeri 20 sen değilsin diyorum. İkinci elemana gidiyorum ve değeri 25 evet sensin diyorum. Linear search algoritmam burada bitmiş oluyor.

- Big-o ya göre incelediğimizde bizim worst case'imiz neydi? Elemanın dizinin sonunda bulunmasıydı. Bu sebepten ötürü n elemanımız varsa big-o notasyonumuz otomatik olarak n oluyor.

- Kaynak Siteler
  * [Youtube - Linear Search #25](https://www.youtube.com/watch?v=fPGqKlUKh7c)
  * [Youtube - Her Yazılımcının Bilmesi Gereken Algoritmalar - Lineer Arama(Linear Search) ve Python ile Kodlaması](https://www.youtube.com/watch?v=hPVJJyXFr-c)
  * [Doğrusal & İkili Arama Algoritmaları (Linear & Binary Search Algorithms)](https://medium.com/@ozgurmehmetakif/do%C4%9Frusal-i%CC%87kili-arama-algoritmalar%C4%B1-linear-binary-search-algorithms-ed5fefc1f003)
  * [Doğrusal Arama (Linear Search)](https://bilgisayarkavramlari.com/2008/11/09/dogrusal-arama-linear-search/)

### C. Binary Search

İkili arama algoritması, elimizde bulunan veri dizisini sıralı olduğunu varsayıyor, bu durumu değiştirerek sonuca varmak istiyor.

- İkili arama algoritması, diziyi her seferinde ikiye bölerek ikili arama yapar. Sıralı bir listem var ise benim Big-o logn olarak karşımıza çıkıyor.

- Aradığım sayı **15** ve benim değer kümem ***[10,15,20,16,22,36,23]*** diyelim. Binary Search bu diziyi manipüle ederek şu ifadeye dönüştürüyor. ***[10,15,16,20,22,23,36]***. *36 sayısını en yüksek sayı, 10 sayısını en düşük sayı ilan ediyor.* Benim aradığım sayı ile ortada kalan sayıyı kıyaslıyor eğer benim aradığım sayım küçükse kendinden büyük bütün sayıları siliyor. Ve kendine yeni bir ortanca belirliyor. Böylelikle gereksiz arama yapmaktan kurtarıyor. ![Binary Search](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/binary-search/figures/binary-search.png)

- Kaynak Siteler
  * [Youtube - Binary Search #26](https://www.youtube.com/watch?v=cvsZCh_0H9A)
  * [Youtube - 4 dakikada Binary Search](https://www.youtube.com/watch?v=fDKIpRe8GW4)
  - [Youtube - İkili Arama Algoritması(Binary Search Algorithm)](https://www.youtube.com/watch?v=Bi9zq4bS4Hw)
  * [Doğrusal & İkili Arama Algoritmaları (Linear & Binary Search Algorithms)](https://medium.com/@ozgurmehmetakif/do%C4%9Frusal-i%CC%87kili-arama-algoritmalar%C4%B1-linear-binary-search-algorithms-ed5fefc1f003)
  * [İkili Arama Algoritması (Binary Search Algorithm)](https://bilgisayarkavramlari.com/2009/12/21/ikili-arama-algoritmasi-binary-search-algorithm/)
  * [Big O Notation ve Binary Search](https://medium.com/@alifurkangokce/big-o-notation-ve-binary-search-d6f3d4cf4574)
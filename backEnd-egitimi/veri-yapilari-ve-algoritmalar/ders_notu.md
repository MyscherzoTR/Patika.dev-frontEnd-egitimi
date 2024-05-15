# Veri Yapıları ve Algoritmalar Ders Notu


## 1. Temel Kavramlar

#### A. Algoritma nedir;

Algoritma belirli bir durumdan başlayıp belirli bir sonuçta biten problemlere çözüm getiren adımlar bütünüdür.

- Kaynak Siteler
    * https://tr.wikipedia.org/wiki/Algoritma
    * https://tr.khanacademy.org/computing/computer-science/algorithms
    * https://tr.khanacademy.org/computing/computer-science/algorithms/intro-to-algorithms/v/what-are-algorithms

#### B. Makine Dili (0 ve 1);

İkili sayılarda bulunan **0 ve 1 rakamları (bit)**, bilgisayarın elektrik iletimi için kullandığı transistörlerin ***(elektrik akımı iletir)*** açık veya kapalı olma durumunu gösterir. Transistörlerde iki tane komut vardır, 0 (kapat, elektrik geçmiyor/yok) ve 1 (aç, elektrik geçiyor/var).

- Bytecode => **Java derleyicisinin (Java Compiler)** Java ile yazılmış kodların makine dili yerine kendine has oluşturduğu Binary (0 ve 1) dosyasıdır.

- JVM => Java Bytecode formatına derlenmiş programların çalışmasını sağlayan bir sistemdir.

- Kaynak Siteler
    * [BİL-110 Bilgisayara Giriş](https://slideplayer.biz.tr/slide/2798593/)
    * [Compiler (Derleyici) ve Interpreter (Yorumlayıcı) Nedir?](https://medium.com/@msenell/derleyi%CC%87ci%CC%87-compiler-ve-yorumlayici-interpreter-%C3%BCzeri%CC%87ne-bi%CC%87r-deneme-d8656619ef6)
    * [Java - Bytecode](https://tr.wikipedia.org/wiki/Java_bytecode)

#### C. Sayı Tabanları (İkilik ve Onluk);
- [Onluk Tabanından İkilik Tabana Çevirme Kod Örneği](https://prog.asmaamir.com/e-tabancevirme)


#### D. Binary Symbols - Araştır!
Sayısal olmayan verilerin bir sembol olduğunu ve 0 ve 1'lerdan oluştuğunu hep birlikte öğrendik. Binary olarak gördüğümüz ifade makine kodundan dolayı farklı bir nesneyi işaret edebilir.

#### E. Bilgisayarda Verilerin Tutulması
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

#### F. Recursion - Araştır!

- Kaynak Siteler
 * [Youtube - Recursive Fonksiynlar Nasıl Çalışır ve Örnek Kodlama](https://www.youtube.com/watch?v=cv7CY8UmFL0)
 * [Java Dersleri #43 - Recursive (Özyineli) Metotlar](https://www.youtube.com/watch?v=I3_wU5fr3Zo)


<hr>


 ## 2. Veri Yapıları 

 ### A. Array - Araştır!
 - Kaynak Siteler
    * [Array Nedir?](https://medium.com/@denizf.b/array-nedir-d9b7afd44ca2)

### B. Linked List - Araştır!
- Linked-List (Bağlı listeler), yan yana zorunluluğu olmadan veri tutmamızı sağlayan yapılardır. Yeni gelen eleman için hafıza'da yeni bir alan açmamız gerekmez. Array'dan farklı olarak elemanlar hafıza içerisinde farklı yerlerde olabilir fakat son gelen eleman kendinden bir önceki elemana ***her zaman adresini bildirmek*** zorundadır.
![Linked-List](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/linked-list/figures/linked-list.png)

Yukarıdaki örnekte gördüğünüz üzere, her bir düğüm bir sonrakinin adresini tutar. Her bir önceki eleman bir sonraki eleman ile bağlıdır.

- Kaynak Siteler
    * [Linked List Nedir](http://cagataykiziltan.net/veri-yapilari-data-structures/1-linked-list-bagli-listeler/)

### C. Linked List vs Array - Farklarını Detaylı Araştır!
+Array, **Memory locality *(araştır)* için iyi.** 
+Array, Veriye sabit sürede ulaşmaya ***Random Access*** denir ve Arraylerin böyle özelliği vardır.
+Linked List, **eleman ekleme ve silme Array'e göre daha kolay.** 
+Linked Listlerde ilgili elemanı bulmak için tek tek sırasıyla elemanları kontrol etmek gerekir.
- ![LinkedList-vs-Array](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/linked-list-array/figures/array-vs-linkedlist-diff.png)

- Kaynak Siteler
    * [Veri Yapılarına Giriş ve Linked List Mantığı](https://ceyhuncozvelioglu.medium.com/kendime-notlar-1-veri-yap%C4%B1lar%C4%B1na-giri%C5%9F-ve-linkedlist-mant%C4%B1%C4%9F%C4%B1-5944bcbb8165)
    * [Dizi (Array) ile Bağlı Liste (Linked List) Arasındaki Farklar](https://www.ysancar.com/veri-yapilari/dizi-ile-bagli-liste-arasindaki-farklar/)

### D. Lindked List Eleman Ekleme/Silme - Detaylı Araştır!
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
    * [stack-kod-örneği](https://www.baskent.edu.tr/~tkaracay/etudio/ders/prg/dataStructures/Collections/ClassStack.pdf)

### F. Queue (FIFO) - Detaylı Araştır!
Queue (Kuyruk), FIFO (First in First out) (İlk giren ilk çıkar) prensibine dayanan, girişlerde ve çıkışlarda belirli bir kurala göre çalışan yapıdır. Stack de verdiğimiz örneği kuyruğa göre uyarlayalım. Biz örnekte altı kapalı bir koli kutusunu düşünmüştük. Şimdi o koli kutusunun altı yırtılmış. Sonuç olarak ne oluyor? İlk giren ilk çıkmış oluyor.

Queue (Kuyruk)'da eleman eklemesi yaparken enqueue methodunu kullanıyoruz. Eleman silerken ise dequeue methodunu kullanıyoruz.

- Örnek engueue ve dequeue
![Örnek engueue ve dequeue](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/queue/figures/queue.png)

    * Enqueue: Yeni elemanın Kuyruğa eklenmesi (yeni birinin sıraya girmesi)
    * Dequeue: Elemanın Kuyruktan çıkarılması (sırası gelenin sıradan çıkması/işi bitenin sıradan ayrılması)
- Kaynak Siteler
    * [Doğrusal Veri Yapıları 4 - Kuyruk (Queue) Kodlu Örnek](https://medium.com/@tolgahan.cepel/do%C4%9Frusal-veri-yap%C4%B1lar%C4%B1-4-kuyruk-queue-dcbd07e8ba77)

### G. Hash Function/ Hash Table - Detaylı Araştır!
- Indexleme
Arraylerde 0 bazlı bir indexleme vardır. Bazı programlama dillerin de 1 bazlı indexlemeler olsa da genel olarak 0 bazlı indexleme kullanılır. Yani 0'dan başlar index sayısı.
![Indexleme](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/hash-table/figures/Indexleme.png)
- Hash Function/ Hash Table
Hash Table, key value prensibine dayanan bir array kümesidir. Key olarak çağırdığınız elemanın değerini (value) yansıtır. 
Hash Table yerine dizileri kullanabilirdik. Fakat her ürünü ve fiyatını tek tek aramak istemediğimiz için hash table kullanıyoruz. Peki bu süreç nasıl işliyor? Hemen bir örnek yapalım. Örneğimiz bir kuru yemiş dükkanından gelecek.
![yok](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/hash-table/figures/%C3%B6rnek-ilk-k%C4%B1s%C4%B1m.png)
    
    * Bu kısımda ilk olarak bulunan ürün sayımız kadar sayısı olan bir Array oluşturduk. 8 ürün varsa 8 elemanlı bir array. ***Yukarıda ki görselde olduğu gibi;***
    * Daha sonra hash fonksiyonundan ürünleri (ürün isimlerini) geçirerek fonksiyonun sonucunda çıkan sayısal değeri **index değeri** olarak kullanacağız. ***Yukarıda ki görselde olduğu gibi;***
    * Her ürün için bir index değeri belirlenmiş oldu ve bu indexler ilk başta oluşturduğumuz Array'in indexleri. Bu indexlerde ürünlerin fiyatlarını tutacağız. ***Aşağıda ki görselde olduğu gibi;***

![yok](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/hash-table/figures/%C3%B6rnek-ikinci-k%C4%B1s%C4%B1m.png)
Şifrelendiği için artık her badem keyi gönderildiğinde 85TL, fıstık keyi gönderildiğinde ise 69 sonucu verecektir.

Özetle, elimizde var olan verileri bir fonksiyondan geçirip indexliyoruz. Bu fonksiyona hash function, bu fonksiyon ile birleştiğimiz dizi yapısına ise Hash Table diyoruz.

- Kaynak Siteler
    * [Hash Table #13](https://www.youtube.com/watch?v=jhc-KG3htrM)
    * [Hash Table (Karım Tablosu, Özet Tablosu) Veri Yapıları 22. Video](https://www.youtube.com/watch?v=_TCkO3DnVs4)
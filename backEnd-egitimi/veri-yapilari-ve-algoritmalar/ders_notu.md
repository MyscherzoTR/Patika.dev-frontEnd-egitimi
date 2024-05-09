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
- Sayısal olmayan verilerin bir sembol olduğunu ve 0 ve 1'lerdan oluştuğunu hep birlikte öğrendik. Binary olarak gördüğümüz ifade makine kodundan dolayı farklı bir nesneyi işaret edebilir.

#### E. Bilgisayarda Verilerin Tutulması
- Bilgisayar, yapısından dolayı içerisinde tutulabilecek veri miktarı sınırlıdır. Bu verilerin en küçük yapı taşları bitlerdir. *Bilgisayar hafızasında ki bir kutucuğa **1 bit** denir*. Kutucuk arttıkça bit sayısıda artar yani ***2 kutucuk varsa 2 bit*** demektir bu. bitler 0 ve 1'lerden oluşur. 

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
-Array, **Memory locality *(araştır)* için iyi.** 
-Array, Veriye sabit sürede ulaşmaya ***Random Access*** denir ve Arraylerin böyle özelliği vardır.
-Linked List, **eleman ekleme ve silme Array'e göre daha kolay.** 
-Linked Listlerde ilgili elemanı bulmak için tek tek sırasıyla elemanları kontrol etmek gerekir.
- ![LinkedList-vs-Array](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/linked-list-array/figures/array-vs-linkedlist-diff.png)

- Kaynak Siteler
    * [Veri Yapılarına Giriş ve Linked List Mantığı](https://ceyhuncozvelioglu.medium.com/kendime-notlar-1-veri-yap%C4%B1lar%C4%B1na-giri%C5%9F-ve-linkedlist-mant%C4%B1%C4%9F%C4%B1-5944bcbb8165)
    * [Dizi (Array) ile Bağlı Liste (Linked List) Arasındaki Farklar](https://www.ysancar.com/veri-yapilari/dizi-ile-bagli-liste-arasindaki-farklar/)
# Veri Yapıları ve Algoritmalar Ders Notu

Veri Yapıları ve Algoritmalar ders notunu hazırlarken bir çok kaynaktan faydalandım. Elimden geldiğince basit ama işe yarar bir not hazırlamaya gayret gösterdim. ***Her konunun sonunda o konuyla alakalı faydalandığım kaynakları belirttim. Belirttiğim kaynaklardaki herşeyi bu nota eklemedim. Her konuyu okuduktan sonra mutlaka kaynaklarda içeriklere de göz atmalısınız.*** Faydalandığım kaynaklardan bazıları;

- Çeşitli Youtube kanalları
- Udemy, BTK Akademi tarzı eğitim siteleri
- patika.dev, coderspace, techcareer.net tarzı oluşumlar
- khanacademy oluşumu
- Medium sitesinde ki makaleler

Ders ile alakalı başlangıç teorik videolar - ***kesinlikle izlenmeli***;

- [Youtube - Algoritma Nasıl Öğrenilir?](https://www.youtube.com/watch?v=mw8GkVWDFok)
- [Youtube - Veri Yapıları Ders 1 Temel Kavramlar](https://www.youtube.com/watch?v=AMq0LhzavhU&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU)
- [Youtube - Veri yapıları ve Algoritmalar - Data Structures and Algorithms](https://www.youtube.com/watch?v=mKPTA7hAewY&list=PLZYKO7600KN-mFeIahqjCVIzYd55wbJ3y)

***Son olarak aşağıdaki izleme listesi izlenmeli!***

- [Youtube - Algoritmaya ve Programcılığa giriş(Playlist)](https://www.youtube.com/playlist?list=PLzIWkToFwqHRQHEefJEZsUGTdpyo4NVtb)

## 1. Temel Kavramlar

### A. Algoritma nedir

Algoritma belirli bir durumdan başlayıp belirli bir sonuçta biten problemlere çözüm getiren adımlar bütünüdür. ***Veya*** Bir işi bitirmek için gerçekleştirilmesi gereken adımlar bütünüdür.

> #### A_1. Kaynak Siteler

- [khanacademy - Algoritma Nedir ve Neden Öğrenmeliyiz?](https://tr.khanacademy.org/computing/computer-science/algorithms/intro-to-algorithms/v/what-are-algorithms)
- [khanacademy - Tahmin Oyunu](https://tr.khanacademy.org/computing/computer-science/algorithms/intro-to-algorithms/a/a-guessing-game)

### B. Makine Dili (0 ve 1)

Bilgisayarda veriler "dijital" şekilde, yani ikili tabanda gösterilir.

İkili sayılarda bulunan **0 ve 1 rakamları (bit)**, bilgisayarın elektrik iletimi için kullandığı transistörlerin ***(elektrik akımı iletir)*** açık veya kapalı olma durumunu gösterir. Transistörlerde iki tane komut vardır, 0 (kapat, elektrik geçmiyor/yok) ve 1 (aç, elektrik geçiyor/var).

Bu iki durumu tanımlamak için ikili(binary) sistem kullanılır. Her sayıya *"binary digits"* kelimelerinin kısaltılmışı olan ***"bit"*** denir.

- Bytecode => **Java derleyicisinin (Java Compiler)** Java ile yazılmış kodların makine dili yerine kendine has oluşturduğu Binary (0 ve 1) dosyasıdır.

- JVM => Java Bytecode formatına derlenmiş programların çalışmasını sağlayan bir sistemdir.

> #### B_1. Kaynak Siteler

- [Compiler (Derleyici) ve Interpreter (Yorumlayıcı) Nedir?](https://medium.com/@msenell/derleyi%CC%87ci%CC%87-compiler-ve-yorumlayici-interpreter-%C3%BCzeri%CC%87ne-bi%CC%87r-deneme-d8656619ef6)
- [Java - Bytecode](https://tr.wikipedia.org/wiki/Java_bytecode)

### C. Sayı Tabanları (İkilik ve Onluk)

İkilik(Binary) ve Onluk(Decimal) tabanlar

> #### C_1. Onluk (Decimal) Gösterimi

Her basamak için 10 olası değer (0-9) vardır. En sağda ki birler basamağıdır (0-9)
Sonraki onlar basamağı (10-90)
Sonraki yüzle basamağı (100-900) şeklinde ilerler.

***Örneğin 506 sayısı;*** 6 birler, 0 onlar, 5 yüzler basamağıdır. *Gösterimi ise;*

- (5 * 10^2) + (0 * 10^1) + (6 * 10^0) = (506)10
- (6 * 1) + (0 * 10) + (5 * 100) = (506)10

> #### C_2. İkili (Binary) Gösterimi

Her basamak için sadece 2 olası değer (0 veya 1) vardır. En sağda ki birler basamağıdır (0 ve 1)
Sonraki ikiler basamağı (1'den 2'ye)
Sonraki dörtler basamağı (1'den 4'e) şeklinde ilerler.

***Örneğin 110 sayısı;*** 0 birler, 1 ikiler, 1 dörtler basamağıdır. *Gösterimi ise;*

- (1 * 2^2) + (1 * 2^1) + (0 * 2^0) = (110)2
- (1* 4) + (1 * 2) + (0 * 1) = (110)2

> #### C_3. Kaynak Siteler

- [Onluk Tabanından İkilik Tabana Çevirme Kod Örneği](https://prog.asmaamir.com/e-tabancevirme)

### D. Binary Symbols(ASCII) - Araştır?

Sayısal olmayan verilerin bir sembol olduğunu ve 0 ve 1'lerdan oluştuğunu hep birlikte öğrendik. Binary olarak gördüğümüz ifade makine kodundan dolayı farklı bir nesneyi işaret edebilir.

ASCII Kodlarıyla "Hello." kelimesi.
![ASCII Kodlarıyla "Hello." kelimesi.](https://player.slideplayer.biz.tr/10/2798593/data/images/img19.jpg)

### E. Bilgisayarda Verilerin Tutulması Byte(Bayt) ve bit Kavramı

Bilgisayar, yapısından dolayı içerisinde tutulabilecek veri miktarı sınırlıdır. Bu verilerin en küçük yapı taşları bitlerdir. *Bilgisayar hafızasında ki bir kutucuğa **1 bit** denir*. Kutucuk arttıkça bit sayısıda artar yani ***2 kutucuk varsa 2 bit*** demektir bu. bitler 0 ve 1'lerden oluşur.

Bu bitleri bir hafıza gibi düşünebiliriz. Ne kadar çok bit dolar ise boyut o kadar artar ve daha az veri depolama alanımız kalır. 8 kutucuk yan yana geldiğinde yani 8 bit olduğunda 1 Byte(Bayt)'a eşit olur. ***8 bit = 1 Byte*** şeklinde adlandırılır. **Metre, Santimetre gibi düşünülebilir tamamen adlandırma.**

Veriler Byte(Bayt) ve Byte'ın katları olarak depolanır/hesaplanır(KB, MB, GB gibi). 1024 olduğunda bir üst gösterime geçilir. Örneğin;

- **1024 Byte = 1 KiloByte(KB)**
- **1024 KiloByte(KB) = 1 MegaByte(MB)**
***eşittir.***

***Peki 1 Bayt(Byte) ne kadar farklı şey ifade edebiliyor;***

8 kutucuk olduğu için *2^8'den 256 farklı şey ifade edebiliyor.* 256 farklı karakterin gösterimi için 0 ve 1'lerden oluşan yeterli farklı kombinasyonu elde ederiz.

- Numaralar
- Büyük, küçük harfler
- Noktalama işaretleri vb.

![Farklı 1 Byte ile gösterim](https://player.slideplayer.biz.tr/10/2798593/data/images/img5.jpg)

> #### E_1. Hadi gelin ***bit ve byte kavramlarını*** Görsel ile Örneklendirelim

![bit ve byte kavramları](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/veri-tutulma/figures/veri-tutulma.png)

- (1 Byte = 8 bit)  demiştik. 8 bit yani 2^8 = **256 farklı şey, sembol ifade eder ve bu işimizi görmeyebilir, yetersiz kalabilir.** Bu durumda 256 sembolden daha fazla bir depolama alanı isteyebiliriz. Peki bu durum da ne yapacağız? Aslında çözüm çok basit Byte'ları yan yana koyarak depolama alanımızı arttıracağız.

Diyelim ki yan yana 4 Byte koyduk. Yani 4*8'den 32 bit koymuş olduk. Bu da *2^32 farklı şey, sembol ifade eder.*

***Dipnot: 4 Byte yazılımda integer(int) ifade eder.***

Hemen bir örnek çözelim.
![bigger bit](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/veri-tutulma/figures/veri-tutulma2.png)

- Binary semboller, kullanan kişiye göre farklılık gösterebilir. Örneğin, 1010 sembolü Ali'ye göre "1" karakterini sembolize ederken, Veli'ye göre "11" sayısını, Ahmet'e göre ise "a" harfini sembolize edebilir.
![Veri Sembolleri](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/veri-tutulma/figures/sembol-veri.png)

> #### E_2. Kaynak Siteler

- [Bit Nedir](https://tr.wikipedia.org/wiki/Bit_(bili%C5%9Fim))
- [Byte Nedir](https://tr.wikipedia.org/wiki/Bayt)

### F. Recursion ve Recursive - Özyineleme

***Rekürsif fonksiyonda(özyinelemeli) temel fikir şudur;*** bir problemi adım adım küçük parçalara ayırarak, temel işleme ulaşıncaya kadar kendi kendini çağıran bir fonksiyon şeklidir. Bu sıralı çağrılardan sonra temel adıma ulaşınca temel adımdaki değeri geriye doğru sararak en üst basamağa taşır ve böylece sonuç bulunur. Aslında özyineleme, döngüler gibi çalışır ve döngülerinde belli bir sınır olduğundan özyinelemede de bir sınır olmalıdır bu sınır temel adım (taban) olmalıdır. Sınır olmazsa işlem sonsuz kez tekrarlanır ve bu durum sistemi çökertebilir.

"recursion" ve "recursive" aynı kavramla ilgilidir, ancak dilbilgisi açısından farklı kullanımlara sahiptirler;

Recursion: Bir ismidir. Programlamada bir fonksiyonun kendi kendini çağırması durumu anlamına gelir. Örneğin, bir problemin çözümünü, problemin daha küçük bir alt problemini çözerek bulmak. ***Örnek: "Recursion is a common technique in computer science."***

Recursive: Bir sıfattır. Bir şeyin kendini tekrar eden veya içeren yapısı olduğunu tanımlar. Örneğin, bir fonksiyonun kendini çağıran bir yapıda olması. ***Örnek: "A recursive function is a function that calls itself."***

Recursive metotlar *her zaman "return" lü metot* olmak zorundadır. Recurison ile alakalı bir kaç örnek çözelim.

> #### F_1. Kod Örnekleri

##### *Örnek 1: Bir Mülakat Sorusu : Döngü Kullanmadan Bir Sayı Dizisini Ekrana Yazdırmak*

Başlangıç 1, bitişi ise 20 olan sayı dizisini döngü kullanmadan tek tek ekrana yazdıralım. Kodumuz PHP ile yazılacak.

###### *Kod 1, İki değer arasında recursive*

```php
function loop($startValue,$endValue){
    echo $startValue. "\n";

    if ($startValue<$endValue)
        loop($startValue+1,$endValue);
}

loop(1,20);
```

###### *Kod 2, İki değer arasında recursive(Daha iyisi)*

```php
function loop($startValue,$endValue){
    if($startValue>$endValue)
        return;

    echo $startValue. "\n";
    loop($startValue+1,$endValue);
}

loop(1,20);
```

<hr>

##### *Örnek 2: Döngü Kullanmadan Faktöriyel Hesabı*

5 sayısının faktöriyeli döngü kullanmadan hesaplanacak. Kodumuz yine PHP ile yazılacak.

###### *Kod 1, fatöriyel recursive*

```php
$result = 1;

function factorial($number){
    global $result;
    
    if($number!=0)
        $result = $result*$number;

    if ($number==1 || $number == 0)
        echo $result;

    elseif($number>1)
        factorial($number-1);

    else
        echo "Faktoriyel Negatif değer alamaz!";
}

factorial(5);
```

Kod 1 örneğinde "global" kullanıldı. Peki "global ne işe yarar neden kullanılır" bir bakalım.

***global $result;*** ifadesi, PHP'de bir fonksiyonun içinden global bir değişkeni kullanmanızı sağlar. PHP'de değişkenler varsayılan olarak yereldir(local variable), yani bir fonksiyon içinde tanımlanan değişkenler sadece o fonksiyon içinde kullanılabilir. Eğer bir fonksiyon içinde tanımlanan bir değişkene erişmek istiyorsanız **"global" anahtar kelimesini kullanmanız** gerekir.

"***global result***" ifadesi kullanılmazsa, fonksiyon içindeki "***result***" değişkeni yerel olur ve "***global result***" değişkenine erişilemez(başka yerdeki result erişilemez).

###### *Kod 2, fatöriyel recursive(Daha iyisi)*

```php
function factorial($number){
    if($number==1 || $number==0)
        return 1;
    
    elseif($number>1)
        return $number * factorial($number-1);

    return "Faktoriyel Negatif değer alamaz!";
}

$result = factorial(5);
echo $result;
```

<hr>

##### *Örnek 3: Listedeki Elemanları Toplama*

Kodumuz Python ile yazılacak.

###### *Kod 1, Python liste gezme özelliği ile: my_list[0:]*

İlk elemandan listenin sonuna kadar elemanları döner. Bu yöntemle listeyi sürekli olarak küçültüyoruz, ta ki tek bir eleman kalana kadar.

Fakat performanslı çalışmaz çünkü her çağrılışında geriye kalan elemanlardan alt liste oluşturur bu metot.; ***my_list[0:]***  

```python
def list_sum(my_list):
    if len(my_list) == 0:
        return 0  # Boş liste için 0 döndürüyoruz
    
    return my_list[0] + list_sum(my_list[1:])

# Test için liste
my_list = [5, 4, 3, 2, 1]
print(list_sum(my_list))
```

###### *Kod 2, listede ki elemanları manuel gezme: index*

Bu yöntem, performans açısından daha verimli olabilir, çünkü her recursive çağrıda yeni bir liste oluşturulmaz ***my_list[0:]*** 'de olduğu gibi.

```python
def list_sum(my_list, index=0):
    if index == len(my_list):  # Liste sonuna geldik
        return 0
    
    return my_list[index] + list_sum(my_list, index + 1)

# Test için liste
my_list = [5, 4, 3, 2, 1]
print(list_sum(my_list))
```

<hr>

##### *Örnek 4: Döngü Kullanmadan Fibonacci Hesabı*

Fibonacci'nin sadece ilk 10 elemanı hesaplanacak. Kodumuz yine PHP ile yazılacak.

###### *Kod 1, döngüden yardım alarak*

```php
function fibonacci($n){
    if ($n <=0)
        return 0;
    
    elseif($n==1)
        return 1;
        
    else
        return fibonacci($n-1) + fibonacci($n-2);
}

for ($i = 1; $i<=10; $i++)
    echo fibonacci($i). "\n";
```

###### *Kod 2, yardımcı fonksiyondan yardım alarak*

```php
function fibonacci($n){
    if ($n<=0)
        return 0;

    elseif($n==1)
        return 1;

    else return fibonacci($n-1) + fibonacci($n-2);
}

function printFibonacci($current, $count){
    if($count>10)
        return;

    echo fibonacci($current) . "\n";
    printFibonacci($current + 1, $count + 1);
}

printFibonacci(1,1);
```

###### f(4) için sözlü bir örnek/açıklama yapalım

Dördüncü(4.) fibonacci elemanı çağrıldığında adımlar aşağıda ki gibidir

```text
f(4) hesaplama => f(3) + f(2) => 2 + 1 = 3
            f(3) hesaplama => f(2) + f(1) => 1 + 1 = 2
                f(2) hesaplama => f(1) + f(0) => 1 + 0 = 1
                    f(1) hesaplama = 1
                    f(0) hesaplama = 0
                f(1) hesaplama = 1
        
            f(2) hesaplama => f(1) + f(0) => 1 + 0 = 1
                f(1) hesaplama = 1
                f(0) hesaplama = 0
```

***Bu nedenle, fibonacci(4)'ün sonucu 3'tür. Adım adım açılımı ise şu şekildedir;***

fibonacci(4) hesaplanırken ***fibonacci(3) ve fibonacci(2)*** fonksiyonları çağrılır.
fibonacci(3) hesaplanırken **fibonacci(2) ve fibonacci(1)** fonksiyonları çağrılır.
fibonacci(2) hesaplanırken **fibonacci(1) ve fibonacci(0)** fonksiyonları çağrılır.
fibonacci(1) ve fibonacci(0) temel durumlar olup, **sırasıyla 1 ve 0 değerlerini** dönerler.
Bu şekilde **özyinelemeli hesaplama** devam eder ve her seferinde ***bir önceki iki Fibonacci sayısının toplamı*** alınarak sonuç döndürülür. Yani her eleman kendisinden önceki iki elemanın toplamıdır;

fibonacci(0) = 0
fibonacci(1) = 1
fibonacci(2) = fibonacci(1) + fibonacci(0) = 1 + 0 = 1
fibonacci(3) = fibonacci(2) + fibonacci(1) = 1 + 1 = 2
fibonacci(4) = fibonacci(3) + fibonacci(2) = 2 + 1 = 3

<hr>

##### *Örnek 5: Hanoi Kuleleri Çözümü*

Hanoi Kuleleri çözümü. Kodumuz Python ile yazılacak. Yazılan kod için count ile adım saydırıldı. Diskler kaç adımda bitiş kısmında sıralanacak sağlaması için; **(2^n)-1** Yani 3 disk varsa 7 adımda bitmesi gerekir işlemin.

```python
count = 0

def Move(sourcePeg, destinationPeg):
    global count 
    count = count+1
    print("Step " + str(count) + " Move the Disc: " + str(sourcePeg) + "-->" + str(destinationPeg))
    
def PlayHanoi(numberOfDisk, sourcePeg, destinationPeg, auxiliaryPeg):
    if numberOfDisk == 1:
        Move(sourcePeg,destinationPeg)
    
    else:
        PlayHanoi(numberOfDisk-1, sourcePeg, auxiliaryPeg, destinationPeg)
        PlayHanoi(1, sourcePeg, destinationPeg, auxiliaryPeg)
        PlayHanoi(numberOfDisk-1, auxiliaryPeg, destinationPeg, sourcePeg)

PlayHanoi(3,"Start","End","Temp")
```

> #### F_2. Kaynak Siteler

- [Youtube - C Öz Yineleme (Recursion) - Veri Yapıları Ders 02](https://www.youtube.com/watch?v=qT-Fh2kxR6s&list=PLIM5iw4GHbNX8O53Z7Dqi1ZIUxZzpFhR8)
- [Youtube - C# Veri Yapıları Ders 8 Rekürsif Yapılar](https://www.youtube.com/watch?v=PNWOP_QoBGI&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU)
- [Youtube - Java 24 - Rekürsif (Özyineli, Recursive) Fonksiyonlar](https://www.youtube.com/watch?v=nbZqkz_jsOQ&list=PLh9ECzBB8tJNWhY-uH1RrvAFI88vC-Snh)
- [Youtube - Java 25 - Recursive (Özyineli) Örnek Çözümü](https://www.youtube.com/watch?v=EgXL4BSe6Zg&list=PLh9ECzBB8tJNWhY-uH1RrvAFI88vC-Snh)
- [Youtube - Java - Recursive Fonksiyonlar Nasıl Çalışır ve Örnek Kodlama](https://www.youtube.com/watch?v=cv7CY8UmFL0&list=PLh9ECzBB8tJNzJqD64MAS0SK5IeNCKCzY)
- [Youtube - Java Dersleri #43 - Recursive (Özyineli) Metotlar](https://www.youtube.com/watch?v=I3_wU5fr3Zo&list=PLEcJSEQK_cD5KHgg9sXumeg659hAr2j4W)
- [Youtube - Recursive fonksiyonlar ve Python ile Hanoi Kuleleri çözümü](https://www.youtube.com/watch?v=4GvMYiPLRtU)
- [Youtube - Python - 09-1 - Recursive Fonksiyonlar](https://www.youtube.com/watch?v=5b4rfahUiP8&list=PLzIWkToFwqHRZWCI_helg4PeN184yTbYS)
- [Recursion Nedir?](https://www.yucelalkan.com/recursion-nedir)
- [Özyineli(Recursive) Fonksiyon Nedir?](https://medium.com/kodcular/%C3%B6zyineli-recursive-fonksiyon-nedir-d98439707a8d)
- [khanacademy - Ders 5: Özyinelemeli Algoritmalar (İlk 5 konu tamamlanmalı)](https://tr.khanacademy.org/computing/computer-science/algorithms/recursive-algorithms/a/the-factorial-function)
- [khanacademy - Zor Görev: Hanoi'yi özyinelemeli olarak çözmek (Bunu yapmayabilirsiniz)](https://tr.khanacademy.org/computing/computer-science/algorithms/towers-of-hanoi/pc/challenge-solve-hanoi-recursively)

<hr>

## 2. Veri Yapıları

### A. Array (Dizi)

String veri tipi aslında hafıza da "***char array***" olarak saklanmaktadır. Sadece tek boyutlu diziler yoktur. 2 Boyutlu, Çok bouytlu dizilerde vardır. Örneğin; matrisler. Matrisleri tablo gibi düşünebilirsiniz. Her satırda bir kayıt vardır fakat bu kayıtların birden fazla niteliği vardır. Ad-Soyad, Yaş gibi.

Dizilerde indis numarası vardır ve ***0*** rakamından başlar. 3 elemanlı bir dizi hayal edelim. Bu elemanların indis numarası sırasıyla: ***0, 1, 2*** olacaktır.

> #### A_1. Avantajları

- Rastgele herhangi bir elemana index kullanarak hızlı erişme.
- Her elemanın değeri kolay silinebilir veya değiştirilebilir.
- Elemanları kolay bir şekilde sıralayabilir ve gezebilirsiniz.
- Bilgisayarlarda native olarak implement edilmiş en hızlı veri yapısı.
- Stacks, Queues, Heaps ve Hash Table gibi veri yapılarının temelini oluşturur.

> #### A_2. Dezavantajları

- Kapasitesi sabittir. Başlangıçta verilen değer neyse o dur.
- Başa, ortaya veya sona eleman eklenemez veya silinemez.
- 10 elemanlı bir boyuta sahip dizi de 4 eleman bile olsa 10 elemanlık yer kaplar hafızada.

> #### A_3. Ne Zaman Kullanılabilir?

- Uzunluğu sabit bir liste varsa.
- Tek değer tipine sahipse elemanlar(type:int gibi).
- Listede matematiksel işlemler yapılmak istebirse.
- Index kullanarak hızlı tarama ve değer değiştirme durumunda.
- Çok boyutlu matematiksel listelere ihtiyaç duyuluyorsa.
- Hafızayı verimli kullanmak istenildiğinde.

> #### A_4 Python da Array Kullanımı

**Pythonda dizilerin birçok özelliği vardır.** Birden farklı şekilde dizi oluşturabilirsiniz. Dizideki bir elemanın değerini değiştirebilirsiniz. Dizide ki elemanları ekrana yazdırabilirsiniz veya dizideki spesifik bir elemanı. Diziye eleman ekleyebilirsiniz. Örneğin;

```Python
# int türünde dizi
int_array = [5, 10, 2, 27, 34, 1, 5] # int türünden oluşan dizi

int_array[0] = 5 # Dizinin ilk elemanının değerini 5 yaptık. İndisler 0 dan başlar!

print(int_array[0]) # İlk elemanı ekrana yazdırdık.

print(int_array) # Diziyi ekrana yazdırdık. Normalde for gibi döngülere ihtiyaç duyarız ekrana yazdırmak için.
# Fakat Python da buna ihtiyaç yoktur print ile yazdırabiliriz.

print(int_array[1:4]) # 1.indisden 4.indise kadar olan elemanları ekrana yazdırdık, 1.indis dahil 4 dahil değil.
# Python'ın bir özelliği, dizileri istediğiniz yerden bölebiliyoruz aralık verebiliyoruz.

print(int_array[:3]) # Başlangıç boş bıraktık. Varsayılan olarak 0'dır. Python özelliği.

print(int_array[2:]) # Son değeri boş bıraktık. Varsayılan olarak dizinin sonuncu elemanıdır. Python özelliği.

print(int_array[-1]) # Dizinin sonuncu elemanını yazdırır. Diziyi tersten okur. Python özelliği.

print(int_array[-2]) # Dizinin sondan ikinci elemanını yazdırır. Diziyi tersten okur. Python özelliği.

print(len(int_array)) # Dizinin uzunluğunu, elaman sayısını verir. İndis ile karıştırılmamalı.
# 10 elemanlı bir dizinin sonuncu elemanının indis değeri 9'dur.

int_array.sort()  # Diziyi küçükten büyüğe sıralar.

int_array.reverse() # Yukarıda diziyi sıraladıktan sonra. reverse ile diziyi ters çeviriyoruz. 
# Bu durumda büyükten küçüğe saralamış oluruz.

int_array.count(5) # Verilen elaman dizide kaç kez tekrar etmiş hesaplar. Bizim dizimizde 5 değeri 2 kez var.

int_array.clear() # Diziyi sıfırlar, temizler, içini boşaltır.

int_array.index(5) # Belirli bir elemanın ilk bulunduğu indeksi döndürür.

-----------------------------------------------------------------------------------------------------

# string türünde dizi
string_array = ["elma", "armut", "portakal", "muz"] # string türünden oluşan dizi

# Diziye eleman ekleme
string_array.append("Üzüm") # Dizinin sonuna "Üzüm" elemanını ekler.

string_array.insert(3,"Nektari") # 3. indise Nektari ekler.

# Diziye toplu eleman ekleme - Python özelliği yine
string_array += ["şeftali", "ananas", "erik"] # Artı ifadesi ile 2 diziyi toplamakta mümkün.

# Diziden eleman silme
del string_array[1] # İndis numarası ile birinci silme yöntemi.

string_array.pop(1) # İndis numarası ile ikinci silme yöntemi.

string_array.remove("portakal") # Değeri bilinen elemanı silme.

# Çarpma Özelliği - Karzezyan Çarpım Yapıyor
string_array *= 2 # Sıralı bir şekilde diziyi 2 katına çıkardı. 
print(string_array) # Görüldüğü gibi dizinin elemanları 2 katına çıktı sıralı;
# ["elma", "armut", "portakal", "muz", "elma", "armut", "portakal", "muz"]

-----------------------------------------------------------------------------------------------------

# 2 boyutlu dizi örneği;

array1 = [
    [2, 0, 3],
    [4, 5, 2],
    [7, 0, 1],
]

array2 = [
    [0, 1, 4],
    [0, 1, 2],
    [0, 1, 1],
]

# Python da çok boyutlu dizileri yazdırmak çok basit. 
# İstenilen satır yazdırılmak istenildiğinde print(array1[0]) ile ilk satır yazdırılır. 
# Dizinin tamamı yazdırılmak istenirse for döngüsü yazıp print(array1[i]).
# 3-3 bir matris olduğu için direkt range(3) dedik. Hem satır sütun eşit hemde boyutu biliniyor.
for i in range(3):
    print(array1[i])

# 2 adet 2 boyutlu diziyi toplama
array3 = [
    [0, 0, 0],
    [0, 0, 0],
    [0, 0, 0],
]

for i in range(3):
    for j in range(3):
        array3[i][j] = array1[i][j] + array[i][j] 
```

> #### A_5. Kod Örnekleri

##### *Örnek 1: X Elemanlı Bir Diziyi Tersten Çeviren Kodu Yazın (swapping işlemi)*

Kodumuz Python ile yazılacak.

###### *Kod 1, kısa ama 2 diziye ihtiyaç duyan yöntem*

```python
array_list = [3, 8, 7, 2, 6, 5]
print("Ana Liste: ", array_list)

reversed_list = []

for i in range(len(array_list) - 1, -1, -1):
    reversed_list.append(array_list[i])

print("Ters Çevrilmiş Liste: ", reversed_list)
```

**range'e verilen 3 parametrenin anlamı;**

- İlk değer başlangıç değeri, bizim durumumuzda ***5***
- İkinci değer bitiş değeri, -1 olunca dur demek yani en son ***0 çalışacak.***
- Eksiltme değeri, sayıyı birer birer azalt demek. ***i++, i-- gibi.***

kısacası 5 ten başlayıp 0'a kadar sayıyı eksilten bir döngü. 5 kez çalışıyor.

###### *Kod 2, uzun ama tek diziye ihtiyaç duyan yöntem*

```python
array_list = [3, 8, 7, 2, 6, 5]
print("Ana Liste: ", array_list)

list_length = len(array_list)

temp_value = 0

for i in range(list_length // 2):
    temp_value = array_list[i]  
    array_list[i] = array_list[list_length-i-1]  
    array_list[list_length-i-1] = temp_value 

print("Ters Çevrilmiş Liste: ", array_list)
```

**list_length//2** => tamsayı bölme işlemi için kullanılır. Ondalıklı sayı hesaba katılmaz. Bölüm sonucu 2.4 ise 2 olarak döndürür.

Bu komutu döngü kaç kez çalışacak bunu belirlemek için kullandık çünkü dizinin boyutu değişebilir ve haliyle döngününde çalışma tekrarı değişmeli.

Şuan dizimiz 6 elemanlı buradan sonuç 3 gelir. Elaman sayısı çift uzunluğa sahip olduğunda sorun yok. 6 eleman varsa baktığınızda ***baştaki 3 ile sondaki 3 eleman yer değiştirmeli***. Yani döngü 3 kez çalışmalı.

Diyelim ki **dizi 5 elemanlı olsaydı** nasıl olurdu? Bölüm sonucu 2 gelirdi. Döngü 2 kez çalışırdı. ***baştaki 2 ile sondaki 2 eleman yer değiştirirdi*** Yani 4 değer yer değiştirirdi. Geriye ise en ortadaki değer tek başına kalırdı.Zaten en ortada olduğundan yeri değişmez. Tek sayılarda yöntem bu şekilde.

İşte bu yüzden ***list_length//2*** kullanıyoruz.

<hr>

##### *Örnek 2: Fibonacci İlk 20 Elemanını Hesaplayan ve Bunu Diziyi Kayıt Eden Kod*

Kodumuz Python ile yazılacak.

###### *Kod 1, ilk yöntem*

```python
array_list = [0]*20 
# 0 değerine sahip 20 elemanlı dizi. 
# Python da direkt dizi boyutunu belirleme yok başlangıçta.

for i in range(20): 
    if i == 0 or i == 1:
        array_list[i] = 1
        
    else:
        array_list[i] = array_list[i-1] + array_list[i-2]
    
print(array_list)
```

###### *Kod 2, ikinci yöntem*

```python
array_list = [0]*20 
# 0 değerine sahip 20 elemanlı dizi. 
# Python da direkt dizi boyutunu belirleme yok başlangıçta.

array_list[0] = 1
array_list[1] = 1

for i in range(2,20):
    array_list[i] = array_list[i-1] + array_list[i-2]
    
print(array_list)
```

###### *Kod 3, Eğer dizi kullanmasaydık işimiz nasıl zor olurdu bir görelim*

```python
fibonacci_first_element = 1
fibonacci_second_element = 1

fibonacci_element = 21

for i in range(1,fibonacci_element):
    
    if i == 1 or i == 2:
        sum = fibonacci_first_element
    
    else:
         fibonacci_first_element = fibonacci_second_element
         fibonacci_second_element = sum
         sum = fibonacci_first_element + fibonacci_second_element
    
    print(sum)
```

Gördüğünüz gibi çok kafa karıştırıcı ve uzun bir yöntem.

> #### A_6. Kaynak Siteler

- [Youtube - C Programlama 7 Diziler (Array)](https://www.youtube.com/watch?v=0bjMFwS8TZY&list=PLh9ECzBB8tJNzJqD64MAS0SK5IeNCKCzY)
- [Youtube - Java Arrays - Diziler - Veri yapıları ve algoritmalar - Data Structures](https://www.youtube.com/watch?v=Itj319eYDMY&list=PLZYKO7600KN-mFeIahqjCVIzYd55wbJ3y)
- [Youtube - Java 12 - Diziler (Arrays)](https://www.youtube.com/watch?v=Xtc50eGgm08&list=PLh9ECzBB8tJNWhY-uH1RrvAFI88vC-Snh)
- [Youtube - Java 23 - Diziler Örnek Çözüm](https://www.youtube.com/watch?v=C9wJKUtuPZ0&list=PLh9ECzBB8tJNWhY-uH1RrvAFI88vC-Snh)
- [Youtube - Java Dersleri #49 - Diziler (Arrays)](https://www.youtube.com/watch?v=Nwyn_Od6HY0&list=PLEcJSEQK_cD5KHgg9sXumeg659hAr2j4W)
- [Youtube - Java Dersleri #50 - Çok Boyutlu Diziler (Multidimensional Array)](https://www.youtube.com/watch?v=JvPx7eZZsvw&list=PLEcJSEQK_cD5KHgg9sXumeg659hAr2j4W)
- [Youtube - Python - 05 - Diziler temel işlemler](https://www.youtube.com/watch?v=o2JyXPL9SeA&list=PLzIWkToFwqHRZWCI_helg4PeN184yTbYS)
- [Youtube - Python - 06 - Çok boyutlu diziler, matrisler](https://www.youtube.com/watch?v=UeYhBv6hTYE&list=PLzIWkToFwqHRZWCI_helg4PeN184yTbYS)
- [Array Nedir?](https://medium.com/@denizf.b/array-nedir-d9b7afd44ca2)
- [VERİ YAPILARI(DATA STRUCTURES)](https://medium.com/@abdulkadir.kamci10/veri%CC%87-yapilari-data-structures-4f3de459f930)

### B. List Nedir ve Linked List İle Arasında ki Farklar - Araştır?

> #### B._1 Kaynak Siteler

- [Youtube - Veri Yapıları Ders 2 Listeler](https://www.youtube.com/watch?v=hnE9_7VBKyI&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU)
- [Youtube - Sıfırdan Python Dersleri Ders 3: Listeler (Lists)](https://www.youtube.com/watch?v=pBMuc4cc_Ck&list=PL3kMAPso9YQ1Ls-5uTTIWWMkJoF_vyj5J)

### C. Linked List - Araştır?

- Linked-List (Bağlı listeler), yan yana zorunluluğu olmadan veri tutmamızı sağlayan yapılardır. Yeni gelen eleman için hafıza'da yeni bir alan açmamız gerekmez. Array'dan farklı olarak elemanlar hafıza içerisinde farklı yerlerde olabilir fakat son gelen eleman kendinden bir önceki elemana ***her zaman adresini bildirmek*** zorundadır.
![Linked-List](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/linked-list/figures/linked-list.png)

Yukarıdaki örnekte gördüğünüz üzere, her bir düğüm bir sonrakinin adresini tutar. Her bir önceki eleman bir sonraki eleman ile bağlıdır.

> #### C_1. Kaynak Siteler

- [Youtube - Bagli Listeler (Linked Lists) - Veri Yapıları Ders 03](https://www.youtube.com/watch?v=SLz8J56hvj0&list=PLIM5iw4GHbNX8O53Z7Dqi1ZIUxZzpFhR8)
- [Youtube - Bağlı Liste Sınıfının Tasarımı - Veri Yapıları - Ders 03](https://www.youtube.com/watch?v=e3ZMNXROg9o&list=PLIM5iw4GHbNX8O53Z7Dqi1ZIUxZzpFhR8)
- [Youtube - Bagli Liste İlk Uygulama - Veri Yapıları Ders 03](https://www.youtube.com/watch?v=PzgV6nn53dk&list=PLIM5iw4GHbNX8O53Z7Dqi1ZIUxZzpFhR8)
- [Youtube - Veri Yapıları Ders 2 Listeler](https://www.youtube.com/watch?v=hnE9_7VBKyI&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU&index=3&t=591s)
- [Youtube - Linked List - Veri Yapıları - Data Structures](https://www.youtube.com/watch?v=Qs4PNb9Y1ME&list=PLZYKO7600KN-mFeIahqjCVIzYd55wbJ3y)
- [Youtube - Veri Yapıları Ders 3 Bağlı Listeler (Tek Yönlü,İki Yönlü,Dairesel)](https://www.youtube.com/watch?v=7vjRwtDP0J4&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU)
- [Youtube - Veri Yapılarına Giriş ve Bağlı Listeler (Linked List) -VY1)](https://www.youtube.com/watch?v=r3uOBb3BM-0)
- [Linked List Nedir](http://cagataykiziltan.net/veri-yapilari-data-structures/1-linked-list-bagli-listeler/)
- [VERİ YAPILARI(DATA STRUCTURES)](https://medium.com/@abdulkadir.kamci10/veri%CC%87-yapilari-data-structures-4f3de459f930)

### D. Linked List vs Array - Farklarını Detaylı Araştır?

+Array, **Memory locality *(araştır)* için iyi.**
+Array, Veriye sabit sürede ulaşmaya ***Random Access*** denir ve Arraylerin böyle özelliği vardır.
+Linked List, **eleman ekleme ve silme Array'e göre daha kolay.**
+Linked Listlerde ilgili elemanı bulmak için tek tek sırasıyla elemanları kontrol etmek gerekir.

- ![LinkedList-vs-Array](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/linked-list-array/figures/array-vs-linkedlist-diff.png)

> #### D_1. Kaynak Siteler

- [Veri Yapılarına Giriş ve Linked List Mantığı](https://ceyhuncozvelioglu.medium.com/kendime-notlar-1-veri-yap%C4%B1lar%C4%B1na-giri%C5%9F-ve-linkedlist-mant%C4%B1%C4%9F%C4%B1-5944bcbb8165)
- [Dizi (Array) ile Bağlı Liste (Linked List) Arasındaki Farklar](https://www.ysancar.com/veri-yapilari/dizi-ile-bagli-liste-arasindaki-farklar/)

### E. Lindked List Eleman Ekleme/Silme - Detaylı Araştır?

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

> #### E_1. Kaynak Siteler

- [Doğrusal Veri Yapıları 2 - Bağlı Liste (Linked List)](https://medium.com/@tolgahan.cepel/do%C4%9Frusal-veri-yap%C4%B1lar%C4%B1-2-ba%C4%9Fl%C4%B1-liste-linked-list-8e5d3d84c41f)

### F. Stack (LIFO) - Detaylı Araştır?

Stack, LIFO (Last in First out) (En son giren en önce çıkar) mantığına dayanan, elemanlar topluluğundan oluşan bir yapıdır. Gelin hemen örneğimize geçelim. Taşınırken topladığınız koli kutusu düşünün. İçerisinde kitaplar var ve en, boy olarak koliye tam olarak koyuluyor. Mantıken kolinin altı kapalı ve üst üste koymanız gerekmektedir. Yeni taşındığınız yerde çıkartırken en üstekinden başlarsınız. İşte stack (Yığın) da aynı mantıkta çalışıyor.

Yığınlara eleman eklerken veya çıkartırken bazı methodlar uygulanır. Bunlardan biri push, diğeri ise pop. Push, yığının üzerine eleman eklemek için kullanılır (Koliye kitap koymak). Pop ise, yığından eleman çıkarmak için kullanılır.

- ***Örnek Push ve Pop***
![Örnek Push ve Pop](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/stack/figures/stack.png)

  - Push: Stack'e eleman eklemek (yığının üstüne tabak koymak). Her seferinde koyulan tabak en üstteki yani son tabak olur.
  - Pop: Stack'ten eleman almak. Yığının en üstünden tabak almak. En son tabak en üstteki olduğu için yığından tabak aldığımızda üstten alırız.

> #### F_1. Kaynak Siteler

- [Youtube - Veri Yapıları Ders 4 Yığıt (Stack) Yapısı](https://www.youtube.com/watch?v=nPl1A6036uk&t)
- [stack-kod-örneği](https://www.baskent.edu.tr/~tkaracay/etudio/ders/prg/dataStructures/Collections/ClassStack.pdf)

### G. Queue (FIFO) - Detaylı Araştır?

Queue (Kuyruk), FIFO (First in First out) (İlk giren ilk çıkar) prensibine dayanan, girişlerde ve çıkışlarda belirli bir kurala göre çalışan yapıdır. Stack de verdiğimiz örneği kuyruğa göre uyarlayalım. Biz örnekte altı kapalı bir koli kutusunu düşünmüştük. Şimdi o koli kutusunun altı yırtılmış. Sonuç olarak ne oluyor? İlk giren ilk çıkmış oluyor.

Queue (Kuyruk)'da eleman eklemesi yaparken enqueue methodunu kullanıyoruz. Eleman silerken ise dequeue methodunu kullanıyoruz.

- ***Örnek engueue ve dequeue***
![Örnek engueue ve dequeue](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/queue/figures/queue.png)

  - Enqueue: Yeni elemanın Kuyruğa eklenmesi (yeni birinin sıraya girmesi)
  - Dequeue: Elemanın Kuyruktan çıkarılması (sırası gelenin sıradan çıkması/işi bitenin sıradan ayrılması)

> #### G_1. Kaynak Siteler

- [Youtube - Veri Yapıları Ders 5 Kuyruk Kavramı](https://www.youtube.com/watch?v=W-wCqjKSpys&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU&index=6)
- [Doğrusal Veri Yapıları 4 - Kuyruk (Queue) Kodlu Örnek](https://medium.com/@tolgahan.cepel/do%C4%9Frusal-veri-yap%C4%B1lar%C4%B1-4-kuyruk-queue-dcbd07e8ba77)

### H. Hash Function(Karma Fonksiyonu)/ Hash Table(Karma Tablosu) - Detaylı Araştır?

- Indexleme
Arraylerde 0 bazlı bir indexleme vardır. Bazı programlama dillerin de 1 bazlı indexlemeler olsa da genel olarak 0 bazlı indexleme kullanılır. Yani 0'dan başlar index sayısı.
![Indexleme](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/hash-table/figures/Indexleme.png)
- Hash Function(Karma Fonksiyonu)/ Hash Table(Karma Tablosu)
Hash Table(Karma Tablosu), key value prensibine dayanan bir array kümesidir. Key olarak çağırdığınız elemanın değerini (value) yansıtır.
Hash Table yerine dizileri kullanabilirdik. Fakat her ürünü ve fiyatını tek tek aramak istemediğimiz için hash table kullanıyoruz. Peki bu süreç nasıl işliyor? Hemen bir örnek yapalım. Örneğimiz bir kuru yemiş dükkanından gelecek.
![yok](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/hash-table/figures/%C3%B6rnek-ilk-k%C4%B1s%C4%B1m.png)

  - Bu kısımda ilk olarak bulunan ürün sayımız kadar sayısı olan bir Array oluşturduk. 8 ürün varsa 8 elemanlı bir array. ***Yukarıda ki görselde olduğu gibi;***
  - Daha sonra hash fonksiyonundan ürünleri (ürün isimlerini) geçirerek fonksiyonun sonucunda çıkan sayısal değeri **index değeri** olarak kullanacağız. ***Yukarıda ki görselde olduğu gibi;***
  - Her ürün için bir index değeri belirlenmiş oldu ve bu indexler ilk başta oluşturduğumuz Array'in indexleri. Bu indexlerde ürünlerin fiyatlarını tutacağız. ***Aşağıda ki görselde olduğu gibi;***

![yok](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/hash-table/figures/%C3%B6rnek-ikinci-k%C4%B1s%C4%B1m.png)
Şifrelendiği için artık her badem keyi gönderildiğinde 85TL, fıstık keyi gönderildiğinde ise 69 sonucu verecektir.

Özetle, elimizde var olan verileri bir fonksiyondan geçirip indexliyoruz. Bu fonksiyona hash function(karma fonksiyonu), bu fonksiyon ile birleştiğimiz dizi yapısına ise Hash Table(Karma Tablosu) diyoruz.

> #### H_1. Kaynak Siteler

- [Youtube - Hash Table #13](https://www.youtube.com/watch?v=jhc-KG3htrM)
- [Youtube - Hash Table (Karım Tablosu, Özet Tablosu) Veri Yapıları 22. Video](https://www.youtube.com/watch?v=_TCkO3DnVs4)

### I. Hash Function(Karma Fonksiyonu)

Hash Function (Karma Fonksiyonu), karma fonksiyonu olabilmesi için bazı temel şartlar vardır.Bunlar;

- Gönderdiğimiz ***anahtarlar (keys) farklı*** olmasına rağmen aynı sonuçları alıyorsak bu bir ***hash function*** değildir.
  - *Farklı girdilere farklı sonuç/çıktı vermeli!*
- Fonksiyona gönderilen ***anahtarlar aynı*** fakat sonuç farklı ise ***hash function*** değildir.
  - *Hash Function sonucu her seferinde aynı girdiye aynı sonuç/çıktı vermeli!*
- Hash Table(Karma Tablosu) için kullanılan dizinin boyutu verilen sonuçların sayısı kadar olmalıdır. Kaç key varsa o kadar elemanlı olmalı dizi(array).
  - *Hash functiondan 8 değer döndü dizinin boyutu 8 elemanlı olmalıdır.*

Fakat her zaman tutarlı olmuyor. Bazen **Collision** dediğimiz sorun ortaya çıkıyor.

- Farklı girdiye farklı sonuç veremiyor. Farklı çıktılar aynı sonuçlar doğurabiliyor.

> #### I_1. Kaynak Siteler

- [Youtube - Hash Function #14](https://www.youtube.com/watch?v=ZX-1qPSYC_k)
- [Youtube - Veri Yapıları Ders 9 / Hash Fonksiyonları 1](https://www.youtube.com/watch?v=OYiNo0BTVxQ&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU&index=10)
- [Youtube - Veri Yapıları Ders 10 / Hash Fonksiyonları - 2](https://www.youtube.com/watch?v=jxwcjv12TG8&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU&index=11)
- [Youtube - Veri Yapıları Ders 11 / Hash Fonksiyonları - 3](https://www.youtube.com/watch?v=Vcr3LizkCuo&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU&index=12)
- [Youtube - Veri Yapıları Ders 12 / Hash Fonksiyonları - 4](https://www.youtube.com/watch?v=5h5mBf4k2do&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU&index=13)

### J. Hash Collision

Hash Function'da ***farklı iki değerden aynı sayı üretilirse*** bu duruma ***Collison (çarpışma)*** denir. Bu olay istediğimiz bir durum değildir.

- Hash Function'lar bazen farklı durumlar için farklı sonuçlar üretemeyebilir. ***Örnek verelim;***
  - Araçları bir hash function dan geçirelim. Bu fonksiyonumuz **araçların son harflerine** göre değer atasın. Motor ve tır, bunların son harfleri ***"R"*** olduğu için fonksiyon çıktısında aynı değerler verilir ve bu **collision'a neden olur.**
- Collision sorunuyla az karşılaşabilmek için kaliteli bir hash function olmalı. Bu sayede verimli bir Hash Table elde etmiş oluyoruz.
- Çarpışma sayısı arttıkça aradığımız şeyi bulma hızı azalır.

> #### J_1. Kaynak Siteler

- [Youtube - Hash Collision #15](https://www.youtube.com/watch?v=FD7nKLnrguE)

<hr>

## 3. Algoritma Analizi

### A. Algoritma Analizi Giriş

- Algoritma analizi, bir algoritmanın çalışabilmesi için gerekli koşulların sağlanıp sağlanamadığını gösteren bir parametredir.
-Algoritma analizi, var olan kaynaklara göre en uygun algoritmayı seçmek için uygulanır. Peki algoritma analizi en iyi nasıl yapılır? Kulağa karmaşık geliyor ama çok basit. Programlama dillerinden ve donanımlardan bağımsız bir şekilde Algoritma analizi yapılmalıdır. Aksi taktirde en uygun sonuç alınamayabilir.
- Donanımlar veya programlama dilleri farklı cihazlarda aynı performansı vermeyebilir. Örnek verecek olursak, cep telefonları için uygulama tasarladığımızı varsayalım. Bu uygulamanın performansı Apple telefonlar için farklı, Android telefonlar için farklı, arasında donanım farklı olanlar için ayrı olacaktır. Donanım ve diller ile algoritma analizi pek sağlıklı değildir.

> #### A_1. Kaynak Siteler

- [Youtube - Algoritma Analizi #16](https://www.youtube.com/watch?v=Pi32FSu1TNg)
- [Asimptotik Analiz, Asimptotik karmaşıklık nedir?](https://egemengulpinar.medium.com/tr-algoritma-analizi-ve-asimtotik-karma%C5%9F%C4%B1kl%C4%B1k-84ad6be27b32)
- [Derinlemesine Algoritma Analizi](https://birhankarahasan.com/algoritma-analizi-nedir-zaman-karmasikligi-big-o-gosterimi)

### B. Ram Modeli

Bir algoritmayı farklı cihazlarda denemek bize pek fazla bir sonuç çıkarmıyordu. Çünkü kaynaklar değişebiliyordu. Bu probleme genel bir çözüm getirebilmek için hayalî bir cihaz düşünelim. Bu cihaz üzerinde bütün algoritmaları çalıştırdıktan sonra bize bir sonuç verecek. Kısacası; **genellenebilir bir analiz yapmak için her algoritmayı aynı bilgisayar ile test ediyor gibi düşüneceğiz.**

Bu hayalî cihaza ***RAM (Random Access Machine)*** diyoruz. Ram, algoritmalar arasındaki farkları belirlemek için kullanacağımız bir araç olacak.

Her işlemin birim zamanı mevcuttur. ***Bunlara örnek;***

- Döngüler kaç defa işlem yapıyorsa (işlem sayısı * kaç kere tekrar edeceği) o kadar birim zaman alır.
- Toplama, Çıkarma, and, or gibi *basit aritmetik/logic işlemler* 1 birim zaman alır.
- Hafızadan her okuma işlemi 1 birim zaman alır.

> #### B_1. Kaynak Siteler

- [Youtube - Ram Modeli(Random Access Machine) #17](https://www.youtube.com/watch?v=lrHoiZig3Z8)
- [ChatGPT - RAM Modeli ve Kullanımı](https://chatgpt.com/share/5acbf049-521c-4593-90b5-44b9cc4b4b48)

### C. Time Complexity

Algoritmanın verimli olması için belli kurallar vardır. ***Örnek: Raflara kitap yerleştirmek*** gibi.

- Kitapları, gelişigüzel raflara dağıtırsak aradığımız kitabı daha fazla zamanda bulabiliriz. Aslında bu bir ***[worst case(Big O)](https://bilgisayarkavramlari.com/2008/12/22/en-kotu-durum-analizi-worst-case-analysis/)***'dir. Beklenilen en kötü durum(*vereceğimiz inputun algoritmamızı en yavaş/en fazla işlem yapacak şekilde çalıştırdığı durum*).
Kitapları filtrelememiz gerekir. Kalın olanları bir rafa, ince olanları bir rafa, küçük boyutta olanları bir rafa koyduğumuz zaman aradığımız şeyi daha rahat bulabiliriz. Algoritma, en kötü senaryoya ne kadar hazırsa, bizi o kadar memnun edebilir.
- Algoritmalar için genellikle sık kullanılan ***average case(Big Theta)***'dir. Genel olarak beklenilen durum(ortalama durum). Kitapların bölümüne göre kaç tane olduğunu biliyorsak average case kullanabiliriz. En büyük rafı miktarı fazla olana ayırabiliriz. Input yoksa average zordur!!!!
- Bir diğer senaryomuz ise ***best case(Big Omega)***'dir. Beklediğimiz en iyi durum(*vereceğimiz inputun algoritmamızı en hızlı şekilde çalıştırdığı durum*). Kitap örneğine devam edecek olursak, bütün kitapların ayrı raflarda olması, alfabeye göre sıralanması best case olarak ifade edilebilir. Çünkü aradığımızı rahatlıkla bulabiliriz.

**Buradaki seçim bize kalmış.** Hangi aralıkta algoritmamızı değerlendirmek istiyorsak ona göre karmaşıklığı baz alabiliriz. Kullanım ihtiyacına göre bu şekillenecektir. *Ancak genel bir tanı itibariyle en kötüyü bilirsek*, ortalama ve en iyi durumu da tahmin etmek için fikrimiz olabilir. ***Genellikle Big O notasyonu hesaplanıp algoritma karmaşıklığı bulunur.***

> #### C_1. Kaynak Siteler

- [Youtube - Time Complexity #18](https://www.youtube.com/watch?v=Ie_Ax6KLI80)
- [Youtube - Algoritma Analizi ve Big O (Time Complexity, Space Complexity)](https://www.youtube.com/watch?v=wMp0BrWaoz8)
- [worst case nedir?](https://bilgisayarkavramlari.com/2008/12/22/en-kotu-durum-analizi-worst-case-analysis/)

### D. Nedir Bu “Big O Notation”?

***Bu örnekleme worst case(en kötü duruma) göre yapılan bir örneklemedir!***

1000 sayfalık bir sözlük düşünelim. **Normal bir A algoritması** 1.sayfadan başlayıp aranılan kelimeyi sayfa sayfa tarar. Bu çok fazla işlem yükü ve beraberinde zaman kaybı getirir.

Bu seferde **B algoritması** diyelim. Sözlük alfabetik olarak sıralanmıştır. Aradığımız kelime için ilk olarak sözlüğü 2'ye böleriz. ***Sol da ilk 500 sayfa sağda son 500 sayfa olarak.*** Sonra aradığımız kelimeye bakarız. Eğer ilk 500 sayfa içinde ki harflerle eşleşiyorsa sağdaki yani son 500 sayfayı eleriz. Tam tersi durumda ise sağ daki 500 sayfa ile eşleşirse bu sefer ilk 500 sayfayı eleriz. Böylece elimizde her **durumda sadece 500 sayfalık** arama yapılacak yer kalmış olur.

Şuan elimizde ***sadece 500 sayfa kaldı.*** Bu sayfalar içinde aynısını yapıyoruz. Yine 2'ye bölüyoruz. Sol ve sağ olarak yine kontrol ediyoruz. Böyle böyle yani 2'ye böle böle aramamız gereken alanı azaltıyoruz. En son elimizde aradığımız kelimeye ait sayfa kalıyor ve bu sayfada da **aynı yöntemi yaparak(bu sefer sayfayı 2'ye bölüyoruz sürekli)** kelimeyi buluyoruz.

1000 sayfalık sözlüğün tamamını teker teker aramak yerine böyle bir yöntemle çok daha az efor ve kısa zamanda aradığımız kelimeyi bulmuş oluyoruz. ***Yani problem her seferinde yarı boyutuna inmiş oluyor.***

Bu örnek 1000 sayfalık bir sözlükte yapılan bir değerlendirmeydi. Algoritmanın faydalı olup olmaması bir çok faktöre/input(sözlük boyutu, aranılan kelime vb.) bağlı olabilir. 10.000 sayfalık bir sözlükte çok daha hızlı olacaktır son sayfalardaki kelimeyi ararken.

***Worst Case örneği değil! Bir dipnot daha iyi anlaşılması için;* Fakat diyelim ki ilk sayfa da bizim aradığımız kelime. Bu durumda **normal A algoritması çok daha hızlı çalışacaktır** Çünkü 1.sayfadan taramaya başladığı için direkt bulacaktır ama B algoritması sürekli sözlüğün ortasından 2'ye böldüğü için çok daha fazla vakit ve işlem alacaktır. Buna rağmen B algoritmasının Worst Case A algoritmasının worst case'inden daha iyi olacaktır. Çünkü A algoritması için Worst Case en sonuncu sayfa artık sözlük kaç sayfa ise.

> #### D_1. İşte bu noktada devreye **"Big O Notation"** girer. ***Peki nedir bu Big O Notation?;***

Bog o natation algoritmanın ne kadar sürede çalışacağını bize söylemeyecej. Bize algoritmamızın çalışma zamanının inputun boyutu ile nasıl değişeceğini söyleyece/gösterecek.

Input Boyutuna(input size), *n* diyelim. Algoritmamızın en kötü durumda n işlem yapması beklenir. Inputum n boyutunda olunca çalışma süremin de en kötü durumda n olmasını *O(n)* ile göstereceğim. Aynısı B algoritması için de geçerli *O(logn)*

Kısacası A algoritması input size göre sürekli artış gösterirken B algoritması bir süre sonra sabit zamanda işlemler(arama vb.) yaptırır.

Big O notation da yapılacak toplam işlem sayısının input size ile nasıl scale olacağına bakıyoruz. Bizim için fonksiyonun yapısı önemli. İşlem sayısı nasıl artıyor; Linear, karesi ile orantılı, logaritmik mi nasıl? Big o notaion bana bunu vermiş oluyor.

> #### D_2. Kaynak Siteler

- [Youtube - Big O Notation #19](https://www.youtube.com/watch?v=AeeSlV64TOI)
- [Nedir Bu “Big O Notation”?](https://medium.com/kodcular/nedir-bu-big-o-notation-b8b9f1416d30)
- [Algoritma Karmaşıklığı (Big-O)](https://medium.com/algorithms-data-structures/algoritma-karma%C5%9F%C4%B1kl%C4%B1%C4%9F%C4%B1-big-o-5f14316890a4)

<hr>

## 4. Sorting (Sıralama) Algoritmaları

### A. Sorting Nedir?

Sorting, kendinden sıralama algoritmaları olarak bahsetmektedir. Sorting, bir eleman dizisini, belirli sıralama kurallarına göre sıralama yapar.

**Searcing: Elemanları en başta sıralamak, eleman aramayı hızlandırabilir.**

Sıralama algoritmaları kullanmamızdaki amaç, algoritmanın isminden de anlaşılacağı üzere sahip olduğumuz veriyi en hızlı şekilde büyükten küçüğe ya da küçükten büyüğe bir sıraya sokmak. Bunun için kullanılan bir çok sıralama algoritması vardır. Bazısı çok hızlı ama yazımı zor, bazısı az sayıda veri için çok hızlı, bazısının da yazması kolaydır.

Herhangi bir sayıdaki tip verilerin sınırlı bellek ve işlem gücü ile belirli bir sıraya göre dizilmesinin sağlanmasıdır. Burada önemli olan en optimum bellek ve performans ikilisini verecek bir algoritmanın elde edilmesidir.

> #### A_1. Sıralama Algoritmalarını Bazı Kriterlere Göre Sınıflandırılabiliriz

- **Bellek Kullanımı:** Çalışırken ek bellek ihtiyacı duyan algoritmalarda kullanılabilecek bir ölçüttür buna ek olarak ayrıca da sıralama işleminin yapılması sırasında hafızanın kullanımına göre de sıralama algoritmaları; Harici sıralama (External Sort) ve Dahili Sıralama (Internal Sort).
- **Hesaplama Karmaşıklığı:** Oluşturulmuş olan algoritmanın yaptığı işlem sayısının genel bir yapı ile ifade edilmesidir. Temel üç grup ölçek kullanılır. Bunlar en iyi (best), ortalama (average) ve en kötü (worst) durumu olarak belirtilir. İşlem yoğunluğu zaman işleyişiyle paralel olduğundan (ne kadar çok işlem yapılırsa o kadar uzun süre geçer) algoritmanın işleyiş süresini de etkiler.
- **Yerdeğiştirmenin Karmaşıklığı:** İçerisinde ek bellek kullanmayan (in place) algoritmalarda kullanılan karşılaştırılabilmesi için önemli bir ölçüttür.
- **Durağanlık(stability):** Algoritmanın uygulanması sırasında sıralanmış bir verinin tekrar sıralamaya tabi tutulup tutulmadığını belirten ölçektir.
- **Rekürsiflik:** İç içe kendi kendini çağıran algoritmalarda kullanılan bir ölçüttür. Burada en önemli kriter stack dediğimiz maksimum iç içe çağırım kapasitesine dikkat edilmesi ve bu kapasitenin kullanılma sıklığıdır.
- **Fakat en önemli kriterler**
  - Hafıza Verimliliği (Memory efficiency)
  - Zaman Verimliliği (Time efficiency)

> #### A_2. Aşağıda Bazı Sıralama Algoritmaları Verilmiştir

- Seçerek Sıralama (Selection Sort)
- Eklemeli Sıralama (Insertion Sort)
- Kabuk Sıralaması (Shell Sort)
- Birleştirmeli Sıralama (Merge Sort)
- Hızlı Sıralama (Quick Sort)
- Kabarcık Sıralaması (Bubble Sort)

> #### A_3. Sıralama Algoritmalarının Karşılaştırılması

Sık kullanılan sıralama algoritmalarının, verinin karmaşıklığına göre gösterdiği performans:

![Sıralama Algoritmalarının Karşılaştırılması](https://www.halildurmus.com/wp-content/uploads/2021/01/593-Siralama-Algoritmalarini-Karsilastirma-1.png)

> #### A_4. Kaynak Siteler

- [Youtube - Sorting #20](https://www.youtube.com/watch?v=v3Z6crtZVek)
- [Sıralama Algoritmaları (Sorting Algorithms)](https://www.halildurmus.com/2021/02/22/siralama-algoritmalari-sorting-algorithms/)
- [Sıralama Algoritmaları](https://serdarkuzucu.com/siralama-algoritmalari/)

### B. Insertion Sort

En basit sorting algoritmalarından biridir.

Yerleştirerek sıralama işlevi belirli bir anda dizinin belirli bir kısmını sıralı tutarak ve bu kısmı her adımda biraz daha genişleterek çalışmaktadır. Sıralı kısım işlev son bulunca dizinin tamamına ulaşmaktadır. Elemanların sırasına uygun olarak listeye tek tek eklenmesi ile gerçekleştirilen sıralamadır.

> #### B_1. Kod Örneği

Aşağıda örnek kod ve çıktısı görülmekte.

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

> #### B_2. Kaynak Siteler

- [Youtube - 2 dakikada Insertion Sort](https://www.youtube.com/watch?v=JU767SDMDvA&list=PL9xmBV_5YoZOZSbGAXAPIq1BeUf4j20pl&index=4)
- [Youtube - Veri Yapıları Ders 34 Insertion Sort](https://www.youtube.com/watch?v=0lpT0XUy29Q&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU&index=35)
- [Insertion Sort Data Structure and Algorithm Tutorials](https://www.geeksforgeeks.org/insertion-sort/)

### C. Selection Sort

En basit sorting algoritmalarından biridir.

![Selection Sort](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/insertion-sort/figures/insertion-sort.png)

Verilen örüntüye ait ***en küçük elemanı buluyor ve en baştaki sayı ile yer değiştiriyor.*** Peki ya devamı? İkinci en küçük elemanı buluyor ve 2. sıra ile değiştiriyor. Baktın ki ***2.sıradaki eleman en küçük hiç dokunma!!!. Hemen 3. sıraya geç.*** 4, 5 derken dizi bitti. İşte insertion sort'un temel çalışma prensibini öğrendin.

![Selection Sort](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/insertion-sort/figures/insertion-sort.png)

> #### C_1. Kaynak Siteler

- [Youtube - Insertion Sort #21(Adı yanlış yazılmış)](https://www.youtube.com/watch?v=GBXm2h4Eu-0)
- [Youtube - 3 dakikada Selection Sort](https://www.youtube.com/watch?v=g-PGLbMth_g&list=PL9xmBV_5YoZOZSbGAXAPIq1BeUf4j20pl&index=5)
- [Youtube - Veri Yapıları Ders 32 Selection Sort](https://www.youtube.com/watch?v=Hr-cghhg-Co&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU&index=33)
- [Youtube - Veri Yapıları Ders 33 Selection Sort Örnek 2](https://www.youtube.com/watch?v=DzgmtogFFfw&list=PLKnjBHu2xXNNwV1Twc3UtaMBqGJx3CCrU&index=34)
- [Selection Sort Data Structure and Algorithm Tutorials](https://www.geeksforgeeks.org/selection-sort/)

### D. Merge Sort

Selection Sort'da, Big-O gösteriminden dolayı input'um arttığında ***n^2*** olduğunda dolayı çalışma zamanı artıyor.

Peki daha hızlı bir şekilde sıralama yapılabilir mi? Evet, Merge Sort burada yardımımıza koşuyor. Bir listeyi her adımda parçaya ayırıp tek eleman kalıncaya kadar bölüyor. Böldükten sonra sıralı bir şekilde bize sunuyor (Performans).

![Merge Sort](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/merge-sort/figures/merge-sort.png)

![Merge Sort](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/merge-sort/figures/big-o-merge.png)

Selection Sort'da, time complexity ***n^2*** olduğundan ötürü çalışma zamanımız artıyordu. Merge sort'da ise ***nlogn*** olduğu için açık ara performans olarak daha iyi diyebiliriz.

> #### D_1. Kaynak Siteler

- [Youtube - Merge Sort #22](https://www.youtube.com/watch?v=Sx1VfR7EvnA)
- [Youtube - 3 dakikada Merge Sort](https://www.youtube.com/watch?v=4VqmGXwpLqc)
- [Youtube - Birleştirme Sıralaması (Merge Sort) ve Parçala Fethet (Divide and Conquer) (Algoritma Analizi 10)](https://www.youtube.com/watch?v=f9CNp_uuNJg)
- [4. BİRLEŞTİRMELİ SIRALAMA (MERGE SORT)](http://cagataykiziltan.net/algoritmalar/1-siralama-algoritmalari/4-birlestirmeli-siralama/)
- [Birleştirme Sıralaması (Merge Sort)](https://bilgisayarkavramlari.com/2008/08/09/birlestirme-siralamasi-merge-sort/)

### E. Quick Sort

Hızlı sıralama günümüzde çok yaygın olarak kullanılan bir sıralama algoritmasıdır. N tane sayıyı ***average case e göre big-o nlogn***, ***worst case e göre big-o n^2*** karmaşıklığı ile sıralanır.

![Quick Sort](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/quick-sort/figures/Quicksort.png)

İlk olarak bir pivot belirler bu pivota göre pivottan küçük ve eşitler sol kısmına, pivottan büyük ve eşitler sağ kısmına yazılır. Parçalanmış kısımlar yeni bir pivot belirlenerek parça pinçik edilir.

> #### E_1. Kaynak Siteler

- [Youtube - Quick Sort #23](https://www.youtube.com/watch?v=EikA3rBMD18)
- [Youtube - 4 dakikada Quick Sort](https://www.youtube.com/watch?v=JU767SDMDvA&list=PL9xmBV_5YoZOZSbGAXAPIq1BeUf4j20pl&index=4)
- [Quick Sort (Hızlı Sıralama Algoritması) Veri Yapıları 13](https://www.youtube.com/watch?v=aubOM9dOy6c)
- [Quick Sort (Hızlı Sıralama) Nedir?](https://medium.com/@turgay2317/quick-sort-h%C4%B1zl%C4%B1-s%C4%B1ralama-nedir-2d6555e5f7e2)
- [Algoritma Dersleri – Quick Sort](https://www.mobilhanem.com/algoritma-dersleri-quick-sort/)
- [Hızlı Sıralama Algoritması (Quick Sort Algorithm)](https://bilgisayarkavramlari.com/2008/08/09/hizli-siralama-algoritmasi-quick-sort-algorithm/)

<hr>

## 5. Searching (Arama) Algoritmaları

### A. Searching Nedir?

Günümüzde veriler gitgide artan bir hal alıyor. Her insanın bir bilgisayarı ve telefonu olduğunu düşünürsek, terabaytlarca veri ediyor. Arama algoritmaları ise istediğim özellikteki verinin elimdeki veri setlerinde aranıp, bulunup getirilmesi demek. Bunun hızlı olmasına önem gösterilir.

> #### A_1. Kaynak Siteler

- [Arama Algoritmaları (Search Algorithms)](https://bilgisayarkavramlari.com/2009/11/23/arama-algoritmalari-search-algorithms/)
- [Arama Algoritmaları (Search Algorithms) Nedir?](https://enesates03.medium.com/arama-algoritmalar%C4%B1-search-algorithms-nedir-7c8be09d541a)

### B. Linear Search

Linear search, tek tek elemanları dolandıktan sonra istediğim elemanın olup olmadığına bakmaktır. En basit arama algoritmasıdır. Örneğin;

- [20,25,46,48] veri setini ele alalım. Benim aradığım eleman 25. İlk elemana gidiyorum ve değeri 20 sen değilsin diyorum. İkinci elemana gidiyorum ve değeri 25 evet sensin diyorum. Linear search algoritmam burada bitmiş oluyor.

- Big-o ya göre incelediğimizde bizim worst case'imiz neydi? Elemanın dizinin sonunda bulunmasıydı. Bu sebepten ötürü n elemanımız varsa big-o notasyonumuz otomatik olarak n oluyor.

> #### B_1. Kaynak Siteler

- [Youtube - Linear Search #25](https://www.youtube.com/watch?v=fPGqKlUKh7c)
- [Youtube - Her Yazılımcının Bilmesi Gereken Algoritmalar - Lineer Arama(Linear Search) ve Python ile Kodlaması](https://www.youtube.com/watch?v=hPVJJyXFr-c)
- [Doğrusal & İkili Arama Algoritmaları (Linear & Binary Search Algorithms)](https://medium.com/@ozgurmehmetakif/do%C4%9Frusal-i%CC%87kili-arama-algoritmalar%C4%B1-linear-binary-search-algorithms-ed5fefc1f003)
- [Doğrusal Arama (Linear Search)](https://bilgisayarkavramlari.com/2008/11/09/dogrusal-arama-linear-search/)

### C. Binary Search

İkili arama algoritması, elimizde bulunan veri dizisinin sıralı olduğunu varsayıyor, bu durumu değiştirerek sonuca varmak istiyor.

İkili arama algoritması, diziyi her seferinde ikiye bölerek ikili arama yapar. Sıralı bir listem var ise Big-o gösterimi ***logn*** olarak karşımıza çıkıyor.

> #### C_1. Örnek Binary Search

Aradığım sayı **15** olsun ve değer kümem ***[10,15,20,16,22,36,23]*** elemanlarından oluşsun.

Binary Search bu diziyi manipüle ederek şu ifadeye dönüştürüyor. ***[10,15,16,20,22,23,36]***. *36 sayısını en yüksek sayı, 10 sayısını ise en düşük sayı ilan eder.* ***Adım adım nasıl arama yaptığını görelim;***
![Binary Search](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/binary-search/figures/binary-search.png)

- Benim aradığım sayı ile ortada kalan sayıyı kıyaslıyor eğer aradığım sayı küçükse, sağda kalan yani ortada ki sayıdan büyük bütün sayıları siliyor.
  - Aradığım sayı ortada ki sayıdan büyükse bu sefer solda kalan yani küçük sayıları siliyor.
- Ve kendine yeni bir ortanca belirliyor. Böylelikle gereksiz arama yapmaktan kurtarıyor.

> #### C_2. Kaynak Siteler

- [Youtube - Binary Search #26](https://www.youtube.com/watch?v=cvsZCh_0H9A)
- [Youtube - 4 dakikada Binary Search](https://www.youtube.com/watch?v=fDKIpRe8GW4)
- [Youtube - İkili Arama Algoritması(Binary Search Algorithm)](https://www.youtube.com/watch?v=Bi9zq4bS4Hw)
- [Doğrusal & İkili Arama Algoritmaları (Linear & Binary Search Algorithms)](https://medium.com/@ozgurmehmetakif/do%C4%9Frusal-i%CC%87kili-arama-algoritmalar%C4%B1-linear-binary-search-algorithms-ed5fefc1f003)
- [İkili Arama Algoritması (Binary Search Algorithm)](https://bilgisayarkavramlari.com/2009/12/21/ikili-arama-algoritmasi-binary-search-algorithm/)
- [Big O Notation ve Binary Search](https://medium.com/@alifurkangokce/big-o-notation-ve-binary-search-d6f3d4cf4574)

### D. Binary Search Tree

Bir düğüm her iki tarafa da referans verebiliyor. Sağ ve sol olarak. Sağ tarafından kendinden büyük elemanlar, sol tarafında ise kendinden küçük elemanlar bulunacak. ![Binary Search Tree](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/veri-yapilari-algoritmalar/binary-search-tree/figures/binary-search-tree.png)

> #### D_1. Örnek Binary Search Tree

Tree'ye eleman eklemek istediğimde root'dan başlıyorum. Baştaki açıklamamızı hatırlayalım. Sağ tarafında kendinden büyük, sol tarafında kendinden küçük elemanlar olmalı.

***Örnek olarak ben 26 sayısını ağaç yapısına eklemek istiyorum.***

Root'a soruyorum senin değerin ne bana döndüğü cevap 56. Yani soluna eklenecek. Sonrasında 30'a soruyorum ve benim sol tarafıma geçmelisin çünkü sen benden küçüksün diyor.

Karşıma 22 değerinde olan düğüm çıkıyor. Eklemek istediğim sayı 22 den büyük olduğu için sağ tarafına bir köşe çekiyorum ve 26 sayısını bağlıyorum.

> #### D_2. Kaynak Siteler

- [Youtube - Binary Search Tree #27](https://www.youtube.com/watch?v=ec0f3Bh-CJE)
- [Youtube - 4 dakikada Binary Search Tree](https://www.youtube.com/watch?v=fDKIpRe8GW4&t=1s)
- [Veri Yapıları — Binary Search Tree Nedir?](https://tsafaelmali.medium.com/binary-search-tree-nedir-2e6fb0621d9)
- [Binary Search Tree' yi Anlamak](https://www.buraksenyurt.com/post/Binary-Search-Tree-yi-Anlamak)

<hr>

## 6. Karar Verme Algoritması

### A. Minimax Algoritması

> #### A_1. Kaynak Siteler

- [Minimax Algoritması ile TicTacToe Oyunu](https://ahmetatasoglu98.medium.com/minimax-algoritmas%C4%B1-ile-tictactoe-oyunu-82fc58d76b61)
- [Minimax Ağaçları (Minimax Tree)](https://bilgisayarkavramlari.com/2009/04/29/minimax-agaclari-minimax-tree/)

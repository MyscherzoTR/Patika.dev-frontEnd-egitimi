# git Markdown Kullanımı Ders Notu

Türkçe Markdown Kullanımı => https://medium.com/deep-learning-turkiye/t%C3%BCrk%C3%A7e-markdown-rehberi-61779d2e2a96

## 1. Markdown için Siteler

A. typora.io => markdown editörü

B. commonmark.org/help => markdown öğrenme

C. notion.so => notion içinde markdown yapısı kullanabiliriz.


## 2. MarkDown Komutları

A. Başlık için;
- #: en büyük başlık => h1 mesela
- ##: 2.en büyük başlık. => h2 mesela
- ###: bu şekilde gidiyor **h6** ya kadar.

B. Liste için *( * veya - )*;
- Örnek listeler (İşaretten sonra boşluk olacak); <br>
        * deneme yıldız 1 <br>
        * deneme yıldız 2 <br>
        - deneme tire bir <br>
        - deneme tire 2
- iç içe liste: Markdown ile iç içe listeler yapmak da oldukça kolay. Alt listelere tab ile girinti verdiğinizde otomatik olarak nested list yapısına dönüşmekte.

C. İtalik, Kalın, Kalın ve İtalik(işaretlerden sonra ve önce boşluk olmayacak);
- Kullanımı bu şekilde: * italik *
- Kullanımı bu şekilde: ** bold **
- Kullanımı bu şekilde: *** bold_italik ***

D. Link için;
- [Yazı veya Açıklama]---(https://technovadi.com) => link bu şekilde kullanılıyor. Arada tireler olmayacak =>
    * [Yazı veya Açıklama](https://technovadi.com) 

E. Fotoğraf/IMG için;
- ![alt_tagı]---(fotoğrafın_konum_linki) => fotoğraf eklemek bu şekilde kullanılıyor. ***alt_tag*** yazısı fotoğraf bulunamadıysa görünür, istediğiniz mesajı yazabilirsiniz. Arada tireler olmayacak =>
    * ![alt_tagı](https://technovadi.com/wp-content/uploads/2018/08/technovadi-logo.png)

F. HR tagı koyma (Ayırıcı);
- "---" veya "***" => 3 tane yan yana. Tırnaklar olmayacak.
    * ---

G. Kod Bluğu Oluşturma;
- Tek Satır Kod Bloğu (Tek backtick) => 2 tane olacak ve arasına yazılacak kodlar "**`**"
    * `console.log("Hello, World!");`
- Çoklu Kod Bloğu (Üç backtick) => 3er tane olacak başta ve sonda ve arasına yazılacak kodlar. "**```**"
    * ``` 
            print("hello") 
            print("world")
        ```
- Çoklu Kod Bloğu Pyton Kodu (Üç backtick) => En baştaki 3 backtickden hemen sonra "**python**" yazılacak.
    * ```python 
            print("hello") 
            print("world")
        ```
- Çoklu Kod Bloğu JS Kodu (Üç backtick) => En baştaki 3 backtickden hemen sonra "**javascript**" yazılacak.
    * ```javascript 
            print("hello") 
            print("world")
        ```
- Çoklu Kod Bloğu PHP Kodu (Üç backtick) => En baştaki 3 backtickden hemen sonra "**php**" yazılacak.
    * ```php
            print("hello") 
            print("world")
        ```

H.  Alıntı Oluşturma: "**> yazılacak_metin**"
- > yazılacak_metin

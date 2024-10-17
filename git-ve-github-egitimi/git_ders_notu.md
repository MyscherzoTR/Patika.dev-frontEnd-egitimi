# git ve Terminal Kullanımı Ders Notu

git ve Terminal Kullanımı ders notunu hazırlarken bir çok kaynaktan faydalandım. Elimden geldiğince basit ama işe yarar bir not hazırlamaya gayret gösterdim. Her konunun sonunda o konuyla alakalı faydalandığım kaynakları belirttim. Belirttiğim kaynaklardaki herşeyi bu nota eklemedim. Her konuyu okuduktan sonra mutlaka kaynaklarda içeriklere de göz atmalısınız. Faydalandığım kaynaklardan bazıları;

- Çeşitli Youtube kanalları
- Udemy, BTK Akademi tarzı eğitim siteleri
- patika.dev, coderspace, techcareer.net tarzı oluşumlar
- Medium sitesinde ki makaleler

Ders ile alakalı başlangıç teorik video ve makaleler - kesinlikle göz atılmalı;

- [Medium - Versiyon Kontrol Sistemi Nedir?](https://furkanalaybeg.medium.com/versiyon-kontrol-sistemi-nedir-2f47bb830064)
- [techcareer.net - Git Nedir?](https://www.techcareer.net/courses/git-github-egitimi/25f77b02-2a95-4cbb-a697-ab18b531c43e)
- [patika.dev - GIT Versiyon Kontrol Sistemi Nedir?](https://academy.patika.dev/tr/courses/git/git-versiyon-kontrol-sistemi-nedir)

Git komutlarını VS Code içinde kullanmak isterseniz; [patika.dev - VS Code içinde Terminal Kullanarak GIT Temel Komutları](https://academy.patika.dev/tr/courses/git/vs-code-icinde-terminal-kullanarak-git-temel-komutlari)

Git komutlarını VS Code içerisinde terminalsiz kullanmak isterseniz; [patika.dev - VS Code içerisinde Terminal Kullanmadan GIT Temel Komutları](https://academy.patika.dev/tr/courses/git/vs-code-icerisinde-terminal-kullanmadan-git-temel-komutlari)

## 1. GIT Nedir, Bize Ne Sağlar ve Ne İşe Yarar?

![Medium - Versiyon Kontrol Sistemi Nedir ?](https://miro.medium.com/v2/resize:fit:640/format:webp/1*sSLUk53Y7xp2DGf_CXoAjQ.jpeg)

Versiyon Kontrol Sistemi Nedir? sorusuna gelirsek; Bir döküman (yazılım projesi, ofis belgesi vb.) üzerinde yaptığınız degişiklikleri adım adım izleyen, istediğinizde kayıt eden ve isterseniz bunu internet üzerindeki bir bilgisayarda veya yerel bir cihazda (respository / repo / depo) saklamanızı ve yönetmenizi sağlayan bir sistemdir.

Versiyon Kontrol Sistemi yerine Kaynak Kod Yönetim Sistemi ifadesini de duymuş olabilirsiniz. İkisi de aynı şeyi ifade etmektedir.

- Birden fazla yerde (dağıtık olarak) dosyalarınızı ve versiyon kontrol bilgilerinizi depolayabilirsiniz. Böylelikle cihaz bağımsız olarak dosyalarınıza erişebilirsiniz.
- "commit" yaparak SnapShot (anlık görüntü) özelliği ile istediğiniz zaman proje veya dosyaların o anki halini kayıt altına alabilirsiniz. Böylelikle ileride bir hata ile karşılaşırsanız herhangi bir zamandaki herhangi bir versiyona dönüş yapabilirsiniz.
- SnapShot alındıktan sonra değişiklik yapılan dosyaları görebilirsiniz.
- Takımların aynı projede beraber çalışmasına imkan verir. Kim neyi düzenledi? Ne ekledi? Ne çıkarttı? Son değişiklik ne zaman yapıldı? gibi bilgilere erişebilirsiniz. Bu sayede topluluk ile proje geliştirme süreçlerini kolaylaştırabilirisiniz.
- Projede verisyonlanmasını istemediğiniz dosyaları belirtebilirsiniz. (node_modules, .mp4, .log, .env gibi)

***dipnot:*** Git'i öğrenirken, düzenli pratik yapmak ve gerçek projeler üzerinde çalışmak çok önemlidir. Ayrıca, Git'in sadece bir versiyon kontrol sistemi değil, aynı zamanda ekip çalışmasını ve proje yönetimini kolaylaştıran güçlü bir araç olduğunu unutmayın. 

***Bu makaleyi okumanızda fayda var. =>*** [Medium - Versiyon Kontrol Sistemi Nedir ?](https://furkanalaybeg.medium.com/versiyon-kontrol-sistemi-nedir-2f47bb830064)

## 2. GIT'in temel kavramları

***Git'in temel kavramlarını daha anlaşılır şekilde açıklayalım;***

- Çalışma Klasörü (Working Directory): Bu, projenin üzerinde çalıştığın alandır, yani dosyalarının fiziksel olarak bulunduğu klasördür. Git, bu klasördeki dosyaları izler. Dosyalarında yaptığın değişiklikler burada gerçekleşir.
- Index (Staging Area): Değişiklik yaptığın dosyaları commit etmeden önce, "sahneye" çıkardığın alandır. Yani commit'e dahil olacak dosyaları burada toplarsın. Bu aşamada, hangi dosyaların commit'e dahil olacağını belirleyip, son halini gözden geçirirsin.
- Local repository (Yerel Depo): Bu alan, yaptığın commit'lerin depolandığı yerdir. Yani projenin geçmişteki sürümlerinin tutulduğu yerdir. Commit'leri yapınca bu yerel repoda saklanır, henüz uzak sunucuya (GitHub, GitLab gibi) gönderilmemiştir.

### A. Özetle

- Çalışma klasöründe değişiklikler/düzenleme/geliştirme yaparsın.
- Commit'lemek istediğin dosyaları Staging Area'ya (Index) eklersin. Eklediğin dosyalar burada commit atılmasını bekler.
- Commit'le bu değişiklikleri Local Repository'ye kaydedersin. Commit geçmişinin localde tutulduğu yerdir.

## 3. GIT Kurulumu

Aşağıda ki videoları izleyip git'i kurabilirsiniz. Kurulum tamamlandıktan sonra git'in terminali olan "Git Bash" yüklenecektir.

- [techcareer.net - git kurulum](https://www.techcareer.net/courses/git-github-egitimi/4767eadf-4a02-45e4-8f7d-9f594d761223)
- [patika.dev - Visual Studio Code ve Git SCM Kurulumu #1](https://academy.patika.dev/tr/courses/git/git-kurulumu)

## 4. Terminal Kullanımı ve Komutları

***dipnot 1:*** Terminalde klasör, dosya isimlerinde büyük-küçük harf hassasiyeti yoktur. Yani "desktop" klasörüne "cd DESKTOP" ile giriş yapabiliriz.

***dipnot 2:*** bir dosya veya klasör adının tamamını terminale yazmaya gerek yok. Örneğin "temel_seviye" adında bir klasör olsun. Bu klasörünün içine girmek istiyoruz.

"cd tem" yazdıktan sonra klavyeden **tab** tuşuna basarsak otomatik ismi tamamlayacaktır. Eğer birden fazla "tem" ile başlayan dosya varsa size tüm dosyaları gösterecektir. Otomatik tamamlamayacaktır.

***Aşağıda bahsedilen komutları pekiştirmek için bu videoyu izleyebilirsiniz;*** [techcareer.net - Terminal Kullanımı](https://www.techcareer.net/courses/git-github-egitimi/d396eb35-184a-4277-9710-c61b0edfeb7e)

### A. pwd  komutu

pwd komutu bulunduğumuz dizini/pathi söyler. Terminalde verilecek örnek çıktı; "**/c/Users/aydin**"

### B. ls komutu

ls komutu bulunduğumuz klasör/dizin içindekileri listeler.

> #### B_1 ls Kullanımı

- ls => Tüm dosyaları ve dizinleri listeler.
- ls -la =>  Tüm dosyaları ve dizinleri ayrıntılı bir şekilde listelerken, gizli dosyaları da gösterir. Windows için aşağıdakiler de kullanılabilir.
  - Get-ChildItem -Force
  - ls -Force

### C. cd komutu

cd komutu ile ilgili klasörlere girilir.

> #### C_1 cd Kullanımı

- cd .git/ => .git klasörüne girer.
- cd .. => bir önceki klasöre gider. Bir adım geri gittik.

### D. mkdir komutu

Bu komut ile klasör oluştururuz.

> #### D_1 mkdir Kullanımı

- mkdir technovadi => technovadi adında klasör oluşturur.

### E. touch komutu

Bu komut ile dosya oluştururuz. Birden farklı kullanımı da vardır.

> #### E_1 touch Kullanımı

- touch deneme.txt => deneme.txt adında dosya oluşturur.
- New-Item deneme.txt => => deneme.txt adında dosya oluşturur.
- New-Item example.txt -ItemType File => İsimlendirmeden ziyada dosya tipini de File olarak belirttik.

### F. clear komutu

clear komutu terminal de yazılanları temizler.

## 5. GIT Terimler

![Git Terimler](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/git/git-bash-ile-git-temel-komutlari/figures/3-GitHub-cheat-sheet-graphic.jpg)

Başlıca bilmemiz gereken bazı terimler;

- **untracked (izlenmeyen):** GIT tarafından henüz takip edilmeyen, yani yeni oluşturulmuş dosyaları ifade eder.
- **unstaged (hazırlanmamış):** Güncellenmiş ancak commit'lenmek için hazırlanmamış dosyaları ifade eder.
- **staged (hazırlanmış):** Commit edilmeyi bekleyen dosyaları ifade eder.
- **deleted (silinmiş):** Projeden silinmiş ama GIT üzerinden kaldırılmamış dosyaları ifade eder.

## 6. GIT, .gitignore Dosyası

### A. .gitignore Nedir?

.gitignore dosyası projemizin kök dizinine oluşturulan düz bir metin dosyasıdır. Adından anlaşıldığı gibi diyor ki beni göz ardı et. Daha doğrusu göz ardı etmek istediğin, local çalışma alanındaki takip edilmesini istemediğin, takım arkadaşların için gerekmeyen dosyaların varsa veya bu dosyaların boyutu reponuza atmanıza gerek olmayacak kadar büyük ölçekli ise buyur beni kullan diyor.

Gel bu dosyaları .gitignore dosyasına koy ki GIT de senin bu dosyalarını artık takip etmesin. Üstelik bu işlemler yapılırken senin halihazırdaki dosyalarını da hiç bir şekilde etkilemesin. Daha ne olsun! Bunlar için git ignore kullanılır;

- Büyük boyutlu dosyalar (image ve video dosyalarınız gibi)
- Paket yöneticisinden indirilen bağımlılıklar, Kütüphane/Library eklemeleri
- IDE eklentileri( örneğin .vscode)
- Sadece kendi çalışma alanınızda olması gereken başkaları tarafından görülmemesi gereken dosyalarınız(şifre, api key, veritabanınıza ilişkin konfigürasyonlar gibi)
- Hassas bilgiler içeren dosyalar(.env gibi)
- Takip edilmesine gerek duyulmayan gereksiz dosyalar(Çalışma dizinizdeki geçici dosyalar, Log dosyaları)
- dist gibi oluşturulan dosyalar

### B. .gitignore dosyası oluşturma

Bunun için bir çok sayfa, site mevzut. Çoğu zaman GitHub'ın kendi sitesinde ki şablonlar iş görüyor fakat nadirde olsa siteye ihtiyaç duyulabilir. Arama motoruna "gitignore generator" veya "gitignore PHP generator" yazarak birçok siteye ulaşabilirsiniz. Benim kullandığım site;

- [Toptal - gitignore generator](https://www.toptal.com/developers/gitignore)
- [github - gitignore](https://github.com/github/gitignore)

> #### B_1 .gitignore Kullanımı

Dosyanın her satırına takip edilmesini istemediğimiz dosyaları veya dizinleri yazarak göz ardı edebiliriz. Tabii bu dosyaları yazarken bize kolaylık sağlayan bazı formatlar var. İşte onlar:

- Dizinleri belirtmek için "/" kullanıyoruz;
  - C/user/ => user içindekileri izlemez.
- Belirtilen dosya hariç diğerlerini hariç bırak/izleme;
  - !files/example.txt => files klasörü içinde ki "***example.txt***" izler sadece.
- Belirtilen dosyaları türlerini hariç bırak/izleme;
  - *.txt => txt uzantılı dosyaları izlemez.
  - *.log => log uzantılı dosyaları izlemez.
- Yorum satırı "#" ile oluşturulur;
  - "***# Geçici dosyalar***"

> #### B_2. Kaynak Siteler

- [techcareer.net - Git Ignore](https://www.techcareer.net/courses/git-github-egitimi/fa58e056-cbe8-46d4-b12e-d06611460f23)
- [patika.dev - .gitignore Dosyası Ne İşe Yarar? Nasıl Kullanırız?](https://academy.patika.dev/tr/courses/git/gitignore-dosyasi-ne-ise-yarar-nasil-kullaniriz)
- [Gitignore Dosyasıyla Gereksiz Dosyaları Yönetme Rehberi](https://www.emrahyuksel.com.tr/projenizi-daha-temiz-tutun-gitignore-dosyasiyla-gereksiz-dosyalari-yonetme-rehberi/)
- [How to Use a .gitignore File](https://www.pluralsight.com/resources/blog/guides/how-to-use-gitignore-file)

## 6. GIT Komutları

![GIT Temel Komutları](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/git/git-bash-ile-git-temel-komutlari/figures/3-GitHub-cheat-sheet-graphic.jpg)

Konuyu bitirdikten sonra pekiştirmek için göz atabilirsiniz; [patika.dev - GIT Bash ile GIT Temel Komutları](https://academy.patika.dev/tr/courses/git/git-bash-ile-git-temel-komutlari)

### A. git Komutlarında ki flag(kısaltmalar) ne anlama geliyor?

Kısaltmalar (flag) Ne Anlama Geliyor?

> #### A_1. -u (veya --update)

Bu flag, git push komutu ile kullanılır ve uzak sunucuya yerel branch'teki değişiklikleri gönderirken aynı adı taşıyan bir branch olup olmadığını kontrol eder. Eğer aynı adı taşıyan bir başka branch bulunursa, yerel branch ile onu ilişkilendirir (tracking) ve sonraki push işlemlerinde hedef branch olarak otomatik olarak bu uzak branch'i kullanır.

> #### A_2. -m (veya --message)

Bu flag, git commit komutu ile kullanılır ve bir commit mesajı eklemek için kullanılır. Mesajı komut satırında belirterek, direkt olarak commit işlemi gerçekleştirilir. Örneğin: **git commit -m "Değişiklikler eklendi"**.

> #### A_3. -b (veya --branch)

Bu flag, git checkout veya git branch komutları ile kullanılır ve bir branch oluştururken veya bir branch'a geçerken kullanılır. Örneğin: **git checkout -b yeni-branch**, hem yeni bir branch oluşturur hem de o branch'e geçiş yapar.

> #### A_4. -d (veya --delete)

Bu flag, git branch komutu ile kullanılır ve bir branch'i siler. Örneğin: **git branch -d silinecek-branch**, silincek-branch adındaki branch'i siler.

> #### A_5. f (veya --force)

Bu flag, git push komutu ile kullanılır ve uzak sunucuya yerel branch'teki değişiklikleri zorla (force) gönderir. Özellikle, geçmişte yapılmış bir push işleminin tersine çevrilmesi gerektiğinde veya zorla güncelleme yapılması gerektiğinde kullanılır. Ancak dikkatli kullanılmalıdır, çünkü uzak sunucuda yapılan değişikliklerin üzerine yazılabilir ve veri kaybına neden olabilir.

### B. git status komutu

![git status komutu](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/git/git-bash-ile-git-temel-komutlari/figures/5-git-status-1.png)

Üzerinde çalışılan projenin o anki durumu hakkında bilgi verir. İlgili dizinde git olup olmadığı kontrol edilir. Eğer git varsa yapılan değişiklikler, izlenen/izlenmeyen dosyalar, eklenen ve silinen dosyalar gibi bilgiler listelenir. Kısacası tüm yapılan değişimleri söyler.

***Dipnot:*** İlk defa bir projede çalışıyorsak bu komut ile kesinlikle git olup olmadığını kontrol etmeliyiz. Eğer git varsa tekrar eklememeliyiz.

> #### B_1. Kaynak Siteler

- [techcareer.net - Git Init, Status, User](https://www.techcareer.net/courses/git-github-egitimi/d171b704-6dbe-4a8c-a497-e2b7ad8c4c40)

### C. git init komutu

Git ilk defa ilgili proje içinde başlatılacaksa. Henüz versiyon kontrolü altında olmayan bir projenin dizininde, boş bir git deposu oluşturmak için kullanılır. local olarak git projesini oluşturuyoruz. Proje içine ".git" gizli şekilde ekliyor, oluşturuyor.

Bilgilendirme yazısı; "Initialized empty Git repository in proje_path/.git/"

![git init komutu](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/git/git-bash-ile-git-temel-komutlari/figures/4-git-init.png)

> #### C_1. Kaynak Siteler

- [techcareer.net - Git Init, Status, User](https://www.techcareer.net/courses/git-github-egitimi/d171b704-6dbe-4a8c-a497-e2b7ad8c4c40)

### D. git config komutu

Yapılandırma ayarlarının içerisinde barındırıldığı bir komut. GIT’in bir çok konfigürasyon ve ayarı vardır, bunlardan ikisi user.name ve user.email olanıdır. Bu ayarları yapılandırmak için aşağıdaki komutları kullanırız. GIT'i ilk kurduğumuzda genellikle aldığımız ilk hata bu configurasyon ayarlarını yapmadığımız için gelir. Burada yazdığınız isim ve email ileride GitHub benzeri bir platforma commit attığınızda da görüneceği için bunu bilerek isimlendirme yapmak yararlı olur.

Ayarların tamamını görüntülemek için; ***git config --list***
Sistem genelinde bu ayarların geçerli olması isteniliyorsa **--global** kullanılmalı.

> #### D_1. git config user.name "user_name"

Sadece şuan içerisinde bulunduğumuz dizinde/klasörde/proje dosyasında geçerli olur.

- git config user.name "Aydın BEKOĞLU"
- git config user.email "aydinbek97@gmail.com"

> #### D_2. git config --global user.email "user_email"

Global olarak tanımlanır kullanıcı. Yani ilgili bilgisayar/serverda ki tüm git projelerinde bu kullanıcı adı/kullanıcı maili kullanılır.

- git config --global user.name "Aydın BEKOĞLU" => Github, GitLab hangi hizmet kullanılıyorsa onda ki mail adresi yazılmalı.
- git config --global user.email "aydinbek97@gmail.com" => Github, GitLab hangi hizmet kullanılıyorsa onda ki mail adresi yazılmalı.

> #### D_3. git config --global --get user.email

- git config --global --get user.name => git de tanımlı olan kullanıcı ismini gösterir.
- git config --global --get user.email => git de tanımlı olan kullanıcı mailini gösterir.

> #### D_4. Kaynak Siteler

- [techcareer.net - Git Init, Status, User](https://www.techcareer.net/courses/git-github-egitimi/d171b704-6dbe-4a8c-a497-e2b7ad8c4c40)

### E. git add komutu

Bu komut ile değişiklik yapılan ve git tarafından izlenmeyen/takip edilmeyen dosyaları izle/takip et diyoruz. Yeni eklenen, silinen veya üzerinde değişiklik yapılan dosyaları staged ortamına göndermek için kullanılır.

Yani çalışma klasöründeki seçili veya bütün dosyaları index(stage) ortamına taşıyor bu komut.

***dipnot;*** Bazı terminallerde "$ git add" başına dolar işareti eklemek gerekebilir.

> #### E_1. Tüm dosyaları izleme

Projede takip edilmeyen tüm dosyaları staged(index) ortamına alır. Örnek kullanımlar;

- git add .
- git add *
- git add -A .

***dipnot;*** "-A" all, tümü anlamına gelir. "." ise tüm dosya uzantılarını ifade eder.

> #### E_2. Belirli dosyaları izleme

Belirli dosyayı staged(index) ortamına alır.

- git add index.html

> #### E_3. Kaynak Siteler

- [Youtube - GIT | Proje İçindeki Birden Fazla Dosyanın Versiyon Kontrol Sistemine Eklenebilmesi #7](https://www.youtube.com/watch?v=TP2K4cx3Asw)
- [techcareer.net - Git Add, Commit](https://www.techcareer.net/courses/git-github-egitimi/ab60bef6-6d8a-4c09-9cf0-bf91e69c713d)

### F. git rm komutu

Staged ortamına eklenmiş bir dosyanın takibinin bırakılması yani untracked (izlenmeyen) hale getirilmesi sağlayan komuttur.

- dosyayı dizinden/klasörden silmek;
  - "git rm file_name"
  - "git rm foler_name"
  - "git rm --cached file_name"
  - "git rm --cached foler_name"

### G. git commit komutu

Commit, staged(index) ortamına alınan dosyaların Local Repository’e gönderilmesidir. Bu işlem git'in gönderilen dosyaları takip etmesini sağlar.

En iyi uygulama yöntemi her biten işlem sonrasında yapılan değişikliklere kısa ve açıklayıcı bir mesaj eklemektir. Ayrıca her commit benzersiz bir kimliğe (unique ID) sahip olur. Bu sayede eski bir commit'e geri dönebilirsiniz ve herhangi bir kayıp yaşama ihtimaliniz kalmaz.

> #### G_1. git commit -m "message" kullanımı

Mesajlı commit atmak. -m yazdıktan sonra mesajı "" bunların arasına yazıyoruz.

- git commit -m "git_ders_notu.md güncellendi"

> #### G_2. git commit --amend kullanımı

Son yapılan commit'i düzenlemeye veya güncellemeye olanak tanır. Yani commit mesajını veya commit'e eklenen dosyalar değiştirilmek istiyorsa bu komutu kullanılabilir.

Genellikle commit işlemi sırasında hata yapıldığında, commit mesajı değiştirilmek/düzenlenmek istenildiğinde veya commit'e eklemeyi unutulan değişiklikler/dosyalar olduğunda kullanılır. 2 farklı kullanımı vardır. Sadece commit mesajını değiştirmek veya commit mesajıyla birlikle dosya düzenlemek, eklemek, silmek.

- Sadece son commit mesajı düzenlenmek istenirse
  - git commit --amend => Commit mesajını düzenleme kısmını açar. İsterseniz commiti düzenlemeyin, ":q" basıp çıkabilirsiniz.
  - git commit --amend -m "commit mesajı değiştirme" => Mesajlı amend işlemi.
- Unutulan Dosyaları Commit'e Eklemek ve commit mesajını düzenlemek için adımlar
  - Yeni yapılan tüm değişiklikler "git add ." ile eklenir.
  - git commit --amend => Eğer commit mesajı değiştirilmek istenmiyorsa "***git commit --amend --no-edit***" kullanılmalı.

**dipnot:** Amend işlemi, commit geçmişini değiştirir, bu yüzden son commit'in başka bir yere push edilmemiş olması gerekir. Eğer commit'i bir uzak sunucuya (örneğin GitHub) push ettiysen, amend sonrası yeni commit'i force push (git push --force) ile göndermen gerekir. Aksi takdirde diğer geliştiricilerde uyumsuzluklar yaşanabilir. Eğer başkalarıyla birlikte çalışıyorsanız ve commit'i pushladıysanız, --amend kullanmadan önce ekibinizle iletişime geçmeniz önemlidir.

> #### G_3. Kaynak Siteler

- [techcareer.net - Git Add, Commit](https://www.techcareer.net/courses/git-github-egitimi/ab60bef6-6d8a-4c09-9cf0-bf91e69c713d)

### H. git log komutu

Projedeki commit geçmişini görüntülememizi sağlar. Bütün commit'ler => hangi branch üzerinde değişiklik yapılmış, commit id'si, yazarı, tarihi ve mesajı ile beraber listelenir.

![git log komutu](https://raw.githubusercontent.com/Kodluyoruz/taskforce/main/git/git-bash-ile-git-temel-komutlari/figures/6-git-log.png)

> #### H_1 git log Kullanımı

- git log => Tümünü getir.
- git log -n 1 => 1 tane getir. İlk sıradakini getirir.
- git log -n 2 => 2 tane getir. İlk 2'yi getirir. "-n" bu işe yarar kaç tane getirmek isteniyor. Sıralama en son eklenen commit yani en üstteki committen başlar.

> #### H_2. Kaynak Siteler

- [techcareer.net - Git Log Eğitimi](https://www.techcareer.net/courses/git-github-egitimi/58a72889-0f6e-4afb-8a7e-05b9af67ff24)

### I. Branch ile alakalı git komutları

Local veya remote repository üzerinde yeni bir branch (dal) eklemek, silmek, dallar arasında geçiş yapmak veya listelemek için kullanılır.

![git branch](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR4IkgIwsGWN52UBrCWimoeCqeQ4fo2F91_mg&s)

- git branch => Repository de var olan branchleri listeler. Aktif branchi de belirtir.
- git branch -a => Tüm uzak(remote) ve yerel(local) branchleri listelemek için;
- git branch -r => uzak(remote) ki branchleri listeteler.
- git branch dev_18 => dev_18 adında yeni bir branch açar.
- git branch -M main => "-M" ile main/ana branch oluşturur.
- git branch -d dev_18 => Belirtilen branchi siler.
- git switch dev_18 => Mevcutta var olan belirtilen branch'e geçiş yapar.
- git checkout dev_18 => Mevcutta var olan belirtilen branch'e geçiş yapar.
- git checkout -b dev_1 => dev_1 adında branch yoksa yeni bir branch oluşturur ve yeni branche geçiş yapar. Bu komut, o anda bulunan branch'in(aktif/çalışılan branch) son halini baz alarak yeni bir dal oluşturur ve bu dala geçiş yapar.
  - git checkout -b dev_2 dev_1 => Bu komut, var olan dev_1 dalını baz alarak dev_2 adında yeni bir dal oluşturur. Hangi branch'in aktif olduğunun bir önemi yok. dev_1 branchinde olmasanız bile dev_1 üzerinden dev_2 oluşturur ve dev_2'ye geçiş yapar.

> #### I_1. Kaynak Siteler

- [techcareer.net - Git Branch](https://www.techcareer.net/courses/git-github-egitimi/f62e862d-b535-4a88-a3c4-3227b6abcead)

### J. Git Merge

Başka bir branch'da olan değişiklikleri, bulunduğumuz branch ile birleştirmek istediğimizde kullanılır. Branchleri merge etmek için bir kaç farklı yöntem mevcut.

![git merge](https://media.geeksforgeeks.org/wp-content/uploads/20230516192737/git-three-way-merging.png)

> #### J_1 git merge header

Diyelim header branch'inde bir geliştirme yaptık. Sonra **git switch main** ile main branchine geçiş yaptık. Sonrasında **git merge header** dediğimizde header branchinde yapılan değişiklikler aktif olan branch (main) ile birleşir.

> #### J_2 git merge --squash header

Bunda da aynı birleştirme sağlanıyor tek farkı birleşme sonrasında commit atmak gerekiyor. Örnek commit mesajı; "***Footer, Aktif branch ile birleştirildi***" şeklinde olabilir.

Fakat bunu yaptığınızda header branchinde daha öncesinde atılan commitler birleştirilen branchde görülmez. Sadece son yazılan commit görünür.

*dipnot:* Şahsen ben bunu önermiyorum normal "merge" çok daha mantıklı geliyor bana. Çünkü header branchinde attığınız commitler gözükmez bu yöntemde.

> #### J_3 git merge --abort

Merge işleminde bir sorun çıktı. Örneğin "conflict" gibi bir sorun ve merge işlemini geri almak, iptal etmek istiyorsunuz.

> #### J_4. Kaynak Siteler

- [techcareer.net - Git Merge Eğitimi](https://www.techcareer.net/courses/git-github-egitimi/c2fb823c-b809-400f-8096-1833fd91ac44)

### K. git stash Komutları

![git stash Komutları](https://media.geeksforgeeks.org/wp-content/uploads/20230504190403/Screenshot-(51).png)

- git stash => Son committen itibaren yapılan tüm değişiklikler "stash" de saklanır.
- git stash pop => En üstteki, en son stash kaydını getirir. Stash'e atılan değişiklikler geri gelir ve o stash'i siler.
- git stash apply => En üstteki, en son stash kaydını getirir. Stash'e atılan değişiklikler geri gelir. Belirtilen stash silinmez "git stash pop" aksine.
- git stash list => stash alınanların listesini gösterir.
- git stash apply stash@{0} => Index'i belirtilen stash geri getirilir. Belirtilen stash silinmez "git stash pop" aksine.
- git stash clear => Tüm stash'leri siler.

> #### K_1. Kaynak Siteler

- [techcareer.net - Git Stash, Pop, List, Apply, Clear](https://www.techcareer.net/courses/git-github-egitimi/a9e523f2-3efd-4c2b-8135-ad332dc0245e)

### L. Git Restore, Checkout

> #### L_1. git restore file_name

Bu komut ile son yapılan değişiklikleri geri alırız. Yani bir adım geriye dönebiliriz.

> #### L_2. git checkout commit_hashdID

Commitler arası geçiş yapmak için: (Eski bir versiyona dönmek istediğimiz zaman). Seçili commite geçiş yaptıktan sonra yeni boş bir branch açıp "git switch new_branch" ile o branche geçiş yapabiliriz. Böylece geçmişte yaptığımız commit üzerinden branch açıp eski geliştirmeleri o branche taşımış oluruz.

> #### L_3. Kaynak Siteler

- [techcareer.net - Git Restore, Checkout](https://www.techcareer.net/courses/git-github-egitimi/6d22ed0f-4326-4058-9b50-031beeb2c6ed)
- [Medium - Git — Commit Geri Alma Seçenekleri](https://muratbaseren.medium.com/git-ile-commit-geri-alma-secenekleri-7bf352cf7fed)

### M. Git Reset, Revert

Git'te yaptığınız bir commit'i geri almanın birkaç yolu vardır. İhtiyacınıza göre aşağıdaki yöntemlerden birini kullanabilirsiniz.

> #### M_1. git reset commit_hashdID

Seçili commite gider ve o commit en son commit olur. Ondan sonra atılan yeni/son commitler tamamen silinir. Yapılan dosya değişiklikleri/geliştirmeler kalır sadece commitler silinir. *Örneğin;*

3 adet commit mesajımız olsun (first_commit_hashdID, second_commit_hashdID, third_commit_hashdID). Hepsinde farklı geliştirmeler mevcut. ***git reset first_commit_hashdID*** ile ilk commite gittik. Diğer commit mesajlarımız silindi yok edildi fakat geliştirmeleri durmaya devam eder.

- **Commit geçmişi:** Belirtilen commit'e geri dönersin ve o commit'ten sonraki commit'ler silinir.
- **Staging area:** Staging area'daki (index'teki) değişiklikler silinir. Yani git add ile eklenen dosyalar.
- **Çalışma klasörü:** Çalışma klasöründeki değişiklikler silinmez. Yani, dosyalarındaki değişiklikler korunur ama commit ve staging area temizlenir. Değişiklikler hala çalışma klasöründe gözükür.

> #### M_2 git reset --soft commit_hashdID

"git reset commit_hashdID" tek farkı staging area'daki değişikliklerde kalır/silinmez.

- **Commit geçmişi:** Belirtilen commit'e geri dönersin ve o commit'ten sonraki commit'ler silinir.
- **Staging area:** Değişiklikler staging area'da (index) kalır.
- **Çalışma klasörü:** Çalışma klasöründeki değişiklikler silinmez. Yani, dosyalarındaki değişiklikler korunur

> #### M_3. git reset --hard commit_hashdID

Seçili commite gider ve o commit en son commit olur. Ondan sonra atılan yeni/son commitler tamamen silinir. Yapılan dosya değişiklikleri/geliştirmeler kalmaz commitlerle birlikte onlarda silinir. **Bu tehlikeli bir işlemdir geri alınamaz!**

- **Commit geçmişi:** Belirtilen commit'e geri dönersin ve o commit'ten sonraki commit'ler silinir.
- **Staging area:** Staging area'daki (index'teki) değişiklikler silinir. Yani git add ile eklenen dosyalar.
- **Çalışma klasörü:** Çalışma klasöründeki dosyalardaki tüm değişiklikler kaybolur. Dosyalar, commit_hashID'e karşılık gelen commit'in içeriğine döner.

> #### M_4. git revert commit_hashdID

Seçili committe yapılan değişikliklerini geri alır. Revert işleminden sonra yeni bir commit atılır ve değişiklikler geri alınmış olur. Yeni atılan committe, revert işlemi olduğunu git otomatik belirtir.

Commit mesajı ve mesaja ait geliştirmeler log da (git log) durmaya devam eder, resette olduğu gibi silinmez. Bu yüzden yeni oluşan commiti de geri almak mümkündür. Yine git revert yapılır ve geri alınan değişiklikler geri gelir.

**dipnot;** hashdID'nin tamamını almaya gerek yok. İlk 7-8 karakter yetiyor.

> #### M_5. Kaynak Siteler

- [techcareer.net - Git Reset, Revert](https://www.techcareer.net/courses/git-github-egitimi/97d0c71f-0a17-46ec-8e25-d2dc1dcc4815)
- [Medium - Git — Commit Geri Alma Seçenekleri](https://muratbaseren.medium.com/git-ile-commit-geri-alma-secenekleri-7bf352cf7fed)

### N. git diff

Repository üzerinde yapılan değişikliklerden sonra dosyalar arasında oluşan farklılıkları göterir. Sadece kayıt edilen alanlardaki farklılıkları değil aynı zamanda;

***Commitler, Branchler, ilgili dosyalar*** arasındaki farkları da gösterir.

> #### N_1. git diff

En son yapılan değişiklikleri son commit ile kıyaslar ve farklılıkları gösterir.

> #### N_2 git diff HEAD

Son commit öncesinde yapılan işlemleri gösterir. Çalışma dizini ile repository (HEAD) arasındaki farklılıkları görmek için:

> #### N_3 git diff main demo

Belirtilen branchler arasında ki farklılıkları gösterir.

> #### N_4. git diff index.html

Verilen dosyadaki değişiklikleri gösterir.

> #### N_5. git diff eski_commit_hashdID..yeni_commit_hashdID

Belirtilen commitler arasında ki farklılıkları gösterir. Eğer dosya ismi verilmezse, tüm projedeki değişiklikleri/farklılıkları gösterir. Dosya dosya gösterir bunları.

- git diff eski_commit_hashdID..yeni_commit_hashdID index.md => Burada index.md dosyasında ki farklılıkları kıyasladık.

> #### N_6  git diff --staged

Çalışma dizini ve staged ortamı arasındaki farkları görmek için:

> #### N_7. Kaynak Siteler

- [techcareer.net - Git Diff Eğitimi](https://www.techcareer.net/courses/git-github-egitimi/15aede67-50ab-4c79-9634-aa79ab1f8cf3)

### O. git remote add origin repository_url

Henüz remote repository bağlantınız aşağıdaki bu komut ile yerel(local) deponuzu uzak(remote) sunucudaki depoya bağlayabilirsiniz.

- git remote add origin http://uzak_deponun_adresi.git

> #### O_1. Kaynak Siteler

- [techcareer.net - Git Push Eğitimi](https://www.techcareer.net/courses/git-github-egitimi/9b8be52a-2493-404f-ad65-ab59f94bcc89)
- [patika.dev - GitHub'a Projemizin Eklenmesi ve Diğer Repo Hosting Web Platformları](https://academy.patika.dev/tr/courses/git/githuba-projemizin-eklenmesi-ve-diger-repo-hosting-web-platformlari)

### P. git push

Projemizde aldığımız commit'leri, remote repository'e gönderir. Commit’lediğimiz dosyaları versiyon kontrol sistemimize gönderir.

> #### P_1 git remote add origin repository_url

Henüz remote repository bağlantınız aşağıdaki bu komut ile yerel(local) deponuzu uzak(remote) sunucudaki depoya bağlayabilirsiniz.

> #### P_2. git push origin main

Bu komut ile komutu ile repomuza dosyalarımızı gönderelim. Burada bahsi geçen origin remote repository'nin kök dizinini belirtir ve sabit bir isimdir. main ise sizin çalıştığınız branch (dal)'ı belirtir.

> #### P_3. git push -u origin main

Bu komut ile komutu ile repomuza dosyalarımızı gönderelim. Burada bahsi geçen origin remote repository'nin kök dizinini belirtir ve sabit bir isimdir. main ise sizin çalıştığınız branch (dal)'ı belirtir.

***-u(veya --update):*** Bu flag, git push komutu ile kullanılır ve uzak sunucuya yerel branch'teki değişiklikleri gönderirken aynı adı taşıyan bir branch olup olmadığını kontrol eder. Eğer aynı adı taşıyan bir başka branch bulunursa, yerel branch ile onu ilişkilendirir (tracking) ve sonraki push işlemlerinde hedef branch olarak otomatik olarak bu uzak branch'i kullanır.

> #### P_4. Kaynak Siteler

- [techcareer.net - Git Push Eğitimi](https://www.techcareer.net/courses/git-github-egitimi/9b8be52a-2493-404f-ad65-ab59f94bcc89)
- [patika.dev - GitHub'a Projemizin Eklenmesi ve Diğer Repo Hosting Web Platformları](https://academy.patika.dev/tr/courses/git/githuba-projemizin-eklenmesi-ve-diger-repo-hosting-web-platformlari)

### R. GIT Pull Request

Kısaca, Pull request (kısaca PR - TR: çekme isteği), yazılım geliştirme sürecinde ekip içi işbirliğini sağlayan ve kod incelemelerini kolaylaştıran önemli bir araçtır. Sadece ekip içi değil, açık kaynaklı projelerde ekip dışından katkı sağlamak isteyen geliştiricilerin de kullandığı bir araçtır.

Genellikle Git gibi versiyon kontrol sistemlerinde kullanılan Pull Request, yeni bir kod değişikliğinin incelenmesi ve onaylanması sürecini yönetir. Bu şekilde projeye katkı sağlamak isteyen ekip üyelerinin ya da geliştiricilerin, projenin sahibine değişiklikleri önerir ve projenin sahibi bu değişiklikleri projeye dahil etmek veya reddetmek için karar verir.

> #### R_1. Kaynak Siteler

- [Youtube - Pull Request Nasıl Yapılır? Contribution | GitHub](https://www.youtube.com/watch?v=N_qEmSRsFlI)
- [techcareer.net - Git Pull Request](https://www.techcareer.net/courses/git-github-egitimi/00a12a9d-c54d-4653-b521-cda4664f22ec)
- [Git'te Pull Request Nasıl Yapılır: Adım Adım PR](https://mustafabaser.net/git-pull-request-nedir)

### S. git fetch & git pull

Her iki komut da bir havuzun yerel kopyalarını güncellemek için kullanılsa da, çok farklı şekillerde çalışırlar.

**'Git fetch'** => keşif gibidir; yerel deponuzu uzak bir depodaki değişikliklerle günceller ancak bu değişiklikleri mevcut çalışma branchle birleştirmez. Mevcut çalışmanızı etkilemeden nelerin değiştiğini görmenizi sağlar.

**'git pull'** => ise biraz daha fazlasını yapar; yalnızca uzak depodan güncellemeleri almakla kalmaz, aynı zamanda bunları otomatik olarak mevcut dalla birleştirir. Bu ayrım, başkalarıyla işbirliği yaparken temiz ve işlevsel bir kod tabanını korumayı amaçlayan geliştiriciler için çok önemlidir.

***dipnot 1:*** Eğer bir 'git pull' işlemini geri almanız gerekiyorsa, yerel branchi önceki durumuna döndürmek için 'git reset, git revert' gibi komutları kullanabilirsiniz.

***dipnot 2:*** git fetch ve git pull işlemlerinde illa remote branch name yazmaya gerek yoktur. Localde hangi branch aktif ise o branchnin remote'u kontrol edilir. Örneğin; ***git pull*** yazmak yeterli.

> #### S_1. git fetch Kullanımı

Herhangi bir değişikliği birleştirmeden remote depodan en son meta veri bilgilerini alır. Bilgileri almak ve değişiklikleri local repository taşımak için adımlar;

- git fetch origin branch_name
- git status
- git merge origin/branch_name

> #### S_2 . git pull Kullanımı

Fetch işlemi aksine merge işlemini otomatik yapar. Uzak depodan en son değişiklikleri getirir ve bunları local branch ile birleştirir.

- git pull origin branch_name

> #### S_3. Kaynak Siteler

- [techcareer.net - Fetch and Pull](https://www.techcareer.net/courses/git-github-egitimi/8c994fdd-4563-422e-a259-9781c8088070)
- [Git Fetch ve Git Pull'u Anlamak](https://www.tempmail.us.com/tr/git/git-fetch-ve-git-pull-u-anlamak)

D. git clone

Mevcut bir Remote Repository'de bulunan dosyaların bilgisayarımızda bir kopyasının oluşturulmasını sağlar.

- git clone <remote_URL>

H. - git rebase => Detaylı araştır.

> ## 7. Genel Kaynak Siteler

- [git sitesi - git kullanım](https://git-scm.com/book/tr/v2) => git'in kendi sitesinde bulunan Türkçe kaynak eğitim.
- [patika.dev - GIT Kursu](https://academy.patika.dev/tr/courses/git)
- [techcareer.net - Git ve GitHub Eğitimi](https://www.techcareer.net/courses/git-github-egitimi)
- [Medium - Temel Git terimleri ve komutları](https://medium.com/@alianilkocak/temel-git-terimleri-ve-komutlar%C4%B1-6bc62b802baf)
- [Medium - GIT CLI ile Komut Komut Versiyonlama!](https://medium.com/fedeveloper/git-bash-ile-komut-komut-versiyonlama-a354efd3063f)
- [Medium - Temel Git terimleri ve komutları](https://medium.com/@alianilkocak/temel-git-terimleri-ve-komutlar%C4%B1-6bc62b802baf)
- [Bilgi Üniversitesi - Türkçe Git 101](https://stk.bilgi.edu.tr/media/uploads/2015/01/12/git101.pdf)

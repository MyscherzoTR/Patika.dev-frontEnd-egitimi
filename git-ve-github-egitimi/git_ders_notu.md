# git ve Terminal Kullanımı Ders Notu

git ve Terminal Kullanımı ders notunu hazırlarken bir çok kaynaktan faydalandım. Elimden geldiğince basit ama işe yarar bir not hazırlamaya gayret gösterdim. Her konunun sonunda o konuyla alakalı faydalandığım kaynakları belirttim. Belirttiğim kaynaklardaki herşeyi bu nota eklemedim. Her konuyu okuduktan sonra mutlaka kaynaklarda içeriklere de göz atmalısınız. Faydalandığım kaynaklardan bazıları;

- Çeşitli Youtube kanalları
- Udemy, BTK Akademi tarzı eğitim siteleri
- patika.dev, coderspace, techcareer.net tarzı oluşumlar
- Medium sitesinde ki makaleler

Ders ile alakalı başlangıç teorik video ve makaleler - kesinlikle göz atılmalı;

- [Versiyon Kontrol Sistemi Nedir?](https://furkanalaybeg.medium.com/versiyon-kontrol-sistemi-nedir-2f47bb830064)
- [techcareer.net - Git Nedir?](https://www.techcareer.net/courses/git-github-egitimi/25f77b02-2a95-4cbb-a697-ab18b531c43e)

## 1. Git'in temel kavramları

***Git'in temel kavramlarını daha anlaşılır şekilde açıklayalım;***

- Çalışma Klasörü (Working Directory): Bu, projenin üzerinde çalıştığın alandır, yani dosyalarının fiziksel olarak bulunduğu klasördür. Git, bu klasördeki dosyaları izler. Dosyalarında yaptığın değişiklikler burada gerçekleşir.
- Index (Staging Area): Değişiklik yaptığın dosyaları commit etmeden önce, "sahneye" çıkardığın alandır. Yani commit'e dahil olacak dosyaları burada toplarsın. Bu aşamada, hangi dosyaların commit'e dahil olacağını belirleyip, son halini gözden geçirirsin.
- Local repository (Yerel Depo): Bu alan, yaptığın commit'lerin depolandığı yerdir. Yani projenin geçmişteki sürümlerinin tutulduğu yerdir. Commit'leri yapınca bu yerel repoda saklanır, henüz uzak sunucuya (GitHub, GitLab gibi) gönderilmemiştir.

### A. Özetle

- Çalışma klasöründe değişiklikler/düzenleme/geliştirme yaparsın.
- Commit'lemek istediğin dosyaları Staging Area'ya (Index) eklersin. Eklediğin dosyalar burada commit atılmasını bekler.
- Commit'le bu değişiklikleri Local Repository'ye kaydedersin. Commit geçmişinin localde tutulduğu yerdir.

## 2. git Kurulumu

[git kurulum](https://www.techcareer.net/courses/git-github-egitimi/4767eadf-4a02-45e4-8f7d-9f594d761223) videosunu izleyip git'i kurabilirsiniz. Kurulum tamamlandıktan sonra git'in terminali olan "Git Bash" yüklenecektir.

>### 2_1 Kaynak Siteler

- [git sitesi - git kullanım](https://git-scm.com/book/tr/v2)

## 3. Terminal Kullanımı ve Komutları

***dipnot 1:*** Terminalde klasör, dosya isimlerinde büyük-küçük harf hassasiyeti yoktur. Yani "desktop" klasörüne "cd DESKTOP" ile giriş yapabiliriz.

***dipnot 2:*** bir dosya veya klasör adının tamamını terminale yazmaya gerek yok. Örneğin "temel_seviye" adında bir klasör olsun. Bu klasörünün içine girmek istiyoruz.

"cd tem" yazdıktan sonra klavyeden **tab** tuşuna basarsak otomatik ismi tamamlayacaktır. Eğer birden fazla "tem" ile başlayan dosya varsa size tüm dosyaları gösterecektir. Otomatik tamamlamayacaktır.

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

### G. Kaynak Siteler

- [techcareer.net - Terminal Kullanımı](https://www.techcareer.net/courses/git-github-egitimi/d396eb35-184a-4277-9710-c61b0edfeb7e)

## 4. Terimler

A. untracked (izlenmeyen): GIT tarafından henüz takip edilmeyen, yani yeni oluşturulmuş dosyaları ifade eder.

B. unstaged (hazırlanmamış): Güncellenmiş ancak commit’lenmek için hazırlanmamış dosyaları ifade eder.

C. staged (hazırlanmış): Commit’lenmeye hazır olan dosyaları ifade eder.

D. deleted (silinmiş): Projeden silinmiş ama GIT üzerinden kaldırılmamış dosyaları ifade eder.

## 5. git Komutları

### A. git status komutu

Üzerinde çalışılan projenin o anki durumu hakkında bilgi verir. İlgili dizinde git olup olmadığı kontrol edilir. Eğer git varsa yapılan değişiklikler, izlenen/izlenmeyen dosyalar, eklenen ve silinen dosyalar gibi bilgiler listelenir. Kısacası tüm yapılan değişimleri söyler. Detaylı araştır!

***Dipnot:*** İlk defa bir projede çalışıyorsak bu komut ile kesinlikle git olup olmadığını kontrol etmeliyiz. Eğer git varsa tekrar eklememeliyiz.

> #### A_1. Kaynak Siteler

- [techcareer.net - Git Init, Status, User](https://www.techcareer.net/courses/git-github-egitimi/d171b704-6dbe-4a8c-a497-e2b7ad8c4c40)

### B. git init komutu

Git ilk defa ilgili proje içinde başlatılacaksa. Henüz versiyon kontrolü altında olmayan bir projenin dizininde, boş bir git deposu oluşturmak için kullanılır. local olarak git projesini oluşturuyoruz. Proje içine ".git" gizli şekilde ekliyor, oluşturuyor.

Bilgilendirme yazısı; "Initialized empty Git repository in proje_path/.git/"

> #### B_1. Kaynak Siteler

- [techcareer.net - Git Init, Status, User](https://www.techcareer.net/courses/git-github-egitimi/d171b704-6dbe-4a8c-a497-e2b7ad8c4c40)

### C. git config komutu

Yapılandırma ayarlarının içerisinde barındırıldığı bir komut. Örnek kullanım;

> #### C_1. git config user.name "user_name" kullanımı

Genel olarak tüm terminallerde geçerlidir bu kural. Sadece şuan içerisinde bulunduğumuz dizinde/klasörde/proje dosyasında geçerli olur bu kullanıcı adı.

- git config user.name "Aydın BEKOĞLU"

> #### C_2. git config --global user.email "user_email" kullanımı

Global olarak tanımlanır kullanıcı. Yani ilgili bilgisayar/serverda ki tüm git projelerinde bu kullanıcı adı/kullanıcı maili kullanılır.

- git config --global user.email "user_email" => Github, GitLab hangi hizmet kullanılıyorsa onda ki mail adresi yazılmalı.
- git config --global --get user.email => git de tanımlı olan kullanıcı mailini gösterir.

> #### C_3. Kaynak Siteler

- [techcareer.net - Git Init, Status, User](https://www.techcareer.net/courses/git-github-egitimi/d171b704-6dbe-4a8c-a497-e2b7ad8c4c40)

### D. git add komutu

Bu komut ile değişiklik yapılan ve git tarafından izlenmeyen/takip edilmeyen dosyaları izle/takip et diyoruz. Yeni eklenen, silinen veya üzerinde değişiklik yapılan dosyaları staged ortamına göndermek için kullanılır.

Yani çalışma klasöründe kileri index(stage) ortamına taşıyor bu komut.

Bazı terminallerde "$ git add" başına dolar işareti eklemek gerekebilir.

> #### D_1. Tüm dosyaları izleme

Projede takip edilmeyen tüm dosyaları staged(index) ortamına alır. Örnek kullanımlar;

- git add .
- git add *
- git add -A .

> #### D_2. Belirli dosyaları izleme

Belirli dosyayı staged(index) ortamına alır.

- git add index.html

> #### D_3. Kaynak Siteler

- [techcareer.net - Git Add, Commit](https://www.techcareer.net/courses/git-github-egitimi/ab60bef6-6d8a-4c09-9cf0-bf91e69c713d)

### F. git commit komutu

Commit, staged(index) ortamına alınan dosyaların Local Repository’e gönderilmesidir. Bu işlem git'in gönderilen dosyaları takip etmesini sağlar.

En iyi uygulama yöntemi her biten işlem sonrasında yapılan değişikliklere kısa ve açıklayıcı bir mesaj eklemektir. Ayrıca her commit benzersiz bir kimliğe (unique ID) sahip olur. Bu sayede eski bir commit'e geri dönebilirsiniz ve herhangi bir kayıp yaşama ihtimaliniz kalmaz.

> #### F_1. git commit -m "message" kullanımı

Mesajlı commit atmak. -m yazdıktan sonra mesajı "" bunların arasına yazıyoruz.

- git commit -m "git_ders_notu.md güncellendi"

> #### F_2. Kaynak Siteler

- [techcareer.net - Git Add, Commit](https://www.techcareer.net/courses/git-github-egitimi/ab60bef6-6d8a-4c09-9cf0-bf91e69c713d)

### G. git log komutu

Projedeki commit geçmişini görüntülememizi sağlar. Bütün commit'ler => hangi branch üzerinde değişiklik yapılmış, commit id'si, yazarı, tarihi ve mesajı ile beraber listelenir.

> #### G_1 git log Kullanımı

- git log => Tümünü getir.
- git log -n 1 => 1 tane getir. İlk sıradakini getirir.
- git log -n 2 => 2 tane getir. İlk 2'yi getirir. "-n" bu işe yarar kaç tane getirmek isteniyor. Sıralama en son eklenen commit yani en üstteki committen başlar.

> #### G_2. Kaynak Siteler

- [techcareer.net - Git Log Eğitimi](https://www.techcareer.net/courses/git-github-egitimi/58a72889-0f6e-4afb-8a7e-05b9af67ff24)

### H. .gitignore

.gitignore dosyasına yazılan uzantıları takip etmez, gözardı eder git. Bunlar için git ignore kullanılır;

- Büyük boyutlu dosyalar
- Kütüphane/Library eklemeleri
- Başkalarının görmesini istemediğiniz dosyalar(şifre, api key vb.)
- Takip edilmesine gerek duyulmayan gereksiz dosyalar

> #### .gitignore dosyası oluşturma

Bunun için bir çok sayfa, site mevzut. Çoğu zaman GitHub'ın kendi sitesinde ki şablonlar iş görüyor fakat nadirde olsa siteye ihtiyaç duyulabilir. Arama motoruna "gitignore generator" veya "gitignore PHP generator" yazarak birçok siteye ulaşabilirsiniz. Benim kullandığım site;

- [Toptal - gitignore generator](https://www.toptal.com/developers/gitignore)

> #### H_2. Kaynak Siteler

- [techcareer.net - Git Ignore](https://www.techcareer.net/courses/git-github-egitimi/fa58e056-cbe8-46d4-b12e-d06611460f23)

### I. Branch ile alakalı git komutları

![git branch](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR4IkgIwsGWN52UBrCWimoeCqeQ4fo2F91_mg&s)

- git branch => Repository de var olan branchleri listeler. Aktif branchi de belirtir.
- git branch dev_18 => dev_18 adında yeni bir branch açar.
- git branch -D dev_18 => Belirtilen branchi siler.
- git switch dev_18 => Belirtilen branch'e geçiş yapar.
- git checkout dev_18 => Belirtilen branch'e geçiş yapar.
- git checkout -b dev_1 => dev_1 adında yeni bir branch oluşturur ve yeni branche geçiş yapar.

> #### I_2. Kaynak Siteler

- [techcareer.net - Git Branch](https://www.techcareer.net/courses/git-github-egitimi/f62e862d-b535-4a88-a3c4-3227b6abcead)

### J. Git Merge

Branchleri merge etmek için bir kaç farklı yöntem mevcut.

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

- [Git Stash, Pop, List, Apply, Clear](https://www.techcareer.net/courses/git-github-egitimi/a9e523f2-3efd-4c2b-8135-ad332dc0245e)

### L. Git Restore, Checkout

> #### L_1. git restore file_name

Bu komut ile son yapılan değişiklikleri geri alırız. Yani bir adım geriye dönebiliriz.

> #### git checkout commit_hashdID

Yazılan commit'e geçiş yapar. Seçili commite geçiş yaptıktan sonra yeni boş bir branch açıp "git switch new_branch" ile o branche geçiş yapabiliriz. Böylece geçmişte yaptığımız commit üzerinden branch açıp eski geliştirmeleri o branche taşımış oluruz.

> #### L_1 Kaynak Siteler

- [Git Restore, Checkout](https://www.techcareer.net/courses/git-github-egitimi/6d22ed0f-4326-4058-9b50-031beeb2c6ed)

I. Commit düzenleme, geri alma vb. Yanlış commit atıldı (commit mesajı, düzenlenen dosya/dosyalar, commit atmadan önce eksik dosya eklendi vb.) bu durumlarda yapılması gereken. Örnek; bir dosya eksik eklendi veya commit atılan dosyaya yeni bir şey eklendi bu durumda yapılması gereken.

- Tüm değişiklikler "git add ." ile eklenir.
- git commit --amend => Bu komut en son eklenen commiti getirir. "git add ." ile eklenen son güncellemeleri ekler ve commit mesajını düzenleme kısmını açar. İsterseniz commiti düzenlemeyin, ":q" basıp çıkabilirsiniz.

J. git commit --amend -m "commit mesajı değiştirme" => Son commitin açıklaması/mesajı değişir.

K. git revert commit_hashdID => Seçili commit değişikliklerini geri alır. Hash ID için tamamını almaya gerek yok. İlk 7-8 karakter yetiyor.

- revert işleminden sonra yeni bir commit atılır ve değişiklikler geri alınmış olur. Bu yeni oluşan commiti de geri almak mümkündür. Yine git revert yapılır ve geri alınan değişiklikler geri gelir.

L. git reset --hard commit_hashdID => Seçili commit en son commit olur ve ondan sonra atılan commitler(daha yeni commitler) tamamen silinir. Bu tehlikeli bir işlemdir geri alınamaz.

M. git diff => en son yapılan commit'teki tüm değişiklikleri gösterir/söyler.

- git diff index.html: verilen dosyadaki değişiklikleri gösterir.

N. git diff eski_commit_hashdID..yeni_commit_hashdID index.md => 2 commiti karşılaştırır farklılıkları gösterir. Burada index.md dosyasında ki farklılıkları kıyasladık.

- index.md yazılmaz ise tüm değişiklikleri/farklılıkları gösterir. Dosya dosya gösterir bunları.

C. git pull =>

D. git fetch =>

H. - git rebase => Detaylı araştır.

T. git rm --cached index.html: Staged ortamına eklenmiş bir dosyanın takibinin bırakılması yani untracked (izlenmeyen) hale getirilmesi sağlayan komuttur.

- dosyayı dizinden/klasörden silmek;
  - "git rm <dosya_name>"
  - "git rm <klasor_name>"

> ## Kaynak Siteler

- [patika.dev - GIT Bash ile GIT Temel Komutları](https://app.patika.dev/courses/git/git-bash-ile-git-temel-komutlari)
- [Medium - Temel Git terimleri ve komutları](https://medium.com/@alianilkocak/temel-git-terimleri-ve-komutlar%C4%B1-6bc62b802baf)

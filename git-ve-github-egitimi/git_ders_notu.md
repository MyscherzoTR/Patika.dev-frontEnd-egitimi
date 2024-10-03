# git ve Terminal Kullanımı Ders Notu

- [Versiyon Kontrol Sistemi Nedir?](https://furkanalaybeg.medium.com/versiyon-kontrol-sistemi-nedir-2f47bb830064)

## 1. Terimler

A. untracked (izlenmeyen): GIT tarafından henüz takip edilmeyen, yani yeni oluşturulmuş dosyaları ifade eder.

B. unstaged (hazırlanmamış): Güncellenmiş ancak commit’lenmek için hazırlanmamış dosyaları ifade eder.

C. staged (hazırlanmış): Commit’lenmeye hazır olan dosyaları ifade eder.

D. deleted (silinmiş): Projeden silinmiş ama GIT üzerinden kaldırılmamış dosyaları ifade eder.

## 2. git Komutları

A. git init => Git ilk defa ilgili proje içinde başlatılacaksa. Henüz versiyon kontrolü altında olmayan bir projenin dizininde, boş bir git deposu oluşturmak için kullanılır. local olarak git projesini oluşturuyoruz. Proje içine ".git" gizli şekilde ekliyor, oluşturuyor. 
Bilgilendirme yazısı; "Initialized empty Git repository in proje_path/.git/"

B. git status => Üzerinde çalışılan projenin o anki durumu hakkında bilgi verir. Yapılan değişiklikler, eklenen ve silinen dosyalar gibi bilgiler listelenir. Detaylı araştır!

C. git pull =>

D. git fetch =>

E. git add Kullanımı => Bu komut ile değişiklik yapılan ve git tarafından izlenmeyen/takip edilmeyen dosyaları izle, takip et diyoruz. Yeni eklenen, silinen veya üzerinde değişiklik yapılan dosyaları staged ortamına göndermek için kullanılır. Bazı terminallerde "$ git add" başına dolar işareti eklemek gerekebilir.

- "git add .", "git add *" veya "git add -A ." => Projede takip edilmeyen tüm dosyaları takip eder.
- git add index.html => Belirli dosyayı takip eder.

F. git commit: Commit, staged ortamına alınan dosyaların Local Repository’e gönderilmesidir. En iyi uygulama yöntemi her kayıt sırasında yapılan değişiklikleri açıklayıcı bir mesaj eklemektir. Ayrıca her commit benzersiz bir kimliğe (unique ID) sahip olur. Bu sayede eski bir commit'e geri dönebilirsiniz ve herhangi bir kayıp yaşama ihtimaliniz kalmaz. 

G. git commit -m "git_ders_notu.md güncellendi" => Mesajlı commit atmak. -m yazdıktan sonra mesajı "" bunların arasına yazıyoruz.

H. git log => Projedeki commit geçmişini görüntülememizi sağlar. Bütün commit'ler, id'si, yazarı, tarihi ve mesajı ile beraber listelenir.

- git log => Tümünü getir.
- git log -n 1 => 1 tane getir. İlk sıradakini getirir.
- git log -n 2 => 2 tane getir. İlk 2'yi getirir. "-n" bu işe yarar kaç tane getirmek isteniyor. Sıralama en son eklenen commit yani en üstteki committen başlar.

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

O. git branch => Branch ile alakalı git komutları

- git branch => Repository de var olan branchleri listeler. Aktif branchi de belirtir.
- git branch dev_18 => dev_18 adında yeni bir branch açar.
- git branch -D dev_18 => Belirtilen branchi siler.

P. git checkout => Branch ile alakalı git komutları

- git checkout dev_18 => Belirtilen branch'e geçiş yapar.
- git checkout -b dev_1 => dev_1 adında yeni bir branch oluşturur ve yeni branche geçiş yapar.

R. git stash => stash komutları

- git stash => Son committen itibaren yapılan tüm değişiklikler "stash" de saklanır.
- git stash list => stash alınanların listesini gösterir.
- git stash clear => Tüm stash leri siler.
- git stash pop => En üstteki, en son kaydı getirir ve o stash siler. Stash atılan değişiklikleri geri gelir.
- git stash apply stash@{0} => Belirtilen stash geri getirilir. Belirtilen stash silinmez "git stash pop" aksine.

S. Branchleri merge etmek => Bir kaç farklı yöntem mevcut.

- git merge header => header branchini aktif olan, seçili branch ile birleştirir. Yani header branchinde yapılan değişiklikler aktif olan branche eklenir.
- git merge --squash footer => Bunda da aynı birleştirme sağlanıyor tek farkı birleşme sonrasında commit atmanız gerekir. Attığınız commit; "Footer, Aktif branch ile Birleştirildi" bu şekilde olabilir. Fakat bunu yaptığınızda Footer branchinde atılan commitler aktif branche görülmez sizin commit mesajında yazdığınız commit görünür. Şahsen ben bunu önermiyorum normal "merge" çok daha mantıklı geliyor bana.
- git rebase => Detaylı araştır.
- git merge --abort => Merge işleminde bir sorun çıktı "conflict" gibi ve merge işlemini geri almak, iptal etmek istiyorsunuz.

T. git rm --cached index.html: Staged ortamına eklenmiş bir dosyanın takibinin bırakılması yani untracked (izlenmeyen) hale getirilmesi sağlayan komuttur.

- dosyayı dizinden/klasörden silmek "git rm <dosya veya klasor_name>"

U. Diğer git komutları makale: [patika.dev - GIT Bash ile GIT Temel Komutları](https://app.patika.dev/courses/git/git-bash-ile-git-temel-komutlari)

V. Temel Git terimleri ve komutları => [Medium - Temel Git terimleri ve komutları](https://medium.com/@alianilkocak/temel-git-terimleri-ve-komutlar%C4%B1-6bc62b802baf)

## 3. Terminal Komutları

A. ls => klasör/dizin içindekileri listeler.

B. ls -la =>  Tüm dosyaları ve dizinleri ayrıntılı bir şekilde listelerken, gizli dosyaları da gösterir. Fakat Linux sistemlerde çalışır. Windows için aşağıdakiler kullanılabilir.

- Get-ChildItem -Force
- ls -Force

C. cd .git/ => .git klasörüne girer.

D. touch deneme.txt => Dosya oluşturur. Fakat Linux sistemlerde çalışır.

- New-Item deneme.txt
- New-Item example.txt -ItemType File => Dosya tipi File belirttik.

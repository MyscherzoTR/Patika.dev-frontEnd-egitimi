# GitHub ve Github Desktop Ders Notları

## 1. GitHub

Github, özellikle yazılım geliştiricileri tarafından kullanılan bir web tabanlı kod barındırma ve versiyon kontrol sistemi olarak bilinir. İşletmeler ve açık kaynaklı projeler gibi birçok kişi ve kuruluş tarafından kullanılan Github, birçok avantajı ve özelliği ile öne çıkar.

### A. Neden GitHub Kullanmalıyız

- İşbirliği(Collaboration): Github, birden fazla kişinin aynı kod üzerinde çalışmasına izin vererek, ekipler arasındaki işbirliğini kolaylaştırır. Projenin herhangi bir yerinde yapılan değişiklikler otomatik olarak senkronize edilir ve diğer kullanıcılar tarafından görülebilir.
- Versiyon Kontrolü(Version Control): Github, değişikliklerin takibi ve farklı sürümlerin saklanması için geliştirilmiş bir versiyon kontrol sistemi olarak kullanılır. Bu sayede, projenin herhangi bir noktasında geri dönüş yapılabilir veya ilerleyen bir versiyona geçilebilir.
- Bunu her hafta bir derse girdiğimizi ve bu derslerimizi bir defterde tuttuğumuzu; dilediğimiz zaman dilediğimiz dersin bilgilerine erişebilir durumda olacağımızı ve o ders bilgileri arasında anlık değiştirmeler yapabilecek olacağımızı düşünerek daha da iyi kavrayabiliriz.
- Açık Kaynaklı Projeler(Open Source Projects): Github, açık kaynaklı projelerin geliştirilmesinde önemli bir rol oynar. Açık kaynaklı projelerin kodları, herhangi bir kişi tarafından görüntülenebilir ve kullanılabilir haldedir. Kodluyoruz Açık Kaynak’ı bu kapsamda tutabiliriz.
- Kolay Entegrasyon(Easy Integration): Github, diğer kod geliştirme araçları ve hizmetleriyle kolay bir şekilde entegre edilebilir. Bu sayede, geliştiricilerin kullandığı diğer araçlarla uyumlu hale getirilebilir.

## 2. Yararlı Kısayollar

A. CTRL + P => Eğer proje localdeyse, repository Publish yapma yerini açar. Github'a pushlama yeri. Proje Github da ise ve bir değişiklik yapıldıysa yapılan değişikliği Pushlar.

B. CTRL + R => Pull Request işlemini başlatır.
  
C. CTRL + I => Repository için Github'da Issue oluşturma (sorun kaydı oluşturur. Detaylı araştırılmalı!).

D. CTRL + ` => Seçilen Komut istemcisinde açar Repository dizini/path.

E. CTRL + Shift + A => Repository'i varsayılan External Editör veya IDE'de açar. Benim bilgisayarımda "VS Code"

F. CTRL + Shift + F => Repository klasörünü açar.

G. CTRL + Shift + G => Repository Github hesabında varsa onun sayfasını açar.

H. CTRL + Shift + P => Pull işlemi yapar. Github dan güncel değişiklikleri çeker.

I. CTRL + Shift + N => New branch; Yeni Branch açar.

J. CTRL + Shift + R => Rename; Aktif Branch adını değiştirir.

K. CTRL + Shift + D => Delete; Aktif Branchi siler.

L. CTRL + Shift + Backspace => Discard all changes; Yapılan tüm değişiklikler geri alınır, iptal edilir.

M. CTRL + Shift + S => Stash all changes; Commit yapmak istenilmediğinde kullanılır stash'e alma. Bunu detaylı araştır.!

N. CTRL + Shift + U => Update from main; Aktif branch'e, main branchde ki son değişiklikleri çeker.

O. CTRL + Shift + B => Compare to branch; 2 farklı branch'i karşılaştırır(origin main ve local main içinde karışlaştırma yapılır. Branch seçimini kullanıcı kendi yapar).

P. CTRL + Shift + C => Compare on Github; Githab üzerinden 2 farklı branch'i karşılaştırır(origin main ve local main içinde karışlaştırma yapılır. Branch seçimini kullanıcı kendi yapar).
___

## 3. Gitignore Oluşturmak için Site

.gitignore nedir ve detaylı öğrenmek için GitHubda paylaştığım bu konuyu okumanızda fayda var => [GIT, .gitignore Dosyası](https://github.com/bekogluaydin/patika.dev-egitimi/blob/main/git-ve-github-egitimi/git_ders_notu.md#6-git-gitignore-dosyas%C4%B1)

A. .gitignore Oluşturma

- [Toptal - gitignore generator](https://www.toptal.com/developers/gitignore)
- [github - gitignore](https://github.com/github/gitignore)

___

## 4. Git Desktop Yararlı Bilgiler

A. Commit History kısmında her hangi bir commit tıklayıp ayalar çarkına basıp açılan menüde "Hide whitespace changes" seçeneği seçmek.
- Beşinci satırda bir kod yazdınız ve commit attınız. Sonrasında Beşinci satırdaki kodun üstüne başka bir şey yazdınız. Bu durumda kaç satırlık değişiklik olduysa Beşinci satırdaki kod 6, 10 vb. satıra kadar ilerler. Ve bu commit değişikliklerinde görünür. O kod silinmedi veya düzenlenmedi sadece satırı değişti bu tarz şeyleri görmek kafa karışıklığına neden olabilir.
- Hide whitespace changes" sayesinde bunları gizleyebiliyoruz. Eklenen, silinen, düzenlenen kod kısımlarını görüyoruz. Gerçekten değişiklik yapılan kısımları gösteriyor.

B. "Diff display", "Hide whitespace changes" ile aynı yerde.
- Unified => Değişiklikleri tek bir yerde alt alt gösterir.
- Split => Değişiklikleri commit atarken ki gibi 2 farklı yerde gösterir. 59. satırda bir değişiklik oldu diyelim bunu sol ve sağ olarak gösterir. Eski hali solda yeni hali sağda olacak şekilde.
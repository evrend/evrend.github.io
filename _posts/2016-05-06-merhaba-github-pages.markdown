---
title:  "Merhaba Github Pages!"
date:   2016-05-06 00:00:00
categories: [github]
tags: [github, jekyll]
---

Github Pages altyapısını ve desteklediği Jekyll Blog teknolojisini kullanarak nasıl kendi bloğunuzu oluşturabilirsiniz ondan bahsedeceğim.

Jekyll ruby ile geliştirilmiş, statik olarak içerikleri yönetmenizi sağlayan, çok hızlı ve güvenli bir teknoloji. Github'da Jekyll'nin bu avantajlarından faydalanarak, biz yazılımcılar için kendi sayfalarını oluşturmalarına imkan tanıyor.

**Github Pages Kullanarak Bloğunuzu Oluşturma**

Öncelikle [Github Pages][github-pages] sayfasını ziyaret ederek bu konudaki en güncel bilgilere ulaşabilirsiniz. Github bizlere iki seçenek sunuyor. İlki [kullanıcılar][users] ve [organizasyonlar][organizations] için sayfa oluşturma. İkincisi [projeler][projects] için sayfa oluşturma. Biz ilk seçenek olan [kullanıcılar][users] için sayfa oluşturma imkanından yararlanacağız.

Bu anlattıklarımı uygulayabilmeniz için öncelikle bir Github hesabınızın olması gerekiyor. Hesabınızla giriş yaptıktan sonra;
Sağ üst tarafta bulunan + işaretine tıklayarak "new repository" seçiniz. Yani kısacası yeni bir repository oluşturacağız.

![new-repo](/images/blog/2016-05-06-merhaba-github-pages/1.png)

Açılan sayfada en önemli nokta repo adınız kullanıcıadınız.github.io şeklinde tanımlamalısınız. Benim için bu [evrend.github.io][users] şeklinde. Sizde kendinize göre ayarlayınız.

![create-repo-secreen](/images/blog/2016-05-06-merhaba-github-pages/2.png)

Sonraki adımda oluşturduğumuz repoyu bilgisayarımıza klonlamalıyız. Klonladığımız repo bloğumuzun tüm içeriğini barındıracaktır. Ben git bash kullanarak github reposunu bilgisayarıma klonluyorum.

``` php
git clone https://github.com/kullanıcıadınız/kullanıcıadınız.github.io
```

![clone-repo](/images/blog/2016-05-06-merhaba-github-pages/3.png)

Repomuzu bilgisayarımıza klonladığımıza göre Jekyll için bir tema seçerek, blogumuzu kullanmaya başlayabiliriz. Jekyll için ücretsiz onlarca tema bulunmaktadır. [jekyllthemes.org][jekyllthemes] adresinden istediğiniz temayı seçerek indirin. Sonrasında zip dosyasının içeriğini az önce indirdiğimiz repomuzun içerisine çıkarın. Repomuzun içerisi aşağıdaki resimdeki gibi görünecektir. Temanızın düzgün görünmesi için _config.yml dosyasında url: 'https://evrend.github.io/' ve baseurl: '/' ayarlarınızı kendinize göre ayarlayınız.

![repo-theme-directory](/images/blog/2016-05-06-merhaba-github-pages/4.png)

Sonrasında sırasıyla aşağıdaki komutları çalıştırarak yaptığımız değişiklikleri commitleyip, github repomuza geri göndereceğiz(push).

``` php
//Reponuzun olduğu klasöre geliniz.
cd evrend.github.io
//Yaptığınız tüm değişiklikleri git commit için ekleyin.
git add .
//Yaptığınız değişiklikleri commitleyin.
git commit -m "Tema test için ilk commit."
//Yaptığımız commit'i repoya gönderiyoruz.
git push origin master
```

Yukarıdaki adımlar hatasız yapıldığı taktirde, kullanıcıadınız.github.io adresinden github sayfanıza giriş yaparak sayfanıza göz atabilirsiniz. sayfam üzerinde yaptığım değişiklikleri görmek için [yaptığım commitleri][projects-commits] incelemeniz yeterlidir. Blog yazıları markdown ile nasıl yazılır diye merak ediyorsanız, sayfamın reposunda post klasörü altındaki postları inceleyebilirsiniz.

Not: Benim kullandığım tema [jekyllthemes.org][jekyllthemes] sitesindeki [jekyll-uno](http://joshgerdes.com/jekyll-uno/) temasıdır.

Bir daha ki yazıya kadar hoşça kalın.

[github-pages]:https://pages.github.com/
[users]: https://github.com/evrend
[organizations]:https://github.com/herkod
[projects]:https://github.com/evrend/evrend.github.io
[projects-commits]:https://github.com/evrend/evrend.github.io/commits/master
[jekyllthemes]:http://jekyllthemes.org/

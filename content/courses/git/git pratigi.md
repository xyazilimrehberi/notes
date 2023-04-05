---
title: git pratigi
---

Bu bölümde Git'in en temel özelliklerini ele alacağım. İlk olarak, bir klasör oluşturarak içinde Git'i başlatacağım. Ardından, "Merhaba Dünya" metnini içeren, `hello.txt` isminde  bir metin dosyası oluşturup bu dosyayı Git'e commit edecek ve bu commit'i git log'unda (kayıt günlüğünde) görüntüleyeceğim. Son olarak, Git'in versiyon takibi yapabilme özelliğini göstermek için bu commit'i geri alıp repo'yu önceki versiyona alacağım. Bu bölüm, bize Git'in temel işlevleri hakkında pratik bir giriş sağlayacak.

## Adım 1: Klasör oluşturma

Terminalinizi veya windows'ta çalışıyorsanız cmd'yi açın, git test klasörünüzü oluşturmak istediğiniz dizine gidin ve ardından yeni bir klasör oluşturmak için aşağıdaki komutu çalıştırın:

```bash
mkdir git-test
```

## Adım 2: Klasörün içine gidin

Yeni oluşturduğunuz klasöre gitmek için aşağıdaki komutu çalıştırın:

```bash
cd git-test
```

Şimdi bu klasördeki dosya ve dizinleri görüntülemek için `ls -lah` komutunu çalıştırın ve klasörün henüz boş olduğunu görün.

## Adım 3: Git repo'yu başlatın

Klasörde yeni bir Git deposu başlatmak için aşağıdaki komutu çalıştırın:

```bash
git init
```

Şimdi `ls -lah` komutunu tekrar çalıştırın ve git init komutu ile oluşturulan `.git` klasörünü görün. Tüm commit geçmişiniz ve değişiklikleriniz bu gizli `.git` klasöründe tutulacak.

<iframe width="560" height="315" src="https://www.youtube.com/embed/6OOFo0Nh_SA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Adım 4: "Merhaba Dünya" metnini içeren bir metin dosyası oluşturun

İçinde "Merhaba Dünya" metni bulunan `hello.txt` adında yeni bir metin dosyası oluşturmak için aşağıdaki komutu çalıştırın:

```bash
echo "Hello World" > hello.txt
```

* Bu dosyayı oluşturmak ve aşağıdaki videoda yaptığım gibi "Merhaba Dünya" metnini eklemek için [[Vim metin düzenleyicisi]]ni de kullanabilirsiniz.

Bu komut ile hello.txt dosyasındaki metni kontrol edebilirsiniz:

```bash
cat hello.txt
```

Ya da sadece dosyayı açın ve metni okuyun.

## Adım 5: Metin dosyasını ekleyin ve commit yapın

Şimdi henüz git'e eklenmemiş değişiklikleriniz olduğunu görmek için bu komutu çalıştırın:

```bash
git status
```

`hello.txt` dosya adının çıktıda kırmızı renkle listelendiğini görüyorsunuz. Kırmızı renk, değişikliklerinizi henüz git'e eklemediğinizi gösterir.

<iframe width="560" height="315" src="https://www.youtube.com/embed/CHC_87kWLGM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Şimdi `hello.txt` dosyasını Git repo'nuza eklemek için aşağıdaki komutları çalıştırın:

```bash
git add hello.txt
```

Şimdi git status komutunu tekrar çalıştıdığınızda dosya adının yeşil renkte olduğunu göreceksiniz. Şimdi değişikliklerinizi commit etmek ve repo'nuzun yeni sürümüne eklemek için aşağıdaki komutu çalıştırın:

```bash
git commit -m "Added hello.txt with Hello World text"
```

Yukaridaki komuttaki `-m` argümanı, geçmişte yaptığınız değişiklikleri hatırlamanıza yarayan bir commit mesajı eklemenize olanak tanır. Bu commit mesajı, gelecekte log'larınızı gözden geçirirken değişikliklerinizi hatırlamanız açısınsan oldukça önemlidir. Her zaman, yaptığınız değişiklikleri doğru bir şekilde yansıtan anlamlı ve açıklayıcı bir commit mesajı kullanmaya özen gösterin. Bu, sizin ve aynı repo üzerinde birlikte çalıştığınız diğer kişilerin commit geçmişine baktıklarında (örneğin `git log`), commit'in amacını ve içeriğini kolayca anlamasına yardımcı olacaktır.

## Adım 6: Commit'i günlükte görüntüleyin

Az önce yaptığınız işlemi Git günlüğünde göstermek için aşağıdaki komutu çalıştırın:

```bash
git log
```

Günlükte commit mesajını ve commit'in diğer ayrıntılarını göreceksiniz.

<iframe width="560" height="315" src="https://www.youtube.com/embed/-9U9FYyDcIc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Adım 7: Bir önceki versiyona geri dönün

Şimdi, hello.txt dosyasının olmadığı ilk duruma geri dönelim. Son işlemi geri almak için aşağıdaki komutu çalıştırın:

```bash
git revert HEAD
```

Bu, önceki commit'te yapılan değişiklikleri geri alan yeni bir commit oluşturacak ve git repo'nuz bir önceki durumuna geri dönecektir.

## Adım 8: Günlükte bu işlemi görüntüleyin

Git günlüğünde revert(geri alma) commit'ini görüntülemek için aşağıdaki komutu çalıştırın:

```bash
git log
```

Git günlüğünde, diğer ilgili bilgilerle birlikte revert commit'inin ayrıntılarını görüyor olacaksınız. Bu bölümde Git ile oluşturduğunuz repo'da, Git'in işlemlerinizi takip etme ve versiyon takibini yapmanızda ne kadar güçlü bir araç olduğunu gördünüz. Kod tabanınızda yapılan değişiklikleri commit günlüğü aracılığıyla görüntülemek ve takibini yapabilmek, kod geliştirirken versiyon kontrolünde önemli bir adımdır. Git, projenizin geçmişini etkili bir şekilde yönetmenize ve izlemenize olanak tanır.

<iframe width="560" height="315" src="https://www.youtube.com/embed/TzUtIy0cg2Q" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Sıradaki: [[courses/git/Son bolum|Son bölüm]]

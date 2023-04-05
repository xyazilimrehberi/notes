---
title: git kurulumu
---


Git'i kullanmaya başlamak için önce bilgisayarınıza yükleyelim. Kurulum adımları işletim sisteminize bağlı olarak farklılık gösterecektir. Aşağıda, windows dahil olmak üzere, farklı işletim sistemleri için gerekli adımlarda size rehberlik edeceğim. Kodlama öğrenme yolculuğunuzun bu noktasında işletim sisteminizi değiştirmenize gerek olmadığını belirtmekte fayda var. Ancak, .Net Framework ile devam etmeye karar vermediğiniz sürece, öğrenme yolculuğunuzda daha da ilerlemeye karar verdiğinizde macOS veya Ubuntu gibi Unix benzeri işletim sistemlerini kullanmanızı tavsiye ediyorum.

Git ile çalışmaya başlamadan önce, Git'in bilgisayarınızda halihazırda yüklü olup olmadığını kontrol edelim. macOS veya Ubuntu gibi herhangi bir Unix benzeri işletim sistemi kullanıyorsanız, [[terminali acmak|terminali açarak]] (Windows kullanıyorsanız, [[cmd yi acmak|CMD'yi açarak]]) aşağıdaki komutu yazın,

```bash
git --version
```

Eğer Git bilgisayarınızda yüklüyse, verisyon numarasının görüntülendiğini göreceksiniz, örneğin:

```bash
> git version 2.30.1 (Apple Git-130)
```

Ancak, aşağıdaki gibi bir çıktı görürseniz

```bash
> command not found: git
```

git'i yüklemeniz gerekiyor.

==macOS kullanıcıları== için, Git'i macOS için bir paket yöneticisi olan Homebrew kullanarak yükleyebilirsiniz. Homebrew'u yüklemek için Terminal'i açın ve aşağıdaki komutu çalıştırın:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Homebrew kurulduktan sonra, aşağıdaki komutu çalıştırarak Git'i kurabilirsiniz:

```bash
brew install git
```

==Ubuntu kullanıcıları== için Git'i apt paket yöneticisini kullanarak yükleyebilirsiniz. Terminali açın ve aşağıdaki komutu çalıştırın:

```bash
sudo apt-get update
sudo apt-get install git
```

==Windows kullanıcıları== için Git yükleyicisini [resmi web sitesinden](https://git-scm.com/download/win) indirebilirsiniz. Yükleyici indirildikten sonra, yükleme işlemini başlatmak için çift tıklayın. Kurulumu tamamlamak için yönergeleri izleyin.

Git'i kurduktan sonra, terminalinizde veya cmd'de `git --version` komutunu tekrar çalıştırarak doğru şekilde yüklenip yüklenmediğini kontrol edebilirsiniz. Versiyon numarasını görüyorsanız, Git'i kullanmaya başlamaya hazırsınız demektir!
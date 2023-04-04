---
title: Temel git teminolojisi
---

Bu bölümde size bazı temel git terminolojisini sunacak olsam da, herhangi bir pratik deneyiminiz olmadan bu terimleri tam olarak anlamak zor olabilir. Bu nedenle, her şeyi ayrıntılı olarak anlamaya çalışmadan genel bir fikir edinmek için bu bölümü okumanızı öneriyorum.

> **Repository:** Repository (repo), git tarafından takip edilen dosya ve dizinlerden oluşan bir koleksiyondur.

> **Commit:** Commit, reponun belirli bir zamandaki anlık görüntüsüdür. Her commit, repodaki dosyalarda yapılan bir dizi değişikliği temsil eder.

> **Branch:** Branch(dal), depodaki ayrı bir geliştirme hattıdır(line). Her branch'ın kendi değişiklikleri ve commit'leri olabilir, bu da birden fazla geliştiricinin farklı özellikler(feature) veya düzeltmeler(fix) üzerinde bağımsız olarak çalışmasına olanak tanır.

> **Merge:** Merge(birleştirme), iki veya daha fazla geliştirme branch'ini tek bir branch'te birleştirme işlemidir. Bu genellikle bir özellik veya düzeltme tamamlandığında ve ana branch'e entegre edilmeye hazır olduğunda yapılır.

> **Pull:** Pull(çekme), değişiklikleri uzaktaki(remote) bir repo'dan alma ve yerel repo'nuza çekme işlemidir.

> **Push:** Push(itme), yerel(local) değişikliklerinizi başkalarıyla paylaşmak için uzak(remote) bir repo'ya gönderme işlemidir.

> **Clone:** Clone(klonlama), üzerinde yerel(local) olarak çalışabilmeniz için uzak(remote) bir repo'nun makinenizde yerel bir kopyasını oluşturma işlemidir.

> **Remote:** Remote, [GitHub](http://github.com/) veya [GitLab](https://gitlab.com/) üzerinde barındırılan bir repo gibi uzak bir repo'ya referanstır.

> **Fork:** Fork, farklı bir hesap(account) veya kuruluşta(organization) uzak bir reponun kopyasını hendi uzak(remote) hesabınızda oluşturma işlemidir. Bu, kopyalanan repo'da orijinal repo'dan bağımsız olarak değişiklik yapmanıza ve istenirse orijinal repo'ya pull request (çekme istekleri) yapmanıza olanak tanır.
# i3wm Kullanım Kılavuzu

Bu repo, [i3 Pencere Yöneticisi](https://i3wm.org/) için Türkçe bir kullanım kılavuzu içerir. Kılavuz, Docsify kullanılarak oluşturulmuş ve GitHub Pages üzerinden yayınlanmıştır.

**Canlı Belge:** [https://yuceltoluyag.github.io/i3wm-kullanimi/](https://yuceltoluyag.github.io/i3wm-kullanimi/)

## Projeyi Yerel Olarak Çalıştırma

Bu dokümantasyon projesini kendi bilgisayarınızda çalıştırmak ve değişiklikleri canlı olarak görmek için aşağıdaki adımları izleyebilirsiniz.

### Gereksinimler

*   [Node.js](https://nodejs.org/) ve npm
*   `docsify-cli`

### Kurulum ve Çalıştırma

1.  **`docsify-cli`'yi yükleyin:**
    Eğer sisteminizde `docsify-cli` yüklü değilse, aşağıdaki komutla global olarak yükleyebilirsiniz:
    ```bash
    npm install -g docsify-cli
    ```

2.  **Projeyi klonlayın:**
    ```bash
    git clone https://github.com/yuceltoluyag/i3wm-kullanimi.git
    cd i3wm-kullanimi
    ```

3.  **Docsify sunucusunu başlatın:**
    Proje ana dizinindeyken aşağıdaki komutu çalıştırın:
    ```bash
    docsify serve docs
    ```
    Bu komut, `http://localhost:3000` adresinde bir geliştirme sunucusu başlatacaktır. Tarayıcınızda bu adresi açarak dokümantasyonu görüntüleyebilirsiniz. Yaptığınız değişiklikler otomatik olarak sayfaya yansıyacaktır.

## İçeriği Güncelleme

Dokümantasyonun içeriği `docs` klasörü altındaki Markdown (`.md`) dosyalarından oluşur.

*   **Ana Sayfa İçeriği:** Ana sayfanın içeriğini değiştirmek için `docs/README.md` dosyasını düzenleyebilirsiniz.
*   **Kenar Çubuğu (Sidebar):** Kenar çubuğundaki menüyü ve içindekiler tablosunu düzenlemek için `docs/_sidebar.md` dosyasını güncelleyebilirsiniz.

Yapılan değişiklikleri `git` ile commit'leyip `push`ladıktan sonra, GitHub Pages üzerinde canlıya alınacaktır.

## Katkıda Bulunma

Katkıda bulunmak isterseniz, lütfen bir "pull request" açın veya bir "issue" oluşturun.
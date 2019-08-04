# i3 Kullanım Kılavuzu

Aşağıda yer alan bilgiler i3wm resmi sitesinden çevrilmiştir. `Yücel Toluyağ`

# i3WM nedir,Neden i3 ?

i3 Window Manager, adındanda anlaşılacağı üzere bir pencere yöneticisidir.  Pencere yöneticileri bir masaüstü değildir(DE). 


# Varsayılan Klavye Ayarları

![varsayilan klavye ayarları](https://i3wm.org/docs/keyboard-layer1.png)

i3wm kurulduktan sonra ekrana hangi tuş ile çalışmak istediğinizi sorar. Varsayılan olarak  **Windows** tuşu seçilidir. Diğer seçenek ise **ALT** tuşudur  Yukarıda ki seçimde alt tuşu seçimi gösterilmiştir.  Yani **Mod1** eğer windows tuşu seçilseydi **Mod4** olarak gösterilecekti. `Bu tanımlamalar ilerleyen bölümlerde config dosyasını okuyup anlamamızda yarar sağlayacaktır. Normalde winkey kullanıyorum ancak site dökümantasyonunda alt(mod1) kullanıldığı için örneklemeleri bu şekilde vereceğim.` 

 - **focus parent** Mod1 + a  açılmış pencerelerin alt pencerelerine odaklanmanızı geçiş yapmanızı sağlar.
 - **stacked layout** Mod1 + s  tüm pencereleri ortak bir alanda toplar.  
 - **dmenu** Mod1 +d  i3wm varsayılan program arama açma arama programıdır. Varsayılan olarak yüklü gelmez yüklemeniz gerekmektedir.
 - **fullscreen** Mod1 +f  açık pencerelerini tam ekran yapar, aynı tuşa tekrar basarsanız mevcut konumuna döner.
 - **left down up right** Mod1 +u,j,k,l   açık pencereler arasında geçiş yapmanızı sağlar. Sol,aşağı,yukarı ve sağ. 
 - **horizantal** Mod1 +h pencereleri yatay olarak bölümlendirir
 - **vertical** Mod1 +v pencereleri dikey olarak  bölümlendirir.
 - **tabbed layout** Mod1 +w  pencereleri tam ekran olarak tab menü moduna alır.
 - **Default layout** Mod1 +e  pencereleri  yığın modu(mod1+s mod1+v mod1+v) gibi kombinasyonları kullandıktan sonra pencere düzenini varsayılan ayara çevirir.
 - **Resize** Mod1 +r   pencereleri boyutlandırmaya  yarar. İsterseniz u j k l tuşlarını kullanın isterseniz ok tuşlarını
 - **focus floating / tiling** Mod1 +boşluk tuşu   pencereyi mevcut konumdan hareket ettirebilir konuma alır. En öne alan pencereyi hareket tuşlarıyla hareket ettirebilirsiniz.
  - **open terminal** Mod1 +enter  varsayılan terminali açar
 -  **Mod1 + 1,2,3,4..** tuşları  çalışma alanları arasında geçiş yapar 
> Shift tuşu kullanılarak yapılacaklar

![shift tuşu ile yapılacaklar](https://i3wm.org/docs/keyboard-layer2.png)

- Shift tuşu **taşıma** ,**sonlandırma**,**çıkış**,**serbest bırakma** vb gibi işlev kazandırır.
- **Kill window** Mod1 + Shift + q  aktif pencereyi kapatır.
- **exit i3** Mod1 + Shift + e  oturumu sonlandırır
- **restart i3** Mod1 + Shift + r  config dosyanızda değişiklik yaptıysanız,yeni ayarlarla birlikte i3 yeniden başlatır.
- **config restart i3** Mod1 + Shift + c resimde gösterilmemiş  ancak c tuşuyla yaptığınız ayarlarıda yenileyebilirsiniz. Ancak  bazı programlar ve scriptlerde  mod1 + shift + r kullanmak daha doğru olur.
-**focus floating / tiling** Mod1 +Shift +boşluk tuşu   pencereyi mevcut konumdan hareket ettirebilir konuma alır. En öne alan pencereyi hareket tuşlarıyla hareket ettirebilirsiniz.
- **left down up right** Mod1 +Shift+u,j,k,l   açık pencereler sağa sola yukarı aşağı taşır. Yön tuşlarınıda kullanabilirsiniz.
- **Mod1 +Shift +1,2,3,4..**  aktif pencerenizi bastığınız çalışma alanına taşır. Örneğin  ALT + Shift +2 bastıysanız üzeirnde bulunduğunuz açık uygulamayı 2 numaralı çalışma alanına taşır.

 sırasıyla splith/splitv (dikey yatay bölümlendirme) stacking(stack modu tek kapsayıcı) tabbed(tab modu)

![split stack tab modu örneği ](https://i3wm.org/docs/modes.png)

Focus Parent Örneği 
Mod1 + a

![Focus Parent Örneği ](https://i3wm.org/docs/tree-shot3.png)

Aktif pencere koyu mavi, mod + a kombinasnuna basıldığı anda hangi çalışma alanına geçiceğini gri şekilde gösteriyor.


# i3 Yapılandırma
Gerçek eğlencenin başladığı yer burası ;-). Çoğu şey ideal çalışma ortamınıza çok bağlıdır, bu yüzden ideal çalışma ortamınızı kendiniz yaratmalısınız.

i3 yapılandırma dosyası herhangi bir programlama dilini kullanmaz.  Basit bir yapı üzerine kurgulanmıştır. Konfigürasyon yapısını anladığınız takdirde, github üzerinde paylaşılan konfig dosyalarınıda rahatça okuyabileceksiniz. Bu okuma sayesinde başka kişilerin konfig dosyalarında faydalanabileceksiniz : )

Örneğin, pencereleri dilediğiniz yere konumlandırabilecek, istediğiniz çalışma alanına istediğiniz uygulamayla birlikte açılmasını sağlayabilecek, uygulamaların otomatik olarak başlatabilecek, i3'ün renklerini değiştirebilicek ve daha bir çok şeyi ayar dosyanız üzerinden gerçekleştirebileceksiniz.

i3 ayar dosyası bazı dağıtımlarda **/etc/i3/config** içerisinde yer alabilir.  Bu dosyayı dilerseniz **~/.i3/config** veya **~/.config/i3/config** içerisine taşıyabilirsiniz.  Standart kullanım ~/.config/i3/config şeklindedir. Bu dosyayı VIM,Sublime,Nano veya herhangi bir editorle düzenleyebilirsiniz.

İ3wm  başlatılığında  config dosyası yoksa otomatik olarak **i3-config-wizard** komutu devreye girer. Bu komutla birlikte size Alt ( Mod1 ) veya Windows ( Mod4 ) MOD tuşlarından hangisini kullanmak isteyeceğinizi sorar, dilediğinizi seçebilirsiniz.
Ayrıca, oluşturulan config dosyası mevcut klavye düzeninizin temel sembollerini kullanır. Yanlışlıkla kapatırsanız veya tüm i3 ayarlarınızı sıfırlamak isterseniz yine bu komutu kullanabilirsiniz.  **i3-config-wizard**  

 - Sıfırlama yaparken önceki konfig dosyasınızın yedeğini almayı
   unutmayın.

İ3 4.0'dan sonra daha basit,anlaşılır anahtar kelime yapısı kullanmaya başlamıştır. Ayar dosyasının okunmaması gibi bir durumla karşılaşanı görmedim ancak, ayar dosyası okunamıyor gibi bir ibare ile karşılaşırsanız. Ayar dosyanızın en başına şu satırı ekleyin.

    # i3 config file (v4)
### Yorum Satırları

Kurulumunuzu yaptıktan sonra hangi tuşun, hangi komutun ne işe yaradığını unutuyorsanız, ayar dosyanız içerisinde **belgelendirme** yapabilirsiniz. Yorumlar #(diez) işareti ile başlar ve yalnızca satırın başında kullanılabilir:

**Örnekler** :

    # Bu bir yorumdur

### Yazı Tipleri (Font)

i3, pencere başlıklarını,sistem yazı tiplerini FreeType yazı tiplerini (Pango aracılığıyla) destekler.

xfontsel [(1)](https://www.x.org/archive/X11R7.5/doc/man/man1/xfontsel.1.html) kullanabilirsiniz . Özel karakterleri görmek için (Unicode), ISO-10646 kodlamasını destekleyen bir font kullanmanız gerekir.

İ3wm ayarladığınız fontu açamaz ise varsayılan yazı tipine geri döner. Buradan  anlaşılabileceği gibi ; 

 - Sisteme ayarlanan font sisteminizde yüklü olmayabilir.
 - Fontunuz sistem içerisinde kullanılmaya uygun değildir.[ Çok karşılaşılan bir durum değildir.]
 
**Sözdizimi** :

    font <font açıklaması> 
    font pango: <font adı> [<stil seçenekleri>] <boyut>

**Örnek Kullanım**:

    font -misc-fixed-medium-r-normal--13-120-75-75-C-70-iso10646-1
    font pango:DejaVu Sans Mono 10
    font pango:DejaVu Sans Mono, Terminus Bold Semi-Condensed 11
    font pango:Terminus 11px

### Klavye Düzeni

Klavyeyle bastınığınız tuşun herhangi bir pencereyi yada uygulamayı çalıştırmasını sağlar. (Örnek için aşağıya bakınız).  İ3wm'ye atadığınız tuşu uniq'tir, yani bir uygulama yada pencere için aynı tuş kombinasyonunu kullanamazsınız. Kullandığınız takdirde hata verecektir. Sistemi yeniden başlatmadan, yada 

    bindsym $mod+Shift+r restart
    bindsym $mod+Shift+w reload
   komutlarını kullanmadan alınan hatayı göremeyiz. Zira her yaptıgımız değişiklikten sonra, yapılan değişikliği görmek için bu kombinasyonu kullanırız. Bu şekilde ayar dosyamızda hata var mı yok mu görebiliriz.

Klavye düzeninizi görebilmek için **xmodmap -pke** komutunu kullanabilirsiniz. Aynı şekilde klavye üzerinde bastığınız tuşun hangi anlama geldiğini görebilmek için  **xev** komutunu kullanabilirsiniz.
    
-   Anahtar kodlarının bir sembol atanmasına gerek yoktur (bazı dizüstü bilgisayarlarda özel satıcı kısayol tuşları için kullanışlıdır) ve farklı bir klavye düzenine ( xmodmap kullanırken ) geçerken anlamlarını değiştirmezler .
  
  Tecrübeyle sabit ;  Bazı konfig dosyalarını okurken bazı kombinasyonların hangi anlama geldiğini anlamayabilirsiniz.  Belki de o konfig arm,laptop veya farklı bir klavye düzeni kullanılan cihazda yapılmıştır. xev komutu burada çok işlevseldir. Örneğin  $mod+minus  şeklinde yazılımış bir ifadenin klavye üzerinde hangi kombinasyona denk geldiğini anlayamıyorsanız. 

    xev | grep -A2 --line-buffered '^KeyRelease' | sed -n "/keycode /s/^.*keycode \([0-9]*\).* (.*, \(.*\)).*$/\1 \2/p"

kodu terminalde çalıştırın klavyeniz üzerinde çeşitli denemeler yapın, sizde olmayan tuşları, yada bir uygulamayı başlatmak için kendinize daha rahat tuş kombinasyonu oluşturabilirsiniz. 

![örnek çıktı](https://i.ibb.co/zHRDt1m/pic-selected-190804-0605-13.png)

resimde görüldüğü üzere hem basılan tuşların karşılığını hemde uniqid'sini vermektedir.

**Kullanım Düzeni Syntax**:

    bindsym [--release] [<Group>+][<Modifiers>+]<keysym> command
    bindcode [--release] [<Group>+][<Modifiers>+]<keycode> command

**Örnek Kullanım**:

    # Tam Ekran
    bindsym $mod+f fullscreen toggle
    
    # i3wm Yeniden Başlatma
    bindsym $mod+Shift+r restart
    
    # Laptopta spesifik bir tuş ataması
    bindcode 214 exec --no-startup-id /home/friday13/toggle_beamer.sh
    
    # Kontrol V tuşunu  $mod +x kombinasyonuyla simule etmek
    bindsym --release $mod+x exec --no-startup-id xdotool key --clearmodifiers ctrl+v
    
    # Ekran Resmi Almak $mod+x (belirli bir alanı seçmek)
    bindsym --release $mod+x exec --no-startup-id import /tmp/latest-screenshot.png

bindsym ve bindcode kısmı dikkatinizi çekmiştir. İşte yukarıda verdiğim bilgiler neticesinde eğer ki bastığımız tuşun numarasını bilmiyorsak yukarıda ki işlemleri uygulayarak öğrenebilirsiniz. Aynı şekilde bindsym kullanırken de kelime karşılığını bilmiyorsak yine aynı yöntemle öğrenebiliyoruz. 

--relase yazılmasını sebebi bazı klavyeler ve bazı uygulamalar doğru kombinasyonu yazıp çalıştırdığınız halde çalışmazlar. **Xdotool** veya **import** uygulamarda dahil etmek zorundayız.

### Fare ile Kombinasyon

Ayar dosyamıza mouse ile  kombinlemek istiyorsak düzenimiz şu şekilde olmalıdır.

    bindsym [--release] [--border] [--whole-window] [--exclude-titlebar] [<Modifiers>+]button<n> command

**Örnek Kullanım**:

    # Farenin orta tuşuyla açık bir uygulamayı kapatabilirsiniz.
    bindsym --release button2 kill
    
    # Farenin orta tuşu ve mod tuşuyla birlikte açık uygulamayı sonlandırır
    bindsym --whole-window $mod+button2 kill
    
    # Farenin sağ tuşuyla mevcut düzen üzerinde geçiş yapabilirsiniz.
    bindsym button3 floating toggle
    bindsym $mod+button3 floating toggle
    
    # Fare tuşlarıyla sağa sola geçebilirsiniz.
    bindsym button9 move left
    bindsym button8 move right


Burada dikkat edilmesi gerek button numaraları , bazı fareler üzerinde tuşlar vardır, bu tuşları kullanabilmek için klavye düzenindeki verdiğim bilgileri fare içinde kullabilirsiniz.

Devamı çok yakında. Bekleyin Bebekleyin dı dıdı tıs
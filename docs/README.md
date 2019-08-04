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
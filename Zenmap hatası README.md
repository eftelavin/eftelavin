Adım 1: Öncelikle herhangi bir rpm sorununuz olmadığından emin olmak için bu komutu çalıştırın :

apt-get --fix-broken install


Adım 2: Yaptıktan sonra bunlara ihtiyacınız olacak: (cd Downloads içerisinde bulunduğumuzdan emin olalım)

wget http://archive.ubuntu.com/ubuntu/pool/universe/p/pygtk/python-gtk2_2.24.0-5.1ubuntu2_amd64.deb
 
wget http://azure.archive.ubuntu.com/ubuntu/pool/universe/p/pygobject-2/python-gobject-2_2.28.6-14ubuntu1_amd64.deb
 
wget http://security.ubuntu.com/ubuntu/pool/universe/p/pycairo/python-cairo_1.16.2-2ubuntu2_amd64.deb
 
dpkg -i python-gobject-2_2.28.6-14ubuntu1_amd64.deb 
 
dpkg -i python-cairo_1.16.2-2ubuntu2_amd64.deb
 
dpkg -i python-gtk2_2.24.0-5.1ubuntu2_amd64.deb
Adım 3: Tüm bunları yükledikten sonra, alien sürümümüzün 8.90 olduğundan emin olalım ve öncelikle yüklü olan alieni bir kaldıralım:

apt-get remove alien
Adım 4: Aşağıdaki siteye giderek alien'i indirelim.

http://archive.ubuntu.com/ubuntu/pool/main/a/alien/alien_8.90_all.deb

Muhtemel bu kod  indirme kodu galiba:

wget http://archive.ubuntu.com/ubuntu/pool/main/a/alien/alien_8.90_all.deb


Adım 5: Alien'i kuralım (cd Downloads içerisinde bulunduğumuzdan emin olalım)

dpkg -i alien_8.90_all.deb


Adım 6: Şimdi zenmap dosyamızı bulacağız ve şu komutları çalıştıracağız:

sudo alien zenmap-7.91-1.noarch.rpm
 
sudo dpkg -i **yıldızları silin ve çevrilen deb uzantılı zenmap dosyanızın adını yazın Örnek (zenmap_7.91-2_all.deb)**.deb
Adım 7: Bu komutlar mükemmel çalışırsa, şimdi çalıştırabilirsiniz:

sudo zenmap

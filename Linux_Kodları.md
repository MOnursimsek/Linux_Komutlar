# **LİNUX KOMUTLARI**


## **1. Yardım Alma Komutları**

| Komut               | Açıklama |
|---------------------|---------|
| `<komut> --help`   | Komutun parametreleri ve argümanları hakkında bilgi verir. Bazen açıklama da içerebilir.|
| `man <komut>`      | Kılavuz (manual) sayfalarını açar, komut hakkında detaylı bilgi içerir. |
| `info <komut>`     | Man sayfasında olmayan veya daha detaylı bilgi içeren yardım dosyalarını gösterir. |
| `apropos <kelime>` | Verilen kelimenin geçtiği man dosyalarını listeler. |
| `whatis <komut>`   | Komut hakkında tek satırlık özet bilgi ve hangi man dosyasında olduğunu gösterir. |


 Bu komutlar ile istediğiniz bir komutun nasıl çalıştığı hakkında bilgi alabilirsiniz.


### **help**
Komut un parametre ve argümanı hakkında kullanım bilgisi verir. Bazen t anıtım bilgisi (açıklama) de
içerebilir

![alt text](Resimler/help.jpeg)

---
### **man**

Kılavuz sayfalarıdır. Manual anlamındadır. Detaylı yardım alma dosyalarıdır.
Man dosyaları yapısal olarak aşağıdaki gibidir:
- NAME: Komut un ismi ve açıklaması.
- SYNOPSIS: Komut un nasıl kullanılacağı.
- DESCRIPTION: Komut un işlevi hakkında det aylı bilgi.
- EXAMPLES: Kullanımıyla ilgili örnekler.
- SEE ALSO: Ayrıca bakılabiliecek olan İlgili başlıklar. 
Referanslar…

/usr/share/man path’i (yolu) altında bulunurlar.

- man1: Genel kullanıcı programları hakkındadır.
- man2: Sistem programları ve çağrıları hk.
- man3: Kütüphane fonksiyonları hk.
- man4: Sürücü ve aygıtlar (/dev) hk.
- man5: Dosya biçimleri hk.
- man6: Oyunlar ve ekran koruyucuları hk.
- man7: Diğer kategorideki çeşitli komutlar hk.
- man8: Sistem yönetimi ve bakım komutları hk.

`man ping` komutunu kullandığınızda aşağıdaki gibi bir kılavuz sayfası gelir sayfanın devamına ok tuşları ile bakabilirsiniz.

![alt text](Resimler/man.jpeg)

---

### **info**
Man sayfasında bulunmayan komut lar için yardımcı olabilecek 3.
parti bir uygulamadır. Eğer kurulu değilse root kullanıcısıyla 

`apt install info` komutuyla kurulabilir.

`info ping` komutunu kullandığınızda aşağıdaki gibi bir kılavuz sayfası gelir sayfanın devamına ok tuşları ile bakabilirsiniz.

![alt text](Resimler/info.jpeg)

---

### **apropos**

Verilen ifadeyi içeren geçtiği man dosyalarını listeler. Hangi man dosyasınında olduğunu parantez içinde yazar.

![alt text](Resimler/apropos.jpeg)

---
### **whatis**

Komut hakkında t ek sat ırlık özet bilgi ve hangi man dosyasında bulunduğunu gösterir.

`whatis -w <komutun bir kısmı>*` şeklindeki kullanımı ile komutun bir kısmını yazıp buna uygun olan komutları listelemesini sağlayabilirsiniz.


![alt text](Resimler/whatis.jpeg)

---

## **2. Bilgi Alma Komutları**

| Komut | Açıklama |
|--------|------------|
| `lsb_release -a` | Kullanılan Linux dağıtımı hakkında ayrıntılı bilgi verir. (`neofetch` uygulaması da kullanılabilir.) |
| `cat /etc/issue` | Kullanılan Linux dağıtımının adını gösterir. |
| `uname -a` | Kullanılan Linux çekirdeği (kernel) ve versiyonu hakkında bilgi verir. `-n`, `-m`, `-r` parametreleriyle daha az ayrıntılı bilgi alınabilir. |
| `hostname` | Bilgisayar adını (hostname) verir. |
| `w` | Aktif kullanıcıları, oturum açma saatlerini ve son açtıkları uygulamaları gösterir. |
| `who` | Aktif kullanıcıları ve giriş saatlerini gösterir. |
| `whoami` | Geçerli kullanıcı adını gösterir. `-b` ve `-r` parametreleriyle de kullanılabilir. |
| `uptime` | Sistemin ne kadar süredir açık olduğunu gösterir. |
| `date` | Günün tarih, saat ve dilimini gösterir.| 
|`ncal` |uygulaması ile takvim de görüntülenebilir. |
| `ifconfig` / `ip a` | Ethernet isimlerini ve IP yapılandırmalarını gösterir. |
| `netstat -tunap` | Aktif TCP-UDP bağlantıları, portlar ve bağlantıdaki programlar hakkında bilgi verir. |
| `cat /proc/cpuinfo` | CPU hakkında detaylı bilgi verir. (`lscpu` komutu daha özet, `cpu-x` uygulaması daha görseldir.) |
| `cat /proc/meminfo` / `free -mh` | RAM ve durumu hakkında detaylı bilgi verir. |
| `vmstat -t` / `-td` / `-tD` | Sistem performansı hakkında anlık genel bilgi verir. (`htop` uygulaması daha gelişmiş bilgi sunar.) |
| `lshw -short` / `hwinfo --short` | Sistem donanımları hakkında detaylı bilgi verir. (`inxi -Fx` de kullanılabilir.) |
| `lsusb` | Takılı USB aygıtları hakkında bilgi verir. |
| `df -h -T` / `lsblk` / `fdisk -l` | Fiziksel ve mantıksal disk kullanımı ile dosya sistemi hakkında bilgi verir. |
| `du -hc <argüman>` | Belirtilen dizin altındaki boyut kullanım değerlerini gösterir. (`ncdu` uygulaması da kullanılabilir.) |


Bu komutlar ile kullandığınız makina ve işletim sistemi hakkında bilgiler alabilirsiniz.

### **lsb_release -a**
Kullanılan Linux dağıtımı (distro’su) hakkında ayrıntılı bilgiverir. 


![alt text](Resimler/lsb.png)

---
### **cat /etc/issue**
Kullanılan Linux dağıtımının adını gösterir. cat komutu aslında bir yazdırma komutudur yani bir dosyanın içeriğini terminale yazdırırı

![alt text](Resimler/cat-etc.png)

---
### **uname**
Kullanılan Linux dağıtımnın çekirdek (kernel) adını ve versiyonu hakkında bilgi verir.
-n, -m, -r paramet releriyle daha ayrınt ısız bilgi alınabilir.

![alt text](Resimler/uname.png)

### **hostname**
Bilgisayar adını (hostname) verir.

![alt text](Resimler/hostname.png)

---
### **w , who , whoami**
`w`	Aktif kullanıcıları, oturum açma saatlerini ve son açtıkları uygulamaları gösterir.

`who`	Aktif kullanıcıları ve giriş saatlerini gösterir.

`whoami`	Geçerli kullanıcı adını gösterir. -b ve -r parametreleriyle de kullanılabilir.

![alt text](Resimler/w.png)

---

### **uptime**
Sistemin ne kadar süredir açık olduğunu gösterir.

![alt text](Resimler/uptime.png)

---

### **date**
 Günün tarih, saat ve dilimini gösterir.

 ![alt text](Resimler/date.png)

---

### **ncal**

ncal uygulaması ile takvim de görüntülenebilir. Uygulama kurmak için yetkili bir kullanıcı ile `apt install ncal ` komutunu çalıştımanız yeterlidir.

 ![alt text](Resimler/ncal.png)

---
### **ifconfig / ip a**
Ethernet isimlerini ve IP yapılandırmalarını gösterir.

![alt text](Resimler/ipa.png)

ifconfig kullanmak için yetkili bir kullanıcı olmak gerekir

![alt text](Resimler/ifconfig.png)

---

### **netstat -tunap**
Aktif TCP-UDP bağlantıları, portlar ve bağlantıdaki programlar hakkında bilgi verir. tunap 5 farklı seçeneğin bir araya gelmiş halidir seçenekleri -t -u -n -a -p şeklinde tek tek kullanabilirsiniz ayrıntılı bilgi için netstat komutunun help ve man sayfalarını inceleyin 

![alt text](Resimler/netstat.png)

---

### **cat /proc/cpuinfo**
İşlem birimlerinizin her biri hakkında detaylı bilgi verir.`lscpu` komutu daha özet, `cpu-x` uygulaması daha görseldir.

![alt text](Resimler/catcpu.png)

![alt text](Resimler/lscpu.png)

cpu-x kullanmadan önce kurmanız gerekir.`apt install cpu-x`

![alt text](Resimler/cpu-x.png)
---

### **cat /proc/meminfo / free -mh**
RAM ve durumu hakkında detaylı bilgi verir.

![alt text](Resimler/catmem.png)

![alt text](Resimler/free.png)
---

### **vmstat -t / -td / -tD**
Sistem performansı hakkında anlık genel bilgi verir. `htop` uygulaması daha gelişmiş bilgi sunar.

![alt text](Resimler/vmstat.png)

![alt text](Resimler/htop.png)

---

### **lshw -short / hwinfo --short**
Sistem donanımları hakkında detaylı bilgi verir. (`inxi -Fx` de kullanılabilir.)

![alt text](Resimler/lshw.png)

![alt text](Resimler/inxi.png)

hwinfo için kurulum gerekir.

---

### **lsusb**
Takılı USB aygıtları hakkında bilgi verir.

![alt text](Resimler/lsusb.png)

---

### **df -h -T / lsblk / fdisk -l**
Fiziksel ve mantıksal disk kullanımı ile dosya sistemi hakkında bilgi verir.

![alt text](Resimler/lsblk.png)

fdisk kurulum ve yetkili kullanıcı gerektirir.

![alt text](Resimler/fdisk.png)

---

### **du -hc <argüman>**
Belirtilen dizin altındaki boyut kullanım değerlerini gösterir.`ncdu` uygulaması da kullanılabilir.

![alt text](Resimler/du-hc.png)

ncdu uygulamasını kurduktan sonra `ncdu ` kodunu çalıştırdığınızda bulunduğunuz dizinin altındaki bütün dizinlerin ve dosyaların boyutunun gösterildiği bir sayfa açılır.

![alt text](Resimler/ncdu.png)

---

## **3. İçerik KOmutları**

| Komut               | İşlev |
|---------------------|------------------------------------------------|
| `pwd`              | Hangi dizinde olduğunuzu gösterir. |
| `cd <dizin>`       | Belirtilen dizine girer. |
| `ls <dizin>`     | Belirtilen dizinin içeriğini listeler. |
| `file <dosya>`   | Belirtilen dosya hakkında bilgi verir. |
| `whereis <argüman>` | Komut, dosya veya klasörün yolunu ve man dosyasındaki yerini gösterir. |
| `which <komut>`  | Komutun tam yolunu gösterir. |
| `type <komut>`   | Komutun türünü ve yerini gösterir. |


Bu komutlar ile dizinler arasında gezinmek, dosyaların içeriği hakkında bilgi almak ve sistemde yüklü komutların yerini belirlemek gibi işlemler yapabilirsiniz.


### **pwd**  
Hangi dizinde olduğunuzu gösterir.  

![alt text](Resimler/pwd.png)  

---  

### **cd <dizin>**  
Belirtilen dizine girer.  

- `cd`: Kullanıcının home dizinine gider. (`cd ~` gibi)  
- `cd ..`: Bir üst dizine gider.  
- `cd ../../`: İki üst dizine gider. ("/" adedi kadar üst dizine çıkar)  
- `cd ../<dizin>`: Önce üst dizine, ardından belirtilen dizine gider.  
- `cd -`: En son bulunduğunuz iki dizin arasında geçiş yapar.  


![alt text](Resimler/cd.png)  

---  

### **ls <dizin>**  
Belirtilen dizinin içeriğini listeler.  

- `ls <dizin>`: Belirtilen dizinin içeriğini listeler.  
- `ls -l`: Ayrıntılı listeleme yapar.  
- `ls -la`: Ayrıntılı ve gizli dosyaları da içeren listeleme yapar.  
- `ls -S`: Boyut büyüklüğüne göre sıralar.  
- `ls -lh`: Boyutları daha anlaşılır bir formatta listeler.  
- `ls -lt`: Değişiklik tarihine göre sıralar.  


![alt text](Resimler/ls.png)  

![alt text](Resimler/ls2.png)  

---  

### **file <dosya>**  
Belirtilen dosya hakkında bilgi verir.  

![alt text](Resimler/file.png)  

---  

### **whereis <argüman>**  
Komut, dosya veya klasörün yolunu ve man dosyasındaki yerini gösterir.  

![alt text](Resimler/whereis.png)  

---  

### **which <komut>**  
Komutun tam yolunu gösterir.  

![alt text](Resimler/which.png)  

---  

### **type <komut>**  
Komutun türünü ve yerini gösterir.  

![alt text](Resimler/type.png)  

---

## **4. Dosya ve Dizin Komutları**

| Komut               | İşlev                                                                 |
|---------------------|-----------------------------------------------------------------------|
| `mkdir <dizinadı>`   | Dizin oluşturma komutudur. `mkdir dizin1 dizin2 dizin3` şeklinde topluca oluşturulabilir. |
| `touch <dosyaadı>`   | Dosya oluşturma komutudur. `touch dosya1 dosya2 dosya3` şeklinde topluca oluşturulabilir. |
| `cp <kaynak> <hedef>` | Dosya kopyalama komutudur. `-i` parametresi ile onay istenir. `-r` parametresi ile dizinler kopyalanabilir. |
| `mv <kaynak> <hedef>` | Dosya taşıma komutudur. İsim değişikliği için de kullanılabilir. `mv <dosyadı> <dosyaadı.uzantısı>` |
| `rm <dosya/dizin>`   | Dosya silme komutudur. `-r` parametresiyle dizinler de silinebilir. `-ri` ile onay istenir, `-rf` ile sorgusuz silme yapılır. |
| `cat <dosyaadı>`     | Dosya okuma komutudur. `-n` parametresi ile satırlar numaralı gösterilir. |
| `nl <dosyaadı>`      | `cat` komutuyla aynı işlevi görür, dosya satırlarını numaralandırarak gösterir. |
| `echo “ifade”`                     | CLI’a veya dosyalara ifade yazmak için kullanılır.|
| `more` ve `less <dosya>`           | Uzun çıktıları daha rahat (bölümlü) okunmalarını sağlarlar. `less`, `more`'dan daha gelişmiştir, büyük dosyalarda daha hızlıdır ve geriye dönük okuma yapabilir. |
| `head` ve `tail <dosya>`           | Çıktıların ilk 10 veya son 10 satırını görüntüler. `-n` parametresiyle 10 değeri değiştirilebilir. |
| `sort <dosya>`                     | Bir dosya içerisindeki satır başı ifadeleri alfabetik sıralamayla listeler. |
| `grep <ifade> <dosya/dizin>`      | Bir ifadeyi dosya veya dizinde aramak için kullanılır. `-i` parametresiyle küçük/büyük harf duyarlılığı gözetmez, `-r` ile dizinlerde arama yapar, `-s` ile hata mesajlarını göstermez, `-v` ile tersine arama yapar. |
| `find <dizin> -name <ifade>`      | Belirli bir dizin içinde geçen ifadeleri (dosyaları) aramak için kullanılır. |
| `locate <dosya>`                   | İndekslenmiş (veritabanında bulunan) dosyalar için arama yapar. Find'ten hızlıdır, ancak veritabanı kullanır. `updatedb` komutuyla indeksi güncellenebilir. |


### **mkdir <dizinadı>**  
Dizin oluşturma komutudur. 

![alt text](Resimler/mkdir.png)

---

### **touch <dosyaadı>**  
Dosya oluşturma komutudur. 

![alt text](Resimler/touch.png)

---

### **cp <kaynak> <hedef>**  
Dosya kopyalama komutudur. `-i` parametresi ile onay istenir. `-r` parametresi ile dizinler kopyalanabilir.  

![alt text](Resimler/cp.png)


---

### **mv <kaynak> <hedef>**  
Dosya taşıma komutudur. İsim değişikliği için de kullanılabilir. `mv <dosyadı> <yeni dosyaadı>`  

![alt text](Resimler/mv.png)

---

### **rm <dosya/dizin>**  
Dosya silme komutudur. `-r` parametresiyle dizinler de silinebilir. `-ri` ile onay istenir, `-rf` ile sorgusuz silme yapılır.  

![alt text](Resimler/rm.png)

---

### **cat <dosyaadı>**  
Dosya okuma komutudur. `-n` parametresi ile satırlar numaralı gösterilir.  

![alt text](Resimler/cat.png)

---

### **nl <dosyaadı>**  
`cat` komutuyla aynı işlevi görür, dosya satırlarını numaralandırarak gösterir.  

![alt text](Resimler/nl.png)

---

### **echo “ifade”**  
CLI’a veya dosyalara ifade yazmak için kullanılır.  

![alt text](Resimler/echo.png)

---

### **more** ve **less <dosya>**  
Uzun çıktıları daha rahat (bölümlü) okunmalarını sağlarlar. `less`, `more`'dan daha gelişmiştir, büyük dosyalarda daha hızlıdır ve geriye dönük okuma yapabilir.  

`more /proc/cpuinfo ` ve `less /proc/cpuinfo` komutları ile uzun bir dosyanın more ve less ile nasıl görüntülendiğini görebilirsiniz.

---

### **head** ve **tail <dosya>**  
Çıktıların ilk 10 veya son 10 satırını görüntüler. `-n` parametresiyle 10 değeri değiştirilebilir. 

![alt text](Resimler/headtail.png)

---

### **sort <dosya>**  
Bir dosya içerisindeki satır başı ifadeleri alfabetik sıralamayla listeler.  

Aşağıda aynı dosyanın sor ve cat ile ayzdırılmış halleri gösterilmiştir.

![alt text](Resimler/sort.png)

![alt text](Resimler/sort2.png)

---

### **grep <ifade> <dosya/dizin>**  
Bir ifadeyi dosya veya dizinde aramak için kullanılır. `-i` parametresiyle küçük/büyük harf duyarlılığı gözetmez, `-r` ile dizinlerde arama yapar, `-s` ile hata mesajlarını göstermez, `-v` ile tersine arama yapar.  

![alt text](Resimler/grep.png)

---

### **find <dizin> -name <ifade>**  
Belirli bir dizin içinde geçen ifadeleri (dosyaları) aramak için kullanılır. 

![alt text](Resimler/find.png)

---

### **locate <dosya>**  
İndekslenmiş (veritabanında bulunan) dosyalar için arama yapar. Find'ten hızlıdır, ancak veritabanı kullanır. `updatedb` komutuyla indeksi güncellenebilir.  

![alt text](Resimler/locate.png)

---

## **5. Komut Operatörleri**

| Operatör                    | İşlev                                                                 |
|-----------------------------|-----------------------------------------------------------------------|
| `<komut> > <dosyaadı>`       | Komutun çıktısını belirtilen dosyaya yazdırır. (Dosyadaki ifadeleri ezer.) |
| `<komut> >> <dosyaadı>`      | Komutun çıktısını belirtilen dosyaya yazdırır. (Dosyadaki ifadeleri ezmez.) |
| `<komut1> \| <komut2>`        | Önceki komutun çıktısını, sonraki komuta girdi olarak gönderir.      |
| `<komut1> ; <komut2>`        | Önceki komut bittiğinde sonraki komutu çalıştırır.                   |
| `<komut1> & <komut2>`        | Komutlar başarı durumuna bakmaksızın arka planda aynı anda çalıştırılır. |
| `<komut> &`                  | Komut arka planda çalıştırılır.                                      |
| `<komut1> && <komut2>`       | Önceki komutun başarılı olması halinde sonraki komut çalıştırılır.    |
| `<komut1> \|\| <komut2>`       | Önceki komutun başarısız olması halinde sonraki komut çalıştırılır.    |

### **>**  
Komutun çıktısını belirtilen dosyaya yazdırır. (Dosyadaki ifadeleri ezer.)  

![alt text](Resimler/op1.png)

---

### **>>**  
Komutun çıktısını belirtilen dosyaya yazdırır. (Dosyadaki ifadeleri ezmez.)  

![alt text](Resimler/op2.png)

---

### **|**  
Önceki komutun çıktısını, sonraki komuta girdi olarak gönderir. 

![alt text](Resimler/op3.png)

---

### **;**  
Önceki komut bittiğinde sonraki komutu çalıştırır.  

![alt text](Resimler/op4.png)

---

### **&**  
Komutlar başarı durumuna bakmaksızın arka planda aynı anda çalıştırılır.  

![alt text](Resimler/op5.png)

Bu komuutan sonra 10 saniye bitince reboot atılır.

---

### **&&**  
Önceki komutun başarılı olması halinde sonraki komut çalıştırılır.  

![alt text](Resimler/op6.png)

---

### **||**  
Önceki komutun başarısız olması halinde sonraki komut çalıştırılır.  

![alt text](Resimler/op7.png)


## **6. Bölüm Arşiv Komutları ve Yönetimi**

| Komut                                      | İşlev                                                                                       |
|--------------------------------------------|---------------------------------------------------------------------------------------------|
| `tar cf arsiv.tar <dosyalar>`              | Dosyaları arşivleme komutudur. Sıkıştırma uygulamaz. `c=create`, `f=file`'ı temsil eder.   |
| `tar xfv arsiv.tar`                        | Arşivden çıkarma komutudur. `x=extract`, `f=file`, `v=verbose`'u temsil eder.              |
| `tar cfz arsiv.tgz/tar.gz <dosyalar>`      | Dosyaları Gzip kullanarak sıkıştırma ve arşivleme komutudur. `z=zip`'i temsil eder.         |
| `tar xfzv arsiv.tgz/tar.gz`                | Gzip dosyalarını çıkarma komutudur. (`-C` parametresiyle farklı bir path'e çıkarılabilir.)   |
| `tar cfj arsiv.tar.bz2 <dosyalar>`         | Dosyaları Bzip2 kullanarak sıkıştırma ve arşivleme komutudur.                               |
| `tar xfjv arsiv.tar.bz2`                   | Bzip2 dosyalarını çıkarma komutudur. (`-C` parametresiyle farklı bir path'e çıkarılabilir.) |
| `zcat arsiv.tgz`                           | Gzip dosyalarının içeriğini okuma/listeme komutudur. (`.tar` dosyalarını okumaz.)           |
| `bzcat arsiv.bz2`                          | Bzip2 dosyalarının içeriğini okuma/listeme komutudur. (`.tar` dosyalarını okumaz.)          |
| `gzip dosya1 dosya2`                       | Dosyaları sıkıştırma komutudur. Dosyalar `.gz` uzantısına dönüşür.                          |
| `gunzip dosya1.gz dosya2.gz`               | Gz dosyalarını çıkarma komutudur.                                                           |
| `bzip2 dosya1 dosya2`                      | Dosyaları sıkıştırma komutudur. Dosyalar `.bz2` uzantısına dönüşür.                         |
| `bunzip2 dosya1.bz2 dosya1.bz2`            | Bz2 dosyalarını çıkarma komutudur.                                                         |
| `zip arsiv.zip <dosyalar>`                 | Dosyaları zip kullanarak sıkıştırma ve arşivleme komutudur.                                 |
| `unzip arsiv.zip`                          | Zip dosyalarını çıkarma komutudur.                                                         |
| `unrar arsiv.rar`                          | Rar dosyalarını çıkarma komutudur. (`unrar-free` ile gelir.)                               |


### **Arşivleme (tar cf arsiv.tar <dosyalar>)**  
Dosyaları arşivleme komutudur. Sıkıştırma uygulamaz. `c=create`, `f=file`'ı temsil eder.  

![alt text](Resimler/tar_c.png)

---

### **Arşivden Çıkarma (tar xfv arsiv.tar)**  
Arşivden çıkarma komutudur. `x=extract`, `f=file`, `v=verbose`'u temsil eder.

![alt text](Resimler/tar_x.png)

---

### **Sıkıştırarak Arşivleme (tar cfz arsiv.tgz/tar.gz <dosyalar>)**  
Dosyaları Gzip kullanarak sıkıştırma ve arşivleme komutudur. `z=zip`'i temsil 
eder.  

![alt text](Resimler/tar_cfz.png)

![alt text](Resimler/tar_cfz2.png)


---

### **Gzip Dosyalarını Çıkarma (tar xfzv arsiv.tgz/tar.gz)**  
Gzip dosyalarını çıkarma komutudur. (`-C` parametresiyle farklı bir path'e çıkarılabilir.)  

![alt text](Resimler/tar_xfzv.png)

---

### **Sıkıştırarak Arşivleme (tar cfj arsiv.tar.bz2 <dosyalar>)**  
Dosyaları Bzip2 kullanarak sıkıştırma ve arşivleme komutudur.  

![alt text](Resimler/tar_cfj.png)

---

### **Bzip2 Dosyalarını Çıkarma (tar xfjv arsiv.tar.bz2)**  
Bzip2 dosyalarını çıkarma komutudur. (`-C` parametresiyle farklı bir path'e çıkarılabilir.)  

![alt text](Resimler/tar_xfjv.png)

---

### **İçerik Okuma (zcat arsiv.tgz)**  
Gzip dosyalarının içeriğini okuma/listeme komutudur. (`.tar` dosyalarını okumaz.)  

![alt text](Resimler/zcat.png)

---

### **İçerik Okuma (bzcat arsiv.bz2)**  
Bzip2 dosyalarının içeriğini okuma/listeme komutudur. (`.tar` dosyalarını okumaz.)  

![alt text](Resimler/bzcat.png)

---

### **Sıkıştırma (gzip dosya1 dosya2)**  
Dosyaları sıkıştırma komutudur. Dosyalar `.gz` uzantısına dönüşür.  

![alt text](Resimler/gzip.png)

---

### **Gz Dosyalarını Çıkarma (gunzip dosya1.gz dosya2.gz)**  
Gz dosyalarını çıkarma komutudur.  

![alt text](Resimler/gunzip.png)

---

### **Sıkıştırma (bzip2 dosya1 dosya2)**  
Dosyaları sıkıştırma komutudur. Dosyalar `.bz2` uzantısına dönüşür. 

![alt text](Resimler/bzip2.png)

---

### **Bz2 Dosyalarını Çıkarma (bunzip2 dosya1.bz2 dosya1.bz2)**  
Bz2 dosyalarını çıkarma komutudur.  

![alt text](Resimler/bunzip2.png)

---

### **Zip Arşivleme (zip arsiv.zip <dosyalar>)**  
Dosyaları zip kullanarak sıkıştırma ve arşivleme komutudur.  

![alt text](Resimler/zip.png)

---

### **Zip Dosyalarını Çıkarma (unzip arsiv.zip)**  
Zip dosyalarını çıkarma komutudur.  

![alt text](Resimler/unzip.png)

---



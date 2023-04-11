# Ucuş Yönetim Sistemi

Not: Tabloyu düzgün görüntülemek için 'Raw' formatında açın.

## Soru;

Uçuşların ve pilotların yönetimi için bir sistem tasarlayın.

 *Hava yolu şirketleri uçuşları gerçekleştirir. Her hava yolunun bir kimliği vardır.
 *Hava yolu şirketi, farklı tipteki uçaklara sahiptir.
 *Uçaklar çalışır veya onarım durumunda olabilir.
 *Her uçuşun benzersiz kimliği, kalkacağı ve ineceği havaalanı, kalkış ve iniş saatleri vardır.
 *Her uçuşun bir pilotu ve yardımcı pilotu vardır ve uçağı kullanırlar.
 *Havaalanlarının benzersiz kimlikleri ve isimleri vardır.
 *Hava yolu şirketlerinin pilotları vardır ve her pilotun bir deneyim seviyesi mevcuttur.
 *Bir uçak tipi, belirli sayıda pilota ihtiyaç duyabilir.
Bu sistemi tasvir eden Class(Sınıf) diyagramını çiziniz.

##Çözüm;


Aşağıdaki sınıf diyagramı, uçuşlar ve pilotların yönetimi için bir sistem tasvir etmektedir. Bu sistemi oluşturmak için kullanılan temel sınıflar HavaYolu, Uçak, Uçuş, Pilot ve Havaalanı'dır.

    +----------------+       +----------------+        +--------------+
    |    HavaYolu    |       |      Uçak      |        |   Uçuş     |
    +----------------+       +----------------+        +--------------+
    |  -kimlik       |       | -model         |        |  -kimlik     |
    |  -ad           |       | -durum         |        |  -kalkışYeri|
    +----------------+       | -pilotSayısı   |        |  -varışYeri |
          ^                   +----------------+        |  -kalkışSaat|
          |                          ^                 |  -varışSaat |
    +----------------+               |                 |  -uçak      |
    |   Havaalanı    |               |                 |  -pilot     |
    +----------------+               |                 +--------------+
    |  -kimlik       |               |                         ^
    |  -ad           |        +-------------+                  |
    |                |        |   Pilot     |          +----------------+
    +----------------+        +-------------+          |    UçakTipi     |
                                 | -ad        |          +----------------+
                                 | -deneyim   |          |  -model         |
                                 +-------------+          |  -pilotSayısı   |
                                                            +----------------+


HavaYolu sınıfı, hava yolu şirketlerini temsil eder ve her şirketin benzersiz bir kimliği ve adı vardır. Bu sınıf aynı zamanda hava yolu şirketinin sahip olduğu uçakları ve pilotları da içerir.

Uçak sınıfı, uçakların özelliklerini temsil eder ve her uçağın bir modeli, durumu ve belirli bir sayıda pilota ihtiyacı vardır.

Uçuş sınıfı, her uçuşun benzersiz bir kimliği, kalkış ve varış havaalanları, kalkış ve varış saatleri ve uçak ve pilot bilgilerini içerir.

Pilot sınıfı, her pilotun bir adı ve deneyim seviyesi gibi özellikleri temsil eder.

Havaalanı sınıfı, her havaalanının benzersiz bir kimliği ve adı vardır.

UçakTipi sınıfı, belirli bir uçak tipi için gerekli pilot sayısı ve model gibi özellikleri temsil eder.

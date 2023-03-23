## Zero Knowledge Proofs (Sıfır Bilgi Kanıtı) Nedir? 

**Zero Knowledge (sıfır bilgi kanıtı)** kavramı, birisinin başka birine bir şeyi kanıtlaması gerektiğinde, kanıtlayan kişinin açıklamalarını, bilgi ve verilerini ifşa etmeden yapabileceği bir yöntemi ifade eder. Bu, güvenli ve gizli bilgi işlemlerinde, özellikle de kriptografi ve veri gizliliği konularında kullanılan bir tekniktir. Blockchain'de, zero knowledge protokolü, işlem gizliliği ve anonimliğini artırmak için kullanılır.

Sıfır bilgi kanıtı, bilgilerin sadece ispatlayan tarafından gizliliği korunduğu özel durumlardan oluşmaktadır. Finansal işlemler, kimlik doğrulama ve veri paylaşımı gibi alanlarda da kullanılır. Örneğin, bir kullanıcının banka hesap bilgilerini doğrulamak istediği bir senaryoda, zero knowledge protokolü, kullanıcının hesap bilgilerini açıklamadan, yalnızca hesabın doğruluğunu doğrulamak için gerekli olan bilgileri sağlamasına izin verebilir.

Zero Knowledge; bir şeyin gerçeğini, o gerçeği nasıl bildiğinizi ya da o gerçeğe dair bildiğiniz şeyleri paylaşmadan doğrulamanıza olanak sağlar. Sıfır bilgi kanıtları, girdi verilerini “doğru” ya da “yanlış” olarak çıktı olarak sunan bir algoritmaya dayanır. 
Sıfır bilgi kanıtı, her türlü verinin geçerliliğini kanıtlayabilir. Bu duruma kişisel veriler dahildir. 

![image](https://user-images.githubusercontent.com/123966022/226602614-1dcd134d-0f47-4fe5-9006-9572d947da13.png)

> Bunu daha somut bir şekilde düşünebiliriz; `C` olarak gösterilen bir programın iki girdisi olduğunu varsayalım: `C(x, w)`. Burada `x` halka açık olan girdi, `w` ise gizli şahit girdisidir. Programın çıktısı boolean yani ya `doğru` ya da `yanlış`. Amaç, belirli bir halka açık girdi `x` verildiğinde, ispatlayıcı bir gizli girdi `w` bildiğini ve `C(x,w) == true` olduğunu kanıtlamaktır.


***Zero Knowledge (Sıfır-bilgi kanıtları)*, özel verilerle ilgili bir dizi açıklamanın kanıtlanmasını sağladığından birçok uygulamada avantaj sağlar:**

- Özel Verilerle İlgili Kanıtlama
    - A kişisinin banka hesabında X'ten fazla para olduğunu kanıtlama
    - Bir bankanın son bir yılda Y varlığıyla işlem yapmadığını kanıtlama
    - Tüm DNA'yı ifşa etmeden eşleşen DNA'yı kanıtlama
    - Kredi skoru Z'den yüksek olan birinin varlığını kanıtlama

- Anonim Yetkilendirme
     - Kimliğini ifşa etmeden web sitesinin kısıtlı alanına erişme hakkına sahip olan R kişisinin bunu kanıtlaması (örneğin, giriş, şifre)
     - Hangi ülkelerin/eyaletlerin listeye dahil edildiğini ifşa etmeden birinin izin verilen ülkelerden/bölgelerden biri olduğunu kanıtlama
     - Metro/otobüs geçiş kartına ait kimlik numarasını ifşa etmeden aylık geçiş hakkına sahip olduğunu kanıtlama

- Anonim Ödemeler 
     - Kimlikle tamamen bağlantısız ödeme yapabilme
     - Gelirlerini ifşa etmeden vergi ödeme

- Hesaplama Dış Kaynak Kullanımı 
     - Pahalı bir hesaplamayı dış kaynak kullanarak gerçekleştirip sonucun doğru olduğunu yeniden yürütmeye gerek kalmadan doğrulama; güvensiz hesaplama kategorisi açılır
     - Herkesin aynı şeyi hesapladığı blok zinciri modelini, bir tarafın hesapladığı ve herkesin doğruladığı modele değiştirme


**Zero Knowledge için üç temel özellik mevcuttur:** 
- **Bütünlük**: Girdi doğru ise, zero knowledge her zaman “doğru” değerini gösterir.
- **Sağlamlık**: Girdi eğer yanlış ise, zero knowledge kandırmak mümkün değildir
- **Gizlilik**: Girdiler, ispatlayan taraf harici kimseyle paylaşılmaz 


Zero Knowledge (sıfır bilgi kanıtı), kanıtlayan taraf ve kanıtı doğrulayan taraf arasında etkileşim yaratır. Haricinde etkileşim olmayan sıfır bilgi kanıtları da bulunmaktadır, bunun en yaygın örneği Fiat-Shamir yöntemine dayanır ve bu yöntem etkileşimli bir şemadan oluşmaktadır. 

Sıfır bilgi kanıt protokolü, kanıtlayan ve kanıtı doğrulayan taraf arasındaki etkileşimi transkript şeklinde sunar. 

İspat geçerlilikleri hesaplama varsayımlarına yani kriptografik hash fonksiyonlarına dayanmaktadır. Hash fonksiyonu, verinin bütünlüğünü sağlamak için kullanılan yöntemlerden biridir. 

**Hash Fonsiyonu örneği:**

![image](https://user-images.githubusercontent.com/123966022/226828348-67d027e9-c676-428d-b5e1-068952622752.png)

## Zero Knowledge Soyut Örnek

X kişisinin *renk körü* olduğunu ve *iki adet kırmızı ve yeşil renklerde topunuz* olduğunu düşünün. X kişisine göre toplar tamamen aynı renk görünüyor ancak topların ayırt edilebileceğinden şüpheleniyor. Bu kişiye topların farklı renklerde olduğunu kanıtlamak istiyorsunuz ancak topların hangisinin kırmızı hangisinin yeşil renk olduğunu açıklamak istemiyorsunuz. 

İspat sistemi şu şekilde işliyor; X kişisi topları alıyor ve arkasına saklıyor. Sonrasında toplardan birini alıyor ve size gösteriyor. Daha sonrasında tekrardan arkasına saklıyor ve tekrardan bir topu gösteriyor. İki toptan birini seçme işlemi eşit olasılıkta gerçekleşiyor. Size sadece topu değiştirip değiştirmediğini sorar, tüm bu olay döngüsünü gerektiği sıklıkta tekrarlanabilir. 
Topların renklerine bakarak X kişisinin topları değiştirip değiştirmediğini kesinlikle söyleyebilirsiniz. Ancak toplar aynı renkteyse ve ayırt edilemiyorsa, %50 yüksek olasılıkla tahmin etmeniz pek mümkün değil. 

![image](https://user-images.githubusercontent.com/123966022/226891787-f4ed49d0-540e-4e16-bacf-091f7fee7fde.png)


- Her ihtimali belirlemede rastgele başarı olasılığınız %50 ve tüm ihtimali belirleme olasılığınız sıfıra yakın. **(Sağlamlık)**
- X kişisi ve siz, ispat işlemini birçok kez tekrarlarsanız, X kişisi topların gerçekten de farklı olduğuna ikna olacaktır. **(Bütünlük)**

Bu ispat sıfır bilgidir, çünkü X kişisi hangi topun yeşil hangi topun kırmızı olduğunu asla öğrenemez ve topların nasıl ayırt edilebileceğine dair de hiçbir bilgi edinmemektedir. 

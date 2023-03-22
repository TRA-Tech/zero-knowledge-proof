## ZERO KNOWLEDGE
**Zero Knowledge**, ilk olarak 1980 yılında MIT araştırmacıları Shafi Goldwasser, Silvio Micali ve Charles Rackoff tarafından ortaya çıkmıştır. Araştırmacılar, *İnteraktif Kanıtlama Sistemleri* üzerinde çalışmalar sürdürürken, birinci taraf **Prover** ve mesajı doğrulayan taraf **Verifier** arasındaki ilişkiyi tanımlayacak teorik çalışmalar yürütmüşlerdir. 

![image](https://user-images.githubusercontent.com/123966022/226599025-82affff6-cf38-4f89-8317-8a9405ac880c.png)


### Zero Knowledge Nedir? 

**Zero Knowledge (sıfır bilgi kanıtı)** kavramı, birisinin başka birine bir şeyi kanıtlaması gerektiğinde, kanıtlayan kişinin açıklamalarını, bilgi ve verilerini ifşa etmeden yapabileceği bir yöntemi ifade eder. Bu, güvenli ve gizli bilgi işlemlerinde, özellikle de kriptografi ve veri gizliliği konularında kullanılan bir tekniktir. Blockchain'de, zero knowledge protokolü, işlem gizliliği ve anonimliğini artırmak için kullanılır.

Sıfır bilgi kanıtı, bilgilerin sadece ispatlayan tarafından gizliliği korunduğu özel durumlardan oluşmaktadır.Finansal işlemler, kimlik doğrulama ve veri paylaşımı gibi alanlarda da kullanılır. Örneğin, bir kullanıcının banka hesap bilgilerini doğrulamak istediği bir senaryoda, zero knowledge protokolü, kullanıcının hesap bilgilerini açıklamadan, yalnızca hesabın doğruluğunu doğrulamak için gerekli olan bilgileri sağlamasına izin verebilir.

Zero Knowledge; bir şeyin gerçeğini, o gerçeği nasıl bildiğinizi ya da o gerçeğe dair bildiğiniz şeyleri paylaşmadan doğrulamanıza olanak sağlar. Sıfır bilgi kanıtları, girdi verilerini “doğru” ya da “yanlış” olarak çıktı olarak sunan bir algoritmaya dayanır. 
Sıfır bilgi kanıtı, her türlü verinin geçerliliğini kanıtlayabilir. Bu duruma kişisel veriler dahildir. 

![image](https://user-images.githubusercontent.com/123966022/226602614-1dcd134d-0f47-4fe5-9006-9572d947da13.png)


**Zero Knowledge için üç temel özellik mevcuttur:** 
- **Bütünlük**: Girdi doğru ise, zero knowledge her zaman “doğru” değerini gösterir.
- **Sağlamlık**: Girdi eğer yanlış ise, zero knowledge kandırmak mümkün değildir
- **Gizlilik**: Girdiler, ispatlayan taraf harici kimseyle paylaşılmaz 


Zero Knowledge (sıfır bilgi kanıtı), kanıtlayan taraf ve kanıtı doğrulayan taraf arasında etkileşim yaratır. Haricinde etkileşim olmayan sıfır bilgi kanıtları da bulunmaktadır, bunun en yaygın örneği Fiat-Shamir yöntemine dayanır ve bu yöntem etkileşimli bir şemadan oluşmaktadır. 

Sıfır bilgi kanıt protokolü, kanıtlayan ve kanıtı doğrulayan taraf arasındaki etkileşimi transkript şeklinde sunar. 

İspat geçerlilikleri hesaplama varsayımlarına yani kriptografik hash fonksiyonlarına dayanmaktadır. Hash fonksiyonu, verinin bütünlüğünü sağlamak için kullanılan yöntemlerden biridir. 

**Hash Fonsiyonu örneği:**

![image](https://user-images.githubusercontent.com/123966022/226828348-67d027e9-c676-428d-b5e1-068952622752.png)

### Zero Knowledge Soyut Örnek

X kişisinin *renk körü* olduğunu ve *iki adet kırmızı ve yeşil renklerde topunuz* olduğunu düşünün. X kişisine göre toplar tamamen aynı renk görünüyor ancak topların ayırt edilebileceğinden şüpheleniyor. Bu kişiye topların farklı renklerde olduğunu kanıtlamak istiyorsunuz ancak topların hangisinin kırmızı hangisinin yeşil renk olduğunu açıklamak istemiyorsunuz. 

İspat sistemi şu şekilde işliyor; X kişisi topları alıyor ve arkasına saklıyor. Sonrasında toplardan birini alıyor ve size gösteriyor. Daha sonrasında tekrardan arkasına saklıyor ve tekrardan bir topu gösteriyor. İki toptan birini seçme işlemi eşit olasılıkta gerçekleşiyor. Size sadece topu değiştirip değiştirmediğini sorar, tüm bu olay döngüsünü gerektiği sıklıkta tekrarlanabilir. 
Topların renklerine bakarak X kişisinin topları değiştirip değiştirmediğini kesinlikle söyleyebilirsiniz. Ancak toplar aynı renkteyse ve ayırt edilemiyorsa, %50 yüksek olasılıkla tahmin etmeniz pek mümkün değil. 

- Her ihtimali belirlemede rastgele başarı olasılığınız %50 ve tüm ihtimali belirleme olasılığınız sıfıra yakın. **(Sağlamlık)**
-	X kişisi ve siz, ispat işlemini birçok kez tekrarlarsanız, X kişisi topların gerçekten de farklı olduğuna ikna olacaktır. **(Bütünlük)**

Bu ispat sıfır bilgidir, çünkü X kişisi hangi topun yeşil hangi topun kırmızı olduğunu asla öğrenemez ve topların nasıl ayırt edilebileceğine dair de hiçbir bilgi edinmemektedir. 

### Zero Knowledge(Sıfır Bilgi Kanıtı) Türleri Nelerdir? 
-	Etkileşimli Sıfır Bilgi Kanıtları: Etkileşimli sıfır bilgi kanıtlarında, kanıtlayan ve doğrulan taraflar birkaç kez etkileşime girerler. Doğrulayıcı, ispat edene kadar sorular sorarak kanıtlayana meydan okur. 
-	Etkileşimsiz Bıfır Bilgi Kanıtları: Etkileşimsiz sıfır bilgi kanıtlarında, kanıtlayan ve doğrulayan taraflar etkileşime geçmezler. Doğrulayıcı tarafından belirli bir zamanda yalnızca bir kez doğrulanabilir. Etkileşimsiz sıfır bilgi kanıtları, etkileşimli sıfır bilgi kanıtlarına göre daha fazla hesaplama gücü gerektirmektedir. 





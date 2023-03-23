# ZERO KNOWLEDGE PROOFS
**Zero Knowledge**, ilk olarak 1980 yılında MIT araştırmacıları Shafi Goldwasser, Silvio Micali ve Charles Rackoff tarafından ortaya çıkmıştır. Araştırmacılar, *İnteraktif Kanıtlama Sistemleri* üzerinde çalışmalar sürdürürken, birinci taraf **Prover** ve mesajı doğrulayan taraf **Verifier** arasındaki ilişkiyi tanımlayacak teorik çalışmalar yürütmüşlerdir. Geçmişi 1980'li yıllara dayanan ve gelecekte hemen hemen her alanda kullanılabilecek bu teknolojiyi detaylarıyla sizler için bu repositories'de topladık. 

![image](https://user-images.githubusercontent.com/123966022/226599025-82affff6-cf38-4f89-8317-8a9405ac880c.png)

## İÇİNDEKİLER 
### Zero Knowledge Proofs Nedir?
### Zero Knowledge Proof (Sıfır Bilgi Kanıtı) Türleri Nelerdir? 
  - Interactive Zero-Knowledge Proofs (Etkileşimli Sıfır Bilgi Kanıtları)
  - Non-Interactive Zero-Knowledge Proofs (Etkileşimsiz Sıfır Bilgi Kanıtları)
  - Zero-Knowledge Succinct Non-Interactive Argument of Knowledge (Öz Kısa Etkileşimsiz Sıfır Bilgi Kanıtları)
  - Zero-Knowledge Scalable Transparent Argument of Knowledge (Öz Kısa Etkileşimsiz Şeffaf Bilgi Kanıtları)
### Zero Knowledge (Sıfır Bilgi Kanıtlarının) Kullanım ve Uygulama Alanları 
### Zero Knowledge (Sıfır Bilgi Kanıtlarının) Zorlukları Nelerdir? 


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

## Zero Knowledge (Sıfır Bilgi Kanıtı) Türleri Nelerdir? 
- Interactive Zero-Knowledge Proofs (Etkileşimli Sıfır Bilgi Kanıtları)
- Non-Interactive Zero-Knowledge Proofs (Etkileşimsiz Sıfır Bilgi Kanıtları)
- Zero-Knowledge Succinct Non-Interactive Argument of Knowledge (Öz Kısa Etkileşimsiz Sıfır Bilgi Kanıtları)
- Zero-Knowledge Scalable Transparent Argument of Knowledge (Öz Kısa Etkileşimsiz Şeffaf Bilgi Kanıtları)


### Interactive Zero-Knowledge Proofs (Etkileşimli Sıfır Bilgi Kanıtları)
Etkileşimli sıfır bilgi kanıtlarında, kanıtlayan ve doğrulan taraflar birkaç kez etkileşime girerler. Doğrulayıcı, ispat edene kadar sorular sorarak kanıtlayana meydan okur. Bu teknoloji, bir kullanıcının bir iddiada bulunmasını ve bu iddiayı kanıtlamasını sağlar, ancak kanıtlayan kişi iddiasının ne olduğunu açıklamaz. 

Örneğin, bir kullanıcının bir şifre ya da kimlik bilgisi hakkında bilgi sahibi olduğunu kanıtlaması gerektiğinde kullanılabilir.

Bu teknoloji, özellikle blok zinciri teknolojileri gibi güvenliğin önemli olduğu alanlarda kullanılır. Etkileşimli sıfır bilgi kanıtları, kullanıcının gizliliğini korurken, güvenilirlik ve doğruluk sağlamak için kullanılabilir.


### Non-Interactive Zero-Knowledge Proofs (Etkileşimsiz Sıfır Bilgi Kanıtları)
Bir kullanıcının bir iddiada bulunmasını ve iddiasını kanıtlamasını sağlayan, ancak kullanıcının doğrudan bir kanıt sunmasına gerek kalmadan yapabilen bir kriptografik protokol türüdür. Bu protokoller, özellikle veri gizliliği ve kimlik doğrulama gibi alanlarda kullanılabilir. Etkileşimsiz sıfır bilgi kanıtlarında, kanıtlayan ve doğrulayan taraflar etkileşime geçmezler. Doğrulayıcı tarafından belirli bir zamanda yalnızca bir kez doğrulanabilir. Etkileşimsiz sıfır bilgi kanıtları, etkileşimli sıfır bilgi kanıtlarına göre daha fazla hesaplama gücü gerektirmektedir. 

Etkileşimsiz sıfır bilgi kanıtları, blok zinciri teknolojileri gibi alanlarda kullanılan dijital para birimleri ve kimlik doğrulama gibi alanlarda kullanışlıdır. Örneğin, bir kullanıcının bir işlemin geçerli olduğunu kanıtlaması gerektiğinde veya bir kullanıcının kimliğinin doğruluğunu kanıtlaması gerektiğinde kullanılabilir. Bu teknoloji, kullanıcıların gizliliğini korurken, doğruluk ve güvenilirlik sağlamak için kullanılabilir.


### Zero-Knowledge Succinct Non-Interactive Argument of Knowledge (Öz Kısa Etkileşimsiz Sıfır Bilgi Kanıtları)
zk-SNARK, Zerocash'ın ortak mucidi, Zcash'ın ortak kurucusu ve StarkWare Industries'in ortak kurucusu olan Profesör Alessandro Chiesa ve ekibi tarafından Ocak 2012'de ortaya çıkarıldı.

zk-SNARK, veri gizliliğini koruyarak doğrulama işlemlerinin hızlı ve verimli bir şekilde yapılmasına olanak tanır. Bu teknoloji, kullanıcının bir iddiayı doğrulamasına olanak tanıyan öz kısa etkileşimsiz sıfır bilgi kanıtlarının bir türüdür. Bir kullanıcının bir iddiayı doğrulaması için sadece bir kanıt sunması yeterlidir ve bu kanıt, oldukça küçük boyutlu ve hızlı bir şekilde doğrulanabilir. Özellikle blok zinciri teknolojileri ve kriptoparalar gibi alanlarda kullanılır.

> SNARK = **S**uccinct **N**on-interactive **AR**guments of **K**nowledge


**Succinct**: Bu, daha küçük boyutlu bir ispatın sağladığı hızlı ve kolay doğrulamayı ifade eder. "Hızlı ve kolay" burada minimal hesaplama gereksinimlerine dönüşür, bu da SNARK'ın azaltılmış gaz tüketimi ve blok zincirinde daha hızlı işlemler için avantajlı olmasını sağlar.

**Non-interactive**: Etkileşimsiz zkp, bir kanıtlayıcının herhangi bir etkileşim olmadan belirli bir bilgiye sahip olduğunu kriptografi yoluyla kanıtlamasına olanak tanıyarak, etkileşimli zkp'nin sınırlamalarını aşar. Bugün zero-knowledge proof teknolojisi olarak adlandırdığımız çoğu şey, etkileşimsiz zkp'dır. (Etkileşimli zkp'nin sınırlaması: İspatlar olasılığa dayanır ve birden fazla etkileşim gerektirir, bu da hız ve hesaplama açısından kısmen verimsizdir.)

(Not: İki teknoloji arasındaki açık kontrast için, karşılaştırmalar erken SNARK'lar üzerinden yapılmıştır.)

Örneğin, kripto para birimleri gibi işlemlerin doğrulanması ve anonimliği sağlamak için kullanılabilir. Ancak, zk-SNARK'ın doğru bir şekilde kullanılması için, gizlilik, güvenlik ve doğruluk konularında dikkatli bir şekilde tasarlanması ve uygulanması gerekmektedir.

![image](https://user-images.githubusercontent.com/123966022/226885106-9669f0b6-c253-4e78-befa-7b7689dbfaf6.png)

**Bir zk-SNARK, üç algoritmadan oluşur:** `G`, `P` ve `V`.

- *Anahtar üreteci* `G`, gizli bir parametre `lambda` ve bir program `C` alır ve iki açık anahtar olan bir *kanıt anahtarı* `pk` ve *doğrulama anahtarı* `vk` üretir. Bu anahtarlar, yalnızca bir kez `C` programı için oluşturulması gereken genel parametrelerdir.

- *Kanıtlayıcı* `P`, kanıt anahtarı `pk`, bir kamu girdisi `x` ve özel bir şahit `w` olarak girilen girdileri alır. Bu algoritma, kanıtlayıcının bir şahit `w` bildiğini ve şahidin programı sağladığını gösteren bir kanıt `prf = P(pk, x, w)` oluşturur.

- *Doğrulayıcı* `V`, doğrulama anahtarı `vk`, bir kamu girdisi `x` ve bir kanıt prf alır ve kanıtın doğru olup olmadığını hesaplar. Bu işlev, kanıtlayıcının `C(x,w) == true` koşulunu sağlayan bir şahit `w` bildiğini doğrular.

Burada anahtar üretiminde kullanılan gizli `lambda` parametresine dikkat edilmelidir. Bu parametre, zk-SNARK'ların gerçek dünya uygulamalarında kullanımını zorlaştırır. Nedeni ise lambda'yı bilen herhangi bir kişi, herhangi bir program `C` ve açık girdi `x` için, gizli `w` bilgisi olmadan doğru olduğu kanıtı `fake_prf` gibi sahte bir kanıt oluşturabilir.

![image](https://user-images.githubusercontent.com/123966022/227129697-e80777ef-d6df-4700-95cf-49aae2ac7587.png)


### Zero-Knowledge Scalable Transparent Argument of Knowledge (Öz Kısa Etkileşimsiz Şeffaf Bilgi Kanıtları)
zk-STARK, 2018 yılında Eli Ben-Sasson ve ekibi tarafından ortaya çıkarılmıştır. zk-STARK, öz kısa etkileşimsiz sıfır bilgi kanıtlarının bir türüdür ve blok zincirlerinde kullanılabilen bir doğrulama protokolüdür. Diğer sıfır bilgi kanıtı türlerinden farklı olarak, zk-STARK'ın temel özelliği ölçeklenebilirliktir. Bu teknoloji, özellikle büyük veri işleme işlemlerinde kullanılabilir.
zk-STARK, veri gizliliğini koruyarak doğrulama işlemlerinin hızlı ve verimli bir şekilde yapılmasına olanak tanır. Kanıtın boyutu, verilerin boyutundan bağımsızdır ve sonuç olarak kanıt, oldukça küçük boyutlu ve hızlı bir şekilde doğrulanabilir.

zk-STARK'ın blok zincirleri gibi alanlarda kullanılabilmesi, özellikle anonimlik ve güvenlik gibi konularda avantaj sağlar. Ancak, zk-STARK'ın uygulanması oldukça karmaşık olabilir ve doğruluğunun, gizliliğinin ve güvenliğinin sağlanması için dikkatli bir şekilde tasarlanması ve uygulanması gerekmektedir. 

> STARK = **S**calable **T**ransparent **AR**guments of **K**nowledge

**Scalable**: zk-STARK, blok zincirinin ölçeklenebilirliğini iyileştirmeye odaklanan bir teknolojidir. Karmaşık ispatları çözerken bile, SNARK'a kıyasla büyük ölçüde daha yüksek bir hesaplama gücü gerektirmez ve bu nedenle daha iyi ölçeklenebilirlik beklenir. Aşağıdaki grafik, STARK beyaz kağıdından alınan verilere dayanarak, hesaplama karmaşıklığı arttıkça SNARK ve STARK için gereken süredeki değişikliği görselleştirir. İspatın artan karmaşıklığına rağmen STARK, nispeten mütevazı dalgalanmalar gösterir.

**Transparent**: STARK güvenilir bir kurulum gerektirmez. Bu, ispat için kullanılan parametrelerin şeffaf bir şekilde açıklandığı anlamına gelir.


### zk-SNARK ve zk-STARK Arasındaki Fark Nedir?

- **Scalability**: zk-SNARK, hesaplama gücü açısından daha yüksek bir ölçeklenebilirlik sınırına sahiptir. Karmaşık ispatları çözerken bile, SNARK'a kıyasla daha az hesaplama gücü gerektirir. Bu nedenle, zk-STARK'a kıyasla daha hızlı ve daha ölçeklenebilir bir teknolojidir.

- **Transparency**: zk-SNARK, ispat için güvenilir bir kurulum gerektirir. Bu kurulum işlemi, herhangi bir hileli davranışta bulunulmaması için çok önemlidir. Ancak zk-STARK, güvenilir bir kurulum gerektirmez ve bu nedenle daha şeffaf bir teknolojidir.

- **Security Assumptions**: zk-SNARK, çift örneklemeli hesaplamalara dayanırken, zk-STARK, post-kuantum güvenlik önlemleri sağlamak için polinomların kullanımına dayanır. Bu nedenle, zk-STARK, gelecekteki kuantum saldırılarına karşı daha dayanıklı olabilir.

- **Proof Size**: Sıfır bilgi kanıtı, bir tarafın (kanıtlayan) belirli bir ifadenin doğru olduğunu diğer tarafına (doğrulayıcıya) açıklamadan kanıtlama yöntemidir. Kanıt boyutu, bu kanıt için gereken veri miktarına atıfta bulunur.
Kanıt boyutu, sıfır bilgi kanıtında belirleyici bir faktördür, çünkü kanıt boyutu ne kadar büyükse, kanıtı oluşturmak ve göndermek için gereken hesaplama ve etkileşim o kadar fazla olur.
Güvenilir kurulumu tamamlanmış bir SNARK'ın ispat boyutu, STARK'lara göre önemli ölçüde daha küçüktür. Sonuç olarak, SNARK'ın gaz tüketimi ve gereken zamanı STARK'tan önemli ölçüde daha düşüktür. Bu, birçok projenin neden SNARK uygulamayı tercih ettiği nedenlerden biridir.


Sonuç olarak, zk-SNARK ve zk-STARK, farklı avantajlar ve dezavantajlar sunan iki farklı teknolojidir. Her ikisi de blok zinciri ve diğer alanlarda gizlilik ve güvenlik açısından önemli bir rol oynamaktadır.


![image](https://user-images.githubusercontent.com/123966022/226895926-6fd963f2-c26c-4dc1-937d-49c0dcb0ed88.png)


zk-STARK hash fonksiyonu kullandığı ve güvenilmez bir kanıt modeli tercih ettiği için; zk-SNARK teknolojisine göre doğrulama işlemi uzun sürebilir. Prover (kanıtlayan taraf) zaman olarak zk-SNARK'a göre daha düşüktür. 

![image](https://user-images.githubusercontent.com/123966022/226896399-56e0f821-8d53-4298-981d-ac983522bd98.png)



## Sıfır Bilgi Kanıtlarının Kullanım ve Uygulama Alanları 

- **Blockchain:** 
Bitcoin ve Ethereum gibi halka açık blokzincirlerinin şeffaflığı, işlemleri kamuya açık ve doğrulanmasını mümkün kılar. Ancak bu durum daha az mahremiyet anlamına gelir ve kullanıcıların anonimleştirilmesine yol açabilir. 
Zero Knowledge bu bağlamda kamuya açık blok zincirlerine daha fazla gizlilik kazandırabilir. Örneğin, Zcash kripto para birimi, Zero-Knowledge Succinct Non-Interactive Argument of Knowledge (zk-SNARK) adlı bir zero-knowledge yöntemine dayanmaktadır. Ayrıca Ethereum blok zincirinde kullanılan ve ölçeklenebilirlik ve gizlilik sağlayan Zero-Knowledge Scalable Transparent Argument of Knowledge (zk-STARK) yöntemidir.

- **Finans:** 
ING, müşterilerinin gizli numaralarını belirli bir aralıklarda doğruluğunu kanıtlayabilecekleri ZKPs yöntemi kullanıyor. Örnek vermek gerekirse, konut kredisi almak için başvuru yapan kişi net maaş bilgisini paylaşmadan kredi almaya uygun olduğunu kanıtlayabilir. 

- **Kimlik Doğrulama:** 
Sıfır bilgi kanıtı, şifre gibi gizli ve kişisel verileri değiştirmeden kullanıcıların kimlik bilgilerini doğrulamalarını sağlayabilir. 

- **Makine Öğrenimi:**
ZKP'ler, bir makine öğrenimi algoritmasının sahibinin model hakkında herhangi bir bilgi açıklamadan diğerlerine model sonuçları hakkında ikna etmesine olanak tanıyabilir.


## Sıfır Bilgi Kanıtlarının Zorlukları Nelerdir? 
- Sıfır Bilgi Kanıtlarının Garantisi Olmaması 

Top seçimi sürecinin her tekrarlama aşamasında kanıtlayıcının yalan söyleme olasılığı azalır, ancak hiçbir zaman sıfıra ulaşamaz. Bu nedenle, sıfır bilgi kanıtları matematiksel olarak gerçek bir kanıt değildir.

- Yoğun Hesaplama Süreci  

Kullanılan algoritmalar, doğrulayıcı ve kanıtlayıcı arasında birçok etkileşim gerektirdiği için (etkileşimli ZKP'lerde), veya yüksek hesaplama kapasiteleri gerektirdiği için (etkileşimsiz ZKP'lerde) hesaplama yoğunluğuna sahiptir. Bu durum, ZKP'lerin yavaş veya mobil cihazlar için uygun olmamasına neden olur.

- Sınırlı Kullanım

Sıfır bilgi kanıtları, sayısal verilere dayandığı için kısıtlıdır. Bu, diğer tür bilgilerle yapılmayacak olan sayısal değerlere bir geçişin gerekliliği anlamına gelir. Bu finansal ve benzeri sayısal işlemler için bir endişe olmayabilirken, sıfır bilgi kanıtları büyük karmaşık veri kümeleriyle kullanıldığında daha az pratiktir.

-	Minimal Altyapı

Başka bir zorluk, protokol ile ilgisi olmayan bir konudur. Sıfır bilgi kanıtlarının uygulanması o kadar yeni ki, belirlenmiş standartlar, diller ve sistemlerin eksikliği bulunmaktadır. Bu altyapı eksikliği, kurumların önce bir etkileşim sistemi kurmadan sıfır bilgi kanıtlarını kullanarak etkileşimde bulunmasını zorlaştırır. ZKProof, sıfır bilgi kanıtlarının benimsenmesini hızlandıracak uluslararası standartları oluşturmaya çalışan bir organizasyondur.


## Ethereum'da zk-SNARK'ların Kullanımı

Ethereum, merkezi olmayan uygulamaların geliştirilmesine olanak sağlayan bir blok zinciridir. Ancak, bu uygulamaların tümü blok zincirinde çalıştırılır ve bu nedenle blok zincirindeki hesaplama gücü ve depolama alanı sınırlıdır. Bu sınırlamalar, bazı uygulamaların yeterince hızlı veya verimli bir şekilde çalışmasını engelleyebilir. Bu sorunu çözmek için, zk-SNARK'lar gibi çözümler Ethereum'un geliştiricileri tarafından entegre edilmeye başlandı.

zk-SNARK'lar, Sıfır Bilgi Kanıtı olarak adlandırılan bir protokolü kullanır. Bu protokol, bir kanıtlayıcının bir belgeyi sunduğu bir doğrulama sistemi oluşturur. Bu doğrulama sistemi, belgeyi doğrulamak için gerekli olan tüm bilgileri içerir, ancak belgenin kendisi hakkında hiçbir bilgi sağlamaz. Bu, belgeyi doğrulamanın, belgenin içeriğinin tam olarak görülmeden yapılmasına olanak tanır.

![image](https://user-images.githubusercontent.com/123966022/227145532-d6dc9599-5210-456a-81d9-cd8b7f9d2f4a.png)

Ethereum'da zk-SNARK'ların kullanımı, doğrulama algoritmasının blok zincirine entegre edilmesiyle gerçekleştirilir. Bu, zincir dışında çalıştırılan bir üreteç kullanılarak kanıt anahtarının ve doğrulama anahtarının oluşturulmasını gerektirir. Daha sonra, bir kanıtlayıcı kanıt anahtarını kullanarak bir kanıt oluşturabilir ve bu kanıt blok zincirine eklenmeden önce doğrulama anahtarı ve kamu girdisi ile birlikte doğrulama algoritmasından geçirilebilir. Doğrulama algoritmasının sonucu, blok zincirindeki akıllı sözleşmenin diğer aktiviteleri tetiklemesine izin verir.

zk-SNARK'lar Ethereum'da birçok farklı kullanım alanı sunar. Örneğin, özel bir veritabanında depolanan özel bilgilerin kullanımını kontrol etmek için kullanılabilirler. Ayrıca, blok zinciri içinde gerçekleştirilen anlaşmaların doğrulanması için kullanılabilirler.

Sonuç olarak, zk-SNARK'lar gibi teknolojiler, blok zincirinin kullanımının daha da genişlemesine olanak tanır ve Ethereum'da daha güvenli ve ölçeklenebilir uygulamaların geliştirilmesine yardımcı olur.


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

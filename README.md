# hafta-2-oop-basics-generic-types
Java OOP Programming and Generic Data Types


# Ödev Sorusu

**Açıklama1:** Soruların her biri ayrı ayrı algoritmaları ifade eder. Algoritma dediğimiz kavram bilgisayar programcılığı için çok önemli bir konudur.
Algoritma düşünce sistematiğini geliştirmeyen bir yazılımcı yazılım kütüphanelerini, programlama dillerini öğrenerek iyi bir programcı olma yolunda çok ileriye gidemez.

**Açıklama2:** Bu önemine istinaden ekstra algoritma ödevleriyle bu sizlerin bu yönünü geliştirmek hedefindeyiz.

**Açıklama3:** Verilen soruları Java dilinde kodlamanızı rica ediyorum. Ayrıca, hazır çözümler kullanmadan herkesin bireysel kodlamalasını rica ediyorum.
Yardımlaşma için birbirinizden ve benden yardım alabilirsiniz. Tek şart copy-paste kodlar lütfen olmasın :) Sizin gelişiminiz için bu çok önemlidir.

**Açıklama4:** Ödev sorularını yaparken takıldığınız yerlerde Google'da aramalar yaparak yardım alabilirsiniz. Unutmayın Google en büyük yardımcınız :)

#Sorular

**Soru1:** 

Girdi:

<img width="130" alt="Screen Shot 2020-03-16 at 00 23 10" src="https://user-images.githubusercontent.com/2838457/76711013-14dd9580-671d-11ea-9157-93452af607cc.png">

Çıktı:

<img width="485" alt="Screen Shot 2020-03-16 at 00 23 18" src="https://user-images.githubusercontent.com/2838457/76711014-160ec280-671d-11ea-8493-4f574e8d955b.png">

Yukarıdaki matrisi Spiral bir biçimde ekrana yazdıran algoritmayı yazınız. Matrisi sabit şekilde oluşturabilirsiniz. Örnek girdi ve çıktı yukarıda yer almaktadır.


**Soru2:**

N x M ile M x T boyutlarında 0-10 arası rastgele sayılardan oluşan iki matris tanımlayınız. Bu iki matrisin çarpımını yapan fonksiyonu yazın. Çarpım sonucu oluşan matrisi ekrana yazdırın. Bu matris çarpımını yapan sınıfı Generic tipte tanımlayınız. Matris sınıfı double, int, float, long gibi Number kökenli matrisleri çarpabilmelidir.


**Soru3:**

N boyutunda 0-10 arası rastgele sayılardan oluşan bir dizi tanımlayınız. Bu dizi içinde mükerrer olan elemanları ekrana yazdıran algoritmayı tasarlayınız.

Örnek: { 2, 4, 5, 11, 33, 2, 5, 55, 100, 1 }

Örnek çıktı:
2
5

**Soru4:**

Sigorta firması için bir yazılım yaptığınızı düşünün. Sigorta firmasının "Bireysel" (Individual) ve "Kurumsal" (Enterprise) olmak üzere iki tip müşteri profili bulunmaktadır. Müşteri profili için "Account" isminde soyut sınıf (abstract class) tasarlayınız. Account sınıfı müşterinin sisteme giriş sonrasında tüm bilgilerinin tutulduğu hesap bilgisidir. "Account" sınıfı içinde "User" tipinde bir nesne referansı bulunur. (Aggeration ilişkisi olarak)

"User" sınıfı müşterinin kişi bilgilerini ifade eder. "User" sınıfında müşterinin

* isim (String), 
* soyisim (String),
* email (String),
* şifre (String),
* meslek (String), 
* yaş (int),
* adres listesi (ArrayList<Address>)
* sisteme son giriş tarihi (Date)

bilgileri bulunur. Ayrıca, "User" sınıfında ArrayList tipinde adreslerinin tutulduğu bir liste vardır.
Adres bilgisi iki tiptir. Ev adresi ("HomeAddress") ve İş adresi ("BusinessAddress") olmak üzere iki tane sınıf tasarlayınız. Bu adres sınıfları "Address" isimli bir interface'den kalıtım alacaktır. Fakat, bu interface'de hangi fonksiyonların olması gerektiğine siz karar vereceksiniz.

Müşteri adreslerinin ekleyip çıkarılma sorumluluğunu üstlenmiş olan "AddressManager" isminde bir sınıf tasarlayınız. Bu sınıfın içinde "User" nesnesinin adres listesine eleman ekleme-çıkarma yapabilen iki tane static fonksiyon tanımlayınız. Bu fonksiyon isimlerini siz belirleyiniz.


"Account" sınıfında müşteri bilgilerini ekrana yazdıran "final" tipinde, değer döndürmeyen ve ismi "showUserInfo" bir fonksiyon tanımlayınız.

"Account" sınıfında müşterilerin yaptırdıkları sigortaları liste halinde saklayınız. Sigortayı temsil eden "Insurance" isminde bir soyut sınıf tasarlayınız. Bu soyut sınıf içinde 

* sigortanın ismi (String),
* sigortanın ücreti (double)
* sigortanın başlangıç-bitiş tarihi (Date)

gibi değişkenlere sahip olacaktır. Ayrıca "calculate" isminde soyut bir fonksiyon tanımlanacaktır. Bu soyut fonksiyon aşağıda kalıtım alınan sınıflarda doldurulacaktır.

Bu soyut sınıftan türeyen 

* "HealthInsurance" (özel sağlık sigortasu), 
* "ResidenceInsurance" (konut sigortası), 
* "TravelInsurance" (seyahat sigortası), 
* "CarInsurance" (otomobil sigortası) 

4 tane alt sınıf tasarlayınız. Her alt sınıf "calculate" isimli soyut fonksiyonu override ederek, sigorta ücretini kendine göre hesaplayacaktır.


Yukarıdaki tanımları dikkate aldığımızda soyut sınıf olan "Account" sınıfında aşağıdakiler yer almalıdır.

* kullanıcının login olma durumu (AuthenticationStatus)
* kullanıcı nesnesi (User)
* kullanıcının yaptırmış olduğu sigortaların listesi (ArrayList<Insurance>)



* AuthenticationStatus tipinde bir enum tanımlayınız. Enum içinde SUCCESS ve FAIL isminde iki tane sabit tanımlayın.
SUCCESS login işlemi başarılı ise kullanılacaktır. FAIL ise login olmamışsa kullanılacaktır. 

* kullanıcının hesabına login olabilmesi için bir fonksiyon tanımlanacaktır. Bu fonksiyon email ve şifre bilgisi alacak ve gelen email şifre bilgisini User sınıfındaki email ve şifre ile kıyaslayacaktır. Eğer girilen bilgiler doğruysa giriş işlemi başarılı olacaktır. Ve kullanıcının login olma durumu SUCCESS'e çekilecektir. Giriş işlemi başarısız ise "InvalidAuthenticationException" tipinde bir hata fırlatacaktır. Bu hata sınıfını Exception isimli Java sınıfından kalıtım alarak sizin yazmanız gerekecektir.

* kullanıcının adreslerine ekleme yapabileceği bir soyut olmayan fonksiyon tanımlanacaktır.
kullanıcının adreslerinden çıkartma yapabileceği bir soyut olmayan fonksiyon tanımlanacaktır.
kullanıcının login olma durumunu veren değer döndüren fonksiyon tanımlanacaktır.

* kullanıcının sigorta poliçesi ekleyebilmesi için soyut (abstract) bir fonksiyon tanımlanacaktır. Bu soyut sınıf "Individual" ve "Enterprise" isimli alt sınıflarda override edilerek doldurulacaktır. Çünkü, bireysel ve kurumsal müşterilerin ekledikleri paketlerin fiyatlarına uygulanan kar marjı farklı olacaktır.


"Individual" ve "Enterprise" sınıfları "Account" sınıfından kalıtım alacaktır.


AccountManager isminde bir sınıf tasarlayınız. Bu sınıf içinde TreeSet tipinde bir veri listesi tutsun. Oluşturduğunuz bireysel ve kurumsal hesapları bu listede saklayınız. bu sınıf içinde login isminde bir fonksiyon tanımlayınız. Bu fonksiyon dışarıdan verilen email ve şifre bilgisini alıp Account listesi üzerinde dolaşıp uygun bir giriş işlemi bulursa Account nesnesini çağrıldığı yere dönecektir. Bu fonksiyon Account nesnesi üzerindeki "login" olma fonksiyonunu çağıracaktır. Unutmayın bu fonksiyon "InvalidAuthenticationException" tipinde hata fırlatabiliyordu. Bu nedenle burada try-catch mekanizması kurmayı unutmayınız.

"Account" sınıfından nesneleri TreeSet içinde tutacağımız için "Comparable" interface'den kalıtım almış olmasına dikkat edin. Ayrıca, "Account" sınıfının "hashCode" ve "equals" fonksiyonlarını doldurmayı unutmayın.


klavyeden email ve şifre bilgisini alan bir sınıf tasarlayınız. Klavyeden alınan email ve şifre bilgisi ile AccountManager sınıfındaki "login" fonksiyonunu çağırın. Eğer geçerli bir kullanıcı ile giriş yapmışsanız bu fonksiyon size Account tipinde bir nesne dönecektir. 

**Bu bir sınav değildir! Geliştirmek için kodluyoruz ... :))**

<<<<<<< HEAD
# SQL Sorgu Alıştırmaları

Bu hafta SQL sorguları üzerine çalışıyorsunuz. Bugünkü alıştırmada sizin için hazırladığımız veritabanında aşağıda istediğimiz sonuçları elde etmenize yarayan SQL sorgularını oluşturacaksınız.

# Proje Kurulumu
Projeyi forklayın ve clonlayın. Tamamladığınızda da pushlayın.

## Kütüphane Bilgi Sistemi

Bu veritabanı, bir okulun kütüphanesinden öğrencilerin aldıkları kitapların bilgisini barındırmaktadır.
* src -> main -> resources altında `test.sql` adında bir dosya bulacaksınız.
* `test.sql` dosyasını projeye başlamadan önce kendi veritabanınızda MUTLAKA ÇALIŞTIRMALISINIZ.
* `application.properties` dosyasında `spring.datasource.username` karşısına veritabanını bağlanmak için kullandığınız kullanıcı ismini MUTLAKA GİRİNİZ.
* `application.properties` dosyasında `spring.datasource.password` karşısına veritabanını bağlanmak için kullandığınız şifreyi MUTLAKA GİRİNİZ.


#Tablolar
`ogrenci` tablosu öğrencilerin listesini tutar.
`islem` tablosu öğrencilerin kütüphaneden aldıkları kitapların bilgilerini tutar
`kitap` tablosu kütüphanedeki kitapların bilgisini tutar
`yazar` tablosu kitapların yazarları bilgisini tutar
`tur` tablosu kitapların türlerini tutar.

Tablo ilişiklerini görmek için [ktphn.png] dosyasına göz atın.

Yazdığınız sorguları buradan test edebilirsiniz: [https://ergineer.com/assets/materials/fkg36so5-kutuphanebilgisistemi-sql/] (update, delete, drop sorguları iptal edilmiştir).

### Görevler

Aşağıda istenilen sonuçlara ulaşabilmek için gerekli SQL sorgularını yazmaya çalışacağız.
İlgili sqlleri `OgrenciRepository` sınıfı altında tanımlanan `QUESTION` stringlerinin karşısına yazınız.
* 1. soru için sql sonucunu `OgrenciRepository` sınıfının içerisindeki `QUESTION_1` stringinin içerisine yazınız.


	1) Öğrenci tablosundaki tüm kayıtları listeleyin.

	
	2) Öğrenci tablosundaki kız öğrencileri listeleyin.
	
	
	3) Öğrenci tablosunda kaydı bulunan sınıfların adını her sınıf bir kez görüntülenecek şekilde listeleyiniz. 
	
	
	4) Öğrenci tablosunda, 10A sınıfında olan kız öğrencileri listeleyiniz.
	
	
	5) Öğrenci numarası 5 ile 10 arasında olan Kız öğrencileri listeleyiniz.
	
	
	6)  Öğrencileri adına göre sıralayınız (alfabetik)
	
	
	7) 10A sınıfındaki öğrencileri okul numarasına göre azalan olarak sıralayınız.
	
	
	8) Öğrenciler tablosundaki en genç öğrenciyi listeleyiniz.
	
	
	9) Öğrenciler tablosundaki en yaşlı öğrenciyi listeleyiniz.
	
	
	10) İkinci harfi E olan ogrencileri listeleyiniz.


=======
#  Java Spring REST API with JPA

### Proje Kurulumu

Projeyi öncelikle forklayın ve clone edin.
Daha sonra projeyi IntellijIDEA kullanarak açınız. README.md dosyasını dikkatli bir şekilde okuyarak istenenleri yapmaya çalışın.
Proje sayımız ilerledikçe proje yönetimimizi kolaylaştırmak adına projelerimizi belli klasör kalıplarında saklamak işimizi kolaylaştırmak adına iyi bir alışkanlıktır.
Örnek bir Lokasyon: Workintech/Sprint_1/Etud.

### Hedeflerimiz:

### Burger Rest Api

 ### Başlangıç
 * Projenizi pushlamadan önce MUTLAKA test klasörü altında bulunan ```MainTest``` ve ```ApplicationPropertiesAndControllerTest``` sınıflarını çalıştırıp testleri kontrol ediniz.
 * Projenizde ```Spring Web, Spring Data Jpa, postgresql``` dependencylerinizin olduğundan emin olunuz.
 * Maven dependency management sistemini kullanarak tüm dependencyleri install edin.
 * Uygulamanızı  ```9000``` portundan ayağa kaldırın.
 * Bir burgerci için rest api dizayn etmeniz istenmektedir.

### Amaç
 * Amacımız veritabanına ekleme yapabileceğimiz bir burger API'yı hazırlamak.
 * Bu Api'yi oluştururken error handling ve validation kurallarına uymalıyız.
 * Dependency Injection kurallarına uymalıyız.
 
 ### Görev 1
 * ```com.workintech.s18d1``` paketi altında ```controller```, ```entity```, ```exceptions```, ```dao```, ```util``` isminde 5 adet daha paket oluşturunuz.
 * Project Lombok'u dependency olarak uygulamanıza ekleyin.
 * ```entity``` paketinin altına ```Burger``` adında bir sınıf tanımlayınız. İçerisinde instance variable olarak ```id, name, price, isVegan, breadType, contents``` isminde 6 tane değişken oluşturun.
 * breadType değişkenini BURGER, WRAP veya DOUBLE değerlerinden birini alabilecek bir enum olarak tanımlayınız.
 * JPA annotation larını uygulayarak bu sınıfı bir veritabanı tablosu olucak şekilde işaretleyiniz.
 * ```application.properties``` dosyanızı kullanarak veritabanı bağlantınızı kurun.
 * ```spring.jpa.hibernate.ddl-auto``` opsiyonu ile ilk başta tablonuzu create edin. Daha sonra bu opsiyonu değiştirerek tablolardaki verilerin silinmesini önleyin.
 * Spring uygulamasının veritabanı loglarını açarak veritabanına yolladığınız her soruguyu inceleyin.

### Görev 2
 * Dao paketi altında ```BurgerDao``` isminde bir interface oluşturun.
 * içerisinde şu işlemleri yapıcak methodları tanımlamalısınız.
 * ```save``` => Burger objesi alır ve bunu veritabanı tablosuna yazar.
 * ```findById``` => Integer id değeri alır ve karşılığında veritabanındaki Burger kaydını döner.
 * ```findAll``` => Hiçbir parametre almaz. Veritabanındaki bütün Burgerleri döner
 * ```findByPrice``` => price parametresi alır. Aldığı price değerinden daha büyük olan Burgerleri pricelarına göre büyükten küçüğe dogru listeler.
 * ```findByBreadType``` => BreadType parametresi alır. Bu parametreye eşit olan breadType tipindeki Burgerleri isimlerine göre alfabetik sırada küçükten büyüğe doğru sıralar
 * ```findByContent``` => Bir adet String değeri alır ve bu değeri contents tablosunda içeren tüm burgerleri döner.
 * ```update``` => Burger objesi alır ve bunu var olan burger objesi ile günceller.
 * ```remove``` => Bir adet id değeri alır ve bu id değerindeki Burger'i siler.
 * BurgerDaoImpl isimli bir sınıf yazınız. BurgerDao sınıfını ```implements``` etmeli.

 ### Görev 3
 * ```controller``` paketi altında ```BurgerController``` adında 1 tane controller yazmalısınız.
 * BurgerDaoImpl sınıfını BurgerController sınıfı altında ```Dependency Injection``` yöntemini kullanarak çağırınız
 * Amacımız CRUD işlemlerini tanımlayan endpointler yazmak.
 * [GET]/workintech/burgers => tüm burger listini dönmeli.
 * [GET]/workintech/burgers/{id} => İlgili id deki burger objesini dönmeli.
 * [POST]/workintech/burgers => Bir adet burger objesini veritabanına kaydeder.
 * [PUT]/workintech/burgers/{id} => İlgili id deki burger objesinin değerlerini yeni gelen data ile değiştirir.
 * [DELETE]/workintech/burgers/{id} => İlgili id değerindeki burger objesini veritabanından siler.
 * [GET]/workintech/burgers/findByPrice => RequestBody'de price değerini alır ve BurgerDaoImpl sınıfındaki findByPrice metodunu çağırır.
 * [GET]/workintech/burgers/findByBreadType => RequestBody'de breadType değerini alır ve BurgerDaoImpl sınıfındaki findByBreadType metodunu çağırır.
 * [GET]/workintech/burgers/findByContent => RequestBody'de content değerini alır ve BurgerDaoImpl sınıfındaki findByContent metodunu çağırır.

 ### Görev 3
 * Her endpointin hata fırlatabileceği senaryolar düşünülmeli ```exceptions``` paketi altına bu Error sınıfları oluşturulmalı.
 * Error Handling Global bir merkezden yönetilmeli. Controller sınıflarının altında olmamalı.
 * BurgerErrorResponse ve BurgerErrorException adnında iki sınıf yazılmalı.
 * BurgerErrorResponse içerisine sadece message stringi instance variable olarak eklenmeli.
 * BurgerException RuntimeException sınıfından türemeli ve içerisinde ek olarak HttpStatus tipinde bir instance variable tutmalıdır.
 * Her Controller ```@Slf4j``` ile işaretlenmelidir. Endpoint bir şekilde hata döndüğünde ```error logu``` basılmalı.
 * validation işlemleri controller sınıfı içinde kalmamalı. ```util``` paketi altında ```BurgerValidation``` isimli bir sınıf oluşturunuz. Validation işlemlerini buraya alınız.

### Görev 4[OPTIONAL]
 * logging.level.org.hibernate.SQL=Debug ve logging.level.org.hibernate.jdbc.bind=trace propertyleri kullanılarak oluşturulan queryleri inceleyiniz.
 * Codepen üzerinden veya bir React uygulaması oluşturarak Spring Boot ile yazdığımız projeye request atmayı deneyiniz.  cors hatasını nasıl çözebiliriz.


 
>>>>>>> 60569d256c635506f1eccb44e0652b4b8fea0d29

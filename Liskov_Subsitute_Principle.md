# Liskov'un yerine geçme prensibi

## Liskov'un yerine geçme prensibi nedir?

SOLID prensiplerinin üçüncü maddesidir. Liskov’un yerine geçme prensibi, Açık Kapalı Prensibi’nin geliştirilmiş halidir ve nesne yönelimli programlama prensiplerinden çok biçimlilik ile de bağlantılıdır. Bu prensibe göre türetilen sınıf nesneleri, temel sınıf davranışının yerini almamalı, tamamlamalıdır.

## Liskov'un yerine geçme prensibi neden kullanılmalıdır?

Yalnızca sözdizimsel ilişkiden ziyade anlamsal bir ilişkidir, çünkü hiyerarşideki türlerin, özellikle nesne türlerinin anlamsal birlikte çalışabilirliğini garanti etmeyi amaçlar. Örneğin bir "kuş" sınıfında "uç" metodunu kullanmak istersek, bazı kuşlar uçamadıkları için kuş sınıfından türetilen sınıflarda uç metodunun bulunmaması gerekir. Bunu sağlayabilmek için Liskov'un yerine geçme prensibi kullanılmalıdır.

## Liskov'un yerine geçme prensibi nasıl kullanılır?

Temel sınıf olarak oluşturulan kuş sınıfında uçma metodu olmamalıdır.

class kus{

}

Uçabilen kuşlar için bir interface oluşturulabilir.

public interface IUcabilenKuslar{

public void uc();

}

Uçabilen kuşlara bu özellik eklenebilir.

class leylek extends kus implements IUcabilenKuslar{

public void uc();

}

Uçamayan kuşlara bu özellik eklenmez.

class deveKusu extends kus{

}

## Liskov'un yerine geçme prensibi nerede tanıtılmıştır?

Orlando, Florida'daki Bilgisayar Derneği (Association for Computing Machinery) SIGPLAN tarafından Uluslararası Nesne Yönelimli Programlama Sistemleri, Diller ve Uygulamalar (Object-oriented Programming, Systems, Languages, and Applications) Konferansında veri soyutlama ve hiyerarşi başlıklı bir açılış konuşmasında tanıtılmıştır.

## Liskov'un yerine geçme prensibi ne zaman tanıtılmıştır?

4 Ekim 1987 tarihinde düzenlenen OOPSLA konferansında tanıtılmıştır.

## Liskov'un yerine geçme prensibi kim tarafından geliştirilmiştir?

![](https://upload.wikimedia.org/wikipedia/commons/thumb/3/38/Barbara_Liskov_MIT_computer_scientist_2010.jpg/220px-Barbara_Liskov_MIT_computer_scientist_2010.jpg)

Barbara Jane Huberman Liskov tarafından geliştirilmiştir. 7 Kasım 1939 yılında Amerika'da doğan Barbara Liskov, matematik alanında lisans derecesi ve fizik alanında yandal eğitimini 1961'de tamamlamıştır. Stanford Üniversitesinde bilgisayar bilimi doktora derecesi alan ilk kadınlardan birisidir. Yapay zeka üzerine çalışmalar yapmış ve kariyerinin ilk yıllarında araştırma personeli olarak Mitre'de çalışmıştır. Programlama dillerine yaptığı katkılarla John von Neumann Madalyası kazanmıştır. 2008 yılında aldığı Turing Ödülü de kazandığı ödüllerden biridir. Barbara Liskov, dört kitabın ve yüzün üzerinde teknik makalenin yazarıdır.

## Kaynaklar

Vaskaran Sarcar, & Sunil Sati. (2019). Java design patterns : a hands-on experience with real-world examples. Apress, New York.  ‌

https://www.cs.utexas.edu/users/downing/papers/LSP-1996.pdf

https://www.cs.ubc.ca/~ebani/papers/LiskofHappySad_ICSE-SEET_2018.pdf
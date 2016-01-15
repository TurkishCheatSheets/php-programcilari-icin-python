# PHP Programcıları İçin Python

Daha önce PHP ile çalışanlar, farklı arayışlara girebilirler. Yeni bir dil keşfetmek istediklerinde öğrenmesi diğer dillere göre hem daha kolay hem de zevk versin isterler.

Python, öğrenmesi daha kolay ve daha zevkli bir programlama dilidir. Bu repoda Python öğrenmeyi düşünen PHP programcılarına basit benzerlikler sunacağım.

## Python

Herhangi bir Linux/Unix dağıtımı kullanıyorsanız Python hazır olarak yüklü gelecektir. Eğer Windows kullanıcısı iseniz Python yorumlayıcısını bilgisayarınıza indirip kurabilirsiniz.

*İndir*: [https://www.python.org/](https://www.python.org/)

Bu repoda Python 3.5.x sürümü ile anlatım yapacağım. Ancak 3.x sürümlerinin önceki sürümlerinde de bu basit bilgiler işinize yarayacaktır.

Daha fazla bilgi almak için Python belgeler sayfasına bakabilirsiniz. [https://docs.python.org/3/](https://docs.python.org/3/)

Python hakkında geçerli ve mükemmel bir Türkçe kaynak arıyorsanız Fırat Özgül tarafından hazırlanan ücretsiz çeviriye göz atabilirsiniz: [http://www.istihza.com/](http://www.istihza.com/)

*Python 2.x/3.x Sürümleri için ayrı ayrı belgelendirmeler mevcuttur.*

## İçerik Tablosu:

 - [Başlarken](#başlarken)
    - 1 - [Ekrana Değer Yazdırmak](#1---ekrana-değer-yazdırmak)
    - 1.1 - [Yorum Satırları](#11---yorum-satırları)
    - 1.2 - [Değişkenler](#12---değişkenler)
    - 1.3 - [Sabitler](#13---sabitler)
    - 1.4 - [Diziler](#14---diziler)
    - 1.5 - [Veri Türleri](#15---veri-türleri)
    - 1.6 - [Karar Yapıları](#16---karar-yapıları)
    - 1.7 - [Döngüler](#17---döngüler)
        - 1.7.1 - [while Döngüsü](#171---while-döngüsü)
        - 1.7.2 - [for Döngüsü](#172---for-döngüsü)
    - 1.8 - [Fonksiyonlar](#18---fonksiyonlar)
    - 1.9 - [Sınıflar](#19---sınıflar)

 - [Yapılacaklar](#yapılacaklar)
 - [Katkı](#katkı)

### Başlarken

Bu bölüme söz dizim ile başlamak istiyorum. Python söz dizimi PHP'ye göre daha basittir. PHP'de bulunan noktalı virgül, Python için gerekli değildir. Ayrıca Python ile kodlama yaparken dil etiketleri açmanıza da gerek yoktur. Python'da dosya uzantıları **.py** şeklinde verilir. Python ile yazılan kodları çalıştırmak için konsol ekranına `python3 dosyaadi.py` komutu verilir.

PHP'de kod yazacaksanız mutlaka PHP etiketini açmalısınız:

```php
<?php

// kodlar burada
```

Python'da kod yazarken böyle bir durum söz konusu değil. Bunu basit bir örnekle görelim:

```python
2+2
```

Bu kod Python dosyasında herhangi bir anlam ifade etmese de çalışan bir koddur.

### 1 - Ekrana Değer Yazdırmak

PHP'de ekrana değer yazdırma işlemini `echo` ile yapıyorduk. Python'da ise bunu `print()` işlevi ile yapıyoruz.

**index.php**

```php
<?php

echo 'Merhaba Dünya';

?>
```
Yukarıdaki kod ile PHP'de merhaba dünya yazdırırken dil etiketlerini açtık ve ifade sonunu noktalı virgül ile kapattık. Fakat Python için böyle bir gereksinim söz konusu değil.

**main.py**

```python
print('Merhaba Dünya')
```

Php'de echo iki şekilde yazılabilir. `echo` ve 'echo()' ancak Python3 ile kodlama yapıyorsanız **print()** sadece `print()` olarak yazılır. Python 2.x sürümlerinde `print` kullanımı da mevcuttur.

### 1.1 - Yorum Satırları

PHP ile yorum satırları şu şekilde gösterilir:

```php
<?php

// Bir yorum satırı
# Bu da yorum satırı

/*
  çok satırdan
  oluşan yorum
*/
```

Python'da ise yorum satırları iki şekilde gösterilir.

```python
# tek satırdan oluşan yorum bölümü
"""
çok satırdan
oluşan yorum
"""
```
Çok satırlı yorum kısmına ayrıca `docstring` de denir. İşlevlerde ve sınıflarda bu tarz docstring tanımlamalarına denk gelebilirsiniz.

### 1.2 - Değişkenler

PHP ile Python değişkenler tip almadan belirtilirler. Ancak PHP, Python'dan farklı olarak değişken tanımında `$` işaretini alır. Python'da ise değişken tanımlarken herhangi bir sembole ihtiyaç duyulmaz.

**index.php**

```php
<?php
    $degisken = "Bir değişken";
?>
```
Yukarıda değişken adının başına `$` dolar gelirken, ayrıca ifade sonuna noktalı virgül de geldi. Python ile tanımlama şöyle:

**main.py**

```python

degisken = "Bir değişken"
```

Python ile değişken tanımlamak bu kadar basittir. Herhangi bir sembol ya da noktalı virgül kuralı aranmaz.

### 1.3 - Sabitler

PHP'de sabitler, `const` ve `define()` ile yapılırken, Python'da böyle bir durum söz konusu değildir. Ancak sabitleri hatırlatır şekilde farklı dosyalarda tanımlamalar yapabilirsiniz.

**index.php**

```php
<?php

const SABIT = "Sabit";

define('BIR_SABIT', 'Sabit İçeriği');
```

Python'da ise durum tamamen farklıdır. Python için herhangi bir sabit tanımlama yoktur. Ancak sabit benzeri yapılar oluşturabiliriz:

**sabitler.py**

```python
SABIT = "Sabit"
BIR_SABIT = "Sabit İçeriği"
```

**main.py**

```python
from sabitler import *

print(SABIT)
```

Python dilinin yapısında sabitler olmasa da, sabit gibi davranan değiştirilemez yapılar da oluşturulabilir.

### 1.4 - Diziler

PHP'de dizileri `array()` işlevi ile ya da öğeleri tek tek belirterek tanımlayabiliriz. Bir örnek verecek olursak:

```php
<?php

$meyveler = array('elma', 'armut', 'kivi', 'portakal');

echo '<pre>';
print_r($meyveler);
echo '</pre>';

Array
(
    [0] => elma
    [1] => armut
    [2] => kivi
    [3] => portakal
)

```

Ayrıca `array()` işlevi olmadan el ile dizileri oluşturabiliriz:

```php
<?php

$meyveler[0] = "elma";
$meyveler[1] = "armut";
$meyveler[2] = "kivi";
$meyveler[3] = "portakal";

echo '<pre>';
print_r($meyveler);
echo '</pre>';

Array
(
    [0] => elma
    [1] => armut
    [2] => kivi
    [3] => portakal
)
```

Kısacası bu şekilde iki tanımı vardır. Python ise listeler ile dizi oluşturmaya destek verir. Örneğin klasik olarak bir liste oluşturalım:

```python

import pprint

meyveler = ['elma', 'armut', 'kivi', 'portakal']

pprint.pprint(meyveler)

repr(meyveler)
```

Yukarıda pprint kütüphanesini dosyaya dahil ettik. Bu kütüphanedeki `pprint()` işlevi, `print_r()` ile aynı görevi görmektedir. Yine bir alt satırdaki `repr()` işlevi de aynı görevi görür. Çıktıları PHP'deki gibi olmakta.

```python

# pprint()

['elma', 'armut', 'kivi', 'portakal']

# repr()

"['elma', 'armut', 'kivi', 'portakal']"
```

Python'da var olan bir diziye ekleme işlemini `append()` işlevi ile yaparız.

```python
meyveler.append("vişne")
```

---
**BURADA TUPLE'DAN BAHSEDİLEBİLİR**
---


### 1.5 - Veri Türleri

PHP ve Python'da değişkenleri tanımlarken verilerin tiplerini belirtmemize gerek yok. Ancak bazı durumlarda bu veri tiplerini bilmemiz gerekebilir. Python için bazı veri tipleri şunlardır:

---
PHP'deki veri tipleri de sıralanabilir.
---

**Numerik Tipler**

- int
- float
- long (Python 2.x için)
- complex

**Diğer Tipler**

- str
- byte (Yalnızca Python 3.x için)
- byte array (Yalnızca Python 3.x için)
- list
- tuple
- dict
- bool (True ya da False durumlarında)

---
**Dict tipinden bahsedilebilir.**
---


### 1.6 - Karar Yapıları

PHP'de ve Python'da karar yapıları farklı şekilde tanımlanır. Karar yapıları başlığı altında if-else kontrollerini anlatacağım.

PHP'de basit bir if tanımı şöyle yapılır:

```php
<?php

if (1 < 2) {
    echo "Küçük";
}

// ya da

if (1 < 2)
    echo "Tek satır ama bu";
```

Burada if tanımı yapıldığında kıvırcık/süslü parantezlerle kapattık. Python için buna gerek yok. Python'da kıvırcık/süslü parantezlerin yerini iki nokta üst üste kullanımı almakta.

```python

if 1 < 2:
    print("Küçük")
```

Bu kullanım PHP'nin tek satırlık if kullanımına benzese de genel tanım olarak böyledir. Birden fazla satır oluşturabiliriz. Örneğin şöyle:

```python

if 1 < 2:
    print("Küçük")
    print("Ve tek satır değil")
    print(2+2)

"""
ÇIKTI

K
V T S D
4
"""
```

aynı kullanımı PHP'de yapmaya kalkarsak hata alırız. Örneğin:

```php
<?php

if (1 < 2)
	echo "ok";
	echo "Noo";
	$i = "f";
	echo $i;
else
	echo "ok"

?>
```

---
**PHP'nin endif ile biten statement'ından bahsedilebilir.**
---

Bu PHP kodu hatalı bir PHP kodudur. Ayrıca diğer durumları da göz önüne alırsak:

Örneğin PHP'nin else ve else if durumlarını Python'da şöyle yaparız:

```python

if 1 < 2:
    print("Minik")
elif 2 > 1:
    print("Garip bir if-else")
else:
    print("Değişik")
```

Python'da else if, elif olarak kullanılır.

*Python'da switch-case deyimi yoktur.*

### 1.7 - Döngüler

PHP'de döngüler for, foreach, while, do-while iken, Python'da sadece for ve while döngüsü vardır. Örneğin PHP'de while döngüsünü şöyle düşünelim:

#### 1.7.1 - while Döngüsü

```php
<?php

$i = 0;

while ($i < 9) {
    echo $i;
    $i++;
}
```

Python'da ise aynı ifade şöyle tanımlanır:

```python

i = 0
while i < 9:
    print(i)
    i = i + 1
```

#### 1.7.2 - for Döngüsü

```php
<?php

for ($i=0; $i < 9; $i++) {
    echo $i;
}
```

Python bunu daha basit hale getirmiştir:

```python
for i in range(9):
    print(i)
```

Burada kullanılan `range()` işlevi, php'de for içindeki üç ifadenin tek işlev içine indirgenmiş halidir. Ayrıca Python'da listeleri yani dizileri çözümlemek de çok basittir.

```python
meyveler = ["elma", "armut", "kivi", "portakal"]

for m in meyveler:
	print(m)
```

Bu aslında Python'da olmayan ama PHP'de olan foreach gibi bir kullanımdır.

### 1.8 - Fonksiyonlar

PHP'de fonksiyonları erişim belirteçleri olmadan düşünürsek şöyle tanımlarız:

```php
function merhaba() {
    echo "Merhaba Dünya"
}
```

Python'da ise işlev yani fonksiyon tanımı şöyle olur:

```python
def merhaba():
    print("Merhaba Dünya")
```

Tıpkı if, elif, else, for, while gibi bunda da iki nokta üst üste tanımladıktan sonra bir `tab` şeklinde girintili olarak Python'da işlevler tanımlanır. Henüz Sınıfları anlatmamış olsam da eğer sınıf fonksiyonlarına sınırlama getirmek istiyorsak yani private olmasını istiyorsak __ (iki adet alt çizgi) kullanmamız gerekiyor. Örneğin:

```python
class Test:
	def merhaba(self):
		print("Merhaba Dünya")
	def __iceri(self):
		print("Merhaba İç Dünya")
	def icerisi(self):
		self.__iceri()

privT = Test()

privT.merhaba()
privT.icerisi()
```

Sınıfları şimdiden anlatmayacağım. PHP'de self bildiğiniz gibi Python'da da aynı işlemekte. Esas konumuza dönersek `__iceri()` işlevi sınıf içerisinde `self` öneki ile başlar ve adı ile çağırılabilir. Ancak dışarıda çağırmaya çalışırsak hata alırız:

Yukarıdaki örnek sınıfta, `icerisi()` işlevi ile private durumda olan `__iceri()` işlevini yazdırmış olduk. Eğer `privT.__iceri()` şeklinde çağırsaydık hata alacaktık. Fonksiyonlara parametre geçirme işlemi yine aynı PHP'deki gibidir.

```php
function merhaba($isim) {
    echo "Merhaba ".$isim;
}
```

Python'da ise şöyledir:

```python
def merhaba(isim):
    print("Merhaba", isim)

merhaba("Ali") # fonksiyon çağırı PHP ile aynıdır. Noktalı virgüle gerek yoktur.
```

Fonksiyonları değer döndürür hale getirebiliriz. PHP ve Python bu konuda benzedir.

```php
function topla($a, $b) {
    return $a+b;
}
```

Python'da ise şöyle değer döndürme yine aynı şekilde yapılır:

```python
def topla(a, b):
    return a+b

fonksiyon_degiskeni = topla(2,5) # değer döndüren fonksiyonun değişkene atanması

print(fonksiyon_degiskeni) # 7
```

### 1.9 - Sınıflar

Python'da sınıflar PHP ile hemen hemen aynı şekilde oluşturulurlar. Bu iki dilin sınıf yapısını karşılaştıracak olursak:

```php

class Sinif {
    public function merhaba() {
        echo "Merhaba Dünya";
    }
}

$a = new Sinif();

$a->merhaba();
```

Python'da ise bu sınıfın tanımlanması şöyle olur:

```python
class Sinif:
    def merhaba(self):
        print("Merhaba Dünya")

a = Sinif()

a.merhaba()
```

Python'da sınıfları türetirken `new` anahtar kelimesini kullanmazsınız. Ve sınıf işlevini çağırırken nokta ile belirtirsiniz. Ayrıca Python'da her oluşturduğunuz sınıfın bir `object` miras almasını önerirler. Örnek:

```python
class Sinif(object):
    def merhaba(self):
        print("Merhaba Dünya")
```

Bu kodun yukarıdakinden hiçbir farkı yok. Nesnelerde miras alma olayı PHP'de `extends` ile yapılırken, Python'da yukarıda gördüğümüz şekliyle yapılmakta.

```php

<?php

class Mesaj {

    public function Harika($mesaj) {
        return "$mesaj harika bir meyvedir.";
    }
}

class Meyve extends Mesaj {

}

$meyve = new Meyve();
echo $meyve->Harika("Elma");

?>
```
Yukarıdaki kodu Python için aynen şöyle yazarız:

```python
class Mesaj:
    def Harika(self, mesaj):
        return(mesaj+" harika bir meyvedir")

class Meyve(Mesaj):
    pass


meyve = Meyve()

print(meyve.Harika("Elma"))
```

Eğer çoklu miras alacak olsaydık şöyle yapardık:

```python

class Meyve(Mesaj, Uretim, Tukeyim, Falan, Filan):
    pass
```

O durumda miras alınmış olan sınıfın ilgili işlevini Meyve sınıfımız ile kullanabilirdik. Yukarıdaki Meyve ~ Mesaj sınıf örnekleri anlamsız dursa da PHP'de ve Python'da nasıl yapıldığını göstermek açısından belirttim.

# Yapılacaklar

- [ ] Dosya İşlemleri Anlatılacak
- [ ] PHP'de Olan Bazı Fonksiyonların Python'daki Karşılıkları Anlatılacak
- [ ] Python ile Web Programlama Üzerine Konular Anlatılacak (Frameworkler vs.)

# Katkı

Siz de bu repoya katkı yapabilirsiniz. Katkılarınızı esirgemeyin.

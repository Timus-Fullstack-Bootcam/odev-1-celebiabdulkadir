# Ödev-1


## 1. JavaScript Nedir ve Tarihsel Gelişimi
JavaScript, **web sayfalarını interaktif ve dinamik** hale getirmek için kullanılan bir programlama dilidir. Web geliştirmede önemli bir rol oynar ve çoğu modern web sayfasının temel bileşenlerinden biridir.
JavaScript'in gelişim süreci aşağıdaki gibi özetlenebilir:

- **1995**: Brendan Eich tarafından Netscape Navigator için geliştirildi ve ilk adı "LiveScript" idi.
- **1996**: Microsoft, Internet Explorer için JScript'i tanıttı.
- **1997**: JavaScript, ECMAScript adı altında bir standart haline geldi.
- **2000'ler**: AJAX kullanımıyla web uygulamaları daha interaktif hale geldi.
- **2009**: Node.js'in piyasaya sürülmesiyle JavaScript, sunucu tarafında da kullanılmaya başlandı.
- **2010 ve Sonrası**: Çeşitli JavaScript çerçeveleri ve kütüphaneleri (React, Angular, Vue.js gibi) geliştirilerek, modern web geliştirmenin temelini oluşturdu.

Bugün JavaScript, web tabanlı uygulamaların geliştirilmesinde en yaygın kullanılan dillerden biridir ve sürekli olarak gelişmekte olan bir ekosisteme sahiptir.
## 2. Java ile javascript arasındaki fark nedir
Java ve JavaScript, isim benzerliklerine rağmen oldukça farklı programlama dilleridir. Ana farkları şunlardır:

### Java

- **Kullanım Alanı**: Özellikle sunucu tarafı uygulamaları, Android mobil uygulamaları ve büyük ölçekli sistemler için kullanılır.
- **Dil Özellikleri**: Nesne yönelimli, sınıf tabanlı, statik tiplemeli bir dildir.
- **Çalışma Ortamı**: Java Virtual Machine (JVM) üzerinde çalışır ve platform bağımsızdır.
- **Sözdizimi**: C ve C++ dillerine benzer bir sözdizimi vardır.
- **Derleme Süreci**: Java kodları öncelikle bytecode'a derlenir ve sonra JVM üzerinde çalıştırılır.

### JavaScript

- **Kullanım Alanı**: Web sayfalarını interaktif ve dinamik hale getirmek için kullanılır. Sunucu tarafında (Node.js ile) da kullanılabilir.
- **Dil Özellikleri**: Nesne tabanlı, prototip tabanlı, dinamik tiplemeli bir dildir.
- **Çalışma Ortamı**: Çoğunlukla web tarayıcıları üzerinde çalışır.
- **Sözdizimi**: Daha esnek ve web geliştirme için optimize edilmiş bir sözdizimi vardır.
- **Yorumlanma Süreci**: JavaScript kodları doğrudan tarayıcı tarafından yorumlanır.

Her iki dil de kendi alanlarında güçlü ve yaygın olarak kullanılan dillerdir, ancak amaç ve kullanım alanları oldukça farklıdır.
## 3. Javascript teki veri tipleri nelerdir açıklayınız
JavaScript, farklı veri tiplerini destekler ve bunlar genellikle iki ana kategoriye ayrılır: İlkel (Primitive) ve Referans (Reference) tipleri.

### İlkel Tipler

#### `string`
- Metin verilerini temsil eder.
- Örnek: `"Merhaba Dünya!"`

#### `number`
- Hem tam sayıları hem de kayan noktalı sayıları temsil eder.
- Örnek: `42`, `3.14`

#### `boolean`
- Mantıksal doğru (`true`) veya yanlış (`false`) değerlerini temsil eder.
- Örnek: `true`, `false`

#### `undefined`
- Değişkenin değerinin atanmadığını gösterir.
- Otomatik olarak atanır; özellikle tanımlanmasına gerek yoktur.

#### `null`
- Hiçbir değeri temsil etmez ve bir değişkene bilinçli olarak atanır.
- Boş veya var olmayan bir değere işaret eder.

#### `bigint`
- Çok büyük tam sayıları temsil etmek için kullanılır.
- Örnek: `9007199254740991n`

#### `symbol`
- Benzersiz ve değiştirilemez bir değer üretir.
- Özellikle nesne özelliklerini benzersiz bir şekilde tanımlamak için kullanılır.

### Referans Tipleri

#### `object`
- Nesneler, dizi (array), fonksiyonlar ve diğer yapılar dahil olmak üzere daha karmaşık veri yapılarını temsil eder.
- Örnek: `{ ad: "Ali", yas: 30 }`, `[1, 2, 3]`

### Özel Durumlar

- `typeof` operatörü, veri tiplerini belirlemek için kullanılır.
- `null`'ün `typeof` değeri `object`tir, bu tarihsel bir JavaScript hatasıdır.

JavaScript, dinamik tiplemeli bir dil olduğu için, değişkenlerin veri tipleri çalışma zamanında değişebilir.
## 4. null ile undefined arasıdaki fark nedir açıklayınız
### `undefined`
- Değer atanmamış değişkenler için varsayılan değer.
- Örnek: `let a;` (a `undefined` olarak atanır)

### `null`
- Bilinçli olarak hiçbir değere sahip olmayan bir değişkeni temsil eder.
- Örnek: `let a = null;` (a'ya `null` atanır)

### Anahtar Farklar
- `undefined` genellikle sistem tarafından atanır.
- `null` programcı tarafından atanır.
- `typeof undefined` → `"undefined"`
- `typeof null` → `"object"`
- Eşitlik kontrolü: `null == undefined` → `true`, ancak `null === undefined` → `false`


## 5. NaN nedir açıklayınız
`NaN`, JavaScript'te "Sayı Olmayan" anlamına gelen özel bir ilkel veri tipidir.

### Özellikleri
- Sayısal olmayan bir işlemin sonucunda ortaya çıkar.
- Örnek: Bir sayı ile bir metni toplamak (`"abc" + 5`).
- `typeof NaN` → `"number"`, ironik bir şekilde `NaN`'ın türü sayı olarak kabul edilir.

### Kontrol
- `NaN` kendisiyle bile eşit değildir: `NaN === NaN` → `false`.
- Bir değerin `NaN` olup olmadığını kontrol etmek için `isNaN()` fonksiyonu kullanılır.

### Kullanım Senaryoları
- Geçersiz veya tanımlanamayan matematiksel işlemlerde ortaya çıkar.
- Örnek: `0/0`, `Math.sqrt(-1)`, `parseInt("abc")`.

`NaN`, hatalı veya tanımsız matematiksel işlemlerin bir sonucu olarak JavaScript tarafından kullanılır ve genellikle hata ayıklamada önemli bir işaretçidir.

## 6. Javascript’te yorum satırı eklemenin kaç farklı yolu vardır
### Tek Satır Yorum
- `//` kullanılır.
- Örnek: `// Bu bir tek satır yorumudur.`

### Çok Satırlı Yorum
- `/*` ile başlar ve `*/` ile biter.
- Örnek: `/* Bu bir çok satırlı yorumdur. */`

Yorumlar, kodun anlaşılabilirliğini artırmak için kullanılır.

## 7. Global değişken ne demektir açıklayınız

Global değişken, JavaScript kodunun herhangi bir yerinden erişilebilen ve tüm fonksiyonlar veya kod blokları tarafından paylaşılan bir değişkendir.

### Özellikleri
- Kodun en üst düzeyinde tanımlanır, herhangi bir fonksiyon veya blok dışında.
- Tüm fonksiyonlar ve kod blokları tarafından okunabilir ve değiştirilebilir.
- Örnek: 
  ```javascript
  var globalDegisken = "Merhaba Dünya!";
  ```
### Dikkat Edilmesi Gerekenler
Global değişkenler, yan etkilere ve istenmeyen değişikliklere sebep olabilirler.
Kod karmaşıklığını artırabilir ve hata bulmayı zorlaştırabilirler.
Mümkün olduğunca sınırlı kullanımı önerilir ve yerel değişkenler tercih edilir.
Global değişkenlerin kullanımı, kodun yönetilebilirliği ve bakımı açısından dikkatli ele alınmalıdır.

## 8. Javascript’te this anahtar kelimesi nedir açıklayınız

`this`, JavaScript'te mevcut yürütme bağlamının bir referansını temsil eder.

### Kullanımı
- **Global Bağlam**: Global düzeyde `this`, global nesneyi (tarayıcılarda `window`, Node.js'te `global`) ifade eder.
- **Nesne Metodu**: Bir nesnenin metodunda `this`, o nesneyi gösterir.
- **Fonksiyon Bağlamı**: Normal fonksiyonlarda, `this` çağrıldığı bağlama göre değişir. Ok fonksiyonlarında (`=>`) ise, `this`, tanımlandığı bağlamın `this` değerini korur.

### Örnek
```javascript
const obje = {
  isim: "Ali",
  selamVer: function() {
    return `Merhaba, ben ${this.isim}`;
  }
};
console.log(obje.selamVer()); // "Merhaba, ben Ali"
```

## 9. == ile === farkını örnekler ile açıklayınız


JavaScript'te `==` ve `===` operatörleri, eşitlik kontrolü yapar ancak farklı yollarla çalışır.

### `==` (Eşitlik Operatörü)
- Değerleri karşılaştırırken tür dönüşümü yapar.
- Farklı türdeki değerler karşılaştırılırken, önce aynı türe dönüştürülür, sonra karşılaştırılır.
- Örnekler:
  - `"5" == 5` → `true` (String "5" sayıya dönüştürülerek karşılaştırılır)
  - `0 == false` → `true` (0 ve `false` aynı türdeymiş gibi değerlendirilir)

### `===` (Katı Eşitlik Operatörü)
- Hem değerleri hem de türlerini karşılaştırır.
- Eğer karşılaştırılan değerlerin türleri farklıysa, doğrudan `false` döner.
- Örnekler:
  - `"5" === 5` → `false` (Farklı türler, eşit değil)
  - `0 === false` → `false` (Farklı türler, eşit değil)

### Öneri
- Genellikle `===` kullanımı daha güvenilirdir çünkü beklenmeyen tür dönüşümlerini önler.

Bu operatörler, JavaScript'te değer karşılaştırmalarında önemli rol oynar ve doğru kullanımı kodun güvenilirliğini artırır.

## 10. let var const farkını tablo yapınız

| Özellik          | `var`                    | `let`                    | `const`                  |
|------------------|--------------------------|--------------------------|--------------------------|
| Kapsam (Scope)   | Fonksiyon kapsamlı       | Blok kapsamlı            | Blok kapsamlı            |
| Yeniden Tanımlama| İzin verir               | İzin vermez              | İzin vermez              |
| Yeniden Atama    | İzin verir               | İzin verir               | İzin vermez              |
| Başlangıç Değeri | `undefined` ile başlar   | Başlangıç değeri gerekli | Başlangıç değeri gerekli |
| Kaldırma (Hoisting) | Var, tanım öncesi erişilebilir | Kısmen, tanımlama öncesi hata verir | Kısmen, tanımlama öncesi hata verir |

### Özet
- `var`: Eski JavaScript'te değişken tanımlamak için kullanılır. Fonksiyon kapsamlıdır ve aynı değişkeni yeniden tanımlamaya izin verir.
- `let`: ES6 ile gelen, blok kapsamlı değişken tanımlama. Yeniden tanımlamaya izin vermez, ancak değeri değiştirilebilir.
- `const`: Sabit değerler için kullanılır. Blok kapsamlıdır ve hem yeniden tanımlamaya hem de değer değiştirmeye izin vermez.

## 11. Arrow fonksiyonun normal fonksiyondan farkları nelerdir
Arrow fonksiyonları (`=>`), JavaScript'te ES6 ile tanıtılan, normal fonksiyonlara alternatif bir yazım sunar.

### Sözdizimi Farkları
- **Arrow Fonksiyonları**: Daha kısa ve sade bir sözdizimi sağlar.
  - Örnek: `const topla = (a, b) => a + b;`
- **Normal Fonksiyonlar**: Geleneksel fonksiyon tanımlama yöntemi.
  - Örnek: `function topla(a, b) { return a + b; }`

### `this` Değerinin Kullanımı
- **Arrow Fonksiyonları**: `this` değeri, fonksiyonun tanımlandığı bağlamın `this` değerini alır (Lexical `this`).
- **Normal Fonksiyonlar**: `this` değeri, fonksiyonun nasıl çağrıldığına bağlıdır.

### Constructor Olarak Kullanım
- **Arrow Fonksiyonları**: Constructor olarak kullanılamazlar, `new` anahtar sözcüğü ile kullanılamazlar.
- **Normal Fonksiyonlar**: Constructor fonksiyonlar olarak kullanılabilirler.

### arguments Nesnesi
- **Arrow Fonksiyonları**: `arguments` nesnesine erişimi yoktur.
- **Normal Fonksiyonlar**: `arguments` nesnesi üzerinden tüm parametrelere erişilebilir.

Arrow fonksiyonları, genellikle daha kısa ve okunabilir kod yazımı için tercih edilirken, `this` bağlamı ve constructor özellikleri gerektiğinde geleneksel fonksiyonlar tercih edilir.

## 12. switch bloğu içinde hatasız nasıl değişken tanımlanır

`switch` bloğu içinde değişken tanımlarken, her `case` veya `default` bölümünü ayrı bir blok olarak düşünmek ve `let` veya `const` kullanmak önemlidir.

### Örnek
```javascript
switch (deger) {
  case 1: {
    let sonuc = "Bir";
    console.log(sonuc);
    break;
  }
  case 2: {
    let sonuc = "İki"; // Aynı isimli değişken, farklı blokta tanımlandığı için sorun çıkarmaz.
    console.log(sonuc);
    break;
  }
  default: {
    let sonuc = "Diğer";
    console.log(sonuc);
  }
}
```

## 13. Pure fonksiyon ne demektir açıklayınız

Bir fonksiyonun "pure" (saf) olması için aşağıdaki iki temel özelliği taşıması gerekir:

1. **Aynı Girdilerle Aynı Çıktıları Üretir**: Pure fonksiyon, aynı girdi (parametre) değerleriyle her zaman aynı çıktıyı verir. Fonksiyonun sonucu yalnızca girdilerine bağlıdır ve dış etkenlerden etkilenmez.

2. **Yan Etki Yoktur (Side Effect-Free)**: Fonksiyon, dış dünyadaki hiçbir şeyi değiştirmez (global değişkenler, I/O işlemleri vb.) ve dış dünyadan etkilenmez. Yani, herhangi bir durum değişikliği yapmaz veya dış kaynaklardan veri almaz.

### Örnek
```javascript
function topla(a, b) {
  return a + b;
}
```

## 14. Rest operatör nedir örnekle açıklayınız

Rest operatörü (`...`), fonksiyonlara geçirilen birden fazla bağımsız değişkeni (argüman) bir dizi olarak ele almak için kullanılır.

### Özellikleri
- Fonksiyonlarda, belirsiz sayıda argümanı bir diziye dönüştürür.
- Genellikle son parametre olarak kullanılır.
- Fonksiyon içinde argümanlar üzerinde döngü yapmayı ve işlem yapmayı kolaylaştırır.

### Örnek
```javascript
function topla(...sayilar) {
  return sayilar.reduce((toplam, deger) => toplam + deger, 0);
}
console.log(topla(1, 2, 3)); // 6
```

## 15. Object destructuring nedir örnekle açıklayınız

Object destructuring, bir nesnenin özelliklerini, daha küçük parçalara ayırmak ve bu özellikleri değişkenlere atamak için kullanılır.

### Özellikleri
- Nesnelerden bir veya daha fazla özelliği, değişkenlere doğrudan atamayı sağlar.
- Kodun daha temiz ve okunabilir olmasına yardımcı olur.
- Özellikler, belirtilen isimlerle değişkenlere atanır.

### Örnek
```javascript
const kisi = {
  isim: "Ahmet",
  yas: 30,
  meslek: "Mühendis"
};
const { isim, yas } = kisi;
console.log(isim); // "Ahmet"
console.log(yas);  // 30 
```

## 16. 2 elemanlı bir objeyi 6 farklı şekilde oluşturunuz

```javascript
const obje1 = { isim: "Ahmet", yas: 30 };
const obje2 = new Object();
obje2.isim = "Ahmet";
obje2.yas = 30;```
const prototip = { isim: "Ahmet", yas: 30 };
const obje3 = Object.create(prototip);
const obje4 = {};
obje4['isim'] = "Ahmet";
obje4['yas'] = 30;
function olusturObjeyi(isim, yas) {
  return { isim, yas };
}
const obje5 = olusturObjeyi("Ahmet", 30);
class Kisi {
  constructor(isim, yas) {
    this.isim = isim;
    this.yas = yas;
  }
}
const obje6 = new Kisi("Ahmet", 30);
```
## 17. 2 elemanlı bir objenin key ve value değerlerinin karakter sayısı ile 2 farklı döngü methodu kullanarak yeni bir obje oluşturunuz
```javascript
const obje = { isim: "Ahmet", meslek: "Mühendis" };

for (const key in obje) {
  if (obje.hasOwnProperty(key)) {
    const keyUzunluk = key.length;
    const valueUzunluk = obje[key].length;
    console.log(`${key}: Anahtar Uzunluğu = ${keyUzunluk}, Değer Uzunluğu = ${valueUzunluk}`);
  }
}

const obje = { isim: "Ahmet", meslek: "Mühendis" };

Object.keys(obje).forEach(key => {
  const keyUzunluk = key.length;
  const valueUzunluk = obje[key].length;
  console.log(`${key}: Anahtar Uzunluğu = ${keyUzunluk}, Değer Uzunluğu = ${valueUzunluk}`);
});
```

## 18. Cookie, local storage ve session storage farkını tablo yapınız


| Özellik                      | Cookie              | Local Storage      | Session Storage    |
|------------------------------|---------------------|--------------------|--------------------|
| Süreklilik                   | Sunucu tarafından belirlenir | Tarayıcı kapatılana kadar kalıcı | Tarayıcı oturumu kapandığında silinir |
| Kapasite                     | Her domain için yaklaşık 4KB | Her domain için yaklaşık 5MB | Her domain için yaklaşık 5MB |
| Erişilebilirlik               | Tüm pencereler/sekmeleler | Aynı pencere/sekmede | Aynı pencere/sekmede |
| Sunucu İle Paylaşılıp Paylaşılmaması | Her HTTP isteğiyle sunucuya gönderilir | Yalnızca istemci tarafında | Yalnızca istemci tarafında |
| Güvenlik                      | Daha az güvenli, XSS ve CSRF'ye karşı savunmasız | Daha güvenli, XSS'e karşı savunmasız | Daha güvenli, XSS'e karşı savunmasız |
| Kullanım Alanları             | Oturum yönetimi, kullanıcı takibi | Geniş veri depolama, kullanıcı tercihleri | Geçici bilgi depolama, oturum bilgileri |

### Özet
- **Cookie**: Oturum yönetimi ve kullanıcı takibi için idealdir. Her HTTP isteği ile sunucuya gönderilir.
- **Local Storage**: Tarayıcı kapansa bile verileri saklar. Genellikle büyük miktarda veri depolama ve kullanıcı tercihlerinin saklanması için kullanılır.
- **Session Storage**: Tarayıcı oturumu boyunca veri saklar ve oturum kapandığında veriler silinir. Oturumla ilgili geçici bilgilerin saklanması için uygundur.

## 19. asenkron ve senkron işlem farkı nedir

| Özellik                 | Senkron İşlem                         | Asenkron İşlem                          |
|-------------------------|---------------------------------------|-----------------------------------------|
| İşleyiş                 | Adım adım sırayla işler. Bir işlem bitmeden diğerine geçilmez. | Birden fazla işlem aynı anda yürütülebilir. Bir işlemin tamamlanmasını beklemeden diğer işlemler devam eder. |
| Bloklama                | İşlem sürerken diğer işlemler bloke olur. | İşlem sürerken diğer işlemler bloke olmaz, arka planda çalışmaya devam eder. |
| Örnekler                | Döngüler, koşullar, senkron fonksiyon çağrıları. | `setTimeout`, `fetch` API istekleri, Promises, async/await. |
| Kullanım Senaryoları    | Hızlı ve az kaynak gerektiren işlemlerde kullanılır. | Ağ istekleri, dosya okuma/yazma gibi zaman alabilecek işlemlerde kullanılır. |
| JavaScript Uygulaması   | JavaScript tek iş parçacıklıdır ve varsayılan olarak senkron çalışır. | Callback fonksiyonları, Promises, async/await ile asenkron işlemler gerçekleştirilir. |

### Özet
- **Senkron İşlem**: Adım adım sırasıyla çalışır, bir işlem bitmeden diğerine geçilmez. Basit ve hızlı işlemler için idealdir.
- **Asenkron İşlem**: İşlemler birbirinden bağımsız yürütülür ve bir işlemin tamamlanmasını beklemeden diğer işlemlere devam edilir. Zaman alabilecek işlemler için tercih edilir.

## 20. Promise nedir ve neden ihtiyaç duyarız

Promise, JavaScript'te asenkron işlemlerin sonuçlarını temsil eden bir nesnedir.

### Temel Özellikleri
- **Asenkron İşlemler için**: Ağ istekleri, dosya okuma/yazma gibi zaman alıcı işlemleri temsil eder.
- **Durumlar**: `pending` (beklemede), `fulfilled` (başarıyla tamamlandı), `rejected` (hata ile sonuçlandı).
- **Sonuç**: Başarılı sonuçlar `resolve` ile, hatalar `reject` ile döndürülür.

### Neden İhtiyaç Duyarız?
- **Callback Cehenneminden Kaçınmak**: Callback'lerin iç içe geçmesiyle oluşan karmaşık yapıları engeller.
- **Daha Temiz Kod**: Zincirleme (`then`, `catch`, `finally`) ile daha okunabilir ve yönetilebilir kod yazmamızı sağlar.
- **Hata Yönetimi**: Hataları yakalamak ve işlemek için düzenli bir yol sunar.
- **Kontrollü Asenkron Akış**: Birden fazla asenkron işlemi sıralı veya paralel olarak kontrol etmeyi kolaylaştırır.

### Örnek
```javascript
const veriAl = new Promise((resolve, reject) => {
  // Asenkron işlem (örneğin, ağ isteği)
  if (/* işlem başarılı */) {
    resolve("Veri alındı");
  } else {
    reject("Hata oluştu");
  }
});
veriAl
  .then(veri => console.log(veri))
  .catch(hata => console.error(hata));
  ```

## Array Soruları ve Çözümleri

### Ödev 2: `dolap` Array İşlemleri

```javascript
var dolap = ["Shirt", "Pant", "TShirt"];

// 1. Dolap arrayindeki son elemanı silip consola yazdırın
var sonEleman = dolap.pop();
console.log(sonEleman); // TShirt

// 2. Dolap arrayindeki ilk elamanı silip yerine “Hat” elemanını gönderip consola yazdırın
var ilkEleman = dolap.shift();
dolap.unshift("Hat");
console.log(dolap); // ["Hat", "Pant"]

// 3. Dolap değişkeninin array olup olmadığını kontrol edin ve sonucu bir değişkene eşitleyin
var isArray = Array.isArray(dolap);
console.log(isArray); // true

// 4. Dolap arrayinde “Pant” elemanın olup olmadığını 3 farklı method ile kontrol edin
console.log(dolap.includes("Pant")); // true
console.log(dolap.indexOf("Pant") !== -1); // true
console.log(dolap.find(eleman => eleman === "Pant") !== undefined); // true

// 5. Dolap arrayindeki elemanların karakter sayısını toplayıp geriye döndürecek fonksiyonu yazın
function karakterSayisiToplami(array) {
  return array.reduce((toplam, eleman) => toplam + eleman.length, 0);
}
console.log(karakterSayisiToplami(dolap)); // 7 (Hat ve Pant)

// 6. Dolap arrayindki tüm elemanları büyük harfe çevirip yeni bir değişkene 3 farklı yöntemle atayın
var buyukHarfler1 = dolap.map(eleman => eleman.toUpperCase());
console.log(buyukHarfler1); // ["HAT", "PANT"]

var buyukHarfler2 = [];
for (var i = 0; i < dolap.length; i++) {
  buyukHarfler2.push(dolap[i].toUpperCase());
}
console.log(buyukHarfler2); // ["HAT", "PANT"]

var buyukHarfler3 = [];
dolap.forEach(eleman => {
  buyukHarfler3.push(eleman.toUpperCase());
});
console.log(buyukHarfler3); // ["HAT", "PANT"]

// 7. Dolap arrayini index sayıları key olacak şekilde objeye çeviriniz
var dolapObjesi = {};
dolap.forEach((eleman, index) => {
  dolapObjesi[index] = eleman;
});
console.log(dolapObjesi); // {0: "Hat", 1: "Pant"}

// 8. Slice ile Splice Farkı Nedir
// slice: Arrayin belirli bir bölümünü kopyalar ve yeni bir array döndürür. Orijinal arrayi değiştirmez.
// splice: Arrayin belirli bir bölümünü kaldırır veya yeni elemanlar ekler. Orijinal arrayi değiştirir.
```


```javascript
const arr = [1, 2, 3, 4, 5, 6, 7, 7, 8, 6, 10];

// 1. Arrayindeki yinelenen sayıları bulun
const yinelenenler = arr.filter((value, index, self) => self.indexOf(value) !== index && self.lastIndexOf(value) === index);
console.log(yinelenenler); // [7, 6]

// 2. Arrayindeki tüm yinelenen sayıları silip yeni bir arrayi 2 farklı method ile oluşturun
var unique1 = [...new Set(arr)];
console.log(unique1); // [1, 2, 3, 4, 5, 6, 7, 8, 10]

var unique2 = arr.filter((value, index, self) => self.indexOf(value) === index);
console.log(unique2); // [1, 2, 3, 4, 5, 6, 7, 8, 10]

// 3. Arrayindeki en yüksek ve en düşük değeri 2 farklı methodla bulun
var enYuksek = Math.max(...arr);
var enDusuk = Math.min(...arr);
console.log(`En yüksek: ${enYuksek}, En düşük: ${enDusuk}`); // En yüksek: 10, En düşük: 1

var siraliArr = arr.slice().sort((a, b) => a - b);
console.log(`En yüksek: ${siraliArr[siraliArr.length - 1]}, En düşük: ${siraliArr[0]}`); // En yüksek: 10, En düşük: 1
```



##### Bu kodun çıktısı nedir neden ?
```javascript
function job() {
    return new Promise(function(resolve, reject) {
        reject();
    });
}

let promise = job();

promise.then(function() {
    console.log('Success 1');
}).then(function() {
    console.log('Success 2');
})
.then(function() {
    console.log('Success 3');
})
.catch(function() {
    console.log('Error 1');
}).then(function() {
    console.log('Success 4');
});

Çıktı:

Error 1
Success 4

```
### Promise Çıktı Analizi

Verilen JavaScript kodunun çıktısını adım adım analiz edelim:

```javascript
function job(state) {
    return new Promise(function(resolve, reject) {
        if (state) {
            resolve('success');
        } else {
            reject('error');
        }
    });
}

let promise = job(true);

promise
.then(function(data) {
    console.log(data); // success
    return job(true);
})
.then(function(data) {
    if (data !== 'victory') {
        throw 'Defeat';
    }
    return job(true);
})
.then(function(data) {
    console.log(data);
})
.catch(function(error) {
    console.log(error); // Defeat
    return job(false);
})
.then(function(data) {
    console.log(data);
    return job(true);
})
.catch(function(error) {
    console.log(error); // error
    return 'Error caught';
})
.then(function(data) {
    console.log(data); // Error caught
    return new Error('test');
})
.then(function(data) {
    console.log('Success:', data.message); // Success: test
})
.catch(function(data) {
    console.log('Error:', data.message);
})
Çıktı:

success
Defeat
error
Error caught
Success: test


```
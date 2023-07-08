# Python Pandas Dersleri

- [Python Pandas Dersleri](#python-pandas-dersleri)
- [1. Pandas Nedir?](#1-pandas-nedir)
- [2. Pandas Kütüphanesini Yükleme ve Çağırma](#2-pandas-kütüphanesini-yükleme-ve-çağırma)
  - [2.1. Yükleme](#21-yükleme)
  - [2.2. Çağırma](#22-çağırma)
- [3. Veri Setini Tanıma, Veri Setinin İçeri Aktarılması ve İncelenmesi](#3-veri-setini-tanıma-veri-setinin-i̇çeri-aktarılması-ve-i̇ncelenmesi)
  - [3.1. Tanıma](#31-tanıma)
  - [3.2. İçeri Aktarma](#32-i̇çeri-aktarma)
  - [3.3. Baştaki Verileri Yazdırma: head()](#33-baştaki-verileri-yazdırma-head)
  - [3.4. Sondaki Verileri Yazdırma: tail()](#34-sondaki-verileri-yazdırma-tail)
  - [3.5. Satır ve Sütun Sayısı Bilgisi Alma: shape](#35-satır-ve-sütun-sayısı-bilgisi-alma-shape)
  - [3.6. Veri Seti Hakkında Detaylı Bilgi Alma: info()](#36-veri-seti-hakkında-detaylı-bilgi-alma-info)
  - [3.7. Sütun ve Satır Gösterimi Ayarları: pd.set\_option()](#37-sütun-ve-satır-gösterimi-ayarları-pdset_option)
- [4. Pandas Series ve Pandas DataFrame Kavramları](#4-pandas-series-ve-pandas-dataframe-kavramları)
  - [4.1. Series](#41-series)
  - [4.2. DataFrame](#42-dataframe)
    - [4.2.1. Sütunlara Erişme](#421-sütunlara-erişme)
      - [4.2.1.1. Tekli Erişim](#4211-tekli-erişim)
      - [4.2.1.2. Çoklu Erişim](#4212-çoklu-erişim)
    - [4.2.2. Satırlara Erişme: iloc ve loc](#422-satırlara-erişme-iloc-ve-loc)
      - [4.2.2.1. iloc](#4221-iloc)
      - [4.2.2.2. loc](#4222-loc)
    - [4.2.3. Satır ve Sütunlara Erişme: İki Nokta Kullanımı](#423-satır-ve-sütunlara-erişme-i̇ki-nokta-kullanımı)
    - [4.2.4. Sütuna Ait Değerleri Saydırma: value\_counts()](#424-sütuna-ait-değerleri-saydırma-value_counts)
- [5. İndeksler](#5-i̇ndeksler)
  - [5.1. İndeks nedir?](#51-i̇ndeks-nedir)
  - [5.2. İndeks Ayarlama: set\_index() ve index\_col](#52-i̇ndeks-ayarlama-set_index-ve-index_col)
  - [5.3. İndeks Aracılığıyla Erişim: loc](#53-i̇ndeks-aracılığıyla-erişim-loc)
  - [5.4. İndeks Sıfırlama: reset\_index()](#54-i̇ndeks-sıfırlama-reset_index)
  - [5.5. İndekslerin Sıralanması: sort\_index()](#55-i̇ndekslerin-sıralanması-sort_index)
- [6. Filtreleme](#6-filtreleme)
  - [6.1. Tekli Filtreleme: İç içe ve loc](#61-tekli-filtreleme-i̇ç-içe-ve-loc)
  - [6.2. Çoklu Filtreleme: \&, | ve isin()](#62-çoklu-filtreleme---ve-isin)
  - [6.3. String İçerenleri Filtreleme: str.contains()](#63-string-i̇çerenleri-filtreleme-strcontains)
- [7. Sütun ve Satır Güncelleme](#7-sütun-ve-satır-güncelleme)
  - [7.1. Sütun Güncelleme: columns, List Comprehension, str.replace(), rename](#71-sütun-güncelleme-columns-list-comprehension-strreplace-rename)
  - [7.2. Satır Güncelleme: loc, at, str.lower(), apply(), applymap(), lambda, map() ve replace()](#72-satır-güncelleme-loc-at-strlower-apply-applymap-lambda-map-ve-replace)
- [8. Sütun ve Satır Ekleme ve Kaldırma](#8-sütun-ve-satır-ekleme-ve-kaldırma)
  - [8.1. Sütun Ekleme ve Kaldırma: str.split() ve drop()](#81-sütun-ekleme-ve-kaldırma-strsplit-ve-drop)
  - [8.2. Satır Ekleme ve Kaldırma: append(), concat() ve drop()](#82-satır-ekleme-ve-kaldırma-append-concat-ve-drop)
- [9. Sıralama](#9-sıralama)
  - [9.1. Tekli Sıralama: sort\_values()](#91-tekli-sıralama-sort_values)
  - [9.2. Çoklu Sıralama: sort\_values()](#92-çoklu-sıralama-sort_values)
  - [9.3. İndekse Göre Sıralama: sort\_index()](#93-i̇ndekse-göre-sıralama-sort_index)
  - [9.4. Serilerin Sıralanması: sort\_values()](#94-serilerin-sıralanması-sort_values)
  - [9.5. En Büyüklerin Sıralanması: nlargest()](#95-en-büyüklerin-sıralanması-nlargest)
  - [9.6. En Küçüklerin Sıralanması: nsmallest()](#96-en-küçüklerin-sıralanması-nsmallest)
- [10. Gruplama ve Özetleme](#10-gruplama-ve-özetleme)
  - [10.1. Tekli Sütunun Bir İstatistik Değeri: median()](#101-tekli-sütunun-bir-i̇statistik-değeri-median)
  - [10.2. Çoklu Sütunların Bir İstatistik Değeri: median()](#102-çoklu-sütunların-bir-i̇statistik-değeri-median)
  - [10.3. İstatistiksel Özet: describe()](#103-i̇statistiksel-özet-describe)
  - [10.4. Değerlerin Saydırılması: value\_counts()](#104-değerlerin-saydırılması-value_counts)
  - [10.5. Değerlerin Yüzdelere Ayrılması: normalize](#105-değerlerin-yüzdelere-ayrılması-normalize)
  - [10.6. Gruplayarak Saydırma, Yüzde Alma ve İndeks İnceleme: groupby(), value\_counts(), normalize ve loc](#106-gruplayarak-saydırma-yüzde-alma-ve-i̇ndeks-i̇nceleme-groupby-value_counts-normalize-ve-loc)
  - [10.7. Bir Gruba Göre Bir İstatistik: groupby() ve median()](#107-bir-gruba-göre-bir-i̇statistik-groupby-ve-median)
  - [10.8. Bir Gruba Göre Birden Fazla İstatistik: groupby(), agg(), median() ve std()](#108-bir-gruba-göre-birden-fazla-i̇statistik-groupby-agg-median-ve-std)
  - [10.9. Bir String İçeriğine Göre Bir İstatistik: groupby(), apply(), lambda, str.contains() ve sum()](#109-bir-string-i̇çeriğine-göre-bir-i̇statistik-groupby-apply-lambda-strcontains-ve-sum)
- [11. Kayıp Veri](#11-kayıp-veri)
  - [11.1. NaN Sayısını Öğrenme: isna() ve sum()](#111-nan-sayısını-öğrenme-isna-ve-sum)
  - [11.2. NaN ve Temizliği: dropna()](#112-nan-ve-temizliği-dropna)
  - [11.3. Kayıp Veriyi Anlatan Manuel Girilmiş String İfadeleri NaN Yapma: replace()](#113-kayıp-veriyi-anlatan-manuel-girilmiş-string-i̇fadeleri-nan-yapma-replace)
  - [11.4. NaN Değerleri String Bir İfadeye Çevirme: fillna()](#114-nan-değerleri-string-bir-i̇fadeye-çevirme-fillna)
  - [11.5. NaN Değerleri Bir Önceki Değere Çevirme: fillna()](#115-nan-değerleri-bir-önceki-değere-çevirme-fillna)
  - [11.6. NaN Değerleri Bir Sonraki Değere Çevirme: fillna()](#116-nan-değerleri-bir-sonraki-değere-çevirme-fillna)
  - [11.7. NaN Değerleri Bir İstatistik Değerine Çevirme: fillna() ve mean()](#117-nan-değerleri-bir-i̇statistik-değerine-çevirme-fillna-ve-mean)
  - [11.8. NaN Değerlerinin Interpolasyon Tahmini: fillna() ve interpolate()](#118-nan-değerlerinin-interpolasyon-tahmini-fillna-ve-interpolate)
- [12. Verilerin Dışarı Aktarılması](#12-verilerin-dışarı-aktarılması)
  - [12.1. CSV: to\_csv()](#121-csv-to_csv)
  - [12.2. XLSX: to\_excel()](#122-xlsx-to_excel)

# 1. Pandas Nedir?

---

Pandas, Python programlama dilinin üzerine inşa edilmiş hızlı, güçlü, esnek ve kullanımı kolay bir açık kaynak veri analizi ve manipülasyonu aracıdır.

# 2. Pandas Kütüphanesini Yükleme ve Çağırma

---

## 2.1. Yükleme

Pandas'ı yüklemek için, Python paket yöneticisi olan `pip`'i kullanabiliriz. Komut, aşağıdaki platformlarda çalıştırılabilir:

* Windows: Komut İstemi (Command Prompt, Cmd) veya PowerShell
* Linux: Terminal
* macOS: Terminal

Cmd kullanarak anlatacağım.

```
pip install pandas
```

Versiyon bilgisi yine Cmd'den aşağıdaki gibi öğrenilebilir.

```
python
import pandas as pd
pd.__version__
```

Bu dersin ilk paylaşımında `1.5.2` versiyonu kullanılıyor olacak.

## 2.2. Çağırma

Pandas başarıyla yüklendikten sonra aşağıdaki ifadeyi ekleyerek kütüphaneyi çağırabiliriz.

```python
import pandas as pd
```

`pd` kısaltmasını kullanmak yaygın bir uygulamadır ancak kısaltma isteğe bağlı olarak değiştirilebilir.

# 3. Veri Setini Tanıma, Veri Setinin İçeri Aktarılması ve İncelenmesi

---

## 3.1. Tanıma

Ders anlatımında, İş Yatırım'ın Hisse Değerleri ve Oranları bölümünde bulunan Özet isimli tabloyu kullanacağız. Verilere [buradan](https://www.isyatirim.com.tr/tr-tr/analiz/hisse/Sayfalar/Temel-Degerler-Ve-Oranlar.aspx#page-1) ulaşabilir ve excel olarak indirebilirsiniz. Veriye erişim tarihim 07/07/2023 olduğu için sizin verileriniz ile farklılıklar olabilir. Eğer GitHub hesabımdaki `python-pandas-dersleri` repo'sunda bulunan `data`'dan `temelozet.xlsx` dosyasını indirirseniz herhangi bir farklılık olmayacaktır.

## 3.2. İçeri Aktarma

Veriyi aşağıdaki gibi içeri aktarabiliriz.

```python
import pandas as pd

df = pd.read_excel('./data/temelozet.xlsx')
```

İlerleyen derslerde göreceğimiz DataFrame'in kısaltması olan `df`'i kullanmak yaygın bir uygulamadır ancak değişken ismi isteğe bağlı olarak değiştirilebilir.

## 3.3. Baştaki Verileri Yazdırma: head()

```python
df.head()
```

![](/imgs/df_head.PNG)

`df.head()` ile veri setinin ilk 5 satırına baktık. Burada 5 varsayılan değerdir. Örneğin, `df.head(10)` ile ilk 10 satıra da bakılabilirdi.

## 3.4. Sondaki Verileri Yazdırma: tail()

```python
df.tail()
```

![](/imgs/df_tail.PNG)

`df.tail()` ile veri setinin son 5 satırına baktık. Burada 5 varsayılan değerdir. Örneğin, `df.tail(10)` ile son 10 satıra da bakılabilirdi.

## 3.5. Satır ve Sütun Sayısı Bilgisi Alma: shape

Tam olarak satır ve sütun sayısı bilgisini alalım.

```python
df.shape
```

`df.shape` veri çerçevesinin boyutunu döndürür ve veri çerçevesinin satır ve sütun sayısını bir demet olarak verir. Örneğimizde, (509, 8) şeklinde bir çıktı veri çerçevesinin 509 satır ve 8 sütundan oluştuğunu gösterir.

```
(509, 8)
```

## 3.6. Veri Seti Hakkında Detaylı Bilgi Alma: info()

`df.info()` fonksiyonu veri çerçevesi hakkında daha detaylı bilgiler sunar. Bu fonksiyon, veri çerçevesindeki her sütunun veri tipini, veri tiplerinin sayısal dağılımını, bellek kullanımını, eksik değerleri ve sütunların ve satırların toplamda kaç olduğu bilgisini gösterir.

```python
df.info()
```

![](/imgs/df_info.PNG)

## 3.7. Sütun ve Satır Gösterimi Ayarları: pd.set_option()

`df.head()` veya `df.tail()` ile çalıştırdığımızda sütunların eğer sütun sayısı fazla olsaydı sadece bir kısmını görebilirdik. Veri çerçevesindeki sütunların tamamını görmek isteseydik `pd.set_option()` ile aşağıdaki ayarı yapabilirdik.

```python
pd.set_option('display.max_columns', None)
```

`None` kullanılmasının amacı, `display.max_columns` seçeneğini sınırlamadan kaldırmaktır.

Aynı şekilde, satır sayısını da aşağıdaki gibi ayarlayabiliriz.

```python
pd.set_option('display.max_rows', None)
```

`None` kullanılmasının amacı, `display.max_rows` seçeneğini sınırlamadan kaldırmaktır.

# 4. Pandas Series ve Pandas DataFrame Kavramları

---

```python
import pandas as pd

df = pd.read_excel('./data/temelozet.xlsx')
```

Pandas DataFrame (bizim örneğimizde içeri aktardığımız `df`), iki boyutlu bir veri tablosunu temsil eder ve sütunlar ve satırlar şeklinde düzenlenmiş verileri içerir. Pandas Series ise (bizim örneğimizde içeri aktardığımız `df`'in herhangi bir sütunu) tek boyutlu bir diziyi temsil eder ve sıralı bir şekilde indekslenmiş verileri içerir.

## 4.1. Series

```python
df_ornek = {
    'Kod': ['A1CAP','ACSEL','ADEL','ADESE','AEFES','AFYON','AGESA'],
    'Sektör': ['Aracı Kurumlar','Kimyasal Ürün','Kırtasiye','Perakande - Ticaret','Meşrubat / İçecek','Çimento','Sigorta']
}
```

Önce Pandas Series'e çevirelim.

```python
pd_seri = pd.Series(df_ornek['Sektör'], index=df_ornek['Kod'])
pd_seri
```

![](/imgs/df_ornek_series.PNG)

Bu kod satırında, `df_ornek` sözlüğünden `Sektör` anahtarına karşılık gelen değerleri alarak bir Pandas Series oluşturduk. `pd.Series()` işlevini kullanarak `df_ornek['Sektör']` listesini ve `df_ornek['Kod']` listesini sırasıyla `values` ve `index` parametreleri olarak verdik. `index`, her bir veri noktasını tanımlayan etiketlerden oluşan bir dizidir.

## 4.2. DataFrame

Şimdi Pandas DataFrame'e çevirelim.

```python
pd_df = pd.DataFrame(df_ornek)
pd_df
```

![](/imgs/df_ornek_dataframe.PNG)

Veri çerçevesinde 0, 1, 2, ... gibi giden değerler görüyoruz. Bunlar indekstir ve indeksler her bir satırı tanımlayan tekil değerlerdir. Ancak tekil olmak zorunda değillerdir ki ilerleyen derslerde göreceğiz.

### 4.2.1. Sütunlara Erişme

#### 4.2.1.1. Tekli Erişim

Son oluşturduğumuz veri çerçevesinden `Sektör` sütununa erişmek istediğimizi varsayalım.

```python
pd_df['Sektör']
```

![](/imgs/df_ornek_sektor.PNG)

Çıktı tanıdık geliyor. Hemen veri tipine bakalım.

```python
type(pd_df['Sektör'])
```

Çıktının bir seriyi temsil eden `pandas.core.series.Series` olduğunu göreceğiz. Serilerin tek boyutlu olduğunu öğrenmiştik. Veri çerçeveleri de serilerin birleşmesinden oluşuyor.

Aynı sütuna ulaşmanın bir başka yolu ise nokta notasyonunu kullanmaktır.

```python
pd_df.Sektör
```

Yine aynı çıktıyı almış olacağız.

![](/imgs/df_ornek_sektor.PNG)

Hangi yöntemi tercih etmeliyiz?

`pd_df['Sektör']` ifadesi, DataFrame üzerindeki sütuna doğrudan bir dizi indeksi kullanarak erişim sağlar. Bu yöntem, sütun ismi boşluk veya özel karakterler içerdiğinde veya Python programlama dilinde özel bir kelimeyle çakıştığında daha güvenlidir. Örneğin, eğer sütun ismi `sutun ismi` veya `if` gibi bir kelime ise bu ifadeleri kullanarak doğrudan sütuna erişim sağlayabiliriz.

`pd_df.Sektör` ifadesi ise, nokta notasyonunu kullanarak sütuna erişim sağlar. Bu ifade daha kısa ve daha okunabilir bir yazım şekli sunar. Ancak bazı durumlarda, sütun ismi boşluk veya özel karakterler içeriyorsa veya Python programlama dilinde özel bir kelimeyle çakışıyorsa hata verebilir.

Daha önce oluşturduğumuz veri çerçevesine sütunlar ekleyip az önce öğrendiklerimizi pekiştirelim.

```python
df_ornek = {
    'Kod': ['A1CAP','ACSEL','ADEL','ADESE','AEFES','AFYON','AGESA'],
    'Hisse Adı': ['A1 Capital', 'Acıselsan Acıpayam Selüloz', 'Adel Kalemcilik', 'Adese AVM', 'Anadolu Efes', 'Afyon Çimento', 'Agesa Hayat ve Emeklilik'],
    'Sektör': ['Aracı Kurumlar','Kimyasal Ürün','Kırtasiye','Perakande - Ticaret','Meşrubat / İçecek','Çimento','Sigorta'],
    'if': [False,False,False,False,True,True,False],
    '@nerede': ['İstanbul','Denizli','İstanbul','Konya','İstanbul','İstanbul','İstanbul']
}

pd_df = pd.DataFrame(df_ornek)
```

`Hisse Adı` sütununa erişmeye çalışalım.

```python
pd_df['Hisse Adı']
```

![](/imgs/df_ornek_column_single_access.PNG)

Bir de nokta notasyonunu kullanalım.

```python
pd_df.Hisse Adı
```

Yukarıdaki ifade ile ilgili sütuna erişmeye çalışırsak `SyntaxError: invalid syntax` hatası alacağız.

Python programlama dilinde anahtar kelime (keyword) olan ve koşullu ifadeleri belirtmek için kullanılan `if` isimli sütuna erişmeye çalışalım.

```python
pd_df['if']
```

Yukarıdaki ifadeyi kullanırsak ilgili sütuna erişebileceğiz. Bir de nokta notasyonunu kullanalım.

```python
pd_df.if
```

Yukarıdaki ifade ile ilgili sütuna erişmeye çalışırsak `SyntaxError: invalid syntax` hatası alacağız.

Özel bir karakter olan `@`'in kullanıldığı sütuna erişmeye çalışalım.

```python
pd_df['@nerede']
```

Yukarıdaki ifadeyi kullanırsak ilgili sütuna erişebileceğiz. Bir de nokta notasyonunu kullanalım.

```python
pd_df.@nerede
```

Yukarıdaki ifade ile ilgili sütuna erişmeye çalışırsak `SyntaxError: invalid syntax` hatası alacağız.

#### 4.2.1.2. Çoklu Erişim

Buraya kadar tek bir sütuna erişimi gördük. Birden fazla sütuna erişmek istediğimizde aşağıdaki ifadeyi kullanıyoruz.

```python
pd_df[['Kod','Hisse Adı']]
```

![](/imgs/df_ornek_column_multiple_access.PNG)

Yukarıdaki iki duruma dikkat edelim. Birincisi, tek sütuna tek köşeli parantez (`[]`) ile ulaşırken çoklu sütunlara çift köşeli parantez (`[[]]`) ile ulaştık. İkincisi, tek sütuna erişirken çıktıyı bir seri olarak alıyorduk ancak çoklu sütunlara erişmek istediğimizde artık bir seri değil bir veri çerçevesi olarak çıktıyı alıyoruz.

Son olarak, sütun isimlerinin tamamını görmek istiyorsak aşağıdaki ifadeyi kullanabiliriz.

```python
pd_df.columns
```

Yukarıdaki ifade ile `Index(['Kod', 'Hisse Adı', 'Sektör', 'if', '@nerede'], dtype='object')` çıktısını almış olacağız.

### 4.2.2. Satırlara Erişme: iloc ve loc

Burada iki tane kavram ile tanışacağız: `iloc` ve `loc`.

#### 4.2.2.1. iloc

`iloc`, integer location anlamına gelir ve DataFrame veya Series üzerinde konum tabanlı indeksleme yapmamıza olanak tanır. İndeksler sıfırdan başlar ve satır veya sütunları belirlemek için tamsayı indekslerini kullanır. `iloc` kullanırken satır veya sütunların konumunu belirtmek için köşeli parantez içinde tamsayı indeksleri kullanırız.

İlk satıra erişelim.

```python
df.iloc[0]
```

![](/imgs/df_iloc_first_row.PNG)

Yukarıda indeksin sütun isimleri olduğunu görüyoruz.

Tek bir satıra erişebileceğimiz gibi birden fazla satıra da erişebiliriz. Tıpkı çoklu sütuna erişimde olduğu gibi ilerleyeceğiz.

```python
df.iloc[[0,1]]
```

![](/imgs/df_iloc_multiple_rows.PNG)

Görüldüğü üzere çift parantez kullandık ve çıktıyı bir veri çerçevesi olarak aldık.

`iloc` ile sütunlara da erişebiliriz. Örneğin, ilk iki satırın 5. sütununa erişmeye çalışalım.

```python
df.iloc[[0,1],4]
```

![](/imgs/df_iloc_rows_and_column.PNG)

`Piyasa Değeri(mn TL)` 5. sütun olsa da indeksler sıfırdan başladığı için konumu 4'tür. Ayrıca çıktıyı seri olarak aldık.

Çoklu sütunlara da erişebiliriz. Örneğin, 4. ve 5. sütunlara erişelim.

```python
df.iloc[[0,1],[3,4]]
```

![](/imgs/df_iloc_rows_and_columns.PNG)

Çoklu olduğu zaman veri çerçevesi olarak alıyoruz.

Son bir bilgi olarak, integer location'ları hangi sırayla yazarsak o sırayla çıktıyı alırız.

```python
df.iloc[[1,0],[4,3]]
```

![](/imgs/df_iloc_rows_and_columns_order.PNG)

#### 4.2.2.2. loc

`loc`, label location anlamına gelir ve DataFrame veya Series üzerinde etiket tabanlı indeksleme yapmak için kullanılan bir indeksleme yöntemidir.

İlk satıra erişelim. Burada 0 etiketine sahip satırı getireceğiz.

```python
df.loc[0]
```

![](/imgs/df_loc_first_row.PNG)

Tek bir satıra erişebileceğimiz gibi birden fazla satıra da erişebiliriz. Bu defa örnek olarak 0 ve 1 etiketlerine sahip satırları getireceğiz.

```python
df.loc[[0,1]]
```

![](/imgs/df_loc_multiple_rows.PNG)

Buraya kadar yaptıklarımız aslında `iloc`'ta yaptıklarımıza benziyor ancak biz etiket bazlı ilerliyoruz. Son olarak, son sütuna erişelim.

```python
df.loc[[0,1], 'Sermaye(mn TL)']
```

![](/imgs/df_loc_rows_and_column.PNG)

`iloc`'tan farklı olarak sütuna erişmek istediğimizde direkt olarak ismini yazdık.

Çoklu sütunlara da erişebiliriz. Örneğin, aşağıdaki iki sütuna erişelim.

```python
df.loc[[0,1], ['Piyasa Değeri(mn TL)','Piyasa Değeri(mn $)']]
```

![](/imgs/df_loc_rows_and_columns.PNG)

Yine sütun isimlerini belirttik ve çift parantez kullandık. Aynı zamanda çoklu olduğu için veri çerçevesi olarak aldık.

Son bir bilgi olarak, label location'ları hangi sırayla yazarsak o sırayla çıktıyı alırız.

```python
df.loc[[1,0], ['Piyasa Değeri(mn $)','Piyasa Değeri(mn TL)']]
```

![](/imgs/df_loc_rows_and_columns_order.PNG)

### 4.2.3. Satır ve Sütunlara Erişme: İki Nokta Kullanımı

Örneğin, ilk 5 hissenin kod bilgilerine erişmek istediğimizi varsayalım. Bu durumda indeks veya etiketleri tek tek yazmamıza gerek kalmayacak. `:` kullanarak da ilk 5 satıra erişebiliriz. Burada dikkat etmemiz gereken nokta çift parantez yerine tek parantez kullanacak olmamızdır.

```python
df.iloc[0:4,0]
# veya
df.loc[0:4, 'Kod']
```

![](/imgs/df_iloc_loc_double_dot_single.PNG)

Aynısını `:` kullanarak sütunlar için de yapabiliriz. `Kod` sütunundan sonra gelen `Hisse Adı`, `Sektör` ve `Kapanış(TL)` sütunlarını da almak istediğimizi varsayalım.

```python
df.iloc[0:4, 0:4]
# veya
df.loc[0:4, 'Kod':'Kapanış(TL)']
```

![](/imgs/df_iloc_loc_double_dot_multiple.PNG)

### 4.2.4. Sütuna Ait Değerleri Saydırma: value_counts()

Sektörlere ve bunlara ait sayılara ulaşalım.

```python
df['Sektör'].value_counts()
```

![](/imgs/df_value_counts.PNG)

Görüldüğü üzere, `GYO` sektörünün sayısı 41 ile ilk sırada yer alıyor. En az şirkete sahip sektörler 1 ile `Eğlence Hizmetleri` ve `Cam` olmuş.

Visual Studio Code editörünü kullananlar için: *`Output is truncated. View as a scrollable element or open in a text editor. Adjust cell output settings...`* şeklinde bir bilgilendirme alabilirsiniz. Burada, `scrollable element` veya `text editor` seçeneklerine tıklarsanız çıktının tamamını görebilirsiniz.

# 5. İndeksler

---

```python
import pandas as pd

df = pd.read_excel('./data/temelozet.xlsx')
```

## 5.1. İndeks nedir?

```python
df
```

![](/imgs/df_index.PNG)

Sol tarafta bir sütunmuş gibi görünen 0, 1, 2, ... değerleri indekstir. İndeksler, bir numaralandırma veya etiketleme mekanizmasıdır. Örneğin, bir liste içindeki elemanların her biri bir indeks değerine sahiptir ve bu indeksler kullanılarak elemanlara erişebiliriz. Örneğimizdeki veri çerçevesinde indeks, satırları etiketlemek veya numaralandırmak için kullanılır. Varsayılan olarak, veri çerçevesinin indeksi sıfırdan başlayan tam sayılarla oluşturulur. Bununla birlikte, indeksler benzersiz olmak zorunda değildir. Yani aynı indeks değeri birden fazla satıra karşılık gelebilir.

## 5.2. İndeks Ayarlama: set_index() ve index_col

İndeks ayarlamayı iki şekilde yapabiliriz. Birincisi, `set_index()` fonksiyonunu kullanmaktır.

Örneğimizdeki `Kod` sütununu indeks olarak ayarlamak istediğimizi varsayalım.

```python
df = df.set_index('Kod')
df
```

![](/imgs/df_index_kod.PNG)

Yukarıda `Kod` sütununu indeks olarak ayarladık. Ancak değişiklikleri yine aynı veri çerçevesine atadık. Bunu yapmak yerine `inplace` parametresini `True` olarak ayarlayabiliriz.

```python
df.set_index('Kod', inplace=True)
df
```

İkincisi ise veriyi içeri aktarma sırasında `index_col` ile indeks ayarlaması yapmaktır.

```python
df = pd.read_excel('./data/temelozet.xlsx', index_col='Kod')
df
```

![](/imgs/df_index_col.PNG)

İndeksin ne olduğunu aşağıdaki gibi kontrol edebiliriz. `name` ile indeksin `Kod` olarak ayarlandığını görebiliriz.

```python
df.index
```

![](/imgs/df_index_result.PNG)

## 5.3. İndeks Aracılığıyla Erişim: loc

`loc` ile `THYAO` indeksine ulaşalım. Aslında burada `iloc` ile `loc`'un ayrımı daha net görmüş olacağız.

```python
df.loc['THYAO']
```

![](/imgs/df_index_spesific.PNG)

Aynı indeksin `Halka AçıklıkOranı (%)` değerine bakalım.

```python
df.loc['THYAO', 'Halka AçıklıkOranı (%)']
```

Çıktıyı `50.4` olarak alacağız.

Yeri gelmişken, `iloc` ile `loc`'un farkını aşağıdaki gibi gösterebiliriz.

```python
df.iloc[0]
```

Yukarıda iloc `A1 Capital` indeksinin değerlerini sağlıklı bir şekilde verebilirken `loc`'u aynı şekilde kullandığımızda `KeyError` hatası alacağız.

```python
df.loc[0]
```

## 5.4. İndeks Sıfırlama: reset_index()

İndeksi `Kod` olarak ayarlamıştık. Varsayılan indeks değerlerine aşağıdaki gibi dönebiliriz.

```python
df.reset_index(inplace=True)
df
```

![](/imgs/df_index_default.PNG)

## 5.5. İndekslerin Sıralanması: sort_index()

İndeksleri artan sırada olacak şekilde sıralayabiliriz.

```python
df.sort_index()
```

![](/imgs/df_index_sort.PNG)

Eğer sıralamayı azalan sırada yapmak istersek `ascending` parametresini `False` yapmamız gerekiyor.

```python
df.sort_index(ascending=False)
```

![](/imgs/df_index_sort_asc_false.PNG)

Eğer sıralamanın kalıcı olmasını istersek `inplace` parametresini `True` yapmalıyız.

```python
df.sort_index(ascending=False, inplace=True)
# ya da
df.sort_index(inplace=True)
```

# 6. Filtreleme

---

```python
import pandas as pd

df = pd.read_excel('./data/temelozet.xlsx', index_col='Kod')
```

## 6.1. Tekli Filtreleme: İç içe ve loc

`Sektör` sütununun `Bankacılık` olduğu değerleri filtreleyelim.

Filtrelemenin birden fazla yolu olabilir.

İlki olan iç içe yöntemine bakalım.

```python
df[df['Sektör'] == 'Bankacılık']
```

![](/imgs/df_filter_single.PNG)

İkinci bir yol olarak `loc`'u kullanabiliriz. Hatta burada filtrelemenin yanında herhangi bir sütunu da seçebiliriz. Örneğin, `Halka AçıklıkOranı (%)` sütununu alalım.

```python
df.loc[df['Sektör'] == 'Bankacılık', 'Halka AçıklıkOranı (%)']
```

![](/imgs/df_filter_single_spesific_column.PNG)

## 6.2. Çoklu Filtreleme: &, | ve isin()

Birden fazla filtreleme yapmak istediğimizde mantıksal operatörleri kullanabiliriz.

Örneğin, hem `Sektör` sütunundan `Bankacılık` değerini hem de `Halka AçıklıkOranı (%)` sütunundan 50'den büyük olanları alalım ve `Hisse Adı` sütunundaki değerleri getirelim.

```python
df.loc[(df['Sektör'] == 'Bankacılık') & (df['Halka AçıklıkOranı (%)'] > 50), 'Hisse Adı']
```

![](/imgs/df_filter_and_condition.PNG)

Burada, her bir filtreleme işlemini parantez içerisine aldık. Örnekte, ve anlamına gelen `&` operatörünü kullandık. Bir de veya anlamına gelen `|` operatörünü kullanalım.

```python
df.loc[(df['Sektör'] == 'Bankacılık') | (df['Halka AçıklıkOranı (%)'] > 50), 'Hisse Adı']
```

![](/imgs/df_filter_or_condition.PNG)

Ve anlamına gelen `&` kullandığımız örneğe uymayan (tersi) değerleri getirelim. Bunun için `~` kullanmamız yeterli olacaktır. Yani, `Sektör` sütunu `Bankacılık` dışı olan ve `Halka AçıklıkOranı (%)` sütunu <=50 olacak ve `Hisse Adı` değerleri gelecek.

```python
df.loc[~(df['Sektör'] == 'Bankacılık') & ~(df['Halka AçıklıkOranı (%)'] > 50), 'Hisse Adı']
```

![](/imgs/df_filter_and_condition_tilda.PNG)

Eğer yukarıdaki ifadeyi `~` her iki filtreyi de dışarıdan kapsayacak şekilde yazarsak `Sektör` sütunu `Bankacılık` olan ve `Halka AçıklıkOranı (%)` sütunu >50 olanları ilk başta alıp sonra bunun dışında kalanları alacak ve `Hisse Adı` değerlerini getirecek. İlk koşula uyan bir tek AKBNK var. Bunun dışında kalan da 508 hisse olacak.

```python
df.loc[~((df['Sektör'] == 'Bankacılık') & (df['Halka AçıklıkOranı (%)'] > 50)), 'Hisse Adı']
```

![](/imgs/df_filter_and_condition_tilda_general.PNG)

Alternatif bir yol olarak `isin()` kullanılabilir.

```python
df_sektor = df.loc[df['Sektör'].isin(['GYO','Bankacılık'])]
df_sektor
```

![](/imgs/df_filter_isin_sektor.PNG)

Sadece `Hisse Adı` sütununu alalım.

```python
df_sektor = df.loc[df['Sektör'].isin(['GYO','Bankacılık']), 'Hisse Adı']
df_sektor
```

![](/imgs/df_filter_isin_sektor_single_column.PNG)

Yukarıda yapılan işlemin karışık gelmemesi için parçalara ayırabiliriz. Böylece yaptığımız işlem daha net anlaşılabilir.

```python
sektorler = ['GYO','Bankacılık']
sektorler_filtre = df['Sektör'].isin(sektorler)
df_sektor = df.loc[sektorler_filtre, 'Sektör']
df_sektor
```

![](/imgs/df_filter_isin_sektor_single_column.PNG)

## 6.3. String İçerenleri Filtreleme: str.contains()

`Hisse Adı` sadece `Enerji` içerenleri filtreleyelim. Bunun için bir string'i içerip içermediği kontrolü yapmış olacağız.

```python
df_filtre_enerji = df.loc[df['Hisse Adı'].str.contains('Enerji', na=False)]
df_filtre_enerji
```

![](/imgs/df_filter_enerji.PNG)

İhtiyacımız olmamasına rağmen `na` parametresini `False` olacak şekilde ekledik. İlgili sütunda `NA / NaN` içerdiğini varsayalım. Bu durumda kodu çalıştırdığımızda `ValueError: Cannot mask with non-boolean array containing NA / NaN values` hatası alırdık. `na=False` olarak ayarlandığında, `contains()` fonksiyonu eksik değerleri içeren satırları dikkate almadan sadece `Enerji` kelimesini içeren satırları filtrelemek için kullanılır. Yani, `Hisse Adı` sütununda `Enerji` kelimesini içeren satırları seçerken eksik değerleri göz ardı eder.

Sadece ilgilendiğimiz `Hisse Adı` sütununu alalım.

```python
df_filtre_enerji = df.loc[df['Hisse Adı'].str.contains('Enerji', na=False), 'Hisse Adı']
df_filtre_enerji
```

![](/imgs/df_filter_enerji_hisseadi.PNG)

# 7. Sütun ve Satır Güncelleme

---

```python
import pandas as pd

df = pd.read_excel('./data/temelozet.xlsx', index_col='Kod')
```

## 7.1. Sütun Güncelleme: columns, List Comprehension, str.replace(), rename

Tüm sütunların isimlerini güncelleyelim.

```python
df.columns = [
    'HisseAdi',
    'Sektor',
    'KapanisTL',
    'PiyasaDegeriMnTL',
    'PiyasaDegeriMnUSD',
    'HalkaAciklikOraniYuzde',
    'SermayeMnTL'
]
df
```

![](/imgs/df_columns_update.PNG)

Tüm sütun isimlerini büyük harfe çevirelim. Bu işlemi tek tek yapmak yerine list comprehension yöntemi ile yapacağız.

```python
df.columns = [sutun.upper() for sutun in df.columns]
df
```

![](/imgs/df_columns_update_listcomp_upper.PNG)

Bu kod, bir Pandas DataFrame'in sütun isimlerini büyük harflere dönüştürmek için kullanılan bir dizi ifadedir. Kod, list comprehension yöntemini kullanarak, DataFrame'in sütunlarını tek tek dolaşarak her bir sütunun ismini büyük harflere dönüştürür ve bu dönüşüm sonucunda oluşan yeni sütun isimlerini DataFrame'in sütunlarına atar.

USD içeren sütunları `$` ile değiştirelim.

```python
df.columns = df.columns.str.replace('USD','$')
df
```

![](/imgs/df_columns_update_replace_usd.PNG)

Hepsini tekrar list comprehension ile bu defa küçük yapalım.

```python
df.columns = [sutun.lower() for sutun in df.columns]
df
```

![](/imgs/df_columns_update_listcomp_lower.PNG)

Sütun güncellemeyi `rename()` ile de yapabiliriz. Değişikliklerin uygulanması için `inplace` parametresini de `True` yapalım.

```python
df.rename(columns={
    'hisseadi':'HisseAdi',
    'sektor':'Sektor',
    'kapanistl':'KapanisTL',
    'piyasadegerimntl':'PiyasaDegeriMnTL',
    'piyasadegerimn$':'PiyasaDegeriMnUSD',
    'halkaaciklikoraniyuzde':'HalkaAciklikOraniYuzde',
    'sermayemntl':'SermayeMnTL'
}, inplace=True)
df
```

![](/imgs/df_columns_update_rename.PNG)

## 7.2. Satır Güncelleme: loc, at, str.lower(), apply(), applymap(), lambda, map() ve replace()

`A1CAP` etiketine sahip satırdaki bilgileri güncelleyelim.

```python
df.loc['A1CAP'] = ['A1 Capital (Test)','Aracı Kurumlar (Test)',26.80,3618.0,138.7,25.9,135]
df
```

![](/imgs/df_row_update.PNG)

Burada ilgili satırdaki bazı sütunlara denk gelen değerleri güncelledik. Eğer çok daha fazla sütun olsaydı tek tek hepsini yazmak zor olurdu. Bilgisini değiştirdiğimiz `Hisse Adı` ve `Sektör` sütunlarına ait değerleri eski haline getirelim.

```python
df.loc['A1CAP', ['Hisse Adı','Sektör']] = ['A1 Capital','Aracı Kurumlar']
df
```

![](/imgs/df_row_update_spesific.PNG)

Eğer tek bir değeri güncellemek istersek bunu iki farklı yoldan yapabiliriz. Birincisi, her zaman kullandığımız `loc`; ikincisi ise `at` yöntemi.

```python
df.loc['A1CAP', 'Hisse Adı'] = 'A1 Capital Test'
# veya
df.at['A1CAP', 'Hisse Adı'] = 'A1 Capital Test'
df
```

![](/imgs/df_row_update_loc_at.PNG)

Bir filtreleme sonrası da tek bir hücre için güncelleme yapılabilir.

```python
df.loc[df['Sektör'] == 'Bankacılık', 'Halka AçıklıkOranı (%)'] = 0
df.loc[df['Sektör'] == 'Bankacılık', 'Halka AçıklıkOranı (%)']
```

![](/imgs/df_rows_update_single_column.PNG)

Çoklu satır güncellemesi yapmak istediğimiz zaman birkaç farklı yolu kullanabiliriz. Örneğin, `Hisse Adı` sütunundaki tüm değerleri küçük yapalım. Bunun için birincisi `str.lower()` kullanabiliriz.

```python
df['Hisse Adı'] = df['Hisse Adı'].str.lower()
df
```

![](/imgs/df_rows_update_single_column_lower.PNG)

İkinci bir yol olan `apply()` ile `Hisse Adı` sütunundaki tüm değerleri büyük harfli yapalım. Bunun için önce bir fonksiyon yazıp ardından bu fonksiyonu `apply()` ile uygulayacağız.

```python
def hisse_adi_guncelle(hisse_adi):
    return hisse_adi.upper()

df['Hisse Adı'] = df['Hisse Adı'].apply(hisse_adi_guncelle)
df
```

![](/imgs/df_rows_update_single_column_lower_apply.PNG)

Üçüncü bir yol olan `apply()` ve `lambda` ile `Hisse Adı` sütunundaki tüm değerlerin yalnızca ilk harflerini büyük bırakalım.

```python
df['Hisse Adı'] = df['Hisse Adı'].apply(lambda x: x.capitalize())
# veya
df['Hisse Adı'] = df['Hisse Adı'].apply(lambda x: x.title())
# veya
df['Hisse Adı'] = df['Hisse Adı'].apply(lambda x: x[0] + x[1:].lower())
df
```

![](/imgs/df_rows_update_single_column_lower_apply_lambda.PNG)

Dördüncü bir yol olan `applymap()` ve `lambda` ile `Hisse Adı` ve `Sektör` sütunlarındaki harfleri küçük yapalım.

```python
df[['Hisse Adı','Sektör']] = df[['Hisse Adı','Sektör']].applymap(lambda x: x.lower())
df
```

![](/imgs/df_rows_update_single_column_lower_applymap_lambda.PNG)

Beşinci bir yol olan `map()` veya `replace()` ile seriler üzerinde güncelleme işlemleri yapabiliriz.

```python
df['Hisse Adı'].map({'a1 capital test':'a1 capital'})
```

![](/imgs/df_rows_update_single_column_map.PNG)

Ancak `map()` yönteminde eşleştirme sözlüğünde yer almayan değerler dönüşüm sırasında `NaN` olarak kabul edilir. Bu noktada `replace()` fonksiyonunu kullanabiliriz.

```python
df['Hisse Adı'].replace({'a1 capital test':'a1 capital'})
```

![](/imgs/df_rows_update_single_column_replace.PNG)

Değişiklikleri kaydetmek için yine aynı veri çerçevesine atayabiliriz.

# 8. Sütun ve Satır Ekleme ve Kaldırma

---

```python
import pandas as pd

df = pd.read_excel('./data/temelozet.xlsx', index_col='Kod')
```

## 8.1. Sütun Ekleme ve Kaldırma: str.split() ve drop()

`Hisse Adı` sütunu ile `Sektör` sütununu yeni bir sütunda birleştirelim.

```python
df['HisseAdi@Sektor'] = df['Hisse Adı'] + '@' + df['Sektör']
df
```

![](/imgs/df_new_column.PNG)

`Hisse Adı` ve `Sektör` sütunlarına ihtiyacımız olmadığını düşünelim. Bunları `drop()` yardımıyla kaldırabiliriz. Değişiklikleri de aynı veri çerçevesine `inplace` parametresini `True` yapıp kaydedelim.

```python
df.drop(columns=['Hisse Adı','Sektör'], inplace=True)
df
```

![](/imgs/df_drop_columns.PNG)

Kaldırdığımız sütunları tekrar yerine koyalım. Bunun için `str.split()` fonksiyonunu kullanacağız.

```python
df['HisseAdi@Sektor'].str.split('@')
```

![](/imgs/df_split_column.PNG)

Sonucu yeni sütunlar olarak genişletelim. Bunu, `expand` parametresi ile yapacağız.

```python
df['HisseAdi@Sektor'].str.split('@', expand=True)
```

![](/imgs/df_split_column_new.PNG)

Yeni oluşan sütunları veri çerçevesine ekleyelim.

```python
df[['Hisse Adı','Sektör']] = df['HisseAdi@Sektor'].str.split('@', expand=True)
df
```

![](/imgs/df_split_column_new_final.PNG)

## 8.2. Satır Ekleme ve Kaldırma: append(), concat() ve drop()

Sadece `Hisse Adı` sütununa bir veri girişi yapalım. Bunu `append()` ile yapacağız.

```python
df.append({'Hisse Adı':'TEST'})
```

Eğer bu şekilde yaparsak `TypeError: Can only append a dict if ignore_index=True` hatasını alacağız. Bu hata, yalnızca bir sözlüğü veri çerçevesine ekleyebileceğimizi söylüyor. Bunu `ignore_index` parametresini `True` yaparak aşabiliriz.

```python
df.append({'Hisse Adı':'TEST'}, ignore_index=True)
```

![](/imgs/df_new_row.PNG)

Görüldüğü üzere, diğerlerini `NaN` olarak ekledi.

İki veri çerçevesini birleştirelim. Bunun için bir veri çerçevesi daha oluşturalım. İlk veri çerçevesini de ilk hali ile kullanalım.

```python
df = pd.read_excel('./data/temelozet.xlsx', index_col='Kod')

df2 = {
    'Kod':['TST'],
    'Hisse Adı':['TEST'],
    'Sektör':['Bankacılık'],
    'Kapanış(TL)':[0],
    'Piyasa Değeri(mn TL)':[0],
    'Piyasa Değeri(mn $)':[0],
    'Halka AçıklıkOranı (%)':[0],
    'Sermaye(mn TL)':[0],
    'USDTRY':26
}
df2 = pd.DataFrame(df2)
df2.set_index('Kod', inplace=True)
df2
```

![](/imgs/df2.PNG)

İkinci veri çerçevesinde bir sütun fazla. Bu durumda birleştirme sırasında bunu görmezden geleceğiz.

```python
df3 = df.append(df2, ignore_index=True)
df3
```

![](/imgs/df3_append.PNG)

Burada aslında çıkan uyarıları da dikkate almamız gerekiyor. Son kodu çalıştırdığımızda bize `FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.` şeklinde bir uyarı veriliyor. Bu uyarı, `append()` fonksiyonunun pandas'ın gelecekteki bir sürümünde kullanımdan kaldırılacağını ve bunun yerine `concat()` fonksiyonunu kullanmamız gerektiğini söylüyor. Biz de kullanalım.

```python
df3 = pd.concat([df,df2], ignore_index=True)
df3
```

![](/imgs/df3_concat.PNG)

Yine aynı çıktıyı aldık.

509 numaralı indeksi kaldırmak istediğimizi varsayalım. Daha önce kullandığımız `drop()` fonksiyonunun içine `index` parametresini ekleyerek kaldırma işlemini gerçekleştirebiliriz.

```python
df3.drop(index=509, inplace=True)
df3
```

![](/imgs/df3_drop_index.PNG)

Yukarıda sadece bir adet indeks belirtip onu kaldırdık. Sadece `Aracı Kurumlar` içeren satırları indeks ile kaldırmak istediğimizi varsayalım. Önce koşulu belirteceğiz ardından da bu koşulun indekslerini alacağız.

```python
df3.drop(index=df3[df3['Sektör'] == 'Aracı Kurumlar'].index, inplace=True)
df3
```

![](/imgs/df3_drop_index_spesific.PNG)

# 9. Sıralama

---

```python
import pandas as pd

df = pd.read_excel('./data/temelozet.xlsx', index_col='Kod')
```

## 9.1. Tekli Sıralama: sort_values()

Veri çerçevesini kapanış fiyatlarına göre sıralayalım.

```python
df.sort_values(by='Piyasa Değeri(mn $)', inplace=True)
df
```

![](/imgs/df_sort_values.PNG)

Yukarıda küçükten büyüğe doğru sıraladık. Şimdi ise büyükten küçüğe doğru sıralayalım.

```python
df.sort_values(by='Piyasa Değeri(mn $)', ascending=False, inplace=True)
df
```

![](/imgs/df_sort_values_asc_false.PNG)

## 9.2. Çoklu Sıralama: sort_values()

`Sektör` sütununa göre artan ve `Piyasa Değeri(mn $)` sütununa göre azalan şekilde sıralayalım.

```python
df.sort_values(by=['Sektör','Piyasa Değeri(mn $)'], ascending=[True, False], inplace=True)
df
```

![](/imgs/df_sort_values_multiple.PNG)

## 9.3. İndekse Göre Sıralama: sort_index()

İndekse göre artan bir şekilde sıralayabiliriz.

```python
df.sort_index(inplace=True)
df
```

![](/imgs/df_sort_index.PNG)

İndekse göre azalan bir şekilde de sıralayabiliriz.

```python
df.sort_index(ascending=False, inplace=True)
df
```

![](/imgs/df_sort_index_asc_false.PNG)

## 9.4. Serilerin Sıralanması: sort_values()

`Sektör` sütununu alıp seri olacak şekilde bir sıralama yapabiliriz.

```python
df['Sektör'].sort_values()
```

![](/imgs/df_sort_values_series.PNG)

## 9.5. En Büyüklerin Sıralanması: nlargest()

`Piyasa Değeri(mn $)` sütununa göre piyasa değeri $ cinsinden en yüksek 10'a bakalım.

```python
df.nlargest(10, 'Piyasa Değeri(mn $)')
```

![](/imgs/df_nlargest.PNG)

## 9.6. En Küçüklerin Sıralanması: nsmallest()

`Piyasa Değeri(mn $)` sütununa göre piyasa değeri $ cinsinden en düşük 10'a bakalım.

```python
df.nsmallest(10, 'Piyasa Değeri(mn $)')
```

![](/imgs/df_nsmallest.PNG)

# 10. Gruplama ve Özetleme

---

```python
import pandas as pd

df = pd.read_excel('./data/temelozet.xlsx', index_col='Kod')
```

## 10.1. Tekli Sütunun Bir İstatistik Değeri: median()

`Piyasa Değeri(mn $)` sütununun medyan değerine bakalım.

```python
df['Piyasa Değeri(mn $)'].median()
```

Piyasa değerinin `107.3` milyon $ olduğu öğrendik.

## 10.2. Çoklu Sütunların Bir İstatistik Değeri: median()

`Piyasa Değeri(mn TL)` ve `Piyasa Değeri(mn $)` sütunlarının medyan değerine bakalım.

```python
df[['Piyasa Değeri(mn TL)','Piyasa Değeri(mn $)']].median()
```

![](/imgs/df_multiple_columns_median.PNG)

## 10.3. İstatistiksel Özet: describe()

Sayısal veri tipine sahip sütunların istatistiksel özetlerine bakalım.

İstatistiksel özet:

* count: Sütundaki non-null (boş olmayan) değerlerin sayısı.
* mean: Sütundaki değerlerin ortalaması.
* std: Sütundaki değerlerin standart sapması.
* min: Sütundaki en küçük değer.
* 25%: Alt çeyrek yüzdesi, sütundaki değerlerin %25'inin altında olan değer.
* 50%: Medyan veya ortanca, sütundaki değerlerin yarısından küçük ve yarısından büyük olan değer.
* 75%: Üst çeyrek yüzdesi, sütundaki değerlerin %75'inin altında olan değer.
* max: Sütundaki en büyük değer.

```python
df_istatistiksel_ozet = df.drop(['Hisse Adı','Sektör'], axis=1)
df_istatistiksel_ozet.describe()
```

`axis=0`'da (varsayılan değer) işlemler satırlar boyunca yapılır. `axis=1`'de ise işlemler sütunlar boyunca yapılır.

![](/imgs/df_describe.PNG)

## 10.4. Değerlerin Saydırılması: value_counts()

`Sektör` sütunundaki değerleri saydıralım.

```python
df['Sektör'].value_counts()
```

![](/imgs/df_value_counts.PNG)

## 10.5. Değerlerin Yüzdelere Ayrılması: normalize

`Sektör` sütunundaki değerleri saydırmıştık. Bunların yüzde paylarını `normalize` parametresini `True` yaparak alabiliriz.

```python
df['Sektör'].value_counts(normalize=True)
```

![](/imgs/df_value_counts_normalize.PNG)

## 10.6. Gruplayarak Saydırma, Yüzde Alma ve İndeks İnceleme: groupby(), value_counts(), normalize ve loc

Öncelikle `Halka AçıklıkOranı (%)` sütununa göre yeni bir sütun oluşturalım. 50'den büyüksek `>50`; küçük veya eşitse `<=50` yazsın.

```python
df['HalkaAciklikOraniGrup'] = df['Halka AçıklıkOranı (%)'].apply(lambda x: '>50' if x > 50 else '<=50')
df
```

![](/imgs/df_new_group.PNG)

Şimdi `Sektör` sütununa göre `HalkaAciklikOraniGrup` sütununu saydıralım.

```python
df.groupby(['Sektör'])['HalkaAciklikOraniGrup'].value_counts()
```

![](/imgs/df_groupby_value_counts.PNG)

İstediğimizi elde ettik. Son olarak örneğin, `Teknoloji` sektörüne bakalım.

```python
df.groupby(['Sektör'])['HalkaAciklikOraniGrup'].value_counts().loc['Teknoloji']
```

![](/imgs/df_groupby_value_counts_spesific.PNG)

Görüldüğü üzere, ilgilendiğimiz sektördeki halka açıklık dağılımı bilgisine gruplandırılmış olarak ulaştık. Aynı bilgiye yüzde olarak da erişebiliriz.

```python
df.groupby(['Sektör'])['HalkaAciklikOraniGrup'].value_counts(normalize=True).loc['Teknoloji']
```

![](/imgs/df_groupby_value_counts_spesific_pct.PNG)

## 10.7. Bir Gruba Göre Bir İstatistik: groupby() ve median()

`Sektör` sütununa göre sektörlerin piyasa değerlerinin medyanını `Piyasa Değeri(mn $)` sütununu kullanarak alalım.

```python
df.groupby(['Sektör'])['Piyasa Değeri(mn $)'].median()
```

![](/imgs/df_groupby_median.PNG)

## 10.8. Bir Gruba Göre Birden Fazla İstatistik: groupby(), agg(), median() ve std()

`Sektör` sütununa göre sektörlerin piyasa değerlerinin medyanını `Piyasa Değeri(mn $)` sütununu kullanarak alalım. Bunun yanına bir de standart sapma ekleyelim.

```python
df.groupby(['Sektör'])['Piyasa Değeri(mn $)'].agg(['median','std'])
```

![](/imgs/df_groupby_agg_median_std.PNG)

Sütun isimlerini güncelleyebiliriz.

```python
df.groupby(['Sektör'])['Piyasa Değeri(mn $)'].agg(Medyan='median',StandartSapma='std')
```

![](/imgs/df_groupby_agg_median_std_update_columns.PNG)

## 10.9. Bir String İçeriğine Göre Bir İstatistik: groupby(), apply(), lambda, str.contains() ve sum()

`Hisse Adı` sütununda `Enerji` içeren hisseleri `HalkaAciklikOraniGrup` sütununa göre saydıralım.

```python
df.groupby(['HalkaAciklikOraniGrup']).apply(lambda x: x['Hisse Adı'].str.contains('Enerji').sum())
# veya
df.groupby(['HalkaAciklikOraniGrup'])['Hisse Adı'].apply(lambda x: x.str.contains('Enerji').sum())
```

![](/imgs/df_groupby_apply_lambda_str_contains_sum.PNG)

# 11. Kayıp Veri

---

```python
import pandas as pd

df = pd.read_excel('./data/temelozet.xlsx', index_col='Kod')
```

## 11.1. NaN Sayısını Öğrenme: isna() ve sum()

Bazı sütunların bazı değerlerini `NaN` yapalım.

```python
import numpy as np

np.random.seed(34)
random_satirlar = df.sample(n=200)
df2 = df
df2.loc[random_satirlar.index, ['Kapanış(TL)','Piyasa Değeri(mn $)']] = np.nan
df2
```

![](/imgs/df2_nan.PNG)

Her bir sütunda kaç adet `NaN` olduğunu bulabiliriz.

```python
df2.isna().sum()
```

Eğer yukarıda bir `sum()` daha eklersek toplam `NaN` sayısını alırız.

```python
df2.isna().sum().sum()
```

Bu da `400` değerini verecektir.

![](/imgs/df2_nan_sum.PNG)

## 11.2. NaN ve Temizliği: dropna()

`dropna()` kullanarak `NaN` içeren satırları kaldırabiliriz.

```python
df2.dropna()
```

![](/imgs/df2_nan_drop.PNG)

509 satırlık veri çerçevesinin iki sütununa 200 adet `NaN` atamıştık. 200'ünü de kaldırıp 309 satırlık bir veri çerçevesi bıraktı.

`dropna()`'i aşağıdaki gibi özelleştirerek de kullanabilirdik.

```python
df2.dropna(axis='index', how='all', subset=['Kapanış(TL)','Piyasa Değeri(mn $)'])
```

![](/imgs/df2_nan_drop.PNG)

Eksik değerlerin satırlarda bulunduğunu belirtmek için `axis='index'` parametresi kullanılır. `how='all'` parametresi, bir satır veya sütunda tüm değerlerin eksik olduğu durumu belirtir. `'all'` değeri, tüm değerlerin eksik olduğu satırları çıkarmak için kullanılır. Yani, bir satırdaki tüm belirtilen sütunlarda eksik değer varsa o satır veri çerçevesinden çıkarılır. `subset` parametresi ile eksik değerlerin kontrol edileceği sütunları belirttik. Sonuç olarak, `Kapanış(TL)` ve `Piyasa Değeri(mn $)` sütunlarında eksik değerleri olan satırları veri çerçevesinden çıkardık.

## 11.3. Kayıp Veriyi Anlatan Manuel Girilmiş String İfadeleri NaN Yapma: replace()

Bazı sütunların bazı değerlerini `NaN` yapmak yerine `Veri Yok` yazdığımızı varsayalım.

```python
import numpy as np

np.random.seed(34)
random_satirlar = df.sample(n=200)
df2 = df
df2.loc[random_satirlar.index, ['Kapanış(TL)','Piyasa Değeri(mn $)']] = 'Veri Yok'
df2
```

![](/imgs/df2_veriyok.PNG)

`Veri Yok` yazan satırları `replace()` ile `NaN` yapalım.

```python
df2.replace(to_replace='Veri Yok', value=np.nan, inplace=True)
df2
```

![](/imgs/df2_veriyok_nan.PNG)

## 11.4. NaN Değerleri String Bir İfadeye Çevirme: fillna()

`NaN` içeren satırları belirlediğimiz bir string ifadeye çevirelim.

```python
df2.fillna(value='VERI YOK')
```

![](/imgs/df2_fillna.PNG)

## 11.5. NaN Değerleri Bir Önceki Değere Çevirme: fillna()

```python
import numpy as np

np.random.seed(34)
random_satirlar = df.sample(n=200)
df2 = df
df2.loc[random_satirlar.index, ['Kapanış(TL)','Piyasa Değeri(mn $)']] = np.nan
```

Bu örnek için pek anlamlı olmasa da nasıl yapıldığını görmek için yapmış olalım. Bunun için `method` parametresini `pad` yapacağız.

```python
df2.fillna(method = 'pad')
```

![](/imgs/df2_fillna_pad.PNG)

## 11.6. NaN Değerleri Bir Sonraki Değere Çevirme: fillna()

```python
import numpy as np

np.random.seed(34)
random_satirlar = df.sample(n=200)
df2 = df
df2.loc[random_satirlar.index, ['Kapanış(TL)','Piyasa Değeri(mn $)']] = np.nan
```

Bu örnek için pek anlamlı olmasa da nasıl yapıldığını görmek için yapmış olalım. Bunun için `method` parametresini `bfill` yapacağız.

```python
df2.fillna(method = 'bfill')
```

![](/imgs/df2_fillna_bfill.PNG)

## 11.7. NaN Değerleri Bir İstatistik Değerine Çevirme: fillna() ve mean()

```python
import numpy as np

np.random.seed(34)
random_satirlar = df.sample(n=200)
df2 = df
df2.loc[random_satirlar.index, ['Kapanış(TL)','Piyasa Değeri(mn $)']] = np.nan
```

Bu örnek için pek anlamlı olmasa da nasıl yapıldığını görmek için yapmış olalım. İstatistik olarak ortalamayı kullanalım.

```python
df2.fillna(value=df2['Kapanış(TL)'].mean())
```

![](/imgs/df2_fillna_mean.PNG)

## 11.8. NaN Değerlerinin Interpolasyon Tahmini: fillna() ve interpolate()

```python
import numpy as np

np.random.seed(34)
random_satirlar = df.sample(n=200)
df2 = df
df2.loc[random_satirlar.index, ['Kapanış(TL)','Piyasa Değeri(mn $)']] = np.nan
```

Bu örnek için pek anlamlı olmasa da nasıl yapıldığını görmek için yapmış olalım. `method` parametresini `linear` yapacağız.

```python
df2.interpolate(method='linear')
```

![](/imgs/df2_interpolate_linear.PNG)

# 12. Verilerin Dışarı Aktarılması

---

## 12.1. CSV: to_csv()

```python
# En basit haliyle kaydetme
df.to_csv('./data/temelozet_v2.csv')

# İndeksleri çıkarma
df.to_csv('./data/temelozet_v2.csv', index=False)

# Türkçe karakterleri dikkate alma
df.to_csv('./data/temelozet_v2.csv', index=False, encoding='utf-8')

# Zip'li kaydetme
zip_secenekler = dict(method='zip', archive_name='output.csv')
df.to_csv('./data/output.zip', compression=zip_secenekler)

# Farklı bir dosyaya kaydetme (yol-1)
from pathlib import Path
dosya_yolu = Path('./data/data_alt/temelozet_v2.csv')
dosya_yolu.parent.mkdir(parents=True, exist_ok=True)
df.to_csv(dosya_yolu)

# Farklı bir dosyaya kaydetme (yol-2)
import os
os.makedirs('./data/data_alt', exist_ok=True)
df.to_csv('./data/data_alt/temelozet_v2.csv')
```

## 12.2. XLSX: to_excel()

```python
# En basit haliyle kaydetme
df.to_excel('./data/temelozet_v2.xlsx')

# İndeksleri çıkarma
df.to_excel('./data/temelozet_v2.xlsx', index=False)

# Sheet ismini değiştirme
df.to_excel('./data/temelozet_v2.xlsx', sheet_name='IsYatirim')
```
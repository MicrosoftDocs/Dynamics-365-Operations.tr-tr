---
title: Tahsisat temelleri
description: Bu konu, tahsisat tabanları hakkında bilgiler sağlar. Tahsisat tabanları, Maliyet muhasebesindeki kilit bileşenlerdendir ve genellikle genel giderleri tahsis etmekte kullanılır.
author: AndersGirke
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimensionMember
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 92824cf0fb5ad361090d8dccfd64353d2c16317c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565869"
---
# <a name="allocation-bases"></a>Tahsisat temelleri 

[!include [banner](../includes/banner.md)]

bir tahsisat tabanı, Maliyet muhasebesinin genel giderleri tahsis ettiği tabandır. Bir tahsisat tabanı, kullanılan makine saatleri, tüketilen kilovat saat (kWh) veya doldurulan metrekare alan gibi bir miktar olabilir. Tahsisat tabanları, genellikle üretilen stoklara genel giderleri atamak için kullanılır. Örneğin bir BT bölümü, giderlerini her bir bölümün kullandığı bilgisayarların sayısına göre tahsis eder.

Maliyet muhasebesinde üç tip tahsisat tabanı vardır:

- Önceden tanımlanan boyut üyesi tahsisat tabanları
- Hiyerarşi tahsisat tabanları
- Formül tahsisat tabanları

## <a name="predefined-dimension-member-allocation-bases"></a>Önceden tanımlanan boyut üyesi tahsisat tabanları

Önceden tanımlanmış boyut üyesi tahsisat tabanları, aşağıdaki türlerden birinde bir boyut üyesi oluşturulduğunda otomatik olarak oluşturulur:

- İstatistiksel boyut üyeleri
- Maliyet öğesi boyut üyeleri

> [!NOTE]
> Bir maliyet öğesi boyutu üyesine dayanan, önceden tanımlanmış boyut üyesi tahsisat tabanları, yalnızca veri kaynağı sağlayıcısından gelen değerleri dikkate alır; genel muhasebe veya bütçe gibi.

### <a name="example-1-use-a-cost-element-dimension-member-as-the-allocation-base"></a>Örnek 1: Bir maliyet öğesi boyut üyesini, tahsisat tabanı olarak kullanmak
Bu örnek, maliyet öğesi 10001 (Maaşlar) üzerine kaydedilen bakiyeye maliyet öğesi 10002 (Personel sigortası)'nı tahsis etmek için bir maliyet tahsisat kuralı oluşturmayı gösterir. Tahsisat kuralı, her bir bölümün maaşlarının toplam maaşlara oranına dayanarak tanımlanır. (İnceleme gerekiyor!)

Genel muhasebede, hesap planı aşağıdaki şekilde tanımlanır.

| Hesabın planı | Ana hesap | Açıklama        | Ana hesap türü |
|------------------|--------------|--------------------|-------------------|
| Paylaşıldı           | 10001        | Maaşlar           | Gider           |
| Paylaşıldı           | 10002        | Personel sigortası | Gider           |

Bir maliyet öğesi boyutu tanımla ve veri bağlayıcıyı yapılandır. Veri içeri aktarıldıktan sonra, aşağıdaki girişler Maliyet muhasebesinde oluşturulur.

**Maliyet öğesi boyut üyeleri**

| Maliyet öğesi boyutunun adı | Maliyet öğesi |  Açıklama       | Türü    |
|-----------------------------|--------------|--------------------|---------|
| Maliyet öğeleri               | 10001        | Maaşlar           | Birincil |
| Maliyet öğeleri               | 10002        | Personel sigortası | Birincil |

**Önceden tanımlanan boyut üyesi tahsisat tabanları** 

| Dosya Adı  | Açıklama        | Maliyet öğesi boyutu |
|-------|--------------------|------------------------|
| 10001 | Maaşlar           | Maliyet öğeleri          |
| 10002 | Personel sigortası | Maliyet öğeleri          |

Aşağıdaki girişler, genel muhasebeye nakledilmiştir:

- Maaşlar ana hesabında gösterilen girişler, Bordro sisteminden gelir ve maliyet merkezlerine nakledilir.
- Personel sigortası için gider, varsayılan maliyet merkezine el ile nakledilir.

| Muhasebeleşme tarihi | Maliyet merkezi |  Açıklama        | Ana hesap |  Açıklama       | Muhasebe para birimi cinsinden tutar |
|-----------------|-------------|---------------------|--------------|--------------------|-------------------------------|
| 03-01-2017      | CC001       | İK                  | 10001        | Maaşlar           | 2.000,00                      |
| 03-01-2017      | CC002       | FI                  | 10001        | Maaşlar           | 5.000,00                      |
| 03-01-2017      | CC003       | ST                  | 10001        | Maaşlar           | 3.000,00                      |
| 03-01-2017      | CC099       | Varsayılan maliyet merkezi | 10002        | Personel sigortası | 1.000,00                      |

Genel muhasebe kaynak verisi işlendikten sonra, aşağıdaki varlıklar Maliyet muhasebesinde oluşturulur.

**Maliyet girişleri**

| Maliyet nesnesi |  Açıklama        | Maliyet öğesi  |  Açıklama       | Maliyet davranışı   |Tutar|Muhasebeleşme tarihi|
|-------------|---------------------|---------------|--------------------|-----------------|------|---------------|
| CC001       | İK                  | 10001         | Maaşlar           | Sınıflandırılmamış    |2.000,00|  03-01-2017    |
| CC002       | FI                  | 10001         | Maaşlar           | Sınıflandırılmamış    |5.000,00|     03-01-2017         |
| CC003       | ST                  | 10001         | Maaşlar           | Sınıflandırılmamış    |3.000,00|      03-01-2017        |
| CC099       | Varsayılan maliyet merkezi | 10002         | Personel sigortası | Sınıflandırılmamış    |1.000,00|      03-01-2017       |

Bu basitleştirilmiş örnekte, maliyet öğesi 10001 (Maaşlar) üzerine kaydedilen bakiyeyle ilişkili maliyet öğesi 10002 (Personel sigortası)'nı tahsis etmek için bir maliyet tahsisat kuralı oluşturulur.

**Maliyet dağıtım kuralı**

| Maliyet nesnesi boyut hiyerarşisi düğümü | Maliyet öğesi boyut hiyerarşisi düğümü | Maliyet davranışı | Tahsisat temeli |
|--------------------------------------|---------------------------------------|---------------|-----------------|
| CC099                                | 10002                                 | Sınıflandırılmamış  | 10001           |

**Genel gider hesaplaması gerçekleştir**

Maliyet öğesi 10001 (Maaşlar), tahsisat tabanına uygulandıktan sonra, genel gider hesaplamasının aşağıdaki gibi olur.

| Maliyet nesnesi | Açıklama | Büyüklük |   Tahsisat faktörü         | Tutar |
|-------------|-------------|-----------|-----------------------------|--------|
| CC001       | İK          | 2.000     | (2.000 ÷ 10.000) × 1.000,00 | 200,00 |
| CC002       | FI          | 5.000     | (5,000 ÷ 10.000) × 1.000,00 | 500.00 |
| CC003       | ST          | 3.000     | (3.000 ÷ 10.000) × 1.000,00 | 300,00 |

**Günlük**

| Günlük | Günlük türü:                          | Mali takvim dönemi | Yıl | Dönem   | Sürüm                                                                 |
|---------|---------------------------------------|------------------------|------|----------|-------------------------------------------------------------------------|
| 00001   | Maliyet dağıtımı hesaplama günlüğü | Mali                 | 2017 | Dönem 1 | Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1 |

**Maliyet nesnesi bakiyesi günlük girişleri**

| Muhasebeleşme tarihi | Maliyet nesnesi | Açıklama         | Maliyet öğesi | Açıklama        | Maliyet davranışı |  Tutar  |
|-----------------|-------------|---------------------|--------------|--------------------|---------------|----------|
| 31-01-2017      | CC099       | Varsayılan maliyet merkezi | 10002        | Personel sigortası | Sınıflandırılmamış  | 1.000,00 |

**Maliyet girişleri**

| Maliyet nesnesi |  Açıklama        | Maliyet öğesi |    Açıklama     | Maliyet davranışı | Tutar    | Muhasebeleşme tarihi |
|-------------|---------------------|--------------|--------------------|---------------|-----------|-----------------|
| CC099       | Varsayılan maliyet merkezi | 10002        | Personel sigortası | Sınıflandırılmamış  | -1.000,00 | 31-01-2017      |
| CC001       | İK                  | 10002        | Personel sigortası | Sınıflandırılmamış  | 200,00    | 31-01-2017      |
| CC002       | FI                  | 10002        | Personel sigortası | Sınıflandırılmamış  | 500.00    | 31-01-2017      |
| CC099       | ST                  | 10002        | Personel sigortası | Sınıflandırılmamış  | 300,00    | 31-01-2017      |

### <a name="example-2-use-a-statistical-dimension-member-as-the-allocation-base"></a>Örnek 2: Bir istatistiksel boyut üyesini, tahsisat tabanı olarak kullanmak

İstatistiksel boyut üyeleri, ilkeleri tanımlamak veya parasal tüketim olmayan maliyet nesnesi tüketimleri raporlamak için kullanılabilir. İstatistiksel boyut üyelerini el ile oluşturabilirsiniz ve onları Veri yönetim içeri aktarma/dışa aktarma aracını kullanarak bir dosyadan alabilirsiniz.

**İstatistiksel boyut üyeleri**

| İstatistiksel boyut adı | İstatistiksel öğe | Açıklama               | Birim |
|----------------------------|---------------------|---------------------------|------|
| İstatistiksel öğeler       | FTE                 | Tam zamanlı personel       | Her   |
| İstatistiksel öğeler       | Elektrik         | Elektrik tüketimi   | kWh  |

Bir istatistiksel boyut üyesi kaydedildiğinde, karşılık gelen bir kayıt önceden belirlenmiş boyut üyesi tahsisat tabanlarında oluşturulur.

**Önceden tanımlanan boyut üyesi tahsisat tabanları**

| Dosya Adı        | Açıklama             | İstatistiksel öğe boyutu |
|-------------|-------------------------|-------------------------------|
| FTE         | Tam zamanlı personel     | İstatistiksel öğeler          |
| Elektrik | Elektrik tüketimi | İstatistiksel öğeler          |

İstatistiksel ölçümler çeşitli kaynaklardan gelebilir:

- Elektrik tüketimi, şirketin çeşitli alanlarında bulunan saatler tarafından ölçülebilir.
- Tablolar istatistiksel ölçümleri tutar. Örneğin, HcmEmployment tablosu, tüm personelin ve çalıştıkları maliyet merkezlerinin bir listesini tutar.

| Dosya Adı       | Maliyet merkezi |  Açıklama  | Çalışan türü |
|------------|-------------|----|-------------|
| Personel A | CC001       | İK | Personel    |
| Personel B | CC002       | FI | Personel    |
| Personel C | CC002       | FI | Personel    |
| Personel D | CC003       | ST | Personel    |
| Personel F | CC003       | ST | Personel    |

> [!NOTE]
> Finansal boyutları içeren tüm tablolar, istatistiksel ölçümlerin kaynağı olarak kullanılabilir.

Maliyet muhasebesi, aşağıdaki veri bağlantılarını kullanarak bir dizi istatistiksel ölçümü destekler:

- Veri yönetimi içeri/dışarı aktarma aracı
- İstatistiksel ölçüler

Sistemden istatistiksel ölçümleri çekmek için bir istatistiksel ölçüm sağlayıcısı şablonu gereklidir. Daha fazla bilgi için, İstatistiksel ölçüm sağlayıcı şablonu'na bakın. (Bu konu yazıldıktan sonra bir bağlantı eklenecektir.)

**İstatistiksel ölçü sağlayıcısı şablonları**

| Dosya Adı  | İşlev | Kaynak tablosu  | Toplam alanı      | Tarih alanı     |
|-------|----------|---------------|----------------|----------------|
| FTE’ler | Say    | HcmEmployment | Uygulanamaz | Uygulanamaz |

İstatistiksel ölçüm kaynak verisi işlendikten sonra, aşağıdaki varlıklar Maliyet muhasebesinde oluşturulacaktır.

**İstatistiksel girişler**

| Maliyet nesnesi | Açıklama      | Muhasebeleşme tarihi | İstatistiksel boyut üyesi | Açıklama         | Büyüklük |
|-------------|------------------|-----------------|------------------------------|---------------------|-----------|
| CC001       | İK               | 31-01-2017      | FTE’ler                        | Tam zamanlı personel | 1.00      |
| CC002       | FI               | 31-01-2017      | FTE’ler                        | Tam zamanlı personel | 2.00      |
| CC003       | ST               | 31-01-2017      | FTE’ler                        | Tam zamanlı personel | 2.00      |

FTE'lerin önceden belirlenmiş boyut üye tahsisat tabanı, bunun içerisinde tahsisat tabanı olarak atanmışsa, bir maliyet dağıtımı kuralının örneği buradadır.

| Maliyet nesnesi | Açıklama  | Büyüklük | Tahsisat faktörü |
|-------------|------|-----------|-------------------|
| CC001       | İK   | 1.00      | (1/5) × Tutar    |
| CC002       | FI   | 2.00      | (2/5) × Tutar    |
| CC003       | ST   | 2.00      | (2/5) × Tutar    |

İstatistiksel ölçümleri Maliyet muhasebesine aktarmak için İçeri aktarılan istatistiksel ölüler veri varlığını kullanabilirsiniz. Veri yönetimi içeri/dışarı aktarma aracını da kullanabilirsiniz. Elektrik tüketimi Excel'de aşağıdaki gibi kaydedilir.

| Muhasebeleşme tarihi | Boyut üyesi | Büyüklük | Kaynak kimlik tanımlayıcı |
|-----------------|------------------|-----------|-------------------|
| 31-01-2017      | CC001            | 2.450,00  | Elektrik       |
| 31-01-2017      | CC002            | 4.100,00  | Elektrik       |
| 31-01-2017      | CC003            | 15.000,00 | Elektrik       |

İstatistiksel ölçüm kaynak verisi işlendikten sonra, aşağıdaki varlıklar Maliyet muhasebesinde oluşturulacaktır.

**İstatistiksel girişler**

| Maliyet nesnesi |    | Muhasebeleşme tarihi | İstatistiksel boyut üyesi |    Açıklama          | Büyüklük |
|-------------|----|-----------------|------------------------------|-------------------------|-----------|
| CC001       | İK | 31-01-2017      | Elektrik                  | Elektrik tüketimi | 2.450,00  |
| CC002       | FI | 31-01-2017      | Elektrik                  | Elektrik tüketimi | 4.100,00  |
| CC003       | ST | 31-01-2017      | Elektrik                  | Elektrik tüketimi | 15.000,00 |

Elektrik önceden belirlenmiş boyut üye tahsisat tabanı, bunun içerisinde tahsisat tabanı olarak atanmışsa, bir maliyet dağıtımı kuralının örneği buradadır.

| Maliyet nesnesi | Açıklama  | Büyüklük | Tahsisat faktörü          |
|-------------|------|-----------|----------------------------|
| CC001       | İK   | 2.450,00  | (2.450 ÷ 21.550) × Tutar  |
| CC002       | FI   | 4.100,00  | (4.100 ÷ 21.550) × Tutar  |
| CC003       | ST   | 15.000,00 | (15.000 ÷ 21.550) × Tutar |

## <a name="hierarchy-allocation-bases"></a>Hiyerarşi tahsisat tabanları

Maliyet muhasebecileri, hiyerarşi tahsisat tabanları bir maliyet nesnesi boyut hiyerarşisi düğümünü, mevcut bir tahsisat tabanına uygulayarak el ile oluşturabilirler. Bu şekilde, orijinal olarak önceden tanımlanmış boyut üyesi tahsisat tabanının aralığını sınırlayabilirsiniz. Bir önceden tanımlanmış boyut üyesi tahsisat tabanı, birden fazla hiyerarşi tahsisat tabanını oluşturmak için kullanılabilir. Aralıklar, hiyerarşi tahsisat tabanlarıyla ilişkilendirilmiş olan maliyet nesnesi boyutu hiyerarşisi içerisinde tutulabilir.

### <a name="example-hierarchy-allocation-bases-that-are-based-on-full-time-employees-in-the-organization"></a>Örnek: Hiyerarşi tahsisat tabanları, kuruluştaki tam zamanlı çalışanları esas alır.
Basitleştirilmiş bir kuruluşu açıklamak için oluşturulabilecek örnek bir maliyet nesnesi boyut hiyerarşisi buradadır.

| Hiyerarşi adı | Düğüm düzeyi 0 | Düğüm düzeyi 1 | Düğüm düzeyi 2 | Boyut üyeleri |
|----------------|--------------|--------------|--------------|-------------------|
| Organizasyon   | CEO          | CFO          | FICO         | CC001             |
| Organizasyon   | CEO          | CFO          | İK           | CC002             |
| Organizasyon   | CEO          | CIO          | ST           | CC003             |

Önceki bölümde oluşturulmuş olan FTE'nin önceden tanımlanmış boyut üye tahsisat tabanı, aşağıdaki girdileri içerir.

**İstatistiksel girişler**

| Maliyet nesnesi | Açıklama  | Muhasebeleşme tarihi | İstatistiksel boyut üyesi | Açıklama | Büyüklük |
|-------------|------|-----------------|------------------------------|---------------------|-----------|
| CC001       | İK   | 31-01-2017      | FTE’ler                        | Tam zamanlı personel | 1.00      |
| CC002       | FI   | 31-01-2017      | FTE’ler                        | Tam zamanlı personel | 2.00      |
| CC003       | ST   | 31-01-2017      | FTE’ler                        | Tam zamanlı personel | 2.00      |

Bir maliyet, kuruluşun mali işler müdürüne (CFO) raporlanan maliyet merkezleri arasında dağıtılmış olmalıdır. Doğru tahsisat oranının, tam zamanlı personel (FTE'ler) sayısının maliyet merkezine oranı olduğu onaylanır.

**Hiyerarşi tahsisat tabanları**

| Dosya Adı                  | Tahsisat temeli | Maliyet nesnesi boyut hiyerarşisi | Maliyet nesnesi boyut hiyerarşisi düğümü |
|-----------------------|-----------------|---------------------------------|--------------------------------------|
| CFO içerisindeki FTE'lerin sayısı | FTE’ler           | Organizasyon                    | CFO                                  |

Bir önizleme işlevi, oluşturulmuş olan hiyerarşi tahsisat tabanını, sistemdeki istatistiksel girdilere dayanarak doğrulamanıza izin verir.

**Tahsisat temeli ayrıntıları**

| Maliyet nesnesi | Açıklama  |  Büyüklük |
|-------------|------|------------|
| CC001       | İK   | 1.00       |
| CC002       | FI   | 2.00       |

CFO hiyerarşisindeki FTE'lerin sayısının tahsisat tabanı, bunun içerisinde tahsisat tabanı olarak atanmışsa, bir maliyet dağıtımı kuralının örneği buradadır.

| Maliyet nesnesi | Açıklama  | Büyüklük | Tahsisat faktörü |
|-------------|------|-----------|-------------------|
| CC001       | İK   | 1.00      | (1/3) × Tutar    |
| CC002       | FI   | 2.00      | (2/3) × Tutar    |

## <a name="formula-allocation-bases"></a>Formül tahsisat tabanları

Formül tahsisat tabanları, doğru tahsisat tabanına ulaşmanız için gelişmiş formüller tanımlamanıza olanak sağlar. Formül tahsisat tabanlarını el ile oluşturabilirsiniz.

Bir formül tahsisat tabanı oluşturduğunuzda, hangi istatistiksel boyutun ve maliyet öğesi boyutunun formülün temeli olacağını seçersiniz. Önceden seçilmiş olan boyutlardan gelen tüm tahsisat tabanları formül tahsisat tabanında kullanılabilir.

> [!NOTE]
> Önceden tanımlanmış formül tahsisat tabanları, yeni bir formül tahsisat tabanı tanımlamakta kullanılabilir.

Formül tahsisat tabanı faktörlerinde bir diğer ad oluşturursunuz ve bunu bir tahsisat tabanı veya sabiti ile ilişkilendirirsiniz. Diğer adlar daha sonra formülü tanımlamak için kullanılır.

Formülünüzü tanımlamak için aşağıdaki işleçleri kullanabilirsiniz.

| Simgeler | Metin           |
|---------|----------------|
| ( )     | Parantezler    |
| \<      | Daha küçük   |
| \>      | Daha büyük    |
| +       | Fark hesap eki       |
| –       | Çıkarma    |
| \*      | Çarpma |

Geleneksel **IF** ifadeleri desteklenmez. Ancak, deyimler oluşturabilir ve bunların doğru olup olmadığını doğrulayabilirsiniz.

| Deyim | Doğrulama | Sonuç |
|-----------|------------|--------|
| a \> b    | Doğru       | 1      |
| a \> b    | Yanlış      | 0      |

### <a name="example-1-a-simple-formula"></a>Örnek 1: Basit bir formül

Elektrik faturaları genellikle iki bölümden oluşur:

- Şebekeye bağlı olmak için sabit bir ücret
- kWh başına tüketim ile ilişkilendirilmiş bir maliyet

Elektrik önceden tanımlanmış boyut üyesi tahsisat tabanı, zaten tanımlanmıştır ve şu değerleri içerir.

**İstatistiksel girişler**

| Maliyet nesnesi | Dosya Adı | Muhasebeleşme tarihi | İstatistiksel boyut üyesi | Açıklama             | Büyüklük |
|-------------|------|-----------------|------------------------------|-------------------------|-----------|
| CC001       | İK   | 31-01-2017      | Elektrik                  | Elektrik tüketimi | 2.450,00  |
| CC002       | FI   | 31-01-2017      | Elektrik                  | Elektrik tüketimi | 4.100,00  |
| CC003       | ST   | 31-01-2017      | Elektrik                  | Elektrik tüketimi | 15.000,00 |

Sabit ücretin şimdi maliyet nesneleri üzerinde eşit biçimde yayılmış olması gerekiyorsa, maliyetleri tahsis etmek için iki seçeneğiniz vardır:

- Yeni bir önceden tanımlanmış tahsisat tabanı, Elektrik sabiti oluşturun ve daha sonra 1,00 istatistiksel ölçüsünü elektrik tüketen her bir maliyet nesnesine uygulayın.
- Sisteminizde zaten tanımlanmış olan Elektrik önceden tanımlanmış tahsisat tabanından faydalanan bir formül tahsisat tabanı, Elektrik sabiti oluşturun. Bu seçeneğin faydası, verinin Maliyet muhasebesine yalnızca bir Elektrik istatistiksel boyut üyesi için yüklenmesi gerekliliğidir.

**Formül tahsisat tabanı** 

| Dosya Adı              | Maliyet öğesi boyutu | İstatistiksel boyut | Formül |
|-------------------|------------------------|-----------------------|---------|
| Elektrik sabiti |                        | İstatistiksel öğeler  |         |

**Formül** alanının doldurulabilmesinden önce, formülde kullanılacak diğer adı belirtmeniz gerekir.

**Formül tahsisat tabanı faktörleri**

| Diğer ad | Sabit | Tahsisat temeli |
|-------|----------|-----------------|
| a     |          | Elektrik     |
| b     | 0,01     |                 |

0'ın (sıfır) bir sabit değer olarak desteklenmediğini unutmayın.

**Formül tahsisat tabanı**

| Dosya Adı              | Maliyet öğesi boyutu | İstatistiksel boyut | Formül |
|-------------------|------------------------|-----------------------|---------|
| Elektrik sabiti |                        | İstatistiksel öğeler  | a \> b  |

Bir önizleme işlevi, oluşturulmuş olan hiyerarşi tahsisat tabanı, sistemdeki istatistiksel girdilere dayanarak doğrulamanıza izin verir.

**Tahsisat temeli ayrıntıları**

| Maliyet nesnesi | Açıklama  | Formül           | Büyüklük |
|-------------|------|-------------------|-----------|
| CC001       | İK   | 2.450,00 \> 0,01  | 1.00      |
| CC002       | FI   | 4.100,00 \> 0,01  | 1.00      |
| CC003       | ST   | 15.000,00 \> 0,01 | 1.00      |

Elektrik formül tahsisat tabanı, bunun içerisinde tahsisat tabanı olarak atanmışsa, bir maliyet dağıtımı kuralının örneği buradadır.

**Maliyet nesnesi büyüklük tahsisat faktörü**

| Maliyet nesnesi | Dosya Adı | Büyüklük |  Tahsisat faktörü |
|-------------|------|-----------|--------------------|
| CC001       | İK   | 1.00      | (1/3) × Tutar     |
| CC002       | FI   | 1.00      | (1/3) × Tutar     |
| CC003       | ST   | 1.00      | (1/3) × Tutar     |

### <a name="example-2-an-advanced-formula"></a>Örnek 2: Gelişmiş bir formül
Bu örnek için, elektriğin maliyeti, yalnızca elektriğin gerçek tüketilen kWh'ını takip etmemelidir. Yönetim, elektrik kullanımını azaltmayı teşvik etmek istiyor. 

| Kural              | Ücret | 
|-------------------|------|
| a <= 10000,00 kWh | 0,75 |
| a > 10000,00 kWh  | 1,15 |

Yeni bir formül tahsisat tabanı olan Elektrik kullanımı oluşturulur.

**Formül tahsisat tabanı**

| Dosya Adı              | Maliyet öğesi boyutu | İstatistiksel boyut | Formül |
|-------------------|------------------------|-----------------------|---------|
| Elektrik kullanımı |                        | İstatistiksel öğeler  |         |

**Formül** alanının doldurulabilmesinden önce, formülde kullanılacak diğer adı belirtmeniz gerekir.

**Formül tahsisat tabanı faktörleri**

| Diğer ad | Sabit  | Tahsisat temeli |
|-------|-----------|-----------------|
| a     |           | Elektrik     |
| b     | 10,000.00 |                 |
| c     | 0,75      |                 |
| d     | 1,15      |                 |

**Formül tahsisat tabanı**

| Dosya Adı              | Maliyet öğesi boyutu | İstatistiksel boyut | Formül                                                    |
|-------------------|------------------------|-----------------------|------------------------------------------------------------|
| Elektrik sabiti |                        | İstatistiksel öğeler  | ((a \> b) × ((b × c) + (a – b) × d)) + ((a \<= b] × a × c) |

Bir önizleme işlevi, oluşturulmuş olan hiyerarşi tahsisat tabanı, sistemdeki istatistiksel girdilere dayanarak doğrulamanıza izin verir.

**Tahsisat temeli ayrıntıları**

| Maliyet nesnesi |    | Formül                                                                                                                             | Büyüklük |
|-------------|----|-------------------------------------------------------------------------------------------------------------------------------------|-----------|
| CC001       | İK | ((2.450,00 \> 10.000,00) × ((10.000,00 × 0,75) + (2.450,00 – 10.000,00) × 1,15)) + ((2.450,00 \<= 10.000,00) × 2.450,00 × 0,75)     | 1.837,50  |
| CC002       | FI | ((4.100,00 \> 10.000,00) × ((10.000,00 × 0,75) + (4.100,00 – 10.000,00) × 1,15)) + ((4.100,00 \<= 10.000,00) × 4.100,00 × 0,75)     | 3.075,00  |
| CC003       | ST | ((15.000,00 \> 10.000,00) × ((10.000,00 × 0,75) + (15.000,00 – 10.000,00) × 1,15)) + ((15.000,00 \<= 10.000,00) × 15.000,00 × 0,75) | 1.3250,00 |

CC003 (BT) için formüle daha ayrıntılı bir bakış aşağıda verilmiştir:

((15.000,00 \> 10.000,00) × ((10.000,00 × 0,75) + (15.000,00 – 10.000,00) × 1,15)) + ((15.000,00 \<= 10.000,00) × 15.000,00 × 0,75) = 13.250,00

(1 × (7.500,00 + 5.000,00 × 1,15)) + (0 × 15.000,00 × 0,75)            

1 × 7.500,00 + 5.750,00 + 0 

Elektrik sabit formül tahsisat tabanı, bunun içerisinde tahsisat tabanı olarak atanmışsa, bir maliyet dağıtımı kuralının örneği buradadır.


| Maliyet nesnesi | Açıklama | Büyüklük |        Tahsisat faktörü         |
|-------------|-------------|-----------|----------------------------------|
|    CC001    |     İK      | 1.837,50  | (1.837,50 ÷ 18.162,50) × Tutar  |
|    CC002    |     FI      | 3.075,00  | (3.075,00 ÷ 18.162,50) × Tutar  |
|    CC003    |     ST      | 13.250,00 | (13.250,00 ÷ 18.162,50) × Tutar |


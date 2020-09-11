---
title: İstatistiksel boyut üyeleri ve istatistiksel ölçü sağlayıcısı şablonları
description: Bu konu, istatistiksel boyut üyeleri ve istatistiksel ölçü sağlayıcısı şablonları hakkında bilgi sağlar. İstatistiksel boyut üyelerini tahsisat maliyet dağılımı ve maliyet tahsisatı gibi ilkelerde tahsisat temeli olarak kullanılabilir. Ayrıca, parasal olmayan maliyet tüketimini bildirmek için de kullanılabilir.
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerSourceEntryProvider, CAMStatisticalDimension, CAMAXStatisticalMeasureProviderTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c46a9e042482ad66e769383b4e81e2df85a5e97b
ms.sourcegitcommit: fa5c45f7842c4d20c994ac1655e2fbf2a1cf14a9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/28/2020
ms.locfileid: "3734922"
---
# <a name="statistical-dimension-members-and-statistical-measure-provider-templates"></a>İstatistiksel boyut üyeleri ve istatistiksel ölçü sağlayıcısı şablonları

[!include [banner](../includes/banner.md)]

İstatistiksel bir boyut ve üyeleri Maliyet muhasebesinde parasal olmayan girişleri kaydetmek ve kontrol etmek için kullanılır. İstatistiksel boyut üyeleri iki amaçla kullanılabilir:

- Maliyet dağıtımı veya maliyet tahsisatı gibi ilkelerde tahsisat temeli olarak
- Parasal olmayan tüketimi raporlamak için

## <a name="statistical-dimension"></a>İstatistiksel boyut

İstatistiksel boyut benzersiz bir ada ve benzersiz boyut üyeleri kümesine sahiptir. İstatistiksel boyut bir Maliyet muhasebesi defteri koduna atanır. Bu ilişki ilgili tüm istatistiksel boyut üyelerini Maliyet muhasebesi defterine bağlar. Bu nedenle, tüm istatistiksel girişler Maliyet muhasebesi defteri bağlamında oluşturulur.

> [!NOTE]
> İstatistiksel boyut birden fazla Maliyet muhasebesi defterine atanabilir.

İstatistiksel boyut örneği burada verilmiştir.

| Dosya Adı                        | Boyut üyeleri için veri bağlayıcı |
|-----------------------------|--------------------------------------|
| Paylaşılan İstatistiksel öğeler | İçe aktarılan boyut üyeleri           |

Maliyet muhasebesi defterine atanmış olan istatistiksel boyut örneğini burada bulabilirsiniz.

| Dosya Adı                  | Muhasebe para birimi | Döviz kuru türü | Mali takvim | Maliyet öğesi boyutu | İstatistiksel boyut       |
|-----------------------|---------------------|--------------------|-----------------|------------------------|-----------------------------|
| Yönetimsel muhasebe | ABD Doları                 | Sabit para birimi  | Mali dönem   | Paylaşılan Maliyet öğeleri   | Paylaşılan İstatistiksel öğeler |

## <a name="statistical-dimension-members"></a>İstatistiksel boyut üyeleri

İstatistiksel boyut üyesi, parasal olmayan ölçüler için kaydetmek istediğiniz bir varlığı temsil eder. Bu ölçümler bir tahsisat temeli olarak veya sadece parasal olmayan değerleri raporlamak için kullanılabilir.

İstatistiksel boyut üyeleri el ile oluşturulabilir. Alternatif olarak, bunlar bir dosyadan Veri yönetimi içe aktarma/dışa aktarma aracı kullanılarak içe aktarılabilir.

İstatistiksel boyu tüyesi otomatik olarak önceden tanımlanmış tahsisat temeli olur. İlkelerde tahsisat temeli olarak veya diğer türdeki tahsisat temellerinde giriş olarak kullanılabilir.

Burada, bazı tipik istatistiksel boyut üyelerinin örnekleri bulunmaktadır.

| İstatistiksel boyut adı  | İstatistiksel öğeler | Açıklama             | Birim |
|-----------------------------|----------------------|-------------------------|------|
| Paylaşılan İstatistiksel öğeler | FTE                  | Tam zamanlı personel     | Ea.  |
| Paylaşılan İstatistiksel öğeler | Elektrik          | Elektrik tüketimi | kWh  |
| Paylaşılan İstatistiksel öğeler | Paket CC              | Paketleme Maliyet merkezi   | Saat |

## <a name="statistical-measure-provider-template"></a>İstatistiksel ölçü sağlayıcısı şablonu

İstatistiksel ölçüler,n kaynağı çok çeşitli kaynaklar olabilir. Dynamics 365 Finance, istatistiksel ölçütler almak için harika bir kaynaktır. İstatistiksel ölçü sağlayıcı şablonunu, almak istediğiniz istatistiksel ölçüleri kolayca yapılandırmak için kullanabilirsiniz.

İstatistiksel ölçü sağlayıcısı şablon tanımını geneldir ve birden çok istatistiksel boyut üyesinde yeniden kullanılabilir.

> [!NOTE]
> Finansal boyutları içeren tüm tablolar, istatistiksel ölçümlerin kaynağı olarak kullanılabilir.

**Örnek: Maliyet merkezi başına çalışan sayısı**

Maliyet merkezi başına çalışan sayısı, yönetimsel içgörü sağlayan çeşitli amaçlarla kullanılabilen bir istatistiksel ölçüdür.

- Maliyet merkezi başına istatistiksel raporlama ölçüsü
- Çeşitli türde gider için bir tahsisat temeli
- Maliyet merkezi başına dahili maliyet oranları:

    - Personele göre maliyet
    - Personele göre gelir

HcmEmployment tablosu kurulumdaki tüm çalışanların bir listesini tutar. Bu tablo genel bir tablodur. Bu nedenle, kayıtlar belirli bir veri alanı koduyla ilgili değildir.

Burada HcmEmployment tablosundaki çalışanlar için bir örnek verilmiştir.

| Dosya Adı       | Maliyet merkezi | Açıklama   | Çalışan türü |
|------------|-------------|----|-------------|
| Çalışan 1 | CC001       | İK | Personel    |
| Çalışan 2 | CC002       | FI | Personel    |
| Çalışan 3 | CC002       | FI | Personel    |
| Çalışan 4 | CC003       | ST | Personel    |
| Çalışan 5 | CC003       | ST | Personel    |
| Çalışan 6 | CC002       | FI | Yüklenici  |

Bir **İstatistiksel ölçü sağlayıcı şablonu** oluşturduğunuzda kayıt sizin için hangi işlevin kullanılacağına karar verir:

- **Sayım** – Maliyet nesnesi başına kayıt sayısı aktarılır.
- **Toplam** – Maliyet nesnesi başına kayıt toplamı aktarılır. ( **Toplam** alanı ve **Tarih** alanı gereklidir.)

## <a name="using-the-count-function"></a>Sayım işlevini kullanma

Örneğin, istatistiksel ölçü sağlayıcısı şablonu aşağıdaki gibi ayarlanabilir.

| Dosya Adı  | İşlev | Kaynak tablosu  | Toplam alanı      | Tarih alanı     |
|-------|----------|---------------|----------------|----------------|
| FTE'ler  | Say    | HcmEmployment | Uygulanamaz | Uygulanamaz |

Kaynak tablosundan alınacak ölçüleri daraltmak için aranacak bir veya daha fazla aralık da ekleyebilirsiniz.

Bu örnekte, yalnızca tüm tam zamanlı çalışanların sayısını (FTE) istiyorsanız, **Çalışan türü** alanına bir aralık ekleyebilirsiniz. **Ölçüt** alanında çıkış aralığını aşağıdaki gibi sınırlandırmak için **Personel**'i seçin.

**Aralıklar**

| Kaynak tablosu  | Alan       | Ölçütler |
|---------------|-------------|----------|
| HcmEmployment | Çalışan türü | Personel |

İstatistiksel ölçümleri Maliyet muhasebesine almadan önce istatistiksel ölçü sağlayıcısı şablonu ile istatistiksel boyut üyesi arasındaki ilişki oluşturmanız gerekir. Bu ilişki Maliyet muhasebesi defteri ile sürümüne göre oluşturulur. İlişki veri bağlayıcı ve veri sağlayıcıdan oluşur. İstatistiksel boyut üyesi başına birden fazla veri bağlayıcı ve veri sağlayıcı olabilir.

> [!NOTE]
> Bu örnekte, **Geçerli sürüm** için yalnızca bir ilişki oluşturacağız.

İlişkiyi kurmak için **Maliyet muhasebesi defteri**\> **Geçerli sürüm** \> **Yönet**\>**İstatistiksel ölçümler**'e gidin. Bu senaryo için verileri Finance'ten almak istediğimiz için **Dynamics 365 Finance – İstatistiksel ölçüler** veri bağlayıcısını seçin.

**Veri kaynağı**

| Dosya Adı        | Veri bağlayıcı                                                                     | İstatistiksel boyut üyesi |
|-------------|------------------------------------------------------------------------------------|------------------------------|
| FTE D365FO | Dynamics 365 Finance - İstatistiksel ölçüler | FTE'ler                         |

**Veri sağlayıcısı yapılandırması**

| İstatistiksel şablon adı |
|---------------------------|
| FTE'ler                      |

İstatistiksel ölçüm kaynak verisi işlendikten sonra, aşağıdaki istatistiksel girişler Maliyet muhasebesinde oluşturulacaktır.

**Günlük**

| Günlük | Günlük türü:                       | Mali takvim dönemi | Yıl   |  Dönem  |  Sürüm | Veri bağlayıcı kaynak girişleri|
|---------|------------------------------------|------------------------|--------|----------|----------|------------------------------|
| 00001   | İstatistiksel giriş transfer günlüğü | Mali                 | 2017   | Dönem 1 | Maliyet muhasebesi defteri USMF | FTE'ler                   |

**İstatistiksel giriş transfer günlüğü girişleri**

| Muhasebeleşme tarihi | Büyüklük | İstatistiksel öğe |   Açıklama       | Maliyet merkezi |
|-----------------|-----------|---------------------|---------------------|-------------|
| 31-01-2017      | 1.00      | FTE'ler                | Tam zamanlı personel | CC001       |
| 31-01-2017      | 2.00      | FTE'ler                | Tam zamanlı personel | CC002       |
| 31-01-2017      | 2.00      | FTE'ler                | Tam zamanlı personel | CC003       |

**İstatistiksel girişler**

| Maliyet nesnesi |    | Muhasebeleşme tarihi | İstatistiksel boyut üyesi |  Açıklama        | Büyüklük |
|-------------|----|-----------------|------------------------------|---------------------|-----------|
| CC001       | İK | 31-01-2017      | FTE'ler                         | Tam zamanlı personel | 1.00      |
| CC002       | FI | 31-01-2017      | FTE'ler                         | Tam zamanlı personel | 2.00      |
| CC003       | ST | 31-01-2017      | FTE'ler                         | Tam zamanlı personel | 2.00      |

Tam zamanlı personel önceden tanımlanmış boyut üyesi tahsisat temeli maliyet dağıtımı kuralında bir tahsisat temeli olarak atanmışsa, maliyet aşağıdaki tahsisat faktörü kullanılarak dağıtılır.

| Maliyet nesnesi | Açıklama    | Büyüklük | Tahsisat faktörü |
|-------------|----|-----------|-------------------|
| CC001       | İK | 1.00      | (1/5) × Tutar    |
| CC002       | FI | 2.00      | (2/5) × Tutar    |
| CC003       | ST | 2.00      | (2/5) × Tutar    |

## <a name="using-the-sum-function"></a>Toplam işlevini kullanma

Üretim maliyet merkezi, CC010 (Paketleme) müşterilere sevk edilmeden önce ürünleri paketlemekle sorumludur. Ürün reçeteleri ve rota ile ürünlere doğrudan işçilik maliyeti eklenir. Maliyet merkezini çalıştırmadan kaynaklanan dolaylı maliyet de üretilen ürünlere tahsis edilmelidir. Genellikle, bu tür tahsisat için en iyi istatistiksel ölçü belirtilen dönemdeki her ürün için kayıtlı üretim saati sayısıdır.

ProdRouteTrans tablosu tüzel kişilik DataAreadID başına tüm üretim işgücü hareketlerini tutar.

Burada ProdRouteTrans tablosu için bir örnek verilmiştir.

| Referans        | Sayı | Operasyon | Türü | Saat  | Fiili tarih | Ürün grubu (Mali boyut) | Tüzel kişilik |
|------------------|--------|-----------|------|-------|---------------|-------------------------------------|--------------|
| Üretim emri | P0001  | Paketleme | Saat | 8,00  | 01-01-2017    | Portakal suyu B2B                    | USMF         |
| Üretim emri | P0001  | Paketleme | Saat | 8,00  | 02-01-2017    | Portakal suyu B2B                    | USMF         |
| Üretim emri | P0002  | Paketleme | Saat | 4,00  | 03-01-2017    | Portakal suyu Tüketici               | USMF         |
| Üretim emri | P0003  | Paketleme | Saat | 4,00  | 03-01-2017    | Portakal suyu Tüketici               | USMF         |
| Üretim emri | P0004  | Reconst.  | Saat | 10,00 | 03-01-2017    | Portakal suyu Tüketici               | USMF         |

Bir **İstatistiksel ölçü sağlayıcı şablonu** oluşturduğunuzda kayıt sizin için hangi işlevin kullanılacağına karar verir:

- **Sayım** – Maliyet nesnesi başına kayıt sayısı aktarılır.
- **Toplam** – Maliyet nesnesi başına kayıt toplamı aktarılır. ( **Toplam** alanı ve **Tarih** alanı gereklidir.)

İstatistiksel ölçü sağlayıcısı şablonu aşağıdaki gibi ayarlanabilir.

| Dosya Adı    | İşlev | Kaynak tablosu   | Toplam alanı | Tarih alanı    |
|---------|----------|----------------|-----------|---------------|
| Paket CC | Toplam      | ProdRouteTrans | Saatler     | Fiili tarih |

Kaynak tablosundan alınacak ölçüleri daraltmak için aranacak aralıklar ekleyebilirsiniz.

Bu örnekte, yalnızca CC010 Paketleme maliyet merkeziyle ilgili saatlerin toplamını istiyorsanız, **Operasyon** alanında bir aralık ekleyebilirsiniz. **Ölçüt** alanında çıkış aralığını sınırlandırmak için **Paketleme**'yi seçin.

**Aralıklar**

| Kaynak tablosu   | Alan     | Ölçütler  |
|----------------|-----------|-----------|
| ProdRouteTrans | Operasyon | Paketleme |

İstatistiksel ölçümleri Maliyet muhasebesine almadan önce istatistiksel ölçü sağlayıcısı şablonu ile istatistiksel boyut üyesi arasındaki ilişki oluşturmanız gerekir. Bu ilişki Maliyet muhasebesi defteri ile sürümüne göre oluşturulur. İlişki veri bağlayıcı ve veri sağlayıcıdan oluşur. İstatistiksel boyut üyesi başına birden fazla veri bağlayıcı ve veri sağlayıcı olabilir.

> [!NOTE]
> Bu örnekte, **Geçerli sürüm** için yalnızca bir ilişki oluşturacağız.

İlişkiyi kurmak için **Maliyet muhasebesi defteri**\> **Geçerli sürüm** \> **Yönet**\>**İstatistiksel ölçümler**'e gidin. Bu senaryo için verileri Finance'ten almak istediğimiz için **Dynamics 365 Finance – İstatistiksel ölçüler** veri bağlayıcısını seçin.

**Veri kaynağı**

| Dosya Adı           | Veri bağlayıcı                                                                     | İstatistiksel boyut üyesi |
|----------------|------------------------------------------------------------------------------------|------------------------------|
| Paket CC D365FO | Dynamics 365 Finance - İstatistiksel ölçüler | Paket CC                      |

Sistem ProdRouteTrans tablosunun her kaydın ayrı bir tüzel kişiliğe ait olduğu bir tablo olduğunu algılar. Bu nedenle, kaynak hareketlerinin aktarılması gereken tüzel kişiliği seçmeniz istenir.

**Veri sağlayıcısı yapılandırması**

| İstatistiksel şablon adı | Tüzel kişilik |
|---------------------------|--------------|
| Paket CC                   | USMF         |

İstatistiksel ölçüm kaynak verisi işlendikten sonra, aşağıdaki istatistiksel girişler Maliyet muhasebesinde oluşturulacaktır.

**Günlük**

| Günlük | Günlük türü:                     | Mali takvim dönemi | Yıl   | Dönem | Sürüm   |   Veri bağlayıcı kaynak girişleri  |
|---------|----------------------------------|------------------------|--------|---------|----------------|---------|
| 00002   | İstatistiksel giriş transfer günlüğü | Mali               | 2017    | Dönem 1  | Maliyet muhasebesi defteri USMF | Paket CC |

**İstatistiksel giriş transfer günlüğü girişleri**

| Muhasebeleşme tarihi | Büyüklük | İstatistiksel öğe |  Açıklama          | Ürün grubu         |
|-----------------|-----------|---------------------|-----------------------|-----------------------|
| 31-01-2017      | 16.00     | Paket CC             | Paketleme Maliyet merkezi | Portakal suyu B2B      |
| 31-01-2017      | 8,00      | Paket CC             | Paketleme Maliyet merkezi | Portakal suyu Tüketici |

**İstatistiksel girişler**

| Maliyet nesnesi           | Muhasebeleşme tarihi | İstatistiksel boyut üyesi |    Açıklama        | Büyüklük |
|-----------------------|-----------------|------------------------------|-----------------------|-----------|
| Portakal suyu B2B      | 31-01-2017      | Paket CC                      | Paketleme Maliyet merkezi | 16.00     |
| Portakal suyu Tüketici | 31-01-2017      | Paket CC                      | Paketleme Maliyet merkezi | 8,00      |

Paketleme maliyet merkezi önceden tanımlanmış boyut üyesi tahsisat temeli maliyet dağıtımı kuralında bir tahsisat temeli olarak atanmışsa, maliyet aşağıdaki tahsisat faktörü kullanılarak dağıtılır.

| Maliyet nesnesi           | Büyüklük | Tahsisat faktörü  |
|-----------------------|-----------|--------------------|
| Portakal suyu B2B      | 16.00     | (16 ÷ 24) × Tutar |
| Portakal suyu Tüketici | 8,00      | (8 ÷ 24) × Tutar  |

## <a name="imported-statistical-measures"></a>İçe aktarılan istatistiksel ölçüler

Veri yönetimi içe aktarma/dışa aktarma aracını kullanarak istatistiksel ölçümleri Maliyet muhasebesine alabilirsiniz.

İçe aktarma için kullanılan veri varlığı İçe aktarılan İstatistiksel ölçümler olarak adlandırılır.

> [!NOTE]
> Bu veri varlığı giriş başına en fazla beş benzersiz boyut değerine izin vermek üzere tasarlanmıştır.

Elektrik tüketimi Microsoft Excel'de veri varlığı için önceden tanımlanan biçim kullanılarak kaydedilir. Aşağıda bir örnek verilmiştir.

| Muhasebeleşme tarihi | Boyut üyesi adı 1 | Boyut üyesi adı 2 | Boyut üyesi adı 5 | Büyüklük  | Kaynak tanımlayıcı |
|-----------------|------------------------|------------------------|------------------------|------------|-------------------|
| 31-01-2017      | CC001                  |                        |                        | 2.450,00   | Elektrik       |
| 31-01-2017      | CC002                  |                        |                        | 4.100,00   | Elektrik       |
| 31-01-2017      | CC003                  |                        |                        | 15.000,00  | Elektrik       |

Verilerini Veri Yönetimi aracılığıyla aktardığınızda, veriler Maliyet muhasebesi aşamalandırma tablosuna depolanır. Bu nedenle, alınan verilerin birden çok Maliyet muhasebesi defterinde kullanılabilir. Verilerin yeniden yüklenmesi gerekli değildir.

Verileri içe aktarmak için **İçe aktarılan veriler** \> **Veri varlığı** \> **İçe aktarılan istatistiksel ölçümler**'e gidin.

| Kaynak tanımlayıcı | Muhasebeleşme tarihi | Büyüklük  | Boyut üyesi adı 1 | Boyut üyesi adı 2 | Boyut üyesi adı 5 |
|-------------------|-----------------|------------|------------------------|------------------------|------------------------|
| Elektrik       | 31-01-2017      | 2.450,00   | CC001                  |                        |                        |
| Elektrik       | 31-01-2017      | 4.100,00   | CC002                  |                        |                        |
| Elektrik       | 31-01-2017      | 15.000,00  | CC003                  |                        |                        |

İstatistiksel ölçümleri Maliyet muhasebesine almadan önce kaynak tanımlayıcı ile istatistiksel boyut üyesi arasında ilişki oluşturmanız gerekir. Bu ilişki Maliyet muhasebesi defteri ile sürümüne göre oluşturulur. İlişki veri bağlayıcı ve veri sağlayıcıdan oluşur. İstatistiksel boyut üyesi başına birden fazla veri bağlayıcı ve veri sağlayıcı olabilir.

> [!NOTE]
> Bu örnekte, **Geçerli sürüm** için yalnızca bir ilişki oluşturacağız.

İlişkiyi kurmak için **Maliyet muhasebesi defteri**\> **Geçerli sürüm** \> **Yönet**\>**İstatistiksel ölçümler**'e gidin. Bu senaryo için, veriler Maliyet muhasebesine Excel aracılığıyla üçüncü taraf sistemden aktarıldığından **İstatistiksel ölçümleri içe aktar** veri bağlayıcısını seçin.

**Veri kaynağı**

| Dosya Adı        | Veri bağlayıcı                | İstatistiksel boyut üyesi |
|-------------|-------------------------------|------------------------------|
| Elektrik | İçe aktarılan istatistiksel ölçüler | Elektrik                  |

**Veri sağlayıcısı yapılandırması**

| Kaynak tanımlayıcısını içe aktar | İşlev | Boyut 1   | Boyut 2 | Boyut 5 |
|--------------------------|----------|--------------|------------|------------|
| Elektrik              | Toplam      | Maliyet merkezleri |            |            |

> [!NOTE]
> Veri sağlayıcısı yapılandırmasını tanımlarken, hangi maliyet nesnesi boyutlarının içe aktarılan hareketlerle eşleştirileceğini belirtmeniz gerekir. İstatistiksel ölçüm kaynak verisi işlendikten sonra, aşağıdaki istatistiksel girişler Maliyet muhasebesinde oluşturulacaktır.

**Günlük**

| Günlük | Günlük türü:                       | Mali takvim dönemi | Yıl  | Perid  |Sürüm      |Veri bağlayıcı kaynak girişleri |
|---------|------------------------------------|------------------------|-------|--------|---------------|-------------|
| 00002   | İstatistiksel giriş transfer günlüğü | Mali                 | 2017  | Dönem 1 | Maliyet muhasebesi defteri USMF | Elektrik |

**İstatistiksel giriş transfer günlüğü girişleri**

| Muhasebeleşme tarihi | Büyüklük  | Maliyet öğesi |   Açıklama           | Maliyet merkezi |
|-----------------|------------|--------------|-------------------------|-------------|
| 31-01-2017      | 2.450,00   | Elektrik  | Elektrik tüketimi | CC001       |
| 31-01-2017      | 4.100,00   | Elektrik  | Elektrik tüketimi | CC002       |
| 31-01-2017      | 15.000,00  | Elektrik  | Elektrik tüketimi | CC003       |

**İstatistiksel girişler**

| Maliyet nesnesi |    | Muhasebeleşme tarihi | İstatistiksel boyut üyesi |      Açıklama                   | Büyüklük  |
|-------------|----|-----------------|------------------------------|-------------------------|------------|
| CC001       | İK | 31-01-2017      | Elektrik                  | Elektrik tüketimi | 2.450,00   |
| CC002       | FI | 31-01-2017      | Elektrik                  | Elektrik tüketimi | 4.100,00   |
| CC003       | ST | 31-01-2017      | Elektrik                  | Elektrik tüketimi | 15.000,00  |

Elektrik önceden tanımlanmış boyut üyesi tahsisat temeli maliyet dağıtımı kuralında bir tahsisat temeli olarak atanmışsa, maliyet aşağıdaki tahsisat faktörü kullanılarak dağıtılır.

| Maliyet nesnesi |    | Büyüklük | Tahsisat faktörü          |
|-------------|----|-----------|----------------------------|
| CC001       | İK | 2.450,00  | (2.450 ÷ 21.550) × Tutar  |
| CC002       | FI | 4.100,00  | (4.100 ÷ 21.550) × Tutar  |
| CC003       | ST | 15.000,00 | (15.000 ÷ 21.550) × Tutar |

## <a name="additional-resources"></a>Ek kaynaklar

[Tahsisat temelleri](allocation-bases.md)

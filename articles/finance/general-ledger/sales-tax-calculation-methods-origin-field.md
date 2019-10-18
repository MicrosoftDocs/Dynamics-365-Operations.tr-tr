---
title: Kaynak alanında satış vergisi hesaplama yöntemleri
description: Bu makalede satış vergisi kodları sayfasında Başlangıç alanındaki seçenekler ve satış vergisinin bir satış vergisi kodu için belirlenen seçeneğe göre nasıl hesaplanacağı hakkında bilgiler verilmiştir.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ec6144599e9bb74333a663a56bdbf07b1999669
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180289"
---
# <a name="sales-tax-calculation-methods-in-the-origin-field"></a>Kaynak alanında satış vergisi hesaplama yöntemleri

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Bu makalede satış vergisi kodları sayfasında Başlangıç alanındaki seçenekler ve satış vergisinin bir satış vergisi kodu için belirlenen seçeneğe göre nasıl hesaplanacağı hakkında bilgiler verilmiştir.

Satış vergisi kodları sayfasında oluşturduğunuz her satış vergisi kodu için, Kaynak alanında vergi tabanı tutarına uygulanacak hesaplama yöntemini seçmelisiniz.

## <a name="percentage-of-net-amount"></a>Net tutar yüzdesi
Net tutar hesaplama yönteminin Yüzdesi Kaynak alanındaki varsayılan değerdir. Satış vergisi, diğer satış vergileri hariç olarak satınalma veya satış tutarının yüzdesi olarak hesaplanır.
### <a name="example"></a>Örnek

Vergi oranı %25. Fatura satırı, her biri 1,00 seviyesinden 10 maddelik bir miktar gösterir ve müşteriye %10'luk bir satır iskontosu izni verilir. Net tutar: (10 x 1,00) -%10 = 9,00 Satış vergisi: 9,00 x %25 = 2,25 Toplam miktar: 9,00 + 2,25 = 11,25

## <a name="percentage-of-gross-amount"></a> Brüt tutar yüzdesi
Brüt tutar yüzdesi yöntemini seçerseniz, satış vergisi brüt satış tutarı yüzdesi olarak hesaplanır. Brüt tutar, satır net tutarı artı (Kaynak = Brüt tutar yüzdesi değerine sahip bir vergi hariç) satır için tüm vergiler ve harçlardır.
### <a name="example"></a>Örnek

Vergi dairesi bir maddeye özel vergi uygulamaktadır. Vergi tutarları, satış vergisi hesaplanmadan önce net tutara eklenir. Aşağıdaki satış vergisi kodları durumunda:
-   HARÇ 1 = %10 Net tutar yüzdesi hesaplama yöntemini kullanarak
-   HARÇ 2 = %20 Net tutar yüzdesi hesaplama yöntemini kullanarak
-   SATIŞ VERGİSİ = %25 Brüt tutar yüzdesi hesaplama yöntemini kullanarak

Net tutar 10.00 ise HARÇ 1, 1.00 (10.00 x %10) ve HARÇ 2 = 2.00'dir (10.00 x %20). Tutarlar şu şekilde olacaktır: Brüt tutar: Net tutar + HARÇ 1 tutarı + HARÇ 2 tutarı (10.00 + 1.00 + 2.00) = 13.00 SATIŞ VERGİSİ = 13.00 x %25 = 3.25 Toplam HARÇLAR ve SATIŞ VERGİLERİ: 1.00 + 2.00 + 3.25 = 6.25 Toplam tutar: 10.00 + 6.25 = 16.25

| **Not**                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hareket için Kaynak = Brüt tutar yüzdesi değerine sahip yalnızca bir vergi kullanılabilir. Hareket için böyle birden fazla vergi kodu belirlenirse, satış vergisinin hesaplanamadığını bildiren bir hata iletisi görüntülenir. |


<a name="percentage-of-sales-tax"></a>Satış vergilerinin yüzdesi
-----------------------

Köken alanında Satış vergisi yüzdesi değerini seçerseniz, satış vergisi, satış vergisi alanındaki Satış vergisi içinde seçili olan satış vergisinin yüzdesi olarak hesaplanır. Satış vergisi alanındaki Satış vergisi içinde seçili olan satış vergisi önce hesaplanır. İkinci satış vergisi daha sonra, ilk satış vergisi tutarı temel alınarak hesaplanır.
### <a name="example"></a>Örnek

Aşağıdaki satış vergisi kodları durumunda:
-   HARÇ 1 = %10 Net tutar yüzdesi yöntemini kullanarak
-   HARÇ 2 = %20, Satış vergisi yüzdesi yöntemini kullanarak, satış vergisi alanındaki Satış vergisi içinde Harç 1 ile
-   SATIŞ VERGİSİ = %25 Brüt tutar yüzdesi yöntemini kullanarak

Net tutar: 10.00 HARÇ 1: 10.00 x %10 = 1.00 HARÇ 2: 1.00 x %20 = 0.20 Brüt tutar: 10.00 + 1.00 + 0.20 = 11.20 SATIŞ VERGİSİ: 11.20 x %25 = 2.80 Toplam HARÇLAR ve SATIŞ VERGİSİ: 1.00 + 0.20 + 2.80 = 4.00 Toplam tutar: 10.00 + 4.00 = 14.00

| **Not**                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vergi hesaplamalarında çok düzeyli vergi mümkün değildir.  Bir vergi, başka bir vergiye dayanılarak zaten hesaplanmış bir vergiye dayanılarak hesaplanamaz. Bir harekette, vergi kodları üzerinde birden fazla tek düzeyli vergi hesaplanabilir. |

## <a name="amount-per-unit"></a>Birim başına tutar
Kaynak alanında Birim başına tutar seçimini yaptığınızda, satış vergisi belge satırına girilen miktarla çarpılan sabit bir birim başına tutar şeklinde hesaplanır. Birim alanında bir birim seçilmelidir. Birim başına tutar Satış vergisi kod değerleri sayfasında belirtilir.
### <a name="example"></a>Örnek

Satış vergisi kodu şu şekilde ayarlanır: birim = kutu başına USD 1.20 Bir satış faturası satırında bir maddeden 25 kutu satılmış Satış vergisi 25 x 1.20 = 30.00 olarak hesaplanır

| **Not**                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hareket satış vergisi kodunda belirtilenden farklı bir birime girilirse, Birim dönüştürme sayfasında ayarlı birim dönüştürmelerine dayanılarak otomatik olarak dönüştürülür. |

###  <a name="amount-per-unit-additional-option"></a>Birim başına tutar, ek seçenek

Hesaplama sekmesinde, bir birim başına tutar hesaplanmış verginin diğer vergi kodlarından önce hesaplanıp, Kaynak = Net tutar yüzdesi hesaplanmış diğer vergi kodlarından önce net tutara eklenip eklenmeyeceğini belirleyebilirsiniz.

### <a name="examples"></a>Örnekler

Bir harekette 2 vergi kodu hesapladığımızı düşünelim:

-   HARÇ: Kaynak = Birim başına tutar ve bir satış vergisi, değer birim başına 5.00 olarak ayarlanır = pcs
-   SATIŞ VERGİSİ: Kaynak = aşağıdaki örnekte gösterildiği gibi, değer %25 olarak ayarlanır

Bir maddenin 1 parçasını birim fiyatı 10,00'dan satıyoruz
#### <a name="example-1"></a>Örnek 1

SATIŞ VERGİSİ: Kaynak = Brüt tutar yüzdesi yöntemi Satış vergisinden önce hesapla seçeneği etkisizdir çünkü SATIŞ VERGİSİ brüt tutarın yüzdesi olarak hesaplanır. HAR: 1 x 5,00 = 5,00 Brüt tutar: 10,00 + 5,00 = 15,00 SATIŞ VERGİSİ: 15,00 x %25 = 3,75 Toplam satış vergisi: 5,00 + 3,75 = 8,75 Toplam tutar: 10,00 + 8,75 = 18,75

#### <a name="example-2"></a>Örnek 2

SATIŞ VERGİSİ: Kaynak = Net tutar yüzdesi HARÇ hesaplaması için satış vergisinden önce hesapla seçeneği seçilmez. Net tutar: 10,00 HARÇ: 1 x 5,00 = 5,00 SATIŞ VERGİSİ: 10,00 x %25 = 2,50 Toplam satış vergisi: 5,00 + 2,50 = 7,50 Toplam tutar: 10,00 + 7,50 = 17,50

#### <a name="example-3"></a>Örnek 3

SATIŞ VERGİSİ: Kaynak = Net tutar yüzdesi HARÇ hesaplaması için satış vergisinden önce hesapla seçeneği seçilir. Net tutar: 10,00 HARÇ: 1 x 5,00 = 5,00 SATIŞ VERGİSİ: (10,00 + 5,00) x %25 = 3,75 Toplam satış vergisi: 5,00 + 3,75 = 8,75 Toplam tutar: 10,00 + 8,75 = 18,75

#### <a name="example-4"></a>Örnek 4

Yalnızca bir vergi olduğu için, Örnek 3 ile Örnek 1'in sonucu aynıdır. İki HARCINIZ olduğunu ve bunlardan yalnızca birinin satış vergisi hesaplaması için net tutara dahil olduğunu varsayın: HARÇ 1: 5,00, Birim başına tutar yöntemi kullanılarak ve Satış vergisinden önce hesapla seçeneği seçilidir HARÇ 2: 2,50, Birim başına tutar yöntemi kullanılarak ve Satış vergisinden önce hesapla seçeneği seçili değildir Satış vergisi: %25, Net tutar yüzdesi yöntemi kullanılarak Net tutar: 10,00 HARÇ 1: 1 x 5,00 = 5,00 HARÇ 2: 1 x 2,50 = 2,50 Satıl vergisine tabi net tutar: 10,00 + 5,00 = 15,00 SATIŞ VERGİSİ: 15,00 x %25 = 3,75 Toplam satış vergileri, harçlar dahil: 5,00 + 2,50 + 3,75 = 11,25 Toplam tutar: 10,00 + 11,25 = 21,25 %25 SATIŞ VERGİSİ net tutarın toplamı için hesaplanır (10,00) + HARÇ 1 (5,00) = 15,00. HARÇ 2, satış vergisi hesaplandıktan sonra vergi tutarına eklenir.

## <a name="calculated-percentage-of-net-amount"></a>Net tutar için hesaplanan yüzde
Net tutarın hesaplanan yüzdesi, vergi hesaplamalarını belge veya günlük için satış vergisi parametresi içeren Tutarların ayarına bağlı olarak farklı şekilde ele alır.
### <a name="example-1"></a>Örnek 1

Belge / günlük Satış vergisi içeren tutarlar = Evet olarak ayarlanır Hareket satırı tutarı: 10,00 Vergi oranı: %25 Satış vergisi: Hareket satırı tutarı x vergi oranı (10,00 x %25) = 2,50 Vergi taban tutarı (kaynak tutar): Hareket satırı tutarı - Satış vergisi (10,00 - 2,50) = 7,50

### <a name="example-2"></a>Örnek 2

Belge / günlük Satış vergisi içeren tutarlar = Hayır olarak ayarlanır Hareket satırı tutarı: 10,00 Vergi oranı: %25 Satış vergisi: (Hareket satırı tutarı x vergi oranı) / (100 - vergi oranı) (10,00 x %25) / (%100 - %25) = 3,33 Vergi taban tutarı (kaynak tutar): Hareket satırı tutarı = 10,00



<a name="additional-resources"></a>Ek kaynaklar
--------

[Marjinal taban ve hesaplama yöntemi alanları temel alınarak satış vergisi oranlarını belirleme](marginal-base-field.md)

[Satış vergisi kodları için tüm tutar ve Aralık hesaplaması seçenekleri](whole-amount-interval-options-sales-tax-codes.md)




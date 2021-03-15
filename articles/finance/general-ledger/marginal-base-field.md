---
title: Marjinal taban ve Hesaplama yöntemi temel alınarak Satış vergisi oranları
description: Bu konuda, Marjinal taban ve Hesaplama yöntemi alanlarındaki değerlerin, satış ve satınalma hareketlerindeki vergi oran(lar)ını nasıl belirlediği açıklanmaktadır.
author: ShylaThompson
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dcb51c730da3f2ad155675f06f5c1cd9e8476d2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988678"
---
# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a>Marjinal taban ve Hesaplama yöntemi temel alınarak Satış vergisi oranları

[!include [banner](../includes/banner.md)]

Bu konuda, Marjinal taban ve Hesaplama yöntemi alanlarındaki değerlerin, satış ve satınalma hareketlerindeki vergi oran(lar)ını nasıl belirlediği açıklanmaktadır.

Satış vergisi kodları sayfasındaki Hesaplama hızlı sekmesi üzerindeki Marjinal taban, Satış vergisi kodu değerleri sayfasından uygun vergi oranlarının seçilmesinde hangi tutarın kullanılacağını belirler. Marjinal taban alanındaki tutar türü, Hesaplama yöntemi alanındaki yöntem ile birlikte bir hareket için doğru vergi oranı/oranlarını bulmak için mantığı belirlemekte kullanılır. 

Bu alanlardaki değerlerin çeşitli birleşimleri, aşağıdaki örneklerde görüldüğü gibi çok farklı satış vergisi hesaplamaları üretir. Bu örnekler, her bir vergi kodu için Satış vergi kodu değerleri sayfasında ayarlananlarla aynı vergi aralığı değerlerini kullanılır. Bu sayfayı açmak için Satış vergisi kodu &gt; Satış vergi kodlarındaki değerler sayfasını tıklatın.

> [!Important]                                                                                                                  
> Eğer bir ya da birden fazla satış vergisi kodunuzun Marjinal tabanı tutarlar veya birimlere dayanıyorsa, Genel muhasebe defteri parametreleri sayfasındaki Hesaplama yöntemi alanı Satır olarak ayarlanmalıdır. |

## <a name="net-amount-per-line"></a> Satır başına net tutar
Bu seçeneği işaretleyip satış vergisi oranını, fatura satırlarının net tutarına dayanarak, diğer vergileri hariç bırakarak belirleyebilirsiniz.

### <a name="example"></a>Örnek

Satış vergisi oranları aşağıdaki aralıklarda belirlenir.

| Tutar aralığı    | Vergi oranı |
|--------------------|----------|
| 0 - 50             | %30      |
| 50 - 100           | %20      |
| 100 - 0 (&gt; 100) | %10      |

> [!NOTE]                                                                                                             
> Son aralıktaki sıfır (0) üst sınırı, 100'ü geçen tüm miktarların aralığa dahil edileceği anlamına gelir.

Marjinal taban: **Satır başına net tutar** 

Hesaplama Yöntemi: **Aralık** 

Her biri 25,00 olan 8 lamba satın alırsınız. 

Fatura satırının net tutarı 200,00 olur. 

Vergi aşağıdaki gibi hesaplanır: 

Toplam satış vergisi = 50 x %30 + 50 x %20 + 100 x %10 = 15 + 10 + 10 = 35,00 

Toplam fatura tutarı = 200,00 + 35,00 = 235,00 

**Fark** 

Faturada her satırda dört madde olan iki satır varsa, her satırdaki net tutar 100,00 olur ve satış vergisi şu şekilde hesaplanır: 

Satış vergisi satırı 1 = 50 x %30 + 50 x %20 = 15 + 10 = 25,00 

Satış vergisi satırı 2 = 50 x %30 + 50 x %20 = 15 + 10 = 25,00 

Toplam satış vergisi = 25,00 + 25,00 = 50,00 

Toplam fatura tutarı = 200,00 + 50,00 = 250,00

## <a name="net-amount-per-unit"></a> Birim başına net tutar
Bu seçeneği, satış vergisi oranlarını, diğer vergiler hariç her birimin değerini esas alarak belirlemek için. Birime dayalı bir marjinal taban seçilirse, satış vergisi kodu için bir Birim'in de belirlenmesi gereklidir.

### <a name="example"></a>Örnek

Satış vergisi oranları aşağıdaki aralıklarda belirlenir.

| Tutar             | Vergi oranı |
|--------------------|----------|
| 0 - 50             | %30      |
| 50 - 100           | %20      |
| 100 - 0 (&gt; 100) | %10      |

Marjinal taban: **Birim başına net tutar** 

Hesaplama yöntemi = **Tam tutar** 

Her biri 25,00 olan 8 lamba satın alırsınız. 

Fatura satırının net tutarı 200,00 olur. 

Vergi aşağıdaki gibi hesaplanır: Birim başına satış vergisi = 25,00 x %30 = 7.50 Toplam satış vergisi = 8 birim x 7,50 = 60,00 Toplam fatura tutarı = 200,00 + 60,00 = 260,00

## <a name="net-amount-of-invoice-balance"></a> Fatura bakiyesinin net tutarı

Bu seçeneği işaretleyip satış vergisi oranını, fatura satırlarının toplam değerine dayanarak, diğer vergileri hariç bırakarak belirleyebilirsiniz.

### <a name="example"></a>Örnek

Satış vergisi oranları aşağıdaki aralıklarda belirlenir.

| Tutar            | Vergi oranı |
|-------------------|----------|
| 0 - 50            | %30      |
| 50 - 100          | %20      |
| 100 -0 (&gt; 100) | %10      |

Marjinal taban: **Fatura bakiyesinin net tutarı** 

Hesaplama yöntemi: **Aralık** Satış faturasının 2 satırı ve her satırda tanesi 25,00 olan 4 lambası vardır. Fatura bakiyesinin net tutarı 4 x 25,00 + 4 x 25,00 = 200,00 olur. Vergi aşağıdaki gibi hesaplanır: Toplam satış vergisi = 50 x 0,30 + 50 x 0,20 + 100 x 0,10 = 15 + 10 + 10 = 35,00 Toplam fatura tutarı = 200,00 + 35,00 = 235,00

## <a name="gross-amount-per-line"></a> Satır başına brüt tutar

Bu seçeneği işaretleyip satış vergisi oranını, satırın değeri için, bu satırın tüm diğer vergiler dahil olmak üzere belirleyebilirsiniz.

> [!NOTE]
> Bir satış vergisi grubunda, Marjinal taban alanında bu seçime sahip yalnızca bir satış vergisi kodunuz olabilir.

### <a name="example"></a>Örnek

Satış vergisi oranları aşağıdaki aralıklarda belirlenir.

| Tutar             | Vergi oranı |
|--------------------|----------|
| 0 - 50             | %30      |
| 50 - 100           | %20      |
| 100 - 0 (&gt; 100) | %10      |

Marjinal taban: **Satır başına brüt tutar** Hesaplama yöntemi: **Aralık** Ayrıca her lamba için hesaplanan 5,00 tutarında vergi kodu özel harç mevcuttur. Bu harç, satış vergisi hesaplamasından önce net tutara eklenir. Her biri 25,00 olan 8 lamba satın alırsınız. Fatura satırının net tutarı 200,00 olur. Fatura satırının brüt tutarı 8 x 25,00 + 8 x 5,00 = 240,00 olur. Vergi aşağıdaki gibi hesaplanır: Toplam satış vergisi = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 20 + 14 = 39,00 Toplam vergi 5,00 x 8 = 40,00 = Toplam fatura tutarı 200,00 + 39,00 + 40,00 = 279,00

**Fark** 

Fatura her satırda 4 madde olan 2 fatura satırı kullanılarak oluşturulursa, fatura satırı başına net tutar 100,00 olur. Fatura satırı bazında (4 x 5.00 harcı dahil) brüt tutarı 120,00 olur ve satış vergisi aşağıdaki gibi oluşturulur: Satış vergisi fatura satırı 1 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Satış vergisi fatura satırı 2 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Toplam satış vergisi 27,00 + 27,00 = 54,00 Toplam vergi 5,00 x 8 = 40,00 Toplam fatura tutarı 200,00 + 54,00 + 40,00 = 294,00

## <a name="gross-amount-per-unit"></a> Birim başına brüt tutar

Bu seçeneği, satış vergisi oranlarını, diğer vergiler dahil, birimin değerini esas alarak belirlemek için.

> [!NOTE]
> Bir satış vergisi grubunda, Marjinal taban alanında bu seçime sahip yalnızca bir satış vergisi kodunuz olabilir.

### <a name="example"></a>Örnek

Satış vergisi oranları aşağıdaki aralıklarda belirlenir.

| Tutar             | Vergi oranı |
|--------------------|----------|
| 0 - 50             | %30      |
| 50 - 100           | %20      |
| 100 - 0 (&gt; 100) | %10      |

Marjinal taban: **Birim başına brüt tutar** Her lamba üzerinde 5,00 özel vergi var. Bu harç, satış vergisi hesaplamasından önce net tutara eklenir. Her biri 25,00 olan 8 lamba satın alırsınız. Birim başına brüt tutarı 30,00 olur. Vergi aşağıdaki gibi hesaplanır: Birim başına satış vergisi = 30 x %30 = 9,00 Toplam satış vergisi 9,00 x 8 = 72,00 Toplam harç = 5,00 x 8 = 40,00 Toplam fatura miktarı = 200,00 + 72,00 + 40,00 = 312,00

## <a name="invoice-total-incl-other-sales-tax-amounts"></a> Diğer satış vergilerinin tutarları dahil fatura toplamı

Bu seçeneği işaretleyip satış vergisi oranını, fatura satırlarının toplam değerine dayanarak, diğer vergiler dahil olarak belirleyebilirsiniz.
> [!NOTE]
> Bir satış vergisi grubunda, Marjinal taban alanında bu seçime sahip yalnızca bir satış vergisi kodunuz olabilir

### <a name="example"></a>Örnek

Satış vergisi oranları aşağıdaki aralıklarda belirlenir.

| Tutar             | Vergi oranı |
|--------------------|----------|
| 0 - 50             | %30      |
| 50 - 100           | %20      |
| 100 - 0 (&gt; 100) | %10      |

Marjinal taban: **Diğer satış vergisi tutarları dahil fatura toplamı** Hesaplama yöntemi: **Aralık**   
Her lambada 5,00 değerinde özel bir harç vardır. Bu harç, satış vergisi hesaplamasından önce net tutara eklenir. Her biri 25,00 olan 8 lamba satın alırsınız. Faturanın net tutarı 200,00 olur. Faturanın brüt tutarı 200,00 + (8 x 5,00) = 240,00 olur. Vergi aşağıdaki gibi hesaplanır: Toplam satış vergisi = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 10 + 14 = 39,00 Toplam vergi 5,00 x 8 = 40,00 = Toplam fatura tutarı 200,00 + 39,00 + 40,00 = 279,00

Daha fazla bilgi için bkz. [Satış vergisi kodları için tam tutar ve Aralık hesaplaması seçenekleri](whole-amount-interval-options-sales-tax-codes.md) ve [Kaynak alanında satış vergisi hesaplama yöntemleri](sales-tax-calculation-methods-origin-field.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
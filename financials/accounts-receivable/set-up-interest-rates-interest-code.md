---
title: "Bir vade farkı kodu için vade farkı oranları ayarlama"
description: "Vade farkı kodları, faizin nasıl belirleneceğini ve ödemesi geciken hesaplarda nasıl hesaplanacağını belirleyen ayarlar içerir."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 9656718d7afbcc6d89e650ab9379900c083507fe
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-interest-rates-for-an-interest-code"></a>Bir vade farkı kodu için vade farkı oranları ayarlama

[!include[banner](../includes/banner.md)]


Vade farkı kodları, faizin nasıl belirleneceğini ve ödemesi geciken hesaplarda nasıl hesaplanacağını belirleyen ayarlar içerir.

Bir tek faiz kodu ayarlayabilir ve birden fazla müşteri deftere nakil profilleri, faturalama kodları veya belirli fatura satırlarına uygulayabilirsiniz. Faiz kodu ayrıntıları değiştiğinde, bu kodu kullanan tüm özellikler değişiklikleri yeni hareketlere otomatik olarak uygular. Her faiz kodu için iki tür oran ayarlayabilirsiniz:
-   Faiz gelirleri için oranlar − Bunlar faturalardaki veya vade farkı dekontlarının faizini borçlandırmadan kazanılan geliri temsil eder.
-   Faiz ödemeleri için oranlar − Bunlar alacak dekontları üzerindeki faiz için ödenen maliyeti temsil eder.

Bu oran türlerinin her ikisi de aynı anda ve aynı vade farkı kodu içinde bulunabilir. Faiz oranları üç hesaplama türüne bağlı olabilir:
-   Yüzdeye göre vade farkı.
-   Tutara göre vade farkı.
-   Tek bir yüzde veya tutar ile sonuçlanan, aralığa göre vade farkı.

Bir vade farkı kodu, faizi hesaplamak için kullanıldığında, ödemenin hareket vade tarihini geçtiği süre boyunca etkin olan her vade farkı oranı için ayrı bir vade farkı dekontu oluşturulur. **Vade farkı kodu** sayfası üzerindeki **Kazançlar** sekmesini kullanıp, faiz alarak edindiğiniz gelirler için vade farkı oranlarını ayarlayabilirsiniz. **Ödemeler** sekmesini kullanıp ödediğiniz vade farkı için vade farkı oranlarını ayarlayın.

## <a name="interest-rates-based-on-a-percentage"></a>Yüzdeye dayalı vade farkı oranları
Belirli bir yüzdeyi hesaplayan vade farkı oranlarını ayarlayabilirsiniz

-   Vade farkı tutarı tüm para birimleri için geçerlidir.
-   İsteğe bağlı vade farkı tutar limitleri girilebilir.
-   **Vade farkı kodlarını ayarla** sayfasındaki **Vade farkını şuna göre hesapla** alanında **Yüzde** seçilidir.

Örneğin, fatura ödemesinin hareket vade tarihini geçtiği her iki ay için yüzde 5 vade farkı koyan vade farkı kodunu ayarlamak için **Her biri için faiz hesapla** alanına 2 girer ve **Ay**'ı seçersiniz.

## <a name="interest-rates-based-on-amounts"></a>Tutarları temel alan faiz oranları
Belirli bir para birimine göre tutarı hesaplayan vade farkı oranlarını ayarlayabilirsiniz
-   Vade farkı kodu içindeki her para birimi için vade farkı tutarı belirtilir.
-   İsteğe bağlı vade farkı tutar limitleri girilebilir.
-   **Vade farkı kodlarını ayarla** sayfasındaki **Vade farkını şuna göre hesapla** alanında **Tutar** seçilidir.

Örneğin, fatura ödemesinin hareket vade tarihini geçtiği her 20 gün için yüzde 25,00 vade farkı koyan vade farkı kodunu ayarlamak için **Her biri için faiz hesapla** alanında 20 girer ve **Gün**'ü seçersiniz.

## <a name="interest-rates-based-on-ranges"></a>Aralıkları temel alan faiz oranları
Geçmiş tutar, tutarın geç kaldığı gün sayısı veya tutarın geç kaldığı ay sayısına bağlı olarak değişen vade farkı oranları ayarlayabilirsiniz.
-   **Para birimine göre kazanç** sekmesini kullanarak her para birimi için belirli vade farkı ayarları tanımlayabilirsiniz. Ayrıca aralığı da buradan tanımlarsınız.
-   **Aralıklar** butonunu ayarlamak istediğiniz aralıkları temsil eden satırlar eklemek için kullanın. **Gelen** değeri aralığın başlangıcını temsil eder ve **Vade farkı değeri** numarası **Vade farkı kodlarını ayarlamak** sayfasının **Vade farklarının dayanağı** alanındaki yüzde veya tutar seçimine bağlı olarak bir yüzdeyi veya tutarı temsil eder.

## <a name="example-1-interest-by-range--amount"></a>Örnek 1: Aralığa göre vade farkı = Tutar
Faturanın ödemesinin hareket vade tarihini aştığını her üç ayda bir değerlendirecek bir vade farkı kodu ayarlarsınız. Hesaplamayı, adımlı tutar aralıklarına göre, bir yüzde vade farkı değerine dayandırmak isteyebilirsiniz. Faiz değeri 1.000,00 olan faturalara kadar yüzde 1, 1.001,00'den 5.000,00 olanlara kadar yüzde 2 ve 5.000,00'den büyük olanlar için yüzde üç olacaktır. Vade farkı kodu alan değerlerini aşağıdaki gibi ayarlayın.

| **Alan adı**                  | **Alan değeri** |
|---------------------------------|-----------------|
| **Vade farkı kodu**               | 3M%ByAmt        |
| **Her biri için faizi hesapla:**    | 3/Ay         |
| **Aralığa göre faiz**           | Tutar          |
| **Vade farkını şuna göre hesapla** | Yüzde      |

Aralığı bilgilerini aşağıdaki gibi ayarlayın.

| **Başlangıç değeri** | **Faiz değeri** |
|----------------|--------------------|
| 0              | 1                  |
| 1,001          | 2                  |
| 5,001          | 3                  |

 
## <a name="example-2-interest-by-range--days"></a>Örnek 2: Aralığa göre faiz = Gün
--------------------------------------------------

Faturanın ödemesinin hareket vade tarihini aştığını her 15 günde bir değerlendirecek bir vade farkı kodu ayarlarsınız. Hesaplamayı, adımlı gün aralıklarına göre, bir tutar vade farkı değerine dayandırmak isteyebilirsiniz. Vade farkı değeri ilk 60 gün içinde 15 günlük 10,00, 61 ve 90. günler arasında 15 günlük 15,00 ve 91 gün ve daha fazlası için her 15 günlük 20,00 olacaktır. Vade farkı kodu alan değerlerini aşağıdaki gibi ayarlayın.

| **Alan adı**                  | **Alan değeri** |
|---------------------------------|-----------------|
| **Vade farkı kodu**               | 15DAmtXDay      |
| **Her biri için faizi hesapla:**    | 15/Gün          |
| **Aralığa göre faiz**           | Gün            |
| **Vade farkını şuna göre hesapla** | Tutar          |

Aralığı bilgilerini aşağıdaki gibi ayarlayın.

| **Başlangıç değeri** | **Faiz değeri** |
|----------------|--------------------|
| 0              | 10                 |
| 61             | 15                 |
| 91             | 20                 |

 
## <a name="example-3-interest-by-range--months"></a>Örnek 3: Aralığa göre faiz = Ay
----------------------------------------------------

Faturanın ödemesinin hareket vade tarihini aştığını her ayda bir değerlendirecek bir vade farkı kodu ayarlarsınız. Hesaplamayı, adımlı aylık aralıklarına göre, bir yüzde vade farkı değerine dayandırmak isteyebilirsiniz. Varde farkı değer, vadenin geçtiği ilk üç ay için her aylık yüzde 1,5, ikinci üç aylık dönem için aylık yüzde 2,0 ve ilk altı aydan sonraki her ay için yüzde 2,5 olacaktır. Vade farkı kodu alan değerlerini aşağıdaki gibi ayarlayın.

| **Alan adı**                  | **Alan değeri** |
|---------------------------------|-----------------|
| **Vade farkı kodu**               | 1M%ByMth        |
| **Her biri için faizi hesapla:**    | 1/Ay         |
| **Aralığa göre faiz**           | Ay          |
| **Vade farkını şuna göre hesapla** | Yüzde      |

Aralığı bilgilerini aşağıdaki gibi ayarlayın.

| **Başlangıç değeri** | **Faiz değeri** |
|----------------|--------------------|
| 0              | 1.5                |
| 4              | 2                  |
| 7              | 2.5                |

## <a name="new-versions"></a>Yeni sürümler
Vade farkı kodlarını yürürlülük tarihi var. Faiz oranını değiştirmek isterseniz, ileriki bir tarihte etkili olacak bir **Yeni sürüm** oluşturabilirsiniz.

Farklı sürümleri görüntülemek için, **Tarihli sürüm** menü seçeneğini kesme tarihini seçmek için kullanabilirsiniz. Ayrıca sayfadaki tüm vade farkı kodlarını görüntülemek için **Tüm kayıtları görüntüle**'yi seçebilirsiniz.





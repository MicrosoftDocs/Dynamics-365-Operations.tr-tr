---
title: Malzeme tüketimini hesapla
description: Bu makalede, malzeme tüketiminin hesaplanmasına ilişkin çeşitli seçenekler hakkında bilgiler sağlanmaktadır.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f58365278200344169b93658e9c92dea2bc4f18f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211658"
---
# <a name="calculate-material-consumption"></a>Malzeme tüketimini hesapla

[!include [banner](../includes/banner.md)]

Bu makalede, malzeme tüketiminin hesaplanmasına ilişkin çeşitli seçenekler hakkında bilgiler sağlanmaktadır. 

Malzeme tüketiminin hesaplanmasına ilişkin aşağıdaki seçenekler **Ürün reçetesi** sayfasının **Satır ayrıntıları** hızlı sekmesinde bulunan **Ayar** ve **Adım tüketimi** sekmelerinde bulunur.

## <a name="variable-and-constant-consumption"></a>Değişken ve sabit tüketim
**Tüketim** alanında, tüketimin bir sabit miktar mı yoksa değişken miktar olarak mı hesaplanacağını seçebilirsiniz. Üretim için sabit miktar veya hacim gerekiyorsa **Sabit**'i seçin, üretilen miktardan bağımsız olarak. Varsayılan ayar olan **Değişken** seçeneğini, mamul ürünler için gereken malzeme tutarı üretilen mamul ürün sayısına orantılı olduğunda seçin.

## <a name="calculating-consumption-from-a-formula"></a>Tüketimi bir formülden hesaplama
**Formül** alanında, malzeme tüketimini hesaplamak için çeşitli formüller ayarlayabilirsiniz. Varsayılan değeri olan **Standart**'ı kullanırsanız, tüketim bir formülle hesaplanmaz. Aşağıdaki formüller **Yükseklik**, **Genişlik**, **Derinlik**, **Yoğunluk** ve **Sabit** alanlarıyla birlikte çalışır:

-   Yükseklik \* Sabit
-   Yükseklik \* Genişlik \* Sabit
-   Yükseklik \* Genişlik \* Derinlik \* Sabit
-   (Yükseklik \* Genişlik \* Derinlik / Yoğunluk) \* Sabit

## <a name="rounding-up-and-multiples"></a>Yuvarlama ve katları
**Yuvarlama** ve **Katları** alanları birlikte kullanıldığında, malzeme tüketim değerini yuvarlamanıza olanak tanır. Örneğin, değeri hammaddenin üretim için çekildiği işleme birimine göre yuvarlayabilirsiniz. **Yuvarlama** alanında şu seçenekler kullanılabilir: **Miktar**, **Ölçüm** ve **Tüketim**.

### <a name="quantity"></a>Miktar

Yuvarlama mekanizması olarak **Miktar** seçerseniz, miktarın belirtilen miktarın katı olması gerekir. Örneğin, tam sayılar gerekiyorsa **Katları** alanına **1** yazın. Ardından sayılar 1'e bölünebilen bir miktara yuvarlanır.

### <a name="measurement"></a>Ölçüm

Genellikle, hammaddenin belirli boyutlarda gelmesi durumunda yuvarlama mekanizması olarak **Ölçüm** seçilir. Örneğin, bir mamul ürün için 2 metre uzunluğunda metal boru parçası gereklidir ve metal boru 4,5 metre uzunluğunda depolanmıştır. Bu durumda, mamul üründen belirli sayıda üretmek için ne kadar metal boru gerektiğini hesaplamak için **Ölçüm** yuvarlama mekanizması kullanılabilir. Bu örnek için **Formül** alanı **Yükseklik \* Sabit** olarak ayarlanır. **Yükseklik** alanı, tamamlanmış mal için gerekli olan borunun boru uzunluğunu belirtmek için **2** olarak ayarlanmıştır. Borunun 4,5 metre uzunluğunda alındığını belirtmek için **Katı** alanı **4,5** olarak ayarlanır. Hesaplama aşağıdaki gibidir:

1.  10 adet mamul için gereken katları sayısı: 10 ÷ 2 = 5 parça
2.  Toplam tüketim: 4,5 × 5 = 22,5 metre metal boru

Tüketilen her beş adet boru için 0,5 metre borunun hurdaya çıktığı varsayılır.

### <a name="consumption"></a>Tüketim

Genellikle, hammaddenin üretimin belirli bir işleme birimi için toptan miktarlarda çekilmesi gerekiyorsa yuvarlama mekanizması olarak **Tüketim** seçilir. Örneğin, bir mamul ürünü üretmek için 2 litre boya gerekmektedir ve boya 25 litrelik kutularda alınmıştır. Bu durumda, tüketimi 25 litrelik kutuların tam sayılarına yuvarlamak için **Tüketim** yuvarlama mekanizması kullanılabilir. 180 adet mamul ürün üretilecekse gerekli boya miktarı aşağıdaki şekilde hesaplanır:

1.  Hurdaya ayrılan hariç gereken boya miktarı: 180 × 2 = 360 litre
2.  Kutu sayısı: 360 ÷ 25 = 14.4; 15'e yuvarlanır
3.  Hurdaya gidecek miktar dahil gereken boya: 15 × 25 = 375 litre

## <a name="step-consumption"></a>Adım tüketimi
Adım tüketimi, miktar aralıklarındaki sabit tüketimi hesaplamak için kullanılır. **Kurulum** sekmesinde **Formül** alanında **Adım tüketimi** seçerseniz, **Adım tüketimi** sekmesindeki adımlar hakkında bilgi girebilirsiniz. Sabit tüketilen miktar, üretilen miktarın aralıkları olarak ayarlanabilir. Örneğin, adım tüketimi aşağıdaki tabloda gösterildiği şekilde ayarlanır.

| Başlangıç serisi | Miktar |
|-------------|----------|
| 0,00        | 10,0000  |
| 100,00      | 20,0000  |
| 200,00      | 40,0000  |

Ürün reçetesi (BOM) miktarı 1 ve üretim miktarı 110'dur. Tüketim formülü Başlangıç serisi (Miktar) = Tüketim'dir. Ürün miktarı 110 olduğundan, "100 seriden başlayarak" ayarına düşer. Bu nedenle miktar 20'dir.




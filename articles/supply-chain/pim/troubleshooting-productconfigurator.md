---
title: Ürün yapılandırıcısındaki sorunları giderme
description: Bu konuda, ürün yapılandırıcı ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklanmaktadır.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e6cfeb6a2b4166dfa9a5a5cc1b7d3d913b865ce2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999618"
---
# <a name="troubleshoot-the-product-configurator"></a>Ürün yapılandırıcısındaki sorunları giderme

Bu konuda, ürün yapılandırıcı ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklanmaktadır.

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a>Satış siparişi satırındaki bir ürünü yapılandırırken madde metninin üzerine yazılıyor.

### <a name="issue-description"></a>Sorun açıklaması

Bu sorun, yapılandırılabilir bir madde için satış siparişi satırı oluşturup madde metnini değiştirdiğinizde oluşur. Maddeyi yapılandırıp **Tamam**'ı seçtiğinizde , standart metin metnin üzerine yazılır.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu davranış beklenmektedir. Metin alanı, yalnızca satır yapılandırıldıktan sonra doldurulan varyant adını içerir. Bu nedenle, metni satırı yapılandırmadan önce değil, sonra değiştirmeniz gerekir.

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>Ürün yapılandırma modelleri hesaplanırken, tamsayı nitelikleri yanlış yuvarlanıyor.

### <a name="issue-description"></a>Sorun açıklaması

Bu sorun, aşağıdaki eylem dizilerini gerçekleştirdiğinizde oluşabilir:

1. Üretim yapılandırması modelinde aşağıdaki öznitelikleri ayarlama:

    - Giriş (tamsayı)
    - Yüzde (ondalık)
    - Sonuç (tamsayı)

2. Aşağıdaki ifadeye sahip bir hesaplama oluşturma:

    *Sonuç* = *Giriş* × *Yüzde* ÷ 100

Bu durumda, tamsayı sonucu her zaman doğru olarak yuvarlanmaz. Örneğin, giriş 1.000 ve yüzde 2,40'tır. Bu nedenle, 1.000'in yüzde 2,40'ı 24 (veya ondalık biçimde 24,00) olduğundan tamsayı sonucunun 24 olmasını beklersiniz. Bunun yerine, sonuç 23 olarak gösterilir. Ancak, yüzde değeri 2,39 olduğunda, hesaplama 23 yerine 24'e yuvarlanır. Yüzde değeri 2,50 olduğunda, hesaplama beklendiği şekilde 25'e yuvarlanır.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu sorun, Microsoft Solver Foundation dahili olarak sayıları kesirleri kullanarak temsil ettiğinden oluşur. Önceki örnekte, yüzdenin 2,40 olduğu hesaplamanın sonucu 27021597764222975 ÷ 1125899906842624 = 23,99999999999999911182158029987476766109466552734375 olarak gösterilir. .NET bu değeri tamsayı olarak verdiğinde 23 değerini döndürür.

Başka senaryolar buna bağlı olduğu için bu davranış değiştirilmez. Önceki örnekte, ek bir ondalık özniteliği ve hesaplama ekleyerek sorunu giderebilirsiniz.

Örneğin, üretim yapılandırması modelinde aşağıdaki öznitelikleri ayarlayabilirsiniz:

- Giriş (tamsayı)
- Yüzde (ondalık)
- ResultDecimal (ondalık)
- ResultInteger (tamsayı)

Bunun ardından aşağıdaki hesaplamaları ekleyebilirsiniz:

- *ResultDecimal* = *Giriş* × *Yüzde* ÷ 100
- *ResultInteger* = *ResultDecimal*
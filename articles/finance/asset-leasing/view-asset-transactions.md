---
title: Yükümlülük, varlık ve gider hareketlerini görüntüleme
description: Bu konu, kiralanan varlıkla ilgili hareketlerin nasıl görüntüleneceğini açıklamaktadır. Bu hareketler, kira yükümlülüğü hareketlerini ve deftere nakledilen icra gideri hareketlerini kapsar.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 76c7eff17df92b01317544112099e391fd05d105
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995380"
---
# <a name="view-liability-asset-and-expense-transactions"></a>Yükümlülük, varlık ve gider hareketlerini görüntüleme

[!include [banner](../includes/banner.md)]

Bu konu, kiralanan varlıkla ilgili hareketlerin nasıl görüntüleneceğini açıklamaktadır. Bu hareketler, kira yükümlülüğü hareketlerini ve deftere nakledilen icra gideri hareketlerini kapsar. Yükümlülük ve kullanım hakkı (ROU) varlığının defter değerleri birçok raporda kullanılır. Bunlar düzeltme değerlerini hesaplamada da kullanılırlar.

## <a name="liability-transactions"></a>Pasif hareketleri

Kira yükümlülük hareketlerini görüntülemek için **Kiralama özeti** sayfasında bir kiralama seçin ve kiralama kaydına eklenmiş defterleri açmak için **Defterler**'i seçin. İlk kabul, fatura veya faiz günlüğü deftere nakledildikten sonra **Yükümlülük hareketleri**'ni seçin.

**Yükümlülük hareketleri** sayfası , kiralama yükümlülüğünü artıran ve azaltan hareketleri gösterir. Bu sayfadaki negatif tutarlar standart uygulamadaki alacak hareketlerini gösterir. Tüm faiz tahakkukları negatif değerler olarak gösterilir ve toplam kiralama yükümlülüğünü artırır. Tüm kiralama düzeltmeleri, kiralama defterinin yapısına ve etkisine bağlı olarak pozitif veya negatif değer olarak gösterilir. Seçili kiralama için kiralama yükümlülüğünün net toplam bakiyesi sayfanın sol alt kısmında gösterilir.

## <a name="asset-transactions"></a>Kıymet hareketleri

Kiralama varlığı hareketlerini görüntülemek için **Kiralama özeti** sayfasında bir kiralama seçin ve kiralama kaydına eklenmiş kiralama defterlerini açmak için **Defterler**'i seçin. Ardından **Varlık hareketleri**'ni seçin.

**Varlık hareketi** sayfası, kiralama varlığını ve birikmiş amortisman hesaplarını artıran veya azaltan hareketleri gösterir. **Yükümlülük hareketleri** sayfasında olduğu gibi borçlar, pozitif değerler olarak gösterilir; alacaklar, negatif değerler olarak gösterilir. Deftere nakledilen ilk kabul ve ardından birikmiş amortisman sayfanın sol alt kısmında varlık bakiyesi olarak görüntülenir. 

## <a name="expenses-transactions"></a>Gider hareketleri

Kiralama gider hareketlerini görüntülemek için **Kiralama özeti** sayfasında bir kiralama seçin ve kiralama kaydına eklenmiş kiralama defterlerini açmak için **Defterler**'i seçin. Ardından **Gider hareketleri**'ni seçin.

**Gider hareketleri** sayfası, kiralama için deftere nakledilen tüm giderleri (ör. faiz giderleri, amortisman giderleri ve icra maliyetleri) gösterir.
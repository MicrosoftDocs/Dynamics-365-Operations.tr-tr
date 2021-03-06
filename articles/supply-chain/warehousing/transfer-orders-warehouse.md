---
title: Transfer emirleri için ambarlar ayarlama
description: Bu konu, transfer emirleri için ambarlar nasıl ayarlayabileceğinizi açıklar.
author: Mirzaab
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation,CustVendTransportPoint2Point
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 9e4ea0f9720bd4e5d2724b507aa32525ac25fa52
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823227"
---
# <a name="set-up-warehouses-for-transfer-orders"></a>Transfer emirleri için ambarlar ayarlama 

[!include [banner](../includes/banner.md)]

Ambarlar arası transfer emirlerini destekleyen bir hiyerarşi oluşturmak için ambar düzeylerini kullanabilirsiniz. Master planlama, bu kurulumu temel alarak madde gereksinimlerini tek tek ambar düzeyinde hesaplar ve bunları karşılamak üzere, atanmış bir kaynak ambardan planlı transfer emirleri oluşturur.

1.  **Stok yönetimi > Kurulum > Stok dökümü > Ambarlar**'a tıklayın.

2.  Stok yenilemesi yapmak istediğiniz ambarı seçin.

3.  **Master planlama** hızlı sekmesinde, **Yeniden doldurma** onay kutusunu seçin.

4.  **Ana ambar** alanında, stok yenileme ambarı olarak atamak istediğiniz ambarı seçin. Master planlama seçilen ambara ait transfer gereksinimini hesaplayıp atanmış **Ana ambar** noktasından bir planlı transfer emri oluşturur.
   
    > [!NOTE]
    > <P><STRONG>Dolum</STRONG> onay kutusunu alanını silerseniz, seçili ambara <STRONG>Ana ambar</STRONG>'a göre bir ambar düzeyi atanır, ancak <STRONG>Ana ambar</STRONG> bir dolum ambarı olarak ayarlanmaz.</P>

5.  Yeni kurulumu uygulamak için sayfayı kapatın.


> [!TIP]
> <P>Yeniden dolum için ambar atamak isterseniz, önce bu ambarı bir stok boyutu olarak <STRONG>Stok boyutu grupları</STRONG> sayfasında ayarlamalısınız. Bu sayfada <STRONG>Etkin</STRONG> alanını ve <STRONG>Boyuta göre kapsama planı</STRONG> alanını ambar için seçin.</P>

## <a name="set-up-transport-lead-time"></a>Taşıma sağlama süresi ayarlama

**Taşıma günü** sayfasında ambarlar arasındaki taşıma sağlama sürelerini de ayarlamanız gerekir. 
1. **Stok yönetimi > Kurulum > Dağıtım > Taşıma günleri**'ne gidin.
2. **Alım noktası** alanında, **ambar**'ı seçin.
3. **Sevkiyat ambarı**, **Alım ambarı** ve **Taşıma günleri**'ni seçin. 
4. (İsteğe bağlı) Taşıma şekline bağlı olarak taşıma süresini de **Teslimat türüne göre taşıma günleri** sekmesinde ayarlayabilirsiniz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
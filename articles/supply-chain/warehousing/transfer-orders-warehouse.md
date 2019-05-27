---
title: Transfer emirleri için ambarlar ayarlama
description: Bu konu, transfer emirleri için ambarlar nasıl ayarlayabileceğinizi açıklar.
author: Mirzaab
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 8111601cb2948c66097b0f5b2f261b7462b279f9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567090"
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

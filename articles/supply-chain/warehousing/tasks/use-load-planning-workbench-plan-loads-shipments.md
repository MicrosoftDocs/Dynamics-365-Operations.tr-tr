---
title: Yük planlama çalışma ekranını kullanarak yükleri ve sevkiyatları planlama
description: Bu konuda yük planlama çalışma alanını, bir satış siparişi için bir yükleme oluşturmada kullanma açıklanmaktadır.
author: ShylaThompson
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5c343ac75d3f2d587dc3298adc2ba9f4b3d08a7ce87a0dd8dd0791cf4d4e050
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723419"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Yük planlama çalışma ekranını kullanarak yükleri ve sevkiyatları planlama

[!include [banner](../../includes/banner.md)]

Bu konuda yük planlama çalışma alanını, bir satış siparişi için bir yükleme oluşturmada kullanma açıklanmaktadır. Bir önkoşul olarak satış siparişi ilk oluşturacağız. Bu yordamı ulaşım koordinatörü için günlük çalışmanın bir parçasıdır. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="create-a-sales-order"></a>Satış siparişi oluştur
1. **Gezinti bölmesi > Modüller > Alacak hesapları > Siparişler > Tüm satış siparişleri**'ne gidin.
2. **Yeni**'yi seçin.
3. **Müşteri hesabı** alanında, aramayı açmak için açılır menü düğmesini seçin.
4. **US-004** hesabını seçin.
5. **Tamam**'ı seçin.
6. **Madde numarası** alanında, açılır menü düğmesini seçerek aramayı açın.
7. **A0001** maddesini seçin. **A0001** taşıma yönetimi için etkindir.  
8. **Tesis** alanında, açılır menü düğmesini seçerek aramayı açın, ardından bir öğe seçin.
9. **Miktar** alanına bir sayı girin.
10. **ambar** alanına bu örnek için '24' yazın. Bu ambar taşımacılık ve gelişmiş ambar yönetimi için etkinleştirilir.  
11. **Kaydet**'i seçin.
12. Sayfayı kapatın.

## <a name="create-a-new-load"></a>Yeni bir yük oluştur
1. **Gezinti bölmesi > Modüller > Taşıma yönetimi > Planlama > Yük planlama çalışma ekranı**'na gidin.
2. **Satış satırları** sekmesini seçin. Şimdi oluşturduğunuz satış siparişi için yük oluşturun. Yükler satınalma siparişlerinin, transfer emirleri ve satış siparişlerinin arz ve talebine göre oluşturulabilirler  
3. Eylem Bölmesinde **Arz ve talep**'i seçin.
4. **Yeni yüke**'yi seçin.
5. **Yük şablonu kodu** alanında aramayı açmak için açılır menü düğmesini seçin. Yük şablonu, ağırlık ve hacim için tüm yükte geçerli olacak maksimum ölçümleri belirler. Yük şablonu örneğin bir konteyner veya kamyonun boyutunu temsil edebilir. Bir madde seçin.
6. **Tamam**'ı seçin.

## <a name="rate-and-route-the-load"></a>Yük için orana ve rota
1. **Oran ve rota**'yı seçin.
2. **Rota çalışma ekranı oranı**'nı seçin.
3. **Atölye oranı**'nı seçin.
4. Listede, istenen kaydı bulun ve seçin.
5. **Ata**'yı seçin.
6. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
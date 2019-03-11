---
title: Yük planlama çalışma ekranını kullanarak yükleri ve sevkiyatları planlama
description: Bu yordam, yük planlama çalışma alanını, bir satış siparişi için bir yükleme oluşturmada nasıl kullanacağınızı gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1927cff48beb30f934bd066c32ab48dfb9d06f74
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "343915"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Yük planlama çalışma ekranını kullanarak yükleri ve sevkiyatları planlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, yük planlama çalışma alanını, bir satış siparişi için bir yükleme oluşturmada nasıl kullanacağınızı gösterir. Bir önkoşul olarak satış siparişi ilk oluşturacağız. Bu yordamı ulaşım koordinatörü için günlük çalışmanın bir parçasıdır. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="create-a-sales-order"></a>Satış siparişi oluştur
1. Alacak hesapları > Siparişler > Tüm satış siparişleri'ne gidin.
2. Yeni'ye tıklayın.
3. Müşteri hesabı alanında, açılır menü düğmesine tıklayarak açılır menü düğmesine tıklayın.
4. Hesap US-004'ü seçin.
5. Tamam'ı tıklatın.
6. Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.
7. Madde A0001'i seçin.
    * A0001, taşıma yönetimi için etkindir.  
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. Miktar alanına bir sayı girin.
10. Ambar alanına '24' yazın.
    * Bu örnekte ambar 24'ü seçin. Bu ambar taşımacılık ve gelişmiş ambar yönetimi için etkinleştirilir.  
11. Kaydet'e tıklayın.
12. Sayfayı kapatın.

## <a name="create-a-new-load"></a>Yeni bir yük oluştur
1. Taşıma yönetimi > Planlama > Yük planlama çalışma ekranına gidin.
2. Satış vergisi satırını tıklatın.
    * Şimdi oluşturduğunuz satış siparişi için yük oluşturacaksınız. Yükler satınalma siparişlerinin, transfer emirleri ve satış siparişlerinin arz ve talebine göre oluşturulabilirler  
3. Eylem Bölmesinde, Arz ve Talep'e tıklayın.
4. Yeni yüke'ye tılayın.
5. Şablon kimliği yükle alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Yük şablonu, ağırlık ve hacim için tüm yükte geçerli olacak maksimum ölçümleri belirler. Yük şablonu örneğin bir konteyner veya kamyonun boyutunu temsil edebilir.  
6. Listede, seçili satırdaki bağlantıya tıklayın.
7. Tamam'a tıklayın.

## <a name="rate-and-route-the-load"></a>Yük için orana ve rota
1. Oran ve rota'ya tıklayın.
2. Rota çalışma ekranı oranı'na tıklayın.
3. Atölye oranı'na tıklayın.
4. Listede, istenen kaydı bulun ve seçin.
5. Atama'yı tıklatın.
6. Sayfayı kapatın.
7. Sayfayı kapatın.


---
title: Şirketlerarası plan oluşturma
description: Bu yordam şirketlerarası plan oluşturmayı gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d378a89bbb4de6d67db0019dc72a27945d50c4e9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "333749"
---
# <a name="create-an-intercompany-plan"></a>Şirketlerarası plan oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam şirketlerarası plan oluşturmayı gösterir. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="set-up-an-intercompany-planning-group"></a>Şirketlerarası planlama grubu ayarlama 
1. Şirketlerarası planlama grupları'na gidin.
    * Master planlama > Kurulum > Şirketlerarası planlama grupları  
2. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, İsim alanı üzerinde '10' değerini girerek filtreleme yapın.
3. Listede, seçili satırı işaretleyin.
4. Sil'i tıklatın.
    * Bu adım, şirketlerarası planlama çalışmasını kısaltmak için gereklidir.   Şirketlerarası planlama, en düşük planlama serisinden başlayarak bir planlama grubu içindeki tüm şirketlerde master planlamayı çalıştırır.  
5. Evet'i tıklatın.
6. Sayfayı kapatın.

## <a name="create-an-intercompany-plan"></a>Şirketlerarası plan oluşturma
1. Şirketlerarası master planlama'ya tıklayın.
    * Bu, Master planlama çalışma alanında olur.  
2. Şirketlerarası planlama grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.
3. Listede, seçili satırdaki bağlantıya tıklayın.
    * Şirketlerarası planlama grubu 10'u seçin.  
4. Şirketlerarası planlama tekrar sayısı alanına '2' yazın.
    * Şirketlerarası planlama grubu 10 iki üyeye sahip. Gecikmeleri kaynak şirketten (USMF) müşteri şirkete (DEMF) yaymak için, iki şirkette de şirketlerarası işlevini iki kez çalıştırmanız gerekir. İlk tekrar, talebi yayar ve kaynak şirketteki (USMF) gecikmeleri tanımlar. İkinci tekrar, gecikmeleri USMF'den DEMF'ye yayar.  
5. İlk tekrarlama alanında bir seçenek belirleyin.
6. İlk tekrarlama alanında 'Yeniden oluşturma' seçeneğini belirleyin.
7. Sonraki tekrarlamalar alanında 'Yeniden oluşturma' seçeneğini belirleyin.
8. İş parçacığı sayısı alanına bir rakam girin.
    * Bu, planlama için kullanılan paralel iş parçacıklarının sayısını temsil eder.  
9. Tamam'a tıklayın.

## <a name="view-the-result-of-the-plan"></a>Planın sonucunu görüntüleme
1. Plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.
2. Listede, seçili satırdaki bağlantıya tıklayın.
    * StaticPlan için bağlantıya tıklayın. USMF şirketinde olmanız gerekir.  
3. Planlı siparişler'e tıklayın.


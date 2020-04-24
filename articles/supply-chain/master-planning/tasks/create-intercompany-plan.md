---
title: Şirketlerarası plan oluşturma
description: Bu yordam şirketlerarası plan oluşturmayı gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a64817f140d8a2302b3b2c2d1e55de103a5bb36
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209709"
---
# <a name="create-an-intercompany-plan"></a>Şirketlerarası plan oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam şirketlerarası plan oluşturmayı gösterir. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="set-up-an-intercompany-planning-group"></a>Şirketlerarası planlama grubu ayarlama 
1. **Gezinti bölmesinde**, **Modüller > Master planlama > Kurulum > Şirketlerarası planlama grupları**'na gidin. 
2. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, İsim alanı üzerinde '10' değerini girerek filtreleme yapın.
3. Listede, seçili satırı işaretleyin.
4. **Sil** öğesini tıklayın. Bu adım, şirketlerarası planlama çalışmasını kısaltmak için gereklidir.   Şirketlerarası planlama, en düşük planlama serisinden başlayarak bir planlama grubu içindeki tüm şirketlerde master planlamayı çalıştırır.  
5. **Evet** seçeneğini tıklatın.
6. Sayfayı kapatın.

## <a name="create-an-intercompany-plan"></a>Şirketlerarası plan oluşturma
1. **Gezinti bölmesinde**, **Modüller > Master planlama > Çalışma alanları > Master planlama**'ya gidin.
2. **Şirketlerarası master planlama**'ya tıklayın.  
3. **Şirketlerarası planlama grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
4. Listede, seçili satırdaki bağlantıya tıklayın. Şirketlerarası planlama grubu 10'u seçin.  
5. **Şirketlerarası planlama tekrar sayısı** alanına '2' yazın. Şirketlerarası planlama grubu 10 iki üyeye sahip. Gecikmeleri kaynak şirketten (USMF) müşteri şirkete (DEMF) yaymak için, iki şirkette de şirketlerarası işlevini iki kez çalıştırmanız gerekir. İlk tekrar, talebi yayar ve kaynak şirketteki (USMF) gecikmeleri tanımlar. İkinci tekrar, gecikmeleri USMF'den DEMF'ye yayar.  
6. **İlk tekrarlama** alanında 'Yeniden oluşturma' seçeneğini belirleyin.
7. **Sonraki tekrarlamalar** alanında 'Yeniden oluşturma' seçeneğini belirleyin.
8. **İş parçacığı sayısı** alanına bir rakam girin. Bu, planlama için kullanılan paralel iş parçacıklarının sayısını temsil eder.  
9. **Tamam**'a tıklayın.

## <a name="view-the-result-of-the-plan"></a>Planın sonucunu görüntüleme
1. **Plan** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
2. Listede, seçili satırdaki bağlantıya tıklayın. StaticPlan için bağlantıya tıklayın. USMF şirketinde olmanız gerekir.  
3. **Planlı siparişler**'e tıklayın.


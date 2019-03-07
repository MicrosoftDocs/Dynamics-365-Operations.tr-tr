---
title: Boyut tabanlı ana ürün için ürün reçetesi oluşturma
description: Bu prosedür için bu sekiz kayıt sırasındaki, önceki 4 kılavuzu tamamlamış olmanız gerekir.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19578f78c11bf0537708e8d516d478f00b13fa95
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "349757"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Boyut tabanlı ana ürün için ürün reçetesi oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu prosedür için bu sekiz kayıt sırasındaki, önceki 4 kılavuzu tamamlamış olmanız gerekir. İlk 4 kayıtta bu prosedürün tamamlanması için gereken verileri kurulur. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu görev tipik olarak ürün tasarımcısı tarafından ele alınır.


## <a name="select-the-product"></a>Ürün seçme
1. Serbest bırakılan ürün bakımı'na tıklayın.
2. Sevk edilen ürünler'e tıklayın.
3. Listede, seçili satırı işaretleyin.
    * Bu sıradaki ilk görev kılavuzunda oluşturduğunuz, boyut tabanlı yapılandırma teknolojisiyle, serbest bırakılan ürün mastarını bulun.  
4. Eylem Bölmesinde, Mühendis öğesine tıklayın.
5. BOM sürümlerini tıklayın.

## <a name="create-new-bom-and-bom-version"></a>Yeni BOM ve BOM sürümünü oluşturma
1. Yeni'ye tıklayın.
2. BOM ve BOM sürümünü tıklayın.
3. İsim alanına bir değer yazın.
    * Bir saha ayarlanması  
    * Bu prosedürde BOM için belirli bir saha ayarlamıyoruz.  
4. Tamam'a tıklayın.
5. Yeni'ye tıklayın.
    * Bu prosedürde BOM'a dört satır ekleyeceğiz. İki satır, kablo seçeneklerini temsil ederken; iki satır, dolap seçeneklerini temsil eder.  
6. Listede, seçili satırı işaretleyin.
7. Madde numarası alanında bir değer girin veya seçin.
    * A0001, HDMI 6' Kablo madde numarasını seçin.  
8. Yapılandırma grubu alanında bir değer girin veya seçin.
    * Bu sıradaki kılavuz 4'te oluşturulan Kablo yapılandırma grubunu seçin.  
9. Yeni'ye tıklayın.
    * A0002, HDMI 12' Kablo madde numarasını seçin.  
10. Listede, seçili satırı işaretleyin.
11. Madde numarası alanında bir değer girin veya seçin.
12. Yapılandırma grubu alanında bir değer girin veya seçin.
    * Kablo yapılandırma grubunu tekrar seçin.  
13. Yeni'ye tıklayın.
14. Listede, seçili satırı işaretleyin.
15. Madde numarası alanında bir değer girin veya seçin.
    * D0002 Dolap madde numarasını seçin.  
16. Yapılandırma grubu alanında bir değer girin veya seçin.
    * Bu BOM satırı için Dolap yapılandırma grubunu seçin.  
17. Yeni'ye tıklayın.
18. Listede, seçili satırı işaretleyin.
19. Madde numarası alanında bir değer girin veya seçin.
    * Son BOM satırı olarak, M0007 Standart Dolap madde numarasını seçin.  
20. Yapılandırma grubu alanında bir değer girin veya seçin.
    * Son BOM satırı için Dolap yapılandırma grubunu seçin.  

## <a name="approve-and-activate"></a>Onayla ve etkinleştir
1. Sayfayı kapatın.
2. Onayla’yı tıklatın.
3. Onaylayan alanında bir değer girin veya bir değer seçin.
4. Ürün reçetesini de onaylamak ister misiniz? sorusunu Evet olarak yanıtlayın. alanda kullandığınızda otomatik olarak işaretlenir.
5. Tamam'a tıklayın.
6. Etkinleştir'i tıklatın.


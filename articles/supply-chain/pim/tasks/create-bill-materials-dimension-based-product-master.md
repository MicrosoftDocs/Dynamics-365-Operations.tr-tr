---
title: Boyut tabanlı ana ürün için ürün reçetesi oluşturma
description: Bu prosedür için bu sekiz kayıt sırasındaki, önceki 4 kılavuzu tamamlamış olmanız gerekir.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f86625821f8a01a6d4949f9dca538a279f52ce9c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565600"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Boyut tabanlı ana ürün için ürün reçetesi oluşturma

[!include [banner](../../includes/banner.md)]

Bu prosedür için bu sekiz kayıt sırasındaki, önceki 4 kılavuzu tamamlamış olmanız gerekir. İlk 4 kayıtta bu prosedürün tamamlanması için gereken verileri kurulur. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu görev tipik olarak ürün tasarımcısı tarafından ele alınır.

## <a name="select-the-product"></a>Ürün seçme

1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. Listede, seçili satırı işaretleyin.
    * Bu sıradaki ilk görev kılavuzunda oluşturduğunuz, boyut tabanlı yapılandırma teknolojisiyle, serbest bırakılan ürün mastarını bulun.  
1. Eylem Bölmesi'nde **Mühendis**'i seçin.
1. **Ürün Reçetesi sürümleri**'ni seçin.

## <a name="create-new-bom-and-bom-version"></a>Yeni BOM ve BOM sürümünü oluşturma

1. **Yeni**'yi seçin.
1. **Ürün Reçetesi ve Ürün Reçetesi sürümü**'nü seçin.
1. **Ad** alanına bir değer yazın.
    * Bir saha ayarlanması  
    * Bu prosedürde BOM için belirli bir saha ayarlamıyoruz.  
1. **Tamam**'ı seçin.
1. **Yeni**'yi seçin.
    * Bu prosedürde BOM'a dört satır ekleyeceğiz. İki satır, kablo seçeneklerini temsil ederken; iki satır, dolap seçeneklerini temsil eder.  
1. Listede, seçili satırı işaretleyin.
1. **Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin.
    * A0001, HDMI 6' Kablo madde numarasını seçin.  
1. **Yapılandırma grubu** alanında bir değer girin veya seçin.
    * Bu sıradaki kılavuz 4'te oluşturulan kablo yapılandırma grubunu seçin.  
1. **Yeni**'yi seçin.
    * A0002, HDMI 12' Kablo madde numarasını seçin.  
1. Listede, seçili satırı işaretleyin.
1. **Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin.
1. **Yapılandırma grubu** alanında bir değer girin veya seçin.
    * Kablo yapılandırma grubunu yeniden seçin.  
1. **Yeni**'yi seçin.
1. Listede, seçili satırı işaretleyin.
1. **Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin.
    * D0002 Dolap madde numarasını seçin.  
1. **Yapılandırma grubu** alanında bir değer girin veya seçin.
    * Bu Ürün Reçetesi satırı için dolap yapılandırma grubunu seçin.  
1. **Yeni**'yi seçin.
1. Listede, seçili satırı işaretleyin.
1. **Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin.
    * Son BOM satırı olarak, M0007 Standart Dolap madde numarasını seçin.  
1. **Yapılandırma grubu** alanında bir değer girin veya seçin.
    * Son Ürün Reçetesi satırı için Dolap yapılandırma grubunu seçin.  

## <a name="approve-and-activate"></a>Onayla ve etkinleştir

1. Sayfayı kapatın.
1. **Onayla**'yı seçin.
1. **Onaylayan** alanında bir değer girin veya bir değer seçin.
1. **Ürün reçetesini de onaylamak ister misiniz?** sorusunu *Evet* olarak yanıtlayın.
1. **Tamam**'ı seçin.
1. **Etkinleştir**'i seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
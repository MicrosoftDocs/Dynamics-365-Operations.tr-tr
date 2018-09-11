--- 
title: Ek amortisman ayarlama
description: "Bu yordam, özel amortisman payının nasıl oluşturulacağını ve bir sabit kıymet defteriyle nasıl ilişkilendirileceğini gösterir."
author: saraschi2
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7e6ebb13084626b477b6e0b24acdc09e2c0d3d6d
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-bonus-depreciation"></a>Ek amortisman ayarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, özel amortisman payının nasıl oluşturulacağını ve bir sabit kıymet defteriyle nasıl ilişkilendirileceğini gösterir. Muhasebeci rolünü ve USMF adlı tüzel kişilik için tanıtım verilerini kullanır.


## <a name="create-a-special-depreciation-allowance"></a>Özel amortisman payı oluşturun
1. Sabit kıymetler > Kurulum > Özel amortisman payı'na gidin.
2. Yeni'ye tıklayın.
3. Özel amortisman payı alanına bir değer girin.
4. Açıklama alanına bir değer girin.
5. Yüzde alanına bir sayı girin.
    * Yüzde gösterilmediyse bir tutar ayarlayın.  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a>Özel amortisman payını bir sabit kıymet grubu defteriyle ilişkilendirme
1. Sabit kıymetler > Kurulum > Sabit kıymet grupları'na gidin.
2. Listede, özel amortisman payıyla ilişkili sabit kıymet grubunu seçin.
3. Defterler'e tıklayın.
4. Listede, özel amortisman payıyla ilişkili defteri seçin.
5. Özel amortisman payı'na tıklayın.
6. Yeni'ye tıklayın.
7. Özel amortisman payı alanına bir değer girin veya seçin.
    * Yüzde veya Tutar için varsayılan değer, özel amortisman payı kurulumundan alınır.  
8. Öncelik alanına bir sayı girin.



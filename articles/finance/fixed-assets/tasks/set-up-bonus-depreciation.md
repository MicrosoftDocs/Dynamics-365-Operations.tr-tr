---
title: Ek amortisman ayarlama
description: Bu yordam, özel amortisman payının nasıl oluşturulacağını ve bir sabit kıymet defteriyle nasıl ilişkilendirileceğini gösterir.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6627e7fa9a1eb1a9131ec7e2c3cc823b49b286cc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257573"
---
# <a name="set-up-bonus-depreciation"></a>Ek amortisman ayarlama

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
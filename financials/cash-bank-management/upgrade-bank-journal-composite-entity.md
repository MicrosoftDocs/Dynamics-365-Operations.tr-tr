---
title: "Banka günlüğü birleşik varlığını güncelleştirme"
description: "Ek BankaHareketTürü alanını birleşik BankaGünlükVarlığı'na eklemek için aşağıdaki adımlar gereklidir."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 43413aad9d537e518f7276ccab11ce01d23cf13f
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017

---

# <a name="update-the-bank-journal-composite-entity"></a>Banka günlüğü birleşik varlığını güncelleştirme

[!include[banner](../includes/banner.md)]


Ek BankaHareketTürü alanını birleşik BankaGünlükVarlığı'na eklemek için aşağıdaki adımlar gereklidir.

Ek BankaHareketTürü alanını birleşik BankaGünlükVarlığı'na eklemek için aşağıdaki adımları kullanın.

1.  Aşağıdaki banka günlüğü birleşik varlıklarını, varlıkları ve aşamalandırma tablolarını derleyin ve eşitleyin:
    -   Birleşik Varlık\\BankaGünlükVarlığı
    -   Varlık\\BankaGünlüğüBaşlıkVarlığı
    -   Varlık\\BankaGünlüğüSatırVarlığı
    -   Tablo\\BankaGünlüğüBaşlıkHazırlığı
    -   Tablo\\BankaGünlüğüSatırHazırlığı

2.  Veri yönetimi\\veri projeleri
    -   **Kaynak Veri**yerleşiminde **Banka Hareketi**türünü gösterin.
        -   Kaynak veri biçimi = XML Öğesi
        -   Varlık adı = Banka Günlüğü
        -   Yükleme veri dosyası = yeni sürüm ÖrnekBankaGünlüğüBirleşikVarlığı.xml
        -   Mevcut dosyanın üzerine yazmak için **Evet**'e tıklayın.
        -   Eşlemeyi sıfırdan oluşturmak için **Evet**'e tıklayın.
        -   Banka Hareketi Türü'nün eşleştiğini doğrulayın.
            -   Satır varlığında **Haritayı görüntüle**'ye tıklayın.
            -   Banka Hareket Türü'nün Kaynak'tan Aşamalandırma'ya eşleştiğini doğrulayın.

3.  Yeni ekstreyi içe aktarın.






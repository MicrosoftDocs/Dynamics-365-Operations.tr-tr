---
title: Banka günlüğü bileşik varlığını güncelleme
description: Bu makalede, ek BankTransactionType alanını birleşik BankJournalEntity öğesine eklemek için gereken adımlar listelenmektedir.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1855f9680ba6bcf8eb46608882a128b4a21f0dac
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715303"
---
# <a name="update-the-bank-journal-composite-entity"></a>Banka günlüğü bileşik varlığını güncelleme

[!include [banner](../includes/banner.md)]

Bu makalede, ek BankTransactionType alanını birleşik BankJournalEntity öğesine eklemek için gereken adımlar listelenmektedir.

Ek BankaHareketTürü alanını birleşik BankaGünlükVarlığı'na eklemek için aşağıdaki adımları kullanın.

1.  Aşağıdaki banka günlüğü birleşik varlıklarını, varlıkları ve aşamalandırma tablolarını derleyin ve eşitleyin:
    -   Birleşik Varlık\\BankaGünlükVarlığı
    -   Varlık\\BankaGünlüğüBaşlıkVarlığı
    -   Varlık\\BankaGünlüğüSatırVarlığı
    -   Tablo\\BankaGünlüğüBaşlıkHazırlığı
    -   Tablo\\BankaGünlüğüSatırHazırlığı

2.  Veri yönetimi\\veri projeleri
    -   **Kaynak Veri** yerleşiminde **Banka Hareketi** türünü gösterin.
        -   Kaynak veri biçimi = XML Öğesi
        -   Varlık adı = Banka Günlüğü
        -   Yükleme veri dosyası = yeni sürüm ÖrnekBankaGünlüğüBirleşikVarlığı.xml
        -   Mevcut dosyanın üzerine yazmak için **Evet**'e tıklayın.
        -   Eşlemeyi sıfırdan oluşturmak için **Evet**'e tıklayın.
        -   Banka Hareketi Türü'nün eşleştiğini doğrulayın.
            -   Satır varlığında **Haritayı görüntüle**'ye tıklayın.
            -   Banka Hareket Türü'nün Kaynak'tan Aşamalandırma'ya eşleştiğini doğrulayın.

3.  Yeni ekstreyi içe aktarın.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]

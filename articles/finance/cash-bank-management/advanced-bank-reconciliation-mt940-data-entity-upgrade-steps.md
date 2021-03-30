---
title: Gelişmiş banka mutabakatı MT940 İçe Aktarma – Bileşik veri varlığı yükseltme
description: MT940 biçimini desteklemek için banka ekstresi içe aktarma varlığına bir sıra numarası eklenmesi gerekir.
author: panolte
manager: AnnBe
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ee5ad476b10077592c61f6827b5596a1b3e66cd6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217446"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>Gelişmiş banka mutabakatı MT940 İçe Aktarma – Bileşik veri varlığı yükseltme

[!include [banner](../includes/banner.md)]

MT940 biçimini desteklemek için banka ekstresi içe aktarma varlığına bir sıra numarası eklenmesi gerekir. 

MT940 biçimini desteklemesi için banka ekstresi içe aktarma varlığını eklemek amacıyla aşağıdaki adımları kullanın.

1.  Aşağıdakileri derleyin ve eşitleyin:
    -   Birleşik Varlık\\BankStatementImportEntity
    -   Varlık\\BankStatementBalanceEntity
    -   Varlık\\BankStatementDocumentEntity
    -   Varlık\\BankStatementEntity
    -   Varlık\\BankStatementLineEntity
    -   Tablolar\\BankStatementStaging

2.  Veri yönetimi\\veri projeleri.
    1.  MT940 içe aktarma projeleri
        1.  XSLT'yi değiştirin.
            -   **Eşlemeyi görüntüle**'ye tıklayın.
            -   Banka ekstresi belgesinde **Eşlemeyi görüntüle**'ye tıklayın.
            -   **Dönüşümler**'e tıklayın
            -   BankReconciliation-to-Composite.xslt dosyasını silin.
            -   BankReconiliation-to-Composite.xsl dosyasının yeni sürümünü ekleyin.

        2.  **Kaynak Veri** düzeninde **Sıra numarası**'nı gösterin.
            1.  Kaynak veri biçimi = XML Öğesi.
            2.  Varlık adı = Banka ekstreleri.
            3.  Yükleme veri dosyası = yeni sürüm ÖrnekBankaBirleşikVarlığı.xml.
            4.  Mevcut dosyanın üzerine yazmak için **Evet**'e tıklayın.
            5.  Yeni bir eşleme oluşturmak için **Evet**'e tıklayın.
            6.  **SıraNumarası**'nın eşleştiğini doğrulayın.
                -   Ekstre varlığında **Eşlemeyi Görüntüle**'ye tıklayın.
                -   **SıraNumarası**'nın Kaynak'tan Aşamalandırma'ya eşleştiğini doğrulayın.

3.  Yeni ekstreyi içe aktarın.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
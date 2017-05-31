---
title: "Gelişmiş banka mutabakatı MT940 İçe Aktarma – Bileşik veri varlığı yükseltme"
description: "MT940 biçimini desteklemek için banka ekstresi içe aktarma varlığına bir sıra numarası eklenmesi gerekir."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 672697254c1bf06e193a51c5c7c83c467a220ce8
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>Gelişmiş banka mutabakatı MT940 İçe Aktarma – Bileşik veri varlığı yükseltme

[!include[banner](../includes/banner.md)]


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






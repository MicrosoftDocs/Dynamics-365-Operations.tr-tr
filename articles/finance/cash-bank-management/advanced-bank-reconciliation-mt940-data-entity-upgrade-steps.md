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
ms.openlocfilehash: 4d3bd54f0f2329c8c0602171a7f3c1ca444672b3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985423"
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





---
title: Excel şablonlarını yeniden uygulayarak Elektronik raporlama biçimlerini değiştirme
description: Bu konuda, değiştirilen bir Excel şablonunu yeniden uygulayarak iş belgeleri oluşturmak için kullanılan Elektronik raporlama biçimini nasıl değiştirebileceğiniz açıklanmaktadır.
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d828412e0d804acf6e6141778512e899bc78a7d
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092856"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a>Excel şablonlarını yeniden uygulayarak Elektronik raporlama biçimlerini değiştirme

[!include [banner](../includes/banner.md)]

Elektronik raporlama (ER) aracı, elektronik biçimde iş belgeleri oluşturmak için kullanılır. Bir iş belgesi oluşturmak için bir ER biçimi oluşturmanız, ardından iş belgesinin düzenini tanımlamak için ER tasarımcısını kullanmanız ve buna dahil edilmesi gereken bilgileri belirtmeniz gerekir. Daha sonra iş belgeleri oluşturmak için ER biçimini çalıştırabilirsiniz.

ER aracı Microsoft Excel dosyaları biçiminde iş belgeleri oluşturmak için kullanılabilir. Bu belgeler için bir Excel belgesini şablon olarak kullanabilirsiniz. ER tasarımcısında belge düzenini tanımlamak için, kullanmak istediğiniz Excel belgesinin içeriklerini şablon olarak tanımlanan ER biçimine aktarabilirsiniz. Ayrıntılı bilgi edinmek ve bu senaryoyu uygulamak için **ER OPENXML biçiminde raporlar oluşturmak için bir yapılandırma tasarlama** görev kılavuzunu (7.5.4.3 Al/BT hizmeti geliştir/çözüm bileşenleri (10677) iş işleminin parçası ) oynatın.

Bir iş belgesi için bir şablon olarak kullanılan Excel belgesinde düzenleme yaparsanız, yeni ER işlevi güncelleştirilen şablonu ER biçimine yeniden uygulamanıza olanak tanır. ER biçimi daha sonra güncelleştirilir ve güncelleştirilen şablona bağlı kalır. Bu işlev hakkında daha fazla bilgi için **ER Bir Excel şablonu uygulayarak bir biçimi değiştirme** (7.5.5.3 Al/BT hizmeti geliştirme/çözüm bileşenleri (10683) iş sürecinin parçası olarak) görev kılavuzunu oynatın. Görev kılavuzunda güncelleştirilmiş bir şablonu içe aktardığınız adımda, şablon olarak Ödeme Raporu Excel dosyasının değiştirilen şablonunu (SampleVendPaymWsReport2) kullanın.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Excel şablonlarını yeniden uygulayarak Elektronik raporlama biçimlerini değiştirme
description: Bu makalede, değiştirilen bir Excel şablonunu yeniden uygulayarak iş belgeleri oluşturmak için kullanılan Elektronik raporlama biçimini nasıl değiştirebileceğiniz açıklanmaktadır.
author: kfend
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
ms.openlocfilehash: 02423a75d96bef0452b8555f8c7a9f0aca0b6771
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283543"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a>Excel şablonlarını yeniden uygulayarak Elektronik raporlama biçimlerini değiştirme

[!include [banner](../includes/banner.md)]

Elektronik raporlama (ER) aracı, elektronik biçimde iş belgeleri oluşturmak için kullanılır. Bir iş belgesi oluşturmak için bir ER biçimi oluşturmanız, ardından iş belgesinin düzenini tanımlamak için ER tasarımcısını kullanmanız ve buna dahil edilmesi gereken bilgileri belirtmeniz gerekir. Daha sonra iş belgeleri oluşturmak için ER biçimini çalıştırabilirsiniz.

ER aracı Microsoft Excel dosyaları biçiminde iş belgeleri oluşturmak için kullanılabilir. Bu belgeler için bir Excel belgesini şablon olarak kullanabilirsiniz. ER tasarımcısında belge düzenini tanımlamak için, kullanmak istediğiniz Excel belgesinin içeriklerini şablon olarak tanımlanan ER biçimine aktarabilirsiniz. Ayrıntılı bilgi edinmek ve bu senaryoyu uygulamak için **ER OPENXML biçiminde raporlar oluşturmak için bir yapılandırma tasarlama** görev kılavuzunu (7.5.4.3 Al/BT hizmeti geliştir/çözüm bileşenleri (10677) iş işleminin parçası ) oynatın. Excel şablonunu içeri aktardığınız görev kılavuzu adımında, Ödeme Raporu Excel dosyasının başlangıçtaki şablonunu [SampleVendPaymWsReport](https://download.microsoft.com/download/e/6/b/e6bb79f0-cc08-44af-96fa-49c7929d4fb8/SampleVendPaymWsReport.xlsx) kullanın.

Bir iş belgesi için bir şablon olarak kullanılan Excel belgesinde düzenleme yaparsanız, yeni ER işlevi güncelleştirilen şablonu ER biçimine yeniden uygulamanıza olanak tanır. ER biçimi daha sonra güncelleştirilir ve güncelleştirilen şablona bağlı kalır. Bu işlev hakkında daha fazla bilgi için **ER Bir Excel şablonu uygulayarak bir biçimi değiştirme** (7.5.5.3 Al/BT hizmeti geliştirme/çözüm bileşenleri (10683) iş sürecinin parçası olarak) görev kılavuzunu oynatın. Görev kılavuzunda güncelleştirilmiş bir şablonu içeri aktardığınız adımda, Ödeme Raporu Excel dosyasının değiştirilen şablonunu [SampleVendPaymWsReport2](https://download.microsoft.com/download/3/1/0/3104d397-c9c5-4227-b68e-f98625313801/SampleVendPaymWsReport2.xlsx) kullanın.

## <a name="additional-resources"></a>Ek kaynaklar

[Şablon güncelleştirme](er-fillable-excel.md#update-a-template)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

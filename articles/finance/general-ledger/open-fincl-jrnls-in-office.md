---
title: Office'te mali günlük şablonlarını açma
description: Bu makalede, bir Microsoft Excel şablonu kullanarak özel mali günlükler oluşturduğunuzda oluşabilecek sorunlar açıklanmaktadır.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a29ab1cb2980ebfed6c6fa6409538bc802849156
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896361"
---
# <a name="open-financial-journal-templates-in-office"></a>Office'te mali günlük şablonlarını açma

[!include [banner](../includes/banner.md)]

Bu makalede, bir Microsoft Excel şablonu kullanarak özel mali günlükler oluşturduğunuzda oluşabilecek sorunlar açıklanmaktadır.

## <a name="symptom"></a>Belirti

Mali günlükler için özel bir Excel şablonu oluşturdunuz ancak **Satırları Excel'de aç** menüsünde görünmüyor. Alternatif olarak, menüde görünüyor ama seçtiğinizde farklı bir şablon açılıyor.

## <a name="resolution"></a>Çözüm

Varsayılan Excel'de Aç işlevi, **Excel'de Aç** menüsünde hangi Office şablonlarının veya veri varlıklarının seçenek olarak görüneceğini belirlemek için geçerli sayfanın kök veri kaynağını (tablo) kullanır. Bu davranış, mali günlükler için ideal bir deneyim değildir çünkü mali günlükler, diğer birçok günlük türünün kök veri kaynağı olarak aynı tabloları (LedgerJournalTable ve LedgerJournalTrans) kullanır.

Mali günlükler için Excel'de Satırları Aç işlevi, yevmiye defteri veya ödeme günlüğü gibi şu anda bağlamında çalıştığınız günlük için tasarlanmış şablonları göstermek üzere tasarlanmıştır. Örneğin, satıcı ödeme günlüğüyle kullanılması amaçlanan bir şablon, birincil hesabınızı satıcı hesabı olarak zorlamak için tasarlanacak.

Şablonu **Satırları Excel'de Aç** ve **Excel Aç** menülerinde kullanılabilir olacak şekilde tanıtmak istiyorsanız kolay bir geliştirici deneyimi **LedgerIJournalExcelTemplate** arabirimini uygulamak ve **DocuTemplateRegistrationBase** sınıfını genişletmektir. Bu yaklaşımın birçok örneği sistemde uygulanmaktadır. Referans için kullanılabilecek bir örnek, yevmiye defteri (veya günlük tutulan günlük) için oluşturulan **LedgerDailyJournalExcelTemplate** arabirimidir.

Şablonunuz için **LedgerIJournalExcelTemplate** arabirimi uygulandığında **Satırları Excel'de aç** menüsü şablonları günlüğünüzün günlük türüne göre filtreler ve yalnızca bu günlük için kullanılabilen şablonları gösterir. Arabirim ayrıca, hesap türü gereksinimlerini karşılamıyorsa bir şablonun günlük için açılamamasını sağlayan bir doğrulama yöntemi sağlar. Örneğin, hesap türünün **Satıcı** veya **Kayıt Defter** türünde olması gerektiğini belirtebilirsiniz.

Bu işlevsellik hakkında daha fazla bilgi için bkz. [Satırları Excel'de Aç menüsüne şablonlar ekleme](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).

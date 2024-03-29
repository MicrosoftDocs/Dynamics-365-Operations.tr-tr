---
title: Tahsisatları işleme
description: Bu makalede tahsisatlar, Microsoft Dynamics 365 Finance'te tahsisatları işleme seçenekleri ve bütçe planlamasında tahsisatların nasıl kullanılabileceği hakkında bilgi verilmektedir. Tahsisatlar, tutarları birden fazla genel muhasebe hesabı birleşimleri arasında dağıtmak için kullanılır. Gelir ve giderlerin muhasebede doğru nesneye yazılmasını sağlamaya yardımcı olurlar.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: kfend
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0629b32d39f4d74ec37eebe92b92e0b186b5fce2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877997"
---
# <a name="process-allocations"></a>Tahsisatları işleme

[!include [banner](../includes/banner.md)]

Bu makalede tahsisatlar, tahsisatları işleme seçenekleri ve bütçe planlamasında tahsisatların nasıl kullanılabileceği hakkında bilgi verilmektedir. Tahsisatlar, tutarları birden fazla genel muhasebe hesabı birleşimleri arasında dağıtmak için kullanılır. Gelir ve giderlerin muhasebede doğru nesneye yazılmasını sağlamaya yardımcı olurlar.

Aşağıdaki özellikler bu işlemi destekler:

-   Muhasebe dağılımlarında Böl eylemini kullanarak veya bir belgeye mali boyut varsayılan şablonları uygulayarak hareket tutarlarını el ile atayabilirsiniz. Daha fazla bilgi için bkz. [Muhasebe dağılımları](../accounts-payable/accounting-distributions.md).
-   Her bir ana hesapta tanımlanan atama şartlarına dayalı olarak hareket tutarlarını otomatik olarak atayın. Tahsisat hesabı girişleri, bir muhasebe girişinin kaynak defter hesabı olarak tanımlanan kriterleri karşılaması durumunda her bir günlük için yüzdeye ve hedef defter hesabına dayalı olarak üretilecektir. Daha fazla bilgi için bkz. [Ana hesap tahsisat koşulları](../general-ledger/main-account-allocation-terms.md)
-   Defter bakiyelerini veya sabit tutarları defter tahsisat kurallarına dayalı olarak otomatik olarak atayın. Defter tahsisat kuralları, atama günlükleri kullanılarak düzenli olarak işlenir. Daha fazla bilgi için bkz. [Tahsisat kuralları](../general-ledger/ledger-allocation-rules.md).

###  <a name="allocations-in-budget-planning"></a>Bütçe planlamasında tahsisatlar

Defter tahsisat kuralları, bütçe planları için kullanılabilir. Defter tahsisat kurallarını bütçe planlamada kullanıyorsanız, tahsisat kuralları, defterdekiyle aynı şekilde çalışacaktır, ancak kaynak verileri ve hedef verileri bütçe planından gelir. Bütçe planları için kullanılacak genel muhasebe tahsisat kurallarını el ile seçebilirsiniz. Alternatif olarak, bir iş akışı işleminin bir parçası olarak çalışan bir tahsisat zamanlaması kullanabilirsiniz.

> [!NOTE]
> Bütçe planlama için şirketler arası defter tahsisat kurallarını kullanamazsınız.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

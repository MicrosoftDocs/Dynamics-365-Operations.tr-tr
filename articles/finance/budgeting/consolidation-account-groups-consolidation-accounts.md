---
title: Konsolidasyon hesabı grupları ve ek konsolidasyon hesapları
description: Bu makalede, konsolidasyon hesabı grupları ve ek konsolidasyon hesapları oluşturma ve bunların nasıl kullanıldıkları hakkında bilgi sağlanmaktadır.
author: panolte
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: kfend
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9e66190fe0bab24545bf19eba59facded63ee197
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882034"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Konsolidasyon hesabı grupları ve ek konsolidasyon hesapları

[!include [banner](../includes/banner.md)]

Bu makalede, konsolidasyon hesabı grupları ve ek konsolidasyon hesapları oluşturma ve bunların nasıl kullanıldıkları hakkında bilgi sağlanmaktadır.

## <a name="consolidation-account-groups"></a>Konsolidasyon hesap grupları

Konsolidasyon hesabı grupları, verileri konsolide etmek için kullanmak isteyebileceğiniz hesap gruplarını oluşturmanıza olanak sağlar. Genellikle, bir konsolidasyon hesabı grubu devletin zorunlu kıldığı hesap planını temsil eder. Bir konsolidasyon hesabı grubu, hesapları şirketin yönetim merkezi tarafından tanımlanan bir gruba da eşlenebilir. Konsolidasyon hesap gruplarını **Konsolidasyonlar** modülünün **Kurulum** alanında bulabilirsiniz. Yeni bir grup eklediğinizde, hesap grubu için bir kimlik tanımlayıcısı ve bir ad girersiniz.

## <a name="additional-consolidation-accounts"></a>İlave konsolidasyon hesapları
Ek konsolidasyon hesapları, mevcut bir hesap planlarından bir hesabı, bir konsolidasyon hesabı grubuna atamanıza olanak sağlar. Daha sonra bir konsolidasyon hesabı değeri ve adı belirtebilirsiniz. 

Ek konsolidasyon hesaplarını **Konsolidasyonlar** modülünün **Kurulum** alanında bulabilirsiniz. Yeni bir konsolidasyon hesabı oluşturduğunuzda, aşağıdaki bilgileri belirtmeniz gerekir:

-   **Ana hesap** – Bu alan, bu sayfada seçmiş olduğunuz hesap planlarına dayanan tüm ana hesapları gösteren bir arama alanıdır. Bir hesabı seçtiğinizde, adı otomatik olarak **Ana hesap adı** alanına girilir.
-   **Konsolidasyon hesabı grubu** – Bu alanı, hesabı atayacağınız grubu belirtmek için kullanın. İki farklı şekilde konsolide ederseniz, aynı hesabı dört konsolidasyon hesabı grubunun tümüne de eklemeniz gerekir.
-   **Konsolidasyon hesabı** – Konsolidasyon hesabının değerini girin. Bu değer, hesap planındaki bir hesap olmak zorunda değildir. İhtiyaç duyduğunuz herhangi bir değer olabilir.
-   **Konsolidasyon hesabı adı** - Hesabın adını, sorgular ve raporlarda belirmesini istediğiniz şekilde girin.
-   **SAT düzeyi** – Bu alan, hesap ekstrelerini Meksika vergi otoritelerine bildirmek için kullanılır. 

Konsolidasyon hesapları gruplarınızı ve ek konsolidasyon hesaplarınızı oluşturmayı tamamladıktan sonra, grubu Konsolidasyon çevrimiçi işleminde seçebilirsiniz.


Daha fazla bilgi için bkz. [Konsolidasyon grupları ve ek konsolidasyon hesapları oluşturma](../general-ledger/tasks/create-consolidation-groups.md). 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

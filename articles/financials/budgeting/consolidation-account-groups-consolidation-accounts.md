---
title: Konsolidasyon hesabı grupları ve ek konsolidasyon hesapları
description: Bu konu, konsolidasyon hesabı grupları ve ek konsolidasyon hesapları oluşturma ve bunların Microsoft Dynamics 365 for Finance and Operations içerisinde nasıl kullanıldıkları hakkında bilgi sağlar.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f1c463ee54512b07f5e45c4df995aefed6110cb0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570961"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Konsolidasyon hesabı grupları ve ek konsolidasyon hesapları

[!include [banner](../includes/banner.md)]

Bu konu, konsolidasyon hesabı grupları ve ek konsolidasyon hesapları oluşturma ve bunların Microsoft Dynamics 365 for Finance and Operations içerisinde nasıl kullanıldıkları hakkında bilgi sağlar.

<a name="consolidation-account-groups"></a>Konsolidasyon hesap grupları
----------------------------

Konsolidasyon hesabı grupları, verileri konsolide etmek için kullanmak isteyebileceğiniz hesap gruplarını oluşturmanıza olanak sağlar. Çoğunlukla, bir konsolidasyon hesabı grubu, devletin zorunlu kıldığı hesap planlarını veya eşleşme hesaplarını, şirketin yönetim merkezi tarafından tanımlanmış bir gruba temsilini sağlar. Konsolidasyon hesap gruplarını **Konsolidasyonlar** modülünün **Kurulum** alanında bulabilirsiniz. Yeni bir grup eklediğinizde, hesap grubu için bir kimlik tanımlayıcısı ve bir ad girersiniz.

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




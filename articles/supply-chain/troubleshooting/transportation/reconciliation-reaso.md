---
title: Mutabakat nedenleriyle kredi hesabı olarak yalnızca ana hesabı ekleyebilirsiniz
description: Taşımacılık yönetiminde bir mutabakat nedeni ayarladığınızda, kredi hesabı olarak yalnızca ana hesabı ekleyebilirsiniz.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c4ba48c5b6e3476c203eed2fddf053ce8af873dd6a7665df54560c8894f8c2d1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750894"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a>Mutabakat nedenleriyle kredi hesabı olarak yalnızca ana hesabı ekleyebilirsiniz

KB numarası: 4603538

## <a name="symptoms"></a>Belirtiler

Taşımacılık yönetiminde bir mutabakat nedeni ayarladığınızda, kredi hesabı olarak yalnızca ana hesabı ekleyebilirsiniz. Kredi hesabı olarak bir maliyet merkezi veya başka bir boyut ekleyemezsiniz. Ancak, borç hesabı başka boyutları seçmenize olanak tanır.

## <a name="resolution"></a>Çözünürlük

Mutabakat; satıcıya ödeme yapmak için değil de belirli bir ana hesaba alacaklandırma için yapılmışsa mutabakat nedeni ayarladığınızda sistem, kredi hesabı için bir mali boyut seçmenize olanak tanımaz.

Hesap yapısı, kredi ana hesabı için belirli bir mali boyut değeri gerektiriyorsa, mali boyut değeri eksik olduğundan elde edilen satıcı günlüğü otomatik olarak nakledilemez. Bu nedenle, önce **Fatura günlüğü** sayfasını kullanarak kredi hesabını el ile belirtmeniz gerekir.

Kredi hesabı için boyut değeri gerekli olduğundan, satıcı faturası günlüğü otomatik olarak nakledilemez. Kredi satırı için boyut değerini ana hesaba el ile ekledikten sonra yine el ile deftere nakletmeniz gerekir.

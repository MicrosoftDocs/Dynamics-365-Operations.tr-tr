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
ms.openlocfilehash: 708081370b27fd51ef9a2329d8392f4515353dcb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026969"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a><span data-ttu-id="af17f-103">Mutabakat nedenleriyle kredi hesabı olarak yalnızca ana hesabı ekleyebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="af17f-103">You can add only the main account as the credit account for reconciliation reasons</span></span>

<span data-ttu-id="af17f-104">KB numarası: 4603538</span><span class="sxs-lookup"><span data-stu-id="af17f-104">KB number: 4603538</span></span>

## <a name="symptoms"></a><span data-ttu-id="af17f-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="af17f-105">Symptoms</span></span>

<span data-ttu-id="af17f-106">Taşımacılık yönetiminde bir mutabakat nedeni ayarladığınızda, kredi hesabı olarak yalnızca ana hesabı ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="af17f-106">When you set up a reconciliation reason in Transportation management, you can add only the main account as the credit account.</span></span> <span data-ttu-id="af17f-107">Kredi hesabı olarak bir maliyet merkezi veya başka bir boyut ekleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="af17f-107">You can't add a cost center or any other dimension as the credit account.</span></span> <span data-ttu-id="af17f-108">Ancak, borç hesabı başka boyutları seçmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="af17f-108">However, the debit account lets you select other dimensions.</span></span>

## <a name="resolution"></a><span data-ttu-id="af17f-109">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="af17f-109">Resolution</span></span>

<span data-ttu-id="af17f-110">Mutabakat; satıcıya ödeme yapmak için değil de belirli bir ana hesaba alacaklandırma için yapılmışsa mutabakat nedeni ayarladığınızda sistem, kredi hesabı için bir mali boyut seçmenize olanak tanımaz.</span><span class="sxs-lookup"><span data-stu-id="af17f-110">If the reconciliation isn't done to pay the vendor but to credit a specific main account, the system doesn't allow you to select a financial dimension for the credit account when you set up the reconciliation reason.</span></span>

<span data-ttu-id="af17f-111">Hesap yapısı, kredi ana hesabı için belirli bir mali boyut değeri gerektiriyorsa, mali boyut değeri eksik olduğundan elde edilen satıcı günlüğü otomatik olarak nakledilemez.</span><span class="sxs-lookup"><span data-stu-id="af17f-111">If the account structure requires a specific financial dimension value for the credit main account, the resulting vendor journal can't be posted automatically, because the financial dimension value is missing.</span></span> <span data-ttu-id="af17f-112">Bu nedenle, önce **Fatura günlüğü** sayfasını kullanarak kredi hesabını el ile belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="af17f-112">Therefore, you must first manually specify the credit account by using the **Invoice journal** page.</span></span>

<span data-ttu-id="af17f-113">Kredi hesabı için boyut değeri gerekli olduğundan, satıcı faturası günlüğü otomatik olarak nakledilemez.</span><span class="sxs-lookup"><span data-stu-id="af17f-113">Because a dimension value is required for the credit account, the vendor invoice journal can't be automatically posted.</span></span> <span data-ttu-id="af17f-114">Kredi satırı için boyut değerini ana hesaba el ile ekledikten sonra yine el ile deftere nakletmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="af17f-114">You must manually post it after you manually add the dimension value to the main account for the credit line.</span></span>

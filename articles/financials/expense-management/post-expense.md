---
title: Gider raporunu deftere nakletme
description: Bu konu bir gider raporunun genel muhasebe defterine nasıl nakledileceğini açıklar.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1252825848aedcdaf633c04edddddca7dd09d774
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570680"
---
# <a name="post-an-expense-report"></a><span data-ttu-id="fa47a-103">Gider raporunu deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="fa47a-103">Post an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa47a-104">Bir gider raporu, onaylanmasından ve genel günlüğe aktarılmasından sonra genel muhasebeye nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="fa47a-104">After an expense report has been approved and transferred to the general journal, it can be posted to the general ledger.</span></span> <span data-ttu-id="fa47a-105">Gider raporunu deftere naklettiğinizde, katma değer vergisi (KDV) iadesi uyun olan giderler tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="fa47a-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="fa47a-106">KDV ödemelerini doğrulama ve iade görevi gider raporunu doğrulamakla sorumlu personele atanır.</span><span class="sxs-lookup"><span data-stu-id="fa47a-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="fa47a-107">Gider raporunda giderler personeli istihdam eden şirketten farklı bir şirket için masraf gösterildiyse, bu giderlerin ödenmesi gereken şirketi ve bu giderleri ödeyecek şirketi doğrulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="fa47a-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify the company that those expenses are owed to and the company that the expenses are owed from.</span></span> <span data-ttu-id="fa47a-108">Örneğin, gider raporu gönderen personel DAT şirketi için çalışmaktadır ancak bir gideri DIR firmasına masraflandırır.</span><span class="sxs-lookup"><span data-stu-id="fa47a-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="fa47a-109">Bu durumda, DAT şirketi gideri ödemesi gereken ve DIR şirketi giderin ödeneceği şirkettir.</span><span class="sxs-lookup"><span data-stu-id="fa47a-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="fa47a-110">Bu günlük satırlarını doğruladıktan sonra, gider satırlarını genel muhasebeye nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fa47a-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="fa47a-111">Gider raporunu deftere nakletmek için **Onaylanan gider raporları** sayfasında gider raporunu seçin ve ardından Eylem Bölmesinde **Deftere naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fa47a-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="fa47a-112">Ayrıca, listedeki tüm gider raporlarını aynı anda deftere nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fa47a-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="fa47a-113">Tüm gider raporlarını seçin ve ardından **Deftere naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fa47a-113">Select all the expense reports, and then select **Post**.</span></span>

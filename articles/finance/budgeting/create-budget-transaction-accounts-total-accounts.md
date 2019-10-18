---
title: İşlem hesapları ve toplam hesaplar için bütçe oluşturma
description: Bu makalede, toplam hesaplara göre bütçe oluşturma işlemine genel bir bakış verilmektedir. Makalede, bütçe kontrolü gerektiği zaman toplam hesaplar için bütçe kontrolünün nasıl etkinleştirileceği de açıklanmaktadır.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f60963bee790737c85161dff03278df0572e3abc
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180375"
---
# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a><span data-ttu-id="a860e-104">İşlem hesapları ve toplam hesaplar için bütçe oluşturma</span><span class="sxs-lookup"><span data-stu-id="a860e-104">Create a budget from transaction accounts and total accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a860e-105">Bu makalede, toplam hesaplara göre bütçe oluşturma işlemine genel bir bakış verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="a860e-105">This article provides an overview of the process for creating budgets based on total accounts.</span></span> <span data-ttu-id="a860e-106">Makalede, bütçe kontrolü gerektiği zaman toplam hesaplar için bütçe kontrolünün nasıl etkinleştirileceği de açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a860e-106">It also explains how to turn on budget control for total accounts, if budget control is required.</span></span>

<span data-ttu-id="a860e-107">Hem bütçe planı hem bütçe kaydı giriş belgeleri, ana hesap türü **Toplam** olan ana hesaplarda bütçe oluşturulmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="a860e-107">Both budget plan and budget register entry documents allow for budgeting on main accounts that have a main account type of **Total**.</span></span> <span data-ttu-id="a860e-108">Fiziksel emtialar yalnızca işlem ana hesaplarına nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="a860e-108">Actuals can be posted only to transactional main accounts.</span></span> 

<span data-ttu-id="a860e-109">**Genel defterden genel bütçe planı** periyodik işlemi için, **Kaynak** sekmesi için **Toplam** ana hesap tipini bir kriter olarak belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a860e-109">For the **Generate budget plan from General ledger** periodic process, on the **Source** tab, you can specify the **Total** main account type as a criterion.</span></span> <span data-ttu-id="a860e-110">Bu durumda, her bir toplam ana hesap hedef bütçe planında yer alacak ve miktar, seçilen ana hesap aralığındaki toplam miktara eşit olacaktır.</span><span class="sxs-lookup"><span data-stu-id="a860e-110">In this case, each total main account will be included in the target budget plan, and the amount will equal the total amount of the range of selected main accounts.</span></span> 

<span data-ttu-id="a860e-111">**Toplam** türündeki ana hesaplar için bütçe kontrolünü etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a860e-111">You can activate budget control for main accounts of the **Total** type.</span></span> <span data-ttu-id="a860e-112">Bu işlev, bütçe gruplarının kullanımıyla desteklenir.</span><span class="sxs-lookup"><span data-stu-id="a860e-112">This functionality is supported through the use of budget groups.</span></span> <span data-ttu-id="a860e-113">Her bir toplam an hesap için, bir bütçe grubu için kontrol edilmiş olan bütçe, **Bütçe denetim yapılandırma** sayfasında oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a860e-113">For each total main account, the budget that should be controlled for a budget group must be created on the \*\*Budget control configuration \*\*page.</span></span> <span data-ttu-id="a860e-114">Belirlediğiniz kriter, toplam ana hesabı ve hesap aralığını içermelidir.</span><span class="sxs-lookup"><span data-stu-id="a860e-114">The criteria that you specify must include the total main account and the range of accounts.</span></span> <span data-ttu-id="a860e-115">Bütçe grupları oluşturma işlemini hızlandırmak için, Bütçe kontrol grupları veri varlığından yararlanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a860e-115">To speed up the process of creating budget groups, you can take advantage of the Budget control groups data entity.</span></span> 

<span data-ttu-id="a860e-116">Raporlamada, örneğin bir mali tabloda bir bütçe kullanılıyorsa toplam hesap için bütçe toplamı şu hesaplardan meydana gelir:</span><span class="sxs-lookup"><span data-stu-id="a860e-116">When a budget is used in reporting, such as on a financial statement, the budget sum for the total account consists of the following amounts:</span></span>

-   <span data-ttu-id="a860e-117">Toplam hesap aralığında her bir işlem defter hesabından oluşturulan bütçeler.</span><span class="sxs-lookup"><span data-stu-id="a860e-117">The budgets that are created from each transaction ledger account in the interval of the total account.</span></span>
-   <span data-ttu-id="a860e-118">Toplam hesaba doğrudan girilen bütçe tutarı.</span><span class="sxs-lookup"><span data-stu-id="a860e-118">The budget amount that is entered directly on the total account.</span></span>

<span data-ttu-id="a860e-119">Bu nedenle, toplam hesap aralığındaki en önemli işlem hesapları için ayrı bütçeler oluşturabilir ve mevcut bütçe tutarını toplam hesaba ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a860e-119">Therefore, you can create separate budgets for the most significant transaction accounts in the interval of the total account, and then add the available budget amount to the total account.</span></span>




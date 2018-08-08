---
title: "Konsolidasyon hesabı grupları ve ek konsolidasyon hesapları"
description: "Bu konu, konsolidasyon hesap grupları ve ek konsolidasyon hesapları ve bunların Microsoft Dynamics 365 for Finance and Operations içerisinde nasıl kullanıldığı hakkında bilgi sağlar."
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: f1c463ee54512b07f5e45c4df995aefed6110cb0
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---

# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="ab2e6-103">Konsolidasyon hesabı grupları ve ek konsolidasyon hesapları</span><span class="sxs-lookup"><span data-stu-id="ab2e6-103">Consolidation account groups and additional consolidation accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab2e6-104">Bu konu, konsolidasyon hesap grupları ve ek konsolidasyon hesapları ve bunların Microsoft Dynamics 365 for Finance and Operations içerisinde nasıl kullanıldığı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="ab2e6-104">This topic provides information about consolidation account groups and additional consolidation accounts, and explains how they are used in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<a name="consolidation-account-groups"></a><span data-ttu-id="ab2e6-105">Konsolidasyon hesap grupları</span><span class="sxs-lookup"><span data-stu-id="ab2e6-105">Consolidation account groups</span></span>
----------------------------

<span data-ttu-id="ab2e6-106">Konsolidasyon hesabı grupları, verileri konsolide etmek için kullanmak isteyebileceğiniz hesap gruplarını oluşturmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="ab2e6-106">Consolidation account groups let you create groups of the accounts that you want to use to consolidate data.</span></span> <span data-ttu-id="ab2e6-107">Çoğunlukla, bir konsolidasyon hesabı grubu, devletin zorunlu kıldığı hesap planlarını veya eşleşme hesaplarını, şirketin yönetim merkezi tarafından tanımlanmış bir gruba temsilini sağlar.</span><span class="sxs-lookup"><span data-stu-id="ab2e6-107">Most often, a consolidation account group represents a government-mandated chart of accounts or maps accounts to a group that is defined by the company's headquarters.</span></span> <span data-ttu-id="ab2e6-108">Konsolidasyon hesap gruplarını **Konsolidasyonlar** modülünün **Kurulum** alanında bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ab2e6-108">You can find consolidation account groups in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="ab2e6-109">Yeni bir grup eklediğinizde, hesap grubu için bir kimlik tanımlayıcısı ve bir ad girersiniz.</span><span class="sxs-lookup"><span data-stu-id="ab2e6-109">When you add a new group, you enter a unique identifier for the account group and a name.</span></span>

## <a name="additional-consolidation-accounts"></a><span data-ttu-id="ab2e6-110">İlave konsolidasyon hesapları</span><span class="sxs-lookup"><span data-stu-id="ab2e6-110">Additional consolidation accounts</span></span>
<span data-ttu-id="ab2e6-111">Ek konsolidasyon hesapları, mevcut bir hesap planlarından bir hesabı, bir konsolidasyon hesabı grubuna atamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="ab2e6-111">Additional consolidation accounts let you assign an account from an existing chart of accounts to a consolidation account group.</span></span> <span data-ttu-id="ab2e6-112">Daha sonra bir konsolidasyon hesabı değeri ve adı belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ab2e6-112">You can then specify a consolidation account value and name.</span></span> 

<span data-ttu-id="ab2e6-113">Ek konsolidasyon hesaplarını **Konsolidasyonlar** modülünün **Kurulum** alanında bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ab2e6-113">You can find additional consolidation accounts in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="ab2e6-114">Yeni bir konsolidasyon hesabı oluşturduğunuzda, aşağıdaki bilgileri belirtmeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="ab2e6-114">When you create a new consolidation account, you must specify the following information:</span></span>

-   <span data-ttu-id="ab2e6-115">**Ana hesap** – Bu alan, bu sayfada seçmiş olduğunuz hesap planlarına dayanan tüm ana hesapları gösteren bir arama alanıdır.</span><span class="sxs-lookup"><span data-stu-id="ab2e6-115">**Main account** – This field is a lookup that shows all the main accounts that are based on the chart of accounts that you selected on the page.</span></span> <span data-ttu-id="ab2e6-116">Bir hesabı seçtiğinizde, adı otomatik olarak **Ana hesap adı** alanına girilir.</span><span class="sxs-lookup"><span data-stu-id="ab2e6-116">When you select an account, the name is automatically entered in the **Main account name** field.</span></span>
-   <span data-ttu-id="ab2e6-117">**Konsolidasyon hesabı grubu** – Bu alanı, hesabı atayacağınız grubu belirtmek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="ab2e6-117">**Consolidation account group** – Use this field to specify the group to assign the account to.</span></span> <span data-ttu-id="ab2e6-118">İki farklı şekilde konsolide ederseniz, aynı hesabı dört konsolidasyon hesabı grubunun tümüne de eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ab2e6-118">If you consolidate in two different ways, you must add the same account to all four consolidation account groups.</span></span>
-   <span data-ttu-id="ab2e6-119">**Konsolidasyon hesabı** – Konsolidasyon hesabının değerini girin.</span><span class="sxs-lookup"><span data-stu-id="ab2e6-119">**Consolidation account** – Enter the value of the consolidation account.</span></span> <span data-ttu-id="ab2e6-120">Bu değer, hesap planındaki bir hesap olmak zorunda değildir.</span><span class="sxs-lookup"><span data-stu-id="ab2e6-120">This value doesn't have to be an account from a chart of accounts.</span></span> <span data-ttu-id="ab2e6-121">İhtiyaç duyduğunuz herhangi bir değer olabilir.</span><span class="sxs-lookup"><span data-stu-id="ab2e6-121">It can be any value that you require.</span></span>
-   <span data-ttu-id="ab2e6-122">**Konsolidasyon hesabı adı** - Hesabın adını, sorgular ve raporlarda belirmesini istediğiniz şekilde girin.</span><span class="sxs-lookup"><span data-stu-id="ab2e6-122">**Consolidation account name** – Enter the name of account as you want it to appear on inquiries and reports.</span></span>
-   <span data-ttu-id="ab2e6-123">**SAT düzeyi** – Bu alan, hesap ekstrelerini Meksika vergi otoritelerine bildirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ab2e6-123">**SAT level** – This field is used to report account statements to the Mexican tax authorities.</span></span> 

<span data-ttu-id="ab2e6-124">Konsolidasyon hesapları gruplarınızı ve ek konsolidasyon hesaplarınızı oluşturmayı tamamladıktan sonra, grubu Konsolidasyon çevrimiçi işleminde seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ab2e6-124">When you've finished creating your consolidation account groups and additional consolidation accounts, you can select the group in the Consolidate online process.</span></span>


<span data-ttu-id="ab2e6-125">Daha fazla bilgi için bkz. [Konsolidasyon grupları ve ek konsolidasyon hesapları oluşturma](../general-ledger/tasks/create-consolidation-groups.md).</span><span class="sxs-lookup"><span data-stu-id="ab2e6-125">For more information, see [Create consolidation groups and additional consolidation accounts](../general-ledger/tasks/create-consolidation-groups.md).</span></span> 





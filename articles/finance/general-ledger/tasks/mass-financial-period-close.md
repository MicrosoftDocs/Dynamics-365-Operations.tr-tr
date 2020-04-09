---
title: Toplu mali dönem kapatma
description: Bu konuda, bir dönemin nasıl beklemeye alındığı veya bir kerede bir dönemin ya da birden fazla tüzel kişiliğin nasıl kalıcı olarak kapatıldığı gösterilir.
author: aprilolson
manager: AnnBe
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a149b35c6964166207effc799a02cd4c59bbb843
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144994"
---
# <a name="mass-financial-period-close"></a><span data-ttu-id="3ccd0-103">Toplu mali dönem kapatma</span><span class="sxs-lookup"><span data-stu-id="3ccd0-103">Mass financial period close</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3ccd0-104">Bu konuda, bir dönemin nasıl beklemeye alındığı veya bir kerede bir dönemin ya da birden fazla tüzel kişiliğin nasıl kalıcı olarak kapatıldığı gösterilir.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-104">This topic shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="3ccd0-105">Ayrıca görev, kullanıcı grubunun belirli modüllere naklinin nasıl sınırlandırılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="3ccd0-106">Gezinti bölmesinde **Modüller > Genel muhasebe > Dönem kapanışı > Genel muhasebe takvimleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-106">In the navigation pane, go to **Modules > General ledger > Period close > Ledger calendars**.</span></span> <span data-ttu-id="3ccd0-107">Görüntülenen tüzel kişilikler listesinin sayfada seçilen mali takvime bağlı olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="3ccd0-108">Yalnızca seçilen mali takvimi kullanan tüzel kişilikler görüntülenecektir.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-108">Only legal entities using the selected fiscal calendar will display.</span></span>
2. <span data-ttu-id="3ccd0-109">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-109">Select **Edit**.</span></span>
3. <span data-ttu-id="3ccd0-110">Durumu değiştirmek istediğiniz dönemi seçin.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="3ccd0-111">Durumu güncelleştirmek istediğiniz tüzel kişilikleri seçin.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-111">Select the legal entities for which you want to update the status.</span></span> <span data-ttu-id="3ccd0-112">Kılavuzun sol üst kısmındaki onay işaretini seçerek tüm tüzel kişilikleri hızlı bir şekilde seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-112">You can quickly select all legal entities by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="3ccd0-113">Seçilen modüle nakil erişimini tanımlamak için **Modül erişimini güncelleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-113">Select **Update module access** to define the posting access to a selected module.</span></span> <span data-ttu-id="3ccd0-114">Modül durumu da kılavuzdaki kayıtları düzenleyerek tek tek güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="3ccd0-115">Birden çok tüzel kişilik kaydını hızlı bir şekilde güncelleştirmek istediğinizde düğmeyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="3ccd0-116">**Uygulama** modülünde, durumunu güncelleştirmek istediğiniz modülü seçin.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-116">In the **Application** module, select the module that you want to update the status.</span></span> <span data-ttu-id="3ccd0-117">**Seç**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-117">Click **Select**.</span></span>
7. <span data-ttu-id="3ccd0-118">**Erişim** düzeyinde **Tümü**, **Hiçbiri** veya belirli bir kullanıcı grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-118">In the **Access** level, select **All**, **None**, or a specific user group.</span></span> <span data-ttu-id="3ccd0-119">**Seç**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-119">Click **Select**.</span></span> <span data-ttu-id="3ccd0-120">Tümü, dönem açıksa, deftere nakil yapabilecek modülü düzenleme erişimi olan tüm kullanıcıları gösterir.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="3ccd0-121">Dönem açıksa, hiçbiri modülde deftere nakil yapamayacak tüm kullanıcıları göstermez.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="3ccd0-122">Belirli bir kullanıcı grubu, dönem açıksa, yalnızca gruptaki modülde deftere nakil yapabilecek kullanıcıları gösterir.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="3ccd0-123">**Güncelleştir**'i seçin</span><span class="sxs-lookup"><span data-stu-id="3ccd0-123">Select **Update**.</span></span>
9. <span data-ttu-id="3ccd0-124">Durumu güncelleştirmek için başka bir dönem seçin.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="3ccd0-125">Durumunu güncelleştirmek istediğiniz tüzel kişilikleri seçin.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-125">Select the legal entites for which you want to update the period status.</span></span>
11. <span data-ttu-id="3ccd0-126">**Dönem durumunu güncelleştir**'i seçin ve durumu **Beklemede**, **Açık** veya **Kalıcı olarak kapatıldı** şeklinde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-126">Select **Update period status** and set the status of **On hold**, **Open**, or **Permanently closed**.</span></span> <span data-ttu-id="3ccd0-127">**Açık**, dönem içinde erişimi olan kullanıcılar tarafından deftere nakil yapılabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-127">**Open** indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="3ccd0-128">**Beklemede** dönemin nakledilemeyeceği ancak yeniden açılabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-128">**On hold** means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="3ccd0-129">**Kalıcı olarak kapatıldı**, dönemin tamamen kapatıldığı ve bir daha açılamayacağı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-129">**Permanently closed** means the period is closed and can never be opened.</span></span> <span data-ttu-id="3ccd0-130">Ayarlamalar nakledilemezler.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="3ccd0-131">Tüm ayarlamalar ve denetimler tamamlanana kadar bir dönemin **Kalıcı olarak kapatıldı** şeklinde ayarlanması önerilmez.</span><span class="sxs-lookup"><span data-stu-id="3ccd0-131">We do not recommend setting a period to **Permanently closed** until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="3ccd0-132">**Güncelleştir**'i seçin</span><span class="sxs-lookup"><span data-stu-id="3ccd0-132">Select **Update**.</span></span>


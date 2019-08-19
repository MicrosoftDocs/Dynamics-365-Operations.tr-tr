---
title: Perakende mağazasına yönelik ekstreler oluşturma, hesaplama ve deftere nakletme
description: Bu konuda bir mağaza için el ile ekstre oluşturma, hesaplama ve deftere nakletme adımları açıklanmaktadır.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 693d1821779d5f7af95b900daa3bb7a2c38a6354
ms.sourcegitcommit: cb63259ad8fa5649ff12bc4a7f195bd1e40bd968
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/16/2019
ms.locfileid: "1755535"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="0ada8-103">Perakende mağazasına yönelik ekstreler oluşturma, hesaplama ve deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="0ada8-103">Create, calculate, and post statements for a retail store</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="0ada8-104">Bu konuda bir mağaza için el ile ekstre oluşturma, hesaplama ve deftere nakletme adımları açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="0ada8-104">This topic describes the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="0ada8-105">Aynı görevler için yapılandırılabilecek toplu işler de vardır.</span><span class="sxs-lookup"><span data-stu-id="0ada8-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="0ada8-106">Toplu işleri yapılandırma ve çalıştırmayla ilgili adımlar diğer konularda bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="0ada8-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="0ada8-107">Bu yordamı tamamlamak için POS'ta tamamlanan ve ardından Dynamics 365 for Finance and Operations uygulamasına çekilen hareketleriniz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0ada8-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="0ada8-108">Bu kayıt USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="0ada8-108">This recording uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="0ada8-109">Giriş sayfasından **Perakende mağaza finansmanları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="0ada8-109">Select **Retail store financials** from the home page.</span></span>
2. <span data-ttu-id="0ada8-110">**Yeni ekstre**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0ada8-110">Select **New statement**.</span></span>
3. <span data-ttu-id="0ada8-111">**Mağaza numarası** alanında, açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="0ada8-111">In the **Store number** field, select a option from the drop-down.</span></span>
4. <span data-ttu-id="0ada8-112">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0ada8-112">Select **OK**.</span></span>
5. <span data-ttu-id="0ada8-113">**Kurulum** grubunda, ekstreye hangi hareketlerin dahil edileceğini ve bunların ekstre satırlarında nasıl gruplandırılacağını denetleyen ayarlar bulunur.</span><span class="sxs-lookup"><span data-stu-id="0ada8-113">The **Setup** group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="0ada8-114">**Kurulum** grubunu açarak bu ayarları değiştirebilir veya varsayılanları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0ada8-114">You can open the **Setup** group and change these settings, or you can use the defaults.</span></span>  
    - <span data-ttu-id="0ada8-115">**Ekstre yöntemi** alanı ekstre satırlarının nasıl gruplandırılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ada8-115">The **Statement method** field defines how the statement lines will be grouped.</span></span>  
    - <span data-ttu-id="0ada8-116">Personel üyesi seçin veya ekstreyi yalnızca belirli bir personel için hesaplamak veya kaydetmek isterseniz **personel/kayıt** alanından kayıt yapın.</span><span class="sxs-lookup"><span data-stu-id="0ada8-116">Select a staff member or a register in the **staff/register** field if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="0ada8-117">**Kapanış yöntemi** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="0ada8-117">In the **Closing method** field, select an option.</span></span>
7. <span data-ttu-id="0ada8-118">Eylem bölmesinden **Ekstre hesapla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="0ada8-118">Select **Calculate statement** from the Action Pane.</span></span>
8. <span data-ttu-id="0ada8-119">**Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0ada8-119">Select **Yes**.</span></span>
    - <span data-ttu-id="0ada8-120">Ekstreyi hesaplandıktan sonra, kullanılan her ödeme ve ekstre yöntemi için toplam tutarları içeren satırlar oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0ada8-120">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    - <span data-ttu-id="0ada8-121">Girilmesi veya güncelleştirilmesi gerekiyorsa her satıra sayılmış bir tutar girin.</span><span class="sxs-lookup"><span data-stu-id="0ada8-121">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="0ada8-122">Sayılan alanı POS'ta yapılan kasa sayımlarından alınan tutarlarla doldurulur.</span><span class="sxs-lookup"><span data-stu-id="0ada8-122">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="0ada8-123">Eylem bölmesinden **Ekstreyi deftere naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0ada8-123">Select **Post statement** from the Action Pane.</span></span>
10. <span data-ttu-id="0ada8-124">**Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0ada8-124">Select **Close**.</span></span>
11. <span data-ttu-id="0ada8-125">Bölmeyi kapatın.</span><span class="sxs-lookup"><span data-stu-id="0ada8-125">Close the pane.</span></span>
12. <span data-ttu-id="0ada8-126">Giriş sayfasından **Perakende mağaza finansmanları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="0ada8-126">At the home page, select **Retail store financials**.</span></span>
13. <span data-ttu-id="0ada8-127">**Deftere nakledilen ekstreler** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="0ada8-127">Select the **Posted statements** tab.</span></span>


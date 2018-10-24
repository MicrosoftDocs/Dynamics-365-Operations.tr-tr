--- 
title: "Çevrimiçi satışlar ve ödemeler deftere naklediliyor"
description: "Bu yordam, çevrimiçi mağaza hareketleri için satış siparişleri ve ödemeler oluşturmak üzere yinelenen bir toplu işi yapılandırma ve çalıştırmayla ilgili açıklamalar içerir."
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 13839bbe6ca03f3cfc7036fce87477bf7d5af2a7
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="93f7a-103">Çevrimiçi satışlar ve ödemeler deftere naklediliyor</span><span class="sxs-lookup"><span data-stu-id="93f7a-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="93f7a-104">Bu yordam, çevrimiçi mağaza hareketleri için satış siparişleri ve ödemeler oluşturmak üzere yinelenen bir toplu işi yapılandırma ve çalıştırmayla ilgili açıklamalar içerir.</span><span class="sxs-lookup"><span data-stu-id="93f7a-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="93f7a-105">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="93f7a-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="93f7a-106">All workspaces > Retail store financials (Tüm çalışma alanları > Perakende mağaza finansmanları) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="93f7a-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="93f7a-107">Siparişleri eşitle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="93f7a-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="93f7a-108">Kuruluş hiyerarşisi alanında 'Bölgeye göre Perakende Mağazalar'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="93f7a-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="93f7a-109">Belirli bir çevrimiçi mağaza seçin veya mağaza grubu için toplu iş oluşturmak istiyorsanız bir düğüm belirtin.</span><span class="sxs-lookup"><span data-stu-id="93f7a-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="93f7a-110">Seçiminizi eklemek için oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="93f7a-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="93f7a-111">Arka planda çalıştır sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="93f7a-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="93f7a-112">Toplu işlem onay kutusunu işaretleyin veya işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="93f7a-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="93f7a-113">Yineleme'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="93f7a-113">Click Recurrence.</span></span>
7. <span data-ttu-id="93f7a-114">Bitiş tarihi yok seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="93f7a-114">Select the No end date option.</span></span>
8. <span data-ttu-id="93f7a-115">Sayım alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="93f7a-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="93f7a-116">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="93f7a-116">Click OK.</span></span>
10. <span data-ttu-id="93f7a-117">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="93f7a-117">Click OK.</span></span>



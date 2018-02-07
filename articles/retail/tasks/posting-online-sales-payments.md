--- 
title: " Çevrimiçi satışları ve ödemeleri deftere nakletme"
description: "Bu yordam, çevrimiçi mağaza hareketleri için satış siparişleri ve ödemeler oluşturmak üzere yinelenen bir toplu işi yapılandırma ve çalıştırmayla ilgili açıklamalar içerir."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 2feaf580c7ae1fc53f9257f117576c99764c6ea0
ms.contentlocale: tr-tr
ms.lasthandoff: 02/07/2018

---
# <a name="post-online-sales-and-payments"></a><span data-ttu-id="2b815-103"> Çevrimiçi satışları ve ödemeleri deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="2b815-103">Post online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="2b815-104">Bu yordam, çevrimiçi mağaza hareketleri için satış siparişleri ve ödemeler oluşturmak üzere yinelenen bir toplu işi yapılandırma ve çalıştırmayla ilgili açıklamalar içerir.</span><span class="sxs-lookup"><span data-stu-id="2b815-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="2b815-105">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="2b815-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="2b815-106">All workspaces > Retail store financials (Tüm çalışma alanları > Perakende mağaza finansmanları) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="2b815-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="2b815-107">Siparişleri eşitle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2b815-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="2b815-108">Kuruluş hiyerarşisi alanında 'Bölgeye göre Perakende Mağazalar'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b815-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="2b815-109">Belirli bir çevrimiçi mağaza seçin veya mağaza grubu için toplu iş oluşturmak istiyorsanız bir düğüm belirtin.</span><span class="sxs-lookup"><span data-stu-id="2b815-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="2b815-110">Seçiminizi eklemek için oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2b815-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="2b815-111">Arka planda çalıştır sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2b815-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="2b815-112">Toplu işlem onay kutusunu işaretleyin veya işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="2b815-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="2b815-113">Yineleme'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2b815-113">Click Recurrence.</span></span>
7. <span data-ttu-id="2b815-114">Bitiş tarihi yok seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="2b815-114">Select the No end date option.</span></span>
8. <span data-ttu-id="2b815-115">Sayım alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="2b815-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="2b815-116">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2b815-116">Click OK.</span></span>
10. <span data-ttu-id="2b815-117">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2b815-117">Click OK.</span></span>



---
title: "Analitik raporları güncelleştirilmedi"
description: "Bu konu, müşterinin verisindeki değişiklikler müşterinin herhangi bir çalışma alanında görüntülenmediğinde ne yapılacağını açıklar."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 46f426a4b0012e87b4d9d21032870ac7fc33c4ae
ms.contentlocale: tr-tr
ms.lasthandoff: 12/04/2018

---

# <a name="analytic-reports-are-not-updated"></a><span data-ttu-id="ffa27-103">Analitik raporları güncelleştirilmedi</span><span class="sxs-lookup"><span data-stu-id="ffa27-103">Analytic reports are not updated</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ffa27-104">**Stok çıkışı**</span><span class="sxs-lookup"><span data-stu-id="ffa27-104">**Issue**</span></span>

<span data-ttu-id="ffa27-105">Bir müşterinin verisi, müşterinin herhangi bir çalışma alanındaki **Analitik** sekmesinde görüntülenmiyor.</span><span class="sxs-lookup"><span data-stu-id="ffa27-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="ffa27-106">**Nedeni**</span><span class="sxs-lookup"><span data-stu-id="ffa27-106">**Cause**</span></span>

<span data-ttu-id="ffa27-107">Varsayılan olarak Microsoft Power BI raporları, her dört saatte bir yenilenir, Dağıtım ölçüm toplu işine uygun olarak.</span><span class="sxs-lookup"><span data-stu-id="ffa27-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="ffa27-108">**Çözünürlük**</span><span class="sxs-lookup"><span data-stu-id="ffa27-108">**Resolution**</span></span>

<span data-ttu-id="ffa27-109">Bu sorun, zamanlama nedeniyle olabilir.</span><span class="sxs-lookup"><span data-stu-id="ffa27-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="ffa27-110">Bu adımları izleyerek toplu işi başlatın ve analitik çalışma alanlarını güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="ffa27-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="ffa27-111">**Toplu işler** sayfasını **Sistem yönetimi \> Bağlantılar \> Toplu işler \> Toplu işler**'i açın.</span><span class="sxs-lookup"><span data-stu-id="ffa27-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="ffa27-112">Alternatif olarak, aramayı kullanın ve **Toplu işler**'e girin.</span><span class="sxs-lookup"><span data-stu-id="ffa27-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="ffa27-113">**Ölçümü dağıt** işini listede bulun.</span><span class="sxs-lookup"><span data-stu-id="ffa27-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="ffa27-114">Sayfanın üstünde **Düzenle**'yi seçin ve zamanlanan başlangıç tarihini/saatini, analitikleri geçerli tarihe daha yakın bir zamanda yenileyecek değere ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ffa27-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Toplu işler](media/batch-jobs.png)


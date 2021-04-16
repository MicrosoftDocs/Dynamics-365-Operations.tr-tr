---
title: Sorun giderme Analitik raporları
description: Bu konu, müşterinin verisindeki değişiklikler müşterinin herhangi bir çalışma alanında görüntülenmediğinde ne yapılacağını açıklar.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b500d519d61edfd20456355376e3fc81f16517a0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794985"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="c280b-103">Sorun giderme Analitik raporları</span><span class="sxs-lookup"><span data-stu-id="c280b-103">Troubleshoot analytic reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c280b-104">**Çıkış**</span><span class="sxs-lookup"><span data-stu-id="c280b-104">**Issue**</span></span>

<span data-ttu-id="c280b-105">Bir müşterinin verisi, müşterinin herhangi bir çalışma alanındaki **Analitik** sekmesinde görüntülenmiyor.</span><span class="sxs-lookup"><span data-stu-id="c280b-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="c280b-106">**Nedeni**</span><span class="sxs-lookup"><span data-stu-id="c280b-106">**Cause**</span></span>

<span data-ttu-id="c280b-107">Varsayılan olarak Microsoft Power BI raporları, her dört saatte bir yenilenir, Dağıtım ölçüm toplu işine uygun olarak.</span><span class="sxs-lookup"><span data-stu-id="c280b-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="c280b-108">**Çözünürlük**</span><span class="sxs-lookup"><span data-stu-id="c280b-108">**Resolution**</span></span>

<span data-ttu-id="c280b-109">Bu sorun, zamanlama nedeniyle olabilir.</span><span class="sxs-lookup"><span data-stu-id="c280b-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="c280b-110">Bu adımları izleyerek toplu işi başlatın ve analitik çalışma alanlarını güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="c280b-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="c280b-111">**Toplu işler** sayfasını **Sistem yönetimi \> Bağlantılar \> Toplu işler \> Toplu işler**'i açın.</span><span class="sxs-lookup"><span data-stu-id="c280b-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="c280b-112">Alternatif olarak, aramayı kullanın ve **Toplu işler**'e girin.</span><span class="sxs-lookup"><span data-stu-id="c280b-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="c280b-113">**Ölçümü dağıt** işini listede bulun.</span><span class="sxs-lookup"><span data-stu-id="c280b-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="c280b-114">Sayfanın üstünde **Düzenle**'yi seçin ve zamanlanan başlangıç tarihini/saatini, analitikleri geçerli tarihe daha yakın bir zamanda yenileyecek değere ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c280b-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Toplu işler](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
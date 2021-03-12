---
title: İçeri aktarma işlerinde tarihi ve saati eşitleme
description: Saat dilimi dönüştürmelerinde sorunları önlemek için içeri aktarma işlerinde UTC saat dilimlerini kullanın.
author: Sunil-Garg
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae04b09a68e64d6d70c0329e689ab08c3903fca0
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798731"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a><span data-ttu-id="93676-103">İçeri aktarma işlerinde tarihi ve saati eşitleme</span><span class="sxs-lookup"><span data-stu-id="93676-103">Synchronize date and time in import jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93676-104">İçeri aktarma işinizin saat dilimini Eşgüdümlü Evrensel Saat'e (UTC) göre ayarlamanız önemlidir.</span><span class="sxs-lookup"><span data-stu-id="93676-104">It's important to set the time zone for your import job to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="93676-105">Farklı bir ayar kullanırsanız içeri aktarılan verilerinizde beklenmeyen tarihler ve saatler görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="93676-105">You might see unexpected dates and times in your imported data if you use a different setting.</span></span> <span data-ttu-id="93676-106">Doğru ayar olmazsa içeri aktarma işlemi UTC tarihini yerel biçime dönüştürür ve sonra sistem ayarları bunu yeniden dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="93676-106">Without the correct setting, the import process converts the UTC date to the local format, and then system settings converts it again.</span></span>

<span data-ttu-id="93676-107">Bu çift dönüştürme, uygulamalar arasında tarihlerin değişmesine neden olur.</span><span class="sxs-lookup"><span data-stu-id="93676-107">This dual conversion causes dates to change between applications.</span></span> <span data-ttu-id="93676-108">Örneğin, yerel saat dilimlerindeki farklar nedeniyle çift dönüştürme sorunu, bir çalışanın başlangıç tarihinin Dynamics 365 Human Resources ve Dynamics 365 Finance arasında farklı olmasına neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="93676-108">For example, the dual conversion could cause an employee's start date to be different between Dynamics 365 Human Resources and Dynamics 365 Finance due to differences in local time zones.</span></span> <span data-ttu-id="93676-109">İçeri aktar işini UTC'ye ayarlamak bu sorunu çözer.</span><span class="sxs-lookup"><span data-stu-id="93676-109">Setting the import job to UTC resolves this problem.</span></span>

1. <span data-ttu-id="93676-110">Dynamics 365 Finance and Operations'da, **Veri yönetimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="93676-110">In Dynamics 365 Finance and Operations, select **Data management**.</span></span>

2. <span data-ttu-id="93676-111">**Projeleri içeri aktar**'ı ve ardından projeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="93676-111">Select **Import projects**, and then select the project.</span></span>

3. <span data-ttu-id="93676-112">**Kaynak tarih biçimi** bölümünde, **CSV-Unicode**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="93676-112">Under **Source date format**, select **CSV-Unicode**.</span></span>

   <span data-ttu-id="93676-113">[![Kaynak tarih biçimini UTC'ye dönüştürme](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span><span class="sxs-lookup"><span data-stu-id="93676-113">[![Change source date format to UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span></span>

4. <span data-ttu-id="93676-114">**Saat dilimi**'ni **Eşgüdümlü Evrensel Saat** olarak değiştirin ve **Dil**'i **En-US** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="93676-114">Change **Timezone** to **Coordinated Universal Timezone**, and change **Language** to **En-US**.</span></span>



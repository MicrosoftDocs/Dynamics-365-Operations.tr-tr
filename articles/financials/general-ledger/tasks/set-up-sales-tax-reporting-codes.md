---
title: Satış vergisi raporlama kodlarını ayarla
description: Satış vergisi raporlama kodları, satış vergisi raporundaki bir alan numarasına karşılık gelir.
author: twheeloc
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4751256858da417ec9bb1b7d9ccd16fb6bef1cac
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916103"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="e2375-103">Satış vergisi raporlama kodlarını ayarla</span><span class="sxs-lookup"><span data-stu-id="e2375-103">Set up sales tax reporting codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e2375-104">Satış vergisi raporlama kodları, satış vergisi raporundaki bir alan numarasına karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="e2375-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="e2375-105">Bunlar, raporlama kodu başına özeti çıkarılan kapatma döneminin satış vergisi tutarlarının yazdırılacağı kod raporu tarafından, ülkeye özel rapor düzenlerinde ve Satış vergisi ödemesinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e2375-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="e2375-106">Satış vergisi raporlama kodlarını oluşturduktan sonra, Satış vergisi kodu sayfasındaki Rapor kurulumu hızlı sekmelerinde bu kodlara gönderme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e2375-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="e2375-107">Bu kayıtta DEMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e2375-107">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="e2375-108">**Gezinti bölmesinde** **Vergi > Kurulum > Satış vergisi > Satış vergisi raporlama kodları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="e2375-108">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="e2375-109">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e2375-109">Click **New**.</span></span>
3. <span data-ttu-id="e2375-110">Raporlama kodunun ait olduğu rapor düzenini seçin.</span><span class="sxs-lookup"><span data-stu-id="e2375-110">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="e2375-111">Bu düzen, bir Satış vergisi kodu için kullanılabilecek raporlama kodlarını filtrelemede kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e2375-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="e2375-112">Her Satış vergisi kodu, bir Rapor düzeni kullanan, bir Satış vergisi dairesine ait bir kapatma dönemine aittir.</span><span class="sxs-lookup"><span data-stu-id="e2375-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="e2375-113">**Raporlama kodu** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e2375-113">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="e2375-114">**Rapor metni** alanında, raporlarda görüntülenecek bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="e2375-114">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="e2375-115">**Kısa açıklama** alanında, dahili amaçlı bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="e2375-115">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="e2375-116">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e2375-116">Click **Save**.</span></span>


---
title: Stopaj vergisini ayarlama
description: Bu konuda, stopaj vergisinin nasıl ayarlanacağı açıklanmaktadır.
author: twheeloc
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 135cca434a1689bf22ee468894dcf8746071e7ca
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144709"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="56933-103">Stopaj vergisini ayarlama</span><span class="sxs-lookup"><span data-stu-id="56933-103">Set up withholding tax</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="56933-104">Bu konuda, stopaj vergisinin nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="56933-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="56933-105">*Stopaj vergisi*, satış vergisi hareketleri oluşturmayan satıcılara uygulanan bir vergidir.</span><span class="sxs-lookup"><span data-stu-id="56933-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="56933-106">Satıcı ödemelerinden hesaplanan stopaj vergisi bir borçtur.</span><span class="sxs-lookup"><span data-stu-id="56933-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="56933-107">Dolayısıyla, stopajın nakledilebileceği hesaplar yalnızca bilanço hesapları veya pasif hesaplarıdır.</span><span class="sxs-lookup"><span data-stu-id="56933-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="56933-108">Bu görev kılavuzunda, stopaj vergisinin nasıl ayarlanacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="56933-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="56933-109">**Gezinme bölmesi > Modüller > Vergi > Dolaylı vergiler > Stopaj vergisi > Stopaj vergisi kodları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="56933-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="56933-110">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="56933-110">Select **New**.</span></span>
3. <span data-ttu-id="56933-111">**Stopaj vergisi kodu** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="56933-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="56933-112">**Stopaj vergisi adı** alanına stopaj vergisi kodunun adı girin.</span><span class="sxs-lookup"><span data-stu-id="56933-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="56933-113">**Ana hesap** alanında, stopaj vergisi borcunun nakletmek için ana hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="56933-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="56933-114">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="56933-114">Select **Save**.</span></span>
7. <span data-ttu-id="56933-115">**Değerler**'i seçin ve listeden istenen kaydı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="56933-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="56933-116">**Değer** alanına, stopaj vergisini hesaplamada kullanılacak bir yüzde girin.</span><span class="sxs-lookup"><span data-stu-id="56933-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="56933-117">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="56933-117">Select **Save**.</span></span>
10. <span data-ttu-id="56933-118">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="56933-118">Close the page.</span></span>
11. <span data-ttu-id="56933-119">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="56933-119">Select **Save**.</span></span>
12. <span data-ttu-id="56933-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="56933-120">Close the page.</span></span>
13. <span data-ttu-id="56933-121">**Gezinme bölmesi > Modüller > Vergi > Dolaylı vergiler > Stopaj vergisi > Stopaj vergisi grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="56933-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="56933-122">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="56933-122">Select **New**.</span></span>
15. <span data-ttu-id="56933-123">**Stopaj vergisi grubu** alanına stopaj vergisi grubunun tanımlayıcısını girin.</span><span class="sxs-lookup"><span data-stu-id="56933-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="56933-124">**Açıklama** alanına stopaj vergisi grubunun adını girin.</span><span class="sxs-lookup"><span data-stu-id="56933-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="56933-125">**Stopaj vergisi kodu** alanında stopaj vergisi kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="56933-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="56933-126">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="56933-126">Select **Save**.</span></span>
19. <span data-ttu-id="56933-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="56933-127">Close the page.</span></span>


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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ae7b13f743336e01f17248c8d6492b31e8044ef
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222323"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="03ba5-103">Stopaj vergisini ayarlama</span><span class="sxs-lookup"><span data-stu-id="03ba5-103">Set up withholding tax</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="03ba5-104">Bu konuda, stopaj vergisinin nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="03ba5-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="03ba5-105">*Stopaj vergisi*, satış vergisi hareketleri oluşturmayan satıcılara uygulanan bir vergidir.</span><span class="sxs-lookup"><span data-stu-id="03ba5-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="03ba5-106">Satıcı ödemelerinden hesaplanan stopaj vergisi bir borçtur.</span><span class="sxs-lookup"><span data-stu-id="03ba5-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="03ba5-107">Dolayısıyla, stopajın nakledilebileceği hesaplar yalnızca bilanço hesapları veya pasif hesaplarıdır.</span><span class="sxs-lookup"><span data-stu-id="03ba5-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="03ba5-108">Bu görev kılavuzunda, stopaj vergisinin nasıl ayarlanacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="03ba5-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="03ba5-109">**Gezinme bölmesi > Modüller > Vergi > Dolaylı vergiler > Stopaj vergisi > Stopaj vergisi kodları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="03ba5-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="03ba5-110">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="03ba5-110">Select **New**.</span></span>
3. <span data-ttu-id="03ba5-111">**Stopaj vergisi kodu** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="03ba5-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="03ba5-112">**Stopaj vergisi adı** alanına stopaj vergisi kodunun adı girin.</span><span class="sxs-lookup"><span data-stu-id="03ba5-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="03ba5-113">**Ana hesap** alanında, stopaj vergisi borcunun nakletmek için ana hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="03ba5-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="03ba5-114">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="03ba5-114">Select **Save**.</span></span>
7. <span data-ttu-id="03ba5-115">**Değerler**'i seçin ve listeden istenen kaydı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="03ba5-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="03ba5-116">**Değer** alanına, stopaj vergisini hesaplamada kullanılacak bir yüzde girin.</span><span class="sxs-lookup"><span data-stu-id="03ba5-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="03ba5-117">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="03ba5-117">Select **Save**.</span></span>
10. <span data-ttu-id="03ba5-118">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="03ba5-118">Close the page.</span></span>
11. <span data-ttu-id="03ba5-119">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="03ba5-119">Select **Save**.</span></span>
12. <span data-ttu-id="03ba5-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="03ba5-120">Close the page.</span></span>
13. <span data-ttu-id="03ba5-121">**Gezinme bölmesi > Modüller > Vergi > Dolaylı vergiler > Stopaj vergisi > Stopaj vergisi grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="03ba5-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="03ba5-122">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="03ba5-122">Select **New**.</span></span>
15. <span data-ttu-id="03ba5-123">**Stopaj vergisi grubu** alanına stopaj vergisi grubunun tanımlayıcısını girin.</span><span class="sxs-lookup"><span data-stu-id="03ba5-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="03ba5-124">**Açıklama** alanına stopaj vergisi grubunun adını girin.</span><span class="sxs-lookup"><span data-stu-id="03ba5-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="03ba5-125">**Stopaj vergisi kodu** alanında stopaj vergisi kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="03ba5-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="03ba5-126">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="03ba5-126">Select **Save**.</span></span>
19. <span data-ttu-id="03ba5-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="03ba5-127">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
--- 
title: Stopaj vergisini ayarlama
description: "Stopaj vergisi, satış vergisi hareketleri oluşturmayan satıcılara uygulanan bir vergidir."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 39ebd6a1a326b0ff2943957c9606e91852d524ce
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="de169-103">Stopaj vergisini ayarlama</span><span class="sxs-lookup"><span data-stu-id="de169-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="de169-104">Stopaj vergisi, satış vergisi hareketleri oluşturmayan satıcılara uygulanan bir vergidir.</span><span class="sxs-lookup"><span data-stu-id="de169-104">Withholding tax is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="de169-105">Satıcı ödemelerinden hesaplanan stopaj vergisi bir borçtur.</span><span class="sxs-lookup"><span data-stu-id="de169-105">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="de169-106">Dolayısıyla, stopajın nakledilebileceği hesaplar yalnızca bilanço hesapları veya pasif hesaplarıdır.</span><span class="sxs-lookup"><span data-stu-id="de169-106">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="de169-107">Bu görev kılavuzunda, stopaj vergisinin nasıl ayarlanacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="de169-107">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="de169-108">Vergi > Dolaylı vergiler > Stopaj vergisi > Stopaj vergisi kodları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="de169-108">Go to Tax > Indirect taxes > Withholding tax > Withholding tax codes.</span></span>
2. <span data-ttu-id="de169-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de169-109">Click New.</span></span>
3. <span data-ttu-id="de169-110">Stopaj vergisi kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="de169-110">In the Withholding tax code field, type a value.</span></span>
4. <span data-ttu-id="de169-111">Stopaj vergisi adı alanına stopaj vergisi kodunun adı girin.</span><span class="sxs-lookup"><span data-stu-id="de169-111">In the Withholding tax name field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="de169-112">Ana hesap alanında, stopaj vergisi borcunun nakletmek için ana hesabı seçin.</span><span class="sxs-lookup"><span data-stu-id="de169-112">In the Main account field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="de169-113">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de169-113">Click Save.</span></span>
7. <span data-ttu-id="de169-114">Değerler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de169-114">Click Values.</span></span>
8. <span data-ttu-id="de169-115">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="de169-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="de169-116">Değer alanına, stopaj vergisini hesaplamada kullanılacak bir yüzde girin.</span><span class="sxs-lookup"><span data-stu-id="de169-116">In the Value field, enter a percentage used for the calculation of the withholding tax.</span></span>
10. <span data-ttu-id="de169-117">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de169-117">Click Save.</span></span>
11. <span data-ttu-id="de169-118">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="de169-118">Close the page.</span></span>
12. <span data-ttu-id="de169-119">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de169-119">Click Save.</span></span>
13. <span data-ttu-id="de169-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="de169-120">Close the page.</span></span>
14. <span data-ttu-id="de169-121">Vergi > Dolaylı vergiler > Stopaj vergisi > Stopaj vergisi grupları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="de169-121">Go to Tax > Indirect taxes > Withholding tax > Withholding tax groups.</span></span>
15. <span data-ttu-id="de169-122">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de169-122">Click New.</span></span>
16. <span data-ttu-id="de169-123">Stopaj vergisi grubu alanına stopaj vergisi grubunun tanımlayıcısını girin.</span><span class="sxs-lookup"><span data-stu-id="de169-123">In the Withholding tax group field, enter the identifier of the withholding tax group.</span></span>
17. <span data-ttu-id="de169-124">Açıklama alanına stopaj vergisi grubunun adını girin.</span><span class="sxs-lookup"><span data-stu-id="de169-124">In the Description field, enter the name of the withholding tax group.</span></span>
18. <span data-ttu-id="de169-125">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="de169-125">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="de169-126">Stopaj vergisi kodu alanında stopaj vergisi kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="de169-126">In the Withholding tax code field, select the withholding tax code.</span></span>
20. <span data-ttu-id="de169-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de169-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="de169-128">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de169-128">Click Save.</span></span>



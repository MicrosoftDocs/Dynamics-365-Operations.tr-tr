--- 
title: "Satıcı faturasındaki satış vergisini hesaplama ve ayarlama"
description: "Orijinal kaynak belgesinde hesaplanandan farklı vergi tutarları görüntüleniyorsa, bu tutarları deftere nakletmeden önce ayarlayabilirsiniz."
author: ShylaThompson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 1af9228e5efd2cd6e414eebf766bb3475b44a360
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="ab71c-103">Satıcı faturasındaki satış vergisini hesaplama ve ayarlama</span><span class="sxs-lookup"><span data-stu-id="ab71c-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ab71c-104">Orijinal kaynak belgesinde hesaplanandan farklı vergi tutarları görüntüleniyorsa, bu tutarları deftere nakletmeden önce ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ab71c-104">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="ab71c-105">Bu görevde DEMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ab71c-105">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="ab71c-106">Borç hesapları > Faturalar > Fatura günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ab71c-106">Go to Accounts payable > Invoices > Invoice journal.</span></span>
2. <span data-ttu-id="ab71c-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab71c-107">Click New.</span></span>
3. <span data-ttu-id="ab71c-108">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ab71c-108">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="ab71c-109">Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ab71c-109">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ab71c-110">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab71c-110">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ab71c-111">Satırlar seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ab71c-111">Click Lines.</span></span>
7. <span data-ttu-id="ab71c-112">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ab71c-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="ab71c-113">Hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="ab71c-113">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="ab71c-114">Fatura alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ab71c-114">In the Invoice field, type a value.</span></span>
10. <span data-ttu-id="ab71c-115">Alacak alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ab71c-115">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="ab71c-116">Mahsup hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="ab71c-116">In the Offset account field, specify the desired values.</span></span>
12. <span data-ttu-id="ab71c-117">Satış vergisi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab71c-117">Click Sales tax.</span></span>
13. <span data-ttu-id="ab71c-118">Toplam gerçek satış vergisi tutarı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ab71c-118">In the Total actual sales tax amount field, enter a number.</span></span>
14. <span data-ttu-id="ab71c-119">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab71c-119">Click OK.</span></span>
15. <span data-ttu-id="ab71c-120">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ab71c-120">Click Save.</span></span>
16. <span data-ttu-id="ab71c-121">Satış vergisi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab71c-121">Click Sales tax.</span></span>
17. <span data-ttu-id="ab71c-122">Ayarlama sekmesinde, satış vergisi tutarları, tek tek satış vergisi kodlarına göre ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="ab71c-122">On the Adjustment tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
18. <span data-ttu-id="ab71c-123">Hesaplanan tutarlardan gerçek tutarı sıfırla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab71c-123">Click Reset actual from calculated amounts.</span></span>
19. <span data-ttu-id="ab71c-124">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab71c-124">Click OK.</span></span>
20. <span data-ttu-id="ab71c-125">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab71c-125">Click Save.</span></span>



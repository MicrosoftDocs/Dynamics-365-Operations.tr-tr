---
title: Satıcı faturasındaki satış vergisini hesaplama ve ayarlama
description: Orijinal kaynak belgesinde hesaplanandan farklı vergi tutarları görüntüleniyorsa, bu tutarları deftere nakletmeden önce ayarlayabilirsiniz.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 803c038d907b68a3c72a83a3e035c4e08b8a8661
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "308932"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="98199-103">Satıcı faturasındaki satış vergisini hesaplama ve ayarlama</span><span class="sxs-lookup"><span data-stu-id="98199-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="98199-104">Orijinal kaynak belgesinde hesaplanandan farklı vergi tutarları görüntüleniyorsa, bu tutarları deftere nakletmeden önce ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="98199-104">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="98199-105">Bu görevde DEMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="98199-105">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="98199-106">Borç hesapları > Faturalar > Fatura günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="98199-106">Go to Accounts payable > Invoices > Invoice journal.</span></span>
2. <span data-ttu-id="98199-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98199-107">Click New.</span></span>
3. <span data-ttu-id="98199-108">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="98199-108">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="98199-109">Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="98199-109">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="98199-110">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98199-110">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="98199-111">Satırlar seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="98199-111">Click Lines.</span></span>
7. <span data-ttu-id="98199-112">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="98199-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="98199-113">Hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="98199-113">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="98199-114">Fatura alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="98199-114">In the Invoice field, type a value.</span></span>
10. <span data-ttu-id="98199-115">Alacak alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="98199-115">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="98199-116">Mahsup hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="98199-116">In the Offset account field, specify the desired values.</span></span>
12. <span data-ttu-id="98199-117">Satış vergisi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98199-117">Click Sales tax.</span></span>
13. <span data-ttu-id="98199-118">Toplam gerçek satış vergisi tutarı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="98199-118">In the Total actual sales tax amount field, enter a number.</span></span>
14. <span data-ttu-id="98199-119">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98199-119">Click OK.</span></span>
15. <span data-ttu-id="98199-120">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="98199-120">Click Save.</span></span>
16. <span data-ttu-id="98199-121">Satış vergisi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98199-121">Click Sales tax.</span></span>
17. <span data-ttu-id="98199-122">Ayarlama sekmesinde, satış vergisi tutarları, tek tek satış vergisi kodlarına göre ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="98199-122">On the Adjustment tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
18. <span data-ttu-id="98199-123">Hesaplanan tutarlardan gerçek tutarı sıfırla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98199-123">Click Reset actual from calculated amounts.</span></span>
19. <span data-ttu-id="98199-124">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98199-124">Click OK.</span></span>
20. <span data-ttu-id="98199-125">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="98199-125">Click Save.</span></span>


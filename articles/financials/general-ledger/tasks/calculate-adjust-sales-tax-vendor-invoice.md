---
title: Satıcı faturasındaki satış vergisini hesaplama ve ayarlama
description: Bu konuda Dynamics 365 for Finance and Operations satıcı faturasındaki satış vergisinin nasıl ayarlanacağı açıklanmaktadır.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 684529087d5348c9e02310f812f8aa6f64c6655f
ms.sourcegitcommit: 016832198c306e8329ad21b5254e7d1cdff74c2f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2019
ms.locfileid: "1862626"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="07d15-103">Satıcı faturasındaki satış vergisini hesaplama ve ayarlama</span><span class="sxs-lookup"><span data-stu-id="07d15-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="07d15-104">Bu konuda Dynamics 365 for Finance and Operations satıcı faturasındaki satış vergisinin nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="07d15-104">This topic explains how to adjust sales tax on a vendor invoice in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="07d15-105">Orijinal kaynak belgesinde hesaplanandan farklı vergi tutarları görüntüleniyorsa, bu tutarları deftere nakletmeden önce ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="07d15-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="07d15-106">Bu görevde DEMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="07d15-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="07d15-107">Gezinti bölmesinde **Modüller > Borç hesapları > Faturalar > Fatura günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="07d15-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="07d15-108">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="07d15-108">Select **New**.</span></span>
3. <span data-ttu-id="07d15-109">Yeni satırdaki **Ad** alanında açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="07d15-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="07d15-110">Eylem Bölmesinde, **Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="07d15-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="07d15-111">**Hesap** alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="07d15-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="07d15-112">**Fatura** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="07d15-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="07d15-113">**Alacak** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="07d15-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="07d15-114">**Mahsup hesap** alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="07d15-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="07d15-115">**Satış vergisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="07d15-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="07d15-116">**Toplam gerçek satış vergisi tutarı** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="07d15-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="07d15-117">**Ayarlama** sekmesinde, satış vergisi tutarları, tek tek satış vergisi kodlarına göre ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="07d15-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="07d15-118">**Hesaplanan tutarlardan gerçek tutarı sıfırla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="07d15-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="07d15-119">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="07d15-119">Select **OK**.</span></span>
14. <span data-ttu-id="07d15-120">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="07d15-120">Select **Save**.</span></span>


---
title: Satıcı faturasındaki satış vergisini hesaplama ve ayarlama
description: Bu konuda Dynamics 365 Finance satıcı faturasındaki satış vergisinin nasıl ayarlanacağı açıklanmaktadır.
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
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 03313d875d23489b3293376dd94f808c73a4bd15
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448641"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="ad0ae-103">Satıcı faturasındaki satış vergisini hesaplama ve ayarlama</span><span class="sxs-lookup"><span data-stu-id="ad0ae-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ad0ae-104">Bu konuda satıcı faturasındaki satış vergisinin nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ad0ae-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="ad0ae-105">Orijinal kaynak belgesinde hesaplanandan farklı vergi tutarları görüntüleniyorsa, bu tutarları deftere nakletmeden önce ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ad0ae-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="ad0ae-106">Bu görevde DEMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ad0ae-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="ad0ae-107">Gezinti bölmesinde **Modüller > Borç hesapları > Faturalar > Fatura günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ad0ae-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="ad0ae-108">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ad0ae-108">Select **New**.</span></span>
3. <span data-ttu-id="ad0ae-109">Yeni satırdaki **Ad** alanında açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ad0ae-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="ad0ae-110">Eylem Bölmesinde, **Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ad0ae-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="ad0ae-111">**Hesap** alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="ad0ae-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="ad0ae-112">**Fatura** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ad0ae-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="ad0ae-113">**Alacak** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ad0ae-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="ad0ae-114">**Mahsup hesap** alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="ad0ae-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="ad0ae-115">**Satış vergisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="ad0ae-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="ad0ae-116">**Toplam gerçek satış vergisi tutarı** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ad0ae-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="ad0ae-117">**Ayarlama** sekmesinde, satış vergisi tutarları, tek tek satış vergisi kodlarına göre ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="ad0ae-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="ad0ae-118">**Hesaplanan tutarlardan gerçek tutarı sıfırla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="ad0ae-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="ad0ae-119">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ad0ae-119">Select **OK**.</span></span>
14. <span data-ttu-id="ad0ae-120">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ad0ae-120">Select **Save**.</span></span>


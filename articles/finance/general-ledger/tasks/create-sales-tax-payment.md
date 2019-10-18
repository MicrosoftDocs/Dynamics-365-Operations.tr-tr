---
title: Satış vergisi ödemesi oluşturma
description: Satış vergisini kapat ve deftere naklet işi, satış vergisi hesaplarındaki satış vergisi bakiyelerini kapatır ve bu bakiyeleri belirli bir dönemin satış vergisi kapatma hesabına mahsup olarak işler.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee69cfee672be1571fd5cc630e33601bb5a48eac
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186176"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="33dd3-103">Satış vergisi ödemesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="33dd3-103">Create a sales tax payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="33dd3-104">Satış vergisini kapat ve deftere naklet işi, satış vergisi hesaplarındaki satış vergisi bakiyelerini kapatır ve bu bakiyeleri belirli bir dönemin satış vergisi kapatma hesabına mahsup olarak işler.</span><span class="sxs-lookup"><span data-stu-id="33dd3-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="33dd3-105">Vergi > Bildirimler > Satış vergisi > Satış vergisini kapat ve deftere naklet'e gidin.</span><span class="sxs-lookup"><span data-stu-id="33dd3-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="33dd3-106">Kapatma dönemi alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="33dd3-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="33dd3-107">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="33dd3-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="33dd3-108">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="33dd3-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="33dd3-109">Genel muhasebe parametreleri sayfasında "Düzeltmeleri dahil et" seçeneği belirtilmezse, kapatma işlemi farklı sürümler için yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="33dd3-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="33dd3-110">Orijinal sürüm, dönem aralığının ilk kapatma işlemidir ve bir dönem aralığı için yalnızca bir kez yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="33dd3-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="33dd3-111">En son düzeltmeler, orijinal sürüm oluşturulduktan sonra deftere nakledilen satış vergisi hareketlerini kapatır.</span><span class="sxs-lookup"><span data-stu-id="33dd3-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="33dd3-112">Hareket tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="33dd3-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="33dd3-113">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="33dd3-113">Click OK.</span></span>


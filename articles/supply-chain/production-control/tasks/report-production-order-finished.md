---
title: Üretim emrinin bittiğini rapor etme
description: Bu yordam, bir üretim emrinin nasıl tamamlanmış olarak bildirileceğini gösterir.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd, ProdSetupReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 93193e6365bcf82fbbf93af81e2581a358899fa1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438991"
---
# <a name="report-a-production-order-as-finished"></a><span data-ttu-id="7b4e9-103">Üretim emrinin bittiğini rapor etme</span><span class="sxs-lookup"><span data-stu-id="7b4e9-103">Report a production order as finished</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7b4e9-104">Bu yordam, bir üretim emrinin nasıl tamamlanmış olarak bildirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-104">This procedure shows how to report a production order as finished.</span></span> <span data-ttu-id="7b4e9-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7b4e9-106">Bu, üretim emri ömrünü açıklayan yedi yordamdan altıncısıdır.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-106">This is the sixth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="report-a-production-order-as-finished"></a><span data-ttu-id="7b4e9-107">Üretim emrinin bittiğini rapor etme</span><span class="sxs-lookup"><span data-stu-id="7b4e9-107">Report a production order as finished</span></span>
1. <span data-ttu-id="7b4e9-108">Üretim denetimi > Üretim emirleri > Tüm üretim emirleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="7b4e9-109">Başlatıldı durumunda olan bir üretim emrini seçin.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-109">Select a production order that has the Started status.</span></span>  
2. <span data-ttu-id="7b4e9-110">Eylem Bölmesinde, Üretim emri öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="7b4e9-111">Tamamlandı olarak bildir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-111">Click Report as finished.</span></span>
    * <span data-ttu-id="7b4e9-112">Bu sayfada, tamamlanmış olarak bildirilecek tamamlanmış ürün miktarını onaylayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-112">On this page, you can confirm the quantity of the finished product to be reported as finished.</span></span>  
4. <span data-ttu-id="7b4e9-113">Genel sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-113">Click the General tab.</span></span>
5. <span data-ttu-id="7b4e9-114">Sağlam miktarını '18' olacak şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-114">Set Good quantity to '18'.</span></span>
6. <span data-ttu-id="7b4e9-115">Hata miktarını '2' olacak şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-115">Set Error quantity to '2'.</span></span>
7. <span data-ttu-id="7b4e9-116">Hata nedeni alanında 'Malzeme' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-116">In the Error cause field, select 'Material'.</span></span>
8. <span data-ttu-id="7b4e9-117">Son iş onay kutusunu işaretleyin veya temizleyin.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-117">Select or clear the End job check box.</span></span>
9. <span data-ttu-id="7b4e9-118">Hatayı kabul et onay kutusunu işaretleyin veya temizleyin.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-118">Select or clear the Accept error check box.</span></span>
10. <span data-ttu-id="7b4e9-119">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-119">Click OK.</span></span>

## <a name="verify-the-report-as-finished-journal"></a><span data-ttu-id="7b4e9-120">Tamamlandı bildirimi günlüğünü onaylayın.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-120">Verify the Report as finished journal</span></span>
1. <span data-ttu-id="7b4e9-121">Eylem Bölmesinde, Görüntüle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-121">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="7b4e9-122">Tamamlandı olarak işaretle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-122">Click Reported as finished.</span></span>
3. <span data-ttu-id="7b4e9-123">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="7b4e9-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7b4e9-125">Tamamlandı bildirimi günlüğü deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-125">The Report as finished journal is posted.</span></span> <span data-ttu-id="7b4e9-126">Günlükte ayarlamalar yapmak istiyorsanız, üzerinde değişiklik yapabileceğiniz yeni bir günlüğü el ile oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-126">If you want to make adjustments to the journal, you can manually create  a new journal where you can make changes.</span></span>  


---
title: İade edilen ürünler için varış günlüğünü deftere nakletme
description: İade edilen ürünler için varış günlüğünü deftere nakledin.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 184ce418ff2ec4b891a24b2b75d37b6b4f5d23f3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006653"
---
# <a name="post-arrival-journal-for-returned-products"></a><span data-ttu-id="bb8b1-103">İade edilen ürünler için varış günlüğünü deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="bb8b1-103">Post arrival journal for returned products</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="bb8b1-104">Bir iadeyi işlemek için öncelikle iade miktarını doğrulayın, madde varış günlüğündeki miktar alanını güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="bb8b1-104">To process a return, first validate the return quantity, update the quantity field in the item arrival journal.</span></span> <span data-ttu-id="bb8b1-105">Daha sonra bir elden çıkarma kodu seçin veya iade edilen maddelerin denetlenecek olduğunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="bb8b1-105">Then select a disposition code or indicate that the returned items have to be inspected.</span></span> <span data-ttu-id="bb8b1-106">Bu adımları tamamladıktan sonra, sipariş iadesi için madde geliş günlüğünü deftere nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb8b1-106">After completing these steps, you can post the item arrival journal for the return order.</span></span>

1.  <span data-ttu-id="bb8b1-107">**Stok yönetimi** \> **Periyodik** \> **Varışa genel bakış**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bb8b1-107">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="bb8b1-108">**Kurulum adı** filtresinde, **İade siparişi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="bb8b1-108">In the **Setup name** filter, select **Return order**.</span></span>

3.  <span data-ttu-id="bb8b1-109">Giriş listesi çok uzunsa, listeyi azaltmak için **Aralık** alanındaki alanları kullanın.</span><span class="sxs-lookup"><span data-stu-id="bb8b1-109">If the list of receipts is long, use the fields in the **Range** area to narrow the list.</span></span>

4.  <span data-ttu-id="bb8b1-110">Deftere nakletmek istediğiniz sipariş iadesinin satırını bulun, **Varış için seç** kutusunu seçin ve **Varışı başlat**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bb8b1-110">Locate the line of the return order that you want to post, select its **Select for arrival** box, and then click **Start arrival**.</span></span>

5.  <span data-ttu-id="bb8b1-111">**Günlükler** \> **Girişlerden varışları göster**'e tıklayıp **Yerleşim günlüğü** formunu açın.</span><span class="sxs-lookup"><span data-stu-id="bb8b1-111">Click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="bb8b1-112">Ayrıntılı bilgileri görüntülemek için bir günlük seçin ve <STRONG>Satırlar</STRONG>'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bb8b1-112">To view detailed information, select a journal, and then click <STRONG>Lines</STRONG>.</span></span></P>


6.  <span data-ttu-id="bb8b1-113">Gerekli güncelleştirmeleri yapın ve **Deftere naklet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bb8b1-113">Make any necessary updates, and then click **Post**.</span></span>

<span data-ttu-id="bb8b1-114">Günlük deftere nakledildikten sonra, iade edilen maddeler stoka kaydedilir ve **İade siparişlerş** formunda maddelerin ambara geldiği gösterilir.</span><span class="sxs-lookup"><span data-stu-id="bb8b1-114">After the journal is posted, the returned items are registered in inventory, and the **Return orders** form indicates that the items have arrived at the warehouse.</span></span>

## <a name="see-also"></a><span data-ttu-id="bb8b1-115">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="bb8b1-115">See also</span></span>

<span data-ttu-id="bb8b1-116">[Yerleşim günlüğü (form)](https://technet.microsoft.com/library/aa584822\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="bb8b1-116">[Location journal (form)](https://technet.microsoft.com/library/aa584822\(v=ax.60\))</span></span>

  



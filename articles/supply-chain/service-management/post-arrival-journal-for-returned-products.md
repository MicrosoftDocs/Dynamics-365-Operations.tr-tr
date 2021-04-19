---
title: İade edilen ürünler için varış günlüğünü deftere nakletme
description: İade edilen ürünler için varış günlüğünü deftere nakledin.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9dbd19b7dab95f5cf746fe6c7e3a9387acbda3ec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810642"
---
# <a name="post-arrival-journal-for-returned-products"></a><span data-ttu-id="dd951-103">İade edilen ürünler için varış günlüğünü deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="dd951-103">Post arrival journal for returned products</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="dd951-104">Bir iadeyi işlemek için öncelikle iade miktarını doğrulayın, madde varış günlüğündeki miktar alanını güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="dd951-104">To process a return, first validate the return quantity, update the quantity field in the item arrival journal.</span></span> <span data-ttu-id="dd951-105">Daha sonra bir elden çıkarma kodu seçin veya iade edilen maddelerin denetlenecek olduğunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="dd951-105">Then select a disposition code or indicate that the returned items have to be inspected.</span></span> <span data-ttu-id="dd951-106">Bu adımları tamamladıktan sonra, sipariş iadesi için madde geliş günlüğünü deftere nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd951-106">After completing these steps, you can post the item arrival journal for the return order.</span></span>

1.  <span data-ttu-id="dd951-107">**Stok yönetimi** \> **Periyodik** \> **Varışa genel bakış**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd951-107">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="dd951-108">**Kurulum adı** filtresinde, **İade siparişi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="dd951-108">In the **Setup name** filter, select **Return order**.</span></span>

3.  <span data-ttu-id="dd951-109">Giriş listesi çok uzunsa, listeyi azaltmak için **Aralık** alanındaki alanları kullanın.</span><span class="sxs-lookup"><span data-stu-id="dd951-109">If the list of receipts is long, use the fields in the **Range** area to narrow the list.</span></span>

4.  <span data-ttu-id="dd951-110">Deftere nakletmek istediğiniz sipariş iadesinin satırını bulun, **Varış için seç** kutusunu seçin ve **Varışı başlat**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd951-110">Locate the line of the return order that you want to post, select its **Select for arrival** box, and then click **Start arrival**.</span></span>

5.  <span data-ttu-id="dd951-111">**Günlükler** \> **Girişlerden varışları göster**'e tıklayıp **Yerleşim günlüğü** formunu açın.</span><span class="sxs-lookup"><span data-stu-id="dd951-111">Click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="dd951-112">Ayrıntılı bilgileri görüntülemek için bir günlük seçin ve <STRONG>Satırlar</STRONG>'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd951-112">To view detailed information, select a journal, and then click <STRONG>Lines</STRONG>.</span></span></P>


6.  <span data-ttu-id="dd951-113">Gerekli güncelleştirmeleri yapın ve **Deftere naklet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd951-113">Make any necessary updates, and then click **Post**.</span></span>

<span data-ttu-id="dd951-114">Günlük deftere nakledildikten sonra, iade edilen maddeler stoka kaydedilir ve **İade siparişlerş** formunda maddelerin ambara geldiği gösterilir.</span><span class="sxs-lookup"><span data-stu-id="dd951-114">After the journal is posted, the returned items are registered in inventory, and the **Return orders** form indicates that the items have arrived at the warehouse.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd951-115">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="dd951-115">See also</span></span>

<span data-ttu-id="dd951-116">[Yerleşim günlüğü (form)](https://technet.microsoft.com/library/aa584822\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="dd951-116">[Location journal (form)](https://technet.microsoft.com/library/aa584822\(v=ax.60\))</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
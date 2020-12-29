---
title: İade edilen maddeleri inceleme yoluyla alma
description: İade edilen maddeleri inceleme yoluyla alın.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bdc42f9c5ece8e2c2570cadf623f52648b7b174e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439459"
---
# <a name="take-returned-items-through-inspection"></a><span data-ttu-id="66fd9-103">İade edilen maddeleri inceleme yoluyla alma</span><span class="sxs-lookup"><span data-stu-id="66fd9-103">Take returned items through inspection</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="66fd9-104">**Stok yönetimi** \> **Periyodik** \> **Kalite yönetimi** \> **Karantina emirleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="66fd9-104">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="66fd9-105">Denetlediğiniz iade maddesine karşılık gelen sipariş satırının yerini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="66fd9-105">Locate the order line that corresponds to the returned item that you are inspecting.</span></span>

    > [!NOTE]
    > <P><span data-ttu-id="66fd9-106">Bir karantina emri yalnızca tek bir madde numarasıyla ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="66fd9-106">A quarantine order can be associated with just a single item number.</span></span> <span data-ttu-id="66fd9-107">Farklı madde numaralarına sahip 10 maddenin tek bir sevkiyatta iade edilmesi ve karantinaya gönderilmesi durumunda, ayrı ayrı 10 karantina emri oluşturulacaktır.</span><span class="sxs-lookup"><span data-stu-id="66fd9-107">If 10 items that have different item numbers are returned in a single shipment and sent to quarantine, 10 individual quarantine orders are created.</span></span></P>

3.  <span data-ttu-id="66fd9-108">Maddeyi inceledikten sonra, maddeye ne yapılması gerektiğini ve ilişkili mali hareketin ne şekilde ele alınacağını belirtmek üzere **Elden çıkarma kodu** alanında bir seçim yapın.</span><span class="sxs-lookup"><span data-stu-id="66fd9-108">After examining the item, make a selection in the **Disposition code** field to indicate what should be done with the item and how to handle the related financial transaction.</span></span> <span data-ttu-id="66fd9-109">Örnekler arasında maddenin stoka geri gönderilmesi ve müşteriye para iadesi yapılması, maddenin ıskartaya çıkarılması ve müşteriye yenisinin gönderilmesi ya da maddenin alacak kaydedilmeksizin müşteriye geri gönderilmesi yer alır.</span><span class="sxs-lookup"><span data-stu-id="66fd9-109">Examples include returning the item to stock and refunding the customer, scrapping the item and sending a replacement to the customer, or returning the item to the customer without credit.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="66fd9-110">Tek bir madde numarası toplu işindeki birden çok iade maddesine aynı elden çıkarma kodunun atanamaması durumunda, her alt toplu işe farklı bir çıkarma kodu atamak için karantina emrini bölmeniz gerekir (<STRONG>İşlevler</STRONG> &gt; <STRONG>Böl</STRONG>).</span><span class="sxs-lookup"><span data-stu-id="66fd9-110">If multiple returned items in a single item number batch cannot be assigned the same disposition code, you must split the quarantine order (<STRONG>Functions</STRONG> &gt; <STRONG>Split</STRONG>) to assign a different disposition code to each sub-batch.</span></span></P>


4.  <span data-ttu-id="66fd9-111">Denetim tamamlandıktan sonra, iade edilen maddeleri serbest bırakmak ve bir madde varış günlük girişi oluşturmak için **Bitti olarak bildir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="66fd9-111">When you are finished with the inspection, click **Report as finished** to release the returned items and create an item arrival journal entry.</span></span> <span data-ttu-id="66fd9-112">Daha sonra maddeleri alan kişi veya departman, stoğa iade edilecek maddeler için günlüğü işler.</span><span class="sxs-lookup"><span data-stu-id="66fd9-112">The person or department that receives the items then processes the journal for the items to be returned to inventory.</span></span>
    
    <span data-ttu-id="66fd9-113">veya</span><span class="sxs-lookup"><span data-stu-id="66fd9-113">–or–</span></span>
    
    <span data-ttu-id="66fd9-114">Karantina emrini sona erdirin ve doğrudan **Stok** işlevlerinden birini kullanarak maddeleri tekrar stoğa taşıyın.</span><span class="sxs-lookup"><span data-stu-id="66fd9-114">End the quarantine order, and move the items back into inventory directly by using one of the **Inventory** functions.</span></span>

5.  <span data-ttu-id="66fd9-115">Değişikliklerinizi kaydetmek için formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="66fd9-115">Close the form to save your changes.</span></span>

## <a name="see-also"></a><span data-ttu-id="66fd9-116">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="66fd9-116">See also</span></span>

[<span data-ttu-id="66fd9-117">İade edilen maddelerin nasıl elden çıkarılacağını belirtme</span><span class="sxs-lookup"><span data-stu-id="66fd9-117">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

  



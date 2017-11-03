---
title: "Üretim emri durumunu tersine çevirme"
description: "Bu konuda, üretim emri durumunun tersine çevrilmesi açıklanmaktadır."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParmStatusDecrease
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 70131
ms.assetid: b1e0df43-b388-4326-8fb7-501f30c89776
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4761e44b6bbc93ebf4a395948f42c2a73013ecb9
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="reverse-the-production-order-status"></a><span data-ttu-id="511a2-103">Üretim emri durumunu tersine çevirme</span><span class="sxs-lookup"><span data-stu-id="511a2-103">Reverse the production order status</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="511a2-104">Bu konuda, üretim emri durumunun tersine çevrilmesi açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="511a2-104">This topic describes how to reverse production order status.</span></span> 

<span data-ttu-id="511a2-105">Bir üretim emrinin durumunu tersine çevirirseniz, emrin kendisi ve rotalarla ilişkili tüm operasyonlar üretim döngüsündeki önceki bir adıma geri döner.</span><span class="sxs-lookup"><span data-stu-id="511a2-105">If you reverse the status of a production order, the order and all operations that are associated with the routes revert to a previous step in the production life cycle.</span></span> <span data-ttu-id="511a2-106">Örneğin, bir üretim emrinin durumunu **Planlandı** ise ve durumu yeniden **Oluşturuldu** olarak değiştirirseniz.</span><span class="sxs-lookup"><span data-stu-id="511a2-106">For example, a production order has a status of **Scheduled**, and you change the status back to **Created**.</span></span> <span data-ttu-id="511a2-107">Bu durumda, sistem önce durumu **Tahmini** olarak değiştirir ki bu **Planlandı**'nın hemen öncesindeki durumdur.</span><span class="sxs-lookup"><span data-stu-id="511a2-107">In this case, the system must first change the status to **Estimated**, which is the status that immediately precedes **Scheduled**.</span></span> <span data-ttu-id="511a2-108">Daha sonra durumu istediğiniz **Oluşturuldu** durumuna değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="511a2-108">It can then change the status to the status that you want, **Created**.</span></span> <span data-ttu-id="511a2-109">**Not:** Emriniz **Tamamlandı bildirimi** durumuna geldiyse, yine de önceki bir duruma geri döndürebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="511a2-109">**Note:** If your order has reached the **Report as finished** status, you can still reverse it to an earlier status.</span></span> <span data-ttu-id="511a2-110">Ancak emirdeki bilgileri güncellemek için tahmini ve operasyon planlamasını, iş planlamasını veya her iki planlama türünü yeniden çalıştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="511a2-110">However, you must re-run estimation and operations scheduling, job scheduling, or both types of scheduling, to update the information on the order.</span></span> <span data-ttu-id="511a2-111">Bu adım gereklidir çünkü kalan madde tüketimi ve operasyon kaynakları tüketimi rezervasyonları da sıfırlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="511a2-111">This step is required, because any reservations of remaining item consumption and operations resource consumption must also be reset.</span></span> <span data-ttu-id="511a2-112">Bu makalenin geri kalanında, bir üretim emrini aşağıdaki şekillerde tersine çevirdiğinizde neler olduğu anlatılmaktadır:</span><span class="sxs-lookup"><span data-stu-id="511a2-112">The rest of this article explains what occurs when you reverse the status of a production order in the following ways:</span></span>

-   <span data-ttu-id="511a2-113">**Tahmin**'den **Oluşturuldu**'ya</span><span class="sxs-lookup"><span data-stu-id="511a2-113">From **Estimated** to **Created**</span></span>
-   <span data-ttu-id="511a2-114">**Planlandı**'dan **Tahmin**'e</span><span class="sxs-lookup"><span data-stu-id="511a2-114">From **Scheduled** to **Estimated**</span></span>
-   <span data-ttu-id="511a2-115">**Serbest bırakıldı**'dan **Planlandı**'ya</span><span class="sxs-lookup"><span data-stu-id="511a2-115">From **Released** to **Scheduled**</span></span>
-   <span data-ttu-id="511a2-116">**Başlatıldı**'dan **Serbest bırakıldı**'ya</span><span class="sxs-lookup"><span data-stu-id="511a2-116">From **Started** to **Released**</span></span>

## <a name="from-estimated-to-created"></a><span data-ttu-id="511a2-117">Tahmin'den Oluşturuldu'ya</span><span class="sxs-lookup"><span data-stu-id="511a2-117">From Estimated to Created</span></span>
<span data-ttu-id="511a2-118">Bir üretim emrinin durumunu **Tahmin**'den **Oluşturuldu**'ya çevirdiğinizde, ürün reçetesindeki maddeler için hesaplanan madde tüketimi kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="511a2-118">When you reverse the status of a production order from **Estimated** to **Created**, the item consumption that was calculated for the items in the bill of materials (BOM) is removed.</span></span> <span data-ttu-id="511a2-119">Üretim satırındaki stok hareketleri silinir ve üretim emri ürün reçetesi satırlarındaki **Artık durumu** alanı **Bitti** olarak sıfırlanır.</span><span class="sxs-lookup"><span data-stu-id="511a2-119">Inventory transactions on the production line are deleted, and the **Remain status** field on the production order's BOM lines is reset to **Ended**.</span></span> <span data-ttu-id="511a2-120">**Türetilmiş satınalmalar** ve **Türetilmiş üretim** seçenekleri seçildiğinde, altta yatan satınalma emirleri veya üretim emirleri silinir.</span><span class="sxs-lookup"><span data-stu-id="511a2-120">When the **Derived purchases** and **Derived production** options are selected, any underlying purchase orders or production orders are deleted.</span></span> <span data-ttu-id="511a2-121">Üretim emrinin maliyetini tahmin ettiyseniz veya maddeleri üretimde kullanılabilmeleri için manuel olarak ters çevirdiyseniz, bu hareketler kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="511a2-121">If you estimated the costs of the production order, or if you manually reserved items so that they could be used in production, those transactions are removed.</span></span>

## <a name="from-scheduled-to-estimated"></a><span data-ttu-id="511a2-122">Planlandı'dan Tahmin'e</span><span class="sxs-lookup"><span data-stu-id="511a2-122">From Scheduled to Estimated</span></span>
<span data-ttu-id="511a2-123">Bir üretim emrinin durumunu **Planlandı**'dan **Tahmin**'e çevirirseniz, planlanan başlangıç ve bitiş tarihleri ve saatleri kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="511a2-123">When you reverse the status of a production order from **Scheduled** to **Estimated**, the scheduled start and end dates and times are removed.</span></span> <span data-ttu-id="511a2-124">Planlama sırasında yapılan kapasite rezervasyonları kaldırılır ve iş planlama sırasında oluşturulan işler silinir.</span><span class="sxs-lookup"><span data-stu-id="511a2-124">Capacity reservations that were made during scheduling are removed, and jobs that were created during job scheduling are deleted.</span></span> <span data-ttu-id="511a2-125">Operasyon planlaması ve iş planlaması ile ilgili olarak **Üretim emri ayrıntıları** sayfasında kayıtlı tüm bilgiler sıfırlanır.</span><span class="sxs-lookup"><span data-stu-id="511a2-125">All information that is recorded about operation scheduling and job scheduling on the **Production order details** page is reset.</span></span>

## <a name="from-released-to-scheduled"></a><span data-ttu-id="511a2-126">Serbest bırakıldı'dan Planlandı'ya</span><span class="sxs-lookup"><span data-stu-id="511a2-126">From Released to Scheduled</span></span>
<span data-ttu-id="511a2-127">Bir üretim emrinin durumunu **Serbest bırakıldı**'dan **Planlandı**'ya çevirirseniz, gerçekleşecek tek değişiklik durum alanındaki değerdir.</span><span class="sxs-lookup"><span data-stu-id="511a2-127">When you reverse the status of a production order from **Released** to **Scheduled**, the only change that occurs is the value in the status field.</span></span>

## <a name="from-started-to-released"></a><span data-ttu-id="511a2-128">Başlatıldı'dan Serbest bırakıldı'ya</span><span class="sxs-lookup"><span data-stu-id="511a2-128">From Started to Released</span></span>
<span data-ttu-id="511a2-129">Bir üretim emrinin durumunu **Başlatıldı**'dan **Serbest bırakıldı**'ya çevirirseniz, bitmiş olarak raporlanan tüm maddeler tersine çevrilir.</span><span class="sxs-lookup"><span data-stu-id="511a2-129">When you reverse the status of a production order from **Started** to **Released**, all items that were reported as finished are reverted.</span></span> <span data-ttu-id="511a2-130">Malzeme alındıysa ve üretime gelen ve giden teslimatlar yapıldıysa, bu ayarlar tersine çevrilir.</span><span class="sxs-lookup"><span data-stu-id="511a2-130">If material has been picked, or if inbound and outbound deliveries have been made to production, those settings are reversed.</span></span> <span data-ttu-id="511a2-131">Üretim emrinin ürün reçetesi satırlarındaki **Artık durumu** alanı **Bitti**'den **Malzeme tüketimi**'ne değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="511a2-131">The **Remain status** field on the production order’s BOM lines is changed from **Ended** to **Material consumption**.</span></span> <span data-ttu-id="511a2-132">Saat kayda geçirildiyse veya üretim rotasındaki operasyonlar için miktarlar bitti şeklinde rapor edildiyse, bu ayarlar ters çevrilir.</span><span class="sxs-lookup"><span data-stu-id="511a2-132">If time has been registered, or if quantities have been reported as finished for the operations in the production route, those settings are reversed.</span></span> <span data-ttu-id="511a2-133">**Artık durumu** alanı, üretim rotasında **Bitti**'den **Rota tüketimi**'ne değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="511a2-133">The **Remain status** field is changed from **Ended** to **Route consumption** in the production route.</span></span> <span data-ttu-id="511a2-134">Devam eden olarak veya süren iş olarak nakledilen tüm maddelere yönelik ayarlar ters çevrilir.</span><span class="sxs-lookup"><span data-stu-id="511a2-134">The settings for all items that are posted as in process or work in process are reversed.</span></span> <span data-ttu-id="511a2-135">**Üretim emri ayrıntıları** sayfasında, başlatılmış veya bitmiş olarak raporlanmış bir miktar gösteren alanlar sıfırlanır.</span><span class="sxs-lookup"><span data-stu-id="511a2-135">On the **Production order details** page, fields that show a quantity that was started or reported as finished are reset.</span></span> <span data-ttu-id="511a2-136">Bu hareketlere yönelik tarihleri de sıfırlanır.</span><span class="sxs-lookup"><span data-stu-id="511a2-136">The dates for those transactions are also reset.</span></span>





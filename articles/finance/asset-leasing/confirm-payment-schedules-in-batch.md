---
title: Toplu işte Varlık kiralama ödeme planlarını onaylama
description: Bu konuda, birden fazla ödeme planının toplu işte nasıl onaylanacağı açıklanmaktadır.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b5a90b96ac598d145e2b0697627de04731b55f59
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4449016"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a><span data-ttu-id="eaf43-103">Toplu işte Varlık kiralama ödeme planlarını onaylama</span><span class="sxs-lookup"><span data-stu-id="eaf43-103">Confirm Asset leasing payment schedules in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eaf43-104">Bu konuda, birden fazla ödeme planının toplu işte nasıl onaylanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="eaf43-104">This topic explains how to confirm multiple payment schedules in a batch.</span></span> <span data-ttu-id="eaf43-105">Ödeme planları, kiralama bazında veya onay toplu iş işlemi aracılığıyla onaylanır.</span><span class="sxs-lookup"><span data-stu-id="eaf43-105">Payment schedules are confirmed either on a lease-to-lease basis or through the confirmation batch process.</span></span> <span data-ttu-id="eaf43-106">Bir günlük girişi yalnızca onaylanmış bir ödeme planı olan bir kiralama için deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="eaf43-106">A journal entry can be posted only against a lease that has a confirmed payment schedule.</span></span> <span data-ttu-id="eaf43-107">Ödeme planının onayı, kiralamaya ilişkin mali bilgilerin son onayı görevi görür.</span><span class="sxs-lookup"><span data-stu-id="eaf43-107">Confirmation of the payment schedule serves as a final approval of the financial information for the lease.</span></span> <span data-ttu-id="eaf43-108">Kiralamanın mali bilgilerinde yapılacak olan tüm değişiklikler (ör. ödemeler ve kiralama süresi) kiralama düzeltmesi oluşturur ve bu şekilde işlenmelidir.</span><span class="sxs-lookup"><span data-stu-id="eaf43-108">All future changes to the financial information for the lease, such as payments and the lease term, constitute a lease adjustment and should be processed in that way.</span></span>

<span data-ttu-id="eaf43-109">Birden fazla ödeme planını onaylamak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="eaf43-109">To confirm multiple payment schedules, follow these steps.</span></span>

1. <span data-ttu-id="eaf43-110">**Varlık kiralama \> Periyodik \> Onay toplu işi** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="eaf43-110">Go to **Asset leasing \> Periodic \> Confirmation batch**.</span></span>
2. <span data-ttu-id="eaf43-111">**Onay toplu işi** sayfasında **Onay toplu işi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="eaf43-111">On the **Confirmation batch** page, select **Confirmation batch**.</span></span>
3. <span data-ttu-id="eaf43-112">Görüntülenen iletişim kutusunda onaylamak istediğiniz defterlere filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="eaf43-112">In the dialog box that appears, filter for the books that you want to confirm.</span></span>

    - <span data-ttu-id="eaf43-113">Belirli bir kiralama grubundaki tüm defterleri onaylamak için **Kiralama grubu** alanında grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="eaf43-113">To confirm all the books in a specific lease group, select the group in the **Lease group** field.</span></span>
    - <span data-ttu-id="eaf43-114">Belirli defterleri onaylamak için **Defter Kimliği** alanında defterleri seçin.</span><span class="sxs-lookup"><span data-stu-id="eaf43-114">To confirm specific books, select the books in the **Book ID** field.</span></span>
    - <span data-ttu-id="eaf43-115">Tüm defterleri onaylamak için **Tüm defterler için** parametresini açın.</span><span class="sxs-lookup"><span data-stu-id="eaf43-115">To confirm all books, turn on the **For all books** parameter.</span></span>

<span data-ttu-id="eaf43-116">Yeni onaylanan defterlerle ilgili bilgiler **Onaylanan defterler** sayfasında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="eaf43-116">Information for the newly confirmed books is shown on the **Confirmed books** page.</span></span> <span data-ttu-id="eaf43-117">Ödeme planları onaylandıktan sonra, kiralamalara göre ilk kabul günlüğü girişleri deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="eaf43-117">After the payment schedules are confirmed, the initial recognition journal entries can be posted against the leases.</span></span>

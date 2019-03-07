---
title: Başkasının yerine ürün sipariş etmek için izinleri ayarlama
description: Bu prosedür diğer çalışanların adına satınalma talepleri hazırlamak için çalışanlara nasıl izin verileceğini gösterir.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35688d191cef06cc15251a6e10a2e8c9afb0e08b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "314820"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a><span data-ttu-id="af3bf-103">Başkasının yerine ürün sipariş etmek için izinleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="af3bf-103">Set up permissions for ordering products on behalf of someone else</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="af3bf-104">Bu prosedür diğer çalışanların adına satınalma talepleri hazırlamak için çalışanlara nasıl izin verileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="af3bf-104">This procedure shows how to grant workers permission to prepare purchase requisitions on behalf of other workers.</span></span> <span data-ttu-id="af3bf-105">Başka bir deyişle, bir satınalma talebi "hazırlayıcısı", başka bir "hazırlayıcı" için bir talep oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="af3bf-105">In other words, a purchase requisition “preparer” can create a requisition for another “requester.”</span></span> <span data-ttu-id="af3bf-106">Bu yordam ayrıca bir çalışanın farklı tüzel varlıklarda veya işletme birimlerindeki sipariş öğelerine ve nasıl erişim verileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="af3bf-106">The procedure also shows how to grant a worker permission to order items and services in different legal entities or operating units.</span></span> <span data-ttu-id="af3bf-107">Bu görevler genellikle bir satınalma yöneticisi tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="af3bf-107">Typically, these tasks are performed by a purchasing manager.</span></span> <span data-ttu-id="af3bf-108">Bu prosedürü USMF demo şirketindeki verilerde veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="af3bf-108">You can use this procedure either on data for the USMF demo company or on your own data.</span></span>


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a><span data-ttu-id="af3bf-109">Başka bir çalışanın adına satınalma talepleri girmek için izin verin</span><span class="sxs-lookup"><span data-stu-id="af3bf-109">Grant permission to enter purchase requisitions on behalf of another worker</span></span>
1. <span data-ttu-id="af3bf-110">Tedarik ve kaynak atama > Ayarlar > İlkeler > Satınalma talebi izinleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="af3bf-110">Go to Procurement and sourcing > Setup > Policies > Purchase requisition permissions.</span></span>
    * <span data-ttu-id="af3bf-111">Geçerli görünüm alanının Hazırlayana göre olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="af3bf-111">Make sure that the Current view field is set to By preparer.</span></span>  <span data-ttu-id="af3bf-112">Sol bölmedeki liste diğer kişiler adına talepler hazırlamak için izin verilmiş kişileri gösterir.</span><span class="sxs-lookup"><span data-stu-id="af3bf-112">The list in the left pane shows the people who can be granted permission to prepare requisitions on behalf of other people.</span></span>  
2. <span data-ttu-id="af3bf-113">İzin verilecek kişiyi (hazırlayan) seçin.</span><span class="sxs-lookup"><span data-stu-id="af3bf-113">Select the person to grant permission to (the preparer).</span></span>
3. <span data-ttu-id="af3bf-114">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="af3bf-114">Click Add.</span></span>
4. <span data-ttu-id="af3bf-115">Talep sahibi olarak eklemek istediğiniz kişiyi bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="af3bf-115">Find and select the person to add as a requester.</span></span>
    * <span data-ttu-id="af3bf-116">Talep sahibi hazırlayanın adına talepler oluşturabilen kişidir.</span><span class="sxs-lookup"><span data-stu-id="af3bf-116">The requester is the person that the preparer can create requisitions on behalf of.</span></span>  
    * <span data-ttu-id="af3bf-117">Hazırlayanın seçilen çalışan adına satınalma talepleri oluşturabilmesi gerekiyorsa Yetkilendirme alanında Özel'i seçin.</span><span class="sxs-lookup"><span data-stu-id="af3bf-117">In the Authorization field, select Specific if the preparer should be able to create purchase requisitions on behalf of the selected worker.</span></span> <span data-ttu-id="af3bf-118">Hazırlayanın bu çalışana rapor veren tüm çalışanlar adına satınalma talebi oluşturabilmesi gerekiyorsa Raporlama'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="af3bf-118">Select Reporting if the preparer should also be able to create purchase requisitions on behalf of all workers who report to that worker.</span></span>  
5. <span data-ttu-id="af3bf-119">Etkili alanında bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="af3bf-119">In the Effective field, enter a date.</span></span>
6. <span data-ttu-id="af3bf-120">Bitiş alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="af3bf-120">In the Expiration field, enter a date.</span></span>

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a><span data-ttu-id="af3bf-121">Seçilen çalışan için satınalma talebi oluşturma iznine sahip hazırlayanları görüntüleyin</span><span class="sxs-lookup"><span data-stu-id="af3bf-121">View preparers who have permission to create purchase requisitions for a selected worker</span></span>
1. <span data-ttu-id="af3bf-122">Geçerli görünüm alanından 'Talep sahibine göre'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="af3bf-122">In the Current view field, select 'By requester'.</span></span>
    * <span data-ttu-id="af3bf-123">Bu görünüm seçilen çalışan adına satınalma talepleri oluşturmak için izin verilen hazırlayanların listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="af3bf-123">This view shows a list of preparers who have been granted permission to create purchase requisitions on behalf of a selected worker.</span></span>  
2. <span data-ttu-id="af3bf-124">Talep sahibi olarak yeni eklediğiniz çalışanı bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="af3bf-124">Use the Quick Filter to find the worker that you just added as the requester.</span></span>
3. <span data-ttu-id="af3bf-125">Talep sahibini seçin.</span><span class="sxs-lookup"><span data-stu-id="af3bf-125">Select the requester.</span></span>
    * <span data-ttu-id="af3bf-126">Hazırlayan listesi sol bölmede seçilen talep sahibi adına maddeleri sipariş etme izni olan kişileri gösterir.</span><span class="sxs-lookup"><span data-stu-id="af3bf-126">The Preparer list shows the people who have permission to order items on behalf of the requester who is selected in the left pane.</span></span>   <span data-ttu-id="af3bf-127">Buraya ek hazırlayanlar ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="af3bf-127">You can add additional preparers here.</span></span>   <span data-ttu-id="af3bf-128">Bu görünüm kişinin birincil tüzel kişiliği veya faaliyet birimi olamayan tüzel kişilikler ve faaliyet birimlerinde talep sahibine talepler oluşturmak için izin vermenizi de sağlar.</span><span class="sxs-lookup"><span data-stu-id="af3bf-128">This view also lets you grant the requester permission to create requisitions in legal entities and operating units that aren't that person's primary legal entity or operating unit.</span></span>  


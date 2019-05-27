---
title: " Bağlılık ödül puanı ayarlamalarını işleme"
description: Bu yordam ile, Bağlılık kartı bilgilerini aramak ve bağlılık programı Ödül puanları ayarlamak gösterilmiştir.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyCards, RetailLoyaltyCardRewardPointTrans, RetailLoyaltyCardRewardPointAdjustment, RetailAffiliationLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85aaa82bf56d55c69f39bab49682c79f51247251
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550197"
---
# <a name="process-loyalty-reward-point-adjustments"></a><span data-ttu-id="dabaa-103"> Bağlılık ödül puanı ayarlamalarını işleme</span><span class="sxs-lookup"><span data-stu-id="dabaa-103">Process loyalty reward point adjustments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="dabaa-104">Bu yordam ile, Bağlılık kartı bilgilerini aramak ve bağlılık programı Ödül puanları ayarlamak gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="dabaa-104">This procedure demonstrates how to look up loyalty card information and adjust loyalty reward points.</span></span> <span data-ttu-id="dabaa-105">Bu görevi oluşturmak için kullanılan demo verisi şirketi USRT'dir.</span><span class="sxs-lookup"><span data-stu-id="dabaa-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="dabaa-106">Bu görev, perakende işlem yöneticisi rolü veya bir müşteri Hizmet Yöneticisi rolü olarak hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="dabaa-106">This task is intended for the Retail operations manager role or a Customer service manager role.</span></span>

1. <span data-ttu-id="dabaa-107">Bağlılık kartına git.</span><span class="sxs-lookup"><span data-stu-id="dabaa-107">Go to Loyalty cards.</span></span>
2. <span data-ttu-id="dabaa-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="dabaa-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="dabaa-109">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dabaa-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="dabaa-110">Kart hareketlerine tıkla.</span><span class="sxs-lookup"><span data-stu-id="dabaa-110">Click Card transactions.</span></span>
    * <span data-ttu-id="dabaa-111">Bu sayfada seçilen bağlılık programı kartının tüm bağlılık hareketleri görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dabaa-111">On this page you can view all loyalty transactions for the selected loyalty card.</span></span>  
5. <span data-ttu-id="dabaa-112">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="dabaa-112">Close the page.</span></span>
6. <span data-ttu-id="dabaa-113">Kart düzeltmelerine tıkla.</span><span class="sxs-lookup"><span data-stu-id="dabaa-113">Click Card adjustments.</span></span>
7. <span data-ttu-id="dabaa-114">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dabaa-114">Click New.</span></span>
8. <span data-ttu-id="dabaa-115">Ödül puanı alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="dabaa-115">In the Reward point field, enter or select a value.</span></span>
9. <span data-ttu-id="dabaa-116">Tutar veya miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="dabaa-116">In the Amount or quantity field, enter a number.</span></span>
    * <span data-ttu-id="dabaa-117">Pozitif veya negatif tutarlar kullanılarak bağlılık kartından puanlar ekleyebilir veya azaltabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dabaa-117">You can add or remove points from the loyalty card by using positive or negative amounts.</span></span>  
10. <span data-ttu-id="dabaa-118">Bağlılık programı alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="dabaa-118">In the Loyalty program field, enter or select a value.</span></span>
11. <span data-ttu-id="dabaa-119">Açıklama alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="dabaa-119">In the Comment field, type a value.</span></span>
12. <span data-ttu-id="dabaa-120">Düzeltmeyi gönder'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dabaa-120">Click Post adjustment.</span></span>
13. <span data-ttu-id="dabaa-121">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dabaa-121">Click Yes.</span></span>
14. <span data-ttu-id="dabaa-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="dabaa-122">Close the page.</span></span>
    * <span data-ttu-id="dabaa-123">Normalde bu noktada ödül puanları özet sekmesinde ödül puanları ayarlaması sonucunu görmek için sayfayı yenilemeniz gerekir. Ancak bunu görev kılavuzu olarak çalıştırıyorsanız, şimdi yenilemeyin çünkü bunu yaparsanız, görev duracaktır.</span><span class="sxs-lookup"><span data-stu-id="dabaa-123">Normally at this point you'd refresh the page to see the result of the reward points adjustment in the Reward point summary tab. But if you are running this as a task guide, don't refresh now because if you do, the task guide will stop.</span></span>  
15. <span data-ttu-id="dabaa-124">Kart hareketlerine tıkla.</span><span class="sxs-lookup"><span data-stu-id="dabaa-124">Click Card transactions.</span></span>
16. <span data-ttu-id="dabaa-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="dabaa-125">Close the page.</span></span>


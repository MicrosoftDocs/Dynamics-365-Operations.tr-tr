---
title: " Perakende ekstreleri için mağaza yapılandırmaları"
description: Bu yordam, Perakende ekstrelerinin oluşturulması ve nakledilmesini etkileyen Perakende mağazasına ilişkin yapılandırmaları gösterir.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9fddeb8434d916df1613d61da88110dec8fb4465
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "354725"
---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="5147f-103"> Perakende ekstreleri için mağaza yapılandırmaları</span><span class="sxs-lookup"><span data-stu-id="5147f-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="5147f-104">Bu yordam, Perakende ekstrelerinin oluşturulması ve nakledilmesini etkileyen Perakende mağazasına ilişkin yapılandırmaları gösterir.</span><span class="sxs-lookup"><span data-stu-id="5147f-104">This procedure walks through configurations for the Retail store that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="5147f-105">Perakende mağazalardaki mali boyutlar başka bir yordamda anlatılacaktır.</span><span class="sxs-lookup"><span data-stu-id="5147f-105">Financial dimensions on Retail stores are covered in another procedure.</span></span> <span data-ttu-id="5147f-106">Bu yordam, USRT demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="5147f-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="5147f-107">Retail and commerce > Channels > Retail stores > All retail stores (Perakende ve ticaret > Kanallar > Perakende mağazaları > Tüm perakende mağazaları) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="5147f-107">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="5147f-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5147f-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="5147f-109">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5147f-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5147f-110">Ekstre/kapanış bölümündeki ayarlar mağaza için ekstre oluşturma, doğrulama ve deftere nakil işlemlerini etkiler.</span><span class="sxs-lookup"><span data-stu-id="5147f-110">The settings in the Statement/closing section affect the statement creation, validation, and posting for the store.</span></span>  <span data-ttu-id="5147f-111">Ekstre/kapanış bölümünü açın.</span><span class="sxs-lookup"><span data-stu-id="5147f-111">Open the Statement/closing section.</span></span>  
    * <span data-ttu-id="5147f-112">Ekstre satırlarını gruplandırmak için kullanmak istediğiniz yöntemi seçin.</span><span class="sxs-lookup"><span data-stu-id="5147f-112">Select the method you want to use to to group the statement lines by.</span></span>  
    * <span data-ttu-id="5147f-113">Ekstreleri ekstre oluşturma toplu işinden oluştururken her gün için yalnızca bir ekstre oluşturulması gerekiyorsa "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="5147f-113">Select "Yes" if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
    * <span data-ttu-id="5147f-114">Kasa sayımı hesaplaması alanı, ödeme beyanlarının birlikte mi ekleneceğini yoksa son eklenen beyanın mı kullanılacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="5147f-114">The Tender declaration calculation field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
    * <span data-ttu-id="5147f-115">Yuvarlama farklarının nakledileceği genel muhasebe hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="5147f-115">Select the ledger account to post rounding differences into.</span></span>  
    * <span data-ttu-id="5147f-116">Maksimum yuvarlama farkı alanına izin verilen maksimum yuvarlama farkını girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5147f-116">In the Maximum rounding difference field, you can enter the maximum rounding difference allowed.</span></span>  
    * <span data-ttu-id="5147f-117">Deftere nakil alanına, bir ekstre için izin verilen maksimum toplam deftere nakil farkını girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5147f-117">In the Posting field, you can enter the maximum total posting difference allowed for a statement.</span></span>  
    * <span data-ttu-id="5147f-118">Vardiya alanına, ekstrede yer alan bir vardiyadaki maksimum toplam farkı girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5147f-118">In the Shift field, you can enter the maximum total difference within a shift in a statement.</span></span>  
    * <span data-ttu-id="5147f-119">Hareket alanına, ekstre satırındaki maksimum toplam farkı girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5147f-119">In the Transaction field, you can enter the maximum total difference in a statement line.</span></span>  
    * <span data-ttu-id="5147f-120">Kapanış yöntemi alanında, bir ekstreye dahil edilen hareketlerin kapatılan bir vardiyanın bir parçası mı olacağını yoksa belirlenen tarih/saat aralığındaki herhangi bir hareketin kullanılmasının mümkün olup olmayacağını belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5147f-120">In the Closing method field, you can define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
    * <span data-ttu-id="5147f-121">İş günü sonu alanına, gece yarısından sonra gerçekleştirilen hareketlerin önceki gün için deftere kaydedilmesi gerekiyorsa bir saat girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5147f-121">In the End of business day field, you can enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
    * <span data-ttu-id="5147f-122">Gece yarısından sonra gerçekleşen hareketlerin deftere önceki günün bir parçası olarak nakledilmesi gerekiyorsa "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="5147f-122">Select "Yes" if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
    * <span data-ttu-id="5147f-123">Tanımlanan her ekstre yöntemi için oluşturulan ekstreleri almak için "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="5147f-123">Select "Yes" to get statements created for each statement method defined.</span></span> <span data-ttu-id="5147f-124">Bu, aynı ayna işlenebilecek çok sayıda küçük ekstre oluşturacağından, deftere nakil performansının yüksek hareket hacmine sahip mağazalar için geliştirilmesi gerektiğinde yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="5147f-124">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
    * <span data-ttu-id="5147f-125">Varsayılan müşteri alanında, bağımsız müşterilere satış için kullanılacak müşteri hesabını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5147f-125">In the Default customer field, you can select the customer account to use for sales to walk-in customers.</span></span>  


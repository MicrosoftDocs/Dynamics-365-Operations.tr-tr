---
title: " Perakende ekstreleri için mağaza yapılandırmaları"
description: Bu yordam, Commerce ekstrelerinin oluşturulması ve nakledilmesini etkileyen mağazasına ilişkin yapılandırmaları gösterir.
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
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
ms.openlocfilehash: 4b73282abd2df92b3f466f7c1c6c210173001fd7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024304"
---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="ac9ba-103"> Perakende ekstreleri için mağaza yapılandırmaları</span><span class="sxs-lookup"><span data-stu-id="ac9ba-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ac9ba-104">Bu yordam, Commerce ekstrelerinin oluşturulması ve nakledilmesini etkileyen mağazasına ilişkin yapılandırmaları gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-104">This procedure walks through configurations for the store that affect how Commerce statements get created and posted.</span></span> <span data-ttu-id="ac9ba-105">Mağazalardaki mali boyutlar başka bir yordamda anlatılacaktır.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-105">Financial dimensions on stores are covered in another procedure.</span></span> <span data-ttu-id="ac9ba-106">Bu yordam, USRT demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="ac9ba-107">**Gezinme paneli**'nde, **Modüller > Perakende ve Ticaret > Kanallar > Mağazaları > Tüm mağazaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-107">In the **Navgiation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
2. <span data-ttu-id="ac9ba-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ac9ba-109">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ac9ba-110">**Düzenle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-110">Click **Edit**.</span></span>
5. <span data-ttu-id="ac9ba-111">**Ekstre/kapanış** hızlı sekmesindeki ayarlar mağaza için ekstre oluşturma, doğrulama ve deftere nakil işlemlerini etkiler.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-111">The settings in the **Statement/closing** fastTab affect the statement creation, validation, and posting for the store.</span></span> <span data-ttu-id="ac9ba-112">**Ekstre/Kapanış** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-112">Expand the **Statement/closing** fastTab.</span></span>  
6. <span data-ttu-id="ac9ba-113">**Ekstre yöntemi** alanında, ekstre satırlarını gruplandırmak için kullanmak istediğiniz yöntemi seçin.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-113">In the **Statement method** field, select the method you want to use to to group the statement lines by.</span></span>  
7. <span data-ttu-id="ac9ba-114">Ekstreleri ekstre oluşturma toplu işinden oluştururken her gün için yalnızca bir ekstre oluşturulması gerekiyorsa **Her gün bir ekstre**'ye "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-114">Select "Yes" in **One statement per day** if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
8. <span data-ttu-id="ac9ba-115">**Kasa sayımı hesaplaması** alanı, ödeme beyanlarının birlikte mi ekleneceğini yoksa son eklenen beyanın mı kullanılacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-115">The **Tender declaration calculation** field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
9. <span data-ttu-id="ac9ba-116">**Yuvarlama** alanında yuvarlama farklarının nakledileceği genel muhasebe hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-116">In the **Rounding** field, select the ledger account to post rounding differences into.</span></span>  
10. <span data-ttu-id="ac9ba-117">**Maksimum yuvarlama farkı** alanına izin verilen maksimum yuvarlama farkını girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-117">In the **Maximum rounding difference** field, enter the maximum rounding difference allowed.</span></span>
11. <span data-ttu-id="ac9ba-118">**Deftere nakil** alanına, bir ekstre için izin verilen maksimum toplam deftere nakil farkını girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-118">In the **Posting** field, enter the maximum total posting difference allowed for a statement.</span></span>
12. <span data-ttu-id="ac9ba-119">**Vardiya** alanına, ekstrede yer alan bir vardiyadaki maksimum toplam farkı girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-119">In the **Shift** field, enter the maximum total difference within a shift in a statement.</span></span>  
13. <span data-ttu-id="ac9ba-120">**Hareket** alanına, ekstre satırındaki maksimum toplam farkı girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-120">In the **Transaction** field, enter the maximum total difference in a statement line.</span></span>  
14. <span data-ttu-id="ac9ba-121">**Kapanış yöntemi** alanında, bir ekstreye dahil edilen hareketlerin kapatılan bir vardiyanın bir parçası mı olacağını yoksa belirlenen tarih/saat aralığındaki herhangi bir hareketin kullanılmasının mümkün olup olmayacağını belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-121">In the **Closing method** field, define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
15. <span data-ttu-id="ac9ba-122">**İş günü sonu** alanına, gece yarısından sonra gerçekleştirilen hareketlerin önceki gün için deftere kaydedilmesi gerekiyorsa bir saat girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-122">In the **End of business day** field, enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
16. <span data-ttu-id="ac9ba-123">Gece yarısından sonra gerçekleşen hareketlerin deftere önceki günün bir parçası olarak nakledilmesi gerekiyorsa **İş günü olarak naklet**'i "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-123">Select "Yes" in **Post as business day** if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
17. <span data-ttu-id="ac9ba-124">Tanımlanan her ekstre yöntemi için oluşturulan ekstreleri almak için **Ekstre yöntemine göre böl**'e "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-124">Select "Yes" in **Split by Statement method** to get statements created for each statement method defined.</span></span> <span data-ttu-id="ac9ba-125">Bu, aynı ayna işlenebilecek çok sayıda küçük ekstre oluşturacağından, deftere nakil performansının yüksek hareket hacmine sahip mağazalar için geliştirilmesi gerektiğinde yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-125">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
18. <span data-ttu-id="ac9ba-126">**Genel** hızlı sekmesinde **Varsayılan müşteri** alanında, bağımsız müşterilere satış için kullanılacak müşteri hesabını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac9ba-126">In the **General** fastTab, in the **Default customer** field, you can select the customer account to use for sales to walk-in customers.</span></span>  


---
title: Satış vergisi kapatma dönemlerini ayarlama
description: Bu konuda, Dynamics 365 Finance'da satış vergisi kapatma dönemlerini nasıl ayarlanacağı açıklanmaktadır.
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5972c44261a6ebd49df0fcbcef9a8c60aaa487e2
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144732"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="ccb04-103">Satış vergisi kapatma dönemlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="ccb04-103">Set up sales tax settlement periods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ccb04-104">Bu konuda, satış vergisi kapatma dönemlerinin nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ccb04-104">This topic explains how to set up sales tax settlement periods.</span></span> <span data-ttu-id="ccb04-105">Satış vergisi kapatma dönemleri, satış vergisinin bildirilip ödenmesi gereken dönem aralıkları hakkında bilgiler içerir.</span><span class="sxs-lookup"><span data-stu-id="ccb04-105">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="ccb04-106">Belirli bir tarih aralığında bir kapatma dönemi için bir kapatma işlemi yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="ccb04-106">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="ccb04-107">Kapatma dönemiyle ilişkili tüm vergi kodları kapatılır.</span><span class="sxs-lookup"><span data-stu-id="ccb04-107">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="ccb04-108">İlgili satış vergisi dairesinin ayarlarına bağlı olarak, vergi borcu ya bir satıcıya veya bir Genel muhasebe hesabına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="ccb04-108">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>

<span data-ttu-id="ccb04-109">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ccb04-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="ccb04-110">Gezinti bölmesinde **Modüller > Vergi > Dolaylı vergiler > Satış vergisi > Satış vergisi kapatma dönemleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ccb04-110">In the navigation pane, go to **Modules > Tax > Indirect taxes > Sales tax > Sales tax settlement periods**.</span></span>
2. <span data-ttu-id="ccb04-111">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ccb04-111">Select **New**.</span></span>
3. <span data-ttu-id="ccb04-112">**Kapatma dönemi** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ccb04-112">In the **Settlement period** field, type a value.</span></span>
4. <span data-ttu-id="ccb04-113">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ccb04-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="ccb04-114">**Makam** alanında kapatma dönemi için oluşturulan bildirimleri ve ödemeleri alan satış vergisi makamını seçin.</span><span class="sxs-lookup"><span data-stu-id="ccb04-114">In the **Authority** field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="ccb04-115">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ccb04-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ccb04-116">**Ödeme koşulları** alanında, açılır menüden istediğiniz kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="ccb04-116">In the **Terms of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="ccb04-117">İlgili Satış vergi dairesi, bir satıcı olarak kurulabilir ve Satış vergisi kapatma işlemi bir açık satıcı faturası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ccb04-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="ccb04-118">Ödeme koşulları, açık satıcı faturası için Vade tarihi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ccb04-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
8. <span data-ttu-id="ccb04-119">Kapatma dönemi aralıkları için tür seçin.</span><span class="sxs-lookup"><span data-stu-id="ccb04-119">Select a type for the settlement period intervals.</span></span>
9. <span data-ttu-id="ccb04-120">Dönem başına dönem aralığı birim sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="ccb04-120">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="ccb04-121">Örneğin üç aylık dönemde 3 ay vardır.</span><span class="sxs-lookup"><span data-stu-id="ccb04-121">For example, a quarter has 3 months.</span></span>
10. <span data-ttu-id="ccb04-122">**Satış vergisi kapatma için toplu iş kullan** onay kutusunu işaretleyin veya kutuda işaret varsa kaldırın.</span><span class="sxs-lookup"><span data-stu-id="ccb04-122">Select or clear the **Use batch processing for sales tax settlement** check box.</span></span> <span data-ttu-id="ccb04-123">Kapatma dönemi için kapatma işlemi arka planda toplu iş olarak sürdürülebilir.</span><span class="sxs-lookup"><span data-stu-id="ccb04-123">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="ccb04-124">Bu bir dönem aralığında çok sayıda vergi hareketi olması durumunda önerilir.</span><span class="sxs-lookup"><span data-stu-id="ccb04-124">This is recommended for a large number of tax transactions within a period interval.</span></span>  
    > [!NOTE]
    > <span data-ttu-id="ccb04-125">Şu anda bu İspanya, İtalya, Japonya ve Hollanda'da desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="ccb04-125">Currently this is not supported in Spain, Japan, and the Netherlands.</span></span>
11. <span data-ttu-id="ccb04-126">**Mahsup vergi hareketleri oluşturmayı engelle** onay kutusunu seçin veya temizleyin.</span><span class="sxs-lookup"><span data-stu-id="ccb04-126">Select or clear the **Prevent generating offset tax transactions** check box.</span></span> <span data-ttu-id="ccb04-127">Varsayılan olarak, sistem kapatma işlemi sırasında mahsup vergi hareketleri oluşturur; bu da bir dönem aralığında çok sayıda vergi hareketi varsa performans sorununa neden olur.</span><span class="sxs-lookup"><span data-stu-id="ccb04-127">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="ccb04-128">Mahsup vergi hareketleri oluşturmayı engellemek için bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ccb04-128">Select this check box to prevent generating offset tax transactions.</span></span>
12. <span data-ttu-id="ccb04-129">**Dönem aralıkları sekmesi**'ni genişletin.</span><span class="sxs-lookup"><span data-stu-id="ccb04-129">Expand the **Period intervals** tab.</span></span>
13. <span data-ttu-id="ccb04-130">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ccb04-130">Select **Add**.</span></span>
14. <span data-ttu-id="ccb04-131">**Başlangıç tarihi** alanında yeni sekmede bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ccb04-131">In the **From date** field in the new row, enter a date.</span></span>
15. <span data-ttu-id="ccb04-132">**Bitiş tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ccb04-132">In the **To date** field, enter a date.</span></span>
16. <span data-ttu-id="ccb04-133">**Yeni dönem aralığı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="ccb04-133">Select **New period interval**.</span></span> <span data-ttu-id="ccb04-134">İlk dönem aralığı girildikten sonra yeni dönemler otomatik olarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="ccb04-134">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="ccb04-135">Gerektiğinde geri dönüp yeni dönem aralıkları ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ccb04-135">You can come back and add new period intervals as required.</span></span>  
17. <span data-ttu-id="ccb04-136">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ccb04-136">Close the page.</span></span>


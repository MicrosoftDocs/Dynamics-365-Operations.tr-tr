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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e2e5340150623057e233ed0acf487c42c61deba2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222131"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="23204-103">Satış vergisi kapatma dönemlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="23204-103">Set up sales tax settlement periods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="23204-104">Bu konuda, satış vergisi kapatma dönemlerinin nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="23204-104">This topic explains how to set up sales tax settlement periods.</span></span> <span data-ttu-id="23204-105">Satış vergisi kapatma dönemleri, satış vergisinin bildirilip ödenmesi gereken dönem aralıkları hakkında bilgiler içerir.</span><span class="sxs-lookup"><span data-stu-id="23204-105">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="23204-106">Belirli bir tarih aralığında bir kapatma dönemi için bir kapatma işlemi yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="23204-106">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="23204-107">Kapatma dönemiyle ilişkili tüm vergi kodları kapatılır.</span><span class="sxs-lookup"><span data-stu-id="23204-107">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="23204-108">İlgili satış vergisi dairesinin ayarlarına bağlı olarak, vergi borcu ya bir satıcıya veya bir Genel muhasebe hesabına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="23204-108">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>

<span data-ttu-id="23204-109">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="23204-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="23204-110">Gezinti bölmesinde **Modüller > Vergi > Dolaylı vergiler > Satış vergisi > Satış vergisi kapatma dönemleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="23204-110">In the navigation pane, go to **Modules > Tax > Indirect taxes > Sales tax > Sales tax settlement periods**.</span></span>
2. <span data-ttu-id="23204-111">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="23204-111">Select **New**.</span></span>
3. <span data-ttu-id="23204-112">**Kapatma dönemi** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="23204-112">In the **Settlement period** field, type a value.</span></span>
4. <span data-ttu-id="23204-113">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="23204-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="23204-114">**Makam** alanında kapatma dönemi için oluşturulan bildirimleri ve ödemeleri alan satış vergisi makamını seçin.</span><span class="sxs-lookup"><span data-stu-id="23204-114">In the **Authority** field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="23204-115">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="23204-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="23204-116">**Ödeme koşulları** alanında, açılır menüden istediğiniz kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="23204-116">In the **Terms of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="23204-117">İlgili Satış vergi dairesi, bir satıcı olarak kurulabilir ve Satış vergisi kapatma işlemi bir açık satıcı faturası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="23204-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="23204-118">Ödeme koşulları, açık satıcı faturası için Vade tarihi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="23204-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
8. <span data-ttu-id="23204-119">Kapatma dönemi aralıkları için tür seçin.</span><span class="sxs-lookup"><span data-stu-id="23204-119">Select a type for the settlement period intervals.</span></span>
9. <span data-ttu-id="23204-120">Dönem başına dönem aralığı birim sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="23204-120">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="23204-121">Örneğin üç aylık dönemde 3 ay vardır.</span><span class="sxs-lookup"><span data-stu-id="23204-121">For example, a quarter has 3 months.</span></span>
10. <span data-ttu-id="23204-122">**Satış vergisi kapatma için toplu iş kullan** onay kutusunu işaretleyin veya kutuda işaret varsa kaldırın.</span><span class="sxs-lookup"><span data-stu-id="23204-122">Select or clear the **Use batch processing for sales tax settlement** check box.</span></span> <span data-ttu-id="23204-123">Kapatma dönemi için kapatma işlemi arka planda toplu iş olarak sürdürülebilir.</span><span class="sxs-lookup"><span data-stu-id="23204-123">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="23204-124">Bu bir dönem aralığında çok sayıda vergi hareketi olması durumunda önerilir.</span><span class="sxs-lookup"><span data-stu-id="23204-124">This is recommended for a large number of tax transactions within a period interval.</span></span>  
    > [!NOTE]
    > <span data-ttu-id="23204-125">Şu anda bu İspanya, İtalya, Japonya ve Hollanda'da desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="23204-125">Currently this is not supported in Spain, Japan, and the Netherlands.</span></span>
11. <span data-ttu-id="23204-126">**Mahsup vergi hareketleri oluşturmayı engelle** onay kutusunu seçin veya temizleyin.</span><span class="sxs-lookup"><span data-stu-id="23204-126">Select or clear the **Prevent generating offset tax transactions** check box.</span></span> <span data-ttu-id="23204-127">Varsayılan olarak, sistem kapatma işlemi sırasında mahsup vergi hareketleri oluşturur; bu da bir dönem aralığında çok sayıda vergi hareketi varsa performans sorununa neden olur.</span><span class="sxs-lookup"><span data-stu-id="23204-127">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="23204-128">Mahsup vergi hareketleri oluşturmayı engellemek için bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="23204-128">Select this check box to prevent generating offset tax transactions.</span></span>
12. <span data-ttu-id="23204-129">**Dönem aralıkları sekmesi**'ni genişletin.</span><span class="sxs-lookup"><span data-stu-id="23204-129">Expand the **Period intervals** tab.</span></span>
13. <span data-ttu-id="23204-130">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="23204-130">Select **Add**.</span></span>
14. <span data-ttu-id="23204-131">**Başlangıç tarihi** alanında yeni sekmede bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="23204-131">In the **From date** field in the new row, enter a date.</span></span>
15. <span data-ttu-id="23204-132">**Bitiş tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="23204-132">In the **To date** field, enter a date.</span></span>
16. <span data-ttu-id="23204-133">**Yeni dönem aralığı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="23204-133">Select **New period interval**.</span></span> <span data-ttu-id="23204-134">İlk dönem aralığı girildikten sonra yeni dönemler otomatik olarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="23204-134">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="23204-135">Gerektiğinde geri dönüp yeni dönem aralıkları ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="23204-135">You can come back and add new period intervals as required.</span></span>  
17. <span data-ttu-id="23204-136">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="23204-136">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
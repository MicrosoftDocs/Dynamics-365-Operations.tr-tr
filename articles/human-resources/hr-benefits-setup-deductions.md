---
title: Kesintileri yapılandırma
description: Varsa, her bir avantaj için bir çalışanın maaşından düşmelerini belirlemek için Microsoft Dynamics 365 Human Resources'ta kesintiler kullanın.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4a916ca2d0d47407ff0d8cc2cc7ca179ecb59bae
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803669"
---
# <a name="configure-deductions"></a><span data-ttu-id="63157-103">Kesintileri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="63157-103">Configure deductions</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="63157-104">Varsa, her bir avantaj için bir çalışanın maaşından düşmelerini belirlemek için Microsoft Dynamics 365 Human Resources'ta kesintiler kullanın.</span><span class="sxs-lookup"><span data-stu-id="63157-104">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="63157-105">Kesintilerin geçerlilik tarihi olduğundan, kesinti bilgilerinin geçmiş kaydını tutabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="63157-105">Deductions are date-effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="63157-106">**Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **Kesintiler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="63157-106">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="63157-107">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="63157-107">Select **New**.</span></span>

3. <span data-ttu-id="63157-108">Aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="63157-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="63157-109">Alan</span><span class="sxs-lookup"><span data-stu-id="63157-109">Field</span></span> | <span data-ttu-id="63157-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="63157-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="63157-111">**Kesinti**</span><span class="sxs-lookup"><span data-stu-id="63157-111">**Deduction**</span></span> | <span data-ttu-id="63157-112">Kazanç kesintiyi tanımlamak için kullanılan benzersiz kod.</span><span class="sxs-lookup"><span data-stu-id="63157-112">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="63157-113">**Tanım**</span><span class="sxs-lookup"><span data-stu-id="63157-113">**Description**</span></span> | <span data-ttu-id="63157-114">Kesintinin bir açıklaması.</span><span class="sxs-lookup"><span data-stu-id="63157-114">A description for the deduction.</span></span> |
   | <span data-ttu-id="63157-115">**Yürürlüğe giriş**</span><span class="sxs-lookup"><span data-stu-id="63157-115">**Effective**</span></span> | <span data-ttu-id="63157-116">Başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="63157-116">The start date.</span></span> <span data-ttu-id="63157-117">Geçerli değer varsayılan sistem tarihidir.</span><span class="sxs-lookup"><span data-stu-id="63157-117">The default value is the current system date.</span></span> |
   | <span data-ttu-id="63157-118">**Bitiş tarihi**</span><span class="sxs-lookup"><span data-stu-id="63157-118">**Expiration**</span></span> | <span data-ttu-id="63157-119">Bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="63157-119">The end date.</span></span> <span data-ttu-id="63157-120">Varsayılan değer 12/31/2154'dir ve hiçbir zaman bunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="63157-120">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="63157-121">**Başlık**</span><span class="sxs-lookup"><span data-stu-id="63157-121">**Heading**</span></span> | <span data-ttu-id="63157-122">Bu kesintinin, bordroya ait kazançların çalışan kısmı için kullanacağı Bordro sistemindeki başlık Kodu.</span><span class="sxs-lookup"><span data-stu-id="63157-122">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="63157-123">Bu, bir üçüncü taraf bordro sağlayıcı kullanırken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="63157-123">This is used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="63157-124">**Personel bordro kesintisi referansı**</span><span class="sxs-lookup"><span data-stu-id="63157-124">**Employee payroll deduction reference**</span></span> | <span data-ttu-id="63157-125">Kazançlar bordrolara işlenirken bu kesinti tutarında personel bölümü için kullanılan, bordro sistemindeki kesinti kodu.</span><span class="sxs-lookup"><span data-stu-id="63157-125">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="63157-126">**Tutar başlığı**</span><span class="sxs-lookup"><span data-stu-id="63157-126">**Amount heading**</span></span> | <span data-ttu-id="63157-127">Bu kesinti miktarının, bordroya ait kazançların çalışan kısmı için kullanacağı Bordro sistemindeki başlık Kodu.</span><span class="sxs-lookup"><span data-stu-id="63157-127">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="63157-128">Bu, bir üçüncü taraf bordro sağlayıcı kullanırken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="63157-128">This is normally used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="63157-129">**Silinebilir**</span><span class="sxs-lookup"><span data-stu-id="63157-129">**Can delete**</span></span> | <span data-ttu-id="63157-130">Dynamics 365 for Finance and Operations'tan aktarılan bir değerin Bordro sistemindeki değerin silinmesine neden olmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="63157-130">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="63157-131">**Eşleştirilmiş sütunlar**</span><span class="sxs-lookup"><span data-stu-id="63157-131">**Paired columns**</span></span> | <span data-ttu-id="63157-132">Bitişik sütunların eşleştirilmiş olduğu başlık ve kesinti tutarının bordro sistemine verip vermeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="63157-132">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="63157-133">**Yürürlük tarihini değiştir**</span><span class="sxs-lookup"><span data-stu-id="63157-133">**Change effective date**</span></span> | <span data-ttu-id="63157-134">Kazanç kesinti değişikliğinin yürürlüğe gireceği tarih.</span><span class="sxs-lookup"><span data-stu-id="63157-134">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="63157-135">Bu tarihte, sistem, kazanç indirimini otomatik olarak değiştirir ve **Kesinti değişikliği güncelleştirmesi** işlemini çalıştırdığınız sürece, bu kesinti ile ilişkili tüm kazanç planlarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="63157-135">On this date, the system automatically changes the benefit deduction and updates all benefit plans associated with this deduction, as long as you run **Deduction change update** processing.</span></span> |
   | <span data-ttu-id="63157-136">**Kesinti değişikliği tamamlandı**</span><span class="sxs-lookup"><span data-stu-id="63157-136">**Deduction change completed**</span></span> | <span data-ttu-id="63157-137">Kazanç kesintisi değişiklikleri kesinti ile yapılan güncelleştirme değişikliği işlemesi ile tamamlandıktan sonra **Kesinti değişikliği tamamlandı** onay kutusu otomatik olarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="63157-137">The **Deduction change completed** check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="63157-138">Hazırlık oranı kurulumunda yapılan değişiklikleri izlemek ve sürdürmek için **eylemler**'i seçin ve **sürümleri koru**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="63157-138">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="63157-139">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="63157-139">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
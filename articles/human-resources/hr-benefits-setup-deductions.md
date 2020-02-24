---
title: Çıkarımları konfigüre et
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7ee9e8f3bc0e9027e41d3aa91bd097a3f046cbb4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010884"
---
# <a name="configure-deductions"></a><span data-ttu-id="34ec7-102">Çıkarımları konfigüre et</span><span class="sxs-lookup"><span data-stu-id="34ec7-102">Configure deductions</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="34ec7-103">Varsa, her bir avantaj için bir çalışanın maaşından düşmelerini belirlemek için Microsoft Dynamics 365 Human Resources'ta kesintiler kullanın.</span><span class="sxs-lookup"><span data-stu-id="34ec7-103">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="34ec7-104">Kesintiler yürürlülük tarihi olduğundan, kesinti bilgilerinin geçmiş kaydını tutabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34ec7-104">Deductions are date effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="34ec7-105">**Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **Kesintiler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="34ec7-105">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="34ec7-106">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="34ec7-106">Select **New**.</span></span>

3. <span data-ttu-id="34ec7-107">Aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="34ec7-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="34ec7-108">Alan</span><span class="sxs-lookup"><span data-stu-id="34ec7-108">Field</span></span> | <span data-ttu-id="34ec7-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="34ec7-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="34ec7-110">Kesinti</span><span class="sxs-lookup"><span data-stu-id="34ec7-110">Deduction</span></span> | <span data-ttu-id="34ec7-111">Kazanç kesintiyi tanımlamak için kullanılan benzersiz kod.</span><span class="sxs-lookup"><span data-stu-id="34ec7-111">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="34ec7-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="34ec7-112">Description</span></span> | <span data-ttu-id="34ec7-113">Kesintinin bir açıklaması.</span><span class="sxs-lookup"><span data-stu-id="34ec7-113">A description for the deduction.</span></span> |
   | <span data-ttu-id="34ec7-114">Yürürlüğe giriş</span><span class="sxs-lookup"><span data-stu-id="34ec7-114">Effective</span></span> | <span data-ttu-id="34ec7-115">Başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="34ec7-115">The start date.</span></span> <span data-ttu-id="34ec7-116">Geçerli değer varsayılan sistem tarihidir.</span><span class="sxs-lookup"><span data-stu-id="34ec7-116">The default value is the current system date.</span></span> |
   | <span data-ttu-id="34ec7-117">Bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="34ec7-117">Expiration</span></span> | <span data-ttu-id="34ec7-118">Bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="34ec7-118">The end date.</span></span> <span data-ttu-id="34ec7-119">Varsayılan değer 12/31/2154'dir ve hiçbir zaman bunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="34ec7-119">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="34ec7-120">Başlık</span><span class="sxs-lookup"><span data-stu-id="34ec7-120">Heading</span></span> | <span data-ttu-id="34ec7-121">Bu kesintinin, bordroya ait kazançların çalışan kısmı için kullanacağı Bordro sistemindeki başlık Kodu.</span><span class="sxs-lookup"><span data-stu-id="34ec7-121">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="34ec7-122">Bu, bir üçüncü taraf Bordro sağlayıcı kullanırken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="34ec7-122">This is used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="34ec7-123">Personel bordro kesintisi referansı</span><span class="sxs-lookup"><span data-stu-id="34ec7-123">Employee payroll deduction reference</span></span> | <span data-ttu-id="34ec7-124">Kazançlar bordrolara işlenirken bu kesinti tutarında personel bölümü için kullanılan, bordro sistemindeki kesinti kodu.</span><span class="sxs-lookup"><span data-stu-id="34ec7-124">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="34ec7-125">Tutar başlığı</span><span class="sxs-lookup"><span data-stu-id="34ec7-125">Amount heading</span></span> | <span data-ttu-id="34ec7-126">Bu kesinti miktarının, bordroya ait kazançların çalışan kısmı için kullanacağı Bordro sistemindeki başlık Kodu.</span><span class="sxs-lookup"><span data-stu-id="34ec7-126">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="34ec7-127">Bu, bir üçüncü taraf Bordro sağlayıcı kullanırken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="34ec7-127">This is normally used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="34ec7-128">Silinebilir</span><span class="sxs-lookup"><span data-stu-id="34ec7-128">Can delete</span></span> | <span data-ttu-id="34ec7-129">Dynamics 365 for Finance and Operations'tan aktarılan bir değerin Bordro sistemindeki değerin silinmesine neden olmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34ec7-129">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="34ec7-130">Eşleştirilmiş sütunlar</span><span class="sxs-lookup"><span data-stu-id="34ec7-130">Paired columns</span></span> | <span data-ttu-id="34ec7-131">Bitişik sütunların eşleştirilmiş olduğu başlık ve kesinti tutarının bordro sistemine verip vermeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34ec7-131">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="34ec7-132">Yürürlük tarihini değiştir</span><span class="sxs-lookup"><span data-stu-id="34ec7-132">Change effective date</span></span> | <span data-ttu-id="34ec7-133">Kazanç kesinti değişikliğinin yürürlüğe gireceği tarih.</span><span class="sxs-lookup"><span data-stu-id="34ec7-133">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="34ec7-134">Bu tarihte, sistem, kazanç indirimini otomatik olarak değiştirir ve güncelleştirme işlemini çalıştırdığınız sürece, bu kesinti ile ilişkili tüm kazanç planlarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="34ec7-134">On this date the system will automatically change the benefit deduction and update all benefit plans associated with this deduction, as long as you run Deduction change update processing.</span></span> |
   | <span data-ttu-id="34ec7-135">Kesinti değişikliği tamamlandı</span><span class="sxs-lookup"><span data-stu-id="34ec7-135">Deduction change completed</span></span> | <span data-ttu-id="34ec7-136">Kazanç kesintisi değişiklikleri kesinti ile yapılan güncelleştirme değişikliği işlemesi ile tamamlandıktan sonra kesinti değişikliği tamamlandı onay kutusu otomatik olarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="34ec7-136">The Deduction change completed check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="34ec7-137">Hazırlık oranı kurulumunda yapılan değişiklikleri izlemek ve sürdürmek için **eylemler**'i seçin ve **sürümleri koru**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="34ec7-137">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="34ec7-138">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="34ec7-138">Select **Save**.</span></span> 

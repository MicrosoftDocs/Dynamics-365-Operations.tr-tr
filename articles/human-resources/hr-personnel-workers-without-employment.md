---
title: İstihdamı bulunmayan çalışanlar
description: Kuruluşunuzla gelecekte, etkin veya geçmişe ait iş kaydı olmayan çalışanlar, İş kaydı olmayan çalışanlar formunda görünür.
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1a137de25924f4c4ec6f6b1fe70f9d21af591c0
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924583"
---
# <a name="workers-without-employment"></a><span data-ttu-id="18c8f-103">İstihdamı bulunmayan çalışanlar</span><span class="sxs-lookup"><span data-stu-id="18c8f-103">Workers without employment</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="18c8f-104">Kuruluşunuzla gelecekte, etkin veya geçmişe ait iş kaydı olmayan çalışanlar, **İş kaydı olmayan çalışanlar** formunda görünür.</span><span class="sxs-lookup"><span data-stu-id="18c8f-104">Workers with no future, active, or historical employment with your organization appear in the **Workers without employment** form.</span></span> <span data-ttu-id="18c8f-105">Bu duruma sahip çalışanlar, iş kaydı olmayan çalışanları içe aktardığınızda veya **Çalışanlar > İş geçmişi** ile bir çalışanın gününü sildiğinizde görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="18c8f-105">Workers with this status can appear when you import workers without an employment record, or when you delete a worker's employment via **Workers > Employment history**.</span></span>

<span data-ttu-id="18c8f-106">Varsayılan olarak, **İş kaydı olmayan çalışanlar** formu aşağıdaki roller tarafından kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="18c8f-106">By default, the **Workers without employment** form is available to the following roles:</span></span>

- <span data-ttu-id="18c8f-107">İnsan Kaynakları Yardımcısı</span><span class="sxs-lookup"><span data-stu-id="18c8f-107">Human Resources Assistant</span></span>
- <span data-ttu-id="18c8f-108">İnsan Kaynakları Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="18c8f-108">Human Resources Manager</span></span>
- <span data-ttu-id="18c8f-109">İşe alan</span><span class="sxs-lookup"><span data-stu-id="18c8f-109">Recruiter</span></span>
- <span data-ttu-id="18c8f-110">Maaş ve Kazançlar Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="18c8f-110">Comp and Benefits Manager</span></span>
- <span data-ttu-id="18c8f-111">Bordro Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="18c8f-111">Payroll Administrator</span></span>
- <span data-ttu-id="18c8f-112">Bordro Müdürü</span><span class="sxs-lookup"><span data-stu-id="18c8f-112">Payroll Manager</span></span>
- <span data-ttu-id="18c8f-113">Eğitim Müdürü</span><span class="sxs-lookup"><span data-stu-id="18c8f-113">Training Manager</span></span>

<span data-ttu-id="18c8f-114">**İş kaydı olmayan çalışanlar** listesinde, listelenen kişileri silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18c8f-114">In the **Workers without employment** list, you can delete the individuals listed.</span></span> <span data-ttu-id="18c8f-115">Varsayılan olarak, bu ayrıcalık İnsan Kaynakları Yardımcısı rolüne verilir.</span><span class="sxs-lookup"><span data-stu-id="18c8f-115">By default, this privilege is given to the Human Resources Assistant role.</span></span> <span data-ttu-id="18c8f-116">Bu ayrıcalığı aşağıdaki adımlarla diğer rollere verebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="18c8f-116">You can give this privilege to other roles with the following steps:</span></span>

1. <span data-ttu-id="18c8f-117">**Sistem yönetimi**'ni ve sonra **Güvenlik yapılandırması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="18c8f-117">Select **System administration**, and then select **Security configuration**.</span></span>

2. <span data-ttu-id="18c8f-118">**Ayrıcalıklar** sekmesinde , **çalışanları korumak** için **ayrıcalıklar** listesine filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="18c8f-118">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>

   <span data-ttu-id="18c8f-119">[![Ayrıcalık listesini filtreleme](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span><span class="sxs-lookup"><span data-stu-id="18c8f-119">[![Filter Privileges list](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span></span>

3. <span data-ttu-id="18c8f-120">**Başvurular** sütununda, **menü öğelerini görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="18c8f-120">In the **References** column, select **Display menu items**.</span></span>

4. <span data-ttu-id="18c8f-121">**Menü öğelerini görüntüle**'de **HcmWorkersWithoutEmployment**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="18c8f-121">In **Display menu items**, select **HcmWorkersWithoutEmployment**.</span></span>

   <span data-ttu-id="18c8f-122">[![Form seç](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span><span class="sxs-lookup"><span data-stu-id="18c8f-122">[![Select form](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span></span>

5. <span data-ttu-id="18c8f-123">**İzin vermek** için **Silme** iznini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="18c8f-123">Set the **Delete** permission to **Grant**.</span></span>

6. <span data-ttu-id="18c8f-124">**Yayımlanmamış nesneler** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="18c8f-124">Select the **Unpublished objects** tab.</span></span>

7. <span data-ttu-id="18c8f-125">**Tümünü yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="18c8f-125">Select **Publish all**.</span></span>

   <span data-ttu-id="18c8f-126">[![Değişiklikleri yayımla](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span><span class="sxs-lookup"><span data-stu-id="18c8f-126">[![Publish changes](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
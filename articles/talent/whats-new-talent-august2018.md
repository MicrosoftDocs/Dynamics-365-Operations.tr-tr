---
title: Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (Ağustos 2018)
description: Bu konuda, Microsoft Dynamics 365 for Talent Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 08/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-08-27
ms.dyn365.ops.version: Talent August 2018 update
ms.openlocfilehash: cdf0893835c1ee9edd89c43b3c5c842d89e6d526
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "306627"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-august-2018"></a><span data-ttu-id="1eb53-103">Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (Ağustos 2018)</span><span class="sxs-lookup"><span data-stu-id="1eb53-103">What's new or changed in Dynamics 365 for Talent Core HR (August 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1eb53-104">**Derleme 8.1.104**</span><span class="sxs-lookup"><span data-stu-id="1eb53-104">**Build 8.1.104**</span></span>

<span data-ttu-id="1eb53-105">Bu konuda, Dynamics 365 for Talent Core HR'deki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="1eb53-105">This topic describes features that are either new or changed in Dynamics 365 for Talent Core HR.</span></span>

## <a name="view-expiring-records-in-manager-self-service"></a><span data-ttu-id="1eb53-106">Yönetici self servis içindeki süresi dolmak üzere olan kayıtları görüntüleme</span><span class="sxs-lookup"><span data-stu-id="1eb53-106">View expiring records in Manager self service</span></span>

<span data-ttu-id="1eb53-107">Artık, Yönetici self servis içindeki süresi dolmak üzere olan kayıtları görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1eb53-107">You can now view expiring records in Manager self-service.</span></span> <span data-ttu-id="1eb53-108">Yeni seçenekler, yöneticilerin görüntüleyebileceği bilgileri yapılandırmanıza izin verir.</span><span class="sxs-lookup"><span data-stu-id="1eb53-108">New options are allow you to configure what information will be available for managers to view.</span></span> <span data-ttu-id="1eb53-109">Bunların arasında aşağıdakiler bulunur:</span><span class="sxs-lookup"><span data-stu-id="1eb53-109">These include:</span></span>

-   <span data-ttu-id="1eb53-110">Sertifikalar</span><span class="sxs-lookup"><span data-stu-id="1eb53-110">Certificates</span></span>

-   <span data-ttu-id="1eb53-111">Kimlik numaraları</span><span class="sxs-lookup"><span data-stu-id="1eb53-111">Identification numbers</span></span>

-   <span data-ttu-id="1eb53-112">Deneme süreleri</span><span class="sxs-lookup"><span data-stu-id="1eb53-112">Probation periods</span></span>

-   <span data-ttu-id="1eb53-113">Filtrelemeler</span><span class="sxs-lookup"><span data-stu-id="1eb53-113">Screenings</span></span>

-   <span data-ttu-id="1eb53-114">Sınamalar</span><span class="sxs-lookup"><span data-stu-id="1eb53-114">Tests</span></span>

<span data-ttu-id="1eb53-115">Ayrıca bu özellik, süresi dolmak üzere olan kayıtların aranacağı gün aralığını belirtmenize de olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="1eb53-115">This feature also gives you the ability to specify the range of days in which to look for expiring records.</span></span>

## <a name="configurable-transfer-actions"></a><span data-ttu-id="1eb53-116">Yapılandırılabilir transfer eylemleri</span><span class="sxs-lookup"><span data-stu-id="1eb53-116">Configurable transfer actions</span></span>

<span data-ttu-id="1eb53-117">Transfer isteğinin girişi sırasında kullanılabilecek seçenekleri role göre yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1eb53-117">You can configure by role the options that will be available during the entry of a transfer request.</span></span> <span data-ttu-id="1eb53-118">Bu özellik, kuruluştaki roller arasında daha fazla esneklik sağlar.</span><span class="sxs-lookup"><span data-stu-id="1eb53-118">This feature provides additional flexibility across the roles in an organization.</span></span>

<span data-ttu-id="1eb53-119">Örneğin, çalışan transferi isteğinde bulunan yöneticiler ücret tutarı önermek veya girmek ya da transfer isteğiyle ilişkilendirilecek görev listelerini seçmek için erişime sahip olmayabilirler.</span><span class="sxs-lookup"><span data-stu-id="1eb53-119">For example, managers requesting employee transfers may not have access to suggest or enter compensation amounts or select the task lists that will be associated with the transfer request.</span></span> <span data-ttu-id="1eb53-120">Bu durumda, yöneticiler transfer istekleri oluşturup gönderebilirler ancak yöneticilerin ücret veya görev listesi atamaları girmelerine izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="1eb53-120">In this case, managers can create and submit transfer requests but are not allowed to enter compensation or task list assignments.</span></span> <span data-ttu-id="1eb53-121">Yine bu yapılandırmada İK yeni ücret değerlerini, transferin tamamlanması sonucu tamamlanacak tüm ek onay listeleri atayabilir.</span><span class="sxs-lookup"><span data-stu-id="1eb53-121">In this same configuration, HR will be able to assign the new compensation values as well as assign any additional checklists to be completed as a result of the transfer completing.</span></span>

<span data-ttu-id="1eb53-122">Varsayılan olarak yeni yapılandırma seçenekleri bu güncelleştirmeden önceki yetenekleri değiştirmemeye ayarlıdır.</span><span class="sxs-lookup"><span data-stu-id="1eb53-122">By default, the new configuration options are set to not change the capabilities prior to this update.</span></span>

## <a name="leave-and-absence"></a><span data-ttu-id="1eb53-123">İzin ve devamsızlık</span><span class="sxs-lookup"><span data-stu-id="1eb53-123">Leave and absence</span></span>

<span data-ttu-id="1eb53-124">Artık İzin ve Devamsızlık bölümünde ek Tarih alanları bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="1eb53-124">There are now additional Date fields available in Leave and Absence.</span></span>

<span data-ttu-id="1eb53-125">Bu özellikle plan düzeyindeki tahakkuk dönemi temelini belirli çalışan tarihlerini kullanacak şekilde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1eb53-125">With this feature you can set the accrual period basis at the plan level to use specific employee dates.</span></span> <span data-ttu-id="1eb53-126">Bu da izin tahakkuk işlemi sırasında plan başlangıç tarihinden farklı tarihlerin kullanılabilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="1eb53-126">This allows for dates other than the plan start date to be used during the leave accrual process.</span></span> <span data-ttu-id="1eb53-127">Çalışana özel tarih seçenekleri aşağıdaki değerleri içerir:</span><span class="sxs-lookup"><span data-stu-id="1eb53-127">Options for employee specific dates include the following values:</span></span>

-   <span data-ttu-id="1eb53-128">Özel (bu güncelleştirmeden önce kullanılabilir)</span><span class="sxs-lookup"><span data-stu-id="1eb53-128">Custom (available prior to this update)</span></span>

-   <span data-ttu-id="1eb53-129">Yıl dönümü tarihi</span><span class="sxs-lookup"><span data-stu-id="1eb53-129">Anniversary date</span></span>

-   <span data-ttu-id="1eb53-130">Orijinal işe alma tarihi</span><span class="sxs-lookup"><span data-stu-id="1eb53-130">Original hire date</span></span>

-   <span data-ttu-id="1eb53-131">Kıdem tarihi</span><span class="sxs-lookup"><span data-stu-id="1eb53-131">Seniority date</span></span>

-   <span data-ttu-id="1eb53-132">Çalışanın ayarlanan başlama tarihi</span><span class="sxs-lookup"><span data-stu-id="1eb53-132">Worker’s adjusted start date</span></span>

-   <span data-ttu-id="1eb53-133">Çalışanın başlama tarihi</span><span class="sxs-lookup"><span data-stu-id="1eb53-133">Worker’s start date</span></span>

<span data-ttu-id="1eb53-134">Personele özel tarihlerden birini kullanmak üzere yapılandırıldığında kayıt işlemi, tahakkuk dönemlerini hesaplamak için belirtilen tarihi kullanır.</span><span class="sxs-lookup"><span data-stu-id="1eb53-134">When configured to use one of the employee specific dates, the enrollment process will use the specified date to calculate the accrual periods.</span></span> <span data-ttu-id="1eb53-135">Tahakkuk dönemi temeli de tahakkuk işlemi sırasında kullanılanları anlamanıza yardımcı olmak için çalışanın plan kaydında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="1eb53-135">The accrual period basis is also displayed on the employee’s plan enrollment to help you understand what’s being used during the accrual process.</span></span>

## <a name="microsoft-word-integration"></a><span data-ttu-id="1eb53-136">Microsoft Word tümleştirmesi</span><span class="sxs-lookup"><span data-stu-id="1eb53-136">Microsoft Word integration</span></span>

<span data-ttu-id="1eb53-137">Belge şablonları Core HR genelinde etkindir.</span><span class="sxs-lookup"><span data-stu-id="1eb53-137">Document templates have been enabled throughout Core HR.</span></span> <span data-ttu-id="1eb53-138">Bu özellik, oluşturduğunuz Word şablonlarını temel alan mektuplar ve raporlar oluşturmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="1eb53-138">This feature allows you to create letters and reports based on Word templates that you create.</span></span>

<span data-ttu-id="1eb53-139">Bu özellik hakkında daha fazla bilgiye [Office tümleştirmesi eğitimi](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-tutorial?toc=/dynamics365/unified-operations/talent/toc.json) bölümünden ulaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1eb53-139">Additional information about this feature is available in the [Office integration tutorial](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-tutorial?toc=/dynamics365/unified-operations/talent/toc.json).</span></span>


## <a name="other-fixes"></a><span data-ttu-id="1eb53-140">Diğer düzeltmeler</span><span class="sxs-lookup"><span data-stu-id="1eb53-140">Other fixes</span></span>

<span data-ttu-id="1eb53-141">Bu sürüm bir dizi hata düzeltmesi, yeni varlıklar, mevcut varlıklarda düzeltmeler ve yerelleştirilmiş etiket değişiklikleri içerir.</span><span class="sxs-lookup"><span data-stu-id="1eb53-141">This release also includes a number of bug fixes, the addition of new entities, fixes to existing entities, and localized label changes.</span></span>

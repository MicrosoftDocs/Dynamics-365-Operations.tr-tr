---
title: Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (1 Ekim 2018)
description: Bu konuda, Microsoft Dynamics 365 for Talent Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 10/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 92f06d29dfa8110106a2a0e71434b2c0c75110b5
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "859287"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-8-2018"></a><span data-ttu-id="e8064-103">Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (8 Ekim 2018)</span><span class="sxs-lookup"><span data-stu-id="e8064-103">What's new or changed in Dynamics 365 for Talent Core HR (October 8, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e8064-104">**Derleme 8.1.1050.0**</span><span class="sxs-lookup"><span data-stu-id="e8064-104">**Build 8.1.1050.0**</span></span>

<span data-ttu-id="e8064-105">Bu konuda, Core HR'deki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e8064-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-other-dates-to-be-used-on-leave-tier-basis-leave-management"></a><span data-ttu-id="e8064-106">İzin katmanı temelinde (İzin Yönetimi) kullanılacak diğer tarihlere izin verin</span><span class="sxs-lookup"><span data-stu-id="e8064-106">Allow other dates to be used on leave tier basis (Leave Management)</span></span>

<span data-ttu-id="e8064-107">Personeli izinle ödüllendirirken izin katmanı, personelin ne kadar izin süresi elde ettiğini belirler.</span><span class="sxs-lookup"><span data-stu-id="e8064-107">When awarding leave to employees, the award tier basis determines how much time off an employee accrues.</span></span> <span data-ttu-id="e8064-108">Şu anda bu katmanlar personelin başlangıç tarihi ve kıdem tarihini temel alır.</span><span class="sxs-lookup"><span data-stu-id="e8064-108">Currently, these tiers are based on employee start date and seniority date.</span></span> <span data-ttu-id="e8064-109">Bazı senaryolarda, organizasyonlar için bu katmanların yıldönümü veya orijinal işe alma tarihi gibi diğer tarihleri temel almasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="e8064-109">In some scenarios, organizations need these tiers to be based on other dates, like anniversary date or original hire date.</span></span> <span data-ttu-id="e8064-110">Bu tarihler zaten izinlerin ne zaman biriktiğini, bir personel bir plana kaydolduğunda aynı tarihlerin kullanılabilmesini, birikme miktarının belirlenmesini tanımlamak için zaten izin planında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e8064-110">These dates are already used on the leave plan to determine when accruals happen, the ability for these same dates to be used when an employee is enrolled in a plan have been added to determine the accrual amount.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="e8064-111">Diğer değişimler</span><span class="sxs-lookup"><span data-stu-id="e8064-111">Other changes</span></span>
<span data-ttu-id="e8064-112">Bu sürümde çeşitli düzeltmeler bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e8064-112">Miscellanous fixes have been included in this release.</span></span>

## <a name="known-issue"></a><span data-ttu-id="e8064-113">Bilinen sorun</span><span class="sxs-lookup"><span data-stu-id="e8064-113">Known issue</span></span>

<span data-ttu-id="e8064-114">**Sorun:** Bir çalışana yeni bir eklenti eklerken, **Yeni** ve **Düzenle** düğmeleri gri haldedir. **Geçici çözüm:** Eklenti sayfasını açmadan önce, **Çalışan** sayfasındaki bilgi kutularının kapalı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="e8064-114">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="e8064-115">**Çalışan** sayfası yüklendiğinde bilgi kutuları kapalıysa, eklentiler düğmeleri etkinleştirilmiş olacaktır.</span><span class="sxs-lookup"><span data-stu-id="e8064-115">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="e8064-116">(Bu sorun sonraki platform güncelleştirmesinde giderilecektir.)</span><span class="sxs-lookup"><span data-stu-id="e8064-116">(This issue will be fixed in the next platform update.)</span></span>

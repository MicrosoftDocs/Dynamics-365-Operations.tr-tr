---
title: Dynamics 365 Talent - Core HR'daki yenilikler veya değişiklikler (8 Ekim 2018)
description: Bu konuda, Microsoft Dynamics 365 Talent - Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
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
ms.openlocfilehash: 30c148a1bf27a221c1d4feacbe89cabfc412872c
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897362"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-8-2018"></a><span data-ttu-id="11d13-103">Dynamics 365 Talent - Core HR'daki yenilikler veya değişiklikler (8 Ekim 2018)</span><span class="sxs-lookup"><span data-stu-id="11d13-103">What's new or changed in Dynamics 365 Talent - Core HR (October 8, 2018)</span></span>

<span data-ttu-id="11d13-104">**Derleme 8.1.1050.0**</span><span class="sxs-lookup"><span data-stu-id="11d13-104">**Build 8.1.1050.0**</span></span>

<span data-ttu-id="11d13-105">Bu konuda, Core HR'deki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="11d13-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-other-dates-to-be-used-on-leave-tier-basis-leave-management"></a><span data-ttu-id="11d13-106">İzin katmanı temelinde (İzin Yönetimi) kullanılacak diğer tarihlere izin verin</span><span class="sxs-lookup"><span data-stu-id="11d13-106">Allow other dates to be used on leave tier basis (Leave Management)</span></span>

<span data-ttu-id="11d13-107">Personeli izinle ödüllendirirken izin katmanı, personelin ne kadar izin süresi elde ettiğini belirler.</span><span class="sxs-lookup"><span data-stu-id="11d13-107">When awarding leave to employees, the award tier basis determines how much time off an employee accrues.</span></span> <span data-ttu-id="11d13-108">Şu anda bu katmanlar personelin başlangıç tarihi ve kıdem tarihini temel alır.</span><span class="sxs-lookup"><span data-stu-id="11d13-108">Currently, these tiers are based on employee start date and seniority date.</span></span> <span data-ttu-id="11d13-109">Bazı senaryolarda, organizasyonlar için bu katmanların yıldönümü veya orijinal işe alma tarihi gibi diğer tarihleri temel almasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="11d13-109">In some scenarios, organizations need these tiers to be based on other dates, like anniversary date or original hire date.</span></span> <span data-ttu-id="11d13-110">Bu tarihler zaten izinlerin ne zaman biriktiğini, bir personel bir plana kaydolduğunda aynı tarihlerin kullanılabilmesini, birikme miktarının belirlenmesini tanımlamak için zaten izin planında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="11d13-110">These dates are already used on the leave plan to determine when accruals happen, the ability for these same dates to be used when an employee is enrolled in a plan have been added to determine the accrual amount.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="11d13-111">Diğer değişimler</span><span class="sxs-lookup"><span data-stu-id="11d13-111">Other changes</span></span>
<span data-ttu-id="11d13-112">Bu sürümde çeşitli düzeltmeler bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="11d13-112">Miscellanous fixes have been included in this release.</span></span>

## <a name="known-issue"></a><span data-ttu-id="11d13-113">Bilinen sorun</span><span class="sxs-lookup"><span data-stu-id="11d13-113">Known issue</span></span>

<span data-ttu-id="11d13-114">**Sorun:** Bir çalışana yeni bir eklenti eklerken, **Yeni** ve **Düzenle** düğmeleri gri haldedir. **Geçici çözüm:** Eklenti sayfasını açmadan önce, **Çalışan** sayfasındaki bilgi kutularının kapalı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="11d13-114">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="11d13-115">**Çalışan** sayfası yüklendiğinde bilgi kutuları kapalıysa, eklentiler düğmeleri etkinleştirilmiş olacaktır.</span><span class="sxs-lookup"><span data-stu-id="11d13-115">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="11d13-116">(Bu sorun sonraki platform güncelleştirmesinde giderilecektir.)</span><span class="sxs-lookup"><span data-stu-id="11d13-116">(This issue will be fixed in the next platform update.)</span></span>

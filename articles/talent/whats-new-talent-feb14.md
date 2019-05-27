---
title: Dynamics 365 for Talent'daki yenilikler veya değişiklikler (14 Şubat 2019)
description: Bu konuda, Microsoft Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
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
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1db7d032eade3f996e0554e64d6ea0704a347ed8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1519282"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-14-2019"></a><span data-ttu-id="fef0b-103">Dynamics 365 for Talent'daki yenilikler veya değişiklikler (14 Şubat 2019)</span><span class="sxs-lookup"><span data-stu-id="fef0b-103">What's new or changed in Dynamics 365 for Talent (February 14, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fef0b-104">Bu konuda, Talent'daki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="fef0b-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="fef0b-105">Attract'te değişiklikler</span><span class="sxs-lookup"><span data-stu-id="fef0b-105">Changes in Attract</span></span>
<span data-ttu-id="fef0b-106">Bu sürümde küçük hata gidermeleri vardır.</span><span class="sxs-lookup"><span data-stu-id="fef0b-106">There are minor bug fixes included with this release.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="fef0b-107">İş almadaki değişiklikler</span><span class="sxs-lookup"><span data-stu-id="fef0b-107">Changes in Onboarding</span></span>
<span data-ttu-id="fef0b-108">Bu sürümde küçük hata gidermeleri vardır.</span><span class="sxs-lookup"><span data-stu-id="fef0b-108">There are minor bug fixes included with this release.</span></span>
 
## <a name="changes-in-core-hr"></a><span data-ttu-id="fef0b-109">Core HR içindeki değişiklikler</span><span class="sxs-lookup"><span data-stu-id="fef0b-109">Changes in Core HR</span></span> 
<span data-ttu-id="fef0b-110">**Derleme 8.1.2146**</span><span class="sxs-lookup"><span data-stu-id="fef0b-110">**Build 8.1.2146**</span></span>

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a><span data-ttu-id="fef0b-111">Personel sabit ücret varlığı tüm kayıtları dışa aktarmaz</span><span class="sxs-lookup"><span data-stu-id="fef0b-111">Employee fixed compensation entity doesn't export all records</span></span>
<span data-ttu-id="fef0b-112">Bu değişiklik ile **Personel sabit ücret** varlığı şimdi tüm kayıtlara dışa aktarır.</span><span class="sxs-lookup"><span data-stu-id="fef0b-112">With this change, the **Employee fixed compensation** entity will now export all records.</span></span> <span data-ttu-id="fef0b-113">Bu varlık, personeller için mevcut sabit ücret kayıtlarını oluşturmak ve güncelleştirmekte kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="fef0b-113">The entity can be used to create and update existing fixed compensation records for employees.</span></span> 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a><span data-ttu-id="fef0b-114">Çalışma sonlandırma tarihi, personelin tercih ettiği saat dilimi ayarlarını dikkate almaz.</span><span class="sxs-lookup"><span data-stu-id="fef0b-114">Employment end date doesn't honor employee preferred time zone settings</span></span>
<span data-ttu-id="fef0b-115">Çalışma sonlandırma tarihleri, artık kullanıcı tarafından tercih edilen saat dilimlerini, bir şirket ile çalışma oluştururken veya sonlandırırken artık dikkate almaktadır.</span><span class="sxs-lookup"><span data-stu-id="fef0b-115">Employment end dates are now honoring the user-preferred time zone when creating or ending employment with a company.</span></span>
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a><span data-ttu-id="fef0b-116">Analizlerdeki İngiltere adresleri, Doğu İsviçre adresleri olarak görüntülenmektedir</span><span class="sxs-lookup"><span data-stu-id="fef0b-116">UK addresses display in Analytics as Eastern Switzerland addresses</span></span>
<span data-ttu-id="fef0b-117">Bu sürümde, bir değişiklik **Personel Yönetimi** "Konuma göre kişi sayısı" raporundaki hatalı hizalamaları düzeltmek üzere yapılmıştır.</span><span class="sxs-lookup"><span data-stu-id="fef0b-117">In this release, a change has been made to correct misalignment in addresses in the **Personnel Management** "Headcount by location" report.</span></span>
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a><span data-ttu-id="fef0b-118">Sonlandırma kodu çalışanın pozisyon atama kaydında, pozisyonu sonlandırırken doldurulmamıştır.</span><span class="sxs-lookup"><span data-stu-id="fef0b-118">Termination code is not populated on the worker position assignment record when ending the position</span></span>
<span data-ttu-id="fef0b-119">Bir personelin konum atamasını sonlandırırken, bir değişiklik varsayılan "Sonlandırma sebebi" koduna yapılmıştır.</span><span class="sxs-lookup"><span data-stu-id="fef0b-119">A change has been made to default the "Termination reason" code when ending the employees position assignment.</span></span>

### <a name="new-entity-created-for-job-compensation-levels"></a><span data-ttu-id="fef0b-120">İş ücret düzeyleri için yeni varlık oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="fef0b-120">New entity created for job compensation levels</span></span>
<span data-ttu-id="fef0b-121">Yeni bir veri yönetimi çerçevesi (DMF) varlığı oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="fef0b-121">A new data management framework (DMF) entity was created.</span></span> <span data-ttu-id="fef0b-122">Varlık, sistemde tanımlanmış her iş için ücret seviyeleri, piyasa değerleri ve anket bilgisi için oluşturma ve güncelleştirme sağlar.</span><span class="sxs-lookup"><span data-stu-id="fef0b-122">The entity provides for creation and updates to compensation levels, market values, and survey information for each job defined in the system.</span></span>

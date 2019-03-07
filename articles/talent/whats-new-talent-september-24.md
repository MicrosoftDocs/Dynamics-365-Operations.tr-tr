---
title: Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (24 Eylül 2018)
description: Bu konuda, Microsoft Dynamics 365 for Talent Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 09/21/2018
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
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: aeb75fe4c775b9003c6429de536498f495224098
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "306591"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-24-2018"></a><span data-ttu-id="3a546-103">Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (24 Eylül 2018)</span><span class="sxs-lookup"><span data-stu-id="3a546-103">What's new or changed in Dynamics 365 for Talent Core HR (September 24, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3a546-104">**Derleme 8.1.1015.0**</span><span class="sxs-lookup"><span data-stu-id="3a546-104">**Build 8.1.1015.0**</span></span>

<span data-ttu-id="3a546-105">Bu konuda, Core HR'deki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="3a546-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="currency-added-to-benefits"></a><span data-ttu-id="3a546-106">Kazançlara para birimi eklendi</span><span class="sxs-lookup"><span data-stu-id="3a546-106">Currency added to Benefits</span></span>

<span data-ttu-id="3a546-107">Kazanç planları, kazancın para birimini içerecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="3a546-107">Benefit plans have been updated to include the currency of the benefit.</span></span> <span data-ttu-id="3a546-108">Bu yeni alan da çalışanın dahil olduğu kazançlarda mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="3a546-108">This new field is also available on worker enrolled benefits.</span></span> <span data-ttu-id="3a546-109">Bu yeni alan Bakım kazançlarının ve Kazanç güvenliği ayrıcalığı listesini görüntülenin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="3a546-109">This new field is part of the Maintain benefits and View a list of benefits security privilege.</span></span>

## <a name="update-proration-process--leave-and-absence"></a><span data-ttu-id="3a546-110">Güncelleştirme bölümlendirme işlemi - İzin ve devamsızlık</span><span class="sxs-lookup"><span data-stu-id="3a546-110">Update proration process – Leave and Absence</span></span>

<span data-ttu-id="3a546-111">Kuruluşlar, çalışanların şirkete ne zaman katıldığı ve çıktığına dayalı olarak farklı izinler verirler.</span><span class="sxs-lookup"><span data-stu-id="3a546-111">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="3a546-112">Kuruluştan ayrılan çalışanlar için bazılarının ödülü kapatma tarihinde sonlandırmaları gerekirken, diğerleri, tahakkuk işlemini durdurmak için çalışılan son güne ihtiyaç duymaktadır.</span><span class="sxs-lookup"><span data-stu-id="3a546-112">For employees leaving the organization, some may need to end the award on the termination date, while others rely on the last day worked to stop the accrual process.</span></span> <span data-ttu-id="3a546-113">Bu değişiklik, kuruluşlara sonlandırma işleminde dahil olunmanın ne zaman sonlandıracağını seçme yeteneği sunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="3a546-113">These changes provide organizations the ability to choose when to end enrollment during the termination process.</span></span> <span data-ttu-id="3a546-114">Bu yeni seçenekler, Çalışanı işten çıkarma ve Çalışanı yöneticiden ayırma self servisinin ayrıcalıklarıdır.</span><span class="sxs-lookup"><span data-stu-id="3a546-114">These new options are part of the privileges for Terminate a worker and Terminate a worker from manager self service.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="3a546-115">Diğer değişimler</span><span class="sxs-lookup"><span data-stu-id="3a546-115">Other changes</span></span>

<span data-ttu-id="3a546-116">Bu sürüm çeşitli hatalara yönelik düzeltmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="3a546-116">This release includes several additional bug fixes.</span></span>

## <a name="known-issue"></a><span data-ttu-id="3a546-117">Bilinen Sorun</span><span class="sxs-lookup"><span data-stu-id="3a546-117">Known Issue</span></span>

-   <span data-ttu-id="3a546-118">**Sorun:** Bir çalışana yeni bir eklenti eklerken, **Yeni** ve **Düzenle** düğmeleri gri haldedir. **Geçici çözüm:** Eklenti sayfasını açmadan önce, **Çalışan** sayfasındaki bilgi kutularının kapalı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="3a546-118">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the fact boxes on the **Worker** page are closed.</span></span> <span data-ttu-id="3a546-119">**Çalışan** sayfası yüklendiğinde bilgi kutuları kapalıysa, eklentiler düğmeleri etkinleştirilmiş olacaktır.</span><span class="sxs-lookup"><span data-stu-id="3a546-119">If the fact boxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="3a546-120">(Bu sorun sonraki platform güncelleştirmesinde giderilecektir.)</span><span class="sxs-lookup"><span data-stu-id="3a546-120">(This issue will be fixed in the next platform update.)</span></span>

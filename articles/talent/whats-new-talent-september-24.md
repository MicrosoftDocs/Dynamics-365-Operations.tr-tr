---
title: Dynamics 365 Talent - Core HR'daki yenilikler veya değişiklikler (24 Eylül 2018)
description: Bu konuda, Microsoft Dynamics 365 Talent - Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 09/21/2018
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
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e0c1a3bf7613db4887e0943a70ad6262a70997f0
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898978"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-24-2018"></a><span data-ttu-id="ce4d7-103">Dynamics 365 Talent - Core HR'daki yenilikler veya değişiklikler (24 Eylül 2018)</span><span class="sxs-lookup"><span data-stu-id="ce4d7-103">What's new or changed in Dynamics 365 Talent - Core HR (September 24, 2018)</span></span>

<span data-ttu-id="ce4d7-104">**Derleme 8.1.1015.0**</span><span class="sxs-lookup"><span data-stu-id="ce4d7-104">**Build 8.1.1015.0**</span></span>

<span data-ttu-id="ce4d7-105">Bu konuda, Core HR'deki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ce4d7-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="currency-added-to-benefits"></a><span data-ttu-id="ce4d7-106">Kazançlara para birimi eklendi</span><span class="sxs-lookup"><span data-stu-id="ce4d7-106">Currency added to Benefits</span></span>

<span data-ttu-id="ce4d7-107">Kazanç planları, kazancın para birimini içerecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="ce4d7-107">Benefit plans have been updated to include the currency of the benefit.</span></span> <span data-ttu-id="ce4d7-108">Bu yeni alan da çalışanın dahil olduğu kazançlarda mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="ce4d7-108">This new field is also available on worker enrolled benefits.</span></span> <span data-ttu-id="ce4d7-109">Bu yeni alan Bakım kazançlarının ve Kazanç güvenliği ayrıcalığı listesini görüntülenin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="ce4d7-109">This new field is part of the Maintain benefits and View a list of benefits security privilege.</span></span>

## <a name="update-proration-process--leave-and-absence"></a><span data-ttu-id="ce4d7-110">Güncelleştirme bölümlendirme işlemi - İzin ve devamsızlık</span><span class="sxs-lookup"><span data-stu-id="ce4d7-110">Update proration process – Leave and Absence</span></span>

<span data-ttu-id="ce4d7-111">Kuruluşlar, çalışanların şirkete ne zaman katıldığı ve çıktığına dayalı olarak farklı izinler verirler.</span><span class="sxs-lookup"><span data-stu-id="ce4d7-111">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="ce4d7-112">Kuruluştan ayrılan çalışanlar için bazılarının ödülü kapatma tarihinde sonlandırmaları gerekirken, diğerleri, tahakkuk işlemini durdurmak için çalışılan son güne ihtiyaç duymaktadır.</span><span class="sxs-lookup"><span data-stu-id="ce4d7-112">For employees leaving the organization, some may need to end the award on the termination date, while others rely on the last day worked to stop the accrual process.</span></span> <span data-ttu-id="ce4d7-113">Bu değişiklik, kuruluşlara sonlandırma işleminde dahil olunmanın ne zaman sonlandıracağını seçme yeteneği sunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ce4d7-113">These changes provide organizations the ability to choose when to end enrollment during the termination process.</span></span> <span data-ttu-id="ce4d7-114">Bu yeni seçenekler, Çalışanı işten çıkarma ve Çalışanı yöneticiden ayırma self servisinin ayrıcalıklarıdır.</span><span class="sxs-lookup"><span data-stu-id="ce4d7-114">These new options are part of the privileges for Terminate a worker and Terminate a worker from manager self service.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="ce4d7-115">Diğer değişimler</span><span class="sxs-lookup"><span data-stu-id="ce4d7-115">Other changes</span></span>

<span data-ttu-id="ce4d7-116">Bu sürüm çeşitli hatalara yönelik düzeltmeler içerir.</span><span class="sxs-lookup"><span data-stu-id="ce4d7-116">This release includes several additional bug fixes.</span></span>

## <a name="known-issue"></a><span data-ttu-id="ce4d7-117">Bilinen Sorun</span><span class="sxs-lookup"><span data-stu-id="ce4d7-117">Known Issue</span></span>

-   <span data-ttu-id="ce4d7-118">**Sorun:** Bir çalışana yeni bir eklenti eklerken, **Yeni** ve **Düzenle** düğmeleri gri haldedir. **Geçici çözüm:** Eklenti sayfasını açmadan önce, **Çalışan** sayfasındaki bilgi kutularının kapalı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="ce4d7-118">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the fact boxes on the **Worker** page are closed.</span></span> <span data-ttu-id="ce4d7-119">**Çalışan** sayfası yüklendiğinde bilgi kutuları kapalıysa, eklentiler düğmeleri etkinleştirilmiş olacaktır.</span><span class="sxs-lookup"><span data-stu-id="ce4d7-119">If the fact boxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="ce4d7-120">(Bu sorun sonraki platform güncelleştirmesinde giderilecektir.)</span><span class="sxs-lookup"><span data-stu-id="ce4d7-120">(This issue will be fixed in the next platform update.)</span></span>

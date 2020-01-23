---
title: Dynamics 365 Talent - Core HR'daki yenilikler veya değişiklikler (15 Kasım 2018)
description: Bu konuda, Microsoft Dynamics 365 Talent - Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
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
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1a7598db1dc4c11864cf5f5a73d00672ceb66e8c
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897478"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-november-15-2018"></a><span data-ttu-id="5f31c-103">Dynamics 365 Talent - Core HR'daki yenilikler veya değişiklikler (15 Kasım 2018)</span><span class="sxs-lookup"><span data-stu-id="5f31c-103">What's new or changed in Dynamics 365 Talent - Core HR (November 15, 2018)</span></span>

<span data-ttu-id="5f31c-104">**Derleme 8.1.2045**</span><span class="sxs-lookup"><span data-stu-id="5f31c-104">**Build 8.1.2045**</span></span>

<span data-ttu-id="5f31c-105">Bu konuda, Core HR'deki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="5f31c-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="other-changesfixes"></a><span data-ttu-id="5f31c-106">Diğer değişimler/düzeltmeler</span><span class="sxs-lookup"><span data-stu-id="5f31c-106">Other changes/fixes</span></span>

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a><span data-ttu-id="5f31c-107">Personelin geçerli konumuna gelecekteki açık bir konuma değiştirilemiyor</span><span class="sxs-lookup"><span data-stu-id="5f31c-107">Unable to change employee´s current position to a future open position</span></span>

<span data-ttu-id="5f31c-108">Konum yalnızca gelecekte kullanılabilirse, konum transferlerine olanak sağlamak için bir değişiklik yapıldı.</span><span class="sxs-lookup"><span data-stu-id="5f31c-108">A change has been made to enable position transfers when the position is only available in the future.</span></span> 

### <a name="position-does-not-display-when-creating-a-new-employee"></a><span data-ttu-id="5f31c-109">Konum, yeni bir çalışan oluşturulduğunda görüntülenmiyor</span><span class="sxs-lookup"><span data-stu-id="5f31c-109">Position does not display when creating a new employee</span></span>

<span data-ttu-id="5f31c-110">Talent içinde yeni çalışanlar işe alırken atamaya açık konumları görüntülemek için bir değişiklik yapıldı.</span><span class="sxs-lookup"><span data-stu-id="5f31c-110">A change has been made to display all open positions that are available for assignment when hiring new employees in Talent.</span></span> <span data-ttu-id="5f31c-111">Bu, geçmişteki pozisyonları veya gelecek tarihteki konumları dahil etmektedir.</span><span class="sxs-lookup"><span data-stu-id="5f31c-111">This includes historical positions or if the postitions have been future dated.</span></span> <span data-ttu-id="5f31c-112">Pozisyonlar artık çalışan başlangıç tarihinde şimdi doğru olarak görüntülenecektir.</span><span class="sxs-lookup"><span data-stu-id="5f31c-112">Positions will now appear correctly based on the employment start date.</span></span> 

### <a name="termination-date-is-displaying-based-on-user-settings"></a><span data-ttu-id="5f31c-113">İşe son verme tarihi kullanıcı ayarlarına dayalı olarak görüntülenir</span><span class="sxs-lookup"><span data-stu-id="5f31c-113">Termination date is displaying based on user settings</span></span>

<span data-ttu-id="5f31c-114">İşe son verme tarihini görüntülerken tercih çalışanın tercih edilen zaman dilimini denk getirmek için geçmiş çalışan listesinde bir değişiklik yapıldı.</span><span class="sxs-lookup"><span data-stu-id="5f31c-114">A change has been made to the past employees list to account for any time zone offsets for the employees preferred time zone when viewing the termination date.</span></span>

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a><span data-ttu-id="5f31c-115">Bana atanmış çalışma öğeleri bağlantıları, doğru bilgiyi göstermiyor</span><span class="sxs-lookup"><span data-stu-id="5f31c-115">Work items assigned to me links not displaying the correct information</span></span>

<span data-ttu-id="5f31c-116">Bu değişiklik ile, listede tekil iş öğelerinin ayrıntılarına gezinti, seçilen öğe için doğru bilgiyi gösterecektir.</span><span class="sxs-lookup"><span data-stu-id="5f31c-116">With this change, navigation to the details of the individual work items in the list will display the correct information for the item selected.</span></span> <span data-ttu-id="5f31c-117">Bu sorun yalnızca gelişmiş güvenlik seçenekleri ile ortaya çıkmaktaydı.</span><span class="sxs-lookup"><span data-stu-id="5f31c-117">This issue only occurred with advanced security options.</span></span>


## <a name="known-issue"></a><span data-ttu-id="5f31c-118">Bilinen sorun</span><span class="sxs-lookup"><span data-stu-id="5f31c-118">Known issue</span></span>

- <span data-ttu-id="5f31c-119">**Sorun**: Bir çalışan için yeni bir eki eklerken **Yeni** ve **Düzenle** düğmeleri gridir.</span><span class="sxs-lookup"><span data-stu-id="5f31c-119">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="5f31c-120">**Çözüm:** Ek sayfasını açmadan önce **Çalışan** sayfasındaki bilgi kutularının kapalı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="5f31c-120">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="5f31c-121">**Çalışan** sayfası yüklendiğinde bilgi kutuları kapalıysa, eklentiler düğmeleri etkinleştirilmiş olacaktır.</span><span class="sxs-lookup"><span data-stu-id="5f31c-121">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="5f31c-122">(Bu sorun sonraki platform güncelleştirmesinde giderilecektir.)</span><span class="sxs-lookup"><span data-stu-id="5f31c-122">(This issue will be fixed in the next platform update.)</span></span>

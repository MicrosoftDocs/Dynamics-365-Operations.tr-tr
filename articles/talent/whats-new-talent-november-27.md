---
title: Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (27 Kasım 2018)
description: Bu konuda, Microsoft Dynamics 365 for Talent Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
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
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 81ea0e4f4878d1967234c597504071ce464a22c5
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1519324"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-27-2018"></a><span data-ttu-id="712dc-103">Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (27 Kasım 2018)</span><span class="sxs-lookup"><span data-stu-id="712dc-103">What's new or changed in Dynamics 365 for Talent Core HR (November 27, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="712dc-104">**Derleme 8.1.2064**</span><span class="sxs-lookup"><span data-stu-id="712dc-104">**Build 8.1.2064**</span></span>

<span data-ttu-id="712dc-105">Bu konuda, Core HR'deki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="712dc-105">This topic describes features that are either new or changed in Core HR.</span></span>


## <a name="changes"></a><span data-ttu-id="712dc-106">Değişiklikler</span><span class="sxs-lookup"><span data-stu-id="712dc-106">Changes</span></span>

### <a name="unable-to-create-a-note-in-case-management"></a><span data-ttu-id="712dc-107">Servis Talebi Yönetiminde not oluşturulamıyor</span><span class="sxs-lookup"><span data-stu-id="712dc-107">Unable to create a note in Case Management</span></span>

<span data-ttu-id="712dc-108">Servis Talebi Yönetimi servis talebi günlüğünde bir not oluşturmaya veya düzenlemeye çalışırken oluşan bir hata için bir değişim yapıldı.</span><span class="sxs-lookup"><span data-stu-id="712dc-108">A change has been made for an issue when attempting to edit or create a note in the case log of Case Management.</span></span>

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a><span data-ttu-id="712dc-109">Analytics sekmesinde, ücret çalışma alanında yanlış yazılmış sözcük</span><span class="sxs-lookup"><span data-stu-id="712dc-109">Misspelled word on the analytics tab in the compensation workspace</span></span> 

<span data-ttu-id="712dc-110">Ücret çalışma alanında, ücret analizi çizelgesinde 'Etnik Köken' kelimesinin yazılışını düzeltmek için bir değişiklik yapıldı.</span><span class="sxs-lookup"><span data-stu-id="712dc-110">A change has been made to correct the spelling of 'Ethnic Origin' in the compensation analytics chart in the compensation workspace.</span></span>

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a><span data-ttu-id="712dc-111">Çalışan self servis çalışma alanı, bir kullanıcı bir çalışana atanmamış olduğunda görüntülenmiyor.</span><span class="sxs-lookup"><span data-stu-id="712dc-111">Employee self-service workspace not displaying when a user isn't assigned to a worker</span></span> 

<span data-ttu-id="712dc-112">**Çalışan self servis** çalışma alanı, bir çalışana atanmamış bir kullanıcı için başlangıçta ilk sayfa olarak seçildiyse bir değişiklik yapıldı.</span><span class="sxs-lookup"><span data-stu-id="712dc-112">A change has been made when the **Employee self-service** workspace is selected as the initial page on startup for a user who is not assigned to a worker.</span></span> <span data-ttu-id="712dc-113">Bu durumda, varsayılan pano görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="712dc-113">In this situation, the default dashboard will be displayed.</span></span>

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a><span data-ttu-id="712dc-114">Bırakma ve Devamsızlık hatası: Bir nesne referansı, bir nesnenin örneğine ayarlanmadı</span><span class="sxs-lookup"><span data-stu-id="712dc-114">Leave and Absence error: Object reference not set to an instance of an object</span></span>

<span data-ttu-id="712dc-115">**Bana atanmış çalışma öğeleri** listesinde, bırakma ve devamsızlık kayıtları onaylandıktan sonra, Bırakma ve Devamsızlıkta bu hatayı düzeltmek için değişiklikler yapıldı.</span><span class="sxs-lookup"><span data-stu-id="712dc-115">Changes have been made to Leave and Absence to correct this error after approving leave and absence records in the **Work items assigned to me** list.</span></span>

### <a name="unable-to-recall-an-image-workflow"></a><span data-ttu-id="712dc-116">Bir resim iş akışı çağrılamıyor</span><span class="sxs-lookup"><span data-stu-id="712dc-116">Unable to recall an image workflow</span></span>

<span data-ttu-id="712dc-117">Bir resim iş akışını geri çağırdıktan sonra, iş akışı "iptal edildi" olarak ayarlanır ve mevcut talep çalışan self servis çalışma alanında silinebilir.</span><span class="sxs-lookup"><span data-stu-id="712dc-117">After recalling an image workflow, the workflow will be set to "cancelled" and the existing request can be deleted in the employee self-service workspace.</span></span>

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a><span data-ttu-id="712dc-118">Geri işe alınan çalışanlar ve yükleniciler, sonlandırmadan sonra birden fazla kez gözükmektedir</span><span class="sxs-lookup"><span data-stu-id="712dc-118">Rehired employees or contractors show up multiple times after termination</span></span> 

<span data-ttu-id="712dc-119">Bu güncelleştirme ile, işine son verildikten sonra işe tekrar alınan çalışanlar çıkılan listede yalnızca bir kez görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="712dc-119">With this update, terminated employees that are rehired will only display one time in the exited list.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="712dc-120">Bilinen sorun</span><span class="sxs-lookup"><span data-stu-id="712dc-120">Known issue</span></span>

- <span data-ttu-id="712dc-121">**Sorun**: Bir çalışan için yeni bir eki eklerken **Yeni** ve **Düzenle** düğmeleri gridir.</span><span class="sxs-lookup"><span data-stu-id="712dc-121">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="712dc-122">**Çözüm:** Ek sayfasını açmadan önce **Çalışan** sayfasındaki bilgi kutularının kapalı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="712dc-122">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="712dc-123">**Çalışan** sayfası yüklendiğinde bilgi kutuları kapalıysa, eklentiler düğmeleri etkinleştirilmiş olacaktır.</span><span class="sxs-lookup"><span data-stu-id="712dc-123">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="712dc-124">(Bu sorun sonraki platform güncelleştirmesinde giderilecektir.)</span><span class="sxs-lookup"><span data-stu-id="712dc-124">(This issue will be fixed in the next platform update.)</span></span>

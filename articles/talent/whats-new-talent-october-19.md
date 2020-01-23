---
title: Dynamics 365 Talent - Core HR'daki yenilikler veya değişiklikler (16 Ekim 2018)
description: Bu konuda, Microsoft Dynamics 365 Talent - Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
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
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d5f2aea5fcc81d0b4c1d8a392a3e56c888440a94
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897408"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-16-2018"></a><span data-ttu-id="5a093-103">Dynamics 365 Talent - Core HR'daki yenilikler veya değişiklikler (16 Ekim 2018)</span><span class="sxs-lookup"><span data-stu-id="5a093-103">What's new or changed in Dynamics 365 Talent - Core HR (October 16, 2018)</span></span>

<span data-ttu-id="5a093-104">**Derleme 8.1.1067**</span><span class="sxs-lookup"><span data-stu-id="5a093-104">**Build 8.1.1067**</span></span>

<span data-ttu-id="5a093-105">Bu konuda, Core HR'deki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="5a093-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-managers-to-update-time-off-requests"></a><span data-ttu-id="5a093-106">Yöneticilerin izin istekleri güncelleştirmesine izin ver</span><span class="sxs-lookup"><span data-stu-id="5a093-106">Allow managers to update time off requests</span></span>

<span data-ttu-id="5a093-107">Personel izin isteklerinin, iş akışında onaylandıktan sonra güncelleştirilmesi gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="5a093-107">Employee time off requests may need to be updated after they are approved through the workflow.</span></span> <span data-ttu-id="5a093-108">Çoğu durumda, yönetici bu güncelleştirmeleri personelin adına sağlar.</span><span class="sxs-lookup"><span data-stu-id="5a093-108">In many cases, the manager makes these updates on the employee’s behalf.</span></span> <span data-ttu-id="5a093-109">Bu yeni özellik, yöneticilere personelleri adına izini güncelleştirme ve izin isteklerini iptal etme özelliği sunar.</span><span class="sxs-lookup"><span data-stu-id="5a093-109">This new feature provides the ability for managers to update time off or cancel time off requests on behalf of their employees.</span></span> <span data-ttu-id="5a093-110">Bu özellik **Adına iş** parametresi tarafından kontrol edilir ve **İnsan kaynağı parametreleri** sayfasından ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="5a093-110">This capability is controlled by the **Work on behalf** parameter that can be set on the **Human Resource Parameters** page.</span></span> 
 
## <a name="allow-hr-to-update-time-off-requests"></a><span data-ttu-id="5a093-111">İK'nın izin istekleri güncelleştirmesine izin ver</span><span class="sxs-lookup"><span data-stu-id="5a093-111">Allow HR to update time off requests</span></span>

<span data-ttu-id="5a093-112">Yukarıdaki özelliği benzer şekilde, personel izin isteklerinin, iş akışında onaylanmasından sonra İK tarafından güncellenmesi gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="5a093-112">Similar to the feature above, employee time off requests may need to be updated by HR after they have been previously approved through the workflow.</span></span> <span data-ttu-id="5a093-113">Bu özellik, İK kullanıcılarının izin isteklerini güncelleştirmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="5a093-113">This feature provides the ability for HR users to update time off requests.</span></span> <span data-ttu-id="5a093-114">Özellik, **Kişiler** çalışma alanında ve **Çalışan** sayfasında **İzin süresini görüntüle** adlı yeni seçenek kullanılarak etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="5a093-114">The capability is enabled in the **People** workspace and on the **Worker** page, using a new option called **View time off**.</span></span> <span data-ttu-id="5a093-115">Bu sayfalarda, İK kullanıcıları isteklerini görüntüleyebilir ve izin hareketlerini güncelleştirebilir; aynı yöneticilerin bu eylemleri yapabildiği gibi.</span><span class="sxs-lookup"><span data-stu-id="5a093-115">On those pages, HR users can view requests and update time off transactions, similar to how managers can perform these actions.</span></span>

<span data-ttu-id="5a093-116">Bu işlevlere erişimi kontrol eden güvenlik görevi aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="5a093-116">The security duty that controls access to this functionality is:</span></span>
- <span data-ttu-id="5a093-117">Görev: Çalışana özel izin ve devamsızlık işlemlerini koru.</span><span class="sxs-lookup"><span data-stu-id="5a093-117">Duty: Maintain worker-specific leave and absence processes.</span></span>
- <span data-ttu-id="5a093-118">Ayrıcalık: Tüm çalışanlar için izin ve devamsızlık isteklerini koru.</span><span class="sxs-lookup"><span data-stu-id="5a093-118">Privilege: Maintain leave and absence requests for all workers.</span></span>

## <a name="other-changes"></a><span data-ttu-id="5a093-119">Diğer değişimler</span><span class="sxs-lookup"><span data-stu-id="5a093-119">Other changes</span></span>
<span data-ttu-id="5a093-120">Aşağıdaki güncelleştirmeler bu sürümde yapıldı:</span><span class="sxs-lookup"><span data-stu-id="5a093-120">The following updates have been made in this release:</span></span>
- <span data-ttu-id="5a093-121">Çalışan işe alma eylemleri, artık **İş akışı tamam** durumunda "sıkışmasın" diye değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="5a093-121">Changes to worker hire actions so that they are no longer "stuck" in **Workflow complete** state.</span></span>
- <span data-ttu-id="5a093-122">Peronsel kaydı, artık çalışma başlangıç tarihi olmadan oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5a093-122">Employment record can now be created without an employment start date.</span></span>
- <span data-ttu-id="5a093-123">Personel self servisinde gösterilen bir kurs için Dynamics 365 Talent kaydı artık tarihteki saat dilimi farkını uyguluyor.</span><span class="sxs-lookup"><span data-stu-id="5a093-123">The Dynamics 365 Talent registration date for a course shown in Employee self-service now applies the time zone offset to the date.</span></span>
- <span data-ttu-id="5a093-124">Excel dosyaları, **Personel Varlığı** kullanılarak artık hatasız şekilde birden çok kez içe aktarılır.</span><span class="sxs-lookup"><span data-stu-id="5a093-124">Excel files can be imported multiple times without any errors using **Employee Entity**.</span></span>

## <a name="known-issue"></a><span data-ttu-id="5a093-125">Bilinen sorun</span><span class="sxs-lookup"><span data-stu-id="5a093-125">Known issue</span></span>

- <span data-ttu-id="5a093-126">**Sorun**: Bir çalışan için yeni bir eki eklerken **Yeni** ve **Düzenle** düğmeleri gridir.</span><span class="sxs-lookup"><span data-stu-id="5a093-126">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="5a093-127">**Çözüm:** Ek sayfasını açmadan önce **Çalışan** sayfasındaki bilgi kutularının kapalı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="5a093-127">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="5a093-128">**Çalışan** sayfası yüklendiğinde bilgi kutuları kapalıysa, eklentiler düğmeleri etkinleştirilmiş olacaktır.</span><span class="sxs-lookup"><span data-stu-id="5a093-128">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="5a093-129">(Bu sorun sonraki platform güncelleştirmesinde giderilecektir.)</span><span class="sxs-lookup"><span data-stu-id="5a093-129">(This issue will be fixed in the next platform update.)</span></span>

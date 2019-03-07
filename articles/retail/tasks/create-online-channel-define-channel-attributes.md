---
title: Çevrimiçi kanal oluştur ve kanal özniteliklerini tanımla
description: Bu yordam yeni bir çevrimiçi kanal oluşturma ve kuruluş hiyerarşisine ekleme konusunda rehberlik sağlar.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e066e9901a97bd5b72815a7af472247ef519ecb9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "312382"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="cabce-103">Çevrimiçi kanal oluştur ve kanal özniteliklerini tanımla</span><span class="sxs-lookup"><span data-stu-id="cabce-103">Create online channel and define channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="cabce-104">Bu yordam yeni bir çevrimiçi kanal oluşturma ve kuruluş hiyerarşisine ekleme konusunda rehberlik sağlar.</span><span class="sxs-lookup"><span data-stu-id="cabce-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="cabce-105">Yeni bir çevrimiçi kanal oluşturmadan önce kuruluş hiyerarşisi oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="cabce-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="cabce-106">Bu yordam, USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="cabce-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="cabce-107">Yeni çevrimiçi kanal oluşturma</span><span class="sxs-lookup"><span data-stu-id="cabce-107">Create a new online channel</span></span>
1. <span data-ttu-id="cabce-108">Perakende ve ticaret > Kanalları > Çevrimiçi mağazalarına gidin.</span><span class="sxs-lookup"><span data-stu-id="cabce-108">Go to Retail and commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="cabce-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cabce-109">Click New.</span></span>
3. <span data-ttu-id="cabce-110">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="cabce-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="cabce-111">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="cabce-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="cabce-112">Mağaza saat dilimi alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="cabce-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="cabce-113">Varsayılan müşteri alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="cabce-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="cabce-114">Müşteri adres defteri alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="cabce-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="cabce-115">Ödeme koşulları alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="cabce-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="cabce-116">Ödeme yöntemi alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="cabce-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="cabce-117">E-posta bildirim profili alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="cabce-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="cabce-118">Mali boyutlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="cabce-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="cabce-119">BusinessUnit alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="cabce-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="cabce-120">Benzer şekilde, diğer tüm varsayılan boyutlar için değeri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cabce-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="cabce-121">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cabce-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="cabce-122">Çevrimiçi kanalı kuruluş hiyerarşisine ekle</span><span class="sxs-lookup"><span data-stu-id="cabce-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="cabce-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="cabce-123">Close the page.</span></span>
2. <span data-ttu-id="cabce-124">Organizasyon yönetimi > Kuruluşlar > Kuruluş hiyerarşileri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="cabce-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="cabce-125">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="cabce-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="cabce-126">Görüntüle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cabce-126">Click View.</span></span>
5. <span data-ttu-id="cabce-127">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cabce-127">Click Edit.</span></span>
    * <span data-ttu-id="cabce-128">Yeni kanal eklemek istediğiniz herhangi bir hiyerarşi düğümünü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cabce-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="cabce-129">Ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cabce-129">Click Insert.</span></span>
7. <span data-ttu-id="cabce-130">Perakende kanalı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cabce-130">Click Retail channel.</span></span>
8. <span data-ttu-id="cabce-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cabce-131">Click OK.</span></span>
9. <span data-ttu-id="cabce-132">İletişim kutusunu açmak için Yayımla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cabce-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="cabce-133">Yürürlük tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="cabce-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="cabce-134">Yayımla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cabce-134">Click Publish.</span></span>


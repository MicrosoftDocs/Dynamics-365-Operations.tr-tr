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
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569533"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="1e0f9-103">Çevrimiçi kanal oluştur ve kanal özniteliklerini tanımla</span><span class="sxs-lookup"><span data-stu-id="1e0f9-103">Create online channel and define channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1e0f9-104">Bu yordam yeni bir çevrimiçi kanal oluşturma ve kuruluş hiyerarşisine ekleme konusunda rehberlik sağlar.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="1e0f9-105">Yeni bir çevrimiçi kanal oluşturmadan önce kuruluş hiyerarşisi oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="1e0f9-106">Bu yordam, USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="1e0f9-107">Yeni çevrimiçi kanal oluşturma</span><span class="sxs-lookup"><span data-stu-id="1e0f9-107">Create a new online channel</span></span>
1. <span data-ttu-id="1e0f9-108">Perakende ve ticaret > Kanalları > Çevrimiçi mağazalarına gidin.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-108">Go to Retail and commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="1e0f9-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-109">Click New.</span></span>
3. <span data-ttu-id="1e0f9-110">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="1e0f9-111">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="1e0f9-112">Mağaza saat dilimi alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="1e0f9-113">Varsayılan müşteri alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="1e0f9-114">Müşteri adres defteri alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="1e0f9-115">Ödeme koşulları alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="1e0f9-116">Ödeme yöntemi alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="1e0f9-117">E-posta bildirim profili alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="1e0f9-118">Mali boyutlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="1e0f9-119">BusinessUnit alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="1e0f9-120">Benzer şekilde, diğer tüm varsayılan boyutlar için değeri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="1e0f9-121">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="1e0f9-122">Çevrimiçi kanalı kuruluş hiyerarşisine ekle</span><span class="sxs-lookup"><span data-stu-id="1e0f9-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="1e0f9-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-123">Close the page.</span></span>
2. <span data-ttu-id="1e0f9-124">Organizasyon yönetimi > Kuruluşlar > Kuruluş hiyerarşileri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="1e0f9-125">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="1e0f9-126">Görüntüle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-126">Click View.</span></span>
5. <span data-ttu-id="1e0f9-127">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-127">Click Edit.</span></span>
    * <span data-ttu-id="1e0f9-128">Yeni kanal eklemek istediğiniz herhangi bir hiyerarşi düğümünü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="1e0f9-129">Ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-129">Click Insert.</span></span>
7. <span data-ttu-id="1e0f9-130">Perakende kanalı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-130">Click Retail channel.</span></span>
8. <span data-ttu-id="1e0f9-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-131">Click OK.</span></span>
9. <span data-ttu-id="1e0f9-132">İletişim kutusunu açmak için Yayımla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="1e0f9-133">Yürürlük tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="1e0f9-134">Yayımla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1e0f9-134">Click Publish.</span></span>


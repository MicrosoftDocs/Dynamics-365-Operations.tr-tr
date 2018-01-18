--- 
title: " Çevrimiçi kanallar oluşturma ve kanal özniteliklerini tanımlama"
description: "Bu yordam yeni bir çevrimiçi kanal oluşturma ve kuruluş hiyerarşisine ekleme konusunda rehberlik sağlar."
author: jashanno
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: d1cdb36b99abb9902f30a7a487a912f3a213dcf8
ms.contentlocale: tr-tr
ms.lasthandoff: 01/18/2018

---
# <a name="create-online-channels-and-define-channel-attributes"></a><span data-ttu-id="5cde8-103"> Çevrimiçi kanallar oluşturma ve kanal özniteliklerini tanımlama</span><span class="sxs-lookup"><span data-stu-id="5cde8-103">Create online channels and define channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="5cde8-104">Bu yordam yeni bir çevrimiçi kanal oluşturma ve kuruluş hiyerarşisine ekleme konusunda rehberlik sağlar.</span><span class="sxs-lookup"><span data-stu-id="5cde8-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="5cde8-105">Yeni bir çevrimiçi kanal oluşturmadan önce kuruluş hiyerarşisi oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5cde8-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="5cde8-106">Bu yordam, USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="5cde8-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="5cde8-107">Yeni çevrimiçi kanal oluşturma</span><span class="sxs-lookup"><span data-stu-id="5cde8-107">Create a new online channel</span></span>
1. <span data-ttu-id="5cde8-108">Perakende ve ticaret > Kanalları > Çevrimiçi mağazalarına gidin.</span><span class="sxs-lookup"><span data-stu-id="5cde8-108">Go to Retail and commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="5cde8-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5cde8-109">Click New.</span></span>
3. <span data-ttu-id="5cde8-110">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="5cde8-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="5cde8-111">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="5cde8-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="5cde8-112">Mağaza saat dilimi alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="5cde8-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="5cde8-113">Varsayılan müşteri alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="5cde8-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="5cde8-114">Müşteri adres defteri alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="5cde8-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="5cde8-115">Ödeme koşulları alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="5cde8-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="5cde8-116">Ödeme yöntemi alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="5cde8-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="5cde8-117">E-posta bildirim profili alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="5cde8-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="5cde8-118">Mali boyutlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="5cde8-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="5cde8-119">BusinessUnit alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="5cde8-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="5cde8-120">Benzer şekilde, diğer tüm varsayılan boyutlar için değeri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5cde8-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="5cde8-121">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5cde8-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="5cde8-122">Çevrimiçi kanalı kuruluş hiyerarşisine ekle</span><span class="sxs-lookup"><span data-stu-id="5cde8-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="5cde8-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5cde8-123">Close the page.</span></span>
2. <span data-ttu-id="5cde8-124">Organizasyon yönetimi > Kuruluşlar > Kuruluş hiyerarşileri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="5cde8-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="5cde8-125">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5cde8-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="5cde8-126">Görüntüle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5cde8-126">Click View.</span></span>
5. <span data-ttu-id="5cde8-127">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5cde8-127">Click Edit.</span></span>
    * <span data-ttu-id="5cde8-128">Yeni kanal eklemek istediğiniz herhangi bir hiyerarşi düğümünü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5cde8-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="5cde8-129">Ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5cde8-129">Click Insert.</span></span>
7. <span data-ttu-id="5cde8-130">Perakende kanalı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5cde8-130">Click Retail channel.</span></span>
8. <span data-ttu-id="5cde8-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5cde8-131">Click OK.</span></span>
9. <span data-ttu-id="5cde8-132">İletişim kutusunu açmak için Yayımla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5cde8-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="5cde8-133">Yürürlük tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="5cde8-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="5cde8-134">Yayımla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5cde8-134">Click Publish.</span></span>



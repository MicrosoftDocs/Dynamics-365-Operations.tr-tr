---
title: Çevrimiçi kanal oluştur ve kanal özniteliklerini tanımla
description: Bu yordam yeni bir çevrimiçi kanal oluşturma ve kuruluş hiyerarşisine ekleme konusunda rehberlik sağlar.
author: jashanno
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e28e717dcf594c5079b4b6987331115356b6bdbc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798525"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="2a9b6-103">Çevrimiçi kanal oluştur ve kanal özniteliklerini tanımla</span><span class="sxs-lookup"><span data-stu-id="2a9b6-103">Create online channel and define channel attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a9b6-104">Bu yordam yeni bir çevrimiçi kanal oluşturma ve kuruluş hiyerarşisine ekleme konusunda rehberlik sağlar.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="2a9b6-105">Yeni bir çevrimiçi kanal oluşturmadan önce kuruluş hiyerarşisi oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="2a9b6-106">Bu yordam, USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="2a9b6-107">Yeni çevrimiçi kanal oluşturma</span><span class="sxs-lookup"><span data-stu-id="2a9b6-107">Create a new online channel</span></span>
1. <span data-ttu-id="2a9b6-108">Retail and Commerce > Kanallar > Çevrimiçi mağazalar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-108">Go to Retail and Commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="2a9b6-109">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-109">Click New.</span></span>
3. <span data-ttu-id="2a9b6-110">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="2a9b6-111">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="2a9b6-112">Mağaza saat dilimi alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="2a9b6-113">Varsayılan müşteri alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="2a9b6-114">Müşteri adres defteri alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="2a9b6-115">Ödeme koşulları alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="2a9b6-116">Ödeme yöntemi alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="2a9b6-117">E-posta bildirim profili alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="2a9b6-118">Mali boyutlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="2a9b6-119">BusinessUnit alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="2a9b6-120">Benzer şekilde, diğer tüm varsayılan boyutlar için değeri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="2a9b6-121">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="2a9b6-122">Çevrimiçi kanalı kuruluş hiyerarşisine ekle</span><span class="sxs-lookup"><span data-stu-id="2a9b6-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="2a9b6-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-123">Close the page.</span></span>
2. <span data-ttu-id="2a9b6-124">Organizasyon yönetimi > Kuruluşlar > Kuruluş hiyerarşileri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="2a9b6-125">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="2a9b6-126">Görüntüle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-126">Click View.</span></span>
5. <span data-ttu-id="2a9b6-127">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-127">Click Edit.</span></span>
    * <span data-ttu-id="2a9b6-128">Yeni kanal eklemek istediğiniz herhangi bir hiyerarşi düğümünü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="2a9b6-129">Ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-129">Click Insert.</span></span>
7. <span data-ttu-id="2a9b6-130">Commerce kanalına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-130">Click Commerce channel.</span></span>
8. <span data-ttu-id="2a9b6-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-131">Click OK.</span></span>
9. <span data-ttu-id="2a9b6-132">İletişim kutusunu açmak için Yayımla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="2a9b6-133">Yürürlük tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="2a9b6-134">Yayımla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-134">Click Publish.</span></span>

## <a name="configure-orders-for-near-real-time-notification"></a><span data-ttu-id="2a9b6-135">Gerçek zamanlı bildirim yakınlarında siparişleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2a9b6-135">Configure orders for near real-time notification</span></span>
1. <span data-ttu-id="2a9b6-136">Retail ve Commerce > Headquarters ayarı > Parametreler > Commerce parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-136">Go to Retail and Commerce  > Headquarters setup > Parameters > Commerce parameters.</span></span>
2. <span data-ttu-id="2a9b6-137">eCommerce sipariş oluşturma için gerçek zamanlı hizmeti "Evet" olarak ayarla.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-137">Set Use realtime service for eCommerce order creation to "Yes".</span></span>
3. <span data-ttu-id="2a9b6-138">Değişiklikleri kanal veritabanıyla eşitlemek için 1070 dağıtım planını yürütün.</span><span class="sxs-lookup"><span data-stu-id="2a9b6-138">Run the 1070 distribution schedule to sync changes to the channel database.</span></span> 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
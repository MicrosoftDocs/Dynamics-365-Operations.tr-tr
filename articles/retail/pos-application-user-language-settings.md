---
title: "POS uygulaması ve kullanıcı dil ayarları"
description: "Bu konu, Retail Modern POS (MPOS) ve Bulut POS'daki dil ayarlarının nasıl değiştirileceğini açıklar."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: dacc072ab5c070010d86302fa08a3066125b23a6
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="pos-application-and-user-language-settings"></a><span data-ttu-id="452b0-103">POS uygulaması ve kullanıcı dil ayarları</span><span class="sxs-lookup"><span data-stu-id="452b0-103">POS application and user language settings</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="452b0-104">Bu konu, Retail Modern POS (MPOS) ve Bulut POS'daki dil ayarlarının nasıl değiştirileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="452b0-104">This topic describes how to change language settings in Retail Modern POS (MPOS) and Cloud POS.</span></span>

<a name="overview"></a><span data-ttu-id="452b0-105">Özet</span><span class="sxs-lookup"><span data-stu-id="452b0-105">Overview</span></span>
========

<span data-ttu-id="452b0-106">Retail Modern POS (MPOS) ve Bulut POS dil ayarları ve çevirilerin mağaza ve kullanıcı ayarları arasında farklılık gösterebildiği ortamları destekler.</span><span class="sxs-lookup"><span data-stu-id="452b0-106">Retail Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="452b0-107">Örneğin, mağaza müşterileri için yaygın olarak İngilizce kullanılan bir bölgede bulunabilir ancak bazı çalışanlar uygulamayı Fransızca çevirileri ile kullanmayı tercih edebilir.</span><span class="sxs-lookup"><span data-stu-id="452b0-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="452b0-108">Veri dili</span><span class="sxs-lookup"><span data-stu-id="452b0-108">Data language</span></span>
<span data-ttu-id="452b0-109">Kullanıcının ayarları ne olursa olsun, MPOS ve Bulut POS veriler için kullanılan çevirileri belirlemek üzere her zaman mağazanın dil ayarlarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="452b0-109">Regardless of the user’s settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="452b0-110">Bu, tüm kullanıcıların ve müşterilerin tutarlı bir deneyimi olmasını garanti eder.</span><span class="sxs-lookup"><span data-stu-id="452b0-110">This will ensure that all users and customers will have a consistent experience.</span></span>  <span data-ttu-id="452b0-111">Veri örnekleri:</span><span class="sxs-lookup"><span data-stu-id="452b0-111">Examples of data include:</span></span>

-   <span data-ttu-id="452b0-112">Ürünler</span><span class="sxs-lookup"><span data-stu-id="452b0-112">Products</span></span>
-   <span data-ttu-id="452b0-113">Öznitelikler ve değerler</span><span class="sxs-lookup"><span data-stu-id="452b0-113">Attributes and values</span></span>
-   <span data-ttu-id="452b0-114">Kategori adları</span><span class="sxs-lookup"><span data-stu-id="452b0-114">Category names</span></span>
-   <span data-ttu-id="452b0-115">Yazdırılan veya e-postayla gönderilen hareket girişleri</span><span class="sxs-lookup"><span data-stu-id="452b0-115">Printed or emailed transaction receipts</span></span>
-   <span data-ttu-id="452b0-116">Ödeme yöntemi adları</span><span class="sxs-lookup"><span data-stu-id="452b0-116">Payment method names</span></span>
-   <span data-ttu-id="452b0-117">Satır görüntüleme iletileri</span><span class="sxs-lookup"><span data-stu-id="452b0-117">Line display messages</span></span>

<span data-ttu-id="452b0-118">Kullanıcı oturum açmadan önce bilinmediğinden ana POS oturum açma ekranı için de mağazanın dili kullanılır.</span><span class="sxs-lookup"><span data-stu-id="452b0-118">The store’s language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="452b0-119">Mağazanın dili için kullanılabilir çeviri yoksa, POS şirketin diline döner.</span><span class="sxs-lookup"><span data-stu-id="452b0-119">If a translation is not available for the store’s language, the POS will revert to the company’s language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="452b0-120">Mağazanın dil ayarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="452b0-120">Configuring the store’s language setting</span></span>

<span data-ttu-id="452b0-121">Mağazanın dil ayarı **Genel &gt; Bölgesel Ayarlar &gt; Dil altındaki **Perakende Mağaza** sayfasında bulunan **Tüm perakende mağazalar**'dan ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="452b0-121">The store’s language setting is set from **All retail stores** on the **Retail Store** page under **General &gt; Regional Settings &gt; Language.</span></span> <span data-ttu-id="452b0-122">**Her mağaza için bir dil seçmek üzere açılır listeyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="452b0-122">**Use the drop down to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="452b0-123">Kullanıcı arabirimi dili</span><span class="sxs-lookup"><span data-stu-id="452b0-123">User interface language</span></span>
<span data-ttu-id="452b0-124">POS kullanıcısının dil ayar,ı uygulama kullanıcı arabiriminde kullanılan çevirileri belirler.</span><span class="sxs-lookup"><span data-stu-id="452b0-124">The POS user’s language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="452b0-125">Bu, tüm etiketleri, menüleri ve veri kabul edilmez listeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="452b0-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="452b0-126">Bunun tek istisnası POS düğme grupları üzerinde görüntülenen metindir.</span><span class="sxs-lookup"><span data-stu-id="452b0-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="452b0-127">Düğme grupları çevirileri desteklemez ve bunlar her zaman metinleri düğmede tanımlandığı şekilde gösterir.</span><span class="sxs-lookup"><span data-stu-id="452b0-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="452b0-128">Çevrilen düğmeleri desteklemek için, ayrı düğme grupları kopyalayıp korumanız ve bunları uygun şekilde kullanıcılara atamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="452b0-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="452b0-129">Kullanıcının dil ayarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="452b0-129">Configuring the user’s language setting</span></span>

<span data-ttu-id="452b0-130">POS kullanıcısının dil ayarı **Perakende &gt; Dil** altındaki **Çalışan** sayfasında bulunan **Tüm çalışanlar** öğesinden ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="452b0-130">The POS user’s language setting is set from **All workers** on the **Worker** page under **Retail &gt; Language**.</span></span>  <span data-ttu-id="452b0-131">Ana Profil öğesinden ayarlanmaz.  Bu ayar POS tarafından kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="452b0-131">It is not set on the main Profile tab.  This setting is not used by POS.</span></span> <span data-ttu-id="452b0-132">Kullanıcının dili ayarlanmamışsa veya çevirilerin mevcut olmadığı bir dile ayarlanmışsa, POS mağazanın diline döner.</span><span class="sxs-lookup"><span data-stu-id="452b0-132">If the user’s language is not set or it is set to a language where translations are not available, the POS will revert to the store’s language.</span></span>  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="452b0-133">** **</span><span class="sxs-lookup"><span data-stu-id="452b0-133">** **</span></span>       | <span data-ttu-id="452b0-134">**Kullanıcı Arabirimi dili** ** **</span><span class="sxs-lookup"><span data-stu-id="452b0-134">**UI language** ** **</span></span>      | <span data-ttu-id="452b0-135">**Veri dili (ürünler, makbuz biçimleri, satır görüntüleme, vs.)**</span><span class="sxs-lookup"><span data-stu-id="452b0-135">**Data language (products, receipt formats, line display, etc.)**</span></span> |
| <span data-ttu-id="452b0-136">**Şirket**</span><span class="sxs-lookup"><span data-stu-id="452b0-136">**Company**</span></span> | <span data-ttu-id="452b0-137">Varsayılan Değer</span><span class="sxs-lookup"><span data-stu-id="452b0-137">Default</span></span>                    | <span data-ttu-id="452b0-138">Varsayılan Değer</span><span class="sxs-lookup"><span data-stu-id="452b0-138">Default</span></span>                                                           |
| <span data-ttu-id="452b0-139">**Mağaza**</span><span class="sxs-lookup"><span data-stu-id="452b0-139">**Store**</span></span>   | <span data-ttu-id="452b0-140">Şirketi geçersiz kılar</span><span class="sxs-lookup"><span data-stu-id="452b0-140">Overrides company</span></span>          | <span data-ttu-id="452b0-141">Şirketi geçersiz kılar</span><span class="sxs-lookup"><span data-stu-id="452b0-141">Overrides company</span></span>                                                 |
| <span data-ttu-id="452b0-142">**Kullanıcı**</span><span class="sxs-lookup"><span data-stu-id="452b0-142">**User**</span></span>    | <span data-ttu-id="452b0-143">Mağazayı veya şirketi geçersiz kılar</span><span class="sxs-lookup"><span data-stu-id="452b0-143">Overrides store or company</span></span> | <span data-ttu-id="452b0-144">Hiçbir Zaman</span><span class="sxs-lookup"><span data-stu-id="452b0-144">Never</span></span>                                                             |







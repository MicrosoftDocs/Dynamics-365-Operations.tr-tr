---
title: Bir mobil cihaz menü öğesini malzeme çekme satırı özeti sağlayacak şekilde ayarlama
description: Bu konu, bir mobil cihazda ambar çalışmasını işleyen ambar çalışanlarına tüm iş satırlarının listesinin nasıl tanımlanacağını açıklar. Bu özellik, malzeme çekme sırasını en iyi duruma getirebilmek için bir iş emrindeki çekme satırlarının genel görünümüne gerek duyan ambar çalışanları için kullanışlı olabilir.
author: MarkusFogelberg
manager: tfehr
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 3a2c8a69a2c64214a38a654042ea2f62575e7f52
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439179"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a><span data-ttu-id="7b1c5-104">Bir mobil cihaz menü öğesini malzeme çekme satırı özeti sağlayacak şekilde ayarlama</span><span class="sxs-lookup"><span data-stu-id="7b1c5-104">Set up a mobile device menu item to provide a pick line overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="7b1c5-105">Bu konu, malzeme çekme işini işlemek için kullanılan mobil cihaz menü ögelerinin çekme satırı genel bakışla ilgili seçeneklerini nasıl yapılandırılacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-105">This topic explains how to configure options that are related to the pick line overview for mobile device menu items that are used to process picking work.</span></span> <span data-ttu-id="7b1c5-106">Çekme satırı genel bakışı ambar işçileri, geçerli görevlerinden ilgili tüm iş satırlarının listesinden seçim yapmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-106">The pick line overview lets warehouse workers view and select from a list of all the work lines that are related to their current task.</span></span> <span data-ttu-id="7b1c5-107">Bu özellik, çalışanların malzeme çekme sıralarını en iyi duruma getirmesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-107">This capability can help workers optimize their picking sequence.</span></span> <span data-ttu-id="7b1c5-108">Bu özellik, çalışanların sabit bir zamanda satırlar arasında dolaşmasına izin veren standart **Atlama** düğmesini değiştirecek seçenekler sunar.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-108">The feature provides options that replace the standard **Skip** button that lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="7b1c5-109">(Ancak, bu düğmeyi kullanma seçeneği hala bulunur.)</span><span class="sxs-lookup"><span data-stu-id="7b1c5-109">(However, the option to use that button is still available.)</span></span>

<span data-ttu-id="7b1c5-110">Yöneticiler her bir menü öğesini, ambar uygulamasının çekme satırı özetini nasıl, ne zaman ve nerede sunduğunu kontrol edebilecek yapılandırabilir.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-110">Admins can configure each menu item individually to control how, when, and where the warehouse app presents the pick line overview.</span></span>

## <a name="turn-on-the-work-pick-line-overview-feature"></a><span data-ttu-id="7b1c5-111">İş çekme satırı özeti özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="7b1c5-111">Turn on the Work pick line overview feature</span></span>

<span data-ttu-id="7b1c5-112">Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-112">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="7b1c5-113">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="7b1c5-114">**Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:</span><span class="sxs-lookup"><span data-stu-id="7b1c5-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="7b1c5-115">**Modül:** _Ambar yönetimi_</span><span class="sxs-lookup"><span data-stu-id="7b1c5-115">**Module:** _Warehouse management_</span></span>
- <span data-ttu-id="7b1c5-116">**Özellik adı:** _İş çekme satırı özeti_</span><span class="sxs-lookup"><span data-stu-id="7b1c5-116">**Feature name:** _Work pick line overview_</span></span>

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a><span data-ttu-id="7b1c5-117">Tüm iş satırlarının listesini göstermek için menü öğelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7b1c5-117">Configure menu items to show a list of all work lines</span></span>

<span data-ttu-id="7b1c5-118">Bir mobil cihaz menü öğesini malzeme çekme satırı özeti sağlayacak şekilde ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-118">To set up a mobile device menu item to provide a pick line overview, follow these steps.</span></span>

1. <span data-ttu-id="7b1c5-119">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-119">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="7b1c5-120">Malzeme çekme işiyle ilişkili menü ögesini seçin veya oluşturun ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="7b1c5-120">Select or create a menu item that is related to picking work, and set the following values:</span></span>

    - <span data-ttu-id="7b1c5-121">**Mod:** *İş*</span><span class="sxs-lookup"><span data-stu-id="7b1c5-121">**Mode:** *Work*</span></span>
    - <span data-ttu-id="7b1c5-122">**Mevcut işi kullan:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="7b1c5-122">**Use existing work:** *Yes*</span></span>
    - <span data-ttu-id="7b1c5-123">**Yöneten:** *Kullanıcı yönlendirmesinde* veya *Sistem yönlendirmesinde*</span><span class="sxs-lookup"><span data-stu-id="7b1c5-123">**Directed by:** *User directed* or *System directed*</span></span>

    <span data-ttu-id="7b1c5-124">Menü ögeleri oluşturma ve **Mobil cihaz menü öğeleri** sayfasında bulunan çeşitli ayarları kullanma hakkında daha fazla bilgi için bkz. [Ambar işi için mobil cihazları ayarlama](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="7b1c5-124">For more information about how to create menu items and use the various settings that are available on the **Mobile device menu items** page, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

1. <span data-ttu-id="7b1c5-125">**Genel** hızlı sekmesinde, **Çalışma satırı listesini göster** alanını aşağıdaki değerlerden birine göre ayarlayarak özelliği yapılandırın:</span><span class="sxs-lookup"><span data-stu-id="7b1c5-125">On the **General** FastTab, configure the feature by setting the **Show work line list** field to one of the following values:</span></span>

    - <span data-ttu-id="7b1c5-126">**Yalnızca talep üzerine göster**: Çalışanlar ambar uygulamasında **Atla** düğmesini seçerek çekme satırı listesini görüntülemeyi seçebilirler.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-126">**Show only upon request** – Workers can choose to view the pick line list by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="7b1c5-127">**Her bir çekmenin başlangıcında göster**: Çalışanlar, bir çekme satırını her başlattıklarında veya tamamladıklarında listeye bakar.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-127">**Show at the start of every pick** – Workers see the list every time that they start or finish a pick line.</span></span> <span data-ttu-id="7b1c5-128">Ambar uygulamasında **Atla** düğmesini seçerek listeyi yeniden görüntüleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-128">They can also view the list again by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="7b1c5-129">**Yalnızca ilk çekmenin başlangıcında göster**: Çalışanlar, listeyi her satırdan sonra değil, her yeni çekme işi başlattıklarında görür.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-129">**Show at the start of the first pick only** – Workers see the list every time that they start new picking work, but not after each line.</span></span> <span data-ttu-id="7b1c5-130">Ambar uygulamasında **Atla** düğmesini seçerek listeyi yeniden görüntüleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-130">They can also view the list again by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="7b1c5-131">**Hiçbir zaman gösterme**: Ambar uygulamasında standart **Atla** düğmesi görünür ve iş satırı listesinin görünümü kapalıdır.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-131">**Never show** – The standard **Skip** button appears in the warehouse app, and display of the work line list is turned off.</span></span> <span data-ttu-id="7b1c5-132">**Atla** düğmesi, işçilerinin, her seferinde bir satır içinde, sabit bir sırada dolaşmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-132">The **Skip** button lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="7b1c5-133">Tüm satırlar işlenene kadar, listede gereksinim duydukları kadar çok sayıda döngü de yapabilirler.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-133">They can also cycle through the list as many times as they require, until all lines have been processed.</span></span>

1. <span data-ttu-id="7b1c5-134">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-134">On the Action Pane, select **Save**.</span></span>

    <span data-ttu-id="7b1c5-135">**Çalışma satırı listesini göster** alanını *Hiçbir zaman gösterme* değeri dışında herhangi bir değere ayarlarsanız, Eylem Bölmesi'ndeki **Alan listesi** düğmesi kullanılabilir duruma gelir.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-135">If you set the **Show work line list** field to any value except *Never show*, the **Field list** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="7b1c5-136">Eylem Bölmesi'nde, **Alan listesi** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-136">On the Action Pane, select **Field list**.</span></span>
1. <span data-ttu-id="7b1c5-137">**Alan listesi** sayfasında, listedeki her satır için ambar uygulamasının gösterdiği bilgileri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-137">On the **Field list** page, configure the information that the warehouse app shows for each line in the list.</span></span>

    - <span data-ttu-id="7b1c5-138">**Birincil denetim** alanı her zaman *LineNum* olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-138">The **Primary control** field is always set to *LineNum*.</span></span> <span data-ttu-id="7b1c5-139">Bu nedenle, listedeki her satır bir satır numarasıyla başlar.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-139">Therefore, each row in the list begins with a line number.</span></span>
    - <span data-ttu-id="7b1c5-140">Gereksinim duyduğunuzda, yedi taneye kadar ek görüntüleme alanı eklemek için kalan **Görüntüleme alanı** alanlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-140">Use the remaining **Display field** fields to add up to seven additional display fields, as you require.</span></span> <span data-ttu-id="7b1c5-141">Her **Görüntüleme alanı** alanında, bir iş satırı alanının adını seçin.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-141">In each **Display field** field, select the name of a work line field.</span></span> <span data-ttu-id="7b1c5-142">Böylece her satır, o alan için bir değer gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-142">Each line will then show a value for that field.</span></span> <span data-ttu-id="7b1c5-143">Değerler, buradan seçtiğiniz sırada gösterilir.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-143">The values will be shown in the order that you select here.</span></span> <span data-ttu-id="7b1c5-144">Yedi değere ihtiyacınız yoksa, **Görüntüleme alanı** alanlarından bazılarını boş bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-144">You can leave some of the **Display field** fields blank if you don't require all seven values.</span></span>

1. <span data-ttu-id="7b1c5-145">Eylem Bölmesi'nde **Kaydet**'i seçin ve ardından **Alan listesi** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="7b1c5-145">On the Action Pane, select **Save**, and then close the **Field list** page.</span></span>

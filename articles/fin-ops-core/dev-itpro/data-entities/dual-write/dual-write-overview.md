---
title: Çift yazmaya genel bakış
description: Bu konu, Çift yazılabilir bir genel bakış içermektedir. Çift yazım, Microsoft Dynamics 365 modele dayalı uygulamalar ve Finance and Operations uygulamalar arasında yakın zamanda gerçek zamanlı etkileşim sağlayan bir altyapıdır.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 64626ebdd7fbad3d47a4b4c6bbc45bf3bc0c8277
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172796"
---
# <a name="dual-write-overview"></a><span data-ttu-id="68059-104">Çift yazmaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="68059-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="68059-105">Çift yazma nedşr?</span><span class="sxs-lookup"><span data-stu-id="68059-105">What is dual-write?</span></span>

<span data-ttu-id="68059-106">Çift yazım, Microsoft Dynamics 365 ve Finance and Operations uygulamalardaki modele dayalı uygulamalar arasında yakın zamanda gerçek zamanlı etkileşim sağlayan bir altyapıdır.</span><span class="sxs-lookup"><span data-stu-id="68059-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between model-driven apps in Microsoft Dynamics 365 and Finance and Operations apps.</span></span> <span data-ttu-id="68059-107">Müşteriler, ürünler, kişiler ve işlemlerle ilgili veriler, uygulama sınırlarının ötesinde akar, bir kuruluştaki tüm bölümler korunur.</span><span class="sxs-lookup"><span data-stu-id="68059-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="68059-108">Çift-yazma, Finance and Operations uygulamalar ve Common Data Service arasında sıkı şekilde bağlanmış, çift yönlü tümleştirme sağlar.</span><span class="sxs-lookup"><span data-stu-id="68059-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="68059-109">Finance and Operations uygulamalardaki tüm veri değişiklikleri Common Data Service'e yazmaya neden olur ve Common Data Service'deki tüm veri değişiklikleri Finance and Operations uygulamalara yazmaya neden olur.</span><span class="sxs-lookup"><span data-stu-id="68059-109">Any data change in Finance and Operations apps causes writes to Common Data Service, and any data change in Common Data Service causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="68059-110">Bu otomatik veri akışı, uygulamalar arasında tümleşik bir kullanıcı deneyimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="68059-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![Uygulamalar arasında veri ilişkisi](media/dual-write-overview.jpg)

<span data-ttu-id="68059-112">Çift yazıış iki yönden sahiptir : *altyapı* yönü ve *uygulama* en yönü.</span><span class="sxs-lookup"><span data-stu-id="68059-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="68059-113">Altyapı</span><span class="sxs-lookup"><span data-stu-id="68059-113">Infrastructure</span></span>

<span data-ttu-id="68059-114">Çift-yazılır altyapı genişletilebilir ve güvenilirdir ve aşağıdaki önemli özellikleri içerir:</span><span class="sxs-lookup"><span data-stu-id="68059-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="68059-115">Uygulamalar arasında eşzamanlı ve çift yönlü veri akışı</span><span class="sxs-lookup"><span data-stu-id="68059-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="68059-116">Çevrimiçi ve çevrimdışı/zaman uyumsuz modlar sistemi destekleyecek şekilde yürütme, duraklatma ve yakalama modlarıyla birlikte eşitleme.</span><span class="sxs-lookup"><span data-stu-id="68059-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="68059-117">Uygulamalar arasında ilk verileri eşitleme yeteneği</span><span class="sxs-lookup"><span data-stu-id="68059-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="68059-118">Veri yöneticileri için etkinliğin birleştirilmiş görünümü ve hata günlükleri</span><span class="sxs-lookup"><span data-stu-id="68059-118">Consolidated view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="68059-119">Özel uyarıları ve eşikleri konfigüre etme ve bildirimlere abone olma yeteneği</span><span class="sxs-lookup"><span data-stu-id="68059-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="68059-120">Filtreleme ve dönüşümler için sezgisel kullanıcı arabirimi (UI)</span><span class="sxs-lookup"><span data-stu-id="68059-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="68059-121">Varlık bağımlılıklarını ve ilişkilerini ayarlama ve görüntüleme yeteneği</span><span class="sxs-lookup"><span data-stu-id="68059-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="68059-122">Standart ve özel varlıklar ve haritalar için genişletilebilirlik</span><span class="sxs-lookup"><span data-stu-id="68059-122">Extensibility for both standard and custom entities and maps</span></span>
+ <span data-ttu-id="68059-123">Güvenilir uygulama yaşam döngüsü yönetimi</span><span class="sxs-lookup"><span data-stu-id="68059-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="68059-124">Yeni müşteriler için kutulu kurulum deneyimi</span><span class="sxs-lookup"><span data-stu-id="68059-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="68059-125">Uygulama</span><span class="sxs-lookup"><span data-stu-id="68059-125">Application</span></span>

<span data-ttu-id="68059-126">Çift-yazıma, Dynamics 365'te bulunan model kullanımlı uygulamalardaki Finance and Operations uygulama ve kavramlar arasında bir eşleme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="68059-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="68059-127">Bu tümleştirme aşağıdaki senaryoları destekler:</span><span class="sxs-lookup"><span data-stu-id="68059-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="68059-128">Tümleşik müşteri aslı</span><span class="sxs-lookup"><span data-stu-id="68059-128">Integrated customer master</span></span>
+ <span data-ttu-id="68059-129">Müşteri bağlılık programı kartlarına ve ödül noktalarına erişim</span><span class="sxs-lookup"><span data-stu-id="68059-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="68059-130">Birleşik ürün uzmanlaşma deneyimi</span><span class="sxs-lookup"><span data-stu-id="68059-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="68059-131">Organizasyon hiyerarşisi farkındalığı</span><span class="sxs-lookup"><span data-stu-id="68059-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="68059-132">Tümleşik satıcı aslı</span><span class="sxs-lookup"><span data-stu-id="68059-132">Integrated vendor master</span></span>
+ <span data-ttu-id="68059-133">Finans ve vergi referans verilerine erişim</span><span class="sxs-lookup"><span data-stu-id="68059-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="68059-134">İsteğe bağlı fiyat altyapısı deneyimi</span><span class="sxs-lookup"><span data-stu-id="68059-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="68059-135">Tümleşik aday müşteri-nakit deneyimi</span><span class="sxs-lookup"><span data-stu-id="68059-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="68059-136">Alan aracıları aracılığıyla hem şirket içi kıymetler hem de müşteri varlıklarını kullanabilme olanağı</span><span class="sxs-lookup"><span data-stu-id="68059-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="68059-137">Entegre temin-ödeme deneyimi</span><span class="sxs-lookup"><span data-stu-id="68059-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="68059-138">Müşteri verileri ve belgeleri ile ilgili tümleşik etkinlikler ve notlar</span><span class="sxs-lookup"><span data-stu-id="68059-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="68059-139">Eldeki stok kullanılabilirliğini ve ayrıntılarını arama yeteneği</span><span class="sxs-lookup"><span data-stu-id="68059-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="68059-140">Proje-nakit deneyimi</span><span class="sxs-lookup"><span data-stu-id="68059-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="68059-141">Parti kavramıyla birden çok adres ve rolü işleyebilme yeteneği</span><span class="sxs-lookup"><span data-stu-id="68059-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="68059-142">Kullanıcılar için tek kaynak yönetimi</span><span class="sxs-lookup"><span data-stu-id="68059-142">Single source management for users</span></span>
+ <span data-ttu-id="68059-143">Perakendecilik ve pazarlama için tümleşik kanallar</span><span class="sxs-lookup"><span data-stu-id="68059-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="68059-144">Promosyonlar ve indirimler ile görünürlük</span><span class="sxs-lookup"><span data-stu-id="68059-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="68059-145">Servis isteği işlevleri</span><span class="sxs-lookup"><span data-stu-id="68059-145">Request-for-service functions</span></span>
+ <span data-ttu-id="68059-146">Kolaylaştırılmış servis işlemleri</span><span class="sxs-lookup"><span data-stu-id="68059-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="68059-147">Çift-yazma kullanmanın başlıca nedenleri</span><span class="sxs-lookup"><span data-stu-id="68059-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="68059-148">Çift-yazılır, Microsoft Dynamics 365 uygulama arasında veri tümleştirmesi sağlar.</span><span class="sxs-lookup"><span data-stu-id="68059-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="68059-149">Bu güçlü çerçeve, ortamları birbirine bağlar ve farklı iş uygulamalarının birlikte çalışmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="68059-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="68059-150">Çift-yazmayı kullanmanız gereken başlıca nedenler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="68059-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="68059-151">Çift-yazılır, Dynamics 365'deki modele dayalı uygulamalar ve Finance and Operations uygulamaları arasında sıkı şekilde bağlanmış, yakın zamanda ve çift yönlü bütünleştirme sağlar.</span><span class="sxs-lookup"><span data-stu-id="68059-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="68059-152">Bu bütünleşme, Microsoft Dynamics 365 tüm iş çözümleri için tek durduran mağaza yapar.</span><span class="sxs-lookup"><span data-stu-id="68059-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="68059-153">Müşteri İlişkileri Yönetimi (CRM) için Microsoft dışı çözümler kullanan ancak Dynamics 365 Finance ve Dynamics 365 Supply Chain Management kullanan müşteriler çift yaz desteği için Dynamics 365'e doğru hareket ettirillerdir.</span><span class="sxs-lookup"><span data-stu-id="68059-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="68059-154">Müşteriler, ürünler, operasyonlar, projeler ve bunların Internet bilgileri (IoT), otomatik olarak çift-yazılabilir olarak Common Data Service'e akar.</span><span class="sxs-lookup"><span data-stu-id="68059-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Common Data Service through dual-write.</span></span> <span data-ttu-id="68059-155">Bu bağlantı, Microsoft Power Platform uzantıları ile ilgilenen işletmeler için çok yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="68059-155">This connection is very useful for businesses that are interested in Microsoft Power Platform expansions.</span></span>
+ <span data-ttu-id="68059-156">Çift-yazılır altyapı, No-Code/Low-Code ilkesini izler.</span><span class="sxs-lookup"><span data-stu-id="68059-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="68059-157">Standart tablo-tablo eşlemelerini genişletmek ve özel eşlemeler eklemek için minimal mühendislik çaba gereklidir.</span><span class="sxs-lookup"><span data-stu-id="68059-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="68059-158">Çift yazım, hem çevrimiçi modu, hem de çevrimdışı modu destekler.</span><span class="sxs-lookup"><span data-stu-id="68059-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="68059-159">Microsoft, çevrimiçi ve çevrimdışı modlar için destek sunan tek şirkettir.</span><span class="sxs-lookup"><span data-stu-id="68059-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a><span data-ttu-id="68059-160">CRM ürünlerinin kullanıcıları ve mimarları için çift-yazılır ortalama nedir?</span><span class="sxs-lookup"><span data-stu-id="68059-160">What does dual-write mean for users and architects of CRM products?</span></span>

<span data-ttu-id="68059-161">Çift-yazılır Finance and Operations uygulamaları ve Common Data Service arasında veri akışını otomatikleştirir.</span><span class="sxs-lookup"><span data-stu-id="68059-161">Dual-write automates the data flow between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="68059-162">Gelecek sürümlerde, Dynamics 365 model temelli uygulamalardaki kavramlar (örneğin, müşteri, ilgili kişi, teklif, ve sipariş), orta ölçekli ve büyük ölçekli pazar müşterilerine göre ölçeklenir.</span><span class="sxs-lookup"><span data-stu-id="68059-162">In future releases, concepts in model-driven apps in Dynamics 365 (for example, customer, contact, quotation, and order) will be scaled to mid-market and upper-mid-market customers.</span></span>

<span data-ttu-id="68059-163">İlk sürümde, otomasyonun çoğu çift-yazılır çözümler tarafından işlenir.</span><span class="sxs-lookup"><span data-stu-id="68059-163">In the first release, most of the automation is handled by dual-write solutions.</span></span> <span data-ttu-id="68059-164">Gelecek sürümlerde, bu çözümler bir Common Data Service parçası olacak.</span><span class="sxs-lookup"><span data-stu-id="68059-164">In future releases, those solutions will become part of Common Data Service.</span></span> <span data-ttu-id="68059-165">Yaklaşan değişikliklerini anlayarak, kendi Common Data Service çalışmalarınızı uzun vadeye kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="68059-165">By understanding the upcoming changes to Common Data Service, you can save yourself effort in the long term.</span></span> <span data-ttu-id="68059-166">Önemli değişikliklerden bazıları şunlardır:</span><span class="sxs-lookup"><span data-stu-id="68059-166">Here are some of the crucial changes:</span></span>

+ <span data-ttu-id="68059-167">Common Data Service şirket ve parti gibi yeni kavramlar olacaktır.</span><span class="sxs-lookup"><span data-stu-id="68059-167">Common Data Service will have new concepts, such as company and party.</span></span> <span data-ttu-id="68059-168">Bu kavramlar Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service ve Dynamics 365 Field Service gibi Common Data Service'e yerleşik tüm uygulamaları etkiler.</span><span class="sxs-lookup"><span data-stu-id="68059-168">These concepts will affect all apps that are built on Common Data Service, such as Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service.</span></span>
+ <span data-ttu-id="68059-169">Aktiviteler ve notlar, C1S (sistemin kullanıcılarını) ve C2s (sistemin müşterileri) desteklenmesi için birleştirilmiş ve genişletilmiştir.</span><span class="sxs-lookup"><span data-stu-id="68059-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>
+ <span data-ttu-id="68059-170">Common Data Service'teki yaklaşan değişikliklerden bazıları şunlardır:</span><span class="sxs-lookup"><span data-stu-id="68059-170">Here are some of the upcoming changes in Common Data Service:</span></span>

    - <span data-ttu-id="68059-171">Ondalık veri türü, para veri türünün yerini alacaktır.</span><span class="sxs-lookup"><span data-stu-id="68059-171">The decimal data type will replace the money data type.</span></span>
    - <span data-ttu-id="68059-172">Tarih etkililiği, aynı yerde geçmiş, şimdiki ve gelecekteki verileri destekleyecaktır.</span><span class="sxs-lookup"><span data-stu-id="68059-172">Date effectivity will support past, present, and future data in the same place.</span></span>
    - <span data-ttu-id="68059-173">Para birimi ve Döviz Kurları için daha fazla destek ve **Döviz Kuru** uygulama programlama arabirimi (API) gözden geçirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="68059-173">There will be more support for currency and exchange rates, and the **Exchange Rate** application programming interface (API) will be revised.</span></span>
    - <span data-ttu-id="68059-174">Birim dönüştürmeleri destekedilecek.</span><span class="sxs-lookup"><span data-stu-id="68059-174">Unit conversions will be supported.</span></span>

<span data-ttu-id="68059-175">Yaklaşan değişiklikler hakkında daha fazla bilgi için, [Common Data Service'deki veriler: aşama 1 ve 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1)'ye bakın.</span><span class="sxs-lookup"><span data-stu-id="68059-175">For more information about upcoming changes, see [Data in Common Data Service – phase 1 & 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1).</span></span>

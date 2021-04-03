---
title: Çift yazmaya genel bakış
description: Bu konuda, müşteri etkileşimi uygulamaları ile Finance and Operations uygulamaları arasında gerçek zamanlıya yakın etkileşim sağlayan çift yazma özelliğine dair genel bir bakış sunulur.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6cc02b483a2975dd3be28032ea7e90b540945492
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561290"
---
# <a name="dual-write-overview"></a><span data-ttu-id="c9598-103">Çift yazmaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="c9598-103">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="c9598-104">Çift yazma nedşr?</span><span class="sxs-lookup"><span data-stu-id="c9598-104">What is dual-write?</span></span>

<span data-ttu-id="c9598-105">Çift yazma, müşteri etkileşimi uygulamaları ile Finance and Operations uygulamaları arasında gerçek zamanlıya yakın etkileşim sağlayan hazır bir altyapıdır.</span><span class="sxs-lookup"><span data-stu-id="c9598-105">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between customer engagement apps and Finance and Operations apps.</span></span> <span data-ttu-id="c9598-106">Müşteriler, ürünler, kişiler ve işlemlerle ilgili veriler, uygulama sınırlarının ötesinde akar, bir kuruluştaki tüm bölümler korunur.</span><span class="sxs-lookup"><span data-stu-id="c9598-106">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="c9598-107">Çift-yazma, Finance and Operations uygulamalar ve Dataverse arasında sıkı şekilde bağlanmış, çift yönlü tümleştirme sağlar.</span><span class="sxs-lookup"><span data-stu-id="c9598-107">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="c9598-108">Finance and Operations uygulamalardaki tüm veri değişiklikleri Dataverse'e yazmaya neden olur ve Dataverse'deki tüm veri değişiklikleri Finance and Operations uygulamalara yazmaya neden olur.</span><span class="sxs-lookup"><span data-stu-id="c9598-108">Any data change in Finance and Operations apps causes writes to Dataverse, and any data change in Dataverse causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="c9598-109">Bu otomatik veri akışı, uygulamalar arasında tümleşik bir kullanıcı deneyimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="c9598-109">This automated data flow provides an integrated user experience across the apps.</span></span>

![Uygulamalar arasında veri ilişkisi](media/dual-write-overview.jpg)

<span data-ttu-id="c9598-111">Çift yazıış iki yönden sahiptir : *altyapı* yönü ve *uygulama* en yönü.</span><span class="sxs-lookup"><span data-stu-id="c9598-111">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="c9598-112">Altyapı</span><span class="sxs-lookup"><span data-stu-id="c9598-112">Infrastructure</span></span>

<span data-ttu-id="c9598-113">Çift-yazılır altyapı genişletilebilir ve güvenilirdir ve aşağıdaki önemli özellikleri içerir:</span><span class="sxs-lookup"><span data-stu-id="c9598-113">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="c9598-114">Uygulamalar arasında eşzamanlı ve çift yönlü veri akışı</span><span class="sxs-lookup"><span data-stu-id="c9598-114">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="c9598-115">Çevrimiçi ve çevrimdışı/zaman uyumsuz modlar sistemi destekleyecek şekilde yürütme, duraklatma ve yakalama modlarıyla birlikte eşitleme.</span><span class="sxs-lookup"><span data-stu-id="c9598-115">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="c9598-116">Uygulamalar arasında ilk verileri eşitleme yeteneği</span><span class="sxs-lookup"><span data-stu-id="c9598-116">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="c9598-117">Veri yöneticileri için etkinliğin birleşmiş görünümü ve hata günlükleri</span><span class="sxs-lookup"><span data-stu-id="c9598-117">Combined view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="c9598-118">Özel uyarıları ve eşikleri konfigüre etme ve bildirimlere abone olma yeteneği</span><span class="sxs-lookup"><span data-stu-id="c9598-118">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="c9598-119">Filtreleme ve dönüşümler için sezgisel kullanıcı arabirimi (UI)</span><span class="sxs-lookup"><span data-stu-id="c9598-119">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="c9598-120">Tablo bağımlılıklarını ve ilişkilerini ayarlama ve görüntüleme yeteneği</span><span class="sxs-lookup"><span data-stu-id="c9598-120">Ability to set and view table dependencies and relationships</span></span>
+ <span data-ttu-id="c9598-121">Standart ve özel tablolar ve haritalar için genişletilebilirlik</span><span class="sxs-lookup"><span data-stu-id="c9598-121">Extensibility for both standard and custom tables and maps</span></span>
+ <span data-ttu-id="c9598-122">Güvenilir uygulama yaşam döngüsü yönetimi</span><span class="sxs-lookup"><span data-stu-id="c9598-122">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="c9598-123">Yeni müşteriler için kutulu kurulum deneyimi</span><span class="sxs-lookup"><span data-stu-id="c9598-123">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="c9598-124">Uygulama</span><span class="sxs-lookup"><span data-stu-id="c9598-124">Application</span></span>

<span data-ttu-id="c9598-125">Çift-yazma, Finance and Operations uygulamalarında bulunan kavramlar ile müşteri etkileşimi uygulamalarındaki kavramlar arasında bir eşleme oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c9598-125">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in customer engagement apps.</span></span> <span data-ttu-id="c9598-126">Bu tümleştirme aşağıdaki senaryoları destekler:</span><span class="sxs-lookup"><span data-stu-id="c9598-126">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="c9598-127">Tümleşik müşteri aslı</span><span class="sxs-lookup"><span data-stu-id="c9598-127">Integrated customer master</span></span>
+ <span data-ttu-id="c9598-128">Müşteri bağlılık programı kartlarına ve ödül noktalarına erişim</span><span class="sxs-lookup"><span data-stu-id="c9598-128">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="c9598-129">Birleşik ürün uzmanlaşma deneyimi</span><span class="sxs-lookup"><span data-stu-id="c9598-129">Unified product mastering experience</span></span>
+ <span data-ttu-id="c9598-130">Organizasyon hiyerarşisi farkındalığı</span><span class="sxs-lookup"><span data-stu-id="c9598-130">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="c9598-131">Tümleşik satıcı aslı</span><span class="sxs-lookup"><span data-stu-id="c9598-131">Integrated vendor master</span></span>
+ <span data-ttu-id="c9598-132">Finans ve vergi referans verilerine erişim</span><span class="sxs-lookup"><span data-stu-id="c9598-132">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="c9598-133">İsteğe bağlı fiyat altyapısı deneyimi</span><span class="sxs-lookup"><span data-stu-id="c9598-133">On-demand price engine experience</span></span>
+ <span data-ttu-id="c9598-134">Tümleşik aday müşteri-nakit deneyimi</span><span class="sxs-lookup"><span data-stu-id="c9598-134">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="c9598-135">Alan aracıları aracılığıyla hem şirket içi kıymetler hem de müşteri varlıklarını kullanabilme olanağı</span><span class="sxs-lookup"><span data-stu-id="c9598-135">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="c9598-136">Entegre temin-ödeme deneyimi</span><span class="sxs-lookup"><span data-stu-id="c9598-136">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="c9598-137">Müşteri verileri ve belgeleri ile ilgili tümleşik etkinlikler ve notlar</span><span class="sxs-lookup"><span data-stu-id="c9598-137">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="c9598-138">Eldeki stok kullanılabilirliğini ve ayrıntılarını arama yeteneği</span><span class="sxs-lookup"><span data-stu-id="c9598-138">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="c9598-139">Proje-nakit deneyimi</span><span class="sxs-lookup"><span data-stu-id="c9598-139">Project-to-cash experience</span></span>
+ <span data-ttu-id="c9598-140">Parti kavramıyla birden çok adres ve rolü işleyebilme yeteneği</span><span class="sxs-lookup"><span data-stu-id="c9598-140">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="c9598-141">Kullanıcılar için tek kaynak yönetimi</span><span class="sxs-lookup"><span data-stu-id="c9598-141">Single source management for users</span></span>
+ <span data-ttu-id="c9598-142">Perakendecilik ve pazarlama için tümleşik kanallar</span><span class="sxs-lookup"><span data-stu-id="c9598-142">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="c9598-143">Promosyonlar ve indirimler ile görünürlük</span><span class="sxs-lookup"><span data-stu-id="c9598-143">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="c9598-144">Servis isteği işlevleri</span><span class="sxs-lookup"><span data-stu-id="c9598-144">Request-for-service functions</span></span>
+ <span data-ttu-id="c9598-145">Kolaylaştırılmış servis işlemleri</span><span class="sxs-lookup"><span data-stu-id="c9598-145">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="c9598-146">Çift-yazma kullanmanın başlıca nedenleri</span><span class="sxs-lookup"><span data-stu-id="c9598-146">Top reasons to use dual-write</span></span>

<span data-ttu-id="c9598-147">Çift-yazılır, Microsoft Dynamics 365 uygulama arasında veri tümleştirmesi sağlar.</span><span class="sxs-lookup"><span data-stu-id="c9598-147">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="c9598-148">Bu güçlü çerçeve, ortamları birbirine bağlar ve farklı iş uygulamalarının birlikte çalışmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="c9598-148">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="c9598-149">Çift-yazmayı kullanmanız gereken başlıca nedenler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c9598-149">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="c9598-150">Çift-yazılır, Dynamics 365'deki modele dayalı uygulamalar ve Finance and Operations uygulamaları arasında sıkı şekilde bağlanmış, yakın zamanda ve çift yönlü bütünleştirme sağlar.</span><span class="sxs-lookup"><span data-stu-id="c9598-150">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="c9598-151">Bu bütünleşme, Microsoft Dynamics 365 tüm iş çözümleri için tek durduran mağaza yapar.</span><span class="sxs-lookup"><span data-stu-id="c9598-151">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="c9598-152">Müşteri İlişkileri Yönetimi (CRM) için Microsoft dışı çözümler kullanan ancak Dynamics 365 Finance ve Dynamics 365 Supply Chain Management kullanan müşteriler çift yaz desteği için Dynamics 365'e doğru hareket ettirillerdir.</span><span class="sxs-lookup"><span data-stu-id="c9598-152">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="c9598-153">Müşteriler, ürünler, operasyonlar, projeler ve bunların Internet bilgileri (IoT), otomatik olarak çift-yazılabilir olarak Dataverse'e akar.</span><span class="sxs-lookup"><span data-stu-id="c9598-153">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Dataverse through dual-write.</span></span> <span data-ttu-id="c9598-154">Bu bağlantı, Power Platform uzantıları ile ilgilenen işletmeler için yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="c9598-154">This connection is useful for businesses that are interested in Power Platform expansions.</span></span>
+ <span data-ttu-id="c9598-155">Çift-yazılır altyapı, No-Code/Low-Code ilkesini izler.</span><span class="sxs-lookup"><span data-stu-id="c9598-155">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="c9598-156">Standart tablo-tablo eşlemelerini genişletmek ve özel eşlemeler eklemek için minimal mühendislik çaba gereklidir.</span><span class="sxs-lookup"><span data-stu-id="c9598-156">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="c9598-157">Çift yazım, hem çevrimiçi modu, hem de çevrimdışı modu destekler.</span><span class="sxs-lookup"><span data-stu-id="c9598-157">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="c9598-158">Microsoft, çevrimiçi ve çevrimdışı modlar için destek sunan tek şirkettir.</span><span class="sxs-lookup"><span data-stu-id="c9598-158">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a><span data-ttu-id="c9598-159">Müşteri etkileşimi uygulamalarının geliştiricileri ve mimarları için çift yazma ortalaması nedir?</span><span class="sxs-lookup"><span data-stu-id="c9598-159">What does dual-write mean for developers and architects of customer engagement apps?</span></span>

<span data-ttu-id="c9598-160">Çift-yazma Finance and Operations uygulamaları ve müşteri etkileşimi uygulamaları arasında veri akışını otomatikleştirir.</span><span class="sxs-lookup"><span data-stu-id="c9598-160">Dual-write automates the data flow between Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="c9598-161">Çift yazma, Dataverse üzerine yüklenen iki AppSource çözümünden oluşur.</span><span class="sxs-lookup"><span data-stu-id="c9598-161">Dual-write consists of two AppSource solutions that are installed on Dataverse.</span></span> <span data-ttu-id="c9598-162">Çözümler, ERP boyutuna ölçeklendirilebilecek şekilde, Dataverse üzerindeki tablo şemasını, eklentileri ve iş akışlarını genişletir.</span><span class="sxs-lookup"><span data-stu-id="c9598-162">The solutions expand the table schema, plugins, and workflows on Dataverse so that they can scale to ERP size.</span></span> <span data-ttu-id="c9598-163">Başarılı bir uygulama için, müşteri etkileşimi uygulamalarının geliştiricileri ve mimarları bu değişiklikleri anlayıp Finance and Operations uygulamalarındaki meslektaşlarıyla birlikte çalışmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c9598-163">For a successful implementation, developers and architects of customer engagement apps must understand these changes and collaborate with their counterparts on Finance and Operations apps.</span></span>

<span data-ttu-id="c9598-164">Finance and Operations uygulamalarla eşitlik oluşturmak için çift yazma, Dataverse şemasında bazı önemli değişiklikler yapar.</span><span class="sxs-lookup"><span data-stu-id="c9598-164">To create parity with Finance and Operations applications, dual-write makes some crucial changes in the Dataverse schema.</span></span> <span data-ttu-id="c9598-165">Planı anladığınızda, gelecekte tasarım ve geliştirme üzerinde yeniden çalışma yapmaktan kaçınabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c9598-165">If you understand the plan, you can avoid some design and development rework in the future.</span></span>

+ <span data-ttu-id="c9598-166">Çift yazma AppSource paketi yüklendiğinde, Dataverse uygulamasında şirket ve taraf gibi yeni kavramlar bulunacaktır.</span><span class="sxs-lookup"><span data-stu-id="c9598-166">When the dual-write AppSource package is installed, Dataverse will have new concepts such as company and party.</span></span> <span data-ttu-id="c9598-167">Bu kavramlar, Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service ve Dynamics 365 Field Service uygulamalarının dahil olduğu Dataverse üzerine inşa edilen uygulamaların sorunsuz bir şekilde Finance and Operations uygulamaları ile etkileşimde bulunmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="c9598-167">These concepts help applications built on Dataverse, including Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service, to interact seamlessly with Finance and Operations apps.</span></span>

+ <span data-ttu-id="c9598-168">Aktiviteler ve notlar, C1S (sistemin kullanıcılarını) ve C2s (sistemin müşterileri) desteklenmesi için birleştirilmiş ve genişletilmiştir.</span><span class="sxs-lookup"><span data-stu-id="c9598-168">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>

+ <span data-ttu-id="c9598-169">Finance and Operations uygulamaları ile Dataverse arasında yapılan para birimi iletimi sırasında veri kaybını önlemek için, müşteri etkileşimi uygulamalarının para birimi veri türünde ondalık basamak sayısını genişletebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c9598-169">To prevent data loss during currency transmission between Finance and Operations apps and the Dataverse, you'll be able to extend the number of decimal places in the currency data type of customers engagement apps.</span></span> <span data-ttu-id="c9598-170">Özellik, var olan satırları meta veri katmanındaki yeni genişletilmiş duruma otomatik olarak çevirir.</span><span class="sxs-lookup"><span data-stu-id="c9598-170">The feature autotranslates existing rows to the new extended state at the metadata layer.</span></span> <span data-ttu-id="c9598-171">Bu işlem sırasında para birimi değeri para verileri yerine ondalık verilere çevrilir ve para birimi değeri 10 basamaklı ondalık değeri destekler.</span><span class="sxs-lookup"><span data-stu-id="c9598-171">During this process, the currency value is translated to decimal data rather than money data, and the currency value supports 10 decimal places.</span></span> <span data-ttu-id="c9598-172">Bu özellik tercihe bağlıdır ve 4 basamaktan fazla ondalık değere ihtiyaç duymayan kuruluşların tercih etmesine gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="c9598-172">This feature is opt-in, and organizations that don't need more than 4 decimal places of precision do not need to opt in.</span></span> <span data-ttu-id="c9598-173">Daha fazla bilgi için, bkz. [Çift yazma için para birimi veri türü taşıma](currrency-decimal-places.md).</span><span class="sxs-lookup"><span data-stu-id="c9598-173">For more information, see [Currency data-type migration for dual-write](currrency-decimal-places.md).</span></span>

+ <span data-ttu-id="c9598-174">[Tarih etkililiği](../../dev-tools/date-effectivity.md) Dataverse uygulamasına eklenecektir.</span><span class="sxs-lookup"><span data-stu-id="c9598-174">[Date effectivity](../../dev-tools/date-effectivity.md) will be added to Dataverse.</span></span> <span data-ttu-id="c9598-175">Aynı tablo üzerinde geçmiş, şimdiki ve gelecekteki verileri destekleyecektir.</span><span class="sxs-lookup"><span data-stu-id="c9598-175">It will support past, present, and future data on the same table.</span></span>

+ <span data-ttu-id="c9598-176">Ürün [birimi dönüştürmeleri](../../../../supply-chain/pim/tasks/manage-unit-measure.md) ürünler, teklifler, siparişler ve faturalar için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="c9598-176">Product [unit conversions](../../../../supply-chain/pim/tasks/manage-unit-measure.md) are supported for products, quotes, orders, and invoices.</span></span>

<span data-ttu-id="c9598-177">Gelecekteki değişiklikler hakkında daha fazla bilgi için, bkz. [Çift yazmadaki yenilikler veya değişiklikler](whats-new-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="c9598-177">For more information about upcoming changes, see [What's new or changed in dual-write](whats-new-dual-write.md).</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
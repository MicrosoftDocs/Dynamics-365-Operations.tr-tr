---
title: Şirket içi ortamlar için donanım boyutlandırma gereksinimleri
description: Şirket içi ortamlar için donanım boyutlandırma gereksinimleri
author: kfend
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 65f21d71c22d295902b968e6c18134e1577e01f2
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812569"
---
# <a name="hardware-sizing-requirements-for-on-premises-environments"></a><span data-ttu-id="ac2f1-103">Şirket içi ortamlar için donanım boyutlandırma gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="ac2f1-103">Hardware sizing requirements for on-premises environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac2f1-104">Şirket içi ortam için donanım ve altyapı boyutlandırmaya başlamadan önce, [Bulut dağıtımları için sistem gereksinimleri](system-requirements.md) ve [Kurulum ve dağıtım yönergeleri](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md) belgelerini okuyun ve altyapı hakkında derinlikli bilgi sahibi olun.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-104">Before you begin the hardware and infrastructure sizing process for an on-premises environment, familiarize yourself with the [System requirements for cloud deployments](system-requirements.md) and [Setup and deployment instructions](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md) to gain a solid understanding off the underlying infrastructure.</span></span>

> [!NOTE]
> <span data-ttu-id="ac2f1-105">Optimum performans için sistem en iyi uygulamalarına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-105">Pay close attention to the system setup best practices for optimum performance.</span></span>

<span data-ttu-id="ac2f1-106">Belgeyi gözden geçirdikten sonra, hareket ve eş zamanlı kullanıcı hacminizi tahmin edebilir ve ortalama çekirdek çıkışına dayanarak ortamınızı boyutlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-106">After you have reviewed the documentation, you can start the process of estimating your transactional and concurrent user volume and sizing your environment based on the average core throughput.</span></span>

## <a name="factors-that-affect-sizing"></a><span data-ttu-id="ac2f1-107">Boyutlandırmayı etkileyen faktörler</span><span class="sxs-lookup"><span data-stu-id="ac2f1-107">Factors that affect sizing</span></span>

<span data-ttu-id="ac2f1-108">Aşağıdaki görselde gösterilen tüm faktörler boyutlandırmaya katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-108">All the factors shown in the following illustration contribute to sizing.</span></span> <span data-ttu-id="ac2f1-109">Daha ayrıntılı bilgi toplandıkça boyutlandırmayı daha hassas şekilde belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-109">The more detailed information that is collected, the more precisely you can determine sizing.</span></span> <span data-ttu-id="ac2f1-110">Destekleyici veri olmadan donanım boyutlandırmanın tutarlı olması olası değildir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-110">Hardware sizing, without supporting data, is likely to be inaccurate.</span></span> <span data-ttu-id="ac2f1-111">Gerekli veri için minimum gereksinim saat başına hareket hat yükünün tepe noktasıdır.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-111">The absolute minimum requirement for necessary data is the peak transaction line load per hour.</span></span>

<span data-ttu-id="ac2f1-112">[![Şirket içi ortamlar için donanım boyutlandırma](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</span><span class="sxs-lookup"><span data-stu-id="ac2f1-112">[![Hardware sizing for on-premises environments](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</span></span>

<span data-ttu-id="ac2f1-113">Soldan sağa bakıldığında, boyutlandırmayı doğru şekilde tahmin etmek için ilk ve en önemli faktör bir hareket profili veya hareket nitelendirmedir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-113">Viewed from left to right, the first and most important factor needed to accurately estimate sizing is a transaction profile or a transaction characterization.</span></span> <span data-ttu-id="ac2f1-114">Saat başına tepe hareket hacmini her zaman bulmak önemlidir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-114">It's important to always find the peak transactional volume per hour.</span></span> <span data-ttu-id="ac2f1-115">Birden fazla tepe dönemi varsa, bu dönemlerin doğru olarak tanımlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-115">If there are multiple peak periods, then these periods need to be accurately defined.</span></span>

<span data-ttu-id="ac2f1-116">Yüküm altyapınızı nasıl etkilediğini anladığınızda, bu faktörler hakkında daha fazla ayrıntıyı anlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="ac2f1-116">As you understand the load that impacts your infrastructure, you also need to understand more detail about these factors:</span></span>

- <span data-ttu-id="ac2f1-117">**Hareketler** – Hareketlerin genellikle gün/hafta boyunca çeşitli tepe noktaları vardır.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-117">**Transactions** – Typically transactions have certain peaks throughout the day/week.</span></span> <span data-ttu-id="ac2f1-118">Bu genellikle hareket türüne bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-118">This mostly depends on the transaction type.</span></span> <span data-ttu-id="ac2f1-119">Zaman ve gider girişleri genellikle haftada bir tepe noktası gösterirlerken Satış siparişi girişleri gün içerisinde tümleştirme veya trickle yolu ile gelirler.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-119">Time and expense entries usually show peaks once per week, whereas Sales order entries often come in bulk via integration or trickle in during the day.</span></span>
- <span data-ttu-id="ac2f1-120">**Eş zamanlı kullanıcıların sayısı** – Eş zamanlı kullanıcıların sayısı ikinci en önemli boyutlandırma faktörüdür.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-120">**Number of concurrent users** – The number of concurrent users is the second most important sizing factor.</span></span> <span data-ttu-id="ac2f1-121">Eş zamanlı kullanıcıların sayısına dayanarak güvenilir boyutlandırma elde edemezsiniz, bu yüzden de kullanabileceğiniz tek veri buysa, bir yaklaşık sayı tahmin edin ve bunu daha fazla veriniz olduğunda elden geçirin.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-121">You cannot reliably get sizing estimates based on the number of concurrent users, so if this is the only data you have available, estimate an approximate number, and then revisit this when you have more data.</span></span> <span data-ttu-id="ac2f1-122">Doğru bir eş zamanlı kullanıcı tanımı şu anlama gelir:</span><span class="sxs-lookup"><span data-stu-id="ac2f1-122">An accurate concurrent user definition means that:</span></span>

    - <span data-ttu-id="ac2f1-123">Adlandırılmış kullanıcılar eşzamanlı kullanıcı değildir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-123">Named users are not concurrent users.</span></span>
    - <span data-ttu-id="ac2f1-124">Eş zamanlı kullanıcılar adlandırılmış kullanıcıların her zaman bir alt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-124">Concurrent users are always a subset of named users.</span></span> 
    - <span data-ttu-id="ac2f1-125">Tepe iş yükleri boyutlandırma için maksimum eş zamanlılığı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-125">Peak workload defines the maximum concurrency for sizing.</span></span>

    <span data-ttu-id="ac2f1-126">Eş zamanlı kullanıcılar için ölçüt, kullanıcının aşağıdaki ölçütlerin tümüne uymasıdır:</span><span class="sxs-lookup"><span data-stu-id="ac2f1-126">Criteria for concurrent users is that the user meets all the following criteria:</span></span>

    - <span data-ttu-id="ac2f1-127">Oturum açmış.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-127">Logged on.</span></span>
    - <span data-ttu-id="ac2f1-128">Sayım sırasında çalışan hareketler/sorgular.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-128">Working transactions/inquiries at the time of counting.</span></span>
    - <span data-ttu-id="ac2f1-129">Kullanılmayan bir oturum değil.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-129">Not an idle session.</span></span>

- <span data-ttu-id="ac2f1-130">**Veri bileşimi** – Bu çoğunlukla sisteminizin nasıl ayarlanıp yapılandırılacağıyla ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-130">**Data composition** – This is mostly about how your system will be set up and configured.</span></span> <span data-ttu-id="ac2f1-131">Örneğin, kaç adet tüzel kişiliğe, kaç tane maddeye, kaç tane ürün reçetesi düzeyine sahip olacaksınız ve güvenlik kurulumunuz ne kadar karmaşık olacak.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-131">For example, how many legal entities you will have, how many items, how many BOM levels, and how complex your security setup will be.</span></span> <span data-ttu-id="ac2f1-132">Bu faktörlerin her biri performansınız üzerinde küçük bir etkiye sahip olacaktır, bu yüzden de bu faktörler, altyapı sözkonusu olduğunda akıllı tercihlerde bulunarak denkleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-132">Each of those factors may have a small impact on performance, so these factors can be offset by using smart choices when it comes to infrastructure.</span></span>
- <span data-ttu-id="ac2f1-133">**Uzantılar** – Özelleştirmeler basit veya karmaşık olabilir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-133">**Extensions** – Customizations can be simple or complex.</span></span> <span data-ttu-id="ac2f1-134">Özelleştirmelerin sayısı ve karmaşıklığın doğası ve kullanımı, gerek duyulan altyapının boyutunu çeşitli şekillerde etkileyebilir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-134">The number of customizations and the nature of complexity and usage has a varied impact on the size of the infrastructure needed.</span></span> <span data-ttu-id="ac2f1-135">Örnek özelleştirmeler için, sadece verimliliği test etmekle kalmak için değil, aynı zamanda altyapı ihtiyaçlarını anlamaya yardımcı olmak için de performans değerlendirmeleri yapmak tavsiye edilir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-135">For complex customizations, it's advised to conduct performance evaluations to ensure that they are not only tested for efficiency but also help understand the infrastructure needs.</span></span> <span data-ttu-id="ac2f1-136">Uzantılar performans ve ölçeklenebilirlik için en iyi yöntemlere uygun olarak kodlanmadıysa daha da önemlidir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-136">This is even more critical when the extensions are not coded according to best practices for performance and scalability.</span></span>
- <span data-ttu-id="ac2f1-137">**Raporlama ve analizler** – Bu faktörler genellikle ağır sorguları, sistemdeki veritabanlarına karşı çalıştırmayı içerir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-137">**Reporting and analytics** – These factors typically include running heavy queries against the various databases in the system.</span></span> <span data-ttu-id="ac2f1-138">Pahalı raporların çalıştırılma sıklığını anlamak ve azaltmak, bunların etkisini daha iyi anlamanıza yardımcı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-138">Understanding and reducing the frequency when expensive reports run will help you understand the impact of them.</span></span>
- <span data-ttu-id="ac2f1-139">**Üçüncü taraf çözümler** – Bu çözümler, ISV'ler gibi, uzantılarla aynı çıkarımlara ve önerilere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-139">**Third-party solutions** – These solutions, like ISVs, have the same implications and recommendations as extensions.</span></span>

## <a name="sizing-your-environment"></a><span data-ttu-id="ac2f1-140">Ortamınızı boyutlandırma</span><span class="sxs-lookup"><span data-stu-id="ac2f1-140">Sizing your environment</span></span>

<span data-ttu-id="ac2f1-141">Boyutlandırma gereksinimlerinizi anlamak için işlemeniz gereken hareketlerin tepe hacmini bilmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-141">To understand your sizing requirements, you need to know the peak volume of transactions that you need to process.</span></span> <span data-ttu-id="ac2f1-142">Yönetim Raporlayıcısı veya SSRS gibi çoğu yedek sistem, daha az kritiktir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-142">Most auxiliary systems, like Management Reporter or SSRS, are less mission critical.</span></span> <span data-ttu-id="ac2f1-143">Bunun sonucu olarak, bu belge çoğunlukla AOS ve SQL Server'a odaklanır.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-143">As a result, this document focuses mostly on AOS and SQL Server.</span></span>

> [!NOTE]
> <span data-ttu-id="ac2f1-144">Genel olarak, hesaplama katmanları ölçeklenir ve N+1 şeklinde ayarlanmalıdır, bu da üç AOS tahmin ediyorsanız, dördüncü bir AOS eklemeniz anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-144">In general, the compute tiers scale out and should be set up in an N+1 fashion, meaning if you estimate three AOS, add a fourth AOS.</span></span> <span data-ttu-id="ac2f1-145">Veritabanı katmanı her zaman açık yüksek kullanılabilirlik kurulumunda ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-145">The database tier should be set up in an Always On highly-available setup.</span></span>

## <a name="sql-server-oltp"></a><span data-ttu-id="ac2f1-146">SQL Server (OLTP)</span><span class="sxs-lookup"><span data-stu-id="ac2f1-146">SQL Server (OLTP)</span></span>

### <a name="sizing"></a><span data-ttu-id="ac2f1-147">Boyutlandırma</span><span class="sxs-lookup"><span data-stu-id="ac2f1-147">Sizing</span></span>

- <span data-ttu-id="ac2f1-148">DB sunucusunda çekirdek başına saat başına 3K - 15K hareket satırı.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-148">3K to 15K transaction lines per hour per core on DB server.</span></span>
- <span data-ttu-id="ac2f1-149">Tipik AOS'tan SQL'e çekirdek oranı birincil SQL Server için 3:1'dir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-149">Typical AOS-to-SQL core ratio 3:1 for the primary SQL Server.</span></span> <span data-ttu-id="ac2f1-150">Ek çekirdekler, seçilen yüksek kullanılabilirlik yapılandırmasına dayalı olarak gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-150">Additional cores are required based on the chosen high availability configuration.</span></span>

    - <span data-ttu-id="ac2f1-151">Veritabanının yoğun olarak işleyen işlemlerin işlenmesi bunu 2:1'e geriletebilir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-151">Processing database-heavy operations may regress this to 2:1.</span></span>

- <span data-ttu-id="ac2f1-152">Aşağıdaki etkenler değişimleri etkiler:</span><span class="sxs-lookup"><span data-stu-id="ac2f1-152">The following factors influence variations:</span></span>

    - <span data-ttu-id="ac2f1-153">Kullanımda olan parametre ayarları.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-153">Parameter settings in use.</span></span>
    - <span data-ttu-id="ac2f1-154">Eklenti düzeyleri.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-154">Levels of extensions.</span></span>
    - <span data-ttu-id="ac2f1-155">Veritabanı günlüğü ve uyarılar gibi ek işlevlerin kullanımı.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-155">Usage of additional functionality, such as database log and alerts.</span></span> <span data-ttu-id="ac2f1-156">Ekstrem veritabanı kaydı alma saat başına çekirdek başına çıkışı 3K satır altına çekecektir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-156">Extreme database logging will further reduce throughput per hour per core below 3K lines.</span></span>
    - <span data-ttu-id="ac2f1-157">Veri bileşiminin karmaşıklığı – Basit bir hesap planına karşılık ayrıntılı bir hesap planının çıkış üzerine etkileri vardır (örnek olarak).</span><span class="sxs-lookup"><span data-stu-id="ac2f1-157">Complexity of data composition – A simple chart of accounts versus a detailed fine-grained chart of accounts has implications on throughput (as an example).</span></span>
    - <span data-ttu-id="ac2f1-158">Hareket nitelendirme.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-158">Transaction characterization.</span></span>
    - <span data-ttu-id="ac2f1-159">Her bir çekirdek için 2 GB - 16 GB arası bellek</span><span class="sxs-lookup"><span data-stu-id="ac2f1-159">2 GB to 16 GB memory for each core.</span></span>
    - <span data-ttu-id="ac2f1-160">DB sunucusu üzerinde Yönetim raporlayıcısı ve SSRS veritabanları gibi yedek veritabanları.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-160">Auxiliary databases on DB server such as Management reporter and SSRS databases.</span></span>
    - <span data-ttu-id="ac2f1-161">Temp DB = veritabanı boyutunun %15'i, fiziksel işlemciler kadar fazla sayıda dosya ile.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-161">Temp DB = 15% of DB size, with as many files as physical processors.</span></span>
    - <span data-ttu-id="ac2f1-162">SAN boyutu ve çıkış, toplam eş zamanlı hareket hacmi/kullanımına dayalıdır.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-162">SAN size and throughput based on total concurrent transaction volume/usage.</span></span>

### <a name="high-availability"></a><span data-ttu-id="ac2f1-163">Yüksek kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="ac2f1-163">High availability</span></span>

<span data-ttu-id="ac2f1-164">SQL Server'ı her zaman bir küme veya yansıtma kurulumunda kullanmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-164">We recommend always utilizing SQL Server in either a cluster or mirroring setup.</span></span> <span data-ttu-id="ac2f1-165">İkinci SQL düğümü, birincil düğüm ile aynı sayıda çekirdeğe sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-165">The second SQL node should have the same number of cores as the primary node.</span></span>

### <a name="active-directory-federation-services-ad-fs"></a><span data-ttu-id="ac2f1-166">Active Directory Federasyon Hizmetleri (AD FS)</span><span class="sxs-lookup"><span data-stu-id="ac2f1-166">Active Directory Federation Services (AD FS)</span></span>

<span data-ttu-id="ac2f1-167">AD FS boyutlandırma için bkz [AD FS Sunucu Kapasite belgeleri](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).</span><span class="sxs-lookup"><span data-stu-id="ac2f1-167">For AD FS sizing, see the [AD FS Server Capacity documentation](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).</span></span>

<span data-ttu-id="ac2f1-168">Bir [boyutlandırma elektronik tablosu](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) dağıtımınızdaki örneklerin sayısını planlamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-168">A [sizing spreadsheet](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) is available for planning the number of instances in your deployment.</span></span>

## <a name="aos-online-and-batch"></a><span data-ttu-id="ac2f1-169">AOS (Çevrimiçi ve toplu iş)</span><span class="sxs-lookup"><span data-stu-id="ac2f1-169">AOS (Online and batch)</span></span>

### <a name="sizing"></a><span data-ttu-id="ac2f1-170">Boyutlandırma</span><span class="sxs-lookup"><span data-stu-id="ac2f1-170">Sizing</span></span>

- <span data-ttu-id="ac2f1-171">Hareket hacmi/kullanıma göre boyutlandırma</span><span class="sxs-lookup"><span data-stu-id="ac2f1-171">Sizing by transaction volume/usage</span></span>

    - <span data-ttu-id="ac2f1-172">Çekirdek başına 2K - 6K satır</span><span class="sxs-lookup"><span data-stu-id="ac2f1-172">2K to 6K lines per core</span></span>
    - <span data-ttu-id="ac2f1-173">Örnek başına 16 GB</span><span class="sxs-lookup"><span data-stu-id="ac2f1-173">16 GB per instance</span></span>
    - <span data-ttu-id="ac2f1-174">Standart kutu – 4 - 24 arası çekirdek</span><span class="sxs-lookup"><span data-stu-id="ac2f1-174">Standard box – 4 to 24 cores</span></span>
    - <span data-ttu-id="ac2f1-175">Çekirdek başına 10 - 15 Kurumsal kullanıcı</span><span class="sxs-lookup"><span data-stu-id="ac2f1-175">10 to 15 Enterprise users per core</span></span>
    - <span data-ttu-id="ac2f1-176">Çekirdek başına 15 - 25 Faaliyet kullanıcısı</span><span class="sxs-lookup"><span data-stu-id="ac2f1-176">15 to 25 Activity users per core</span></span>
    - <span data-ttu-id="ac2f1-177">Çekirdek başına 25 - 50 Takım üyesi</span><span class="sxs-lookup"><span data-stu-id="ac2f1-177">25 to 50 Team members per core</span></span>

- <span data-ttu-id="ac2f1-178">Toplu İş</span><span class="sxs-lookup"><span data-stu-id="ac2f1-178">Batch</span></span>

    - <span data-ttu-id="ac2f1-179">Çekirdek başına 1 - 4 toplu iş iş parçacığı</span><span class="sxs-lookup"><span data-stu-id="ac2f1-179">1 to 4 batch threads per core</span></span>
    - <span data-ttu-id="ac2f1-180">Toplu iş pencere nitelendirmesine göre boyut</span><span class="sxs-lookup"><span data-stu-id="ac2f1-180">Size based on batch window characterization</span></span>

- <span data-ttu-id="ac2f1-181">AOS, Veri Yönetimi ve Toplu işin Service Fabric'te aynı rolde olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-181">Note that the AOS, Data Management, and Batch are on the same role in the Service Fabric.</span></span> <span data-ttu-id="ac2f1-182">Bu üç iş yükünü birleştirerek boyutlandırmanız, bunları Microsoft Dynamics AX 2012'deki gibi ayırmamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-182">You need to size for these three workloads combined, and not separate these like in Microsoft Dynamics AX 2012.</span></span>
- <span data-ttu-id="ac2f1-183">SQL Server için aynı değişkenlik faktörleri burada da geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-183">The same variability factors for SQL Server apply here.</span></span>

### <a name="high-availability"></a><span data-ttu-id="ac2f1-184">Yüksek kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="ac2f1-184">High availability</span></span>

- <span data-ttu-id="ac2f1-185">Tahmin ettiğinizden 1-2 adet daha fazla kullanılabilir AOS'e sahip olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-185">Ensure that you have at least 1 to 2 more AOS available than you estimate.</span></span>
- <span data-ttu-id="ac2f1-186">En az 3-4 sanal ana bilgisayara sahip olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-186">Ensure that you have at least 3 to 4 virtual hosts available.</span></span>

## <a name="management-reporter"></a><span data-ttu-id="ac2f1-187">Yönetim raporlayıcısı</span><span class="sxs-lookup"><span data-stu-id="ac2f1-187">Management reporter</span></span>

<span data-ttu-id="ac2f1-188">Çoğu durumunda ve yaygın olarak kullanılmadığında, iki düğümün kullanılmasıyla önerilen minimum gereksinimler iyi iş görecektir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-188">In most cases, unless used extensively, the recommended minimum requirements using two nodes should work well.</span></span> <span data-ttu-id="ac2f1-189">Yalnızca ağır kullanımınız söz konusu olduğu durumlarda ikiden fazla düğüme ihtiyaç duyarsınız.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-189">Only in cases where there is heavy use will you need more than two nodes.</span></span> <span data-ttu-id="ac2f1-190">Lütfen gerektiği şekilde ölçeklendirin.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-190">Please scale as needed.</span></span>

## <a name="sql-server-reporting-services"></a><span data-ttu-id="ac2f1-191">SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="ac2f1-191">SQL Server Reporting Services</span></span>

<span data-ttu-id="ac2f1-192">Genel kullanım sürümü için yalnızca bir SSRS düğümü dağıtılabilir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-192">For the general availability release, only one SSRS node can be deployed.</span></span> <span data-ttu-id="ac2f1-193">SSRS düğümünüzü test ederken izleyin ve SSRS tarafından kullanılabilir çekirdeklerin sayısını ihtiyaca göre artırın.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-193">Monitor your SSRS node while testing and increase the number of cores available for SSRS on a need basis.</span></span> <span data-ttu-id="ac2f1-194">Önceden yapılandırılmış bir ikincil düğümün SSRS VM'den farklı bir sanal makinede kullanılabilir olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-194">Make sure that you have a preconfigured secondary node available on a virtual host that is different than the SSRS VM.</span></span> <span data-ttu-id="ac2f1-195">Bu, SSRS'yi barındıran sanal makine veya sanal ana bilgisayarda bir sorun olursa önemlidir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-195">This is important if there is an issue with the virtual machine that hosts SSRS or the virtual host.</span></span> <span data-ttu-id="ac2f1-196">Bu durumda, bunların değiştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-196">If this the case, they would need to be replaced.</span></span>

## <a name="environment-orchestrator"></a><span data-ttu-id="ac2f1-197">Ortam Orchestrator</span><span class="sxs-lookup"><span data-stu-id="ac2f1-197">Environment Orchestrator</span></span>

<span data-ttu-id="ac2f1-198">Orchestrator hizmeti, dağıtım ve LCS ile ilgili iletişimi yöneten hizmetidir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-198">The Orchestrator service is the service that manages your deployment and the related communication with LCS.</span></span> <span data-ttu-id="ac2f1-199">Bu hizmet, birincil Service Fabric hizmeti olarak dağıtılır ve en az üç VM gerektirir.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-199">This service is deployed as the primary Service Fabric service and requires at least three VMs.</span></span> <span data-ttu-id="ac2f1-200">Bu hizmet Service Fabric düzenleme hizmeti ile birlikte yer alır.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-200">This service is co-located with the Service Fabric orchestration services.</span></span> <span data-ttu-id="ac2f1-201">Bu, kümenin tepe yük noktasına göre boyutlandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-201">This and should be sized to the peak load of the cluster.</span></span> <span data-ttu-id="ac2f1-202">Daha fazla bilgi için bkz [Service Fabric küme kapasite planlama konusunda dikkate alınacaklar](/azure/service-fabric/service-fabric-cluster-capacity).</span><span class="sxs-lookup"><span data-stu-id="ac2f1-202">For more information, see [Service Fabric cluster capacity planning considerations](/azure/service-fabric/service-fabric-cluster-capacity).</span></span>

## <a name="virtualization-and-oversubscription"></a><span data-ttu-id="ac2f1-203">Sanallaştırma ve aşırı talep</span><span class="sxs-lookup"><span data-stu-id="ac2f1-203">Virtualization and oversubscription</span></span>

<span data-ttu-id="ac2f1-204">AOS gibi pek çok kritik görev hizmetleri ayrılmış kaynaklara (çekirdekler, bellek ve disk) sahip Sanal ana bilgisayarlarda barındırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ac2f1-204">Mission critical services like the AOS should be hosted on Virtual hosts that have dedicated resources – cores, memory, and disk.</span></span>

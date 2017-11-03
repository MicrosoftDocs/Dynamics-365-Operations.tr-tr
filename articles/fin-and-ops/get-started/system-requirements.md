---
title: "Bulut dağıtımları için sistem gereksinimleri"
description: "Bu konuda Microsoft Dynamics 365 for Finance and Operations ve bulut dağıtımları için Enterprise Edition geçerli sürümü için sistem gereksinimleri belirtilmektedir."
author: sericks007
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 83637b4b2ccc01950e68569b3b8bee1a7cd69855
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="system-requirements-for-cloud-deployments"></a><span data-ttu-id="97a34-103">Bulut dağıtımları için sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="97a34-103">System requirements for cloud deployments</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="97a34-104">Bu konuda Microsoft Dynamics 365 for Finance and Operations ve bulut dağıtımları için Enterprise Edition geçerli sürümü için sistem gereksinimleri belirtilmektedir.</span><span class="sxs-lookup"><span data-stu-id="97a34-104">This topic lists the system requirements for the current version of Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, for cloud deployments.</span></span> <span data-ttu-id="97a34-105">Finance and Operations'u yüklemeden önce bu adım uygun olduğunda, çalışmakta olduğunuz sistemin minimum ağ, donanım ve yazılım gereksinimlerini karşıladığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="97a34-105">Before you install Finance and Operations, when this step is appropriate, verify that the system that you're working with meets or exceeds the minimum network, hardware, and software requirements.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="97a34-106">Desteklenen web tarayıcıları</span><span class="sxs-lookup"><span data-stu-id="97a34-106">Supported web browsers</span></span>
<span data-ttu-id="97a34-107">Web uygulamasını belirtilen işletim sistemleri üzerinde çalışan aşağıdaki web tarayıcılarından birinde çalıştırabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="97a34-107">The web application can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="97a34-108">Windows 10 üzerinde Microsoft Edge (son genel olarak yayımlanmış sürüm)</span><span class="sxs-lookup"><span data-stu-id="97a34-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="97a34-109">Windows 10, Windows 8.1 veya Windows 7 üzerinde Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="97a34-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="97a34-110">Windows 10, Windows 8.1, Windows 8, Windows 7 veya Google Nexus 10 tablet üzerinde Google Chrome (son genel olarak yayımlanan sürümü)</span><span class="sxs-lookup"><span data-stu-id="97a34-110">Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet</span></span>
-   <span data-ttu-id="97a34-111">Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) ve 10.12 (Sierra) veya Apple iPad üzerinde Apple Safari (son genel olarak yayınlanmış sürüm)</span><span class="sxs-lookup"><span data-stu-id="97a34-111">Apple Safari (latest publicly available version) on Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) or 10.12 (Sierra), or Apple iPad</span></span>

<span data-ttu-id="97a34-112">Her web tarayıcısı için en son sürümü bulmak için, yazılım üreticisinin web sitesine gidin.</span><span class="sxs-lookup"><span data-stu-id="97a34-112">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> -   <span data-ttu-id="97a34-113">Görev Kaydedici'yi ekran görüntüleri yakalamak ve bunları oluşturulan Microsoft Word belgelerine dahile etmek için bir önceden yayınlanmış Chrome eklentisinin etkinleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="97a34-113">You must install a pre-release Chrome extension to enable Task Recorder to capture screenshots and include them in Microsoft Word documents that are generated.</span></span> <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> -   <span data-ttu-id="97a34-114">İş Akışı Düzenleyicisi bir ClickOnce uygulaması olarak başlatılır.</span><span class="sxs-lookup"><span data-stu-id="97a34-114">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="97a34-115">ClickOnce uygulamalarını yalnızca Microsoft Edge ve Internet Explorer (Microsoft Windows'un desteklenen bir sürümünde) destekler.</span><span class="sxs-lookup"><span data-stu-id="97a34-115">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="97a34-116">İş Akışı Düzenleyicisi ClickOnce uygulaması için 64-bit uyumlu bir işletim sistemi gereklidir.</span><span class="sxs-lookup"><span data-stu-id="97a34-116">The Workflow Editor ClickOnce application requires a 64-bit-compatible operating system.</span></span>
> -   <span data-ttu-id="97a34-117">Finansal raporlama için Rapor Tasarımcısı bir ClickOnce uygulaması olarak başlatılır.</span><span class="sxs-lookup"><span data-stu-id="97a34-117">The Report Designer for Financial reporting is started as a ClickOnce application.</span></span> <span data-ttu-id="97a34-118">64-bit uyumlu bir işletim sistemi gerektirir.</span><span class="sxs-lookup"><span data-stu-id="97a34-118">It requires a 64-bit-compatible operating system.</span></span> <span data-ttu-id="97a34-119">Chrome kullanıyorsanız, Rapor Tasarımcısı istemcisini indirebilmek için ClickOnce eklentisini yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="97a34-119">If you’re using Chrome, you must install a ClickOnce extension to download the Report Designer client.</span></span> <span data-ttu-id="97a34-120">Chrome'u gizli modda kullanıyorsnız, ClickOnce eklentisinin gizli mod için de etkinleştirildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="97a34-120">If you use Chrome in Incognito mode, make sure that the ClickOnce extension is also enabled for Incognito mode.</span></span>
> -   <span data-ttu-id="97a34-121">PDF dosyalarının önizlemesini yapmak için (en son sürüm genel kullanıma açık) Windows 10 üzerinde, Microsoft Edge veya (en son sürüm genel kullanıma açık) Windows 10, Windows 8.1, Windows 8, Windows 7 veya Google Nexus 10 tablet üzerinde Google Chrome gibi tarayıcıları kullanmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="97a34-121">To preview PDF files, we recommend that you use browsers such as Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>

### <a name="supported-web-browsers-for-retail-cloud-pos"></a><span data-ttu-id="97a34-122">Perakende Bulut POS'u için desteklenen web tarayıcıları</span><span class="sxs-lookup"><span data-stu-id="97a34-122">Supported web browsers for Retail Cloud POS</span></span>

<span data-ttu-id="97a34-123">Retail Cloud POS belirtilen işletim sistemleri üzerinde çalışan aşağıdaki web tarayıcılarından birinde çalıştırılabilir:</span><span class="sxs-lookup"><span data-stu-id="97a34-123">Retail Cloud POS can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="97a34-124">Windows 10 üzerinde Microsoft Edge (son genel olarak yayımlanmış sürüm)</span><span class="sxs-lookup"><span data-stu-id="97a34-124">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="97a34-125">Windows 10, Windows 8.1 veya Windows 7 üzerinde Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="97a34-125">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="97a34-126">Windows 10, Windows 8.1 veya Windows 7 üzerinde Chrome (son genel olarak yayımlanmış sürüm)</span><span class="sxs-lookup"><span data-stu-id="97a34-126">Chrome (latest publicly available version) on Windows 10, Windows 8.1, or Windows 7</span></span>

## <a name="network-requirements"></a><span data-ttu-id="97a34-127">Ağ gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="97a34-127">Network requirements</span></span>
-   <span data-ttu-id="97a34-128">Finance and Operations 250-300 milisaniye (ms) veya daha az gecikmeye sahip ağlar için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="97a34-128">Finance and Operations is designed for networks that have a latency of 250–300 milliseconds (ms) or less.</span></span> <span data-ttu-id="97a34-129">Bu gecikme, bir tarayıcı istemcisinden Finance and Operations'ı barındıran Microsoft Azure veri merkezine iletim süresidir.</span><span class="sxs-lookup"><span data-stu-id="97a34-129">This latency is the latency from a browser client to the Microsoft Azure datacenter that hosts Finance and Operations.</span></span> <span data-ttu-id="97a34-130">Ağ gecikmesini <http://www.azurespeed.com>'da sınamanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="97a34-130">We recommend that you test network latency at <http://www.azurespeed.com>.</span></span>
-   <span data-ttu-id="97a34-131">Finance and Operations için bant genişliği gereksinimleri senaryoya bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="97a34-131">Bandwidth requirements for Finance and Operations depend on your scenario.</span></span> <span data-ttu-id="97a34-132">En tipik senaryolar 50 kilobayt/saniye (KBps) üzerinde bir bant genişliği gerektirir.</span><span class="sxs-lookup"><span data-stu-id="97a34-132">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span> <span data-ttu-id="97a34-133">Ancak, kapsamlı özelleştirme içeren çalışma alanları veya senaryolar gibi yüksek yük gereksinimleri olan senaryolar için daha fazla bant genişliği öneririz.</span><span class="sxs-lookup"><span data-stu-id="97a34-133">However, we recommend more bandwidth for scenarios that have high payload requirements, such as scenarios that involve workspaces or extensive customization.</span></span>

<span data-ttu-id="97a34-134">Genel olarak, Finance and Operations İnternet için optimize edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="97a34-134">In general, Finance and Operations is optimized for the internet.</span></span> <span data-ttu-id="97a34-135">Bir tarayıcı istemcisinden Azure veri merkezine gidiş dönüş sayısı oldukça küçüktür ve tüm yükü sıkıştırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="97a34-135">The number of round trips from a browser client to the Azure datacenter is very small, and the whole payload is compressed.</span></span> 

> [!WARNING]
> <span data-ttu-id="97a34-136">Kullanıcı sayısıyla minimum bant genişliği gereksinimlerini çarpıp bir müşteri konumundan bant genişliği gereksinimlerini hesaplama.</span><span class="sxs-lookup"><span data-stu-id="97a34-136">Don't calculate bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="97a34-137">Belirli bir konumun eşzamanlı kullanımını hesaplamak çok zordur.</span><span class="sxs-lookup"><span data-stu-id="97a34-137">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="97a34-138">Bant genişliği gereksinimleri konusunda kaygıları olan müşteriler, Finance and Operations'ın bir önizleme sürümünü kullanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="97a34-138">Customers who are concerned about bandwidth requirements should use a preview version of Finance and Operations.</span></span>

## <a name="net-framework-requirements"></a><span data-ttu-id="97a34-139">.NET Framework gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="97a34-139">.NET Framework requirements</span></span>
<span data-ttu-id="97a34-140">Finance and Operations, belge yönlendirme aracısı gibi ClickOnce uygulamaları için Microsoft .NET Framework sürüm 4.6.2 gerektirir.</span><span class="sxs-lookup"><span data-stu-id="97a34-140">Finance and Operations requires the Microsoft .NET Framework version 4.6.2 for all ClickOnce applications, such as the document routing agent.</span></span> <span data-ttu-id="97a34-141">Yükleme yönergeleri için bkz. [.NET Framework'ü yükleme](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="97a34-141">For installation instructions, see [Installing the .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="97a34-142">Desteklenen Microsoft Office uygulamaları</span><span class="sxs-lookup"><span data-stu-id="97a34-142">Supported Microsoft Office applications</span></span>
<span data-ttu-id="97a34-143">Aşağıdaki Microsoft Office uygulamaları Finance and Operations şirket içi dağıtımlarında bulutta desteklenir.</span><span class="sxs-lookup"><span data-stu-id="97a34-143">The following Microsoft Office applications are supported in cloud and on-premises deployments of Finance and Operations:</span></span>

-   <span data-ttu-id="97a34-144">Microsoft Excel ve Word eklentilerini çalıştırmak için Windows veya Mac için Microsoft Office 2016'yı yüklemiş olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="97a34-144">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="97a34-145">Sürüm gereksinimleri hakkında daha fazla bilgi için bkz. [Office tümleştirme sorunlarını giderme](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="97a34-145">For more information about version requirements, see [Office integration troubleshooting](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span></span>
-   <span data-ttu-id="97a34-146">Excel'e Aktar veya Word'e Aktar işleviyle oluşturulan belgeleri görüntülemek için Microsoft Office 2007 veya sonraki bir sürümü yüklemiş olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="97a34-146">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="retail-modern-pos-requirements"></a><span data-ttu-id="97a34-147">Retail Modern POS gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="97a34-147">Retail Modern POS requirements</span></span>

> [!NOTE]
> <span data-ttu-id="97a34-148">Retail Modern POS çevrimdışı bir veritabanı kullanacaksa, bilgisayarın Microsoft SQL Server için tüm sistem gereksinimlerini karşılaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="97a34-148">If Retail Modern POS will use an offline database, the computer must meet all system requirements for Microsoft SQL Server.</span></span> <span data-ttu-id="97a34-149">Bir Retail Modern POS çevrimdışı veritabanı Microsoft SQL Server 2012 Service Pack 3 veya sonrası, Microsoft SQL Server 2014 Service 2 veya sonrası ve Microsoft SQL Server 2016 ile çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="97a34-149">A Retail Modern POS offline database will work on Microsoft SQL Server 2012 with Service Pack 3 or later, Microsoft SQL Server 2014 with Service Pack 2 or later, and Microsoft SQL Server 2016.</span></span> <span data-ttu-id="97a34-150">Her zaman kullanılabilir en son sürümü kullanmanızı ve en son hizmet paketlerini yüklemenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="97a34-150">We recommend that you always use the latest version that is available, and that you install all the latest service packs.</span></span>

### <a name="supported-operating-systems"></a><span data-ttu-id="97a34-151">Desteklenen işletim sistemleri</span><span class="sxs-lookup"><span data-stu-id="97a34-151">Supported operating systems</span></span>

-   <span data-ttu-id="97a34-152">Retail Modern POS 32 bitlik bir uygulama olmakla birlikte, hem x86 hem de x64 mimarileri üzerinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="97a34-152">Retail Modern POS is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="97a34-153">Retail Modern POS yalnızca Windows 10 Pro, Enterprise ve Enterprise Long Term Servicing Branch (LTSB) sürümlerinde desteklenir.</span><span class="sxs-lookup"><span data-stu-id="97a34-153">Retail Modern POS is supported only on Windows 10 Pro, Enterprise, and Enterprise Long Term Servicing Branch (LTSB) editions.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="97a34-154">Minimum sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="97a34-154">Minimum system requirements</span></span>

-   <span data-ttu-id="97a34-155">Desteklenen en düşük çözünürlük 1280 × 1024'tür.</span><span class="sxs-lookup"><span data-stu-id="97a34-155">The minimum supported resolution is 1,280 × 1,024.</span></span>
-   <span data-ttu-id="97a34-156">Retail Modern POS'un çalıştığı bilgisayarın aşağıdaki gereksinimleri karşılaması gerekir:</span><span class="sxs-lookup"><span data-stu-id="97a34-156">The computer that Retail Modern POS runs on must meet these requirements:</span></span>

    -   <span data-ttu-id="97a34-157">En az 2 gigahertz at (GHz) hızla çalışan bir çift çekirdekli işlemcisi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="97a34-157">It must have, at a minimum, a dual-core processor that runs at no less than 2 gigahertz (GHz).</span></span>
    -   <span data-ttu-id="97a34-158">En az 3 gigabayt (GB) rastgele erişim belleği (RAM) olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="97a34-158">It must have, at a minimum, 3 gigabytes (GB) of random-access memory (RAM).</span></span>
    -   <span data-ttu-id="97a34-159">İnternet erişiminin olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="97a34-159">It must have internet access.</span></span>

## <a name="retail-hardware-station-requirements"></a><span data-ttu-id="97a34-160">Retail hardware station gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="97a34-160">Retail hardware station requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="97a34-161">Desteklenen işletim sistemleri</span><span class="sxs-lookup"><span data-stu-id="97a34-161">Supported operating systems</span></span>

-   <span data-ttu-id="97a34-162">Retail hardware station 32 bitlik bir uygulama olmakla birlikte, hem x86 hem de x64 mimarileri üzerinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="97a34-162">Retail hardware station is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="97a34-163">Retail hardware station aşağıdaki işletim sistemlerinde desteklenir:</span><span class="sxs-lookup"><span data-stu-id="97a34-163">Retail hardware station is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="97a34-164">Windows 7 Professional, Enterprise ve Ultimate sürümleri</span><span class="sxs-lookup"><span data-stu-id="97a34-164">Windows 7 Professional, Enterprise, and Ultimate editions</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="97a34-165">Windows 7 yalnızca Internet Explorer 11 sistem üzerine el ile yüklendiyse desteklenir.</span><span class="sxs-lookup"><span data-stu-id="97a34-165">Windows 7 is supported only if Internet Explorer 11 is manually installed on the system.</span></span>

    -   <span data-ttu-id="97a34-166">Windows 8.1 Güncelleme 1 Professional, Enterprise ve Embedded sürümleri</span><span class="sxs-lookup"><span data-stu-id="97a34-166">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="97a34-167">Windows 10 Pro, Enterprise ve Enterprise LTSB sürümleri</span><span class="sxs-lookup"><span data-stu-id="97a34-167">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="97a34-168">Minimum sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="97a34-168">Minimum system requirements</span></span>

<span data-ttu-id="97a34-169">Aşağıdaki öğelerin yüklenip kullanılabilmesi için bilgisayarın tüm sistem gereksinimlerini karşılaması gerekir:</span><span class="sxs-lookup"><span data-stu-id="97a34-169">The computer must meet all system requirements for installing and using the following items:</span></span>

-   <span data-ttu-id="97a34-170">Internet Information Services (IIS)</span><span class="sxs-lookup"><span data-stu-id="97a34-170">Internet Information Services (IIS)</span></span>
-   <span data-ttu-id="97a34-171">Üçüncü taraf donanım</span><span class="sxs-lookup"><span data-stu-id="97a34-171">Third-party hardware</span></span>

## <a name="retail-store-scale-unit-requirements"></a><span data-ttu-id="97a34-172">Perakende Mağaza Ölçeği Birimi gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="97a34-172">Retail Store Scale Unit requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="97a34-173">Desteklenen işletim sistemleri</span><span class="sxs-lookup"><span data-stu-id="97a34-173">Supported operating systems</span></span>

-   <span data-ttu-id="97a34-174">Perakende Mağaza Ölçeği Birimi 32 bitlik bir uygulama olmakla birlikte, hem x86 hem de x64 mimarileri üzerinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="97a34-174">Retail Store Scale Unit is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="97a34-175">Perakende Mağaza Ölçeği Birimi aşağıdaki işletim sistemlerinde desteklenir:</span><span class="sxs-lookup"><span data-stu-id="97a34-175">Retail Store Scale Unit is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="97a34-176">Windows 7 Professional, Enterprise ve Ultimate sürümleri</span><span class="sxs-lookup"><span data-stu-id="97a34-176">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="97a34-177">Windows 8.1 Güncelleme 1 Professional, Enterprise ve Embedded sürümleri</span><span class="sxs-lookup"><span data-stu-id="97a34-177">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="97a34-178">Windows 10 Pro, Enterprise ve Enterprise LTSB sürümleri</span><span class="sxs-lookup"><span data-stu-id="97a34-178">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="97a34-179">Minimum sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="97a34-179">Minimum system requirements</span></span>

-   <span data-ttu-id="97a34-180">4 GB RAM</span><span class="sxs-lookup"><span data-stu-id="97a34-180">4 GB of RAM</span></span>
-   <span data-ttu-id="97a34-181">1.6 GHz çekirdek başına en yüksek CPU hızı (En az iki çekirdek.)</span><span class="sxs-lookup"><span data-stu-id="97a34-181">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="97a34-182">En az 10 GB boş alan (kanal veritabanı için büyük bir boş alan gerekebilir.)</span><span class="sxs-lookup"><span data-stu-id="97a34-182">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

### <a name="recommended-system-requirements"></a><span data-ttu-id="97a34-183">Önerilen sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="97a34-183">Recommended system requirements</span></span>

-   <span data-ttu-id="97a34-184">6 GB RAM</span><span class="sxs-lookup"><span data-stu-id="97a34-184">6 GB of RAM</span></span>
-   <span data-ttu-id="97a34-185">2.4 GHz i7 (veya eşdeğeri) çekirdek başına en yüksek CPU hızı (Dört çekirdek önerilir.)</span><span class="sxs-lookup"><span data-stu-id="97a34-185">2.4 GHz i7 (or equivalent) peak CPU speed per core (Four cores are recommended.)</span></span>
-   <span data-ttu-id="97a34-186">En az 10 GB boş alan (kanal veritabanı için büyük bir boş alan gerekebilir.)</span><span class="sxs-lookup"><span data-stu-id="97a34-186">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="connector-requirements"></a><span data-ttu-id="97a34-187">Bağlayıcı gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="97a34-187">Connector requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="97a34-188">Desteklenen işletim sistemleri</span><span class="sxs-lookup"><span data-stu-id="97a34-188">Supported operating systems</span></span>

-   <span data-ttu-id="97a34-189">Connector for Microsoft Dynamics AX'te iki ayrı yükleyici olan bir Async Server Connector service ve bir Real-time service for Dynamics AX 2012 R3 bulunur.</span><span class="sxs-lookup"><span data-stu-id="97a34-189">The Connector for Microsoft Dynamics AX has two separate installers, one for Async Server Connector service and one for Real-time service for Dynamics AX 2012 R3.</span></span>
-   <span data-ttu-id="97a34-190">İki bileşen de 32 bitlik bir uygulama olmakla birlikte, bunlar hem x86 hem de x64 mimarileri üzerinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="97a34-190">Both components are 32-bit applications, but they will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="97a34-191">Her iki bileşen de aşağıdaki işletim sistemlerinde desteklenir:</span><span class="sxs-lookup"><span data-stu-id="97a34-191">Both components are supported on the following operating systems:</span></span>

    -   <span data-ttu-id="97a34-192">Windows 7 Professional, Enterprise ve Ultimate sürümleri</span><span class="sxs-lookup"><span data-stu-id="97a34-192">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="97a34-193">Windows 8.1 Güncelleme 1 Professional, Enterprise ve Embedded sürümleri</span><span class="sxs-lookup"><span data-stu-id="97a34-193">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="97a34-194">Windows 10 Pro, Enterprise ve Enterprise LTSB sürümleri</span><span class="sxs-lookup"><span data-stu-id="97a34-194">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>
    -   <span data-ttu-id="97a34-195">Microsoft Windows Server 2012 R2 ve Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="97a34-195">Microsoft Windows Server 2012 R2 and Microsoft Windows Server 2016</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="97a34-196">Minimum sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="97a34-196">Minimum system requirements</span></span>
-   <span data-ttu-id="97a34-197">2 GB RAM (4 GB RAM önerilir.)</span><span class="sxs-lookup"><span data-stu-id="97a34-197">2 GB of RAM (4 GB of RAM are recommended.)</span></span>
-   <span data-ttu-id="97a34-198">1.6 GHz çekirdek başına en yüksek CPU hızı (En az iki çekirdek.)</span><span class="sxs-lookup"><span data-stu-id="97a34-198">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="97a34-199">En az 10 GB boş alan (kanal veritabanı için büyük bir boş alan gerekebilir.)</span><span class="sxs-lookup"><span data-stu-id="97a34-199">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="requirements-for-development-on-local-vms"></a><span data-ttu-id="97a34-200">Yerel VM'ler üzerinde geliştirme için gereksinimler</span><span class="sxs-lookup"><span data-stu-id="97a34-200">Requirements for development on local VMs</span></span>
<span data-ttu-id="97a34-201">Yerel sanal makinelerde (VM) geliştirme için gereksinimler hakkında bilgi için bkz. [yerinde çalışan VM](../../dev-itpro/dev-tools/access-instances.md).</span><span class="sxs-lookup"><span data-stu-id="97a34-201">For information about the requirements for development on local virtual machines (VMs), see [VM running on-premises](../../dev-itpro/dev-tools/access-instances.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="97a34-202">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="97a34-202">See also</span></span>

[<span data-ttu-id="97a34-203">Dynamics 365 for Finance and Operations, Enterprise Edition'ın değerlendirme kopyasını edinin</span><span class="sxs-lookup"><span data-stu-id="97a34-203">Get an evaluation copy of Dynamics 365 for Finance and Operations, Enterprise edition</span></span>](../../dev-itpro/dev-tools/get-evaluation-copy.md)


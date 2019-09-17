---
title: Talent sistem gereksinimleri ve güncelleştirme ilkesi
description: Bu konu Dynamics 365 for Talent için gereksinimleri listeler. Güncelleştirme ilkesi de açıklanmaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 6c881bf25e7145228ccf7ef73a7ef3637c115a49
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741787"
---
# <a name="talent-system-requirements-and-update-policy"></a><span data-ttu-id="5ef24-104">Talent sistem gereksinimleri ve güncelleştirme ilkesi</span><span class="sxs-lookup"><span data-stu-id="5ef24-104">Talent system requirements and update policy</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5ef24-105">Bu konu Attract, Onboard ve Core HR dahil olmak üzere Microsoft Dynamics 365 for Talent için gereksinimleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="5ef24-105">This topic describes requirements for Microsoft Dynamics 365 for Talent, including Attract, Onboard, and Core HR.</span></span> <span data-ttu-id="5ef24-106">Ayrıca, Talent'ın kullanılabildiği ülkeler ve bölgeler ile birlikte Talent verileri için diller ve yerelleştirme hakkında bilgiler de ana hatlarıyla açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="5ef24-106">It also outlines the countries and regions where Talent is available, plus information about languages and localization for Talent data.</span></span> <span data-ttu-id="5ef24-107">Ek olarak bu konu Talent ile ilgili güncelleştirme ilkesini içerir.</span><span class="sxs-lookup"><span data-stu-id="5ef24-107">In additions, this topic provides the update policy for Talent.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="5ef24-108">Desteklenen web tarayıcıları</span><span class="sxs-lookup"><span data-stu-id="5ef24-108">Supported web browsers</span></span>

<span data-ttu-id="5ef24-109">Microsoft Dynamics 365 for Talent web uygulamasını belirtilen işletim sistemleri üzerinde çalışan aşağıdaki web tarayıcılarından birinde çalıştırabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="5ef24-109">The Microsoft Dynamics 365 for Talent web application can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="5ef24-110">Windows 10 üzerinde Microsoft Edge (son genel olarak yayımlanmış sürüm)</span><span class="sxs-lookup"><span data-stu-id="5ef24-110">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="5ef24-111">Windows 10, Windows 8.1 veya Windows 7 üzerinde Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="5ef24-111">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="5ef24-112">Google Chrome (genel yayımlanmış en son sürüm)</span><span class="sxs-lookup"><span data-stu-id="5ef24-112">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="5ef24-113">Apple Safari (genel yayımlanmış son sürüm)</span><span class="sxs-lookup"><span data-stu-id="5ef24-113">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="5ef24-114">Her web tarayıcısı için en son sürümü bulmak için, yazılım üreticisinin web sitesine gidin.</span><span class="sxs-lookup"><span data-stu-id="5ef24-114">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="5ef24-115">Görev Kaydedici'den oluşturulmuş görüntüleri yakalamak ve bunları Microsoft Word belgelerine eklemek için bir Chrome eklentisinin yüklü olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="5ef24-115">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="5ef24-116">İş Akışı Düzenleyicisi bir ClickOnce uygulaması olarak başlatılır.</span><span class="sxs-lookup"><span data-stu-id="5ef24-116">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="5ef24-117">Yalnızca Microsoft Edge ve Internet Explorer (desteklenen bir Microsoft Windows sürümü üzerinde) ClickOnce uygulamalarını destekler.</span><span class="sxs-lookup"><span data-stu-id="5ef24-117">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="5ef24-118">İş Akışı Düzenleyicisi ClickOnce uygulaması için 64-bit uyumlu bir işletim sistemi gereklidir.</span><span class="sxs-lookup"><span data-stu-id="5ef24-118">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="5ef24-119">PDF dosyalarının önizlemesini yapmak için (en son sürüm genel kullanıma açık) Windows 10 üzerinde, Microsoft Edge veya (en son sürüm genel kullanıma açık) Windows 10, Windows 8.1, Windows 8, Windows 7 veya Google Nexus 10 tablet üzerinde Google Chrome gibi modern tarayıcıları kullanmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="5ef24-119">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="5ef24-120">Ağ gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="5ef24-120">Network requirements</span></span>
> * <span data-ttu-id="5ef24-121">Dynamics 365 for Talent 250-300 milisaniye (ms) veya daha az gecikmeye sahip ağlar için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="5ef24-121">Dynamics 365 for Talent is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="5ef24-122">Bu, bir tarayıcı istemcisinden Dynamics 365 for Talent'ı barındıran Microsoft Azure veri merkezine iletim süresidir.</span><span class="sxs-lookup"><span data-stu-id="5ef24-122">This is the latency from a browser client to the Microsoft Azure data center that hosts Dynamics 365 for Talent.</span></span> <span data-ttu-id="5ef24-123">Ağ gecikmesini [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test") adresinden test etmenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="5ef24-123">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="5ef24-124">Dynamics 365 for Talent için bant genişliği gereksinimlerini senaryoya bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="5ef24-124">Bandwidth requirements for Dynamics 365 for Talent depend on your scenario.</span></span> <span data-ttu-id="5ef24-125">En tipik senaryolar 50 kilobayt/saniye (KBps) üzerinde bir bant genişliği gerektirir.</span><span class="sxs-lookup"><span data-stu-id="5ef24-125">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="5ef24-126">Kullanıcı sayısıyla minimum bant genişliği gereksinimlerini çarpıp bir müşteri konumundan bant genişliği gereksinimlerini hesaplamayın.</span><span class="sxs-lookup"><span data-stu-id="5ef24-126">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="5ef24-127">Belirli bir konumun eşzamanlı kullanımını hesaplamak çok zordur.</span><span class="sxs-lookup"><span data-stu-id="5ef24-127">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="5ef24-128">Bant genişliği gereksinimleri konusunda kaygıları olan müşteriler Dynamics 365 for Talent'ın bir deneme sürümünü kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="5ef24-128">For customers who are concerned about bandwidth requirements, use a trial version of Dynamics 365 for Talent.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="5ef24-129">Desteklenen Microsoft Office uygulamaları</span><span class="sxs-lookup"><span data-stu-id="5ef24-129">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="5ef24-130">Microsoft Excel ve Word eklentilerini çalıştırmak için Windows veya Mac için Microsoft Office 2016'yı yüklemiş olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5ef24-130">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="5ef24-131">Sürüm gereksinimleri hakkında daha fazla bilgi için bkz. [Office tümleştirme sorunlarını giderme](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office tümleştirme sorunlarını giderme").</span><span class="sxs-lookup"><span data-stu-id="5ef24-131">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="5ef24-132">Excel'e Aktar veya Word'e Aktar işleviyle oluşturulan belgeleri görüntülemek için Microsoft Office 2007 veya sonraki bir sürümü yüklemiş olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5ef24-132">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="5ef24-133">Bölgesel kullanılabilirlik, diller ve yerelleştirme</span><span class="sxs-lookup"><span data-stu-id="5ef24-133">Regional availability, languages, and localization</span></span>

<span data-ttu-id="5ef24-134">Talent'ın desteklediği ülkeler, bölgeler ve dillere ilişkin bir PDF dosyasını [Microsoft Dynamics 365'in uluslararası kullanılabilirliği](https://docs.microsoft.com/dynamics365/get-started/availability) bölümünden indirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ef24-134">You can download a PDF file of the countries, regions, and languages Talent supports at [International availability of Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="5ef24-135">Kullanıcı arabirimi başka dillere yerelleştirilmiş olmasına karşın, tüm kullanıcı verileri girildiği dilde depolanır.</span><span class="sxs-lookup"><span data-stu-id="5ef24-135">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="5ef24-136">Diğer dillerde e-postalar ve şablonlar oluşturabilirsiniz ancak zamanlama bilgileri gibi veriler şu anda yalnızca İngilizce olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5ef24-136">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="5ef24-137">Ülkeye veya bölgeye özel özelleştirmeler oluşturmakla ilgilenen bir geliştiricisiyseniz veya şu anda Microsoft tarafından desteklenmeyen bir ülke veya bölge için çözüm oluşturan bir geliştiriciyseniz bkz. [Globalleştirme](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span><span class="sxs-lookup"><span data-stu-id="5ef24-137">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>

## <a name="update-policy"></a><span data-ttu-id="5ef24-138">Güncelleştirme ilkesi</span><span class="sxs-lookup"><span data-stu-id="5ef24-138">Update policy</span></span>

<span data-ttu-id="5ef24-139">Microsoft Dynamics 365 for Talent, bir bulut hizmeti olarak sunulur.</span><span class="sxs-lookup"><span data-stu-id="5ef24-139">Microsoft Dynamics 365 for Talent is serviced as a cloud offering.</span></span> <span data-ttu-id="5ef24-140">Dynamics 365 for Talent güncelleştirmeleri süreklidir ve Microsoft tarafından otomatik olarak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="5ef24-140">Updates to Dynamics 365 for Talent are continuous and applied automatically by Microsoft.</span></span>

<span data-ttu-id="5ef24-141">Güncelleştirmeler düzenli aralıklarla yayımlanır ve tüm ortamlar için yapılır.</span><span class="sxs-lookup"><span data-stu-id="5ef24-141">Updates are released on a regular cadence and will be made to all environments.</span></span> <span data-ttu-id="5ef24-142">Dynamics 365 for Talent, ürün destek kullanılabilirliği hakkında düzenli ve öngörülebilir kılavuzlar sunan [Microsoft Desteği Yaşam Döngüsü ilkesi](https://support.microsoft.com/gp/lifecycle#gp/OSSLpolicy "Microsoft Desteği Yaşam Döngüsü") ile uygun olarak desteklenir.</span><span class="sxs-lookup"><span data-stu-id="5ef24-142">Dynamics 365 for Talent is supported according to the [Microsoft Support Lifecycle policy](https://support.microsoft.com/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle"), which provides consistent and predictable guidelines for product support availability.</span></span>

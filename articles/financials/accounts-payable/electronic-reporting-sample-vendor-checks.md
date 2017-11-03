---
title: "Satıcı çekleri örnek elektronik raporlama"
description: "Bu konu, Elektronik raporlama örnek çek biçimlerinin nasıl kullanılacağı hakkında genel bilgi sağlar."
author: twheeloc
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c9abea228cdaae84ca2b9aada9f36bbe79c1dc6b
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

[!include[banner](../includes/banner.md)]

# <a name="electronic-reporting-sample-check-formats"></a><span data-ttu-id="86bc2-103">Elektronik raporlama örnek çek biçimleri</span><span class="sxs-lookup"><span data-stu-id="86bc2-103">Electronic reporting sample check formats</span></span>

<span data-ttu-id="86bc2-104">Satıcı çeklerinizi biçimlendirmek için Elektronik raporlama (ER) kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86bc2-104">You can use Electronic reporting (ER) to format vendor checks.</span></span> <span data-ttu-id="86bc2-105">Pek çok bankaya özel çek sağlayıcısı–özel çek biçimi piyasada mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="86bc2-105">Many bank-specific and check provider–specific check formats are available on the market.</span></span> <span data-ttu-id="86bc2-106">Örnek çek biçimleri, ER araç havuzundaki Ödeme çeki modeline eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="86bc2-106">Sample check formats have been included in the Payment check model in the ER tool repository.</span></span> <span data-ttu-id="86bc2-107">Bu örnek çekler **Ortadaki çek (ABD)** ve **Altına üst denetleme çeki (ABD)** olarak etiketlenmiştir.</span><span class="sxs-lookup"><span data-stu-id="86bc2-107">These sample checks are labeled **Check in the middle (US)** and **Check on top stub below (US)**.</span></span>

## <a name="what-check-formats-are-currently-supported"></a><span data-ttu-id="86bc2-108">Hangi çek biçimleri şu anda desteklenmektedir?</span><span class="sxs-lookup"><span data-stu-id="86bc2-108">What check formats are currently supported?</span></span>

<span data-ttu-id="86bc2-109">Sürekli olarak Microsoft Dynamics Lifecycle Services'daki (LCS) Paylaşılan varlık kitaplığına gidip varlık türü **GER yapılandırması** olan mevcut dosyaların geçerli listesini görüntülemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="86bc2-109">You should always go to the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) and view the current list of available files that have an asset type of **GER configuration**.</span></span> <span data-ttu-id="86bc2-110">Sonraki "Neyi ayarlamam gerekiyor?" bölümünde, mevcut yapılandırmaları incelemek ve seçili yapılandırmaları içe aktarmak için bir LCS havuzunun nasıl oluşturulacağının açıklandığını açıklayan konuya bağlantı verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="86bc2-110">The next section, “What do I have to set up?,” includes a link to a topic that explains how to create an LCS repository so that you can review available configurations and import selected configurations.</span></span>

<span data-ttu-id="86bc2-111">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition çekin üstte bulunduğu ve iki havale bölümü tarafından izlenen bir örnek biçimi içermektedir.</span><span class="sxs-lookup"><span data-stu-id="86bc2-111">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, includes a sample format where the check is on top, followed by two remittance sections.</span></span> <span data-ttu-id="86bc2-112">Ayrıca, çekin ortada, iki havale bölümü arasında bulunduğu bir örnek biçim de içermektedir.</span><span class="sxs-lookup"><span data-stu-id="86bc2-112">It also includes a sample format where the check is in the middle, between two remittance sections.</span></span> <span data-ttu-id="86bc2-113">Bu örnek biçimleri, Deluxe iş çek biçimlerine karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="86bc2-113">These sample formats correspond to Deluxe business checks formats.</span></span>

## <a name="what-do-i-have-to-set-up"></a><span data-ttu-id="86bc2-114">Neyi ayarlamam gerekiyor?</span><span class="sxs-lookup"><span data-stu-id="86bc2-114">What do I have to set up?</span></span>

- <span data-ttu-id="86bc2-115">ER kullanarak çek yazdırmadan önce, en az bir etkin çek yapılandırmasının ER yapılandırmanıza aktarılmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="86bc2-115">Before you can print checks by using ER, at least one active check configuration must be imported into your ER configurations.</span></span> <span data-ttu-id="86bc2-116">Yönergeler için bkz. [Lifecycle Services'dan Elektronik raporlama yapılandırmalarını karşıdan yükle](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="86bc2-116">For instructions, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>
- <span data-ttu-id="86bc2-117">Banka hesabı için Nakit ve banka yönetimini çeklerini yapılandırırken, **Genel elektronik Dışa aktarma biçimi** onay kutusunu seçin ve sonra uygun dışa aktarma biçim yapılandırmasını çek biçimi olarak seçin.</span><span class="sxs-lookup"><span data-stu-id="86bc2-117">When you configure Cash and bank management checks for the bank account, select the **Generic electronic Export format** check box, and then select the appropriate check format as an export format configuration.</span></span>
- <span data-ttu-id="86bc2-118">Ayrıca, havale üzerine yazdırılacak makbuz satırlarının sayısını da belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="86bc2-118">You must also specify the number of slip lines that will be printed on the remittance.</span></span> <span data-ttu-id="86bc2-119">Bu sayıyı hesaplarken başlık satırlarını eklediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="86bc2-119">Be sure to include the header rows when you calculate this number.</span></span> <span data-ttu-id="86bc2-120">İki örnek çek biçimi için, önerilen irsaliye satırı sayısı 17'dir.</span><span class="sxs-lookup"><span data-stu-id="86bc2-120">For the two sample check formats, the recommended number of slip lines is 17.</span></span> <span data-ttu-id="86bc2-121">Bununla birlikte, bu sayı, çek stokunuz ve yazıcı sürücülerinize göre farklılık gösterecektir.</span><span class="sxs-lookup"><span data-stu-id="86bc2-121">However, this number will vary, depending on your check stock and your printer drivers.</span></span>
- <span data-ttu-id="86bc2-122">Çek biçimini doğrulamak için bir test çeki yazdırmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="86bc2-122">We recommend that you print a test check to validate the check layout.</span></span> <span data-ttu-id="86bc2-123">Bir test çeki yazdırmak için **Yazdırma testi** seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="86bc2-123">To print a test check, select the **Print test** option.</span></span> <span data-ttu-id="86bc2-124">Örnek çek biçimleri, Microsoft Excel için gelişmiş yazdırma özellikleri içinde **Kenar boşlukları** **Yok** olarak ayarlandığında en iyi çalışır.</span><span class="sxs-lookup"><span data-stu-id="86bc2-124">The sample check formats work best when **Margins** is set to **None** in the advanced printer properties for Microsoft Excel.</span></span> <span data-ttu-id="86bc2-125">Test çeki oluşturulduktan sonra, Excel çıktısının düzenlenmesini etkinleştirin ve sayfa düzenini, tüm kenar boşlukları **0** (sıfır) olacak şekilde yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="86bc2-125">After the test check has been generated, enable editing of the Excel output, and configure the page layout so that all margins are set to **0** (zero).</span></span> <span data-ttu-id="86bc2-126">Çeklerin test kopyasını, çek stokunuzla kıyaslayın ve hizalamadan tatmin olana kadar ayar yapın.</span><span class="sxs-lookup"><span data-stu-id="86bc2-126">Compare the test copy of the checks to your check stock, and adjust the settings until you're satisfied with the alignment.</span></span>
- <span data-ttu-id="86bc2-127">Ödeme günlüğünde yapılandırılmış banka hesabı için ödemeler oluşturduğunuzda, çekler belirtilen biçim kullanılarak yazdırılır.</span><span class="sxs-lookup"><span data-stu-id="86bc2-127">When you generate payments for the configured bank account in the payment journal, the checks will be printed by using the specified format.</span></span>

<span data-ttu-id="86bc2-128">Daha fazla bilgi için [Bir Elektronik raporlamada biçimini değiştir](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="86bc2-128">For more information, see [Modify an Electronic reporting format](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).</span></span>


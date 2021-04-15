---
title: Yazıcı ER hedefi türü
description: Bu konuda, Elektronik raporlama (ER) biçiminin her KLASÖR veya DOSYA bileşeni için yazıcı hedefini nasıl yapılandırabileceğiniz açıklanmaktadır.
author: NickSelin
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 83081f8c17a903cd447a34596df2e61ebda0cafc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753444"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a><span data-ttu-id="2e36b-103">Yazıcı hedefi</span><span class="sxs-lookup"><span data-stu-id="2e36b-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e36b-104">Oluşturulan bir belgeyi doğrudan yazdırma için bir ağ yazıcısına doğrudan gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2e36b-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2e36b-105">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="2e36b-105">Prerequisites</span></span>

<span data-ttu-id="2e36b-106">Başlamadan önce, Belge Yönlendirme Aracısı'nı yükleyip yapılandırmanız ve ardından ağ yazıcılarını kaydettirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2e36b-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="2e36b-107">Daha fazla bilgi için bkz. [Ağdan yazdırmayı etkinleştirmek için Belge Yönlendirme Aracısı'nı yükleme](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span><span class="sxs-lookup"><span data-stu-id="2e36b-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="2e36b-108">Yazıcı hedefini kullanıma açma</span><span class="sxs-lookup"><span data-stu-id="2e36b-108">Make the Printer destination available</span></span>

<span data-ttu-id="2e36b-109">**Yazıcı** hedefini Microsoft Dynamics 365 Finance'in geçerli kurulumunda kullanıma açmak için **Özellik yönetimi** çalışma alanına gidin ve aşağıdaki özellikleri şu sırayla açın:</span><span class="sxs-lookup"><span data-stu-id="2e36b-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="2e36b-110">Elektronik Raporlama giden belgelerini Microsoft Office biçimlerinden PDF'e dönüştür</span><span class="sxs-lookup"><span data-stu-id="2e36b-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="2e36b-111">Giden belgeler için Elektronik raporlama hedefi olarak Belge Yönlendirme Aracısı</span><span class="sxs-lookup"><span data-stu-id="2e36b-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="2e36b-112">[![Özellik yönetimi'nde ER yazıcı hedefi özelliğini açma](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="2e36b-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="2e36b-113">Uygulanabilirlik</span><span class="sxs-lookup"><span data-stu-id="2e36b-113">Applicability</span></span>

<span data-ttu-id="2e36b-114">**Yazıcı** hedefi, yalnızca, yazdırılabilir PDF biçiminde (PDF Merger veya PDF dosya biçimi öğeleri) veya Microsoft Office Excel/Word biçiminde (Excel dosyası) çıktı oluşturmak için kullanılan dosya bileşenleri için yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="2e36b-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="2e36b-115">Çıktı PDF biçiminde oluşturulunca yazıcıya gönderilir.</span><span class="sxs-lookup"><span data-stu-id="2e36b-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="2e36b-116">Çıktı Microsoft Office biçiminde oluşturulursa otomatik olarak PDF biçimine dönüştürülüp yazıcıya gönderilir.</span><span class="sxs-lookup"><span data-stu-id="2e36b-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="2e36b-117">Sınırlamalar</span><span class="sxs-lookup"><span data-stu-id="2e36b-117">Limitations</span></span>

<span data-ttu-id="2e36b-118">**Yazıcı** hedefi yalnızca bulut dağıtımları için uygulanır.</span><span class="sxs-lookup"><span data-stu-id="2e36b-118">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="2e36b-119">Yazıcı hedefini kullanma</span><span class="sxs-lookup"><span data-stu-id="2e36b-119">Use the Printer destination</span></span>

1. <span data-ttu-id="2e36b-120">Oluşturulan belgeyi bir yazıcıya göndermek için **Etkinleştirildi** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2e36b-120">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="2e36b-121">**Yazıcı adı** alanında, gerekli ağ yazıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="2e36b-121">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="2e36b-122">Oluşturulan çıktıyı daha sonra yazdırmaya hazır olması için yazdırma arşivinde saklamak için **Yazdırma arşivine kaydedilsin mi?** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2e36b-122">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="2e36b-123">Arşivlenmiş çıktıya daha sonra erişmek için, **Kuruluş yönetimi** \> **Sorgular ve raporlar** \> **Rapor arşivi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="2e36b-123">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="2e36b-124">[![Yazıcı hedefini kullanma](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="2e36b-124">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="2e36b-125">**Yazıcı** hedefini yapılandırdığınız zaman, **PDF'e dönüştür** seçeneğinin etkinleştirilmiş olması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="2e36b-125">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="2e36b-126">Seçenek kapalı olsa bile, yazdırma amacıyla PDF dönüştürme işlemi yapılır.</span><span class="sxs-lookup"><span data-stu-id="2e36b-126">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

<span data-ttu-id="2e36b-127">Bir giden belgeyi Excel biçiminde yazdırırken belirli bir [sayfa yönlendirmesini](electronic-reporting-destinations.md#SelectPdfPageOrientation) kullanmak için **PDF'ye Dönüştür** seçeneğini etkinleştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="2e36b-127">To use a specific [page orientation](electronic-reporting-destinations.md#SelectPdfPageOrientation) when you print an outbound document in Excel format, you must turn on the **Convert to PDF** option.</span></span> <span data-ttu-id="2e36b-128">**PDF 'ye Dönüştür** seçeneğini **Evet** olarak ayarladığınızda, **sayfa yönlendirme** alanı kullanılabilir duruma gelir.</span><span class="sxs-lookup"><span data-stu-id="2e36b-128">When you set the **Convert to PDF** option to **Yes**, the **Page orientation** field becomes available.</span></span> <span data-ttu-id="2e36b-129">**Sayfa yönlendirme** alanında, sayfa yönlendirmesi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2e36b-129">In the **Page orientation** field, you can select a page orientation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2e36b-130">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2e36b-130">Additional resources</span></span>

- [<span data-ttu-id="2e36b-131">Elektronik raporlamaya (ER) genel bakış</span><span class="sxs-lookup"><span data-stu-id="2e36b-131">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="2e36b-132">Elektronik raporlama (ER) hedefleri</span><span class="sxs-lookup"><span data-stu-id="2e36b-132">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: Yazıcı ER hedefi türü
description: Bu konuda, Elektronik raporlama (ER) biçiminin her KLASÖR veya DOSYA bileşeni için yazıcı hedefini nasıl yapılandırabileceğiniz açıklanmaktadır.
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: c6e298f62ec69f349eb713d66313e535c7e01881
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094091"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a><span data-ttu-id="cbcc7-103">Yazıcı hedefi</span><span class="sxs-lookup"><span data-stu-id="cbcc7-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cbcc7-104">Oluşturulan bir belgeyi doğrudan yazdırma için bir ağ yazıcısına doğrudan gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cbcc7-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cbcc7-105">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="cbcc7-105">Prerequisites</span></span>

<span data-ttu-id="cbcc7-106">Başlamadan önce, Belge Yönlendirme Aracısı'nı yükleyip yapılandırmanız ve ardından ağ yazıcılarını kaydettirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="cbcc7-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="cbcc7-107">Daha fazla bilgi için bkz. [Ağdan yazdırmayı etkinleştirmek için Belge Yönlendirme Aracısı'nı yükleme](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span><span class="sxs-lookup"><span data-stu-id="cbcc7-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="cbcc7-108">Yazıcı hedefini kullanıma açma</span><span class="sxs-lookup"><span data-stu-id="cbcc7-108">Make the Printer destination available</span></span>

<span data-ttu-id="cbcc7-109">**Yazıcı** hedefini Microsoft Dynamics 365 Finance'in geçerli kurulumunda kullanıma açmak için **Özellik yönetimi** çalışma alanına gidin ve aşağıdaki özellikleri şu sırayla açın:</span><span class="sxs-lookup"><span data-stu-id="cbcc7-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="cbcc7-110">Elektronik Raporlama giden belgelerini Microsoft Office biçimlerinden PDF'e dönüştür</span><span class="sxs-lookup"><span data-stu-id="cbcc7-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="cbcc7-111">Giden belgeler için Elektronik raporlama hedefi olarak Belge Yönlendirme Aracısı</span><span class="sxs-lookup"><span data-stu-id="cbcc7-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="cbcc7-112">[![Özellik yönetimi'nde ER yazıcı hedefi özelliğini açma](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="cbcc7-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="cbcc7-113">Uygulanabilirlik</span><span class="sxs-lookup"><span data-stu-id="cbcc7-113">Applicability</span></span>

<span data-ttu-id="cbcc7-114">**Yazıcı** hedefi, yalnızca, yazdırılabilir PDF biçiminde (PDF Merger veya PDF dosya biçimi öğeleri) veya Microsoft Office Excel/Word biçiminde (Excel dosyası) çıktı oluşturmak için kullanılan dosya bileşenleri için yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="cbcc7-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="cbcc7-115">Çıktı PDF biçiminde oluşturulunca yazıcıya gönderilir.</span><span class="sxs-lookup"><span data-stu-id="cbcc7-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="cbcc7-116">Çıktı Microsoft Office biçiminde oluşturulursa otomatik olarak PDF biçimine dönüştürülüp yazıcıya gönderilir.</span><span class="sxs-lookup"><span data-stu-id="cbcc7-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="cbcc7-117">Sınırlamalar</span><span class="sxs-lookup"><span data-stu-id="cbcc7-117">Limitations</span></span>

<span data-ttu-id="cbcc7-118">Bu özellik bir önizleme özelliğidir ve 365 Önizleme [Microsoft Dynamics 365 Önizlemeler için Ek Kullanım Koşulları](https://go.microsoft.com/fwlink/?linkid=2105274)'nda açıklanan kullanım koşullarına tabidir.</span><span class="sxs-lookup"><span data-stu-id="cbcc7-118">This feature is a preview feature and is subject to the terms of use that are described in [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://go.microsoft.com/fwlink/?linkid=2105274).</span></span>

<span data-ttu-id="cbcc7-119">**Yazıcı** hedefi yalnızca bulut dağıtımları için uygulanır.</span><span class="sxs-lookup"><span data-stu-id="cbcc7-119">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="cbcc7-120">Yazıcı hedefini kullanma</span><span class="sxs-lookup"><span data-stu-id="cbcc7-120">Use the Printer destination</span></span>

1. <span data-ttu-id="cbcc7-121">Oluşturulan belgeyi bir yazıcıya göndermek için **Etkinleştirildi** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cbcc7-121">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="cbcc7-122">**Yazıcı adı** alanında, gerekli ağ yazıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="cbcc7-122">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="cbcc7-123">Oluşturulan çıktıyı daha sonra yazdırmaya hazır olması için yazdırma arşivinde saklamak için **Yazdırma arşivine kaydedilsin mi?** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cbcc7-123">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="cbcc7-124">Arşivlenmiş çıktıya daha sonra erişmek için, **Kuruluş yönetimi** \> **Sorgular ve raporlar** \> **Rapor arşivi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="cbcc7-124">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="cbcc7-125">[![Yazıcı hedefini kullanma](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="cbcc7-125">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="cbcc7-126">**Yazıcı** hedefini yapılandırdığınız zaman, **PDF'e dönüştür** seçeneğinin etkinleştirilmiş olması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="cbcc7-126">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="cbcc7-127">Seçenek kapalı olsa bile, yazdırma amacıyla PDF dönüştürme işlemi yapılır.</span><span class="sxs-lookup"><span data-stu-id="cbcc7-127">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

<span data-ttu-id="cbcc7-128">Bir giden belgeyi Excel biçiminde yazdırırken belirli bir [sayfa yönlendirmesini](electronic-reporting-destinations.md#SelectPdfPageOrientation) kullanmak için **PDF'ye Dönüştür** seçeneğini etkinleştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="cbcc7-128">To use a specific [page orientation](electronic-reporting-destinations.md#SelectPdfPageOrientation) when you print an outbound document in Excel format, you must turn on the **Convert to PDF** option.</span></span> <span data-ttu-id="cbcc7-129">**PDF 'ye Dönüştür** seçeneğini **Evet** olarak ayarladığınızda, **sayfa yönlendirme** alanı kullanılabilir duruma gelir.</span><span class="sxs-lookup"><span data-stu-id="cbcc7-129">When you set the **Convert to PDF** option to **Yes**, the **Page orientation** field becomes available.</span></span> <span data-ttu-id="cbcc7-130">**Sayfa yönlendirme** alanında, sayfa yönlendirmesi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cbcc7-130">In the **Page orientation** field, you can select a page orientation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cbcc7-131">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="cbcc7-131">Additional resources</span></span>

- [<span data-ttu-id="cbcc7-132">Elektronik raporlamaya (ER) genel bakış</span><span class="sxs-lookup"><span data-stu-id="cbcc7-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="cbcc7-133">Elektronik raporlama (ER) hedefleri</span><span class="sxs-lookup"><span data-stu-id="cbcc7-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)

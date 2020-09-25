---
title: Arşiv ER hedef türü
description: Bu konu, giden belgeler oluşturmak üzere yapılandırılan bir Elektronik raporlama (ER) biçiminin her KLASÖR veya DOSYA bileşeni için bir arşiv hedefinin nasıl yapılandırılacağı hakkında bilgi sağlamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8797a68507a5116c6adbf1f2d805838fa507958c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745597"
---
# <a name="archive-destination"></a><span data-ttu-id="da607-103">Arşiv hedefi</span><span class="sxs-lookup"><span data-stu-id="da607-103">Archive destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="da607-104">Giden belgeler oluşturmak üzere yapılandırılan bir Elektronik raporlama (ER) biçiminin her KLASÖR veya DOSYA bileşeni için bir arşiv hedefi yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="da607-104">You can configure an archive destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="da607-105">Hedef ayarına bağlı olarak, oluşturulan bir belge, ER işleri listesindeki bir kaydın eki olarak depolanır.</span><span class="sxs-lookup"><span data-stu-id="da607-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span>

<span data-ttu-id="da607-106">Oluşturulan belgeyi Microsoft SharePoint klasörüne veya Microsoft Azure Depolama'ya göndermek için bu seçeneği kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="da607-106">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="da607-107">Seçili belge türü ile tanımlanan bir hedefe çıktı göndermek için **Etkin** değerini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="da607-107">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="da607-108">Yalnızca grubun **Dosya** olarak ayarlandığı belge türleri seçim için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="da607-108">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="da607-109">Belge [türlerini](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) **Kuruluş yönetimi** \> **Belge yönetimi** \> **Belge türleri**'nde tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="da607-109">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="da607-110">ER hedefleri için yapılandırma, belge yönetim sistemi için yapılandırma ile aynıdır.</span><span class="sxs-lookup"><span data-stu-id="da607-110">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="da607-111">[![Belge türleri sayfası](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="da607-111">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="da607-112">Konum dosyanın kaydedildiği yeri belirler.</span><span class="sxs-lookup"><span data-stu-id="da607-112">The location determines where the file is saved.</span></span> <span data-ttu-id="da607-113">**Arşiv** hedefi etkinleştirildikten sonra, sonuçlar İş arşivinde kaydedilebilir.</span><span class="sxs-lookup"><span data-stu-id="da607-113">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="da607-114">Sonuçları **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Elektronik raporlama arşivlenmiş işler** içerisinde görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="da607-114">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="da607-115">**Kuruluş yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama** \> **Elektronik raporlama parametreleri**'ne giderek İş arşivi için bir belge seçin.</span><span class="sxs-lookup"><span data-stu-id="da607-115">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="da607-116">Daha fazla bilgi için bkz. [Elektronik raporlama (ER) çerçevesini yapılandırma](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span><span class="sxs-lookup"><span data-stu-id="da607-116">For more information, [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="da607-117">SharePoint</span><span class="sxs-lookup"><span data-stu-id="da607-117">SharePoint</span></span>

<span data-ttu-id="da607-118">Dosyayı belirlenen bir SharePoint klasörüne kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="da607-118">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="da607-119">Varsayılan SharePoint sunucusunu tanımlamak için **Kuruluş yönetimi** \> **Belge yönetimi** \> **Belge yönetimi parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="da607-119">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="da607-120">**SharePoint** sekmesinde, SharePoint klasörünü yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="da607-120">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="da607-121">Sonra, bunu ER çıktısının kaydedileceği klasör olarak seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="da607-121">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="da607-122">Bu belge türünde **SharePoint** konumunun seçilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="da607-122">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="da607-123">[![Bir SharePoint klasörü seçmek](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="da607-123">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="da607-124">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="da607-124">Azure Storage</span></span>

<span data-ttu-id="da607-125">Belge türü konumu **Azure depolama** olarak ayarlandığında Azure Depolama'ya bir dosya kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="da607-125">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="da607-126">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="da607-126">Additional resources</span></span>

- [<span data-ttu-id="da607-127">Elektronik raporlamaya (ER) genel bakış</span><span class="sxs-lookup"><span data-stu-id="da607-127">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="da607-128">Elektronik raporlama (ER) hedefleri</span><span class="sxs-lookup"><span data-stu-id="da607-128">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="da607-129">Belge yönetimini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="da607-129">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)

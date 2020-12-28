---
title: Arşiv ER hedef türü
description: Bu konu, giden belgeler oluşturmak üzere yapılandırılan bir Elektronik raporlama (ER) biçiminin her KLASÖR veya DOSYA bileşeni için bir arşiv hedefinin nasıl yapılandırılacağı hakkında bilgi sağlamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 11/30/2020
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
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 3dee7ec614ec1372feaa1150f5e4ebb14c32f60e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679690"
---
# <a name="archive-er-destination-type"></a><span data-ttu-id="f4be3-103">Arşiv ER hedef türü</span><span class="sxs-lookup"><span data-stu-id="f4be3-103">Archive ER destination type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4be3-104">Giden belgeler oluşturmak üzere yapılandırılan bir Elektronik raporlama (ER) biçiminin her **Klasör** veya **Dosya** bileşeni için bir arşiv hedefi yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f4be3-104">You can configure an archive destination for each **Folder** or **File** component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="f4be3-105">Hedef ayarına bağlı olarak, oluşturulan bir belge, ER işleri listesindeki bir kaydın eki olarak depolanır.</span><span class="sxs-lookup"><span data-stu-id="f4be3-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span> <span data-ttu-id="f4be3-106">Sonuçları görüntülemek için **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Elektronik raporlama işleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="f4be3-106">To view the results, go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting jobs**.</span></span>

<span data-ttu-id="f4be3-107">Oluşturulan belgeyi Microsoft SharePoint klasörüne veya Microsoft Azure Depolama'ya göndermek için bu seçeneği kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f4be3-107">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="f4be3-108">Seçili belge türü ile tanımlanan bir hedefe çıktı göndermek için **Etkin** değerini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f4be3-108">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="f4be3-109">Yalnızca grubun **Dosya** olarak ayarlandığı belge türleri seçim için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f4be3-109">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="f4be3-110">Belge [türlerini](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) **Kuruluş yönetimi** \> **Belge yönetimi** \> **Belge türleri**'nde tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="f4be3-110">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="f4be3-111">ER hedefleri için yapılandırma, belge yönetim sistemi için yapılandırma ile aynıdır.</span><span class="sxs-lookup"><span data-stu-id="f4be3-111">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="f4be3-112">[![Belge türleri sayfası](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="f4be3-112">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="f4be3-113">Konum dosyanın kaydedildiği yeri belirler.</span><span class="sxs-lookup"><span data-stu-id="f4be3-113">The location determines where the file is saved.</span></span> <span data-ttu-id="f4be3-114">**Arşiv** hedefi etkinleştirildikten sonra, sonuçlar İş arşivinde kaydedilebilir.</span><span class="sxs-lookup"><span data-stu-id="f4be3-114">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="f4be3-115">Sonuçları **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Elektronik raporlama arşivlenmiş işler** içerisinde görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f4be3-115">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="f4be3-116">**Kuruluş yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama** \> **Elektronik raporlama parametreleri**'ne giderek İş arşivi için bir belge seçin.</span><span class="sxs-lookup"><span data-stu-id="f4be3-116">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="f4be3-117">Daha fazla bilgi için [Elektronik raporlama (ER) çerçevesini yapılandırma](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="f4be3-117">For more information, see [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="f4be3-118">SharePoint</span><span class="sxs-lookup"><span data-stu-id="f4be3-118">SharePoint</span></span>

<span data-ttu-id="f4be3-119">Dosyayı belirlenen bir SharePoint klasörüne kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f4be3-119">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="f4be3-120">Varsayılan SharePoint sunucusunu tanımlamak için **Kuruluş yönetimi** \> **Belge yönetimi** \> **Belge yönetimi parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="f4be3-120">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="f4be3-121">**SharePoint** sekmesinde, SharePoint klasörünü yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="f4be3-121">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="f4be3-122">Sonra, bunu ER çıktısının kaydedileceği klasör olarak seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f4be3-122">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="f4be3-123">Bu belge türünde **SharePoint** konumunun seçilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="f4be3-123">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="f4be3-124">[![Bir SharePoint klasörü seçmek](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="f4be3-124">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="f4be3-125">Azure Depolama</span><span class="sxs-lookup"><span data-stu-id="f4be3-125">Azure Storage</span></span>

<span data-ttu-id="f4be3-126">Belge türü konumu **Azure depolama** olarak ayarlandığında Azure Depolama'ya bir dosya kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f4be3-126">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

> [!NOTE] 
> <span data-ttu-id="f4be3-127">İşlenmesi gereken belgeler için 7 gün saklama politikası uygulayan Veri yönetimi çerçevesinin aksine, ER çerçevesi dosyaları kalıcı olarak Azure Blob depolama alanında depolar.</span><span class="sxs-lookup"><span data-stu-id="f4be3-127">The ER framework permanently stores files in Azure Blob storage unlike the Data management framework that applies the seven-day retention policy for documents that must be processed.</span></span> <span data-ttu-id="f4be3-128">Daha fazla bilgi için bkz. [İleti durumu alma API'si](../data-entities/recurring-integrations.md#api-for-getting-message-status) ve [Durum denetimi API'si](../data-entities/data-management-api.md#status-check-api).</span><span class="sxs-lookup"><span data-stu-id="f4be3-128">For more information, see [API for getting message status](../data-entities/recurring-integrations.md#api-for-getting-message-status) and [Status check API](../data-entities/data-management-api.md#status-check-api).</span></span> <span data-ttu-id="f4be3-129">ER ile ilgili dosyalar, gerekli olduğu sürece, Azure Blob depolamada, uygulama tablosu kayıtlarının ekleri olarak depolanır.</span><span class="sxs-lookup"><span data-stu-id="f4be3-129">The ER-related files will be stored in Azure Blob storage as attachments of application table records as long as necessary.</span></span> <span data-ttu-id="f4be3-130">Azure Blob depolama alanından bu dosyanın eklendiği uygulama tablosu kaydıyla birlikte tek bir dosya silinir.</span><span class="sxs-lookup"><span data-stu-id="f4be3-130">A single file will be deleted from Azure Blob storage along with the application table record that this file was attached to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4be3-131">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f4be3-131">Additional resources</span></span>

- [<span data-ttu-id="f4be3-132">Elektronik raporlamaya (ER) genel bakış</span><span class="sxs-lookup"><span data-stu-id="f4be3-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="f4be3-133">Elektronik raporlama (ER) hedefleri</span><span class="sxs-lookup"><span data-stu-id="f4be3-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="f4be3-134">Belge yönetimini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f4be3-134">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)

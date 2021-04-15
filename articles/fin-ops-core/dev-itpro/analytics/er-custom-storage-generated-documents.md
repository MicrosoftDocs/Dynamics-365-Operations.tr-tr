---
title: Oluşturulan belgeler için özel depolama konumu belirtin
description: Bu konu, Elektronik raporlama (ER) biçimlerinin oluşturduğu belgeler için depolama konumlarının listesini genişletmeyi açıklar.
author: NickSelin
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: dab70b213efc7e7a3537aa2b47b9edf38d492d34
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753732"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a><span data-ttu-id="e492e-103">Oluşturulan belgeler için özel depolama konumu belirtin</span><span class="sxs-lookup"><span data-stu-id="e492e-103">Specify a custom storage location for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e492e-104">Elektronik raporlama (ER) çerçevesinin Uygulama programlama arabirimi (API), ER biçimlerinin oluşturduğu depolama konumlarını genişletmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="e492e-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="e492e-105">Bu konu, özel bir depolama konumu eklemek için tamamlamanız gereken ana görevlerin genel bakışını içerir.</span><span class="sxs-lookup"><span data-stu-id="e492e-105">This topic includes an overview of the main tasks that you must complete to add a custom storage location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e492e-106">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="e492e-106">Prerequisites</span></span>

<span data-ttu-id="e492e-107">Sürekli yapılandırma destekleyen bir topoloji dağıtmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e492e-107">You must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="e492e-108">(Daha fazla bilgi için bkz. [Sürekli yapılandırma ve test otomasyonu destekleyen topolojiler dağıtın](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) Bu topolojiye aşağıdaki rollerden biriyle erişiminiz olması gerekir:</span><span class="sxs-lookup"><span data-stu-id="e492e-108">(For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="e492e-109">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="e492e-109">Electronic reporting developer</span></span>
- <span data-ttu-id="e492e-110">Elektronik raporlama işlev danışmanı</span><span class="sxs-lookup"><span data-stu-id="e492e-110">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="e492e-111">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="e492e-111">System administrator</span></span>

<span data-ttu-id="e492e-112">Bu topoloji için geliştirme ortamına da erişiminiz olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="e492e-112">You must also have access to the development environment for this topology.</span></span>

## <a name="create-or-import-an-er-format-configuration"></a><span data-ttu-id="e492e-113">Bir ER biçimi yapılandırması oluşturun veya içe aktarın</span><span class="sxs-lookup"><span data-stu-id="e492e-113">Create or import an ER format configuration</span></span>

<span data-ttu-id="e492e-114">Geçerli topolojide [yeni bir ER biçimi oluşturun](tasks/er-format-configuration-2016-11.md) bu sayede bir özel depolama konumu ekleyebileceğiniz belgeler oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e492e-114">In the current topology, [create a new ER format](tasks/er-format-configuration-2016-11.md) to generate documents that you plan to add a custom storage location for.</span></span> <span data-ttu-id="e492e-115">Alternatif olarak [bu topolojiye mevcut bir ER biçimi içe aktarın](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="e492e-115">Alternatively, [import an existing ER format into this topology](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![Biçim tasarımcısı sayfası](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> <span data-ttu-id="e492e-117">Oluşturduğunuz veya içe aktardığınız ER biçimi, aşağıdaki biçim öğelerinden en az birini içermelidir:</span><span class="sxs-lookup"><span data-stu-id="e492e-117">The ER format that you create or import must contain at least one of the following format elements:</span></span>
>
> - <span data-ttu-id="e492e-118">Dosya</span><span class="sxs-lookup"><span data-stu-id="e492e-118">File</span></span>
> - <span data-ttu-id="e492e-119">Klasör</span><span class="sxs-lookup"><span data-stu-id="e492e-119">Folder</span></span>
> - <span data-ttu-id="e492e-120">Birleştirici</span><span class="sxs-lookup"><span data-stu-id="e492e-120">Merger</span></span>
> - <span data-ttu-id="e492e-121">Ek</span><span class="sxs-lookup"><span data-stu-id="e492e-121">Attachment</span></span>

## <a name="create-a-new-document-type"></a><span data-ttu-id="e492e-122">Yeni bir belge tipi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e492e-122">Create a new document type</span></span>

<span data-ttu-id="e492e-123">Bir ER biçiminin oluşturduğu belgelerin nasıl yönlendirileceğini belirtmek için [Elektronik raporlama (ER) hedefleri](electronic-reporting-destinations.md) yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e492e-123">To specify how documents that an ER format generates are routed, you must configure [Electronic reporting (ER) destinations](electronic-reporting-destinations.md).</span></span> <span data-ttu-id="e492e-124">Oluşturulan belgeleri dosyalar olarak depolamak için yapılandırılmış her ER hedefinde, Belge yönetimi çerçevesinin belge türünü belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e492e-124">In each ER destination that is configured to store generated documents as files, you must specify a document type of the Document management framework.</span></span> <span data-ttu-id="e492e-125">Farklı belge türleri farklı ER biçimlerinin oluşturduğu belgeleri yönlendirmekte kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e492e-125">Different document types can be used to route documents that different ER formats generate.</span></span>

1. <span data-ttu-id="e492e-126">Daha önceden oluşturduğunuz veya içe aktardığınız ER biçimi için yeni bir [belge türü](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e492e-126">Add a new [document type](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) for the ER format that you created or imported earlier.</span></span> <span data-ttu-id="e492e-127">Aşağıdaki örnekte, belge türü **FileX**'tir.</span><span class="sxs-lookup"><span data-stu-id="e492e-127">In the illustration that follows, the document type is **FileX**.</span></span>
2. <span data-ttu-id="e492e-128">Bu belge türünü diğer belge türlerinden ayırt etmek için adında belirli bir anahtar kelime dahil edin.</span><span class="sxs-lookup"><span data-stu-id="e492e-128">To differentiate this document type from other document types, include a specific keyword in its name.</span></span> <span data-ttu-id="e492e-129">Örneğin, aşağıdaki görselde, adı **(LOCAL) folder**'dır.</span><span class="sxs-lookup"><span data-stu-id="e492e-129">For example, in the illustration that follows, the name is **(LOCAL) folder**.</span></span>
3. <span data-ttu-id="e492e-130">**Sınıf** alanında, **Dosya ekle** belirtin.</span><span class="sxs-lookup"><span data-stu-id="e492e-130">In the **Class** field, specify **Attach file**.</span></span>
4. <span data-ttu-id="e492e-131">**Grup** alanında, **Dosya** belirtin.</span><span class="sxs-lookup"><span data-stu-id="e492e-131">In the **Group** field, specify **File**.</span></span>

![Belge türleri sayfası](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> <span data-ttu-id="e492e-133">Belge türleri şirkete özeldir.</span><span class="sxs-lookup"><span data-stu-id="e492e-133">Document types are company-specific.</span></span> <span data-ttu-id="e492e-134">Yapılandırılan hedefle ER biçimini birden fazla şirkette kullanmak için her bir şirkette ayrı bir belge türü yapılandırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="e492e-134">To use an ER format with a configured destination in multiple companies, you must configure a separate document type in each company.</span></span>

## <a name="review-source-code"></a><span data-ttu-id="e492e-135">Kaynak kod gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="e492e-135">Review source code</span></span>

<span data-ttu-id="e492e-136">**ERDocuManagement** sınıfının **insertFile()** yönteminin kodunu gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="e492e-136">Review the code of the **insertFile()** method of the **ERDocuManagement** class.</span></span> <span data-ttu-id="e492e-137">**AttachingFile()** olayının, oluşturulan dosya bir kayda eklendiğinde oluştuğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="e492e-137">Notice that the **AttachingFile()** event is raised while the generated file is attached to a record.</span></span>


```xpp
/// <summary>
/// Inserts file as attachment in Document Management.
/// </summary>
/// <param name = "_owner">A record as the attachment owner.</param>
/// <param name = "_stream">The file stream.</param>
/// <param name = "_filePath">The file path with name.</param>
/// <param name = "_attachmentName">The name of file attachment.</param>
/// <returns>The reference to inserted file.</returns>
[Hookable(false)]
public DocuRef insertFile(
    Common _owner, 
    System.IO.Stream _stream, 
    str _filePath, 
    str _attachmentName, 
    DocuTypeId _docuTypeId)
{
    DocuRef docuRef;
    if (_stream)
    {
        DocuType::createDefaults();
        if (!this.isDocuTypeValid(_docuTypeId))
        {
            throw error(strFmt("@ElectronicReporting:DocuTypeIsNotValid", _docuTypeId));
        }
        var args = ERDocuManagementAttachingFileEventArgs::construct(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        ERDocuManagementEvents::onAttachingFile(args);
        if (args.isHandled())
        {
            docuRef = args.getDocuRef();
        }
        else
        {
            docuRef = this.attachFile(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        }
    }
    return docuRef;
}
```

<span data-ttu-id="e492e-138">**AttachingFile()** olayı aşağıdaki ER hedefleri işlendiğinde gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="e492e-138">The **AttachingFile()** event is raised when the following ER destinations are processed:</span></span>

- <span data-ttu-id="e492e-139">**Arşiv** – Bu hedef kullanıldığında ERFormatMappingRunJobTable tablosunda oluşturulan ER biçimi için yeni bir kayıt çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="e492e-139">**Archive** – When this destination is used, a new record for the ER format that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="e492e-140">Bu kayıttaki **Arşiv** alanı **Hatalı**'dır.</span><span class="sxs-lookup"><span data-stu-id="e492e-140">The **Archived** field in this record is set to **False**.</span></span> <span data-ttu-id="e492e-141">ER biçimi başarıyla çalışırsa, oluşturulan belge bu kayda eklenir ve **AttachingFile()** olayı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e492e-141">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="e492e-142">Bu ER hedefinde seçilen belge türü, eklenen dosyanın depolama konumunu belirle (Microsoft Azure Depolama veya bir Microsoft SharePoint klasörü).</span><span class="sxs-lookup"><span data-stu-id="e492e-142">The document type that is selected in this ER destination determines the storage location for the attached file (Microsoft Azure Storage or a Microsoft SharePoint folder).</span></span>
- <span data-ttu-id="e492e-143">**İş arşivi** – Bu hedef kullanıldığında ERFormatMappingRunJobTable tablosunda oluşturulan ER formunda için yeni bir kayıt çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="e492e-143">**Job archive** – When this destination is used, a new record for the ER form that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="e492e-144">Bu kayıttaki **Arşiv** alanı **Doğru**'dır.</span><span class="sxs-lookup"><span data-stu-id="e492e-144">The **Archived** field in this record is set to **True**.</span></span> <span data-ttu-id="e492e-145">ER biçimi başarıyla çalışırsa, oluşturulan belge bu kayda eklenir ve **AttachingFile()** olayı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e492e-145">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="e492e-146">ER parametrelerinde yapılandırılan belge türü, iliştirilen dosya için depolama konumunu belirler (Azure Depolama veya bir SharePoint klasörü).</span><span class="sxs-lookup"><span data-stu-id="e492e-146">The document type that is configured in the ER parameters determines the storage location for the attached file (Azure Storage or a SharePoint folder).</span></span>

![Elektronik raporlama parametreleri sayfası](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a><span data-ttu-id="e492e-148">Bir ER hedefini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="e492e-148">Configure an ER destination</span></span>

1. <span data-ttu-id="e492e-149">Oluşturduğunuz veya içe aktardığınız ER biçiminin önceden belirtilen öğelerden biri için (dosya, klasörü, birleştirme veya ek) arşivlenen hedefleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="e492e-149">Configure the archived destination for one of the previously mentioned elements (file, folder, merger, or attachment) of the ER format that you created or imported.</span></span> <span data-ttu-id="e492e-150">Yönergeler için bkz. [ER Yapılandır hedefler](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span><span class="sxs-lookup"><span data-stu-id="e492e-150">For guidance, see [ER Configure destinations](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span></span>
2. <span data-ttu-id="e492e-151">Yapılandırılan hedef için daha önce eklediğiniz belge türünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="e492e-151">Use the document type that you added earlier for the configured destination.</span></span> <span data-ttu-id="e492e-152">(Bu konudaki örnek için, belge türü **FileX**'tir.)</span><span class="sxs-lookup"><span data-stu-id="e492e-152">(For the example in this topic, the document type is **FileX**.)</span></span>

![Hedef ayarları iletişim kutusu](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a><span data-ttu-id="e492e-154">Kaynak kodu değiştir</span><span class="sxs-lookup"><span data-stu-id="e492e-154">Modify source code</span></span>

1. <span data-ttu-id="e492e-155">Microsoft Visual Studio projenize yeni bir sınıf ekleyin ve daha önceden belirtilen **AttachingFile()** etkinliğine abone olmak için kodu yazın.</span><span class="sxs-lookup"><span data-stu-id="e492e-155">Add a new class to your Microsoft Visual Studio project, and write code to subscribe to the **AttachingFile()** event that was mentioned earlier.</span></span> <span data-ttu-id="e492e-156">(Kullanılan genişletilebilirlik modeli hakkında daha fazla bilgi için bkz. [EventHandlerResult kullanarak yanıtla](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) Örneğin, yeni sınıfta, aşağıdaki eylemleri gerçekleştiren kodu yazın:</span><span class="sxs-lookup"><span data-stu-id="e492e-156">(For more information about the extensibility pattern that is used, see [Respond by using EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) For example, in the new class, write code that performs the following actions:</span></span>

    1. <span data-ttu-id="e492e-157">Oluşturulan dosyaları, Application Object Server (AOS) servisini çalıştıran sunucunun yerel dosya sisteminin bir klasöründe depolayın.</span><span class="sxs-lookup"><span data-stu-id="e492e-157">Store generated files in a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    2. <span data-ttu-id="e492e-158">Bu oluşturulan dosyaları yalnızca yeni belge türü (örneğin, adında "(LOCAL)" anahtar kelimesini içeren **FileX** türü) kullanıldığında, bir dosya ER çalıştırma iş günlüğünün kaydına eklendiğinde.</span><span class="sxs-lookup"><span data-stu-id="e492e-158">Store these generated files only when the new document type (for example, the **FileX** type that has the "(LOCAL)" keyword in its name) is used while a file is attached to the record in the ER execution job log.</span></span>

    ```xpp
    class ERDocuSubscriptionSample
    {
        void new()
        {
        }
        [SubscribesTo(classStr(ERDocuManagementEvents), 
        staticDelegateStr(ERDocuManagementEvents, 
        attachingFile))]
        public static void ERDocuManagementEvents_attachingFile(ERDocuManagementAttachingFileEventArgs _args)
        {
            if (!_args.isHandled())
            {
                DocuType docuType = DocuType::find(_args.getDocuTypeId());
                if (strContains(docuType.Name, '(LOCAL)'))
                {
                    _args.markAsHandled();
                    var stream = _args.getStream();
                    if (stream.CanSeek)
                    {
                        stream.Seek(0, System.IO.SeekOrigin::Begin);
                    }
                    using (var localStream = System.IO.File::OpenWrite(@'c:\0\' + _args.getAttachmentName()))
                    {
                        stream.CopyTo(localStream);
                    }
                }
            }
        }
    }
    ```

2. <span data-ttu-id="e492e-159">Projenizi yeniden inşa edin.</span><span class="sxs-lookup"><span data-stu-id="e492e-159">Rebuild your project.</span></span>

## <a name="run-the-er-format-that-you-created-or-imported"></a><span data-ttu-id="e492e-160">Oluşturduğunuz veya içe aktardığınız ER biçimini yürütün</span><span class="sxs-lookup"><span data-stu-id="e492e-160">Run the ER format that you created or imported</span></span>

1. <span data-ttu-id="e492e-161">Oluşturduğunuz veya içe aktardığınız ER biçimini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="e492e-161">Execute the ER format that you created or imported.</span></span>
2. <span data-ttu-id="e492e-162">**Organizasyon yönetimi \> Elektronik raporlama \> Elektronik raporlama işleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e492e-162">Go to **Organization administration \> Electronic reporting \> Electronic reporting jobs**.</span></span> <span data-ttu-id="e492e-163">Bu yürütme işi için oluşturulan ve oluşturulan dosyanın eklenmiş olduğu kaydı bulun.</span><span class="sxs-lookup"><span data-stu-id="e492e-163">Find the record that was created for this execution job, and that has the generated file attached to it.</span></span>
3. <span data-ttu-id="e492e-164">Oluşturulan aynı dosyayı bulmak için yerel **C:\\0** klasörünü gezin.</span><span class="sxs-lookup"><span data-stu-id="e492e-164">Explore the local **C:\\0** folder to find same generated file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e492e-165">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e492e-165">Additional resources</span></span>

- [<span data-ttu-id="e492e-166">Elektronik raporlama (ER) hedefleri</span><span class="sxs-lookup"><span data-stu-id="e492e-166">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="e492e-167">Genişletilebilirlik giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="e492e-167">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
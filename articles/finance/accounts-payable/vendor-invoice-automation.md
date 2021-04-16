---
title: Taranan belgeler için fatura otomasyonu
description: Bu konu ekler içeren faturalar da dahil olmak üzere satıcı faturalarının uçtan uca otomasyonu için kullanılabilir olan özellikleri açıklar.
author: abruer
ms.date: 03/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoiceHeaderStagingListPage
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d776ad4eda623f55a69d81eefd0e88842d9da401
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841249"
---
# <a name="invoice-automation-for-scanned-documents"></a><span data-ttu-id="a9022-103">Taranan belgeler için fatura otomasyonu</span><span class="sxs-lookup"><span data-stu-id="a9022-103">Invoice automation for scanned documents</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9022-104">Bu konu ekler içeren faturalar da dahil olmak üzere satıcı faturalarının uçtan uca otomasyonu için kullanılabilir olan veri varlıklarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="a9022-104">This topic explains the data entities that are available for end-to-end automation of vendor invoices, including invoices with attachments.</span></span>

<span data-ttu-id="a9022-105">Borç hesapları (AP) işlemlerini daha verimli kullanmak isteyen kuruluşlar genellikle fatura işlemlerini daha etkin olması gereken işlem alanları içinde ne üst sıralardan birine koyar.</span><span class="sxs-lookup"><span data-stu-id="a9022-105">Organizations that want to streamline their Accounts payable (AP) processes often identify invoice processing as one of the top process areas that should be more efficient.</span></span> <span data-ttu-id="a9022-106">Çoğu durumda, bu kuruluşlar kağıt fatura işlemlerini üçüncü taraf bir optik karakter tanıma (OCR) servis sağlayıcısına aktarırlar.</span><span class="sxs-lookup"><span data-stu-id="a9022-106">In many cases, these organizations offload the processing of paper invoices to a third-party optical character recognition (OCR) service provider.</span></span> <span data-ttu-id="a9022-107">Daha sonra her faturanın taranan görüntüsüyle birlikte makine tarafından okunabilir fatura meta verilerini alırlar.</span><span class="sxs-lookup"><span data-stu-id="a9022-107">They then receive machine-readable invoice metadata together with a scanned image of each invoice.</span></span> <span data-ttu-id="a9022-108">Otomasyona yardımcı olmak için "son mil" çözümü faturalama sisteminde bu yapıların kullanımını etkinleştirmek için oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="a9022-108">To help with automation, a “last mile” solution is then built to enable consumption of these artifacts in the invoicing system.</span></span> <span data-ttu-id="a9022-109">Şimdi bu "son mil" otomasyonu, bir fatura otomasyon çözümüyle kullanıma hazır hale getirilmektedir.</span><span class="sxs-lookup"><span data-stu-id="a9022-109">Now this “last mile” automation is enabled out of the box, through an invoice automation solution.</span></span>

## <a name="solution-context"></a><span data-ttu-id="a9022-110">Çözüm bağlamı</span><span class="sxs-lookup"><span data-stu-id="a9022-110">Solution context</span></span>

<span data-ttu-id="a9022-111">Fatura otomasyon çözümü, fatura başlığı ve fatura satırları ve faturayla ilgili ekler için fatura meta verilerini kabul edebilen standart bir arabirim sunar.</span><span class="sxs-lookup"><span data-stu-id="a9022-111">The invoice automation solution enables a standard interface that can accept invoice metadata for the invoice header and invoice lines, and also attachments that are applicable to the invoice.</span></span> <span data-ttu-id="a9022-112">Bu arabirimle uyumlu yapılar oluşturabilen her dış sistem, fatura ve eklerin otomatik işlenmesi için akışı gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="a9022-112">Any external system that can generate artifacts that comply with this interface will be able to send the feed for automatic processing of invoices and attachments.</span></span>

<span data-ttu-id="a9022-113">Aşağıda Contoso'nun satıcı faturası işleme için bir OCR hizmet sağlayıcısı ile ortaklık kurduğu basit bir tümleştirme senaryosu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="a9022-113">The following illustration shows a sample integration scenario where Contoso has partnered with an OCR service provider for vendor invoice processing.</span></span> <span data-ttu-id="a9022-114">Contoso satıcıları servis sağlayıcısına faturaları e-posta ile gönderir.</span><span class="sxs-lookup"><span data-stu-id="a9022-114">Contoso’s vendors send invoices to the service provider by email.</span></span> <span data-ttu-id="a9022-115">OCR işlemi aracılığıyla, hizmet sağlayıcısı fatura meta verilerini (başlığı ve/veya satırlar) ve taranan fatura görüntüsünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9022-115">Through OCR processing, the service provider generates invoice metadata (header and/or lines) and a scanned image of the invoice.</span></span> <span data-ttu-id="a9022-116">Bunun ardından bir tümleştirme katmanı bu yapıları dönüştürerek kullanılabilir hale getirir.</span><span class="sxs-lookup"><span data-stu-id="a9022-116">An integration layer then transforms these artifacts so that they can be consumed.</span></span>

![Basit tümleştirme senaryosu](media/vendor_invoice_automation_01.png)

<span data-ttu-id="a9022-118">Fatura tümleştirme gerektiğinde önceki senaryonun çeşitli kullanımları mümkün olabilir.</span><span class="sxs-lookup"><span data-stu-id="a9022-118">Several variations of the preceding scenario are possible if invoice integration is required.</span></span> <span data-ttu-id="a9022-119">Veri geçiş işlemleri; faturaları ve eklerini oluşturmak için bu arabirimin kullanılabileceği başka bir kullanım örneğidir.</span><span class="sxs-lookup"><span data-stu-id="a9022-119">Data migration is another use case where this interface can be used to create invoices and attachments.</span></span>

### <a name="solution-components"></a><span data-ttu-id="a9022-120">Çözüm bileşenleri</span><span class="sxs-lookup"><span data-stu-id="a9022-120">Solution components</span></span>

<span data-ttu-id="a9022-121">Çözümün temeli aşağıdaki bileşenlerden oluşur:</span><span class="sxs-lookup"><span data-stu-id="a9022-121">The solution footprint consists of the following components:</span></span>

+ <span data-ttu-id="a9022-122">Fatura başlığı, fatura satırları ve fatura ekleri için veri varlıkları</span><span class="sxs-lookup"><span data-stu-id="a9022-122">Data entities for the invoice header, invoice lines, and invoice attachments</span></span>
+ <span data-ttu-id="a9022-123">Faturalar için özel durum işleme</span><span class="sxs-lookup"><span data-stu-id="a9022-123">Exception processing for invoices</span></span>
+ <span data-ttu-id="a9022-124">Faturalarda yan yana ek görüntüleyici</span><span class="sxs-lookup"><span data-stu-id="a9022-124">A side-by-side attachment viewer in invoices</span></span>

<span data-ttu-id="a9022-125">Bu konunun kalan kısmında bu çözüm bileşenlerinin ayrıntılı açıklamaları verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="a9022-125">The rest of this topic provides detailed descriptions of these solution components.</span></span>

## <a name="data-entities"></a><span data-ttu-id="a9022-126">Veri varlıkları</span><span class="sxs-lookup"><span data-stu-id="a9022-126">Data entities</span></span>

<span data-ttu-id="a9022-127">Veri paketi, fatura başlıklarının, fatura satırlarının ve fatura eklerinin oluşturulabilmesi için gönderilmesi gereken iş birimidir.</span><span class="sxs-lookup"><span data-stu-id="a9022-127">A data package is the unit of work that must be sent so that invoice headers, invoice lines, and invoice attachments can be created.</span></span> <span data-ttu-id="a9022-128">Aşağıdaki veri varlıkları veri paketini oluşturan yapılan için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="a9022-128">The following data entities are used for the artifacts that make up the data package:</span></span>

+ <span data-ttu-id="a9022-129">Satıcı faturası başlığı</span><span class="sxs-lookup"><span data-stu-id="a9022-129">Vendor invoice header</span></span>
+ <span data-ttu-id="a9022-130">Satıcı faturası satırı</span><span class="sxs-lookup"><span data-stu-id="a9022-130">Vendor invoice line</span></span>
+ <span data-ttu-id="a9022-131">Satıcı faturası belge eki</span><span class="sxs-lookup"><span data-stu-id="a9022-131">Vendor invoice document attachment</span></span>

<span data-ttu-id="a9022-132">Satıcı fatura belgesi eki bu özelliğin bir parçası olarak sunulan yeni bir veri varlığıdır.</span><span class="sxs-lookup"><span data-stu-id="a9022-132">Vendor invoice document attachment is a new data entity that is introduced as part of this feature.</span></span> <span data-ttu-id="a9022-133">Satıcı fatura başlığı varlığı ekleri desteleyecek şekilde değiştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="a9022-133">The Vendor invoice header entity has been modified so that it supports attachments.</span></span> <span data-ttu-id="a9022-134">Satıcı fatura satırı varlığı bu özellik için değiştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="a9022-134">The Vendor invoice line entity hasn’t been modified for this feature.</span></span>

<span data-ttu-id="a9022-135">Veri paketleri hakkında ayrıntılı bilgi için bkz. [Veri yönetimine genel bakış](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="a9022-135">For detailed information about data packages, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span> <span data-ttu-id="a9022-136">Veri paketlerinin veri yönetimi çalışma alanını kullanılarak nasıl oluşturulacağı hakkında bilgi için bkz. [Dynamics 365 Finance and Operations uygulama çözümünde veri paketlerini işleme ve kullanma](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="a9022-136">For information about how to create data packages using the data management workspace, see [Process and consume data packages in Dynamics 365 Finance and Operations apps solution](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md).</span></span>

<span data-ttu-id="a9022-137">Faturaları ve ekleri içeren test verilerini hızla oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a9022-137">To quickly generate test data that includes invoices and attachments, follow these steps.</span></span>

1. <span data-ttu-id="a9022-138">Örneğinizde oturum açın.</span><span class="sxs-lookup"><span data-stu-id="a9022-138">Sign in to your instance.</span></span>
1. <span data-ttu-id="a9022-139">**Borç hesapları** > **Faturalar** > **Bekleyen satıcı faturaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="a9022-139">Go to **Accounts payables** > **Invoices** > **Pending vendor invoices**.</span></span>
1. <span data-ttu-id="a9022-140">Satırları ve ekleri olan faturalar oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a9022-140">Create invoices that have lines and attachments.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a9022-141">Ekler başlık ekleri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a9022-141">The attachments must be header attachments.</span></span> <span data-ttu-id="a9022-142">Şu anda Satıcı faturası belge eki varlığı satır eklerini desteklememektedir.</span><span class="sxs-lookup"><span data-stu-id="a9022-142">Currently, the Vendor invoice document attachment entity doesn’t support line attachments.</span></span>

1. <span data-ttu-id="a9022-143">**Veri yönetimi** çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="a9022-143">Open the **Data management** workspace.</span></span>
1. <span data-ttu-id="a9022-144">Satıcı faturası başlığı, Satıcı faturası satırı ve Satıcı faturası belge eki varlıkları içeren bir dışa aktarma işi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a9022-144">Create an export job that includes the Vendor invoice header, Vendor invoice line, and Vendor invoice document attachment entities.</span></span>
1. <span data-ttu-id="a9022-145">Verileri dışa aktarın.</span><span class="sxs-lookup"><span data-stu-id="a9022-145">Export the data.</span></span>
1. <span data-ttu-id="a9022-146">Dışa aktarılan verileri paket olarak indirin.</span><span class="sxs-lookup"><span data-stu-id="a9022-146">Download the exported data as a package.</span></span> <span data-ttu-id="a9022-147">Şimdi paketi test amacıyla verileri hedef kurulumlara aktarmak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9022-147">You can now use the package to import data into target instances for testing purposes.</span></span>

### <a name="determining-the-legal-entity-for-an-invoice"></a><span data-ttu-id="a9022-148">Bir fatura için tüzel kişilik belirleme</span><span class="sxs-lookup"><span data-stu-id="a9022-148">Determining the legal entity for an invoice</span></span>

<span data-ttu-id="a9022-149">Veri paketleriyle içe aktarılan faturalar ait oldukları tüzel kişilikle iki şekilde ilişkilendirilebilir:</span><span class="sxs-lookup"><span data-stu-id="a9022-149">Invoices that are imported via data packages can be associated with the legal entity that they belong to in two ways:</span></span>

+ <span data-ttu-id="a9022-150">Faturayı işleyen içe aktarma işlemi faturayı işin **Veri yönetimi** çalışma alanında planlandığı aynı şirkete aktarır.</span><span class="sxs-lookup"><span data-stu-id="a9022-150">The import job that processes the invoice imports it into the same company in which the job was scheduled in the **Data management** workspace.</span></span> <span data-ttu-id="a9022-151">Başka bir deyişle, işin şirketi faturanın ait olduğu şirketi belirler.</span><span class="sxs-lookup"><span data-stu-id="a9022-151">In other words, the company of the job determines the company that the invoice belongs to.</span></span>
+ <span data-ttu-id="a9022-152">Faturaları içeren veri paketi Finance'e gönderildiğinde, arayan (yani Finance dışında çalışan tümleştirme uygulaması) HTTP isteğinde şirket kodunu açık şekilde belirtebilir.</span><span class="sxs-lookup"><span data-stu-id="a9022-152">When the data package that contains invoices is sent to Finance, the caller (that is, the integration application that runs outside of Finance) can explicitly mention the company ID in the HTTP request.</span></span> <span data-ttu-id="a9022-153">Bu durumda, Finance'te işleme işinin çalıştığı şirket bağlamı geçersiz kılınır ve faturalar HTTP isteğiyle geçirilen şirket için içe aktarılır.</span><span class="sxs-lookup"><span data-stu-id="a9022-153">In this case, the company context in which the processing job runs in Finance is overridden, and the invoices are imported into the company that was passed via the HTTP request.</span></span>

> [!NOTE]
> <span data-ttu-id="a9022-154">Bu davranış standart veri yönetimi davranışıdır.</span><span class="sxs-lookup"><span data-stu-id="a9022-154">This behavior is standard data management behavior.</span></span> <span data-ttu-id="a9022-155">Burada, faturalar bağlamında, yalnızca bütünlük açısından açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="a9022-155">It’s explained here, in the context of invoices, just for the sake of completeness.</span></span>

## <a name="exception-processing"></a><span data-ttu-id="a9022-156">Özel durum işleme</span><span class="sxs-lookup"><span data-stu-id="a9022-156">Exception processing</span></span>

<span data-ttu-id="a9022-157">Satıcı faturalarının Finance and Operations'a tümleştirme yoluyla geldiği senaryolarda, Borç hesapları ekibi üyesinin özel durumları veya başarısız olan faturaları işlemesi ve başarısız faturalardan bekleyen faturalar oluşturması için kolay bir yol olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a9022-157">In scenarios where vendor invoices come into Finance and Operations via integration, there must be an easy way for an Accounts payable team member to process exceptions or failed invoices, and to create pending invoices out of failed invoices.</span></span> <span data-ttu-id="a9022-158">Satıcı faturaları için bu özel durum işleme özelliği artık Finance and Operations'ın bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="a9022-158">This exception processing for vendor invoices is now part of Finance and Operations.</span></span>

### <a name="vendor-invoices-that-failed-to-import-list-page"></a><span data-ttu-id="a9022-159">İçe aktarılamayan satıcı faturaları liste sayfası</span><span class="sxs-lookup"><span data-stu-id="a9022-159">Vendor invoices that failed to import list page</span></span>

<span data-ttu-id="a9022-160">Özel durumlar için yeni liste sayfası **Borç hesapları** > **Faturalar** > **İçe aktarma hataları** > **İçe aktarılamayan satıcı faturaları**'nda bulunur.</span><span class="sxs-lookup"><span data-stu-id="a9022-160">The new list page for invoice exceptions is available at **Accounts payable** > **Invoices** > **Import failures** > **Vendor invoices that failed to import**.</span></span> <span data-ttu-id="a9022-161">Bu sayfa, Satıcı fatura başlık verileri varlığının aşamalandırma tablosundaki tüm satıcı faturası başlığı kayıtlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9022-161">This page shows all the vendor invoice header records from the staging table of the Vendor invoice header data entity.</span></span> <span data-ttu-id="a9022-162">Aynı kayıtları **veri yönetimi** çalışma alanından görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9022-162">Note that you can view the same records from the **Data management** workspace.</span></span> <span data-ttu-id="a9022-163">Özel durum işleme özelliğinde sunulan aynı işlemleri **Veri yönetimi** çalışma alanından da gerçekleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9022-163">You can also perform the same actions that are provided in the exception handling feature from the **Data management** workspace.</span></span> <span data-ttu-id="a9022-164">Özel durum işleme özelliği işlevsel bir kullanıcı için en iyi duruma getirildi, bu da kullanımını kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="a9022-164">The exception handling feature has been optimized for a functional user, which makes it easier to use.</span></span>

![Özel durumlar listesi sayfası](media/vendor_invoice_automation_02.png)

<span data-ttu-id="a9022-166">Bu liste sayfası akış ile gelen aşağıdaki alanları içerir:</span><span class="sxs-lookup"><span data-stu-id="a9022-166">This list page includes the following fields that come in via the feed:</span></span>

+ <span data-ttu-id="a9022-167">**Şirket** – Faturanın ait olduğu şirket</span><span class="sxs-lookup"><span data-stu-id="a9022-167">**Company** – The company that the invoice belongs to</span></span>
+ <span data-ttu-id="a9022-168">**Hata iletisi** – Faturanın neden oluşturulamadığını açıklayan veri yönetimi çerçevesi sorunlarına ilişkin hata iletisi</span><span class="sxs-lookup"><span data-stu-id="a9022-168">**Error message** – The error message that the data management framework issues to explain why the invoice could not be created</span></span>
+ <span data-ttu-id="a9022-169">**Numara** – Fatura numarası</span><span class="sxs-lookup"><span data-stu-id="a9022-169">**Number** – The invoice number</span></span>
+ <span data-ttu-id="a9022-170">**Fatura hesabı**</span><span class="sxs-lookup"><span data-stu-id="a9022-170">**Invoice account**</span></span>
+ <span data-ttu-id="a9022-171">**Ad** - Satıcının adı</span><span class="sxs-lookup"><span data-stu-id="a9022-171">**Name** – The vendor’s name</span></span>
+ <span data-ttu-id="a9022-172">**Satıcı hesabı**</span><span class="sxs-lookup"><span data-stu-id="a9022-172">**Vendor account**</span></span>
+ <span data-ttu-id="a9022-173">**Satınalma siparişi** - Fatura için satın alma siparişi (PO) numarası</span><span class="sxs-lookup"><span data-stu-id="a9022-173">**Purchase order** – The purchase order (PO) number for the invoice</span></span>
+ <span data-ttu-id="a9022-174">**Deftere nakil tarihi**</span><span class="sxs-lookup"><span data-stu-id="a9022-174">**Posting date**</span></span>
+ <span data-ttu-id="a9022-175">**Fatura tarihi**</span><span class="sxs-lookup"><span data-stu-id="a9022-175">**Invoice date**</span></span>
+ <span data-ttu-id="a9022-176">**Fatura açıklaması**</span><span class="sxs-lookup"><span data-stu-id="a9022-176">**Invoice description**</span></span>
+ <span data-ttu-id="a9022-177">**Para birimi**</span><span class="sxs-lookup"><span data-stu-id="a9022-177">**Currency**</span></span>
+ <span data-ttu-id="a9022-178">**Günlük**</span><span class="sxs-lookup"><span data-stu-id="a9022-178">**Log**</span></span>
+ <span data-ttu-id="a9022-179">**Satır referansı** – Dış sistemden gelen tanımlayıcı</span><span class="sxs-lookup"><span data-stu-id="a9022-179">**Line reference** – The identifier that comes from the external system</span></span>

    > [!NOTE]
    > <span data-ttu-id="a9022-180">Referans satırı fatura kodu değildir.</span><span class="sxs-lookup"><span data-stu-id="a9022-180">The line reference isn’t the invoice ID.</span></span>

<span data-ttu-id="a9022-181">Bu liste sayfasında aşağıdaki şekillerde kullanabileceğiniz bir önizleme bölmesi de vardır:</span><span class="sxs-lookup"><span data-stu-id="a9022-181">This list page also has a preview pane that you can used in the following ways:</span></span>

+ <span data-ttu-id="a9022-182">Tam hata iletisini görmek - Böylece ızgaradaki **Kata iletisi** sütununu genişletmeniz gerekmez.</span><span class="sxs-lookup"><span data-stu-id="a9022-182">View the whole error message, so that you don’t have to expand the **Error message** column in the grid.</span></span>

<span data-ttu-id="a9022-183">Liste sayfası aşağıdaki eylemleri destekler:</span><span class="sxs-lookup"><span data-stu-id="a9022-183">The list page supports the following actions:</span></span>

+ <span data-ttu-id="a9022-184">**Düzenle** – Sorunları gidermek için özel durum kaydını düzenleme modunda açın.</span><span class="sxs-lookup"><span data-stu-id="a9022-184">**Edit** – Open the exception record in edit mode, so that you can fix the issues.</span></span>
+ <span data-ttu-id="a9022-185">**Seçenekler** – Liste sayfalarında kullanılabilir olan standart seçeneklere erişin.</span><span class="sxs-lookup"><span data-stu-id="a9022-185">**Options** – Access the standard options that are available on list pages.</span></span> <span data-ttu-id="a9022-186">Özel durumlar liste sayfasını çalışma alanınıza liste veya kutucuk olarak sabitlemek için **Çalışma alanına ekle** seçeneğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9022-186">You can use the **Add to workspace** option to pin the exceptions list page to your workspace as a list or tile.</span></span>

### <a name="vendor-invoices-that-failed-to-import-details-page"></a><span data-ttu-id="a9022-187">İçe aktarılamayan satıcı faturaları ayrıntı sayfası</span><span class="sxs-lookup"><span data-stu-id="a9022-187">Vendor invoices that failed to import details page</span></span>

<span data-ttu-id="a9022-188">Düzenleme modunu başlattığınızda, sorunları olan faturanın **İçe aktarılamayan satıcı faturaları ayrıntıları** sayfası açılır.</span><span class="sxs-lookup"><span data-stu-id="a9022-188">When you start edit mode, the **Vendor invoices that failed to import details** page for the invoice that has issues will open.</span></span> <span data-ttu-id="a9022-189">Eki olan bir faturada sorunlar varsa, ek görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="a9022-189">If there are issues with an invoice that has an attachment, the attachment won't be displayed.</span></span> <span data-ttu-id="a9022-190">Ekin faturaya yeniden eklenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="a9022-190">The attachment must be re-attached to the invoice.</span></span>

<span data-ttu-id="a9022-191">**İçe aktarılamayan satıcı faturaları ayrıntıları** sayfası bekleyen bir fatura oluşturmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="a9022-191">The **Vendor invoices that failed to import details** page lets you create a pending invoice.</span></span> <span data-ttu-id="a9022-192">Özel durum işlemenin bir parçası olarak faturadaki sorunları giderdikten sonra, bekleyen fatura oluşturmak için **Bekleyen fatura oluştur** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a9022-192">After you’ve fixed the issues on an invoice as part of processing an exception, select the **Create pending invoice** button to create the pending invoice.</span></span> <span data-ttu-id="a9022-193">Bekleyen fatura arka planda oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a9022-193">The pending invoice will be created in the background.</span></span> 

### <a name="shared-service-vs-organization-based-exception-processing"></a><span data-ttu-id="a9022-194">Paylaşılan hizmetler ile kuruluş tabanlı özel durum işleme karşılaştırması</span><span class="sxs-lookup"><span data-stu-id="a9022-194">Shared service vs. organization-based exception processing</span></span>

<span data-ttu-id="a9022-195">Özel durumlar listesi sayfası **Veri yönetimi** çalışma alanının aşamalandırma kayıtlarını işlemek için desteklediği standart güvenlik yapılarını destekler.</span><span class="sxs-lookup"><span data-stu-id="a9022-195">The exceptions list page supports the standard security constructs that the **Data management** workspace supports for the processing of staging records.</span></span> <span data-ttu-id="a9022-196">Fatura içe aktarma işi aşağıdaki şekillerde güvenlik altına alınabilir:</span><span class="sxs-lookup"><span data-stu-id="a9022-196">The invoice import job can be secured in the following ways:</span></span>

+ <span data-ttu-id="a9022-197">Kullanıcı rolüne göre</span><span class="sxs-lookup"><span data-stu-id="a9022-197">By user role</span></span>
+ <span data-ttu-id="a9022-198">Kullanıcıya göre</span><span class="sxs-lookup"><span data-stu-id="a9022-198">By user</span></span>
+ <span data-ttu-id="a9022-199">Tüzel kişiliğe göre</span><span class="sxs-lookup"><span data-stu-id="a9022-199">By legal entity</span></span>

![Kullanıcı rolüne ve tüzel kişiliğe göre güvenlik altına alınan içer aktarma işlemi](media/vendor_invoice_automation_04.png)

<span data-ttu-id="a9022-201">Fatura içe aktarma işi için güvenlik yapılandırıldıysa, özel durumlar listesi bu ayarları kabul eder.</span><span class="sxs-lookup"><span data-stu-id="a9022-201">If security is configured for the invoice import job, the exceptions list page honors those settings.</span></span> <span data-ttu-id="a9022-202">Kullanıcılar, yalnızca bu kurulumun görmelerine izin verdiği fatura özel durumu kayıtlarını görebilir.</span><span class="sxs-lookup"><span data-stu-id="a9022-202">Users will be able to see only the invoice exception records that this setup allows them to see.</span></span>

<span data-ttu-id="a9022-203">Örneğin, Contoso fatura özel durumlarını tüzel kişiliğe göre işleme kararı verir.</span><span class="sxs-lookup"><span data-stu-id="a9022-203">For example, Contoso has decided to process invoice exceptions by legal entity.</span></span> <span data-ttu-id="a9022-204">Bu nedenle, güvenlik fatura içe aktarma işleminde A tüzel kişiliğindeki kullanıcının yalnızca A tüzel kişiliğindeki fatura özel durumlarını görmesine, B tüzel kişiliğindeki kullanıcının yalnızca B tüzel kişiliğindeki fatura özel durumlarını görmesine izin verecek şekilde yapılandırılır. Bu ayar, fatura özel durumlarının yönetimi için görev ayrımına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="a9022-204">Therefore, security is configured on the invoice import job in such a way that a user in legal entity A can see only invoice exceptions in legal entity A, whereas a user in legal entity B can see only invoice exceptions in legal entity B. This setup enables segregation of duties for the management of invoice exceptions.</span></span>

<span data-ttu-id="a9022-205">Conotoso herhangi bir güvenlik uygulamamaya da karar verebilirdi; bu durumda aynı kullanıcılar tüm tüzel kişiliklere ait fatura özel durumlarıyla işlem yapabilirdi.</span><span class="sxs-lookup"><span data-stu-id="a9022-205">Contoso could also decide not to enforce any security, so that the same users can process invoice exceptions for all legal entities.</span></span> <span data-ttu-id="a9022-206">Bu ayar, fatura özel durumlarının yönetimi için paylaşılan hizmetler senaryosuna olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="a9022-206">This setup enables a shared services scenario for the management of invoice exceptions.</span></span>

## <a name="side-by-side-attachment-viewer"></a><span data-ttu-id="a9022-207">Yan yana ek görüntüleyici</span><span class="sxs-lookup"><span data-stu-id="a9022-207">Side-by-side attachment viewer</span></span>

<span data-ttu-id="a9022-208">Satıcı faturalarındaki ekleri kolaylıkla görebilmeniz için, faturalama işleminde kullanılan aşağıdaki sayfalarda artık bir fatura görüntüleyici sunulmaktadır:</span><span class="sxs-lookup"><span data-stu-id="a9022-208">To help you easily view the attachments for vendor invoices, the following pages that are used in the invoicing process now provide an attachment viewer:</span></span>

+ <span data-ttu-id="a9022-209">**Özel durumları işleme**</span><span class="sxs-lookup"><span data-stu-id="a9022-209">**Exception handling**</span></span>
+ <span data-ttu-id="a9022-210">**Bekleyen satıcı faturaları** sayfası (fatura gözden geçirme işleminde de kullanılabilir)</span><span class="sxs-lookup"><span data-stu-id="a9022-210">**Pending vendor invoices** page (also available in the invoice review process)</span></span>
+ <span data-ttu-id="a9022-211">**Fatura günlüğü** sorgu sayfası (deftere nakledilen faturalar için)</span><span class="sxs-lookup"><span data-stu-id="a9022-211">**Invoice journal** inquiry page (for posted invoices)</span></span>

<span data-ttu-id="a9022-212">Ek görüntüleyicinin sağladığı ana işlevler:</span><span class="sxs-lookup"><span data-stu-id="a9022-212">Here is the main functionality that the attachment viewer provides:</span></span>

+ <span data-ttu-id="a9022-213">Belge yönetiminin desteklediği tümek türlerini görün (dosyalar, görüntüler, URL'ler ve notlar).</span><span class="sxs-lookup"><span data-stu-id="a9022-213">View all attachment types that Document management supports (files, images, URLs, and notes).</span></span>
+ <span data-ttu-id="a9022-214">Çok sayfalı TIFF dosyalarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="a9022-214">View multi-page TIFF files.</span></span>
+ <span data-ttu-id="a9022-215">Görüntü dosyalarında aşağıdaki eylemleri gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="a9022-215">Perform the following actions on image files:</span></span>
  + <span data-ttu-id="a9022-216">Resmin bölümlerini vurgulayın.</span><span class="sxs-lookup"><span data-stu-id="a9022-216">Highlight parts of the image.</span></span>
  + <span data-ttu-id="a9022-217">Resmin bölümlerini engelleyin.</span><span class="sxs-lookup"><span data-stu-id="a9022-217">Block parts of the image.</span></span>
  + <span data-ttu-id="a9022-218">Resme ek açıklama ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a9022-218">Add annotations to the image.</span></span>
  + <span data-ttu-id="a9022-219">Resmi yakınlaştırın ve uzaklaştırın.</span><span class="sxs-lookup"><span data-stu-id="a9022-219">Zoom in and out on the image.</span></span>
  + <span data-ttu-id="a9022-220">Görüntüyü kaydırın.</span><span class="sxs-lookup"><span data-stu-id="a9022-220">Pan the image.</span></span>
  + <span data-ttu-id="a9022-221">Geri al ve yinele eylemleri.</span><span class="sxs-lookup"><span data-stu-id="a9022-221">Undo and redo actions.</span></span>
  + <span data-ttu-id="a9022-222">Resmin boyutuna sığdır.</span><span class="sxs-lookup"><span data-stu-id="a9022-222">Fit the image to size.</span></span>

> [!NOTE]
> <span data-ttu-id="a9022-223">Bu eylemler yalnızca resim dosyaları için (JPEG, TIFF, PNG vb.) kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a9022-223">These actions are available only for image files (JPEG, TIFF, PNG, and so on).</span></span> <span data-ttu-id="a9022-224">Bu eylemleri kullanarak resimde yaptığınız tüm değişiklikler resim dosyasına kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="a9022-224">Any changes that you make to an image by using these actions are saved to the image file.</span></span> <span data-ttu-id="a9022-225">Şu anda, ek görüntüleyici sürüm veya denetim özellikleri içermez.</span><span class="sxs-lookup"><span data-stu-id="a9022-225">Currently, the attachment viewer doesn’t include versioning or auditing capabilities.</span></span>

### <a name="default-attachment"></a><span data-ttu-id="a9022-226">Varsayılan ek</span><span class="sxs-lookup"><span data-stu-id="a9022-226">Default attachment</span></span>

<span data-ttu-id="a9022-227">Bir satıcı faturasında bir veya daha fazla ek varsa, belgelerden birini **Ekler** sayfasında varsayılan ek olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9022-227">If a vendor invoice has more than one attachment, you can set one of the documents as the default attachment on the **Attachments** page.</span></span> <span data-ttu-id="a9022-228">**Varsayılan ektir** seçeneği bu özelliğin bir parçası olarak eklenmiş olan yeni bir seçenektir.</span><span class="sxs-lookup"><span data-stu-id="a9022-228">The **Is default attachment** option is a new option that was added as part of this feature.</span></span> <span data-ttu-id="a9022-229">Bu seçenek aynı zamanda Satıcı faturası belge eki veri varlığı için de ortaya çıkar.</span><span class="sxs-lookup"><span data-stu-id="a9022-229">This option is also exposed in the Vendor invoice document attachment data entity.</span></span> <span data-ttu-id="a9022-230">Bu nedenle, varsayılan ek tümleştirmeler aracılığıyla ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="a9022-230">Therefore, the default attachment can be set through integrations.</span></span>

<span data-ttu-id="a9022-231">Yalnızca tek bir belge varsayılan ek olarak ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="a9022-231">Only one document can be set as the default attachment.</span></span> <span data-ttu-id="a9022-232">Bir belgeyi varsayılan ek olarak ayarladıktan sonra, bu belge fatura açıldığında otomatik olarak ek görüntüleyicide görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="a9022-232">After you set a document as the default attachment, it’s automatically shown in the attachment viewer when the invoice is opened.</span></span> <span data-ttu-id="a9022-233">Varsayılan ek olarak bir belge ayarlamazsanız, görüntüleyicisi fatura açıldığında otomatik olarak herhangi bir ek görüntülemez.</span><span class="sxs-lookup"><span data-stu-id="a9022-233">If you don’t set any document as the default attachment, the viewer doesn’t automatically show any attachment when the invoice is opened.</span></span>

### <a name="showhide-invoice-attachments"></a><span data-ttu-id="a9022-234">Fatura eklerini göster/gizle</span><span class="sxs-lookup"><span data-stu-id="a9022-234">Show/hide invoice attachments</span></span>

<span data-ttu-id="a9022-235">**Özel durum işleme**, **Bekleyen fatura** ve **Fatura günlüğü** sorgu sayfalarında, ek görüntüleyiciyi gizlemenizi veya göstermenizi sağlayan yeni bir düğme bulunur.</span><span class="sxs-lookup"><span data-stu-id="a9022-235">A new button that is available on the **Exception processing**, **Pending invoice**, and **Invoice journal** inquiry pages lets you show or hide the attachment viewer.</span></span>

## <a name="security"></a><span data-ttu-id="a9022-236">Güvenlik</span><span class="sxs-lookup"><span data-stu-id="a9022-236">Security</span></span>

<span data-ttu-id="a9022-237">Ek görüntüleyicideki aşağıdaki eylemler rol tabanlı güvenlikle denetlenir:</span><span class="sxs-lookup"><span data-stu-id="a9022-237">The following actions in the attachment viewer are controlled via role-based security:</span></span>

+ <span data-ttu-id="a9022-238">Vurgulama</span><span class="sxs-lookup"><span data-stu-id="a9022-238">Highlighting</span></span>
+ <span data-ttu-id="a9022-239">Engelle</span><span class="sxs-lookup"><span data-stu-id="a9022-239">Block</span></span>
+ <span data-ttu-id="a9022-240">Ek açıklama</span><span class="sxs-lookup"><span data-stu-id="a9022-240">Annotation</span></span>

### <a name="pending-vendor-invoices-page"></a><span data-ttu-id="a9022-241">Beklemedeki satıcı faturaları sayfası</span><span class="sxs-lookup"><span data-stu-id="a9022-241">Pending vendor invoices page</span></span>

<span data-ttu-id="a9022-242">Aşağıdaki ayrıcalıklar vurgulama, engelleme veya ek açıklama ekleme işlemleri için ek görüntüleyiciye salt okuma erişimi veya okuma/yazma erişimi sağlar:</span><span class="sxs-lookup"><span data-stu-id="a9022-242">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions:</span></span>

+ <span data-ttu-id="a9022-243">**Satıcı fatura resmini koru** – Bu ayrıcalık, okuma/yazma erişimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a9022-243">**Maintain vendor invoice image** – This privilege provides read/write access.</span></span>
+ <span data-ttu-id="a9022-244">**Satıcı fatura resmini görüntüle** – Bu ayrıcalık, salt okuma erişimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a9022-244">**View vendor invoice image** – This privilege provides read-only access.</span></span>

<span data-ttu-id="a9022-245">Aşağıdaki görevler, şu eylemler için ek görüntüleyiciye salt okuma veya okuma/yazma erişimi sağlar:</span><span class="sxs-lookup"><span data-stu-id="a9022-245">The following duties provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="a9022-246">**Satıcı faturalarını koru** – Satıcı fatura resmini koru ayrıcalığı bu göreve atanır.</span><span class="sxs-lookup"><span data-stu-id="a9022-246">**Maintain vendor invoices** – The Maintain vendor invoice image privilege is assigned to this duty.</span></span>
+ <span data-ttu-id="a9022-247">**Satıcı fatura durumunu sorgula** – Satıcı fatura resmini görüntüle ayrıcalığı bu göreve atanır.</span><span class="sxs-lookup"><span data-stu-id="a9022-247">**Inquire into vendor invoice status** – The View vendor invoice image privilege is assigned to this duty.</span></span>

<span data-ttu-id="a9022-248">Aşağıdaki roller, şu eylemler için ek görüntüleyiciye salt okuma veya okuma/yazma erişimi sağlar:</span><span class="sxs-lookup"><span data-stu-id="a9022-248">The following roles provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="a9022-249">**Borç hesapları memuru** ve **Borç Hesapları yöneticisi** – Bu rollere Satıcı faturalarını koru görevi atanır.</span><span class="sxs-lookup"><span data-stu-id="a9022-249">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>
+ <span data-ttu-id="a9022-250">**Borç hesapları memuru**, **Borç Hesapları yöneticisi**, **Borç hesapları merkezi ödeme memuru** ve **Borç hesapları ödemeler memuru** – Bu rollere satıcı faturası durumunu sorgula görevi atanır.</span><span class="sxs-lookup"><span data-stu-id="a9022-250">**Accounts payable clerk**, **Accounts payable manager**, **Accounts payable centralized payments clerk**, and **Accounts payable payments clerk** – The Inquire into vendor invoice status duty is assigned to these roles.</span></span>

### <a name="vendor-invoice-attachment"></a><span data-ttu-id="a9022-251">Satıcı faturası eki</span><span class="sxs-lookup"><span data-stu-id="a9022-251">Vendor invoice attachment</span></span>

<span data-ttu-id="a9022-252">Aşağıdaki ayrıcalıklar vurgulama, engelleme veya ek açıklama ekleme işlemleri için ek görüntüleyiciye salt okuma erişimi veya okuma/yazma erişimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a9022-252">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions.</span></span>

> [!NOTE]
> <span data-ttu-id="a9022-253">Bu bölümde söz edilen bu roller, ek görüntüleyicideki fatura resimlerine salt okuma erişimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a9022-253">Out of the box, the roles that are mentioned in this section provide read-only access to the invoice images in the attachment viewer.</span></span> <span data-ttu-id="a9022-254">Bir rolün resimler için yazma erişimi de olması gerekiyorsa, bu role yazma erişimini burada açıklanan ayrıcalığı ve görevi vererek sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9022-254">If a role must also have write access to the images, you can grant write access to that role by using the privilege and duty that are described here.</span></span>

+ <span data-ttu-id="a9022-255">**Satıcı fatura başlığı varlığı resmini koru** – Bu ayrıcalık, ek görüntüleyicideki fatura resimlerine okuma/yazma erişimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a9022-255">**Maintain vendor invoice header entity image** – This privilege provides read/write access to the invoice images in the attachment viewer.</span></span>
+ <span data-ttu-id="a9022-256">**Satıcı fatura başlığı varlığı resmini görüntüle** – Bu ayrıcalık, ek görüntüleyicideki fatura resimlerine salt okuma erişimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a9022-256">**View vendor invoice header entity image** – This privilege provides read-only view to the invoice image in the attachment viewer.</span></span>

<span data-ttu-id="a9022-257">Aşağıdaki görevler, şu eylemler için ek görüntüleyiciye salt okuma erişimi sağlar:</span><span class="sxs-lookup"><span data-stu-id="a9022-257">The following duties provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="a9022-258">**Satıcı faturalarını koru** – Satıcı fatura başlığı varlığı resmini koru ayrıcalığı bu göreve atanır.</span><span class="sxs-lookup"><span data-stu-id="a9022-258">**Maintain vendor invoices** – The Maintain vendor invoice header entity image privilege is assigned to this duty.</span></span>

<span data-ttu-id="a9022-259">Aşağıdaki roller, şu eylemler için ek görüntüleyiciye salt okuma erişimi sağlar:</span><span class="sxs-lookup"><span data-stu-id="a9022-259">The following roles provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="a9022-260">**Borç hesapları memuru** ve **Borç Hesapları yöneticisi** – Bu rollere Satıcı faturalarını koru görevi atanır.</span><span class="sxs-lookup"><span data-stu-id="a9022-260">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>

<span data-ttu-id="a9022-261">Varsayılan olarak, kullanıcı rolü herhangi bir sayfada düzenleme hakları sağlıyorsa, kullanıcı ek görüntüleyicide de vurgulama, engelleme ve not ekleme eylemleri için düzenleme hakkında sahip olur.</span><span class="sxs-lookup"><span data-stu-id="a9022-261">By default, if the user role provides edit rights on any page, the user will also have edit rights on the attachments viewer for the highlighting, block, and annotation actions.</span></span> <span data-ttu-id="a9022-262">Bununla birlikte, belirli bir rolün sayfada düzenleme haklarına sahipken ek görüntüleyicide bu haklara sahip olmaması gereken senaryolar varsa, önceki listedeki uygun ayrıcalıklar bu kullanım örneğini karşılamak üzere kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a9022-262">However, if there are scenarios where a specific role should have edit rights on the page but not on the attachment viewer, the appropriate privileges from the preceding list can be used to satisfy the use case.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
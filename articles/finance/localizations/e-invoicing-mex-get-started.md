---
title: Meksika için Elektronik faturalamayı kullanmaya başlama
description: Bu konu, Meksika için Elektronik faturalamayı kullanmaya başlamanıza yardımcı olacak bilgiler içerir.
author: gionoder
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 2f5dd1d6bc520c9f5349c77dfcabdf2d538881ce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840064"
---
# <a name="get-started-with-electronic-invoicing-for-mexico"></a><span data-ttu-id="8dac2-103">Meksika için Elektronik faturalamayı kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="8dac2-103">Get started with Electronic invoicing for Mexico</span></span>

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="8dac2-104">Meksika için elektronik faturalama şu anda Comprobante Fiscal Digital por Internet (CFDI) belgesindeki kullanılabilir ve Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management üzerinde oluşturulan ilgili tümleştirmelerde tüm işlevleri desteklemeyebilir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-104">Electronic invoicing for Mexico might not currently support all the functions that are available in the Comprobante Fiscal Digital por Internet (CFDI) document, and in the related integration that is built into Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="8dac2-105">Bu konu, Meksika için Elektronik faturalamayı kullanmaya başlamanıza yardımcı olacak bilgiler içerir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-105">This topic provides information that will help you get started with Electronic invoicing for Mexico.</span></span> <span data-ttu-id="8dac2-106">Regulatory Configuration Services (RCS) ve Finance için ülkeye bağlı olan yapılandırma adımlarında size kılavuzluk eder.</span><span class="sxs-lookup"><span data-stu-id="8dac2-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="8dac2-107">Ayrıca, servis üzerinden CFDI faturalarını göndermek için Finance'de izlemeniz gereken adımlarda size yol gösterir ve işlem sonuçlarının nasıl gözden geçirileceğini ve CFDI faturalarının durumunu açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="8dac2-107">It also guides you through the steps that you must follow in Finance to submit CFDI invoices through the service, and it explains how to review the processing results and the status of CFDI invoices.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8dac2-108">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="8dac2-108">Prerequisites</span></span>

<span data-ttu-id="8dac2-109">Bu konudaki adımları gerçekleştirmeden önce, [elektronik faturalamayı kullanmaya başlama](e-invoicing-get-started.md) adımlarını tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-109">Before you complete the steps in this topic, you must complete the steps in [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="8dac2-110">RCS kurulumu</span><span class="sxs-lookup"><span data-stu-id="8dac2-110">RCS setup</span></span>

<span data-ttu-id="8dac2-111">RCS kurulumu sırasında şu görevleri tamamlayacaksınız:</span><span class="sxs-lookup"><span data-stu-id="8dac2-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="8dac2-112">CFDI faturalarını işlemek için e-faturalama özelliğini içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="8dac2-112">Import the e-Invoicing feature for processing CFDI invoices.</span></span>
2. <span data-ttu-id="8dac2-113">CFDI faturaları hakkında yanıtlar oluşturmak, göndermek ve almak, iptal hakkındaki yanıtları göndermek ve almak için gereken biçim yapılandırmalarını gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-113">Review the format configurations that are required to generate, submit, and receive responses about CFDI invoices, and to submit and receive responses about cancellation.</span></span>
3. <span data-ttu-id="8dac2-114">CFDI fatura gönderme senaryolarını destekleyen olayları yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="8dac2-114">Configure the events that support the CFDI invoice submission scenarios.</span></span>
4. <span data-ttu-id="8dac2-115">CFDI faturalarını işlemek için e-faturalama özelliğini yayınlayın.</span><span class="sxs-lookup"><span data-stu-id="8dac2-115">Publish the e-Invoicing feature for CFDI invoices.</span></span>

> [!NOTE]
> <span data-ttu-id="8dac2-116">"E-faturala özelliği", Elektronik faturalama sunucusunu kullanmak üzere yapılandırılmış ve yayımlanmış olan kaynağın genel adıdır.</span><span class="sxs-lookup"><span data-stu-id="8dac2-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing server.</span></span> <span data-ttu-id="8dac2-117">Bu durumda, CFDI faturaları (MX), ayarlayacağınız e-faturalama özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-117">In this case, CFDI invoices (MX) are the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="8dac2-118">E-faturalama özelliğini içe aktarma</span><span class="sxs-lookup"><span data-stu-id="8dac2-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="8dac2-119">RCS hesabınızda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="8dac2-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="8dac2-120">**Genelleştirme özellikleri** çalışma alanında **Özellikler** bölmesinde **E-faturalama** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="8dac2-121">**E-faturalama özellikleri** sayfasında, Genel depodan **CFDI faturaları (MX)** özelliğini içe aktarmak için **İçe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-121">On the **e-Invoicing Features** page, select **Import** to import the **CFDI invoices (MX)** feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8dac2-122">Listede özelliği göremiyorsanız, **Eşitle**'yi seçin ve 3. adımı tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="8dac2-122">If you don't see the feature in the list, select **Synchronize**, and then repeat step 3.</span></span>

![CFDI faturaları (MX) özelliğini içe aktarma](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

<span data-ttu-id="8dac2-124">**CFDI faturaları (MX)** özelliğini Global depodan içe aktardığınızda, yapılandırmalar ve eylemlerle birlikte tüm özellik ayarları da içe aktarılır.</span><span class="sxs-lookup"><span data-stu-id="8dac2-124">When you import the **CFDI invoices (MX)** feature from the Global repository, all the feature settings, including configurations and actions, are also imported.</span></span>

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a><span data-ttu-id="8dac2-125">CFDI faturaları (MX) özelliğinin yeni bir sürümünü oluşturma</span><span class="sxs-lookup"><span data-stu-id="8dac2-125">Create a new version of the CFDI invoices (MX) feature</span></span>

<span data-ttu-id="8dac2-126">Örneğin, URL'lerin güncelleştirilmesi gerekiyorsa, yeni bir sürüm oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8dac2-126">You can create a new version if, for example, URLs must be updated.</span></span> <span data-ttu-id="8dac2-127">Daha fazla bilgi için, bkz. [E-faturalama CFDI](tasks/mx-00010-e-invoicing-cfdi.md).</span><span class="sxs-lookup"><span data-stu-id="8dac2-127">For more information, see [E-invoicing CFDI](tasks/mx-00010-e-invoicing-cfdi.md).</span></span>

- <span data-ttu-id="8dac2-128">**E-faturalama özellikleri** sayfasında, **Sürümler** sekmesinde, **Yeni** ögesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-128">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![Yeni e-faturalama özellik sürümü ekleme](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="8dac2-130">Yapılandırma sürümünü güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="8dac2-130">Update the configuration version</span></span>

1. <span data-ttu-id="8dac2-131">**E-faturalama özellikleri** sayfasında, **Yapılandırmalar** sekmesinde, yapılandırma sürümlerini (ER dosya biçimi yapılandırmaları) yönetmek için **Ekle** veya **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-131">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![E-faturalama özellik yapılandırmalarını yönetme](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    <span data-ttu-id="8dac2-133">Yeni bir sürüm oluşturduğunuzda, tüm yapılandırmalar en son yayınlanan sürümden devralınır.</span><span class="sxs-lookup"><span data-stu-id="8dac2-133">When you create a new version, all configurations are inherited from the last published version.</span></span> <span data-ttu-id="8dac2-134">CFDI faturalarını işlemek için aşağıdaki yapılandırmalar gereklidir:</span><span class="sxs-lookup"><span data-stu-id="8dac2-134">To process CFDI invoices, the following configurations are required:</span></span>

    - <span data-ttu-id="8dac2-135">CFDI faturası (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="8dac2-135">CFDI invoice (BusinessDocumentService)</span></span>
    - <span data-ttu-id="8dac2-136">CFDI yanıt iletisi alma</span><span class="sxs-lookup"><span data-stu-id="8dac2-136">CFDI response message import</span></span>
    - <span data-ttu-id="8dac2-137">CFDI hata günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="8dac2-137">CFDI error log import</span></span>
    - <span data-ttu-id="8dac2-138">CFDI iptal isteği (MX) (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="8dac2-138">CFDI cancelation request (MX) (BusinessDocumentService)</span></span>
    - <span data-ttu-id="8dac2-139">CFDI faturası (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="8dac2-139">CFDI invoice (BusinessDocumentService)</span></span>

2. <span data-ttu-id="8dac2-140">Listede bir yapılandırma sürümü seçin ve sonra da yapılandırmayı düzenleyebileceğiniz veya görüntüleyebileceğiniz **Biçim tasarımcısı** sayfasını açmak için **Düzenle** veya **Görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-140">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![Biçim tasarımcısı sayfasını açma](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. <span data-ttu-id="8dac2-142">**Biçim tasarımcısı** sayfasını, ER biçimi dosya yapılandırmalarını düzenlemek ve görüntülemek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="8dac2-142">Use the **Format designer** page to edit and view the ER format file configurations.</span></span> <span data-ttu-id="8dac2-143">Daha fazla bilgi için bkz. [Elektronik belge yapılandırmalarını oluşturma](../../dev-itpro/analytics/electronic-reporting-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="8dac2-143">For more information, see [Create electronic document configurations](../../dev-itpro/analytics/electronic-reporting-configuration.md).</span></span>

    ![Biçim tasarımcısı sayfası](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="8dac2-145">E-faturalama özellik kurulumlarını yönetme</span><span class="sxs-lookup"><span data-stu-id="8dac2-145">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="8dac2-146">**E-faturalama özellikleri** sayfasında, **Kurulumlar** sekmesinde, E-faturalama özellik kurulumlarını yönetmek için **Ekle**, **Sil** veya **Düzenle** ögesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-146">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![E-faturalama özellik kurulumlarını yönetme](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

<span data-ttu-id="8dac2-148">Onaya CFDI faturalarını göndermek için (XML dosyasını oluşturun, XML dosyasını gönderin ve yanıtı işleyin), **Satış faturası** özellik kurulumu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-148">To submit CFDI invoices for authorization (generate the XML file, submit the XML file, and process the response), the **Sales invoice** feature setup is required.</span></span>

<span data-ttu-id="8dac2-149">CFDI fatura iptali göndermek için **İptal etme** ve **İptal etme** özelliği kurulumları gereklidir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-149">To submit CFDI invoice cancellation, the **Cancellation** and **Cancel** feature setups are required.</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="8dac2-150">Satış faturası özellik kurulumunu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="8dac2-150">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="8dac2-151">**E-faturalama özellikleri** sayfasında, **Kurulumlar** sekmesinde, **Özellik kurulumu** sütununda **Satış faturası**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-151">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="8dac2-152">Eylemleri, uygulanabilirlik kurallarını ve değişkenleri yapılandırmak için **Düzenle** ögesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-152">Select **Edit** to configure the actions, applicability rules, and variables.</span></span>

    ![E-faturalama özellik kurulumunu düzenleme](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="8dac2-154">**Özellik sürümü kurulumu** sayfasında, eylemler listesini yönetmek için **Eylemler** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-154">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="8dac2-155">Eylemler, olayın tam olarak yürütülmesi için sırayla çalıştırılması gereken işlemlerin listesini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="8dac2-155">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![Eylemler sekmesi](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | <span data-ttu-id="8dac2-157">Eylem kodu</span><span class="sxs-lookup"><span data-stu-id="8dac2-157">Action ID</span></span> | <span data-ttu-id="8dac2-158">Eylem</span><span class="sxs-lookup"><span data-stu-id="8dac2-158">Action</span></span>                   | <span data-ttu-id="8dac2-159">Eylem adı</span><span class="sxs-lookup"><span data-stu-id="8dac2-159">Action name</span></span>                                  | <span data-ttu-id="8dac2-160">Eylem açıklaması</span><span class="sxs-lookup"><span data-stu-id="8dac2-160">Action description</span></span>                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | <span data-ttu-id="8dac2-161">1</span><span class="sxs-lookup"><span data-stu-id="8dac2-161">1</span></span>         | <span data-ttu-id="8dac2-162">Belgeyi dönüştür</span><span class="sxs-lookup"><span data-stu-id="8dac2-162">Transform document</span></span>       | <span data-ttu-id="8dac2-163">Dijital işareti olmadan CFDI E-fatura oluşturma</span><span class="sxs-lookup"><span data-stu-id="8dac2-163">Generate CFDI E-Invoice without digital sign</span></span> | <span data-ttu-id="8dac2-164">CFDI e-fatura oluşturun.</span><span class="sxs-lookup"><span data-stu-id="8dac2-164">Generate the CFDI e-invoice.</span></span>                                |
    | <span data-ttu-id="8dac2-165">2</span><span class="sxs-lookup"><span data-stu-id="8dac2-165">2</span></span>         | <span data-ttu-id="8dac2-166">Belgeyi imzala</span><span class="sxs-lookup"><span data-stu-id="8dac2-166">Sign document</span></span>            | <span data-ttu-id="8dac2-167">Dijital imza</span><span class="sxs-lookup"><span data-stu-id="8dac2-167">Digital sign</span></span>                                 | <span data-ttu-id="8dac2-168">E-faturayı gönderim için dijital olarak imzalayın.</span><span class="sxs-lookup"><span data-stu-id="8dac2-168">Digitally sign the e-invoice for submission.</span></span>                |
    | <span data-ttu-id="8dac2-169">3</span><span class="sxs-lookup"><span data-stu-id="8dac2-169">3</span></span>         | <span data-ttu-id="8dac2-170">Meksika PAC hizmetini çağır</span><span class="sxs-lookup"><span data-stu-id="8dac2-170">Call Mexican PAC service</span></span> | <span data-ttu-id="8dac2-171">CFDI e-fatura gönder</span><span class="sxs-lookup"><span data-stu-id="8dac2-171">Submit CFDI E-Invoice</span></span>                        | <span data-ttu-id="8dac2-172">Windows Communication Foundation (WCF) istemcisi, CFDI e-faturasını gönderir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-172">The Windows Communication Foundation (WCF) client submits the CFDI e-invoice.</span></span> |
    | <span data-ttu-id="8dac2-173">4</span><span class="sxs-lookup"><span data-stu-id="8dac2-173">4</span></span>         | <span data-ttu-id="8dac2-174">Yanıtı işle</span><span class="sxs-lookup"><span data-stu-id="8dac2-174">Process response</span></span>         | <span data-ttu-id="8dac2-175">Web servis yanıtını çözümle</span><span class="sxs-lookup"><span data-stu-id="8dac2-175">Analyze web service response</span></span>                 | <span data-ttu-id="8dac2-176">Web hizmeti yanıtını çözümleyin ve hata günlüğünü döndürür.</span><span class="sxs-lookup"><span data-stu-id="8dac2-176">Analyze the web service response, and return the error log.</span></span> |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a><span data-ttu-id="8dac2-177">Meksika PAC Web Hizmetleri için URL'yi ayarlama</span><span class="sxs-lookup"><span data-stu-id="8dac2-177">Set up the URL for Mexican PAC web services</span></span> 

1. <span data-ttu-id="8dac2-178">**Özellik sürümü kurulumu** sayfasında, **Eylemler** sekmesindeki **Eylemler** hızlı sekmesinde, **Meksika PAC Servisi çağır** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-178">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Mexican PAC service**.</span></span>
2. <span data-ttu-id="8dac2-179">**Parametreler** hızlı sekmesinde, **URL adresi** alanına, CFDI fatura gönderimi için Web hizmetinin URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-179">On the **Parameters** FastTab, in the **URL address** field, enter the URL of the web service for CFDI invoice submission.</span></span>

> [!NOTE]
> <span data-ttu-id="8dac2-180">**İptal** ve **İptal isteği** özelliği kurulumları için **Meksika PAC servisini çağır** eylemi URL'sini güncelleştirmek üzere aynı adımları kullanın.</span><span class="sxs-lookup"><span data-stu-id="8dac2-180">Use the same steps to update the URL for **Call Mexican PAC service** action for the **Cancel** and **Cancelation request** feature setups.</span></span>

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a><span data-ttu-id="8dac2-181">Taslak sürümünü bir E-faturalama ortamına atama</span><span class="sxs-lookup"><span data-stu-id="8dac2-181">Assign the Draft version to an e-Invoicing environment</span></span>

1. <span data-ttu-id="8dac2-182">**E-faturalama özellikleri** sayfasında, **Ortamlar** sekmesinde, **Etkinleştir** ögesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-182">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="8dac2-183">**Ortamlar** alanında, ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-183">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="8dac2-184">**Geçerlilik başlangıcı** alanında, yeni ortamın geçerli olacağı tarihi seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-184">In the **Effective from** field, select the date when the environment should become effective.</span></span>
3. <span data-ttu-id="8dac2-185">**Etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-185">Select **Enable**.</span></span>

![E-faturalama ortamını etkinleştirme](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a><span data-ttu-id="8dac2-187">Sürüm durumunu Tamamlandı olarak değiştirme</span><span class="sxs-lookup"><span data-stu-id="8dac2-187">Change the version status to Completed</span></span>

1. <span data-ttu-id="8dac2-188">**E-faturalama Özellikleri** sayfasındaki **Sürümler** sekmesinde, **Taslak** durumundaki e-faturalama özelliğinin sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-188">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="8dac2-189">**Durumu değiştir \> Tamamla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-189">Select **Change status \> Complete**.</span></span>

## <a name="change-the-version-status-to-published"></a><span data-ttu-id="8dac2-190">Sürüm durumunu Yayımlandı olarak değiştirme</span><span class="sxs-lookup"><span data-stu-id="8dac2-190">Change the version status to Published</span></span>

- <span data-ttu-id="8dac2-191">**E-faturalama özellikleri** sayfasında, **Sürümler** sekmesinde, **Durumu değiştir \> Yayımla** ögesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-191">On the **e-Invoicing Features** page, on the **Versions** tab, select **Change status \> Publish**.</span></span>

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="8dac2-192">E-faturalama özelliğini yayımlama</span><span class="sxs-lookup"><span data-stu-id="8dac2-192">Publish the e-Invoicing feature</span></span>

1. <span data-ttu-id="8dac2-193">**E-faturalama özellikleri** sayfasında, **CFDI faturaları (MX)** özelliğinin durumunu yönetmek için **Sürümler** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-193">On the **e-Invoicing Features** page, select the **Versions** tab to manage the status of the **CFDI invoices (MX)** feature.</span></span>
2. <span data-ttu-id="8dac2-194">Özelliğin durumunu değiştirmek için **Durumu değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-194">Select **Change status** to change the status of the feature.</span></span>

![E-faturalama özelliğinin durumunu değiştirme](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing--integration-in-finance"></a><span data-ttu-id="8dac2-196">Finance'de Elektronik faturalama tümleştirmesi kurulumu</span><span class="sxs-lookup"><span data-stu-id="8dac2-196">Set up Electronic invoicing  integration in Finance</span></span>

<span data-ttu-id="8dac2-197">Finance içindeki Elektronik faturalamayı ayarlamak için şu görevleri tamamlayacaksınız:</span><span class="sxs-lookup"><span data-stu-id="8dac2-197">To set up Electronic invoicing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="8dac2-198">ER veri modelini, ER veri modeli eşleştirmesini ve CFDI faturaları için gereken biçimleri içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="8dac2-198">Import the ER data model, the ER data model mapping, and the formats that are required for CFDI invoices.</span></span>
2. <span data-ttu-id="8dac2-199">CFDI faturalarını güncelleştirmek için yanıt tiplerini yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="8dac2-199">Configure response types for updating the CFDI invoices.</span></span> <span data-ttu-id="8dac2-200">Bu yanıt türleri yetkili sertifika sağlayıcı (PAC) sunucusundan yanıt olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8dac2-200">These response types are used for the response from the authorized certification provider (PAC) server.</span></span>

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a><span data-ttu-id="8dac2-201">ER veri modelini, ER veri modeli eşleştirmesini ve CFDI faturaları için bağlam yapılandırmalarını içe aktarın</span><span class="sxs-lookup"><span data-stu-id="8dac2-201">Import the ER data model, ER data model mapping, and context configurations for CFDI invoices</span></span>

1. <span data-ttu-id="8dac2-202">Finance'de oturum açın.</span><span class="sxs-lookup"><span data-stu-id="8dac2-202">Sign in to Finance.</span></span>
2. <span data-ttu-id="8dac2-203">**Elektronik raporlama** çalışma alanında, **Yapılandırma sağlayıcıları** bölümünde, **Microsoft** başlığını seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-203">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span> <span data-ttu-id="8dac2-204">Bu yapılandırma sağlayıcısının **Etkin** olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="8dac2-204">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="8dac2-205">Sağlayıcının **Etkin** olarak nasıl ayarlanacağı hakkında daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve etkin olarak işaretleme](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="8dac2-205">For information about how to set a provider to **Active**, see [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span></span>
3. <span data-ttu-id="8dac2-206">**Depolar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-206">Select **Repositories**.</span></span>
4. <span data-ttu-id="8dac2-207">**Genel kaynak \> Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-207">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="8dac2-208">**Fatura modeli**, **Fatura modeli eşlemesi**, **CFDI fatura biçimi (MX)**, **CFDI fatura iptal isteği biçimi (MX)** ve **CFDI fatura iptali biçimi (MX)** ögelerini ni içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="8dac2-208">Import **Invoice model**, **Invoice model mapping**, **CFDI invoice format (MX)**, **CFDI invoice cancelation request format (MX)**, and **CFDI invoice cancel format (MX)**.</span></span>

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a><span data-ttu-id="8dac2-209">CFDI faturalarını işlemek için özelliği açma</span><span class="sxs-lookup"><span data-stu-id="8dac2-209">Turn on the feature for processing CFDI invoices</span></span>

1. <span data-ttu-id="8dac2-210">**Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="8dac2-211">**Özellikler** sekmesinde, **MX-00010** ve **MX-00016** özellik referansları için satırlarda **Etkinleştir** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-211">On the **Features** tab, select the **Enable** check box in the rows for feature references **MX-00010** and **MX-00016**.</span></span>

![CFDI faturalarını işlemek için özellikleri açma](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a><span data-ttu-id="8dac2-213">ER yapılandırmalarını içe aktarma ve CFDI faturalarını güncelleştirmek için yanıt tiplerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="8dac2-213">Import ER configurations and set up the response types for updating CFDI invoices</span></span>

#### <a name="import-er-configurations"></a><span data-ttu-id="8dac2-214">ER yapılandırmaları içe aktarın</span><span class="sxs-lookup"><span data-stu-id="8dac2-214">Import ER configurations</span></span>

1. <span data-ttu-id="8dac2-215">**Elektronik raporlama** çalışma alanında, **Yapılandırma sağlayıcıları** bölümünde, **Microsoft** başlığını seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-215">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span>
3. <span data-ttu-id="8dac2-216">**Depolar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-216">Select **Repositories**.</span></span>
4. <span data-ttu-id="8dac2-217">**Genel kaynak \> Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-217">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="8dac2-218">**Yanıt iletisi modeli**, **CFDI hata günlüğü alma (MX)** ve **CFDI yanıt iletisi içeri aktarma (MX)** ögelerini içeri aktarın.</span><span class="sxs-lookup"><span data-stu-id="8dac2-218">Import **Response message model**, **CFDI error log import (MX)**, and **CFDI response message import (MX)**.</span></span>

#### <a name="set-up-the-response-types"></a><span data-ttu-id="8dac2-219">Yanıt türlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="8dac2-219">Set up the response types</span></span>

1. <span data-ttu-id="8dac2-220">**Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-220">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="8dac2-221">**Elektronik belge** sekmesinde **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-221">On the **Electronic document** tab, select **Add**.</span></span>
3. <span data-ttu-id="8dac2-222">Müşteri fatura günlüğünü girin ve sonra **Tablo adı** alanında proje faturasını seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-222">Enter the customer invoice journal, and then, in the **Table name** field, select the project invoice.</span></span>
4. <span data-ttu-id="8dac2-223">Her tablo için, ilgili belge bağlamını tanımlayın:</span><span class="sxs-lookup"><span data-stu-id="8dac2-223">For each table, define a related document context:</span></span>

    - <span data-ttu-id="8dac2-224">**Müşteri fatura günlüğü** için **Müşteri fatura bağlamı**'nı girin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-224">For **Customer invoice journal**, enter **Customer invoice context**.</span></span>
    - <span data-ttu-id="8dac2-225">**Proje faturası** için **Proje fatura bağlamı**'nı girin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-225">For **Project invoice**, enter **Project invoice context**.</span></span>

4. <span data-ttu-id="8dac2-226">Elektronik faturalamadan döndürülecek ve bir müşteri fatura günlüğünde veya proje faturasına dahil edilen yanıt türlerini yapılandırmak için **Yanıt türleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-226">Select **Response types** to configure the response types that can be returned from Electronic invoicing and included in a customer invoice journal or project invoice.</span></span>
5. <span data-ttu-id="8dac2-227">**Yeni**'yi seçin ve sonra **Yanıt türü** alanında, **Yanıt**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-227">Select **New**, and then, in the **Response type** field, select **Response**.</span></span>
6. <span data-ttu-id="8dac2-228">**Gönderim durumu** alanında, **Bekliyor**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-228">In the **Submission status** field, select **Pending**.</span></span>
7. <span data-ttu-id="8dac2-229">**Model eşleme** alanında, **Yanıt iletisi içe aktarma biçimi - Yanıt iletisinden model eşlemesi** ögesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-229">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
8. <span data-ttu-id="8dac2-230">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-230">Select **Save**.</span></span>
9. <span data-ttu-id="8dac2-231">**Yeni**'yi seçin ve sonra **Yanıt türü** alanında, **ResponseData** ögesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-231">Select **New**, and then, in the **Response type** field, select **ResponseData**.</span></span>
10. <span data-ttu-id="8dac2-232">**Gönderim durumu** alanında, **Bekliyor**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-232">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="8dac2-233">**Model eşleme** alanında, **CFDI yanıtı veri içe aktarma biçimi (ayrıntılar) – Yanıt verilerini içe aktarma** ögesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-233">In the **Model mapping** field, select **CFDI response data import format (details) – Response data import**.</span></span>
12. <span data-ttu-id="8dac2-234">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-234">Select **Save**.</span></span>

## <a name="process-electronic-invoices-in-finance"></a><span data-ttu-id="8dac2-235">Finance içindeki elektronik faturaları işleme</span><span class="sxs-lookup"><span data-stu-id="8dac2-235">Process electronic invoices in Finance</span></span> 

<span data-ttu-id="8dac2-236">Elektronik faturalama ile Finance içindeki CFDI faturalarının işlenmesi sırasında aşağıdaki görevleri gerçekleştirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="8dac2-236">During the processing of CFDI invoices in Finance through Electronic invoicing, you can perform the following tasks:</span></span>

- <span data-ttu-id="8dac2-237">CFDI faturalarını gönderin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-237">Submit CFDI invoices.</span></span>
- <span data-ttu-id="8dac2-238">Gönderme yürütme günlüklerine bakın.</span><span class="sxs-lookup"><span data-stu-id="8dac2-238">View the submission execution logs.</span></span>
- <span data-ttu-id="8dac2-239">Bir CFDI faturasının iptalini gönderin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-239">Submit the cancellation of a CFDI invoice.</span></span>

### <a name="submit-cfdi-invoices"></a><span data-ttu-id="8dac2-240">CFDI faturalarını gönderme</span><span class="sxs-lookup"><span data-stu-id="8dac2-240">Submit CFDI invoices</span></span>

<span data-ttu-id="8dac2-241">**Yapılandırılabilir Elektronik faturalama tümleştirmesi** özelliğini açtıktan sonra, **CFDI faturalarını göndermek için Elektronik faturayı dışa/içe aktar** işlemi (**Alacak hesapları \> Fatura \> E-faturalar**) artık kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="8dac2-241">After you turn on the **Configurable Electronic invoicing integration** feature, the **Export/Import electronic invoice** process (**Accounts receivable \> Invoices \> E-invoices**) for submitting CFDI invoices can no longer be used.</span></span> <span data-ttu-id="8dac2-242">**Elektronik belge gönderme** adı verilen yeni bir işlemle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-242">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="8dac2-243">Yeni **Elektronik belge gönder** işlemini kullanmadan önce, Meksika e-faturaları için gerekli olan kurulumun tamamlandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="8dac2-243">Before you use the new **Submit electronic documents** process, verify that the setup that is required for Mexican e-invoices was completed.</span></span> <span data-ttu-id="8dac2-244">Daha fazla bilgi için bkz. [CFDI düzen sürümü 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).</span><span class="sxs-lookup"><span data-stu-id="8dac2-244">For more information, see [CFDI layout version 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).</span></span>

1. <span data-ttu-id="8dac2-245">**Kuruluş Yönetimi \> Dönemlik \> Elektronik belgeler \> Elektronik belgeleri gönder** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-245">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="8dac2-246">Herhangi bir belgenin ilk gönderimi için, **Belgeyi yeniden gönder** seçeneğini her zaman **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8dac2-246">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="8dac2-247">Belgeyi servis aracılığıyla yeniden göndermeniz gerekiyorsa, bu seçeneği **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8dac2-247">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="8dac2-248">**Dahil edilecek kayıtlar** hızlı sekmesinde, gönderilecek belgeleri seçmek üzere bir sorgu oluşturabileceğiniz **Sorgulama** iletişim kutusunu açmak için **Filtre**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-248">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![Bir CFDI belgesi gönderme](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> <span data-ttu-id="8dac2-250">Servis aracılığıyla ilk belgeyi gönderme denemeniz sırasında, Elektronik faturalama ile bağlantıyı onaylamanız istenecektir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-250">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with Electronic invoicing.</span></span> <span data-ttu-id="8dac2-251">**Elektronik Belge Gönderme Hizmetine bağlanmak için burayı tıklayın** ögesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-251">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-submission-logs"></a><span data-ttu-id="8dac2-252">Gönderme günlüklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="8dac2-252">View submission logs</span></span>

<span data-ttu-id="8dac2-253">Gönderme günlüklerini gönderilen tüm belgelerin veya yalnızca gönderilen bir belge için görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8dac2-253">You can view the submission logs for all submitted documents or for just one submitted document.</span></span>

#### <a name="view-all-submission-logs"></a><span data-ttu-id="8dac2-254">Bütün gönderme günlüklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="8dac2-254">View all submission logs</span></span>

<span data-ttu-id="8dac2-255">**Yapılandırılabilir Elektronik faturalama tümleştirmesi** özelliğini açtıktan sonra, belge gönderme işlemini takip etmenizi sağlayan yeni bir sayfa kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-255">After you turn on the **Configurable Electronic invoicing integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="8dac2-256">Gönderilen tüm belgelerin gönderme günlüklerini görüntülemek için bu sayfayı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8dac2-256">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="8dac2-257">**Kuruluş Yönetimi \> Dönemlik \> Elektronik belgeler \> Elektronik belgeleri gönderme günlüğü** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-257">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="8dac2-258">**Belge türü** alanında, gerekli elektronik belgelerle ilgili olarak filtre uygulamak için **Müşteri fatura günlüğü** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-258">In the **Document type** field, select **Customer invoice journal** to filter for the required electronic documents.</span></span>

    ![Gönderme günlüklerinin görüntülemek üzere bir belge türü seçme](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. <span data-ttu-id="8dac2-260">Eylem Bölmesi'nde, gönderme yürütme günlüklerinin ayrıntılarını görüntülemek için **Sorgulamalar \> Gönderme ayrıntıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-260">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Gönderme günlüğü ayrıntılarını görüntüleme](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

<span data-ttu-id="8dac2-262">Gönderme günlüklerindeki bilgiler üç hızlı sekme arasında bölünür:</span><span class="sxs-lookup"><span data-stu-id="8dac2-262">The information in the submission logs is divided among three FastTabs:</span></span>

- <span data-ttu-id="8dac2-263">**İşleme eylemleri**: Bu hızlı sekmede, RCS'de ayarlanan özellik sürümünde yapılandırılan eylemler için yürütme günlükleri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-263">**Processing actions** – This FastTab shows the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="8dac2-264">**Durum** sütunu eylemin başarıyla çalıştırılıp çalıştırılmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-264">The **Status** column shows whether the action was successfully run.</span></span>
- <span data-ttu-id="8dac2-265">**Eylem dosyaları**: Bu hızlı sekme, eylemlerin yürütülmesi sırasında oluşturulan ara dosyaları gösterir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-265">**Action files** – This FastTab shows the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="8dac2-266">Dosyayı indirmek ve görüntülemek için **Görünüm** öğesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8dac2-266">You can select **View** to download and view the file.</span></span>
- <span data-ttu-id="8dac2-267">**İşleme eylem günlüğü**: Bu hızlı sekmede, elektronik faturalama ve hedef Web servisi arasındaki iletişimin sonuçları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-267">**Processing action log** – This FastTab shows the results of the communication between Electronic invoicing and the target web service.</span></span> <span data-ttu-id="8dac2-268">Ayrıca Web servis işlemi tarafından döndürülen sonuçları da gösterir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-268">It also shows what was returned by the processing from the web service.</span></span> <span data-ttu-id="8dac2-269">**Hata kodu** sütunu, yetkilendirme Web hizmeti tarafından döndürülen dönüş kodunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-269">The **Error code** column shows the return code that was returned by the authorization web service.</span></span>

<span data-ttu-id="8dac2-270">Gönderilen CFDI faturası yetkilendirilirse, durumu **Onaylandı** olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-270">When the submitted CFDI invoice is authorized, its status is updated to **Approved**.</span></span>

#### <a name="view-submission-logs-from-cfdi-invoices"></a><span data-ttu-id="8dac2-271">CFDI faturalarından gönderme günlüklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="8dac2-271">View submission logs from CFDI invoices</span></span>

<span data-ttu-id="8dac2-272">**Yapılandırılabilir Elektronik faturalandırma tümleştirme** özelliğini açtıktan sonra, tüm CFDI faturalarından gönderme günlüklerini de görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8dac2-272">After you turn on the **ConfigurableElectronic invoicing integration** feature, you can also view the submission logs from CFDI invoices.</span></span>

1. <span data-ttu-id="8dac2-273">**Alacak hesapları \> Sorgulamalar ve raporlar \> CFDI (elektronik faturalar)** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-273">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="8dac2-274">**Yapılandırılabilir Elektronik faturalama tümleştirme** özelliği etkinleştirildikten sonra gönderilen bir CFDI faturası seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-274">Select a CFDI invoice that was submitted after the **Configurable Electronic invoicing integration** feature was turned on.</span></span>
3. <span data-ttu-id="8dac2-275">Eylem Bölmesi'ndeki **Geçmiş** sekmesinde, **Elektronik belge günlüğü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-275">On the Action Pane, on the **History** tab, select **Electronic document log**.</span></span>

![CFDI faturalarından gönderme günlüklerini görüntüleme](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> <span data-ttu-id="8dac2-277">**Yapılandırılabilir Elektronik faturalama tümleştirme** özelliği açılmadan önce gönderilen CFDI faturaları için **Geçmiş** düğmesi kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-277">For CFDI invoices that were submitted before the **Configurable Electronic invoicing integration** feature was turned on, the **History** button is available.</span></span> <span data-ttu-id="8dac2-278">**Yapılandırılabilir Elektronik faturalama tümleştirme** özelliği açıldıktan sonra gönderilen CFDI faturaları için **Geçmiş** düğmesi kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="8dac2-278">The **History** button isn't available for CFDI invoices that were submitted after the **Configurable Electronic invoicing integration** feature was turned on.</span></span>

### <a name="submit-cancellation-of-cfdi-invoices"></a><span data-ttu-id="8dac2-279">CFDI faturalarına ait iptal gönderme</span><span class="sxs-lookup"><span data-stu-id="8dac2-279">Submit cancellation of CFDI invoices</span></span>

<span data-ttu-id="8dac2-280">**Yapılandırılabilir Elektronik faturalama tümleştirmesi** özelliği etkinleştirildikten sonra, CFDI faturalarını iptal etmek için kullanılan eski işlem artık kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="8dac2-280">After you turn on the **Configurable Electronic invoicing integration** feature, the old process for canceling CFDI invoices can no longer be used.</span></span> <span data-ttu-id="8dac2-281">**Elektronik belge gönderme günlüğü** sayfasına katıştırılmış yeni bir iptal işlemi ile değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-281">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

1. <span data-ttu-id="8dac2-282">**Alacak hesapları \> Sorgulamalar ve raporlar \> CFDI (elektronik faturalar)** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-282">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="8dac2-283">CFDI faturası **Onaylandı** durumundaysa, **İşlevler \> CFDI'yi iptal et** ögesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-283">If the CFDI invoice has a status of **Approved**, select **Functions \> Cancel CFDI**.</span></span>
3. <span data-ttu-id="8dac2-284">**Kuruluş Yönetimi \> Dönemlik \> Elektronik belgeler \> Elektronik belgeleri gönderme günlüğü** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-284">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
4. <span data-ttu-id="8dac2-285">CFDI faturasını seçin ve sonra **İşlevler \> İlgili gönderimleri gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-285">Select the CFDI invoice, and then select **Functions \> Send related submissions**.</span></span>
5. <span data-ttu-id="8dac2-286">İlgili gönderim için bir açıklama girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-286">Enter a description for the related submission, and then select **OK**.</span></span>

#### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="8dac2-287">İptal gönderim günlüklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="8dac2-287">View cancellation submission logs</span></span>

1. <span data-ttu-id="8dac2-288">**Kuruluş Yönetimi \> Dönemlik \> Elektronik belgeler \> Elektronik belgeleri gönderme günlüğü** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="8dac2-289">**Belge türü** alanında, yalnızca müşteri faturası günlüğü ile ilgili olarak filtre uygulamak için **Müşteri fatura günlüğü** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-289">In the **Document type** field, select **Customer invoice journal** to filter for customer invoice journal documents only.</span></span>
3. <span data-ttu-id="8dac2-290">CFDI faturasını seçin ve sonra Eylem Bölmesi'nde, **Sorgulamalar \> İlgili gönderim**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-290">Select the CFDI invoice, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="8dac2-291">**İlgili gönderimler** sayfası, belirli bir CFDI faturası için tüm ilgili gönderimleri ve bunların gönderim durumlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-291">The **Related submissions** page shows all related submissions, and their submission status, for a given CFDI invoice.</span></span> <span data-ttu-id="8dac2-292">Aşağıdaki çizimde, ilk satır, CFDI faturasının onayını talep eden gönderimi temsil eder.</span><span class="sxs-lookup"><span data-stu-id="8dac2-292">In the following illustration, the first line represents the submission that requested approval of the CFDI invoice.</span></span> <span data-ttu-id="8dac2-293">İkinci satır, bu CFDI faturasını iptal eden gönderimi temsil eder.</span><span class="sxs-lookup"><span data-stu-id="8dac2-293">The second line represents the submission that canceled that CFDI invoice.</span></span>

    ![İptal gönderim günlüklerini görüntüleme](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. <span data-ttu-id="8dac2-295">Eylem Bölmesi'nde, gönderme yürütme günlüklerinin ayrıntılarını görüntülemek için **Sorgulamalar \> Gönderme ayrıntıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="8dac2-295">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![İptal gönderim günlüğü detaylarını görüntüleme](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="8dac2-297">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="8dac2-297">Privacy notice</span></span>
<span data-ttu-id="8dac2-298">**CFDI Meksika elektronik fatura (MX)** özelliğinin etkinleştirilmesi kuruluş vergi kayıt kodunu içeren sınırlı verilerin gönderilmesini gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-298">Enabling the **CFDI Mexican electronic invoice (MX)** feature may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="8dac2-299">Bu, devlete ait Web servisi ile tümleştirme için gerekli önceden tanımlanmış biçimde vergi dairesine elektronik fatura göndermek amacıyla vergi dairesi tarafından yetkilendirilen üçüncü taraf kuruluşlarına iletilecektir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-299">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="8dac2-300">Bir yönetici, **Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri** sayfasına giderek **CFDI Meksika elektronik fatura (MX)** özelliğini etkinleştirebilir ve devre dışı bırakabilir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-300">An administrator can enable and disable the **CFDI Mexican electronic invoice (MX)** feature by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="8dac2-301">**Özellikler** sekmesini seçin, **CFDI Meksika elektronik fatura (MX)** özelliğini içeren satırları seçin ve sonra uygun seçimi yapın.</span><span class="sxs-lookup"><span data-stu-id="8dac2-301">Select the **Features** tab, select the rows containing the **CFDI Mexican electronic invoice (MX)** feature, and then make the appropriate selection.</span></span> <span data-ttu-id="8dac2-302">Bu harici sistemlerden alınan verilerin bu Dynamics 365 çevrimiçi hizmetine aktarılması [gizlilik bildirimimize](https://go.microsoft.com/fwlink/?LinkId=512132) tabidir.</span><span class="sxs-lookup"><span data-stu-id="8dac2-302">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="8dac2-303">Daha fazla bilgi için, lütfen ülkeye özel özellik belgelerindeki Gizlilik bildirimi bölümlerine bakın.</span><span class="sxs-lookup"><span data-stu-id="8dac2-303">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8dac2-304">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="8dac2-304">Additional resources</span></span>

- [<span data-ttu-id="8dac2-305">Elektronik faturalamaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="8dac2-305">Electronic invoicing overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="8dac2-306">Elektronik faturalamayı kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="8dac2-306">Get started with Electronic invoicing</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="8dac2-307">Elektronik faturalamayı ayarlama</span><span class="sxs-lookup"><span data-stu-id="8dac2-307">Set up Electronic invoicing</span></span>](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

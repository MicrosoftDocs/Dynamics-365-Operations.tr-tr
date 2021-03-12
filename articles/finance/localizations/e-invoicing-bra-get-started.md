---
title: Brezilya için Elektronik faturalama eklentisini kullanmaya başlangıç
description: Bu konu, Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management ile Brezilya için Elektronik faturalama eklentisini kullanmaya başlamanıza yardımcı olacak bilgiler içerir.
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 0320bd1d9e93cc30ed75f28e387ac2ec8dbfc226
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4962847"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a><span data-ttu-id="cec8f-103">Brezilya için Elektronik faturalama eklentisini kullanmaya başlangıç</span><span class="sxs-lookup"><span data-stu-id="cec8f-103">Get started with the Electronic invoicing add-on for Brazil</span></span> 

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> <span data-ttu-id="cec8f-104">Brezilya için elektronik faturalama eklentisi, şu anda Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management üzerinde oluşturulan mali belge tümleştirmelerinde kullanılabilen tüm işlevleri desteklemez.</span><span class="sxs-lookup"><span data-stu-id="cec8f-104">The Electronic invoicing add-on for Brazil doesn't currently support all the functions that are available in the fiscal document integration that is built into Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="cec8f-105">Bu konu, Brezilya için Elektronik faturalama eklentisini kullanmaya başlamanıza yardımcı olacak bilgiler içerir.</span><span class="sxs-lookup"><span data-stu-id="cec8f-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Brazil.</span></span> <span data-ttu-id="cec8f-106">Regulatory Configuration Services'te (RCS) ülkeye bağlı olan yapılandırma adımlarında Finance ve Supply Chain Management uygulamalarında size kılavuzluk eder.</span><span class="sxs-lookup"><span data-stu-id="cec8f-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and in Finance and Supply Chain Management.</span></span> <span data-ttu-id="cec8f-107">Ayrıca servis üzerinden bir NF-e mali belgesi (Elektronik mali belge modeli 55) gönderme sürecinde size yol gösterir ve işleme sonuçlarının ve mali belgelerin durumunun nasıl gözden geçirdiğinin açıklar.</span><span class="sxs-lookup"><span data-stu-id="cec8f-107">It also guides you through the process of submitting an NF-e fiscal document (Electronic fiscal document model 55) through the service, and it explains how review the processing results and the status of the fiscal documents.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cec8f-108">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="cec8f-108">Prerequisites</span></span>

<span data-ttu-id="cec8f-109">Bu konudaki adımları gerçekleştirmeden önce, [elektronik faturalama eklentisini kullanmaya başlama](e-invoicing-get-started.md) adımlarını tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="cec8f-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="cec8f-110">RCS kurulumu</span><span class="sxs-lookup"><span data-stu-id="cec8f-110">RCS setup</span></span>

<span data-ttu-id="cec8f-111">RCS kurulumu sırasında şu görevleri tamamlayacaksınız:</span><span class="sxs-lookup"><span data-stu-id="cec8f-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="cec8f-112">NF-e mali belgeleri için E-faturalama özelliğini içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="cec8f-112">Import the e-Invoicing feature for NF-e fiscal documents.</span></span>
2. <span data-ttu-id="cec8f-113">Onaya NF-e mali belgelerini göndermek için gerekli dosya biçimlerini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-113">Review the file formats that are required to submit NF-e fiscal documents for authorization.</span></span>
3. <span data-ttu-id="cec8f-114">Onaylı bir NF-e iptalini istemek için gereken dosya biçimlerini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-114">Review the file formats that are required to request the cancellation of an approved NF-e.</span></span>
4. <span data-ttu-id="cec8f-115">Onaya NF-e mali belgelerini göndermek için gerekli olayı yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="cec8f-115">Configure the event that is required to submit NF-e fiscal documents for authorization.</span></span>
5. <span data-ttu-id="cec8f-116">Onaylı bir NF-e iptalini istemek için gereken olayı yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="cec8f-116">Configure the event that is required to request the cancellation of an approved NF-e.</span></span>
6. <span data-ttu-id="cec8f-117">E-faturalama özelliğini elektronik faturalama eklenti ortamına atayın.</span><span class="sxs-lookup"><span data-stu-id="cec8f-117">Assign the e-Invoicing feature to an Electronic invoicing add-on environment.</span></span>
7. <span data-ttu-id="cec8f-118">E-faturalama özelliğini yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="cec8f-118">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="cec8f-119">"E-faturala özelliği", Elektronik faturalama eklenti sunucusunu kullanmak üzere yapılandırılmış ve yayımlanmış olan kaynağın genel adıdır.</span><span class="sxs-lookup"><span data-stu-id="cec8f-119">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="cec8f-120">E-fatura özellik kurulumu, başka şeylerin yanı sıra, yapılandırılabilir dışarı aktarma ve içe aktarma dosyaları oluşturmak için Elektronik Raporlama (ER) yapılandırma biçimlerinin kullanılması ve isteklerin gönderilmesi, yanıtları içe aktarmaya ve yanıt içeriğini ayrıştırmaya olanak tanıyan eylemleri ve eylem akışlarının kullanımını birleştirir.</span><span class="sxs-lookup"><span data-stu-id="cec8f-120">The setup of the e-Invoicing feature combines, among other things, the use of Electronic reporting (ER) configuration formats to create configurable export and import files, and the use of actions and actions flows to enable the creation of configurable rules to send requests, import responses, and parse the response contents.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="cec8f-121">E-faturalama özelliğini içe aktarma</span><span class="sxs-lookup"><span data-stu-id="cec8f-121">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="cec8f-122">RCS hesabınızda oturum açma</span><span class="sxs-lookup"><span data-stu-id="cec8f-122">Sign in to your RCS account</span></span>
2. <span data-ttu-id="cec8f-123">**Genelleştirme özellikleri** çalışma alanında **Özellikler** bölmesinde **E-faturalama** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-123">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="cec8f-124">**E-faturalama Özellikleri** sayfasında, Genel depodan NF-e mali belge E-faturalama özelliğini içe aktarmak için **İçe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-124">On the **e-Invoicing Features** page, select **Import** to import a NF-e fiscal document e-Invoicing feature from the Global repository.</span></span>

    ![İçe aktarma düğmesi](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. <span data-ttu-id="cec8f-126">NF-e mali belge özelliğini seçin ve **İçe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-126">Select the NF-e fiscal document feature, and then select **Import**.</span></span>

    ![NF-e özelliğini içe aktarma](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a><span data-ttu-id="cec8f-128">NF-e mali belgeler özelliğinin yeni bir sürümünü oluşturma</span><span class="sxs-lookup"><span data-stu-id="cec8f-128">Create a new version of the NF-e fiscal document feature</span></span>

- <span data-ttu-id="cec8f-129">**E-faturalama özellikleri** sayfasında, **Sürümler** sekmesinde, **Yeni** ögesini seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-129">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![Yeni e-faturalama özellik sürümü ekleme](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="cec8f-131">Yapılandırma sürümünü güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="cec8f-131">Update the configuration version</span></span>

1. <span data-ttu-id="cec8f-132">**E-faturalama özellikleri** sayfasında, **Yapılandırmalar** sekmesinde, yapılandırma sürümlerini (ER dosya biçimi yapılandırmaları) yönetmek için **Ekle** veya **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-132">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![E-faturalama özellik yapılandırmalarını yönetme](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - <span data-ttu-id="cec8f-134">NF-e mali belge özelliğinin yeni sürümünü oluşturduğunuzda, tüm yapılandırma sürümleri (ER dosya biçimleri) en son sürümden devralınır.</span><span class="sxs-lookup"><span data-stu-id="cec8f-134">When you create a new version of the NF-e fiscal document feature, all configuration version (ER file formats) are inherited from the latest version.</span></span>
    - <span data-ttu-id="cec8f-135">Onaya NF-e mali belgesini göndermek üzere aşağıdaki yapılandırma sürümleri gereklidir:</span><span class="sxs-lookup"><span data-stu-id="cec8f-135">To submit the NF-e fiscal document for authorization, the following configuration versions are required:</span></span>

        - <span data-ttu-id="cec8f-136">NFe gönderim dışa aktarma biçimi</span><span class="sxs-lookup"><span data-stu-id="cec8f-136">NFe submit export format</span></span>
        - <span data-ttu-id="cec8f-137">NFe yanıt iletisi alma</span><span class="sxs-lookup"><span data-stu-id="cec8f-137">NFe response message import</span></span>
        - <span data-ttu-id="cec8f-138">NFe hata günlüğü alma</span><span class="sxs-lookup"><span data-stu-id="cec8f-138">NFe error log import</span></span>

    - <span data-ttu-id="cec8f-139">NF-e iptalini göndermek için aşağıdaki yapılandırma sürümü gereklidir:</span><span class="sxs-lookup"><span data-stu-id="cec8f-139">To submit the NF-e cancellation, the following configuration version is required:</span></span>

        - <span data-ttu-id="cec8f-140">NFe iptal dışa aktarma biçimi</span><span class="sxs-lookup"><span data-stu-id="cec8f-140">NFe cancel export format</span></span>

2. <span data-ttu-id="cec8f-141">Listede bir yapılandırma sürümü seçin ve sonra da yapılandırmayı düzenleyebileceğiniz veya görüntüleyebileceğiniz **Biçim tasarımcısı** sayfasını açmak için **Düzenle** veya **Görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-141">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![Biçim tasarımcısı sayfasını açma](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. <span data-ttu-id="cec8f-143">**Biçim tasarımcısı** sayfasını, ER biçimi dosya yapılandırmalarını düzenlemek veya görüntülemek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="cec8f-143">Use the **Format designer** page to edit or view the ER format file configurations.</span></span> <span data-ttu-id="cec8f-144">Daha fazla bilgi için bkz. [Elektronik belge yapılandırmalarını oluşturma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).</span><span class="sxs-lookup"><span data-stu-id="cec8f-144">For more information, see [Create electronic document configurations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).</span></span>

    ![Biçim tasarımcısı sayfası](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="cec8f-146">E-faturalama özellik kurulumlarını yönetme</span><span class="sxs-lookup"><span data-stu-id="cec8f-146">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="cec8f-147">**E-faturalama özellikleri** sayfasında, **Kurulumlar** sekmesinde, E-faturalama özellik kurulumlarını (yani NF-e etkinlikleri) yönetmek için **Ekle** veya **Sil** ögesini seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-147">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add** or **Delete** to manage the e-Invoicing feature setups (that is, NF-e events).</span></span>

![E-faturalama özellik kurulumlarını yönetme](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="cec8f-149">Başka bir e-faturalama özelliğinden türetilen NF-e mali belge özelliğinin yeni bir sürümünü oluşturduğunuzda, tüm özellik kurulumları (NF-e olayları) en son sürümden devralınır.</span><span class="sxs-lookup"><span data-stu-id="cec8f-149">When you create a new version of the NF-e fiscal document feature that is derived from another e-Invoicing feature, all feature setups (NF-e events) are inherited from the latest version.</span></span>

<span data-ttu-id="cec8f-150">Onaya NF-e mali belgelerini göndermek için **Gönder** özellik kurulumu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="cec8f-150">To submit NF-e fiscal documents for authorization, the **Submit** feature setup is required.</span></span>

<span data-ttu-id="cec8f-151">NF-e iptali göndermek için **İptal** özelliği kurulumu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="cec8f-151">To submit NF-e cancellation, the **Cancellation** feature setup is required.</span></span>

#### <a name="configure-the-submit-feature-setup"></a><span data-ttu-id="cec8f-152">Gönderme özelliği kurulumunu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="cec8f-152">Configure the Submit feature setup</span></span>

1. <span data-ttu-id="cec8f-153">**E-faturalama özellikleri** sayfasında, **Kurulumlar** sekmesinde, **Özellik kurulumu** sütununda **Gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-153">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Submit**.</span></span>
2. <span data-ttu-id="cec8f-154">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-154">Select **Edit**.</span></span>

    ![E-faturalama özellik kurulumunu düzenleme](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="cec8f-156">**Özellik sürümü kurulumu** sayfasında, eylemler listesini yönetmek için **Eylemler** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-156">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span>

    ![Eylemler sekmesi](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. <span data-ttu-id="cec8f-158">Onaya NF-e göndermek için gerekli eylemleri gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-158">Review the actions that are required to submit an NF-e for authorization.</span></span>

    | <span data-ttu-id="cec8f-159">Eylem kodu</span><span class="sxs-lookup"><span data-stu-id="cec8f-159">Action ID</span></span> | <span data-ttu-id="cec8f-160">Eylem adı</span><span class="sxs-lookup"><span data-stu-id="cec8f-160">Action name</span></span>                  | <span data-ttu-id="cec8f-161">Eylem açıklaması</span><span class="sxs-lookup"><span data-stu-id="cec8f-161">Action description</span></span>                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | <span data-ttu-id="cec8f-162">1</span><span class="sxs-lookup"><span data-stu-id="cec8f-162">1</span></span>         | <span data-ttu-id="cec8f-163">Belgeyi dönüştür</span><span class="sxs-lookup"><span data-stu-id="cec8f-163">Transform document</span></span>           | <span data-ttu-id="cec8f-164">Gönderme için NF-e XML dosyasını oluşturun.</span><span class="sxs-lookup"><span data-stu-id="cec8f-164">Create the NF-e XML file for submission.</span></span>                          |
    | <span data-ttu-id="cec8f-165">2</span><span class="sxs-lookup"><span data-stu-id="cec8f-165">2</span></span>         | <span data-ttu-id="cec8f-166">Belgeyi imzala</span><span class="sxs-lookup"><span data-stu-id="cec8f-166">Sign document</span></span>                | <span data-ttu-id="cec8f-167">XML dosyasına dijital sertifika uygulayın.</span><span class="sxs-lookup"><span data-stu-id="cec8f-167">Apply the digital certificate to the XML file.</span></span>                    |
    | <span data-ttu-id="cec8f-168">3</span><span class="sxs-lookup"><span data-stu-id="cec8f-168">3</span></span>         | <span data-ttu-id="cec8f-169">Brezilya SEFAZ hizmetini çağır</span><span class="sxs-lookup"><span data-stu-id="cec8f-169">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="cec8f-170">İmzalı XML dosyasını yetkilendirme için Web hizmetlerine gönderin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-170">Submit the signed XML file to the web services for authorization.</span></span> |
    | <span data-ttu-id="cec8f-171">4</span><span class="sxs-lookup"><span data-stu-id="cec8f-171">4</span></span>         | <span data-ttu-id="cec8f-172">Yanıtı işle</span><span class="sxs-lookup"><span data-stu-id="cec8f-172">Process response</span></span>             | <span data-ttu-id="cec8f-173">Web servis yanıtını alın.</span><span class="sxs-lookup"><span data-stu-id="cec8f-173">Get the web service response.</span></span>                                     |
    | <span data-ttu-id="cec8f-174">5</span><span class="sxs-lookup"><span data-stu-id="cec8f-174">5</span></span>         | <span data-ttu-id="cec8f-175">Belgeyi dönüştür</span><span class="sxs-lookup"><span data-stu-id="cec8f-175">Transform document</span></span>           | <span data-ttu-id="cec8f-176">Yanıt olarak alınan dosyanın içeriğini ayrıştırın.</span><span class="sxs-lookup"><span data-stu-id="cec8f-176">Parse the content of the file that is received as a response.</span></span>     |
    | <span data-ttu-id="cec8f-177">6</span><span class="sxs-lookup"><span data-stu-id="cec8f-177">6</span></span>         | <span data-ttu-id="cec8f-178">Belgeyi dönüştür</span><span class="sxs-lookup"><span data-stu-id="cec8f-178">Transform document</span></span>           | <span data-ttu-id="cec8f-179">Gönderimin durumunu sorgulamak için XML dosyasını oluşturun.</span><span class="sxs-lookup"><span data-stu-id="cec8f-179">Create the XML file to inquire about status of the submission.</span></span>    |
    | <span data-ttu-id="cec8f-180">7</span><span class="sxs-lookup"><span data-stu-id="cec8f-180">7</span></span>         | <span data-ttu-id="cec8f-181">Brezilya SEFAZ hizmetini çağır</span><span class="sxs-lookup"><span data-stu-id="cec8f-181">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="cec8f-182">Gönderme durumunu talep eden XML dosyasını gönderin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-182">Submit the XML file that requests the submission status.</span></span>          |
    | <span data-ttu-id="cec8f-183">8</span><span class="sxs-lookup"><span data-stu-id="cec8f-183">8</span></span>         | <span data-ttu-id="cec8f-184">Yanıtı işle</span><span class="sxs-lookup"><span data-stu-id="cec8f-184">Process response</span></span>             | <span data-ttu-id="cec8f-185">Web servis yanıtını alın.</span><span class="sxs-lookup"><span data-stu-id="cec8f-185">Get the web service response.</span></span>                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a><span data-ttu-id="cec8f-186">SEFAZ Web Hizmetleri için URL'yi ayarlama</span><span class="sxs-lookup"><span data-stu-id="cec8f-186">Set up the URL for SEFAZ web services</span></span> 

1. <span data-ttu-id="cec8f-187">**Özellik sürümü kurulumu** sayfasında, **Eylemler** sekmesindeki **Eylemler** hızlı sekmesinde, **Brezilya SEFAZ servisini çağır** seçeneğini belirleyin (eylem kimliği **3**).</span><span class="sxs-lookup"><span data-stu-id="cec8f-187">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **3**).</span></span>
2. <span data-ttu-id="cec8f-188">**Parametreler** hızlı sekmesinde, **URL adresi parametresi** alanına, NF-e gönderimi için SEFAZ Web hizmetinin URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-188">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for NF-e submission.</span></span>
3. <span data-ttu-id="cec8f-189">**Eylemler** hızlı sekmesinde, **Brezilya SEFAZ servisini çağır** (eylem kimliği **7**) öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-189">On the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **7**).</span></span>
4. <span data-ttu-id="cec8f-190">**Parametreler** hızlı sekmesinde, **URL adresi parametresi** alanına, NF-e gönderimi için SEFAZ Web hizmetinin URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-190">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for NF-e submission.</span></span>

#### <a name="configure-the-cancellation-feature-setup"></a><span data-ttu-id="cec8f-191">İptal özelliği kurulumunu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="cec8f-191">Configure the Cancellation feature setup</span></span>

1. <span data-ttu-id="cec8f-192">**E-faturalama özellikleri** sayfasında, **Kurulumlar** sekmesinde, **Özellik kurulumu** sütununda **İptal**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-192">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Cancellation**.</span></span>
2. <span data-ttu-id="cec8f-193">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-193">Select **Edit**.</span></span>
3. <span data-ttu-id="cec8f-194">**Özellik sürümü kurulumu** sayfasında, eylemler listesini yönetmek için **Eylemler** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-194">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span>
4. <span data-ttu-id="cec8f-195">Onaylı bir NF-e iptalini istemek için gereken eylemleri gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-195">Review the actions that are required to request the cancellation of an approved NF-e.</span></span>

    | <span data-ttu-id="cec8f-196">Eylem kodu</span><span class="sxs-lookup"><span data-stu-id="cec8f-196">Action ID</span></span> | <span data-ttu-id="cec8f-197">Eylem adı</span><span class="sxs-lookup"><span data-stu-id="cec8f-197">Action name</span></span>                  | <span data-ttu-id="cec8f-198">Eylem açıklaması</span><span class="sxs-lookup"><span data-stu-id="cec8f-198">Action description</span></span>                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="cec8f-199">1</span><span class="sxs-lookup"><span data-stu-id="cec8f-199">1</span></span>         | <span data-ttu-id="cec8f-200">Belgeyi dönüştür</span><span class="sxs-lookup"><span data-stu-id="cec8f-200">Transform document</span></span>           | <span data-ttu-id="cec8f-201">Gönderme için NF-e iptal XML dosyasını oluşturun.</span><span class="sxs-lookup"><span data-stu-id="cec8f-201">Create the NF-e cancellation XML file for submission.</span></span>            |
    | <span data-ttu-id="cec8f-202">2</span><span class="sxs-lookup"><span data-stu-id="cec8f-202">2</span></span>         | <span data-ttu-id="cec8f-203">Belgeyi imzala</span><span class="sxs-lookup"><span data-stu-id="cec8f-203">Sign document</span></span>                | <span data-ttu-id="cec8f-204">XML dosyasına dijital sertifika uygulayın.</span><span class="sxs-lookup"><span data-stu-id="cec8f-204">Apply the digital certificate to the XML file.</span></span>                   |
    | <span data-ttu-id="cec8f-205">3</span><span class="sxs-lookup"><span data-stu-id="cec8f-205">3</span></span>         | <span data-ttu-id="cec8f-206">Brezilya SEFAZ hizmetini çağır</span><span class="sxs-lookup"><span data-stu-id="cec8f-206">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="cec8f-207">İmzalı XML dosyasını iptal için Web hizmetlerine gönderin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-207">Submit the signed XML file to the web services for cancellation.</span></span> |
    | <span data-ttu-id="cec8f-208">4</span><span class="sxs-lookup"><span data-stu-id="cec8f-208">4</span></span>         | <span data-ttu-id="cec8f-209">Yanıtı işle</span><span class="sxs-lookup"><span data-stu-id="cec8f-209">Process response</span></span>             | <span data-ttu-id="cec8f-210">Web servis yanıtını alın.</span><span class="sxs-lookup"><span data-stu-id="cec8f-210">Get the web service response.</span></span>                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a><span data-ttu-id="cec8f-211">SEFAZ Web Hizmetleri için URL'yi ayarlama</span><span class="sxs-lookup"><span data-stu-id="cec8f-211">Set up the URL for SEFAZ web services</span></span>

1. <span data-ttu-id="cec8f-212">**Özellik sürümü kurulumu** sayfasında, **Eylemler** sekmesindeki **Eylemler** hızlı sekmesinde, **Brezilya SEFAZ servisini çağır** seçeneğini belirleyin (eylem kimliği **3**).</span><span class="sxs-lookup"><span data-stu-id="cec8f-212">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **3**).</span></span>
2. <span data-ttu-id="cec8f-213">**Parametreler** hızlı sekmesinde, **URL adresi parametresi** alanına, onaylı NF-e iptali için SEFAZ Web hizmetinin URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-213">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for cancellation of an approved NF-e.</span></span>

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a><span data-ttu-id="cec8f-214">E-faturalama ortamını kullanılabilir hale getirme ve Taslak sürümü atama</span><span class="sxs-lookup"><span data-stu-id="cec8f-214">Make an e-Invoicing environment available and assign a Draft version</span></span>

1. <span data-ttu-id="cec8f-215">**E-faturalama özellikleri** sayfasında, **Ortamlar** sekmesinde, **Etkinleştir** ögesini seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-215">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="cec8f-216">**Ortamlar** alanında, ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-216">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="cec8f-217">**Geçerlilik başlangıcı** alanında, yeni ortamın geçerli olacağı tarihi seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-217">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="cec8f-218">**Etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-218">Select **Enable**.</span></span>

![E-faturalama ortamını etkinleştirme](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a><span data-ttu-id="cec8f-220">Durumu Tamamlandı olarak değiştirme</span><span class="sxs-lookup"><span data-stu-id="cec8f-220">Change the status to Completed</span></span>

1. <span data-ttu-id="cec8f-221">**E-faturalama Özellikleri** sayfasındaki **Sürümler** sekmesinde, **Taslak** durumundaki e-faturalama özelliğinin sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-221">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="cec8f-222">**Durumu değiştir \> Tamamla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-222">Select **Change status \> Complete**.</span></span>

### <a name="change-the-status-to-publish"></a><span data-ttu-id="cec8f-223">Durumu Yayımla olarak değiştirme</span><span class="sxs-lookup"><span data-stu-id="cec8f-223">Change the status to Publish</span></span>

1. <span data-ttu-id="cec8f-224">**E-faturalama Özellikleri** sayfasındaki **Sürümler** sekmesinde, **Tamamlandı** durumundaki e-faturalama özelliğinin sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-224">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="cec8f-225">**Durumu değiştir \> Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-225">Select **Change status \> Publish**.</span></span>

![E-faturalama özelliğini yayımlama](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a><span data-ttu-id="cec8f-227">Finance ve Supply Chain Management uygulamalarında Elektronik faturalama eklenti kurulumu</span><span class="sxs-lookup"><span data-stu-id="cec8f-227">Set up Electronic invoicing add-on integration in Finance or Supply Chain Management</span></span>

<span data-ttu-id="cec8f-228">Kurulum sırasında şu görevleri tamamlayacaksınız:</span><span class="sxs-lookup"><span data-stu-id="cec8f-228">During setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="cec8f-229">Brezilya için NF-e Federal özelliğini açın.</span><span class="sxs-lookup"><span data-stu-id="cec8f-229">Turn on the NF-e Federal feature for Brazil.</span></span>
2. <span data-ttu-id="cec8f-230">Belirli ER veri modelini, ER veri modeli eşleştirmesini ve NF-e mali belgeleri için gereken biçimleri içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="cec8f-230">Import the specific ER data model, the data model mapping, and the formats that are required for NF-e fiscal documents.</span></span>
3. <span data-ttu-id="cec8f-231">ER yapılandırmalarını içe aktarın ve gönderme işleminin sonucu döndürüldükten sonra mali belgenizin durumunu güncelleştirmek için gerekli olan yanıt tiplerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cec8f-231">Import the ER configuration, and set up the response types that are required to update the status of the fiscal document after the submission process is returned.</span></span>

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a><span data-ttu-id="cec8f-232">Brezilya için NF-e Federal özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="cec8f-232">Turn on the NF-e Federal feature for Brazil</span></span>

1. <span data-ttu-id="cec8f-233">**Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-233">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="cec8f-234">**Özellikler** sekmesinde, **BR00053** özellik referansları için satırlarda **Etkinleştir** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-234">On the **Features** tab, select the **Enable** check box in the row for feature reference **BR00053**.</span></span>

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a><span data-ttu-id="cec8f-235">NF-e mali belgeleri için gerekli ER veri modeli eşleştirmesini içe aktarma</span><span class="sxs-lookup"><span data-stu-id="cec8f-235">Import the ER data model mapping required for NF-e fiscal documents</span></span>

1. <span data-ttu-id="cec8f-236">Finance'de oturum açın.</span><span class="sxs-lookup"><span data-stu-id="cec8f-236">Sign in to Finance.</span></span>
2. <span data-ttu-id="cec8f-237">**Elektronik raporlama** çalışma alanında, **Yapılandırma sağlayıcıları** bölümünde, **Microsoft**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-237">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** tile.</span></span> <span data-ttu-id="cec8f-238">Bu yapılandırma sağlayıcısının **Etkin** olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="cec8f-238">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="cec8f-239">Sağlayıcının **Etkin** olarak nasıl ayarlanacağı hakkında daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve etkin olarak işaretleme](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="cec8f-239">For information about how to set a provider to **Active**, see [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span></span>
3. <span data-ttu-id="cec8f-240">**Depolar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-240">Select **Repositories**.</span></span>
4. <span data-ttu-id="cec8f-241">**Genel kaynak \> Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-241">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="cec8f-242">**Mali belge eşleme** yapılandırmalarını içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="cec8f-242">Import **Fiscal documents mapping** configurations.</span></span>

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a><span data-ttu-id="cec8f-243">ER yapılandırmalarını içe aktarma ve mali belgeler için yanıt tiplerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="cec8f-243">Import ER configurations and set up the response types for fiscal documents</span></span>

1. <span data-ttu-id="cec8f-244">**Elektronik raporlama** çalışma alanında, **Yapılandırma sağlayıcıları** bölümünde, **Microsoft**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-244">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** tile.</span></span>
2. <span data-ttu-id="cec8f-245">**Depolar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-245">Select **Repositories**.</span></span>
3. <span data-ttu-id="cec8f-246">**Genel kaynak \> Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-246">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="cec8f-247">**NF-e hata günlük alma (BR)**, **NF-e yanıt veri alma biçimi (BR)** ve **NF-e yanıt iletisi alma (BR)** ögelerini içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="cec8f-247">Import **NF-e error log import (BR)**, **NF-e response data import format (BR)**, and **NF-e response message import (BR)**.</span></span>
5. <span data-ttu-id="cec8f-248">**Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-248">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
6. <span data-ttu-id="cec8f-249">**Elektronik belge** sekmesinde **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-249">On the **Electronic document** tab, select **Add**.</span></span>
6. <span data-ttu-id="cec8f-250">**Tablo adı** alanında, **Mali belge başlığı** değerini girin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-250">In the **Table name** field, enter **Fiscal document header**.</span></span>
7. <span data-ttu-id="cec8f-251">**Belge bağlamı** alanında, **Müşteri faturası bağlam modeli – Mali belge bağlamı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-251">In the **Document context** field, select **Customer invoice context model – Fiscal document context**.</span></span>
8. <span data-ttu-id="cec8f-252">**Yanıt türleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-252">Select **Response types**.</span></span>
9. <span data-ttu-id="cec8f-253">**Yeni**'yi seçin ve sonra **Yanıt türü** alanında, **Yanıt**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-253">Select **New**, and then, in the **Response type** field, select **Response**.</span></span>
10. <span data-ttu-id="cec8f-254">**Gönderim durumu** alanında, **Bekliyor**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-254">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="cec8f-255">**Model eşleme** alanında, **Yanıt iletisi içe aktarma biçimi - Yanıt iletisinden model eşlemesi** ögesini seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-255">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
12. <span data-ttu-id="cec8f-256">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-256">Select **Save**.</span></span>
13. <span data-ttu-id="cec8f-257">**Yeni**'yi seçin ve sonra **Yanıt türü** alanında, **ResponseData** ögesini girin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-257">Select **New**, and then, in the **Response type** field, enter **ResponseData**.</span></span>
14. <span data-ttu-id="cec8f-258">**Gönderim durumu** alanında, **Bekliyor**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-258">In the **Submission status** field, select **Pending**.</span></span>
15. <span data-ttu-id="cec8f-259">**Model eşleme** alanında, **NFe yanıtı veri içe aktarma biçimi – Yanıt verilerini içe aktarma** ögesini seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-259">In the **Model mapping** field, select **NFe response data import format – Response data import**.</span></span>
16. <span data-ttu-id="cec8f-260">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-260">Select **Save**.</span></span>

## <a name="electronic-invoice-processing"></a><span data-ttu-id="cec8f-261">Elektronik fatura işleme</span><span class="sxs-lookup"><span data-stu-id="cec8f-261">Electronic invoice processing</span></span>

<span data-ttu-id="cec8f-262">Finance'de işlem sırasında şu görevleri tamamlayacaksınız:</span><span class="sxs-lookup"><span data-stu-id="cec8f-262">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="cec8f-263">Elektronik faturalama eklentisi aracılığıyla mali belge gönderin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-263">Submit a fiscal document through the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="cec8f-264">Gönderme yürütme günlüklerini görüntüleyin ve işlemenin sonuçlarını gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-264">View the submission execution logs and review the results of processing.</span></span>
3. <span data-ttu-id="cec8f-265">Elektronik faturalama eklentisi aracılığıyla mali belge iptalini gönderin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-265">Submit the cancellation of a fiscal document through the Electronic invoicing add-on.</span></span>

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a><span data-ttu-id="cec8f-266">SEFAZ yetkilendirmesi için NF-e mali belgeleri gönderme</span><span class="sxs-lookup"><span data-stu-id="cec8f-266">Submit NF-e fiscal documents for SEFAZ authorization</span></span> 

<span data-ttu-id="cec8f-267">**Yapılandırılabilir Elektronik faturalama eklenti tümleştirmesi** özelliğini açtıktan sonra, onaya NF-e mali belgelerini göndermek için kullanılan eski işlem (**NF-e işlemini dışa/içe aktarma**) artık kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="cec8f-267">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for submitting NF-e fiscal documents for authorization (**Export/Import NF-e process**) can no longer be used.</span></span> <span data-ttu-id="cec8f-268">**Elektronik belge gönderme** adı verilen yeni bir işlemle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="cec8f-268">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="cec8f-269">Devam etmeden önce, müşterinin mali kurulumu tarafından verilen bir veya daha fazla müşteri mali belge modeli 55 olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="cec8f-269">Before you continue, make sure that you have one or more customer fiscal documents model 55 that were issued by the customer's fiscal establishment.</span></span> <span data-ttu-id="cec8f-270">Bu mali belgelerin yönü **Giden** olarak ayarlanmalıdır ve durumu **Oluşturuldu** olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="cec8f-270">The direction for these fiscal documents must be set to **Outgoing**, and the status must be **Created**.</span></span> <span data-ttu-id="cec8f-271">Daha fazla bilgi için bkz. [Müşteri mali belgelerini düzenleme (Brezilya)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).</span><span class="sxs-lookup"><span data-stu-id="cec8f-271">For more information, see [Issue customer fiscal document (Brazil)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).</span></span>

1. <span data-ttu-id="cec8f-272">**Kuruluş Yönetimi \> Dönemlik \> Elektronik belgeler \> Elektronik belgeleri gönder** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-272">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="cec8f-273">Herhangi bir belgenin ilk gönderimi için, **Belgeyi yeniden gönder** seçeneğini her zaman **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cec8f-273">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="cec8f-274">Belgeyi servis aracılığıyla yeniden göndermeniz gerekiyorsa, bu seçeneği **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cec8f-274">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="cec8f-275">**Dahil edilecek kayıtlar** hızlı sekmesinde, gönderilecek belgeleri seçmek üzere bir sorgu oluşturabileceğiniz **Sorgulama** iletişim kutusunu açmak için **Filtre**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-275">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>
4. <span data-ttu-id="cec8f-276">**Aralık** sekmesinde **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-276">On the **Range** tab, select **Add**.</span></span>
5. <span data-ttu-id="cec8f-277">**Tablo** alanında, **Mali belge başlığı** değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-277">In the **Table** field, select **Fiscal document header**.</span></span>
6. <span data-ttu-id="cec8f-278">**Türetilmiş tablo** alanında, **Mali belge başlığı** değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-278">In the **Derived table** field, select **Fiscal document header**.</span></span>
6. <span data-ttu-id="cec8f-279">**Alan** alanında, **Numara** değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-279">In the **Field** field, select **Number**.</span></span>
7. <span data-ttu-id="cec8f-280">**Ölçüt** alanına, gönderilmesi gereken mali belgenin numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-280">In the **Criteria** field, enter the number of the fiscal document that should be submitted.</span></span>
8. <span data-ttu-id="cec8f-281">**Sorgulama** iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-281">Select **OK** to close the **Inquiry** dialog box.</span></span>
8. <span data-ttu-id="cec8f-282">Seçili belgeleri göndermek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-282">Select **OK** to submit the selected documents.</span></span>

> [!NOTE]
> <span data-ttu-id="cec8f-283">Servis aracılığıyla ilk belgeyi gönderme denemeniz sırasında, Elektronik faturalama eklentisi ile bağlantıyı onaylamanız istenecektir.</span><span class="sxs-lookup"><span data-stu-id="cec8f-283">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="cec8f-284">**Elektronik Belge Gönderme Hizmetine bağlanmak için burayı tıklayın** ögesini seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-284">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-all-submission-logs"></a><span data-ttu-id="cec8f-285">Bütün gönderme günlüklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="cec8f-285">View all submission logs</span></span>

<span data-ttu-id="cec8f-286">**Yapılandırılabilir Elektronik faturalama eklenti tümleştirmesi** özelliğini açtıktan sonra, belge gönderme işlemini takip etmenizi sağlayan yeni bir sayfa kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="cec8f-286">After you turn on the **Configurable Electronic invoicing add-on integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="cec8f-287">Gönderilen tüm belgelerin gönderme günlüklerini görüntülemek için bu sayfayı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cec8f-287">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="cec8f-288">**Kuruluş Yönetimi \> Dönemlik \> Elektronik belgeler \> Elektronik belgeleri gönderme günlüğü** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="cec8f-289">**Belge türü** alanında, yalnızca mali belgelerle ilgili filtre uygulamak için **Mali belge başlığı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-289">In the **Document type** field, select **Fiscal document header** to filter for fiscal documents only.</span></span>
3. <span data-ttu-id="cec8f-290">Eylem Bölmesi'nde, gönderme yürütme günlüklerinin ayrıntılarını görüntülemek için **Sorgulamalar \> Gönderme ayrıntıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-290">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

![Gönderme günlüğü ayrıntılarını görüntüleme](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> <span data-ttu-id="cec8f-292">NF-e mali belgeler için **Hata kodu** sütunu, SEFAZ Web hizmeti tarafından döndürülen dönüş kodunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="cec8f-292">For NF-e fiscal documents, the **Error code** column shows the return code that was returned by SEFAZ web services.</span></span>

### <a name="view-submission-logs-through-the-fiscal-document-page"></a><span data-ttu-id="cec8f-293">Mali belge sayfası yoluyla gönderme günlüklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="cec8f-293">View submission logs through the fiscal document page</span></span>

<span data-ttu-id="cec8f-294">**Yapılandırılabilir Elektronik faturalandırma eklentisi tümleştirme** özelliğini açtıktan sonra, mali belge sayfası aracılığıyla gönderme günlüklerini de görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cec8f-294">After you turn on the **Configurable Electronic invoicing add-on integration** feature, you can also view the submission logs through the fiscal document page.</span></span>

1. <span data-ttu-id="cec8f-295">**Genel muhasebe \> Sorgulamalar ve raporlar \> Mali belgeler \> Tüm mali belgeler** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-295">Go to **General ledger \> Inquiries and reports \> Fiscal documents \> All fiscal documents**.</span></span>
2. <span data-ttu-id="cec8f-296">Daha önce Elektronik faturalama eklentisi aracılığıyla gönderilen bir mali belge seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-296">Select a fiscal document that was previously submitted through the Electronic invoicing add-on.</span></span>
3. <span data-ttu-id="cec8f-297">Eylem Bölmesi'ndeki **NF-e federal** sekmesinde, **Elektronik belge günlüğü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-297">On the Action Pane, on the **NF-e federal** tab, select **Electronic document log**.</span></span>

![Mali belge sayfası yoluyla gönderme günlüklerini görüntüleme](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a><span data-ttu-id="cec8f-299">SEFAZ iptali için onaylı NF-e mali belgeleri gönderme</span><span class="sxs-lookup"><span data-stu-id="cec8f-299">Submit approved NF-e fiscal documents for SEFAZ cancellation</span></span>

<span data-ttu-id="cec8f-300">**Yapılandırılabilir Elektronik faturalama eklentisi tümleştirmesi** özelliği etkinleştirildikten sonra, NF-e mali belgelerini iptal etmek için kullanılan eski işlem artık kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="cec8f-300">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for canceling NF-e fiscal documents can no longer be used.</span></span> <span data-ttu-id="cec8f-301">**Elektronik belge gönderme günlüğü** sayfasına katıştırılmış yeni bir iptal işlemi ile değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="cec8f-301">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

> [!NOTE]
> <span data-ttu-id="cec8f-302">Onaylanmış bir NF-e mali belge için müşteri mali belgesini iptal etme işlemini çalıştırdığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="cec8f-302">Make sure that you've run the cancellation of the customer fiscal document for an approved NF-e fiscal document.</span></span> <span data-ttu-id="cec8f-303">Daha fazla bilgi için bkz. [Müşteri mali belgelerini iptal etme (Brezilya)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).</span><span class="sxs-lookup"><span data-stu-id="cec8f-303">For more information see, [Cancel customer fiscal document (Brazil)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).</span></span>

1. <span data-ttu-id="cec8f-304">**Kuruluş Yönetimi \> Dönemlik \> Elektronik belgeler \> Elektronik belgeleri gönderme günlüğü** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-304">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="cec8f-305">Mali belgeyi seçin ve sonra **İşlevler \> İlgili gönderimleri gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-305">Select the fiscal document, and then select **Functions \> Send related submissions**.</span></span>
3. <span data-ttu-id="cec8f-306">İlgili gönderim için bir açıklama girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-306">Enter a description for the related submission, and then select **OK**.</span></span>

### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="cec8f-307">İptal gönderim günlüklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="cec8f-307">View cancellation submission logs</span></span>

1. <span data-ttu-id="cec8f-308">**Kuruluş Yönetimi \> Dönemlik \> Elektronik belgeler \> Elektronik belgeleri gönderme günlüğü** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-308">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="cec8f-309">**Belge türü** alanında, yalnızca mali belgelerle ilgili filtre uygulamak için **Mali belge başlığı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-309">In the **Document type** field, select **Fiscal document header** to filter for fiscal documents only.</span></span>
3. <span data-ttu-id="cec8f-310">Mali belgeyi seçin ve sonra Eylem Bölmesi'nde, **Sorgulamalar \> İlgili gönderim**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-310">Select the fiscal document, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="cec8f-311">İlgili gönderimler, ilk olarak yapılan ana gönderimle ilgili gönderimlerdir.</span><span class="sxs-lookup"><span data-stu-id="cec8f-311">Related submissions are submissions that are related to a main submission that was made first.</span></span> <span data-ttu-id="cec8f-312">Örneğin, belirli bir NFe'ye yetki veren gönderim ana gönderimdir.</span><span class="sxs-lookup"><span data-stu-id="cec8f-312">For example, the submission that authorizes a specific NF-e is the main submission.</span></span> <span data-ttu-id="cec8f-313">SEFAZ içinde aynı NF-e'nin iptal işlemini isteyen gönderim ilgili bir gönderimdir.</span><span class="sxs-lookup"><span data-stu-id="cec8f-313">The submission that requests the cancellation of the same NF-e in SEFAZ is a related submission.</span></span> <span data-ttu-id="cec8f-314">Yalnızca, başka bir gönderimden yapılan işin iptal edilmesini talep ettiğinden var olur.</span><span class="sxs-lookup"><span data-stu-id="cec8f-314">It exists only because it's requesting the cancellation of the job that was done through another submission.</span></span>

    <span data-ttu-id="cec8f-315">**İlgili gönderimler** sayfası, belirli bir mali belge için tüm ilgili gönderimleri ve bunların gönderim durumlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cec8f-315">The **Related submissions** page shows all related submissions, and their submission status, for a given fiscal document.</span></span> <span data-ttu-id="cec8f-316">Aşağıdaki çizimde, ilk satır, mali belgenin onayını talep eden gönderimi temsil eder.</span><span class="sxs-lookup"><span data-stu-id="cec8f-316">In the following illustration, the first line represents the submission that requested approval of the fiscal document.</span></span> <span data-ttu-id="cec8f-317">İkinci satır, bu mali belgeyi iptal eden gönderimi temsil eder.</span><span class="sxs-lookup"><span data-stu-id="cec8f-317">The second line represents the submission that canceled that fiscal document.</span></span>

    ![İptal gönderim günlüklerini görüntüleme](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. <span data-ttu-id="cec8f-319">Eylem Bölmesi'nde, gönderme yürütme günlüklerinin ayrıntılarını görüntülemek için **Sorgulamalar \> Gönderme ayrıntıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="cec8f-319">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![İptal gönderim günlüğü detaylarını görüntüleme](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="cec8f-321">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="cec8f-321">Privacy notice</span></span>
<span data-ttu-id="cec8f-322">BR-00053 (NF-e Federal) özelliğinin etkinleştirilmesi, kuruluş vergi kayıt kodunu içeren sınırlı verilerin gönderilmesini gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="cec8f-322">Enabling the BR-00053 (NF-e Federal) feature may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="cec8f-323">Bu, devlete ait Web servisi ile tümleştirme için gerekli önceden tanımlanmış biçimde vergi dairesine elektronik fatura göndermek amacıyla vergi dairesi tarafından yetkilendirilen üçüncü taraf kuruluşlarına iletilecektir.</span><span class="sxs-lookup"><span data-stu-id="cec8f-323">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="cec8f-324">Bir yönetici, **Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri** sayfasına giderek BR-00053 (NF-e Federal) özelliğini etkinleştirebilir ve devre dışı bırakabilir.</span><span class="sxs-lookup"><span data-stu-id="cec8f-324">An administrator can enable and disable the BR-00053 (NF-e Federal) feature by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="cec8f-325">**Özellikler** sekmesini seçin, BR-00053 özelliğini içeren satırı seçin ve sonra uygun seçimi yapın.</span><span class="sxs-lookup"><span data-stu-id="cec8f-325">Select the **Features** tab, select the row containing the BR-00053 feature, and then make the appropriate selection.</span></span> <span data-ttu-id="cec8f-326">Bu harici sistemlerden alınan verilerin bu Dynamics 365 çevrimiçi hizmetine aktarılması [gizlilik bildirimimize](https://go.microsoft.com/fwlink/?LinkId=512132) tabidir.</span><span class="sxs-lookup"><span data-stu-id="cec8f-326">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="cec8f-327">Daha fazla bilgi için, lütfen ülkeye özel özellik belgelerindeki Gizlilik bildirimi bölümlerine bakın.</span><span class="sxs-lookup"><span data-stu-id="cec8f-327">Please consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="cec8f-328">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="cec8f-328">Additional resources</span></span>

- [<span data-ttu-id="cec8f-329">Elektronik faturalama eklentisine genel bakış</span><span class="sxs-lookup"><span data-stu-id="cec8f-329">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="cec8f-330">Elektronik faturalama eklentisini kullanmaya başlangıç</span><span class="sxs-lookup"><span data-stu-id="cec8f-330">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="cec8f-331">Elektronik faturalamayı eklentisini kurma</span><span class="sxs-lookup"><span data-stu-id="cec8f-331">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)

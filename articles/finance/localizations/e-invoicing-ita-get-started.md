---
title: İtalya için Elektronik faturalama eklentisini kullanmaya başlangıç
description: Bu konu, Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management ile İtalya için Elektronik faturalama eklentisini kullanmaya başlamanıza yardımcı olacak bilgiler içerir.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c513141f820c95fe3842478361693701f1e3641b
ms.sourcegitcommit: f860ac2b18f6bbbfc4a46b497baec2477105b116
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/19/2020
ms.locfileid: "4448992"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-italy"></a><span data-ttu-id="52946-103">İtalya için Elektronik faturalama eklentisini kullanmaya başlangıç</span><span class="sxs-lookup"><span data-stu-id="52946-103">Get started with the Electronic invoicing add-on for Italy</span></span>

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> <span data-ttu-id="52946-104">İtalya için Elektronik faturalama eklentisi, Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management içinden elektronik fatura için kullanılabilen tüm işlevleri şimdilik desteklemeyebilir.</span><span class="sxs-lookup"><span data-stu-id="52946-104">The Electronic invoicing add-on for Italy might not currently support all the functions that are available for electronic invoices in Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> 

<span data-ttu-id="52946-105">Bu konu, İtalya için Elektronik faturalama eklentisini kullanmaya başlamanıza yardımcı olacak bilgiler içerir.</span><span class="sxs-lookup"><span data-stu-id="52946-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Italy.</span></span> <span data-ttu-id="52946-106">Regulatory Configuration Services (RCS) ve Finance için ülkeye bağlı olan yapılandırma adımlarında size kılavuzluk eder.</span><span class="sxs-lookup"><span data-stu-id="52946-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="52946-107">Ayrıca, hizmet yoluyla İtalya'ya özel **FatturaPA** biçiminde oluşturulan elektronik faturaları gönderme sürecinde size yol gösterir ve işleme sonuçlarının nasıl incelendiğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="52946-107">It also guides you through the process for submitting electronic invoices that are generated in the Italy-specific **FatturaPA** format through the service, and it explains how to review the results of processing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="52946-108">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="52946-108">Prerequisites</span></span>

<span data-ttu-id="52946-109">Bu konudaki adımları gerçekleştirmeden önce, [elektronik faturalama eklentisini kullanmaya başlama](e-invoicing-get-started.md) adımlarını tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="52946-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="52946-110">RCS kurulumu</span><span class="sxs-lookup"><span data-stu-id="52946-110">RCS setup</span></span>

<span data-ttu-id="52946-111">RCS kurulumu sırasında şu görevleri tamamlayacaksınız:</span><span class="sxs-lookup"><span data-stu-id="52946-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="52946-112">Müşteri elektronik faturalarının **FatturaPA** formatında dışa aktarılması için e-faturalama özelliğini içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="52946-112">Import the e-Invoicing feature for the export of customer electronic invoices in the **FatturaPA** format.</span></span>
2. <span data-ttu-id="52946-113">Elektronik faturalar hakkında yanıtlar oluşturmak, göndermek ve almak için gerekli olan biçim yapılandırmalarını gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="52946-113">Review the format configurations that are required to generate, submit, and receive responses about electronic invoices.</span></span>
3. <span data-ttu-id="52946-114">Elektronik fatura gönderme senaryolarını destekleyen olayları yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="52946-114">Configure the events that support the electronic invoice submission scenarios.</span></span>
4. <span data-ttu-id="52946-115">E-faturalama özelliğini yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="52946-115">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="52946-116">"E-faturala özelliği", Elektronik faturalama eklenti sunucusunu kullanmak üzere yapılandırılmış ve yayımlanmış olan kaynağın genel adıdır.</span><span class="sxs-lookup"><span data-stu-id="52946-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="52946-117">Bu durumda müşteri elektronik faturalarının dışa aktarılması kuracağınız E-faturalama özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="52946-117">In this case, the export of customer electronic invoices is the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="52946-118">E-faturalama özelliğini içe aktarma</span><span class="sxs-lookup"><span data-stu-id="52946-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="52946-119">RCS hesabınızda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="52946-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="52946-120">**Genelleştirme özellikleri** çalışma alanında **Özellikler** bölmesinde **E-faturalama** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="52946-121">**E-faturalama Özellikleri** sayfasında, Genel depodan E-faturalama özelliğini içe aktarmak için **İçe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-121">On the **e-Invoicing Features** page, select **Import** to import the e-Invoicing feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="52946-122">Kullanılabilir özelliklerin listesini göremiyorsanız, **Eşitle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-122">If you don't see the list of available features, select **Synchronize**.</span></span> 

4. <span data-ttu-id="52946-123">**E-faturaları dışa aktar (IT)** özelliğini seçin ve **içe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-123">Select the **e-Invoices Export (IT)** feature, and then select **Import**.</span></span>

![E-faturalar dışa aktarma (IT) özelliğini içe aktarma](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

<span data-ttu-id="52946-125">**E-faturalar dışa aktarma (IT)** özelliğini Genel depodan içe aktardığınızda, sonraki bölümlerde açıklanan tüm ayarlar da alınır.</span><span class="sxs-lookup"><span data-stu-id="52946-125">When you import the **e-Invoices Export (IT)** feature from the Global repository, all the settings that are described in the next sections are also imported.</span></span>

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a><span data-ttu-id="52946-126">E-faturaları dışa aktar (IT) özelliğinin yeni bir sürümünü oluşturma</span><span class="sxs-lookup"><span data-stu-id="52946-126">Create a new version of the e-Invoices Export (IT) feature</span></span>

1. <span data-ttu-id="52946-127">**E-faturalama özellikleri** sayfasında, **Sürümler** sekmesinde, **Yeni** ögesini seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-127">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span> 

    ![Yeni e-faturalama özellik sürümü ekleme](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    <span data-ttu-id="52946-129">Sonra, e-faturalama özelliğiyle ilişkilendirilmiş Elektronik raporlama (ER) biçimlerini yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52946-129">Next, you will configure the Electronic reporting (ER) formats that are associated with the e-Invoicing feature.</span></span>

2. <span data-ttu-id="52946-130">**Yapılandırmalar** sekmesinde, yapılandırma sürümlerini yönetmek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-130">On the **Configurations** tab, select **Add** to manage the configuration versions.</span></span>

    ![E-faturalama özellik yapılandırma sürümlerini yönetme](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    <span data-ttu-id="52946-132">Bu adımda, İtalya için e-faturaları dışa aktarmak için kullanılan farklı dosyaların ER biçimlerini ekler ve yapılandırırsınız.</span><span class="sxs-lookup"><span data-stu-id="52946-132">In this step, you're adding and configuring the ER formats of different files that are used to export Italian e-invoices.</span></span> <span data-ttu-id="52946-133">İtalyan FatturaPA e-faturalar için, aşağıdaki standart yapılandırmaları veya e-faturalama için kullandığınız gerçek özelleştirilmiş yapılandırmaları kullanın:</span><span class="sxs-lookup"><span data-stu-id="52946-133">For Italian FatturaPA e-invoices, use either the following standard configurations or the actual customized configurations that you use for e-invoicing:</span></span>

    - <span data-ttu-id="52946-134">Satış faturası (IT)</span><span class="sxs-lookup"><span data-stu-id="52946-134">Sales invoice (IT)</span></span>
    - <span data-ttu-id="52946-135">Proje faturası (IT)</span><span class="sxs-lookup"><span data-stu-id="52946-135">Project invoice (IT)</span></span>

    <span data-ttu-id="52946-136">Başka bir E-faturalama özelliğinden türetilen bir E-faturalama özelliği oluşturduğunuzda, tüm ER biçimleri orijinal özellikten devralınır.</span><span class="sxs-lookup"><span data-stu-id="52946-136">When you create an e-Invoicing feature that is derived from another e-Invoicing feature, all ER formats are inherited from the original feature.</span></span>

3. <span data-ttu-id="52946-137">Belirli bir ER biçimi dosya yapılandırması seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-137">Select a specific ER format file configuration.</span></span>
4. <span data-ttu-id="52946-138">**Biçim tasarımcısı** sayfasını açmak için **Düzenle** veya **Görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-138">Select **Edit** or **View** to open the **Format designer** page.</span></span>

    ![Biçim tasarımcısı sayfasını açma](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. <span data-ttu-id="52946-140">**Biçim tasarımcısı** sayfasını, ER biçimi dosya yapılandırmalarını düzenlemek ve görüntülemek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="52946-140">Use the **Format designer** page to edit and view the ER format file configurations.</span></span>

    ![Biçim tasarımcısı sayfası](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="52946-142">E-faturalama özellik kurulumlarını yönetme</span><span class="sxs-lookup"><span data-stu-id="52946-142">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="52946-143">**E-faturalama özellikleri** sayfasında, **Kurulumlar** sekmesinde, E-faturalama özellik kurulumlarını yönetmek için **Ekle**, **Sil** veya **Düzenle** ögesini seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-143">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![E-faturalama özellik kurulumlarını yönetme](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="52946-145">Bu adımda, XML çıkış dosyalarının **FatturaPA** biçiminde oluşturulması ve dijital imzalanması (gerekirse) dahil olmak üzere elektronik faturalara uygulanabilir olayları yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52946-145">In this step, you configure the events that are applicable to electronic invoices, including generation of the XML output files in **FatturaPA** format and digital signing (if required).</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="52946-146">Satış faturası özellik kurulumunu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="52946-146">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="52946-147">**E-faturalama özellikleri** sayfasında, **Kurulumlar** sekmesinde, **Özellik kurulumu** sütununda **Satış faturası**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-147">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="52946-148">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-148">Select **Edit**.</span></span>
3. <span data-ttu-id="52946-149">**Özellik sürümü kurulumu** sayfasında, eylemler listesini yönetmek için **Eylemler** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-149">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="52946-150">Eylemler, olayın tam olarak yürütülmesi için sırayla çalıştırılması gereken işlemlerin listesini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="52946-150">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![Eylemler sekmesi](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | <span data-ttu-id="52946-152">Eylem kodu</span><span class="sxs-lookup"><span data-stu-id="52946-152">Action ID</span></span> | <span data-ttu-id="52946-153">Eylem adı</span><span class="sxs-lookup"><span data-stu-id="52946-153">Action name</span></span>        | <span data-ttu-id="52946-154">Eylem açıklaması</span><span class="sxs-lookup"><span data-stu-id="52946-154">Action description</span></span>                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | <span data-ttu-id="52946-155">1</span><span class="sxs-lookup"><span data-stu-id="52946-155">1</span></span>         | <span data-ttu-id="52946-156">Belgeyi dönüştür</span><span class="sxs-lookup"><span data-stu-id="52946-156">Transform document</span></span> | <span data-ttu-id="52946-157">E-fatura XML dosyasını **FatturaPA** biçiminde oluşturun.</span><span class="sxs-lookup"><span data-stu-id="52946-157">Create the e-invoice XML file in **FatturaPA** format.</span></span> |
    | <span data-ttu-id="52946-158">2</span><span class="sxs-lookup"><span data-stu-id="52946-158">2</span></span>         | <span data-ttu-id="52946-159">Belgeyi imzala</span><span class="sxs-lookup"><span data-stu-id="52946-159">Sign document</span></span>      | <span data-ttu-id="52946-160">XML dosyasına dijital imza uygulayın.</span><span class="sxs-lookup"><span data-stu-id="52946-160">Apply a digital signature to the XML file.</span></span>             |

4. <span data-ttu-id="52946-161">Uygulanabilirlik kurallarını görüntülemek ve sürdürmek için **Uygulanabilirlik kuralları** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-161">Select the **Applicability rules** tab to view and maintain the applicability rules.</span></span> <span data-ttu-id="52946-162">Uygulanabilirlik kuralları, eylemin çalışacağı bağlamı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="52946-162">Applicability rules define the context where the action will be run.</span></span>

    ![Uygulanabilirlik kuralları sekmesi](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. <span data-ttu-id="52946-164">Değişkenleri görüntülemek ve sürdürmek için **Değişkenler** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-164">Select the **Variables** tab to view and maintain the variables.</span></span>

    ![Değişkenler sekmesi](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. <span data-ttu-id="52946-166">Eylemleri çalıştırmak için gerekli olan ortak değişkenleri tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="52946-166">Define the public variables that are required to run the actions.</span></span>

### <a name="configure-the-project-invoice-feature-setup"></a><span data-ttu-id="52946-167">Proje faturası özellik kurulumunu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="52946-167">Configure the Project invoice feature setup</span></span> 

<span data-ttu-id="52946-168">**Proje faturası** özelliği kurulumunu yapılandırmak için gerekli adımlar ve ayarlar, **Satış faturası** özelliği kurulumuyla ilgili adımlara ve ayarlara benzer.</span><span class="sxs-lookup"><span data-stu-id="52946-168">The steps and settings that are required to configure the **Project invoice** feature setup are very similar to the steps and settings for the **Sales invoice** feature setup.</span></span> <span data-ttu-id="52946-169">Proje faturalarıyla çalışırken satış faturalarına ilişkin yordamlara bakın.</span><span class="sxs-lookup"><span data-stu-id="52946-169">When you work with project invoices, see the procedures for sales invoices.</span></span>

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a><span data-ttu-id="52946-170">E-faturalama özelliğini ortama atama</span><span class="sxs-lookup"><span data-stu-id="52946-170">Assign the e-Invoicing feature to the environment</span></span>

1. <span data-ttu-id="52946-171">**E-faturalama özellikleri** sayfasında, **Ortamlar** sekmesinde, **Etkinleştir** ögesini seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-171">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="52946-172">**Ortamlar** alanında, ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-172">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="52946-173">**Geçerlilik başlangıcı** alanında, yeni ortamın geçerli olacağı tarihi seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-173">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="52946-174">**Etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-174">Select **Enable**.</span></span> 

![E-faturalama ortamını etkinleştirme](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="52946-176">E-faturalama özelliğini yayımlama</span><span class="sxs-lookup"><span data-stu-id="52946-176">Publish the e-invoicing feature</span></span>

<span data-ttu-id="52946-177">Sürüm durumunu **Tamamlandı** veya **Yayımlandı** olarak değiştirerek e-faturalama özelliğini yayımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52946-177">You can publish the e-Invoicing feature by changing the version status to **Completed** or **Published**.</span></span>

### <a name="change-the-version-status-to-completed"></a><span data-ttu-id="52946-178">Sürüm durumunu Tamamlandı olarak değiştirme</span><span class="sxs-lookup"><span data-stu-id="52946-178">Change the version status to Completed</span></span>

1. <span data-ttu-id="52946-179">**E-faturalama Özellikleri** sayfasındaki **Sürümler** sekmesinde, **Taslak** durumundaki e-faturalama özelliğinin sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-179">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="52946-180">**Durumu değiştir \> Tamamla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-180">Select **Change status \> Complete**.</span></span> 

### <a name="change-the-version-status-to-published"></a><span data-ttu-id="52946-181">Sürüm durumunu Yayımlandı olarak değiştirme</span><span class="sxs-lookup"><span data-stu-id="52946-181">Change the version status to Published</span></span> 

1. <span data-ttu-id="52946-182">**E-faturalama Özellikleri** sayfasındaki **Sürümler** sekmesinde, **Tamamlandı** durumundaki e-faturalama özelliğinin sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-182">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="52946-183">**Durumu değiştir \> Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-183">Select **Change status \> Publish**.</span></span>

![E-faturalama özelliğinin durumunu değiştirme](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance"></a><span data-ttu-id="52946-185">Finance'de Elektronik faturalama eklentisi tümleştirmesi kurulumu</span><span class="sxs-lookup"><span data-stu-id="52946-185">Set up the Electronic invoicing add-on integration in Finance</span></span>

<span data-ttu-id="52946-186">Finance kurulumu sırasında şu görevleri tamamlayacaksınız:</span><span class="sxs-lookup"><span data-stu-id="52946-186">During the setup of Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="52946-187">ER veri modelini, ER veri modeli eşleştirmesini ve FatturaPA e-faturaları için bağlam yapılandırmalarını içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="52946-187">Import the ER data model, the ER data model mapping, and the context configurations for FatturaPA e-invoices.</span></span>
2. <span data-ttu-id="52946-188">İtalya e-faturalarını dijital olarak imzalamak için gerekli sertifikayı yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="52946-188">Configure the certificate that is required to digitally sign Italian e-invoices.</span></span>

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a><span data-ttu-id="52946-189">ER veri modelini, veri modeli eşlemesini ve biçimlerini içe aktarma</span><span class="sxs-lookup"><span data-stu-id="52946-189">Import the ER data model, data model mapping, and formats</span></span>

1. <span data-ttu-id="52946-190">**Elektronik raporlama** çalışma alanında, **İş Belge Servisi** yapılandırma sağlayıcısının **Etkin** olarak ayarlandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="52946-190">In the **Electronic reporting** workspace, verify that the **Business Document Service** configuration provider is set to **Active**.</span></span>
2. <span data-ttu-id="52946-191">**Depolar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-191">Select **Repositories**.</span></span>
3. <span data-ttu-id="52946-192">**Genel kaynak \> Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-192">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="52946-193">**Fatura modeli**, **Fatura modeli eşlemesi** ve **Müşteri faturası bağlam modeli** ögelerini içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="52946-193">Import **Invoice model**, **Invoice model mapping**, and **Customer invoice context model**.</span></span>

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a><span data-ttu-id="52946-194">İtalya için müşteri elektronik faturalarını dışa aktarma özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="52946-194">Turn on the feature for exporting customer electronic invoices for Italy</span></span>

1. <span data-ttu-id="52946-195">**Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="52946-195">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="52946-196">**Özellikler** sekmesinde, **IT00036** özellik referansları için satırlarda **Etkinleştirildi** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-196">On the **Features** tab, select the **Enabled** check box in the row for feature reference **IT00036**.</span></span>

![FatturaPA özelliğini etkinleştirme](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a><span data-ttu-id="52946-198">Elektronik belge yapılandırma</span><span class="sxs-lookup"><span data-stu-id="52946-198">Configure electronic documents</span></span>

1. <span data-ttu-id="52946-199">**Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="52946-199">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="52946-200">**Elektronik belge** sekmesinde, **Ekle**'yi seçin ve İtalya e-faturaları oluşturmak için gerekli tabloları girin:</span><span class="sxs-lookup"><span data-stu-id="52946-200">On the **Electronic document** tab, select **Add**, and enter the tables that are required to generate Italian e-invoices:</span></span>

    - <span data-ttu-id="52946-201">**Tablo adı:** Müşteri fatura günlüğü</span><span class="sxs-lookup"><span data-stu-id="52946-201">**Table name:** Customer invoice journal</span></span>
    - <span data-ttu-id="52946-202">**Tablo adı:** Proje faturası</span><span class="sxs-lookup"><span data-stu-id="52946-202">**Table name:** Project invoice</span></span>

3. <span data-ttu-id="52946-203">Her tablo için, ilgili belge bağlamını tanımlayın:</span><span class="sxs-lookup"><span data-stu-id="52946-203">For each table, define a related document context:</span></span>

    - <span data-ttu-id="52946-204">**Müşteri fatura günlüğü** için **Müşteri fatura bağlamı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-204">For **Customer invoice journal**, select **Customer invoice context**.</span></span>
    - <span data-ttu-id="52946-205">**Proje faturası** için **Proje fatura bağlamı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-205">For **Project invoice**, select **Project invoice context**.</span></span>

![Yanıt türlerini ayarlama](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a><span data-ttu-id="52946-207">Elektronik fatura işleme</span><span class="sxs-lookup"><span data-stu-id="52946-207">Electronic invoice processing</span></span>

<span data-ttu-id="52946-208">Finance'de işlem sırasında şu görevleri tamamlayacaksınız:</span><span class="sxs-lookup"><span data-stu-id="52946-208">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="52946-209">Elektronik faturalama eklentisi ile İtalya için e-faturaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="52946-209">Generate Italian e-invoices through the Electronic invoicing add-on</span></span>
2. <span data-ttu-id="52946-210">Yürütme günlüklerini görüntüleme ve işlemenin sonuçlarını gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="52946-210">View the execution logs and review the results of processing</span></span>

### <a name="generate-electronic-invoices"></a><span data-ttu-id="52946-211">Elektronik faturaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="52946-211">Generate electronic invoices</span></span>

<span data-ttu-id="52946-212">**Yapılandırılabilir Elektronik faturalama eklentisi tümleştirme** özelliğini açtıktan ve **IT00036** özelliğini etkinleştirdikten sonra, İtalya için e-faturaları oluşturmak için eski Finance işlemi artık kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="52946-212">After you turn on the **Configurable Electronic invoicing add-on integration** feature and activate the **IT00036** feature, the old Finance process for generating Italian e-invoices can no longer be used.</span></span> <span data-ttu-id="52946-213">**Elektronik belge gönderme** adı verilen yeni bir işlemle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="52946-213">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

<span data-ttu-id="52946-214">E-fatura belgelerinizin gerektirdiği gibi belgeleri el ile gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52946-214">You can submit the documents manually, based on your demand for e-invoice documents.</span></span>

> [!NOTE]
> <span data-ttu-id="52946-215">Devam etmeden önce, İtalya'ya ait e-faturalar için gerekli olan kurulumun tamamlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="52946-215">Before you continue, verify that the setup that is required for Italian e-invoices was completed.</span></span> <span data-ttu-id="52946-216">Daha fazla bilgi için bkz. [Müşteri elektronik faturaları](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices).</span><span class="sxs-lookup"><span data-stu-id="52946-216">For more information, see [Customer electronic invoices](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices).</span></span> <span data-ttu-id="52946-217">Elektronik faturalama eklentisi etkinleştirilmesi nedeniyle, bu konuda açıklanan bazı kurulum adımları kullanılamayabilir.</span><span class="sxs-lookup"><span data-stu-id="52946-217">Be aware that some of the setup steps that are described in that topic might be unavailable because of Electronic invoicing add-on activation.</span></span>

1. <span data-ttu-id="52946-218">**Kuruluş Yönetimi \> Dönemlik \> Elektronik belgeler \> Elektronik belgeleri gönder** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="52946-218">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="52946-219">Herhangi bir belgenin ilk gönderimi için, **Belgeyi yeniden gönder** seçeneğini **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="52946-219">For the first submission of any document, set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="52946-220">Belgeyi servis aracılığıyla yeniden göndermeniz gerekiyorsa, bu seçeneği **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="52946-220">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="52946-221">**Dahil edilecek kayıtlar** hızlı sekmesinde, gönderilecek belgeleri seçmek üzere bir sorgu oluşturabileceğiniz **Sorgulama** iletişim kutusunu açmak için **Filtre**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-221">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![Elektronik belgeleri gönder iletişim kutusu](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a><span data-ttu-id="52946-223">Filtre sorgusu</span><span class="sxs-lookup"><span data-stu-id="52946-223">Filter query</span></span>

1. <span data-ttu-id="52946-224">**Sorgulama** iletişim kutusunda, hem satış faturaları hem de proje faturaları için filtreleme koşullarını yapılandırın veya gönderilmeyen tüm faturaları dahil etmek için koşulları boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="52946-224">In the **Inquiry** dialog box, configure the filtering conditions for both sales invoices and project invoices, or leave the conditions blank to include all unsubmitted invoices.</span></span>

    ![Gönderme filtresi ölçütlerini ayarlama](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. <span data-ttu-id="52946-226">**Sorgulama** iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-226">Select **OK** to close the **Inquiry** dialog box.</span></span>
3. <span data-ttu-id="52946-227">Seçili belgeleri göndermek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-227">Select **OK** submit the selected documents.</span></span>

> <span data-ttu-id="52946-228">![NOT] Hizmet aracılığıyla ilk belge gönderme denemeniz sırasında, Elektronik faturalama eklentisi ile bağlantıyı onaylamanız istenecektir.</span><span class="sxs-lookup"><span data-stu-id="52946-228">![NOTE] During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="52946-229">**Elektronik Belge Gönderme Hizmetine bağlanmak için burayı tıklayın** ögesini seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-229">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

#### <a name="view-submission-logs"></a><span data-ttu-id="52946-230">Gönderme günlüklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="52946-230">View submission logs</span></span>

<span data-ttu-id="52946-231">Gönderilen tüm belgelerin gönderme günlüklerini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52946-231">You can view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="52946-232">**Kuruluş Yönetimi \> Dönemlik \> Elektronik belgeler \> Elektronik belgeleri gönderme günlüğü** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="52946-232">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="52946-233">**Belge türü** alanında, gerekli elektronik belgelerle ilgili olarak filtre uygulamak için **Müşteri fatura günlüğü** veya **Proje faturası** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="52946-233">In the **Document type** field, select **Customer invoice journal** or **Project invoice** to filter for the required electronic documents.</span></span>

    ![Gönderme günlüklerinin görüntülemek üzere bir belge türü seçme](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    <span data-ttu-id="52946-235">**Gönderim durumu** sütununda gösterilen değer, gönderme işleminin durumunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="52946-235">The value that is shown in the **Submission status** column represents the status of the submission process.</span></span> <span data-ttu-id="52946-236">İşlemin yapılandırılmış olarak çalışıp çalışmadığını ve başka bir eylemin gerekli olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="52946-236">It indicates whether the process ran as configured and whether additional action is required.</span></span>

3. <span data-ttu-id="52946-237">Eylem Bölmesi'nde, gönderme yürütme günlüklerinin ayrıntılarını görüntülemek için **Sorgulamalar \> Gönderme ayrıntıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="52946-237">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Gönderme günlüğü ayrıntılarını görüntüleme](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. <span data-ttu-id="52946-239">**İşleme eylemleri** hızlı sekmesinde, RCS'de ayarlanan özellik sürümünde yapılandırılan eylemler için yürütme günlüklerini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52946-239">On the **Processing actions** FastTab, you can view the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="52946-240">**Durum** sütunu eylemin başarıyla çalıştırılıp çalıştırılmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="52946-240">The **Status** column shows whether the action was successfully run.</span></span>
5. <span data-ttu-id="52946-241">**Eylem dosyaları** hızlı sekmesinde, eylemlerin yürütülmesi sırasında oluşturulan ara dosyaları görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52946-241">On the **Action files** FastTab, you can view the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="52946-242">Çıkış XML dosyasını **FatturaPA** biçiminde indirmek ve içeriğini görüntülemek için **Görünüm** öğesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52946-242">You can select **View** to download the output XML file in **FatturaPA** format and view its content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52946-243">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="52946-243">Related topics</span></span>

- [<span data-ttu-id="52946-244">Elektronik faturalama eklentisine genel bakış</span><span class="sxs-lookup"><span data-stu-id="52946-244">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="52946-245">Elektronik faturalama eklentisini kullanmaya başlangıç</span><span class="sxs-lookup"><span data-stu-id="52946-245">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="52946-246">Elektronik faturalamayı eklentisini kurma</span><span class="sxs-lookup"><span data-stu-id="52946-246">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)

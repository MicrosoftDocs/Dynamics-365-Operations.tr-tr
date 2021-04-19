---
title: Dynamics 365 Commerce değerlendirme ortamı için isteğe bağlı özellikleri yapılandırma
description: Bu konu, Microsoft Dynamics 365 Commerce değerlendirme ortamı için isteğe bağlı özelliklerin nasıl yapılandırılacağını açıklamaktadır.
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6bc968c2659380bb8c92292ee19e3a7ec8a20a2b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795919"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="e9ff4-103">Dynamics 365 Commerce değerlendirme ortamı için isteğe bağlı özellikleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="e9ff4-103">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e9ff4-104">Bu konu, Microsoft Dynamics 365 Commerce değerlendirme ortamı için isteğe bağlı özelliklerin nasıl yapılandırılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e9ff4-105">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="e9ff4-105">Prerequisites</span></span>

<span data-ttu-id="e9ff4-106">İşlem e-posta özelliklerini değerlendirmek istiyorsanız, aşağıdaki önkoşulların karşılanması gerekir:</span><span class="sxs-lookup"><span data-stu-id="e9ff4-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="e9ff4-107">Kullanılabilir bir e-posta sunucunuz var (Basit Posta Transfer Protokolü \[SMTP\] sunucusu); Bunlar, değerlendirme ortamını temin ettiğiniz Microsoft Azure aboneliğinden kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the evaluation environment.</span></span>
- <span data-ttu-id="e9ff4-108">Sunucunun tam etki alanı adına (FQDN)/IP adresi, SMTP bağlantı noktası numaranız ve kullanılabilir kimlik doğrulama detayları vardır.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="e9ff4-109">Görüntüyü arka arkaya konfigüre etme</span><span class="sxs-lookup"><span data-stu-id="e9ff4-109">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="e9ff4-110">Medya taban URL'nizi bulun</span><span class="sxs-lookup"><span data-stu-id="e9ff4-110">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="e9ff4-111">Bu yordamı tamamlayabilmek için, [sitenizi Commerce'ta ayarlama](cpe-post-provisioning.md#set-up-your-site-in-commerce) adımlarını tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-111">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="e9ff4-112">Sağlama sırasında e-Ticareti başlattığınız zamanı not ettiğiniz URL'yi kullanarak Commerce site oluşturucu aracında oturum açın (bkz. [e-Ticareti başlatma](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="e9ff4-112">Sign in to the Commerce site builder by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="e9ff4-113">**Fabrikam** sitesini açın.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-113">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="e9ff4-114">Soldaki menüden **Medya Kitaplığı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-114">On the menu on the left, select **Media Library**.</span></span>
1. <span data-ttu-id="e9ff4-115">Herhangi bir tek resim varlığı seçin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-115">Select any single image asset.</span></span>
1. <span data-ttu-id="e9ff4-116">Sağdaki Özellik denetçisinde, **genel URL** özelliğini bulun.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-116">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="e9ff4-117">Değer bir URL.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-117">The value is a URL.</span></span> <span data-ttu-id="e9ff4-118">Aşağıda bir örnek verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="e9ff4-118">Here is an example:</span></span>

    <span data-ttu-id="e9ff4-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="e9ff4-120">URL'deki son tanımlayıcıyı (önceki örnek URL'de **MA1nQC**) aşağıdaki dizeyle Değiştirin: **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-120">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="e9ff4-121">Örnek URL'nin bu değişiklik yapıldıktan sonra nasıl göründüğü aşağıda vardır:</span><span class="sxs-lookup"><span data-stu-id="e9ff4-121">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="e9ff4-122">Bu URL, ortam taban URL'sidir.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-122">This URL is your media base URL.</span></span> <span data-ttu-id="e9ff4-123">Not alın.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-123">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="e9ff4-124">Ortam temel URL'si güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="e9ff4-124">Update the media base URL</span></span>

1. <span data-ttu-id="e9ff4-125">Commerce Headquarters'da oturum açın.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-125">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="e9ff4-126">Soldaki menüyü kullanarak, **Modüller \> Perakende ve ticaret \>> Kanal ayarı \> Kanal profilleri** gidin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-126">Use the menu on the left to go to **Modules \> Retail and commerce \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="e9ff4-127">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-127">Select **Edit**.</span></span>
1. <span data-ttu-id="e9ff4-128">**Profil özelliklerinden**, **ortam sunucusu temel URL**'sinin özellik değerini daha önce oluşturduğunuz ortam taban URL'siyle değiştirin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-128">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="e9ff4-129">**scXXXXXXXXX** adlı kanalı seçin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-129">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="e9ff4-130">**Profil özellikleri** altında, **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-130">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="e9ff4-131">Eklenen özellik için, özellik anahtarı olarak **ortam sunucusu temel URL**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-131">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="e9ff4-132">Özellik değeri olarak, önceden oluşturduğunuz ortam taban URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-132">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="e9ff4-133">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-133">Select **Save**.</span></span>

## <a name="configure-and-test-the-email-server"></a><span data-ttu-id="e9ff4-134">E-posta sunucusunu yapılandırma ve test etme</span><span class="sxs-lookup"><span data-stu-id="e9ff4-134">Configure and test the email server</span></span>

> [!NOTE]
> <span data-ttu-id="e9ff4-135">Burada girdiğiniz SMTP sunucusu ya da e-posta hizmetinin, ortam için kullandığınız Azure aboneliği içinden erişilebilir olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-135">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="e9ff4-136">Commerce Headquarters'da oturum açın.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-136">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="e9ff4-137">Soldaki menüyü kullanarak, **Modüller \> Retail ve Commerce \> Headquarters kurulumu \> Parametreler \> E-posta parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-137">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Email parameters**.</span></span>
1. <span data-ttu-id="e9ff4-138">**SMTP** ayarları sekmesinde, **giden posta sunucusu** alanına SMTP sunucunuzun veya e-posta hizmetinizin FQDN'sini veya IP adresini girin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-138">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="e9ff4-139">**SMTP port numarası** alanına port numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-139">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="e9ff4-140">(Güvenli Yuvalar katmanı \[SSL\]'yi kullanmıyorsanız, varsayılan bağlantı noktası numarası **25**'tir.)</span><span class="sxs-lookup"><span data-stu-id="e9ff4-140">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="e9ff4-141">Kimlik doğrulama gerekliyse, değerleri **Kullanıcı adı** ve **parola** alanlarına girin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-141">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="e9ff4-142">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-142">Select **Save**.</span></span>
1. <span data-ttu-id="e9ff4-143">**Yenile**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-143">Select **Refresh**.</span></span>
1. <span data-ttu-id="e9ff4-144">**Test e-postası** sekmesinde, **e-posta sağlayıcısı** alanından **SMTP**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-144">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="e9ff4-145">**Gönder** alanına, test e-adresinin teslim edilmesini istediğiniz e-posta adresini girin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-145">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="e9ff4-146">**Test e-postası gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-146">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="e9ff4-147">E-posta şablonlarını yapılandır</span><span class="sxs-lookup"><span data-stu-id="e9ff4-147">Configure email templates</span></span>

<span data-ttu-id="e9ff4-148">E-postalarını göndermek istediğiniz her işlemsel olay için e-posta şablonunun geçerli bir gönderen e-posta adresiyle güncelleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-148">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="e9ff4-149">Commerce Headquarters'da oturum açın.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-149">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="e9ff4-150">Soldaki menüyü kullanarak, **Modüller \> Retail ve Commerce \> Headquarters kurulumu \> Parametreler \> Kuruluş e-posta şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-150">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="e9ff4-151">**Listeyi göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-151">Select **Show list**.</span></span>
1. <span data-ttu-id="e9ff4-152">Listedeki her şablon için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="e9ff4-152">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="e9ff4-153">**Gönderen e-postası** alanına Gönderen e-posta adresini girin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-153">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="e9ff4-154">İsteğe bağlı: **gönderen adı** alanına gönderen adı olarak kullanılacak adı girin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-154">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="e9ff4-155">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-155">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="e9ff4-156">E-posta şablonlarını özelleştirme</span><span class="sxs-lookup"><span data-stu-id="e9ff4-156">Customize email templates</span></span>

<span data-ttu-id="e9ff4-157">E-posta şablonlarını farklı görüntüler kullanacak şekilde özelleştirmek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-157">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="e9ff4-158">Veya şablonların bağlantılarını, değerlendirme ortamınıza gitmeleri için güncelleştirmek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-158">Or you might want to update the links in the templates so that they go to your evaluation environment.</span></span> <span data-ttu-id="e9ff4-159">Bu prosedür, varsayılan şablonların nasıl karşıdan yükleneceğini açıklar, bunları özelleştirin ve sistemdeki şablonları güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-159">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="e9ff4-160">Tarayıcı kullanarak, [Microsoft Dynamics 365 Commerce Değerlendirme varsayılan e-posta şablonları zip dosyasını](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) indirin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-160">In a web browser, download the [Microsoft Dynamics 365 Commerce Evaluation default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="e9ff4-161">Bu dosya aşağıdaki HTML belgelerini içerir:</span><span class="sxs-lookup"><span data-stu-id="e9ff4-161">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="e9ff4-162">Sipariş onayı şablonu</span><span class="sxs-lookup"><span data-stu-id="e9ff4-162">Order confirmation template</span></span>
    - <span data-ttu-id="e9ff4-163">Hediye kartı şablonu</span><span class="sxs-lookup"><span data-stu-id="e9ff4-163">Issue gift card template</span></span>
    - <span data-ttu-id="e9ff4-164">Yeni sipariş şablonu</span><span class="sxs-lookup"><span data-stu-id="e9ff4-164">New order template</span></span>
    - <span data-ttu-id="e9ff4-165">Paket sipariş şablonu</span><span class="sxs-lookup"><span data-stu-id="e9ff4-165">Pack order template</span></span>
    - <span data-ttu-id="e9ff4-166">Sipariş şablonu al</span><span class="sxs-lookup"><span data-stu-id="e9ff4-166">Pick order template</span></span>

1. <span data-ttu-id="e9ff4-167">Metin veya HTML Düzenleyicisi kullanarak şablonları özelleştirin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-167">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="e9ff4-168">[Desteklenen belirteçler](#supported-tokens-in-the-email-template) listesine bu konunun ilerisinde bakın.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-168">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="e9ff4-169">Commerce'de oturum açın.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-169">Sign in to Commerce.</span></span>
1. <span data-ttu-id="e9ff4-170">Soldaki menüyü kullanarak, **Modüller \> Kuruluş yönetimi \> Kurulum \>> Kuruluş e-posta şablonları** gidin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-170">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="e9ff4-171">Tüm şablonları görmek için soldaki listeyi genişletin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-171">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="e9ff4-172">Özelleştirmek istediğiniz her şablon için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="e9ff4-172">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="e9ff4-173">Listeden şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-173">Select the template in the list.</span></span>
    1. <span data-ttu-id="e9ff4-174">**E -posta iletisi içeriği** altında, listeden uygun dil sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-174">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="e9ff4-175">(Varsayılan dil değeri **tr-tr**'dir.)</span><span class="sxs-lookup"><span data-stu-id="e9ff4-175">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="e9ff4-176">**E-posta iletisi içeriği** altında **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-176">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="e9ff4-177">**E-posta şablonu karşıya yükle** bölmesi görünür.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-177">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="e9ff4-178">**Gözat**'ı seçin ve özelleştirilmiş içeriğe sahip olan HTML dosyasını bulun.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-178">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="e9ff4-179">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-179">Select **Upload**.</span></span> <span data-ttu-id="e9ff4-180">Şablonunuz sisteme yüklenir ve bir önizleme gösterilir.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-180">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="e9ff4-181">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-181">Select **OK**.</span></span>
    1. <span data-ttu-id="e9ff4-182">İsteğe bağlı: Şablonun **konu** özelliğini özelleştirin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-182">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="e9ff4-183">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-183">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="e9ff4-184">E-posta şablonunda desteklenen belirteçler</span><span class="sxs-lookup"><span data-stu-id="e9ff4-184">Supported tokens in the email template</span></span>

<span data-ttu-id="e9ff4-185">E-posta oluşturulduğunda, bu belirteçler, müşteriye uygulanan gerçek değerlerle e-posta işleme zamanında değiştirilecek.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-185">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="e9ff4-186">Satış siparişi</span><span class="sxs-lookup"><span data-stu-id="e9ff4-186">Sales order</span></span>

<span data-ttu-id="e9ff4-187">Aşağıdaki belirteçler genel satış siparişi için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-187">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="e9ff4-188">Belirtecin adı</span><span class="sxs-lookup"><span data-stu-id="e9ff4-188">Name of the token</span></span> | <span data-ttu-id="e9ff4-189">Belirteç</span><span class="sxs-lookup"><span data-stu-id="e9ff4-189">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="e9ff4-190">Sipariş numarası</span><span class="sxs-lookup"><span data-stu-id="e9ff4-190">Order number</span></span>      | <span data-ttu-id="e9ff4-191">%salesid%</span><span class="sxs-lookup"><span data-stu-id="e9ff4-191">%salesid%</span></span> |
| <span data-ttu-id="e9ff4-192">Müşteri adı</span><span class="sxs-lookup"><span data-stu-id="e9ff4-192">Customer's name</span></span>   | <span data-ttu-id="e9ff4-193">%customername%</span><span class="sxs-lookup"><span data-stu-id="e9ff4-193">%customername%</span></span> |
| <span data-ttu-id="e9ff4-194">Teslimat adresi</span><span class="sxs-lookup"><span data-stu-id="e9ff4-194">Delivery address</span></span>  | <span data-ttu-id="e9ff4-195">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="e9ff4-195">%deliveryaddress%</span></span> |
| <span data-ttu-id="e9ff4-196">Fatura adresi</span><span class="sxs-lookup"><span data-stu-id="e9ff4-196">Billing address</span></span>   | <span data-ttu-id="e9ff4-197">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="e9ff4-197">%customeraddress%</span></span> |
| <span data-ttu-id="e9ff4-198">Sipariş tarihi</span><span class="sxs-lookup"><span data-stu-id="e9ff4-198">Order date</span></span>        | <span data-ttu-id="e9ff4-199">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="e9ff4-199">%shipdate%</span></span> |
| <span data-ttu-id="e9ff4-200">Teslimat şekli</span><span class="sxs-lookup"><span data-stu-id="e9ff4-200">Delivery mode</span></span>     | <span data-ttu-id="e9ff4-201">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="e9ff4-201">%modeofdelivery%</span></span> |
| <span data-ttu-id="e9ff4-202">İskonto</span><span class="sxs-lookup"><span data-stu-id="e9ff4-202">Discount</span></span>          | <span data-ttu-id="e9ff4-203">%discount%</span><span class="sxs-lookup"><span data-stu-id="e9ff4-203">%discount%</span></span> |
| <span data-ttu-id="e9ff4-204">Satış vergisi</span><span class="sxs-lookup"><span data-stu-id="e9ff4-204">Sales tax</span></span>         | <span data-ttu-id="e9ff4-205">%tax%</span><span class="sxs-lookup"><span data-stu-id="e9ff4-205">%tax%</span></span> |
| <span data-ttu-id="e9ff4-206">Sipariş toplamı</span><span class="sxs-lookup"><span data-stu-id="e9ff4-206">Order total</span></span>       | <span data-ttu-id="e9ff4-207">%total%</span><span class="sxs-lookup"><span data-stu-id="e9ff4-207">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="e9ff4-208">Satış satırı</span><span class="sxs-lookup"><span data-stu-id="e9ff4-208">Sales line</span></span>

<span data-ttu-id="e9ff4-209">Aşağıdaki belirteçler siparişteki her ürün için değerlerle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-209">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="e9ff4-210">**Ürün listesi - Başlangıç** belirtecini her ürün için tekrarlanan HTML bloğunun başına yerleştirin ve bloğun sonuna **ürün listesi - uç** belirtecini koyun.</span><span class="sxs-lookup"><span data-stu-id="e9ff4-210">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="e9ff4-211">Belirtecin adı</span><span class="sxs-lookup"><span data-stu-id="e9ff4-211">Name of the token</span></span>      | <span data-ttu-id="e9ff4-212">Belirteç</span><span class="sxs-lookup"><span data-stu-id="e9ff4-212">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="e9ff4-213">Ürün listesi - başlangıç</span><span class="sxs-lookup"><span data-stu-id="e9ff4-213">Product list - start</span></span>   | \<!--%tablebegin.salesline% --\> |
| <span data-ttu-id="e9ff4-214">Ürün listesi - bitiş</span><span class="sxs-lookup"><span data-stu-id="e9ff4-214">Product list - end</span></span>     | \<!--%tableend.salesline%--\> |
| <span data-ttu-id="e9ff4-215">Ürün adı</span><span class="sxs-lookup"><span data-stu-id="e9ff4-215">Product name</span></span>           | <span data-ttu-id="e9ff4-216">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="e9ff4-216">%lineproductname%</span></span> |
| <span data-ttu-id="e9ff4-217">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9ff4-217">Description</span></span>            | <span data-ttu-id="e9ff4-218">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="e9ff4-218">%lineproductdescription%</span></span> |
| <span data-ttu-id="e9ff4-219">Miktar</span><span class="sxs-lookup"><span data-stu-id="e9ff4-219">Quantity</span></span>               | <span data-ttu-id="e9ff4-220">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="e9ff4-220">%linequantity%</span></span> |
| <span data-ttu-id="e9ff4-221">Satır birim fiyatı</span><span class="sxs-lookup"><span data-stu-id="e9ff4-221">Line unit price</span></span>        | <span data-ttu-id="e9ff4-222">%lineprice% (doğrula)</span><span class="sxs-lookup"><span data-stu-id="e9ff4-222">%lineprice% (verify)</span></span> |
| <span data-ttu-id="e9ff4-223">satır maddesi toplamı</span><span class="sxs-lookup"><span data-stu-id="e9ff4-223">line item total</span></span>        | <span data-ttu-id="e9ff4-224">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="e9ff4-224">%linenetamount%</span></span> |
| <span data-ttu-id="e9ff4-225">satır iskontosu</span><span class="sxs-lookup"><span data-stu-id="e9ff4-225">line discount</span></span>          | <span data-ttu-id="e9ff4-226">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="e9ff4-226">%linediscount%</span></span> |
| <span data-ttu-id="e9ff4-227">Sevk tarihi</span><span class="sxs-lookup"><span data-stu-id="e9ff4-227">Ship date</span></span>              | <span data-ttu-id="e9ff4-228">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="e9ff4-228">%lineshipdate%</span></span> |
| <span data-ttu-id="e9ff4-229">Tedarik yöntemi</span><span class="sxs-lookup"><span data-stu-id="e9ff4-229">Procurement method</span></span>     | <span data-ttu-id="e9ff4-230">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="e9ff4-230">%linedeliverymode%</span></span> |
| <span data-ttu-id="e9ff4-231">teslimat adresi</span><span class="sxs-lookup"><span data-stu-id="e9ff4-231">delivery address</span></span>       | <span data-ttu-id="e9ff4-232">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="e9ff4-232">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="e9ff4-233">Satırın satış birimi</span><span class="sxs-lookup"><span data-stu-id="e9ff4-233">Sales unit of the line</span></span> | <span data-ttu-id="e9ff4-234">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="e9ff4-234">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="e9ff4-235">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e9ff4-235">Additional resources</span></span>

[<span data-ttu-id="e9ff4-236">Dynamics 365 Commerce değerlendirme ortamına genel bakış</span><span class="sxs-lookup"><span data-stu-id="e9ff4-236">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="e9ff4-237">Dynamics 365 Commerce değerlendirme ortamı sağlama</span><span class="sxs-lookup"><span data-stu-id="e9ff4-237">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="e9ff4-238">Dynamics 365 Commerce değerlendirme ortamı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="e9ff4-238">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="e9ff4-239">Dynamics 365 Commerce değerlendirme ortamında BOPIS yapılandırma</span><span class="sxs-lookup"><span data-stu-id="e9ff4-239">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="e9ff4-240">Dynamics 365 Commerce değerlendirme ortamıyla ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="e9ff4-240">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="e9ff4-241">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="e9ff4-241">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="e9ff4-242">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="e9ff4-242">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="e9ff4-243">Microsoft Azure portalı</span><span class="sxs-lookup"><span data-stu-id="e9ff4-243">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="e9ff4-244">Dynamics 365 Commerce web sitesi</span><span class="sxs-lookup"><span data-stu-id="e9ff4-244">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
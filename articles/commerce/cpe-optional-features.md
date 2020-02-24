---
title: Dynamics 365 Commerce önizleme ortamı için isteğe bağlı özellikleri yapılandırma
description: Bu konu, Microsoft Dynamics 365 Commerce önizleme ortamı için isteğe bağlı özelliklerin nasıl yapılandırılacağını açıklamaktadır.
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 43b23b9ef881b2ab2f3d005d4ba761848a7fa4ed
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024741"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="78231-103">Dynamics 365 Commerce önizleme ortamı için isteğe bağlı özellikleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="78231-103">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="78231-104">Bu konu, Microsoft Dynamics 365 Commerce önizleme ortamı için isteğe bağlı özelliklerin nasıl yapılandırılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="78231-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="78231-105">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="78231-105">Prerequisites</span></span>

<span data-ttu-id="78231-106">İşlem e-posta özelliklerini değerlendirmek istiyorsanız, aşağıdaki önkoşulların karşılanması gerekir:</span><span class="sxs-lookup"><span data-stu-id="78231-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="78231-107">Kullanılabilir bir e-posta sunucunuz var (Basit Posta Transfer Protokolü \[SMTP\] sunucusu); Bunlar, önizleme ortamını temin ettiğiniz Microsoft Azure aboneliğinden kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="78231-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the preview environment.</span></span>
- <span data-ttu-id="78231-108">Sunucunun tam etki alanı adına (FQDN)/IP adresi, SMTP bağlantı noktası numaranız ve kullanılabilir kimlik doğrulama detayları vardır.</span><span class="sxs-lookup"><span data-stu-id="78231-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

<span data-ttu-id="78231-109">Yeni çok yönlü kanal görüntülerini alarak dijital varlık yönetimi özelliklerini değerlendirmek istiyorsanız, içerik yönetimi sistemi (CMS) kiracısının adının kullanılabilir olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="78231-109">If you want to evaluate Digital Asset Management features by ingesting new omni-channel images, you must have the name of your content management system (CMS) tenant available.</span></span> <span data-ttu-id="78231-110">Bu adı bulma yönergeleri daha sonra bu konunun içinde sağlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="78231-110">Instructions for finding this name are provided later in this topic.</span></span> <span data-ttu-id="78231-111">>>>(S: talimatlar nerede?)</span><span class="sxs-lookup"><span data-stu-id="78231-111">>>>(Q: where are the instructions?)</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="78231-112">Görüntüyü arka arkaya konfigüre etme</span><span class="sxs-lookup"><span data-stu-id="78231-112">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="78231-113">Medya taban URL'nizi bulun</span><span class="sxs-lookup"><span data-stu-id="78231-113">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="78231-114">Bu yordamı tamamlayabilmek için, [sitenizi Commerce'ta ayarlama](cpe-post-provisioning.md#set-up-your-site-in-commerce) adımlarını tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="78231-114">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="78231-115">Sağlama sırasında e-ticareti başlattığınızda oluşan bir not oluşturduğunuz URL'yi kullanarak Commerce site yönetimi aracında oturum açın (bkz. [e-Ticareti başlat](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="78231-115">Sign in to the Commerce site management tool by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="78231-116">**Fabrikam** sitesini açın.</span><span class="sxs-lookup"><span data-stu-id="78231-116">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="78231-117">Soldaki menüden **Varlıkları** seçin.</span><span class="sxs-lookup"><span data-stu-id="78231-117">On the menu on the left, select **Assets**.</span></span>
1. <span data-ttu-id="78231-118">Herhangi bir tek resim varlığı seçin.</span><span class="sxs-lookup"><span data-stu-id="78231-118">Select any single image asset.</span></span>
1. <span data-ttu-id="78231-119">Sağdaki Özellik denetçisinde, **genel URL** özelliğini bulun.</span><span class="sxs-lookup"><span data-stu-id="78231-119">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="78231-120">Değer bir URL.</span><span class="sxs-lookup"><span data-stu-id="78231-120">The value is a URL.</span></span> <span data-ttu-id="78231-121">Aşağıda bir örnek verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="78231-121">Here is an example:</span></span>

    <span data-ttu-id="78231-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="78231-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="78231-123">URL'deki son tanımlayıcıyı (önceki örnek URL'de **MA1nQC**) aşağıdaki dizeyle Değiştirin: **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="78231-123">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="78231-124">Örnek URL'nin bu değişiklik yapıldıktan sonra nasıl göründüğü aşağıda vardır:</span><span class="sxs-lookup"><span data-stu-id="78231-124">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="78231-125">Bu URL, ortam taban URL'sidir.</span><span class="sxs-lookup"><span data-stu-id="78231-125">This URL is your media base URL.</span></span> <span data-ttu-id="78231-126">Not alın.</span><span class="sxs-lookup"><span data-stu-id="78231-126">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="78231-127">Ortam temel URL'si güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="78231-127">Update the media base URL</span></span>

1. <span data-ttu-id="78231-128">Dynamics 365 Retail'da oturum açın</span><span class="sxs-lookup"><span data-stu-id="78231-128">Sign in to Dynamics 365 Retail.</span></span>
1. <span data-ttu-id="78231-129">Soldaki menüyü kullanarak, **Modüller \> Perakende \>> Kanal ayarı \> Kanal profilleri** gidin.</span><span class="sxs-lookup"><span data-stu-id="78231-129">Use the menu on the left to go to **Modules \> Retail \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="78231-130">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="78231-130">Select **Edit**.</span></span>
1. <span data-ttu-id="78231-131">**Profil özelliklerinden**, **ortam sunucusu temel URL**'sinin özellik değerini daha önce oluşturduğunuz ortam taban URL'siyle değiştirin.</span><span class="sxs-lookup"><span data-stu-id="78231-131">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="78231-132">Soldaki listeden, **varsayılan** kanal altında diğer kanalı seçin.</span><span class="sxs-lookup"><span data-stu-id="78231-132">In the list on the left, under the **Default** channel, select the other channel.</span></span>
1. <span data-ttu-id="78231-133">**Profil özellikleri** altında, **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="78231-133">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="78231-134">Eklenen özellik için, özellik anahtarı olarak **ortam sunucusu temel URL**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="78231-134">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="78231-135">Özellik değeri olarak, önceden oluşturduğunuz ortam taban URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="78231-135">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="78231-136">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="78231-136">Select **Save**.</span></span>

## <a name="configure-the-email-server"></a><span data-ttu-id="78231-137">E-posta sunucusunu yapılandır</span><span class="sxs-lookup"><span data-stu-id="78231-137">Configure the email server</span></span>

> [!NOTE]
> <span data-ttu-id="78231-138">Burada girdiğiniz SMTP sunucusu ya da e-posta hizmetinin, ortam için kullandığınız Azure aboneliği içinden erişilebilir olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="78231-138">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="78231-139">Retail'da oturum açın.</span><span class="sxs-lookup"><span data-stu-id="78231-139">Sign in to Retail.</span></span>
1. <span data-ttu-id="78231-140">Soldaki menüyü kullanarak, **Modüller \> Sistem yönetimi \> Kurulum \> E-posta \> E-posta parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="78231-140">Use the menu on the left to go to **Modules \> System administration \> Setup \> Email \> Email parameters**.</span></span>
1. <span data-ttu-id="78231-141">**SMTP** ayarları sekmesinde, **giden posta sunucusu** alanına SMTP sunucunuzun veya e-posta hizmetinizin FQDN'sini veya IP adresini girin.</span><span class="sxs-lookup"><span data-stu-id="78231-141">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="78231-142">**SMTP port numarası** alanına port numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="78231-142">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="78231-143">(Güvenli Yuvalar katmanı \[SSL\]'yi kullanmıyorsanız, varsayılan bağlantı noktası numarası **25**'tir.)</span><span class="sxs-lookup"><span data-stu-id="78231-143">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="78231-144">Kimlik doğrulama gerekliyse, değerleri **Kullanıcı adı** ve **parola** alanlarına girin.</span><span class="sxs-lookup"><span data-stu-id="78231-144">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="78231-145">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="78231-145">Select **Save**.</span></span>
1. <span data-ttu-id="78231-146">**Yenile**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="78231-146">Select **Refresh**.</span></span>
1. <span data-ttu-id="78231-147">**Test e-postası** sekmesinde, **e-posta sağlayıcısı** alanından **SMTP**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="78231-147">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="78231-148">**Gönder** alanına, test e-adresinin teslim edilmesini istediğiniz e-posta adresini girin.</span><span class="sxs-lookup"><span data-stu-id="78231-148">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="78231-149">**Test e-postası gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="78231-149">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="78231-150">E-posta şablonlarını yapılandır</span><span class="sxs-lookup"><span data-stu-id="78231-150">Configure email templates</span></span>

<span data-ttu-id="78231-151">E-postalarını göndermek istediğiniz her işlemsel olay için e-posta şablonunun geçerli bir gönderen e-posta adresiyle güncelleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="78231-151">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="78231-152">Retail'da oturum açın.</span><span class="sxs-lookup"><span data-stu-id="78231-152">Sign in to Retail.</span></span>
1. <span data-ttu-id="78231-153">Soldaki menüyü kullanarak, **Modüller \> Kuruluş yönetimi \> Kurulum \>> Kuruluş e-posta şablonları** gidin.</span><span class="sxs-lookup"><span data-stu-id="78231-153">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="78231-154">**Listeyi göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="78231-154">Select **Show list**.</span></span>
1. <span data-ttu-id="78231-155">Listedeki her şablon için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="78231-155">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="78231-156">**Gönderen e-postası** alanına Gönderen e-posta adresini girin.</span><span class="sxs-lookup"><span data-stu-id="78231-156">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="78231-157">İsteğe bağlı: **gönderen adı** alanına gönderen adı olarak kullanılacak adı girin.</span><span class="sxs-lookup"><span data-stu-id="78231-157">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="78231-158">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="78231-158">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="78231-159">E-posta şablonlarını özelleştirme</span><span class="sxs-lookup"><span data-stu-id="78231-159">Customize email templates</span></span>

<span data-ttu-id="78231-160">E-posta şablonlarını farklı görüntüler kullanacak şekilde özelleştirmek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="78231-160">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="78231-161">Veya şablonların bağlantılarını, önizleme ortamınıza gitmeleri için güncelleştirmek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="78231-161">Or you might want to update the links in the templates so that they go to your preview environment.</span></span> <span data-ttu-id="78231-162">Bu prosedür, varsayılan şablonların nasıl karşıdan yükleneceğini açıklar, bunları özelleştirin ve sistemdeki şablonları güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="78231-162">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="78231-163">Tarayıcı kullanarak, [Microsoft Dynamics 365 Commerce Preview varsayılan e-posta şablonları. zip dosyasını](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) karşıdan yükleyin.</span><span class="sxs-lookup"><span data-stu-id="78231-163">In a web browser, download the [Microsoft Dynamics 365 Commerce Preview default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="78231-164">Bu dosya aşağıdaki HTML belgelerini içerir:</span><span class="sxs-lookup"><span data-stu-id="78231-164">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="78231-165">Sipariş onayı şablonu</span><span class="sxs-lookup"><span data-stu-id="78231-165">Order confirmation template</span></span>
    - <span data-ttu-id="78231-166">Hediye kartı şablonu</span><span class="sxs-lookup"><span data-stu-id="78231-166">Issue gift card template</span></span>
    - <span data-ttu-id="78231-167">Yeni sipariş şablonu</span><span class="sxs-lookup"><span data-stu-id="78231-167">New order template</span></span>
    - <span data-ttu-id="78231-168">Paket sipariş şablonu</span><span class="sxs-lookup"><span data-stu-id="78231-168">Pack order template</span></span>
    - <span data-ttu-id="78231-169">Sipariş şablonu al</span><span class="sxs-lookup"><span data-stu-id="78231-169">Pick order template</span></span>

1. <span data-ttu-id="78231-170">Metin veya HTML Düzenleyicisi kullanarak şablonları özelleştirin.</span><span class="sxs-lookup"><span data-stu-id="78231-170">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="78231-171">[Desteklenen belirteçler](#supported-tokens-in-the-email-template) listesine bu konunun ilerisinde bakın.</span><span class="sxs-lookup"><span data-stu-id="78231-171">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="78231-172">Retail'da oturum açın.</span><span class="sxs-lookup"><span data-stu-id="78231-172">Sign in to Retail.</span></span>
1. <span data-ttu-id="78231-173">Soldaki menüyü kullanarak, **Modüller \> Kuruluş yönetimi \> Kurulum \>> Kuruluş e-posta şablonları** gidin.</span><span class="sxs-lookup"><span data-stu-id="78231-173">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="78231-174">Tüm şablonları görmek için soldaki listeyi genişletin.</span><span class="sxs-lookup"><span data-stu-id="78231-174">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="78231-175">Özelleştirmek istediğiniz her şablon için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="78231-175">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="78231-176">Listeden şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="78231-176">Select the template in the list.</span></span>
    1. <span data-ttu-id="78231-177">**E -posta iletisi içeriği** altında, listeden uygun dil sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="78231-177">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="78231-178">(Varsayılan dil değeri **tr-tr**'dir.)</span><span class="sxs-lookup"><span data-stu-id="78231-178">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="78231-179">**E-posta iletisi içeriği** altında **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="78231-179">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="78231-180">**E-posta şablonu karşıya yükle** bölmesi görünür.</span><span class="sxs-lookup"><span data-stu-id="78231-180">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="78231-181">**Gözat**'ı seçin ve özelleştirilmiş içeriğe sahip olan HTML dosyasını bulun.</span><span class="sxs-lookup"><span data-stu-id="78231-181">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="78231-182">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="78231-182">Select **Upload**.</span></span> <span data-ttu-id="78231-183">Şablonunuz sisteme yüklenir ve bir önizleme gösterilir.</span><span class="sxs-lookup"><span data-stu-id="78231-183">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="78231-184">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="78231-184">Select **OK**.</span></span>
    1. <span data-ttu-id="78231-185">İsteğe bağlı: Şablonun **konu** özelliğini özelleştirin.</span><span class="sxs-lookup"><span data-stu-id="78231-185">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="78231-186">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="78231-186">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="78231-187">E-posta şablonunda desteklenen belirteçler</span><span class="sxs-lookup"><span data-stu-id="78231-187">Supported tokens in the email template</span></span>

<span data-ttu-id="78231-188">E-posta oluşturulduğunda, bu belirteçler, müşteriye uygulanan gerçek değerlerle e-posta işleme zamanında değiştirilecek.</span><span class="sxs-lookup"><span data-stu-id="78231-188">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="78231-189">Satış siparişi</span><span class="sxs-lookup"><span data-stu-id="78231-189">Sales order</span></span>

<span data-ttu-id="78231-190">Aşağıdaki belirteçler genel satış siparişi için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="78231-190">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="78231-191">Belirtecin adı</span><span class="sxs-lookup"><span data-stu-id="78231-191">Name of the token</span></span> | <span data-ttu-id="78231-192">Belirteç</span><span class="sxs-lookup"><span data-stu-id="78231-192">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="78231-193">Sipariş numarası</span><span class="sxs-lookup"><span data-stu-id="78231-193">Order number</span></span>      | <span data-ttu-id="78231-194">%salesid%</span><span class="sxs-lookup"><span data-stu-id="78231-194">%salesid%</span></span> |
| <span data-ttu-id="78231-195">Müşteri adı</span><span class="sxs-lookup"><span data-stu-id="78231-195">Customer's name</span></span>   | <span data-ttu-id="78231-196">%customername%</span><span class="sxs-lookup"><span data-stu-id="78231-196">%customername%</span></span> |
| <span data-ttu-id="78231-197">Teslimat adresi</span><span class="sxs-lookup"><span data-stu-id="78231-197">Delivery address</span></span>  | <span data-ttu-id="78231-198">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="78231-198">%deliveryaddress%</span></span> |
| <span data-ttu-id="78231-199">Fatura adresi</span><span class="sxs-lookup"><span data-stu-id="78231-199">Billing address</span></span>   | <span data-ttu-id="78231-200">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="78231-200">%customeraddress%</span></span> |
| <span data-ttu-id="78231-201">Sipariş tarihi</span><span class="sxs-lookup"><span data-stu-id="78231-201">Order date</span></span>        | <span data-ttu-id="78231-202">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="78231-202">%shipdate%</span></span> |
| <span data-ttu-id="78231-203">Teslimat şekli</span><span class="sxs-lookup"><span data-stu-id="78231-203">Delivery mode</span></span>     | <span data-ttu-id="78231-204">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="78231-204">%modeofdelivery%</span></span> |
| <span data-ttu-id="78231-205">İskonto</span><span class="sxs-lookup"><span data-stu-id="78231-205">Discount</span></span>          | <span data-ttu-id="78231-206">%discount%</span><span class="sxs-lookup"><span data-stu-id="78231-206">%discount%</span></span> |
| <span data-ttu-id="78231-207">Satış vergisi</span><span class="sxs-lookup"><span data-stu-id="78231-207">Sales tax</span></span>         | <span data-ttu-id="78231-208">%tax%</span><span class="sxs-lookup"><span data-stu-id="78231-208">%tax%</span></span> |
| <span data-ttu-id="78231-209">Sipariş toplamı</span><span class="sxs-lookup"><span data-stu-id="78231-209">Order total</span></span>       | <span data-ttu-id="78231-210">%total%</span><span class="sxs-lookup"><span data-stu-id="78231-210">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="78231-211">Satış satırı</span><span class="sxs-lookup"><span data-stu-id="78231-211">Sales line</span></span>

<span data-ttu-id="78231-212">Aşağıdaki belirteçler siparişteki her ürün için değerlerle değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="78231-212">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="78231-213">**Ürün listesi - Başlangıç** belirtecini her ürün için tekrarlanan HTML bloğunun başına yerleştirin ve bloğun sonuna **ürün listesi - uç** belirtecini koyun.</span><span class="sxs-lookup"><span data-stu-id="78231-213">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="78231-214">Belirtecin adı</span><span class="sxs-lookup"><span data-stu-id="78231-214">Name of the token</span></span>      | <span data-ttu-id="78231-215">Belirteç</span><span class="sxs-lookup"><span data-stu-id="78231-215">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="78231-216">Ürün listesi - başlangıç</span><span class="sxs-lookup"><span data-stu-id="78231-216">Product list - start</span></span>   | <span data-ttu-id="78231-217">\<!--%tablebegin.salesline% --\></span><span class="sxs-lookup"><span data-stu-id="78231-217">\<!--%tablebegin.salesline% --\></span></span> |
| <span data-ttu-id="78231-218">Ürün listesi - bitiş</span><span class="sxs-lookup"><span data-stu-id="78231-218">Product list - end</span></span>     | <span data-ttu-id="78231-219">\<!--%tableend.salesline%--\></span><span class="sxs-lookup"><span data-stu-id="78231-219">\<!--%tableend.salesline%--\></span></span> |
| <span data-ttu-id="78231-220">Ürün adı</span><span class="sxs-lookup"><span data-stu-id="78231-220">Product name</span></span>           | <span data-ttu-id="78231-221">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="78231-221">%lineproductname%</span></span> |
| <span data-ttu-id="78231-222">Tanım</span><span class="sxs-lookup"><span data-stu-id="78231-222">Description</span></span>            | <span data-ttu-id="78231-223">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="78231-223">%lineproductdescription%</span></span> |
| <span data-ttu-id="78231-224">Miktar</span><span class="sxs-lookup"><span data-stu-id="78231-224">Quantity</span></span>               | <span data-ttu-id="78231-225">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="78231-225">%linequantity%</span></span> |
| <span data-ttu-id="78231-226">Satır birim fiyatı</span><span class="sxs-lookup"><span data-stu-id="78231-226">Line unit price</span></span>        | <span data-ttu-id="78231-227">%lineprice% (doğrula)</span><span class="sxs-lookup"><span data-stu-id="78231-227">%lineprice% (verify)</span></span> |
| <span data-ttu-id="78231-228">satır maddesi toplamı</span><span class="sxs-lookup"><span data-stu-id="78231-228">line item total</span></span>        | <span data-ttu-id="78231-229">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="78231-229">%linenetamount%</span></span> |
| <span data-ttu-id="78231-230">satır iskontosu</span><span class="sxs-lookup"><span data-stu-id="78231-230">line discount</span></span>          | <span data-ttu-id="78231-231">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="78231-231">%linediscount%</span></span> |
| <span data-ttu-id="78231-232">Sevk tarihi</span><span class="sxs-lookup"><span data-stu-id="78231-232">Ship date</span></span>              | <span data-ttu-id="78231-233">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="78231-233">%lineshipdate%</span></span> |
| <span data-ttu-id="78231-234">Tedarik yöntemi</span><span class="sxs-lookup"><span data-stu-id="78231-234">Procurement method</span></span>     | <span data-ttu-id="78231-235">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="78231-235">%linedeliverymode%</span></span> |
| <span data-ttu-id="78231-236">teslimat adresi</span><span class="sxs-lookup"><span data-stu-id="78231-236">delivery address</span></span>       | <span data-ttu-id="78231-237">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="78231-237">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="78231-238">Satırın satış birimi</span><span class="sxs-lookup"><span data-stu-id="78231-238">Sales unit of the line</span></span> | <span data-ttu-id="78231-239">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="78231-239">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="78231-240">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="78231-240">Additional resources</span></span>

[<span data-ttu-id="78231-241">Dynamics 365 Commerce önizleme ortamına genel bakış</span><span class="sxs-lookup"><span data-stu-id="78231-241">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="78231-242">Dynamics 365 Commerce önizleme ortamını hazırlama</span><span class="sxs-lookup"><span data-stu-id="78231-242">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="78231-243">Dynamics 365 Commerce önizleme ortamını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="78231-243">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="78231-244">Dynamics 365 Commerce önizleme ortamıyla ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="78231-244">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="78231-245">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="78231-245">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="78231-246">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="78231-246">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="78231-247">Microsoft Azure portalı</span><span class="sxs-lookup"><span data-stu-id="78231-247">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="78231-248">Dynamics 365 Commerce web sitesi</span><span class="sxs-lookup"><span data-stu-id="78231-248">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

---
title: Microsoft Dynamics 365 Talent - Attract'ta e-posta ayarlarını yapılandırma
description: Bu konu, Microsoft Dynamics 365 Talent - Attract tarafından gönderilen e-posta ayarlarının nasıl yapılandırılacağını açıklamaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: a457deec757a5d5a3e01c6903b2dd7a9d975ef0b
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551553"
---
# <a name="configure-email-settings-in-microsoft-dynamics-365-talent---attract"></a><span data-ttu-id="dd060-103">Microsoft Dynamics 365 Talent - Attract'ta e-posta ayarlarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="dd060-103">Configure email settings in Microsoft Dynamics 365 Talent - Attract</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="dd060-104">Markanız güven oluşturur ve pozisyonlarınıza başvurmadan önce adaylarla bir ilişki kurmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="dd060-104">Your brand establishes trust and helps you build a relationship with candidates before they even apply for your positions.</span></span> <span data-ttu-id="dd060-105">Olumlu marka algısı en yeteneklilerin ilgisini çeker ve mevcut çalışanların da bağlılığını kuvvetlendirir.</span><span class="sxs-lookup"><span data-stu-id="dd060-105">Positive brand perception attracts top talent and increases the loyalty of existing employees.</span></span> <span data-ttu-id="dd060-106">Microsoft Dynamics 365 Talent: Attract şirketinizin markasını yansıtması için e-postaları yapılandırmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="dd060-106">Microsoft Dynamics 365 Talent: Attract lets you configure emails so that they reflect your company's brand.</span></span> <span data-ttu-id="dd060-107">Bu nedenle, iş adaylarıyla başvuru süreci boyunca tutarlı bir deneyim sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd060-107">Therefore, you can provide a consistent experience to job candidates as they progress through the application process.</span></span>

<span data-ttu-id="dd060-108">Attract aşağıdaki eylemleri gerçekleştirmenizi sağlar:</span><span class="sxs-lookup"><span data-stu-id="dd060-108">Attract lets you perform these actions:</span></span>

- <span data-ttu-id="dd060-109">E-posta ayarlarını şirketinizin Microsoft Exchange e-posta hizmeti hesabı kullanılacak şekilde yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="dd060-109">Configure email settings so that your company's Microsoft Exchange email service account is used.</span></span> <span data-ttu-id="dd060-110">Böylece adaylar, e-postaların şirkettinizden geldiğini bilir.</span><span class="sxs-lookup"><span data-stu-id="dd060-110">In this way, candidates know that the emails are coming from your company.</span></span> <span data-ttu-id="dd060-111">Örneğin ayarlarınızı adaylarınızın e-postalarınızı `contoso@microsoft.com` yerine `recruiting@contoso.com` adresinden almalarını sağlayacak şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd060-111">For example, you can configure your settings so that candidates receive emails from `recruiting@contoso.com` instead of `contoso@microsoft.com`.</span></span>
- <span data-ttu-id="dd060-112">E-posta şablonları için genel bir üstbilgi ve altbilgi ayarlayarak tüm e-posta iletişimleriniz için tutarlı bir marka oluşturun.</span><span class="sxs-lookup"><span data-stu-id="dd060-112">Create consistent branding for all your email communications by setting a global header and footer for email templates.</span></span> 

> [!NOTE]
> <span data-ttu-id="dd060-113">Attract'i e-posta göndermek amacıyla şirketinizin e-posta hizmeti hesabını kullanacak şekilde yapılandırmak için Kapsamlı işe alma eklentisi gerekir.</span><span class="sxs-lookup"><span data-stu-id="dd060-113">To configure Attract so that it uses your company's email service account to send email, you need the Comprehensive hiring add-on.</span></span>

## <a name="connect-an-email-service-account"></a><span data-ttu-id="dd060-114">E-posta hizmet hesabına bağlanın</span><span class="sxs-lookup"><span data-stu-id="dd060-114">Connect an email service account</span></span>

<span data-ttu-id="dd060-115">Şirketinizin e-posta hizmeti hesabına bağlanarak iş adaylarınız için markalı bir e-posta deneyimi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd060-115">By connecting your company's email service account, you can create a branded email experience for your job candidates.</span></span> <span data-ttu-id="dd060-116">Şirket hesabınızı bağlamazsanız Attract, varsayılan Microsoft markalı e-posta hizmeti hesabını kullanır.</span><span class="sxs-lookup"><span data-stu-id="dd060-116">If you don't connect your company account, Attract uses the default Microsoft-branded email service account.</span></span>

1. <span data-ttu-id="dd060-117">**Ayarlar** düğmesini (sayfanın sağ üst köşesindki çark simgesi) seçin ve sonra **Yönetici merkezini** seçin.</span><span class="sxs-lookup"><span data-stu-id="dd060-117">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="dd060-118">**E-posta ayarları** sekmesinde, **E-posta hizmeti hesapları** altında **Şirket hesabı bağla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="dd060-118">On the **Email settings** tab, under **Email service accounts**, select **Connect a company account**.</span></span>

    ![Şirketinizin e-posta hizmeti hesabına Attract'te bağlama](./media/attract-admin-email-service-accounts.png)

    <span data-ttu-id="dd060-120">Paylaşılan bir e-posta hesabı oluşturma hakkında daha fazla bilgi için [Paylaşılan e-posta hesabı Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes)'deki paylaşılan posta kutularına bakın.</span><span class="sxs-lookup"><span data-stu-id="dd060-120">For more information about how to create a shared email account, see [Shared mailboxes in Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span></span>

3. <span data-ttu-id="dd060-121">Microsoft oturum açma penceresinde, şirket kimlik bilgilerinizi kullanarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="dd060-121">In the Microsoft sign-in window, sign in by using your corporate credentials.</span></span>
4. <span data-ttu-id="dd060-122">Henüz bir e-posta hizmeti hesabı ayarlamadıysanız veya yeni bir hesap eklemek istiyorsanız **Yeni hizmet hesabı ekle**'yi seçin ve sonra e-posta bilgilerinizi girin.</span><span class="sxs-lookup"><span data-stu-id="dd060-122">If you haven't yet set up an email service account, or if you want to add a new one, select **Add new service account**, and then enter your email information.</span></span> <span data-ttu-id="dd060-123">Kullanmak istediğiniz e-posta hizmeti hesabını zaten ayarladıysanız onu seçin.</span><span class="sxs-lookup"><span data-stu-id="dd060-123">If you've already set up the email service account that you want to use, select it.</span></span>

<span data-ttu-id="dd060-124">E-posta hizmeti hesabınız başarıyla yapılandırıldığında, bunu **E-posta hizmeti hesapları altında** görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd060-124">When your email service account is successfully configured, you will see it listed under **Email service accounts**.</span></span>

## <a name="disconnect-an-email-service-account"></a><span data-ttu-id="dd060-125">E-posta hizmet hesabıyla bağlantıyı kesin</span><span class="sxs-lookup"><span data-stu-id="dd060-125">Disconnect an email service account</span></span>

<span data-ttu-id="dd060-126">E-posta iletişiminde şirketinizin etki alanını, Attract kullanarak durdurmak istiyorsanız bir e-posta hizmeti hesabının bağlantısını kesebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd060-126">If you want to stop using your company's domain in email communications through Attract, you can disconnect an email service account.</span></span>

1. <span data-ttu-id="dd060-127">**Ayarlar** düğmesini (sayfanın sağ üst köşesindki çark simgesi) seçin ve sonra **Yönetici merkezini** seçin.</span><span class="sxs-lookup"><span data-stu-id="dd060-127">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="dd060-128">**E-posta ayarları** sekmesinde, **E-posta hizmeti hesapları** altında, kesmek istediğiniz e-posta hizmeti hesabının yanındaki **Daha fazla** düğmesini (üç dikey nokta) seçin.</span><span class="sxs-lookup"><span data-stu-id="dd060-128">On the **Email settings** tab, under **Email service accounts**, select the **More** button (three vertical dots) next to the email service account that you want to disconnect.</span></span>
3. <span data-ttu-id="dd060-129">**E-posta hesabı bağlantısını kes**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="dd060-129">Select **Disconnect email account**.</span></span>

    ![Şirketinizin e-posta hizmeti hesabının bağlantısını kesme](./media/attract-admin-disconnect-email-account.png)

4. <span data-ttu-id="dd060-131">İşlemi onaylamanız istendiğinde, **Bağlantıyı kes**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="dd060-131">When you're prompted to confirm the operation, select **Disconnect**.</span></span>

    ![Şirketinizin e-posta hizmeti hesabının bağlantısının kesilmesini onaylama](./media/attract-admin-email-confirm-disconnect.png)

<span data-ttu-id="dd060-133">Farklı bir e-posta hizmeti hesabı bağlamazsanız Attract'tan atılan e-postalarda varsayılan olarak Microsoft markalı e-posta hizmeti hesabı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dd060-133">If you don't connect a different email service account, emails that are sent from Attract will use the default Microsoft-branded email service account.</span></span>

## <a name="configure-email-template-settings"></a><span data-ttu-id="dd060-134">E-posta şablonu ayarlarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="dd060-134">Configure email template settings</span></span>

<span data-ttu-id="dd060-135">Şirketinizin logosunu ve diğer bilgileri e-postalarınızın markalı başlığı olması için karşıdan yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd060-135">You can upload an image of your company's logo and other information as a branded header for your emails.</span></span> <span data-ttu-id="dd060-136">Ayrıca e-posta altbilgilerindeki Gizlilik ilkenize ve kullanım koşullarına da bağlantı sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd060-136">You can also provide links to your privacy policy and terms of use in email footers.</span></span>

> [!NOTE]
> <span data-ttu-id="dd060-137">Ülkenizde, bölgenizde ve e-posta alıcısının ülkesinde ve bölgesinde yürürlükte olan tüm yasalara uymanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dd060-137">You must comply with all applicable laws of your country or region, and also the country or region that governs the email recipient.</span></span> <span data-ttu-id="dd060-138">Bu yasalar istenmeyen posta önleme düzenlemeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="dd060-138">These laws include anti-spam regulations.</span></span>

1. <span data-ttu-id="dd060-139">**Ayarlar** düğmesini (sayfanın sağ üst köşesindki çark simgesi) seçin ve sonra **Yönetici merkezini** seçin.</span><span class="sxs-lookup"><span data-stu-id="dd060-139">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="dd060-140">**E-posta ayarları** sekmesinde, **E-posta şablonu ayarları** altında, e-posta üstbilgileriniz olarak kullanmak istediğiniz görüntüyü görüntü kutusuna sürükleyin veya dosyaya gözatmak için görüntü kutusuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd060-140">On the **Email settings** tab, under **Email template settings**, drag the image that you want to use as your email header into the image box, or click in the image box to browse for the file.</span></span> <span data-ttu-id="dd060-141">Varolan bir görüntüyü değiştirmek için önce görüntünün yanındaki **Kaldır**'ı seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="dd060-141">To replace an existing image, you must first select **Remove** next to it.</span></span> <span data-ttu-id="dd060-142">Görüntü bir JPEG, JPG, PNG veya SVG dosyası olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="dd060-142">The image must be a JPEG, JPG, PNG, or SVG file.</span></span> <span data-ttu-id="dd060-143">Görüntüler için önerilen boyut 25-800 piksel genişliğinde ve 25 ila 150 piksel yüksekliğindedir.</span><span class="sxs-lookup"><span data-stu-id="dd060-143">The recommended size for images is between 25 and 800 pixels wide, and between 25 and 150 pixels high.</span></span> <span data-ttu-id="dd060-144">Başlık için maksimum dosya boyutu 1 megabayttır (MB).</span><span class="sxs-lookup"><span data-stu-id="dd060-144">The maximum file size for the header is 1 megabyte (MB).</span></span>

    ![Şirketinizin e-posta üstbilgisine resim ekleme](./media/attract-admin-email-header.png)

3. <span data-ttu-id="dd060-146">**İletişim için Gizlilik politikanızın** altında şirketinizin gizlilik ilkesine bir bağlantı sağlayın.</span><span class="sxs-lookup"><span data-stu-id="dd060-146">Under **Your Privacy policy for communications**, provide a link to your company's privacy policy.</span></span> <span data-ttu-id="dd060-147">**İletişim için Hüküm ve Koşullarınızın** altında şirketinizin kullanım koşullarına bir bağlantı sağlayın.</span><span class="sxs-lookup"><span data-stu-id="dd060-147">Under **Your Terms and conditions for communication**, provide a link to your company's terms of use.</span></span>

    ![Şirketinizin gizlilik politikasına ve e-posta alt bilgisi ile ilgili kullanım koşullarına bağlantılar ekleme](./media/attract-admin-email-footer.png)

4. <span data-ttu-id="dd060-149">E-posta şablon ayarlarınızı kaydetmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="dd060-149">Select **Save** to save your email template settings.</span></span>

---
title: Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta Azure Active Directory (Azure AD) işletme-müşteri (B2C) kiracılar kullanıcıları için özelleştirilmiş kaydolmayı işleyen özel sayfaların nasıl oluşturulacağı açıklanmaktadır.
author: brianshook
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3328fad5328ae1954a6749f9a5eebcb71c723698
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477960"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a><span data-ttu-id="62e28-103">Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama</span><span class="sxs-lookup"><span data-stu-id="62e28-103">Set up custom pages for user sign-ins</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="62e28-104">Bu konuda, Microsoft Dynamics 365 Commerce'ta Azure Active Directory (Azure AD) işletme-müşteri (B2C) kiracılar kullanıcıları için özelleştirilmiş kaydolmayı işleyen özel sayfaların nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="62e28-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

<span data-ttu-id="62e28-105">Dynamics 365 Commerce'te kullanıcı oturum açma akışlarını işlemek amacıyla yazılan özel sayfaları kullanmak için, Commerce ortamında başvurulacak Azure AD ilkeleri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="62e28-105">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="62e28-106">Azure AD B2C uygulamasını kullanarak "Kaydet ve oturum aç," "profil düzenlemesi" ve "parola sıfırlama" Azure AD B2C ilkelerini yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="62e28-106">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="62e28-107">Daha sonra, Azure AD B2C kiracısı ve ilke adlarına, Microsoft Dynamics Lifecycle Services (LCS) kullanılarak Commerce ortamı için yapılan sağlama işlemi sırasında başvurulabilir.</span><span class="sxs-lookup"><span data-stu-id="62e28-107">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="62e28-108">Özel ticaret sayfaları oturum açma, kayıt, hesap profili düzenleme veya parola sıfırlama modülü kullanılarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="62e28-108">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="62e28-109">Bu özel sayfalar için yayınlanan sayfa URL'lerine, Azure portalında Azure AD B2C ilkesi yapılandırmalarında başvurulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="62e28-109">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="62e28-110">B2C ilkelerini ayarla</span><span class="sxs-lookup"><span data-stu-id="62e28-110">Set up B2C policies</span></span>

<span data-ttu-id="62e28-111">Azure AD B2C kiracınızı ayarladıktan ve Commerce ortamınızla ilişkilendirdikten sonra, Azure portalında **Azure AD B2C** sayfasına gidin ve menüsünde, **İlkeler** altında, **Kullanıcı akışlarını (ilkeler)** seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-111">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![Kullanıcı akışları (ilkeler) komutu menüde](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="62e28-113">"Kaydet ve oturum aç", "Profil düzenlemesi" ve "parola sıfırlama" kullanıcı oturum açma akışlarını yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="62e28-113">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="62e28-114">"Oturum aç ve oturum aç" ilkesini yapılandırın</span><span class="sxs-lookup"><span data-stu-id="62e28-114">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="62e28-115">"Oturum aç ve oturum aç" ilkesini yapılandırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="62e28-115">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="62e28-116">**Yeni Kullanıcı akışı**'nı seçin ve **önerilen** sekmede **Kaydol ve oturum aç** ilkesini seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-116">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="62e28-117">İlke için bir ad girin (örneğin **B2C\_1\_KaydolOturumAç**).</span><span class="sxs-lookup"><span data-stu-id="62e28-117">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="62e28-118">**Kimlik sağlayıcıları** bölümünde, ilke için kullanılacak kimlik sağlayıcılarını seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-118">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="62e28-119">En azından, **e-posta kaydı** seçilmelidir.</span><span class="sxs-lookup"><span data-stu-id="62e28-119">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="62e28-120">**Öznitelik topla** sütununda, **E-posta Adresi**, **Verilen ad** ve **Soyadı** onay kutularını seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-120">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="62e28-121">**İade talebi** sütununda , **e-posta adreslerinin**, **verilen ad**, **kimlik sağlayıcı**, **soyadı** ve **kullanıcının nesne kodu** onay kutularını seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-121">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![Seçilen öznitelikler ve talepler](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="62e28-123">İlkeyi oluşturmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-123">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="62e28-124">Yeni ilke adını çift tıklatın ve sonra gezinme bölmesinde **Özellikler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-124">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="62e28-125">**JavaScript'i zorlamayı etkinleştir sayfa düzeni (Önizleme)** seçeneğini **açık** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="62e28-125">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![Yeni ilke için Özellikler sayfası](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="62e28-127">İlke adı, Commerce ortamında tam olarak referans edilir.</span><span class="sxs-lookup"><span data-stu-id="62e28-127">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="62e28-128">(**B2C\_1\_** öneki başvuruya dahil edilecek.) İlkeler, oluşturulduktan sonra yeniden adlandırılamaz.</span><span class="sxs-lookup"><span data-stu-id="62e28-128">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="62e28-129">Commerce ortamınız için varolan bir ilkeyi değiştiriyorsanız, özgün ilkeyi silebilir ve aynı ada sahip yeni bir ilke oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="62e28-129">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="62e28-130">Alternatif olarak, ortam önceden sağlanmış ise, yeni ilke adını bir servis isteği aracılığıyla gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="62e28-130">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="62e28-131">Özel sayfaları oluşturduktan sonra kurulum işlemini bitirmek için bu ilkeye geri dönersiniz.</span><span class="sxs-lookup"><span data-stu-id="62e28-131">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="62e28-132">Şimdilik, Azure portalında **Kullanıcı akışları (ilkeler)** sayfasına dönmek için ilkeyi kapatın.</span><span class="sxs-lookup"><span data-stu-id="62e28-132">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="62e28-133">"Profil düzenleme" ilkesini yapılandırın</span><span class="sxs-lookup"><span data-stu-id="62e28-133">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="62e28-134">"Profil düzenleme" ilkesini yapılandırmak üzere bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="62e28-134">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="62e28-135">**Yeni Kullanıcı akışı**'nı seçin ve **önerilen** sekmede **Profil düzenleme** ilkesini seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-135">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="62e28-136">İlke için bir ad girin (örneğin **B2C\_1\_ProfilDüzenleme**).</span><span class="sxs-lookup"><span data-stu-id="62e28-136">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="62e28-137">**Kimlik sağlayıcıları** bölümünde, ilke için kullanılacak kimlik sağlayıcılarını seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-137">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="62e28-138">En azından **yerel hesap girişi** seçilmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="62e28-138">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="62e28-139">**Öznitelik topla** sütununda, **E-posta Adresleri** ve **Soyadı** onay kutularını seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-139">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="62e28-140">**İade talebi** sütununda , **e-posta adreslerinin**, **verilen ad**, **kimlik sağlayıcı**, **soyadı** ve **kullanıcının nesne kodu** onay kutularını seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-140">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="62e28-141">İlkeyi oluşturmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-141">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="62e28-142">Yeni ilke adını çift tıklatın ve sonra gezinme bölmesinde **Özellikler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-142">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="62e28-143">**JavaScript'i zorlamayı etkinleştir sayfa düzeni (Önizleme)** seçeneğini **açık** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="62e28-143">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="62e28-144">Özel sayfaları oluşturduktan sonra kurulum işlemini bitirmek için bu ilkeye geri dönersiniz.</span><span class="sxs-lookup"><span data-stu-id="62e28-144">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="62e28-145">Şimdilik, Azure portalında **Kullanıcı akışları (ilkeler)** sayfasına dönmek için ilkeyi kapatın.</span><span class="sxs-lookup"><span data-stu-id="62e28-145">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="62e28-146">"Parola sıfırlama" ilkesini yapılandırın</span><span class="sxs-lookup"><span data-stu-id="62e28-146">Configure the "Password reset" policy</span></span>

<span data-ttu-id="62e28-147">"Parola sıfırlama" ilkesini yapılandırmak üzere bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="62e28-147">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="62e28-148">**Yeni Kullanıcı akışı**'nı seçin ve **Önizleme** sekmede **Parola sıfırlama v1.1** ilkesini seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-148">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![Önizleme sekmesinde parola sıfırlama v 1.1 ilkesi seçildi](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="62e28-150">İlke için bir ad girin (örneğin **B2C\_1\_ParolayıUnut**).</span><span class="sxs-lookup"><span data-stu-id="62e28-150">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="62e28-151">**Kimlik sağlayıcılar** bölümünde, **e-posta adresini kullanarak Parolayı Sıfırla** 'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-151">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="62e28-152">**İade talebi** sütununda , **e-posta adreslerinin**, **verilen ad**, **soyadı** ve **kullanıcının nesne kodu** onay kutularını seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-152">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![Talepler seçildi](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="62e28-154">İlkeyi oluşturmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-154">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="62e28-155">Yeni ilke adını çift tıklatın ve sonra gezinme bölmesinde **Özellikler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-155">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="62e28-156">**JavaScript'i zorlamayı etkinleştir sayfa düzeni (Önizleme)** seçeneğini **açık** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="62e28-156">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="62e28-157">Özel sayfaları oluşturduktan sonra kurulum işlemini bitirmek için bu ilkeye geri dönersiniz.</span><span class="sxs-lookup"><span data-stu-id="62e28-157">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="62e28-158">Şimdilik, Azure portalında **Kullanıcı akışları (ilkeler)** sayfasına dönmek için ilkeyi kapatın.</span><span class="sxs-lookup"><span data-stu-id="62e28-158">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="62e28-159">Özel sayfalar oluşturma</span><span class="sxs-lookup"><span data-stu-id="62e28-159">Build the custom pages</span></span>

<span data-ttu-id="62e28-160">Kullanıcı oturum açma işlerine özel sayfalar oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="62e28-160">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="62e28-161">Commerce geliştirme araçlarında sitenize gidin.</span><span class="sxs-lookup"><span data-stu-id="62e28-161">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="62e28-162">Aşağıdaki beş şablonu ve beş sayfayı oluşturun:</span><span class="sxs-lookup"><span data-stu-id="62e28-162">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="62e28-163">**Oturum açma** şablonu ve oturum açma modülünü kullanan sayfa.</span><span class="sxs-lookup"><span data-stu-id="62e28-163">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="62e28-164">**Kaydolma** şablonu ve kaydolma modülünü kullanan sayfa.</span><span class="sxs-lookup"><span data-stu-id="62e28-164">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="62e28-165">**Parola sıfırlama** şablonu ve parola sıfırlama modülünü kullanan sayfa.</span><span class="sxs-lookup"><span data-stu-id="62e28-165">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="62e28-166">**Parola sıfırlama doğrulaması** şablonu ve parola sıfırlama doğrulama modülünü kullanan sayfa.</span><span class="sxs-lookup"><span data-stu-id="62e28-166">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="62e28-167">Hesap profili düzenleme modülünü kullanan bir **profil Düzenle** şablonu ve sayfa</span><span class="sxs-lookup"><span data-stu-id="62e28-167">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="62e28-168">Sayfaları derlediğinizde aşağıdaki yönergeleri izleyin:</span><span class="sxs-lookup"><span data-stu-id="62e28-168">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="62e28-169">Her sayfa veya modülle ilgili iş gereksinimlerinize en uygun düzeni ve stili kullanın.</span><span class="sxs-lookup"><span data-stu-id="62e28-169">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="62e28-170">Azure AD B2C kurulumunda kullanılması gereken tüm sayfaları ve URL 'leri yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="62e28-170">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="62e28-171">Sayfalar ve URL'ler yayımlandıktan sonra, Azure AD B2C ilkesi yapılandırmaları için kullanılması gereken URL'leri toplayın.</span><span class="sxs-lookup"><span data-stu-id="62e28-171">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="62e28-172">A **?preloadscripts = true** soneki kullanıldığında, her URL 'ye eklenir.</span><span class="sxs-lookup"><span data-stu-id="62e28-172">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="62e28-173">Göreli bağlantıları olan evrensel üstbilgileri ve altbilgileri yeniden kullanmayın.</span><span class="sxs-lookup"><span data-stu-id="62e28-173">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="62e28-174">Kullanıldıkları sırada bu sayfalar Azure AD B2C etki alanında barındırılacak çünkü tüm bağlantılar için yalnızca mutlak URL'ler kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="62e28-174">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="62e28-175">Azure AD B2C ilkelerini özel sayfa bilgileriyle konfigüre edin</span><span class="sxs-lookup"><span data-stu-id="62e28-175">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="62e28-176">Azure portalında **Azure AD B2C** sayfasına dönün ve sonra menüde **ilkeler** altında **Kullanıcı akışları'nı (ilkeler)** seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-176">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="62e28-177">"Kaydol ve oturum aç" ilkesini özel sayfa bilgileriyle güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="62e28-177">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="62e28-178">"Kaydol ve oturum aç" ilkesini özel sayfa bilgileriyle güncelleştirmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="62e28-178">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="62e28-179">Daha önce konfigüre ettiğiniz **oturum açma ve kaydolma** ilkesinde, gezinti bölmesinde **sayfa düzenleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-179">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="62e28-180">**Birleşik kayıt veya oturum açma sayfa** düzenini seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-180">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="62e28-181">**Özel sayfa içeriğini kullan** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="62e28-181">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="62e28-182">**Özel sayfa URI** alanına tam oturum açma URL 'si girin.</span><span class="sxs-lookup"><span data-stu-id="62e28-182">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="62e28-183">**?preloadscripts=true** sonekini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="62e28-183">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="62e28-184">Örneğin ``www.<my domain>.com/sign-in?preloadscripts=true`` yazın.</span><span class="sxs-lookup"><span data-stu-id="62e28-184">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="62e28-185">**Sayfa düzeni sürümü (Önizleme)** alanında, **1.2.0** seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-185">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="62e28-186">**Yerel hesap kayıt sayfası** düzenini seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-186">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="62e28-187">**Özel sayfa içeriğini kullan** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="62e28-187">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="62e28-188">**Özel sayfa URI** alanına tam oturum açma URL 'si girin.</span><span class="sxs-lookup"><span data-stu-id="62e28-188">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="62e28-189">**?preloadscripts=true** sonekini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="62e28-189">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="62e28-190">Örneğin ``www.<my domain>.com/sign-up?preloadscripts=true`` yazın.</span><span class="sxs-lookup"><span data-stu-id="62e28-190">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="62e28-191">**Sayfa düzeni sürümü (Önizleme)** alanında, **1.2.0** seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-191">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="62e28-192">**Kullanıcı öznitelikleri** bölümünde, şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="62e28-192">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="62e28-193">**E-posta adresi**, **verilen ad** ve **Soyadı** öznitelikleri için **doğrulama gerekli** alanında **Hayır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-193">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="62e28-194">**Verilen ad** ve **Soyadı** öznitelikleri için **İsteğe bağlı** alanında **Hayır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-194">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![Yerel hesap kayıt sayfası ilkesi yapılandırması](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="62e28-196">"Profil düzenleme" ilkesini özel sayfa bilgileriyle güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="62e28-196">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="62e28-197">"Profil düzenleme" ilkesini özel sayfa bilgileriyle güncelleştirmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="62e28-197">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="62e28-198">Daha önce konfigüre ettiğiniz **Profil düzenleme** ilkesinde, gezinti bölmesinde **sayfa düzenleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-198">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="62e28-199">**Profil düzenleme sayfa** düzenini seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-199">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="62e28-200">**Özel sayfa içeriğini kullan** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="62e28-200">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="62e28-201">**Özel sayfa URI** alanına tam profil düzenleme URL'si girin.</span><span class="sxs-lookup"><span data-stu-id="62e28-201">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="62e28-202">**?preloadscripts=true** sonekini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="62e28-202">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="62e28-203">Örneğin ``www.<my domain>.com/profile-edit?preloadscripts=true`` yazın.</span><span class="sxs-lookup"><span data-stu-id="62e28-203">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="62e28-204">**Sayfa düzeni sürümü (Önizleme)** alanında, **1.2.0** seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-204">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="62e28-205">**Kullanıcı öznitelikleri** bölümünde, şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="62e28-205">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="62e28-206">**E-posta adresi**, **verilen ad** öznitelikleri için **doğrulama gerekli** alanında **Hayır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-206">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="62e28-207">**Verilen ad** ve **Soyadı** öznitelikleri için **İsteğe bağlı** alanında **Hayır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-207">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="62e28-208">"Parola sıfırlama" ilkesini özel sayfa bilgileriyle güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="62e28-208">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="62e28-209">"Parola sıfırlama" ilkesini özel sayfa bilgileriyle güncelleştirmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="62e28-209">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="62e28-210">Daha önce konfigüre ettiğiniz **Parola sıfırlama** ilkesinde, gezinti bölmesinde **sayfa düzenleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-210">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="62e28-211">**Yeni parola sayfası** düzenini seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-211">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="62e28-212">**Özel sayfa içeriğini kullan** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="62e28-212">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="62e28-213">**Özel sayfa URI** alanına tam parola sıfırlama URL'si girin.</span><span class="sxs-lookup"><span data-stu-id="62e28-213">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="62e28-214">**?preloadscripts=true** sonekini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="62e28-214">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="62e28-215">Örneğin ``www.<my domain>.com/passwordreset?preloadscripts=true`` yazın.</span><span class="sxs-lookup"><span data-stu-id="62e28-215">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="62e28-216">**Sayfa düzeni sürümü (Önizleme)** alanında, **1.2.0** seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-216">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="62e28-217">**Hesap doğrulama sayfası** düzenini seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-217">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="62e28-218">**Özel sayfa içeriğini kullan** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="62e28-218">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="62e28-219">**Özel sayfa URI** alanına tam parola sıfırlama doğrulama URL'si girin.</span><span class="sxs-lookup"><span data-stu-id="62e28-219">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="62e28-220">**?preloadscripts=true** sonekini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="62e28-220">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="62e28-221">Örneğin ``www.<my domain>.com/passwordreset-verification?preloadscripts=true`` yazın.</span><span class="sxs-lookup"><span data-stu-id="62e28-221">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="62e28-222">**Sayfa düzeni sürümü (Önizleme)** alanında, **1.2.0** seçin.</span><span class="sxs-lookup"><span data-stu-id="62e28-222">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="62e28-223">Etiketler ve açıklamalar için varsayılan metin dizelerini Özelleştir</span><span class="sxs-lookup"><span data-stu-id="62e28-223">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="62e28-224">Modül kitaplığında, oturum açma modülleri, Etiketler ve açıklamalar için varsayılan metin dizeleriyle önceden doldurulur.</span><span class="sxs-lookup"><span data-stu-id="62e28-224">In the module library, sign-in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="62e28-225">Yazılım geliştirme setinde (SDK) Bu dizeleri, günlük modülünde bulunan Global.JSON dosyasındaki değerleri güncelleştirerek özelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="62e28-225">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="62e28-226">Örneğin, Unutulan parola bağlantısı için varsayılan metin **parola unutuldu mu?**'dur.</span><span class="sxs-lookup"><span data-stu-id="62e28-226">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="62e28-227">Aşağıda bu varsayılan metin oturum açma sayfasında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="62e28-227">The following shows this default text on the sign-in page.</span></span>

![Oturum açma sayfasında Unutulan parola bağlantısı için varsayılan metin](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="62e28-229">Ancak, modül kitaplığı oturum açma modülü için Global.json dosyasında **Parolayı unuttunuz mu?** metnini düzenleyebilirsiniz, aşağıdaki şekilde gösterildiği gibi.</span><span class="sxs-lookup"><span data-stu-id="62e28-229">However, in the global.json file for the module library sign-in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![Oturum açma modülünün Global.json dosyasında bağlantı metni güncelleştirildi](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="62e28-231">Global.json dosyasını güncelleştirip değişikliklerinizi yayımladıktan sonra, yeni bağlantı metni hem ticaret hem de canlı oturum açma sayfasında bulunan modülde günlükte görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="62e28-231">After you update the global.json file and publish your changes, the new link text appears in the sign-in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="62e28-232">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="62e28-232">Additional resources</span></span>

[<span data-ttu-id="62e28-233">Etki alanı adınızı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="62e28-233">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="62e28-234">Yeni bir e-ticaret kiracısını dağıtma</span><span class="sxs-lookup"><span data-stu-id="62e28-234">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="62e28-235">E-ticaret sitesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="62e28-235">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="62e28-236">Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="62e28-236">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="62e28-237">robots.txt dosyalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="62e28-237">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="62e28-238">URL yeniden yönlendirmelerini toplu olarak yükleme</span><span class="sxs-lookup"><span data-stu-id="62e28-238">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="62e28-239">Commerce'ta B2C kiracısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="62e28-239">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="62e28-240">Commerce ortamında birden fazla B2C kiracısı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="62e28-240">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="62e28-241">İçerik teslim ağı (CDN) için destek ekleme</span><span class="sxs-lookup"><span data-stu-id="62e28-241">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="62e28-242">Konum tabanlı mağaza algılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="62e28-242">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

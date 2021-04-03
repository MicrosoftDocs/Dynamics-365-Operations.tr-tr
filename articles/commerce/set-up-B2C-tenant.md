---
title: Commerce'ta B2C kiracısı ayarlama
description: Bu konu, Dynamics 365 Commerce'ta kullanıcı sitesi kimlik doğrulaması için Azure Active Directory (Azure AD) işletme-müşteri arası (B2C) kiracılarınızın nasıl kurulacağını açıklamaktadır.
author: BrianShook
manager: annbe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4ee667bb49e70e0c881a2db1248b3f0c7fc017ce
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478152"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a><span data-ttu-id="6a6eb-103">Commerce'ta B2C kiracısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="6a6eb-103">Set up a B2C tenant in Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6a6eb-104">Bu konu, Dynamics 365 Commerce'ta kullanıcı sitesi kimlik doğrulaması için Azure Active Directory (Azure AD) işletme-müşteri arası (B2C) kiracılarınızın nasıl kurulacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-104">This topic describes how to set up your Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants for user site authentication in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6a6eb-105">Dynamics 365 Commerce, kullanıcı kimlik bilgileri ve kimlik doğrulama akışlarını desteklemek için Azure AD B2C kullanır.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-105">Dynamics 365 Commerce uses Azure AD B2C to support user credential and authentication flows.</span></span> <span data-ttu-id="6a6eb-106">Kullanıcı, bu akışlar aracılığıyla kaydolabilir, oturum açabilir ve parolasını sıfırlayabilir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-106">A user can sign up, sign in, and reset their password through these flows.</span></span> <span data-ttu-id="6a6eb-107">Azure AD B2C kullanıcının hassas kimlik doğrulama bilgilerini (örneğin, kullanıcı adı ve parolası) depolar.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-107">Azure AD B2C stores sensitive user authentication information, such as username and password.</span></span> <span data-ttu-id="6a6eb-108">B2C kiracısındaki kullanıcı kaydı, bir B2C yerel hesap kaydını ya da B2C sosyal kimlik sağlayıcısı kaydını depolar.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-108">The user record in the B2C tenant will store either a B2C local account record or a B2C social identity provider record.</span></span> <span data-ttu-id="6a6eb-109">Bu B2C kayıtları Commerce ortamındaki müşteri kaydına geri bağlantı sağlar.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-109">These B2C records will link back to the customer record in the Commerce environment.</span></span>

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a><span data-ttu-id="6a6eb-110">Azure portalında mevcut bir AAD B2C kiracısı oluşturma veya bu kiracıya bağlantı sağlama</span><span class="sxs-lookup"><span data-stu-id="6a6eb-110">Create or link to an existing AAD B2C tenant in the Azure portal</span></span>

1. <span data-ttu-id="6a6eb-111">[Azure portalında](https://portal.azure.com/) adresinden oturum açın.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-111">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="6a6eb-112">Azure portalı menüsünden, **Kaynak oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-112">From the Azure portal menu, select **Create a resource**.</span></span> <span data-ttu-id="6a6eb-113">Commerce ortamınızla bağlanacak aboneliği ve dizini kullandığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-113">Be sure to use the subscription and directory that will be connected with your Commerce environment.</span></span>

    ![Azure Portalında Kaynak Oluşturma](./media/B2CImage_1.png)

1. <span data-ttu-id="6a6eb-115">**Kimlik \> Azure Active Directory B2C**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-115">Go to **Identity \> Azure Active Directory B2C**.</span></span>
1. <span data-ttu-id="6a6eb-116">**Yeni B2C Kiracısı Oluştur veya mevcut bir Kiracıya bağla** sayfasında, şirketinizin gereksinimlerine en uygun olan aşağıdaki seçeneklerden birini kullanın:</span><span class="sxs-lookup"><span data-stu-id="6a6eb-116">Once on the **Create New B2C Tenant or Link to existing Tenant** page, use one of the options below that best suits your company's needs:</span></span>

    - <span data-ttu-id="6a6eb-117">**Yeni Azure AD B2C kiracısı oluştur**: Yeni bir AAD B2C kiracısı oluşturmak için bu seçeneği kullanın.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-117">**Create a new Azure AD B2C Tenant**: Use this option to create a new AAD B2C tenant.</span></span>
        1. <span data-ttu-id="6a6eb-118">**Yeni bir Azure AD B2C Kiracısı oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-118">Select **Create a new Azure AD B2C Tenant**.</span></span>
        1. <span data-ttu-id="6a6eb-119">**Kuruluş adı** altında, kuruluş adını girin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-119">Under **Organization name**, enter the organization name.</span></span>
        1. <span data-ttu-id="6a6eb-120">**İlk etki alanı adı** altında, ilk etki alanı adını girin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-120">Under **Initial domain name**, enter the initial domain name.</span></span>
        1. <span data-ttu-id="6a6eb-121">**Ülke veya bölge** için ülkeyi veya bölgeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-121">For **Country or region**, select the country or region.</span></span>
        1. <span data-ttu-id="6a6eb-122">Kiracı oluşturmak için **Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-122">Select **Create** to create the tenant.</span></span>

     ![Yeni bir Azure AD Kiracısı Oluşturma](./media/B2CImage_2.png)

     - <span data-ttu-id="6a6eb-124">**Mevcut Azure AD B2C kiracısını Azure aboneliğime bağla**: Bu seçeneği, zaten bağlanmak istediğiniz bir Azure AD B2C kiracınız varsa kullanın.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-124">**Link an existing Azure AD B2C Tenant to my Azure subscription**: Use this option if you already have an Azure AD B2C tenant you want to link to.</span></span>
        1. <span data-ttu-id="6a6eb-125">**Mevcut Azure AD B2C Kiracısını Azure aboneliğime bağla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-125">Select **Link an existing Azure AD B2C Tenant to my Azure subscription**.</span></span>
        1. <span data-ttu-id="6a6eb-126">**Azure AD B2C Kiracısı** için uygun B2C kiracısını seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-126">For **Azure AD B2C Tenant**, select the appropriate B2C tenant.</span></span> <span data-ttu-id="6a6eb-127">Seçim kutusunda "Uygun B2C Kiracısı bulunamadı" iletisi görünürse, mevcut bir uygun B2C kiracınız yoktur ve yenisini oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-127">If the message "No eligible B2C Tenants found" appears in the selection box, you do not have an existing eligible B2C tenant and will need to create a new one.</span></span>
        1. <span data-ttu-id="6a6eb-128">**Kaynak grubu** için **Yeni oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-128">For **Resource group**, select **Create new**.</span></span> <span data-ttu-id="6a6eb-129">Kiracıyı içerecek kaynak grubu için bir **Ad** girin, **Kaynak grubu konumu**'nu ve ardından **Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-129">Enter a **Name** for the resource group that will contain the tenant, select the **Resource group location**, and then select **Create**.</span></span>

    ![Mevcut Azure AD B2C Kiracısını Azure Aboneliğine Bağlama](./media/B2CImage_3.png)

1. <span data-ttu-id="6a6eb-131">Yeni Azure AD B2C dizini oluşturulduktan sonra (bu birkaç dakika sürebilir), panoda yeni dizine bir bağlantı görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-131">Once the new Azure AD B2C directory is created (this may take a few moments), a link to the new directory will appear on the dashboard.</span></span> <span data-ttu-id="6a6eb-132">Bu bağlantı sizi "Azure Active Directory B2C'ye hoş geldiniz" sayfasına yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-132">This link will direct you to the "Welcome to Azure Active Directory B2C" page.</span></span>

    ![Yeni AAD Dizinine bağlama](./media/B2CImage_4.png)

> [!NOTE]
> <span data-ttu-id="6a6eb-134">Azure hesabınızda birden fazla aboneliğiniz varsa veya etkin bir aboneliğe bağlamadan B2C kiracısı ayarladıysanız, **Sorun giderme** başlığı sizi kiracıyı aboneliğe bağlamaya yönlendirecektir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-134">If you have multiple subscriptions within your Azure account or have set up the B2C tenant without linking to an active subscription, a **Troubleshoot** banner will direct you to link the tenant to a subscription.</span></span> <span data-ttu-id="6a6eb-135">Sorun giderme iletisini seçin ve abonelik sorununu gidermek için yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-135">Select the troubleshooting message and follow the instructions to resolve the subscription issue.</span></span>

<span data-ttu-id="6a6eb-136">Aşağıdaki resimde, bir Azure AD B2C **Sorun giderme** başlığı örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-136">The following image shows an example of an Azure AD B2C **Troubleshoot** banner.</span></span>

![Dizinde Etkin Abonelik olmadığını gösteren uyarı](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a><span data-ttu-id="6a6eb-138">B2C uygulaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="6a6eb-138">Create the B2C application</span></span>

<span data-ttu-id="6a6eb-139">B2C kiracısı oluşturulduktan sonra, Commerce eylemleriyle etkileşimde bulunmak için kiracı içinde bir B2C uygulaması oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-139">Once the B2C tenant has been created, you will create a B2C application within the tenant to interact with the Commerce actions.</span></span>

<span data-ttu-id="6a6eb-140">B2C uygulaması oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-140">To create the B2C application, follow these steps.</span></span>

1. <span data-ttu-id="6a6eb-141">Azure portalında **Uygulamalar (Eski)** öğesini ve sonra **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-141">In the Azure portal, select **Applications(Legacy)** and then select **Add**.</span></span>
1. <span data-ttu-id="6a6eb-142">**Ad** altında, istenen AAD B2C uygulamasının adını girin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-142">Under **Name**, enter the name of the desired AAD B2C application.</span></span>
1. <span data-ttu-id="6a6eb-143">**Web App/Web API** altında, **Web uygulaması / web API'sı ekle** için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-143">Under **Web App/Web API**, for **Include web app / web API**, select **Yes**.</span></span>
1. <span data-ttu-id="6a6eb-144">**Örtülü akışa izin ver** için **Evet**'i (varsayılan değer) seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-144">For **Allow implicit flow**, select **Yes** (the default value).</span></span>
1. <span data-ttu-id="6a6eb-145">**Yanıt URL'si** altında, atanmış yanıt URL'lerinizi girin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-145">Under **Reply URL**, enter your dedicated reply URLs.</span></span> <span data-ttu-id="6a6eb-146">Yanıt URL'leri ve nasıl biçimlendirilecekleri hakkında bilgi almak için aşağıdaki [Yanıt URL'leri](#reply-urls) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-146">See [Reply URLs](#reply-urls) below for information on reply URLs and how to format them here.</span></span>
1. <span data-ttu-id="6a6eb-147">**Yerel istemciyi dahil et** için **Hayır**'ı seçin (varsayılan değer).</span><span class="sxs-lookup"><span data-stu-id="6a6eb-147">For **Include native client**, select **No** (the default value).</span></span>
1. <span data-ttu-id="6a6eb-148">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-148">Select **Create**.</span></span>

### <a name="reply-urls"></a><span data-ttu-id="6a6eb-149">Yanıt URL'leri</span><span class="sxs-lookup"><span data-stu-id="6a6eb-149">Reply URLs</span></span>

<span data-ttu-id="6a6eb-150">Yanıt URL'leri, siteniz bir kullanıcı kimliğini doğrulamak için Azure AD B2C çağırdığında dönüş etki alanlarını için izin listesi sağladığından önemlidir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-150">Reply URLs are important as they provide an allow list of the return domains when your site calls Azure AD B2C to authenticate a user.</span></span> <span data-ttu-id="6a6eb-151">Bu, kimliği doğrulanmış kullanıcının oturum açtığı etki alanına (site etki alanı) geri döndürülmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-151">This permits the return of the authenticated user back to the domain from which they are signing into (your site domain).</span></span> 

<span data-ttu-id="6a6eb-152">**Azure AD B2c - Uygulamalar \> Yeni uygulama** ekranındaki **Yanıt URL'si** kutusunda, hem sitenizin etki alanı hem de (ortamınız sağlandıktan sonra) Commece tarafından oluşturulan URL için ayrı satırlar eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-152">In the **Reply URL** box on the **Azure AD B2c - Applications \> New application** screen, you need to add separate lines for both your site domain and (once your environment is provisioned) the Commerce-generated URL.</span></span> <span data-ttu-id="6a6eb-153">Bu URL'lerin her zaman geçerli bir URL biçimi kullanması ve yalnızca temel URL'ler olması gerekir (sonunda eğik çizgi veya yollar olmamalıdır).</span><span class="sxs-lookup"><span data-stu-id="6a6eb-153">These URLs must always use a valid URL format and must be base URLs only (no trailing forward slashes or paths).</span></span> <span data-ttu-id="6a6eb-154">Ardından ``/_msdyn365/authresp`` dizesinin temel URL'lere aşağıdaki örneklerde gösterildiği şekilde eklenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-154">The string ``/_msdyn365/authresp`` then needs to be appended to the base URLs, as in the following examples.</span></span>

- <span data-ttu-id="6a6eb-155">``https://www.fabrikam.com/_msdyn365/authresp``(Etki alanı e-ticaret etki alanıyla tamamen eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-155">``https://www.fabrikam.com/_msdyn365/authresp`` (The domain should match the e-commerce domain completely.</span></span> <span data-ttu-id="6a6eb-156">Birden çok etki alanınız varsa, her etki alanı için bu URL'yi eklemeniz gerekir.)</span><span class="sxs-lookup"><span data-stu-id="6a6eb-156">If you have multiple domains, you need to add this URL for each domain.)</span></span>
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a><span data-ttu-id="6a6eb-157">Kullanıcı akış ilkeleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="6a6eb-157">Create user flow policies</span></span>

<span data-ttu-id="6a6eb-158">Kullanıcı akışları, Azure AD B2C'nin güvenli oturum açma, kaydolma, profil düzenleme ve parola kullanıcı deneyimlerini unutmak için kullandığı ilkelerdir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-158">User flows are the policies Azure AD B2C uses to provide secure sign in, sign up, edit profile, and forget password user experiences.</span></span> <span data-ttu-id="6a6eb-159">Dynamics 365 Commerce, Azure AD B2C kiracısı ile etkileşimde bulunmak üzere ilke eylemlerini gerçekleştirmek için bu akışları kullanır.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-159">Dynamics 365 Commerce uses these flows to perform the policy actions to interact with the Azure AD B2C tenant.</span></span> <span data-ttu-id="6a6eb-160">Bir kullanıcı bu ilkelerle etkileşim kurduğunda, eylemleri gerçekleştirmek üzere Azure AD B2C kiracısına yeniden yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-160">When a user interacts with these policies, they are redirected to the Azure AD B2C tenant to perform the actions.</span></span>

<span data-ttu-id="6a6eb-161">Azure AD B2C üç temel kullanıcı akışı türü sağlar:</span><span class="sxs-lookup"><span data-stu-id="6a6eb-161">Azure AD B2C provides three basic user flow types:</span></span>
- <span data-ttu-id="6a6eb-162">Kaydolma ve oturum açma</span><span class="sxs-lookup"><span data-stu-id="6a6eb-162">Sign up and sign in</span></span>
- <span data-ttu-id="6a6eb-163">Profil düzenleme</span><span class="sxs-lookup"><span data-stu-id="6a6eb-163">Profile editing</span></span>
- <span data-ttu-id="6a6eb-164">Parola sıfırlandı</span><span class="sxs-lookup"><span data-stu-id="6a6eb-164">Password reset</span></span>

<span data-ttu-id="6a6eb-165">Azure AD tarafından sağlanan varsayılan kullanıcı akışlarını kullanmayı seçebilirsiniz; bu durumda AAD B2C tarafından barındırılan sayfa görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-165">You can choose to use the default user flows provided by Azure AD, which will display a page hosted by AAD B2C.</span></span> <span data-ttu-id="6a6eb-166">Alternatif olarak, bu kullanıcı akış deneyimlerinin görünümünü ve hissini denetlemek için bir HTML sayfası oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-166">Alternately, you can create an HTML page to control the look and feel of these user flow experiences.</span></span> 

<span data-ttu-id="6a6eb-167">Dynamics 365 Commerce için kullanıcı ilkesi sayfalarını özelleştirmek üzere bkz. [Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama](custom-pages-user-logins.md).</span><span class="sxs-lookup"><span data-stu-id="6a6eb-167">To customize the user policy pages for Dynamics 365 Commerce, see [Set up custom pages for user logins](custom-pages-user-logins.md).</span></span> <span data-ttu-id="6a6eb-168">Ek bilgi için bkz. [Azure Active Directory B2C'de kullanıcı arabirimi deneyimlerini özelleştirme](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span><span class="sxs-lookup"><span data-stu-id="6a6eb-168">For additional information, see [Customize the interface of user experiences in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span></span>

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a><span data-ttu-id="6a6eb-169">Kullanıcı akış ilkesinde kaydolma ve oturum açma oluşturma</span><span class="sxs-lookup"><span data-stu-id="6a6eb-169">Create a sign up and sign in user flow policy</span></span>

<span data-ttu-id="6a6eb-170">Kullanıcı akışı ilkesinde kaydolma ve oturum açma oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-170">To create a sign up and sign in user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="6a6eb-171">Azure portalında, sol gezinti bölmesinde **Kullanıcı akışları (ilkeler)** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-171">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="6a6eb-172">**Azure AD B2C - Kullanıcı akışları (ilkeler)** sayfasında, **Yeni Kullanıcı Akışı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-172">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="6a6eb-173">**Önerilen** sekmesinde, **Kaydet ve oturum aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-173">On the **Recommended** tab, select **Sign up and sign in**.</span></span>
1. <span data-ttu-id="6a6eb-174">**Ad** altında bir ilke adı girin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-174">Under **Name**, enter a policy name.</span></span> <span data-ttu-id="6a6eb-175">Bu ad, daha sonra portalın atadığı bir önekle (örneğin, "B2C_1_") birlikte görüntülenecektir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-175">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="6a6eb-176">**Kimlik sağlayıcıları** altında, uygun onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-176">Under **Identity providers**, select the appropriate check box.</span></span>
1. <span data-ttu-id="6a6eb-177">**Çok faktörlü Kimlik Doğrulaması** altında şirketiniz için uygun seçeneği belirleyin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-177">Under **Multifactor Authentication**, select the appropriate choice for your company.</span></span> 
1. <span data-ttu-id="6a6eb-178">**Kullanıcı öznitelikleri ve talepler** altında, öznitelikleri  veya iade taleplerini toplamak için ilgili seçenekleri seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-178">Under **User attributes and claims**, select options to collect attributes or return claims as appropriate.</span></span> <span data-ttu-id="6a6eb-179">Commerce aşağıdaki varsayılan seçenekleri gerekli kılar:</span><span class="sxs-lookup"><span data-stu-id="6a6eb-179">Commerce requires the following default options:</span></span>

    | <span data-ttu-id="6a6eb-180">**Öznitelik topla**</span><span class="sxs-lookup"><span data-stu-id="6a6eb-180">**Collect  attribute**</span></span> | <span data-ttu-id="6a6eb-181">**İade talebi**</span><span class="sxs-lookup"><span data-stu-id="6a6eb-181">**Return  claim**</span></span> |
    | ---------------------- | ----------------- |
    | <span data-ttu-id="6a6eb-182">E-posta Adresi</span><span class="sxs-lookup"><span data-stu-id="6a6eb-182">Email Address</span></span>          | <span data-ttu-id="6a6eb-183">E-posta Adresleri</span><span class="sxs-lookup"><span data-stu-id="6a6eb-183">Email Addresses</span></span>   |
    | <span data-ttu-id="6a6eb-184">Verilen Ad</span><span class="sxs-lookup"><span data-stu-id="6a6eb-184">Given Name</span></span>             | <span data-ttu-id="6a6eb-185">Verilen Ad</span><span class="sxs-lookup"><span data-stu-id="6a6eb-185">Given Name</span></span>        |
    |                        | <span data-ttu-id="6a6eb-186">Kimlik Sağlayıcı</span><span class="sxs-lookup"><span data-stu-id="6a6eb-186">Identity Provider</span></span> |
    | <span data-ttu-id="6a6eb-187">Soyadı</span><span class="sxs-lookup"><span data-stu-id="6a6eb-187">Surname</span></span>                | <span data-ttu-id="6a6eb-188">Soyadı</span><span class="sxs-lookup"><span data-stu-id="6a6eb-188">Surname</span></span>           |
    |                        | <span data-ttu-id="6a6eb-189">Kullanıcının Nesne kodu</span><span class="sxs-lookup"><span data-stu-id="6a6eb-189">User’s Object ID</span></span>  |

1. <span data-ttu-id="6a6eb-190">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-190">Select **Create**.</span></span>

<span data-ttu-id="6a6eb-191">Aşağıdaki resim, kullanıcı akışında Azure AD B2C kayıt olma ve oturum açmayla ilgili bir örnektir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-191">The following image is an example of the Azure AD B2C sign up and sign in user flow.</span></span>

![Kayıt Olma ve Oturum Açma ilke ayarları](./media/B2CImage_11.png)

<span data-ttu-id="6a6eb-193">Aşağıdaki resimde, kullanıcı akışındaki Azure AD B2C kayıt olma ve oturum açma eylemindeki **Kullanıcı akışı çalıştır** seçeneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-193">The following image shows the **Run user flow** option in the Azure AD B2C sign up and sign in user flow.</span></span>

![İlke akışında kullanıcı akışı seçeneğini çalıştır](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a><span data-ttu-id="6a6eb-195">Profil düzenleme kullanıcı akışı ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="6a6eb-195">Create a profile editing user flow policy</span></span>

<span data-ttu-id="6a6eb-196">Profil düzenleme kullanıcı akışı ilkesi oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-196">To create a profile editing user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="6a6eb-197">Azure portalında, sol gezinti bölmesinde **Kullanıcı akışları (ilkeler)** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-197">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="6a6eb-198">**Azure AD B2C - Kullanıcı akışları (ilkeler)** sayfasında, **Yeni Kullanıcı Akışı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-198">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="6a6eb-199">**Önerilen** sekmesinde **Profil düzenleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-199">On the **Recommended** tab, select **Profile editing**.</span></span>
1. <span data-ttu-id="6a6eb-200">**Ad** altında, profil düzenleme kullanıcı akışını girin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-200">Under **Name**, enter the profile editing user flow.</span></span> <span data-ttu-id="6a6eb-201">Bu ad, daha sonra portalın atadığı bir önekle (örneğin, "B2C_1_") birlikte görüntülenecektir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-201">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="6a6eb-202">**Kimlik sağlayıcılar** altında **Yerel Hesap Oturum Açma** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-202">Under **Identity providers**, select **Local Account SignIn**.</span></span>
1. <span data-ttu-id="6a6eb-203">**Kullanıcı öznitelikleri** altında, aşağıdaki onay kutularını seçin:</span><span class="sxs-lookup"><span data-stu-id="6a6eb-203">Under **User attributes**, select the following check boxes:</span></span>
    - <span data-ttu-id="6a6eb-204">**E-posta Adresleri** (yalnızca **İade talebi**)</span><span class="sxs-lookup"><span data-stu-id="6a6eb-204">**Email Addresses** (**Return claim** only)</span></span>
    - <span data-ttu-id="6a6eb-205">**Verilen Ad** (**Öznitelik topla** ve **İade talebi**)</span><span class="sxs-lookup"><span data-stu-id="6a6eb-205">**Given Name** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="6a6eb-206">**Kimlik Sağlayıcı** (yalnızca **İade talebi**)</span><span class="sxs-lookup"><span data-stu-id="6a6eb-206">**Identity Provider** (**Return claim** only)</span></span>
    - <span data-ttu-id="6a6eb-207">**Soyadı** (**Öznitelik topla** ve **İade talebi**)</span><span class="sxs-lookup"><span data-stu-id="6a6eb-207">**Surname** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="6a6eb-208">**Kullanıcı Nesne Kodu** (yalnızca **İade talebi**)</span><span class="sxs-lookup"><span data-stu-id="6a6eb-208">**User's Object ID** (**Return claim** only)</span></span>
1. <span data-ttu-id="6a6eb-209">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-209">Select **Create**.</span></span>

<span data-ttu-id="6a6eb-210">Aşağıdaki resimde, Azure AD B2C profili düzenleme kullanıcı akışı örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-210">The following image shows an example of the Azure AD B2C profile editing user flow.</span></span>

![Profil Düzenleme kullanıcı akışı oluşturma](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a><span data-ttu-id="6a6eb-212">Parola sıfırlama kullanıcı akışı ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="6a6eb-212">Create a password reset user flow policy</span></span>

<span data-ttu-id="6a6eb-213">Parola sıfırlama kullanıcı akışı ilkesi oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-213">To create a password reset user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="6a6eb-214">Azure portalında, sol gezinti bölmesinde **Kullanıcı akışları (ilkeler)** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-214">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="6a6eb-215">**Azure AD B2C - Kullanıcı akışları (ilkeler)** sayfasında, **Yeni Kullanıcı Akışı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-215">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="6a6eb-216">**Önerilen** sekmesinde **Parola Sıfırlama**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-216">On the **Recommended** tab, select **Password Reset**.</span></span>
1. <span data-ttu-id="6a6eb-217">**Ad** altında, parola sıfırlama kullanıcı akışı için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-217">Under **Name**, enter a name for the password reset user flow.</span></span>
1. <span data-ttu-id="6a6eb-218">**Kimlik sağlayıcılar** atında **E-posta adresini kullanarak parolayı sıfırla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-218">Under **Identity providers**, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="6a6eb-219">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-219">Select **Create**.</span></span>
1. <span data-ttu-id="6a6eb-220">**Uygulama talepleri** altında, aşağıdaki onay kutularını seçin:</span><span class="sxs-lookup"><span data-stu-id="6a6eb-220">Under **Application claims**, select the following check boxes:</span></span>
    - <span data-ttu-id="6a6eb-221">**E-posta adresleri**</span><span class="sxs-lookup"><span data-stu-id="6a6eb-221">**Email addresses**</span></span>
    - <span data-ttu-id="6a6eb-222">**Verilen Ad**</span><span class="sxs-lookup"><span data-stu-id="6a6eb-222">**Given Name**</span></span>
    - <span data-ttu-id="6a6eb-223">**Soyadı**</span><span class="sxs-lookup"><span data-stu-id="6a6eb-223">**Surname**</span></span>
    - <span data-ttu-id="6a6eb-224">**Kullanıcı Nesne kodu**</span><span class="sxs-lookup"><span data-stu-id="6a6eb-224">**User's Object ID**</span></span>
1. <span data-ttu-id="6a6eb-225">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-225">Select **Create**.</span></span>

<span data-ttu-id="6a6eb-226">Aşağıdaki resimde, Azure AD B2C parola sıfırlama kullanıcı akışında **Posta adresi kullanılarak parolayı sıfırla** ayarının nerede yapıldığı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-226">The following image shows where to set **Reset Password using mail address** in the Azure AD B2C password reset user flow.</span></span>

![Parola Sıfırlama ilkesinde "Posta adresini kullanarak Parolayı Sıfırla" ayarı](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a><span data-ttu-id="6a6eb-228">Sosyal kimlik sağlayıcıları ekleme (İsteğe bağlı)</span><span class="sxs-lookup"><span data-stu-id="6a6eb-228">Add social identity providers (Optional)</span></span>

<span data-ttu-id="6a6eb-229">Sosyal kimlik sağlayıcıları kullanıcıların kimlik doğrulama için sosyal hesaplarını kullanmalarına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-229">Social identity providers allow users to use their social accounts for authentication.</span></span> <span data-ttu-id="6a6eb-230">Sosyal kimlik sağlayıcı kimlik doğrulaması ekleme Dynamics 365 Commerce'ta isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-230">Adding social identity provider authentication is optional in Dynamics 365 Commerce.</span></span> 

<span data-ttu-id="6a6eb-231">Sosyal kimlik sağlayıcı kimlik doğrulaması eklenmezse, varsayılan Azure AD B2C profilleri kullanıcı tabanınızın ana profilleri olacaktır.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-231">If social identity provider authentication is not added, the default Azure AD B2C profiles will be the main profiles for your user base.</span></span> <span data-ttu-id="6a6eb-232">Kullanıcılar kendi kullanıcı adını (tercih ettikleri e-posta adresi) seçer ve bir parola ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-232">Users will select their own username (their preferred email address) and set a password.</span></span> <span data-ttu-id="6a6eb-233">Azure AD B2C, kullanıcıların kimliklerini doğrudan doğrular.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-233">Azure AD B2C will authenticate users directly.</span></span> 

<span data-ttu-id="6a6eb-234">Sosyal kimlik sağlayıcı kimlik doğrulaması eklenir ve kullanıcı sunulan sosyal kimlik sağlayıcılardan birini seçerse, Azure AD B2C kiracısında yine de bir varlık oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-234">If social identity provider authentication is added and a user chooses one of the social identity providers offered, an entity is still created in the Azure AD B2C tenant.</span></span> <span data-ttu-id="6a6eb-235">Azure AD B2C, kullanıcının kimlik bilgilerini sosyal kimlik sağlayıcıyla doğrulayacaktır.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-235">Azure AD B2C will then authenticate the user's credentials with the social identity provider.</span></span>

> [!NOTE]
> <span data-ttu-id="6a6eb-236">Kimlik sağlayıcı oturum açma işlemi B2C kiracısı içinde bir kayıt oluşturur ancak bu kayıt, kimlik doğrulama için harici sosyal kimlik sağlayıcı referansı çağıracağından yerel hesaplardan farklı bir biçimdedir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-236">The identity provider sign in creates a record in the B2C tenant, but in a different format than local accounts since it will call the external social identity provider reference for authentication.</span></span> <span data-ttu-id="6a6eb-237">Kullanıcı, sosyal kimlik sağlayıcılarında aynı e-posta adresini kullanabilir; bu, kimlik doğrulama için kullanılan e-posta kullanıcı adının kiracı için benzersiz olmayabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-237">The user can use the same email address across social identity providers, meaning that the email username used for authentication may not be unique to the tenant.</span></span> <span data-ttu-id="6a6eb-238">Azure AD B2C, yalnızca kullanıcıların yerel B2C hesaplarında benzersiz bir e-posta adresine sahip olmasını zorunlu kılar.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-238">Azure AD B2C will only enforce that users have a unique email address on local B2C accounts.</span></span>

<span data-ttu-id="6a6eb-239">Kimlik doğrulama için bir sosyal kimlik sağlayıcısı eklemeden önce, kimlik sağlayıcının portalına gitmeniz ve Azure AD B2C belgelerinde belirtildiği gibi bir kimlik sağlayıcı uygulaması ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-239">Before you can add a social identity provider for authentication, you must go to the identity provider's portal and set up an identity provider application as instructed in the Azure AD B2C documentation.</span></span> <span data-ttu-id="6a6eb-240">Belge bağlantılarının listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-240">A list of links to the documentation is provided below.</span></span>

- [<span data-ttu-id="6a6eb-241">Amazon</span><span class="sxs-lookup"><span data-stu-id="6a6eb-241">Amazon</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [<span data-ttu-id="6a6eb-242">Azure AD (Tek Kiracı)</span><span class="sxs-lookup"><span data-stu-id="6a6eb-242">Azure AD (Single Tenant)</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [<span data-ttu-id="6a6eb-243">Microsoft Hesabı</span><span class="sxs-lookup"><span data-stu-id="6a6eb-243">Microsoft Account</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [<span data-ttu-id="6a6eb-244">Facebook</span><span class="sxs-lookup"><span data-stu-id="6a6eb-244">Facebook</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [<span data-ttu-id="6a6eb-245">GitHub</span><span class="sxs-lookup"><span data-stu-id="6a6eb-245">GitHub</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [<span data-ttu-id="6a6eb-246">Google</span><span class="sxs-lookup"><span data-stu-id="6a6eb-246">Google</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [<span data-ttu-id="6a6eb-247">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="6a6eb-247">LinkedIn</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [<span data-ttu-id="6a6eb-248">OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="6a6eb-248">OpenID Connect</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [<span data-ttu-id="6a6eb-249">Twitter</span><span class="sxs-lookup"><span data-stu-id="6a6eb-249">Twitter</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a><span data-ttu-id="6a6eb-250">Sosyal kimlik sağlayıcı ekleme ve ayarlama</span><span class="sxs-lookup"><span data-stu-id="6a6eb-250">Add and set up a social identity provider</span></span>

<span data-ttu-id="6a6eb-251">Bir sosyal kimlik sağlayıcısı eklemek ve ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-251">To add and set up a social identity provider, follow these steps.</span></span>  

1. <span data-ttu-id="6a6eb-252">Azure portalında **Kimlik Sağlayıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-252">In the Azure portal, navigate to **Identity Providers**.</span></span>
1. <span data-ttu-id="6a6eb-253">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-253">Select **Add**.</span></span> <span data-ttu-id="6a6eb-254">**Kimlik sağlayıcı ekle** ekranı görünür.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-254">The **Add identity provider** screen appears.</span></span>
1. <span data-ttu-id="6a6eb-255">**Ad** altında, kullanıcılara oturum açma ekranında gösterilecek adı girin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-255">Under **Name**, enter the name to be displayed to users on your sign in screen.</span></span>
1. <span data-ttu-id="6a6eb-256">**Kimlik sağlayıcı türü** altında, listeden bir kimlik sağlayıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-256">Under **Identity provider type**, select an identity provider from the list.</span></span>
1. <span data-ttu-id="6a6eb-257">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-257">Select **OK**.</span></span>
1. <span data-ttu-id="6a6eb-258">**Sosyal kimlik sağlayıcı ayarla** ekranına erişmek için **Bu kimlik sağlayıcıyı ayarla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-258">Select **Set up this identity provider** to access the **Set up the social identity provider** screen.</span></span>
1. <span data-ttu-id="6a6eb-259">**İstemci Kimliği** altında, kimlik sağlayıcı uygulaması kurulumundan elde edilen istemci kimliğini girin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-259">Under **Client ID**, enter the client ID as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="6a6eb-260">**İstemci gizli anahtarı** altında, kimlik sağlayıcı uygulaması kurulumundan elde edilen istemci gizli anahtarını girin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-260">Under **Client secret**, enter the client secret as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="6a6eb-261">Kaydolma oturum açma ilkeleri için kullanıcı akışı ekleme:</span><span class="sxs-lookup"><span data-stu-id="6a6eb-261">Attach user flow for sign in sign up policies:</span></span>
1. <span data-ttu-id="6a6eb-262">**Azure AD B2C – Kullanıcı akışları (ilkeler) \> {oturum açma kayıt olma ilkeniz} \> Kimlik sağlayıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-262">Go to **Azure AD B2C – User flows (policies) \> {your sign-in sign-up policy} \> Identity providers**.</span></span>
1. <span data-ttu-id="6a6eb-263">Oturum aç/kaydol kullanıcı akışı ilkesini eklemek için, hesabınız için ayarladığınız her bir kimlik sağlayıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-263">To attach the sign in/sign up user flow policy, select each identity provider you have set up for your account.</span></span> <span data-ttu-id="6a6eb-264">Bunları test etmek amacıyla her bir kimlik sağlayıcısı için **Kullanıcı akışını çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-264">To test these, select **Run user flow** for each identity provider.</span></span> <span data-ttu-id="6a6eb-265">Yeni bir sekme, yeni kimlik sağlayıcı seçim kutusunu görüntüleyen oturum açma sayfasını görüntüleyecektir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-265">A new tab will display the sign-in page displaying the new identity provider selection box.</span></span>

<span data-ttu-id="6a6eb-266">Aşağıdaki resim, Azure AD B2C'deki **Kimlik sağlayıcı ekle** ve **Sosyal kimlik sağlayıcı ayarla** ekranlarının örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-266">The following image shows examples of the **Add identity provider** and **Set up the social identity provider** screens in Azure AD B2C.</span></span>

![Uygulamanıza bir Sosyal Kimlik Sağlayıcı ekleme](./media/B2CImage_14.png)

<span data-ttu-id="6a6eb-268">Aşağıdaki resimde, Azure AD B2C **Kimlik Sağlayıcıları** sayfasında kimlik sağlayıcılarının nasıl seçileceği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-268">The following image shows an example of how to select identity providers on the Azure AD B2C **Identity Providers** page.</span></span>

![İlkeniz için etkinleştirilecek her Sosyal Kimlik Sağlayıcıyı seçme](./media/B2CImage_16.png)

<span data-ttu-id="6a6eb-270">Aşağıdaki resimde, sosyal kimlik sağlayıcı oturum açma düğmesinin görüntülendiği varsayılan oturum açma ekranı örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-270">The following image shows an example of a default sign-in screen with a social identity provider sign-in button displayed.</span></span>

![Sosyal Kimlik Sağlayıcı oturum açma düğmesinin görüntülendiği varsayılan oturum açma ekranı örneği](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a><span data-ttu-id="6a6eb-272">Commerce Headquarters'ı yeni Azure AD B2C bilgileri ile güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="6a6eb-272">Update Commerce headquarters with the new Azure AD B2C information</span></span>

<span data-ttu-id="6a6eb-273">Yukarıdaki Azure AD B2C sağlama adımları tamamlandıktan sonra, Azure AD B2C uygulamasının Dynamics 365 Commerce ortamınıza kaydedilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-273">Once the Azure AD B2C provisioning steps above are completed, the Azure AD B2C application must be registered in your Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="6a6eb-274">Genel merkezi Azure AD B2C bilgileriyle güncelleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-274">To update headquarters with the new Azure AD B2C information, follow these steps.</span></span>

1. <span data-ttu-id="6a6eb-275">Commerce'ta **Commerce Paylaşılan Parametreleri**'ne gidin ve sol menüde **Kimlik Sağlayıcılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-275">In Commerce, go to **Commerce Shared Parameters** and select **Identity Providers** in the left menu.</span></span>
1. <span data-ttu-id="6a6eb-276">**Kimlik Sağlayıcılar** altında aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="6a6eb-276">Under **Identity Providers**, do the following:</span></span>
    1. <span data-ttu-id="6a6eb-277">**Veren** kutusuna, kimlik sağlayıcı verenin URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-277">In the **Issuer** box, enter the identity provider issuer URL.</span></span> <span data-ttu-id="6a6eb-278">Veren URL'nizi bulmak için, aşağıdaki [Verenin URL'sini al](#obtain-issuer-url) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-278">To find your issuer URL, see [Obtain issuer URL](#obtain-issuer-url) below.</span></span>
    1. <span data-ttu-id="6a6eb-279">**Ad** kutusuna, veren kaydınız için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-279">In the **Name** box, enter a name for your issuer record.</span></span>
    1. <span data-ttu-id="6a6eb-280">**Tür** kutusuna, **Azure AD B2C (id_token)** girin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-280">In the **Type** box, enter **Azure AD B2C (id_token)**.</span></span>
1. <span data-ttu-id="6a6eb-281">**Bağlı Olan Taraflar** altında, yukarıdaki B2C kimlik sağlayıcı öğesi seçiliyken aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="6a6eb-281">Under **Relying Parties**, with the above B2C identity provider item selected, do the following:</span></span>
    1. <span data-ttu-id="6a6eb-282">**İstemci Kimliği** kutusuna, B2C uygulama kimliğinizi girin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-282">In the **ClientID** box, enter your B2C application ID.</span></span> <span data-ttu-id="6a6eb-283">Bunu, B2C uygulamanızın özellikler sayfasındaki **Uygulama Kimliği** kutusunda bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-283">You can find this in the **Application ID** box of your B2C application's properties page.</span></span>
    1. <span data-ttu-id="6a6eb-284">**Tür** kutusuna **Genel** girin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-284">In the **Type** box, enter **Public**.</span></span>
    1. <span data-ttu-id="6a6eb-285">**Kullanıcı Türü** kutusuna **Müşteri** girin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-285">In the **User Type** box, enter **Customer**.</span></span>
1. <span data-ttu-id="6a6eb-286">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-286">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="6a6eb-287">Commerce arama kutusunda, **Dağıtım planı**'nı arayın</span><span class="sxs-lookup"><span data-stu-id="6a6eb-287">In the Commerce search box, search for **Distribution schedule**</span></span>
1. <span data-ttu-id="6a6eb-288">**Dağıtım planları** sayfasının sol gezinti menüsünde, **1110 Global yapılandırma** işini seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-288">In the left navigation menu of the **Distribution schedules** page, select job **1110 Global configuration**.</span></span>
1. <span data-ttu-id="6a6eb-289">Eylem bölmesinde **Şimdi Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-289">On the action pane, select **Run Now**.</span></span>

### <a name="obtain-issuer-url"></a><span data-ttu-id="6a6eb-290">Verenin URL'sini alma</span><span class="sxs-lookup"><span data-stu-id="6a6eb-290">Obtain issuer URL</span></span>

<span data-ttu-id="6a6eb-291">Kimlik sağlayıcı veren URL'nizi almak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-291">To obtain your identity provider issuer URL, follow these steps.</span></span>

1. <span data-ttu-id="6a6eb-292">B2C kiracınızı ve ilkenizi kullanarak aşağıdaki gibi bir meta veri adres URL'si oluşturun: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span><span class="sxs-lookup"><span data-stu-id="6a6eb-292">Create a metadata address URL in the following format using your B2C tenant and policy: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span></span>
    - <span data-ttu-id="6a6eb-293">Örnek: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-293">Example: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span></span>
1. <span data-ttu-id="6a6eb-294">Meta veri adresi URL'sini tarayıcının adres çubuğuna girin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-294">Enter the metadata address URL into a browser address bar.</span></span>
1. <span data-ttu-id="6a6eb-295">Meta verilerde, kimlik sağlayıcı veren URL'sini (**"veren"** değeri) kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-295">In the metadata, copy the identity provider issuer URL (the value for **"issuer"**).</span></span>
    - <span data-ttu-id="6a6eb-296">Örnek: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-296">Example: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span></span>

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a><span data-ttu-id="6a6eb-297">Commerce site oluşturucuda B2C kiracınızı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6a6eb-297">Configure your B2C tenant in Commerce site builder</span></span>

<span data-ttu-id="6a6eb-298">Azure AD B2C kiracısı kurulumu tamamlandıktan sonra, B2C kiracısını Commerce site oluşturucuda yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-298">Once setup of your Azure AD B2C tenant is completed, you must configure the B2C tenant in Commerce site builder.</span></span> <span data-ttu-id="6a6eb-299">Yapılandırma adımları Azure portalından B2C uygulama bilgilerinin toplanmasını, bu B2C uygulama bilgilerinin site oluşturucuya girilmesini ve daha sonra B2C uygulamasının sitenizle ve kanalınızla ilişkilendirilmesini içerir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-299">Configuration steps include collecting B2C application information from the Azure portal, entering that B2C application information into site builder, and then associating the B2C application with your site and channel.</span></span>

### <a name="collect-the-required-application-information"></a><span data-ttu-id="6a6eb-300">Gerekli uygulama bilgilerini toplama</span><span class="sxs-lookup"><span data-stu-id="6a6eb-300">Collect the required application information</span></span>

<span data-ttu-id="6a6eb-301">Gerekli uygulama bilgilerini toplamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-301">To collect the required application information, follow these steps.</span></span>

1. <span data-ttu-id="6a6eb-302">Azure portalında **Giriş \> Azure AD B2C - Uygulamalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-302">In the Azure portal, go to **Home \> Azure AD B2C - Applications**.</span></span>
1. <span data-ttu-id="6a6eb-303">Uygulamanızı seçin ve sonra sol gezinti bölmesinde uygulama ayrıntılarını elde etmek için **Özellikler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-303">Select your application, and then in the left navigation pane select **Properties** to obtain the application details.</span></span>
1. <span data-ttu-id="6a6eb-304">**Uygulama kimliği** kutusunda, B2C kiracınızda oluşturulan B2C uygulamasının uygulama kodunu toplayın.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-304">From the **Application ID** box, collect the application ID of the B2C application created in your B2C tenant.</span></span> <span data-ttu-id="6a6eb-305">Bu, daha sonra site oluşturucuda **İstemci GUID**'i olarak girilir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-305">This will later be entered as the **Client GUID** in site builder.</span></span>
1. <span data-ttu-id="6a6eb-306">**Yanıt URL'si** altından, yanıt URL'sini alın.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-306">Under **Reply URL**, collect the reply URL.</span></span>
1. <span data-ttu-id="6a6eb-307">**Giriş \> Azure AD B2C – Kullanıcı akışları (ilkeler)** öğesine gidin ve her kullanıcı akışı ilkesinin adını toplayın.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-307">Go to **Home \> Azure AD B2C – User flows (policies)**, and then collect the names of each user flow policy.</span></span>

<span data-ttu-id="6a6eb-308">Aşağıdaki resim **Azure AD B2C - Uygulamalar** sayfasının bir örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-308">The following image shows an example of the **Azure AD B2C - Applications** page.</span></span>

![Kiracınız içinde B2C Uygulamasına gitme](./media/B2CImage_19.png)

<span data-ttu-id="6a6eb-310">Aşağıdaki resim Azure AD B2C'deki uygulamanın **Özellikler** sayfasının bir örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-310">The following image shows an example of an application **Properties** page in Azure AD B2C.</span></span> 

![B2C Uygulamasının Özelliklerinden Uygulama Kodunu Kopyalama](./media/B2CImage_21.png)

<span data-ttu-id="6a6eb-312">Aşağıdaki resimde, **Azure AD B2C - Kullanıcı akışları (ilkeler)** sayfasındaki kullanıcı akış ilkelerinin bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-312">The following image shows an example of user flow policies on the **Azure AD B2C – User flows (policies)** page.</span></span>

![Her B2C ilke akışının adını toplama](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a><span data-ttu-id="6a6eb-314">AAD B2C kiracısı uygulama bilgilerinizi Commerce'a girme</span><span class="sxs-lookup"><span data-stu-id="6a6eb-314">Enter your AAD B2C tenant application information into Commerce</span></span>

<span data-ttu-id="6a6eb-315">B2C kiracısını sitelerinizle ilişkilendirmeden önce, Azure AD B2C kiracısı ayrıntılarını Commerce site oluşturucusuna girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-315">You must enter details of the Azure AD B2C tenant into Commerce site builder before associating the B2C tenant with your site(s).</span></span>

<span data-ttu-id="6a6eb-316">AAD B2C kiracısı uygulama bilgilerinizi Commerce'a eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-316">To add your AAD B2C tenant application information to Commerce, follow these steps.</span></span>

1. <span data-ttu-id="6a6eb-317">Ortamınız için Commerce site oluşturucuda yönetici olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-317">Sign in as an administrator to Commerce site builder for your environment.</span></span>
1. <span data-ttu-id="6a6eb-318">Sol gezinti bölmesinde, genişletmek için **Kiracı Ayarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-318">In the left navigation pane, select **Tenant Settings**  to expand it.</span></span>
1. <span data-ttu-id="6a6eb-319">**Kiracı Ayarları** altında **B2C Ayarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-319">Under **Tenant Settings**, select **B2C Settings**.</span></span> 
1. <span data-ttu-id="6a6eb-320">Ana pencerede **B2C Uygulamaları**'nın yanındaki **Yönet** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-320">In the main window next **B2C Applications**, select **Manage**.</span></span> <span data-ttu-id="6a6eb-321">(Kiracınız B2C Uygulamaları listesinde görüntüleniyorsa, daha önce bir yönetici tarafından eklenmiş demektir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-321">(If your tenant appears in the B2C Applications list, then it was already added by an administrator.</span></span> <span data-ttu-id="6a6eb-322">Aşağıdaki adım 6'da belirtilen öğelerin B2C Uygulamanız ile eşleştiğini doğrulayın.)</span><span class="sxs-lookup"><span data-stu-id="6a6eb-322">Verify that the items in step 6 below match your B2C Application.)</span></span>
1. <span data-ttu-id="6a6eb-323">**B2C Uygulaması Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-323">Select **Add B2C Application**.</span></span>
1. <span data-ttu-id="6a6eb-324">B2C kiracısı ve uygulamanızın değerlerini kullanarak, aşağıdaki gerekli maddeleri görüntülenen forma girin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-324">Enter the following required items in the form displayed, using values from your B2C tenant and application.</span></span> <span data-ttu-id="6a6eb-325">Gerekli olmayan alanlar (yıldız işareti olmayan alanlar) boş bırakılabilir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-325">Fields that are not required (those without an asterisk) may be left blank.</span></span>

    - <span data-ttu-id="6a6eb-326">**Uygulama Adı**: B2C Uygulamanızın adı, örneğin "Fabrikam B2C".</span><span class="sxs-lookup"><span data-stu-id="6a6eb-326">**Application Name**: The name for your B2C Application, for example "Fabrikam B2C".</span></span>
    - <span data-ttu-id="6a6eb-327">**Kiracı Adı**: B2C kiracısı adı (örneğin, etki alanı B2C kiracısı için "fabrikam.onmicrosoft.com" olarak görünüyorsa "Fabrikam" kullanın).</span><span class="sxs-lookup"><span data-stu-id="6a6eb-327">**Tenant Name**: The name of your B2C tenant (for example, use "fabrikam" if the domain appears as "fabrikam.onmicrosoft.com" for the B2C tenant).</span></span> 
    - <span data-ttu-id="6a6eb-328">**Parola Unutma İlkesi Kimliği**: Parolayı unutma kullanıcı akışı ilke kimliği, örneğin "B2C_1_PasswordReset".</span><span class="sxs-lookup"><span data-stu-id="6a6eb-328">**Forget Password Policy ID**: The forget password user flow policy ID, for example "B2C_1_PasswordReset".</span></span>
    - <span data-ttu-id="6a6eb-329">**Kaydolma Oturum Açma İlkesi Kimliği**: Kullanıcı akış ilkesi kayıt olma ve oturum açma kimliği, örneğin "B2C_1_signup_signin".</span><span class="sxs-lookup"><span data-stu-id="6a6eb-329">**Signup Signin Policy ID**: The sign up and sign in user flow policy ID, for example "B2C_1_signup_signin".</span></span>
    - <span data-ttu-id="6a6eb-330">**İstemci GUID'i**: B2C uygulama kimliği, örneğin "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span><span class="sxs-lookup"><span data-stu-id="6a6eb-330">**Client GUID**: The B2C application ID, for example "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span></span>
    - <span data-ttu-id="6a6eb-331">**Profil Düzenle İlkesi Kimliği**: Profil düzenleme kullanıcı akışı ilkesi kimliği, örneğin "B2C_1A_ProfileEdit".</span><span class="sxs-lookup"><span data-stu-id="6a6eb-331">**Edit Profile Policy ID**: The profile editing user flow policy ID, for example "B2C_1A_ProfileEdit".</span></span>

1. <span data-ttu-id="6a6eb-332">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-332">Select **OK**.</span></span> <span data-ttu-id="6a6eb-333">Şimdi, B2C uygulamanızın adının listede yer aldığını görmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-333">You should now see the name of your B2C application appear in the list.</span></span>
1. <span data-ttu-id="6a6eb-334">Değişikliklerinizi kaydetmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-334">Select **Save** to save your changes.</span></span>

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a><span data-ttu-id="6a6eb-335">B2C uygulamasını sitenizle ve kanalınızla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="6a6eb-335">Associate the B2C application to your site and channel</span></span>

> [!WARNING]
> <span data-ttu-id="6a6eb-336">Siteniz zaten bir B2C uygulamasıyla ilişkilendirilmişse, farklı bir B2C uygulamasına geçmek, bu ortamda zaten kaydolan kullanıcılar için kurulmuş olan geçerli referansları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-336">If your site is already associated with a B2C application, changing to a different B2C application will remove the current references established for users already signed up in this environment.</span></span> <span data-ttu-id="6a6eb-337">Değiştirilmesi durumunda, geçerli olarak atanmış olan B2C uygulamasıyla ilişkilendirilmiş kimlik bilgileri kullanıcılar tarafından kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-337">If changed, any credentials associated with the currently-assigned B2C application will not be available to users.</span></span> 
> 
> <span data-ttu-id="6a6eb-338">Yalnızca kanalın B2C uygulamasını ilk kez ayarlıyorsanız veya kullanıcıların yeni B2C uygulamasıyla bu kanala yönelik yeni kimlik bilgileriyle yeniden kaydolmasını istiyorsanız, B2C uygulamasını güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-338">Only update the B2C application if you are setting up the channel's B2C application for the first time or if you intend to have users re-sign up with new credentials to this channel with the new B2C application.</span></span> <span data-ttu-id="6a6eb-339">Kanalları B2C uygulamalarıyla ilişkilendirilirken dikkatli olun ve uygulamaları açık şekilde adlandırın.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-339">Take caution when associating channels to B2C applications, and name applications clearly.</span></span> <span data-ttu-id="6a6eb-340">Bir kanal aşağıdaki adımlarda bir B2C uygulamasıyla ilişkilendirilmezse, siteniz için o kanalda oturum açan kullanıcılar, B2C uygulamalarının **Kiracı \> B2C Ayarları** listesinde **varsayılan** olarak gösterilen B2C uygulamasına girecektir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-340">If a channel is not associated to a B2C application in the steps below, users signing into that channel for your site will be entered into the B2C application showing as **default** in the **Tenant Settings \> B2C Settings** list of B2C applications.</span></span>

<span data-ttu-id="6a6eb-341">B2C uygulamasını sitenizle ve kanalınızla ilişkilendirmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-341">To associate the B2C application to your site and channel, follow these steps.</span></span>

1. <span data-ttu-id="6a6eb-342">Commerce site oluşturucuda sitenize gidin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-342">Navigate to your site in Commerce site builder.</span></span>
1. <span data-ttu-id="6a6eb-343">Sol gezinti bölmesinde, genişletmek için **Site Ayarları** seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-343">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="6a6eb-344">**Site Ayarları** altında, **Kanallar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-344">Below **Site Settings**, select **Channels**.</span></span>
1. <span data-ttu-id="6a6eb-345">**Kanallar** altındaki ana pencerede kanalı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-345">In the main window under **Channels**, select your channel.</span></span>
1. <span data-ttu-id="6a6eb-346">Sağdaki kanal özellikleri bölmesinde, **B2C Uygulaması Seç** açılır menüsünden B2C uygulamanızın adını seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-346">In the channel properties pane on the right, select your B2C application name from the **Select B2C Application** drop down menu.</span></span>
1. <span data-ttu-id="6a6eb-347">**Kapat**'ı ve ardından **Kaydet ve Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-347">Select **Close**, and then select **Save and Publish**.</span></span>

## <a name="additional-b2c-information"></a><span data-ttu-id="6a6eb-348">Ek B2C bilgileri</span><span class="sxs-lookup"><span data-stu-id="6a6eb-348">Additional B2C information</span></span>

### <a name="customer-migration"></a><span data-ttu-id="6a6eb-349">Müşteri geçişi</span><span class="sxs-lookup"><span data-stu-id="6a6eb-349">Customer migration</span></span>

<span data-ttu-id="6a6eb-350">Müşteri kayıtlarını önceki bir kimlik sağlayıcı platformundan geçirmeyi düşünüyorsanız, lütfen müşteri geçiş gereksinimlerinizi gözden geçirmek için Dynamics 365 Commerce ekibiyle birlikte çalışın.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-350">If you are considering migrating customer records from a previous identity provider platform, please work with the Dynamics 365 Commerce team to review your customer migration needs.</span></span>

<span data-ttu-id="6a6eb-351">Müşteri geçisindeki ek Azure AD B2C belgeleri için bkz. [Kullanıcıları Azure Active Directory B2C'ye geçirme](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span><span class="sxs-lookup"><span data-stu-id="6a6eb-351">For additional Azure AD B2C documentation on customer migration, see [Migrate users to Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span></span>

### <a name="custom-policies"></a><span data-ttu-id="6a6eb-352">Özel ilkeler</span><span class="sxs-lookup"><span data-stu-id="6a6eb-352">Custom policies</span></span>

<span data-ttu-id="6a6eb-353">Azure AD B2C etkileşimlerini ve ilke akışlarını standart B2C ilkeleriyle sunulandan daha fazla özelleştirme hakkında ek bilgi için bkz. [Azure Active Directory'deki özel ilkeler](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span><span class="sxs-lookup"><span data-stu-id="6a6eb-353">For additional information regarding customizing Azure AD B2C interactions and policy flows beyond what is offered by B2C standard policies, see [Custom policies in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span></span> 

### <a name="secondary-admin"></a><span data-ttu-id="6a6eb-354">İkincil yönetici</span><span class="sxs-lookup"><span data-stu-id="6a6eb-354">Secondary admin</span></span>

<span data-ttu-id="6a6eb-355">B2C kiracınızın **Kullanıcılar** bölümünde isteğe bağlı, ikincil bir yönetici hesabı eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-355">An optional, secondary administrator account can be added in the **Users** section of your B2C tenant.</span></span> <span data-ttu-id="6a6eb-356">Bu doğrudan bir hesap veya genel bir hesap olabilir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-356">This can be a direct account or a general account.</span></span> <span data-ttu-id="6a6eb-357">Bir hesabı ekip kaynakları arasında paylaşmanız gerekirse, ortak hesap da oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-357">If you need to share an account across team resources, a common account can also be created.</span></span> <span data-ttu-id="6a6eb-358">Azure AD B2C'de depolanan verilerin hassasiyeti nedeniyle, ortak hesabın şirketinizin güvenlik uygulamalarıyla yakından izlenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="6a6eb-358">Due to the sensitivity of the data stored in Azure AD B2C, a common account should be monitored closely per your company's security practices.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6a6eb-359">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="6a6eb-359">Additional resources</span></span>

[<span data-ttu-id="6a6eb-360">Etki alanı adınızı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6a6eb-360">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="6a6eb-361">Yeni bir e-ticaret kiracısını dağıtma</span><span class="sxs-lookup"><span data-stu-id="6a6eb-361">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="6a6eb-362">E-ticaret sitesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="6a6eb-362">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="6a6eb-363">Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="6a6eb-363">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="6a6eb-364">robots.txt dosyalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="6a6eb-364">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

<span data-ttu-id="6a6eb-365">[URL yeniden yönlendirmelerini toplu olarak yükle](upload-bulk-redirects.md)Dynamics 365 Commerce siteyi çevrimiçi kanalla ilişkilendir</span><span class="sxs-lookup"><span data-stu-id="6a6eb-365">[Upload URL redirects in bulk](upload-bulk-redirects.md)Associate a Dynamics 365 Commerce site with an online channel</span></span>

[<span data-ttu-id="6a6eb-366">Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama</span><span class="sxs-lookup"><span data-stu-id="6a6eb-366">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="6a6eb-367">Commerce ortamında birden fazla B2C kiracısı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6a6eb-367">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="6a6eb-368">İçerik teslim ağı (CDN) için destek ekleme</span><span class="sxs-lookup"><span data-stu-id="6a6eb-368">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="6a6eb-369">Konum tabanlı mağaza algılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="6a6eb-369">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

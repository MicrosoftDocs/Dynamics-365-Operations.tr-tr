---
title: Commerce ortamında birden fazla B2C kiracısı yapılandırma
description: Bu konu, özel bir Dynamics 365 Commerce ortamında kullanıcı kimlik doğrulaması için kanal başına birden çok Microsoft Azure Active Directory (Azure AD) İşletme-Müşteri Arası (B2C) kiracısının ne zaman ve nasıl ayarlanacağını açıklamaktadır.
author: BrianShook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: c813adb79ae1b78a052332e077393f125830633f
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027734"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a><span data-ttu-id="0b0a5-103">Commerce ortamında birden fazla B2C kiracısı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="0b0a5-103">Configure multiple B2C tenants in a Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0b0a5-104">Bu konu, özel bir Dynamics 365 Commerce ortamında kullanıcı kimlik doğrulaması için kanal başına birden çok Microsoft Azure Active Directory (Azure AD) işletme-müşteri arası (B2C) kiracısının ne zaman ve nasıl ayarlanacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-104">This topic describes when and how to set up multiple Microsoft Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants per channel for user authentication in a dedicated Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="0b0a5-105">Dynamics 365 Commerce, kullanıcı kimlik bilgileri ve kimlik doğrulama akışlarını desteklemek için Azure AD B2C bulut kimliği hizmetini kullanır.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-105">Dynamics 365 Commerce uses the Azure AD B2C cloud identity service to support user credentials and authentication flows.</span></span> <span data-ttu-id="0b0a5-106">Kullanıcılar parolalarını kaydetmek, oturum açmak ve sıfırlamak için kimlik doğrulama akışlarını kullanabilirler.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-106">Users can use the authentication flows to sign up, sign in, and reset their password.</span></span> <span data-ttu-id="0b0a5-107">Azure AD B2C kullanıcının hassas kimlik doğrulama bilgilerini (örneğin, kullanıcı adı ve parola) depolar.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-107">Azure AD B2C stores a user's sensitive authentication information, such as the user name and password.</span></span> <span data-ttu-id="0b0a5-108">Kullanıcı kaydı her B2C kiracısı için benzersizdir ve kullanıcı adı (e-posta adresi) kimlik bilgileri ya da sosyal kimlik sağlayıcısı kimlik bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-108">The user record is unique to each B2C tenant, and it uses either user name (email address) credentials or social identity provider credentials.</span></span>

<span data-ttu-id="0b0a5-109">Çoğu durumda, bir Commerce ortamında tek bir Azure AD B2C kiracısı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-109">In most cases, a single Azure AD B2C tenant is used in a Commerce environment.</span></span> <span data-ttu-id="0b0a5-110">Böylece Commerce müşterileri aynı Commerce ortamında birden çok site oluşturabilir ve yayımlayabilir ve aynı müşteri kimlik bilgileri bu sitelerde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-110">Commerce customers can then create and publish multiple sites in the same Commerce environment, and the same customer credentials will be used across these sites.</span></span> <span data-ttu-id="0b0a5-111">Ancak, ortamdaki sitelerin farklı markalar olarak değerlendirilmesi ve kullanıcılara ayrı işletmeler halinde görünmesi gerekiyorsa, site/marka ayrımı için kullanılan kanal için bir B2C kiracısı yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-111">However, if the sites in the environment should be treated as different brands and appear to users as separate businesses, a B2C tenant can be configured for the channel that is used for the site/brand separation.</span></span>

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a><span data-ttu-id="0b0a5-112">Kanal başına birden çok B2C kiracısı ayarlarken dikkate alınması gereken noktalar</span><span class="sxs-lookup"><span data-stu-id="0b0a5-112">Considerations when multiple B2C tenants are set up per channel</span></span>

<span data-ttu-id="0b0a5-113">Genellikle, her bir kanal veya site ayrı bir işletme ele alındığında, Commerce'taki Kullanıcı kimlik doğrulaması akışlarına göre en iyi seçenek, ayrı tüzel kişilikler kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-113">Often, when each channel or site is being treated as a separate business, the best option with respect to user authentication flows in Commerce is to use separate legal entities.</span></span> <span data-ttu-id="0b0a5-114">Ancak, her bir kanalı/siteyi aynı ortam ve tüzel kişilik içinde tutmak ama her bir site için ayrı kullanıcı kimlik doğrulaması olmasını istiyorsanız, devam etmeden önce aşağıdaki noktaları göz önünde bulundurmanız önemlidir:</span><span class="sxs-lookup"><span data-stu-id="0b0a5-114">However, if you want to keep each channel/site in the same environment and legal entity, but want to have separate user authentication for each site, it's important that you consider the following points before you proceed:</span></span>

- <span data-ttu-id="0b0a5-115">Kullanıcıların her bir kanal/site için kendi farklı kimlik bilgileri olacaktır.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-115">Users will have their own distinct credentials for each channel/site.</span></span>

    <span data-ttu-id="0b0a5-116">Her hesap ayrı bir B2C kiracısında benzersiz bir giriş olacağından, aynı kişinin kanal/site başına iki ayrı hesabı olabilir.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-116">The same person can have two separate accounts per channel/site, because each account will be a unique entry into a separate B2C tenant.</span></span>

- <span data-ttu-id="0b0a5-117">Microsoft Dynamics ortamında, genel kayıt aramaları için ayrı müşteri kayıtları döndürülür.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-117">In the Microsoft Dynamics environment, separate customer records will be returned for global record searches.</span></span>

    <span data-ttu-id="0b0a5-118">Bir kullanıcı kanallar/siteler arasında aynı e-posta adresini kullanırsa, genel müşteri aramaları her bir kanal/site için sonuçları döndürür.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-118">If a user uses the same email address across channels/sites, global customer searches will return results for each channel/site.</span></span> <span data-ttu-id="0b0a5-119">(Bir kanal göstergesi gösterilecektir.)</span><span class="sxs-lookup"><span data-stu-id="0b0a5-119">(A channel indicator will be shown.)</span></span>

- <span data-ttu-id="0b0a5-120">Adres defteri, kullanıcıları her kanal için izlemek amacıyla kullanıcıları gruplamaya yardımcı olmak üzere kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-120">The address book can be used to help group users, so that they can be tracked per channel.</span></span>
- <span data-ttu-id="0b0a5-121">Kanal başına müşteri kaydı sayısı artabilir ve bu artış genel müşteri aramalarının performansını etkileyebilir.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-121">The number of customer records per channel might increase, and this increase might affect the performance of global customer searches.</span></span>
- <span data-ttu-id="0b0a5-122">B2C kiracıları, müşterilerin yanlış bir kiracıya kaydolması durumunu engellenmeye yardımcı olmak amacıyla bir kanalla dikkatli şekilde eşlenmelidir.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-122">B2C tenants must be carefully mapped to a channel, to help prevent situations where customers sign up for an incorrect tenant.</span></span> <span data-ttu-id="0b0a5-123">Aksi durumda, karışıklık veya izleme sorunları oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-123">Otherwise, confusion or tracking issues can occur.</span></span>

<span data-ttu-id="0b0a5-124">Aşağıdaki örnekte bir Commerce ortamındaki birden fazla B2C kiracısı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-124">The following illustration shows multiple B2C tenants in a Commerce environment.</span></span>

![Commerce ortamındaki birden fazla B2C kiracısı](media/MultiB2C_In_Environment.png)

<span data-ttu-id="0b0a5-126">İşletmeniz için aynı Commerce ortamında kanal başına farklı B2C kiracıları gerektiğine karar verirseniz, bu özelliği istemek için aşağıdaki bölümlerdeki yordamları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-126">If you decide that your business requires distinct B2C tenants per channel in the same Commerce environment, complete the procedures in the following sections to request this feature.</span></span>

## <a name="configure-b2c-tenants-in-your-environment"></a><span data-ttu-id="0b0a5-127">Ortamınızdaki B2C kiracıları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="0b0a5-127">Configure B2C tenants in your environment</span></span>

<span data-ttu-id="0b0a5-128">Ortamınızda B2C kiracıları yapılandırmak için, bu bölümdeki ilgili yordamları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-128">To configure B2C tenants in your environment, complete the relevant procedures in this section.</span></span>

### <a name="add-an-azure-ad-b2c-tenant"></a><span data-ttu-id="0b0a5-129">Azure AD B2C kiracısı ekleme</span><span class="sxs-lookup"><span data-stu-id="0b0a5-129">Add an Azure AD B2C tenant</span></span>

<span data-ttu-id="0b0a5-130">Ortamınıza bir Azure AD B2C kiracısı eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-130">To add an Azure AD B2C tenant to your environment, follow these steps.</span></span>

1. <span data-ttu-id="0b0a5-131">Bir sistem yöneticisi olarak ortamınız için Commerce site oluşturucuda oturum açın. Azure AD B2C kiracıları yapılandırmak için Commerce ortamınızda sistem yöneticisi olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-131">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="0b0a5-132">Sol gezinti bölmesinde, genişletmek için **Kiracı Ayarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-132">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="0b0a5-133">**B2C Ayarları**'nı ve daha sonra **Yönet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-133">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="0b0a5-134">**B2C Uygulaması Ekle**'yi seçin ve aşağıdaki bilgileri girin:</span><span class="sxs-lookup"><span data-stu-id="0b0a5-134">Select **Add B2C Application**, and then enter the following information:</span></span>

    - <span data-ttu-id="0b0a5-135">**Uygulama Adı**: Commerce'ta yönetme bağlamında uygulama için kullanılacak adı girin.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-135">**Application Name**: Enter the name that should be used for the application in the context of managing it in Commerce.</span></span> <span data-ttu-id="0b0a5-136">Azure portalında Azure AD B2C uygulamasını kurarken seçtiğiniz uygulama adını kullanmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-136">We recommend that you use the application name that you chose when you set up the Azure AD B2C application in the Azure portal.</span></span> <span data-ttu-id="0b0a5-137">Böylece, Commerce'ta B2C kiracıları yönetirken karışıklığı azaltabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-137">In this way, you can help reduce confusion when you manage B2C tenants in Commerce.</span></span>
    - <span data-ttu-id="0b0a5-138">**Kiracı Adı**: B2C kiracısı adını Azure portalında göründüğü şekliyle girin.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-138">**Tenant Name**: Enter the B2C tenant name as it appears in the Azure portal.</span></span>
    - <span data-ttu-id="0b0a5-139">**Parolayı Unut İlke Kimliği**: İlke kimliğini (Azure portalındaki ilkenin adı) girin.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-139">**Forget Password Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="0b0a5-140">**Kaydol Oturum Aç İlke Kimliği**: İlke kimliğini (Azure portalındaki ilkenin adı) girin.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-140">**Signup Signin Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="0b0a5-141">**İstemci GUID'i**: Azure AD B2C kiracısı kimliğini Azure portalında göründüğü şekliyle girin (B2C kiracısı için uygulama kimliği değil).</span><span class="sxs-lookup"><span data-stu-id="0b0a5-141">**Client GUID**: Enter the Azure AD B2C tenant ID as it appears in the Azure portal (not the application ID for the B2C tenant).</span></span>
    - <span data-ttu-id="0b0a5-142">**Profili Düzenle İlke Kimliği**: İlke kimliğini (Azure portalındaki ilkenin adı) girin.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-142">**Edit Profile Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>

1. <span data-ttu-id="0b0a5-143">Bu bilgileri girmeyi bitirdiğinizde, değişikliklerinizi kaydetmek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-143">When you've finished entering this information, select **OK** to save your changes.</span></span> <span data-ttu-id="0b0a5-144">Yeni Azure AD B2C kiracınız şimdi **B2C uygulamalarını yönet** altındaki listede görünmelidir.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-144">Your new Azure AD B2C tenant should now appear in the list under **Manage B2C Applications**.</span></span>

> [!NOTE]
> <span data-ttu-id="0b0a5-145">Dynamics 365 Commerce takım bunları ayarlamanızı istemedikçe **Kapsam**, **Etkileşimli olmayan ilke kodu**, **Etkileşimli olmayan istemci kodu**, **Oturum açma özel etki alanı** ve **Kayıt ilkesi Kodu** alanlarını boş bırakmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-145">You should leave fields such as **Scope**, **Non Interactive Policy ID**, **Non Interactive Client ID**, **Login Custom Domain**, and **Sign Up Policy ID** blank unless the Dynamics 365 Commerce team instructs you to set them.</span></span>


### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a><span data-ttu-id="0b0a5-146">Azure AD B2C kiracısını yönetme veya silme</span><span class="sxs-lookup"><span data-stu-id="0b0a5-146">Manage or delete an Azure AD B2C tenant</span></span>

1. <span data-ttu-id="0b0a5-147">Bir sistem yöneticisi olarak ortamınız için Commerce site oluşturucuda oturum açın. Azure AD B2C kiracıları yapılandırmak için Commerce ortamınızda sistem yöneticisi olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-147">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="0b0a5-148">Sol gezinti bölmesinde, genişletmek için **Kiracı Ayarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-148">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="0b0a5-149">**B2C Ayarları**'nı ve daha sonra **Yönet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-149">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="0b0a5-150">B2C kiracısını düzenlemek için yanındaki kalem simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-150">To edit a B2C tenant, select the pencil symbol next to it.</span></span> <span data-ttu-id="0b0a5-151">B2C kiracısını silmek için, yanındaki çöp tenekesi simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-151">To delete a B2C tenant, select the trash can symbol next to it.</span></span>
1. <span data-ttu-id="0b0a5-152">**Kaydet**'i ve sonra değişikliklerinizi etkinleştirmek için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-152">Select **Save**, and then select **Publish** to activate your changes.</span></span>

> [!WARNING]
> <span data-ttu-id="0b0a5-153">Bir B2C kiracısı canlı/yayımlanmış bir site için yapılandırıldığında, kullanıcılar kiracıda bulunan hesapları kullanarak oturum açabilirler.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-153">When a B2C tenant is configured for a live/published site, users might have signed up by using accounts that are present on the tenant.</span></span> <span data-ttu-id="0b0a5-154">**Kiracı Ayarları \> B2C Kiracısı** menüsünde yapılandırılmış bir kiracıyı silerseniz, bu B2C kiracısının ilişkisini, kiracının kanallarıyla ilişkilendirilmiş olan sitelerden kaldırırsınız.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-154">If you delete a configured tenant on the **Tenant Settings \> B2C Tenant** menu, you remove the association of that B2C tenant from sites that are associated with any channels of the tenant.</span></span> <span data-ttu-id="0b0a5-155">Bu durumda, kullanıcılarınız hesaplarında artık oturum açamayabilirler.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-155">In this case, your users might no longer be able to sign in to their accounts.</span></span> <span data-ttu-id="0b0a5-156">Bu nedenle, yapılandırılmış bir kiracıyı silerken çok dikkatli olun.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-156">Therefore, use extreme caution when you delete a configured tenant.</span></span>
>
> <span data-ttu-id="0b0a5-157">Yapılandırılmış bir kiracı silindiğinde, B2C kiracısı ve kayıtları korunmaya devam eder, ancak bu kiracının Commerce sistem yapılandırması değiştirilir veya kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-157">When a configured tenant is deleted, the B2C tenant and records will continue to be maintained, but the Commerce system configuration of that tenant will be changed or removed.</span></span> <span data-ttu-id="0b0a5-158">Siteye kaydolmaya veya sitede oturum açmaya çalışan kullanıcılar, varsayılan veya sitenin kanalı için yapılandırılan yeni ilişkili B2C kiracısında yeni bir firma kaydı oluşturacaktır.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-158">Users who try to sign up or sign in to the site will create a new account record in the default or newly associated B2C tenant that is configured for the channel of the site.</span></span>

## <a name="configure-your-channel-with-a-b2c-tenant"></a><span data-ttu-id="0b0a5-159">Kanalınızı bir B2C kiracısı ile yapılandırma</span><span class="sxs-lookup"><span data-stu-id="0b0a5-159">Configure your channel with a B2C tenant</span></span>

1. <span data-ttu-id="0b0a5-160">Bir sistem yöneticisi olarak ortamınız için Commerce site oluşturucuda oturum açın. Azure AD B2C kiracıları yapılandırmak için Commerce ortamınızda sistem yöneticisi olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-160">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="0b0a5-161">Sol gezinti bölmesinde, genişletmek için **Site Ayarları** seçin.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-161">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="0b0a5-162">**Kanallar**'ı seçin ve sonra yapılandırılacak kanalı seçin.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-162">Select **Channels**, and then select the channel to configure.</span></span>
1. <span data-ttu-id="0b0a5-163">Sağdaki özellikler bölmesinde, **B2C Uygulaması Seç** alanında, bu kanal için kullanılacak yapılandırılmış Azure AD B2C kiracısını seçin.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-163">In the properties pane on the right, in the **Select B2C Application** field, select the configured Azure AD B2C tenant to use for this channel.</span></span>
1. <span data-ttu-id="0b0a5-164">Yeni veya güncelleştirilmiş yapılandırmayı uygulamak için komut çubuğunda **Kaydet ve Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-164">On the command bar, select **Save and Publish** to commit the new or updated configuration.</span></span>

> [!WARNING]
> <span data-ttu-id="0b0a5-165">Kanala atanmış B2C uygulamasını değiştirirseniz, ortamda zaten kaydolmuş olan tüm kullanıcılar için kurulmuş olan geçerli başvuruları kaldırırsınız.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-165">If you change the B2C application that is assigned to the channel, you remove the current references that have been established for any users who have already signed up in the environment.</span></span> <span data-ttu-id="0b0a5-166">Bu durumda, geçerli olarak atanmış olan B2C uygulamasıyla ilişkilendirilmiş kimlik bilgileri kullanıcılar tarafından kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-166">In this case, any credentials that are associated with the currently assigned B2C application won't be available to users.</span></span> <span data-ttu-id="0b0a5-167">Bu nedenle, yalnızca kanalı ilk kez ayarlıyorsanız kanal Azure AD B2C yapılandırmasını değiştirin; hiçbir kullanıcı oturum açamayacaktır.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-167">Therefore, change a channel Azure AD B2C configuration only if you're setting up the channel for the first time, and no users have been able to sign up.</span></span> <span data-ttu-id="0b0a5-168">Aksi durumda, kullanıcıların yeni Azure AD B2C kiracısında bir kayıt oluşturmak için yeniden kaydolması gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="0b0a5-168">Otherwise, users might have to sign up again to establish a record in the new Azure AD B2C tenant.</span></span>
## <a name="additional-resources"></a><span data-ttu-id="0b0a5-169">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0b0a5-169">Additional resources</span></span>

[<span data-ttu-id="0b0a5-170">Etki alanı adınızı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="0b0a5-170">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="0b0a5-171">Yeni bir e-ticaret kiracısını dağıtma</span><span class="sxs-lookup"><span data-stu-id="0b0a5-171">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="0b0a5-172">E-ticaret sitesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0b0a5-172">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="0b0a5-173">Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="0b0a5-173">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="0b0a5-174">robots.txt dosyalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="0b0a5-174">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="0b0a5-175">URL yeniden yönlendirmelerini toplu olarak yükleme</span><span class="sxs-lookup"><span data-stu-id="0b0a5-175">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="0b0a5-176">Commerce'ta B2C kiracısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="0b0a5-176">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="0b0a5-177">Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama</span><span class="sxs-lookup"><span data-stu-id="0b0a5-177">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="0b0a5-178">İçerik teslim ağı (CDN) için destek ekleme</span><span class="sxs-lookup"><span data-stu-id="0b0a5-178">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="0b0a5-179">Konum tabanlı mağaza algılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="0b0a5-179">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

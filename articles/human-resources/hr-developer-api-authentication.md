---
title: Kimlik doğrulama
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 025feca31eed8649bc319a1e1a1b6d1af3ddb128
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010912"
---
# <a name="authentication"></a><span data-ttu-id="2c606-102">Kimlik doğrulama</span><span class="sxs-lookup"><span data-stu-id="2c606-102">Authentication</span></span>

<span data-ttu-id="2c606-103">Bu makalede, Microsoft Dynamics 365 Human Resources veri uygulama programı arabirimi (API) ile kimlik doğrulaması yapma hakkında genel bakış bilgileri sağlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="2c606-103">This article provides overview information about how to authenticate with the Microsoft Dynamics 365 Human Resources data application programming interface (API).</span></span>

## <a name="overview"></a><span data-ttu-id="2c606-104">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="2c606-104">Overview</span></span>

<span data-ttu-id="2c606-105">İnsan Kaynakları veri API'si OData uygulamasıdır.</span><span class="sxs-lookup"><span data-stu-id="2c606-105">The data API for Human Resources is an OData implementation.</span></span> <span data-ttu-id="2c606-106">Daha fazla bilgi için bkz. [Açık Veri Protokolü (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span><span class="sxs-lookup"><span data-stu-id="2c606-106">For more information, see [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span></span>

<span data-ttu-id="2c606-107">Uygulama, uygulamanızın isteklerine hizmet vermeden önce, yetkili bir arayan olarak kimlik doğrulaması yapmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2c606-107">Your application must authenticate as an authorized caller before the API will service requests from your application.</span></span>

## <a name="fundamentals"></a><span data-ttu-id="2c606-108">Temel bilgiler</span><span class="sxs-lookup"><span data-stu-id="2c606-108">Fundamentals</span></span>

<span data-ttu-id="2c606-109">Veri API'yi çağırmak için uygulamanızın Microsoft Identity platformundan bir erişim belirteci edinmeleri gerekir.</span><span class="sxs-lookup"><span data-stu-id="2c606-109">To call the data API, your application must acquire an access token from the Microsoft identity platform.</span></span> <span data-ttu-id="2c606-110">Erişim belirteci, uygulamanız ve İnsan Kaynakları içinde kaynakları arama izni hakkında bilgiler içerir.</span><span class="sxs-lookup"><span data-stu-id="2c606-110">The access token contains information about your application and the permission that it has to call resources in Human Resources.</span></span>

### <a name="access-token"></a><span data-ttu-id="2c606-111">Erişim belirteci</span><span class="sxs-lookup"><span data-stu-id="2c606-111">Access token</span></span>

<span data-ttu-id="2c606-112">Microsoft Identity platform tarafından verilen erişim belirteçleri, Base64 ile kodlanmış JavaScript nesne gösterimi (JSON) Web belirteçleridir (JWT'ler).</span><span class="sxs-lookup"><span data-stu-id="2c606-112">Access tokens issued by the Microsoft identity platform are base64–encoded JavaScript Object Notation (JSON) Web Tokens (JWTs).</span></span> <span data-ttu-id="2c606-113">Bunlar, veri API'sının (ve Microsoft Identity platformuyla güvenlik altına alınan diğer Web API'lerinin) çağrıyı yapanın doğrulanması ve arayanın istediği işlemi gerçekleştirmek için doğru izinlere sahip olduğundan emin olmak için kullandığı bilgiler (talepler) içerir.</span><span class="sxs-lookup"><span data-stu-id="2c606-113">They contain information (claims) that the data API (and other web APIs that are secured by the Microsoft identity platform) use to validate the caller and make sure that the caller has the correct permissions to perform the operation they're requesting.</span></span> <span data-ttu-id="2c606-114">Çağrılar sırasında, erişim belirteçlerini opak olarak kabul edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2c606-114">During calls, you can treat access tokens as opaque.</span></span> <span data-ttu-id="2c606-115">Erişim belirteçlerini, Aktarım Katmanı Güvenliği (TLS) ve Köprü Metni Aktarım Protokolü Güvenli (HTTPS) gibi güvenli bir kanaldan her zaman aktarmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2c606-115">You should always transmit access tokens over a secure channel, such as Transport Layer Security (TLS) and Hypertext Transfer Protocol Secure (HTTPS).</span></span>

<span data-ttu-id="2c606-116">İşte Microsoft Identity platform tarafından verilen bir erişim simgesi örneği.</span><span class="sxs-lookup"><span data-stu-id="2c606-116">Here is an example of an access token that is issued by the Microsoft identity platform.</span></span>

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

<span data-ttu-id="2c606-117">Veri API'sini çağırmak için, erişim belirtecini HTTP isteğinizin yetkilendirme üstbilgisine bir taşıyıcı belirteci olarak iliştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="2c606-117">To call the data API, you attach the access token as a bearer token to the authorization header in your HTTP request.</span></span> <span data-ttu-id="2c606-118">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="2c606-118">Here is an example.</span></span>

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a><span data-ttu-id="2c606-119">Azure portalını kullanarak yeni uygulama kaydedin</span><span class="sxs-lookup"><span data-stu-id="2c606-119">Register a new application by using the Azure portal</span></span>

1. <span data-ttu-id="2c606-120">İş veya okul hesabı veya kişisel Microsoft hesabı ile [Microsoft Azure portalda](https://portal.azure.com) oturum açın.</span><span class="sxs-lookup"><span data-stu-id="2c606-120">Sign in to the [Microsoft Azure portal](https://portal.azure.com) with a work or school account, or a personal Microsoft account.</span></span>

2. <span data-ttu-id="2c606-121">Hesabınız size birden fazla kiracı erişimi veriyorsa, sağ üst köşedeki hesabınızı seçin ve Portal oturumunuzu istediğiniz Azure Active Directory (Azure AD) kiracıya ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2c606-121">If your account gives you access to more than one tenant, select your account in the upper-right corner, and set your portal session to the Azure Active Directory (Azure AD) tenant that you want.</span></span>

3. <span data-ttu-id="2c606-122">Sol bölmede **Azure Active Directory** hizmeti seçin ve sonra **uygulama kaydı \> yeni kaydı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2c606-122">In the left pane, select the **Azure Active Directory** service, and then select **App registrations \> New registration**.</span></span>

4. <span data-ttu-id="2c606-123">**Bir uygulamayı kaydet** sayfası göründüğünde, uygulamanızın kayıt bilgilerini girin:</span><span class="sxs-lookup"><span data-stu-id="2c606-123">When the **Register an application** page appears, enter your application's registration information:</span></span>

    - <span data-ttu-id="2c606-124">**Ad**: Uygulamanın kullanıcılarına gösterilecek anlamlı bir uygulama adı girin.</span><span class="sxs-lookup"><span data-stu-id="2c606-124">**Name**: Enter a meaningful application name that will be shown to users of the app.</span></span>
    - <span data-ttu-id="2c606-125">**Desteklenen hesap türleri**: Uygulamanızın desteklemesi gereken hesap türlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="2c606-125">**Supported account types**: Select the types of accounts that your app should support.</span></span>

        | <span data-ttu-id="2c606-126">Desteklenen hesap türleri</span><span class="sxs-lookup"><span data-stu-id="2c606-126">Supported account types</span></span> | <span data-ttu-id="2c606-127">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c606-127">Description</span></span> |
        |-------------------------|-------------|
        | <span data-ttu-id="2c606-128">Yalnızca bu kuruluş dizinindeki hesaplar</span><span class="sxs-lookup"><span data-stu-id="2c606-128">Accounts in this organizational directory only</span></span> | <span data-ttu-id="2c606-129">İş kolu uygulaması oluşturuyorsanız, bu seçeneği seçin.</span><span class="sxs-lookup"><span data-stu-id="2c606-129">Select this option if you're building a line-of-business app.</span></span> <span data-ttu-id="2c606-130">Uygulamayı bir dizine kaydetmediğiniz sürece bu seçenek kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="2c606-130">This option isn't available unless you're registering the app in a directory.</span></span><p><span data-ttu-id="2c606-131">Bu seçenek yalnızca tek kiracılı **Azure AD** olarak eşlendi.</span><span class="sxs-lookup"><span data-stu-id="2c606-131">This option is mapped to **Azure AD only single-tenant**.</span></span></p><p><span data-ttu-id="2c606-132">Uygulamayı bir dizinin dışına kaydetmediğiniz sürece bu seçenek varsayılan seçenektir.</span><span class="sxs-lookup"><span data-stu-id="2c606-132">This option is the default option unless you're registering the app outside a directory.</span></span> <span data-ttu-id="2c606-133">Bu durumda, varsayılan seçenek **Azure AD çok kiracılı ve kişisel Microsoft hesaplarıdır.**</span><span class="sxs-lookup"><span data-stu-id="2c606-133">In that case, the default option is **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p> |
        | <span data-ttu-id="2c606-134">Herhangi bir kuruluş dizinindeki hesaplar</span><span class="sxs-lookup"><span data-stu-id="2c606-134">Accounts in any organizational directory</span></span> | <span data-ttu-id="2c606-135">Tüm iş ve Eğitim müşterilerini hedeflemek için bu seçeneği belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2c606-135">Select this option to target all business and educational customers.</span></span><p><span data-ttu-id="2c606-136">Bu seçenek yalnızca çok kiracılı **Azure AD** olarak eşlendi.</span><span class="sxs-lookup"><span data-stu-id="2c606-136">This option is mapped to **Azure AD only multi-tenant**.</span></span></p><p><span data-ttu-id="2c606-137">Uygulamayı **tek Azure AD kiracılı**olarak kaydettirdiğiniz takdirde, **kimlik doğrulama** dikey penceresini **Azure AD yalnızca çok kiracılı** olarak güncelleştirmek ve **Azure AD yalnızca tek kiracı**'ya geri yüklemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2c606-137">If you registered the app as **Azure AD only single-tenant**, you can use the **Authentication** blade to update it to **Azure AD only multi-tenant** and then back to **Azure AD only single-tenant**.</span></span></p> |
        | <span data-ttu-id="2c606-138">Herhangi bir kuruluş dizinindeki hesaplar ve kişisel Microsoft hesapları</span><span class="sxs-lookup"><span data-stu-id="2c606-138">Accounts in any organizational directory and personal Microsoft accounts</span></span> | <span data-ttu-id="2c606-139">En geniş müşteri kümesini hedeflemek için bu seçeneği seçin.</span><span class="sxs-lookup"><span data-stu-id="2c606-139">Select this option to target the widest set of customers.</span></span><p><span data-ttu-id="2c606-140">Bu seçenek **Azure AD çok kiracılı ve kişisel Microsoft hesapları** ile eşleşir.</span><span class="sxs-lookup"><span data-stu-id="2c606-140">This option is mapped to **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p><p><span data-ttu-id="2c606-141">Uygulamayı **Azure AD çok kiracılı ve kişisel Microsoft hesaplarıyla** kaydettirdiğiniz takdirde, bu ayarı Kullanıcı arabiriminde (UI) değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="2c606-141">If you registered the app as **Azure AD multi-tenant and personal Microsoft accounts**, you can't change this setting in the user interface (UI).</span></span> <span data-ttu-id="2c606-142">Bunun yerine, desteklenen hesap türlerini değiştirmek için uygulama bildirimi Düzenleyicisini kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="2c606-142">Instead, you must use the application manifest editor to change the supported account types.</span></span></p> |

    - <span data-ttu-id="2c606-143">**Yeniden yönlendirme URI'si** (isteğe bağlı) – Oluşturmakta olduğunuz uygulamanın türünü seçin : **Web** veya **ortak istemci (mobil ve masaüstü)**.</span><span class="sxs-lookup"><span data-stu-id="2c606-143">**Redirect URI (optional)** – Select the type of app that you're building: **Web** or **Public client (mobile & desktop)**.</span></span> <span data-ttu-id="2c606-144">Sonra uygulamanın yeniden yönlendirme URI'sini (veya yanıt URL'si) girin.</span><span class="sxs-lookup"><span data-stu-id="2c606-144">Then enter the redirect URI (or reply URL) for the app.</span></span>

        - <span data-ttu-id="2c606-145">Web Apps için uygulamanın temel URL'sini belirtin.</span><span class="sxs-lookup"><span data-stu-id="2c606-145">For web apps, provide the base URL of the app.</span></span> <span data-ttu-id="2c606-146">Örneğin, `http://localhost:31544` yerel makinenizde çalışan bir Web uygulamasının URL'si olabilir.</span><span class="sxs-lookup"><span data-stu-id="2c606-146">For example, `http://localhost:31544` might be the URL for a web app that runs on your local machine.</span></span> <span data-ttu-id="2c606-147">Kullanıcılar daha sonra bu URL'yi bir Web istemci uygulamasında oturum açmak için kullanırlar.</span><span class="sxs-lookup"><span data-stu-id="2c606-147">Users then use this URL to sign in to a web client app.</span></span>
        - <span data-ttu-id="2c606-148">Ortak istemci uygulamaları için, Azure AD'nin belirteç yanıtlarını döndürmek üzere kullandığı URI 'yi sağlayın.</span><span class="sxs-lookup"><span data-stu-id="2c606-148">For public client apps, provide the URI that Azure AD uses to return token responses.</span></span> <span data-ttu-id="2c606-149">`myapp://auth` Gibi uygulamanıza özel bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="2c606-149">Enter a value that is specific to your app, such as `myapp://auth`.</span></span>

        <span data-ttu-id="2c606-150">Web uygulamaları veya yerel uygulamalar için belirli örnekleri görmek üzere, [Microsoft Identity platform (önceden geliştiriciler için Azure Active Directory idi)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts) üzerinde hızlı başlangıçlara bakın.</span><span class="sxs-lookup"><span data-stu-id="2c606-150">To see specific examples for web apps or native apps, see the quickstarts in [Microsoft identity platform (formerly Azure Active Directory for developers)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span></span>

5. <span data-ttu-id="2c606-151">**API izinleri**altında, **izin Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2c606-151">Under **API permissions**, select **Add a permission**.</span></span> <span data-ttu-id="2c606-152">Sonra, **Kuruluşumun kullandığı API'ler** sekmesinde **Dynamics 365 Human Resources** arayın ve uygulamanıza **Kullanıcı\_kimliğe bürünme** izni ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2c606-152">Then, on the **APIs my organization uses** tab, search for **Dynamics 365 Human Resources**, and add the **user\_impersonation** permission to your app.</span></span> <span data-ttu-id="2c606-153">İnsan Kaynakları için Uygulama Kodu: f9be0c49-aa22-4ec6-911a-c5da515226ff.</span><span class="sxs-lookup"><span data-stu-id="2c606-153">The Application ID for Human Resources is f9be0c49-aa22-4ec6-911a-c5da515226ff.</span></span> <span data-ttu-id="2c606-154">Doğru uygulamayı seçtiğinizden emin olmak için bu kodu kullanın.</span><span class="sxs-lookup"><span data-stu-id="2c606-154">Use this ID to ensure you have chosen the correct application.</span></span>

6. <span data-ttu-id="2c606-155">**Kayıt**'ı seç.</span><span class="sxs-lookup"><span data-stu-id="2c606-155">Select **Register**.</span></span>

   <span data-ttu-id="2c606-156">[![Azure portalında yeni bir uygulama kaydediliyor](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="2c606-156">[![Registering a new app in the Azure portal](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span></span>

<span data-ttu-id="2c606-157">Azure AD, uygulamanıza benzersiz bir uygulama kimliği (istemci kimliği) atar ve sizi uygulamanızın **genel bakış** sayfasına götürür.</span><span class="sxs-lookup"><span data-stu-id="2c606-157">Azure AD assigns a unique application ID (client ID) to your app, and takes you to the **Overview** page for your app.</span></span> <span data-ttu-id="2c606-158">Uygulamanıza daha fazla özellik eklemek için, marka ve sertifikalar ve gizlilikler için seçenekler gibi diğer yapılandırma seçeneklerini belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2c606-158">To add more capabilities to your app, you can select other configuration options, such as options for branding and for certificates and secrets.</span></span>

## <a name="retrieving-an-access-token"></a><span data-ttu-id="2c606-159">Erişim belirteci alınıyor</span><span class="sxs-lookup"><span data-stu-id="2c606-159">Retrieving an access token</span></span>

<span data-ttu-id="2c606-160">İnsan Kaynakları veri API'sini çağırmak için erişim belirteci alma yönteminin nasıl alınacağı, istemci uygulamanızı geliştirmek için hangi teknolojilere kullandığınız ile ilgili bilgiler elde edilir.</span><span class="sxs-lookup"><span data-stu-id="2c606-160">The specifics of how you retrieve an access token for calling the Human Resources data API will depend on what technologies you're using to develop your client application.</span></span> <span data-ttu-id="2c606-161">Örneğin, bir [üçüncü taraf yardımcı programıyla](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (Postman gibi) test edilebilir, bir C# konsol uygulaması veya Web hizmeti geliştiriyor veya bir JavaScript/TypeScript istemcisi oluşturuluyor olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2c606-161">For example, you might be [testing with a third party utility](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (such as Postman), developing a C# console application or web service, or building a javascript/TypeScript client.</span></span>

<span data-ttu-id="2c606-162">Örnek C# istemci uygulaması:</span><span class="sxs-lookup"><span data-stu-id="2c606-162">Example C# client application:</span></span>
```C#
using System;
using System.Net.Http;
using System.Threading.Tasks;

// requires appropriate NuGet package references in the project
using Microsoft.IdentityModel.Clients.ActiveDirectory;

namespace TalentODataPoC
{
    class Program
    {
        // prereq: This client app must be registered in Azure Active Directory. The app must be
        // registered as requiring permission to the Dynamics 365 for Talent API (with the Dynamics
        // HCM Workload delegated permission).
        static string clientId = "4fc703ef-672c-4e2c-813f-2f9d29d726db"; // This value should be obtained from AAD and must match your registered app
        static string talentNamespaceUri = "";

        public static async Task CallTalentODataService()
        {
            // authority URI
            UriBuilder uri = new UriBuilder("https://login.microsoftonline.com/common");
            AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

            // request token for the resource we want to access (Human Resources). This will authenticate
            // the user and return an access token containing claims for the authenticated user.
            var authResult = await authenticationContext.AcquireTokenAsync(
                "http://hr.talent.dynamics.com", /*Talent app id or resource URI*/
                clientId, /*registered client app id*/
                new Uri("https://localhost"), /*redirect URI, as registered in your AAD app*/
                new PlatformParameters(PromptBehavior.SelectAccount));

            // create the authorization header, which needs to be passed in the Header of the HTTP Requests to Talent
            string authHeader = authResult.CreateAuthorizationHeader();

            // HINT: paste the JWT into https://jwt.ms to decode and view it
            Console.Write("authHeader: ");
            Console.WriteLine(authHeader);
            Console.WriteLine();

            HttpClient client = new HttpClient();
            client.DefaultRequestHeaders.Add("Authorization", authHeader);

            string s;

            Console.Write("Talent Namespace URI: ");
            Console.WriteLine(talentNamespaceUri);
            Console.WriteLine();

            // call the OData service to get JobType data from Talent
            var resultOdata = await client.GetAsync(talentNamespaceUri + "data/JobTypes");
            s = await resultOdata.Content.ReadAsStringAsync();
            Console.WriteLine(s);
            Console.WriteLine();
        }

        static void Main(string[] args)
        {
            Console.WriteLine();

            // if the user passes in a single parameter, assume it is the namespaceUri for Talent
            if (args.Length == 1)
            {
                talentNamespaceUri = args[0];
            } else if (args.Length == 0)
            {
                Console.WriteLine("Enter Talent URL including namespace.");
                Console.WriteLine("Example: https://aos-rts-sf-21454f9d830-prod-westus2.hr.talent.dynamics.com/namespaces/2328af1a-2d45-4c6a-99e3-12a4c3867dcf/");
                Console.Write("> ");
                talentNamespaceUri = Console.ReadLine();
                if (!talentNamespaceUri.EndsWith("/"))
                {
                    talentNamespaceUri = talentNamespaceUri + "/";
                }
            } else
            {
                Console.WriteLine("Unexpected Arguments");
                System.Environment.Exit(1);
            }

            Task t = Program.CallTalentODataService();
            t.Wait();
        }
    }
}
```

<span data-ttu-id="2c606-163">Bir erişim belirteci aldıktan sonra, doğrulama üstbilgisindeki belirteci yukarıda açıklandığı şekilde, Data API'ye gönderdiğiniz her istekle bir taşıyıcı belirteci olarak geçireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="2c606-163">Once you've retrieved an access token, you'll pass the token in the Authorization header as a bearer token with each request you send to the data API, as described above.</span></span>

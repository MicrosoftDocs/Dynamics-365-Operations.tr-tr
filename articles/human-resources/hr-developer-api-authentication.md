---
title: Kimlik Doğrulama
description: Bu makalede, Microsoft Dynamics 365 Human Resources veri uygulama programı arabirimi (API) ile kimlik doğrulaması yapma hakkında genel bakış bilgileri sağlanmaktadır.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 60774d162d733404166e710932291a736eb0d8b4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465546"
---
# <a name="authentication"></a><span data-ttu-id="0c46f-103">Kimlik Doğrulama</span><span class="sxs-lookup"><span data-stu-id="0c46f-103">Authentication</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0c46f-104">Bu makalede, Microsoft Dynamics 365 Human Resources veri uygulama programı arabirimi (API) ile kimlik doğrulaması yapma hakkında genel bakış bilgileri sağlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="0c46f-104">This article provides overview information about how to authenticate with the Microsoft Dynamics 365 Human Resources data application programming interface (API).</span></span>

## <a name="overview"></a><span data-ttu-id="0c46f-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="0c46f-105">Overview</span></span>

<span data-ttu-id="0c46f-106">İnsan Kaynakları veri API'si OData uygulamasıdır.</span><span class="sxs-lookup"><span data-stu-id="0c46f-106">The data API for Human Resources is an OData implementation.</span></span> <span data-ttu-id="0c46f-107">Daha fazla bilgi için bkz. [Açık Veri Protokolü (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span><span class="sxs-lookup"><span data-stu-id="0c46f-107">For more information, see [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span></span>

<span data-ttu-id="0c46f-108">Uygulama, uygulamanızın isteklerine hizmet vermeden önce, yetkili bir arayan olarak kimlik doğrulaması yapmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0c46f-108">Your application must authenticate as an authorized caller before the API will service requests from your application.</span></span>

## <a name="fundamentals"></a><span data-ttu-id="0c46f-109">Temel bilgiler</span><span class="sxs-lookup"><span data-stu-id="0c46f-109">Fundamentals</span></span>

<span data-ttu-id="0c46f-110">Veri API'yi çağırmak için uygulamanızın Microsoft Identity platformundan bir erişim belirteci edinmeleri gerekir.</span><span class="sxs-lookup"><span data-stu-id="0c46f-110">To call the data API, your application must acquire an access token from the Microsoft identity platform.</span></span> <span data-ttu-id="0c46f-111">Erişim belirteci, uygulamanız ve İnsan Kaynakları içinde kaynakları arama izni hakkında bilgiler içerir.</span><span class="sxs-lookup"><span data-stu-id="0c46f-111">The access token contains information about your application and the permission that it has to call resources in Human Resources.</span></span>

### <a name="access-token"></a><span data-ttu-id="0c46f-112">Erişim belirteci</span><span class="sxs-lookup"><span data-stu-id="0c46f-112">Access token</span></span>

<span data-ttu-id="0c46f-113">Microsoft Identity platform tarafından verilen erişim belirteçleri, Base64 ile kodlanmış JavaScript nesne gösterimi (JSON) Web belirteçleridir (JWT'ler).</span><span class="sxs-lookup"><span data-stu-id="0c46f-113">Access tokens issued by the Microsoft identity platform are base64–encoded JavaScript Object Notation (JSON) Web Tokens (JWTs).</span></span> <span data-ttu-id="0c46f-114">Bunlar, veri API'sının (ve Microsoft Identity platformuyla güvenlik altına alınan diğer Web API'lerinin) çağrıyı yapanın doğrulanması ve arayanın istediği işlemi gerçekleştirmek için doğru izinlere sahip olduğundan emin olmak için kullandığı bilgiler (talepler) içerir.</span><span class="sxs-lookup"><span data-stu-id="0c46f-114">They contain information (claims) that the data API (and other web APIs that are secured by the Microsoft identity platform) use to validate the caller and make sure that the caller has the correct permissions to perform the operation they're requesting.</span></span> <span data-ttu-id="0c46f-115">Çağrılar sırasında, erişim belirteçlerini opak olarak kabul edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0c46f-115">During calls, you can treat access tokens as opaque.</span></span> <span data-ttu-id="0c46f-116">Erişim belirteçlerini, Aktarım Katmanı Güvenliği (TLS) ve Köprü Metni Aktarım Protokolü Güvenli (HTTPS) gibi güvenli bir kanaldan her zaman aktarmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0c46f-116">You should always transmit access tokens over a secure channel, such as Transport Layer Security (TLS) and Hypertext Transfer Protocol Secure (HTTPS).</span></span>

<span data-ttu-id="0c46f-117">İşte Microsoft Identity platform tarafından verilen bir erişim simgesi örneği.</span><span class="sxs-lookup"><span data-stu-id="0c46f-117">Here is an example of an access token that is issued by the Microsoft identity platform.</span></span>

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

<span data-ttu-id="0c46f-118">Veri API'sini çağırmak için, erişim belirtecini HTTP isteğinizin yetkilendirme üstbilgisine bir taşıyıcı belirteci olarak iliştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="0c46f-118">To call the data API, you attach the access token as a bearer token to the authorization header in your HTTP request.</span></span> <span data-ttu-id="0c46f-119">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="0c46f-119">Here is an example.</span></span>

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a><span data-ttu-id="0c46f-120">Azure portalını kullanarak yeni uygulama kaydedin</span><span class="sxs-lookup"><span data-stu-id="0c46f-120">Register a new application by using the Azure portal</span></span>

1. <span data-ttu-id="0c46f-121">İş veya okul hesabı veya kişisel Microsoft hesabı ile [Microsoft Azure portalda](https://portal.azure.com) oturum açın.</span><span class="sxs-lookup"><span data-stu-id="0c46f-121">Sign in to the [Microsoft Azure portal](https://portal.azure.com) with a work or school account, or a personal Microsoft account.</span></span>

2. <span data-ttu-id="0c46f-122">Hesabınız size birden fazla kiracı erişimi veriyorsa, sağ üst köşedeki hesabınızı seçin ve Portal oturumunuzu istediğiniz Azure Active Directory (Azure AD) kiracıya ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0c46f-122">If your account gives you access to more than one tenant, select your account in the upper-right corner, and set your portal session to the Azure Active Directory (Azure AD) tenant that you want.</span></span>

3. <span data-ttu-id="0c46f-123">Sol bölmede **Azure Active Directory** hizmeti seçin ve sonra **uygulama kaydı \> yeni kaydı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="0c46f-123">In the left pane, select the **Azure Active Directory** service, and then select **App registrations \> New registration**.</span></span>

4. <span data-ttu-id="0c46f-124">**Bir uygulamayı kaydet** sayfası göründüğünde, uygulamanızın kayıt bilgilerini girin:</span><span class="sxs-lookup"><span data-stu-id="0c46f-124">When the **Register an application** page appears, enter your application's registration information:</span></span>

    - <span data-ttu-id="0c46f-125">**Ad**: Uygulamanın kullanıcılarına gösterilecek anlamlı bir uygulama adı girin.</span><span class="sxs-lookup"><span data-stu-id="0c46f-125">**Name**: Enter a meaningful application name that will be shown to users of the app.</span></span>
    - <span data-ttu-id="0c46f-126">**Desteklenen hesap türleri**: Uygulamanızın desteklemesi gereken hesap türlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="0c46f-126">**Supported account types**: Select the types of accounts that your app should support.</span></span>

        | <span data-ttu-id="0c46f-127">Desteklenen hesap türleri</span><span class="sxs-lookup"><span data-stu-id="0c46f-127">Supported account types</span></span> | <span data-ttu-id="0c46f-128">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c46f-128">Description</span></span> |
        |-------------------------|-------------|
        | <span data-ttu-id="0c46f-129">Yalnızca bu kuruluş dizinindeki hesaplar</span><span class="sxs-lookup"><span data-stu-id="0c46f-129">Accounts in this organizational directory only</span></span> | <span data-ttu-id="0c46f-130">İş kolu uygulaması oluşturuyorsanız, bu seçeneği seçin.</span><span class="sxs-lookup"><span data-stu-id="0c46f-130">Select this option if you're building a line-of-business app.</span></span> <span data-ttu-id="0c46f-131">Uygulamayı bir dizine kaydetmediğiniz sürece bu seçenek kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="0c46f-131">This option isn't available unless you're registering the app in a directory.</span></span><p><span data-ttu-id="0c46f-132">Bu seçenek yalnızca tek kiracılı **Azure AD** olarak eşlendi.</span><span class="sxs-lookup"><span data-stu-id="0c46f-132">This option is mapped to **Azure AD only single-tenant**.</span></span></p><p><span data-ttu-id="0c46f-133">Uygulamayı bir dizinin dışına kaydetmediğiniz sürece bu seçenek varsayılan seçenektir.</span><span class="sxs-lookup"><span data-stu-id="0c46f-133">This option is the default option unless you're registering the app outside a directory.</span></span> <span data-ttu-id="0c46f-134">Bu durumda, varsayılan seçenek **Azure AD çok kiracılı ve kişisel Microsoft hesaplarıdır.**</span><span class="sxs-lookup"><span data-stu-id="0c46f-134">In that case, the default option is **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p> |
        | <span data-ttu-id="0c46f-135">Herhangi bir kuruluş dizinindeki hesaplar</span><span class="sxs-lookup"><span data-stu-id="0c46f-135">Accounts in any organizational directory</span></span> | <span data-ttu-id="0c46f-136">Tüm iş ve Eğitim müşterilerini hedeflemek için bu seçeneği belirleyin.</span><span class="sxs-lookup"><span data-stu-id="0c46f-136">Select this option to target all business and educational customers.</span></span><p><span data-ttu-id="0c46f-137">Bu seçenek yalnızca çok kiracılı **Azure AD** olarak eşlendi.</span><span class="sxs-lookup"><span data-stu-id="0c46f-137">This option is mapped to **Azure AD only multi-tenant**.</span></span></p><p><span data-ttu-id="0c46f-138">Uygulamayı **tek Azure AD kiracılı** olarak kaydettirdiğiniz takdirde, **kimlik doğrulama** dikey penceresini **Azure AD yalnızca çok kiracılı** olarak güncelleştirmek ve **Azure AD yalnızca tek kiracı**'ya geri yüklemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0c46f-138">If you registered the app as **Azure AD only single-tenant**, you can use the **Authentication** blade to update it to **Azure AD only multi-tenant** and then back to **Azure AD only single-tenant**.</span></span></p> |
        | <span data-ttu-id="0c46f-139">Herhangi bir kuruluş dizinindeki hesaplar ve kişisel Microsoft hesapları</span><span class="sxs-lookup"><span data-stu-id="0c46f-139">Accounts in any organizational directory and personal Microsoft accounts</span></span> | <span data-ttu-id="0c46f-140">En geniş müşteri kümesini hedeflemek için bu seçeneği seçin.</span><span class="sxs-lookup"><span data-stu-id="0c46f-140">Select this option to target the widest set of customers.</span></span><p><span data-ttu-id="0c46f-141">Bu seçenek **Azure AD çok kiracılı ve kişisel Microsoft hesapları** ile eşleşir.</span><span class="sxs-lookup"><span data-stu-id="0c46f-141">This option is mapped to **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p><p><span data-ttu-id="0c46f-142">Uygulamayı **Azure AD çok kiracılı ve kişisel Microsoft hesaplarıyla** kaydettirdiğiniz takdirde, bu ayarı Kullanıcı arabiriminde (UI) değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="0c46f-142">If you registered the app as **Azure AD multi-tenant and personal Microsoft accounts**, you can't change this setting in the user interface (UI).</span></span> <span data-ttu-id="0c46f-143">Bunun yerine, desteklenen hesap türlerini değiştirmek için uygulama bildirimi Düzenleyicisini kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="0c46f-143">Instead, you must use the application manifest editor to change the supported account types.</span></span></p> |

    - <span data-ttu-id="0c46f-144">**Yeniden yönlendirme URI'si** (isteğe bağlı) – Oluşturmakta olduğunuz uygulamanın türünü seçin : **Web** veya **ortak istemci (mobil ve masaüstü)**.</span><span class="sxs-lookup"><span data-stu-id="0c46f-144">**Redirect URI (optional)** – Select the type of app that you're building: **Web** or **Public client (mobile & desktop)**.</span></span> <span data-ttu-id="0c46f-145">Sonra uygulamanın yeniden yönlendirme URI'sini (veya yanıt URL'si) girin.</span><span class="sxs-lookup"><span data-stu-id="0c46f-145">Then enter the redirect URI (or reply URL) for the app.</span></span>

        - <span data-ttu-id="0c46f-146">Web Apps için uygulamanın temel URL'sini belirtin.</span><span class="sxs-lookup"><span data-stu-id="0c46f-146">For web apps, provide the base URL of the app.</span></span> <span data-ttu-id="0c46f-147">Örneğin, `http://localhost:31544` yerel makinenizde çalışan bir Web uygulamasının URL'si olabilir.</span><span class="sxs-lookup"><span data-stu-id="0c46f-147">For example, `http://localhost:31544` might be the URL for a web app that runs on your local machine.</span></span> <span data-ttu-id="0c46f-148">Kullanıcılar daha sonra bu URL'yi bir Web istemci uygulamasında oturum açmak için kullanırlar.</span><span class="sxs-lookup"><span data-stu-id="0c46f-148">Users then use this URL to sign in to a web client app.</span></span>
        - <span data-ttu-id="0c46f-149">Ortak istemci uygulamaları için, Azure AD'nin belirteç yanıtlarını döndürmek üzere kullandığı URI 'yi sağlayın.</span><span class="sxs-lookup"><span data-stu-id="0c46f-149">For public client apps, provide the URI that Azure AD uses to return token responses.</span></span> <span data-ttu-id="0c46f-150">`myapp://auth` Gibi uygulamanıza özel bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="0c46f-150">Enter a value that is specific to your app, such as `myapp://auth`.</span></span>

        <span data-ttu-id="0c46f-151">Web uygulamaları veya yerel uygulamalar için belirli örnekleri görmek üzere, [Microsoft Identity platform (önceden geliştiriciler için Azure Active Directory idi)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts) üzerinde hızlı başlangıçlara bakın.</span><span class="sxs-lookup"><span data-stu-id="0c46f-151">To see specific examples for web apps or native apps, see the quickstarts in [Microsoft identity platform (formerly Azure Active Directory for developers)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span></span>

5. <span data-ttu-id="0c46f-152">**API izinleri** altında, **izin Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0c46f-152">Under **API permissions**, select **Add a permission**.</span></span> <span data-ttu-id="0c46f-153">Sonra, **Kuruluşumun kullandığı API'ler** sekmesinde **Dynamics 365 Human Resources** arayın ve uygulamanıza **Kullanıcı\_kimliğe bürünme** izni ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0c46f-153">Then, on the **APIs my organization uses** tab, search for **Dynamics 365 Human Resources**, and add the **user\_impersonation** permission to your app.</span></span> <span data-ttu-id="0c46f-154">İnsan Kaynakları için Uygulama Kodu: f9be0c49-aa22-4ec6-911a-c5da515226ff.</span><span class="sxs-lookup"><span data-stu-id="0c46f-154">The Application ID for Human Resources is f9be0c49-aa22-4ec6-911a-c5da515226ff.</span></span> <span data-ttu-id="0c46f-155">Doğru uygulamayı seçtiğinizden emin olmak için bu kodu kullanın.</span><span class="sxs-lookup"><span data-stu-id="0c46f-155">Use this ID to ensure you have chosen the correct application.</span></span>

6. <span data-ttu-id="0c46f-156">**Kayıt**'ı seç.</span><span class="sxs-lookup"><span data-stu-id="0c46f-156">Select **Register**.</span></span>

   <span data-ttu-id="0c46f-157">[![Azure portalında yeni bir uygulama kaydediliyor](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="0c46f-157">[![Registering a new app in the Azure portal](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span></span>

<span data-ttu-id="0c46f-158">Azure AD, uygulamanıza benzersiz bir uygulama kimliği (istemci kimliği) atar ve sizi uygulamanızın **genel bakış** sayfasına götürür.</span><span class="sxs-lookup"><span data-stu-id="0c46f-158">Azure AD assigns a unique application ID (client ID) to your app, and takes you to the **Overview** page for your app.</span></span> <span data-ttu-id="0c46f-159">Uygulamanıza daha fazla özellik eklemek için, marka ve sertifikalar ve gizlilikler için seçenekler gibi diğer yapılandırma seçeneklerini belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0c46f-159">To add more capabilities to your app, you can select other configuration options, such as options for branding and for certificates and secrets.</span></span>

## <a name="retrieving-an-access-token"></a><span data-ttu-id="0c46f-160">Erişim belirteci alınıyor</span><span class="sxs-lookup"><span data-stu-id="0c46f-160">Retrieving an access token</span></span>

<span data-ttu-id="0c46f-161">İnsan Kaynakları veri API'sini çağırmak için erişim belirteci alma yönteminin nasıl alınacağı, istemci uygulamanızı geliştirmek için hangi teknolojilere kullandığınız ile ilgili bilgiler elde edilir.</span><span class="sxs-lookup"><span data-stu-id="0c46f-161">The specifics of how you retrieve an access token for calling the Human Resources data API will depend on what technologies you're using to develop your client application.</span></span> <span data-ttu-id="0c46f-162">Örneğin, bir [üçüncü taraf yardımcı programıyla](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (Postman gibi) test edilebilir, bir C# konsol uygulaması veya Web hizmeti geliştiriyor veya bir JavaScript/TypeScript istemcisi oluşturuluyor olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0c46f-162">For example, you might be [testing with a third party utility](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (such as Postman), developing a C# console application or web service, or building a javascript/TypeScript client.</span></span>

<span data-ttu-id="0c46f-163">Örnek C# istemci uygulaması:</span><span class="sxs-lookup"><span data-stu-id="0c46f-163">Example C# client application:</span></span>
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

<span data-ttu-id="0c46f-164">Bir erişim belirteci aldıktan sonra, doğrulama üstbilgisindeki belirteci yukarıda açıklandığı şekilde, Data API'ye gönderdiğiniz her istekle bir taşıyıcı belirteci olarak geçireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="0c46f-164">Once you've retrieved an access token, you'll pass the token in the Authorization header as a bearer token with each request you send to the data API, as described above.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
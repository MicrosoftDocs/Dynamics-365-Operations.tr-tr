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
ms.openlocfilehash: 963bec2b817c59e3b5860c5ff5885e165ec8656a
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115572"
---
# <a name="authentication"></a>Kimlik Doğrulama

Bu makalede, Microsoft Dynamics 365 Human Resources veri uygulama programı arabirimi (API) ile kimlik doğrulaması yapma hakkında genel bakış bilgileri sağlanmaktadır.

## <a name="overview"></a>Genel Bakış

İnsan Kaynakları veri API'si OData uygulamasıdır. Daha fazla bilgi için bkz. [Açık Veri Protokolü (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).

Uygulama, uygulamanızın isteklerine hizmet vermeden önce, yetkili bir arayan olarak kimlik doğrulaması yapmalıdır.

## <a name="fundamentals"></a>Temel bilgiler

Veri API'yi çağırmak için uygulamanızın Microsoft Identity platformundan bir erişim belirteci edinmeleri gerekir. Erişim belirteci, uygulamanız ve İnsan Kaynakları içinde kaynakları arama izni hakkında bilgiler içerir.

### <a name="access-token"></a>Erişim belirteci

Microsoft Identity platform tarafından verilen erişim belirteçleri, Base64 ile kodlanmış JavaScript nesne gösterimi (JSON) Web belirteçleridir (JWT'ler). Bunlar, veri API'sının (ve Microsoft Identity platformuyla güvenlik altına alınan diğer Web API'lerinin) çağrıyı yapanın doğrulanması ve arayanın istediği işlemi gerçekleştirmek için doğru izinlere sahip olduğundan emin olmak için kullandığı bilgiler (talepler) içerir. Çağrılar sırasında, erişim belirteçlerini opak olarak kabul edebilirsiniz. Erişim belirteçlerini, Aktarım Katmanı Güvenliği (TLS) ve Köprü Metni Aktarım Protokolü Güvenli (HTTPS) gibi güvenli bir kanaldan her zaman aktarmanız gerekir.

İşte Microsoft Identity platform tarafından verilen bir erişim simgesi örneği.

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

Veri API'sini çağırmak için, erişim belirtecini HTTP isteğinizin yetkilendirme üstbilgisine bir taşıyıcı belirteci olarak iliştirmelisiniz. Aşağıda bir örnek verilmiştir.

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a>Azure portalını kullanarak yeni uygulama kaydedin

1. İş veya okul hesabı veya kişisel Microsoft hesabı ile [Microsoft Azure portalda](https://portal.azure.com) oturum açın.

2. Hesabınız size birden fazla kiracı erişimi veriyorsa, sağ üst köşedeki hesabınızı seçin ve Portal oturumunuzu istediğiniz Azure Active Directory (Azure AD) kiracıya ayarlayın.

3. Sol bölmede **Azure Active Directory** hizmeti seçin ve sonra **uygulama kaydı \> yeni kaydı**'nı seçin.

4. **Bir uygulamayı kaydet** sayfası göründüğünde, uygulamanızın kayıt bilgilerini girin:

    - **Ad**: Uygulamanın kullanıcılarına gösterilecek anlamlı bir uygulama adı girin.
    - **Desteklenen hesap türleri**: Uygulamanızın desteklemesi gereken hesap türlerini seçin.

        | Desteklenen hesap türleri | Tanım |
        |-------------------------|-------------|
        | Yalnızca bu kuruluş dizinindeki hesaplar | İş kolu uygulaması oluşturuyorsanız, bu seçeneği seçin. Uygulamayı bir dizine kaydetmediğiniz sürece bu seçenek kullanılamaz.<p>Bu seçenek yalnızca tek kiracılı **Azure AD** olarak eşlendi.</p><p>Uygulamayı bir dizinin dışına kaydetmediğiniz sürece bu seçenek varsayılan seçenektir. Bu durumda, varsayılan seçenek **Azure AD çok kiracılı ve kişisel Microsoft hesaplarıdır.**</p> |
        | Herhangi bir kuruluş dizinindeki hesaplar | Tüm iş ve Eğitim müşterilerini hedeflemek için bu seçeneği belirleyin.<p>Bu seçenek yalnızca çok kiracılı **Azure AD** olarak eşlendi.</p><p>Uygulamayı **tek Azure AD kiracılı** olarak kaydettirdiğiniz takdirde, **kimlik doğrulama** dikey penceresini **Azure AD yalnızca çok kiracılı** olarak güncelleştirmek ve **Azure AD yalnızca tek kiracı**'ya geri yüklemek için kullanabilirsiniz.</p> |
        | Herhangi bir kuruluş dizinindeki hesaplar ve kişisel Microsoft hesapları | En geniş müşteri kümesini hedeflemek için bu seçeneği seçin.<p>Bu seçenek **Azure AD çok kiracılı ve kişisel Microsoft hesapları** ile eşleşir.</p><p>Uygulamayı **Azure AD çok kiracılı ve kişisel Microsoft hesaplarıyla** kaydettirdiğiniz takdirde, bu ayarı Kullanıcı arabiriminde (UI) değiştiremezsiniz. Bunun yerine, desteklenen hesap türlerini değiştirmek için uygulama bildirimi Düzenleyicisini kullanmalısınız.</p> |

    - **Yeniden yönlendirme URI'si** (isteğe bağlı) – Oluşturmakta olduğunuz uygulamanın türünü seçin : **Web** veya **ortak istemci (mobil ve masaüstü)**. Sonra uygulamanın yeniden yönlendirme URI'sini (veya yanıt URL'si) girin.

        - Web Apps için uygulamanın temel URL'sini belirtin. Örneğin, `http://localhost:31544` yerel makinenizde çalışan bir Web uygulamasının URL'si olabilir. Kullanıcılar daha sonra bu URL'yi bir Web istemci uygulamasında oturum açmak için kullanırlar.
        - Ortak istemci uygulamaları için, Azure AD'nin belirteç yanıtlarını döndürmek üzere kullandığı URI 'yi sağlayın. `myapp://auth` Gibi uygulamanıza özel bir değer girin.

        Web uygulamaları veya yerel uygulamalar için belirli örnekleri görmek üzere, [Microsoft Identity platform (önceden geliştiriciler için Azure Active Directory idi)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts) üzerinde hızlı başlangıçlara bakın.

5. **API izinleri** altında, **izin Ekle** 'yi seçin. Sonra, **Kuruluşumun kullandığı API'ler** sekmesinde **Dynamics 365 Human Resources** arayın ve uygulamanıza **Kullanıcı\_kimliğe bürünme** izni ekleyin. İnsan Kaynakları için Uygulama Kodu: f9be0c49-aa22-4ec6-911a-c5da515226ff. Doğru uygulamayı seçtiğinizden emin olmak için bu kodu kullanın.

6. **Kayıt**'ı seç.

   [![Azure portalında yeni bir uygulama kaydediliyor](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)

Azure AD, uygulamanıza benzersiz bir uygulama kimliği (istemci kimliği) atar ve sizi uygulamanızın **genel bakış** sayfasına götürür. Uygulamanıza daha fazla özellik eklemek için, marka ve sertifikalar ve gizlilikler için seçenekler gibi diğer yapılandırma seçeneklerini belirleyebilirsiniz.

## <a name="retrieving-an-access-token"></a>Erişim belirteci alınıyor

İnsan Kaynakları veri API'sini çağırmak için erişim belirteci alma yönteminin nasıl alınacağı, istemci uygulamanızı geliştirmek için hangi teknolojilere kullandığınız ile ilgili bilgiler elde edilir. Örneğin, bir [üçüncü taraf yardımcı programıyla](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (Postman gibi) test edilebilir, bir C# konsol uygulaması veya Web hizmeti geliştiriyor veya bir JavaScript/TypeScript istemcisi oluşturuluyor olabilirsiniz.

Örnek C# istemci uygulaması:
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

Bir erişim belirteci aldıktan sonra, doğrulama üstbilgisindeki belirteci yukarıda açıklandığı şekilde, Data API'ye gönderdiğiniz her istekle bir taşıyıcı belirteci olarak geçireceksiniz.

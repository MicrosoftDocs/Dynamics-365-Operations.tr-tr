---
title: Sanal tablo tabanlı tümleştirmeler için güvenlik yapılandırması kavramları
description: Bu makalede, Microsoft Dynamics 365 Human Resources ve diğer sistemler arasında tümleştirme oluşturmaya yönelik bir mimari açıklanmaktadır.
author: twheeloc
ms.date: 11/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 219ceb0adae0cee5f74a39140ab74af9fdac1eb6
ms.sourcegitcommit: ea79bf014bbf495ac8e28db29502c8bd85a75f32
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/11/2022
ms.locfileid: "9759663"
---
# <a name="security-configuration-concepts-for-virtual-table-based-integrations"></a>Sanal tablo tabanlı tümleştirmeler için güvenlik yapılandırması kavramları

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Dynamics 365 Human Resources ile üçüncü taraf bir sistem arasında tümleştirme oluşturmak için [Microsoft Dataverse sanal tabloları (varlıklar)](/dev-itpro/power-platform/virtual-entities-overview) kullanmaya yönelik bir mimari açıklanmaktadır. Makale, güvenlik yapılandırmasına ve sistem sınırları arasında işlevsel, güvenli bir sistem oluşturmak için gereken kimlik doğrulama ve yetkilendirme konularına odaklanmaktadır.

## <a name="prerequisite-reference-articles"></a>Önkoşul başvuru makaleleri

Aşağıdaki makalelerde bu makaledeki kavramlar hakkında daha fazla bilgi sağlanmaktadır:

- [Sanal varlıklara genel bakış](/dev-itpro/power-platform/virtual-entities-overview)
- [Sanal tablolaru (varlıklar) kullanmaya başlama](/developer/data-platform/virtual-entities/get-started-ve)
- [Çok kiracılı sunucudan-sunucuya kimlik doğrulaması (Microsoft Dataverse) kullanma](/developer/data-platform/use-multi-tenant-server-server-authentication)
- [Microsoft Dataverse ile OAuth kimlik doğrulaması kullanma (Dataverse)](/developer/data-platform/authenticate-oauth)
- [Microsoft kimlik platformunda OAuth 2.0 istemci kimlik bilgileri akışı](/azure/active-directory/develop/v2-oauth2-client-creds-grant-flow)
- [Kimlik doğrulaması ve yetkilendirme](/dev-itpro/power-platform/authentication-and-authorization)

## <a name="architecture"></a>Mimari 

Aşağıdaki mimari diyagram, sanal tablolar (varlıklar) kullanan bir tümleştirmenin kapsadığı ana kavramları gösterir.

![Sanal tablo tabanlı tümleştirme.](./media/Hosts.jpg)

Aşağıda önceki diyagramdaki bazı öğelerin açıklaması verilmiştir:

- **Microsoft** – Microsoft, farklı Dynamics 365 ürünlerini müşteriler adına barındırır ve çalıştırır.

    - **Azure Active Directory (Azure AD) kiracısı C** – Microsoft'un sahip olduğu bir Azure AD kiracısı. Bu, Dynamics 365 uygulamalarının kayıtlı olduğu kiracıdır.

- **Tümleştirme iş ortağı**

    - **Tümleştirilen sistemi** – Dynamics 365 ile tümleştirilmekte olan sistem. Bu, Dynamics 365'te depolanan verilere dayanan bir bordro sistemi veya herhangi bir sistem olabilir.
    - **Bağdaştırıcı** - Hem Dynamics 365 hem de tümleştirme sistemiyle etkileşimde bulunmaktan sorumlu yazılım veya hizmet.

        > [!NOTE]
        > Bir bağdaştırıcının birden fazla Dynamics 365 müşterisi tarafından kullanılması amaçlanıyorsa, beklenti Azure AD'de çok kiracılı bir uygulama olarak kaydedilmesidir.

    - **Azure AD kiracısı A** - Tümleştirme iş ortağına ait olan bir Azure AD kiracısı. Bu, bağdaştırıcı uygulama kimliğinin kayıtlı olduğu kiracıdır.

- **Karşılıklı müşteri** - Dynamics 365 Human Resources ve tümleştirme iş ortağının çözümünü uygulayan bir müşteri.

    - **Dynamics 365 Finance veya Human Resources** – Tümleştirilen sistemin gerektirdiği müşteri verilerini içeren müşteriye özel Dynamics 365 Finance veya Human Resources kurulumu.
    - **Dataverse** – Finance veya Human Resources'a bağlanan müşteriye özel Dataverse ortamı. Dataverse, Dynamics 365 verileriyle etkileşim için bir Web API'si sağlar.
    - **Azure AD kiracısı B** – Müşterinin Azure AD kiracısı. Kimlik sağlayıcı (yetkilendirme sunucusu) olarak çalışır ve müşterinin Dataverse kurulumunu aramak için arayanları yetkilendiren belirteçler düzenler.

## <a name="basic-request-flow"></a>Temel istek akışı

Bu bölümde, bir tümleştirmeye dahil edilen tipik bir isteğin temel akışı açıklanmıştır. Bu makalenin önceki bölümünde yer alan mimari diyagrama başvurur.

Tipik bir istek, bağdaştırıcının Dynamics 365 verileri için sorgu oluşturmasını ve sonra da bu verileri kaydetmesini ve tümleştirme sistemine eşitlemesini gerektirir.

1. Bağdaştırıcı ilgili verileri sorgulamak için Dataverse Web API'sini çağırır.

    > [!NOTE]
    > Kimlik doğrulama bir önkoşuldur ve belirteç alımı işlemin ana kısmıdır. Kimlik doğrulaması, [Sistem sınırlarında kimlik doğrulaması ve yetkilendirme](#authentication-and-authorization-at-system-boundaries) bölümünde açıklanmaktadır.

    Bu çağrı, sanal tablo aracılığıyla kullanıma sunulan uygulama verilerini sorgulamak üzere Dataverse Web API'sine karşı gerçekleştirilir. (Bkz. Diyagram "2. İlk Eşitleme" ve "3. Delta Eşitleme".)

2. Dataverse, sanal tabloyu Sanal varlık eklentisi (diyagramdaki "Sanal Tablo Ara Sunucusu") aracılığıyla sorgulayarak isteği işler. Dataverse isteği, Finance veya Human Resources veritabanında fiziksel olarak depolanan verileri sorgulamak için Finance veya Human Resources Sanal varlık hizmetine iletilir.
3. Finance veya Human Resources Sanal varlık hizmeti, sanal varlığa yapılan isteği Dataverse sanal varlığını destekleyen Finance veya Human Resources varlığındaki bir sorguya çevirir. Veriler veritabanından alınır, Dataverse varlık gösterimine geri çevrilir ve çağrıyı yapana geri gönderilir.
4. Bağdaştırıcı, gerekli tüm eşleme ve veri çevirisi işlemini tamamlar ve tümleştirilen sistem veritabanındaki verileri kalıcı hale getirmek için tümleştirilen sisteme çağrı yapar. (Bkz. Diyagram "4. Verileri kaydet".)

## <a name="authentication-and-authorization-at-system-boundaries"></a>Sistem sınırlarında kimlik doğrulama ve yetkilendirme

*Kimlik doğrulama*, bir kullanıcının veya uygulamanın kimliğinin kanıtlanmış olduğunu doğrular ve kullanıcının veya uygulamanın olduklarını söyledikleri kişi olduğunu onaylar. *Yetkilendirme*, kullanıcıya veya uygulamaya belirli uygulama düzeyinde izinlere erişme izni verir. Daha fazla bilgi için, bkz. [Kimlik doğrulama ve yetkilendirme](/azure/active-directory/develop/authentication-vs-authorization).

Bu makalenin önceki bölümünde yer alan mimari diyagramdaki birçok sistemler arası çağrı bağdaştırıcıyı içerir. Aşağıdaki çağrıları yapmak için bağdaştırıcının kendi kimliğini doğrulaması gerekir:

- Dataverse'e çağrı
- Tümleştirme sistemine çağrı

Diyagramdaki sistem sınırlarına bakın. Sistemlerin arasındaki her web isteğinin kimliğinin doğrulanması ve veri çağırana geri döndürülmeden önce uygulama düzeyinde yetkilendirme denetimleri geçilmesi gerekir. Finance veya Human Resources tarafından desteklenen bir Dynamics 365 sanal tablosuna yönelik bir istekte, kimlik doğrulama ve yetkilendirme denetimleri aşağıdaki sistem sınırlarında gerekli kılınır:

- Bağdaştırıcı ve Dataverse Web API'si (OData) uç noktası arasındaki çağrı
- Dataverse Sanal varlık eklentisi ile Finance veya Human Resources Sanal varlık hizmeti arasındaki çağrı

Her iki durumda da, önce kimlik doğrulama denetimleri yapılır. Ardından, kimliği doğrulanmış kullanıcı veya uygulamanın, istenen verileri almak için doğru uygulama düzeyi ayrıcalıklarına sahip olduğundan emin olmak için uygulama düzeyinde yetkilendirme denetimleri yapılır.

Dataverse'i çağırmak için kimlik doğrulaması, Dataverse'e yapılan web isteğine HTTP başlığı olarak dahil edilmesi gereken taşıyıcı belirteç aracılığıyla işlenir. Bağdaştırıcının, kiracı B Azure AD kurulumundan bir belirteç alması gerekir. (Bkz. Diyagram "1. Belirteç Al".) Azure AD, kimlik doğrulama akışında kimlik sağlayıcı olarak hareket eder.

Bağdaştırıcı, uygulama kimliğini (gizli anahtar olmayan, Azure AD kiracı A'da kayıtlı olduğu şekilde) ve yalnızca bağdaştırıcı uygulamasının sahip olduğu bir uygulama gizli anahtarı ve sertifika sağlayarak kimlik doğrulaması yapar.

Kullanıcı veya uygulama kimliği, Dataverse'e çağrılar yapmak için doğrulandıktan sonra, her bir istek için Dataverse düzeyinde yetkilendirme denetimleri gerçekleştirilir. Bu denetimler, çağrıyı yapanın (diyagramdaki belirtilen "\<guid A\>" olan bağdaştırıcı uygulamasının kimliği) uygun uygulama izinlerine sahip olmasını sağlar. Uygulama düzeyinde yetkilendirme, bağdaştırıcının uygulama kimliğini temsil eden bir uygulama kullanıcısı aracılığıyla Dataverse'de yönetilir. Uygulama düzeyindeki izinler, belirli Dataverse tanımlı uygulama rollerine erişim izni verilerek yönetilir. Bu roller, uygulamaya ayrıntılı ayrıcalıklar sağlar.

Daha ayrıntılı açıklama için bkz. [Birden çok kiracılı sunucudan sunucuya kimlik doğrulaması kullanma](/power-apps/developer/data-platform/use-multi-tenant-server-server-authentication).

Dataverse düzeyinde uygulama izni denetimleri geçirilirse Sanal varlık eklentisi, Finance veya Human Resources ortamındaki Sanal varlık hizmeti uç noktasına çağrı yapar. Bu çağrıyı yapmak için sunucular arası (S2S) kimlik doğrulaması kullanılır. Finance and Operations sanal veri kaynağı yapılandırması kaydında yapılandırılan kimliği ve gizli anahtarı kullanır.

![Korumalı alan ortamındaki Finance and Operations sanal veri kaynağı yapılandırması kaydı.](./media/sandbox.jpg)

Daha fazla bilgi için bkz. [Dataverse sanal varlıklarını yapılandırma](/dev-itpro/power-platform/admin-reference).

Dataverse Sanal varlık eklentisinden Finance veya Human Resources'a yapılan çağrı bağdaştırıcıdan Dataverse'e yapılan orijinal çağrının bağdaştırıcı kimliğini (mimari diyagramında tanımlanan "\<guid A\>" kimlik) içerir. Sanal varlık veri kaynağı doğru yapılandırılsa ve S2S kimlik doğrulama denetimleri geçilirse, Finance veya Human'taki Sanal varlık hizmeti sorguyu orijinal çağrı yapanın (bağdaştırıcı, \<guid A\>) bağlamında çalıştırır. Finance veya Human Resources düzeyindeki uygulama izni denetimleri (yetkilendirme), bağdaştırıcının sorgu aracılığıyla istenen veri varlıklarına erişmek için gerekli ayrıcalıklara sahip olmasını sağlamak amacıyla yapılır.

Finance ve Human Resources güvenliği aşağıdaki yollarla yönetilir:

1. Bağdaştırıcı kimliğini ( \<guid A\>) belirli bir Finance veya Human Resources kullanıcısına eşleyerek. Bu eşleme, **Azure Active Directory uygulamaları** sayfasında gerçekleştirilir. Daha fazla bilgi için bkz. [Harici uygulamanızı kaydetme](/dev-itpro/data-entities/services-home-page.md#register-your-external-application).
2. Finance veya Human Resources kullanıcısına uygun uygulama düzeyinde rolleri, görevleri ve ayrıcalıkları vererek. Daha fazla bilgi için bkz. [Rol tabanlı güvenlik](/dev-itpro/sysadmin/role-based-security).

Bağdaştırıcı uygulamasına (\<guid A\>) istenen verilere erişmek için gereken ayrıcalıklar verilirse, aşağıdaki olaylar gerçekleşir:

1. Sorgu çalıştırılır.
2. Veriler, Dataverse varlık sayfalarına geri çevrilir.
3. Veriler bağdaştırıcıya geri döndürülür.

> [!IMPORTANT]
> Geliştirme sırasında bağdaştırıcı, Yönetici rolüne sahip bir Finance veya Human Resources kullanıcısı kullanılarak çalıştırılabilir. Ancak, üretim ortamında bağdaştırıcı hiçbir zaman Yönetici ayrıcalıklarıyla çalıştırılmamalıdır.

## <a name="key-takeaways"></a>Önemli temel bilgiler

Sanal tablo ya da varlık mimarisinin bazı önemli etkileri aşağıda verilmektedir:

- Human Resources tarafından desteklenen sanal tabloların güvenlik yapılandırması Human Resources'ta yönetilir.
- Müşteri (Bu makalenin önceki bölümündeki mimari diyagramında "Karşılıklı müşteri"), tümleştirme bağdaştırıcısı kimliğine (diyagramda tanımlanan "\<guid A\>") verilen ayrıcalıklar üzerinde tam denetime sahiptir.
- Müşteri, Human Resources ortamının doğru güvenlik yapılandırmasına sahip olmasından sorumludur. Bağdaştırıcıyı oluşturan tümleştirme iş ortağı, bağdaştırıcının gerektirdiği ayrıcalıklar hakkında rehberlik sağlamalıdır.

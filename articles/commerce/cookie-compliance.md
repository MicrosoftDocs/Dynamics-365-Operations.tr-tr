---
title: Çerez uyumluluğu
description: Bu konu, tanımlama bilgisi uyumu ve Microsoft Dynamics 365 Commerce'in içerdiği varsayılan ilkelerin dikkate alınması konularını açıklamaktadır.
author: BrianShook
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4f54b9b8130a167dbecdb13fccd7039f827f6ed0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416326"
---
# <a name="cookie-compliance"></a><span data-ttu-id="424b4-103">Çerez uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="424b4-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="424b4-104">Bu konu, tanımlama bilgisi uyumu ve Microsoft Dynamics 365 Commerce'in içerdiği varsayılan ilkelerin dikkate alınması konularını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="424b4-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="424b4-105">Özet</span><span class="sxs-lookup"><span data-stu-id="424b4-105">Overview</span></span>

<span data-ttu-id="424b4-106">E-ticaret müşterilerini etkileyen izleme teknolojileri kullanıldığında, gizlilik önemli bir etkendir.</span><span class="sxs-lookup"><span data-stu-id="424b4-106">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="424b4-107">Avrupa Birliği (AB) içindeki genel veri koruma düzenlemesi (GDPR) gibi gizlilik uyumluluk standartları nedeniyle, günümüzde etkin olan tüm siteler için elektronik gizlilik yönergeleri dikkate alınmalıdır.</span><span class="sxs-lookup"><span data-stu-id="424b4-107">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="424b4-108">Birçok e-ticaret sitesine varsayılan olarak genel erişim sağlandığından, e-ticaret sitenizin uyumluluk standartlarını incelemeniz önemlidir.</span><span class="sxs-lookup"><span data-stu-id="424b4-108">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="424b4-109">Microsoft'un çerez uyumluluğu için kullandığı temel ilkeler hakkında daha fazla bilgi için [Microsoft Güven Merkezi](https://www.microsoft.com/trust-center)'ni ziyaret edin.</span><span class="sxs-lookup"><span data-stu-id="424b4-109">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="424b4-110">Aynı zamanda, uyumluluk ve gizlilik alanları hakkında daha fazla bilgi edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="424b4-110">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="424b4-111">Aşağıdaki tabloda, Dynamics 365 Commerce siteleri tarafından yerleştirilen tanımlama bilgilerine ilişkin geçerli başvuru listesi gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="424b4-111">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="424b4-112">Tanımlama bilgisi adı</span><span class="sxs-lookup"><span data-stu-id="424b4-112">Cookie name</span></span>                               | <span data-ttu-id="424b4-113">Kullanım</span><span class="sxs-lookup"><span data-stu-id="424b4-113">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="424b4-114">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="424b4-114">.AspNet.Cookies</span></span>                             | <span data-ttu-id="424b4-115">Çoklu oturum açma (SSO) için Microsoft Azure Active Directory (Azure AD) kimlik doğrulama bilgilerini depolar.</span><span class="sxs-lookup"><span data-stu-id="424b4-115">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="424b4-116">Şifreli kullanıcı asıl bilgisini depolar (adı, soyadı, eposta).</span><span class="sxs-lookup"><span data-stu-id="424b4-116">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="424b4-117">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="424b4-117">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="424b4-118">Sepet örneğine eklenen ürünlerin listesini almak için kullanılan alışveriş sepeti kodunu depolar.</span><span class="sxs-lookup"><span data-stu-id="424b4-118">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="424b4-119">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="424b4-119">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="424b4-120">Tanımlama bilgisi uyumluluk onayı izleme.</span><span class="sxs-lookup"><span data-stu-id="424b4-120">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="424b4-121">ai_session</span><span class="sxs-lookup"><span data-stu-id="424b4-121">ai_session</span></span>                                  | <span data-ttu-id="424b4-122">Uygulamanın belirli sayfalarını ve özelliklerini içeren kaç kullanıcı etkinliği oturumu olduğunu saptar.</span><span class="sxs-lookup"><span data-stu-id="424b4-122">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="424b4-123">ai_user</span><span class="sxs-lookup"><span data-stu-id="424b4-123">ai_user</span></span>                                     | <span data-ttu-id="424b4-124">Uygulamayı ve özelliklerini kaç kişinin kullanmış olduğunu saptar.</span><span class="sxs-lookup"><span data-stu-id="424b4-124">Detects how many people used the app and its features.</span></span> <span data-ttu-id="424b4-125">Kullanıcılar anonim kimlikler kullanılarak sayılır.</span><span class="sxs-lookup"><span data-stu-id="424b4-125">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="424b4-126">b2cru</span><span class="sxs-lookup"><span data-stu-id="424b4-126">b2cru</span></span>                                       | <span data-ttu-id="424b4-127">Yeniden yönlendirme URL'sini dinamik olarak depolar.</span><span class="sxs-lookup"><span data-stu-id="424b4-127">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="424b4-128">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="424b4-128">JSESSIONID</span></span>                                  | <span data-ttu-id="424b4-129">Adyen ödeme bağlayıcısı tarafından kullanıcı oturumunu depolamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="424b4-129">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="424b4-130">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="424b4-130">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="424b4-131">Kimlik Doğrulama</span><span class="sxs-lookup"><span data-stu-id="424b4-131">Authentication</span></span>                                               |
| <span data-ttu-id="424b4-132">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="424b4-132">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="424b4-133">İstek durumunu korumak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="424b4-133">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="424b4-134">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="424b4-134">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="424b4-135">CRSF koruması için kullanılan siteler arası istek sahteciliği (CRSF) belirteci.</span><span class="sxs-lookup"><span data-stu-id="424b4-135">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="424b4-136">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="424b4-136">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="424b4-137">İstekleri uygun üretim kimlik doğrulama sunucusu örneğine yönlendirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="424b4-137">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="424b4-138">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="424b4-138">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="424b4-139">İstekleri uygun üretim kimlik doğrulama sunucusu örneğine yönlendirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="424b4-139">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="424b4-140">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="424b4-140">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="424b4-141">İstekleri uygun üretim kimlik doğrulama sunucusu örneğine yönlendirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="424b4-141">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="424b4-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="424b4-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="424b4-143">SSO oturumunu sürdürmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="424b4-143">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="424b4-144">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="424b4-144">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="424b4-145">Geçerli hareket dahil olmak üzere hareketleri izlemek için kullanılır (işletme tüketici arası (B2C) sitede kimlik doğrulaması yapan açık sekme sayısı).</span><span class="sxs-lookup"><span data-stu-id="424b4-145">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="424b4-146">Bir e-ticaret sitesinde site kullanıcısı tanımlama bilgisi izni</span><span class="sxs-lookup"><span data-stu-id="424b4-146">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="424b4-147">Bir e-ticaret sitesi özelliği veya modülü gerekli olmayan bir tanımlama bilgisi kullanırsa, tanımlama bilgisi izlenmeden önce site kullanıcısının onayı alınmalıdır.</span><span class="sxs-lookup"><span data-stu-id="424b4-147">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="424b4-148">Site kullanıcılarına e-ticaret sitesinde tanımlama bilgisi izni sağlamasına olanak vermek için, site yazarı sayfanın üst bilgi modülüne, izin sorulmasını ve alınmasını sağlamak amacıyla bir tanımlama bilgisi izin modülü ekleyip yapılandırmalıdır.</span><span class="sxs-lookup"><span data-stu-id="424b4-148">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="424b4-149">Site kullanıcısı izni, sitenin bir sayfasında gerekli olmayan tanımlama bilgilerini kullanan bir özellik veya modülle ilgili olarak verilmelidir.</span><span class="sxs-lookup"><span data-stu-id="424b4-149">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="424b4-150">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="424b4-150">Additional resources</span></span>

[<span data-ttu-id="424b4-151">Erişilebilirlik özellikleri ve yetenekleri</span><span class="sxs-lookup"><span data-stu-id="424b4-151">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="424b4-152">Uyumluluğa genel bakış</span><span class="sxs-lookup"><span data-stu-id="424b4-152">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="424b4-153">Gizlilik ilkesi sayfası ekleme</span><span class="sxs-lookup"><span data-stu-id="424b4-153">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="424b4-154">İzlenen içerik değişiklikleriyle ilişkili kullanıcı kimliklerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="424b4-154">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="424b4-155">Tanımlama bilgisi izin modülü</span><span class="sxs-lookup"><span data-stu-id="424b4-155">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="424b4-156">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="424b4-156">Header module</span></span>](author-header-module.md)

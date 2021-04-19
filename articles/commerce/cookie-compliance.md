---
title: Çerez uyumluluğu
description: Bu konu, tanımlama bilgisi uyumu ve Microsoft Dynamics 365 Commerce'in içerdiği varsayılan ilkelerin dikkate alınması konularını açıklamaktadır.
author: BrianShook
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2cc2089bc3052c0c59cb0414f8301123a9a30df2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796039"
---
# <a name="cookie-compliance"></a><span data-ttu-id="a7e2f-103">Çerez uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="a7e2f-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a7e2f-104">Bu konu, tanımlama bilgisi uyumu ve Microsoft Dynamics 365 Commerce'in içerdiği varsayılan ilkelerin dikkate alınması konularını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a7e2f-105">E-ticaret müşterilerini etkileyen izleme teknolojileri kullanıldığında, gizlilik önemli bir etkendir.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-105">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="a7e2f-106">Avrupa Birliği (AB) içindeki genel veri koruma düzenlemesi (GDPR) gibi gizlilik uyumluluk standartları nedeniyle, günümüzde etkin olan tüm siteler için elektronik gizlilik yönergeleri dikkate alınmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-106">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="a7e2f-107">Birçok e-ticaret sitesine varsayılan olarak genel erişim sağlandığından, e-ticaret sitenizin uyumluluk standartlarını incelemeniz önemlidir.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-107">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="a7e2f-108">Microsoft'un çerez uyumluluğu için kullandığı temel ilkeler hakkında daha fazla bilgi için [Microsoft Güven Merkezi](https://www.microsoft.com/trust-center)'ni ziyaret edin.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-108">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="a7e2f-109">Aynı zamanda, uyumluluk ve gizlilik alanları hakkında daha fazla bilgi edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-109">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="a7e2f-110">Aşağıdaki tabloda, Dynamics 365 Commerce siteleri tarafından yerleştirilen tanımlama bilgilerine ilişkin geçerli başvuru listesi gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-110">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="a7e2f-111">Tanımlama bilgisi adı</span><span class="sxs-lookup"><span data-stu-id="a7e2f-111">Cookie name</span></span>                               | <span data-ttu-id="a7e2f-112">Kullanım</span><span class="sxs-lookup"><span data-stu-id="a7e2f-112">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="a7e2f-113">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="a7e2f-113">.AspNet.Cookies</span></span>                             | <span data-ttu-id="a7e2f-114">Çoklu oturum açma (SSO) için Microsoft Azure Active Directory (Azure AD) kimlik doğrulama bilgilerini depolar.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-114">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="a7e2f-115">Şifreli kullanıcı asıl bilgisini depolar (adı, soyadı, eposta).</span><span class="sxs-lookup"><span data-stu-id="a7e2f-115">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="a7e2f-116">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="a7e2f-116">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="a7e2f-117">Sepet örneğine eklenen ürünlerin listesini almak için kullanılan alışveriş sepeti kodunu depolar.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-117">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="a7e2f-118">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="a7e2f-118">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="a7e2f-119">Tanımlama bilgisi uyumluluk onayı izleme.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-119">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="a7e2f-120">ai_session</span><span class="sxs-lookup"><span data-stu-id="a7e2f-120">ai_session</span></span>                                  | <span data-ttu-id="a7e2f-121">Uygulamanın belirli sayfalarını ve özelliklerini içeren kaç kullanıcı etkinliği oturumu olduğunu saptar.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-121">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="a7e2f-122">ai_user</span><span class="sxs-lookup"><span data-stu-id="a7e2f-122">ai_user</span></span>                                     | <span data-ttu-id="a7e2f-123">Uygulamayı ve özelliklerini kaç kişinin kullanmış olduğunu saptar.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-123">Detects how many people used the app and its features.</span></span> <span data-ttu-id="a7e2f-124">Kullanıcılar anonim kimlikler kullanılarak sayılır.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-124">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="a7e2f-125">b2cru</span><span class="sxs-lookup"><span data-stu-id="a7e2f-125">b2cru</span></span>                                       | <span data-ttu-id="a7e2f-126">Yeniden yönlendirme URL'sini dinamik olarak depolar.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-126">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="a7e2f-127">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="a7e2f-127">JSESSIONID</span></span>                                  | <span data-ttu-id="a7e2f-128">Adyen ödeme bağlayıcısı tarafından kullanıcı oturumunu depolamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-128">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="a7e2f-129">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="a7e2f-129">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="a7e2f-130">Kimlik Doğrulama</span><span class="sxs-lookup"><span data-stu-id="a7e2f-130">Authentication</span></span>                                               |
| <span data-ttu-id="a7e2f-131">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="a7e2f-131">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="a7e2f-132">İstek durumunu korumak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-132">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="a7e2f-133">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="a7e2f-133">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="a7e2f-134">CRSF koruması için kullanılan siteler arası istek sahteciliği (CRSF) belirteci.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-134">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="a7e2f-135">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="a7e2f-135">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="a7e2f-136">İstekleri uygun üretim kimlik doğrulama sunucusu örneğine yönlendirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-136">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="a7e2f-137">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="a7e2f-137">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="a7e2f-138">İstekleri uygun üretim kimlik doğrulama sunucusu örneğine yönlendirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-138">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="a7e2f-139">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="a7e2f-139">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="a7e2f-140">İstekleri uygun üretim kimlik doğrulama sunucusu örneğine yönlendirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-140">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="a7e2f-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="a7e2f-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="a7e2f-142">SSO oturumunu sürdürmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-142">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="a7e2f-143">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="a7e2f-143">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="a7e2f-144">Geçerli hareket dahil olmak üzere hareketleri izlemek için kullanılır (işletme tüketici arası (B2C) sitede kimlik doğrulaması yapan açık sekme sayısı).</span><span class="sxs-lookup"><span data-stu-id="a7e2f-144">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="a7e2f-145">Bir e-ticaret sitesinde site kullanıcısı tanımlama bilgisi izni</span><span class="sxs-lookup"><span data-stu-id="a7e2f-145">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="a7e2f-146">Bir e-ticaret sitesi özelliği veya modülü gerekli olmayan bir tanımlama bilgisi kullanırsa, tanımlama bilgisi izlenmeden önce site kullanıcısının onayı alınmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-146">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="a7e2f-147">Site kullanıcılarına e-ticaret sitesinde tanımlama bilgisi izni sağlamasına olanak vermek için, site yazarı sayfanın üst bilgi modülüne, izin sorulmasını ve alınmasını sağlamak amacıyla bir tanımlama bilgisi izin modülü ekleyip yapılandırmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-147">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="a7e2f-148">Site kullanıcısı izni, sitenin bir sayfasında gerekli olmayan tanımlama bilgilerini kullanan bir özellik veya modülle ilgili olarak verilmelidir.</span><span class="sxs-lookup"><span data-stu-id="a7e2f-148">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a7e2f-149">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a7e2f-149">Additional resources</span></span>

[<span data-ttu-id="a7e2f-150">Erişilebilirlik özellikleri ve yetenekleri</span><span class="sxs-lookup"><span data-stu-id="a7e2f-150">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="a7e2f-151">Uyumluluğa genel bakış</span><span class="sxs-lookup"><span data-stu-id="a7e2f-151">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="a7e2f-152">Gizlilik ilkesi sayfası ekleme</span><span class="sxs-lookup"><span data-stu-id="a7e2f-152">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="a7e2f-153">İzlenen içerik değişiklikleriyle ilişkili kullanıcı kimliklerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="a7e2f-153">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="a7e2f-154">Tanımlama bilgisi izin modülü</span><span class="sxs-lookup"><span data-stu-id="a7e2f-154">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="a7e2f-155">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="a7e2f-155">Header module</span></span>](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

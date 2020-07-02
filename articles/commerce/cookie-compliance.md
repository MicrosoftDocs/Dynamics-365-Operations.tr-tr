---
title: Çerez uyumluluğu
description: Bu konu, tanımlama bilgisi uyumu ve Microsoft Dynamics 365 Commerce'in içerdiği varsayılan ilkelerin dikkate alınması konularını açıklamaktadır.
author: BrianShook
manager: annbe
ms.date: 06/12/2020
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
ms.openlocfilehash: e1fa016dc9f46b048220f0f83e4b0783087de91e
ms.sourcegitcommit: c66c4c67a21e7d7d3a94a3fd766c3184b6e65c4e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/12/2020
ms.locfileid: "3446925"
---
# <a name="cookie-compliance"></a><span data-ttu-id="5e5f5-103">Çerez uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="5e5f5-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5e5f5-104">Bu konu, tanımlama bilgisi uyumu ve Microsoft Dynamics 365 Commerce'in içerdiği varsayılan ilkelerin dikkate alınması konularını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="5e5f5-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5e5f5-105">Özet</span><span class="sxs-lookup"><span data-stu-id="5e5f5-105">Overview</span></span>

<span data-ttu-id="5e5f5-106">E-ticaret müşterilerini etkileyen izleme teknolojileri kullanıldığında, gizlilik önemli bir etkendir.</span><span class="sxs-lookup"><span data-stu-id="5e5f5-106">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="5e5f5-107">Avrupa Birliği (AB) içindeki genel veri koruma düzenlemesi (GDPR) gibi gizlilik uyumluluk standartları nedeniyle, günümüzde etkin olan tüm siteler için elektronik gizlilik yönergeleri dikkate alınmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5e5f5-107">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="5e5f5-108">Birçok e-ticaret sitesine varsayılan olarak genel erişim sağlandığından, e-ticaret sitenizin uyumluluk standartlarını incelemeniz önemlidir.</span><span class="sxs-lookup"><span data-stu-id="5e5f5-108">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="5e5f5-109">Microsoft'un çerez uyumluluğu için kullandığı temel ilkeler hakkında daha fazla bilgi için [Microsoft Güven Merkezi](https://www.microsoft.com/trust-center)'ni ziyaret edin.</span><span class="sxs-lookup"><span data-stu-id="5e5f5-109">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="5e5f5-110">Aynı zamanda, uyumluluk ve gizlilik alanları hakkında daha fazla bilgi edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5e5f5-110">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="5e5f5-111">Aşağıdaki tabloda, Dynamics 365 Commerce siteleri tarafından yerleştirilen tanımlama bilgilerine ilişkin geçerli başvuru listesi gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="5e5f5-111">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="5e5f5-112">Tanımlama bilgisi adı</span><span class="sxs-lookup"><span data-stu-id="5e5f5-112">Cookie name</span></span>                               | <span data-ttu-id="5e5f5-113">Kullanım</span><span class="sxs-lookup"><span data-stu-id="5e5f5-113">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="5e5f5-114">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="5e5f5-114">.AspNet.Cookies</span></span>                             | <span data-ttu-id="5e5f5-115">Çoklu oturum açma (SSO) için Microsoft Azure Active Directory (Azure AD) kimlik doğrulama bilgilerini depolar.</span><span class="sxs-lookup"><span data-stu-id="5e5f5-115">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="5e5f5-116">Şifreli kullanıcı asıl bilgisini depolar (adı, soyadı, eposta).</span><span class="sxs-lookup"><span data-stu-id="5e5f5-116">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="5e5f5-117">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="5e5f5-117">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="5e5f5-118">Sepet örneğine eklenen ürünlerin listesini almak için kullanılan alışveriş sepeti kodunu depolar.</span><span class="sxs-lookup"><span data-stu-id="5e5f5-118">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="5e5f5-119">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="5e5f5-119">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="5e5f5-120">Tanımlama bilgisi uyumluluk onayı izleme.</span><span class="sxs-lookup"><span data-stu-id="5e5f5-120">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="5e5f5-121">ai_session</span><span class="sxs-lookup"><span data-stu-id="5e5f5-121">ai_session</span></span>                                  | <span data-ttu-id="5e5f5-122">Uygulamanın belirli sayfalarını ve özelliklerini içeren kaç kullanıcı etkinliği oturumu olduğunu saptar.</span><span class="sxs-lookup"><span data-stu-id="5e5f5-122">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="5e5f5-123">ai_user</span><span class="sxs-lookup"><span data-stu-id="5e5f5-123">ai_user</span></span>                                     | <span data-ttu-id="5e5f5-124">Uygulamayı ve özelliklerini kaç kişinin kullanmış olduğunu saptar.</span><span class="sxs-lookup"><span data-stu-id="5e5f5-124">Detects how many people used the app and its features.</span></span> <span data-ttu-id="5e5f5-125">Kullanıcılar anonim kimlikler kullanılarak sayılır.</span><span class="sxs-lookup"><span data-stu-id="5e5f5-125">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="5e5f5-126">b2cru</span><span class="sxs-lookup"><span data-stu-id="5e5f5-126">b2cru</span></span>                                       | <span data-ttu-id="5e5f5-127">Yeniden yönlendirme URL'sini dinamik olarak depolar.</span><span class="sxs-lookup"><span data-stu-id="5e5f5-127">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="5e5f5-128">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="5e5f5-128">JSESSIONID</span></span>                                  | <span data-ttu-id="5e5f5-129">Adyen ödeme bağlayıcısı tarafından kullanıcı oturumunu depolamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5e5f5-129">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="5e5f5-130">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="5e5f5-130">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="5e5f5-131">Kimlik Doğrulama</span><span class="sxs-lookup"><span data-stu-id="5e5f5-131">Authentication</span></span>                                               |
| <span data-ttu-id="5e5f5-132">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="5e5f5-132">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="5e5f5-133">İstek durumunu korumak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5e5f5-133">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="5e5f5-134">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="5e5f5-134">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="5e5f5-135">CRSF koruması için kullanılan siteler arası istek sahteciliği (CRSF) belirteci.</span><span class="sxs-lookup"><span data-stu-id="5e5f5-135">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="5e5f5-136">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="5e5f5-136">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="5e5f5-137">İstekleri uygun üretim kimlik doğrulama sunucusu örneğine yönlendirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5e5f5-137">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="5e5f5-138">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="5e5f5-138">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="5e5f5-139">İstekleri uygun üretim kimlik doğrulama sunucusu örneğine yönlendirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5e5f5-139">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="5e5f5-140">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="5e5f5-140">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="5e5f5-141">İstekleri uygun üretim kimlik doğrulama sunucusu örneğine yönlendirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5e5f5-141">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="5e5f5-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="5e5f5-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="5e5f5-143">SSO oturumunu sürdürmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5e5f5-143">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="5e5f5-144">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="5e5f5-144">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="5e5f5-145">Geçerli hareket dahil olmak üzere hareketleri izlemek için kullanılır (işletme tüketici arası (B2C) sitede kimlik doğrulaması yapan açık sekme sayısı).</span><span class="sxs-lookup"><span data-stu-id="5e5f5-145">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="5e5f5-146">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="5e5f5-146">Additional resources</span></span>

[<span data-ttu-id="5e5f5-147">Erişilebilirlik özellikleri ve yetenekleri</span><span class="sxs-lookup"><span data-stu-id="5e5f5-147">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="5e5f5-148">Uyumluluğa genel bakış</span><span class="sxs-lookup"><span data-stu-id="5e5f5-148">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="5e5f5-149">Gizlilik ilkesi sayfası ekleme</span><span class="sxs-lookup"><span data-stu-id="5e5f5-149">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="5e5f5-150">İzlenen içerik değişiklikleriyle ilişkili kullanıcı kimliklerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="5e5f5-150">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

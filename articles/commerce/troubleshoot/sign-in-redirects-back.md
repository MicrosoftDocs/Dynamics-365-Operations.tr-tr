---
title: Oturum açma bağlantısı yeniden e-ticaret sitesine yönlendiriyor
description: Bu konu, oturum açma bağlantısının oturum açma sayfasına gitmek yerine e-ticaret sitesine geri yönlendirmesine yardımcı olabilecek sorun giderme kılavuzu sağlar.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a1d0ae4e487c391020947c607d5d7cb5d1ba6af4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020615"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a><span data-ttu-id="ad4c4-103">Oturum açma bağlantısı yeniden e-ticaret sitesine yönlendiriyor</span><span class="sxs-lookup"><span data-stu-id="ad4c4-103">Sign-in link redirects back to an e-commerce site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ad4c4-104">Bu konu, oturum açma bağlantısının oturum açma sayfasına gitmek yerine e-ticaret sitesine geri yönlendirmesine yardımcı olabilecek sorun giderme kılavuzu sağlar.</span><span class="sxs-lookup"><span data-stu-id="ad4c4-104">This topic provides troubleshooting guidance that can help when a sign-in link redirects back to the e-commerce site instead of going to the sign-in page.</span></span>

## <a name="description"></a><span data-ttu-id="ad4c4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad4c4-105">Description</span></span>

<span data-ttu-id="ad4c4-106">Commerce Site Builder'da yeni bir Microsoft Azure Active Directory B2C (Azure AD B2C) kiracısı yapılandırdıktan sonra, **Oturum aç** bağlantısını seçen kullanıcılar oturum açma sayfasına gitmeden ana e-ticaret açılış sayfasına geri yönlendiriliyor.</span><span class="sxs-lookup"><span data-stu-id="ad4c4-106">After you configure a new Microsoft Azure Active Directory B2C (Azure AD B2C) tenant in Commerce site builder, users who select the **Sign in** link are redirected back to the main e-commerce landing page without going to the sign-in page.</span></span>

## <a name="resolution"></a><span data-ttu-id="ad4c4-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="ad4c4-107">Resolution</span></span>

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a><span data-ttu-id="ad4c4-108">Azure AD B2C uygulamasında yanıt URL'sinin doğru yapılandırıldığını onaylayın</span><span class="sxs-lookup"><span data-stu-id="ad4c4-108">Confirm that the reply URL is correctly configured in the Azure AD B2C application</span></span>

<span data-ttu-id="ad4c4-109">Azure AD B2C uygulamasında yanıt URL'sinin doğru yapılandırıldığını onaylamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ad4c4-109">To confirm that the reply URL is correctly configured in the Azure AD B2C application, follow these steps.</span></span>

1. <span data-ttu-id="ad4c4-110">[Azure portal](https://portal.azure.com/)'a gidin.</span><span class="sxs-lookup"><span data-stu-id="ad4c4-110">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="ad4c4-111">Sitenizin erişimi için oluşturduğunuz Azure AD B2C uygulamasını seçin.</span><span class="sxs-lookup"><span data-stu-id="ad4c4-111">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="ad4c4-112">Azure AD B2C kurulumu sırasında oluşturduğunuz uygulamayı seçin.</span><span class="sxs-lookup"><span data-stu-id="ad4c4-112">Select the application that you created during the Azure AD B2C setup.</span></span>
1. <span data-ttu-id="ad4c4-113">**Yanıt URL'si** altında, aşağıdaki resimdeki örnekte gösterildiği gibi, listenin hem site etki alanı URL'si hem de e-ticaret tarafından oluşturulan URL girdilerini içerdiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="ad4c4-113">Under **Reply URL**, make sure that the list includes entries for both the site domain URL and the e-commerce-generated URL, as shown in the example in the following illustration.</span></span>

    ![Azure AD B2C yanıt URL'si girişleri](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> <span data-ttu-id="ad4c4-115">Hem site etki alanı URL'si hem de e-ticaret tarafından oluşturulan URL, başta veya sonda eğik çizgiler içermeyen geçerli bir URL biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ad4c4-115">Both the site domain URL and the e-commerce-generated URL must be in a valid URL format that doesn't include leading or trailing slashes.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad4c4-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ad4c4-116">Additional resources</span></span>

[<span data-ttu-id="ad4c4-117">Azure Active Directory B2C'de web uygulamasını kaydetme</span><span class="sxs-lookup"><span data-stu-id="ad4c4-117">Register a web application in Azure Active Directory B2C</span></span>](/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[<span data-ttu-id="ad4c4-118">Commerce'ta B2C kiracısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="ad4c4-118">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)
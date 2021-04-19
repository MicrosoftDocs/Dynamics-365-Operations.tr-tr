---
title: Test veya geliştirme sırasında mağazaya erişimi sınırlama
description: Bu konu mağaza içi test veya geliştirme gerçekleştirilirken Microsoft Dynamics 365 Commerce mağazasına erişimin nasıl kısıtlanacağını açıklamaktadır.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: f5cba6b7ff3aa65441c932e72fa458bda0d0fc69
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801543"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a><span data-ttu-id="025e0-103">Test veya geliştirme sırasında mağazaya erişimi sınırlama</span><span class="sxs-lookup"><span data-stu-id="025e0-103">Restrict access to a storefront during testing or development</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="025e0-104">Bu konu mağaza içi test veya geliştirme gerçekleştirilirken Microsoft Dynamics 365 Commerce mağazasına erişimin nasıl kısıtlanacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="025e0-104">This topic explains how to restrict access to a Microsoft Dynamics 365 Commerce storefront while internal testing or development is occurring.</span></span>

## <a name="description"></a><span data-ttu-id="025e0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="025e0-105">Description</span></span>

<span data-ttu-id="025e0-106">Mağaza içi test veya etkin geliştirme sırasında, harici kullanıcıların yayınlanan mağaza sayfalarına erişmesini engellemek için sitenize erişimi kısıtlamak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="025e0-106">During internal testing or active development, you might want to restrict access to your site to prevent external users from accessing the published storefront pages.</span></span>

## <a name="resolution"></a><span data-ttu-id="025e0-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="025e0-107">Resolution</span></span>

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a><span data-ttu-id="025e0-108">Standart Kullanıcı akışlarını kullanarak Azure AD B2C'yi ayarlama</span><span class="sxs-lookup"><span data-stu-id="025e0-108">Set up Azure AD B2C by using standard user flows</span></span>

<span data-ttu-id="025e0-109">E-Ticaret siteniz için Azure Active Directory B2C'yi (Azure AD B2C) yapılandırma hakkında bilgi için, bkz. [Commerce'te B2C kiracısı ayarlama](../set-up-b2c-tenant.md).</span><span class="sxs-lookup"><span data-stu-id="025e0-109">For information about how to configure Azure Active Directory B2C (Azure AD B2C) for your e-commerce site, see [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md).</span></span>

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a><span data-ttu-id="025e0-110">Mağaza sayfalara Kullanıcı erişimini kısıtlama ve yeni kullanıcıların oluşturulmasını engelleme</span><span class="sxs-lookup"><span data-stu-id="025e0-110">Restrict user access to storefront pages and block the creation of new users</span></span>

<span data-ttu-id="025e0-111">Commerce Site Builder'da mağaza sayfalarına Kullanıcı erişimini kısıtlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="025e0-111">To restrict user access to storefront pages in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="025e0-112">Sitenize gidin.</span><span class="sxs-lookup"><span data-stu-id="025e0-112">Go to your site.</span></span>
1. <span data-ttu-id="025e0-113">**Sayfaları** seçin ve sonra da kullanıcı erişimini kısıtlayacağınız sayfayı seçin.</span><span class="sxs-lookup"><span data-stu-id="025e0-113">Select **Pages**, and then select the page to restrict user access for.</span></span>
1. <span data-ttu-id="025e0-114">Modül veya parça yuvasını seçin ve ardından **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="025e0-114">Select the module or fragment slot, and then select **Edit**.</span></span>
1. <span data-ttu-id="025e0-115">Özellikler bölmesinde, **Oturum açılması gerekiyor mu?** seçeneğini belirleyin ve sonra **düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="025e0-115">In the properties pane, select **Requires sign-in?**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="025e0-116">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="025e0-116">Select **Publish**.</span></span>

<span data-ttu-id="025e0-117">Azure AD'de yeni kullanıcıların oluşturulmasını engellemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="025e0-117">To block the creation of new users in Azure AD, follow these steps.</span></span>

1. <span data-ttu-id="025e0-118">[Azure portal](https://portal.azure.com/)'a gidin.</span><span class="sxs-lookup"><span data-stu-id="025e0-118">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="025e0-119">Sitenizin erişimi için oluşturduğunuz Azure AD B2C uygulamasını seçin.</span><span class="sxs-lookup"><span data-stu-id="025e0-119">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="025e0-120">Soldaki gezinti bölmesinde **Kullanıcı akışlarını** seçin.</span><span class="sxs-lookup"><span data-stu-id="025e0-120">In the left navigation, select **User flows**.</span></span>
1. <span data-ttu-id="025e0-121">**Kullanıcı akışları** sayfasında, **Yeni Kullanıcı Akışı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="025e0-121">At the top of the **User Flows** page, select **New user flow**.</span></span>
1. <span data-ttu-id="025e0-122">**Bir Kullanıcı akış türü seçin** sayfasında, **önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="025e0-122">On the **Select a user flow type** page, select **Preview**.</span></span>
1. <span data-ttu-id="025e0-123">Sayfanın ortasında, **oturum aç: v2** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="025e0-123">In the middle of the page, select **Sign in v2**.</span></span> <span data-ttu-id="025e0-124">Daha sonra, test veya geliştirme sırasında akışı Azure AD B2C için sitenizin standart Kullanıcı akışı olarak yapılandırmak için, [Commerce'te bir B2C kiracısı ayarlama](../set-up-b2c-tenant.md) adımlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="025e0-124">Then follow the steps in [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md) to configure the flow as your site's standard user flow for Azure AD B2C during testing or development.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="025e0-125">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="025e0-125">Additional resources</span></span>

[<span data-ttu-id="025e0-126">Commerce'ta B2C kiracısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="025e0-126">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)

[<span data-ttu-id="025e0-127">Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama</span><span class="sxs-lookup"><span data-stu-id="025e0-127">Set up custom pages for user sign-ins</span></span>](../custom-pages-user-logins.md)

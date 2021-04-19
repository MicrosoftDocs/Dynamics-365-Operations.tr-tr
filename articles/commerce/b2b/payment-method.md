---
title: B2B e-ticaret siteleri için müşteri hesabı ödeme yöntemini yapılandırma
description: Bu konuda, B2B e-ticaret siteleri için müşteri hesabı ödeme yönteminin nasıl yapılandırılacağı açıklanmaktadır.
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 62e8f4949dcea1cb201bece171991047ce28da04
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799817"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a><span data-ttu-id="8f565-103">B2B e-ticaret siteleri için müşteri hesabı ödeme yöntemini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="8f565-103">Configure the customer account payment method for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8f565-104">Bu konuda, B2B e-ticaret siteleri için müşteri hesabı ödeme yönteminin nasıl yapılandırılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="8f565-104">This topic describes how to configure the customer account payment method for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="8f565-105">Perakendeciler, e-ticaret kanalında sattıkları ürünler ve hizmetler karşılığında çeşitli türlerde ödemeler kabul edebilirler.</span><span class="sxs-lookup"><span data-stu-id="8f565-105">Retailers can accept various types of payment in exchange for the products and services that they sell in an e-commerce channel.</span></span> <span data-ttu-id="8f565-106">Perakendecinin kabul edeceği ödeme türlerinin her biri, sistem ayarlandığında Microsoft Dynamics 365 Commerce'te yapılandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8f565-106">Each payment type that a retailer accepts must be configured in Microsoft Dynamics 365 Commerce when the system is set up.</span></span> <span data-ttu-id="8f565-107">Müşteri hesabı (veya "açık hesap") ödeme yöntemi, B2B e-ticaret sitelerinde desteklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="8f565-107">The customer account (or "on account") payment method must be supported on B2B e-commerce sites.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="8f565-108">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="8f565-108">Prerequisites</span></span>

1. <span data-ttu-id="8f565-109">Müşteri hesabı ödeme yöntemini Commerce Headquarters'a ekleyin.</span><span class="sxs-lookup"><span data-stu-id="8f565-109">Add the customer account payment method in Commerce headquarters.</span></span>
2. <span data-ttu-id="8f565-110">Müşteri hesabı ödeme yöntemini e-ticaret kanalıyla ilişkilendirin.</span><span class="sxs-lookup"><span data-stu-id="8f565-110">Associate the customer account payment method with the e-commerce channel.</span></span>
3. <span data-ttu-id="8f565-111">Commerce Headquarters'da **Perakende ve Ticaret \> Müşteriler \> Tüm müşteriler \> Ödeme varsayılanları** bölümünde müşteri için **Açık hesaba izin ver**'in etkinleştirildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="8f565-111">Make sure that **Allow on account** is enabled for the customer at **Retail and Commerce \> Customers \> All customers \> Payment defaults** in Commerce headquarters.</span></span> <span data-ttu-id="8f565-112">Ayrıca, Commerce Headquarters'da **Perakende ve Ticaret \> Müşteriler \> Tüm müşteriler \>Kredi ve Tahsilatlar**'da **Kredi limiti** parametrelerinin müşteri için uygun şekilde ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="8f565-112">Also make sure that **Credit limit** parameters are set appropriately for the customer at **Retail and Commerce \> Customers \> All customers \> Credit and Collections** in Commerce headquarters.</span></span> 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a><span data-ttu-id="8f565-113">Commerce site oluşturucusunda müşteri hesabı ödeme yöntemini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="8f565-113">Enable the customer account payment method in Commerce site builder</span></span> 

<span data-ttu-id="8f565-114">Commerce site oluşturucuda müşteri hesabı ödeme yöntemini etkinleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8f565-114">To enable the customer account payment method in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="8f565-115">**Site Ayarları \> Uzantılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="8f565-115">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="8f565-116">**Müşteri hesabı ödemelerini etkinleştir** özelliğini **B2B müşterileri için etkin** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8f565-116">Set the **Enable customer account payments** property to **Enabled for B2B customers**.</span></span> 
1. <span data-ttu-id="8f565-117">**kaydet ve yayınla** yı seçin.</span><span class="sxs-lookup"><span data-stu-id="8f565-117">Select **Save and Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="8f565-118">Yeni site ayarları yalnızca app.settings.json dosyası güncelleştirildikten sonra etkinleşir.</span><span class="sxs-lookup"><span data-stu-id="8f565-118">The new site settings take effect only after the app.settings.json file is updated.</span></span> <span data-ttu-id="8f565-119">Daha fazla bilgi için bkz. [SDK ve Modül kitaplığı güncelleştirmeleri](../e-commerce-extensibility/sdk-updates.md).</span><span class="sxs-lookup"><span data-stu-id="8f565-119">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md).</span></span>

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a><span data-ttu-id="8f565-120">B2B e-ticaret siteleri için ödeme sayfasında müşteri hesabı ödeme yöntemini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="8f565-120">Enable the customer account payment method on the checkout page for the B2B e-commerce site</span></span>

<span data-ttu-id="8f565-121">B2B e-ticaret sitesinin ödeme sayfasında müşteri hesabı ödeme yöntemini etkinleştirmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8f565-121">To enable the customer account payment method on the checkout page for the B2B e-commerce site, follow these steps.</span></span>

1. <span data-ttu-id="8f565-122">Commerce site oluşturucusunda, B2B e-ticaret sitesinin ödeme modüllerini içeren ödeme sayfasını veya parçasını bulun ve düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="8f565-122">In Commerce site builder, find and edit the checkout page or fragment that contains the checkout module for the B2B e-commerce site.</span></span>
1. <span data-ttu-id="8f565-123">**Ödeme bölümü kapsayıcısı** alanında, **Modül Ekle**'yi seçin ve **Müşteri hesabı ödemesi** modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="8f565-123">In the **Checkout section container** slot, select **Add Module**, and then add a **Customer account payment** module.</span></span>
1. <span data-ttu-id="8f565-124">Üç noktayı (**...**) seçip gerektiği gibi **Yukarı Taşı** veya **Aşağı Taşı**'yı seçerek **Müşteri hesabı ödemesi** modülunu konumlandırın.</span><span class="sxs-lookup"><span data-stu-id="8f565-124">Position the **Customer account payment** module by selecting the ellipsis (**...**), and then selecting **Move Up** or **Move Down** as required.</span></span>
1. <span data-ttu-id="8f565-125">**Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="8f565-125">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a><span data-ttu-id="8f565-126">Müşteri hesabı ödeme yönteminin etkinleştirildiğini ve yayınlandığını onaylayın</span><span class="sxs-lookup"><span data-stu-id="8f565-126">Confirm that the customer account payment method has been enabled and published</span></span>

<span data-ttu-id="8f565-127">Müşteri hesabı ödeme yönteminin etkinleştirildiğini onaylamak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8f565-127">To confirm that the customer account payment method has been enabled, follow these steps.</span></span>

1. <span data-ttu-id="8f565-128">E-ticaret sitesinde oturum açın.</span><span class="sxs-lookup"><span data-stu-id="8f565-128">Sign in to the e-commerce site.</span></span>
1. <span data-ttu-id="8f565-129">Sepete ürün ekleyin.</span><span class="sxs-lookup"><span data-stu-id="8f565-129">Add a product to the cart.</span></span>
1. <span data-ttu-id="8f565-130">Ödeme sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="8f565-130">Go to the checkout page.</span></span> <span data-ttu-id="8f565-131">Yeni **Müşteri Hesabı** ödeme yöntemini görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="8f565-131">You should see the new **Customer Account** payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8f565-132">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="8f565-132">Additional resources</span></span>

[<span data-ttu-id="8f565-133">B2B e-ticaret sitesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="8f565-133">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="8f565-134">B2B kuruluşlar için kuruluş modelleme hiyerarşileri oluşturma</span><span class="sxs-lookup"><span data-stu-id="8f565-134">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="8f565-135">B2B e-ticaret sitelerindeki iş ortağı kullanıcılarını yönetme</span><span class="sxs-lookup"><span data-stu-id="8f565-135">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="8f565-136">B2B e-ticaret siteleri için ürün miktarı sınırlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="8f565-136">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)

[<span data-ttu-id="8f565-137">SDK ve Modül kitaplığı güncelleştirmeleri</span><span class="sxs-lookup"><span data-stu-id="8f565-137">SDK and Module library updates</span></span>](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
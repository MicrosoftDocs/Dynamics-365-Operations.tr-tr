---
title: Sonraki ödemelerim için kaydet seçeneği görünmüyor
description: Bu konu, bir e-ticaret sitesinin ödeme sayfasında ödeme yöntemi altında sonraki ödemelerim için kaydet onay kutusu görüntülenmediğinde yardımcı olabilecek sorun giderme kılavuzu sağlar.
author: Reza-Assadi
manager: AnnBe
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
ms.openlocfilehash: 3a4fbcd522651ed1b82b72b751ff6ead44c94a71
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585575"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a><span data-ttu-id="a98e5-103">"Sonraki ödemelerim için kaydet" seçeneği görünmüyor</span><span class="sxs-lookup"><span data-stu-id="a98e5-103">"Save for my next payment" option doesn't appear</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a98e5-104">Bu konu, bir e-ticaret sitesinin ödeme sayfasında **ödeme yöntemi** altında **sonraki ödemelerim için kaydet** onay kutusu görüntülenmediğinde yardımcı olabilecek sorun giderme kılavuzu sağlar.</span><span class="sxs-lookup"><span data-stu-id="a98e5-104">This topic provides troubleshooting guidance that can help when the **Save for my next payment** check box doesn't appear under **Payment method** on an e-commerce site's checkout page.</span></span>

## <a name="description"></a><span data-ttu-id="a98e5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a98e5-105">Description</span></span>

<span data-ttu-id="a98e5-106">**Sonraki ödemelerim için Kaydet** onay kutusu bir e-ticaret sitesinin ödeme sayfasındaki **ödeme yöntemi** bölümünde görünmüyor.</span><span class="sxs-lookup"><span data-stu-id="a98e5-106">The **Save for my next payment** check box doesn't appear in the **Payment method** section on an e-commerce site's checkout page.</span></span>

<span data-ttu-id="a98e5-107">Aşağıdaki resimde **sonraki ödemelerim için kaydet** onay kutusunun yer aldığı bir ödeme sayfası örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="a98e5-107">The following illustration shows an example of a checkout page that includes the **Save for my next payment** check box.</span></span>

![Ödeme modülündeki sonraki ödemelerim için kaydet onay kutusu](media/payment-module-save-payment.jpg)

## <a name="resolution"></a><span data-ttu-id="a98e5-109">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="a98e5-109">Resolution</span></span>

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a><span data-ttu-id="a98e5-110">Commerce Headquarters'da Adyen için Dynamics 365 Paymet Connector'ın doğru yapılandırıldığını doğrulayın</span><span class="sxs-lookup"><span data-stu-id="a98e5-110">Verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters</span></span>

<span data-ttu-id="a98e5-111">Commerce Headquarters'da Adyen için Dynamics 365 Paymet Connector'ın doğru yapılandırıldığını doğrulamak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a98e5-111">To verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a98e5-112">**Retail ve Commerce \> Kanallar \> Çevrimiçi mağazalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="a98e5-112">Go to **Retail and Commerce \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="a98e5-113">Çevrimiçi mağazayı seçin.</span><span class="sxs-lookup"><span data-stu-id="a98e5-113">Select the online store.</span></span>
1. <span data-ttu-id="a98e5-114">**Ödeme Hesapları** hızlı sekmesinde, **e-ticarette ödeme bilgilerinin kaydedilmesine izin ver** alanındaki değerin **Doğru** olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="a98e5-114">On the **Payment accounts** FastTab, make sure that the **Allow saving payment information in e-commerce** field is set to **True**.</span></span>

![Commerce Headquarters'da e-ticaret alanında ödeme bilgilerinin kaydedilmesine izin verme](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a><span data-ttu-id="a98e5-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a98e5-116">Additional resources</span></span>

[<span data-ttu-id="a98e5-117">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="a98e5-117">Payment module</span></span>](../payment-module.md)

[<span data-ttu-id="a98e5-118">Adyen bağlayıcısı ile çevrimiçi ödeme araçlarını kaydetme</span><span class="sxs-lookup"><span data-stu-id="a98e5-118">Saving online payment instruments with the Adyen connector</span></span>](../dev-itpro/adyen-connector-listPI.md)

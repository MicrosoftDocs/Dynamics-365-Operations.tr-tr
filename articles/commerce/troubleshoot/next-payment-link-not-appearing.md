---
title: Sonraki ödemelerim için kaydet seçeneği görünmüyor
description: Bu konu, bir e-ticaret sitesinin ödeme sayfasında ödeme yöntemi altında sonraki ödemelerim için kaydet onay kutusu görüntülenmediğinde yardımcı olabilecek sorun giderme kılavuzu sağlar.
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
ms.openlocfilehash: af19a3abd78d543d82f7a8d017e2dc413115a6d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018446"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a><span data-ttu-id="8a975-103">"Sonraki ödemelerim için kaydet" seçeneği görünmüyor</span><span class="sxs-lookup"><span data-stu-id="8a975-103">"Save for my next payment" option doesn't appear</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8a975-104">Bu konu, bir e-ticaret sitesinin ödeme sayfasında **ödeme yöntemi** altında **sonraki ödemelerim için kaydet** onay kutusu görüntülenmediğinde yardımcı olabilecek sorun giderme kılavuzu sağlar.</span><span class="sxs-lookup"><span data-stu-id="8a975-104">This topic provides troubleshooting guidance that can help when the **Save for my next payment** check box doesn't appear under **Payment method** on an e-commerce site's checkout page.</span></span>

## <a name="description"></a><span data-ttu-id="8a975-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a975-105">Description</span></span>

<span data-ttu-id="8a975-106">**Sonraki ödemelerim için Kaydet** onay kutusu bir e-ticaret sitesinin ödeme sayfasındaki **ödeme yöntemi** bölümünde görünmüyor.</span><span class="sxs-lookup"><span data-stu-id="8a975-106">The **Save for my next payment** check box doesn't appear in the **Payment method** section on an e-commerce site's checkout page.</span></span>

<span data-ttu-id="8a975-107">Aşağıdaki resimde **sonraki ödemelerim için kaydet** onay kutusunun yer aldığı bir ödeme sayfası örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="8a975-107">The following illustration shows an example of a checkout page that includes the **Save for my next payment** check box.</span></span>

![Ödeme modülündeki sonraki ödemelerim için kaydet onay kutusu](media/payment-module-save-payment.jpg)

## <a name="resolution"></a><span data-ttu-id="8a975-109">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="8a975-109">Resolution</span></span>

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a><span data-ttu-id="8a975-110">Commerce Headquarters'da Adyen için Dynamics 365 Paymet Connector'ın doğru yapılandırıldığını doğrulayın</span><span class="sxs-lookup"><span data-stu-id="8a975-110">Verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters</span></span>

<span data-ttu-id="8a975-111">Commerce Headquarters'da Adyen için Dynamics 365 Paymet Connector'ın doğru yapılandırıldığını doğrulamak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8a975-111">To verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="8a975-112">**Retail ve Commerce \> Kanallar \> Çevrimiçi mağazalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="8a975-112">Go to **Retail and Commerce \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="8a975-113">Çevrimiçi mağazayı seçin.</span><span class="sxs-lookup"><span data-stu-id="8a975-113">Select the online store.</span></span>
1. <span data-ttu-id="8a975-114">**Ödeme Hesapları** hızlı sekmesinde, **e-ticarette ödeme bilgilerinin kaydedilmesine izin ver** alanındaki değerin **Doğru** olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="8a975-114">On the **Payment accounts** FastTab, make sure that the **Allow saving payment information in e-commerce** field is set to **True**.</span></span>

![Commerce Headquarters'da e-ticaret alanında ödeme bilgilerinin kaydedilmesine izin verme](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a><span data-ttu-id="8a975-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="8a975-116">Additional resources</span></span>

[<span data-ttu-id="8a975-117">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="8a975-117">Payment module</span></span>](../payment-module.md)

[<span data-ttu-id="8a975-118">Adyen bağlayıcısı ile çevrimiçi ödeme araçlarını kaydetme</span><span class="sxs-lookup"><span data-stu-id="8a975-118">Saving online payment instruments with the Adyen connector</span></span>](../dev-itpro/adyen-connector-listPI.md)

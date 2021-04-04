---
title: Ödemeler, siparişler faturalanmadan veya sevk edilmeden önce otomatik olarak kapatılıyor
description: Bu konu, satış siparişinin faturalanmamış veya sevk edilmemiş olmasına rağmen, sipariş verildikten sonra bir ödemenin Adyen portalında hemen kapatılmasıyla ilgili sorun giderme kılavuzu sağlar.
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
ms.openlocfilehash: 788854a3119eb9ffaf839beb93a5bc15cdcd6387
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585573"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a><span data-ttu-id="7be28-103">Ödemeler, siparişler faturalanmadan veya sevk edilmeden önce otomatik olarak kapatılıyor</span><span class="sxs-lookup"><span data-stu-id="7be28-103">Payments are automatically settled before orders are invoiced or shipped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7be28-104">Bu konu, satış siparişinin faturalanmamış veya sevk edilmemiş olmasına rağmen, sipariş verildikten sonra bir ödemenin Adyen portalında hemen kapatılmasıyla ilgili sorun giderme kılavuzu sağlar.</span><span class="sxs-lookup"><span data-stu-id="7be28-104">This topic provides troubleshooting guidance that can help when a payment is settled in the Adyen portal immediately after an order is placed, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="description"></a><span data-ttu-id="7be28-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7be28-105">Description</span></span>

<span data-ttu-id="7be28-106">Bir sipariş verildikten sonra, satış siparişi faturalanmamış veya sevk edilmemiş olmasına rağmen, Adyen portalında ödeme hemen kapatılıyor.</span><span class="sxs-lookup"><span data-stu-id="7be28-106">After an order is placed, the payment is immediately settled in the Adyen portal, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="resolution"></a><span data-ttu-id="7be28-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="7be28-107">Resolution</span></span>

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a><span data-ttu-id="7be28-108">Adyen portalında e-ticaret ödemeleri için el ile kaydetmeyi yapılandırın</span><span class="sxs-lookup"><span data-stu-id="7be28-108">Configure manual capture for e-commerce payments in the Adyen portal</span></span>

<span data-ttu-id="7be28-109">Adyen portalında e-ticaret ödemeleri için el ile kaydetmeyi yapılandırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7be28-109">To configure manual capture for e-commerce payments in the Adyen portal, follow these steps.</span></span>

1. <span data-ttu-id="7be28-110">Adyen portalında oturum açın.</span><span class="sxs-lookup"><span data-stu-id="7be28-110">Sign in to the Adyen portal.</span></span>
1. <span data-ttu-id="7be28-111">Sağ üst köşede, e-ticaret kanalı için satıcı hesabınızı seçin.</span><span class="sxs-lookup"><span data-stu-id="7be28-111">In the upper-right corner, select your merchant account for the e-commerce channel.</span></span>
1. <span data-ttu-id="7be28-112">Üst gezinti çubuğunda, **Hesap**'ı seçin ve ardından **Ayarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7be28-112">On the top navigation, select **Account**, and then select **Settings**.</span></span>
1. <span data-ttu-id="7be28-113">**Kaydetme gecikmesi** alanında, **el ile** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="7be28-113">In the **Capture Delay** field, select **manual**.</span></span>

    ![Adyen portalında kaydetme gecikmesi ayarı](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a><span data-ttu-id="7be28-115">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7be28-115">Additional resources</span></span>

[<span data-ttu-id="7be28-116">Adyen ödeme kaydetme</span><span class="sxs-lookup"><span data-stu-id="7be28-116">Adyen payment capture</span></span>](https://docs.adyen.com/point-of-sale/capturing-payments)

[<span data-ttu-id="7be28-117">Adyen için Dynamics 365 Ödeme Bağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="7be28-117">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="7be28-118">Dynamics 365 için Adyen Payment Connector sorunlarını giderme</span><span class="sxs-lookup"><span data-stu-id="7be28-118">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)

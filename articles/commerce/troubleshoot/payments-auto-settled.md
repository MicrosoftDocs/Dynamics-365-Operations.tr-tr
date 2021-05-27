---
title: Ödemeler, siparişler faturalanmadan veya sevk edilmeden önce otomatik olarak kapatılıyor
description: Bu konu, satış siparişinin faturalanmamış veya sevk edilmemiş olmasına rağmen, sipariş verildikten sonra bir ödemenin Adyen portalında hemen kapatılmasıyla ilgili sorun giderme kılavuzu sağlar.
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
ms.openlocfilehash: b4fd37a3c45f2559c9659f072ca0b6f02e712f53
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018272"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a><span data-ttu-id="4be63-103">Ödemeler, siparişler faturalanmadan veya sevk edilmeden önce otomatik olarak kapatılıyor</span><span class="sxs-lookup"><span data-stu-id="4be63-103">Payments are automatically settled before orders are invoiced or shipped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4be63-104">Bu konu, satış siparişinin faturalanmamış veya sevk edilmemiş olmasına rağmen, sipariş verildikten sonra bir ödemenin Adyen portalında hemen kapatılmasıyla ilgili sorun giderme kılavuzu sağlar.</span><span class="sxs-lookup"><span data-stu-id="4be63-104">This topic provides troubleshooting guidance that can help when a payment is settled in the Adyen portal immediately after an order is placed, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="description"></a><span data-ttu-id="4be63-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4be63-105">Description</span></span>

<span data-ttu-id="4be63-106">Bir sipariş verildikten sonra, satış siparişi faturalanmamış veya sevk edilmemiş olmasına rağmen, Adyen portalında ödeme hemen kapatılıyor.</span><span class="sxs-lookup"><span data-stu-id="4be63-106">After an order is placed, the payment is immediately settled in the Adyen portal, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="resolution"></a><span data-ttu-id="4be63-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="4be63-107">Resolution</span></span>

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a><span data-ttu-id="4be63-108">Adyen portalında e-ticaret ödemeleri için el ile kaydetmeyi yapılandırın</span><span class="sxs-lookup"><span data-stu-id="4be63-108">Configure manual capture for e-commerce payments in the Adyen portal</span></span>

<span data-ttu-id="4be63-109">Adyen portalında e-ticaret ödemeleri için el ile kaydetmeyi yapılandırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4be63-109">To configure manual capture for e-commerce payments in the Adyen portal, follow these steps.</span></span>

1. <span data-ttu-id="4be63-110">Adyen portalında oturum açın.</span><span class="sxs-lookup"><span data-stu-id="4be63-110">Sign in to the Adyen portal.</span></span>
1. <span data-ttu-id="4be63-111">Sağ üst köşede, e-ticaret kanalı için satıcı hesabınızı seçin.</span><span class="sxs-lookup"><span data-stu-id="4be63-111">In the upper-right corner, select your merchant account for the e-commerce channel.</span></span>
1. <span data-ttu-id="4be63-112">Üst gezinti çubuğunda, **Hesap**'ı seçin ve ardından **Ayarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4be63-112">On the top navigation, select **Account**, and then select **Settings**.</span></span>
1. <span data-ttu-id="4be63-113">**Kaydetme gecikmesi** alanında, **el ile** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="4be63-113">In the **Capture Delay** field, select **manual**.</span></span>

    ![Adyen portalında kaydetme gecikmesi ayarı](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a><span data-ttu-id="4be63-115">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="4be63-115">Additional resources</span></span>

[<span data-ttu-id="4be63-116">Adyen ödeme kaydetme</span><span class="sxs-lookup"><span data-stu-id="4be63-116">Adyen payment capture</span></span>](https://docs.adyen.com/point-of-sale/capturing-payments)

[<span data-ttu-id="4be63-117">Adyen için Dynamics 365 Ödeme Bağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="4be63-117">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="4be63-118">Dynamics 365 için Adyen Payment Connector sorunlarını giderme</span><span class="sxs-lookup"><span data-stu-id="4be63-118">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)

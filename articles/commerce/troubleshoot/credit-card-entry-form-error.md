---
title: Kredi kartı giriş sayfası ödeme sırasında hata görüntülüyor
description: Bu konu, ödeme yöntemi bölümü yüklenmediğinde ve hata iletisi gösterildiğinde yardımcı olabilecek sorun giderme kılavuzu sağlar.
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
ms.openlocfilehash: d2c5f01d17df79c9b23fd513aaeb5c0605d657e9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801783"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a><span data-ttu-id="e0508-103">Kredi kartı giriş sayfası ödeme sırasında hata görüntülüyor</span><span class="sxs-lookup"><span data-stu-id="e0508-103">Credit card entry page shows an error at checkout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e0508-104">Bu konu, **ödeme yöntemi** bölümü yüklenmediğinde ve hata iletisi gösterildiğinde yardımcı olabilecek sorun giderme kılavuzu sağlar.</span><span class="sxs-lookup"><span data-stu-id="e0508-104">This topic provides troubleshooting guidance that can help when the **Payment method** section isn't loaded and shows an error message.</span></span>

## <a name="description"></a><span data-ttu-id="e0508-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0508-105">Description</span></span>

<span data-ttu-id="e0508-106">Çevrimiçi bir mağazanın ödeme sayfasını açtığınızda, **ödeme yöntemi** bölümü yüklenmiyor ve şu hata iletisi görüntüleniyor: "Bir sorun oluştu.</span><span class="sxs-lookup"><span data-stu-id="e0508-106">When you open the checkout page of an online store, the **Payment method** section isn't loaded, and the following error message is shown: "Something went wrong.</span></span> <span data-ttu-id="e0508-107">Lütfen daha sonra yeniden deneyin."</span><span class="sxs-lookup"><span data-stu-id="e0508-107">Please try again later."</span></span>

![Ödeme modülü hatası](media/payment-module-error.jpg)

## <a name="resolution"></a><span data-ttu-id="e0508-109">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="e0508-109">Resolution</span></span>

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a><span data-ttu-id="e0508-110">Commerce Scale Unit önbelleğinin süresinin dolmasını bekleyin</span><span class="sxs-lookup"><span data-stu-id="e0508-110">Wait for the Commerce Scale Unit cache to expire</span></span>

<span data-ttu-id="e0508-111">Çevrimiçi mağazanın ödeme sayfasındaki ödeme servisi ayarları Commerce Scale Unit'te önbelleğe alınır ve e-ticaret sitesinde görüntülenmesi 15 dakika kadar sürebilir.</span><span class="sxs-lookup"><span data-stu-id="e0508-111">The payment service settings on the online store's checkout page are cached on the Commerce Scale Unit and can take up to 15 minutes to appear on the e-commerce site.</span></span> <span data-ttu-id="e0508-112">Bu ödeme servisi ayarları satıcı hesap kimliği, bulut API anahtarı ve ödeme yöntemiyle ilişkili çeşitli yapılandırma ayarları ile ilgili değişiklikleri içerir.</span><span class="sxs-lookup"><span data-stu-id="e0508-112">These payment service settings include changes to the merchant account ID, cloud API key, and various configuration settings that are related to the payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0508-113">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e0508-113">Additional resources</span></span>

[<span data-ttu-id="e0508-114">Çevrimiçi kanalı ayarlama</span><span class="sxs-lookup"><span data-stu-id="e0508-114">Set up an online channel</span></span>](../channel-setup-online.md)

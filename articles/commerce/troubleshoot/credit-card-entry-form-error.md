---
title: Kredi kartı giriş sayfası ödeme sırasında hata görüntülüyor
description: Bu konu, ödeme yöntemi bölümü yüklenmediğinde ve hata iletisi gösterildiğinde yardımcı olabilecek sorun giderme kılavuzu sağlar.
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
ms.openlocfilehash: f0751fc76e6eb4320f766886b4c1efcb1042e996
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585568"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a><span data-ttu-id="b3f97-103">Kredi kartı giriş sayfası ödeme sırasında hata görüntülüyor</span><span class="sxs-lookup"><span data-stu-id="b3f97-103">Credit card entry page shows an error at checkout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b3f97-104">Bu konu, **ödeme yöntemi** bölümü yüklenmediğinde ve hata iletisi gösterildiğinde yardımcı olabilecek sorun giderme kılavuzu sağlar.</span><span class="sxs-lookup"><span data-stu-id="b3f97-104">This topic provides troubleshooting guidance that can help when the **Payment method** section isn't loaded and shows an error message.</span></span>

## <a name="description"></a><span data-ttu-id="b3f97-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3f97-105">Description</span></span>

<span data-ttu-id="b3f97-106">Çevrimiçi bir mağazanın ödeme sayfasını açtığınızda, **ödeme yöntemi** bölümü yüklenmiyor ve şu hata iletisi görüntüleniyor: "Bir sorun oluştu.</span><span class="sxs-lookup"><span data-stu-id="b3f97-106">When you open the checkout page of an online store, the **Payment method** section isn't loaded, and the following error message is shown: "Something went wrong.</span></span> <span data-ttu-id="b3f97-107">Lütfen daha sonra yeniden deneyin."</span><span class="sxs-lookup"><span data-stu-id="b3f97-107">Please try again later."</span></span>

![Ödeme modülü hatası](media/payment-module-error.jpg)

## <a name="resolution"></a><span data-ttu-id="b3f97-109">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="b3f97-109">Resolution</span></span>

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a><span data-ttu-id="b3f97-110">Commerce Scale Unit önbelleğinin süresinin dolmasını bekleyin</span><span class="sxs-lookup"><span data-stu-id="b3f97-110">Wait for the Commerce Scale Unit cache to expire</span></span>

<span data-ttu-id="b3f97-111">Çevrimiçi mağazanın ödeme sayfasındaki ödeme servisi ayarları Commerce Scale Unit'te önbelleğe alınır ve e-ticaret sitesinde görüntülenmesi 15 dakika kadar sürebilir.</span><span class="sxs-lookup"><span data-stu-id="b3f97-111">The payment service settings on the online store's checkout page are cached on the Commerce Scale Unit and can take up to 15 minutes to appear on the e-commerce site.</span></span> <span data-ttu-id="b3f97-112">Bu ödeme servisi ayarları satıcı hesap kimliği, bulut API anahtarı ve ödeme yöntemiyle ilişkili çeşitli yapılandırma ayarları ile ilgili değişiklikleri içerir.</span><span class="sxs-lookup"><span data-stu-id="b3f97-112">These payment service settings include changes to the merchant account ID, cloud API key, and various configuration settings that are related to the payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b3f97-113">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b3f97-113">Additional resources</span></span>

[<span data-ttu-id="b3f97-114">Çevrimiçi kanalı ayarlama</span><span class="sxs-lookup"><span data-stu-id="b3f97-114">Set up an online channel</span></span>](../channel-setup-online.md)

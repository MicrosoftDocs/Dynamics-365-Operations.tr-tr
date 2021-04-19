---
title: Varsayılan ödeme hizmeti ile ilgili sipariş eşitleme hatası
description: Bu konu, bir çevrimiçi sipariş eşitlendiğinde oluşabilecek bir hatayı gidermeye yardımcı olabilecek sorun giderme kılavuzu sağlar.
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
ms.openlocfilehash: 45eeae751051b58e1c9e725eb4ed4b5240026e7f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801447"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a><span data-ttu-id="e46f7-103">Varsayılan ödeme hizmeti ile ilgili sipariş eşitleme hatası</span><span class="sxs-lookup"><span data-stu-id="e46f7-103">Order synchronization error related to the default payment service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e46f7-104">Bu konu, bir çevrimiçi sipariş eşitlendiğinde oluşabilecek bir hatayı gidermeye yardımcı olabilecek sorun giderme kılavuzu sağlar.</span><span class="sxs-lookup"><span data-stu-id="e46f7-104">This topic provides troubleshooting guidance that can help fix an error that might occur when an online order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="e46f7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e46f7-105">Description</span></span>

<span data-ttu-id="e46f7-106">Çevrimiçi bir siparişi eşitlediğinizde, şu hata iletisini alırsınız: "Kredi kartı işlemlerini işlemek için varsayılan bir ödeme hizmeti olmalıdır."</span><span class="sxs-lookup"><span data-stu-id="e46f7-106">When you sync an online order, you receive the following error message: "There must be a default payment service to process credit card transactions."</span></span>

![Eksik varsayılan ödeme hizmeti hatası](media/default-payment-method-error.jpg)

## <a name="resolution"></a><span data-ttu-id="e46f7-108">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="e46f7-108">Resolution</span></span>

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a><span data-ttu-id="e46f7-109">Commerce genel merkezinde varsayılan ödeme hizmetini onaylama veya ayarlama</span><span class="sxs-lookup"><span data-stu-id="e46f7-109">Confirm or set the default payment service in Commerce headquarters</span></span>

<span data-ttu-id="e46f7-110">Commerce genel merkezinde varsayılan ödeme hizmetini onaylamak veya ayarlamak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e46f7-110">To confirm or set the default payment service in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="e46f7-111">**Alacak hesapları \> Ödeme kurulumu \> Ödeme hizmetleri** menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="e46f7-111">Go to **Accounts receivable \> Payment setup \> Payment services**.</span></span>
1. <span data-ttu-id="e46f7-112">**Yeni kredi kartları için varsayılan işlemci** seçeneğinin bir ödeme servisi için **Evet** olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="e46f7-112">Make sure that the **Default processor for new credit cards** option is set to **Yes** for one payment service.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e46f7-113">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e46f7-113">Additional resources</span></span>

[<span data-ttu-id="e46f7-114">Kredi kartı ayarı, onayı ve çekimi</span><span class="sxs-lookup"><span data-stu-id="e46f7-114">Credit card setup, authorization, and capture</span></span>](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/credit-card-authorizations)

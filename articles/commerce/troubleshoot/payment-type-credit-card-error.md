---
title: Satış siparişi sayfasında ödeme türü kredi kartı olmalıdır hatası
description: Bu konu, sipariş eşitlendikten sonra satış siparişi sayfasında hata iletisi gösterildiğinde size yardımcı olabilecek sorun giderme kılavuzu sağlar.
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
ms.openlocfilehash: 5be19949e9d1dbc43fdd3e6def119effa50a34d0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018422"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a><span data-ttu-id="73a12-103">Satış siparişi sayfasında "ödeme türü kredi kartı olmalıdır" hatası</span><span class="sxs-lookup"><span data-stu-id="73a12-103">"Payment type must be credit card" error on the sales order page</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="73a12-104">Bu konu, sipariş eşitlendikten sonra satış siparişi sayfasında hata iletisi gösterildiğinde size yardımcı olabilecek sorun giderme kılavuzu sağlar.</span><span class="sxs-lookup"><span data-stu-id="73a12-104">This topic provides troubleshooting guidance that can help when an error message is shown on the sales order page after an order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="73a12-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="73a12-105">Description</span></span>

<span data-ttu-id="73a12-106">Satış siparişi sayfasını bir siparişi eşitledikten sonra açtığınızda, şu hata iletisini alırsınız: "kredi kartı numarası belirtildiği için ödeme türü kredi kartı olmalıdır."</span><span class="sxs-lookup"><span data-stu-id="73a12-106">When you open the sales order page after you sync an order, you receive the following error message: "The payment type must be credit card, since the credit card number has been specified."</span></span>

![Ödeme türü kredi kartı olmalıdır hatası](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a><span data-ttu-id="73a12-108">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="73a12-108">Resolution</span></span>

### <a name="set-the-payment-type-in-commerce-headquarters"></a><span data-ttu-id="73a12-109">Commerce Headquarters'da ödeme türünü ayarlayın</span><span class="sxs-lookup"><span data-stu-id="73a12-109">Set the payment type in Commerce headquarters</span></span>

1. <span data-ttu-id="73a12-110">**Alacak hesapları \> Ödemeler kurulumu \> Ödeme şartları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="73a12-110">Go to **Accounts receivable \> Payment setup \> Terms of payment**.</span></span>
1. <span data-ttu-id="73a12-111">Sol gezinti bölmesinde ödeme koşullarınızı seçin.</span><span class="sxs-lookup"><span data-stu-id="73a12-111">In the left navigation, select your terms of payment.</span></span>
1. <span data-ttu-id="73a12-112">**Ödeme türü** alanında, **kredi kartı**'nın seçildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="73a12-112">In the **Payment type** field, make sure that **Credit card** is selected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73a12-113">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="73a12-113">Additional resources</span></span>

[<span data-ttu-id="73a12-114">Çevrimiçi satışları ve ödemeleri deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="73a12-114">Posting of online sales and payments</span></span>](../tasks/posting-online-sales-payments.md)

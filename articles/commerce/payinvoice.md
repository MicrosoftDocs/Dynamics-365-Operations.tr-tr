---
title: Fatura ödeme senaryolarını ayarlama
description: Bu konuda, Dynamics 365 Commerce'ın nasıl fatura ödemeleriyle ilgili çeşitli senaryoları destekleyecek şekilde yapılandırılacağı açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6f818fa552fe5651dc7d56de265fe989c57fa822
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257085"
---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="0ecd4-103">Fatura ödeme senaryolarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="0ecd4-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0ecd4-104">Dynamics 365 Commerce'daki Fatura öde işlevi aşağıdakileri destekleyecek şekilde genişletilmiştir:</span><span class="sxs-lookup"><span data-stu-id="0ecd4-104">The Pay invoice functionality in Dynamics 365 Commerce has been expanded to support:</span></span>

- <span data-ttu-id="0ecd4-105">Tek bir POS hareketinde birden fazla satış siparişi faturasının ödenmesi.</span><span class="sxs-lookup"><span data-stu-id="0ecd4-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="0ecd4-106">Serbest metin faturaları, proje tabanlı faturalar ve alacak dekontları gibi çeşitli müşteri faturası türlerinin ödenmesi.</span><span class="sxs-lookup"><span data-stu-id="0ecd4-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="0ecd4-107">Bu senaryoları etkinleştirmek üzere, mağazalar için işlev profilinin aşağıda belirtildiği gibi yapılandırılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="0ecd4-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>

1. <span data-ttu-id="0ecd4-108">**Retail ve Commerce \> Kanal kurulumu \> POS ayarı \> POS profilleri \> İşlevsellik profilleri**'ne gidin ve değişiklikleri yapmak istediğiniz mağazalarla ilişkili bir profil seçin.</span><span class="sxs-lookup"><span data-stu-id="0ecd4-108">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>
2. <span data-ttu-id="0ecd4-109">**İşlevler** sekmesinde, aşağıdaki parametreleri gerektiği gibi yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="0ecd4-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="0ecd4-110">**Satış siparişi faturası**: Kullanıcıların tek bir POS hareketinde bir veya daha fazla satış siparişi tabanlı faturayı ödemesine izin vermek için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0ecd4-110">**Sales order invoice** – Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="0ecd4-111">**Serbest metin faturası**: Kullanıcıların tek bir POS hareketinde bir veya daha fazla serbest metin tabanlı faturayı ödemesine izin vermek için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0ecd4-111">**Free text invoice** – Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="0ecd4-112">**Proje faturası**: Kullanıcıların tek bir POS hareketinde bir veya daha fazla proje tabanlı faturayı ödemesine izin vermek için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0ecd4-112">**Project invoice** – Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="0ecd4-113">**Satış siparişi alacak dekontu**: Kullanıcıların birden fazla satış siparişi tabanlı alacak dekontunu açık faturalara göre kapatmasına veya açık bir alacak dekontu için bir geri ödeme işlemi yapmasına izin vermek için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0ecd4-113">**Sales order credit note** – Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="0ecd4-114">Kısmi tutarları ödeme veya kapatma henüz desteklenmemektedir.</span><span class="sxs-lookup"><span data-stu-id="0ecd4-114">Payment or settlement of partial amounts is not yet supported.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
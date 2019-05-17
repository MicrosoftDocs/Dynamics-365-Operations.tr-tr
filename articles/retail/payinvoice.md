---
title: Ödeme faturası senaryolarını ayarlama
description: Bu konuda, Dynamics 365 for Retail'ın nasıl fatura ödemeleriyle ilgili çeşitli senaryoları destekleyecek şekilde yapılandırılacağı açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 158d8ca8a97c473e940f76dd3f35cecc4e9dd7f4
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517188"
---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="0d49f-103">Ödeme faturası senaryolarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="0d49f-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0d49f-104">Dynamics 365 for Retail'daki Fatura öde işlevi aşağıdakileri destekleyecek şekilde genişletilmiştir:</span><span class="sxs-lookup"><span data-stu-id="0d49f-104">The Pay invoice functionality in Dynamics 365 for Retail has been expanded to support:</span></span>

- <span data-ttu-id="0d49f-105">Tek bir POS hareketinde birden fazla satış siparişi faturasının ödenmesi.</span><span class="sxs-lookup"><span data-stu-id="0d49f-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="0d49f-106">Serbest metin faturaları, proje tabanlı faturalar ve alacak dekontları gibi çeşitli müşteri faturası türlerinin ödenmesi.</span><span class="sxs-lookup"><span data-stu-id="0d49f-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="0d49f-107">Bu senaryoları etkinleştirmek üzere, mağazalar için işlev profilinin aşağıda belirtildiği gibi yapılandırılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="0d49f-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>

1. <span data-ttu-id="0d49f-108">**Perakende \> Kanal ayarı \> POS ayarı \> POS profilleri \> İşlev profilleri**'ne gidin ve değişiklikleri yapmak istediğiniz mağazalarla ilişkili bir profil seçin.</span><span class="sxs-lookup"><span data-stu-id="0d49f-108">Go to **Retail \> Channel setup \> POS setup \> POS profiles \> Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>
2. <span data-ttu-id="0d49f-109">**İşlevler** sekmesinde, aşağıdaki parametreleri gerektiği gibi yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="0d49f-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="0d49f-110">**Satış siparişi faturası**: Kullanıcıların tek bir POS hareketinde bir veya daha fazla satış siparişi tabanlı faturayı ödemesine izin vermek için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0d49f-110">**Sales order invoice** – Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="0d49f-111">**Serbest metin faturası**: Kullanıcıların tek bir POS hareketinde bir veya daha fazla serbest metin tabanlı faturayı ödemesine izin vermek için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0d49f-111">**Free text invoice** – Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="0d49f-112">**Proje faturası**: Kullanıcıların tek bir POS hareketinde bir veya daha fazla proje tabanlı faturayı ödemesine izin vermek için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0d49f-112">**Project invoice** – Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="0d49f-113">**Satış siparişi alacak dekontu**: Kullanıcıların birden fazla satış siparişi tabanlı alacak dekontunu açık faturalara göre kapatmasına veya açık bir alacak dekontu için bir geri ödeme işlemi yapmasına izin vermek için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0d49f-113">**Sales order credit note** – Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="0d49f-114">Kısmi tutarları ödeme veya kapatma henüz desteklenmemektedir.</span><span class="sxs-lookup"><span data-stu-id="0d49f-114">Payment or settlement of partial amounts is not yet supported.</span></span>

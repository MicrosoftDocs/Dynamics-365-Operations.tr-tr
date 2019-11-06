---
title: Perakende hareketi tutarlılık denetleyicisinde kuralları devre dışı bırakma
description: Bu konuda, Microsoft Dynamics 365 Retail'deki perakende hareketi tutarlılık denetleyicisi kurallarını devre dışı bırakma işlevi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bf8df2fb9f8f5c33ceb13eb012fb6879f81ec66
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/14/2019
ms.locfileid: "2586309"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="f8955-103">Perakende hareketi tutarlılık denetleyicisinde kuralları devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="f8955-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="f8955-104">Perakendecilerin, kendilerine özgü benzersiz iş senaryoları ve süreçleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="f8955-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="f8955-105">Bu nedenle, perakende hareketi tutarlılık denetleyicisine varsayılan olarak eklenen tüm kurallar tüm perakendeciler için geçerli değildir.</span><span class="sxs-lookup"><span data-stu-id="f8955-105">Therefore, not all the rules that are included by default in the retail transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="f8955-106">Microsoft Dynamics 365 Retail, farklılıklara uyum sağlamak için geçerli olmayan kuralları devre dışı bırakmak üzere kullanılabilen bir işlev sunar.</span><span class="sxs-lookup"><span data-stu-id="f8955-106">To accommodate differences, Microsoft Dynamics 365 Retail provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="f8955-107">Ortamınızdaki perakende hareketi tutarlılık denetleyicisinde bulunan kuralların listesini görüntülemek ve her kuralın durumunu görmek için **Perakende \> Genel merkez kurulumu \> Parametreler \> Perakende parametreleri**'ne gidin ve **Hareket doğrulama** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f8955-107">To view the list of rules that are available in the retail transaction consistency checker in your environment, and to see the status of each rule, go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="f8955-108">Varsayılan olarak, her kuralın **Etkin**'dir.</span><span class="sxs-lookup"><span data-stu-id="f8955-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="f8955-109">Bu nedenle, perakende hareketlerini perakende ekstrelerine eklenmeden önce doğrulamak için tüm kurallar kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f8955-109">Therefore, all the rules are used to validate retail transactions before they are pulled into the retail statements.</span></span> <span data-ttu-id="f8955-110">Bir kuralı devre dışı bırakmak için durumunu **Devre dışı** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="f8955-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="f8955-111">Ekstre hesaplama işlemi sırasında perakende hareketleri doğrulanırken devre dışı bırakılan kurallar dikkate alınmaz.</span><span class="sxs-lookup"><span data-stu-id="f8955-111">Disabled rules aren't considered when retail transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="f8955-112">Tüm doğrulama sürecini atlamak için, etkinleştirilen kuralları dikkate almadan **Perakende \> Genel merkez kurulumu \> Parametreler \> Perakende parametreleri**'ne gidin ve sonra **Hareket doğrulama** sekmesinde **Perakende hareketleri için tutarlılık denetleyicisini devre dışı bırak** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f8955-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Retail transactions** option to **Yes**.</span></span> <span data-ttu-id="f8955-113">Bu seçenek **Hayır** olarak ayarlandıktan sonra, kullanıcı arabiriminden (UI) tekrar **Evet** olarak değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="f8955-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>

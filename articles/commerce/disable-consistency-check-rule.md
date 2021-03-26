---
title: Perakende hareketi tutarlılık denetleyicisinde kuralları devre dışı bırakma
description: Bu konuda, Microsoft Dynamics 365 Commerce'taki hareket tutarlılık denetleyicisi kurallarını devre dışı bırakma işlevi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: abd97819d44963d22269efc9536f746c3c0b3812
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230602"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="f2ee1-103">Perakende hareketi tutarlılık denetleyicisinde kuralları devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="f2ee1-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2ee1-104">Perakendecilerin, kendilerine özgü benzersiz iş senaryoları ve süreçleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="f2ee1-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="f2ee1-105">Bu nedenle, ticari hareket tutarlılık denetleyicisine varsayılan olarak eklenen tüm kurallar tüm perakendeciler için geçerli değildir.</span><span class="sxs-lookup"><span data-stu-id="f2ee1-105">Therefore, not all the rules that are included by default in the commerce transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="f2ee1-106">Microsoft Dynamics 365 Commerce, farklılıklara uyum sağlamak için geçerli olmayan kuralları devre dışı bırakmak üzere kullanılabileceğiniz bir işlev sunar.</span><span class="sxs-lookup"><span data-stu-id="f2ee1-106">To accommodate differences, Microsoft Dynamics 365 Commerce provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="f2ee1-107">Ortamınızdaki ticari hareket tutarlılık denetleyicisinde bulunan kuralların listesini görüntülemek ve her kuralın durumunu görmek için **Retail ve Commerce \> Genel merkez kurulumu \> Parametreler \> Commerce parametreleri**'ne gidin ve **Hareket doğrulama** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f2ee1-107">To view the list of rules that are available in the transaction consistency checker in your environment, and to see the status of each rule, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="f2ee1-108">Varsayılan olarak, her kuralın durumu **Etkin** olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="f2ee1-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="f2ee1-109">Bu nedenle, ticari hareketleri ticari ekstrelere eklenmeden önce doğrulamak için tüm kurallar kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f2ee1-109">Therefore, all the rules are used to validate transactions before they are pulled into the commerce statements.</span></span> <span data-ttu-id="f2ee1-110">Bir kuralı devre dışı bırakmak için durumunu **Devre Dışı** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="f2ee1-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="f2ee1-111">Ekstre hesaplama işlemi sırasında ticari hareketler doğrulanırken devre dışı bırakılan kurallar dikkate alınmaz.</span><span class="sxs-lookup"><span data-stu-id="f2ee1-111">Disabled rules aren't considered when transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="f2ee1-112">Tüm doğrulama sürecini atlamak için, etkinleştirilen kuralları dikkate almadan **Retail ve Commerce \> Genel merkez kurulumu \> Parametreler \> Commerce parametreleri**'ne gidin ve sonra **Hareket doğrulama** sekmesinde **Commerce hareketleri için tutarlılık denetleyicisini devre dışı bırak** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f2ee1-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Commerce transactions** option to **Yes**.</span></span> <span data-ttu-id="f2ee1-113">Bu seçenek **Hayır** olarak ayarlandıktan sonra, kullanıcı arabiriminden (UI) tekrar **Evet** olarak değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="f2ee1-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
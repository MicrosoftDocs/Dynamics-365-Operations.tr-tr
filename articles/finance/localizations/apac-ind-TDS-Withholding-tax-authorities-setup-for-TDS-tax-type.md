---
title: TDS vergi türü için stopaj vergisi yetkililerini ayarlama
description: Bu konu, Kaynakta Kesilen Vergi (TDS) yetkililerinin nasıl ayarlanacağını açıklar.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 5375363a9b1383a83e80fc3c4b841780adab4172
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023650"
---
# <a name="set-up-withholding-tax-authorities-for-the-tds-tax-type"></a><span data-ttu-id="0238f-103">TDS vergi türü için stopaj vergisi yetkililerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="0238f-103">Set up withholding tax authorities for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0238f-104">Bu konu, Kaynakta Kesilen Vergi (TDS) yetkililerinin nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="0238f-104">This topic explains how to set up Tax Deducted at Source (TDS) authorities.</span></span>

1. <span data-ttu-id="0238f-105">**Vergi \> Dolaylı vergiler \> Stopaj vergisi yetkililieri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="0238f-105">Go to **Tax \> Indirect taxes \> Withholding tax authorities**.</span></span>

    <span data-ttu-id="0238f-106">[![Stopaj vergisi yetkilileri sayfası](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span><span class="sxs-lookup"><span data-stu-id="0238f-106">[![Withholding tax authorities page](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span></span>

2. <span data-ttu-id="0238f-107">TDS vergi türü için stopaj vergisi yetkililerini ayarlamak üzere **Vergi türü** alanında **TDS**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0238f-107">In the **Tax type** field, select **TDS** to set up withholding tax authorities for the TDS tax type.</span></span>
3. <span data-ttu-id="0238f-108">Eylem bölmesinde, bir satır oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0238f-108">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="0238f-109">**Stopaj vergisi yetkilisi** alanında, TDS yetkilisi için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="0238f-109">In the **Withholding tax authority** field, enter a name for the TDS authority.</span></span>
5. <span data-ttu-id="0238f-110">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="0238f-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="0238f-111">**Genel** hızlı sekmesinde, **Satıcı hesabı** alanındaki TDS yetkilisi için satıcı hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="0238f-111">On the **General** FastTab, in the **Vendor account** field, select the vendor account for the TDS authority.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0238f-112">TDS yetkili satıcısına borçlu olan fonların yatırılacağı bankanın adını belirlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="0238f-112">You must define the name of the bank where funds that are owed to the TDS authority vendor will be deposited.</span></span> <span data-ttu-id="0238f-113">Banka adı, **Banka hesapları** sayfasında (**Borç hesapları \> Tüm satıcılar \> Satıcı \> Kurulum \> Banka hesapları**) belirlenir.</span><span class="sxs-lookup"><span data-stu-id="0238f-113">The bank's name is defined on the **Bank accounts** page (**Accounts payable \> All vendors \> Vendor \> Set up \> Bank accounts**).</span></span>

7. <span data-ttu-id="0238f-114">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0238f-114">Close the page.</span></span>

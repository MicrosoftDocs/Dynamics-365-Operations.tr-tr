---
title: Koda göre satış vergisi ödemesi raporunu yazdırma
description: Bu konu, Koda göre satış vergisi ödemesi raporunu muhasebe veya vergi kodu para birimi cinsinden yazdırmak için gerekli olan ayarlar ve eylemler hakkında bilgi içerir.
author: anasyash
manager: AnnBe
ms.date: 04/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 3c3b251aadfa997f453e60b0842f89a6f09eb9cb
ms.sourcegitcommit: 88347d0f0ac862a77f269a05f1801d30dc93586e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2020
ms.locfileid: "3260267"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a><span data-ttu-id="21116-103">Koda göre satış vergisi ödemesi raporunu yazdırma</span><span class="sxs-lookup"><span data-stu-id="21116-103">Print the Sales tax payment by code report</span></span> 

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="21116-104">**Koda göre satış vergisi ödemesi** raporunu yazdırmak için **Vergi** \> **Sorgular ve raporlar** \> **Satış vergisi raporları** \> **Koda göre satış vergisi ödemesi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="21116-104">To print the **Sales tax payment by code** report, go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span> <span data-ttu-id="21116-105">Varsayılan olarak, rapor tutarları **Satış vergisi raporlama kodları** sayfasında ayarlanan tüm raporlama kodları için tüzel kişiliğin muhasebe para birimi cinsinden oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="21116-105">By default, report amounts are generated in the accounting currency of the legal entity for all reporting codes that are set up on the **Sales tax reporting codes** page.</span></span>

<span data-ttu-id="21116-106">Ayrıca, bu raporu **Satış vergisi kodları** sayfasındaki satış vergisi kodlarına atanan tüm raporlama kodları için satış vergisi kodlarının para birimi cinsinden satış vergisi ödeme tutarlarını göstermek için de oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="21116-106">You can also generate this report so that it shows the sales tax payment amounts in the currencies of sales tax codes for all reporting codes that are assigned to sales tax codes on the **Sales tax codes** page.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="21116-107">Özelliği etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="21116-107">Turn on the feature</span></span>

<span data-ttu-id="21116-108">**Özellik yönetimi** çalışma alanında, aşağıdaki özelliği etkinleştirin: **Koda göre satış vergisi ödemesi raporunu satış vergisi kodu para birimi cinsinden oluştur**.</span><span class="sxs-lookup"><span data-stu-id="21116-108">In the **Feature management** workspace, turn on the following feature: **Generate the Sales tax payment by code report in the sales tax code currency**.</span></span>

## <a name="run-the-report"></a><span data-ttu-id="21116-109">Raporu çalıştırma</span><span class="sxs-lookup"><span data-stu-id="21116-109">Run the report</span></span>

1. <span data-ttu-id="21116-110">**Vergi** \> **Sorgular ve raporlar** \> **Satış vergisi raporları** \> **Koda göre satış vergisi ödemesi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="21116-110">Go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span>
2. <span data-ttu-id="21116-111">**Rapor para birimi** alanında, aşağıdaki değerlerden birini seçin:</span><span class="sxs-lookup"><span data-stu-id="21116-111">In the **Report currency** field, select one of the following values:</span></span>

    - <span data-ttu-id="21116-112">**Muhasebe para birimi** – Rapor tutarlarını muhasebe para birimi cinsinden yazdırın.</span><span class="sxs-lookup"><span data-stu-id="21116-112">**Accounting currency** – Print the report amounts in the accounting currency.</span></span>
    - <span data-ttu-id="21116-113">**Satış vergisi kodu para birimi** – Rapor tutarlarını satış vergisi kodlarının para birimi cinsinden yazdırın.</span><span class="sxs-lookup"><span data-stu-id="21116-113">**Sales tax code currency** – Print the report amounts in the currencies of sales tax codes.</span></span>

    ![Koda göre satış vergisi ödemesi iletişim kutusu](media/Sales-tax-payment-by-code.png)

<span data-ttu-id="21116-115">Aşağıdaki resim, oluşturulan raporun bir örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="21116-115">The following illustration shows an example of the report that is generated.</span></span> <span data-ttu-id="21116-116">Rapor, raporlama kodunun atandığı satış vergisi kodu için **Satış vergisi para birimi** alanının **EUR** olarak ayarlanması durumunda raporlama kodu **101**'in **EUR** para birimine sahip olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="21116-116">The report shows that reporting code **101** has the **EUR** currency if the **Sales tax currency** field is set to **EUR** for the sales tax code that the reporting code is assigned to.</span></span>

![Koda göre satış vergisi ödemesi raporu örneği](media/Sales-tax-payment-by-code-2.png)
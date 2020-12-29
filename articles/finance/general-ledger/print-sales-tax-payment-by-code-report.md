---
title: Koda göre satış vergisi ödemesi raporunu yazdırma
description: Bu konu, Koda göre satış vergisi ödemesi raporunu muhasebe veya vergi kodu para birimi cinsinden yazdırmak için gerekli olan ayarlar ve eylemler hakkında bilgi içerir.
author: anasyash
manager: AnnBe
ms.date: 05/27/2020
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
ms.openlocfilehash: 7033999f7258e9ddd1d01620f9ad416e94ef3111
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448824"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a>Koda göre satış vergisi ödemesi raporunu yazdırma 

[!include [banner](../includes/banner.md)]

**Koda göre satış vergisi ödemesi** raporunu yazdırmak için **Vergi** \> **Sorgular ve raporlar** \> **Satış vergisi raporları** \> **Koda göre satış vergisi ödemesi**'ne gidin. Varsayılan olarak, rapor tutarları **Satış vergisi raporlama kodları** sayfasında ayarlanan tüm raporlama kodları için tüzel kişiliğin muhasebe para birimi cinsinden oluşturulur.

Ayrıca, bu raporu **Satış vergisi kodları** sayfasındaki satış vergisi kodlarına atanan tüm raporlama kodları için satış vergisi kodlarının para birimi cinsinden satış vergisi ödeme tutarlarını göstermek için de oluşturabilirsiniz.

## <a name="turn-on-the-feature"></a>Özelliği etkinleştirme

**Özellik yönetimi** çalışma alanında, aşağıdaki özelliği etkinleştirin: **Koda göre satış vergisi ödemesi raporunu satış vergisi kodu para birimi cinsinden oluştur**.

## <a name="run-the-report"></a>Raporu çalıştırma

1. **Vergi** \> **Sorgular ve raporlar** \> **Satış vergisi raporları** \> **Koda göre satış vergisi ödemesi**'ne gidin.
2. **Rapor para birimi** alanında, aşağıdaki değerlerden birini seçin:

    - **Muhasebe para birimi** – Rapor tutarlarını muhasebe para birimi cinsinden yazdırın.
    - **Satış vergisi kodu para birimi** – Rapor tutarlarını satış vergisi kodlarının para birimi cinsinden yazdırın.

    ![Koda göre satış vergisi ödemesi iletişim kutusu](media/Sales-tax-payment-by-code.png)

Aşağıdaki resim, oluşturulan raporun bir örneğini gösterir. Rapor, raporlama kodunun atandığı satış vergisi kodu için **Satış vergisi para birimi** alanının **EUR** olarak ayarlanması durumunda raporlama kodu **101**'in **EUR** para birimine sahip olduğunu gösterir.

![Koda göre satış vergisi ödemesi raporu örneği](media/Sales-tax-payment-by-code-2.png)

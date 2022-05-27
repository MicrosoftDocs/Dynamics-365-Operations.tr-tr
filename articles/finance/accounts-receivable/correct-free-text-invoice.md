---
title: Bir serbest metin faturasını düzeltmek
description: Bu konuda, deftere nakledilmiş bir metin faturasının nasıl düzeltileceği ve düzeltilmiş fatura olarak yeniden nasıl yayınlanacağı açıklanmaktadır.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7fb535b14f4c270f914a427d09027c37b3be7b72
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716230"
---
# <a name="correct-a-free-text-invoice"></a>Bir serbest metin faturasını düzeltmek

[!include [banner](../includes/banner.md)]

Bu konuda, deftere nakledilmiş bir metin faturasının nasıl düzeltileceği ve düzeltilmiş fatura olarak yeniden nasıl yayınlanacağı açıklanmaktadır.

Deftere nakledilmiş bir Dekont/Serbest metin faturasını düzeltmek için deftere nakledilen serbest metinli faturayı açın. **Fatura** sayfası üzerinde, **İptal** seçeneğini tıklatın ve daha sonra **Doğru fatura**'yı seçin. Bir neden kodu seçin, yorumlar ekleyin ve yeni düzeltilmiş fatura için tarih seçin. Düzeltilmiş faturayı değiştirebilir ve nakledebilirsiniz. 

Düzeltilmiş faturayı deftere naklettiğinizde, bir iptal etme faturası alacak tutarı için orijinal fatura tutarına eşit oluşturulur. Bu nedenle, orijinal fatura ve fatura iptal etmenin birleşik bakiyesi 0 (sıfır) olur. İptal etme faturası, orijinal faturaya karşı kapatılır. 

Düzeltilmiş Fatura'yı deftere naklettikten sonra üç faturanız olacaktır:

-   **Orijinal fatura** – Düzelttiğiniz bilgileri içeren fatura.
-   **İptal faturası** – Oluşturulan en son Düzeltilmiş faturayı iptal etmek için sistem tarafından oluşturulan iade faturası.
-   **Düzeltilmiş fatura** – Düzeltilen fatura bilgileri içeren bir fatura.

İptal etme ve düzeltme faturalarını iki şekilde tanımlayabilirsiniz:

-   **Tüm serbest metin faturaları** sayfası bir **Düzeltme** sütunu içerir, burada hangi faturaların iptal faturası ve düzeltme faturası olduğunu görebilirsiniz.
-   Dekont/Serbest metin faturası başlığı **İptal Faturası '\[fatura numarası\]'** veya **Düzeltilmiş Fatura '\[fatura numarası\]'** durumunu gösterir.

> [!NOTE]
> Bu özellik sadece **Serbest metin fatura düzeltmesi** konfigürasyon anahtarı seçiliyse kullanılabilir. Yapılandırma anahtarlarının nasıl etkinleştirileceği hakkında daha fazla bilgi için [Bakım modu](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) konusundaki YApılandırma anahtarlarını Etkinleştir (veya Devre Dışı Bırak) bölümüne bakın. 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

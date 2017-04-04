---
title: "Bir serbest metin faturasını düzeltmek"
description: "Bu makalede, deftere nakledilmiş bir metin faturasının nasıl düzeltileceği ve düzeltilmiş fatura olarak yeniden nasıl yayınlanacağı açıklanmaktadır."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: ab16c517abfd3fa2b59625fff04b7427ee3471bb
ms.lasthandoff: 03/31/2017


---

# <a name="correct-a-free-text-invoice"></a>Bir serbest metin faturasını düzeltmek

Bu makalede, deftere nakledilmiş bir metin faturasının nasıl düzeltileceği ve düzeltilmiş fatura olarak yeniden nasıl yayınlanacağı açıklanmaktadır.

Deftere nakledilmiş bir Dekont/Serbest metin faturasını düzeltmek için deftere nakledilen serbest metinli faturayı açın. Üzerinde **fatura** sayfa, seçme **iptal**ve sonra seçin **doğru fatura**. Bir neden kodu seçin, yorumlar ekleyin ve yeni düzeltilmiş fatura için tarih seçin. Düzeltilmiş faturayı değiştirebilir ve nakledebilirsiniz. 

Düzeltilmiş faturayı deftere naklettiğinizde, bir iptal etme faturası alacak tutarı için orijinal fatura tutarına eşit oluşturulur. Bu nedenle, orijinal fatura ve fatura iptal etmenin birleşik bakiyesi 0 (sıfır) olur. İptal etme faturası, orijinal faturaya karşı kapatılır. 

Düzeltilmiş Fatura'yı deftere naklettikten sonra üç faturanız olacaktır:

-   **Orijinal fatura** – Düzelttiğiniz bilgileri içeren fatura.
-   **İptal faturası** – Oluşturulan en son Düzeltilmiş faturayı iptal etmek için sistem tarafından oluşturulan iade faturası.
-   **Düzeltilmiş fatura** – Düzeltilen fatura bilgileri içeren bir fatura.

İptal etme ve düzeltme faturalarını iki şekilde tanımlayabilirsiniz:

-   **Tüm serbest metin faturaları** sayfası bir **Düzeltme** sütunu içerir, burada hangi faturaların iptal faturası ve düzeltme faturası olduğunu görebilirsiniz.
-   Dekont/Serbest metin faturası başlığında bir durumunu gösterir **Cancelling Fatura '\[fatura numarası\]'** veya **Corrected Fatura '\[fatura numarası\]'**.

> [!NOTE]
> Bu özelliği yalnızca **serbest metin faturası düzeltme** konfigürasyon anahtarı seçiliyse.



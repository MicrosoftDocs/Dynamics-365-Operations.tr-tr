---
title: Bir serbest metin faturasını düzeltmek
description: Bu makalede, deftere nakledilmiş bir metin faturasının nasıl düzeltileceği ve düzeltilmiş fatura olarak yeniden nasıl yayınlanacağı açıklanmaktadır.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76cf1f24a31f246a41601908ebba308551925d90
ms.sourcegitcommit: d0fa8d0140fa81029527edb317623c1a7737c593
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863024"
---
# <a name="correct-a-free-text-invoice"></a><span data-ttu-id="81d86-103">Bir serbest metin faturasını düzeltmek</span><span class="sxs-lookup"><span data-stu-id="81d86-103">Correct a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81d86-104">Bu makalede, deftere nakledilmiş bir metin faturasının nasıl düzeltileceği ve düzeltilmiş fatura olarak yeniden nasıl yayınlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="81d86-104">This article explains how to correct a free text invoice that has been posted and reissue it as a corrected invoice.</span></span>

<span data-ttu-id="81d86-105">Deftere nakledilmiş bir Dekont/Serbest metin faturasını düzeltmek için deftere nakledilen serbest metinli faturayı açın.</span><span class="sxs-lookup"><span data-stu-id="81d86-105">To correct a free text invoice that has already been posted, open the posted free text invoice.</span></span> <span data-ttu-id="81d86-106">**Fatura** sayfası üzerinde, **İptal** seçeneğini tıklatın ve daha sonra **Doğru fatura**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="81d86-106">On the **Invoice** page, select **Cancel**, and then select **Correct invoice**.</span></span> <span data-ttu-id="81d86-107">Bir neden kodu seçin, yorumlar ekleyin ve yeni düzeltilmiş fatura için tarih seçin.</span><span class="sxs-lookup"><span data-stu-id="81d86-107">Select a reason code, add comments, and select the date for new corrected invoice.</span></span> <span data-ttu-id="81d86-108">Düzeltilmiş faturayı değiştirebilir ve nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="81d86-108">You can modify the corrected invoice, and post it.</span></span> 

<span data-ttu-id="81d86-109">Düzeltilmiş faturayı deftere naklettiğinizde, bir iptal etme faturası alacak tutarı için orijinal fatura tutarına eşit oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="81d86-109">When you post the corrected invoice, a canceling invoice is created for a credit amount that equals the original invoice amount.</span></span> <span data-ttu-id="81d86-110">Bu nedenle, orijinal fatura ve fatura iptal etmenin birleşik bakiyesi 0 (sıfır) olur.</span><span class="sxs-lookup"><span data-stu-id="81d86-110">Therefore, the combined balance of the original invoice and the canceling invoice is 0 (zero).</span></span> <span data-ttu-id="81d86-111">İptal etme faturası, orijinal faturaya karşı kapatılır.</span><span class="sxs-lookup"><span data-stu-id="81d86-111">The canceling invoice is settled against the original invoice.</span></span> 

<span data-ttu-id="81d86-112">Düzeltilmiş Fatura'yı deftere naklettikten sonra üç faturanız olacaktır:</span><span class="sxs-lookup"><span data-stu-id="81d86-112">After you post the corrected invoice, you will have three invoices:</span></span>

-   <span data-ttu-id="81d86-113">**Orijinal fatura** – Düzelttiğiniz bilgileri içeren fatura.</span><span class="sxs-lookup"><span data-stu-id="81d86-113">**Original invoice** – The invoice that includes the information that you're correcting.</span></span>
-   <span data-ttu-id="81d86-114">**İptal faturası** – Oluşturulan en son Düzeltilmiş faturayı iptal etmek için sistem tarafından oluşturulan iade faturası.</span><span class="sxs-lookup"><span data-stu-id="81d86-114">**Canceling invoice** – The system-generated credit invoice that was created to cancel the invoice that was most recently corrected.</span></span>
-   <span data-ttu-id="81d86-115">**Düzeltilmiş fatura** – Düzeltilen fatura bilgileri içeren bir fatura.</span><span class="sxs-lookup"><span data-stu-id="81d86-115">**Corrected invoice** – The invoice that contains the corrected invoice information.</span></span>

<span data-ttu-id="81d86-116">İptal etme ve düzeltme faturalarını iki şekilde tanımlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="81d86-116">You can identify canceling and correcting invoices in two ways:</span></span>

-   <span data-ttu-id="81d86-117">**Tüm serbest metin faturaları** sayfası bir **Düzeltme** sütunu içerir, burada hangi faturaların iptal faturası ve düzeltme faturası olduğunu görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="81d86-117">The **All free text invoices** page includes a **Correction** column, where you can see which invoices are canceling invoices and corrected invoices.</span></span>
-   <span data-ttu-id="81d86-118">Dekont/Serbest metin faturası başlığı **İptal Faturası '\[fatura numarası]\]'** veya **Düzeltilmiş Fatura '\[fatura numarası\]'** durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="81d86-118">The header of the free text invoice shows a status of **Cancelling invoice '\[invoice number\]'** or **Corrected invoice '\[invoice number\]'**.</span></span>

> [!NOTE]
> <span data-ttu-id="81d86-119">Bu özellik sadece **Serbest metin fatura düzeltmesi** konfigürasyon anahtarı seçiliyse kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="81d86-119">This feature is available only if the **Free text invoice correction** configuration key is selected.</span></span> <span data-ttu-id="81d86-120">Yapılandırma anahtarlarının nasıl etkinleştirileceği hakkında daha fazla bilgi için [Bakım modu](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/maintenance-mode) konusundaki YApılandırma anahtarlarını Etkinleştir (veya Devre Dışı Bırak) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="81d86-120">For more information on how to enable Configuration keys refer to the Enable (or disable) configuration keys section in the [Maintenance mode](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/maintenance-mode) topic.</span></span> 




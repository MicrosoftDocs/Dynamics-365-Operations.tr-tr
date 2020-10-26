---
title: Satıcı faturası otomasyonu sonuçlarını görüntüleme (önizleme)
description: Bu konu, otomatik iş akışına gönder işleminde bulunan satıcı faturalarının durumunun nasıl görüntüleneceğini açıklamaktadır.
author: abruer
manager: AnnBe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 65e7929e612c8465f26a2f3bc7df6f13620e5b4e
ms.sourcegitcommit: 3387595e41fb03e98bb437588f6de78794ae383f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930955"
---
# <a name="view-vendor-invoice-automation-results-preview"></a><span data-ttu-id="628c7-103">Satıcı faturası otomasyonu sonuçlarını görüntüleme (önizleme)</span><span class="sxs-lookup"><span data-stu-id="628c7-103">View vendor invoice automation results (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="628c7-104">Bu konu, otomatik iş akışına gönder işleminde bulunan satıcı faturalarının durumunun nasıl görüntüleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="628c7-104">This topic explains how to view the status of vendor invoices that are in the automated submit-to-workflow process.</span></span> <span data-ttu-id="628c7-105">Her içe aktarılan satıcı faturası için otomasyon geçmişinin ayrıntıları korunur.</span><span class="sxs-lookup"><span data-stu-id="628c7-105">Details of the automation history are maintained for each imported vendor invoice.</span></span> <span data-ttu-id="628c7-106">Otomatikleştirdiğiniz iş süreçlerine bağlı olarak, **Bekleyen satıcı faturaları** sayfası **Otomatik giriş eşleştirme durumu** ve **Otomatik iş akışına gönderme durumu** değerlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="628c7-106">Depending on the business processes that you've automated, the **Pending vendor invoices** page shows **Automated receipt match status** and **Automated submit to workflow status** values.</span></span> <span data-ttu-id="628c7-107">Otomatik adımda başarısız olan faturalara odaklanmak için detayları görüntüleyebilir ve bir plan yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="628c7-107">You can view the details and make a plan to focus on the invoices that failed an automated step.</span></span> <span data-ttu-id="628c7-108">Daha sonra, sorunu düzelttikten sonra içe aktarılan fatura için otomatik işlemi devam ettirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="628c7-108">Then, after you correct the issue, you can resume the automated process for the imported invoice.</span></span>

<span data-ttu-id="628c7-109">Gönderilen bir faturayı düzenlemeden önce otomatik işlemeyi duraklatmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="628c7-109">Before you can edit an invoice that has been submitted, you must pause the automated processing.</span></span> <span data-ttu-id="628c7-110">Otomatik iş akışına gönderme işlemindeki bir faturanın duraklatılması gerekiyorsa, **Otomatik işlemeye dahil et** alanını **Satıcı faturaları** sayfasında **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="628c7-110">If an invoice in the automated submit-to-workflow process must be paused, set the **Include in Automated processing** field to **No** on the **Vendor invoices** page.</span></span> <span data-ttu-id="628c7-111">**Otomatik işleme dahil et** **Evet** olarak ayarlanana kadar otomasyon çalışmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="628c7-111">Automation then won't run until **Include in Automated processing** is set to **Yes**.</span></span> <span data-ttu-id="628c7-112">Bir fatura, henüz iş akışı sisteminde değilse ve otomatikleştirilmiş süreç tarafından kullanılmıyorsa, daha fazla otomasyon yapılmamak üzere duraklatılabilir.</span><span class="sxs-lookup"><span data-stu-id="628c7-112">An invoice can be paused from further automation if it isn't yet in the workflow system and isn't used by the automated process.</span></span>

<span data-ttu-id="628c7-113">İçe aktarılan bir fatura iş akışına gönder işlemine tabi ise, faturanın **Otomasyon durumu** değerini **Satıcı faturaları** sayfasında görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="628c7-113">If an imported invoice is subject to the submit-to-workflow process, you can view its **Automation status** value on the **Vendor invoices** page.</span></span> <span data-ttu-id="628c7-114">Aşağıdaki durumlar izlenir:</span><span class="sxs-lookup"><span data-stu-id="628c7-114">The following statuses are tracked:</span></span>

- <span data-ttu-id="628c7-115">**Dahil edildi** – **Borç hesapları parametreleri** sayfasında tanımlanan otomatik işlemler doğru çalışıyor, ancak henüz tamamlanmadı.</span><span class="sxs-lookup"><span data-stu-id="628c7-115">**Included** – The automated processes that are defined on the **Accounts payable parameters** page are running correctly but haven't yet been completed.</span></span>
- <span data-ttu-id="628c7-116">**Duraklatıldı** – **Borç hesapları parametreleri** sayfasında tanımlanan otomatik işlemler çalıştı ancak işlemde en az bir adım başarısız oldu.</span><span class="sxs-lookup"><span data-stu-id="628c7-116">**Paused** – The automated processes that are defined on the **Accounts payable parameters** page have run, but at least one step in the process failed.</span></span> <span data-ttu-id="628c7-117">**Duraklatıldı** durumu **Otomatik işleme dahil et** alanı **Hayır** olarak ayarlanmışsa da geçerli olur.</span><span class="sxs-lookup"><span data-stu-id="628c7-117">The **Paused** status is also applied if the **Include in automated processing** field is set to **No**.</span></span> <span data-ttu-id="628c7-118">**En son sonuçları görüntüle**'yi seçerek hataları görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="628c7-118">You can view the failures by selecting **View most recent results**.</span></span>
- <span data-ttu-id="628c7-119">**İş akışında** – İçe aktarılan fatura, otomatik iş akışına gönderme işlemi tarafından veya el ile iş akışı sistemine gönderildi.</span><span class="sxs-lookup"><span data-stu-id="628c7-119">**In workflow** – The imported invoice has been submitted to the workflow system, either by the automated submit-to-workflow process or manually.</span></span>
- <span data-ttu-id="628c7-120">**İş akışı tamamlandı** – İçe aktarılan fatura için iş akışı işlemi tamamlandı.</span><span class="sxs-lookup"><span data-stu-id="628c7-120">**Workflow complete** – The workflow process has been completed for the imported invoice.</span></span>

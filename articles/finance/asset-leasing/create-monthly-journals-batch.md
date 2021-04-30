---
title: Toplu işte aylık günlük girişleri oluşturma
description: Bu konuda, aylık kira giderleri kaydedilirken verimliliği artırmaya yardımcı olmak için toplu işte günlük girişlerinin nasıl oluşturulacağını açıklamaktadır.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ca84e56569ea5ddbb4d5335d0944a6bd8a50a1b1
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881216"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a><span data-ttu-id="aad48-103">Toplu işte aylık günlük girişleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="aad48-103">Create monthly journal entries in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aad48-104">Bu konuda, aylık kira giderleri kaydedilirken verimliliği artırmaya yardımcı olmak için toplu işte günlük girişlerinin nasıl oluşturulacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="aad48-104">This topic explains how to create journal entries in a batch to help increase efficiency when monthly lease expenses are recorded.</span></span> <span data-ttu-id="aad48-105">Birden fazla plandan günlük girişleri oluşturmak için toplu iş işleme kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="aad48-105">Batch processing can be used to create journal entries from multiple schedules.</span></span> <span data-ttu-id="aad48-106">Bu günlük girişleri arasında kira ödemeleri, yükümlülük amortismanı, kullanım hakkı (ROU) varlığı amortismanı ve icra maliyeti giderleri yer alır.</span><span class="sxs-lookup"><span data-stu-id="aad48-106">These journal entries can include lease payments, liability amortization, right-of-use (ROU) asset amortization, and executory cost expenses.</span></span> <span data-ttu-id="aad48-107">Aynı anda birden fazla kiralamanın ilk kabulünü yapmak veya aynı anda birden fazla kiralama için geçiş düzeltmeleri oluşturmak amacıyla toplu iş işlemeyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aad48-107">You can also use batch processing to do the initial recognition of multiple leases at the same time, or to create transition adjustments for multiple leases at the same time.</span></span>

<span data-ttu-id="aad48-108">Toplu iş ayarlamak veya birden fazla kiralama için ödeme faturaları, amortisman veya faiz işlemek amacıyla **Varlık kiralama \> Periyodik \> Toplu iş günlük oluşturma** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="aad48-108">To set up a batch job, or to process payment invoices, depreciation, or interest for multiple leases, go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span> <span data-ttu-id="aad48-109">Görüntülenen iletişim kutusunda, günlük girişlerinin oluşturulacağı planlamayı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aad48-109">In the dialog box that appears, you can select the schedule that the journal entries should be created from.</span></span> <span data-ttu-id="aad48-110">Toplu işin belirli varlıklar, kiralama grupları veya kiralama defterleri için çalıştırılıp çalıştırılmayacağını da belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aad48-110">You can also specify whether the batch process should be run for specific entities, lease groups, or lease books.</span></span>

> [!NOTE]
> <span data-ttu-id="aad48-111">Yükümlülük amortismanı planlaması, ödemeler, amortisman ve giderler gibi sonraki hareketler, yalnızca ilgili kiralama için ilk kabul deftere nakledildikten sonra deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="aad48-111">Subsequent transactions, such as liability amortization schedules, payments, depreciation, and expenses, will be posted only after the initial recognition for corresponding leases is posted.</span></span>
>
> <span data-ttu-id="aad48-112">Günlük girişleri oluşturulur ancak siz **Çalıştır** komutunu seçene kadar deftere nakledilemez.</span><span class="sxs-lookup"><span data-stu-id="aad48-112">The journal entries are created, but they won't be posted until you select the **Run** command.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

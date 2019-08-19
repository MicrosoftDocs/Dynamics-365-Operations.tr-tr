---
title: Muhasebe kaynağı gezgini
description: Bu makalede, genel muhasebe girişleri arkasındaki kaynak bilgilerinin ayrıntılı analizi için kullanabileceğiniz Muhasebe kaynağı gezgini hakkında bilgiler verilmektedir.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 904f1f9fb139248205b426aec5a0372f2edb1e59
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837530"
---
# <a name="accounting-source-explorer"></a><span data-ttu-id="01695-103">Muhasebe kaynağı gezgini</span><span class="sxs-lookup"><span data-stu-id="01695-103">Accounting source explorer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01695-104">Bu makalede, genel muhasebe girişleri arkasındaki kaynak bilgilerinin ayrıntılı analizi için kullanabileceğiniz Muhasebe kaynağı gezgini hakkında bilgiler verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="01695-104">This article provides information about Accounting source explorer, which you can use for detailed analysis of the source information behind general ledger accounting entries.</span></span>

<span data-ttu-id="01695-105">Muhasebe kaynağı gezgini, kaynak bilgilerini gösteren yeni bir sayfadır.</span><span class="sxs-lookup"><span data-stu-id="01695-105">Accounting source explorer is a new page that shows source information.</span></span> <span data-ttu-id="01695-106">Muhasebe kaynak gezginin, ister bir tek başına araç isterseniz de genel muhasebe defteri muhasebe girişleri arkasındaki ayrıntıları analiz etmek için bir araç olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01695-106">You can use Accounting source explorer either as a stand-alone tool or to analyze the details behind general ledger accounting entries.</span></span> <span data-ttu-id="01695-107">Örneğin, Muhasebe kaynak gezginini, Mizan içindeki bir bakiye veya fiş hareketindeki en ayrıntılı bilgiyi edinmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01695-107">For example, you can use Accounting source explorer to get the most detailed source information for a balance in Trail balance or for a voucher transaction.</span></span> <span data-ttu-id="01695-108">Ardından, bilgilerini Microsoft Excel programında ayrıntılı şekilde değerlendirmek (örneğin PivotTable raporu içinde veya üzerinde kullanmak) için MS Excel'e Aktar özelliğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01695-108">You can then use the Export to MS Excel feature to further slice and dice the information in Microsoft Excel (for example, in a PivotTable or on a PivotTable report).</span></span>

<span data-ttu-id="01695-109">Muhasebe kaynağı gezgini daima genel muhasebe hesabı için tutarı Genel defterde gösterildiği şekilde (örneğin Mizan) aynı olarak gösterir.</span><span class="sxs-lookup"><span data-stu-id="01695-109">Accounting source explorer always shows the same total amount per ledger account as General ledger shows (for example, in Trial balance).</span></span> <span data-ttu-id="01695-110">Mizanda olduğu gibi segmentleri ayrı sütunlarda görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01695-110">As in Trial balance, you can display segments in separate columns.</span></span> <span data-ttu-id="01695-111">Sadece uygun mali boyut kümesini seçmeniz yeterlidir.</span><span class="sxs-lookup"><span data-stu-id="01695-111">Just select the appropriate financial dimension set.</span></span> 

<span data-ttu-id="01695-112">Analiz için bir tarih aralığını tanımlamak için parametreleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01695-112">You can use parameters to define a date interval for the analysis.</span></span> <span data-ttu-id="01695-113">Bu işlev ayrıca Mizandaki işlevlere benzerdir.</span><span class="sxs-lookup"><span data-stu-id="01695-113">This functionality also resembles the functionality in Trial balance.</span></span>

<span data-ttu-id="01695-114">Kaynak belge çerçevesini kullanan tüm belgeler için, Muhasebe kaynak gezgini, muhasebe dağılımlarına dayanarak ve mevcutsa, proje muhasebe dağılımlarına dayanarak ek bilgiyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="01695-114">For all documents that use the source document framework, Accounting source explorer shows additional information, based on accounting distributions and, if applicable, project accounting distributions.</span></span> <span data-ttu-id="01695-115">Bu bilgilere, parasal tutar türü, proje, faaliyet, kategori ve satır özelliği dahildir.</span><span class="sxs-lookup"><span data-stu-id="01695-115">This information includes the monetary amount type, project, activity, category, and line property.</span></span> <span data-ttu-id="01695-116">Burada, gerçekleştirebileceğiniz analizlere bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="01695-116">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="01695-117">Satın alma emirleri ile satıcı faturaları arasındaki farklar, çünkü her bir fark örneğin masraf farkı vb. gibi bir parasal tutar türüyle temsil edilir</span><span class="sxs-lookup"><span data-stu-id="01695-117">Variances between purchase orders and vendor invoices, because each variance is represented by a monetary amount type, such as charge variance</span></span>
-   <span data-ttu-id="01695-118">Proje, ticari birim ve ana hesap başına faturalanabilir - faturalanamayan saatler ve masraflar karşılaştırması</span><span class="sxs-lookup"><span data-stu-id="01695-118">Billable versus non-billable hours and expenses per project, business unit, and main account</span></span>

<span data-ttu-id="01695-119">Kaynak belgesi referans kimlikleri konseptini kullanan kaynak belgeler için, Muhasebe kaynağı gezgini örneğin müşteri, satıcı, çalışan, ürün, miktar, birim metni ve açıklamalar gibi daha fazla ayrıntıyı gösterir.</span><span class="sxs-lookup"><span data-stu-id="01695-119">For source documents that use the source document reference identities concept, Accounting source explorer shows even more details, such as the customer, vendor, worker, product, quantity, unit text, and descriptions.</span></span> <span data-ttu-id="01695-120">Burada, gerçekleştirebileceğiniz analizlere bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="01695-120">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="01695-121">Bir mali dönem için maliyet raporlarına dayalı olarak ticari birim ve otel markası başına otel masrafları</span><span class="sxs-lookup"><span data-stu-id="01695-121">Hotel expenses per business unit and hotel brand for a fiscal period, based on expense reports</span></span>
-   <span data-ttu-id="01695-122">Satıcı, ürün, departman başına iskontolar</span><span class="sxs-lookup"><span data-stu-id="01695-122">Discounts per vendor, product, department</span></span>

<span data-ttu-id="01695-123">Bu belgeler için, Muhasebe kaynağı gezgininden ayrıca mevcut kaynak belgesine geçiş yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01695-123">For these documents, you can also navigate to the actual source document from Accounting source explorer.</span></span>




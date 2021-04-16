---
title: Genel muhasebe hareketine göre satış vergisi belirtimi raporu
description: Bu konu altında, Genel muhasebe hareketine göre satış vergisi belirtimi raporunun nasıl kullanılacağı, satış vergisi hesaplanan genel muhasebe hareketleri hakkındaki bilgilerin nasıl görüntüleneceği ve yazdırılacağı açıklanmaktadır.
author: ericwang
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 75913edcbac0151d5d27d866ff5430b194c62738
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815272"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a><span data-ttu-id="5b018-103">Genel muhasebe hareketine göre satış vergisi belirtimi raporu</span><span class="sxs-lookup"><span data-stu-id="5b018-103">Sales tax specification by ledger transaction report</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b018-104">Bu konu altında, **Genel muhasebe hareketine göre satış vergisi belirtimi** raporunun nasıl kullanılacağı, satış vergisi hesaplanan genel muhasebe hareketleri hakkındaki bilgilerin nasıl görüntüleneceği ve yazdırılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="5b018-104">This topic explains how to use the **Sales tax specification by ledger transaction** report to view and print information about ledger transactions that sales tax is calculated for.</span></span>

## <a name="tax-accounts-vs-non-tax-accounts"></a><span data-ttu-id="5b018-105">Vergi hesapları - vergi dışı hesaplar karşılaştırması</span><span class="sxs-lookup"><span data-stu-id="5b018-105">Tax accounts vs. non-tax accounts</span></span>

<span data-ttu-id="5b018-106">**Genel muhasebe hareketine göre satış vergisi belirtimi** raporu, hem vergi hesapları hem de vergi dışı hesaplar için vergi hareketlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5b018-106">The **Sales tax specification by ledger transaction** report shows tax transactions for both tax accounts and non-tax accounts.</span></span> <span data-ttu-id="5b018-107">Bu hesaplar aşağıdaki şekilde kategorize edilir:</span><span class="sxs-lookup"><span data-stu-id="5b018-107">These accounts are categorized in the following way:</span></span>

- <span data-ttu-id="5b018-108">**Vergi hesabı** – Bir vergi hareketi deftere nakledildiğinde hesap bir vergi hesabı olarak değerlendirilir ve **Satış Vergisi** günlük satırındaki ana hesap satış vergisi borç hesabı veya satış vergisi alacak hesabı gibi bir vergi hesabıdır.</span><span class="sxs-lookup"><span data-stu-id="5b018-108">**Tax account** – An account is considered a tax account when a tax transaction is posted, and the main account on the **Sales Tax** journal line is a tax account, such as a sales tax payable account or a sales tax receivable account.</span></span>
- <span data-ttu-id="5b018-109">**Vergi dışı hesap** – Bir vergi hareketi deftere nakledildiğinde hesap bir vergi dışı hesap olarak değerlendirilir ve orijinal hareketteki ana hesap, gelir hesabı veya gider hesabı gibi vergi dışı bir hesaptır.</span><span class="sxs-lookup"><span data-stu-id="5b018-109">**Non-tax account** – An account is considered a non-tax account when a tax transaction is posted, and the main account on the original transaction is a non-tax account, such as a revenue account or an expense account.</span></span>

<span data-ttu-id="5b018-110">Vergi hesapları için, rapordaki **Kaynak**, **Satış vergisi alacağı** ve **Satış vergisi borcu** sütunları **0** (sıfır) değerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5b018-110">For tax accounts, the **Origin**, **Sales tax receivable**, and **Sales tax payable** columns on the report show **0** (zero).</span></span> <span data-ttu-id="5b018-111">Vergi dışı hesaplar için bu sütunlar tutarları gösterir.</span><span class="sxs-lookup"><span data-stu-id="5b018-111">For non-tax accounts, those columns show amounts.</span></span>

## <a name="filtering-the-data-on-the-report"></a><span data-ttu-id="5b018-112">Rapordaki verileri filtreleme</span><span class="sxs-lookup"><span data-stu-id="5b018-112">Filtering the data on the report</span></span>

<span data-ttu-id="5b018-113">Raporu oluşturduğunuz zaman aşağıdaki varsayılan alanlar kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5b018-113">When you generate the report, the following default fields are available.</span></span> <span data-ttu-id="5b018-114">Bu alanları, raporda gösterilen verileri filtrelemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5b018-114">You can use these fields to filter the data that is shown on the report.</span></span>

| <span data-ttu-id="5b018-115">Alan</span><span class="sxs-lookup"><span data-stu-id="5b018-115">Field</span></span>                      | <span data-ttu-id="5b018-116">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b018-116">Description</span></span> |
|----------------------------|-------------|
| <span data-ttu-id="5b018-117">Tarih</span><span class="sxs-lookup"><span data-stu-id="5b018-117">Date</span></span>                       | <span data-ttu-id="5b018-118">Vergi hareketlerinin tarih aralığını tanımlamak için **Başlangıç** ve **Bitiş** bölümlerindeki alanları kullanın.</span><span class="sxs-lookup"><span data-stu-id="5b018-118">Use the fields in the **From** and **To** sections to define a date range for the tax transactions.</span></span> |
| <span data-ttu-id="5b018-119">Ana hesap</span><span class="sxs-lookup"><span data-stu-id="5b018-119">Main account</span></span>               | <span data-ttu-id="5b018-120">Bir ana hesaplar aralığı tanımlamak için **Başlangıç** ve **Bitiş** bölümlerindeki alanları kullanın.</span><span class="sxs-lookup"><span data-stu-id="5b018-120">Use the fields in the **From** and **To** sections to define a range of main accounts.</span></span> |
| <span data-ttu-id="5b018-121">Satış vergisi kodu</span><span class="sxs-lookup"><span data-stu-id="5b018-121">Sales tax code</span></span>             | <span data-ttu-id="5b018-122">Bir satış vergisi kodları aralığı tanımlamak için **Başlangıç** ve **Bitiş** bölümlerindeki alanları kullanın.</span><span class="sxs-lookup"><span data-stu-id="5b018-122">Use the fields in the **From** and **To** sections to define a range of sales tax codes.</span></span> |
| <span data-ttu-id="5b018-123">Gruplama</span><span class="sxs-lookup"><span data-stu-id="5b018-123">Grouping</span></span>                   | <span data-ttu-id="5b018-124">Raporun genel muhasebe hesabına göre mi yoksa satış vergisi koduna göre mi gruplandırılacağını seçin.</span><span class="sxs-lookup"><span data-stu-id="5b018-124">Select whether the report should be grouped by ledger account or sales tax code.</span></span> |
| <span data-ttu-id="5b018-125">Satış vergisi koduna göre alt toplamlar</span><span class="sxs-lookup"><span data-stu-id="5b018-125">Subtotal by sales tax code</span></span> | <span data-ttu-id="5b018-126">Satış vergisi koduna göre ara toplamları göstermek için bu seçeneği **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5b018-126">Set this option to **Yes** to show subtotals by sales tax code.</span></span> |
| <span data-ttu-id="5b018-127">Yalnızca toplamlar</span><span class="sxs-lookup"><span data-stu-id="5b018-127">Totals only</span></span>                | <span data-ttu-id="5b018-128">Yalnızca toplamları göstermek için bu seçeneği **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5b018-128">Set this option to **Yes** to show only totals.</span></span> |
| <span data-ttu-id="5b018-129">Yalnızca ana hesaplar</span><span class="sxs-lookup"><span data-stu-id="5b018-129">Main accounts only</span></span>         | <span data-ttu-id="5b018-130">Rapora yalnızca ana hesapları eklemek için bu seçeneği **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5b018-130">Set this option to **Yes** to include only main accounts on the report.</span></span> |

## <a name="showing-only-non-tax-accounts-on-the-report"></a><span data-ttu-id="5b018-131">Raporda yalnızca vergi dışı hesapları gösterme</span><span class="sxs-lookup"><span data-stu-id="5b018-131">Showing only non-tax accounts on the report</span></span>

<span data-ttu-id="5b018-132">Raporda yalnızca vergi dışı hesapları göstermek için aşağıdaki şekilde gösterildiği gibi bir filtre koşulu ayarlayın (örneğin yıldız (\*) girin).</span><span class="sxs-lookup"><span data-stu-id="5b018-132">To show only non-tax accounts on the report, set up a filter condition, such as an asterisk (\*), as shown in the following illustration.</span></span>

![Vergi dışı hesapları gösteren rapor](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
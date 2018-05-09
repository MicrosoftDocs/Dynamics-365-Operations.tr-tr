---
title: "Türetilmiş defterlerle deftere nakletme"
description: "Bu makale, türetilmiş defterlerin nasıl kullanılacağını açıklar."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 463c43f9960a21ab88da92febaa9a65e370326e8
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="post-with-derived-books"></a><span data-ttu-id="8ade2-103">Türetilmiş defterlerle deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="8ade2-103">Post with derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ade2-104">Bu makale, türetilmiş defterlerin nasıl kullanılacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="8ade2-104">This article describes how to use derived books.</span></span>

<span data-ttu-id="8ade2-105">Türetilmiş defterler içeren bir defter için hareketleri deftere naklettiğinizde, türetilmiş defter hareketleri otomatik olarak günlüklerde, satınalma siparişlerinde ve serbest metin faturalarında deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="8ade2-105">When you post transactions for a book that contains derived books, the derived book transactions are posted automatically in journals, purchase orders, or free text invoices.</span></span> <span data-ttu-id="8ade2-106">Ancak birincil defter hareketlerini Sabit kıymetler günlüğünde hazırlarsanız türetilmiş hareketlere ait miktarları deftere nakletmeden önce görüntüleyebilir ve değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8ade2-106">However, if you prepare the primary book transactions in the Fixed assets journal, you can view and modify the amounts of the derived transactions before you post them.</span></span>
-   <span data-ttu-id="8ade2-107">Satış vergisi ve müşteri veya satıcı hesapları gibi birtakım hesaplar yalnızca bir kez birincil defterin deftere nakilleriyle güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="8ade2-107">Certain accounts, such as sales tax and customer or vendor accounts, are updated only once by postings of the primary book.</span></span> <span data-ttu-id="8ade2-108">Türetilmiş defter hareketleri, Sabit kıymet nakil profilleri sayfasındaki türetilmiş defter için tanımlanmış hesaplardaki deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="8ade2-108">The derived book transactions are posted to the accounts that have been defined for the derived book in the Fixed asset posting profiles page.</span></span>
-   <span data-ttu-id="8ade2-109">Alım, çoğu zaman türetilmiş defter için hareket türü olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8ade2-109">Acquisition is often used as the transaction type for the derived books.</span></span> <span data-ttu-id="8ade2-110">Bunu, defter ile türetilmiş defterin, sabit kıymetin alım zamanından başlanarak sabit kıymete uygulanması gerektiği durumlarda kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="8ade2-110">You use this when the book and the derived book should be applied to the fixed asset from the time of the acquisition of the fixed asset.</span></span>
-   <span data-ttu-id="8ade2-111">Hareket türü bilgisine ait diğer değerler de uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="8ade2-111">Other values for the transaction type can also apply.</span></span> <span data-ttu-id="8ade2-112">Örneğin, birincil defter ve türetilmiş defterler satış veya elden çıkarma açısından aynı aralıklara sahipse bir türetilmiş defterin kurulumunda tüm sabit kıymet hareket türleri kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8ade2-112">For example, if the primary book and the derived books have the same intervals regarding sale or disposal, all fixed asset transaction types are available for the setup of a derived book.</span></span>

> [!WARNING]
> <span data-ttu-id="8ade2-113">Türetilmiş defterde deftere nakledilen amortisman, birincil defter için deftere nakledilen tutarın aynısı olur.</span><span class="sxs-lookup"><span data-stu-id="8ade2-113">Depreciation posted in the derived book will be the same amount as was posted for the primary book.</span></span> <span data-ttu-id="8ade2-114">Amortisman yöntemleri defterler arasında farklılık gösteriyorsa türetilmiş işlemini kullanarak amortisman hareketleri oluşturmamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8ade2-114">If the depreciation methods are different between the books, you should not generate depreciation transactions using the derived process.</span></span> |

## <a name="example"></a><span data-ttu-id="8ade2-115">Örnek</span><span class="sxs-lookup"><span data-stu-id="8ade2-115">Example</span></span> 
<span data-ttu-id="8ade2-116">Aşağıdaki bilgiler, türetilmiş defter işleviyle alım hareketlerinin nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="8ade2-116">The following information describes how to set up acquisition transactions with the derived book functionality.</span></span>

1.  <span data-ttu-id="8ade2-117">Defterler sayfasında defterler oluşturun.</span><span class="sxs-lookup"><span data-stu-id="8ade2-117">Create the books on the Books page.</span></span>
    -   <span data-ttu-id="8ade2-118">Muhasebeye yönelik defter: VM 1, Geçerli deftere nakil katmanı</span><span class="sxs-lookup"><span data-stu-id="8ade2-118">The book for accounting: VM 1, Current posting layer</span></span>
    -   <span data-ttu-id="8ade2-119">Vergi amaçlı defter: VM 2, Vergi deftere nakil katmanı</span><span class="sxs-lookup"><span data-stu-id="8ade2-119">The book for tax purposes: VM 2, Tax posting layer</span></span>

2.  <span data-ttu-id="8ade2-120">VM 1'de, Türetilen defterler sekmesine tıklayın. VM 2'yi Defter alanından ve Hareket türü alnından Satınalma'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="8ade2-120">On VM 1, click the Derived books tab. Select VM 2 in the Book field, and Acquisition in the Transaction type field.</span></span>

<span data-ttu-id="8ade2-121">Ardından, defterler belirli sabit kıymetlere eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="8ade2-121">The books then can be attached to specific fixed assets.</span></span> 

<span data-ttu-id="8ade2-122">Bir alım, defter VM 1'e sahip bir sabit kıymet için deftere nakledildiğinde, alım yalnızca VM 1'de değil, aynı zamanda türetilmiş defter VM 2'de de deftere nakledilmiştir.</span><span class="sxs-lookup"><span data-stu-id="8ade2-122">When an acquisition is posted for a fixed asset with book VM 1, the acquisition is posted not only on VM 1, but also on the derived book VM 2.</span></span> <span data-ttu-id="8ade2-123">Her iki sabit kıymet defterinin durumu da Açık olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="8ade2-123">The status of both fixed asset books is updated to Open.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="8ade2-124">Türetilmiş defterleri kullanmıyorsanız sabit kıymet alımını hem VM 1 defteri, hem de VM 2 defteri için deftere nakletmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8ade2-124">If you do not use derived books, you must post the acquisition of the fixed asset both for book VM 1 and book VM 2.</span></span>

<span data-ttu-id="8ade2-125">Daha fazla bilgi için bkz. [Türetilmiş defterler](derived-books.md).</span><span class="sxs-lookup"><span data-stu-id="8ade2-125">For more information, see [Derived books](derived-books.md)</span></span>





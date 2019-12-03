---
title: Perakende mağaza hareketleri için akış tabanlı sipariş oluşturma
description: Bu konuda, Microsoft Dynamics 365 Retail'deki perakende mağazası hareketleri için akış tabanlı sipariş oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: deb8399aa401af16b6fe123a433eb21864e178c6
ms.sourcegitcommit: 92322167f57b66d2accc134aaf862e6b9931ec94
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2019
ms.locfileid: "2693101"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a><span data-ttu-id="fe2e5-103">Perakende mağaza hareketleri için akış tabanlı sipariş oluşturma (Genel önizleme)</span><span class="sxs-lookup"><span data-stu-id="fe2e5-103">Trickle feed-based order creation for retail store transactions (Public preview)</span></span>

[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="fe2e5-104">Dynamics 365 Retail 10.0.4 ve önceki sürümlerinde, perakende ekstresi deftere nakli gün sonunda gerçekleştirilen bir işlemdir ve tüm hareketler günün sonunda defterlere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-104">In Dynamics 365 Retail versions 10.0.4 and earlier, retail statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="fe2e5-105">Büyük hareketler sınırlı bir zaman aralığında işlenmek zorunda olduğundan zaman zaman yük ve kilitlenmelere ve ekstre deftere nakil hatalarına yol açar.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="fe2e5-106">Ayrıca perakendeciler, gün içinde kendi defterlerinde gelir ve ödemeleri göremez.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="fe2e5-107">Retail sürüm 10.0.5'te genel önizlemesi sunulan akış tabanlı sipariş oluşturma özelliğiyle hareketler gün içinde işlenir. Yalnızca ödemelerle ilgili mali mutabakat ve diğer nakit yönetimi hareketleri günün sonunda işlenir.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-107">With the public preview of trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="fe2e5-108">Bu işlev satış siparişleri, faturalar ve ödemeler oluşturma yükünü gün içine dağıtarak daha iyi performans sağlar ve gelir ve ödemeleri defterlerde neredeyse gerçek zamanlı olarak görme olanağı tanır.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="fe2e5-109">Akış tabanlı deftere nakil özelliğini kullanma</span><span class="sxs-lookup"><span data-stu-id="fe2e5-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="fe2e5-110">Perakende hareketlerin deftere akış tabanlı olarak nakledilmesi özelliğini etkinleştirmek için **Sistem yönetimi > Kurulum > Lisans yapılandırması**'na gidin ve **Perakende ekstreleri** anahtarını devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-110">To enable trickle feed-based posting of retail transactions, go to **System administration > Set up > License configuration** and disable the the **Retail statements** key.</span></span>

2. <span data-ttu-id="fe2e5-111">Aynı sayfada **Perakende ekstreleri (akış) – Önizleme** lisans anahtarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-111">On the same page, enable the **Retail statements (trickle feed) – Preview** license key.</span></span> <span data-ttu-id="fe2e5-112">Bu anahtarı etkinleştirdiğinizde, deftere nakledilmeyi bekleyen bir ekstre bulunmadığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-112">When you enable this key, make sure there are no pending statements waiting to be posted.</span></span> 

> [!Important]
> <span data-ttu-id="fe2e5-113">**Perakende ekstreleri (akış) - Önizleme** lisansı anahtarını etkinleştirmeden önce, deftere nakledilmeyi bekleyen ekstreler bulunmadığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-113">Before you enable the **Retail statements (trickle feed) – Preview** license key, make sure that no pending statements are waiting to be posted.</span></span>

3. <span data-ttu-id="fe2e5-114">Geçerli ekstre belgesi iki farklı türe bölünür: hareket ekstresi ve mali tablo.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-114">The current statement document will be split into two different types; transactional statement and financial statement.</span></span>

      - <span data-ttu-id="fe2e5-115">Hareket ekstresi deftere nakledilmemiş ve doğrulanmış tüm perakende hareketlerini alır ve sizin yapılandırdığınız hızda satış siparişleri, satış faturaları, ödeme ve iskonto günlükleri ve gelir-gider hareketleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-115">The transactional statement will pick up all unposted and validated retail transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="fe2e5-116">Bu işlemi, perakende hareketleri P işi aracılığıyla Retail Headquarters'a yüklenirken belgelerin oluşturulmasını sağlamak için yüksek sıklıkta çalışmak üzere yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-116">You should configure this process to run at a high frequency so that documents are created when the retail transactions are uploaded into Retail Headquarters through the P-job.</span></span> <span data-ttu-id="fe2e5-117">Satış siparişlerini ve satış faturalarını zaten oluşturan hareket ekstresi sayesinde **Stoğu deftere naklet** toplu işini yapılandırmanıza gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-117">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="fe2e5-118">Ancak, bu yapılandırmayı özel iş gereksinimlerinizi karşılamak amacıyla kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-118">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="fe2e5-119">Mali tablo gün sonunda oluşturulacak şekilde tasarlanmıştır ve yalnızca **Vardiya** kapatma yöntemini destekler.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-119">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="fe2e5-120">Bu tablo mali mutabakatla sınırlandırılır ve yalnızca farklı ödemeler için sayılan tutar ile hareket tutarı arasındaki tutar farklarına yönelik günlükleri ve diğer nakit yönetimi hareketlerine ilişkin günlükleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-120">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

4. <span data-ttu-id="fe2e5-121">Hareket ekstresini hesaplamak için **Perakende > Perakende BT > POS Deftere nakil > Hareket ekstrelerini toplu işte hesapla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-121">To calculate the transactional statement, click **Retail > Retail IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="fe2e5-122">Hareket ekstrelerini toplu işle deftere nakletmek için **Perakende > Perakende BT > POS Deftere nakil > Hareket ekstrelerini toplu işle deftere naklet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-122">To post the transactional statement statements in batch, click **Retail > Retail IT > POS Posting > Post transactional statements in batch**.</span></span>

5. <span data-ttu-id="fe2e5-123">Mali tabloyu hesaplamak için **Perakende > Perakende BT > POS Deftere nakil > Mali tabloları toplu işte hesapla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-123">To calculate the financial statement, click **Retail > Retail IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="fe2e5-124">Mali tabloları toplu işle deftere nakletmek için **Perakende > Perakende BT > POS Deftere nakil > Mali tabloları toplu işle deftere naklet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-124">To post the financial statements in batch, click **Retail > Retail IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="fe2e5-125">**Perakende > Perakende BT > POS Deftere nakil > Ekstreleri toplu işle hesapla** ve **Perakende > Perakende BT > POS Deftere nakil > Ekstreleri toplu işle deftere naklet** menü öğeleri bu yeni özellikle birlikte kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-125">The menu items **Retail > Retail IT > POS Posting > Calculate statements in batch** and **Retail > Retail IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="fe2e5-126">Alternatif olarak, hareket ve mali tablo türlerini el ile oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-126">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="fe2e5-127">**Perakende > Kanallar > Perakende mağazaları**'na gidin ve **Perakende ekstreleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-127">Go to **Retail > Channels > Retail stores** and click **Retail statements**.</span></span> <span data-ttu-id="fe2e5-128">**Yeni**'ye tıklayın ve oluşturmak istediğiniz ekstre türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-128">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="fe2e5-129">**Perakende ekstreleri** sayfasındaki alanlar ve sayfanın **Ekstre grubu** altındaki eylemler, seçilen ekstre türüne göre ilgili verileri ve eylemleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="fe2e5-129">Fields on the **Retail statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>

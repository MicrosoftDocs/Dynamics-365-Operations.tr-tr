---
title: Perakende mağaza hareketleri için akış tabanlı sipariş oluşturma
description: Bu konuda, Microsoft Dynamics 365 Commerce'taki mağaza hareketleri için akış tabanlı sipariş oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 06/08/2020
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
ms.openlocfilehash: 6e097ead7cacb3f71452323656546a4be661457f
ms.sourcegitcommit: 7061a93f9f2b54aec4bc4bf0cc92691e86d383a6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "3710295"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a><span data-ttu-id="14502-103">Perakende mağaza hareketleri için akış tabanlı sipariş oluşturma</span><span class="sxs-lookup"><span data-stu-id="14502-103">Trickle feed-based order creation for retail store transactions</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="14502-104">Dynamics 365 Retail 10.0.4 ve önceki sürümlerinde, ekstre deftere nakli gün sonunda gerçekleştirilen bir işlemdir ve tüm hareketler günün sonunda defterlere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="14502-104">In Dynamics 365 Retail versions 10.0.4 and earlier, statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="14502-105">Büyük hareketler sınırlı bir zaman aralığında işlenmek zorunda olduğundan zaman zaman yük ve kilitlenmelere ve ekstre deftere nakil hatalarına yol açar.</span><span class="sxs-lookup"><span data-stu-id="14502-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="14502-106">Ayrıca perakendeciler, gün içinde kendi defterlerinde gelir ve ödemeleri göremez.</span><span class="sxs-lookup"><span data-stu-id="14502-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="14502-107">Retail sürüm 10.0.5'te sunulan akış tabanlı sipariş oluşturma özelliğiyle hareketler gün içinde işlenir. Yalnızca ödemelerle ilgili mali mutabakat ve diğer nakit yönetimi hareketleri günün sonunda işlenir.</span><span class="sxs-lookup"><span data-stu-id="14502-107">With trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="14502-108">Bu işlev satış siparişleri, faturalar ve ödemeler oluşturma yükünü gün içine dağıtarak daha iyi performans sağlar ve gelir ve ödemeleri defterlerde neredeyse gerçek zamanlı olarak görme olanağı tanır.</span><span class="sxs-lookup"><span data-stu-id="14502-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="14502-109">Akış tabanlı deftere nakil özelliğini kullanma</span><span class="sxs-lookup"><span data-stu-id="14502-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="14502-110">Hareketlerin deftere akış tabanlı olarak nakledilmesi özelliğini etkinleştirmek için **Sistem yönetimi > Ayarlar > Lisans yapılandırması** bölümüne gidin ve **Ekstreler** anahtarını devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="14502-110">To enable trickle feed-based posting of transactions, go to **System administration > Set up > License configuration** and disable the the **Statements** key.</span></span>

2. <span data-ttu-id="14502-111">Aynı sayfada, **Ekstreler (akış) – Önizleme** lisans anahtarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="14502-111">On the same page, enable the **Statements (trickle feed) – Preview** license key.</span></span> <span data-ttu-id="14502-112">Bu anahtarı etkinleştirdiğinizde, deftere nakledilmeyi bekleyen bir ekstre bulunmadığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="14502-112">When you enable this key, make sure there are no pending statements waiting to be posted.</span></span> 

    > [!Important]
    > <span data-ttu-id="14502-113">**Ekstreler (akış) - Önizleme** lisansı anahtarını etkinleştirmeden önce, deftere nakledilmeyi bekleyen ekstreler bulunmadığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="14502-113">Before you enable the **Statements (trickle feed) – Preview** license key, make sure that no pending statements are waiting to be posted.</span></span>

3. <span data-ttu-id="14502-114">Geçerli ekstre belgesi iki farklı türe bölünür: hareket ekstresi ve mali tablo.</span><span class="sxs-lookup"><span data-stu-id="14502-114">The current statement document will be split into two different types; transactional statement and financial statement.</span></span>

      - <span data-ttu-id="14502-115">Hareket ekstresi, deftere nakledilmemiş ve doğrulanmış tüm hareketleri alır ve sizin yapılandırdığınız hızda satış siparişleri, satış faturaları, ödeme ve iskonto günlükleri ve gelir-gider hareketleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="14502-115">The transactional statement will pick up all unposted and validated transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="14502-116">Bu işlemi, hareketleri P işi aracılığıyla Genel Merkez'e yüklenirken belgelerin oluşturulmasını sağlamak için yüksek sıklıkta çalışmak üzere yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="14502-116">You should configure this process to run at a high frequency so that documents are created when the transactions are uploaded into Headquarters through the P-job.</span></span> <span data-ttu-id="14502-117">Satış siparişlerini ve satış faturalarını zaten oluşturan hareket ekstresi sayesinde **Stoğu deftere naklet** toplu işini yapılandırmanıza gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="14502-117">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="14502-118">Ancak, bu yapılandırmayı özel iş gereksinimlerinizi karşılamak amacıyla kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="14502-118">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="14502-119">Mali tablo gün sonunda oluşturulacak şekilde tasarlanmıştır ve yalnızca **Vardiya** kapatma yöntemini destekler.</span><span class="sxs-lookup"><span data-stu-id="14502-119">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="14502-120">Bu tablo, mali mutabakatla sınırlandırılır ve yalnızca farklı ödemeler için sayılan tutar ile hareket tutarı arasındaki tutar farklarına yönelik günlükleri ve diğer nakit yönetimi hareketlerine ilişkin günlükleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="14502-120">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

4. <span data-ttu-id="14502-121">Hareket ekstresini hesaplamak için **Retail ve Commerce > Retail ve Commerce BT > POS deftere nakli > Hareket ekstrelerini toplu işte hesapla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="14502-121">To calculate the transactional statement, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="14502-122">Hareket ekstrelerini toplu işle deftere nakletmek için **Retail ve Commerce > Retail ve Commerce BT > POS deftere nakli > Hareket ekstrelerini toplu işle deftere naklet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="14502-122">To post the transactional statement statements in batch, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Post transactional statements in batch**.</span></span>

5. <span data-ttu-id="14502-123">Mali tabloyu hesaplamak için **Retail ve Commerce > Retail ve Commerce BT > POS deftere nakli > Mali tabloları toplu işte hesapla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="14502-123">To calculate the financial statement, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="14502-124">Mali tabloları toplu işle deftere nakletmek için **Retail ve Commerce > Retail ve Commerce BT > POS deftere nakli > Mali tabloları toplu işle deftere naklet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="14502-124">To post the financial statements in batch, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="14502-125">**Retail ve Commerce > Retail ve Commerce BT > POS deftere nakli > Ekstreleri toplu işle hesapla** ve **Retail ve Commerce > Retail ve Commerce BT > POS deftere nakli > Ekstreleri toplu işle deftere naklet** menü öğeleri bu yeni özellikle birlikte kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="14502-125">The menu items **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate statements in batch** and **Retail and Commerce > Retail and Commerce IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="14502-126">Alternatif olarak, hareket ve mali tablo türlerini el ile oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="14502-126">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="14502-127">**Retail ve Commerce > Kanallar > Mağazalar**'a gidin ve **Ekstreler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="14502-127">Go to **Retail and Commerce > Channels > Stores** and click **Statements**.</span></span> <span data-ttu-id="14502-128">**Yeni**'ye tıklayın ve oluşturmak istediğiniz ekstre türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="14502-128">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="14502-129">**Ekstreler** sayfasındaki alanlar ve sayfanın **Ekstre grubu** altındaki eylemler, seçilen ekstre türüne göre ilgili verileri ve eylemleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="14502-129">Fields on the **Statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>

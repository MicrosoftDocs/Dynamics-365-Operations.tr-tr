---
title: Perakende mağaza hareketleri için akış tabanlı sipariş oluşturma
description: Bu konuda, Microsoft Dynamics 365 Commerce'taki mağaza hareketleri için akış tabanlı sipariş oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 09/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1f864fd6e3aa62cabd039922ed55ad5f7714f0ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991374"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a><span data-ttu-id="aabe8-103">Perakende mağaza hareketleri için akış tabanlı sipariş oluşturma</span><span class="sxs-lookup"><span data-stu-id="aabe8-103">Trickle feed-based order creation for retail store transactions</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="aabe8-104">Dynamics 365 Retail 10.0.4 ve önceki sürümlerinde, ekstre deftere nakli gün sonunda gerçekleştirilen bir işlemdir ve tüm hareketler günün sonunda defterlere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="aabe8-104">In Dynamics 365 Retail versions 10.0.4 and earlier, statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="aabe8-105">Büyük hareketler sınırlı bir zaman aralığında işlenmek zorunda olduğundan zaman zaman yük ve kilitlenmelere ve ekstre deftere nakil hatalarına yol açar.</span><span class="sxs-lookup"><span data-stu-id="aabe8-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="aabe8-106">Ayrıca perakendeciler, gün içinde kendi defterlerinde gelir ve ödemeleri göremez.</span><span class="sxs-lookup"><span data-stu-id="aabe8-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="aabe8-107">Retail sürüm 10.0.5'te sunulan akış tabanlı sipariş oluşturma özelliğiyle hareketler gün içinde işlenir. Yalnızca ödemelerle ilgili mali mutabakat ve diğer nakit yönetimi hareketleri günün sonunda işlenir.</span><span class="sxs-lookup"><span data-stu-id="aabe8-107">With trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="aabe8-108">Bu işlev satış siparişleri, faturalar ve ödemeler oluşturma yükünü gün içine dağıtarak daha iyi performans sağlar ve gelir ve ödemeleri defterlerde neredeyse gerçek zamanlı olarak görme olanağı tanır.</span><span class="sxs-lookup"><span data-stu-id="aabe8-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="aabe8-109">Akış tabanlı deftere nakil özelliğini kullanma</span><span class="sxs-lookup"><span data-stu-id="aabe8-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="aabe8-110">Perakende hareketlerinin akışa tabanlı olarak deftere naklini sağlamak için, Özellik yönetimini kullanarak **Perakende ekstreleri - Akış** adlı özelliği etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="aabe8-110">To enable trickle feed-based posting of retail transactions, enable the feature named **Retail statements - Trickle feed** using Feature management.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="aabe8-111">Özelliği etkinleştirmeden önce, deftere nakledilmeyi bekleyen ekstre bulunmadığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="aabe8-111">Before you enable the feature, make sure that no pending statements are waiting to be posted.</span></span>

2. <span data-ttu-id="aabe8-112">Geçerli ekstre belgesi iki türe bölünür: hareket ekstresi ve mali tablo.</span><span class="sxs-lookup"><span data-stu-id="aabe8-112">The current statement document will be split into two types: transactional statement and financial statement.</span></span>

      - <span data-ttu-id="aabe8-113">Hareket ekstresi, deftere nakledilmemiş ve doğrulanmış tüm hareketleri alır ve yapılandırdığınız hızda satış siparişleri, satış faturaları, ödeme ve iskonto günlükleri ve gelir-gider hareketleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aabe8-113">The transactional statement will pick up all unposted and validated transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="aabe8-114">Bu işlemi, hareketleri P işi aracılığıyla Genel Merkez'e yüklenirken belgelerin oluşturulmasını sağlamak için yüksek sıklıkta çalışmak üzere yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="aabe8-114">You should configure this process to run at a high frequency so that documents are created when the transactions are uploaded into Headquarters through the P-job.</span></span> <span data-ttu-id="aabe8-115">Satış siparişlerini ve satış faturalarını zaten oluşturan hareket ekstresi sayesinde **Stoğu deftere naklet** toplu işini yapılandırmanıza gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="aabe8-115">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="aabe8-116">Ancak, bu yapılandırmayı özel iş gereksinimlerinizi karşılamak amacıyla kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aabe8-116">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="aabe8-117">Mali tablo gün sonunda oluşturulacak şekilde tasarlanmıştır ve yalnızca **Vardiya** kapatma yöntemini destekler.</span><span class="sxs-lookup"><span data-stu-id="aabe8-117">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="aabe8-118">Bu tablo, mali mutabakatla sınırlandırılır ve yalnızca farklı ödemeler için sayılan tutar ile hareket tutarı arasındaki tutar farklarına yönelik günlükleri ve diğer nakit yönetimi hareketlerine ilişkin günlükleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aabe8-118">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

3. <span data-ttu-id="aabe8-119">Hareket ekstresini hesaplamak için **Retail ve Commerce > Retail ve Commerce BT > POS Deftere Nakli > Hareket ekstrelerini toplu olarak hesapla**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="aabe8-119">To calculate the transactional statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="aabe8-120">Hareket ekstrelerini toplu işle deftere nakletmek için **Retail ve Commerce > Retail ve Commerce BT > POS Deftere Nakli > Hareket ekstrelerini toplu olarak deftere naklet**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="aabe8-120">To post the transactional statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post transactional statements in batch**.</span></span>

4. <span data-ttu-id="aabe8-121">Mali tabloyu hesaplamak için **Retail ve Commerce > Retail ve Commerce BT > POS Deftere Nakli > Mali tabloları toplu olarak hesapla**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="aabe8-121">To calculate the financial statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="aabe8-122">Mali tabloları toplu işle deftere nakletmek için **Retail ve Commerce > Retail ve Commerce BT > POS Deftere Nakli > Mali tabloları toplu işle deftere naklet**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="aabe8-122">To post the financial statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="aabe8-123">**Retail ve Commerce > Retail ve Commerce BT > POS deftere nakli > Ekstreleri toplu işle hesapla** ve **Retail ve Commerce > Retail ve Commerce BT > POS deftere nakli > Ekstreleri toplu işle deftere naklet** menü öğeleri bu yeni özellikle birlikte kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="aabe8-123">The menu items **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate statements in batch** and **Retail and Commerce > Retail and Commerce IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="aabe8-124">Alternatif olarak, hareket ve mali tablo türlerini el ile oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aabe8-124">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="aabe8-125">**Retail ve Commerce > Kanallar > Mağazalar**'a gidin ve **Ekstreler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aabe8-125">Go to **Retail and Commerce > Channels > Stores** and click **Statements**.</span></span> <span data-ttu-id="aabe8-126">**Yeni**'ye tıklayın ve oluşturmak istediğiniz ekstre türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="aabe8-126">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="aabe8-127">**Ekstreler** sayfasındaki alanlar ve sayfanın **Ekstre grubu** altındaki eylemler, seçilen ekstre türüne göre ilgili verileri ve eylemleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="aabe8-127">Fields on the **Statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>

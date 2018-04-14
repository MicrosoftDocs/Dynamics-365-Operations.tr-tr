---
title: "POS için nakit para birimlerini yapılandırma"
description: "Banknotlar ve bozuk paralar için arka ofiste tanımlana nakit para birimleri, kasiyerler, satış sorumluları ve yöneticiler tarafından mağazada POS içerisinden kullanılabilir."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 4a7d80783368b6b39d48f80a3329d4053169c464
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="configure-cash-denominations-for-pos"></a><span data-ttu-id="d492f-103">POS için nakit para birimlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="d492f-103">Configure cash denominations for POS</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="d492f-104">Banknotlar ve bozuk paralar için arka ofiste tanımlana nakit para birimleri, kasiyerler, satış sorumluları ve yöneticiler tarafından mağazada POS içerisinden kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d492f-104">Cash denominations for notes and coins can be defined in the back office to be used by cashiers, sales associates, and managers at the store from within the POS.</span></span> <span data-ttu-id="d492f-105">Bu para birimleri, gün sonu kasa sayımlarında sayıma yardımcı olmak veya bir satışın sayımını hızlıca gerçekleştirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d492f-105">These denominations can be used to aid in counting cash for end of day tender declarations or for quickly tendering a sale.</span></span>

## <a name="define-denominations"></a><span data-ttu-id="d492f-106">Para birimlerini tanımla</span><span class="sxs-lookup"><span data-stu-id="d492f-106">Define denominations</span></span>
<span data-ttu-id="d492f-107">Para birimleri mağaza başına **Ayarlama** > **Mağaza özelliğinden nakit ara birimi seçeneği** üzerinde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="d492f-107">The denominations are set up per store on the **Set up** > **Cash declaration option from the store property** page.</span></span> 

![nakit para birimleri](./media/image1-denomination.png)

<span data-ttu-id="d492f-109">Bir para birimini tanımlamak için:</span><span class="sxs-lookup"><span data-stu-id="d492f-109">To define a denomination:</span></span>
1. <span data-ttu-id="d492f-110">**Yeni**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d492f-110">Click **New**.</span></span>
1. <span data-ttu-id="d492f-111">Türü belirtin (bozuk para veya banknot).</span><span class="sxs-lookup"><span data-stu-id="d492f-111">Specify the type (coin or note).</span></span>
1. <span data-ttu-id="d492f-112">Tutarı (değeri) belirtin.</span><span class="sxs-lookup"><span data-stu-id="d492f-112">Specify the amount (value).</span></span>

![nakit para birimleri](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a><span data-ttu-id="d492f-114">İşlev profilini yapılandırın</span><span class="sxs-lookup"><span data-stu-id="d492f-114">Configure the functionality profile</span></span>
<span data-ttu-id="d492f-115">POS içinde nakit ile öderken, kullanıcı banknot para birimlerini, müşteri tarafından ödenen tutarı hızlıca girmek için kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="d492f-115">When paying by cash in POS, the user can use the note denominations to quickly enter the amount paid by the customer.</span></span> <span data-ttu-id="d492f-116">İşlev profilinde, para birimini POS içerisinde göstermek için iki seçeneği yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d492f-116">In the functionality profile, you can configure the two options for showing the denomination in POS.</span></span>

<span data-ttu-id="d492f-117">**Vadesi gelen tutara eşit veya büyük**: Varsayılan olarak, POS yalnızca vadesi gelen tutardan büyük olan banknot para birimlerini gösterir, bu da tek dokunuşla kasa sayımına olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="d492f-117">**Greater or equal to amount due**: By default, POS will only show the note denominations that are greater than the amount due, which allows for one-touch tendering.</span></span> <span data-ttu-id="d492f-118">Örneğin, vadesi gelen tutar 7,50 $ ise, POS aşağıdaki para birimlerini gösterir: 10 $, 20 $, 50 $ ve 100 $.</span><span class="sxs-lookup"><span data-stu-id="d492f-118">For example, if the amount due is $7.50, POS would show the following denominations: $10, $20, $50, and $100.</span></span> <span data-ttu-id="d492f-119">Bu tutarlardan herhangi birine dokunmak, satış için kasa sayımını otomatik olarak bu tutardan yapar.</span><span class="sxs-lookup"><span data-stu-id="d492f-119">Touching any of these amounts will automatically tender the sale for that amount.</span></span> <span data-ttu-id="d492f-120">1 $ ve 5 $ banknotları, bunların vadesi gelen tutardan daha az olmalarından dolayı görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="d492f-120">The $1 and $5 notes are not shown since these amounts are less than the amount due.</span></span>

<span data-ttu-id="d492f-121">**Tüm para birimleri**: Tüm banknot para birimlerini, vadesi gelen tutardan bağımsız olarak POS içerisinde her zaman göstermek için bu seçeneği seçin.</span><span class="sxs-lookup"><span data-stu-id="d492f-121">**All denominations**: Select this option to always show all note denominations in POS, regardless of the amount due.</span></span> <span data-ttu-id="d492f-122">Bu, kullanıcının vadesi gelen tutara ulaşmak için banknot kombinasyonlarını kullanabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="d492f-122">This means that the user can use a combination of notes to reach the amount due.</span></span> <span data-ttu-id="d492f-123">Örneğin, vadesi gelen tutar 25,00 $ ise, kullanıcı satışı tamamlamak için 20 $ ve 5 $ seçebilir.</span><span class="sxs-lookup"><span data-stu-id="d492f-123">For example, if the amount due is $25.00, the user can choose $20 and $5 to complete the sale.</span></span>


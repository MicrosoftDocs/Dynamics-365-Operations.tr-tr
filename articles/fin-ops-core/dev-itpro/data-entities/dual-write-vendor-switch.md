---
title: Satıcı tasarımları arasında geçiş yapma
description: ''
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772376"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="43ea0-102">Satıcı tasarımları arasında geçiş yapma</span><span class="sxs-lookup"><span data-stu-id="43ea0-102">Switch between vendor designs</span></span>

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="43ea0-103">Satıcı veri akışı</span><span class="sxs-lookup"><span data-stu-id="43ea0-103">Vendor data flow</span></span> 

<span data-ttu-id="43ea0-104">Satıcı yönetimi için diğer Dynamics 365 uygulamalarını kullanmak ve satıcı bilgilerini müşterilerden ayırmak istiyorsanız bu temel satıcı tasarımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="43ea0-104">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![Temel satıcı akışı](media/dual-write-switch-1.png)
 
<span data-ttu-id="43ea0-106">Satıcı yönetimi için diğer Dynamics 365 uygulamalarını kullanmak ve satıcı bilgilerini depolamak için **Hesap** varlığını kullanmaya devam etmek istiyorsanız bu genişletilmiş satıcı tasarımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="43ea0-106">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="43ea0-107">Bu tasarımda, satıcı beklemede durumu ve satıcı profili gibi genişletilmiş satıcı bilgileri Common Data Service'te **satıcılar** varlığında depolanır.</span><span class="sxs-lookup"><span data-stu-id="43ea0-107">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![Genişletilmiş satıcı akışı](media/dual-write-switch-2.png)
 
<span data-ttu-id="43ea0-109">Genişletilmiş satıcı tasarımını kullanmak için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="43ea0-109">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="43ea0-110">**SupplyChainCommon** çözüm paketi, aşağıdaki görüntüde gösterilen iş akışı işlem şablonlarını içerir.</span><span class="sxs-lookup"><span data-stu-id="43ea0-110">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="43ea0-111">![İş akışı işlem şablonları](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="43ea0-111">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="43ea0-112">İş akışı işlem şablonlarını kullanarak yeni iş akışı işlemleri oluşturma:</span><span class="sxs-lookup"><span data-stu-id="43ea0-112">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="43ea0-113">**Hesap Varlığında Satıcılar Oluşturma** iş akışı işlemi şablonunu kullanarak **Satıcı** varlığı için yeni bir iş akışı işlemi oluşturun ve **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="43ea0-113">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="43ea0-114">Bu iş akışı **Hesap** varlığı için satıcı oluşturma senaryosunu işler.</span><span class="sxs-lookup"><span data-stu-id="43ea0-114">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="43ea0-115">![Hesap Varlığında Satıcılar oluşturma](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="43ea0-115">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="43ea0-116">**Hesaplar Varlığını Güncelleştirme** iş akışı işlemi şablonunu kullanarak **Satıcı** varlığı için yeni bir iş akışı işlemi oluşturun ve **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="43ea0-116">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="43ea0-117">Bu iş akışı **Hesap** varlığı için satıcı güncelleştirme senaryosunu işler.</span><span class="sxs-lookup"><span data-stu-id="43ea0-117">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="43ea0-118">![Hesaplar Varlığını Güncelleştirme](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="43ea0-118">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="43ea0-119">**Hesaplar** varlığında oluşturulan şablonlardan yeni iş akışı işlemleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="43ea0-119">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="43ea0-120">![Satıcılar varlığında satıcılar oluşturma](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="43ea0-120">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="43ea0-121">![Satıcı varlığını güncelleştirme](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="43ea0-121">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="43ea0-122">İş akışlarını gereksinimlerinize göre gerçek zamanlı veya arka plan iş akışları olarak yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="43ea0-122">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="43ea0-123">![Arka plan iş akışına dönüştürme](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="43ea0-123">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="43ea0-124">Satıcı bilgilerini depolamak için Customer Engagement **Hesap** varlığını kullanmaya başlamak için **Hesap** ve **Satıcı** varlıklarında oluşturduğunuz iş akışlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="43ea0-124">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the Customer Engagement **Account** entity for storing vendor information.</span></span> 
 

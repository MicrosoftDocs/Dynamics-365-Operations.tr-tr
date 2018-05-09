--- 
title: "ISO20022 ödeme biçimini kullanarak satıcı ödemeleri oluşturma ve dışa aktarma"
description: "Bu yordamda, Satıcı ödeme günlüğünde ödeme satırlarının ve ISO2022 Alacak transferi örneğini kullanarak bir satıcı ödemesi dosyasının nasıl oluşturulacağını gösterir."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 906f9611370e19ad4f063d15608d3564c5292c96
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="6420f-103">ISO20022 ödeme biçimini kullanarak satıcı ödemeleri oluşturma ve dışa aktarma</span><span class="sxs-lookup"><span data-stu-id="6420f-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6420f-104">Bu yordamda, Satıcı ödeme günlüğünde ödeme satırlarının ve ISO2022 Alacak transferi örneğini kullanarak bir satıcı ödemesi dosyasının nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6420f-104">This procedure shows how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span> 

<span data-ttu-id="6420f-105">Bu yordamı oluşturmak için kullanılan demo veri şirketi DEMF'dir.</span><span class="sxs-lookup"><span data-stu-id="6420f-105">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="6420f-106">Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak satıcı ödemesi işlemini gösteren beş yordamın beşincisidir.</span><span class="sxs-lookup"><span data-stu-id="6420f-106">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="6420f-107">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="6420f-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-payment-lines"></a><span data-ttu-id="6420f-108">Ödeme satırları oluşturun</span><span class="sxs-lookup"><span data-stu-id="6420f-108">Create payment lines</span></span>
1. <span data-ttu-id="6420f-109">Borç hesapları > Ödemeler > Ödeme günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="6420f-109">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="6420f-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6420f-110">Click New.</span></span>
3. <span data-ttu-id="6420f-111">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6420f-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="6420f-112">Ad alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6420f-112">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="6420f-113">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6420f-113">Click Lines.</span></span>
6. <span data-ttu-id="6420f-114">Ödeme teklifi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6420f-114">Click Payment proposal.</span></span>
7. <span data-ttu-id="6420f-115">Ödeme teklifi oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6420f-115">Click Create payment proposal.</span></span>
8. <span data-ttu-id="6420f-116">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="6420f-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="6420f-117">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6420f-117">Click Filter.</span></span>
10. <span data-ttu-id="6420f-118">Listede, Satıcılar tablosu ve Satıcı hesabı alanı için satır seçin.</span><span class="sxs-lookup"><span data-stu-id="6420f-118">In the list, select the row for Vendors table and Vendor account field.</span></span>
11. <span data-ttu-id="6420f-119">Ölçütler alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="6420f-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="6420f-120">Ödeme yapmak için satıcı hareketlerini seçmek amacıyla herhangi bir ölçütü uygulayabilirsiniz. Bu örnek satıcı hesabı olarak DE-001'i kullanır.</span><span class="sxs-lookup"><span data-stu-id="6420f-120">You can apply any criteria for selecting vendor transactions to pay, for this example use DE-001 as a vendor account.</span></span>  
12. <span data-ttu-id="6420f-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6420f-121">Click OK.</span></span>
13. <span data-ttu-id="6420f-122">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6420f-122">Click OK.</span></span>
14. <span data-ttu-id="6420f-123">Ödemeleri oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6420f-123">Click Create payments.</span></span>

## <a name="generate-an-iso20022-payment-file"></a><span data-ttu-id="6420f-124">ISO20022 ödeme dosyası oluşturma</span><span class="sxs-lookup"><span data-stu-id="6420f-124">Generate an ISO20022 payment file</span></span>



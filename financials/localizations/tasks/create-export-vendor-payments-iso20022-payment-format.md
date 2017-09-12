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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7cc90bc86cd489b124a806c480632dd53ba47f3f
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="e81d0-103">ISO20022 ödeme biçimini kullanarak satıcı ödemeleri oluşturma ve dışa aktarma</span><span class="sxs-lookup"><span data-stu-id="e81d0-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e81d0-104">Bu yordamda, Satıcı ödeme günlüğünde ödeme satırlarının ve ISO2022 Alacak transferi örneğini kullanarak bir satıcı ödemesi dosyasının nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e81d0-104">This procedure shows how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span> 

<span data-ttu-id="e81d0-105">Bu yordamı oluşturmak için kullanılan demo veri şirketi DEMF'dir.</span><span class="sxs-lookup"><span data-stu-id="e81d0-105">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="e81d0-106">Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak satıcı ödemesi işlemini gösteren beş yordamın beşincisidir.</span><span class="sxs-lookup"><span data-stu-id="e81d0-106">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="e81d0-107">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="e81d0-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-payment-lines"></a><span data-ttu-id="e81d0-108">Ödeme satırları oluşturun</span><span class="sxs-lookup"><span data-stu-id="e81d0-108">Create payment lines</span></span>
1. <span data-ttu-id="e81d0-109">Borç hesapları > Ödemeler > Ödeme günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e81d0-109">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="e81d0-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e81d0-110">Click New.</span></span>
3. <span data-ttu-id="e81d0-111">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="e81d0-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="e81d0-112">Ad alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="e81d0-112">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="e81d0-113">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e81d0-113">Click Lines.</span></span>
6. <span data-ttu-id="e81d0-114">Ödeme teklifi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e81d0-114">Click Payment proposal.</span></span>
7. <span data-ttu-id="e81d0-115">Ödeme teklifi oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e81d0-115">Click Create payment proposal.</span></span>
8. <span data-ttu-id="e81d0-116">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="e81d0-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="e81d0-117">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e81d0-117">Click Filter.</span></span>
10. <span data-ttu-id="e81d0-118">Listede, Satıcılar tablosu ve Satıcı hesabı alanı için satır seçin.</span><span class="sxs-lookup"><span data-stu-id="e81d0-118">In the list, select the row for Vendors table and Vendor account field.</span></span>
11. <span data-ttu-id="e81d0-119">Ölçütler alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="e81d0-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="e81d0-120">Ödeme yapmak için satıcı hareketlerini seçmek amacıyla herhangi bir ölçütü uygulayabilirsiniz. Bu örnek satıcı hesabı olarak DE-001'i kullanır.</span><span class="sxs-lookup"><span data-stu-id="e81d0-120">You can apply any criteria for selecting vendor transactions to pay, for this example use DE-001 as a vendor account.</span></span>  
12. <span data-ttu-id="e81d0-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e81d0-121">Click OK.</span></span>
13. <span data-ttu-id="e81d0-122">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e81d0-122">Click OK.</span></span>
14. <span data-ttu-id="e81d0-123">Ödemeleri oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e81d0-123">Click Create payments.</span></span>

## <a name="generate-an-iso20022-payment-file"></a><span data-ttu-id="e81d0-124">ISO20022 ödeme dosyası oluşturma</span><span class="sxs-lookup"><span data-stu-id="e81d0-124">Generate an ISO20022 payment file</span></span>



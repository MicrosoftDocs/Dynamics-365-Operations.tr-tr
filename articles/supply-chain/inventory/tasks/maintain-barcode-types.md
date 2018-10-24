--- 
title: "Barkod türlerini koru"
description: "Bu yordam, malzeme çekme listesi raporunun bir parçası olarak da kullanılabilen yeni bir barkod açıklamasının nasıl ayarlanacağını gösterir."
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: a0d7092228f078f528ec1cb9ac56d7034c44bccf
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="maintain-barcode-types"></a><span data-ttu-id="3db73-103">Barkod türlerini koru</span><span class="sxs-lookup"><span data-stu-id="3db73-103">Maintain barcode types</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3db73-104">Bu yordam, malzeme çekme listesi raporunun bir parçası olarak da kullanılabilen yeni bir barkod açıklamasının nasıl ayarlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3db73-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="3db73-105">Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3db73-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="3db73-106">USMF kullanıyorsanız, gösterilen örnek değerleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3db73-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="3db73-107">Bu görevler genellikle ambar Yöneticisi tarafından yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="3db73-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="3db73-108">Barkodlar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="3db73-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="3db73-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3db73-109">Click New.</span></span>
3. <span data-ttu-id="3db73-110">Barkod ayarı alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3db73-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="3db73-111">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3db73-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3db73-112">Barkod türü alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="3db73-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="3db73-113">USMF kullanıyorsanız, 'Code 39' öğesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3db73-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="3db73-114">Boyut alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3db73-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="3db73-115">Maksimum uzunluk alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3db73-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="3db73-116">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3db73-116">Click Save.</span></span>
9. <span data-ttu-id="3db73-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3db73-117">Close the page.</span></span>
10. <span data-ttu-id="3db73-118">Stok ve ambar yönetim parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="3db73-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="3db73-119">Barkod ayarı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="3db73-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="3db73-120">Daha önce oluşturduğunuz barkod ayarını seçin, ancak barkod biçiminin işleminde kullanılan kayıt türünün benzersiz tanımlayıcı biçimiyle eşleşmesi gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="3db73-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="3db73-121">Örneğin, malzeme çekme rotalarının barkod biçimi genellikle bir numara sırası olan malzeme çekme rotası başvuru biçimiyle eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="3db73-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="3db73-122">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3db73-122">Click Save.</span></span>
13. <span data-ttu-id="3db73-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3db73-123">Close the page.</span></span>



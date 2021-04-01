---
title: Barkod türlerini koru
description: Bu yordam, malzeme çekme listesi raporunun bir parçası olarak da kullanılabilen yeni bir barkod açıklamasının nasıl ayarlanacağını gösterir.
author: perlynne
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 112438417e425b8b77dd56f25e0b6e6db21c5148
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244411"
---
# <a name="maintain-barcode-types"></a><span data-ttu-id="4a687-103">Barkod türlerini koru</span><span class="sxs-lookup"><span data-stu-id="4a687-103">Maintain barcode types</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4a687-104">Bu yordam, malzeme çekme listesi raporunun bir parçası olarak da kullanılabilen yeni bir barkod açıklamasının nasıl ayarlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4a687-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="4a687-105">Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4a687-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="4a687-106">USMF kullanıyorsanız, gösterilen örnek değerleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4a687-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="4a687-107">Bu görevler genellikle ambar Yöneticisi tarafından yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="4a687-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="4a687-108">Barkodlar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="4a687-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="4a687-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4a687-109">Click New.</span></span>
3. <span data-ttu-id="4a687-110">Barkod ayarı alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="4a687-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="4a687-111">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="4a687-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4a687-112">Barkod türü alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="4a687-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="4a687-113">USMF kullanıyorsanız, 'Code 39' öğesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4a687-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="4a687-114">Boyut alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="4a687-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="4a687-115">Maksimum uzunluk alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="4a687-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="4a687-116">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4a687-116">Click Save.</span></span>
9. <span data-ttu-id="4a687-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4a687-117">Close the page.</span></span>
10. <span data-ttu-id="4a687-118">Stok ve ambar yönetim parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="4a687-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="4a687-119">Barkod ayarı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="4a687-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="4a687-120">Daha önce oluşturduğunuz barkod ayarını seçin, ancak barkod biçiminin işleminde kullanılan kayıt türünün benzersiz tanımlayıcı biçimiyle eşleşmesi gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="4a687-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="4a687-121">Örneğin, malzeme çekme rotalarının barkod biçimi genellikle bir numara sırası olan malzeme çekme rotası başvuru biçimiyle eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="4a687-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="4a687-122">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4a687-122">Click Save.</span></span>
13. <span data-ttu-id="4a687-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4a687-123">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
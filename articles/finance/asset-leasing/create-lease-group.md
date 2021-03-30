---
title: Kiralama grubu oluşturma
description: Bu konuda, kiralama gruplarının nasıl ayarlanacağı açıklanmaktadır. Yeni kiralamalar oluşturmak için kiralama grupları gereklidir.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e8ad226e87776615d9c19a239e0fb90b648d9c49
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210469"
---
# <a name="create-a-lease-group"></a><span data-ttu-id="5a5e7-104">Kiralama grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="5a5e7-104">Create a lease group</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a5e7-105">Bu konuda, kiralama gruplarının nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-105">This topic explains how to set up lease groups.</span></span> <span data-ttu-id="5a5e7-106">Yeni kiralamalar oluşturmak için kiralama grupları gereklidir.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-106">Lease groups are required to create new leases.</span></span> <span data-ttu-id="5a5e7-107">Kiralama defterleri her bir kiralama grubuyla ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-107">Lease books are associated with each lease group.</span></span> <span data-ttu-id="5a5e7-108">Kiralama defterleri, her kiralama için oluşturulması gereken varsayılan defterleri belirler.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-108">Lease books determine the default books that must be created for each lease.</span></span> <span data-ttu-id="5a5e7-109">**Kiralamayı deftere nakletme parametreleri** sayfasında bir kiralama grubuna belirli hesaplar atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-109">You can assign specific accounts to a lease group on the **Lease posting parameters** page.</span></span>

## <a name="create-a-lease-book-and-add-a-lease-group"></a><span data-ttu-id="5a5e7-110">Kiralama defteri oluşturma ve kiralama grubu ekleme</span><span class="sxs-lookup"><span data-stu-id="5a5e7-110">Create a lease book and add a lease group</span></span>

1. <span data-ttu-id="5a5e7-111">**Varlık kiralama \> Kurulum \> Kiralama grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-111">Go to **Asset leasing \> Setup \> Lease groups**.</span></span>
2. <span data-ttu-id="5a5e7-112">Eylem Bölmesinde, kiralama grubu eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-112">On the Action Pane, select **New** to add a lease group.</span></span> <span data-ttu-id="5a5e7-113">Izgaraya yeni bir satır eklenir.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-113">A line is added to the grid.</span></span>
3. <span data-ttu-id="5a5e7-114">Yeni satırdaki **Kiralama grubu** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-114">On the new line, in the **Lease group** field, enter a value.</span></span>
4. <span data-ttu-id="5a5e7-115">**Açıklama** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-115">In the **Description** field, enter a value.</span></span>

<span data-ttu-id="5a5e7-116">Yeni girdiğiniz bilgiler, **Kiralama ekle** sayfasındaki **Kiralama grubu**'na eklenir.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-116">The information that you just entered is added to the **Lease group** field on the **Add lease** page.</span></span>

## <a name="associate-a-book-with-a-lease-group"></a><span data-ttu-id="5a5e7-117">Defteri bir kiralama grubuyla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="5a5e7-117">Associate a book with a lease group</span></span>

<span data-ttu-id="5a5e7-118">Kiralama grupları oluşturduktan sonra her gruba defter atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-118">After you create lease groups, you can assign books to each group.</span></span> <span data-ttu-id="5a5e7-119">Kiralama oluşturup bunu bir kiralama grubuna atadıktan sonra sistem, söz konusu kiralama grubuyla ilişkili her defter için bir dizi plan oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-119">When you create a lease and assign it to a lease group, the system creates a set of schedules for each book that is associated with that lease group.</span></span>

> [!NOTE]
> <span data-ttu-id="5a5e7-120">Defterler kiralama grubuna atanmadan önce ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-120">Books must be set up before they can be assigned to a lease group.</span></span>

1. <span data-ttu-id="5a5e7-121">**Varlık kiralama \> Kurulum \> Kiralama grubu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-121">Go to **Asset leasing \> Setup \> Lease group**.</span></span>
2. <span data-ttu-id="5a5e7-122">Bir kiralama grubunu seçin ve ardından **Defter**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-122">Select a lease group, and then select **Books**.</span></span>
3. <span data-ttu-id="5a5e7-123">**Yeni**'yi seçin ve ardından **Defter türü** alanında kiralama grubuna atanacak defteri seçin.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-123">Select **New**, and then, in the **Book type** field, select the book to assign to the lease group.</span></span> <span data-ttu-id="5a5e7-124">Bir kiralamanın farklı yöntemlerle hesaplanması gerekiyorsa bir kiralama grubuna birden fazla defter atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5a5e7-124">You can assign multiple books to a lease group if a lease must be accounted for in different ways.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
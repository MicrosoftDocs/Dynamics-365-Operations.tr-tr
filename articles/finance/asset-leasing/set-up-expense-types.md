---
title: Gider türlerini ayarlama
description: Bu konuda Varlık kiralamada giderleri ayarlama açıklanmaktadır.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b50f406c7411ff8ed990a312fde9c2fc0ba3c3db
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819710"
---
# <a name="set-up-expense-types"></a><span data-ttu-id="268cc-103">Gider türlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="268cc-103">Set up expense types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="268cc-104">Bu konuda Varlık kiralamada giderleri ayarlama açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="268cc-104">This topic explains how to set up expense types in Asset leasing.</span></span> <span data-ttu-id="268cc-105">Ödeme planı ile temsil edilmeyen maliyetler *gider maliyetleri* olarak bilinir.</span><span class="sxs-lookup"><span data-stu-id="268cc-105">Costs that aren't represented by the payment schedule are known as *expense costs*.</span></span> <span data-ttu-id="268cc-106">Bu maliyetlere örnek olarak emlak vergileri, ortak alan bakım maliyetleri ve sigorta giderleri verilebilir.</span><span class="sxs-lookup"><span data-stu-id="268cc-106">Examples of these costs include property taxes, common area maintenance costs, and insurance expenses.</span></span>

## <a name="add-an-administrative-expense-type"></a><span data-ttu-id="268cc-107">İdari gider türü ekleme</span><span class="sxs-lookup"><span data-stu-id="268cc-107">Add an administrative expense type</span></span>

1. <span data-ttu-id="268cc-108">**Varlık kiralama \> Kurulum \> Gider türleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="268cc-108">Go to **Asset leasing \> Setup \> Expense types**.</span></span>
2. <span data-ttu-id="268cc-109">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="268cc-109">Select **New**.</span></span>
3. <span data-ttu-id="268cc-110">Uygun alanlara yeni gider türünü ve açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="268cc-110">In the appropriate fields, enter the new expense type and a description.</span></span>

## <a name="assign-accounts-to-administrative-costs"></a><span data-ttu-id="268cc-111">İdari maliyetlere hesaplar atama</span><span class="sxs-lookup"><span data-stu-id="268cc-111">Assign accounts to administrative costs</span></span>

<span data-ttu-id="268cc-112">Daha sonra, hesapları gider türleriyle ilişkilendirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="268cc-112">Next, you should associate accounts with the expense types.</span></span> <span data-ttu-id="268cc-113">Gider planı girişleri deftere nakledildiğinde bu hesaplar borçlandırılır.</span><span class="sxs-lookup"><span data-stu-id="268cc-113">These accounts will be debited when expense schedule entries are posted.</span></span> <span data-ttu-id="268cc-114">Mahsup hesap, her bir kiralamadaki **İcra maliyeti ödeme planı** satırlarında belirtilir.</span><span class="sxs-lookup"><span data-stu-id="268cc-114">The offset account is specified on the **Executory costs payment schedule** lines on each lease.</span></span>

1. <span data-ttu-id="268cc-115">**Varlık kiralama \> Kurulum \> Varlık kiralama parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="268cc-115">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="268cc-116">**Hesaplar** sekmesindeki **İcra maliyetleri** hızlı sekmesinin **Gider türü** alanında gider türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="268cc-116">On the **Accounts** tab, on the **Executory costs** FastTab, in the **Expense type** field, select the expense type.</span></span>
3. <span data-ttu-id="268cc-117">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="268cc-117">Select **Add**.</span></span>
4. <span data-ttu-id="268cc-118">**Defter türü** alanında, idari maliyetlerle ilişkilendirilecek defter türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="268cc-118">In the **Book type** field, select the book type to link to the administrative costs.</span></span>

    > [!NOTE]
    > <span data-ttu-id="268cc-119">Aynı gider hesabına birden fazla defter türü bağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="268cc-119">Multiple book types can be linked to the same expense account.</span></span>

5. <span data-ttu-id="268cc-120">**Hesap kodu** alanında, defterin hangi kiralamalara uygulanacağını belirtin:</span><span class="sxs-lookup"><span data-stu-id="268cc-120">In the **Account code** field, specify which leases the book should be applied to:</span></span>

    - <span data-ttu-id="268cc-121">**Tümü**: Defteri tüm kiralamalara uygulayın.</span><span class="sxs-lookup"><span data-stu-id="268cc-121">**All** – Apply the book to all leases.</span></span>
    - <span data-ttu-id="268cc-122">**Grup**: Defteri belirli bir kiralama grubuna uygulayın.</span><span class="sxs-lookup"><span data-stu-id="268cc-122">**Group** – Apply the book to a specific group of leases.</span></span>
    - <span data-ttu-id="268cc-123">**Tablo**: Defteri belirli kiralamalara uygulayın.</span><span class="sxs-lookup"><span data-stu-id="268cc-123">**Table** – Apply the book to specific leases.</span></span>

6. <span data-ttu-id="268cc-124">**Hesap kodu** alanında **Grup**'u veya **Tablo**'yu seçtiyseniz, **Hesap/Grup numarası** alanında bir hesap numarası veya grup numarası seçin.</span><span class="sxs-lookup"><span data-stu-id="268cc-124">If you selected **Group** or **Table** in the **Account code** field, select an account number or group number in the **Account/Group number** field.</span></span>
7. <span data-ttu-id="268cc-125">Uygun alanlarda, finansal kiralama ana hesabını ve işletme kiralaması ana hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="268cc-125">In the appropriate fields, select the finance lease main account and the operating lease main account.</span></span>

<span data-ttu-id="268cc-126">Bu adımları tamamladığınızda, seçili bir kiralamanın **Kiralama ayrıntıları** sayfasınde **İcra maliyeti ödeme planı** satırları üzerinden giderleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="268cc-126">When you've completed these steps, you can add expenses through the **Executory costs payment schedule** lines on the **Lease details** page of a selected lease.</span></span> <span data-ttu-id="268cc-127">Alternatif olarak, yeni bir kiralama oluştururken de giderleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="268cc-127">Alternatively, you can add expenses when you create a new lease.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
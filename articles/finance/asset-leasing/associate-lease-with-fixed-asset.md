---
title: Kiralamaları sabit varlıklarla ilişkilendirme
description: Bu konuda, mevcut bir sabit varlığın yeni bir kiralamayla nasıl ilişkilendirileceği açıklanır.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 5c4f14d38b3cfc2c4d09cfeb5854204701250757
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260865"
---
# <a name="associate-fixed-assets-with-leases"></a><span data-ttu-id="d0805-103">Kiralamaları sabit varlıklarla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="d0805-103">Associate fixed assets with leases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0805-104">Bu konuda, mevcut bir sabit varlığın yeni bir kiralamayla nasıl ilişkilendirileceği açıklanır.</span><span class="sxs-lookup"><span data-stu-id="d0805-104">The topic explains how to associate an existing fixed asset with a new lease.</span></span> <span data-ttu-id="d0805-105">Bir sabit varlığı kiralamayla ilişkilendirdiğinizde, ilk kabuldeki kullanım hakkı (ROU) varlığı sabit varlığın alım maliyeti olur.</span><span class="sxs-lookup"><span data-stu-id="d0805-105">When you associate a fixed asset with a lease, the right-of-use (ROU) asset value at initial recognition will be the acquisition cost of the fixed asset.</span></span>

<span data-ttu-id="d0805-106">Sabit bir varlığı kiralamayla ilişkilendirmeden önce Sabit varlıklarda sabit varlık için bir kayıt oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d0805-106">Before you can associate a fixed asset with a lease, you must create a record for the fixed asset in Fixed assets.</span></span> <span data-ttu-id="d0805-107">Ardından, **Kiralama özeti** sayfasında kiralama oluşturmanız ve varlığı bu kiralamaya bağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d0805-107">Then, on the **Lease summary** page, you must create a lease and link the asset to that lease.</span></span>

1. <span data-ttu-id="d0805-108">[Kiralama ekleme veya kopyalama](add-lease.md) konu başlığındaki adımları izleyerek kiralama ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d0805-108">Add a lease by following the steps in [Add or copy leases](add-lease.md).</span></span> <span data-ttu-id="d0805-109">**Kiralama ekle** sayfasındaki **Sabit varlık numarası** alanında henüz alınmamış olan varlığı seçin.</span><span class="sxs-lookup"><span data-stu-id="d0805-109">On the **Add lease** page, in the **Fixed asset number** field, select the asset that hasn't yet been acquired.</span></span>
2. <span data-ttu-id="d0805-110">**Defterler**'i seçin ve ödeme planını onaylayın.</span><span class="sxs-lookup"><span data-stu-id="d0805-110">Select **Books**, and confirm the payment schedule.</span></span>
3. <span data-ttu-id="d0805-111">**İlk kabul**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="d0805-111">Select **Initial recognition**.</span></span>
4. <span data-ttu-id="d0805-112">**Varlık kiralama günlüğü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="d0805-112">Select **Asset leasing journal**.</span></span>

    <span data-ttu-id="d0805-113">Kiralama için ilk kabul günlüğü girişi, genellikle ROU varlığı hesabına borçlandırılan tutar için sabit varlığı borçlandırır.</span><span class="sxs-lookup"><span data-stu-id="d0805-113">The initial recognition journal entry for the lease debits the fixed asset for the amount that is usually debited to the ROU asset account.</span></span>

    <span data-ttu-id="d0805-114">Sabit varlıkla ilgili hareket türü ve defteri artık görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0805-114">You can now view the transaction type and book for the fixed asset.</span></span>

5. <span data-ttu-id="d0805-115">**Günlük ayrıntılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d0805-115">Select **Journal details**.</span></span>
6. <span data-ttu-id="d0805-116">Günlük girişiyle ilgili ayrı satırları görüntülemek için **Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d0805-116">Select **Lines** to view the individual lines for the journal entry.</span></span>
7. <span data-ttu-id="d0805-117">Varlığı içeren günlük girişini seçin ve ardından **Sabit Varlıklar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d0805-117">Select the journal line that contains the asset, and then select the **Fixed Assets** tab.</span></span>

    <span data-ttu-id="d0805-118">**Sabit varlıklar** sekmesi hareket türünü ve defteri gösterir.</span><span class="sxs-lookup"><span data-stu-id="d0805-118">The **Fixed assets** tab shows the transaction type and the book.</span></span> <span data-ttu-id="d0805-119">Varsayılan olarak, **Hareket türü** alanı **Alım** olarak ayarlanır, **Defter** alanı sabit varlık için geçerli defter olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="d0805-119">By default, the **Transaction type** field is set to **Acquisition**, and the **Book** field is set to the current book for the fixed asset.</span></span>

<span data-ttu-id="d0805-120">İlk kabul günlüğü girişi deftere nakledildikten sonra, hareket sabit varlık için alım hareketi olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="d0805-120">After you post the initial recognition journal entry, the transaction appears as an acquisition transaction for the fixed asset.</span></span> <span data-ttu-id="d0805-121">Hareket tablosunu görüntülemek için **Sabit varlıklar \> Sabit varlıklar \> Sabit varlıklar** bölümüne gidin, uygun varlığı seçin ve **Değerlemeler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d0805-121">To view the transaction table, go to **Fixed assets \> Fixed assets \> Fixed assets**, select the appropriate asset, and then select **Valuations**.</span></span> <span data-ttu-id="d0805-122">İlk kabul günlüğü girişinde belirtilen sabit varlık için bir alım hareketi oluşturulduğu görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0805-122">You should see that the initial recognition journal entry has created an acquisition transaction for the specified fixed asset.</span></span>

<span data-ttu-id="d0805-123">Artık Sabit varlıklardaki standart amortisman işlevi kullanılarak sabit varlığa amortisman uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="d0805-123">The fixed asset can now be depreciated by using the standard depreciation functionality in Fixed assets.</span></span> <span data-ttu-id="d0805-124">Amortisman hakkında daha fazla bilgi için bkz. [Amortisman yöntemleri ve kuralları](../fixed-assets/depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="d0805-124">For more information about depreciation, see [Depreciation methods and conventions](../fixed-assets/depreciation-methods-conventions.md).</span></span>

> [!NOTE]
> <span data-ttu-id="d0805-125">Sabit varlığı bir kiralamayla ilişkilendirirseniz Varlık kiralamada **Varlık amortismanı** ve **Kira değer düşüşü** düğmeleri devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="d0805-125">If you associate a fixed asset with a lease, the **Asset depreciation** and **Lease impairment** buttons are disabled in Asset leasing.</span></span> <span data-ttu-id="d0805-126">Sabit varlıklardaki varlık amortismanı ve kira değer düşüşü hareketlerini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0805-126">You can view asset depreciation and lease impairment transactions from Fixed assets.</span></span> <span data-ttu-id="d0805-127">Bir sorgu formu açan **Varlık hareketleri** düğmesi de devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="d0805-127">The **Asset transactions** button, which opens an inquiry form is also disabled.</span></span> <span data-ttu-id="d0805-128">**Varlık hareketleri** sorgu formunu Sabit varlıklarda da açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0805-128">You can also open the **Asset transactions** inquiry form in Fixed assets.</span></span>  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
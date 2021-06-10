---
title: Hiçbir değişiklik yapmamış olsanız bile madde karşılama ayarlarını kaydetmeniz istenir
description: Hiçbir değişiklik yapmamış olsanız bile madde karşılama ayarlarını kaydetmeniz istenir.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049494"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a><span data-ttu-id="814bd-103">Hiçbir değişiklik yapmamış olsanız bile madde karşılama ayarlarını kaydetmeniz istenir</span><span class="sxs-lookup"><span data-stu-id="814bd-103">You're prompted to save item coverage settings even though you made no changes</span></span>

<span data-ttu-id="814bd-104">KB numarası: 4615588</span><span class="sxs-lookup"><span data-stu-id="814bd-104">KB number: 4615588</span></span>

## <a name="symptoms"></a><span data-ttu-id="814bd-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="814bd-105">Symptoms</span></span>

<span data-ttu-id="814bd-106">Bazı senaryolarda, **Madde kapsamı V2** varlığı üzerinden öğeleri aldıktan sonra *Madde kapsamı* sayfasını açtığınızda aşağıdaki iletiyi alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="814bd-106">In some scenarios, you might receive the following message when you open the **Item coverage** page after you import items through the *Item coverage V2* entity:</span></span>

> <span data-ttu-id="814bd-107">Kapatmadan önce değişikliklerinizi kaydetmek istiyor musunuz?</span><span class="sxs-lookup"><span data-stu-id="814bd-107">Do you want to save your changes before closing?</span></span>

<span data-ttu-id="814bd-108">Herhangi bir değişiklik yapmamış olsanız bile bu iletiyi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="814bd-108">You receive this message even though you haven't made any changes.</span></span>

## <a name="resolution"></a><span data-ttu-id="814bd-109">Çözüm</span><span class="sxs-lookup"><span data-stu-id="814bd-109">Resolution</span></span>

<span data-ttu-id="814bd-110">**Madde kapsamı** sayfası, varlık alma gibi veritabanında son zamanlarda doğrudan değişiklikler yapıldıktan sonra iletinin gösterilmesine neden olabilecek karmaşık varsayılan mantık içerir.</span><span class="sxs-lookup"><span data-stu-id="814bd-110">The **Item coverage** page includes complex defaulting logic that might cause the message to be shown after direct changes have recently been made in the database, such as through entity import.</span></span> <span data-ttu-id="814bd-111">Örneğin, `AREGENERALSETTINGSOVERRIDDEN` varlık alanı *Hayır* olarak ayarlanır, ancak `PRODUCTCOVERAGEGROUPID` ve/veya `VENDORACCOUNTNUMBER` gibi alanlar için yeni veya değiştirilmiş değerler sağlayan bir dosya alırsınız.</span><span class="sxs-lookup"><span data-stu-id="814bd-111">For example, the `AREGENERALSETTINGSOVERRIDDEN` entity field is set to *No*, but you import a file that provides new or modified values for fields such as `PRODUCTCOVERAGEGROUPID` and/or `VENDORACCOUNTNUMBER`.</span></span> <span data-ttu-id="814bd-112">Bu durumda, `AREGENERALSETTINGSOVERRIDDEN` alanı *Hayır* olarak ayarlandığından, **madde kapsamı** sayfasını içe aktarma işleminden sonra ilk kez açtığınızda değerler alanlardan otomatik olarak temizlenir.</span><span class="sxs-lookup"><span data-stu-id="814bd-112">In this case, because the `AREGENERALSETTINGSOVERRIDDEN` field is set to *No*, the values are automatically cleared from the fields when you open the **Item coverage** page for the first time after the import.</span></span> <span data-ttu-id="814bd-113">Değişiklikleri ileti kutusu istemiyle kaydederseniz, bunlar veritabanında depolanır.</span><span class="sxs-lookup"><span data-stu-id="814bd-113">If you save the changes as the message box prompts, they are stored in the database.</span></span> <span data-ttu-id="814bd-114">Aksi takdirde, sayfayı bir sonraki açışınızda aynı iletiyi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="814bd-114">Otherwise, you will receive the same message the next time that you open the page.</span></span>

<span data-ttu-id="814bd-115">Bu davranışı önlemek, ancak varlık içer aktarm üzerinden `PRODUCTCOVERAGEGROUPID` gibi alanların değerlerini de eklemek için, `AREGENERALSETTINGSOVERRIDDEN` alanını içe aktardığınızda *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="814bd-115">To prevent this behavior but also include values for fields such as `PRODUCTCOVERAGEGROUPID` through entity import, set `AREGENERALSETTINGSOVERRIDDEN` to *Yes* when you import.</span></span>

---
title: Günlüklerde ertelenen vergi hesaplamasını etkinleştirme
description: Bu konu, günlük satırlarının sayısı çok fazla olduğunda vergi hesaplama performansını artırmaya yardımcı olmak için Ertlenen vergi hesaplaması özelliğinin nasıl etkinleştirileceğini açıklamaktadır.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
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
ms.author: roschlom
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: d842b60b3cca8c29b281ab4a6a1b6c3b0bad3684
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236734"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a><span data-ttu-id="63bb1-103">Günlüklerde ertelenen vergi hesaplamasını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="63bb1-103">Enable delayed tax calculation on journals</span></span>
[!include [banner](../includes/banner.md)]


<span data-ttu-id="63bb1-104">Bu konu, günlüklerde satış vergisi hesaplamasını nasıl erteleyebileceğinizi açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="63bb1-104">This topic explains how you can delay sales tax calculation on journals.</span></span> <span data-ttu-id="63bb1-105">Bu özellik, birçok günlük satırı olduğunda vergi hesaplamalarında performansın artırılmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="63bb1-105">This capability helps improve the performance of tax calculations when there are many journal lines.</span></span>

<span data-ttu-id="63bb1-106">Varsayılan olarak, vergiyle ilgili alanlar her güncelleştirildiğinde, günlük satırlarındaki satış vergisi tutarları hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="63bb1-106">By default, sales tax amounts on journal lines are calculated whenever tax-related fields are updated.</span></span> <span data-ttu-id="63bb1-107">Bu alanlar, satış vergisi grupları ve madde satış vergisi grupları için alanlar içerir.</span><span class="sxs-lookup"><span data-stu-id="63bb1-107">These fields include the fields for sales tax groups and item sales tax groups.</span></span> <span data-ttu-id="63bb1-108">Günlük satırındaki her güncelleştirme vergi tutarlarının tüm günlük satırlarında yeniden hesaplanmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="63bb1-108">Any update to a journal line causes tax amounts to be recalculated for all journal lines.</span></span> <span data-ttu-id="63bb1-109">Bu davranış kullanıcının gerçek zamanlı olarak hesaplanan vergi tutarlarının görebilmesine yardımcı olmakla birlikte, günlük satırlarının sayısı çok büyükse performansı da etkileyebilir.</span><span class="sxs-lookup"><span data-stu-id="63bb1-109">Although this behavior helps user see tax amounts calculated in real time, it can also affect performance if the number of journal lines is very large.</span></span>

<span data-ttu-id="63bb1-110">Ertelenen vergi hesaplaması özelliği günlüklerde vergi hesaplamasını ertelemenizi sağlar ve bu nedenle performans sorunlarını gidermeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="63bb1-110">The Delayed tax calculation feature lets you delay tax calculation on journals and therefore helps fix performance issues.</span></span> <span data-ttu-id="63bb1-111">Bu özellik açık olduğunda, vergi tutarları yalnızca kullanıcı **Satış Vergisi**'ni seçerse veya günlüğü deftere naklederse hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="63bb1-111">When this feature is turned on, tax amounts are calculated only when a user selects **Sales Tax** or posts the journal.</span></span>

<span data-ttu-id="63bb1-112">Satış vergilerinin hesaplamasını üç düzeyde erteleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="63bb1-112">You can delay the calculation of sales taxes at three levels:</span></span>

- <span data-ttu-id="63bb1-113">Tüzel kişilik</span><span class="sxs-lookup"><span data-stu-id="63bb1-113">Legal entity</span></span>
- <span data-ttu-id="63bb1-114">Günlük adı</span><span class="sxs-lookup"><span data-stu-id="63bb1-114">Journal name</span></span>
- <span data-ttu-id="63bb1-115">Günlük başlığı</span><span class="sxs-lookup"><span data-stu-id="63bb1-115">Journal header</span></span>

<span data-ttu-id="63bb1-116">Sistem, günlük başlığı ayarına öncelik verir.</span><span class="sxs-lookup"><span data-stu-id="63bb1-116">The system gives priority to the setting for the journal header.</span></span> <span data-ttu-id="63bb1-117">Varsayılan olarak, bu ayar günlük adından alınır.</span><span class="sxs-lookup"><span data-stu-id="63bb1-117">By default, this setting is taken from the journal name.</span></span> <span data-ttu-id="63bb1-118">Varsayılan olarak, günlük adı oluşturulduğunda, günlük adı içina yar **Genel muhasebe parametreleri** sayfasındaki ayardan alınır.</span><span class="sxs-lookup"><span data-stu-id="63bb1-118">By default, the setting for the journal name is taken from the setting on the **General ledger parameters** page when the journal name is created.</span></span> <span data-ttu-id="63bb1-119">Aşağıdaki bölümlerde tüzel kişiler, günlük adları ve günlük başlıkları için ertelenen vergi hesaplamasının nasıl etkinleştirileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="63bb1-119">The following sections explain how to turn on delayed tax calculation for legal entities, journal names, and journal headers.</span></span>

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a><span data-ttu-id="63bb1-120">Tüzel kişilik düzeyinde ertelenen vergi hesaplamasını açma</span><span class="sxs-lookup"><span data-stu-id="63bb1-120">Turn on delayed tax calculation at the legal entity level</span></span>

1. <span data-ttu-id="63bb1-121">**Genel muhasebe\> Genel muhasebe ayarı \> Genel muhasebe parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="63bb1-121">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="63bb1-122">**Satış vergisi** sekmesinde, **Genel** hızlı sekmesi üzerinde **Ertelenen vergi hesaplaması** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="63bb1-122">On the **Sales tax** tab, on the **General** FastTab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Genel muhasebe parametrelerini görüntüsü](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a><span data-ttu-id="63bb1-124">Günlük adı düzeyinde ertelenen vergi hesaplamasını açma</span><span class="sxs-lookup"><span data-stu-id="63bb1-124">Turn on delayed tax calculation at the journal name level</span></span>

1. <span data-ttu-id="63bb1-125">**Genel muhasebe \> Günlük ayarı \> Günlük adları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="63bb1-125">Go to **General ledger \> Journal setup \> Journal names**.</span></span>
2. <span data-ttu-id="63bb1-126">**Genel** hızlı sekmesinde, **Satış vergisi** bölümünde **Ertelenen vergi hesaplaması** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="63bb1-126">On the **General** FastTab, in the **Sales tax** section, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Günlük adları görüntüsü](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a><span data-ttu-id="63bb1-128">Günlük başlığı düzeyinde ertelenen vergi hesaplamasını açma</span><span class="sxs-lookup"><span data-stu-id="63bb1-128">Turn on delayed tax calculation at the journal header level</span></span>

1. <span data-ttu-id="63bb1-129">**Genel muhasebe \> Günlük girişleri \> Genel günlükler**.</span><span class="sxs-lookup"><span data-stu-id="63bb1-129">Go to **General ledger \> Journal entries \> General journals**.</span></span>
2. <span data-ttu-id="63bb1-130">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="63bb1-130">Select **New**.</span></span>
3. <span data-ttu-id="63bb1-131">Bir günlük adı seçin.</span><span class="sxs-lookup"><span data-stu-id="63bb1-131">Select a journal name.</span></span>
4. <span data-ttu-id="63bb1-132">**Kurulum** sekmesinde, **Ertelenen vergi hesaplaması** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="63bb1-132">On the **Setup** tab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Genel günlük sayfası resmi](media/delayed-tax-calculation-journal-header.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
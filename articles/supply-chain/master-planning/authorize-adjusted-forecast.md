---
title: Bir düzeltilmiş tahmini onayla
description: Tüm tahmin verilerinin hemen yetkilendirilmesi gerekmez. Bu makale bir tahminin yetkilendirildiği dönemi nasıl belirtebileceğinizi açıklar. Ayrıca, özel şirketler ve tahmin modelleri için tahmini nasıl yetkilendirebileceğinizi açıklar.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e511aa8181b5d554f3392bdc5f0c299dc031ee4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203952"
---
# <a name="authorize-an-adjusted-forecast"></a><span data-ttu-id="d5bad-105">Bir düzeltilmiş tahmini onayla</span><span class="sxs-lookup"><span data-stu-id="d5bad-105">Authorize an adjusted forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d5bad-106">Tüm tahmin verilerinin hemen yetkilendirilmesi gerekmez.</span><span class="sxs-lookup"><span data-stu-id="d5bad-106">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="d5bad-107">Bu makale bir tahminin yetkilendirildiği dönemi nasıl belirtebileceğinizi açıklar.</span><span class="sxs-lookup"><span data-stu-id="d5bad-107">This article explains how you can specify the period that a forecast is authorized for.</span></span> <span data-ttu-id="d5bad-108">Ayrıca, özel şirketler ve tahmin modelleri için tahmini nasıl yetkilendirebileceğinizi açıklar.</span><span class="sxs-lookup"><span data-stu-id="d5bad-108">It also explains how you can authorize the forecast for specific companies and forecast models.</span></span>

<span data-ttu-id="d5bad-109">Tüm tahmin verilerinin hemen yetkilendirilmesi gerekmez.</span><span class="sxs-lookup"><span data-stu-id="d5bad-109">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="d5bad-110">Tahminin yetkilendirildiği dönemin başlangıç ve bitiş tarihlerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d5bad-110">You can specify the start and end dates of the period that the forecast is authorized for.</span></span> <span data-ttu-id="d5bad-111">Bu işlev, belli aralıkları dondurmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="d5bad-111">This functionality lets you freeze specific buckets.</span></span> 

<span data-ttu-id="d5bad-112">Belirttiğiniz başlangıç ve bitiş tarihleri, tahminin oluşturulduğu demetin başlangıç ve bitiş tarihlerine karşılık gelmek zorundadır.</span><span class="sxs-lookup"><span data-stu-id="d5bad-112">The start and end dates that you specify must correspond to the start and end dates of the bucket that the forecast is generated in.</span></span> <span data-ttu-id="d5bad-113">Sistem bu kısıtlamayı zorlar ve tarihleri ayarlama gerekliyse otomatik olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d5bad-113">The system enforces this restriction and automatically adjusts the dates, if adjustment is required.</span></span> 

<span data-ttu-id="d5bad-114">**Yetkilendirme** sayfasının **Ayrıntılar** öğesinde, en son oluşturulan tahmin hakkındaki ayrıntıları görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d5bad-114">On the **Details** tab of the **Authorization** page, you can view details about the forecast that was most recently generated.</span></span> 

<span data-ttu-id="d5bad-115">Kullanılacak tahmini yetkilendirecek şirketleri ve tahmin modellerini seçebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d5bad-115">You can select the companies and the forecast models to authorize the forecast for use.</span></span> <span data-ttu-id="d5bad-116">Varsayılan olarak, kılavuz tahmini talebin oluşturulduğu tüm şirketleri içerir.</span><span class="sxs-lookup"><span data-stu-id="d5bad-116">By default, the grid includes all the companies that forecast demand has been created for.</span></span> <span data-ttu-id="d5bad-117">Her şirket için, ana planlama parametrelerinde ayarlanan geçerli tahmin planına karşılık gelen tahmin modeli önceden doldurulur.</span><span class="sxs-lookup"><span data-stu-id="d5bad-117">For each company, the forecast model that corresponds to the current forecast plan that is set up in the master planning parameters is prefilled.</span></span> <span data-ttu-id="d5bad-118">Ancak, bu tahmin modelini o şirkete ait olan herhangi bir tahmin modeli ile değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d5bad-118">However, you can change this forecast model to any forecast model that belongs to that company.</span></span> <span data-ttu-id="d5bad-119">Seçili bir şirket için hiçbir tahmini talep verisi oluşturulmadıysa, içe aktarma sırasında bir uyarı iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="d5bad-119">If no forecast demand data has been generated for a selected company, you receive a warning message at import time.</span></span> 

<span data-ttu-id="d5bad-120">**Temel talep tahmininde yapılan manüel ayarlamaları kaydet** onay kutusunun nasıl çalıştığını anlamanız çok önemlidir.</span><span class="sxs-lookup"><span data-stu-id="d5bad-120">It's very important that you understand how the **Save the manual adjustments made to the baseline demand forecast** check box works.</span></span> <span data-ttu-id="d5bad-121">İstatistik temel tahminde manüel ayarlamalar yaptıysanız, bu onay kutusundaki işaretler kaldırılmış olsa bile ayarlanan değerleri kullanım için yetkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="d5bad-121">If you've made manual adjustments to the statistical baseline forecast, the adjusted values are authorized for use, even if this check box is cleared.</span></span> <span data-ttu-id="d5bad-122">Bununla birlikte, değişiklikler yetkilendirmeden sonra kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="d5bad-122">However, the changes are discarded after the authorization.</span></span> <span data-ttu-id="d5bad-123">Bu nedenle, bir daha bir tahmin oluşturulduğunda, bu tahmin sadece istatistiksel bir tahmin olur ve **Manüel ayarlamaları talep tahminine aktar** öğesi seçilse bile manüel geçersiz kılmalar olmaz.</span><span class="sxs-lookup"><span data-stu-id="d5bad-123">Therefore, the next time that a forecast is generated, that forecast is only a statistical forecast and doesn't have any manual overrides, even if **Transfer manual adjustments to the demand forecast** is selected.</span></span> <span data-ttu-id="d5bad-124">Bu nedenle, tüm manüel değişiklikleri tutmanıza veya kaldırmanıza izin veren bir mekanizma olan **Temel talep tahmininde yapılan manüel ayarlamaları kaydet** onay kutusunu düşünebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d5bad-124">Therefore, you can consider the **Save the manual adjustments made to the baseline demand forecast** check box a mechanism that lets you keep or discard all manual changes.</span></span>

<a name="additional-resources"></a><span data-ttu-id="d5bad-125">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="d5bad-125">Additional resources</span></span>
--------

[<span data-ttu-id="d5bad-126">Temel tahminde manüel ayarlamalar yapma</span><span class="sxs-lookup"><span data-stu-id="d5bad-126">Make manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)

[<span data-ttu-id="d5bad-127">Tahmin doğruluğunu izleme</span><span class="sxs-lookup"><span data-stu-id="d5bad-127">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)




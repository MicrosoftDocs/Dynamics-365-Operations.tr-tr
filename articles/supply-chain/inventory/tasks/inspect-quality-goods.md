---
title: Malların kalitesini denetleme
description: Bu konu, bir kalite emrinin nasıl işleyeceğini açıklar.
author: perlynne
manager: tfehr
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e37ac8c9320d427b9f9a3ca32b0e4667c7023339
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244435"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="9674b-103">Malların kalitesini denetleme</span><span class="sxs-lookup"><span data-stu-id="9674b-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9674b-104">Bu konu, bir kalite emrinin nasıl işleyeceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="9674b-104">This topic explains how to process a quality order.</span></span> <span data-ttu-id="9674b-105">Bu kılavuzu USMF demo şirketinde çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9674b-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="9674b-106">Bu örnek işleme başlamadan önce "000016" satınalma siparişini onaylamanız ve ürün alış irsaliyesini deftere nakletmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9674b-106">Before you start this example procedure, you need to confirm purchase order "000016" and post a product receipt.</span></span> <span data-ttu-id="9674b-107">Bu otomatik olarak bir kalite emri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9674b-107">This will automatically create a quality order.</span></span> <span data-ttu-id="9674b-108">Kalite incelemeleri genellikle bir kalite memuru tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="9674b-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="9674b-109">Bir kalite emri seçin</span><span class="sxs-lookup"><span data-stu-id="9674b-109">Select a quality order</span></span>
1. <span data-ttu-id="9674b-110">Gezinti panelinde **Modüller > Stok yönetimi > Periyodik görevler > Kalite yönetimi > Kalite emirleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="9674b-110">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="9674b-111">Bu yordamı başlatmadan önce oluşturulan kalite emrini seçin.</span><span class="sxs-lookup"><span data-stu-id="9674b-111">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="9674b-112">Test sonuçlarını kaydetme</span><span class="sxs-lookup"><span data-stu-id="9674b-112">Record test results</span></span>
1. <span data-ttu-id="9674b-113">**Sonuçlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9674b-113">Select **Results**.</span></span>
2. <span data-ttu-id="9674b-114">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="9674b-114">Select **Edit**.</span></span>
3. <span data-ttu-id="9674b-115">**Sonuç miktarı** alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9674b-115">In the **Result quantity** field, enter a number.</span></span>
4. <span data-ttu-id="9674b-116">**Tesis** alanında, açılır menüden istediğiniz kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="9674b-116">In the **Outcome** field, select the desired record in the drop-down menu.</span></span>  
- <span data-ttu-id="9674b-117">Bu örnekte sonuç, önceden tanımlanmış bir sonuca bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="9674b-117">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="9674b-118">Normalde, örneğin bir ebat veya başka bir boyut gibi, daha belirli bir test sonucu kaydedersiniz.</span><span class="sxs-lookup"><span data-stu-id="9674b-118">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
5. <span data-ttu-id="9674b-119">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9674b-119">Select **Save**.</span></span>
6. <span data-ttu-id="9674b-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9674b-120">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="9674b-121">Kalite emrini doğrula</span><span class="sxs-lookup"><span data-stu-id="9674b-121">Validate the quality order</span></span>
1. <span data-ttu-id="9674b-122">**Doğrula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="9674b-122">Select **Validate**.</span></span>
2. <span data-ttu-id="9674b-123">**Doğrulayan** alanında, açılan menüden denetimi gerçekleştiren kullanıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="9674b-123">In the **Validated by** field, select the user performing the inspection from the drop-down menu.</span></span>  
3. <span data-ttu-id="9674b-124">**Seç**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9674b-124">Click **Select**.</span></span>
4. <span data-ttu-id="9674b-125">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9674b-125">Select **OK**.</span></span>
5. <span data-ttu-id="9674b-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9674b-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
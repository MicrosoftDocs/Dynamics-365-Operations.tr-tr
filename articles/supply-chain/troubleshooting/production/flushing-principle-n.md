---
title: Ürün reçetesi satırlarındaki otomatik tüketim ilke ayarları dikkate alınmıyor
description: Ürün reçetesi (BOM) satırlarındaki otomatik tüketim ilke ayarları dikkate alınmıyor.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026985"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a><span data-ttu-id="76076-103">Ürün reçetesi satırlarındaki otomatik tüketim ilke ayarları dikkate alınmıyor</span><span class="sxs-lookup"><span data-stu-id="76076-103">Flushing principle settings on BOM lines aren't respected</span></span>

<span data-ttu-id="76076-104">KB numarası: 4612725</span><span class="sxs-lookup"><span data-stu-id="76076-104">KB number: 4612725</span></span>

## <a name="symptoms"></a><span data-ttu-id="76076-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="76076-105">Symptoms</span></span>

<span data-ttu-id="76076-106">Bu sorun, **Üretim kontrol parametreleri** sayfasının **Otomatik güncelleştirme** sekmesindeki **Otomatik ürün reçetesi tüketimi**, *Otomatik tüketim ilkesi* olarak ayarlandığında gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="76076-106">This issue occurs when the **Automatic BOM consumption** field on the **Automatic update** tab of the **Production control parameters** page is set to *Flushing principle*.</span></span> <span data-ttu-id="76076-107">Bu ayar, bir satınalma siparişi alındığında, tüm ürün reçetesi (BOM) satırlarının otomatik olarak tüketilmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="76076-107">This setting indicates that all bill of materials (BOM) lines should automatically be consumed when a purchase order is received.</span></span> <span data-ttu-id="76076-108">Ürün reçetesi satırlarındaki **Otomatik tüketim ilkesi** alanı *Manuel* olarak ayarlanmışsa, ürün reçetesi satırlarının otomatik olarak tüketilemeyebilir.</span><span class="sxs-lookup"><span data-stu-id="76076-108">If the **Flushing principle** field on BOM lines is explicitly set to *Manual*, you might expect that the BOM lines won't automatically be consumed.</span></span> <span data-ttu-id="76076-109">Ancak bu sorun oluştuğunda, **Otomatik tüketim ilkesi** alanının *Manuel* olarak ayarlandığı ürün reçetesi satırları yine de otomatik olarak tüketilir.</span><span class="sxs-lookup"><span data-stu-id="76076-109">However, when this issue occurs, BOM lines where the **Flushing principle** field is set to *Manual* are automatically consumed anyway.</span></span>

## <a name="resolution"></a><span data-ttu-id="76076-110">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="76076-110">Resolution</span></span>

<span data-ttu-id="76076-111">Bu sorunla karşılaşıyorsanız, üretim kontrol parametreleriniz, ürün reçetesi satırlarındaki **Otomatik tüketim ilkesi** ayarını geçersiz kılmak üzere ayarlanmış olabilir.</span><span class="sxs-lookup"><span data-stu-id="76076-111">If you're experiencing this issue, your production control parameters might be set up to override the **Flushing principle** setting on BOM lines.</span></span> <span data-ttu-id="76076-112">**Üretim denetimi parametreleri** sayfasında, **Otomatik güncelleştirme** sekmesinde, **Otomatik ürün reçetesi tüketimi** alanının değerini denetleyin.</span><span class="sxs-lookup"><span data-stu-id="76076-112">On the **Production control parameters** page, on the **Automatic update** tab, check the value of the **Automatic BOM consumption** field.</span></span> <span data-ttu-id="76076-113">*Her zaman* olarak ayarlanmışsa, sistem tüm ürün reçetesi satırlarındaki **Otomatik tüketim ilkesi** ayarını dikkate almaz ve satırları her zaman tüketir.</span><span class="sxs-lookup"><span data-stu-id="76076-113">If it's set to *Always*, the system will disregard the **Flushing principle** setting on all BOM lines and will always flush the lines.</span></span> <span data-ttu-id="76076-114">Sistemin, ürün reçetesi satırlarındaki **Otomatik tüketim ilkesi** ayarını uygulaması için, **Otomatik ürün reçetesi tüketimi** alanının değerini *Otomatik tüketim ilkesi* olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="76076-114">To make the system respect the **Flushing principle** setting on BOM lines, change the value of the **Automatic BOM consumption** field to *Flushing principle*.</span></span>

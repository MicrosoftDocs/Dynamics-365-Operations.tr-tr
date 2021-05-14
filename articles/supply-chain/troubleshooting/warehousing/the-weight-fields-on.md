---
title: Yük satırlarındaki ağırlık alanları, yükteki ağırlık alanlarıyla eşleşmiyor
description: Yük satırlarındaki ağırlık alanları, yükteki ağırlık alanlarıyla eşleşmiyor
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 639b82a9d46b74f179d6904d2c3b8e7dfb813b58
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924363"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a><span data-ttu-id="7a5f2-103">Yük satırlarındaki ağırlık alanları, yükteki ağırlık alanlarıyla eşleşmiyor</span><span class="sxs-lookup"><span data-stu-id="7a5f2-103">The weight fields on load lines don't match the weight fields on the load</span></span>

<span data-ttu-id="7a5f2-104">Hata kodları: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span><span class="sxs-lookup"><span data-stu-id="7a5f2-104">Error codes: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span></span>

## <a name="symptoms"></a><span data-ttu-id="7a5f2-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="7a5f2-105">Symptoms</span></span>

<span data-ttu-id="7a5f2-106">Sistem, aşağıdaki hata iletisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="7a5f2-106">The system shows the following error message:</span></span>

> <span data-ttu-id="7a5f2-107">Yük satırlarındaki ağırlık alanları, %1 yükündeki ağırlık alanlarıyla eşleşmiyor.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-107">The weight fields on load lines do not match the weight fields on load %1.</span></span> <span data-ttu-id="7a5f2-108">Ağırlık alanlarını yeniden hesaplamak için Ambar yükü ağırlığı tutarlılık denetimini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-108">Run the Warehouse load weight consistency check to recalculate the weight fields.</span></span>

## <a name="cause"></a><span data-ttu-id="7a5f2-109">Nedeni</span><span class="sxs-lookup"><span data-stu-id="7a5f2-109">Cause</span></span>

<span data-ttu-id="7a5f2-110">**Net ağırlık** ve **Dara ağırlık** alanları, yük satırında *0* (sıfır) olarak ayarlı.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-110">The **Net weight** and **Tara weight** fields are set to *0* (zero) on the load line.</span></span> <span data-ttu-id="7a5f2-111">Ancak, ürün üzerindeki ağırlık ölçüleri için ağırlık alanları *0* olarak ayarlı değil.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-111">However, the weight fields aren't set to *0* for the weight measurements on the product.</span></span> <span data-ttu-id="7a5f2-112">Yük satırında ağırlık alanları ayarlanmamışsa, yük satırındaki miktarla ilgili tüm düzeltmeler yüklemede yanlış ağırlık hesaplamasına neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-112">When weight fields aren't set on the load line, any corrections of the quantity on the load line might cause incorrect weight calculation on the load.</span></span> <span data-ttu-id="7a5f2-113">Bu sorun, yük satırı oluşturulduktan sonra üründeki ağırlıklar değiştirilirse oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-113">This issue might occur if the weights on the product have been changed since the load line was created.</span></span>

## <a name="resolution"></a><span data-ttu-id="7a5f2-114">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="7a5f2-114">Resolution</span></span>

<span data-ttu-id="7a5f2-115">Varsayılan olarak, bir yük satırı oluşturulduğunda, ürünün ağırlık alanları üzerine girilir.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-115">By default, when a load line is created, the weight fields from the product are entered on it.</span></span> <span data-ttu-id="7a5f2-116">Ağırlık sıfırsa, *Ambar yükü ağırlığı tutarlılık denetimi* işlevini kullanarak bunu yeniden hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-116">If the weight is zero, you can recalculate it by using the *Warehouse load weight consistency check* functionality.</span></span>

1. <span data-ttu-id="7a5f2-117">**Sistem yönetimi \> Periyodik görevler \> Veritabanı \> Tutarlılık denetimi** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-117">Go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="7a5f2-118">**Tutarlılık denetimi** iletişim kutusunda, **Modül** alanını *Ambar yönetimi* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-118">In the **Consistency check** dialog box, set the **Module** field to *Warehouse management*.</span></span>
1. <span data-ttu-id="7a5f2-119">**Denetle/Onar** alanını *Hatayı düzelt* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-119">Set the **Check/Fix** field to *Fix error*.</span></span>
1. <span data-ttu-id="7a5f2-120">Onay kutusu listesinde **Ambar yük ağırlığı tutarlılık denetimi** onay kutusunu seçin ve yalnızca bu onay kutusunun satırının vurgulandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-120">In the checkbox list, select the **Warehouse load weight consistency check** checkbox, and make sure that only the row for this checkbox is highlighted.</span></span>
1. <span data-ttu-id="7a5f2-121">Onay kutusu listesinin en üstünde üç nokta düğmesini (**...**) seçin ve menüden **İletişim kutusu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-121">At the top of the checkbox list, select the ellipsis button (**...**), and then select **Dialog** on the menu.</span></span>
1. <span data-ttu-id="7a5f2-122">**Ambar yük ağırlığı tutarlılık denetimi** iletişim kutusunda, tutarlılık denetiminin çalışacağı ölçütü belirtmek için aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="7a5f2-122">In the **Warehouse load weight consistency check** dialog box, set the following fields to specify the criteria that the consistency check should run for:</span></span>

    - <span data-ttu-id="7a5f2-123">**Yük kodu:** Bir yük kodu belirtin.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-123">**Load ID:** Specify a load ID.</span></span> <span data-ttu-id="7a5f2-124">Tüm yük kodlarını denetlemek için bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-124">Leave this blank to check all load IDs.</span></span>
    - <span data-ttu-id="7a5f2-125">**Madde numarası:** Bir madde numarası belirtin.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-125">**Item number:** Specify an item number.</span></span> <span data-ttu-id="7a5f2-126">Tüm maddeleri denetlemek için bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-126">Leave this blank to check all items.</span></span>
    - <span data-ttu-id="7a5f2-127">**Yükte her zaman ağırlığı yeniden hesapla:** Bu seçeneği *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-127">**Always recalculate weight on loads:** Set this option to *Yes*.</span></span>
    - <span data-ttu-id="7a5f2-128">**Yük satırlarında ağırlık üzerine yazmaya izin ver:** Bu seçeneği *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-128">**Allow overwrite of weight on load lines:** Set this option to *Yes*.</span></span>

1. <span data-ttu-id="7a5f2-129">**Ambar yükü ağırlığı tutarlılık denetimi** iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-129">Select **OK** to close the **Warehouse load weight consistency check** dialog box.</span></span>
1. <span data-ttu-id="7a5f2-130">Üç nokta düğmesini seçin ve menüden **Yürüt**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-130">Select the ellipsis button, and then select **Execute** on the menu.</span></span>

<span data-ttu-id="7a5f2-131">Ağırlık, belirttiğiniz ölçütlere göre yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-131">The weight is recalculated based on the criteria that you specified.</span></span> <span data-ttu-id="7a5f2-132">Tutarlılık denetiminin sonucunu görmek için **İleti ayrıntıları** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="7a5f2-132">Select the **Message details** link to view the result of the consistency check.</span></span>

---
title: Sevkiyat konsolidasyon ilkesi, Ambara serbest bırakma sayfasından geçersiz kılındığında sevkiyatları konsolide etme
description: Bu konu, bir veya daha fazla satış satırının Ambara serbest bırakma sayfasından manuel olarak ambara serbest bırakılmasının ve serbest bırakmadan önce sistem tarafından tanımlanan sevkiyat konsolidasyon ilkesinin geçersiz kılınmasının gerektiği bir senaryo sunar.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: be573f3a137fbd74ba2f5d8bb346e4bb9f9116c1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237119"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden-from-the-release-to-warehouse-page"></a><span data-ttu-id="67de8-103">Sevkiyat konsolidasyon ilkesi, Ambara serbest bırakma sayfasından geçersiz kılındığında sevkiyatları konsolide etme</span><span class="sxs-lookup"><span data-stu-id="67de8-103">Consolidate shipments when the shipment consolidation policy is overridden from the Release to warehouse page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67de8-104">Bu konu, bir veya daha fazla satış satırının **Ambara serbest bırakma** sayfasından manuel olarak ambara serbest bırakılmasının ve serbest bırakmadan önce sistem tarafından tanımlanan sevkiyat konsolidasyon ilkesinin geçersiz kılınmasının gerektiği bir senaryo sunar.</span><span class="sxs-lookup"><span data-stu-id="67de8-104">This topic presents a scenario where one or more sales lines must be manually released to the warehouse from the **Release to warehouse** page, and the system-defined shipment consolidation policy must be overridden before the release.</span></span> <span data-ttu-id="67de8-105">Örneğin, genellikle açık sevkiyatlarla konsolide edilmemiş bir siparişin açık sevkiyatlarla konsolide edilmesi gerekirse sevkiyat konsolidasyon ilkesinin geçersiz kılınması gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="67de8-105">An override of the shipment consolidation policy might be required if, for example, an order that isn't usually consolidated with open shipments must be consolidated with open shipments.</span></span>

<span data-ttu-id="67de8-106">Senaryo sırasında, bir satış siparişleri kümesi oluşturacak ve siparişleri ambara serbest bırakmadan önce varsayılan sevkiyat konsolidasyon ilkesini geçersiz kılacaksınız.</span><span class="sxs-lookup"><span data-stu-id="67de8-106">During the scenario, you will create a set of sales orders and then override the default shipment consolidation policy before you release the orders to the warehouse.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="67de8-107">Tanıtım verilerini kullanılabilir hale getirme</span><span class="sxs-lookup"><span data-stu-id="67de8-107">Make demo data available</span></span>

<span data-ttu-id="67de8-108">Bu konudaki senaryo, Microsoft Dynamics 365 Supply Chain Management için sağlanan standart tanıtım verilerinde bulunan değerlere ve kayıtlara başvurur.</span><span class="sxs-lookup"><span data-stu-id="67de8-108">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="67de8-109">Alıştırmaları yaparken burada sağlanan değerleri kullanmak isterseniz tanıtım verisinin yüklü olduğu bir ortamda çalıştığınızdan ve başlamadan önce tüzel kişiliği **USMF** olarak ayarladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="67de8-109">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="67de8-110">Sevkiyat konsolidasyon ilkelerini ve ürün filtrelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="67de8-110">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="67de8-111">Burada açıklanan senaryo, özelliği önceden açtığınız, [Sevkiyat konsolidasyonu ilkelerini yapılandırma](configure-shipment-consolidation-policies.md) alıştırmalarını yaptığınız ve burada açıklanan ilkeleri ve diğer kayıtları oluşturduğunuz varsayımına dayanır.</span><span class="sxs-lookup"><span data-stu-id="67de8-111">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="67de8-112">Bu senaryoya devam etmeden önce söz konusu alıştırmaları yaptığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="67de8-112">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="67de8-113">Bu senaryo için satış siparişleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="67de8-113">Create the sales orders for this scenario</span></span>

1. <span data-ttu-id="67de8-114">**Alacak hesapları \> Siparişler \> Tüm satış siparişleri** öğesine gidin ve aşağıdaki ayarlara sahip birbirinin aynı üç satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="67de8-114">Go to **Accounts receivable \> Orders \> All sales orders**, and create three identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="67de8-115">**Müşteri hesabı:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="67de8-115">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="67de8-116">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="67de8-116">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="67de8-117">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="67de8-117">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="67de8-118">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="67de8-118">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="67de8-119">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="67de8-119">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a><span data-ttu-id="67de8-120">Satış siparişlerini Ambara serbest bırakma sayfasından serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="67de8-120">Release the sales orders from the Release to warehouse page</span></span>

<span data-ttu-id="67de8-121">Ambara serbest bırakma sırasında sevkiyat konsolidasyon ilkesini geçersiz kılmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="67de8-121">Follow these steps to override the shipment consolidation policy during the release to the warehouse.</span></span>

1. <span data-ttu-id="67de8-122">**Ambar yönetimi \> Ambara serbest bırak \> Ambara serbest bırak** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="67de8-122">Go to **Warehouse management \> Release to warehouse \> Release to warehouse**.</span></span>
1. <span data-ttu-id="67de8-123">Üst bölmede, bu senaryo için oluşturduğunuz ilk satış siparişini seçin.</span><span class="sxs-lookup"><span data-stu-id="67de8-123">In the upper pane, select the first sales order that you created for this scenario.</span></span>
1. <span data-ttu-id="67de8-124">Satırı, ambara serbest bırakmaya eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="67de8-124">Select **Add** to add the line to the release to the warehouse.</span></span> <span data-ttu-id="67de8-125">*Varsayılan* sevkiyat konsolidasyon ilkesinin alt bölmede uygulandığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="67de8-125">Notice that the *Default* shipment consolidation policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="67de8-126">Alt bölmede, **Yeni sevkiyat konsolidasyon ilkesini seç** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="67de8-126">In the bottom pane, select **Select new shipment consolidation policy**.</span></span>
1. <span data-ttu-id="67de8-127">Aynı ilkenin diğer açık sevkiyatlarıyla konsolidasyona olanak veren bir ilke seçin.</span><span class="sxs-lookup"><span data-stu-id="67de8-127">Select a policy that allows for consolidation with other open shipments of the same policy.</span></span> <span data-ttu-id="67de8-128">Örneğin, *CustomerOrderNo* ilkesini seçin.</span><span class="sxs-lookup"><span data-stu-id="67de8-128">For example, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="67de8-129">**Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="67de8-129">Select **Release to warehouse**.</span></span>
1. <span data-ttu-id="67de8-130">Bu senaryo için oluşturduğunuz ikinci ve üçüncü satış siparişlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="67de8-130">Select the second and third sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="67de8-131">Satırları, ambara serbest bırakmaya eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="67de8-131">Select **Add** to add the lines to the release to the warehouse.</span></span> <span data-ttu-id="67de8-132">*Varsayılan* ilkesinin alt bölmede uygulandığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="67de8-132">Notice that the *Default* policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="67de8-133">İkinci satırı seçin ve sonra, **Yeni sevkiyat konsolidasyon ilkesi seç** alanında, *CustomerOrderNo* ilkesini seçin.</span><span class="sxs-lookup"><span data-stu-id="67de8-133">Select the second line, and then, in the **Select new shipment consolidation policy** field, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="67de8-134">Her iki satır için **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="67de8-134">Select **Release to warehouse** for both lines.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="67de8-135">Sevkiyatları doğrulama</span><span class="sxs-lookup"><span data-stu-id="67de8-135">Verify the shipments</span></span>

<span data-ttu-id="67de8-136">İki sevkiyat oluşturulmuş olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="67de8-136">Two shipments should have been created:</span></span>

- <span data-ttu-id="67de8-137">İlk sevkiyat iki satır içerir ve *CustomerOrderNo* sevkiyat konsolidasyon ilkesi kullanılarak oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="67de8-137">The first shipment contains two lines and was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>
- <span data-ttu-id="67de8-138">İkinci sevkiyat bir satır içerir ve *Varsayılan* sevkiyat konsolidasyon ilkesi kullanılarak oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="67de8-138">The second shipment contains one line and was created by using the *Default* shipment consolidation policy.</span></span>

<span data-ttu-id="67de8-139">Oluşturulan sevkiyatları gözden geçirmek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="67de8-139">Follow these steps to review the shipments that were created.</span></span>

1. <span data-ttu-id="67de8-140">**Ambar yönetimi \> Sevkiyatlar \> Tüm sevkiyatlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="67de8-140">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="67de8-141">Gerekli sevkiyatı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="67de8-141">Find and select the required shipment.</span></span>
1. <span data-ttu-id="67de8-142">**Sevkiyat konsolidasyon ilkesi** alanında, sevkiyat oluşturulduğunda kullanılan konsolidasyon ilkesini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="67de8-142">In the **Shipment consolidation policy** field, review the consolidation policy that was used when the shipment was created.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="67de8-143">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="67de8-143">Additional resources</span></span>

- [<span data-ttu-id="67de8-144">Sevkiyat konsolidasyonu ilkeleri</span><span class="sxs-lookup"><span data-stu-id="67de8-144">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="67de8-145">Sevkiyat konsolidasyon ilkelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="67de8-145">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
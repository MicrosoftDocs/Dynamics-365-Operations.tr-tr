---
title: Perakende mağazası, ürünlerin teslim alınacağı mağazalar listesinde görünmüyor
description: Bu konu, ürünlerin teslim alınabileceği mağazalar listesinde bir perakende mağazası yer almadığında size yardımcı olabilecek sorun giderme kılavuzu sağlar.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ad7ddf8a17640471a2344c45eef76f682d29ef2b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020839"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a><span data-ttu-id="a60ec-103">Perakende mağazası, ürünlerin teslim alınacağı mağazalar listesinde görünmüyor</span><span class="sxs-lookup"><span data-stu-id="a60ec-103">Retail store doesn't appear in the list of stores to pick up from</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a60ec-104">Bu konu, ürünlerin teslim alınabileceği mağazalar listesinde bir perakende mağazası yer almadığında size yardımcı olabilecek sorun giderme kılavuzu sağlar.</span><span class="sxs-lookup"><span data-stu-id="a60ec-104">This topic provides troubleshooting guidance that can help when a retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="description"></a><span data-ttu-id="a60ec-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a60ec-105">Description</span></span>

<span data-ttu-id="a60ec-106">Bir perakende mağazası, ürünlerin teslim alınabileceği mağazalar listesinde görünmüyor.</span><span class="sxs-lookup"><span data-stu-id="a60ec-106">A retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="resolution"></a><span data-ttu-id="a60ec-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="a60ec-107">Resolution</span></span>

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a><span data-ttu-id="a60ec-108">Commerce Headquarters'da mağaza adresi için boylam ve enlemi yapılandırın</span><span class="sxs-lookup"><span data-stu-id="a60ec-108">Configure the longitude and latitude for the store address in Commerce headquarters</span></span>

<span data-ttu-id="a60ec-109">Commerce Headquarters'da mağaza adresi için boylam ve enlemi yapılandırmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a60ec-109">To configure the longitude and latitude for the store address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a60ec-110">**Retail ve Commerce \> Kanallar \> Mağazalar \> Tüm mağazalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="a60ec-110">Go to **Retail and Commerce \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="a60ec-111">E-ticaret sitesinde ürün teslim alma seçenekleri arasında görünmesini istediğiniz mağazayı bulun.</span><span class="sxs-lookup"><span data-stu-id="a60ec-111">Find the store that you want to appear among the pickup options on the e-commerce site.</span></span> <span data-ttu-id="a60ec-112">**İşletme birimi numarası** değerini not alın.</span><span class="sxs-lookup"><span data-stu-id="a60ec-112">Make a note of its **Operating unit number** value.</span></span>
1. <span data-ttu-id="a60ec-113">**Kuruluş yönetimi \> Kuruluşlar \> İşletme birimleri** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="a60ec-113">Go to **Organization administration \> Organizations \> Operating units**.</span></span>
1. <span data-ttu-id="a60ec-114">Daha önce not ettiğiniz işletme birimi numarasını arayın ve arama sonuçlarında işletme birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="a60ec-114">Search for the operating unit number that you noted earlier, and then select the operating unit in the search results.</span></span>
1. <span data-ttu-id="a60ec-115">**Adresler** hızlı sekmesinde, **diğer seçenekler**'i seçin ve sonra **Gelişmiş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a60ec-115">On the **Addresses** FastTab, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="a60ec-116">**Genel** hızlı sekmesinde, **boylam** ve **enlem** alanlarının doğru ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="a60ec-116">On the **General** FastTab, make sure that the **Longitude** and **Latitude** fields are correctly set.</span></span> <span data-ttu-id="a60ec-117">Bu adımın bir parçası olarak, değerlerin pozitif veya negatif sayılar olarak doğru belirtildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="a60ec-117">As part of this step, make sure that the values are correctly specified as positive or negative numbers.</span></span>

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a><span data-ttu-id="a60ec-118">Commerce Headquarters'da karşılama gruplarını yapılandırın</span><span class="sxs-lookup"><span data-stu-id="a60ec-118">Configure fulfillment groups in Commerce headquarters</span></span>

<span data-ttu-id="a60ec-119">Commerce Headquarters'da karşılama gruplarını yapılandırmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a60ec-119">To configure fulfillment groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a60ec-120">**Retail ve Commerce \> Kanallar \> Çevrimiçi mağazalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="a60ec-120">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="a60ec-121">Yapılandırılacak çevrimiçi mağazayı seçin.</span><span class="sxs-lookup"><span data-stu-id="a60ec-121">Select the online store to configure.</span></span>
1. <span data-ttu-id="a60ec-122">Eylem bölmesinde, **Kurulum** sekmesini ve ardından **Karşılama grubu ataması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a60ec-122">On the Action Pane, select **Set up**, and then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="a60ec-123">**Karşılama grubu ataması** sayfasında, çevrimiçi mağaza için karşılama grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="a60ec-123">On the **Fulfillment group assignment** page, select the fulfillment group for the online store.</span></span>
1. <span data-ttu-id="a60ec-124">**Kurulum altında** perakende mağazanın karşılama grubu için doğru yapılandırıldığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="a60ec-124">Under **Setup**, make sure that the retail store is correctly configured for the fulfillment group.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a60ec-125">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a60ec-125">Additional resources</span></span> 

[<span data-ttu-id="a60ec-126">Faaliyet birimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a60ec-126">Create an operating unit</span></span>](../../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md)

[<span data-ttu-id="a60ec-127">Çevrimiçi kanalı ayarlama</span><span class="sxs-lookup"><span data-stu-id="a60ec-127">Set up an online channel</span></span>](../channel-setup-online.md)
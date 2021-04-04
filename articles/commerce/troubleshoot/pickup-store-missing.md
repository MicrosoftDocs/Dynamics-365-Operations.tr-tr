---
title: Perakende mağazası, ürünlerin teslim alınacağı mağazalar listesinde görünmüyor
description: Bu konu, ürünlerin teslim alınabileceği mağazalar listesinde bir perakende mağazası yer almadığında size yardımcı olabilecek sorun giderme kılavuzu sağlar.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 652f5f1a779a412c21c18814071ba0fb7dd2e155
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585580"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a><span data-ttu-id="0aee7-103">Perakende mağazası, ürünlerin teslim alınacağı mağazalar listesinde görünmüyor</span><span class="sxs-lookup"><span data-stu-id="0aee7-103">Retail store doesn't appear in the list of stores to pick up from</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0aee7-104">Bu konu, ürünlerin teslim alınabileceği mağazalar listesinde bir perakende mağazası yer almadığında size yardımcı olabilecek sorun giderme kılavuzu sağlar.</span><span class="sxs-lookup"><span data-stu-id="0aee7-104">This topic provides troubleshooting guidance that can help when a retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="description"></a><span data-ttu-id="0aee7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0aee7-105">Description</span></span>

<span data-ttu-id="0aee7-106">Bir perakende mağazası, ürünlerin teslim alınabileceği mağazalar listesinde görünmüyor.</span><span class="sxs-lookup"><span data-stu-id="0aee7-106">A retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="resolution"></a><span data-ttu-id="0aee7-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="0aee7-107">Resolution</span></span>

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a><span data-ttu-id="0aee7-108">Commerce Headquarters'da mağaza adresi için boylam ve enlemi yapılandırın</span><span class="sxs-lookup"><span data-stu-id="0aee7-108">Configure the longitude and latitude for the store address in Commerce headquarters</span></span>

<span data-ttu-id="0aee7-109">Commerce Headquarters'da mağaza adresi için boylam ve enlemi yapılandırmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0aee7-109">To configure the longitude and latitude for the store address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="0aee7-110">**Retail ve Commerce \> Kanallar \> Mağazalar \> Tüm mağazalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="0aee7-110">Go to **Retail and Commerce \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="0aee7-111">E-ticaret sitesinde ürün teslim alma seçenekleri arasında görünmesini istediğiniz mağazayı bulun.</span><span class="sxs-lookup"><span data-stu-id="0aee7-111">Find the store that you want to appear among the pickup options on the e-commerce site.</span></span> <span data-ttu-id="0aee7-112">**İşletme birimi numarası** değerini not alın.</span><span class="sxs-lookup"><span data-stu-id="0aee7-112">Make a note of its **Operating unit number** value.</span></span>
1. <span data-ttu-id="0aee7-113">**Kuruluş yönetimi \> Kuruluşlar \> İşletme birimleri** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="0aee7-113">Go to **Organization administration \> Organizations \> Operating units**.</span></span>
1. <span data-ttu-id="0aee7-114">Daha önce not ettiğiniz işletme birimi numarasını arayın ve arama sonuçlarında işletme birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="0aee7-114">Search for the operating unit number that you noted earlier, and then select the operating unit in the search results.</span></span>
1. <span data-ttu-id="0aee7-115">**Adresler** hızlı sekmesinde, **diğer seçenekler**'i seçin ve sonra **Gelişmiş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0aee7-115">On the **Addresses** FastTab, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="0aee7-116">**Genel** hızlı sekmesinde, **boylam** ve **enlem** alanlarının doğru ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="0aee7-116">On the **General** FastTab, make sure that the **Longitude** and **Latitude** fields are correctly set.</span></span> <span data-ttu-id="0aee7-117">Bu adımın bir parçası olarak, değerlerin pozitif veya negatif sayılar olarak doğru belirtildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="0aee7-117">As part of this step, make sure that the values are correctly specified as positive or negative numbers.</span></span>

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a><span data-ttu-id="0aee7-118">Commerce Headquarters'da karşılama gruplarını yapılandırın</span><span class="sxs-lookup"><span data-stu-id="0aee7-118">Configure fulfillment groups in Commerce headquarters</span></span>

<span data-ttu-id="0aee7-119">Commerce Headquarters'da karşılama gruplarını yapılandırmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0aee7-119">To configure fulfillment groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="0aee7-120">**Retail ve Commerce \> Kanallar \> Çevrimiçi mağazalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="0aee7-120">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="0aee7-121">Yapılandırılacak çevrimiçi mağazayı seçin.</span><span class="sxs-lookup"><span data-stu-id="0aee7-121">Select the online store to configure.</span></span>
1. <span data-ttu-id="0aee7-122">Eylem bölmesinde, **Kurulum** sekmesini ve ardından **Karşılama grubu ataması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="0aee7-122">On the Action Pane, select **Set up**, and then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="0aee7-123">**Karşılama grubu ataması** sayfasında, çevrimiçi mağaza için karşılama grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="0aee7-123">On the **Fulfillment group assignment** page, select the fulfillment group for the online store.</span></span>
1. <span data-ttu-id="0aee7-124">**Kurulum altında** perakende mağazanın karşılama grubu için doğru yapılandırıldığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="0aee7-124">Under **Setup**, make sure that the retail store is correctly configured for the fulfillment group.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0aee7-125">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0aee7-125">Additional resources</span></span> 

[<span data-ttu-id="0aee7-126">Faaliyet birimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0aee7-126">Create an operating unit</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit)

[<span data-ttu-id="0aee7-127">Çevrimiçi kanalı ayarlama</span><span class="sxs-lookup"><span data-stu-id="0aee7-127">Set up an online channel</span></span>](../channel-setup-online.md)

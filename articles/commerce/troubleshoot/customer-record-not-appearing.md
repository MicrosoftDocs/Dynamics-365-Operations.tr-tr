---
title: Müşteri kayıtları Commerce headquarters'da görünmüyor
description: Bu konu, müşteri kayıtlarının Commerce Headquarters'da hemen görünmemesine yardımcı olabilecek sorun giderme kılavuzu sağlar.
author: Reza-Assadi
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
ms.openlocfilehash: 5499e3c059c9e735df87ef8b462d446e0710d90c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801807"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a><span data-ttu-id="db795-103">Müşteri kayıtları Commerce headquarters'da görünmüyor</span><span class="sxs-lookup"><span data-stu-id="db795-103">Customer records don't appear in Commerce headquarters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="db795-104">Bu konu, müşteri kayıtlarının Commerce Headquarters'da hemen görünmemesine yardımcı olabilecek sorun giderme kılavuzu sağlar.</span><span class="sxs-lookup"><span data-stu-id="db795-104">This topic provides troubleshooting guidance that can help when customer records don't immediately appear in Commerce headquarters.</span></span>

## <a name="description"></a><span data-ttu-id="db795-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="db795-105">Description</span></span>

<span data-ttu-id="db795-106">E-ticaret mağazasında kaydolma akışını kullanarak yeni bir müşteri kaydı oluşturduğunuzda, ilgili müşteri kaydı hemen Commerce Headquarters'da görünmüyor.</span><span class="sxs-lookup"><span data-stu-id="db795-106">When you create a new customer record by using the sign-up flow in the e-commerce storefront, the corresponding customer record doesn't immediately appear in Commerce headquarters.</span></span>

## <a name="resolution"></a><span data-ttu-id="db795-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="db795-107">Resolution</span></span>

### <a name="disable-customer-creation-in-async-mode"></a><span data-ttu-id="db795-108">Zaman uyumsuz modda müşteri oluşturmayı devre dışı bırakın</span><span class="sxs-lookup"><span data-stu-id="db795-108">Disable customer creation in async mode</span></span>

> [!IMPORTANT]
> <span data-ttu-id="db795-109">Zaman uyumsuz müşteri oluşturmayı devre dışı bırakırsanız, her kaydın oluşturulması Commerce Headquarters'a gönderilen gerçek zamanlı bir talep üreteceği için sistem performansı etkilenebilir.</span><span class="sxs-lookup"><span data-stu-id="db795-109">If you disable asynchronous customer creation, system performance could be affected, because creation of each record will produce a real-time request to Commerce headquarters.</span></span> <span data-ttu-id="db795-110">Ayrıca, Commerce Headquarters kapalı ise (örneğin, bakım akışları sırasında), tüm yeni müşteri oluşturma akışlarında hata ortaya çıkaracaktır.</span><span class="sxs-lookup"><span data-stu-id="db795-110">In addition, if Commerce headquarters is down (for example, during servicing flows), any new customer creation flows will produce errors.</span></span>

<span data-ttu-id="db795-111">Commerce Headquarters'da zaman uyumsuz modda müşteri oluşturmayı devre dışı bırakmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="db795-111">To disable customer creation in async mode in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="db795-112">**Retail ve Commerce \> Kanal kurulumu \> Çevrimiçi mağaza kurulumu \> İşlevsellik profilleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="db795-112">Go to **Retail and Commerce \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="db795-113">Çevrimiçi kanallarınız için henüz bir işlevsellik profili kullanmıyorsanız, bir tane oluşturun.</span><span class="sxs-lookup"><span data-stu-id="db795-113">If you aren't already using a functionality profile for your online channel, create one.</span></span>
1. <span data-ttu-id="db795-114">**Zaman uyumsuz modda müşteri oluştur** seçeneğinin **Hayır** olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="db795-114">Make sure that the **Create customer in async mode** option is set to **No**.</span></span>
1. <span data-ttu-id="db795-115">**Retail ve Commerce \> Kanallar \> Çevrimiçi mağazalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="db795-115">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="db795-116">Zaman uyumsuz müşteri oluşturmayı devre dışı bırakmak istediğiniz çevrimiçi mağazayı seçin.</span><span class="sxs-lookup"><span data-stu-id="db795-116">Select the online store to disable asynchronous customer creation for.</span></span>
1. <span data-ttu-id="db795-117">**Genel** sekmesinde, **işlevsellik profili** alanının çevrimiçi kanalınız için kullanmakta olduğunuz işlevsellik profiline ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="db795-117">On the **General** tab, make sure that the **Functionality profile** field is set to the functionality profile that you're using for your online channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db795-118">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="db795-118">Additional resources</span></span>

[<span data-ttu-id="db795-119">Commerce'te B2C kiracısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="db795-119">Setup a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)

---
title: Kalite yönetimi madde örnekleme
description: Bu konu, madde örneklemenin nasıl ayarlanacağını açıklar.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae8bfd329ca0d7c30adcd93a759ee6bea7b76278
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022240"
---
# <a name="quality-management-item-sampling"></a><span data-ttu-id="3c297-103">Kalite yönetimi madde örnekleme</span><span class="sxs-lookup"><span data-stu-id="3c297-103">Quality management item sampling</span></span>

<span data-ttu-id="3c297-104">Madde örnekleme, kalite ilişkilendirmenin bir parçası olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3c297-104">Item sampling is used as part of a quality association.</span></span> <span data-ttu-id="3c297-105">Denetlenecek geçerli fiziksel stok tutarını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="3c297-105">It defines the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="3c297-106">Örnekleme miktar, yüzde veya tam plaka tabanlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="3c297-106">Sampling can be based on fixed quantities, a percentage, or a full license plate.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="3c297-107">Madde örneklemesi ayarlayın</span><span class="sxs-lookup"><span data-stu-id="3c297-107">Set up item sampling</span></span>

<span data-ttu-id="3c297-108">Madde örneklemeyi kurmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="3c297-108">Follow these steps to set up item sampling.</span></span>

1. <span data-ttu-id="3c297-109">**Stok yönetimi \> Kurulum \> Kalite kontrol \> Madde örnekleme**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="3c297-109">Go to **Inventory management \> Setup \> Quality control \> Item sampling**.</span></span>
1. <span data-ttu-id="3c297-110">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3c297-110">Select **New**.</span></span>
1. <span data-ttu-id="3c297-111">**Madde örnekleme** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3c297-111">In the **Item sampling** field, enter a value.</span></span>
1. <span data-ttu-id="3c297-112">**Açıklama** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3c297-112">In the **Description** field, enter a value.</span></span>
1. <span data-ttu-id="3c297-113">**Değer** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3c297-113">In the **Value** field, enter a number.</span></span> <span data-ttu-id="3c297-114">Bu değer, bitişik alanda seçilen miktar belirtimi değeriyle ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="3c297-114">This value is related to the quantity specification value that is selected in the adjacent field.</span></span>
1. <span data-ttu-id="3c297-115">Bir test başarısız olduğunda, tüm lot veya sipariş satırı miktarının engellenmesi için, **İşlem** bölümünde **Tam durdurma** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="3c297-115">In the **Process** section, select the **Full blocking** check box if the whole lot or order line quantity should be blocked if a test is failed.</span></span> <span data-ttu-id="3c297-116">Bu onay kutusu temizlenirse, test başarısız olduğunda yalnızca kalite emrindeki maddeler engellenir.</span><span class="sxs-lookup"><span data-stu-id="3c297-116">If this check box is cleared, only the items in the quality order will be blocked if a test is failed.</span></span>
1. <span data-ttu-id="3c297-117">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3c297-117">Select **Save**.</span></span>
1. <span data-ttu-id="3c297-118">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3c297-118">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="3c297-119">*Ambar işlemleri için kalite yönetimi* özelliği bazı ek madde örnekleme yetenekleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="3c297-119">The *Quality management for warehouse processes* feature provides additional item sampling capabilities.</span></span> <span data-ttu-id="3c297-120">*Madde örnekleme kapsamı* kavramı ve miktar belirtimi olarak tam plaka tanımlamaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="3c297-120">It adds the concept of *item sampling scope* and lets you define a full license plate as the quantity specification.</span></span> <span data-ttu-id="3c297-121">Bu özelliği etkinleştirdiyseniz bkz. [Ambar işlemleri için kalite yönetimi](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="3c297-121">If you've turned on this feature, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

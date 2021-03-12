---
title: Genel adres defterini yapılandır
description: Genel adres defteri için güvenlik ilkeleri ve varsayılan değerleri ayarlamak için bu yordamı kullanın.
author: msftbrking
manager: AnnBe
ms.date: 07/23/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirParameters
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4dcee425fc1225dcfcf8ba4282f4176acfeaa268
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796814"
---
# <a name="configure-the-global-address-book"></a><span data-ttu-id="3dd4a-103">Genel adres defterini yapılandır</span><span class="sxs-lookup"><span data-stu-id="3dd4a-103">Configure the global address book</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3dd4a-104">Genel adres defteri için güvenlik ilkeleri ve varsayılan değerleri ayarlamak için bu yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-104">Use this procedure to set the default values and security policies for the global address book.</span></span> 

<span data-ttu-id="3dd4a-105">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="3dd4a-106">Bu görev planlama ve yapılandırma takımı için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-106">This task is intended for the Planning and configuration team.</span></span>

1. <span data-ttu-id="3dd4a-107">Gezinti bölmesinde **Modüller > Kuruluş yönetimi > Genel adres defteri > Genel adres defteri parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-107">In the Navigation pane, go to **Modules > Organization administration > Global address book > Global address book parameters**.</span></span>
2. <span data-ttu-id="3dd4a-108">**Ad sırası** alanında adların nasıl gösterileceğini seçin.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-108">In the **Name sequence** field, select how names should be shown.</span></span>
3. <span data-ttu-id="3dd4a-109">**Rolü olmayan tarafları sil** alanında, rol atanmamış olan tarafların silinip silinmeyeceğini seçin.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-109">In **Delete parties with no roles**, select whether to delete parties with that have not been assigned a role.</span></span>
4. <span data-ttu-id="3dd4a-110">**Tekrarlanan öğe denetimi kullan**'da yinelenen kayıtların denetlenip denetlenmeyeceğini seçin.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-110">In **Use duplicate check**, select whether to check for duplicate records.</span></span>
5. <span data-ttu-id="3dd4a-111">**Adreslerde DUNS numarasını görüntüle**'de adreslerde DUNS numarasının görüntülenip görüntülenmeyeceğini seçin.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-111">In **Display DUNS number on addresses**, select whether to display the DUNS number on addresses.</span></span>
6. <span data-ttu-id="3dd4a-112">**Benzersiz DUNS numarasını denetle**'de benzersiz DUNS numaralarının kontrol edilip edilmeyeceğini seçin.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-112">In **Check for unique DUNS number**, select whether to check for unique DUNS numbers.</span></span>
7. <span data-ttu-id="3dd4a-113">**Taraf** alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-113">In the **Party** field, select an option.</span></span>
8. <span data-ttu-id="3dd4a-114">**Müşteri** alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-114">In the **Customer** field, select an option.</span></span>
9. <span data-ttu-id="3dd4a-115">**Satıcı** alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-115">In the **Vendor** field, select an option.</span></span>
10. <span data-ttu-id="3dd4a-116">**Potansiyel** alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-116">In the **Prospect** field, select an option.</span></span>
11. <span data-ttu-id="3dd4a-117">**Rekabetçi** alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-117">In the **Competitor** field, select an option.</span></span>
12. <span data-ttu-id="3dd4a-118">**Özel konum güvenliği** sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-118">Click the **Private location security** tab.</span></span>
13. <span data-ttu-id="3dd4a-119">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-119">In the list, find and select the desired record.</span></span> <span data-ttu-id="3dd4a-120">**Seçilen roller**'i bölmesine eklemek üzere birden çok rol seçmek için Shift tuşuna basın ve seçili rolleri eklemek için oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-120">Press the Shift key to select multiple roles to add to the **Selected roles** pane and then click the arrow to add the selected roles.</span></span>  
14. <span data-ttu-id="3dd4a-121">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3dd4a-121">Click **Save**.</span></span>


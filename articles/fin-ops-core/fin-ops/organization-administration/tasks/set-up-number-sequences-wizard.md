---
title: Sihirbaz kullanarak numara serilerini ayarlama
description: Bu konu, bir sihirbaz kullanarak aynı anda tüm gerekli numara sıralarının nasıl ayarlanacağını açıklar.
author: sericks007
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f97c4cd6cdb117ebdd67a155478bb6f8d1703541
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180423"
---
# <a name="set-up-number-sequences-using-a-wizard"></a><span data-ttu-id="1749f-103">Sihirbaz kullanarak numara serilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="1749f-103">Set up number sequences using a wizard</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1749f-104">Numara serileri, ana veri kayıtları ve bunları gerektiren işlem kayıtları için okunabilir ve benzersiz tanımlayıcılarını oluşturmada kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1749f-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="1749f-105">Tanımlayıcı gerektiren bir ana veri veya hareket kaydı, referans olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="1749f-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="1749f-106">Bir referans için yeni kayıtlar oluşturmadan önce, bir numara serisi oluşturmalı ve bunu referans ile ilişkilendirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="1749f-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="1749f-107">Bu konu, bir sihirbaz kullanarak aynı anda tüm gerekli numara sıralarının nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="1749f-107">This topic explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="1749f-108">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="1749f-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="1749f-109">**Gezinti > Modüller > Kuruluş yönetimi > Numara serileri > Numara serileri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="1749f-109">Go to **Navigation > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="1749f-110">**Oluştur**seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="1749f-110">Select **Generate**.</span></span>
3. <span data-ttu-id="1749f-111">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1749f-111">Select **Next**.</span></span>

   - <span data-ttu-id="1749f-112">Bu sayfada, kimlik kodu, en küçük değer ve en yüksek değeri değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1749f-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="1749f-113">Ayrıca, numara serisinin sürekli olması gerekip gerekmediğini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1749f-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
   - <span data-ttu-id="1749f-114">Numara serisi için önceden numara tahsis etmeniz gerekiyorsa **Devamlı** seçeneğini seçmeyin.</span><span class="sxs-lookup"><span data-stu-id="1749f-114">Do not select the **Continuous** option if you must preallocate numbers for the number sequence.</span></span> <span data-ttu-id="1749f-115">Numara sırasının biçimi için bir kapsam kesim eklemek için biçimi listeden seçin ve **Kapsam Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1749f-115">To add a scope segment to the format of a number sequence, select the format in the list, and then select **Include scope in format**.</span></span> <span data-ttu-id="1749f-116">Numara sırasının biçimi için bir kapsam kesim çıkarmak için biçimi listeden seçin ve **Kapsam Çıkar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1749f-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then select **Remove scope from format**.</span></span> <span data-ttu-id="1749f-117">Bir numara serisi otomatik oluşturulmadan dışarıda tutmak için listede numara serisini seçin ve ardından **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1749f-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then select **Delete**.</span></span>  

4. <span data-ttu-id="1749f-118">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1749f-118">Select **Next**.</span></span>
5. <span data-ttu-id="1749f-119">**Bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1749f-119">Select **Finish**.</span></span>


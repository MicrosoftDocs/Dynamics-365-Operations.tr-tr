--- 
title: "Bir sihirbaz kullanarak satınalma için numara serilerini ayarla"
description: "Numara serileri, ana veri kayıtları ve bunları gerektiren işlem kayıtları için okunabilir ve benzersiz tanımlayıcılarını oluşturmada kullanılır."
author: sericks007
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e8f3227f231ffc287bd6ea6204ed50f8b684e5fb
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-number-sequences-by-using-a-wizard"></a><span data-ttu-id="a704f-103">Bir sihirbaz kullanarak satınalma için numara serilerini ayarla</span><span class="sxs-lookup"><span data-stu-id="a704f-103">Set up number sequences by using a wizard</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a704f-104">Numara serileri, ana veri kayıtları ve bunları gerektiren işlem kayıtları için okunabilir ve benzersiz tanımlayıcılarını oluşturmada kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a704f-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="a704f-105">Tanımlayıcı gerektiren bir ana veri veya hareket kaydı, referans olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="a704f-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="a704f-106">Bir referans için yeni kayıtlar oluşturmadan önce, bir numara serisi oluşturmalı ve bunu referans ile ilişkilendirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="a704f-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="a704f-107">Bu yordam, bir sihirbaz kullanarak aynı anda tüm gerekli numara sıralarının nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="a704f-107">This procedure explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="a704f-108">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="a704f-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="a704f-109">(Kuruluş yönetim > Numara serileri > Numara serileri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a704f-109">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="a704f-110">Üret'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a704f-110">Click Generate.</span></span>
3. <span data-ttu-id="a704f-111">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a704f-111">Click Next.</span></span>
    * <span data-ttu-id="a704f-112">Bu sayfada, kimlik kodu, en küçük değer ve en yüksek değeri değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a704f-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="a704f-113">Ayrıca, numara serisinin sürekli olması gerekip gerekmediğini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a704f-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
    * <span data-ttu-id="a704f-114">Numara serisi için önceden numara tahsis etmeniz gerekiyorsa Devamlı seçeneğini seçmeyin.</span><span class="sxs-lookup"><span data-stu-id="a704f-114">Do not select the Continuous option if you must preallocate numbers for the number sequence.</span></span>     <span data-ttu-id="a704f-115">Numara sırasının biçimi için bir kapsam kesim eklemek için biçimi listeden seçin ve Kapsam Ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a704f-115">To add a scope segment to the format of a number sequence, select the format in the list, and then click Include scope in format.</span></span>     <span data-ttu-id="a704f-116">Numara sırasının biçimi için bir kapsam kesim çıkarmak için biçimi listeden seçin ve Kapsam Çıkar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a704f-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then click Remove scope from format.</span></span>     <span data-ttu-id="a704f-117">Bir numara serisi otomatik oluşturulmadan dışarıda tutmak için listede numara serisini seçin ve ardından Sil'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a704f-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then click Delete.</span></span>  
4. <span data-ttu-id="a704f-118">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a704f-118">Click Next.</span></span>
5. <span data-ttu-id="a704f-119">Son düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a704f-119">Click Finish.</span></span>



---
title: Varlık hizmet düzeyleri
description: Bu konuda Varlık Yönetimi'ndeki varlık hizmet düzeyleri açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35e7a55b1ba230be6bb72b20fcd805ea061b648e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439206"
---
# <a name="asset-service-levels"></a><span data-ttu-id="c2b82-103">Varlık hizmet düzeyleri</span><span class="sxs-lookup"><span data-stu-id="c2b82-103">Asset service levels</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c2b82-104">Bu konuda Varlık Yönetimi'ndeki varlık hizmet düzeyleri açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c2b82-104">This topic explains asset service levels in Asset Management.</span></span> <span data-ttu-id="c2b82-105">Varlık hizmet düzeyleri varlıklarla ilişkilidir ve bakım isteklerine ve iş emirlerine aktarılır.</span><span class="sxs-lookup"><span data-stu-id="c2b82-105">Asset service levels are related to assets, and are transferred to maintenance requests and work orders.</span></span> <span data-ttu-id="c2b82-106">İş emri planlaması sırasında iş emirlerinin önceliğini hesaplamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c2b82-106">They are used to calculate the priority of work orders during work order scheduling.</span></span> <span data-ttu-id="c2b82-107">Değişiklik gerekiyorsa, varlık hizmet düzeyleri değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="c2b82-107">Asset service levels can be changed, if changes are required.</span></span>

<span data-ttu-id="c2b82-108">İş emri planlaması için derecelendirme puanlarının hesaplanmasıyla ilgili kurulum hakkında daha fazla bilgi için bkz. [Varlık Yönetimi parametreleri](../setup-for-objects/enterprise-asset-management-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c2b82-108">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span> <span data-ttu-id="c2b82-109">Varlık hizmet düzeyi için en az bir varsayılan kayıt ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c2b82-109">You must set up at least one default record for the asset service level.</span></span> <span data-ttu-id="c2b82-110">Bu varsayılan kayıt, iş emri planlaması sırasında başka bir eşleşme bulunamazsa kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c2b82-110">This default record is used if no other match is found during work order scheduling.</span></span>

<span data-ttu-id="c2b82-111">**Örnek 1:** Başka bir eşleşme bulunmazsa kullanılan varsayılan hizmet düzeyi.</span><span class="sxs-lookup"><span data-stu-id="c2b82-111">**Example 1:** The default service level that is used if no other match is found.</span></span> <span data-ttu-id="c2b82-112">Bu kayıtta, yalnızca bir hizmet düzeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="c2b82-112">In this record, you select only a service level.</span></span>

<span data-ttu-id="c2b82-113">**Örnek 2:** Volvo kamyon için işleri planlamak üzere kullanılan yüksek hizmet düzeyi.</span><span class="sxs-lookup"><span data-stu-id="c2b82-113">**Example 2:** A high service level that is used to schedule jobs for a Volvo truck engine.</span></span> <span data-ttu-id="c2b82-114">Bu kayıtta, ilgili bir varlık türü (**Kamyon** gibi), bir üretici (**Volvo**) ve bir hizmet düzeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="c2b82-114">In this record, you select a relevant asset type (such as **Truck Engine**), a manufacturer (**Volvo**), and a service level.</span></span>

## <a name="set-up-asset-service-levels"></a><span data-ttu-id="c2b82-115">Varlık hizmet düzeyleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="c2b82-115">Set up asset service levels</span></span>

1. <span data-ttu-id="c2b82-116">**Varlık yönetimi** \> **Kurulum** \> **Varlık hizmet düzeyleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c2b82-116">Select **Asset management** \> **Setup** \> **Asset service levels**.</span></span>
2. <span data-ttu-id="c2b82-117">Bir kayıt oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c2b82-117">Select **New** to create a record.</span></span>
3. <span data-ttu-id="c2b82-118">Varlık hizmet düzeyi için gerekli olan ayrıntı düzeyine bağlı olarak **İşlem yapılacak yerleşim**, **Varlık türü**, **Üretici**, **Model**, **Varlık**, **İş emri türü** ve **Hizmet düzeyi** alanlarında ilgili seçimleri yapın.</span><span class="sxs-lookup"><span data-stu-id="c2b82-118">Depending on the detail level that is required for the asset service level, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Work order type**, and **Service level** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c2b82-119">Varlık hizmet düzeyi bakım talepleri ve iş emirleri için kullanıldığında, Varlık yönetimi olası bir eşleşmeyi denetlemek için tüm varlık hizmet düzeyi kayıtlarına bakar.</span><span class="sxs-lookup"><span data-stu-id="c2b82-119">When the asset service level is used for maintenance requests and work orders, Asset Management goes through all asset service level records to check for a possible match.</span></span> <span data-ttu-id="c2b82-120">Her zaman ilk önce en belirgin birleşimi denetler.</span><span class="sxs-lookup"><span data-stu-id="c2b82-120">It always checks the most specific combination first.</span></span> <span data-ttu-id="c2b82-121">Başka bir deyişle, Varlık Yönetimi **İş emri türü** alanı için bir eşleşme arar.</span><span class="sxs-lookup"><span data-stu-id="c2b82-121">In other words, Asset Management first checks for a match for the **Work order type** field.</span></span> <span data-ttu-id="c2b82-122">Eşleşme bulamazsa **Varlık** alanı için eşleşmeleri denetler ve bu şekilde devam eder.</span><span class="sxs-lookup"><span data-stu-id="c2b82-122">If no match is found, it checks for a match for the **Asset** field, and so on.</span></span> <span data-ttu-id="c2b82-123">**Varlık hizmet düzeyleri** sayfasının düzeninde gördüğünüz gibi bu davranış en belirgin birleşimi bulmak için Varlık Yönetimi'nin eşleşme için sağdan sola her kaydı denetleyeceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="c2b82-123">As you can see in the layout of the **Asset service levels** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="c2b82-124">Eşleşme bulunmazsa, bu alanlarda hiçbir seçimi olmayan varsayılan kayıt kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c2b82-124">If no match is found, the default record that has no selections in those fields is used.</span></span>

4. <span data-ttu-id="c2b82-125">**Hizmet düzeyi** alanında, hizmet düzeyini (önceliği) belirten bir sayı seçin.</span><span class="sxs-lookup"><span data-stu-id="c2b82-125">In the **Service level** field, select a number that indicates the service level (priority).</span></span>


> [!NOTE]
> <span data-ttu-id="c2b82-126">**Varlık hizmeti düzeyleri** sayfasındaki bir varlık hizmet düzeyi kaydını bir iş emri üzerinde zaten kullandıktan sonra değiştirirseniz, bakım taleplerindeki ve iş emirlerindeki hizmet düzeyi buna göre güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="c2b82-126">If you change an asset service level record on the **Asset service levels** page after you've already used it on a work order, the service level on maintenance requests and work orders isn't updated accordingly.</span></span>

---
title: Sorumlu bakım görevlileri
description: Bu konuda Varlık Yönetimi'nde sorumlu bakım görevlisi ayarlama işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 432a235668bbd969f497003a98b7f66390e5308f
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790548"
---
# <a name="responsible-maintenance-workers"></a><span data-ttu-id="e05e6-103">Sorumlu bakım görevlileri</span><span class="sxs-lookup"><span data-stu-id="e05e6-103">Responsible maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="e05e6-104">Sorumlu bakım görevlisi, varlık türleri, varlıklar, işlem yapılacak yerleşim, bakım işi türü kategorileri, bakım işi türleri, bakım işi türü türevleri ve ticaret ile ilgili olabilir.</span><span class="sxs-lookup"><span data-stu-id="e05e6-104">Responsible maintenance workers can be related to asset types, assets, functional locations, maintenance job type categories, maintenance job types, maintenance job type variants, and trades.</span></span> <span data-ttu-id="e05e6-105">İş emri ve bakım taleplerinde, çalışma emrinden sorumlu olması gereken bakım görevlileri hakkında bir tercih belirtmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e05e6-105">They can be used on work orders and maintenance requests to indicate a preference about the maintenance workers who should be responsible for a work order.</span></span> <span data-ttu-id="e05e6-106">(Ancak, bu bakım görevlileri mutlaka iş emrini yürütmek için planlanan aynı çalışanlar değildir.) Bu işlevin kullanılması isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e05e6-106">(However, those maintenance workers aren't necessarily the same workers who are scheduled to carry out the work order.) Use of this functionality is optional.</span></span> <span data-ttu-id="e05e6-107">Örneğin, belirli iş türleri veya çalışma alanları için sorumlu çalışanlaro veya çalışan gruplarını seçmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e05e6-107">For example, it can be used to select responsible workers or worker groups for specific work types or work areas.</span></span>

<span data-ttu-id="e05e6-108">İş emri yaşam döngüsü veya bakım talebi yaşam döngüsü sırasında, sorumlu bakım görevlileri değiştirilebilir veya güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="e05e6-108">During a work order lifecycle or a maintenance request lifecycle, responsible maintenance workers can be changed or updated.</span></span> <span data-ttu-id="e05e6-109">Bu değişiklik veya güncelleştirme, örneğin, bakım talebi yaşam döngüsü durumu veya iş emri yaşam döngüsü durumunda bir değişiklik ile ilgili olabilir.</span><span class="sxs-lookup"><span data-stu-id="e05e6-109">This change or update might be related to, for example, a change in the maintenance request lifecycle state or the work order lifecycle state.</span></span>

<span data-ttu-id="e05e6-110">**Sorumlu bakım görevlileri** sayfasındaki kurulum, iş emri planlaması sırasında *kullanılmaz*.</span><span class="sxs-lookup"><span data-stu-id="e05e6-110">The setup on the **Responsible maintenance workers** page is *not* used during work order scheduling.</span></span>

> [!NOTE]
> <span data-ttu-id="e05e6-111">Varlık Yönetimi'nde, iş emri planlaması sırasında iş emirlerine tahsis edilebilecek *tercih edilen* bakım görevlisini de ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e05e6-111">In Asset Management, you can also set up *preferred* maintenance workers who might be allocated to work orders during work order scheduling.</span></span>

<span data-ttu-id="e05e6-112">Sorumlu bakım görevlilerini ayarlaymadan önce, seçim için kullanılabilir olması gereken işçiler ve bakım görevlilerinin gruplarını ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e05e6-112">Before you can set up responsible maintenance workers, you must set up the workers and maintenance worker groups that should be available for selection.</span></span> <span data-ttu-id="e05e6-113">(Çalışan ve bakım görevlileri gruplarını nasıl ayarlayacağınızla ilgili daha fazla bilgi için bkz: [Bakım görevlileri ve çalışan grupları](../setup-for-objects/workers-and-worker-groups.md).)</span><span class="sxs-lookup"><span data-stu-id="e05e6-113">For information about how to set up workers and maintenance worker groups, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-responsible-maintenance-workers"></a><span data-ttu-id="e05e6-114">Sorumlu bakım görevlilerini ayarla</span><span class="sxs-lookup"><span data-stu-id="e05e6-114">Set up responsible maintenance workers</span></span>

1. <span data-ttu-id="e05e6-115">**Kıymet yönetimi** \> **Kurulum** \> **Çalışanlar** \> **Sorumlu bakım görevlileri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e05e6-115">Select **Asset management** \> **Setup** \> **Workers** \> **Responsible maintenance workers**.</span></span>
2. <span data-ttu-id="e05e6-116">Bir kayıt oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e05e6-116">Select **New** to create a record.</span></span>
3. <span data-ttu-id="e05e6-117">Öncelikle yalnızca **Sorumlu bakım görevlisi** alanını ve/veya **Sorumlu çalışan** alanını ayarladığınız varsayılan sorumlu bakım görevlisi veya sorumlu bakım görevlisi grubu kurulumunu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e05e6-117">First create a default responsible maintenance worker or responsible maintenance worker group setup, where you set only the **Responsible maintenance worker group** field and/or the **Responsible worker** field.</span></span> <span data-ttu-id="e05e6-118">Kalan alanları boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="e05e6-118">Leave the remaining fields blank.</span></span> <span data-ttu-id="e05e6-119">Bu varsayılan kurulum, iş emri planlaması sırasında başka, daha özel kombinasyon iş emrinin içeriğiyle eşleşirse kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="e05e6-119">This default setup will be used during work order scheduling if no other, more specific combination matches the contents of the work order.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e05e6-120">Bir bakım talebinin yaratılması sırasında, **Tüm bakım talepleri** sayfasında seçim için sorumlu bir bakım görevlisi veya sorumlu bakım görevlisi grubu oluşturulduğunda, Varlık Yönetimi olası bir eşleşmeyi kontrol etmek için tüm sorumlu bakım görevlisi kayıtlarını kontrol eder.</span><span class="sxs-lookup"><span data-stu-id="e05e6-120">During creation of a maintenance request, when a responsible maintenance worker or responsible maintenance worker group is made available for selection on the **All maintenance requests** page, Asset Management goes through all responsible maintenance worker records to check for a possible match.</span></span> <span data-ttu-id="e05e6-121">Her zaman ilk önce en belirgin birleşimi denetler.</span><span class="sxs-lookup"><span data-stu-id="e05e6-121">It always checks the most specific combination first.</span></span> <span data-ttu-id="e05e6-122">Diğer bir deyişle, Kıymet Yönetimi önce **Ticaret** alanı için bir eşleşme arar.</span><span class="sxs-lookup"><span data-stu-id="e05e6-122">In other words, Asset Management first checks for a match for the **Trade** field.</span></span> <span data-ttu-id="e05e6-123">Eşleşme bulamazsa **Bakım işi** alanı için eşleşmeleri denetler.</span><span class="sxs-lookup"><span data-stu-id="e05e6-123">If no match is found, it checks for a match for the **Maintenance job type variant** field.</span></span> <span data-ttu-id="e05e6-124">Eşleşme bulamazsa **Bakım işi türü** alanı için eşleşmeleri denetler ve bu şekilde devam eder.</span><span class="sxs-lookup"><span data-stu-id="e05e6-124">If no match is found, it checks for a match for the **Maintenance job type** field, and so on.</span></span> <span data-ttu-id="e05e6-125">Sayfanın mizanpajında gördüğünüz gibi bu davranış en spesifik kombinasyonu bulmak için varlık yönetimi, her kaydı sağdan sola doğru kontrol eder (ilk önce **Ticaret**, sonra **Bakım işi türü varyantı**, sonra **Bakım işi türü**, sonra **Bakım işi türü kategorisi**, sonra **İşlem yapılacak yerleşim**, sonra **Varlık** ve son olarak **Varlık türü**).</span><span class="sxs-lookup"><span data-stu-id="e05e6-125">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match (first **Trade**, then **Maintenance job type variant**, then **Maintenance job type**, then **Maintenance job type category**, then **Functional location**, then **Asset**, and finally **Asset type**).</span></span> <span data-ttu-id="e05e6-126">Eşleşme bulunmazsa, bu yedi alanda hiçbir seçimi olmayan varsayılan kayıt kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e05e6-126">If no match is found, the default record that has no selections in those seven fields is used.</span></span>

<span data-ttu-id="e05e6-127">Aşağıdaki çizimde bir **Sorumlu bakım görevlileri** liste sayfasının bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e05e6-127">The following illustration shows an example of the **Responsible maintenance workers** page.</span></span>

![Şekil 1](media/08-setup-for-requests.png)

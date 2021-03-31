---
title: İş emri türleri
description: Bu konuda Varlık Yönetimi'nde iş emri türünü açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 561ca87740d90590262716f0042fca6b59dafc69
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223542"
---
# <a name="work-order-types"></a><span data-ttu-id="58fb2-103">İş emri türleri</span><span class="sxs-lookup"><span data-stu-id="58fb2-103">Work order types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="58fb2-104">İş emri türleri, iş emirlerini sınıflandırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="58fb2-104">Work order types are used to categorize work orders.</span></span> <span data-ttu-id="58fb2-105">Örneğin, önleyici bakım ve düzeltici bakım ya da ilgili bakımiş emirlerine sahip olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58fb2-105">For example, you might have work orders that are related to preventive maintenance or corrective maintenance.</span></span>

<span data-ttu-id="58fb2-106">Bir iş emri türü, iş emri yaşam döngüsü modeliyle bir ilişki tanımlar.</span><span class="sxs-lookup"><span data-stu-id="58fb2-106">A work order type defines an affiliation with a work order lifecycle model.</span></span> <span data-ttu-id="58fb2-107">Bir iş emri yaşam döngüsü modeli, bir iş emrinde ayarlayabilecek iş emri yaşam döngüsü durumlarını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="58fb2-107">A work order lifecycle model defines the work order lifecycle states that can be set on a work order.</span></span> <span data-ttu-id="58fb2-108">(İş emri yaşam döngüsü durumlarına örnek olarak **Oluşturma tarihi**, **İşlemde**, ve **Tamamlandı** verilebilir.)</span><span class="sxs-lookup"><span data-stu-id="58fb2-108">(Examples of work order lifecycle states include **Created**, **In Process**, and **Finished**.)</span></span>

<span data-ttu-id="58fb2-109">İş emri yaşam döngüsü durumları ve proje aşamaları hakkında daha fazla bilgi için bkz [İş emri yaşam döngüsü durumu](work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="58fb2-109">For more information about work order lifecycle states and project stages, see [Work order lifecycle states](work-order-lifecycle-states.md).</span></span>

1. <span data-ttu-id="58fb2-110">**Kıymet yönetimi** \> **Kurulum** \> **İş emirleri** \> **İş emri türleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="58fb2-110">Select **Asset management** \> **Setup** \> **Work orders** \> **Work order types**.</span></span>
2. <span data-ttu-id="58fb2-111">İş emri türü oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="58fb2-111">Select **New** to create a work order type.</span></span>
3. <span data-ttu-id="58fb2-112">**İş emri türü** alanına iş emri türü için bir kimlik girin.</span><span class="sxs-lookup"><span data-stu-id="58fb2-112">In the **Work order type** field, enter an ID for the work order type.</span></span>
4. <span data-ttu-id="58fb2-113">**Ad** alanına, bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="58fb2-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="58fb2-114">**İş emri yaşam döngüsü modeli** alanında bir yaşam döngüsü modeli seçin.</span><span class="sxs-lookup"><span data-stu-id="58fb2-114">In the **Work order lifecycle model** field, select a lifecycle model.</span></span>
5. <span data-ttu-id="58fb2-115">Bu tip bir iş emriyle ilişkili tüm iş siparişi işleri aynı bakım görevlisine zamanlanacaksa, **Bir bakım görevlisi** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="58fb2-115">Set the **One maintenance worker** option to **Yes** if all work order jobs that are related to a work order of this type should be scheduled to the same maintenance worker.</span></span>
6. <span data-ttu-id="58fb2-116">**Maliyet türü** alanında, uygun şekilde **Düzeltici**, **Önleyici** veya **Yatırım** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="58fb2-116">In the **Cost type** field, select **Corrective**, **Preventive**, or **Investment**, as appropriate.</span></span> <span data-ttu-id="58fb2-117">Bir iş emrindeki tüm iş emri işleri maliyet türünde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="58fb2-117">All work order jobs on a work order must have the same cost type.</span></span>
7. <span data-ttu-id="58fb2-118">**Zorunlu** bölümünde, arıza ile ilgili veya bakım kapalı kalma süresi ile ilgili bilgilerin bu tip bir iş emrine eklendiğini belirtmek için, ilgili seçenekleri **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="58fb2-118">In the **Mandatory** section, set the relevant options to **Yes** to specify which fault-related or maintenance downtime–related information is added to a work order of this type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="58fb2-119">**Zorunlu** bölümündeki seçenekler **İş emri yaşam döngüsü durumları** sayfasının **Doğrula** hızlı sekmesindeki seçeneklerle ilişkilidir (**Kıymet yönetimi** \> **Kurulum** \> **İş emirleri** \> **Yaşam döngüsü durumuları**).</span><span class="sxs-lookup"><span data-stu-id="58fb2-119">The options in the **Mandatory** section are related to the options on the **Validate** FastTab of the **Work order lifecycle states** page (**Asset management** \> **Setup** \> **Work orders** \> **Lifecycle states**).</span></span>

8. <span data-ttu-id="58fb2-120">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="58fb2-120">Select **Save**.</span></span>

![İş emri türleri](media/16-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Bakım taleplerinden iş istekleri oluşturma
description: Bu konuda Kıymet Yönetimi'nde bakım taleplerinden iş istekleri oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23039306bb827beb861eaacc3177f4917fabc8bf
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018108"
---
# <a name="create-work-orders-from-maintenance-requests"></a><span data-ttu-id="03fa8-103">Bakım taleplerinden iş istekleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="03fa8-103">Create work orders from maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="03fa8-104">Bakım talepleri oluşturduktan sonra, bunları iş emirlerine kolayca dönüştürebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03fa8-104">After you've created maintenance requests, you can easily convert them to work orders.</span></span> <span data-ttu-id="03fa8-105">Bu konu, bakım talepleriyle çalışmak, aynı anda birkaç bakım talebi güncelleştirmek ve aynı anda birkaç bakım talebi için bir iş emri oluşturmak için en hızlı yolu açıklar.</span><span class="sxs-lookup"><span data-stu-id="03fa8-105">This topic describes the quickest way to work with maintenance requests, update several maintenance requests at the same time, and then create a work order for several maintenance requests at the same time.</span></span> <span data-ttu-id="03fa8-106">**Etkin bakım talepleri** veya **İşlem yapılacak yerleşim bakım talepleri** sayfasında, aynı anda bir bakım talebiyle çalışabilir ve bir bakım talebini bir iş emrine dönüştürebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03fa8-106">On the **Active maintenance requests** or **My functional location maintenance requests** page, you can also work with one maintenance request at a time and convert one maintenance request to a work order.</span></span>

> [!NOTE]
> <span data-ttu-id="03fa8-107">Her bakım talebi yalnızca bir iş emri ile ilgili olabilir.</span><span class="sxs-lookup"><span data-stu-id="03fa8-107">Every maintenance request can be related to only one work order.</span></span> <span data-ttu-id="03fa8-108">Ancak, bakım taleplerini farklı varlıklar olsa bile birden çok bakım talebi bir iş emrine dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="03fa8-108">However, multiple maintenance requests can be included in one work order, even if the maintenance requests have different assets.</span></span>

1. <span data-ttu-id="03fa8-109">**Varlık yönetimi** \> **Ortak** \> **bakım talepleri** \> **Tüm bakım talepleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="03fa8-109">Select **Asset management** \> **Common** \> **maintenance requests** \> **All maintenance requests**.</span></span>
2. <span data-ttu-id="03fa8-110">Bakım taleplerinden bir iş emri oluşturmadan önce, bu bilgiler ilgili ise bakım talepleri için en az bir bakım işi türü ve aynı zamanda bir bakım işi türü varyantı ve ticaret, seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="03fa8-110">Before you can create a work order from maintenance requests, you must select, at a minimum, a maintenance job type for the maintenance requests, and also a maintenance job type variant and trade, if this information is relevant.</span></span> <span data-ttu-id="03fa8-111">Kılavuz görünümünde, bakım talebinin bilgilerini kolayca güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03fa8-111">In the grid view, you can easily update information for a maintenance request.</span></span>
3. <span data-ttu-id="03fa8-112">Bir iş emri oluşturmaya hazır olduğunuzda, içine dahil etmek için bakım taleplerini seçin.</span><span class="sxs-lookup"><span data-stu-id="03fa8-112">When you're ready to create a work order, select the maintenance requests to include in it.</span></span>

    - <span data-ttu-id="03fa8-113">İş emrini dönüştürmek için birkaç bakım talebi seçerseniz iş emrini oluşturmadan önce her iki **Varlık** alanı ve **Bakım iş türü** alanı ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="03fa8-113">If you select several maintenance requests to convert to a work order, both the **Asset** field and the **Maintenance job type** field must be set before you create the work order.</span></span>
    - <span data-ttu-id="03fa8-114">İş emrini dönüştürmek için bir bakım talebi seçerseniz iş emrini oluşturmadan önce yalnızca **Varlık** alanının ayarlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="03fa8-114">If you select one maintenance request to convert to a work order, only the **Asset** field must be set before you create the work order.</span></span> <span data-ttu-id="03fa8-115">Ancak, iş emrini oluşturduğunuzda, **İş emri oluştur** iletişim kutusunda bir bakım işi türü (ve bu bilgiler uygun ise, ilgili bakım iş türü varyantı ve ticaret) seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03fa8-115">However, when you create the work order, you can select a maintenance job type (and a related maintenance job type variant and trade, if this information is relevant) in the **Create work order** dialog box.</span></span>

4. <span data-ttu-id="03fa8-116">**İş emri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="03fa8-116">Select **Work order**.</span></span>
5. <span data-ttu-id="03fa8-117">**İş emri oluştur** iletişim kutusunda, alanları ayarlayın ve sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="03fa8-117">In the **Create work order** dialog box, set the fields, and then select **OK**.</span></span>

    <span data-ttu-id="03fa8-118">Bir ileti çubuğu, yeni bir iş emri oluşturulduğunu bildirebilir.</span><span class="sxs-lookup"><span data-stu-id="03fa8-118">A message bar might notify you that a new work order has been created.</span></span>

    <span data-ttu-id="03fa8-119">Ayrıca, bir bakım talebini temel alan bir iş emri oluşturduğunuzda, bakım talebiyle ilgili varlık bir garanti sözleşmesine eklendiğinde, bir ileti çubuğu garanti anlaşması hakkında sizi uyarır.</span><span class="sxs-lookup"><span data-stu-id="03fa8-119">Additionally, when you create a work order that is based on a maintenance request, if the asset that is related to the maintenance request is included in a warranty agreement, a message bar notifies you about the warranty agreement.</span></span>

6. <span data-ttu-id="03fa8-120">**Varlık yönetimi** \> **Ortak** \> **İş emirleri** \> **Tüm iş emirleri**'ni seçin ve yeni iş emrini açın.</span><span class="sxs-lookup"><span data-stu-id="03fa8-120">Select **Asset management** \> **Common** \> **Work orders** \> **All work orders**, and open the new work order.</span></span>

    ![Yeni iş emri açma](media/05-manage-maintenance-requests.png)


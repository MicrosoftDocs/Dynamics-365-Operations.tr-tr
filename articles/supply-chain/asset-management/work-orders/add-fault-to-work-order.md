---
title: İş emrine arıza ekleme
description: Bu konu, Varlık Yönetiminde iş emirlerine arıza kayıtlarının nasıl ekleneceğini açıklamaktadır.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e82026f1d73e7368d93109bc0b895b7368ac84d4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439327"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="c0ba9-103">İş emrine hata ekle</span><span class="sxs-lookup"><span data-stu-id="c0ba9-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="c0ba9-104">Arıza tasarımcısında tasarlanmış arızaları bir iş emrine ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-104">You can add faults that were set up in the fault designer to a work order.</span></span> <span data-ttu-id="c0ba9-105">İş emrinde seçilen varlık için kullanılan varlık türlerine bir veya daha fazla arıza kaydı bağlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-105">One or more fault records must be connected to the asset types that are used for the asset that is selected in the work order.</span></span> <span data-ttu-id="c0ba9-106">Kurulum hakkında daha fazla bilgi için bkz. [Arıza yönetimi](../setup-for-work-orders/fault-management.md)</span><span class="sxs-lookup"><span data-stu-id="c0ba9-106">For more information about the setup, see [Fault management](../setup-for-work-orders/fault-management.md).</span></span>

1. <span data-ttu-id="c0ba9-107">**Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-107">Select **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="c0ba9-108">Arıza kaydı yapmak için iş emrini seçin ve sonra Eylem bölmesinde, **İş emri** sekmesinde, **Varlık** grubunda, **Varlık arızası**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-108">Select the work order to make a fault registration on, and then, on the Action Pane, on the **Work order** tab, in the **Asset** group, select **Asset fault**.</span></span>

3. <span data-ttu-id="c0ba9-109">**Belirtiler** hızlı sekmesinde **Satır ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-109">On the **Symptoms** FastTab, select **Add line**.</span></span> <span data-ttu-id="c0ba9-110">**Arıza** alanına otomatik olarak sıralı bir arıza numarası girilir.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-110">A sequential fault number is automatically entered in the **Fault** field.</span></span>

4. <span data-ttu-id="c0ba9-111">**Arıza belirtisi** alanında ilgili belirtiyi seçin.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-111">In the **Fault symptom** field, select the relevant symptom.</span></span>

5. <span data-ttu-id="c0ba9-112">**Arıza alanı** ve **Arıza türü** alanlarında uygun değerleri seçin.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-112">In the **Fault area** and **Fault type** fields, select the appropriate values.</span></span>

6. <span data-ttu-id="c0ba9-113">**Arıza tarihi** alanına geçerli tarih otomatik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="c0ba9-114">Gereksinim duyduğunuz şekilde farklı bir tarih seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-114">You can select a different date as you require.</span></span>

7. <span data-ttu-id="c0ba9-115">**Seçilen belirtinin nedenleri** hızlı sekmesine, sorunun nedenini açıklayan bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-115">On the **Causes for selected symptom** FastTab, add a line to describe the cause of the issue.</span></span>

8. <span data-ttu-id="c0ba9-116">**Seçilen belirtinin çözümleri** hızlı sekmesine, sorunun olası çözümünü açıklayan bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-116">On the **Remedies for selected symptom** FastTab, add a line to describe a possible solution to the issue.</span></span>

9. <span data-ttu-id="c0ba9-117">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-117">Select **Save**.</span></span>

<span data-ttu-id="c0ba9-118">Aşağıdaki şekilde bir arıza merkezi kaydı örneği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-118">The illustration below shows an example of a fault registration.</span></span>

![Şekil 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="c0ba9-120">Varlık arızalarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="c0ba9-120">View asset faults</span></span>

<span data-ttu-id="c0ba9-121">**Varlık arızaları** listesinde, varlıklara kaydedilen tüm arızalara genel bakış bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-121">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="c0ba9-122">**Varlık arızaları** liste sayfasında, varlıklara kaydedilmiş olan tüm arızalara genel bakış bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-122">On the **Asset faults** list page, you can get an overview of all faults that have been registered on assets.</span></span> <span data-ttu-id="c0ba9-123">Sayfayı açmak için **Varlık yönetimi** > **Sorgular** > **Varlık arızası** > **Varlık arızaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-123">To open the page, select **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="c0ba9-124">Varlık arızası raporunu yazdırma</span><span class="sxs-lookup"><span data-stu-id="c0ba9-124">Print asset fault report</span></span>

<span data-ttu-id="c0ba9-125">**Tüm varlıklar** liste sayfasından, tüm arıza kayıtlarını görüntüleyen bir varlık arıza raporu yazdırabilir ve arıza istatistiklerine ilişkin bir grafik özet alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-125">From the **All assets** list page, you can print an asset fault report that shows all fault registrations and a graphical overview of fault statistics.</span></span>

1. <span data-ttu-id="c0ba9-126">**Varlık yönetimi** > **Ortak** > **Varlıklar** > **Tüm varlıklar** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-126">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="c0ba9-127">Arıza raporu yazdırılacak olan varlığı seçin.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-127">Select the asset to print a fault report for.</span></span>

3. <span data-ttu-id="c0ba9-128">Eylem Bölmesinde, **Genel** sekmesindeki **Raporlar** gurubunda **Varlık arızası**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-128">On the Action Pane, on the **General** tab, in the **Reports** group, select **Asset fault**.</span></span>

4. <span data-ttu-id="c0ba9-129">Belirli bir dönem girin veya bir arıza türü seçin.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-129">Enter a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="c0ba9-130">Raporu yazdırmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-130">Select **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="c0ba9-131">Çeşitli varlıklar veya varlık türleri için bir arıza raporu yazdırmak üzere **Varlık yönetimi** > **Raporlar** > **Varlıklar** > **Varlık arızası**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="c0ba9-131">To print a fault report for several assets or asset types, select **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>


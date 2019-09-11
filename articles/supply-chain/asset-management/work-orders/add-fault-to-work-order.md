---
title: İş emrine arıza ekleme
description: Bu konu, Varlık Yönetiminde iş emirlerine arıza kayıtlarının nasıl ekleneceğini açıklamaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875950"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="2ad33-103">İş emrine arıza ekleme</span><span class="sxs-lookup"><span data-stu-id="2ad33-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="2ad33-104">Arıza tasarımcısında bir iş emrine arızalar kurulumu ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ad33-104">You can add faults set up in the fault designer to a work order.</span></span> <span data-ttu-id="2ad33-105">İş emrinde seçilen varlık, kendisine bağlanmış bir veya daha fazla arıza kaydı olan varlık türleri içermelidir.</span><span class="sxs-lookup"><span data-stu-id="2ad33-105">The asset selected in the work order must contain asset types that have one or more fault records connected to it.</span></span> <span data-ttu-id="2ad33-106">[Arıza yönetimi](../setup-for-work-orders/fault-management.md) bölümünden kurulum hakkında daha fazla bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="2ad33-106">Read more about setup in the [Fault management](../setup-for-work-orders/fault-management.md) section.</span></span>

1. <span data-ttu-id="2ad33-107">**Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ad33-107">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="2ad33-108">Listede, arıza kaydı yapmak istediğiniz iş emrini seçin ve **Varlık arızası**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ad33-108">In the list, select the work order on which you want to make a fault registration and click **Asset fault**.</span></span>

3. <span data-ttu-id="2ad33-109">**Belirtiler** hızlı sekmesinde **Satır ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ad33-109">On the **Symptoms** FastTab, click **Add line**.</span></span> <span data-ttu-id="2ad33-110">**Arıza** alanına otomatik olarak sıralı bir arıza numarası eklenir.</span><span class="sxs-lookup"><span data-stu-id="2ad33-110">A sequential fault number is automatically inserted in the **Fault** field.</span></span>

4. <span data-ttu-id="2ad33-111">**Arıza belirtisi** alanında ilgili belirtiyi seçin.</span><span class="sxs-lookup"><span data-stu-id="2ad33-111">Select the relevant symptom in the **Fault symptom** field.</span></span>

5. <span data-ttu-id="2ad33-112">**Arıza alanı** ve **Arıza türü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="2ad33-112">Select **Fault area** and **Fault type**.</span></span>

6. <span data-ttu-id="2ad33-113">**Arıza tarihi** alanına geçerli tarih otomatik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="2ad33-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="2ad33-114">Gerekirse başka bir tarih seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ad33-114">You can select another date, if necessary.</span></span>

7. <span data-ttu-id="2ad33-115">**Seçilen belirtinin nedenleri** hızlı sekmesine, sorunun nedenini açıklayan bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2ad33-115">On the **Causes for selected symptom** FastTab, add a line describing the cause of the problem.</span></span>

8. <span data-ttu-id="2ad33-116">**Seçilen belirtinin çözümleri** hızlı sekmesine, sorunun olası çözümünü açıklayan bir satır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2ad33-116">On the **Remedies for selected symptom** FastTab, add a line describing a possible solution to the problem.</span></span>

9. <span data-ttu-id="2ad33-117">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ad33-117">Click **Save**.</span></span>

![Şekil 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="2ad33-119">Varlık arızalarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="2ad33-119">View asset faults</span></span>

<span data-ttu-id="2ad33-120">**Varlık arızaları** listesinde, varlıklara kaydedilen tüm arızalara genel bakış bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ad33-120">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="2ad33-121">Listeyi açmak için **Varlık yönetimi** > **Sorgular** > **Varlık arızası** > **Varlık arızaları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ad33-121">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults** to open the list.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="2ad33-122">Varlık arızası raporunu yazdırma</span><span class="sxs-lookup"><span data-stu-id="2ad33-122">Print asset fault report</span></span>

<span data-ttu-id="2ad33-123">**Tüm varlıklar** listesi sayfasından, tüm arıza kayıtlarını görüntüleyen bir kıymet hata raporu yazdırabilir ve hata istatistiklerine ilişkin bir grafik özet alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ad33-123">From the **All assets** list page, you can print an asset fault report displaying all fault registrations as well as a graphic overview of fault statistics.</span></span>

1. <span data-ttu-id="2ad33-124">**Varlık yönetimi** > **Ortak** > **Varlıklar** > **Tüm varlıklar** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2ad33-124">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="2ad33-125">**Varlıklar** listesinde, bir arıza raporu yazdırmak istediğiniz varlığı seçin.</span><span class="sxs-lookup"><span data-stu-id="2ad33-125">In the **Assets** list, select the asset for which you want to print a fault report.</span></span>

3. <span data-ttu-id="2ad33-126">**Genel** sekmesinde > **Raporlar** bölümünde **Varlık arızası**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ad33-126">On the **General** tab > **Reports section**, click **Asset fault**.</span></span>

4. <span data-ttu-id="2ad33-127">Belirli bir dönem ekleyin veya bir hata türü seçin.</span><span class="sxs-lookup"><span data-stu-id="2ad33-127">Insert a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="2ad33-128">Raporu yazdırmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ad33-128">Click **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="2ad33-129">Ayrıca **Varlık yönetimi** > **Raporlar** > **Varlıklar** > **Varlık arızası**'na tıklayarak çeşitli varlıklar veya varlık türleri için bir arıza raporu yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ad33-129">You can also print a fault report for several assets or asset types by clicking **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>


---
title: Kıymet hata maliyeti denetimi
description: Bu konuda Varlık Yönetimi'nde varlık arıza maliyet denetimini açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.openlocfilehash: 2fe75c327cdc2bdd76173430ed551895f5941c7b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918315"
---
# <a name="asset-fault-cost-control"></a><span data-ttu-id="3f576-103">Kıymet hata maliyeti denetimi</span><span class="sxs-lookup"><span data-stu-id="3f576-103">Asset fault cost control</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="3f576-104">Varlık Yönetimi'nde, varlık arıza kayıtlarındaki maliyetleri hesaplayarak fiili maliyetlerin arızalardaki bütçe maliyetlerine karşılaştırmasına genel bakış elde edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f576-104">In Asset Management, you can calculate costs on asset fault registrations to get an overview of actual costs compared to budget costs on faults.</span></span> <span data-ttu-id="3f576-105">Fiili maliyetler deftere nakledilen hareketleri temel alarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="3f576-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="3f576-106">Tarih, belirtinin kaydedildiği arıza tarihidir.</span><span class="sxs-lookup"><span data-stu-id="3f576-106">The date is the fault date on which the symptom was recorded.</span></span>

1. <span data-ttu-id="3f576-107">**Varlık Yönetimi** > **Sorgular** > **Varlık hatası** > **Varlık hata maliyet denetimi**'ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3f576-107">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault cost control**.</span></span>

2. <span data-ttu-id="3f576-108">**Varlık arıza maliyeti denetimi** iletişim kutusunda, gerekirse hesaplamaya dahil edilecek bir mali boyut kümesi seçin.</span><span class="sxs-lookup"><span data-stu-id="3f576-108">In the **Asset fault cost control** dialog, select a financial dimension set to be included in the calculation, if required.</span></span>

4. <span data-ttu-id="3f576-109">Sıfır saat içeren sonuçları göstermek istemiyorsanız, **sıfır atlama** düğmesi üzerinde "Evet" seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="3f576-109">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="3f576-110">İşlem yapılacak yerleşimlerle ilgili olarak maliyet denetimi satırlarının ne kadar ayrıntılı olmasını istediğinizi belirtmek için **Düzey** alanını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f576-110">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> <span data-ttu-id="3f576-111">Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim yapınız varsa, işlem yapılacak yerleşim için tüm varlık arızası maliyet denetimi satırları üst düzeyde gösterilir ve dolayısıyla bir satırdaki saatler, alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="3f576-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="3f576-112">**Düzey** alanına "0" sayısını girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeylerinde bulunan tüm varlık arıza maliyet denetimi satırlarını gösteren ayrıntılı bir sonuç görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="3f576-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault cost control lines on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="3f576-113">Aramayı sınırlandırmak istiyorsanız, Hızlı Sekme **dahil edilecek kayıtlar** üzerinde belirli kıymetleri, arıza tarihlerini, arıza nedenlerini ve arızaları seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f576-113">If you want to limit the search, you can select specific assets, fault dates, and fault causes on the **Records to include** FastTab.</span></span>

7. <span data-ttu-id="3f576-114">Hesaplamayı başlatmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3f576-114">Click **OK** to start the calculation.</span></span>

8. <span data-ttu-id="3f576-115">**Gruplandırma ölçütü...** eylem bölmesi gruplarında, hesaplamanın gerekli ayrıntı düzeyini göstermek için ilgili düğmelere tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3f576-115">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="3f576-116">Seçilen eylem bölmesi düğmeleri vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="3f576-116">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="3f576-117">Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3f576-117">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="3f576-118">Aşağıdaki şekil, varlık arıza maliyeti denetimi hesaplamasının birkaç örneğini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="3f576-118">The figure below shows an example of an asset fault cost control calculation.</span></span>

![Şekil 1](media/05-controlling-and-reporting.png)

<span data-ttu-id="3f576-120">Varsayılanları ayarlamak hakkında bilgi için [Arıza yönetimi](../setup-for-work-orders/fault-management.md)'ne başvurun.</span><span class="sxs-lookup"><span data-stu-id="3f576-120">Refer to the [Fault management](../setup-for-work-orders/fault-management.md) section for information on how to set up faults.</span></span>

>[!NOTE]
><span data-ttu-id="3f576-121">**Orijinal bütçe** alanı, bütçe maliyetlerini iş emri tahmininden gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f576-121">The **Original budget** field shows budget costs from the work order forecast.</span></span> <span data-ttu-id="3f576-122">**Fiili maliyet** alanı, iş emirlerinde deftere nakledilen maliyetleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f576-122">The **Actual cost** field shows posted costs on work orders.</span></span> <span data-ttu-id="3f576-123">**Taahhüt edilen maliyet** alanı, şirketinizin iş siparişleri ile ilgili olarak taahhüt edildiği toplam maliyet miktarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f576-123">The **Committed cost** field shows total costs that your company is committed to in relation to work orders.</span></span>


---
title: Kıymet hata maliyeti denetimi
description: Bu konuda Varlık Yönetimi'nde varlık arıza maliyet denetimini açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCostControlFault
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 93bd6fb320822f17af5725e227936df623f8d0be
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439197"
---
# <a name="asset-fault-cost-control"></a><span data-ttu-id="226ac-103">Kıymet hata maliyeti denetimi</span><span class="sxs-lookup"><span data-stu-id="226ac-103">Asset fault cost control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="226ac-104">Varlık Yönetimi'nde, varlık arıza kayıtlarındaki maliyetleri hesaplayarak fiili maliyetlerin bütçe maliyetlerine karşılaştırmasına genel bakış elde edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="226ac-104">In Asset Management, you can calculate costs on asset fault registrations to get an overview of actual costs compared to budget costs.</span></span> <span data-ttu-id="226ac-105">Fiili maliyetler deftere nakledilen hareketleri temel alarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="226ac-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="226ac-106">Tarih, belirtinin kaydedildiği arıza tarihidir.</span><span class="sxs-lookup"><span data-stu-id="226ac-106">The date is the fault date on which the symptom was recorded.</span></span>

1. <span data-ttu-id="226ac-107">**Varlık Yönetimi** > **Sorgular** > **Varlık hatası** > **Varlık hata maliyet denetimi**'ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="226ac-107">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault cost control**.</span></span>

2. <span data-ttu-id="226ac-108">**Varlık arıza maliyeti denetimi** iletişim kutusunda, gerekirse hesaplamaya dahil edilecek bir mali boyut kümesi seçin.</span><span class="sxs-lookup"><span data-stu-id="226ac-108">In the **Asset fault cost control** dialog, select a financial dimension set to be included in the calculation, if required.</span></span>

4. <span data-ttu-id="226ac-109">Sıfır saat içeren sonuçları göstermek istemiyorsanız, **sıfır atlama** düğmesi üzerinde "Evet" seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="226ac-109">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="226ac-110">İşlem yapılacak yerleşimlerle ilgili olarak maliyet denetimi satırlarının ne kadar ayrıntılı olmasını istediğinizi belirtmek için **Düzey** alanını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="226ac-110">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="226ac-111">Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim yapınız varsa, işlem yapılacak yerleşim için tüm varlık arızası maliyet denetimi satırları üst düzeyde gösterilir ve dolayısıyla bir satırdaki saatler, alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="226ac-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="226ac-112">**Düzey** alanına "0" sayısını girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeylerinde bulunan tüm varlık arıza maliyet denetimi satırlarını gösteren ayrıntılı bir sonuç görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="226ac-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault cost control lines on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="226ac-113">Aramayı sınırlandırmak istiyorsanız, Hızlı Sekme **dahil edilecek kayıtlar** üzerinde belirli kıymetleri, arıza tarihlerini, arıza nedenlerini ve arızaları seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="226ac-113">If you want to limit the search, you can select specific assets, fault dates, and fault causes on the **Records to include** FastTab.</span></span>

7. <span data-ttu-id="226ac-114">Hesaplamayı başlatmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="226ac-114">Click **OK** to start the calculation.</span></span>

8. <span data-ttu-id="226ac-115">**Gruplandırma ölçütü** düğmelerine tıklayarak hesaplamanın gerekli ayrıntı düzeyini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="226ac-115">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="226ac-116">Seçilen **Gruplandırma ölçütü** düğmeleri vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="226ac-116">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="226ac-117">Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="226ac-117">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="226ac-118">Örnek</span><span class="sxs-lookup"><span data-stu-id="226ac-118">Example</span></span>

<span data-ttu-id="226ac-119">Bu örnekte, varlık arıza maliyeti denetim hesaplaması gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="226ac-119">This example shows an asset fault cost control calculation.</span></span>

- <span data-ttu-id="226ac-120">**Orijinal bütçe** alanı, bütçe maliyetlerini iş emri tahmininden gösterir.</span><span class="sxs-lookup"><span data-stu-id="226ac-120">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="226ac-121">**Fiili maliyet** alanı, iş emirlerinde deftere nakledilen maliyetleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="226ac-121">The **Actual cost** field shows posted costs on work orders.</span></span> 
- <span data-ttu-id="226ac-122">**Taahhüt edilen maliyet** alanı, şirketinizin iş siparişleri ile ilgili olarak taahhüt edildiği toplam maliyet miktarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="226ac-122">The **Committed cost** field shows total costs that your company is committed to in relation to work orders.</span></span>

    ![Şekil 1](media/05-controlling-and-reporting.png)

<span data-ttu-id="226ac-124">Arızaları ayarlama hakkında bilgi için [Arıza yönetimi](../setup-for-work-orders/fault-management.md) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="226ac-124">For information about how to set up faults, see the [Fault management](../setup-for-work-orders/fault-management.md) topic.</span></span>

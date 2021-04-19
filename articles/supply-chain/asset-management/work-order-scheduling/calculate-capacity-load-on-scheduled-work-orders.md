---
title: Planlanan iş emirlerinde kapasite yükünü hesaplama
description: Bu konu, Varlık Yönetiminde, planlanan iş emirleriyle ilgili kapasite yükünün nasıl hesaplanacağını açıklamaktadır.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 09e0fc17a288a278b7b1feaba8c7b73425aa2d52
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808172"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a><span data-ttu-id="bd484-103">Planlanan iş emirlerinde kapasite yükünü hesaplama</span><span class="sxs-lookup"><span data-stu-id="bd484-103">Calculate capacity load on scheduled work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="bd484-104">Belirli bir dönem için kaynakların iş yükünün genel görünümünü almak için planlanan iş emirlerindeki kapasite yükünü hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bd484-104">You can calculate capacity load on scheduled work orders to get an overview of the work load on resources for a specific period.</span></span> <span data-ttu-id="bd484-105">Hesaplamalar aşağıdaki kaynaklar için yapılabilir: Bakım görevlileri, çalışan grupları, araçlar ve varlıklar.</span><span class="sxs-lookup"><span data-stu-id="bd484-105">Calculations can be made for the following resources: Maintenance workers, worker groups, tools, and assets.</span></span>

1. <span data-ttu-id="bd484-106">**Varlık yönetimi** > **Sorgular** > **Plan** > **Kapasite yükü**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bd484-106">Click **Asset management** > **Inquiries** > **Schedule** > **Capacity load**.</span></span>

2. <span data-ttu-id="bd484-107">**Kapasite yükünü hesapla** iletişim kutusu > **Göster** alanında hesaplamak istediğiniz yük türünü seçin: **Kapasite**, **Ayrılmış** veya **Kalan**.</span><span class="sxs-lookup"><span data-stu-id="bd484-107">In the **Calculate capacity load** dialog > **Show** field, select which load type you want to calculate: **Capacity**, **Reserved**, or **Remainder**.</span></span>

3. <span data-ttu-id="bd484-108">Sıfır içeren sonuçları göstermek istemiyorsanız, **Sıfırı atla** düğmesi üzerinde **Evet** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="bd484-108">Select **Yes** on the **Skip zero** toggle button if you do not want to show results containing zero.</span></span>

4. <span data-ttu-id="bd484-109">İlgili kaydırma düğmesinde **Evet**'i seçerek kapasite yükünü hesaplamak istediğiniz kaynak türlerini seçin: **Çalışan**, **Bakım görevlisi grubu**, **Araç** ve **Varlık**.</span><span class="sxs-lookup"><span data-stu-id="bd484-109">Select the resource types for which you want to calculate capacity load by selecting **Yes** on the relevant toggle buttons: **Worker**, **Maintenance worker group**, **Tool**, and **Asset**.</span></span>

5. <span data-ttu-id="bd484-110">**Başlangıç tarihi** alanında otomatik hesaplama için başlangıç tarihini seçin.</span><span class="sxs-lookup"><span data-stu-id="bd484-110">Select the start date for the calculation in the **From date** field.</span></span>

6. <span data-ttu-id="bd484-111">**Aralık türü** alanında, hesaplama aralığını seçin: **Gün**, **Hafta**, **Ay** veya **Üç aylık dönem**.</span><span class="sxs-lookup"><span data-stu-id="bd484-111">In the **Interval type** field, select the interval for the calculation: **Day**, **Week**, **Month**, or **Quarter**.</span></span>

7. <span data-ttu-id="bd484-112">**Dönem sıklığı** alanında, hesaplamak istediğiniz aralık sayısını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="bd484-112">In the **Period frequency** field, insert the number of intervals you want to calculate.</span></span> <span data-ttu-id="bd484-113">Örneğin, aralık türü olarak **Gün** seçtiyseniz ve bu alana "5" sayısını eklerseniz, başlangıç tarihinden itibaren beş gün için bir hesaplama yapılır.</span><span class="sxs-lookup"><span data-stu-id="bd484-113">For example, if you have selected **Day** as the interval type, and you enter the number "5" in this field, a calculation of five days from the start date will be made.</span></span>

8. <span data-ttu-id="bd484-114">Hesaplamayı başlatmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bd484-114">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="bd484-115">Aşağıdaki şekil, **Ayrılmış** yük türü için üç haftayı kapsayan bir hesaplamanın sonucunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd484-115">The figure below shows the result of a calculation covering three weeks for the load type **Reserved**.</span></span>

![Şekil 1](media/08-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="bd484-117">Hesaplamalarınız için **Kapasite** veya **Kalan** yük türlerini seçerseniz, seçili dönemde kaynaklar için rezervasyon yoksa aynı sonuç görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="bd484-117">If you select the load types **Capacity** or **Remainder** for your calculation, the same result will be displayed if no reservations have been made for the resources in the selected period.</span></span>

<span data-ttu-id="bd484-118">Bakım zamanlaması satırlarındaki ve zamanlanmamış iş emirlerindeki kapasite yükünün nasıl hesaplanacağı hakkında bilgi için bkz. [Kapasite yükünü hesaplama](../capacity-planning/calculate-capacity-load.md).</span><span class="sxs-lookup"><span data-stu-id="bd484-118">For information about how to calculate capacity load on maintenance schedule lines and not scheduled work orders, refer to [Calculate capacity load](../capacity-planning/calculate-capacity-load.md).</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
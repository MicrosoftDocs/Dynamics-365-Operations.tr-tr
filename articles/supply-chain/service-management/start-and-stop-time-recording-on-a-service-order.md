---
title: Servis siparişinde zaman kaydını başlatma ve durdurma
description: Servis siparişinde zaman kaydını başlatın ve durdurun.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dcec3cfde34959de73132c8d764df25fb676d140
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242361"
---
# <a name="start-and-stop-time-recording-on-a-service-order"></a><span data-ttu-id="76024-103">Servis siparişinde zaman kaydını başlatma ve durdurma</span><span class="sxs-lookup"><span data-stu-id="76024-103">Start and stop time recording on a service order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="76024-104">Servis düzeyi sözleşmesi tanımlanan bir servis siparişi için zaman kaydını durdurmak ve başlatmak üzere bu yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="76024-104">Use this procedure to start and stop time recording for a service order for which a service level agreement is defined.</span></span>

## <a name="start-time-recording"></a><span data-ttu-id="76024-105">Zaman kaydını başlatma</span><span class="sxs-lookup"><span data-stu-id="76024-105">Start time recording</span></span>

1.  <span data-ttu-id="76024-106">**Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="76024-106">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="76024-107">**Servis siparişi** sekmesine tıklayın. **Eylem bölmesi**'nde, **Servis düzeyi sözleşmesi** grubunda **Başlat**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="76024-107">Click the **Service order** tab. On the **Action Pane**, in the **Service level agreement** group, click **Start**.</span></span>

3.  <span data-ttu-id="76024-108">Zaman kaydının başlatılacağı tarih ve saati girin.</span><span class="sxs-lookup"><span data-stu-id="76024-108">Enter the date and time that the time recording should be started.</span></span>

## <a name="stop-time-recording"></a><span data-ttu-id="76024-109">Zaman kaydetmeyi durdur</span><span class="sxs-lookup"><span data-stu-id="76024-109">Stop time recording</span></span>

1.  <span data-ttu-id="76024-110">**Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="76024-110">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="76024-111">**Servis siparişi** sekmesine tıklayın. **Eylem bölmesi**'nde, **Servis düzeyi sözleşmesi** grubunda **Durdur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="76024-111">Click the **Service order** tab. On the **Action Pane**, in the **Service level agreement** group, click **Stop**.</span></span>

3.  <span data-ttu-id="76024-112">Zaman kaydının durdurulacağı tarih ve saati girin.</span><span class="sxs-lookup"><span data-stu-id="76024-112">Enter the date and time that the time recording should be stopped.</span></span>

4.  <span data-ttu-id="76024-113">**Bir iptal nedeni ekle**'yi seçin ve zaman kaydını durdurma nedeni sağlamak için **Aşama neden kodu** listesinden bir neden kodu seçin.</span><span class="sxs-lookup"><span data-stu-id="76024-113">Select **Add a revocation reason**, and select a reason code in the **Stage reason code** list to provide a reason for stopping the time recording.</span></span>


> [!NOTE]
> <P><span data-ttu-id="76024-114"><STRONG>Servis yönetim parametreleri</STRONG> formunda <STRONG>Süre aşımıyla ilgili neden kodu</STRONG> seçilirse , zaman kaydını durdurmadan önce bir neden kodu sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="76024-114">If <STRONG>Reason code on exceeding time</STRONG> is selected in the <STRONG>Service management parameters</STRONG> form, you must provide a reason code before you can stop the time recording.</span></span></P>



## <a name="see-also"></a><span data-ttu-id="76024-115">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="76024-115">See also</span></span>

<span data-ttu-id="76024-116">[SDA zaman kaydını başlat (form)](https://technet.microsoft.com/library/hh242297\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="76024-116">[Start SLA time recording (form)](https://technet.microsoft.com/library/hh242297\(v=ax.60\))</span></span>

<span data-ttu-id="76024-117">[SDA zaman kaydını durdur (form)](https://technet.microsoft.com/library/hh242241\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="76024-117">[Stop SLA time recording (form)](https://technet.microsoft.com/library/hh242241\(v=ax.60\))</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
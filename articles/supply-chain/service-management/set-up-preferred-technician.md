---
title: Tercih edilen teklifi ayarlama
description: Servis anlaşması veya servis siparişi için bir tercih edilen teknisyen olarak herhangi bir çalışan seçebilirsiniz.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87b2554197c1963cdd7ba0871edb532661d10945
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256075"
---
# <a name="set-up-a-preferred-technician"></a><span data-ttu-id="66f4c-103">Tercih edilen teklifi ayarlama</span><span class="sxs-lookup"><span data-stu-id="66f4c-103">Set up a preferred technician</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="66f4c-104">Servis anlaşması veya servis siparişi için bir tercih edilen teknisyen olarak herhangi bir çalışan seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="66f4c-104">You can select any worker as a preferred technician for a service agreement or service order.</span></span> <span data-ttu-id="66f4c-105">Bununla birlikte, çalışanı uygun gönderme takımına dahil etmek iyi bir fikirdir; böylece çalışan **Gönderme panosu**'na dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="66f4c-105">However, it is a good idea to add the worker to the appropriate dispatch team so that the worker is included on the **Dispatch board**.</span></span>

## <a name="assign-employee-to-a-dispatch-team"></a><span data-ttu-id="66f4c-106">Çalışanı bir gönderilen ekibe atama</span><span class="sxs-lookup"><span data-stu-id="66f4c-106">Assign employee to a dispatch team</span></span>

1.  <span data-ttu-id="66f4c-107">**İnsan kaynakları** \> **Ortak** \> **Çalışanlar** \> **Çalışanlar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="66f4c-107">Click **Human resources** \> **Common** \> **Workers** \> **Workers**.</span></span> <span data-ttu-id="66f4c-108">Çalışan ayrıntıları sayfasını açmak için çalışana çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="66f4c-108">Double-click a worker to open the worker details page.</span></span> <span data-ttu-id="66f4c-109">**Eylem Bölmesi**'nde **Kurulum** \> **Gönderme takımı**'na tıklayarak **Gönderme çalışanları** formunu açın.</span><span class="sxs-lookup"><span data-stu-id="66f4c-109">On the **Action Pane**, click **Setup** \>**Dispatch team** to open the **Dispatch workers** form.</span></span>

2.  <span data-ttu-id="66f4c-110">**Gönderme takımı** alanında, çalışanın atanacağı takımı seçin.</span><span class="sxs-lookup"><span data-stu-id="66f4c-110">In the **Dispatch team** field, select the team to assign the worker to.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a><span data-ttu-id="66f4c-111">Tercih edilen teknisyeni bir servis anlaşmasına atama</span><span class="sxs-lookup"><span data-stu-id="66f4c-111">Assign a preferred technician to a service agreement</span></span>

1.  <span data-ttu-id="66f4c-112">**Servis yönetimi** \> **Ortak** \> **Servis sözleşmeleri** \> **Servis sözleşmeleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="66f4c-112">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="66f4c-113">Ayrıntılar formunu açmak için bir servis sözleşmesine çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="66f4c-113">Double-click a service agreement to open the details form.</span></span>

2.  <span data-ttu-id="66f4c-114">Uygun gönderme takımının bir üyesini servis anlaşması için tercih edilen teknisyen olarak atamak üzere **Genel** sekmesindeki **Tercih edilen teknisyen** listesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="66f4c-114">On the **General** tab, select the **Preferred technician** field, and then select a member of the appropriate dispatch team as the preferred technician for the service agreement.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-order"></a><span data-ttu-id="66f4c-115">Tercih edilen teknisyeni bir servis siparişine atama</span><span class="sxs-lookup"><span data-stu-id="66f4c-115">Assign a preferred technician to a service order</span></span>

1.  <span data-ttu-id="66f4c-116">**Servis yönetimi** \> **Periyodik** \> **Gönderme panosu**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="66f4c-116">Click **Service management** \> **Periodic** \> **Dispatch board**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="66f4c-117"><STRONG>Gönderme panosu</STRONG> formunda, görüntülemek istediğiniz gönderme faaliyetleri için bir tarih aralığı belirtin.</span><span class="sxs-lookup"><span data-stu-id="66f4c-117">In the <STRONG>Dispatch board</STRONG> form, specify a date range for dispatch activities to view.</span></span> <span data-ttu-id="66f4c-118">Ayrıca, kapatılmış faaliyetlerin görüntülenip görüntülenmeyeceğini ve gönderme faaliyet listesini üyesi olduğunuz veya denetleme yetkisine sahip olduğunuz ekiplerle sınırlandırıp sınırlandırmayacağınızı da belirtin.</span><span class="sxs-lookup"><span data-stu-id="66f4c-118">Also, specify whether to display closed activities and whether to limit the dispatch activity list to teams that you belong to or are authorized to monitor.</span></span> <span data-ttu-id="66f4c-119"><STRONG>Gönderme panosu</STRONG> formunu açmak için <STRONG>Tamam</STRONG>'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="66f4c-119">Click <STRONG>OK</STRONG> to open the <STRONG>Dispatch board</STRONG>.</span></span></P>



2.  <span data-ttu-id="66f4c-120">Değiştirilecek servis faaliyetinin satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="66f4c-120">Select the line of the service activity to modify.</span></span>

3.  <span data-ttu-id="66f4c-121">Uygun gönderme takımının bir üyesini servis çağrısı için tercih edilen teknisyen olarak atamak üzere **İlgili** sekmesindeki **Çalışan** listesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="66f4c-121">On the **Related** tab, use the **Worker** list to assign a member of the appropriate dispatch team as the preferred technician for the service call.</span></span>

## <a name="see-also"></a><span data-ttu-id="66f4c-122">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="66f4c-122">See also</span></span>

[<span data-ttu-id="66f4c-123">Servis sözleşmeleri geliştirme ve oluşturmaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="66f4c-123">Develop and establish service agreements overview</span></span>](service-agreements.md)

[<span data-ttu-id="66f4c-124">Servis siparişlerini el ile oluşturma</span><span class="sxs-lookup"><span data-stu-id="66f4c-124">Create service orders manually</span></span>](create-service-orders-manually.md)

<span data-ttu-id="66f4c-125">[Servis anlaşmaları (form)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="66f4c-125">[Service agreements (form)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))</span></span>
  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
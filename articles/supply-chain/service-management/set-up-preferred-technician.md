---
title: Tercih edilen teklifi ayarlama
description: "Servis anlaşması veya servis siparişi için bir tercih edilen teknisyen olarak herhangi bir çalışan seçebilirsiniz."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 390e436b63fdfe82e0b743e7f286cae3bb29be55
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---


# <a name="set-up-a-preferred-technician"></a><span data-ttu-id="69916-103">Tercih edilen teklifi ayarlama</span><span class="sxs-lookup"><span data-stu-id="69916-103">Set up a preferred technician</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="69916-104">Servis anlaşması veya servis siparişi için bir tercih edilen teknisyen olarak herhangi bir çalışan seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="69916-104">You can select any worker as a preferred technician for a service agreement or service order.</span></span> <span data-ttu-id="69916-105">Bununla birlikte, çalışanı uygun gönderme takımına dahil etmek iyi bir fikirdir; böylece çalışan **Gönderme panosu**'na dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="69916-105">However, it is a good idea to add the worker to the appropriate dispatch team so that the worker is included on the **Dispatch board**.</span></span>

## <a name="assign-employee-to-a-dispatch-team"></a><span data-ttu-id="69916-106">Çalışanı bir gönderilen ekibe atama</span><span class="sxs-lookup"><span data-stu-id="69916-106">Assign employee to a dispatch team</span></span>

1.  <span data-ttu-id="69916-107">**İnsan kaynakları** \> **Ortak** \> **Çalışanlar** \> **Çalışanlar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69916-107">Click **Human resources** \> **Common** \> **Workers** \> **Workers**.</span></span> <span data-ttu-id="69916-108">Çalışan ayrıntıları sayfasını açmak için çalışana çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69916-108">Double-click a worker to open the worker details page.</span></span> <span data-ttu-id="69916-109">**Eylem Bölmesi**'nde **Kurulum** \> **Gönderme takımı**'na tıklayarak **Gönderme çalışanları** formunu açın.</span><span class="sxs-lookup"><span data-stu-id="69916-109">On the **Action Pane**, click **Setup** \>**Dispatch team** to open the **Dispatch workers** form.</span></span>

2.  <span data-ttu-id="69916-110">**Gönderme takımı** alanında, çalışanın atanacağı takımı seçin.</span><span class="sxs-lookup"><span data-stu-id="69916-110">In the **Dispatch team** field, select the team to assign the worker to.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a><span data-ttu-id="69916-111">Tercih edilen teknisyeni bir servis anlaşmasına atama</span><span class="sxs-lookup"><span data-stu-id="69916-111">Assign a preferred technician to a service agreement</span></span>

1.  <span data-ttu-id="69916-112">**Servis yönetimi** \> **Ortak** \> **Servis sözleşmeleri** \> **Servis sözleşmeleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69916-112">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="69916-113">Ayrıntılar formunu açmak için bir servis sözleşmesine çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69916-113">Double-click a service agreement to open the details form.</span></span>

2.  <span data-ttu-id="69916-114">Uygun gönderme takımının bir üyesini servis anlaşması için tercih edilen teknisyen olarak atamak üzere **Genel** sekmesindeki **Tercih edilen teknisyen** listesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="69916-114">On the **General** tab, select the **Preferred technician** field, and then select a member of the appropriate dispatch team as the preferred technician for the service agreement.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-order"></a><span data-ttu-id="69916-115">Tercih edilen teknisyeni bir servis siparişine atama</span><span class="sxs-lookup"><span data-stu-id="69916-115">Assign a preferred technician to a service order</span></span>

1.  <span data-ttu-id="69916-116">**Servis yönetimi** \> **Periyodik** \> **Gönderme panosu**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69916-116">Click **Service management** \> **Periodic** \> **Dispatch board**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="69916-117"><STRONG>Gönderme panosu</STRONG> formunda, görüntülemek istediğiniz gönderme faaliyetleri için bir tarih aralığı belirtin.</span><span class="sxs-lookup"><span data-stu-id="69916-117">In the <STRONG>Dispatch board</STRONG> form, specify a date range for dispatch activities to view.</span></span> <span data-ttu-id="69916-118">Ayrıca, kapatılmış faaliyetlerin görüntülenip görüntülenmeyeceğini ve gönderme faaliyet listesini üyesi olduğunuz veya denetleme yetkisine sahip olduğunuz ekiplerle sınırlandırıp sınırlandırmayacağınızı da belirtin.</span><span class="sxs-lookup"><span data-stu-id="69916-118">Also, specify whether to display closed activities and whether to limit the dispatch activity list to teams that you belong to or are authorized to monitor.</span></span> <span data-ttu-id="69916-119"><STRONG>Gönderme panosu</STRONG> formunu açmak için <STRONG>Tamam</STRONG>'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="69916-119">Click <STRONG>OK</STRONG> to open the <STRONG>Dispatch board</STRONG>.</span></span></P>



2.  <span data-ttu-id="69916-120">Değiştirilecek servis faaliyetinin satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="69916-120">Select the line of the service activity to modify.</span></span>

3.  <span data-ttu-id="69916-121">Uygun gönderme takımının bir üyesini servis çağrısı için tercih edilen teknisyen olarak atamak üzere **İlgili** sekmesindeki **Çalışan** listesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="69916-121">On the **Related** tab, use the **Worker** list to assign a member of the appropriate dispatch team as the preferred technician for the service call.</span></span>

## <a name="see-also"></a><span data-ttu-id="69916-122">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="69916-122">See also</span></span>

[<span data-ttu-id="69916-123">Servis anlaşmaları</span><span class="sxs-lookup"><span data-stu-id="69916-123">Service agreements</span></span>](service-agreements.md)

[<span data-ttu-id="69916-124">Servis siparişlerini el ile oluşturma</span><span class="sxs-lookup"><span data-stu-id="69916-124">Create service orders manually</span></span>](create-service-orders-manually.md)

<span data-ttu-id="69916-125">[Servis anlaşmaları (form)](https://technet.microsoft.com/en-us/library/aa617823\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="69916-125">[Service agreements (form)](https://technet.microsoft.com/en-us/library/aa617823\(v=ax.60\))</span></span>
  



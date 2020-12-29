---
title: Servis siparişlerini iptal et
description: Bir servis siparişini veya servis siparişi satırını servis siparişinin kendisinden silebilir veya bir periyodik iş çalıştırarak birden çok servis siparişini iptal edebilirsiniz.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce3cb9ebc3536ba1b333a7bef6b5c679e09d7516
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439475"
---
# <a name="cancel-service-orders"></a><span data-ttu-id="58e02-103">Servis siparişlerini iptal et</span><span class="sxs-lookup"><span data-stu-id="58e02-103">Cancel service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="58e02-104">Bir servis siparişini veya servis siparişi satırını servis siparişinin kendisinden silebilir veya bir periyodik iş çalıştırarak birden çok servis siparişini iptal edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58e02-104">You can cancel a service order or service order line from the service order itself, or you can cancel multiple service orders by running a periodic job.</span></span>


> [!NOTE]
> <P><span data-ttu-id="58e02-105">Servis siparişinin aşaması iptal etmeye izin vermiyorsa, servis siparişinin madde gereksinimleri varsa veya servis siparişi zaten deftere nakledildiyse servis siparişi iptal edilemez.</span><span class="sxs-lookup"><span data-stu-id="58e02-105">Service orders cannot be canceled if the stage of the service order does not allow cancelation, if the service order has item requirements, or if the service order has already been posted.</span></span></P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a><span data-ttu-id="58e02-106">Servis siparişini Servis siparişleri formundan iptal etme</span><span class="sxs-lookup"><span data-stu-id="58e02-106">Cancel a service order in the Service orders form</span></span>

1.  <span data-ttu-id="58e02-107">**Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58e02-107">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="58e02-108">Servis siparişini seçin Eylem bölmesinde **Siparişi iptal et**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58e02-108">Select the service order, and on the Action Pane, click **Cancel order**.</span></span>

## <a name="cancel-a-service-order-line"></a><span data-ttu-id="58e02-109">Servis siparişi satırını iptal etme</span><span class="sxs-lookup"><span data-stu-id="58e02-109">Cancel a service order line</span></span>

1.  <span data-ttu-id="58e02-110">**Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58e02-110">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="58e02-111">İptal etmek istediğiniz satırı içeren servis siparişine çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58e02-111">Double-click the service order that contains the line you want to cancel.</span></span>

2.  <span data-ttu-id="58e02-112">İptal etmek istediğiniz servis siparişi satırını seçin ve **Sipariş satırı iptal et**'e tıklayarak satırın durumunu **İptal edildi** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="58e02-112">Select the service order line that you want to cancel, and then click **Cancel order line** to change the status of the line to **Canceled**.</span></span>


> [!TIP]
> <P><span data-ttu-id="58e02-113">Bir servis siparişi satırının iptalini geri almak ve durumu yeniden <STRONG>Oluşturuldu</STRONG> olarak değiştirmek için <STRONG>İptali geri al</STRONG>'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58e02-113">To reverse the cancellation of a service order line and change the status back to <STRONG>Created</STRONG>, click <STRONG>Revoke cancel</STRONG>.</span></span></P>


## <a name="cancel-multiple-service-orders"></a><span data-ttu-id="58e02-114">Birden çok servis siparişini iptal etme</span><span class="sxs-lookup"><span data-stu-id="58e02-114">Cancel multiple service orders</span></span>

1.  <span data-ttu-id="58e02-115">**Servis yönetimi** \> **Periyodik** \> **Servis siparişleri** \> **Servis siparişlerini iptal et**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58e02-115">Click **Service management** \> **Periodic** \> **Service orders** \> **Cancel service orders**.</span></span>

2.  <span data-ttu-id="58e02-116">**Seç** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58e02-116">Click the **Select** button.</span></span>

3.  <span data-ttu-id="58e02-117">**Sorgu** formunda, **Ölçüt** sütununda iptal etmek istediğiniz servis siparişlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="58e02-117">In the **Inquiry** form, in the **Criteria** column, select the service orders that you want to cancel.</span></span>

4.  <span data-ttu-id="58e02-118">**Sorgu** formunu kapatmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58e02-118">Click **OK** to close the **Inquiry** form.</span></span>

5.  <span data-ttu-id="58e02-119">İptal edilen servis siparişlerini gösteren bir bilgi günlüğü oluşturmak için **Bilgi Günlüğünü Göster** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="58e02-119">Select the **Show Infolog** check box to generate an Infolog that lists the canceled service orders.</span></span>

6.  <span data-ttu-id="58e02-120">Bir servis siparişinin **İptal edildi** durumunu tersine çevirmek istiyorsanız, **İptali geri al** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="58e02-120">Select the **Revoke cancel** check box if you want to reverse the **Canceled** status of a service order.</span></span>

7.  <span data-ttu-id="58e02-121">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="58e02-121">Click **OK**.</span></span>

<span data-ttu-id="58e02-122">Seçilen servis siparişleri iptal edilir veya **İptal edildi** ilerleme durumları tekrar **İşlemde**'ye döndürülür.</span><span class="sxs-lookup"><span data-stu-id="58e02-122">The selected service orders are either canceled or their progress status of **Canceled** has been reversed to **In process**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="58e02-123"><STRONG>İptali geri al</STRONG> onay kutusunu işaretlerseniz, <STRONG>İptal edildi</STRONG> ilerleme durumundaki servis siparişleri tersine çevrilir ve <STRONG>İşlemde</STRONG> ilerleme durumuna sahip servis siparişleri iptal edilmez.</span><span class="sxs-lookup"><span data-stu-id="58e02-123">If you select the <STRONG>Revoke cancel</STRONG> check box, service orders with a progress status of <STRONG>Canceled</STRONG> are reversed and service orders with a progress status of <STRONG>In process</STRONG> are not canceled.</span></span></P>


  



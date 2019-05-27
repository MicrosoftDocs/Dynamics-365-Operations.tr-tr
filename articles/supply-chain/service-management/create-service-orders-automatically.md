---
title: Servis siparişlerini otomatik olarak oluşturma
description: Bir servis sözleşmesi veya birden fazla servis sözleşmesi için servis siparişleri oluşturabilirsiniz.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee68190b117b974ff4131f5d2237d138cac1fda3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552288"
---
# <a name="create-service-orders-automatically"></a><span data-ttu-id="1e1ad-103">Servis siparişlerini otomatik olarak oluşturma</span><span class="sxs-lookup"><span data-stu-id="1e1ad-103">Create service orders automatically</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1e1ad-104">Bir servis sözleşmesi veya birden fazla servis sözleşmesi için servis siparişleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1e1ad-104">You can create service orders for one service agreement or for several service agreements.</span></span> <span data-ttu-id="1e1ad-105">Oluşturulduklarında, servis siparişlerinizi **Servis siparişleri** formunda görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1e1ad-105">When they are created, you can view your service orders in the **Service orders** form.</span></span>

<span data-ttu-id="1e1ad-106">Servis siparişleri servis anlaşmasının geçerli periyodu için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1e1ad-106">Service orders are created only for the valid period of the service agreement.</span></span> <span data-ttu-id="1e1ad-107">**Servis siparişleri oluştur** formunda belirttiğiniz aralık servis sözleşmesinin başlangıç tarihinden önce veya bitiş tarihinden sonraysa, servis siparişleri yalnızca aralığın servis sözleşmesinin süresi içinde yer alan parçası için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1e1ad-107">If the interval that you specify in the **Create service orders** form is before the starting date or after the ending date of the service agreement, service orders are created only for the part of the interval that is within the service agreement dates.</span></span>

<span data-ttu-id="1e1ad-108">Servis siparişlerini el ile veya servis sözleşmesi satırından otomatik olarak oluşturduğunuzda, satırda bir bitiş tarihi belirlemediyseniz, servis siparişi satırın başlangıç ve bitiş tarihleri tarafından tanımlanan zaman aralığı içinde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1e1ad-108">When you create service orders manually or automatically from the service agreement line, the service order must be in the time interval that is defined by the starting and ending dates for the line, unless you do not specify an ending date on the line.</span></span>

## <a name="create-service-orders-automatically-for-a-service-agreement"></a><span data-ttu-id="1e1ad-109">Servis anlaşması için otomatik olarak servis siparişleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="1e1ad-109">Create service orders automatically for a service agreement</span></span>

1.  <span data-ttu-id="1e1ad-110">**Servis yönetimi** \> **Ortak** \> **Servis sözleşmeleri** \> **Servis sözleşmeleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1e1ad-110">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="1e1ad-111">Bir servis anlaşması seçin.</span><span class="sxs-lookup"><span data-stu-id="1e1ad-111">Select a service agreement.</span></span>

3.  <span data-ttu-id="1e1ad-112">**Teslim et** sekmesine ve ardından **Planlanan servis siparişleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1e1ad-112">Click the **Deliver** tab, and then click **Planned service orders**.</span></span>

4.  <span data-ttu-id="1e1ad-113">Servis dönemini tanımlamak için tarihleri **Başlangıç tarihi** ve **Bitiş tarihi** alanlarında belirtin.</span><span class="sxs-lookup"><span data-stu-id="1e1ad-113">Specify dates in the **From date** and **To date** fields to define the service period.</span></span>

5.  <span data-ttu-id="1e1ad-114">Oluşturulan servis siparişleri listesini göstermek için **Bilgi Günlüğünü Göster** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1e1ad-114">Select the **Show Infolog** check box to display a list of the service orders that are created.</span></span>

6.  <span data-ttu-id="1e1ad-115">**Hareket türlerini dahil et** alan grubunda hareket türlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="1e1ad-115">Select transaction types in the **Include transaction types** field group.</span></span> <span data-ttu-id="1e1ad-116">Hareket türleri, servis anlaşmasında oluşturulan satırları temsil eder ve seçtiğiniz her hareket türü, servis anlaşması satırında belirttiğiniz servis aralığına bağlı olarak çeşitli servis siparişleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1e1ad-116">The transaction types represent the lines that are created in the service agreement, and each transaction type that you select generates several service orders, depending on the service interval that is specified on the service agreement line.</span></span>

7.  <span data-ttu-id="1e1ad-117">Sürekli bir servis siparişleri serisinde eksik olan servis siparişlerini oluşturmak için **Sürekli** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1e1ad-117">To create any service orders that are missing from continuous series of service orders, select the **Continuous** check box.</span></span>

8.  <span data-ttu-id="1e1ad-118">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1e1ad-118">Click **OK**.</span></span>

## <a name="create-service-orders-automatically-for-several-service-agreements"></a><span data-ttu-id="1e1ad-119">Servis anlaşması için otomatik olarak çeşitli servis siparişleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="1e1ad-119">Create service orders automatically for several service agreements</span></span>

1.  <span data-ttu-id="1e1ad-120">**Servis yönetimi** \> **Periyodik** \> **Servis siparişleri** \> **Servis siparişleri oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1e1ad-120">Click **Service management** \> **Periodic** \> **Service orders** \> **Create service orders**.</span></span>

2.  <span data-ttu-id="1e1ad-121">Servis siparişleri oluştururken kullanmak amacıyla ölçüt eklemek veya kaldırmak üzere seçim yapmak **Seç**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1e1ad-121">Click **Select** to make selections to add or remove criteria to use to create service orders.</span></span>

3.  <span data-ttu-id="1e1ad-122">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1e1ad-122">Click **OK**.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e1ad-123">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="1e1ad-123">See also</span></span>

[<span data-ttu-id="1e1ad-124">Servis emirleri</span><span class="sxs-lookup"><span data-stu-id="1e1ad-124">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="1e1ad-125">Servis siparişlerini otomatik oluşturma</span><span class="sxs-lookup"><span data-stu-id="1e1ad-125">Automatically creating service orders</span></span>](auto-create-service-orders.md)

  



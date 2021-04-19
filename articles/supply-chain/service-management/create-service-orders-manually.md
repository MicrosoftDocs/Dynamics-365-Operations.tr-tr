---
title: Servis siparişlerini el ile oluşturma
description: Servis siparişlerini, bir servis sözleşmesi kullanarak veya **Servis siparişleri** formunu kullanarak el ile oluşturabilirsiniz.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 486b4a0291ca527e647c9b5a41ff2e65a7820291
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817593"
---
# <a name="create-service-orders-manually"></a><span data-ttu-id="572ed-103">Servis siparişlerini el ile oluşturma</span><span class="sxs-lookup"><span data-stu-id="572ed-103">Create service orders manually</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="572ed-104">Servis siparişlerini, bir servis sözleşmesi kullanarak veya **Servis siparişleri** formunu kullanarak el ile oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="572ed-104">You can create service orders manually by using a service agreement or by using the **Service orders** form.</span></span> <span data-ttu-id="572ed-105">Aynı zamanda bir projeden servis siparişi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="572ed-105">You can also create a service order from a project.</span></span>

> [!TIP]
> <P><span data-ttu-id="572ed-106">Servis siparişleri oluşturmak için otomatik işlemleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="572ed-106">You can use automated processes to create service orders.</span></span> 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a><span data-ttu-id="572ed-107">Servis sözleşmesinden el ile servis siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="572ed-107">Create a service order manually from a service agreement</span></span>

1.  <span data-ttu-id="572ed-108">**Servis yönetimi** \> **Ortak** \> **Servis sözleşmeleri** \> **Servis sözleşmeleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="572ed-108">Select **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="572ed-109">Bir servis anlaşması seçin veya yeni bir servis anlaşması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="572ed-109">Select a service agreement or create a new service agreement.</span></span>

3.  <span data-ttu-id="572ed-110">**Teslim et** sekmesini seçin, **Oluştur** grubunda **Planlanan servis siparişleri**'ni seçerek **Servis siparişleri oluştur** formunu açın.</span><span class="sxs-lookup"><span data-stu-id="572ed-110">Select the **Deliver** tab and in the **Create** group select **Planned service orders** to open the **Create service orders** form.</span></span>

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a><span data-ttu-id="572ed-111">Servis siparişleri formunda el ile servis siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="572ed-111">Create a service order manually in the Service orders form</span></span>

1.  <span data-ttu-id="572ed-112">**Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="572ed-112">Select **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="572ed-113">Yeni servis siparişi oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="572ed-113">Select **New** to create a new service order.</span></span>

3.  <span data-ttu-id="572ed-114">Servis siparişi için servis siparişi satırları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="572ed-114">Create service order lines for the service order.</span></span>

> [!NOTE]
> <P><span data-ttu-id="572ed-115"><STRONG>Servis yönetimi parametreleri</STRONG> formundaki <STRONG>Servis sözleşmesi olmadan izin ver</STRONG> onay kutusu işaretlenirse servis siparişini servis sözleşmesine iliştirmeden servis siparişi satırlarından hareketleri nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="572ed-115">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="572ed-116">Onay kutusu işaretlenmezse, servis siparişi satırlarını nakletmeden önce projeye el ile oluşturulan servis siparişini iliştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="572ed-116">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-a-project"></a><span data-ttu-id="572ed-117">Projeden bir servis siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="572ed-117">Create a service order from a project</span></span>

1.  <span data-ttu-id="572ed-118">**Proje yönetimi ve muhasebe** \> **Genel** \> **Projeler** \> **Tüm projeler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="572ed-118">Go to **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="572ed-119">**Projeler** formunda, **Eylem Bölmesi**'nde **Yönet** sekmesini ve \> **Servis** \> **Servis siparişleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="572ed-119">In the **Projects** form, on the **Action Pane**, select the **Manage** tab \> select **Service** \> **Service orders**.</span></span>

3.  <span data-ttu-id="572ed-120">**Servis siparişleri** formunda önceki el ile servis siparişi oluşturma yordamını takip edin.</span><span class="sxs-lookup"><span data-stu-id="572ed-120">Follow the previous procedure to create a service order manually in the **Service orders** form.</span></span> <span data-ttu-id="572ed-121">**Proje kodu** alanı proje referansını gösterir.</span><span class="sxs-lookup"><span data-stu-id="572ed-121">The **Project ID** field displays the project reference.</span></span>

> [!NOTE]
> <P><span data-ttu-id="572ed-122"><STRONG>Servis yönetimi parametreleri</STRONG> formundaki <STRONG>Servis sözleşmesi olmadan izin ver</STRONG> onay kutusu işaretlenirse servis siparişini servis sözleşmesine iliştirmeden servis siparişi satırlarından hareketleri nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="572ed-122">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="572ed-123">Onay kutusu işaretlenmezse, servis siparişi satırlarını nakletmeden önce projeye el ile oluşturulan servis siparişini iliştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="572ed-123">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-the-sales-order-form"></a><span data-ttu-id="572ed-124">Satış siparişi formundan servis siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="572ed-124">Create a service order from the Sales order form</span></span>

<span data-ttu-id="572ed-125">**Satış siparişine dayalı yeni bir servis siparişi oluştur** sihirbazını kullanarak **satış siparişleri** formundan bir servis siparişi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="572ed-125">You can create a service order from the **Sales orders** form by using the **Create a new service order based on the sales order** wizard.</span></span>

1.  <span data-ttu-id="572ed-126">**Satış ve pazarlama** \> **Yaygın** \> **Satış siparişleri** \> **Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="572ed-126">Go to **Sales and marketing** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="572ed-127">İlgili satış siparişini açın.</span><span class="sxs-lookup"><span data-stu-id="572ed-127">Open the relevant sales order.</span></span>

3.  <span data-ttu-id="572ed-128">**Satış siparişi** sekmesinde, **Servis siparişi**'ni seçerek **Satış siparişine dayalı yeni bir servis siparişi oluştur** sihirbazını başlatın.</span><span class="sxs-lookup"><span data-stu-id="572ed-128">On the **Sales order** tab, select **Service order** to start the **Create a new service order based on the sales order** wizard.</span></span>

4.  <span data-ttu-id="572ed-129">**İleri \>** seçeneğini belirleyin, **Servis siparişi için sözleşme seç** sayfasında aşağıdaki adımları tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="572ed-129">Select **Next \>**, and then complete the following steps on the **Select agreement for service order** page:</span></span>
    
      - <span data-ttu-id="572ed-130">Yeni servis siparişinin ilişkilendirilmesi gereken servis sözleşmesini seçmek için **Servis sözleşmesi** alanını işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="572ed-130">Use the **Service agreement** field to select the service agreement with which the new service order should be associated.</span></span>
    
      - <span data-ttu-id="572ed-131">İsteğe bağlı: Bu servis siparişini belirli bir projeyle ilişkilendirmek için **Proje Kodu** alanını kullanın.</span><span class="sxs-lookup"><span data-stu-id="572ed-131">Optional: Use the **Project ID** field to associate this service order with a particular project.</span></span>

5.  <span data-ttu-id="572ed-132">**İleri \>** seçeneğini belirleyin, **Servis siparişi oluştur** sayfasında aşağıdaki adımları tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="572ed-132">Select **Next \>**, and then complete the following steps on the **Create service order** page:</span></span>
    
      - <span data-ttu-id="572ed-133">**Tercih edilen servis zamanı** alanında servis çağrısının başlayacağı tarih ve saati girin.</span><span class="sxs-lookup"><span data-stu-id="572ed-133">Enter a date and time for the service call to begin in the **Preferred service time** field.</span></span>
    
      - <span data-ttu-id="572ed-134">İsteğe bağlı: **Açıklama** alanındaki metni değiştirin.</span><span class="sxs-lookup"><span data-stu-id="572ed-134">Optional: Modify the text in the **Description** field.</span></span> <span data-ttu-id="572ed-135">Varsayılan olarak bu alan önceki sayfada seçtiğiniz servis sözleşmesinin açıklamasını içerir.</span><span class="sxs-lookup"><span data-stu-id="572ed-135">By default, this field contains the description of the service agreement that you selected on the previous page.</span></span>
    
      - <span data-ttu-id="572ed-136">**Sorumlu** alanında, sözleşmeden sorumlu olan çalışanın kimliğini ve ne olduğunu biliyorsanız, müşterinin servis çağrısı için tercih ettiği teknisyenin kimliğini girin.</span><span class="sxs-lookup"><span data-stu-id="572ed-136">In the **Responsible** field, select the ID of the employee who is responsible for the agreement, and if you know what it is, enter the ID of the customer's preferred technician for the service call.</span></span>
    
      - <span data-ttu-id="572ed-137">**İlgili Kişi Kimliği** alanında müşterinin şirketinde bu servis siparişiyle ilgili olarak sizinle bağlantı kurması gereken kişiyi seçin.</span><span class="sxs-lookup"><span data-stu-id="572ed-137">In the **Contact ID** field, select the person in the customer's company who should be contacted regarding this service order.</span></span>

6.  <span data-ttu-id="572ed-138">**İleri \>**'yi ve ardından **Bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="572ed-138">Select **Next \>**, and then select **Finish**.</span></span>


## <a name="see-also"></a><span data-ttu-id="572ed-139">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="572ed-139">See also</span></span>

[<span data-ttu-id="572ed-140">Servis siparişleri</span><span class="sxs-lookup"><span data-stu-id="572ed-140">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="572ed-141">Servis siparişlerini otomatik olarak oluşturma</span><span class="sxs-lookup"><span data-stu-id="572ed-141">Create service orders automatically</span></span>](create-service-orders-automatically.md)

<span data-ttu-id="572ed-142">[Servis siparişleri oluştur (sınıf formu)](https://technet.microsoft.com/library/aa553901\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="572ed-142">[Create service orders (class form)](https://technet.microsoft.com/library/aa553901\(v=ax.60\))</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
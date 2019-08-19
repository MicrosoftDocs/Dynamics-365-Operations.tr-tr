---
title: İade edilen maddelerin girişini kaydetme
description: İade edilen maddelerin girişini Varış özeti formunu veya Kayıt formunu kullanarak kaydedebilirsiniz.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08a40d7e95ffb17a096f759b332e77aeaf96ffd6
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742275"
---
# <a name="register-the-receipt-of-returned-items"></a><span data-ttu-id="72efc-103">İade edilen maddelerin girişini kaydetme</span><span class="sxs-lookup"><span data-stu-id="72efc-103">Register the receipt of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="72efc-104">İade edilen maddelerin girişini kaydetmek için iki yöntem bulunur.</span><span class="sxs-lookup"><span data-stu-id="72efc-104">There are two methods for registering the receipt of returned items.</span></span> <span data-ttu-id="72efc-105">İlk yöntem **Varış özeti** formunu kullanan ambar alma sürecidir.</span><span class="sxs-lookup"><span data-stu-id="72efc-105">The first method is a warehouse receiving process that uses the **Arrival overview** form.</span></span> <span data-ttu-id="72efc-106">İkinci yöntem **Kayıt** formunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="72efc-106">The second uses the **Registration** form.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a><span data-ttu-id="72efc-107">İade edilen maddelerin girişini Varış özeti formuna kaydetme</span><span class="sxs-lookup"><span data-stu-id="72efc-107">Register the receipt of returned items in the Arrival overview form</span></span>

<span data-ttu-id="72efc-108">**Varış özeti** formunu bir iade sevkiyatını İade Malzemeler İzni (RMA) numarasına göre tanımlamak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72efc-108">You can use the **Arrival overview** form to identify a return shipment by its Return Material Authorization (RMA) number.</span></span> <span data-ttu-id="72efc-109">**Kurulum** sekmesinde bir günlük adı tanımlandıysa ve **Varış özeti** formunda seçili satırlara karşılık gelen günlük satırları varsa **Varışı başlat**'a tıkladığınızda yeni bir günlük başlığı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="72efc-109">If a journal name is defined on the **Setup** tab, and journal lines that correspond to the lines selected on the **Arrival overview** form exist, a new journal header is created when you click **Start arrival**.</span></span>

1.  <span data-ttu-id="72efc-110">**Stok yönetimi** \> **Periyodik** \> **Varışa genel bakış**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72efc-110">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="72efc-111">**Kurulum adı** alanında, **İade siparişi**'ni seçin ve ardından **Güncelleştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72efc-111">In the **Setup name** field, select **Return order**, and then click **Update**.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="72efc-112">Arama sonuçlarını daraltmak için <STRONG>Aralık</STRONG> alanlarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72efc-112">You can use the <STRONG>Range</STRONG> fields to narrow the search results.</span></span> <span data-ttu-id="72efc-113">Kesin bir sonuç için <STRONG>RMA numarası</STRONG> alanına RMA numarasını yazabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72efc-113">You can type or select the RMA number in the <STRONG>RMA number</STRONG> field for an exact result.</span></span> <span data-ttu-id="72efc-114">Hangi gelen varışların görüntüleneceğini sınırlandıran filtre kümesini tanımlamak ve kaydetmek için <STRONG>Kurulum</STRONG> sekmesine tıklayın. Kullanılabilir filtreler türleri, ambarları ve noktaları içerir.</span><span class="sxs-lookup"><span data-stu-id="72efc-114">To define and save a set of filters that will restrict which incoming arrivals are displayed, click the <STRONG>Setup</STRONG> tab. The available filters include types, warehouses, and docks.</span></span></P>

    

    > [!WARNING]
    > <P><span data-ttu-id="72efc-115">İade siparişleri <STRONG>Varış özeti</STRONG> formundaki diğer varış türleriyle karıştırılamaz.</span><span class="sxs-lookup"><span data-stu-id="72efc-115">Return orders cannot be mixed with other arrival types in the <STRONG>Arrival overview</STRONG> form.</span></span> <span data-ttu-id="72efc-116">Bu nedenle, referans daima satış siparişi olacaktır ancak günlük başlığında satış siparişi kodu belirtilmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="72efc-116">Therefore, the reference will always be sales order, but no sales order ID will be specified on the journal header.</span></span></P>



3.  <span data-ttu-id="72efc-117">**Girişler** ızgarasında iade edilen maddeyle eşleşen satırı bulun ve sonra **Varış için seç** sütununda onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="72efc-117">In the **Receipts** grid, locate the line that matches the item being returned, and then select the check box in the **Select for arrival** column.</span></span>

4.  <span data-ttu-id="72efc-118">Örneğin orijinal siparişten iade sevkiyatına dahil edilmeyen maddeler gibi belirli satırları iade girişinin dışında tutmak için formun alt bölümündeki **Satırlar** tablosunda bulunan ilgili **Varış için seç** onay kutularını temizleyin.</span><span class="sxs-lookup"><span data-stu-id="72efc-118">To exclude certain lines from the return receipt, such as items from the original order that were not included in the return shipment, clear the associated **Select for arrival** check boxes in the **Lines** table in the lower part of the form.</span></span>

5.  <span data-ttu-id="72efc-119">Bir varış günlüğü oluşturmak için **Varışı başlat** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72efc-119">Click the **Start arrival** button to create an arrival journal.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="72efc-120">Birden fazla iade siparişi seçebilir ve tümünü tek bir varış işlemine dahil edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72efc-120">You can select multiple return orders and include them all in a single arrival process.</span></span> <span data-ttu-id="72efc-121">Her iade siparişi satırı karşılık gelen varış günlüğü satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="72efc-121">Each return order line will be copied into a corresponding item arrival journal line.</span></span></P>

    

    > [!NOTE]
    > <P><span data-ttu-id="72efc-122"><STRONG>Madde varışı</STRONG> formunu kullanarak bir varış günlüğünü el ile de oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72efc-122">You can also manually create an arrival journal by using the <STRONG>Item arrival</STRONG> form.</span></span> 



6.  <span data-ttu-id="72efc-123">**Stok Yönetimi** \> **Günlükler** \> **Madde varışı** \> **Madde varışı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="72efc-123">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>

7.  <span data-ttu-id="72efc-124">Yeni oluşturduğunuz varış günlüğünü seçin ve **Satırlar**'ı tıklayarak **Günlük satırları, yerleşimler** formunu açın.</span><span class="sxs-lookup"><span data-stu-id="72efc-124">Select the arrival journal that you just created and then click **Lines** to open the **Journal lines, locations** form.</span></span>

8.  <span data-ttu-id="72efc-125">**Genel** sekmesinde **Miktar** alanında sayıyı düzeltin ve gerekirse **Elden çıkarma kodu** alanında bir elden çıkarma kodu atayın.</span><span class="sxs-lookup"><span data-stu-id="72efc-125">On the **General** tab, adjust the number in the **Quantity** field, if it is required, and then assign a disposition code in the **Disposition code** field.</span></span>
    
    <span data-ttu-id="72efc-126">Alternatif olarak, İade edilen maddelerin bir karantina emri bağlamında denetleme işlemine gönderilmesini sağlamak için **Karantina yönetimi** onay kutusunu seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72efc-126">Alternatively, you can select the **Quarantine management** check box to have the returned items sent through an inspection process in the context of a quarantine order.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="72efc-127">İade edilen maddeleri karantina yoluyla gönderirseniz, bir elden çıkarma kodu belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="72efc-127">If you send the returned items through quarantine, you cannot specify a disposition code.</span></span></P>



9.  <span data-ttu-id="72efc-128">**Doğrula** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72efc-128">Click the **Validate** button.</span></span>

10. <span data-ttu-id="72efc-129">Doğrulama sürecinde hata yoksa **Deftere naklet** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72efc-129">If there are no errors in the validation process, click **Post**.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a><span data-ttu-id="72efc-130">İade edilen maddelerin girişini Kayıt formuna kaydetme</span><span class="sxs-lookup"><span data-stu-id="72efc-130">Register the receipt of returned items in the Registration form</span></span>

<span data-ttu-id="72efc-131">**Varış özeti** formunu kullanmaya alternatif olarak iade edilen maddelerin varışını kaydetmek için **Kayıt** formunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72efc-131">As an alternative to using the **Arrival overview** form, you can use the **Registration** form to register the arrival of returned items.</span></span>

1.  <span data-ttu-id="72efc-132">**Satış ve pazarlama** \> **Genel** \> **İade siparişleri** \> **Tüm iade siparişleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72efc-132">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span> <span data-ttu-id="72efc-133">Yeni bir iade siparişi oluşturun veya iade siparişini listeden açın.</span><span class="sxs-lookup"><span data-stu-id="72efc-133">Create a new return order or open the return order from the list.</span></span> <span data-ttu-id="72efc-134">**Satırlar** hızlı sekmesinde iade siparişi satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="72efc-134">On the **Lines** FastTab, select the return order line.</span></span> <span data-ttu-id="72efc-135">**Satırı güncelleştir**'e ve ardından **Kayıt**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72efc-135">Click **Update line**, and then click **Registration**.</span></span>

2.  <span data-ttu-id="72efc-136">**Elden çıkarma kodu** alanında bir elden çıkarma kodu atayın ve **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72efc-136">Assign a disposition code in the **Disposition code** field, and then click **OK**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="72efc-137"><STRONG>Kayıt</STRONG> formu kullanıldığında maddeyi bir karantina emri olarak denetime göndermek mümkün değildir.</span><span class="sxs-lookup"><span data-stu-id="72efc-137">It is not possible to send the item for inspection as a quarantine order using the <STRONG>Registration</STRONG> form.</span></span></P>



3.  <span data-ttu-id="72efc-138">**Hareketler** ızgarasında, kaydedilecek hareketi seçin.</span><span class="sxs-lookup"><span data-stu-id="72efc-138">In the **Transactions** grid, select the transaction to be registered.</span></span>

4.  <span data-ttu-id="72efc-139">**Şimdi kaydet** ızgarasında **Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72efc-139">In the **Register now** grid, click **Add**.</span></span> <span data-ttu-id="72efc-140">Tüm iade edilen maddeler **Şimdi kaydet** ızgarasında görünene kadar önceki iki adımı tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="72efc-140">Repeat the previous two steps until all of the returned items appear in the **Register now** grid.</span></span>

5.  <span data-ttu-id="72efc-141">**Tümünü deftere naklet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="72efc-141">Click **Post all**.</span></span>

## <a name="see-also"></a><span data-ttu-id="72efc-142">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="72efc-142">See also</span></span>

<span data-ttu-id="72efc-143">[Varış özeti (form)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="72efc-143">[Arrival overview (form)](https://technet.microsoft.com/library/hh227654\(v=ax.60\))</span></span>

  



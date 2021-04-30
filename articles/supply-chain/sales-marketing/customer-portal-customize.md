---
title: Müşteri portalını özelleştirme ve kullanma
description: Bu konu, müşteri portalının sisteminize eklendikten sonra nasıl özelleştirileceğini açıklamaktadır.
author: dasani-madipalli
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6d4cc52a90b25406080032c7a98caa59f53ce188
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909012"
---
# <a name="customize-and-use-the-customer-portal"></a><span data-ttu-id="b621d-103">Müşteri portalını özelleştirme ve kullanma</span><span class="sxs-lookup"><span data-stu-id="b621d-103">Customize and use the Customer portal</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b621d-104">Bu konuda, kutudan bulunmayan farklı sayfalar müşteri portalında açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="b621d-104">This topic describes the different pages that available in the Customer portal out of the box.</span></span> <span data-ttu-id="b621d-105">Sayfaların ne yaptığını ve bunları nasıl özelleştirebileceğinizi açıklar.</span><span class="sxs-lookup"><span data-stu-id="b621d-105">It explains what the pages do and how you can customize them.</span></span>

<span data-ttu-id="b621d-106">Müşteri Portalı birkaç Web sayfası ve kutudan birinin dışında bir eylem sunar.</span><span class="sxs-lookup"><span data-stu-id="b621d-106">The Customer portal offers a few webpages and actions out of the box.</span></span> <span data-ttu-id="b621d-107">Aşağıdaki site haritası bu Web sayfalarının ve eylemlerin genel görünümünü ve eylemleri gerçekleştirebilecek rolleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="b621d-107">The following site map provides an overview of those webpages and actions, and the roles that can perform the actions.</span></span>

<span data-ttu-id="b621d-108">![Müşteri Portalı site haritası](media/customer-portal-site-map.png "Müşteri Portalı site haritası")</span><span class="sxs-lookup"><span data-stu-id="b621d-108">![Customer portal site map](media/customer-portal-site-map.png "Customer portal site map")</span></span>

## <a name="typical-customizations"></a><span data-ttu-id="b621d-109">Normal özelleştirmeler</span><span class="sxs-lookup"><span data-stu-id="b621d-109">Typical customizations</span></span>

<span data-ttu-id="b621d-110">Aşağıdaki konular Power Apps portalların ve portalların nasıl özelleştirilebileceği hakkında temel bilgileri öğrenmenize yardımcı olur:</span><span class="sxs-lookup"><span data-stu-id="b621d-110">The following topics will help you learn the basics about Power Apps portals and how you can customize portals:</span></span>

- <span data-ttu-id="b621d-111">[Şablonlarla çalışma](/powerapps/maker/portals/work-with-templates) – Bu konuda, Power Apps portalların nasıl çalıştığı ve portallardaki basit özelleştirmelerin nasıl yapılacağı ile ilgili genel bir bakış sunulmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b621d-111">[Work with templates](/powerapps/maker/portals/work-with-templates) – This topic provides a general overview of how Power Apps portals works and how you can do simple customizations of portals.</span></span>
- <span data-ttu-id="b621d-112">[Portal içeriğini yönetme](/dynamics365/portals/manage-portal-content) – Bu konu, portalınızda yüzeyiniz içeriği nasıl yöneteceğinizi ve özelleştirebileceğinizi açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="b621d-112">[Manage portal content](/dynamics365/portals/manage-portal-content) – This topic explains how you can manage and customize the content that you surface in your portal.</span></span>
- <span data-ttu-id="b621d-113">[CSS Düzenle](/powerapps/maker/portals/edit-css) – Bu konu, portalınızdaki Kullanıcı arabirimi (UI) için daha karmaşık özelleştirmeler yapmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="b621d-113">[Edit CSS](/powerapps/maker/portals/edit-css) – This topic helps you make more complex customizations to the user interface (UI) of your portal.</span></span>
- <span data-ttu-id="b621d-114">[Portalınız için bir tema oluşturun](/dynamics365/portals/create-theme) – Bu konu, portalınız için bir UI teması oluşturmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="b621d-114">[Create a theme for your portal](/dynamics365/portals/create-theme) – This topic helps you create a UI theme for your portal.</span></span>
- <span data-ttu-id="b621d-115">[Portal içeriğini kolayca oluşturma ve gösterme](/dynamics365/portals/create-expose-portal-content): Bu konu, portalınız için kullandığınız temel verileri ve tabloları yönetmenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="b621d-115">[Create and expose portal content easily](/dynamics365/portals/create-expose-portal-content) – This topic helps you manage the underlying data and tables that you use for your portal.</span></span>
- <span data-ttu-id="b621d-116">[Bir ilgili kişiyi portalda kullanılmak üzere konfigüre etme](/powerapps/maker/portals/configure/configure-contacts) – Bu konu Kullanıcı rollerinin nasıl oluşturulacağını ve özelleştirileceğini ve güvenlik ve kimlik doğrulamanın Power Apps portalda nasıl çalıştığını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="b621d-116">[Configure a contact for use on a portal](/powerapps/maker/portals/configure/configure-contacts) – This topic explains how to create and customize user roles, and how security and authentication work in Power Apps portals.</span></span>
- <span data-ttu-id="b621d-117">[Tablo formları ve portallardaki Web formları için notları yapılandırma](/powerapps/maker/portals/configure-notes): Bu konu, portala nasıl belge ve ek depolama alanı ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="b621d-117">[Configure notes for table forms and web forms on portals](/powerapps/maker/portals/configure-notes) – This topic explains how to add documents and additional storage to your portal.</span></span>
- <span data-ttu-id="b621d-118">[Portal Web sitesi için hata işleme](/powerapps/maker/portals/admin/view-portal-error-log) – Bu konu, portal hata günlüklerinin nasıl görüntüleneceğini ve bunları Microsoft Azure BLOB depolama hesabınızda nasıl depolayabileceğinizi açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="b621d-118">[Error handling for portal website](/powerapps/maker/portals/admin/view-portal-error-log) – This topic explains how to view portal error logs and store them in your Microsoft Azure Blob storage account.</span></span>

## <a name="customize-the-order-creation-process"></a><span data-ttu-id="b621d-119">Sipariş oluşturma işlemini Özelleştir</span><span class="sxs-lookup"><span data-stu-id="b621d-119">Customize the order creation process</span></span>

<span data-ttu-id="b621d-120">Bir kullanıcı müşteri portalını kullanarak sipariş gönderdiğinde, sipariş ilgili Dynamics 365 Supply Chain Management ortamla otomatik olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="b621d-120">When a user submits an order by using the Customer portal, the order is automatically synced to the corresponding Dynamics 365 Supply Chain Management environment.</span></span> <span data-ttu-id="b621d-121">Kullanıcı harici bir müşteri olduğu için, gerekli bazı bilgiler kasıtlı olarak kendi kendine gizlenir.</span><span class="sxs-lookup"><span data-stu-id="b621d-121">Because the user is an external customer, some required information is intentionally hidden from him or her.</span></span> <span data-ttu-id="b621d-122">Bu bilgiler form gönderildiğinde otomatik olarak doldurulacaktır.</span><span class="sxs-lookup"><span data-stu-id="b621d-122">This information will automatically be filled in when the form is submitted.</span></span>

<span data-ttu-id="b621d-123">Bu bölüm, ilgili kişilerin hataları önlemek amacıyla nasıl ayarlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b621d-123">This section shows how you should set up contacts to avoid errors.</span></span> <span data-ttu-id="b621d-124">Otomatik olarak ayarlanan alanları ve gerekiyorsa bu alanların değerini nasıl değiştirebileceğinizi açıklar.</span><span class="sxs-lookup"><span data-stu-id="b621d-124">It explains fields that are automatically set and how you can modify the value of those fields if you must.</span></span>

### <a name="the-out-of-box-order-creation-process"></a><span data-ttu-id="b621d-125">Kullanıma hazır sipariş oluşturma işlemi</span><span class="sxs-lookup"><span data-stu-id="b621d-125">The out-of-box order creation process</span></span>

<span data-ttu-id="b621d-126">Müşteri portalından sipariş gönderme standart adımları aşağıda verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b621d-126">Here are the standard steps for submitting an order from the Customer portal.</span></span>

1. <span data-ttu-id="b621d-127">Giriş sayfasında, **Sipariş Oluştur** Sihirbazını açmak için **sipariş oluştur** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="b621d-127">On the home page, select the **Create order** tile to open the **Create Order** wizard.</span></span>
1. <span data-ttu-id="b621d-128">**Sipariş bilgileri** sayfasında, aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b621d-128">On the **Order Information** page, set the following fields:</span></span>

    - <span data-ttu-id="b621d-129">**Talep edilen giriş tarihi** – teslimat tarihini belirtin.</span><span class="sxs-lookup"><span data-stu-id="b621d-129">**Requested receipt date** – Specify the date of delivery.</span></span>
    - <span data-ttu-id="b621d-130">**Teslimat adresi** – Siparişin teslim edileceği adresi girin.</span><span class="sxs-lookup"><span data-stu-id="b621d-130">**Delivery address** – Enter the address that the order should be delivered to.</span></span>
    - <span data-ttu-id="b621d-131">**Şirket** -Müşteri şirketin adını seçin.</span><span class="sxs-lookup"><span data-stu-id="b621d-131">**Company** – Select the name of the customer company.</span></span> <span data-ttu-id="b621d-132">Bu alan yönetici olmayan kullanıcılar için otomatik olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="b621d-132">This field is automatically set for non-admin users.</span></span>
    - <span data-ttu-id="b621d-133">**Talep numarası** – Siparişin talep numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="b621d-133">**Requisition number** – Enter the requisition number of the order.</span></span> <span data-ttu-id="b621d-134">Bu alanın doldurulması zorunlu değildir.</span><span class="sxs-lookup"><span data-stu-id="b621d-134">This field isn't required.</span></span>
    - <span data-ttu-id="b621d-135">**Sevkiyat ülkesi/bölgesi** – Maddelerin teslim edileceği ülkeyi veya bölgeyi girin.</span><span class="sxs-lookup"><span data-stu-id="b621d-135">**Ship to country/region** – Enter the country or region that the items will be delivered to.</span></span> <span data-ttu-id="b621d-136">Bu alan yönetici olmayan kullanıcılar için otomatik olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="b621d-136">This field is automatically set for non-admin users.</span></span>

    <span data-ttu-id="b621d-137">![Sipariş Bilgileri sayfası](media/customer-portal-order-information.png "Sipariş Bilgileri sayfası")</span><span class="sxs-lookup"><span data-stu-id="b621d-137">![Order Information page](media/customer-portal-order-information.png "Order Information page")</span></span>

1. <span data-ttu-id="b621d-138">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b621d-138">Select **Next**.</span></span>
1. <span data-ttu-id="b621d-139">**Öğeler** sayfasında **Öğe Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b621d-139">On the **Items** page, select **Add Item**.</span></span>

    <span data-ttu-id="b621d-140">![Öğeler sayfası](media/customer-portal-items.png "Öğeler sayfası")</span><span class="sxs-lookup"><span data-stu-id="b621d-140">![Items page](media/customer-portal-items.png "Items page")</span></span>

1. <span data-ttu-id="b621d-141">**Öğe bilgileri** iletişim kutusunda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b621d-141">In the **Item Information** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="b621d-142">**Ürün adı** - Siparişe eklenecek bir ürün bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="b621d-142">**Product Name** – Find and select a product to add to the order.</span></span>
    - <span data-ttu-id="b621d-143">**Miktar** - Seçili ürünün miktarını girin.</span><span class="sxs-lookup"><span data-stu-id="b621d-143">**Quantity** – Enter the quantity of the selected product.</span></span>
    - <span data-ttu-id="b621d-144">**Birim** – ölçü birimini belirtin (örneğin, **EA.**, **kgs** veya **kutu**).</span><span class="sxs-lookup"><span data-stu-id="b621d-144">**Unit** – Specify the unit of measure (for example, **ea.**, **kgs**, or **box**).</span></span>
    - <span data-ttu-id="b621d-145">**Tahmini Net tutar** – değer, maddenin tahmini fiyatı olarak seçilen birimin miktarını × olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="b621d-145">**Estimated net amount** – The value is calculated as the estimated price of the item × the quantity for the selected unit.</span></span>

    <span data-ttu-id="b621d-146">![Öğe Bilgileri iletişim kutusu](media/customer-portal-item-information.png "Öğe Bilgileri iletişim kutusu")</span><span class="sxs-lookup"><span data-stu-id="b621d-146">![Item Information dialog box](media/customer-portal-item-information.png "Item Information dialog box")</span></span>

1. <span data-ttu-id="b621d-147">Siparişineöğe eklemek için **Gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b621d-147">Select **Submit** to add the item to the order.</span></span>
1. <span data-ttu-id="b621d-148">Sipariş vermek istediğiniz tüm öğeleri ekleyinceye kadar 4 ile 6 arasındaki adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="b621d-148">Repeat steps 4 through 6 until you've added all the items that you want to order.</span></span>
1. <span data-ttu-id="b621d-149">Öğeleri eklemeyi bitirdiğinizde, **öğeler** sayfasında **ileri** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b621d-149">When you've finished adding items, select **Next** on the **Items** page.</span></span>
1. <span data-ttu-id="b621d-150">**Sipariş bilgileri** sayfası siparişin özetini sağlar.</span><span class="sxs-lookup"><span data-stu-id="b621d-150">The **Order Information** page provides a summary of the order.</span></span> <span data-ttu-id="b621d-151">Sipariş içeriğini ve teslimat ayrıntılarını gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="b621d-151">Review the order contents and delivery details.</span></span> <span data-ttu-id="b621d-152">Her şey doğru görünüyorsa, siparişi göndermek için **Gönder** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b621d-152">If everything looks correct, select **Submit** to submit the order.</span></span>

    <span data-ttu-id="b621d-153">![Sipariş Bilgileri sayfası](media/customer-portal-order-submit.png "Sipariş Bilgileri sayfası")</span><span class="sxs-lookup"><span data-stu-id="b621d-153">![Order Information page](media/customer-portal-order-submit.png "Order Information page")</span></span>

### <a name="standard-data-setup"></a><span data-ttu-id="b621d-154">Standart veri ayarlama</span><span class="sxs-lookup"><span data-stu-id="b621d-154">Standard data setup</span></span>

<span data-ttu-id="b621d-155">Sorunsuz bir kullanıcı deneyiminin sağlanmasına yardımcı olmak için, müşteri portalı gerekli birkaç alana ait değerleri otomatik olarak doldurur.</span><span class="sxs-lookup"><span data-stu-id="b621d-155">To help ensure a smooth user experience, the Customer portal automatically fills in values for several required fields.</span></span> <span data-ttu-id="b621d-156">Bu değerler siparişi gönderen müşterinin ilgili kişi kaydındaki bilgileri temel alınır.</span><span class="sxs-lookup"><span data-stu-id="b621d-156">These values are based on information in the contact record of the customer who is submitting the order.</span></span>

<span data-ttu-id="b621d-157">Siparişleri göndermek için müşteri portalını kullanacak bir müşteriye ait her [ilgili kişi satırı](/powerapps/maker/portals/configure/configure-contacts) için, aşağıdaki gerekli alanlar için değerlerin belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="b621d-157">For each [contact row](/powerapps/maker/portals/configure/configure-contacts) that belongs to a customer who will use the Customer portal to submit orders, values must be specified for the following required fields.</span></span> <span data-ttu-id="b621d-158">Aksi takdirde, hatalar oluşur.</span><span class="sxs-lookup"><span data-stu-id="b621d-158">Otherwise, errors will occur.</span></span>

- <span data-ttu-id="b621d-159">**Şirket** – Siparişin ait olduğu yasal varlık</span><span class="sxs-lookup"><span data-stu-id="b621d-159">**Company** – The legal entity that the order belongs to</span></span>
- <span data-ttu-id="b621d-160">**Olası müşteri** - Siparişle ilişkilendirilen müşteri hesabı.</span><span class="sxs-lookup"><span data-stu-id="b621d-160">**Potential customer** – The customer account that is associated with the order</span></span>
- <span data-ttu-id="b621d-161">**Fiyat listesi** – Müşteri için özel fiyat listesi</span><span class="sxs-lookup"><span data-stu-id="b621d-161">**Price list** – The custom price list for the customer</span></span>
- <span data-ttu-id="b621d-162">**Para birimi** – Fiyatın para birimi</span><span class="sxs-lookup"><span data-stu-id="b621d-162">**Currency** – The currency of the price</span></span>
- <span data-ttu-id="b621d-163">**Sevkiyat ülkesi/bölgesi** – Maddelerin teslim edileceği ülkeyi veya bölge</span><span class="sxs-lookup"><span data-stu-id="b621d-163">**Ship to country/region** – The country or region that the items will be delivered to</span></span>

<span data-ttu-id="b621d-164">Satış siparişi tablosu için aşağıdaki alanlar otomatik olarak ayarlanır:</span><span class="sxs-lookup"><span data-stu-id="b621d-164">The following fields are automatically set for the sales order table:</span></span>

- <span data-ttu-id="b621d-165">**Dil** – Siparişin dili (varsayılan olarak, değer, ilgili kişi kaydından alınır.)</span><span class="sxs-lookup"><span data-stu-id="b621d-165">**Language** – The language of the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="b621d-166">**Sevkiyat ülkeye/bölgeye** - Maddelerin teslim edileceği ülke veya bölge (varsayılan olarak, değer ilgili kişi kaydından alınır.)</span><span class="sxs-lookup"><span data-stu-id="b621d-166">**Ship to country/region** – The country or region that the items will be delivered to (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="b621d-167">**İlgili kişi** - Sipariş hakkında bilgi için iletişim kurulabilecek Kullanıcı (varsayılan olarak, değer ilgili kişi kaydından alınır.)</span><span class="sxs-lookup"><span data-stu-id="b621d-167">**Contact person** – The user who can be contacted for information about the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="b621d-168">**Şirket** – Siparişin ait olduğu yasal varlık (varsayılan olarak, değer ilgili kişi kaydından alınır.)</span><span class="sxs-lookup"><span data-stu-id="b621d-168">**Company** – The legal entity that the order belongs to (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="b621d-169">**Potansiyel müşteri** -Siparişle ilişkilendirilmiş müşteri hesabı (varsayılan olarak, değer, ilgili kişi kaydından alınır.)</span><span class="sxs-lookup"><span data-stu-id="b621d-169">**Potential customer** – The customer account that is associated with the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="b621d-170">**Fatura müşterisi** -Siparişle ilişkilendirilmiş faturaladırma hesabı (Varsayılan değer, ilgili kişi kaydından olası müşteridir.)</span><span class="sxs-lookup"><span data-stu-id="b621d-170">**Invoice customer** – The billing account of the order (The default value is the potential customer from the contact record.)</span></span>
- <span data-ttu-id="b621d-171">**Satış siparişi adı** – Satış siparişinin adı (varsayılan değer **Satış siparişi**.)</span><span class="sxs-lookup"><span data-stu-id="b621d-171">**Sales order name** – The name of the sales order (The default value is **sales order**.)</span></span>
- <span data-ttu-id="b621d-172">**Para birimi** – Fiyat para birimi (varsayılan olarak, değer, ilgili kişi kaydından alınır.)</span><span class="sxs-lookup"><span data-stu-id="b621d-172">**Currency** – The currency of the price (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="b621d-173">**Fiyat listesi** – Müşteri için özel fiyat listesi (varsayılan olarak, değer, ilgili kişi kaydından alınır).</span><span class="sxs-lookup"><span data-stu-id="b621d-173">**Price list** – The custom price list for the customer (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="b621d-174">**Teslimat adresi açıklaması** – Satış siparişinin teslimat adresi (varsayılan değer **Teslimat adresi açıklamasıdır**.)</span><span class="sxs-lookup"><span data-stu-id="b621d-174">**Delivery address description** – The delivery address of the sales order (The default value is **delivery address description**.)</span></span>

### <a name="modify-the-order-creation-process"></a><span data-ttu-id="b621d-175">Sipariş oluşturma işlemini değiştirme</span><span class="sxs-lookup"><span data-stu-id="b621d-175">Modify the order creation process</span></span>

<span data-ttu-id="b621d-176">Temel sipariş oluşturma sürecini değiştirmezseniz, müşteri portalının görünümünü ve Kullanıcı arabirimini serbestçe değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b621d-176">You can freely modify the appearance and UI of the Customer portal if you don't change the basic order creation process.</span></span> <span data-ttu-id="b621d-177">Sipariş oluşturma sürecini değiştirmek istiyorsanız, aklınızda tutmanız gereken birkaç nokta vardır.</span><span class="sxs-lookup"><span data-stu-id="b621d-177">If you want to change the order creation process, there are a few points that you must keep in mind.</span></span>

<span data-ttu-id="b621d-178">Aşağıdaki sütunların çift yazılır olarak satış siparişi oluşturması gerektiğinden bu sütunları Microsoft Dataverse'teki satış siparişi tablosundan bu sütunları silmeyin:</span><span class="sxs-lookup"><span data-stu-id="b621d-178">Don't remove the following columns from the sales order table in Microsoft Dataverse, because they are required to create a sales order in dual-write:</span></span>

- <span data-ttu-id="b621d-179">**Şirket** – Siparişin ait olduğu yasal varlık</span><span class="sxs-lookup"><span data-stu-id="b621d-179">**Company** – The legal entity that the order belongs to</span></span>
- <span data-ttu-id="b621d-180">**Ad** - Satış siparişi adı</span><span class="sxs-lookup"><span data-stu-id="b621d-180">**Name** – The name of the sales order</span></span>
- <span data-ttu-id="b621d-181">**Para birimi** – Fiyatın para birimi</span><span class="sxs-lookup"><span data-stu-id="b621d-181">**Currency** – The currency of the price</span></span>
- <span data-ttu-id="b621d-182">**Fiyat listesi** – Müşteri için özel fiyat listesi</span><span class="sxs-lookup"><span data-stu-id="b621d-182">**Price list** – The custom price list for the customer</span></span>
- <span data-ttu-id="b621d-183">**Sevkiyat ülkesi/bölgesi** – Maddelerin teslim edileceği ülkeyi veya bölge</span><span class="sxs-lookup"><span data-stu-id="b621d-183">**Ship to country/region** – The country or region that the items will be delivered to</span></span>
- <span data-ttu-id="b621d-184">**Olası müşteri** - Siparişle ilişkilendirilen müşteri hesabı.</span><span class="sxs-lookup"><span data-stu-id="b621d-184">**Potential customer** – The customer account that is associated with the order</span></span>
- <span data-ttu-id="b621d-185">**Dil** – Siparişin dili (genellikle, bu dil potansiyel müşterinin dilidir.)</span><span class="sxs-lookup"><span data-stu-id="b621d-185">**Language** – The language of the order (Typically, this language is the language of the potential customer.)</span></span>
- <span data-ttu-id="b621d-186">**Teslimat adresi açıklaması** – Satış siparişinin teslimat adresi</span><span class="sxs-lookup"><span data-stu-id="b621d-186">**Delivery address description** – The delivery address of the sales order</span></span>

<span data-ttu-id="b621d-187">Maddeler için aşağıdaki sütunlar gereklidir:</span><span class="sxs-lookup"><span data-stu-id="b621d-187">For items, the following columns are required:</span></span>

- <span data-ttu-id="b621d-188">**Ürün** - Sipariş ürünü</span><span class="sxs-lookup"><span data-stu-id="b621d-188">**Product** – The product to order</span></span>
- <span data-ttu-id="b621d-189">**Miktar** - Seçili ürünün miktarı</span><span class="sxs-lookup"><span data-stu-id="b621d-189">**Quantity** – The quantity of the selected product</span></span>
- <span data-ttu-id="b621d-190">**Birim** – ölçü birimini (örneğin, **EA.**, **kgs** veya **kutu**)</span><span class="sxs-lookup"><span data-stu-id="b621d-190">**Unit** – The unit of measure (for example, **ea.**, **kgs**, or **box**)</span></span>
- <span data-ttu-id="b621d-191">**Sevkiyat ülkesi/bölgesi** – Ülke veya teslimat bölgesi</span><span class="sxs-lookup"><span data-stu-id="b621d-191">**Ship to country/region** – The country or region of delivery</span></span>
- <span data-ttu-id="b621d-192">**Teslimat adresi açıklaması** – Siparişinin teslimat adresi</span><span class="sxs-lookup"><span data-stu-id="b621d-192">**Delivery address description** – The delivery address of the order</span></span>

<span data-ttu-id="b621d-193">Müşteri portalınızın tüm bu sütunlar için değer gönderdiğinden emin olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b621d-193">You must make sure that your Customer portal somehow submits values for all these columns.</span></span>

<span data-ttu-id="b621d-194">Sayfaya sütun eklemek veya sütunları kaldırmak istiyorsanız bkz. [Kolaylaştırılmış bir veri girişi deneyimi için hızlı kayıt formları oluşturma veya düzenleme](/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).</span><span class="sxs-lookup"><span data-stu-id="b621d-194">If you want to add columns to the page, or remove columns, see [Create or edit quick create forms for a streamlined data entry experience](/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).</span></span>

<span data-ttu-id="b621d-195">Sütunların önceden belirlenme şeklini ve bu sayfa kaydedildiğinde değerlerin nasıl ayarlanacağını değiştirmek istiyorsanız Power Apps portal belgelerinde aşağıdaki bilgileri inceleyin:</span><span class="sxs-lookup"><span data-stu-id="b621d-195">If you want to change how columns are preset and how values are set when the page is saved, see the following information in the Power Apps portals documentation:</span></span>

- [<span data-ttu-id="b621d-196">Önceden doldurulan alan</span><span class="sxs-lookup"><span data-stu-id="b621d-196">Prepopulate field</span></span>](/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [<span data-ttu-id="b621d-197">Kaydederken değeri ayarla</span><span class="sxs-lookup"><span data-stu-id="b621d-197">Set Value On Save</span></span>](/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a><span data-ttu-id="b621d-198">Giriş sayfasını Özelleştir</span><span class="sxs-lookup"><span data-stu-id="b621d-198">Customize the home page</span></span>

<span data-ttu-id="b621d-199">Müşteri Power Apps portalındaki tüm kontroller yerleşik Portal denetimleridir.</span><span class="sxs-lookup"><span data-stu-id="b621d-199">All the controls in the Customer portal are built-in Power Apps portals controls.</span></span> <span data-ttu-id="b621d-200">Bunları, Power Apps Portal belgelerinde [sayfa oluşturma](/powerapps/maker/portals/compose-page) içindeki adımları izleyerek özelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b621d-200">You can customize them by following the steps in [Compose a page](/powerapps/maker/portals/compose-page) in the Power Apps portals documentation.</span></span>

<span data-ttu-id="b621d-201">Ana sayfada kutucukları oluşturmak için müşteri portalı şablonunda bulunan tek özel kontrol kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b621d-201">The only custom control that is included in the Customer portal template is used to create the tiles on the home page.</span></span>

<span data-ttu-id="b621d-202">![Giriş sayfasındaki kutucuklar](media/customer-portal-home-page-tiles.png "Giriş sayfasındaki kutucuklar")</span><span class="sxs-lookup"><span data-stu-id="b621d-202">![Tiles on the home page](media/customer-portal-home-page-tiles.png "Tiles on the home page")</span></span>

<span data-ttu-id="b621d-203">Kutucukları değiştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b621d-203">To modify the tiles, follow these steps.</span></span>

1. <span data-ttu-id="b621d-204">[Portal Yönetimi uygulamasını](/powerapps/maker/portals/configure/configure-portal) açın.</span><span class="sxs-lookup"><span data-stu-id="b621d-204">Open the [Portal Management app](/powerapps/maker/portals/configure/configure-portal).</span></span>
1. <span data-ttu-id="b621d-205">Soldaki gezinti bölmesinde **Sayfa Şablonları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="b621d-205">In the navigation pane on the left, select **Page Templates**.</span></span>

    <span data-ttu-id="b621d-206">![Portal Yönetimi gezinti bölmesi](media/customer-portal-nav.png "Portal Yönetimi gezinti bölmesi")</span><span class="sxs-lookup"><span data-stu-id="b621d-206">![Portal Management navigation pane](media/customer-portal-nav.png "Portal Management navigation pane")</span></span>

1. <span data-ttu-id="b621d-207">**Giriş** adlı bir sayfa şablonu seçin.</span><span class="sxs-lookup"><span data-stu-id="b621d-207">Select the page template that is named **Home**.</span></span>
1. <span data-ttu-id="b621d-208">**Web şablonu** alanında, ilgili sayfanın kaynak kodunu açmak için **giriş** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="b621d-208">In the **Web Template** field, select the **Home** link to open the source code for that page.</span></span>

    <span data-ttu-id="b621d-209">![Web şablonu alanı](media/customer-portal-web-template.png "Web şablonu alanı")</span><span class="sxs-lookup"><span data-stu-id="b621d-209">![Web Template field](media/customer-portal-web-template.png "Web Template field")</span></span>

1. <span data-ttu-id="b621d-210">Artık giriş sayfasının tüm kaynak kodunu görmelisiniz ve bunu gereksinim duyduğunuz gibi değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b621d-210">You should now see all the source code for the home page and can modify it as you require.</span></span>

## <a name="resources"></a><span data-ttu-id="b621d-211">Kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b621d-211">Resources</span></span>

<span data-ttu-id="b621d-212">Müşteri portalını nasıl ayarlayabileceğinizi ve özelleştirebileceğinizi öğrenmek için aşağıdaki kaynaklara bakın:</span><span class="sxs-lookup"><span data-stu-id="b621d-212">To learn more about how you can set up and customize the Customer portal, see the following resources:</span></span>

- [<span data-ttu-id="b621d-213">Power Apps portal belgeleri</span><span class="sxs-lookup"><span data-stu-id="b621d-213">Power Apps portals documentation</span></span>](/powerapps/maker/portals/overview)
- [<span data-ttu-id="b621d-214">Çift yazma belgeleri</span><span class="sxs-lookup"><span data-stu-id="b621d-214">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [<span data-ttu-id="b621d-215">Portal yaşam döngüsü hakkında</span><span class="sxs-lookup"><span data-stu-id="b621d-215">About portal lifecycle</span></span>](/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="b621d-216">Bir portalı yükselt</span><span class="sxs-lookup"><span data-stu-id="b621d-216">Upgrade a portal</span></span>](/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="b621d-217">Portal konfigürasyonu geçir</span><span class="sxs-lookup"><span data-stu-id="b621d-217">Migrate portal configuration</span></span>](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="b621d-218">Çözüm yaşam döngüsü yönetimi: Customer Engagement için Dynamics 365 uygulamaları</span><span class="sxs-lookup"><span data-stu-id="b621d-218">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Satış noktasında (POS) müşteri giriş bildirimlerini etkinleştirme
description: Bu konuda, Microsoft Dynamics 365 Commerce satış noktasında (POS) müşteri giriş bildirimlerinin nasıl etkinleştirileceği açıklanmıştır.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b42dc7766f8a69a7409c28d21b49cc96eca18dd4
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271437"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a><span data-ttu-id="da061-103">Satış noktasında (POS) müşteri giriş bildirimlerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="da061-103">Enable customer check-in notifications in point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="da061-104">Bu konuda, Microsoft Dynamics 365 Commerce satış noktasında (POS) müşteri giriş bildirimlerinin nasıl etkinleştirileceği açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="da061-104">This topic describes how to enable customer check-in notifications in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="da061-105">"Sipariş teslim alma için hazır" e-postalarında kuruluşlar, müşterilere, şirket içinde bulunduklarını ve paketin kendilerine teslim edilmesini beklediklerini mağazaya bildirmelerine olanak tanıyan bir bağlantı veya düğme sunabilir.</span><span class="sxs-lookup"><span data-stu-id="da061-105">In their "order ready for pickup" emails, organizations can provide a link or button that lets customers notify the store that they are on the premises and waiting for their package to be brought out to them.</span></span> <span data-ttu-id="da061-106">Ardından müşteriler giriş alır ve mağaza, POS uygulamasında görev olarak bir bildirim alır.</span><span class="sxs-lookup"><span data-stu-id="da061-106">Customers then receive a check-in confirmation, and the store receives a notification as a task in its POS application.</span></span> <span data-ttu-id="da061-107">Bu görev, bir satış temsilcisinin siparişi müşterinin aracına teslim etmesi için bir istem görevi görür.</span><span class="sxs-lookup"><span data-stu-id="da061-107">This task serves as a prompt for a sales associate to deliver the order to the customer's vehicle.</span></span> <span data-ttu-id="da061-108">Bu sayede müşterinin mağazaya girmesi gerekmez.</span><span class="sxs-lookup"><span data-stu-id="da061-108">Therefore, the customer doesn't have to enter the store.</span></span>

<span data-ttu-id="da061-109">Müşteri girişi iş akışı, müşterilerden, park yeri numarası, araçlarının marka, model ve rengi ile teslimat talimatları gibi ek bilgiler toplamak için de yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="da061-109">The customer check-in workflow can also be configured to collect additional information from customers, such as their parking spot number, the make, model, and color of their vehicle, and delivery instructions.</span></span> <span data-ttu-id="da061-110">Perakende mağaza görevlisi, bu bilgileri kullanarak sipariş karşılama işlemini kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="da061-110">The retail store attendant can use this information to facilitate order fulfillment.</span></span>

## <a name="enable-customer-check-in"></a><span data-ttu-id="da061-111">Müşteri giriş özelliğini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="da061-111">Enable customer check-in</span></span>

<span data-ttu-id="da061-112">Müşteri giriş özelliği etkinleştirildiğinde, Commerce bir sipariş onay kodu (kanal referans kodu olarak da bilinir) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="da061-112">When the customer check-in feature is turned on, Commerce generates an order confirmation ID (also known as the channel reference ID).</span></span> <span data-ttu-id="da061-113">Ayrıca, satış noktası (POS) veya çağrı merkezi kanalları üzerinden oluşturulan siparişler için de sipariş onay kodları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="da061-113">It also generates order confirmation IDs for orders that are created through point of sale (POS) or call center channels.</span></span> 

<span data-ttu-id="da061-114">Commerce genel merkezde müşteri girişi özelliğini açmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="da061-114">To turn on the customer check-in feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="da061-115">**Çalışma alanları \> Özellik yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="da061-115">Go to **Workspaces \> Feature management**.</span></span>
2. <span data-ttu-id="da061-116">**Kanallar arasında tutarlı bir kanal referans kodu biçimi oluştur** özelliğini arayın.</span><span class="sxs-lookup"><span data-stu-id="da061-116">Search for the **Generate a consistent channel reference ID format across channels** feature.</span></span> 
3. <span data-ttu-id="da061-117">Özelliği seçin, daha sonra özellikler bölmesinde yer alan **Şimdi etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="da061-117">Select the feature, and then select **Enable now** in the properties pane.</span></span> 

## <a name="create-a-check-in-confirmation-page"></a><span data-ttu-id="da061-118">Giriş onayı sayfası oluşturma</span><span class="sxs-lookup"><span data-stu-id="da061-118">Create a check-in confirmation page</span></span>

<span data-ttu-id="da061-119">E-ticaret sitenizde, giriş onayı deneyimi olarak hizmet verecek yeni bir sayfa oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="da061-119">On your e-commerce site, you must create a new page that will serve as the check-in confirmation experience.</span></span> <span data-ttu-id="da061-120">Ek yapılandırmalarla sayfaya siparişi karşılama işlemini kolaylaştırmak için müşterilerden ek bilgiler toplayan bir form da ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="da061-120">Through additional configuration, the page can also include a form that collects additional information from customers to facilitate order fulfillment.</span></span> <span data-ttu-id="da061-121">Sayfa ve modülün nasıl ayarlanacağı konusunda bilgi için bkz. [Müşteri girişi modülü](check-in-pickup-module.md).</span><span class="sxs-lookup"><span data-stu-id="da061-121">For information about how to set up the page and module, see [Customer check-in module](check-in-pickup-module.md).</span></span>

## <a name="configure-the-transactional-email-template"></a><span data-ttu-id="da061-122">İşlem tabanlı e-posta şablonunu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="da061-122">Configure the transactional email template</span></span>

<span data-ttu-id="da061-123">Müşterilerin, siparişleri teslim alma için hazır olduğunda aldıkları işlem tabanlı e-posta için şablona bir **Buradayım** bağlantısı veya düğmesi eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="da061-123">You must add an **I am here** link or button to the template for the transactional email that customers receive when their order is ready for pickup.</span></span> <span data-ttu-id="da061-124">Müşteriler, siparişlerini almak üzere geldiklerini mağazaya bildirmek için bu bağlantıyı veya düğmeyi kullanır.</span><span class="sxs-lookup"><span data-stu-id="da061-124">Customers will use this link or button to notify the store that they have arrived to pick up their order.</span></span> 

<span data-ttu-id="da061-125">Bağlantı veya düğmeyi, **Paketleme tamamlandı** bildirimi türü ve yol kenarı sipariş karşılama için kullandığınız teslimat moduna eşlenen şablona ekleyin.</span><span class="sxs-lookup"><span data-stu-id="da061-125">Add the link or button to the template that is mapped to the **Packing completed** notification type and the mode of delivery that you're using for curbside order fulfillment.</span></span> <span data-ttu-id="da061-126">Şablonda, oluşturduğunuz giriş onay sayfasının URL'sine yönlendiren bir HTML bağlantısı veya düğme oluşturun.</span><span class="sxs-lookup"><span data-stu-id="da061-126">In the template, create an HTML link or button that points to the URL of the check-in confirmation page that you created.</span></span> <span data-ttu-id="da061-127">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="da061-127">Here is an example.</span></span>

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
<span data-ttu-id="da061-128">E-posta şablonlarını yapılandırma hakkında daha fazla bilgi için bkz. [Teslimat moduna göre işlem tabanlı e-postaları özelleştirme](customize-email-delivery-mode.md).</span><span class="sxs-lookup"><span data-stu-id="da061-128">For more information about how to configure email templates, see [Customize transactional emails by mode of delivery](customize-email-delivery-mode.md).</span></span> 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a><span data-ttu-id="da061-129">POS'ta bir giriş onayı görevi oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="da061-129">A check-in confirmation task is created in POS</span></span>

<span data-ttu-id="da061-130">Müşteri mağazaya, teslim alma için geldiklerini bildirdiklerinde bir giriş onayı bildirimi alırlar ve POS'ta, müşterinin siparişi almak için geldiği mağaza için görevler listesinde bir görev oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="da061-130">After a customer notifies the store that they are present for pickup, they receive a check-in confirmation notification, and a task is created in the tasks list in POS for the store where the customer is picking up the order.</span></span> <span data-ttu-id="da061-131">Görev, siparişi yerine getirmek için gerekli tüm müşteri ve sipariş bilgilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="da061-131">The task contains all the customer and order information that is required to fulfill the order.</span></span> <span data-ttu-id="da061-132">Görev içinde, talimatlar alanında, ek bilgiler formu aracılığıyla müşteriden toplanan tüm bilgiler gösterilir.</span><span class="sxs-lookup"><span data-stu-id="da061-132">In the task, the instructions field shows any information that was collected from the customer through the additional information form.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="da061-133">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="da061-133">Additional resources</span></span>

[<span data-ttu-id="da061-134">Teslim modülü için giriş</span><span class="sxs-lookup"><span data-stu-id="da061-134">Check-in for pickup module</span></span>](check-in-pickup-module.md)

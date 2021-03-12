---
title: POS'ta teslimat şeklini değiştirme
description: Bu konu, POS'ta teslimat işlemi değişiklik modunun nasıl yapılandırıldığını ve kullanıldığını açıklamaktadır.
author: hhainesms
manager: annbe
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 6bfe27a7b4a768da00c67e307a0bd7e57b333d11
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965439"
---
# <a name="change-mode-of-delivery-in-pos"></a><span data-ttu-id="64a2c-103">POS'ta teslimat şeklini değiştirme</span><span class="sxs-lookup"><span data-stu-id="64a2c-103">Change mode of delivery in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="64a2c-104">Bu konu, satış noktası (POS) ortamında "teslimat şeklini değiştir" işlevinin nasıl ayarlanacağını ve kullanılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="64a2c-104">This topic describes how to set up and use the "change mode of delivery" functionality in your point of sale (POS) environment.</span></span> 

<span data-ttu-id="64a2c-105">Dynamics 365 Commerce 10.0.10 ve sonraki sürümlerinde, **Teslimat şeklini değiştir** işlemi (647) POS ekran düzenlerinize eklenmek üzere sunulur.</span><span class="sxs-lookup"><span data-stu-id="64a2c-105">In Dynamics 365 Commerce versions 10.0.10 and later, the **Change mode of delivery** operation (647) is available to add to your POS screen layouts.</span></span>

<span data-ttu-id="64a2c-106">Teslimat şeklini değiştir özelliği, POS hareketinde bir veya daha fazla sevkiyat yapılandırılmış satış satırı için teslimat şeklini değiştirme seçeneği sunar.</span><span class="sxs-lookup"><span data-stu-id="64a2c-106">The change mode of delivery feature provides you with the option to change the mode of delivery for one or more shipment-configured sales lines on the POS transaction.</span></span> <span data-ttu-id="64a2c-107">Önceki Commerce sürümlerinde, sevkiyat için yapılandırılmış mevcut bir satırda teslimat şeklini değiştirmek istediğinizde, tam **Tümünü sevk et** veya **Seçileni sevk et** yapılandırma akışlarından geçmeniz gerekirdi.</span><span class="sxs-lookup"><span data-stu-id="64a2c-107">In previous versions of Commerce, you had to go through the full **Ship all** or **Ship selected** configuration flows if you wanted to change the mode of delivery on an existing line that was configured for shipment.</span></span> <span data-ttu-id="64a2c-108">Bu işlem zaman alıyordu ve satır için teslimat kaynağında veya teslimat tarihlerinde yanlışlıkla değişikliklere neden olabiliyordu.</span><span class="sxs-lookup"><span data-stu-id="64a2c-108">This process was time consuming and could result in accidental changes to the delivery origin or delivery dates for the line.</span></span> <span data-ttu-id="64a2c-109">Yeni işlev, bu satış satırlarındaki teslimat şeklini etkili şekilde güncelleştirmek için alternatif bir yöntem sağlar.</span><span class="sxs-lookup"><span data-stu-id="64a2c-109">The new functionality provides an alternative method for efficiently updating the mode of delivery on these sales lines.</span></span>

<span data-ttu-id="64a2c-110">POS düğme kılavuzundaki bir düğmeye işlem ekleme hakkında daha fazla bilgi için bkz. [Satış noktası için ekran düzenleri](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).</span><span class="sxs-lookup"><span data-stu-id="64a2c-110">For more information about how to add an operation to a button on your POS button grid, see [Screen layouts for the point of sale](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).</span></span>

<span data-ttu-id="64a2c-111">Bu özellik POS'ta yapılandırıldıktan sonra,**Teslimat şeklini değiştir**'i seçtiğinizde, teslimat şeklini değiştirmek istediğiniz hareketin satırlarını seçmenize olanak sağlayan bir liste sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="64a2c-111">After this feature is configured in POS, when you select **Change mode of delivery**, you will be presented with a list page that allows you to choose the lines of the transaction that you want to change the mode of delivery for.</span></span> <span data-ttu-id="64a2c-112">Satırların bazılarını veya tümünü seçebilir veya herhangi bir değişiklik yapmadan çıkabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64a2c-112">You can choose some or all of the lines, or exit without making any changes.</span></span> <span data-ttu-id="64a2c-113">Daha önce sevkiyat için yapılandırılmış olan satış satırları, listede değiştirebileceğiniz tek satırlardır.</span><span class="sxs-lookup"><span data-stu-id="64a2c-113">The sales lines that were previously configured for shipment are the only lines in the list that you can change.</span></span> <span data-ttu-id="64a2c-114">Malzeme çekme veya teslim alma için belirlenmiş bir satırı sevk edilmek üzere değiştirmek istiyorsanız, **Tümünü sevk et** veya **Seçileni sevk et** işlemlerini kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="64a2c-114">If you want to change a line designated for pickup or carryout to ship, you must use the **Ship all** or **Ship selected** operations.</span></span> <span data-ttu-id="64a2c-115">Buna karşılık, sevkiyat olarak belirlenmiş bir satırı malzeme çekme veya teslim alma olarak değiştirmek istiyorsanız **Tümünü çek**, **Seçileni çek**, **Tümünü teslim al** veya **Seçileni teslim al** işlemlerini kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="64a2c-115">Conversely, if you want to change a line designated as a shipment to a pickup or carryout, you must use the  **Pickup all**, **Pickup selected**, **Carryout all**, or **Carryout selected** operations.</span></span>

<span data-ttu-id="64a2c-116">Değiştirmek istediğiniz satırları seçtikten sonra, teslimat şekli seçeneklerini belirlemek için **Teslimat şeklini değiştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="64a2c-116">After you select the lines that you want to change, click **Change mode of delivery** to be prompted to select the delivery mode options.</span></span> <span data-ttu-id="64a2c-117">Değiştirilecek birden fazla satır seçtiyseniz, POS yalnızca tüm seçili ürünler için izin verilebilir olarak yapılandırılmış teslimat şekillerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="64a2c-117">If you selected multiple lines to change, POS will only display modes of delivery that have been configured as allowable for all of the selected products.</span></span> <span data-ttu-id="64a2c-118">Teslimat şekilleri belirli ürünleri ve teslimat adreslerini destekleyecek şekilde yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="64a2c-118">Modes of delivery can be configured to support specific products and delivery addresses.</span></span> <span data-ttu-id="64a2c-119">Bir ürün ve adres birleşimi için kabul edilebilir ancak başka bir seçilen ürün ve adres birleşimi için kabul edilebilir olmayan bir teslimat şekli varsa, teslimat şekli kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="64a2c-119">If there is a mode of delivery that is acceptable for one product and address combination but is not acceptable for another selected product and address combination, the mode of delivery is not available.</span></span> <span data-ttu-id="64a2c-120">Bir ürün tarafından desteklenmeyen bir teslimat şeklini başka bir ürünün teslimat şekli olarak seçmek istiyorsanız, satırları tek tek seçmeniz ve teslimat şeklini her bir satır için ayrı olarak değiştirmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="64a2c-120">You may need to select lines one by one and change the mode of delivery for each line separately if you want to select a mode of delivery for one product that is not supported by another product.</span></span>  

<span data-ttu-id="64a2c-121">Yeni teslimat şeklini seçtikten sonra hareket sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="64a2c-121">After you select the new mode of delivery, the transaction page is displayed.</span></span> <span data-ttu-id="64a2c-122">Yeni teslimat şekli seçimlerinizi gözden geçirmek için hareket listesinde **Teslimat** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="64a2c-122">To review your new delivery mode selections, select the **Delivery** tab on the transaction list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="64a2c-123">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="64a2c-123">Additional resources</span></span>

[<span data-ttu-id="64a2c-124">Çağrı merkezi siparişleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="64a2c-124">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="64a2c-125">Teslimat şekline göre işlem tabanlı e-postaları özelleştirme</span><span class="sxs-lookup"><span data-stu-id="64a2c-125">Customize transactional emails by mode of delivery</span></span>](customize-email-delivery-mode.md)

---
title: POS'ta seri numarası denetimli ürünleri iade etme
description: Bu konu, serileştirilmiş maddeleri Microsoft Dynamics 365 Commerce satış noktası (POS) uygulamasında iade sürecinin bir parçası olarak doğrulamaya yönelik özellikleri açıklamaktadır.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7a067994828f3df577c0dc4146d26ac81990d4ac
ms.sourcegitcommit: 927574c77f4883d906e5c7bddf0af9b717e492bf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129835"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a><span data-ttu-id="e31de-103">POS'ta seri numarası denetimli ürünleri iade etme</span><span class="sxs-lookup"><span data-stu-id="e31de-103">Return serial number–controlled products in POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="e31de-104">Bu konu, serileştirilmiş maddeleri Microsoft Dynamics 365 Commerce satış noktası (POS) uygulamasında iade sürecinin bir parçası olarak doğrulamaya yönelik özellikleri açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="e31de-104">This topic describes the capabilities for validating serialized items as part of the return process in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

> [!NOTE]
> <span data-ttu-id="e31de-105">Commerce sürüm 10.0.20 ve sonrasında, **POS'ta birleşik iade işleme deneyimi** olarak adlandırılan yeni bir özellik mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="e31de-105">In the Commerce version 10.0.20 release and later, a new feature that is named **Unified return processing experience in POS** is available.</span></span> <span data-ttu-id="e31de-106">POS'ta iade siparişi işleme sırasında seri numara doğrulamasını kullanmak için bu özelliği etkinleştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="e31de-106">To use serial number validation during return order processing in POS, you must turn on this feature.</span></span> <span data-ttu-id="e31de-107">Bu özellik etkinleştirildiğinde sağladığı diğer özellikler hakkında bilgi için, bkz. [POS'ta iade oluşturma](POS-returns.md).</span><span class="sxs-lookup"><span data-stu-id="e31de-107">For information about others capabilities that this feature provides when it's turned on, see [Create returns in POS)](POS-returns.md).</span></span>
>
> <span data-ttu-id="e31de-108">Özellik, etkinleştirildikten sonra kapatılamaz.</span><span class="sxs-lookup"><span data-stu-id="e31de-108">After the feature is turned on, it can't be turned off.</span></span>

## <a name="options-for-validating-serialized-returns"></a><span data-ttu-id="e31de-109">Serileştirilmiş iadeleri doğrulama seçenekleri</span><span class="sxs-lookup"><span data-stu-id="e31de-109">Options for validating serialized returns</span></span>

<span data-ttu-id="e31de-110">**POS'ta birleşik iade işleme deneyimi** özelliği açık olduğunda, kuruluşlar POS üzerinden seri numarası denetimli maddelerin iadesinde doğrulama gerçekleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="e31de-110">When the **Unified return processing experience in POS** feature is turned on, organizations can perform a validation on returns of serial number–controlled items through POS.</span></span> <span data-ttu-id="e31de-111">Döndürülen seri numarası, satılan orijinal seri numarasından farklıysa bu özellik kullanıcıları uyarabilir.</span><span class="sxs-lookup"><span data-stu-id="e31de-111">This capability can warn users if the serial number that is being returned differs from the original serial number that was sold.</span></span> <span data-ttu-id="e31de-112">Commerce sürüm 10.0.20 ve sonrasında kullanıcıların aldığı ileti yalnızca bir uyarı iletisidir.</span><span class="sxs-lookup"><span data-stu-id="e31de-112">In the Commerce version 10.0.20 release and later, the message that users receive is only a warning message.</span></span> <span data-ttu-id="e31de-113">Kullanıcılar, başlangıçta satılan seri numarasından farklı bir seri numarasına sahip bir iade işlemine devam edebilir.</span><span class="sxs-lookup"><span data-stu-id="e31de-113">Users can continue to process a return against a serial number that differs from the serial number that was originally sold.</span></span>

<span data-ttu-id="e31de-114">**POS'ta birleşik iade işleme deneyimi** özelliği etkinleştirildikten sonra bir kuruluşun seri numarası doğrulamasını yapılandırmak için Commerce genel merkezinde **Retail ve Commerce \> Genel merkez kurulumu \> Parametreler \> Commerce parametreleri** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="e31de-114">To configure serial number validation for an organization after the **Unified return processing experience in POS** feature is turned on, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters** in Commerce headquarters.</span></span> <span data-ttu-id="e31de-115">**Stok** sekmesinde, **Mağaza stoku işlemleri** hızlı sekmesinde, **POS iadelerinde seri numaralarını doğrulama** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e31de-115">On the **Inventory** tab, on the **Store inventory operations** FastTab, set the **Enable validation of serial numbers on POS returns** option to **Yes**.</span></span>

## <a name="process-returns-for-serialized-items-in-pos"></a><span data-ttu-id="e31de-116">POS'ta serileştirilmiş maddelerin iadesi</span><span class="sxs-lookup"><span data-stu-id="e31de-116">Process returns for serialized items in POS</span></span>

<span data-ttu-id="e31de-117">**POS iadelerinde seri numaraların doğrulamasını etkinleştir** seçeneği **Evet** olarak ayarlanmışsa, POS aracılığıyla seri numarası denetimli bir madde iade edildiğinde kullanıcı, **İade edilebilir ürünler** sayfasındaki ayrıntılar bölmesine iade satırına ait seri numarasını girebilir.</span><span class="sxs-lookup"><span data-stu-id="e31de-117">If the **Enable validation of serial numbers on POS returns** option has been set to **Yes**, when a serial number–controlled item is returned through POS, the user can enter the serial number for the return line in the details pane on the **Returnable products** page.</span></span> <span data-ttu-id="e31de-118">Girilen seri numarası, satış hareketi için satılan orijinal seri numarasıyla eşleşmiyorsa, kullanıcı bir uyarı iletisi alır.</span><span class="sxs-lookup"><span data-stu-id="e31de-118">If the serial number that is entered doesn't match the original serial number that was sold for the sales transaction, the user receives a warning message.</span></span> <span data-ttu-id="e31de-119">Ancak, uygulama kullanıcının iadeyi deftere nakletmeye devam etmesini engellemez.</span><span class="sxs-lookup"><span data-stu-id="e31de-119">However, the application doesn't prevent the user from continuing to post the return.</span></span>

> [!NOTE]
> <span data-ttu-id="e31de-120">POS, yalnızca orijinal sipariş edilen miktarın birden fazla olmadığı iade satırlarında seri numaralarının doğrulanmasını destekler.</span><span class="sxs-lookup"><span data-stu-id="e31de-120">Currently, POS supports validation of serial numbers only on return lines where the original ordered quantity is no more than one.</span></span> <span data-ttu-id="e31de-121">Orijinal satış siparişi satırı, POS dışı bir kanalda oluşturulmuşsa ve belirli bir satış satırındaki serileştirilmiş madde için sipariş edilen miktar birden büyükse, madde POS üzerinden doğru şekilde iade edilemez.</span><span class="sxs-lookup"><span data-stu-id="e31de-121">If the original sales order line was created in a non-POS channel, and if the quantity that was ordered for the serialized item on a given sales line is more than one, the item can't be correctly returned through POS.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e31de-122">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e31de-122">Additional resources</span></span>

[<span data-ttu-id="e31de-123">POS'ta iade oluşturma</span><span class="sxs-lookup"><span data-stu-id="e31de-123">Create returns in POS</span></span>](POS-returns.md)

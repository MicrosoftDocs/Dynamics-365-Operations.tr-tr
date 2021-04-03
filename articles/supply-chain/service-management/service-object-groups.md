---
title: Servis nesne grupları
description: Nesne grupları, raporlara ve istatistiklere yönelik nesneler hakkındaki verilerin sıralaması ve filtrelenmesi açısından yararlıdır.
author: ShylaThompson
manager: tfehr
ms.date: 05/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9d19e29dbddb0bccf3221cc82e6dbb2c05f7e85
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5266091"
---
# <a name="service-object-groups"></a><span data-ttu-id="b841b-103">Servis nesne grupları</span><span class="sxs-lookup"><span data-stu-id="b841b-103">Service object groups</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b841b-104">Nesne grupları, raporlara ve istatistiklere yönelik nesneler hakkındaki verilerin sıralaması ve filtrelenmesi açısından yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="b841b-104">Object groups are useful for sorting and filtering the data about objects for reports and statistics.</span></span> <span data-ttu-id="b841b-105">Örneğin, nesneleri coğrafi konuma veya türe göre gruplandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b841b-105">For example, you can group objects by geographical location or by type.</span></span>

## <a name="group-by-geographical-location"></a><span data-ttu-id="b841b-106">Coğrafi konuma göre gruplandırma</span><span class="sxs-lookup"><span data-stu-id="b841b-106">Group by geographical location</span></span>

<span data-ttu-id="b841b-107">Şirket hizmetlerinizin bulunduğu farklı nesnelerin yerini göstermek üzere bu gruplandırma yöntemini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b841b-107">You can use this grouping method to show where the various different objects that your company services are located.</span></span> <span data-ttu-id="b841b-108">Nesneleri coğrafi konuma göre gruplandırmak aynı zamanda örneğin, belirli bir ülkede/bölgede şirketinizin zaten hizmet verdiği nesneleri tanımlamanız gereken durumlarda da yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="b841b-108">Grouping objects by geographical location can also be useful if, for example, you must identify the objects that your company already provides services for in a particular country/region.</span></span>

## <a name="example"></a><span data-ttu-id="b841b-109">Örnek</span><span class="sxs-lookup"><span data-stu-id="b841b-109">Example</span></span>

<span data-ttu-id="b841b-110">Belçika'da bulunan bir müşteri servis merkezinizi arayarak ABC adlı bir nesne için bir servis sözleşmesi oluşturmak ister.</span><span class="sxs-lookup"><span data-stu-id="b841b-110">A customer from Belgium calls your service center and wants to create a service agreement for an object, ABC.</span></span> <span data-ttu-id="b841b-111">Belçika'da servis yapılan tüm nesnelere Belçika adında bir coğrafi konum nesne grubu iliştirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b841b-111">You have attached an object group for geographical location, Belgium, to all objects that are serviced in Belgium.</span></span> <span data-ttu-id="b841b-112">Bu grubu bir filtre olarak kullanarak, ABC'nin programınızda bir kayıt olarak bulunup bulunmadığını veya yeni bir nesne oluşturmanız gerekip gerekmediğini görmek üzere hızlı bir arama yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b841b-112">By using this group as a filter, you can quickly search to see whether you already have a record for ABC in the program, or whether you must set up a new object.</span></span> 

## <a name="group-by-type"></a><span data-ttu-id="b841b-113">Tipe göre gruplandırma</span><span class="sxs-lookup"><span data-stu-id="b841b-113">Group by type</span></span>

<span data-ttu-id="b841b-114">Bu gruplandırma yöntemini, şirketinizin servis verdiği nesne türlerine göstermek üzere kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b841b-114">You can use this grouping method to show the types of objects that your company services.</span></span> <span data-ttu-id="b841b-115">Ayrıca, nesneleri türe göre gruplandırmak programdaki benzer mevcut nesneleri temel alan yeni bir nesne oluşturmak istediğiniz durumlarda da yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="b841b-115">Grouping objects by type can also be useful if, for example, you want to create a new object based on similar objects that already exist in the program.</span></span>

## <a name="example"></a><span data-ttu-id="b841b-116">Örnek</span><span class="sxs-lookup"><span data-stu-id="b841b-116">Example</span></span>

<span data-ttu-id="b841b-117">Müşteri sizi arayarak HIJ adındaki bir klima cihazı için sizinle bir servis sözleşmesi yapmak ister.</span><span class="sxs-lookup"><span data-stu-id="b841b-117">A customer calls and wants to set up a service agreement for an air conditioning machine, HIJ.</span></span> <span data-ttu-id="b841b-118">Bu cihaz için henüz bir kaydınız yoktur.</span><span class="sxs-lookup"><span data-stu-id="b841b-118">You do not already have a record for this machine.</span></span> <span data-ttu-id="b841b-119">Ancak, Klima adlı bir nesne grubu oluşturur ve bu grubu tüm klima nesnelerine iliştirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b841b-119">However, you have set up an object group titled Air Conditioners, and you have attached this group to all air conditioning objects.</span></span> <span data-ttu-id="b841b-120">Bu nedenle, diğer tüm klima cihazlarını çabuk şekilde arayıp tanımlayabilir ve HIJ'ye ait servis sözleşmesi satırlarını oluşturmak için bu nesnelerden alınmış şablon bilgilerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b841b-120">Therefore, you can quickly search for and identify all other air conditioning machines and use the template information from these objects to create service agreement lines for HIJ.</span></span> <span data-ttu-id="b841b-121">Nesne gruplarını bu şekilde kullanarak hızlı bir şekilde yeni nesneler oluşturabilir ve bunlar üzerinde gerçekleştirilecek servis görevlerini belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b841b-121">By using object groups in this manner, you can quickly set up new objects and determine the service tasks that must be performed on them.</span></span> 

## <a name="create-service-object-groups"></a><span data-ttu-id="b841b-122">Servis nesnesi grupları oluşturma</span><span class="sxs-lookup"><span data-stu-id="b841b-122">Create service object groups</span></span>

<span data-ttu-id="b841b-123">Servis nesneleri atayabileceğiniz gruplar oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b841b-123">Create groups that you can assign service objects to.</span></span> <span data-ttu-id="b841b-124">Servis nesneleri, servislerin gerçekleştirilmesinde kullanılan stok maddeleri ve diğer ürünlerdir.</span><span class="sxs-lookup"><span data-stu-id="b841b-124">Service objects are inventory items and other products for which services are performed.</span></span> <span data-ttu-id="b841b-125">Servis nesnelerini gruplandırarak benzer ve ilgili servis nesneleriyle ilgili raporlar oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b841b-125">By grouping service objects, you can create reports for similar and related service objects.</span></span> <span data-ttu-id="b841b-126">Örneğin, bir servis nesne grubu iki servis nesnesi içerebilir: Bir servis nesnesi bir set ve diğer servis setin takılması için gerçekleştirilen hizmettir.</span><span class="sxs-lookup"><span data-stu-id="b841b-126">For example, a service object group might consist of two service objects: One service object is a kit, and the second service object is the service to install the kit.</span></span>

<span data-ttu-id="b841b-127">Servis nesne grupları oluşturmak için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="b841b-127">To create service object groups, follow these steps:</span></span>

1. <span data-ttu-id="b841b-128">**Servis yönetimi > Kurulum > Servis nesneleri > Servis nesnesi grupları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b841b-128">Click **Service management > Setup > Service objects > Service object groups**.</span></span>

2. <span data-ttu-id="b841b-129">Yeni servis nesnesi grubu oluşturmak için **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b841b-129">Click **New** to create a new service object group.</span></span>

3. <span data-ttu-id="b841b-130">Servis nesnesi grubu için benzersiz bir ad ve isteğe bağlı olarak açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="b841b-130">Enter a unique name for the service object group and, optionally, a description.</span></span>

<span data-ttu-id="b841b-131">Servis nesnelerini **Servis nesneleri** formunu kullanarak gruba atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b841b-131">You can assign service objects to the group by using the **Service objects** form.</span></span> 

## <a name="see-also"></a><span data-ttu-id="b841b-132">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="b841b-132">See also</span></span>

[<span data-ttu-id="b841b-133">Servis nesneleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="b841b-133">Create service objects</span></span>](create-service-objects.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
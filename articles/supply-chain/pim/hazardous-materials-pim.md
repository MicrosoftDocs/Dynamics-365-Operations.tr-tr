---
title: Tehlikeli maddeler
description: Bu konu, ortamınızda depolanan tehlikeli madde belge ve bilgileri hakkında bilgi sağlamaktadır.
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 156cd4ec3a1d1a08ba43832a93fde0d4f22ac2ed
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007653"
---
# <a name="hazardous-materials"></a><span data-ttu-id="c5af2-103">Tehlikeli maddeler</span><span class="sxs-lookup"><span data-stu-id="c5af2-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="c5af2-104">Tehlikeli maddeler hakkındaki bilgiler Ürün bilgileri yönetimi'nde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="c5af2-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="c5af2-105">Bu modül, ambar yönetimiyle yazdırılabilen belgeleri de sağlar.</span><span class="sxs-lookup"><span data-stu-id="c5af2-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="c5af2-106">Tehlikeli mal olarak sınıflandırılmış malzemeler sevk ediyorsanız, sevkiyata ek resmi belgeler de dahil edilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="c5af2-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="c5af2-107">Tehlikeli maddeler işlevselliği, müşterilerin sınıflandırma bilgilerini depolamasına ve serbest bırakma kalemleriyle ilişkilendirmesine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="c5af2-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="c5af2-108">Bu bilgiler daha sonra sevkiyat belgelerinin hazırlanmasına yardımcı olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c5af2-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c5af2-109">Microsoft Dynamics 365 Supply Chain Management'taki tehlikeli malzeme özellikleri, tehlikeli ürünlerinizle ilgili bilgileri kaydetmenize ve bu bilgilere başvurmanıza yardımcı olabilecek kullanışlı ürün bilgisi alanları ve ilgili işlevler koleksiyonu sağlar.</span><span class="sxs-lookup"><span data-stu-id="c5af2-109">The hazardous materials features in Microsoft Dynamics 365 Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="c5af2-110">Bu özellikler, sevk ettiğiniz tehlikeli malzemeler hakkındaki bilgilerin aynısını içeren sevkiyat belgelerini tasarlamanıza ve yazdırmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="c5af2-110">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="c5af2-111">Ancak, sistem ülkenizdeki veya bölgenizdeki geçerli tüm yönetmeliklerle otomatik olarak uyumlu hale gelmez.</span><span class="sxs-lookup"><span data-stu-id="c5af2-111">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="c5af2-112">Bu araçlar ortak yönetmeliklere uymanıza yardımcı olacak şekilde tasarlanmış olsa da kendi başlarına yeterli değillerdir ve bununla ilgili bir garanti sunulmaz.</span><span class="sxs-lookup"><span data-stu-id="c5af2-112">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="c5af2-113">Geçerli tüm yönetmelikleri bilmek ve bunlara uymak için gerekli tüm adımları atmaktan kuruluşunuz sorumludur.</span><span class="sxs-lookup"><span data-stu-id="c5af2-113">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

<span data-ttu-id="c5af2-114">Bu işlevi kullanabilmeniz için aşağıdaki kurulum gereklidir:</span><span class="sxs-lookup"><span data-stu-id="c5af2-114">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="c5af2-115">**Ürün bilgileri yönetimi:** Serbest bırakılan ürünlere uygulanabilecek kodları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c5af2-115">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="c5af2-116">**Ambar yönetimi:** Sevkiyat bilgilerini yazdırmak için ek sevkiyat belgeleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="c5af2-116">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="c5af2-117">Ürün bilgileri yönetimi</span><span class="sxs-lookup"><span data-stu-id="c5af2-117">Product information management</span></span>

<span data-ttu-id="c5af2-118">Ürün bilgileri yönetimi'nde, kara, hava ve deniz yoluyla taşıma için tehlikeli mal listelerinde sağlanan referans bilgilerini ekleyebileceğiniz bir dizi kurulum tablosu vardır.</span><span class="sxs-lookup"><span data-stu-id="c5af2-118">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="c5af2-119">Sıklıkla başvurulan düzenlemelerden bazıları şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c5af2-119">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="c5af2-120">**ADR** – Tehlikeli malların uluslararası karayollarında taşınmasıyla ilgili düzenlemeler</span><span class="sxs-lookup"><span data-stu-id="c5af2-120">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="c5af2-121">**CFR 49** – ABD'de tehlikeli malların taşınmasına yönelik düzenlemeler</span><span class="sxs-lookup"><span data-stu-id="c5af2-121">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="c5af2-122">**IMDG** – Uluslararası Denizcilik Tehlikeli Maddeler (IMDG) kodu</span><span class="sxs-lookup"><span data-stu-id="c5af2-122">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="c5af2-123">**IATA** – Uluslararası Hava Taşımacılığı Birliği (IATA) tehlikeli mal düzenlemeleri</span><span class="sxs-lookup"><span data-stu-id="c5af2-123">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="c5af2-124">Bu düzenlemelerin her biri, referans kodları içeren bir tehlikeli mallar listesi içerir.</span><span class="sxs-lookup"><span data-stu-id="c5af2-124">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="c5af2-125">Her bir taşıma türünün listeleri, paylaşılan uluslararası sınıflandırmalarda birleştirilir.</span><span class="sxs-lookup"><span data-stu-id="c5af2-125">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="c5af2-126">Supply Chain Management, bu listelerdeki paylaşılan kodlar için bir başvuru tablosu sağlar.</span><span class="sxs-lookup"><span data-stu-id="c5af2-126">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="c5af2-127">Her listede, tanımlanabilecek bazı benzersiz kodlar da vardır.</span><span class="sxs-lookup"><span data-stu-id="c5af2-127">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="c5af2-128">Bu bilgileri yapılandırmaya başlamak için ilk parametreleri yapılandırmada kullanabileceğiniz bir düzenleme oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c5af2-128">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="c5af2-129">Ambar yönetimi</span><span class="sxs-lookup"><span data-stu-id="c5af2-129">Warehouse management</span></span>

<span data-ttu-id="c5af2-130">Bir sevkiyat hazırlanırken çeşitli yeni raporlar yazdırılabilir.</span><span class="sxs-lookup"><span data-stu-id="c5af2-130">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="c5af2-131">Bu raporlar, Ürün bilgileri yönetimi'nde ayarladığınız bilgileri kullanır.</span><span class="sxs-lookup"><span data-stu-id="c5af2-131">These reports use the information that you set up in Product information management.</span></span>

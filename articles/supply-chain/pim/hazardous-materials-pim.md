---
title: Tehlikeli maddeler
description: Bu konu, ortamınızda depolanan tehlikeli madde belge ve bilgileri hakkında bilgi sağlamaktadır.
author: lachlancashMS
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76dd6539e39bb77c546e613b290fc5decba9457f
ms.sourcegitcommit: 4c60f5dccdf0b94ed110a657ef331546adc5424a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2020
ms.locfileid: "2982320"
---
# <a name="hazardous-materials"></a><span data-ttu-id="acbcc-103">Tehlikeli maddeler</span><span class="sxs-lookup"><span data-stu-id="acbcc-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="acbcc-104">Tehlikeli maddeler hakkındaki bilgiler Ürün bilgileri yönetimi'nde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="acbcc-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="acbcc-105">Bu modül, ambar yönetimiyle yazdırılabilen belgeleri de sağlar.</span><span class="sxs-lookup"><span data-stu-id="acbcc-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="acbcc-106">Tehlikeli mal olarak sınıflandırılmış malzemeler sevk ediyorsanız, sevkiyata ek resmi belgeler de dahil edilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="acbcc-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="acbcc-107">Tehlikeli maddeler işlevselliği, müşterilerin sınıflandırma bilgilerini depolamasına ve serbest bırakma kalemleriyle ilişkilendirmesine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="acbcc-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="acbcc-108">Bu bilgiler daha sonra sevkiyat belgelerinin hazırlanmasına yardımcı olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="acbcc-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="acbcc-109">Microsoft Dynamics 365 Supply Chain Management, tehlikeli madde sevkiyatının yönetimine yardımcı olmak amacıyla, ürünlerle ilgili ek referans bilgileri ayarlamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="acbcc-109">To help manage shipments of dangerous goods, Microsoft Dynamics 365 Supply Chain Management lets you set up additional reference information that is related to products.</span></span> <span data-ttu-id="acbcc-110">Ayrıca, ek sevkiyat belgeleri de ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="acbcc-110">You can also set up additional shipment documents.</span></span> <span data-ttu-id="acbcc-111">Ancak, sistem ülkenizin veya bölgenizin düzenlemeleriyle otomatik olarak uyumlu hale gelmez.</span><span class="sxs-lookup"><span data-stu-id="acbcc-111">However, the system isn't automatically compliant with your country's or region's regulations.</span></span> <span data-ttu-id="acbcc-112">Bunun yerine, genel programınıza yardımcı olabilecek bir araçtır.</span><span class="sxs-lookup"><span data-stu-id="acbcc-112">Instead, it's a tool that can help your overall program.</span></span>

<span data-ttu-id="acbcc-113">Bu işlevi kullanabilmeniz için aşağıdaki kurulum gereklidir:</span><span class="sxs-lookup"><span data-stu-id="acbcc-113">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="acbcc-114">**Ürün bilgileri yönetimi:** Serbest bırakılan ürünlere uygulanabilecek kodları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="acbcc-114">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="acbcc-115">**Ambar yönetimi:** Sevkiyat bilgilerini yazdırmak için ek sevkiyat belgeleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="acbcc-115">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="acbcc-116">Ürün bilgileri yönetimi</span><span class="sxs-lookup"><span data-stu-id="acbcc-116">Product information management</span></span>

<span data-ttu-id="acbcc-117">Ürün bilgileri yönetimi'nde, kara, hava ve deniz yoluyla taşıma için tehlikeli mal listelerinde sağlanan referans bilgilerini ekleyebileceğiniz bir dizi kurulum tablosu vardır.</span><span class="sxs-lookup"><span data-stu-id="acbcc-117">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="acbcc-118">Sıklıkla başvurulan düzenlemelerden bazıları şunlardır:</span><span class="sxs-lookup"><span data-stu-id="acbcc-118">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="acbcc-119">**ADR** – Tehlikeli malların uluslararası karayollarında taşınmasıyla ilgili düzenlemeler</span><span class="sxs-lookup"><span data-stu-id="acbcc-119">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="acbcc-120">**CFR 49** – ABD'de tehlikeli malların taşınmasına yönelik düzenlemeler</span><span class="sxs-lookup"><span data-stu-id="acbcc-120">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="acbcc-121">**IMDG** – Uluslararası Denizcilik Tehlikeli Maddeler (IMDG) kodu</span><span class="sxs-lookup"><span data-stu-id="acbcc-121">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="acbcc-122">**IATA** – Uluslararası Hava Taşımacılığı Birliği (IATA) tehlikeli mal düzenlemeleri</span><span class="sxs-lookup"><span data-stu-id="acbcc-122">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="acbcc-123">Bu düzenlemelerin her biri, referans kodları içeren bir tehlikeli mallar listesi içerir.</span><span class="sxs-lookup"><span data-stu-id="acbcc-123">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="acbcc-124">Her bir taşıma türünün listeleri, paylaşılan uluslararası sınıflandırmalarda birleştirilir.</span><span class="sxs-lookup"><span data-stu-id="acbcc-124">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="acbcc-125">Supply Chain Management, bu listelerdeki paylaşılan kodlar için bir başvuru tablosu sağlar.</span><span class="sxs-lookup"><span data-stu-id="acbcc-125">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="acbcc-126">Her listede, tanımlanabilecek bazı benzersiz kodlar da vardır.</span><span class="sxs-lookup"><span data-stu-id="acbcc-126">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="acbcc-127">Bu bilgileri yapılandırmaya başlamak için ilk parametreleri yapılandırmada kullanabileceğiniz bir düzenleme oluşturun.</span><span class="sxs-lookup"><span data-stu-id="acbcc-127">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="acbcc-128">Ambar yönetimi</span><span class="sxs-lookup"><span data-stu-id="acbcc-128">Warehouse management</span></span>

<span data-ttu-id="acbcc-129">Bir sevkiyat hazırlanırken çeşitli yeni raporlar yazdırılabilir.</span><span class="sxs-lookup"><span data-stu-id="acbcc-129">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="acbcc-130">Bu raporlar, Ürün bilgileri yönetimi'nde ayarladığınız bilgileri kullanır.</span><span class="sxs-lookup"><span data-stu-id="acbcc-130">These reports use the information that you set up in Product information management.</span></span>

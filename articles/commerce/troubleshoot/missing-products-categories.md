---
title: Ortam kopyaladıktan sonra ürün ve kategoriler eksik
description: Bu konu, bir site ortamlar arasında veya aynı ortam içinde kopyalandıktan sonra ürün ve kategorilerin eksik olduğu durumlarda yardımcı olabilecek sorun giderme kılavuzu sağlar.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 35f2cbd98a91149395f40bf821c1d5d7e58eaf77
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585581"
---
# <a name="products-and-categories-missing-after-environment-copy"></a><span data-ttu-id="15142-103">Ortam kopyaladıktan sonra ürün ve kategoriler eksik</span><span class="sxs-lookup"><span data-stu-id="15142-103">Products and categories missing after environment copy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="15142-104">Bu konu, bir site ortamlar arasında veya aynı ortam içinde kopyalandıktan sonra ürün ve kategorilerin eksik olduğu durumlarda yardımcı olabilecek sorun giderme kılavuzu sağlar.</span><span class="sxs-lookup"><span data-stu-id="15142-104">This topic provides troubleshooting guidance that can help when products and categories are missing after a site is copied between environments or within the same environment.</span></span>

## <a name="description"></a><span data-ttu-id="15142-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="15142-105">Description</span></span>

<span data-ttu-id="15142-106">Bir site bir ortamdan diğerine veya aynı ortam içinde kopyalandıktan sonra, sitede ürünler ve Kategoriler eksik.</span><span class="sxs-lookup"><span data-stu-id="15142-106">After a site is copied from one environment to another, or within the same environment, the products and categories are missing from the site.</span></span> <span data-ttu-id="15142-107">Ürünler ve Kategoriler e-ticaret mağazasında ve Commerce Site Builder'daki **ürünler** sekmesinde yok.</span><span class="sxs-lookup"><span data-stu-id="15142-107">The products and categories will be missing from the e-commerce storefront and from the **Products** tab in Commerce site builder.</span></span>

## <a name="resolution"></a><span data-ttu-id="15142-108">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="15142-108">Resolution</span></span>

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a><span data-ttu-id="15142-109">Kanal işletim birimi numarasını Commerce Site Builder'da yeni kopyalanmış bir siteyle eşleyin</span><span class="sxs-lookup"><span data-stu-id="15142-109">Map the channel operating unit number to a newly copied site in Commerce site builder</span></span>

<span data-ttu-id="15142-110">Kanal işletim birimi numarasını (OUN) Commerce Site Builder'da yeni kopyalanmış bir siteyle eşlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="15142-110">To map the channel operating unit number (OUN) to a newly copied site in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="15142-111">Yeni kopyalanan siteyi seçin.</span><span class="sxs-lookup"><span data-stu-id="15142-111">Select the newly copied site.</span></span>
1. <span data-ttu-id="15142-112">**Site Ayarları** altında, **Kanallar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="15142-112">Under **Site settings**, select **Channels**.</span></span>
1. <span data-ttu-id="15142-113">Kanal adının yanındaki üç noktayı (**...**) seçin ve sonra **çevrimiçi mağaza kanalını Değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="15142-113">Next to the channel name, select the ellipsis (**...**), and then select **Change online store channel**.</span></span>
1. <span data-ttu-id="15142-114">**Çevrimiçi mağaza kanalını Değiştir** iletişim kutusunda, yeni kopyalanan siteyle eşlenecek kanalı seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="15142-114">In the **Change online store channel** dialog box, select the channel to map to the newly copied site, and then select **OK**.</span></span>
1. <span data-ttu-id="15142-115">**Kaydet ve yayınla** yı seçin.</span><span class="sxs-lookup"><span data-stu-id="15142-115">Select **Save and publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="15142-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="15142-116">Additional resources</span></span>

[<span data-ttu-id="15142-117">Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="15142-117">Associate a Dynamics 365 Commerce site with an online channel</span></span>](../associate-site-online-store.md)

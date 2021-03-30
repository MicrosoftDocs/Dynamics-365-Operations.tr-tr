---
title: Perakende satış fiyatı raporları
description: Bu konu, çeşitli ürünler için gelecekteki fiyat değişiklikleri görmek için kullanılan fiyat raporlama özelliğine bir genel bakış sağlar.
author: shajain
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: f317b22f2794dc71093068a51c8e9d4e6d7d55ac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231164"
---
# <a name="retail-price-reports"></a><span data-ttu-id="65d95-103">Perakende satış fiyatı raporları</span><span class="sxs-lookup"><span data-stu-id="65d95-103">Retail price reports</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="65d95-104">Müşterilerine rekabetçi fiyatlar sunabilmek için perakendeciler ürünlerinin fiyatını sıklıkla değiştirir.</span><span class="sxs-lookup"><span data-stu-id="65d95-104">In order to provide competitive prices to their customers, retailers often change prices of products.</span></span> <span data-ttu-id="65d95-105">Mağaza yöneticileri, geçmişte veya gelecekteki fiyat değişikliklerine hızlı erişime sahip olmak isterler, bu sayede mağaza raflarında gösterilen fiyat etiketlerini güncelleştirmek için gerekli kaynakları planlayabilirler.</span><span class="sxs-lookup"><span data-stu-id="65d95-105">Store managers want the ability to easily access recent or upcoming price changes so that they can plan for the required resources to update the price labels displayed on the store shelves.</span></span> <span data-ttu-id="65d95-106">Retail 10.0 sürümünün yayınlanmasıyla, bir mağaza yöneticisi **Fiyat** raporunu **Tüm perakende mağazaları \> Mağaza \> Fiyat raporu**'na giderek ve mağaza ile ilişkilendirilmiş ürünlerin fiyatlarını görüntülemek ve güncelleştirmek için açabilirler.</span><span class="sxs-lookup"><span data-stu-id="65d95-106">With release 10.0 of Retail, a store manager can open the **Price** report by navigating to **All stores \> Store \> Price report** and viewing the updated prices for the products associated to the store.</span></span> 

<span data-ttu-id="65d95-107">Fiyat raporunu etkinleştirmek için **Mağaza için fiyat raporunu etkinleştir** parametresinin açık olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="65d95-107">To enable the price report, the **Enable price report for store** parameter must be turned on.</span></span> <span data-ttu-id="65d95-108">Bu parametre **Ticaret parametreleri \> İskontolar \> Çeşitli** sekmesinde bulunur. **Fiyat raporu** sayfasını açmak, çeşitli yapılandırmaları içeren bir iletişim kutusunu görüntüler.</span><span class="sxs-lookup"><span data-stu-id="65d95-108">This parameter is located on the **Commerce parameters \> Discounts \> Miscellaneous** tab. Opening the **Price report** page displays a dialog box with various configurations.</span></span> <span data-ttu-id="65d95-109">Kullanılabilir yapılandırmalar aşağıda listelenmiştir.</span><span class="sxs-lookup"><span data-stu-id="65d95-109">The available configurations are listed below.</span></span>

| <span data-ttu-id="65d95-110">Konfigürasyon</span><span class="sxs-lookup"><span data-stu-id="65d95-110">Configuration</span></span> | <span data-ttu-id="65d95-111">Açıklama</span><span class="sxs-lookup"><span data-stu-id="65d95-111">Description</span></span> |
|---|---|
| <span data-ttu-id="65d95-112">Başlangıç tarihi / Bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="65d95-112">From date / To date</span></span>| <span data-ttu-id="65d95-113">Fiyat raporunun oluşturulacağı veri aralığı.</span><span class="sxs-lookup"><span data-stu-id="65d95-113">The date range for which the price report should be generated.</span></span> <span data-ttu-id="65d95-114">Güncel süre sınırı 7 gündür.</span><span class="sxs-lookup"><span data-stu-id="65d95-114">The duration is currently limited to 7 days.</span></span> |
| <span data-ttu-id="65d95-115">Kanal</span><span class="sxs-lookup"><span data-stu-id="65d95-115">Channel</span></span>| <span data-ttu-id="65d95-116">Fiyat raporunun oluşturulacağı mağazası.</span><span class="sxs-lookup"><span data-stu-id="65d95-116">The store for which the price report should be generated.</span></span> |
| <span data-ttu-id="65d95-117">Ürünleri kullanılabilir stokla birlikte görüntüle</span><span class="sxs-lookup"><span data-stu-id="65d95-117">Display products with available inventory</span></span>| <span data-ttu-id="65d95-118">Bunu **Evet** olarak ayarlamak, mağazada yalnızca fiziksel stoku bulunan ürünler için fiyatları listeler.</span><span class="sxs-lookup"><span data-stu-id="65d95-118">Setting this to **Yes** will show the prices for only those products which currently have physical inventory available in the store.</span></span> |
| <span data-ttu-id="65d95-119">Çeşitler için fiyatları görüntüle</span><span class="sxs-lookup"><span data-stu-id="65d95-119">Display prices for variants</span></span> | <span data-ttu-id="65d95-120">Bunu **Evet** olarak ayarlamak, ana ürünlerle birlikte ürün çeşitlerinin de fiyatlarını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="65d95-120">Setting this to **Yes** will display the prices of the variants along with the product masters.</span></span> <span data-ttu-id="65d95-121">Bu yalnızca çeşide özel fiyatlarınız varsa **Açık** olarak seçilmelidir, çünkü satırların sayısı çok artar.</span><span class="sxs-lookup"><span data-stu-id="65d95-121">This should only be turned **On** if you have variant-specific prices, because the number of rows grows very large.</span></span> <span data-ttu-id="65d95-122">Gelecekteki sürümlerde, boyuta bağlı fiyatları etkileştireceğiz ve böylece mağaza yöneticisi, fiyatların görüntülenmesi istediği boyutları seçebilecek.</span><span class="sxs-lookup"><span data-stu-id="65d95-122">In future releases, we will enable the dimensions-based prices so that the store manager can choose the dimensions for which the prices should be displayed.</span></span> |
| <span data-ttu-id="65d95-123">Ürünleri fiyat değişiklikleriyle birlikte görüntüle</span><span class="sxs-lookup"><span data-stu-id="65d95-123">Display products with price changes</span></span> | <span data-ttu-id="65d95-124">Bu ayarı **Evet** olarak işaretlemek, yalnızca fiyatların değiştiği tarihlerdeki fiyatları görüntüler.</span><span class="sxs-lookup"><span data-stu-id="65d95-124">Setting this to **Yes** will display the prices for only those dates on which the price has been changed.</span></span> <span data-ttu-id="65d95-125">*Bir önceki gün* fiyatı için seçilen **Başlangıç tarihi** her zaman görüntülenecektir, böylece mağaza yöneticisi seçilen sürenin tamamında fiyatları değişmemiş ürünleri kolayca tespit edebilir ve geçerli fiyatı da görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="65d95-125">The price for *one day before* the selected **From date** will always be displayed, so that the store manager can easily identity the products which have not changed prices for the entire selected duration, and can also view the current price.</span></span> |

<span data-ttu-id="65d95-126">Rapor oluşturulduktan sonra Excel dosyası ek filtreleme ihtiyaçlarını gidermek için indirilebilir.</span><span class="sxs-lookup"><span data-stu-id="65d95-126">After the report is generated, the Excel file can be downloaded for any additional filtering needs.</span></span> <span data-ttu-id="65d95-127">Fiyat raporu, geçmiş tarihlerdeki ürünlerin eski fiyatlarını denetlemek için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="65d95-127">The price report can also be used to check the historical prices of products for past dates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Global Stok Muhasebesi genel defteri
description: Bu konu, bir para birimi, takvim, kural ve tüzel kişilikle ilişkilendirme birleşimiyle tanımlanan Global Stok Muhasebesi genel defterlerini açıklar.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea3434675aa3b7f2304be93ef9b489747994fa9d
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273238"
---
# <a name="global-inventory-accounting-ledger"></a><span data-ttu-id="e7a11-103">Global Stok Muhasebesi genel defteri</span><span class="sxs-lookup"><span data-stu-id="e7a11-103">Global Inventory Accounting ledger</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="e7a11-104">Global Stok Muhasebesi'nin kendi genel muhasebe defterleri kümesi vardır.</span><span class="sxs-lookup"><span data-stu-id="e7a11-104">Global Inventory Accounting has its own set of ledgers.</span></span> <span data-ttu-id="e7a11-105">İlgili bir tüzel kişilik için stokla ilgili bir hareket işlendiğinde, sistem bu hareketi gerektiği gibi herhangi bir sayıdaki Global Stok Muhasebesi genel muhasebe defterlerinde hesaplayabilir.</span><span class="sxs-lookup"><span data-stu-id="e7a11-105">Each time an inventory-related transaction is processed for a relevant legal entity, the system can account for that transaction in any number of Global Inventory Accounting ledgers, as required.</span></span>

<span data-ttu-id="e7a11-106">Genel muhasebe defteri, borç ve alacak ölçümlerinin bir kaydıdır.</span><span class="sxs-lookup"><span data-stu-id="e7a11-106">A ledger is a register of debit and credit measures.</span></span> <span data-ttu-id="e7a11-107">Bu ölçümler maliyet öğeleri ve yardımcı muhasebe hesapları kullanılarak sınıflandırılır.</span><span class="sxs-lookup"><span data-stu-id="e7a11-107">These measures are classified by using cost elements and subledger accounts.</span></span> <span data-ttu-id="e7a11-108">Global Stok Muhasebesi genel muhasebe defteri bir para birimi, takvim, kural ve tüzel kişilikle ilişkilendirme birleşimiyle tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="e7a11-108">A Global Inventory Accounting ledger is defined by its combination of a currency, a calendar, a convention, and an association with a legal entity.</span></span>

<span data-ttu-id="e7a11-109">Global Stok Muhasebesi defterlerinizi ayarlamak için **Global stok muhasebesi \> Ayar \>Global tok muhasebesi defterleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e7a11-109">To set up your Global Inventory Accounting ledgers, go to **Global inventory accounting \> Setup \> Global inventory accounting ledgers**.</span></span> <span data-ttu-id="e7a11-110">Her genel muhasebe defteri için aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="e7a11-110">For each ledger, set the following fields:</span></span>

- <span data-ttu-id="e7a11-111">**Ad**: Defterin adını girin.</span><span class="sxs-lookup"><span data-stu-id="e7a11-111">**Name** – Enter the name of the ledger.</span></span>
- <span data-ttu-id="e7a11-112">**Açıklama**: Defterin açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="e7a11-112">**Description** – Enter a description of the ledger.</span></span>
- <span data-ttu-id="e7a11-113">**Mali takvim**: Genel muhasebe defteri için mali takvimi belirtin.</span><span class="sxs-lookup"><span data-stu-id="e7a11-113">**Fiscal calendar** – Specify the fiscal calendar for the ledger.</span></span>
- <span data-ttu-id="e7a11-114">**Para birimi ve döviz kuru türü**: Genel muhasebe defterinin kullandığı muhasebe para birimini ve döviz kuru türünü seçmek için bu hızlı sekmedeki alanları kullanın.</span><span class="sxs-lookup"><span data-stu-id="e7a11-114">**Currency and exchange rate type** – Use the fields on this FastTab to select the accounting currency that the ledger uses, and the exchange rate type.</span></span> <span data-ttu-id="e7a11-115">Seçtiğiniz para birimi tüzel kişiliğin kullandığı para biriminden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="e7a11-115">The currency that you select can differ from the currency that the legal entity uses.</span></span> <span data-ttu-id="e7a11-116">Global Stok Muhasebesi'nde, kullanıcılar istedikleri kadar maliyetlendirme genel defteri tanımlayabilir.</span><span class="sxs-lookup"><span data-stu-id="e7a11-116">In Global Inventory Accounting, users can define as many costing ledgers as they require.</span></span> <span data-ttu-id="e7a11-117">Global Stok Muhasebesi, birden fazla para biriminde ve birden fazla değerlemede stok muhasebesini destekler.</span><span class="sxs-lookup"><span data-stu-id="e7a11-117">Global Inventory Accounting supports inventory accounting in multiple currencies and in multiple valuations.</span></span> <span data-ttu-id="e7a11-118">Aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="e7a11-118">Set the following fields:</span></span>

    - <span data-ttu-id="e7a11-119">**Para Birimi**: Stokla ilgili değerlerin tutulduğu maliyetlendirme para birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="e7a11-119">**Currency** – Select the costing currency that inventory-related values are maintained in.</span></span> <span data-ttu-id="e7a11-120">Bu değerler stok değerini, satılan malların maliyetini, transitteki stoğu ve her türlü farkı içerir.</span><span class="sxs-lookup"><span data-stu-id="e7a11-120">These values include the inventory value, cost of goods sold, inventory in transit, and all kinds of variance.</span></span>
    - <span data-ttu-id="e7a11-121">**Döviz kuru türü**: Hareket para birimi cinsinden hareket tutarını ve maddelerin standart maliyetini maliyet para birimine dönüştürmek için sistemin kullanması gereken döviz kurunu seçin.</span><span class="sxs-lookup"><span data-stu-id="e7a11-121">**Exchange rate type** – Select the exchange rate that the system should use to convert the transaction amount in the transaction currency and the standard cost of the items into the costing currency.</span></span>

- <span data-ttu-id="e7a11-122">**Kural adı**: Bir kural belirtin.</span><span class="sxs-lookup"><span data-stu-id="e7a11-122">**Convention name** – Specify a convention.</span></span> <span data-ttu-id="e7a11-123">Kural, maliyetlerin bu genel muhasebede nasıl hesaplanacağını belirleyen ilkeler topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="e7a11-123">A convention is a collection of policies that establish how costs will be accounted in this ledger.</span></span>
- <span data-ttu-id="e7a11-124">**Tüzel kişilik**: Genel muhasebe, seçili tüzel kişiliğe nakledilen belgeleri muhasebeleştirecektir.</span><span class="sxs-lookup"><span data-stu-id="e7a11-124">**Legal entity** – The ledger will account the documents that are posted to the selected legal entity.</span></span>
- <span data-ttu-id="e7a11-125">**Hazırlama**: Genel muhasebe oluşturulmadan önce oluşturulan stok hareketlerinin genel muhasebedeki para birimine ve kurala göre işlenip işlenmeyeceğini seçin.</span><span class="sxs-lookup"><span data-stu-id="e7a11-125">**Priming** – Select whether inventory transactions that were created before the ledger was created should be processed according to the currency and convention in the ledger.</span></span> <span data-ttu-id="e7a11-126">Aşağıdaki değerlerden birini seçin:</span><span class="sxs-lookup"><span data-stu-id="e7a11-126">Select one of the following values:</span></span>

    - <span data-ttu-id="e7a11-127">**Etkinleştirildi**: Genel muhasebe, genel muhasebe oluşturulmadan önce oluşturulan hareketleri işlemelidir.</span><span class="sxs-lookup"><span data-stu-id="e7a11-127">**Activated** – The ledger should process transactions that were created before the ledger was created.</span></span>
    - <span data-ttu-id="e7a11-128">**Devre dışı**: Genel muhasebe, yalnızca genel muhasebe oluşturulduktan sonra oluşturulan hareketleri işlemelidir.</span><span class="sxs-lookup"><span data-stu-id="e7a11-128">**Deactivated** – The ledger should process only transactions that are created after the ledger was created.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="e7a11-129">Yeni belgeler girdikten sonra geri dönüp bu alanı **ayarlayamazsınız**.</span><span class="sxs-lookup"><span data-stu-id="e7a11-129">You will **not** be able to come back and set this field after you enter new documents.</span></span>

- <span data-ttu-id="e7a11-130">**Durum**: Sistem, yeni oluşturulan genel muhasebe defterlerinin durumunu otomatik olarak *Hazırla* olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e7a11-130">**Status** – The system automatically sets the status of newly created ledgers to *Prepare*.</span></span>

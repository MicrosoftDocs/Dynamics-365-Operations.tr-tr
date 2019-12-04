---
title: Bir talep tahmin hesaplarken, geçmiş işlem verilerinden aykırı değerleri kaldırın.
description: Bu makale bir talep tahmini hesaplamak için kullanılan geçmiş verilerden aykırı değerlerin nasıl dışarıda bırakılabileceğini açıklamaktadır. Aykırı değerleri dışarıda bırakarak tahmin doğruluğunu artırabilirsiniz.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0373448cba908c1ba3889c3e533c205e0410bab8
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813628"
---
# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a><span data-ttu-id="0f743-104">Bir talep tahmin hesaplarken, geçmiş işlem verilerinden aykırı değerleri kaldırın.</span><span class="sxs-lookup"><span data-stu-id="0f743-104">Remove outliers from historical transaction data when calculating a demand forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f743-105">Bu makale bir talep tahmini hesaplamak için kullanılan geçmiş verilerden aykırı değerlerin nasıl dışarıda bırakılabileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="0f743-105">This article describes how to exclude outliers from the historical data that is used to calculate a demand forecast.</span></span> <span data-ttu-id="0f743-106">Aykırı değerleri dışarıda bırakarak tahmin doğruluğunu artırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f743-106">By excluding outliers, you can improve forecast accuracy.</span></span>

<span data-ttu-id="0f743-107">Tahmin doğruluğunu artırmak için aykırı değerleri dışarıda bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f743-107">You can exclude outliers to improve forecast accuracy.</span></span> <span data-ttu-id="0f743-108">Bu isteğe bağlı bir görevdir.</span><span class="sxs-lookup"><span data-stu-id="0f743-108">This is an optional task.</span></span> <span data-ttu-id="0f743-109">İşleme genel bakış:</span><span class="sxs-lookup"><span data-stu-id="0f743-109">Here is an overview of the process:</span></span>

1.  <span data-ttu-id="0f743-110">Dışarıda bırakılacak hareketleri seçmek için bir sorgu kullanabileceğiniz **Aykırı değerleri temizleme** sayfasını açmak için **Master planlama** &gt; **Kurulum** &gt; **Talep tahmini** &gt; **Aykırı değerleri temizle** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0f743-110">Click **Master planning** &gt; **Setup** &gt; **Demand forecasting** &gt; **Outlier removal** to open the **Outlier removal** page, where you can use a query to select the transactions to exclude.</span></span>
2.  <span data-ttu-id="0f743-111">Sorgunun uygulandığı şirketi seçin ve sonra isim ve açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="0f743-111">Select the company that the query applies to, and then enter a name and description.</span></span> <span data-ttu-id="0f743-112">**Sorgu tarihi** alanı otomatik olarak mevcut tarih olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="0f743-112">The **Query date** field is automatically set to the current date.</span></span>
3.  <span data-ttu-id="0f743-113">Sorgunun bulacağı hareketlerden geçmişe dönük verileri çıkarmak için **Etkin** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="0f743-113">Select the **Active** check box to exclude the transactions that the query finds from the historical data.</span></span> <span data-ttu-id="0f743-114">Bu ayar, bir temel tahmin oluşturduğunuzda etkin olacaktır.</span><span class="sxs-lookup"><span data-stu-id="0f743-114">This setting will take effect when you create a baseline forecast.</span></span>
4.  <span data-ttu-id="0f743-115">**Aykırı değer temizleme sorgu** sayfası üzerinde ekleme, kaldırma ve temel tahmini hesaplanırken hangi hareketlerin hariç tutulacağını tanımlayan ölçütü seçin.</span><span class="sxs-lookup"><span data-stu-id="0f743-115">On the **Outlier removal query** page, you can add, remove, and select the criteria that define which transactions will be excluded when the baseline forecast is calculated.</span></span> <span data-ttu-id="0f743-116">Örneğin, dışlamak için belirli bir madde veya sipariş hareketini seçin.</span><span class="sxs-lookup"><span data-stu-id="0f743-116">For example, select a specific item or order transaction to exclude.</span></span>
5.  <span data-ttu-id="0f743-117">**Hareketleri görüntüle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0f743-117">Click **Display transactions**.</span></span> <span data-ttu-id="0f743-118">**Aykırı değer hareketleri** sayfası sorguda belirlediğiniz ve talep tahmini hesaplandığında geçmişe dönük verilerden hariç tutulacak kriterlere karşılık gelen hareketleri listeler.</span><span class="sxs-lookup"><span data-stu-id="0f743-118">The **Outlier transactions** page lists the transactions that meet the criteria that you defined in the query, and that will be excluded from the historical data when the demand forecast is calculated.</span></span>

<span data-ttu-id="0f743-119">**Not:** Ayrıca var olan bir sorguyu temel alan bir sorgu da oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f743-119">**Note:** You can also create a query that is based on an existing query.</span></span> <span data-ttu-id="0f743-120">Kopyalanacak sorguyu seçin ve sonra **Tekrarlama**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0f743-120">Select the query to copy, and then click **Duplicate**.</span></span> <span data-ttu-id="0f743-121">**Sorgu tarihi** alanı, sürümü tanımlar.</span><span class="sxs-lookup"><span data-stu-id="0f743-121">The **Query date** field identifies the version.</span></span> <span data-ttu-id="0f743-122">Sorguyu olduğu gibi kullanabilir veya **Sorguyu düzenle**'yi tıklayıp ölçütü değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f743-122">You can use the query as it is, or you can click **Edit query** to modify the criteria.</span></span> <span data-ttu-id="0f743-123">İsteğe bağlı olarak, yeni sorgunun adını ve açıklamasını değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f743-123">You can optionally modify the name and description of the new query.</span></span>

<a name="additional-resources"></a><span data-ttu-id="0f743-124">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0f743-124">Additional resources</span></span>
--------

[<span data-ttu-id="0f743-125">Talep tahminine genel bakış</span><span class="sxs-lookup"><span data-stu-id="0f743-125">Demand forecasting overview</span></span>](introduction-demand-forecasting.md)

[<span data-ttu-id="0f743-126">Tahmin doğruluğunu izleme</span><span class="sxs-lookup"><span data-stu-id="0f743-126">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)




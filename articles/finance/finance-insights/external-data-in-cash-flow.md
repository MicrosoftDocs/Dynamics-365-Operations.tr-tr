---
title: Nakit akışı tahminlerinde dış verileri kullanma (önizleme)
description: Bu konuda, dış verilerin nakit akışı tahminlerine girilebilmesi veya içeri aktarılması için tamamlamanız gereken kurulum adımları açıklanmıştır.
author: rcarlson
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 66bdb8bd638859bb4fc5565e3f12a8f671addcff
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186702"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="8d79f-103">Nakit akışı tahminlerinde dış verileri kullanma (önizleme)</span><span class="sxs-lookup"><span data-stu-id="8d79f-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8d79f-104">Dış veriler nakit akışı tahminlerine girilebilir veya içeri aktarılabilir.</span><span class="sxs-lookup"><span data-stu-id="8d79f-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="8d79f-105">Bu konu, dış verilerin kullanılmasına özgü kurulum adımlarını ve dış verilerin nakit akışı tahminine eklenmesini sağlayan adımları açıklar.</span><span class="sxs-lookup"><span data-stu-id="8d79f-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="8d79f-106">Dış verilerin kurulumu</span><span class="sxs-lookup"><span data-stu-id="8d79f-106">External data setup</span></span>

<span data-ttu-id="8d79f-107">Nakit akışı tahminlerinde dış verilerin kullanımını destekleyen ayarlar girmek için **Nakit akışı tahmin kurulum** sayfasındaki **Dış kaynak** sekmesini (**Nakit ve banka yönetimi \> Nakit akışı tahmini**) kullanın.</span><span class="sxs-lookup"><span data-stu-id="8d79f-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="8d79f-108">Bu kurulum hakkında daha fazla bilgi için bkz. [Nakit akışı tahmini](../cash-bank-management/cash-flow-forecasting.md).</span><span class="sxs-lookup"><span data-stu-id="8d79f-108">For more information about the setup, see [Cash flow forecasting](../cash-bank-management/cash-flow-forecasting.md).</span></span>

<span data-ttu-id="8d79f-109">Nakit akışı tahminlerine dış veriler girmek için dış verileri girerken ve değiştirirken Excel'de Aç deneyimini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8d79f-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="8d79f-110">**Dış veri** düğmesini seçin ve ardından **Dış Veri Ekle** veya **Mevcut dış verileri düzenle** seçeneklerinden birini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="8d79f-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="8d79f-111">Microsoft Excel dosyası açıldığında, aşağıdaki alanlara bilgi girebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="8d79f-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="8d79f-112">**Giriş Kodu**</span><span class="sxs-lookup"><span data-stu-id="8d79f-112">**Entry ID**</span></span>
- <span data-ttu-id="8d79f-113">**Açıklama** (isteğe bağlı)</span><span class="sxs-lookup"><span data-stu-id="8d79f-113">**Description** (optional)</span></span>
- <span data-ttu-id="8d79f-114">**Dış Kaynak adı**: Mali İçgörüleri ayarlarken tanımladığınız listedeki değerlerden birini seçin.</span><span class="sxs-lookup"><span data-stu-id="8d79f-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="8d79f-115">**Tüzel Kişilik**</span><span class="sxs-lookup"><span data-stu-id="8d79f-115">**Legal Entity**</span></span>
- <span data-ttu-id="8d79f-116">**Date**</span><span class="sxs-lookup"><span data-stu-id="8d79f-116">**Date**</span></span>
- <span data-ttu-id="8d79f-117">**Hareket para birimi cinsinden tutar**</span><span class="sxs-lookup"><span data-stu-id="8d79f-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="8d79f-118">**Para Birimi Kodu**</span><span class="sxs-lookup"><span data-stu-id="8d79f-118">**Currency Code**</span></span>
- <span data-ttu-id="8d79f-119">**Varsayılan Boyut** (isteğe bağlı)</span><span class="sxs-lookup"><span data-stu-id="8d79f-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="8d79f-120">**Belge numarası** (isteğe bağlı)</span><span class="sxs-lookup"><span data-stu-id="8d79f-120">**Document number** (optional)</span></span>
- <span data-ttu-id="8d79f-121">**Hesap numarası** (isteğe bağlı)</span><span class="sxs-lookup"><span data-stu-id="8d79f-121">**Account number** (optional)</span></span>
- <span data-ttu-id="8d79f-122">**Hesap adı** (isteğe bağlı)</span><span class="sxs-lookup"><span data-stu-id="8d79f-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="8d79f-123">Veri Yönetimi çerçevesi kullanarak dış verileri içe aktarma</span><span class="sxs-lookup"><span data-stu-id="8d79f-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="8d79f-124">**Veri Yönetimi** çalışma alanı ve **Nakit akışı tahmini dış kaynak girişi** olarak adlandırılan varlığı kullanarak nakit akışı tahminleri için dış verileri içeri aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8d79f-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="8d79f-125">Ek olarak, kurulum verilerini bir ortamdan diğerine taşımanız gerekiyorsa gereken kurulum tablolarında aşağıdaki varlıklar alanı kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="8d79f-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="8d79f-126">Nakit akışı tahmini harici kaynak ayarı</span><span class="sxs-lookup"><span data-stu-id="8d79f-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="8d79f-127">Nakit akışı tahmini harici kaynak tüzel kişiliği ayarı</span><span class="sxs-lookup"><span data-stu-id="8d79f-127">Cash flow forecast external source legal entity setup</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

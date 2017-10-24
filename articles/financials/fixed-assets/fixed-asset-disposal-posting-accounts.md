---
title: "Sabit kıymet elden çıkarma deftere nakil hesapları"
description: "Bu makalede, genel muhasebe deftere nakil hesaplarının kıymetlerin elden çıkarılmasına yönelik nasıl ayarlanacağı açıklanmaktadır."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0129eae177d44100b09c2b7bce553dd5bde5ce0c
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="806fd-103">Sabit kıymet elden çıkarma deftere nakil hesapları</span><span class="sxs-lookup"><span data-stu-id="806fd-103">Fixed asset disposal posting accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="806fd-104">Bu makalede, genel muhasebe deftere nakil hesaplarının kıymetlerin elden çıkarılmasına yönelik nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="806fd-104">This article explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="806fd-105">Sabit kıymet deftere nakil profilleri sayfasında, Genel muhasebe hesapları FastTab'de, Elden çıkarma - satış ve Elden çıkarma - ıskarta seçeneklerini belirleyerek genel muhasebeye nakilleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="806fd-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="806fd-106">Her iki hareket tipi için de, sabit kıymetin elden çıkarma değeri için genel muhasebe hesabına alacak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="806fd-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="806fd-107">Borç, örneğin bir banka hesabı olabilen mahsup hesaba nakledilir.</span><span class="sxs-lookup"><span data-stu-id="806fd-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="806fd-108">Müşteriye sabit bir varlık satılırsa, mahsup hesabı yerine müşteri hesabı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="806fd-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="806fd-109">Elden çıkarma seçeneğine, ardından Satış veya Iskarta seçeneğine tıklayın, sonra da sabit kıymetin net defter değerini tersine çevirmek için ayrıntılı hesaplar ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="806fd-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="806fd-110">Ayrıca Elden çıkarma parametreleri sayfasındaki Nakledilecek değer ve Satış değeri alanlarına bilgi de girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="806fd-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="806fd-111">Düşük değer havuzundaki bir kıymete ilişkin elden çıkarma hareketi, düşük değer havuzunun net defter değerini yalnızca elden çıkarılan tutar kadar düşürür.</span><span class="sxs-lookup"><span data-stu-id="806fd-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="806fd-112">Ancak, bir kıymetin satışı düşük değer havuzunun net defter değerini geçtiğinde, net defter değeri sıfıra düşer.</span><span class="sxs-lookup"><span data-stu-id="806fd-112">However, when the sale of an asset is exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>







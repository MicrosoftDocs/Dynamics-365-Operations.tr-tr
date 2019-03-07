---
title: Sabit kıymeti elden çıkarma deftere nakil hesapları
description: Bu konuda, genel muhasebe deftere nakil hesaplarının kıymetlerin elden çıkarılmasına yönelik nasıl ayarlanacağı açıklanmaktadır.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8e00c00b0cb7058858fde3774941911ce20fb6f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "367191"
---
# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="4738a-103">Sabit kıymeti elden çıkarma deftere nakil hesapları</span><span class="sxs-lookup"><span data-stu-id="4738a-103">Fixed asset disposal posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4738a-104">Bu konuda, genel muhasebe deftere nakil hesaplarının kıymetlerin elden çıkarılmasına yönelik nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4738a-104">This topic explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="4738a-105">Sabit kıymet deftere nakil profilleri sayfasında, Genel muhasebe hesapları FastTab'de, Elden çıkarma - satış ve Elden çıkarma - ıskarta seçeneklerini belirleyerek genel muhasebeye nakilleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4738a-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="4738a-106">Her iki hareket tipi için de, sabit kıymetin elden çıkarma değeri için genel muhasebe hesabına alacak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="4738a-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="4738a-107">Borç, örneğin bir banka hesabı olabilen mahsup hesaba nakledilir.</span><span class="sxs-lookup"><span data-stu-id="4738a-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="4738a-108">Müşteriye sabit bir varlık satılırsa, mahsup hesabı yerine müşteri hesabı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4738a-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="4738a-109">Elden çıkarma seçeneğine, ardından Satış veya Iskarta seçeneğine tıklayın, sonra da sabit kıymetin net defter değerini tersine çevirmek için ayrıntılı hesaplar ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4738a-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="4738a-110">Ayrıca Elden çıkarma parametreleri sayfasındaki Nakledilecek değer ve Satış değeri alanlarına bilgi de girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4738a-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="4738a-111">Düşük değer havuzundaki bir kıymete ilişkin elden çıkarma hareketi, düşük değer havuzunun net defter değerini yalnızca elden çıkarılan tutar kadar düşürür.</span><span class="sxs-lookup"><span data-stu-id="4738a-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="4738a-112">Ancak, bir kıymetin satışı düşük değer havuzunun net defter değerini geçtiğinde, net defter değeri sıfıra düşer.</span><span class="sxs-lookup"><span data-stu-id="4738a-112">However, when the sale of an asset exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>






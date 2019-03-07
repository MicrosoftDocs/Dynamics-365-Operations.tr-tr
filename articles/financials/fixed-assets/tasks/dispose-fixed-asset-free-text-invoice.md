---
title: Serbest metin faturası kullanarak sabit kıymeti elden çıkarma
description: Bu yordam, Sabit kıymetler günlüğündeki alım teklifi kullanılarak bir sabit kıymetin nasıl alındığını gösterir.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c58cef0609c8f931eace13ee0dec89f3eee7fed
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "310749"
---
# <a name="dispose-of-a-fixed-asset-using-a-free-text-invoice"></a><span data-ttu-id="ed897-103">Serbest metin faturası kullanarak sabit kıymeti elden çıkarma</span><span class="sxs-lookup"><span data-stu-id="ed897-103">Dispose of a fixed asset using a free text invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ed897-104">Bu prosedür, serbest metin faturası kullanarak bir sabit kıymetin nasıl elden çıkarılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed897-104">This procedure shows how to dispose of a fixed asset using the free text invoice.</span></span>

1. <span data-ttu-id="ed897-105">Alacak hesapları > Faturalar > Tüm serbest metin faturaları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ed897-105">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="ed897-106">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ed897-106">Click New.</span></span>
3. <span data-ttu-id="ed897-107">Müşteri hesabı alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="ed897-107">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="ed897-108">Varsayılan fatura tarihini doğrulama ve düzenleme (varsa).</span><span class="sxs-lookup"><span data-stu-id="ed897-108">Validate the default Invoice date and edit if applicable.</span></span>
5. <span data-ttu-id="ed897-109">Kalan varsayılan başlık alanlarını, örneğin Para birimi gibi doğrulayın ve gerekirse düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="ed897-109">Validate remaining default header fields, such as Currency and edit if applicable.</span></span>
6. <span data-ttu-id="ed897-110">Fatura satırına bir Açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="ed897-110">Enter a Description into the invoice line.</span></span>
7. <span data-ttu-id="ed897-111">Fatura satırı için Ana hesabı girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="ed897-111">Enter or select the Main account for the invoice line.</span></span>
8. <span data-ttu-id="ed897-112">Varsayılan Satış vergisi grubunu ve Madde satış vergisi grubunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="ed897-112">Validate the default Sales tax group and Item sales tax group.</span></span>
9. <span data-ttu-id="ed897-113">Sabit kıymetin Birim fiyatını veya Satış miktarını girin.</span><span class="sxs-lookup"><span data-stu-id="ed897-113">Enter the Unit price or hte Amount of the sale of the fixed asset.</span></span>
10. <span data-ttu-id="ed897-114">Satır ayrıntılarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ed897-114">Click Line details.</span></span>  
11. <span data-ttu-id="ed897-115">Satılacak Sabit kıymet numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="ed897-115">Select the Fixed asset number to be sold.</span></span>
12. <span data-ttu-id="ed897-116">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ed897-116">Click Post.</span></span>


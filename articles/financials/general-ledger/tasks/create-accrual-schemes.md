---
title: Tahakkuk planları oluşturma
description: Bu görev kılavuzu, hesap tahakkuk düzeni oluşturmayı adım adım açıklar.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ce96ccfb0dc3e4a723af967147dae93772c5b44f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553143"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="94a2c-103">Tahakkuk planları oluşturma</span><span class="sxs-lookup"><span data-stu-id="94a2c-103">Create accrual schemes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="94a2c-104">Bu görev kılavuzu, hesap tahakkuk düzeni oluşturmayı adım adım açıklar.</span><span class="sxs-lookup"><span data-stu-id="94a2c-104">This task guide steps through creating an accrual scheme.</span></span> <span data-ttu-id="94a2c-105">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="94a2c-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="94a2c-106">Genel muhasebe > Günlük kurulumu > Tahakkuk düzenleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="94a2c-106">Go to General ledger > Journal setup > Accrual schemes.</span></span>
2. <span data-ttu-id="94a2c-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="94a2c-107">Click New.</span></span>
3. <span data-ttu-id="94a2c-108">Tahakkuk tanımlaması alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="94a2c-108">In the Accrual identification field, type a value.</span></span>
4. <span data-ttu-id="94a2c-109">Tahakkuk düzeninin Açıklama alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="94a2c-109">In the Description of accrual scheme field, type a value.</span></span>
5. <span data-ttu-id="94a2c-110">Borç alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="94a2c-110">In the Debit field, specify the desired values.</span></span>
    * <span data-ttu-id="94a2c-111">Tanımlanan ana hesap, günlük fiş satırında borç ana hesabıyla değiştirilir ve genel muhasebe tahakkuk hareketlerine bağlı olarak ertelemenin tersine çevrilmesi için de kullanılır.</span><span class="sxs-lookup"><span data-stu-id="94a2c-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="94a2c-112">Alacak alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="94a2c-112">In the Credit field, specify the desired values.</span></span>
    * <span data-ttu-id="94a2c-113">Tanımlanan ana hesap, günlük fiş satırında alacak ana hesabıyla değiştirilir ve genel muhasebe tahakkuk hareketlerine bağlı olarak ertelemenin tersine çevrilmesi için de kullanılır.</span><span class="sxs-lookup"><span data-stu-id="94a2c-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="94a2c-114">Fiş alanında, hareketler deftere nakledildiğinde fişin nasıl belirlenmesini istediğinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="94a2c-114">In the Voucher field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="94a2c-115">Açıklama alanında, deftere nakledilecek hareketleri açıklayacak bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="94a2c-115">In the Description field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="94a2c-116">Dönem sıklığı alanında, hareketlerin ne sıklıkta gerçekleşmesi gerektiğini seçin.</span><span class="sxs-lookup"><span data-stu-id="94a2c-116">In the Period frequency field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="94a2c-117">Döneme göre oluşum sayısı alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="94a2c-117">In the Number of occurrences by period field, enter a number.</span></span>
11. <span data-ttu-id="94a2c-118">Hareketleri naklet alanında, hareketlerin deftere nakledilmesi gereken Aylık vb. gibi bir süre seçin.</span><span class="sxs-lookup"><span data-stu-id="94a2c-118">In the Post transactions field, select when the transactions should be posted, such as Monthly.</span></span>


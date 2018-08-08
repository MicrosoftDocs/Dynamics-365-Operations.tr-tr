--- 
title: "Tahakkuk planları oluşturma"
description: "Bu görev kılavuzu, hesap tahakkuk düzeni oluşturmayı adım adım açıklar."
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 10f585577c094bfedcd0f0835ed08e1f73c6e476
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---
# <a name="create-accrual-schemes"></a><span data-ttu-id="12b53-103">Tahakkuk planları oluşturma</span><span class="sxs-lookup"><span data-stu-id="12b53-103">Create accrual schemes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="12b53-104">Bu görev kılavuzu, hesap tahakkuk düzeni oluşturmayı adım adım açıklar.</span><span class="sxs-lookup"><span data-stu-id="12b53-104">This task guide steps through creating an accrual scheme.</span></span> <span data-ttu-id="12b53-105">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="12b53-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="12b53-106">Genel muhasebe > Günlük kurulumu > Tahakkuk düzenleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="12b53-106">Go to General ledger > Journal setup > Accrual schemes.</span></span>
2. <span data-ttu-id="12b53-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="12b53-107">Click New.</span></span>
3. <span data-ttu-id="12b53-108">Tahakkuk tanımlaması alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="12b53-108">In the Accrual identification field, type a value.</span></span>
4. <span data-ttu-id="12b53-109">Tahakkuk düzeninin Açıklama alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="12b53-109">In the Description of accrual scheme field, type a value.</span></span>
5. <span data-ttu-id="12b53-110">Borç alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="12b53-110">In the Debit field, specify the desired values.</span></span>
    * <span data-ttu-id="12b53-111">Tanımlanan ana hesap, günlük fiş satırında borç ana hesabıyla değiştirilir ve genel muhasebe tahakkuk hareketlerine bağlı olarak ertelemenin tersine çevrilmesi için de kullanılır.</span><span class="sxs-lookup"><span data-stu-id="12b53-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="12b53-112">Alacak alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="12b53-112">In the Credit field, specify the desired values.</span></span>
    * <span data-ttu-id="12b53-113">Tanımlanan ana hesap, günlük fiş satırında alacak ana hesabıyla değiştirilir ve genel muhasebe tahakkuk hareketlerine bağlı olarak ertelemenin tersine çevrilmesi için de kullanılır.</span><span class="sxs-lookup"><span data-stu-id="12b53-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="12b53-114">Fiş alanında, hareketler deftere nakledildiğinde fişin nasıl belirlenmesini istediğinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="12b53-114">In the Voucher field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="12b53-115">Açıklama alanında, deftere nakledilecek hareketleri açıklayacak bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="12b53-115">In the Description field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="12b53-116">Dönem sıklığı alanında, hareketlerin ne sıklıkta gerçekleşmesi gerektiğini seçin.</span><span class="sxs-lookup"><span data-stu-id="12b53-116">In the Period frequency field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="12b53-117">Döneme göre oluşum sayısı alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="12b53-117">In the Number of occurrences by period field, enter a number.</span></span>
11. <span data-ttu-id="12b53-118">Hareketleri naklet alanında, hareketlerin deftere nakledilmesi gereken Aylık vb. gibi bir süre seçin.</span><span class="sxs-lookup"><span data-stu-id="12b53-118">In the Post transactions field, select when the transactions should be posted, such as Monthly.</span></span>



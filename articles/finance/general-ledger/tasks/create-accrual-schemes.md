---
title: Tahakkuk planları oluşturma
description: Bu konu, bir tahakkuk planının nasıl oluşturulacağını açıklar.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e8f8cf8546187ae1c65d4966887e1c5842dff431
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175676"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="c9820-103">Tahakkuk planları oluşturma</span><span class="sxs-lookup"><span data-stu-id="c9820-103">Create accrual schemes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c9820-104">Bu konu, bir tahakkuk planının nasıl oluşturulacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="c9820-104">This topic explains how to create an accrual scheme.</span></span> <span data-ttu-id="c9820-105">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c9820-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="c9820-106">**Gezinti bölmesi > Modüller > Genel muhasebe > Günlük ayarı > Tahakkuk planı**.</span><span class="sxs-lookup"><span data-stu-id="c9820-106">Go to **Navigation pane > Modules > General ledger > Journal setup > Accrual schemes**.</span></span>
2. <span data-ttu-id="c9820-107">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c9820-107">Select **New**.</span></span>
3. <span data-ttu-id="c9820-108">**Tahakkuk tanımlaması** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c9820-108">In the **Accrual identification** field, type a value.</span></span>
4. <span data-ttu-id="c9820-109">**Tahakkuk düzeninin Açıklama** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c9820-109">In the **Description of accrual scheme** field, type a value.</span></span>
5. <span data-ttu-id="c9820-110">**Borç** alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="c9820-110">In the **Debit** field, specify the desired values.</span></span> <span data-ttu-id="c9820-111">Tanımlanan ana hesap, günlük fiş satırında borç ana hesabıyla değiştirilir ve genel muhasebe tahakkuk hareketlerine bağlı olarak ertelemenin tersine çevrilmesi için de kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c9820-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="c9820-112">**Alacak** alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="c9820-112">In the **Credit** field, specify the desired values.</span></span> <span data-ttu-id="c9820-113">Tanımlanan ana hesap, günlük fiş satırında alacak ana hesabıyla değiştirilir ve genel muhasebe tahakkuk hareketlerine bağlı olarak ertelemenin tersine çevrilmesi için de kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c9820-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="c9820-114">**Fiş** alanında, hareketler deftere nakledildiğinde fişin nasıl belirlenmesini istediğinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="c9820-114">In the **Voucher** field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="c9820-115">**Açıklama** alanında, deftere nakledilecek hareketleri açıklayacak bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c9820-115">In the **Description** field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="c9820-116">**Dönem sıklığı** alanında, hareketlerin ne sıklıkta gerçekleşmesi gerektiğini seçin.</span><span class="sxs-lookup"><span data-stu-id="c9820-116">In the **Period frequency** field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="c9820-117">**Döneme göre oluşum sayısı** alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="c9820-117">In the **Number of occurrences by period** field, enter a number.</span></span>
11. <span data-ttu-id="c9820-118">**Hareketleri naklet** alanında, hareketlerin deftere nakledilmesi gereken **Aylık** vb. gibi bir süre seçin.</span><span class="sxs-lookup"><span data-stu-id="c9820-118">In the **Post transactions** field, select when the transactions should be posted, such as **Monthly**.</span></span>


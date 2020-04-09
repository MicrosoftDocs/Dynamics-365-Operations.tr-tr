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
ms.openlocfilehash: a83870c4cec4de2e51e90ff1889d4beff6c23f95
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145211"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="e57c2-103">Tahakkuk planları oluşturma</span><span class="sxs-lookup"><span data-stu-id="e57c2-103">Create accrual schemes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e57c2-104">Bu konu, bir tahakkuk planının nasıl oluşturulacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="e57c2-104">This topic explains how to create an accrual scheme.</span></span> <span data-ttu-id="e57c2-105">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e57c2-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="e57c2-106">**Gezinti bölmesi > Modüller > Genel muhasebe > Günlük ayarı > Tahakkuk planı**.</span><span class="sxs-lookup"><span data-stu-id="e57c2-106">Go to **Navigation pane > Modules > General ledger > Journal setup > Accrual schemes**.</span></span>
2. <span data-ttu-id="e57c2-107">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e57c2-107">Select **New**.</span></span>
3. <span data-ttu-id="e57c2-108">**Tahakkuk tanımlaması** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="e57c2-108">In the **Accrual identification** field, type a value.</span></span>
4. <span data-ttu-id="e57c2-109">**Tahakkuk düzeninin Açıklama** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="e57c2-109">In the **Description of accrual scheme** field, type a value.</span></span>
5. <span data-ttu-id="e57c2-110">**Borç** alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="e57c2-110">In the **Debit** field, specify the desired values.</span></span> <span data-ttu-id="e57c2-111">Tanımlanan ana hesap, günlük fiş satırında borç ana hesabıyla değiştirilir ve genel muhasebe tahakkuk hareketlerine bağlı olarak ertelemenin tersine çevrilmesi için de kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e57c2-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="e57c2-112">**Alacak** alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="e57c2-112">In the **Credit** field, specify the desired values.</span></span> <span data-ttu-id="e57c2-113">Tanımlanan ana hesap, günlük fiş satırında alacak ana hesabıyla değiştirilir ve genel muhasebe tahakkuk hareketlerine bağlı olarak ertelemenin tersine çevrilmesi için de kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e57c2-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="e57c2-114">**Fiş** alanında, hareketler deftere nakledildiğinde fişin nasıl belirlenmesini istediğinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="e57c2-114">In the **Voucher** field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="e57c2-115">**Açıklama** alanında, deftere nakledilecek hareketleri açıklayacak bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="e57c2-115">In the **Description** field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="e57c2-116">**Dönem sıklığı** alanında, hareketlerin ne sıklıkta gerçekleşmesi gerektiğini seçin.</span><span class="sxs-lookup"><span data-stu-id="e57c2-116">In the **Period frequency** field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="e57c2-117">**Döneme göre oluşum sayısı** alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e57c2-117">In the **Number of occurrences by period** field, enter a number.</span></span>
11. <span data-ttu-id="e57c2-118">**Hareketleri naklet** alanında, hareketlerin deftere nakledilmesi gereken **Aylık** vb. gibi bir süre seçin.</span><span class="sxs-lookup"><span data-stu-id="e57c2-118">In the **Post transactions** field, select when the transactions should be posted, such as **Monthly**.</span></span>


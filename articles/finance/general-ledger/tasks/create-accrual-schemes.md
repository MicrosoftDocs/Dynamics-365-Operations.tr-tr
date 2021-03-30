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
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c021f71735e63c270e8f1998d77d4e4abcc5506
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236710"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="c3cda-103">Tahakkuk planları oluşturma</span><span class="sxs-lookup"><span data-stu-id="c3cda-103">Create accrual schemes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c3cda-104">Bu konu, bir tahakkuk planının nasıl oluşturulacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="c3cda-104">This topic explains how to create an accrual scheme.</span></span> <span data-ttu-id="c3cda-105">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c3cda-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="c3cda-106">**Gezinti bölmesi > Modüller > Genel muhasebe > Günlük ayarı > Tahakkuk planı**.</span><span class="sxs-lookup"><span data-stu-id="c3cda-106">Go to **Navigation pane > Modules > General ledger > Journal setup > Accrual schemes**.</span></span>
2. <span data-ttu-id="c3cda-107">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3cda-107">Select **New**.</span></span>
3. <span data-ttu-id="c3cda-108">**Tahakkuk tanımlaması** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c3cda-108">In the **Accrual identification** field, type a value.</span></span>
4. <span data-ttu-id="c3cda-109">**Tahakkuk düzeninin Açıklama** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c3cda-109">In the **Description of accrual scheme** field, type a value.</span></span>
5. <span data-ttu-id="c3cda-110">**Borç** alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="c3cda-110">In the **Debit** field, specify the desired values.</span></span> <span data-ttu-id="c3cda-111">Tanımlanan ana hesap, günlük fiş satırında borç ana hesabıyla değiştirilir ve genel muhasebe tahakkuk hareketlerine bağlı olarak ertelemenin tersine çevrilmesi için de kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c3cda-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="c3cda-112">**Alacak** alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="c3cda-112">In the **Credit** field, specify the desired values.</span></span> <span data-ttu-id="c3cda-113">Tanımlanan ana hesap, günlük fiş satırında alacak ana hesabıyla değiştirilir ve genel muhasebe tahakkuk hareketlerine bağlı olarak ertelemenin tersine çevrilmesi için de kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c3cda-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="c3cda-114">**Fiş** alanında, hareketler deftere nakledildiğinde fişin nasıl belirlenmesini istediğinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3cda-114">In the **Voucher** field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="c3cda-115">**Açıklama** alanında, deftere nakledilecek hareketleri açıklayacak bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c3cda-115">In the **Description** field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="c3cda-116">**Dönem sıklığı** alanında, hareketlerin ne sıklıkta gerçekleşmesi gerektiğini seçin.</span><span class="sxs-lookup"><span data-stu-id="c3cda-116">In the **Period frequency** field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="c3cda-117">**Döneme göre oluşum sayısı** alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="c3cda-117">In the **Number of occurrences by period** field, enter a number.</span></span>
11. <span data-ttu-id="c3cda-118">**Hareketleri naklet** alanında, hareketlerin deftere nakledilmesi gereken **Aylık** vb. gibi bir süre seçin.</span><span class="sxs-lookup"><span data-stu-id="c3cda-118">In the **Post transactions** field, select when the transactions should be posted, such as **Monthly**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
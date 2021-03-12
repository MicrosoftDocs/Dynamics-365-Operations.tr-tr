---
title: Ödeme için indirimleri işleme
description: Bu yordam, onaylanmış ve işlenmiş müşteri indirimlerini alacak dekontlarına dönüştürmeyi göstermektedir.
author: omulvad
manager: tfehr
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b1d32d94daef570e37a1a36d948fe18cd4041e46
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966167"
---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="db32f-103">Ödeme için indirimleri işleme</span><span class="sxs-lookup"><span data-stu-id="db32f-103">Process rebates for payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="db32f-104">Bu yordam, onaylanmış ve işlenmiş müşteri indirimlerini alacak dekontlarına dönüştürmeyi göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="db32f-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="db32f-105">Bu kılavuzu USMF demo şirketinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="db32f-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="db32f-106">Bu kılavuz için önkoşul İşaretli duruma sahip bir veya daha fazla indirim talep olmasıdır.</span><span class="sxs-lookup"><span data-stu-id="db32f-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="db32f-107">USMF kullanıyorsanız,"Müşteri indirimleri oluştur ve işle" kılavuzunu bu kılavuza başlamadan önce işleyin.</span><span class="sxs-lookup"><span data-stu-id="db32f-107">If you're using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="db32f-108">Alacak dekontunu indirim talebine dönüştürme</span><span class="sxs-lookup"><span data-stu-id="db32f-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="db32f-109">Tüm müşteriler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="db32f-109">Go to All customers.</span></span>
2. <span data-ttu-id="db32f-110">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="db32f-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="db32f-111">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="db32f-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="db32f-112">Eylem Bölmesinde, Tahsil et'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="db32f-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="db32f-113">Hareketleri kapat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="db32f-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="db32f-114">İşlevler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="db32f-114">Click Functions.</span></span>
7. <span data-ttu-id="db32f-115">İndirim programı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="db32f-115">Click Rebate program.</span></span>
    * <span data-ttu-id="db32f-116">Bu indirim sayfası müşteri indirim çalışma ekranında işlediğiniz ve İşaretli durumda olan indirim taleplerini listeler.</span><span class="sxs-lookup"><span data-stu-id="db32f-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="db32f-117">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="db32f-117">Click Edit.</span></span>
    * <span data-ttu-id="db32f-118">Alacak dekontuna dahil etmek istediğiniz talepler için İşaretle alanında onay işaretleri koyun.</span><span class="sxs-lookup"><span data-stu-id="db32f-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="db32f-119">İşlevler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="db32f-119">Click Functions.</span></span>
10. <span data-ttu-id="db32f-120">Alacak dekontu oluşturma'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="db32f-120">Click Create credit note.</span></span>
    * <span data-ttu-id="db32f-121">Bir günlüğün nakledildiğini bildiren bir ileti görüntülenir (Alacak hesapları parametreleri sayfasında belirtildiği gibi bu, alacak hesapları tüketim günlüğüdür).</span><span class="sxs-lookup"><span data-stu-id="db32f-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="db32f-122">Bu işlem gerçek borç (alacak) tutarının müşteri bakiyesine aktarılmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="db32f-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="db32f-123">Yani müşterinin hesabına alacak kaydedildiği ve İndirim tahakkuk hesabına borç kaydedildiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="db32f-123">This means that the customer's account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="db32f-124">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="db32f-124">Close the page.</span></span>
12. <span data-ttu-id="db32f-125">İptal'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="db32f-125">Click Cancel.</span></span>
    * <span data-ttu-id="db32f-126">Güncelleştirmeleri görebilmeniz için sayfayı yeniler.</span><span class="sxs-lookup"><span data-stu-id="db32f-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="db32f-127">Eylem Bölmesinde, Tahsil et'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="db32f-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="db32f-128">Hareketleri kapat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="db32f-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="db32f-129">Toplam indirim miktarını temsil eden negatif bir miktar hareketinin, fatura referansı olmadan müşterinin hesabına eklendiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="db32f-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="db32f-130">İptal'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="db32f-130">Click Cancel.</span></span>


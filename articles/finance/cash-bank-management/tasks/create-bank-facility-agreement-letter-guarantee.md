---
title: Teminat mektubu için banka hizmet sözleşmesi oluşturma
description: Bu görev teminat mektubu işlemek için bir banka tesis sözleşmesi oluşturur.
author: panolte
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: edeadc1b8502171b9ce892efdaeb9347e399b771
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989114"
---
# <a name="create-a-bank-facility-agreement-for-the-letter-of-guarantee"></a><span data-ttu-id="721f4-103">Teminat mektubu için banka hizmet sözleşmesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="721f4-103">Create a bank facility agreement for the letter of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="721f4-104">Bu görev teminat mektubu işlemek için bir banka tesis sözleşmesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="721f4-104">This task creates a bank facility agreement to process a letter of guarantee.</span></span> <span data-ttu-id="721f4-105">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="721f4-105">This task uses the USMF demo company.</span></span> 


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="721f4-106">Banka kredi anlaşması oluşturma</span><span class="sxs-lookup"><span data-stu-id="721f4-106">Create Bank facility agreement</span></span>
1. <span data-ttu-id="721f4-107">Nakit ve Banka yönetimi > Teminat mektupları > Banka tesisi anlaşmaları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="721f4-107">Go to Cash and bank management > Letters of guarantee > Bank facility agreements.</span></span>
2. <span data-ttu-id="721f4-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="721f4-108">Click New.</span></span>
3. <span data-ttu-id="721f4-109">Sözleşme numarası alanına, hareketin banka sözleşme numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="721f4-109">In the Agreement number field, enter the bank agreement number for the transaction.</span></span>
4. <span data-ttu-id="721f4-110">Banka hesabı alanında, garanti mektubunun açık olduğu banka hesap numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="721f4-110">In the Bank account field, select the bank account number for which the letter of guarantee is open.</span></span> 
5. <span data-ttu-id="721f4-111">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="721f4-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="721f4-112">Başlangıç tarihi alanına tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="721f4-112">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="721f4-113">Bitiş tarihi alanına tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="721f4-113">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="721f4-114">Genel bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="721f4-114">Toggle the expansion of the General section.</span></span>
9. <span data-ttu-id="721f4-115">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="721f4-115">Click Add line.</span></span>
10. <span data-ttu-id="721f4-116">Kredi türü alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="721f4-116">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="721f4-117">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="721f4-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="721f4-118">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="721f4-118">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="721f4-119">Limit alanına, banka ile üzerine anlaşılmış olan miktarı girin.</span><span class="sxs-lookup"><span data-stu-id="721f4-119">In the Limit field, enter the amount negotiated with the bank.</span></span>
14. <span data-ttu-id="721f4-120">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="721f4-120">Click Save.</span></span>
15. <span data-ttu-id="721f4-121">Teminat mektubu bölümün genişlemesini değiştirin.</span><span class="sxs-lookup"><span data-stu-id="721f4-121">Toggle the expansion of the Letter of guarantee section.</span></span>
16. <span data-ttu-id="721f4-122">Hesaplama yöntemi alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="721f4-122">In the Calculation method field, select an option.</span></span>
    * <span data-ttu-id="721f4-123">Nakit Kar marjı, ihraç komisyonu, uzatma komisyonu, artış değeri komisyonu veya azalma değeri komisyonu için hesaplama yöntemini ve yüzde ayrıntılarını uygun olarak girin.</span><span class="sxs-lookup"><span data-stu-id="721f4-123">Enter the calculation method and percentage details for the Cash margin, Issuance commission, Extension commission, Increase value commission, or Decrease value commission, as appropriate.</span></span>   
17. <span data-ttu-id="721f4-124">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="721f4-124">Click Save.</span></span>

## <a name="extend-bank-facility-agreement"></a><span data-ttu-id="721f4-125">Banka hizmet sözleşmesini genişletin</span><span class="sxs-lookup"><span data-stu-id="721f4-125">Extend bank facility agreement</span></span>
1. <span data-ttu-id="721f4-126">İletişim kutusu formunu açmak için Genişlet'e tıklayın</span><span class="sxs-lookup"><span data-stu-id="721f4-126">Click Extend to open the drop dialog.</span></span>
2. <span data-ttu-id="721f4-127">Yeni anlaşma numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="721f4-127">In the New agreement number field, type a value.</span></span>
3. <span data-ttu-id="721f4-128">Bitiş tarihi alanına tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="721f4-128">In the End date field, enter a date and time.</span></span>
4. <span data-ttu-id="721f4-129">Genişlet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="721f4-129">Click Extend.</span></span>
5. <span data-ttu-id="721f4-130">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="721f4-130">Click Save.</span></span>
6. <span data-ttu-id="721f4-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="721f4-131">Close the page.</span></span>


---
title: Vergi dairesi ayarlama
description: Satış vergisi makamları, toplanan satış vergisinin bildirilip ödenmesi gereken kurumlardır.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 160b2507b7ca14ebab54b4775f29615c4aa5f8e0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815104"
---
# <a name="set-up-sales-tax-authorities"></a><span data-ttu-id="464fa-103">Vergi dairesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="464fa-103">Set up sales tax authorities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="464fa-104">Satış vergisi makamları, toplanan satış vergisinin bildirilip ödenmesi gereken kurumlardır.</span><span class="sxs-lookup"><span data-stu-id="464fa-104">Sales tax authorities are entities to which collected sales tax needs to be reported and paid.</span></span> <span data-ttu-id="464fa-105">Satış vergilerini doğrudan bu kuruma ödeyebileceğiniz gibi, satış vergisi kurumu için oluşturduğunuz bir satıcı hesabı aracılığıyla da ödeyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="464fa-105">You can pay sales taxes to the authority directly or through a vendor account that you create for the sales tax authority.</span></span> <span data-ttu-id="464fa-106">Bunu yaparsanız, şirket satış vergisi yetkilisine zamanında ödeme yapmak için normal ödeme rutinlerini kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="464fa-106">If you do this, the company can use its usual payment routines to pay the sales tax authority on time.</span></span> <span data-ttu-id="464fa-107">Vergi yetkilisini satıcı olarak ayarlamazsanız, birisinin uygun vade tarihinde vergi yetkilisine el ile bir ödeme hazırlaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="464fa-107">If you do not set up the tax authority as a vendor, someone must prepare a manual payment to the tax authority on the appropriate due date.</span></span> <span data-ttu-id="464fa-108">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="464fa-108">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="464fa-109">Vergi > Dolaylı vergiler > Satış vergisi > Satış vergisi makamları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="464fa-109">Go to Tax > Indirect taxes > Sales tax > Sales tax authorities.</span></span>
2. <span data-ttu-id="464fa-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="464fa-110">Click New.</span></span>
3. <span data-ttu-id="464fa-111">Makam alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="464fa-111">In the Authority field, type a value.</span></span>
4. <span data-ttu-id="464fa-112">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="464fa-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="464fa-113">Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="464fa-113">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="464fa-114">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="464fa-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="464fa-115">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="464fa-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="464fa-116">Ülkeniz/bölgeniz için bir rapor düzeni varsa, bu düzeni seçin.</span><span class="sxs-lookup"><span data-stu-id="464fa-116">Select the report layout for your country/region, if one is available.</span></span> <span data-ttu-id="464fa-117">Rapor düzenleri vergi dairesi gereksinimlerine karşılık gelmiyorsa, varsayılan düzeni kullanın.</span><span class="sxs-lookup"><span data-stu-id="464fa-117">If the report layouts do not correspond to the requirements of the sales tax authority, use default layout.</span></span>
9. <span data-ttu-id="464fa-118">Ödenecek vergi toplam tutarının nasıl yuvarlanacağını belirtmek için Yuvarlama formuna ve Yuvarlama alanlarına değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="464fa-118">Enter values in the Rounding form and the Round-off fields to specify how the tax total amount to be paid should be rounded.</span></span> <span data-ttu-id="464fa-119">Genel muhasebede otomatik hareketlerin ayarlanması için, tüm yuvarlama farkları Hesaplar'a nakledilir.</span><span class="sxs-lookup"><span data-stu-id="464fa-119">Any rounding differences will be posted to Accounts for automatic transactions set up in General ledger.</span></span>
10. <span data-ttu-id="464fa-120">Yuvarlama alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="464fa-120">In the Round-off field, enter a number.</span></span>
11. <span data-ttu-id="464fa-121">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="464fa-121">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
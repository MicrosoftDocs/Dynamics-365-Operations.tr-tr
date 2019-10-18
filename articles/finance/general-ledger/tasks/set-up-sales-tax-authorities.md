---
title: Vergi dairesi ayarlama
description: Satış vergisi makamları, toplanan satış vergisinin bildirilip ödenmesi gereken kurumlardır.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb0b30be91e33cb50af0ae5c2e4dcd75bd12599b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175671"
---
# <a name="set-up-sales-tax-authorities"></a><span data-ttu-id="f5050-103">Vergi dairesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="f5050-103">Set up sales tax authorities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f5050-104">Satış vergisi makamları, toplanan satış vergisinin bildirilip ödenmesi gereken kurumlardır.</span><span class="sxs-lookup"><span data-stu-id="f5050-104">Sales tax authorities are entities to which collected sales tax needs to be reported and paid.</span></span> <span data-ttu-id="f5050-105">Satış vergilerini doğrudan bu kuruma ödeyebileceğiniz gibi, satış vergisi kurumu için oluşturduğunuz bir satıcı hesabı aracılığıyla da ödeyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f5050-105">You can pay sales taxes to the authority directly or through a vendor account that you create for the sales tax authority.</span></span> <span data-ttu-id="f5050-106">Bunu yaparsanız, şirket satış vergisi yetkilisine zamanında ödeme yapmak için normal ödeme rutinlerini kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="f5050-106">If you do this, the company can use its usual payment routines to pay the sales tax authority on time.</span></span> <span data-ttu-id="f5050-107">Vergi yetkilisini satıcı olarak ayarlamazsanız, birisinin uygun vade tarihinde vergi yetkilisine el ile bir ödeme hazırlaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="f5050-107">If you do not set up the tax authority as a vendor, someone must prepare a manual payment to the tax authority on the appropriate due date.</span></span> <span data-ttu-id="f5050-108">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f5050-108">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="f5050-109">Vergi > Dolaylı vergiler > Satış vergisi > Satış vergisi makamları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="f5050-109">Go to Tax > Indirect taxes > Sales tax > Sales tax authorities.</span></span>
2. <span data-ttu-id="f5050-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5050-110">Click New.</span></span>
3. <span data-ttu-id="f5050-111">Makam alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="f5050-111">In the Authority field, type a value.</span></span>
4. <span data-ttu-id="f5050-112">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="f5050-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="f5050-113">Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="f5050-113">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f5050-114">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f5050-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f5050-115">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5050-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f5050-116">Ülkeniz/bölgeniz için bir rapor düzeni varsa, bu düzeni seçin.</span><span class="sxs-lookup"><span data-stu-id="f5050-116">Select the report layout for your country/region, if one is available.</span></span> <span data-ttu-id="f5050-117">Rapor düzenleri vergi dairesi gereksinimlerine karşılık gelmiyorsa, varsayılan düzeni kullanın.</span><span class="sxs-lookup"><span data-stu-id="f5050-117">If the report layouts do not correspond to the requirements of the sales tax authority, use default layout.</span></span>
9. <span data-ttu-id="f5050-118">Ödenecek vergi toplam tutarının nasıl yuvarlanacağını belirtmek için Yuvarlama formuna ve Yuvarlama alanlarına değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="f5050-118">Enter values in the Rounding form and the Round-off fields to specify how the tax total amount to be paid should be rounded.</span></span> <span data-ttu-id="f5050-119">Genel muhasebede otomatik hareketlerin ayarlanması için, tüm yuvarlama farkları Hesaplar'a nakledilir.</span><span class="sxs-lookup"><span data-stu-id="f5050-119">Any rounding differences will be posted to Accounts for automatic transactions set up in General ledger.</span></span>
10. <span data-ttu-id="f5050-120">Yuvarlama alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="f5050-120">In the Round-off field, enter a number.</span></span>
11. <span data-ttu-id="f5050-121">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5050-121">Click Save.</span></span>


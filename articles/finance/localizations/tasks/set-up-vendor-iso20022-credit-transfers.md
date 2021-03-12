---
title: ISO20022 alacak transferleri için satıcıları ve satıcı banka hesaplarını ayarlama
description: Bu yordam, ISO20022 Alacak transferi veya başka bir satıcı ödemesi dosyası oluşturma işlemi için gereken, satıcı ve satıcıya özel banka hesabı bilgilerinin nasıl ayarlanacağını gösterir.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a7245824c53ab594d62e9296e1f32d32a96ab84
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988032"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="540e5-103">ISO20022 alacak transferleri için satıcıları ve satıcı banka hesaplarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="540e5-103">Set up vendors and vendor bank accounts for ISO20022 credit transfers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="540e5-104">Bu yordam, ISO20022 Alacak transferi veya başka bir satıcı ödemesi dosyası oluşturma işlemi için gereken, satıcı ve satıcıya özel banka hesabı bilgilerinin nasıl ayarlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="540e5-104">This procedure demonstrates how to set up the vendor and vendor specific bank account information required for ISO20022 Credit transfer or any other vendor payment file generation.</span></span> 

<span data-ttu-id="540e5-105">Bu yordamı oluşturmak için kullanılan demo veri şirketi DEMF'dir.</span><span class="sxs-lookup"><span data-stu-id="540e5-105">The demo data company used to create this procedure is DEMF.</span></span>
<span data-ttu-id="540e5-106">Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak satıcı ödemesi işlemini gösteren beş yordamın dördüncüsüdür.</span><span class="sxs-lookup"><span data-stu-id="540e5-106">This is the fourth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="540e5-107">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="540e5-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-bank-details"></a><span data-ttu-id="540e5-108">Banka ayrıntılarını ayarlayın</span><span class="sxs-lookup"><span data-stu-id="540e5-108">Set up bank details</span></span>
1. <span data-ttu-id="540e5-109">Borç hesapları > Satıcılar > Tüm satıcılar seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="540e5-109">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="540e5-110">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="540e5-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="540e5-111">Örneğin, Satıcı hesabı alanında "DE-001" değerini girerek filtreleme yapın.</span><span class="sxs-lookup"><span data-stu-id="540e5-111">For example, filter on the Vendor account field with a value of 'DE-001'.</span></span>
3. <span data-ttu-id="540e5-112">Satıcı ayrıntılarını açmak için DE-001'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="540e5-112">Click DE-001 to open vendor details.</span></span>
4. <span data-ttu-id="540e5-113">Eylem Bölmesinde, Satıcı'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="540e5-113">On the Action Pane, click Vendor.</span></span>
5. <span data-ttu-id="540e5-114">Banka hesapları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="540e5-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="540e5-115">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="540e5-115">Click Edit.</span></span>
    * <span data-ttu-id="540e5-116">Kullanılabilir herhangi bir banka hesabı yoksa, yeni bir banka hesabı oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="540e5-116">If there is no bank account available, you need to create a new one.</span></span>  
7. <span data-ttu-id="540e5-117">SWIFT kodu alanına "COBADEFFXXX" yazın.</span><span class="sxs-lookup"><span data-stu-id="540e5-117">In the SWIFT code field, type 'COBADEFFXXX'.</span></span>
8. <span data-ttu-id="540e5-118">IBAN alanına "DE36200400000628808808" yazın.</span><span class="sxs-lookup"><span data-stu-id="540e5-118">In the IBAN field, type 'DE36200400000628808808'.</span></span>
9. <span data-ttu-id="540e5-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="540e5-119">Close the page.</span></span>

## <a name="set-up-a-method-of-payment-for-the-vendor"></a><span data-ttu-id="540e5-120">Satıcı için ödeme yöntemi ayarlama</span><span class="sxs-lookup"><span data-stu-id="540e5-120">Set up a method of payment for the vendor</span></span>
1. <span data-ttu-id="540e5-121">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="540e5-121">Click Edit.</span></span>
2. <span data-ttu-id="540e5-122">Ödeme bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="540e5-122">Expand or collapse the Payment section.</span></span>
3. <span data-ttu-id="540e5-123">Ödeme yöntemi alanında açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="540e5-123">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="540e5-124">Listede, SEPA CT satırındaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="540e5-124">In the list, click the link in the SEPA CT row.</span></span>
5. <span data-ttu-id="540e5-125">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="540e5-125">Click Save.</span></span>


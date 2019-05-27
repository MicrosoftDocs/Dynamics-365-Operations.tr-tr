---
title: ISO20022 ödeme biçimini kullanarak satıcı ödemeleri oluşturma ve dışa aktarma
description: Bu yordamda, Satıcı ödeme günlüğünde ödeme satırlarının ve ISO2022 Alacak transferi örneğini kullanarak bir satıcı ödemesi dosyasının nasıl oluşturulacağını gösterir.
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b589d64a4446420164175b41f435cf48daac01a9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570065"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="852ba-103">ISO20022 ödeme biçimini kullanarak satıcı ödemeleri oluşturma ve dışa aktarma</span><span class="sxs-lookup"><span data-stu-id="852ba-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="852ba-104">Bu konu, Satıcı ödeme günlüğünde ödeme satırlarının ve ISO2022 Alacak transferi örneğini kullanarak bir satıcı ödemesi dosyasının nasıl oluşturulacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="852ba-104">This topic explains how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span>

<span data-ttu-id="852ba-105">Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak satıcı ödemesi işlemini gösteren beş yordamın beşincisidir.</span><span class="sxs-lookup"><span data-stu-id="852ba-105">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="852ba-106">Bu örneği tamamlamak için DEMF demo verisini kullanın.</span><span class="sxs-lookup"><span data-stu-id="852ba-106">Use the DEMF demo data to complete this example.</span></span>

## <a name="example"></a><span data-ttu-id="852ba-107">Örnek</span><span class="sxs-lookup"><span data-stu-id="852ba-107">Example</span></span>

1.  <span data-ttu-id="852ba-108">**Borç hesapları > Ödemeler > Ödeme günlüğü'ne** gidin.</span><span class="sxs-lookup"><span data-stu-id="852ba-108">Go to **Accounts payable > Payments > Payment journal**.</span></span>
2.  <span data-ttu-id="852ba-109">**Yeni**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="852ba-109">Click **New**.</span></span>
3.  <span data-ttu-id="852ba-110">**Ad** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="852ba-110">In the **Name** field, enter or select a value.</span></span>
4.  <span data-ttu-id="852ba-111">**Satırlar >Ödeme teklifi > Ödeme teklifi oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="852ba-111">Click **Lines > Payment proposal > Create payment proposal**.</span></span>
5.  <span data-ttu-id="852ba-112">**Eklenecek kayıtlar** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="852ba-112">Expand the **Records to include** section.</span></span>
6.  <span data-ttu-id="852ba-113">**Filtrele** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="852ba-113">Click **Filter**.</span></span>
7.  <span data-ttu-id="852ba-114">Listede, **Satıcılar tablosu** ve **Satıcı hesabı alanı** için satır seçin.</span><span class="sxs-lookup"><span data-stu-id="852ba-114">In the list, select the row for **Vendors table** and **Vendor account field**.</span></span>
8.  <span data-ttu-id="852ba-115">**Ölçütler** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="852ba-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="852ba-116">Ödeme yapmak için satıcı hareketlerini seçmek amacıyla herhangi bir ölçütü uygulayabilirsiniz. Bu örnek satıcı hesabı olarak DE-001'i kullanır.</span><span class="sxs-lookup"><span data-stu-id="852ba-116">You can apply any criteria for selecting vendor transactions to pay, for this example, use DE-001 as a vendor account.</span></span>
12. <span data-ttu-id="852ba-117">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="852ba-117">Click **OK**.</span></span>
13. <span data-ttu-id="852ba-118">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="852ba-118">Click **OK**.</span></span>
14. <span data-ttu-id="852ba-119">**Ödemeleri oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="852ba-119">Click **Create payments**.</span></span>
15. <span data-ttu-id="852ba-120">ISO20022 ödeme dosyası oluşturma.</span><span class="sxs-lookup"><span data-stu-id="852ba-120">Generate an ISO20022 payment file.</span></span>
    1.  <span data-ttu-id="852ba-121">**Ödemeler oluştur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="852ba-121">Click **Generate payments**.</span></span>
    2.  <span data-ttu-id="852ba-122">**Ödeme yöntemi** alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="852ba-122">In the **Method of payment** field, enter or select a value.</span></span>
    3.  <span data-ttu-id="852ba-123">**Dosya adı** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="852ba-123">In the **File name** field, type a value.</span></span> <span data-ttu-id="852ba-124">Bu örnekte, EUR ödemesi nedeniyle oluşturulan dosya SEPA uyumlu olacaktır.</span><span class="sxs-lookup"><span data-stu-id="852ba-124">For this example, because of the EUR payment, the generated file will be SEPA compliant.</span></span> <span data-ttu-id="852ba-125">ISO20022 kredi transferi ve diğer satıcı ödeme biçimleri de diğer para birimlerinde ödemeler oluşturmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="852ba-125">ISO20022 credit transfer as well as other vendor payment formats can also be used for generating payments in other currencies.</span></span>
    4.  <span data-ttu-id="852ba-126">**Banka hesabı** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="852ba-126">In the **Bank account** field, enter or select a value.</span></span>


---
title: Kredi mektubu için banka hizmet sözleşmesi oluşturma
description: Bu görev, bir Kredi mektubunu işlemek için Banka kredi anlaşması oluşturma konusunda açıklama sağlar.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankDocumentFacilityAgreement, BankAccountTableLookUp, BankDocumentFacilityAgreementExtension, DefaultDashboard
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 18395f300965df7e024f0eec2b53fa4e8ad2cc3e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566214"
---
# <a name="create-a-bank-facility-agreement-for-a-letter-of-credit"></a><span data-ttu-id="8ec0d-103">Kredi mektubu için banka hizmet sözleşmesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8ec0d-103">Create a bank facility agreement for a letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8ec0d-104">Bu görev, bir Kredi mektubunu işlemek için Banka kredi anlaşması oluşturma konusunda açıklama sağlar.</span><span class="sxs-lookup"><span data-stu-id="8ec0d-104">This task walks through the creating a Bank facility agreement to process a Letter of credit.</span></span> <span data-ttu-id="8ec0d-105">Bu görevden önce banka kredileri ve deftere nakil profilleri ayarlamak isteyeceksiniz.</span><span class="sxs-lookup"><span data-stu-id="8ec0d-105">You will want to set up bank facilities and posting profiles before this task.</span></span>  <span data-ttu-id="8ec0d-106">Bu görevde 'USMF' demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="8ec0d-106">This task uses the demo company 'USMF'.</span></span>  


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="8ec0d-107">Banka kredi anlaşması oluşturma</span><span class="sxs-lookup"><span data-stu-id="8ec0d-107">Create Bank facility agreement</span></span>
1. <span data-ttu-id="8ec0d-108">Nakit ve banka yönetimi > Kredi mektupları > Banka kredi anlaşmaları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="8ec0d-108">Go to Cash and bank management > Letters of credit > Bank facility agreements.</span></span>
2. <span data-ttu-id="8ec0d-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8ec0d-109">Click New.</span></span>
3. <span data-ttu-id="8ec0d-110">Sözleşme numarası alanına bankayla yapılan anlaşmaya göre anlaşma numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="8ec0d-110">In the Agreement number field, enter the agreement number according to the agreement with the bank.</span></span>
4. <span data-ttu-id="8ec0d-111">Banka hesabı alanına, düzenleyen bankadaki hesap numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="8ec0d-111">In the Bank account field, enter the account number at the issuing bank.</span></span>
5. <span data-ttu-id="8ec0d-112">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8ec0d-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="8ec0d-113">Başlangıç tarihi alanına tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="8ec0d-113">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="8ec0d-114">Bitiş tarihi alanına tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="8ec0d-114">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="8ec0d-115">Genel bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="8ec0d-115">Expand or collapse the General section.</span></span>
9. <span data-ttu-id="8ec0d-116">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8ec0d-116">Click Add line.</span></span>
10. <span data-ttu-id="8ec0d-117">Kredi türü alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8ec0d-117">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="8ec0d-118">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="8ec0d-118">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="8ec0d-119">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8ec0d-119">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="8ec0d-120">Limit alanına, banka ile üzerine anlaşılmış olan kredi tutarını girin.</span><span class="sxs-lookup"><span data-stu-id="8ec0d-120">In the Limit field, enter the facility amount that was negotiated with the bank.</span></span>
14. <span data-ttu-id="8ec0d-121">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8ec0d-121">Click Save.</span></span>
15. <span data-ttu-id="8ec0d-122">İletişim kutusu formunu açmak için Genişlet'e tıklayın</span><span class="sxs-lookup"><span data-stu-id="8ec0d-122">Click Extend to open the drop dialog.</span></span>
16. <span data-ttu-id="8ec0d-123">Yeni anlaşma numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="8ec0d-123">In the New agreement number field, type a value.</span></span>
17. <span data-ttu-id="8ec0d-124">Bitiş tarihi alanına tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="8ec0d-124">In the End date field, enter a date and time.</span></span>
18. <span data-ttu-id="8ec0d-125">Genişlet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8ec0d-125">Click Extend.</span></span>
19. <span data-ttu-id="8ec0d-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8ec0d-126">Close the page.</span></span>


--- 
title: "I-9 belge türlerini ayarlama"
description: "Bu yordam, I-9 onaylaması için kullanılan belgelerin görüntülenmesi ve ayarlanmasını gösterir."
author: ShielaSogge
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a05fec7b79003d5b98470d85644d70bd1dbac285
ms.openlocfilehash: d3d2f38327ea82ecddf998161edf86bf32e04db0
ms.contentlocale: tr-tr
ms.lasthandoff: 02/06/2018

---
# <a name="set-up-i-9-document-types"></a><span data-ttu-id="2cfaa-103">I-9 belge türlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="2cfaa-103">Set up I-9 document types</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="2cfaa-104">Bu yordam, I-9 onaylaması için kullanılan belgelerin görüntülenmesi ve ayarlanmasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2cfaa-104">This procedure shows how to view and set up document types that are used for I-9 verification.</span></span> <span data-ttu-id="2cfaa-105">I-9 belge türlerini ayarlamadan önce, belgeyi veren kurumları ve kimlik türleri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2cfaa-105">Before you set up I-9 document types, you must also set up the issuing agencies and identification types.</span></span> <span data-ttu-id="2cfaa-106">Bu yordamı oluşturmak için kullanılan demo verisi şirketi, işlemi tamamlamak için gerekli örnek belge veren kurumlar ve kimlik türleri de bulunduran USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="2cfaa-106">The demo data company used to create this procedure is USMF, which includes examples of the issue agencies and identification types that are needed to complete the procedure.</span></span>

1. <span data-ttu-id="2cfaa-107">İnsan Kaynakları > Çalışanlar > I-9 > I-9 belge türleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="2cfaa-107">Go to Human resources > Workers > I-9 > I-9 document types.</span></span>
2. <span data-ttu-id="2cfaa-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2cfaa-108">Click New.</span></span>
3. <span data-ttu-id="2cfaa-109">I-9 belge türü alanına, bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="2cfaa-109">In the I-9 document type field, type a value.</span></span>
    * <span data-ttu-id="2cfaa-110">Örnek: Okul kimliği.</span><span class="sxs-lookup"><span data-stu-id="2cfaa-110">Example: School ID.</span></span>  
4. <span data-ttu-id="2cfaa-111">Kimlik türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="2cfaa-111">Select the identification type.</span></span>  <span data-ttu-id="2cfaa-112">Örnek:  Okul kimliği</span><span class="sxs-lookup"><span data-stu-id="2cfaa-112">Example:  School ID</span></span>
    * <span data-ttu-id="2cfaa-113">Sosyal Güvenlik numarası, vize numarası, pasaport kimliği veya sürücü belgesi kimlik türüne örnekleri teşkil eder.</span><span class="sxs-lookup"><span data-stu-id="2cfaa-113">Examples of identification types include a Social Security number (SSN), visa number, passport ID, or driver's license.</span></span>  
5. <span data-ttu-id="2cfaa-114">Belge türü için kullanılan I-9 belge listesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2cfaa-114">Select the I-9 document list that is used for the document type.</span></span>
    * <span data-ttu-id="2cfaa-115">I-9 işleminin bir parçası olarak, personelin işverene kimliklerini ve çalışma izinlerini gösteren belge sunmaları gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2cfaa-115">As part of the I-9 process, employees must present documentation that shows the employer their identity and employment authorization.</span></span> <span data-ttu-id="2cfaa-116">ABD Vatandaşlık ve Göçmen Hizmetleri web sitesi, hangi belgelerin kabul edilebilir oldukları ve hangi listeye girdikleri konusunda bilgi içermektedir.</span><span class="sxs-lookup"><span data-stu-id="2cfaa-116">The US Citizenship and Immigration Services website contains information about which documents are acceptable, and which list they belong to.</span></span>  <span data-ttu-id="2cfaa-117">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="2cfaa-117">http://www.uscis.gov</span></span>  
6. <span data-ttu-id="2cfaa-118">Form alanına, bu belge türü için resmi form numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="2cfaa-118">In the Form field, Enter the official form number for the document type.</span></span> <span data-ttu-id="2cfaa-119">Örnek: Okul kimliği.</span><span class="sxs-lookup"><span data-stu-id="2cfaa-119">Example: School ID.</span></span>
    * <span data-ttu-id="2cfaa-120">Resmi form numaraları ABD Vatandaşlık ve Göçmen Hizmetleri web sitesinde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="2cfaa-120">The official form numbers can be found on the US Citizenship and Immigration Services website.</span></span>  <span data-ttu-id="2cfaa-121">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="2cfaa-121">http://www.uscis.gov</span></span>  
7. <span data-ttu-id="2cfaa-122">Aktif onay kutusunu işaretleyin veya işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="2cfaa-122">Check or uncheck the Active checkbox.</span></span>
8. <span data-ttu-id="2cfaa-123">Bitiş tarihi alanında, tarihi '27/10/2019' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2cfaa-123">In the Expire field, set the date to '2019-10-27'.</span></span>
    * <span data-ttu-id="2cfaa-124">Son kullanma tarihi isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="2cfaa-124">The expiration date is optional.</span></span>  
9. <span data-ttu-id="2cfaa-125">Belge türünü veren kurumu seçin.</span><span class="sxs-lookup"><span data-stu-id="2cfaa-125">Select the agency that issued the document type.</span></span> <span data-ttu-id="2cfaa-126">Örnek: Eyalet/Bölge</span><span class="sxs-lookup"><span data-stu-id="2cfaa-126">Example: Province/territory</span></span>
10. <span data-ttu-id="2cfaa-127">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2cfaa-127">Click Save.</span></span>



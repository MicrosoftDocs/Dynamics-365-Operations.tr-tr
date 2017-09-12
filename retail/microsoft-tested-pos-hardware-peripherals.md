---
title: "POS donanımı çevre birimleri"
description: "Perakende Modern satış noktası (POS) ve Bulut POS, birden fazla arabirim ve dağıtım seçeneği ile bir satıcının çeşitlik iş senaryolarını sağlamak için çok çeşitli POS donanım aksesuarlarını kullanabilir."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 215234
ms.assetid: 1893d4b3-e1b7-4b66-be58-0102addd5b36
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 97d374230cc6e833b9f585de000e1252f2a78b9d
ms.openlocfilehash: 17738e794f18fddc7320b1b40ef55376fba0de24
ms.contentlocale: tr-tr
ms.lasthandoff: 08/30/2017

---

# <a name="pos-hardware-peripherals"></a><span data-ttu-id="6fcb3-103">POS donanımı çevre birimleri</span><span class="sxs-lookup"><span data-stu-id="6fcb3-103">POS hardware peripherals</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="6fcb3-104">Perakende Modern satış noktası (POS) ve Bulut POS, birden fazla arabirim ve dağıtım seçeneği ile bir satıcının çeşitlik iş senaryolarını sağlamak için çok çeşitli POS donanım aksesuarlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="6fcb3-104">Retail Modern point of sale (POS) and Cloud POS can utilize a wide range of POS hardware peripherals, with multiple interfaces and deployment options to achieve a retailer’s various business scenarios.</span></span> 

<span data-ttu-id="6fcb3-105">Üreticiler ve modeller arasında en geniş cihaz seçeneklerini desteklemek için POS Perakende POS'u, Windows cihaz sürücüleri ve Windows hizmet noktası uygulama programı arayüzü (API'lar) için OLE gibi standart arabirimlerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="6fcb3-105">To support the widest selection of devices across manufactures and models, POS utilizes standard interfaces such as OLE for Retail POS (OPOS), Windows device drivers, and Windows point of service application program interfaces (APIs).</span></span> <span data-ttu-id="6fcb3-106">Genel olarak, uygun sürücü sağlandığında POS, bu cihazlarda çalışır.</span><span class="sxs-lookup"><span data-stu-id="6fcb3-106">Generally, POS will work on these devices provided that the appropriate driver is supplied.</span></span> <span data-ttu-id="6fcb3-107">Ancak, her üretici ve yazılım geliştiricinin bu standartları uygulaması çeşitlilik gösterebildiğinden, genellikle desteklenen yeteneklerde veya davranışlarda farklılıklar bulunur.</span><span class="sxs-lookup"><span data-stu-id="6fcb3-107">However, because each manufacturer and software developer’s implementation of these standards can vary, there are often differences in supported capabilities or behaviors.</span></span>

<span data-ttu-id="6fcb3-108">Aşağıdaki listede Microsoft tarafından dahili olarak sınanmış olan her sınıftan cihaz modelleri bulunur.</span><span class="sxs-lookup"><span data-stu-id="6fcb3-108">The following list includes device models, in each class, that have been tested internally by Microsoft.</span></span>

<span data-ttu-id="6fcb3-109">**OPOS cihazları**</span><span class="sxs-lookup"><span data-stu-id="6fcb3-109">**OPOS devices**</span></span>

-   <span data-ttu-id="6fcb3-110">Barkod – Motorola DS9208</span><span class="sxs-lookup"><span data-stu-id="6fcb3-110">Barcode – Motorola DS9208</span></span>
-   <span data-ttu-id="6fcb3-111">MSR – HP IDRA-334133, Magtek PN - 21073062</span><span class="sxs-lookup"><span data-stu-id="6fcb3-111">MSR – HP IDRA-334133, Magtek PN - 21073062</span></span>
-   <span data-ttu-id="6fcb3-112">LineDisplay – Epson M58DC</span><span class="sxs-lookup"><span data-stu-id="6fcb3-112">LineDisplay – Epson M58DC</span></span>
-   <span data-ttu-id="6fcb3-113">Pinpad – Verifone 1000SE</span><span class="sxs-lookup"><span data-stu-id="6fcb3-113">Pinpad – Verifone 1000SE</span></span>
-   <span data-ttu-id="6fcb3-114">İmza yakalama cihazı – Scriptel ST1550</span><span class="sxs-lookup"><span data-stu-id="6fcb3-114">Signature pad – Scriptel ST1550</span></span>
-   <span data-ttu-id="6fcb3-115">Yazıcı – EPSON TM-T88IV, TMT88V</span><span class="sxs-lookup"><span data-stu-id="6fcb3-115">Printer – EPSON TM-T88IV, TMT88V</span></span>
-   <span data-ttu-id="6fcb3-116">Kasa çekmecesi – Star SMD2-1317BK44</span><span class="sxs-lookup"><span data-stu-id="6fcb3-116">Cash drawer – Star SMD2-1317BK44</span></span>
-   <span data-ttu-id="6fcb3-117">Tartı – Datalogic Magellan 8400</span><span class="sxs-lookup"><span data-stu-id="6fcb3-117">Scale – Datalogic Magellan 8400</span></span>

<span data-ttu-id="6fcb3-118">**Klavye kaması MSR**</span><span class="sxs-lookup"><span data-stu-id="6fcb3-118">**Keyboard wedge MSR**</span></span>

-   <span data-ttu-id="6fcb3-119">Magtek USB</span><span class="sxs-lookup"><span data-stu-id="6fcb3-119">Magtek USB</span></span>

<span data-ttu-id="6fcb3-120">**Ödeme terminali**</span><span class="sxs-lookup"><span data-stu-id="6fcb3-120">**Payment terminal**</span></span>

-   <span data-ttu-id="6fcb3-121">Equinox L3500</span><span class="sxs-lookup"><span data-stu-id="6fcb3-121">Equinox L3500</span></span>
-   <span data-ttu-id="6fcb3-122">Verifone MX925</span><span class="sxs-lookup"><span data-stu-id="6fcb3-122">Verifone MX925</span></span>

<span data-ttu-id="6fcb3-123">**Ağ cihazları**</span><span class="sxs-lookup"><span data-stu-id="6fcb3-123">**Network devices**</span></span>

-   <span data-ttu-id="6fcb3-124">Yazıcı – Star TSP650II</span><span class="sxs-lookup"><span data-stu-id="6fcb3-124">Printer – Star TSP650II</span></span>
-   <span data-ttu-id="6fcb3-125">Kasa çekmecesi – APG Atwood</span><span class="sxs-lookup"><span data-stu-id="6fcb3-125">Cash drawer – APG Atwood</span></span>
-   <span data-ttu-id="6fcb3-126">Ödeme terminali – MX915, MX925</span><span class="sxs-lookup"><span data-stu-id="6fcb3-126">Payment terminal – MX915, MX925</span></span>

<span data-ttu-id="6fcb3-127">**MPOS, yalnızca doğrudan IPC**</span><span class="sxs-lookup"><span data-stu-id="6fcb3-127">**MPOS direct IPC only**</span></span>

-   <span data-ttu-id="6fcb3-128">Barkod – Honeywell 1900, HP LS2208</span><span class="sxs-lookup"><span data-stu-id="6fcb3-128">Barcode – Honeywell 1900, HP LS2208</span></span>
-   <span data-ttu-id="6fcb3-129">MSR – Magtek PN - 21073075</span><span class="sxs-lookup"><span data-stu-id="6fcb3-129">MSR – Magtek PN - 21073075</span></span>






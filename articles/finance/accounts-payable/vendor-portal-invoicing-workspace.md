---
title: Satıcı iş birliği faturalama çalışma alanı
description: Bu konuda, satıcı faturalarını görüntüleme ve satıcı iş birliği faturalama çalışma alanından faturaları gönderme açıklanmaktadır.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ddb9d561e9785ee744c49d7fe03128102e77e9d3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248219"
---
# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="fbf38-103">Satıcı iş birliği faturalama çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="fbf38-103">Vendor collaboration invoicing workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fbf38-104">Bu konuda, satıcı faturalarını görüntüleme ve satıcı iş birliği faturalama çalışma alanından faturaları gönderme açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="fbf38-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="fbf38-105">**Satıcı işbirliği faturalama** çalışma alanı, satıcı faturası bilgilerini görüntülemek ve iş akışı özelliklerini kullanarak sisteme fatura göndermek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="fbf38-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to the system using workflow capabilities.</span></span>


<a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="fbf38-106">Satıcı işbirliği faturalama çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="fbf38-106">Vendor collaboration invoicing workspace</span></span>
----------------------------------------

### <a name="summary-tiles"></a><span data-ttu-id="fbf38-107">Özet kutucukları</span><span class="sxs-lookup"><span data-stu-id="fbf38-107">Summary tiles</span></span>

<span data-ttu-id="fbf38-108">**Özet** kutucukları seçili satıcının faturalarına bir genel bakış sunar.</span><span class="sxs-lookup"><span data-stu-id="fbf38-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="fbf38-109">Faturaları durumlarına göre görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbf38-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="fbf38-110">Taslak faturalar iş akışına gönderilmemiştir.</span><span class="sxs-lookup"><span data-stu-id="fbf38-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="fbf38-111">Gönderilen, onaylanmamış faturalar satıcının gönderdiği ancak uygulamada deftere nakledilmeyen faturalardır.</span><span class="sxs-lookup"><span data-stu-id="fbf38-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in the application.</span></span>
-   <span data-ttu-id="fbf38-112">Onaylanmış, ödenmemiş faturalar, deftere nakledilmiş ancak henüz tamamen ödenmemiş faturalardır.</span><span class="sxs-lookup"><span data-stu-id="fbf38-112">Approved, not paid invoices are those that have been posted, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="fbf38-113">Ödenmiş faturalar uygulamada tamamen ödenmiş faturalardır.</span><span class="sxs-lookup"><span data-stu-id="fbf38-113">Paid invoices are those that have been fully paid in the application.</span></span>

<span data-ttu-id="fbf38-114">Bir kutucuğa tıklandığında **Faturalar listesi** sayfasının filtrelenmiş bir görünümü açılır.</span><span class="sxs-lookup"><span data-stu-id="fbf38-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>

### <a name="tabular-lists"></a><span data-ttu-id="fbf38-115">Sekmeli listeler</span><span class="sxs-lookup"><span data-stu-id="fbf38-115">Tabular lists</span></span>

<span data-ttu-id="fbf38-116">**Sekmeli listeler** bölümünde, faturalamanın durumu özet kutucuklardaki gibi, Taslak ve Gönderildi, onaylanmadı listelerine benzer şekilde ayrılır.</span><span class="sxs-lookup"><span data-stu-id="fbf38-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="fbf38-117">Taslak durumunda, fatura iş akışına gönderilebilir veya silinebilir.</span><span class="sxs-lookup"><span data-stu-id="fbf38-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="fbf38-118">Son sekmeli liste, faturaları bulmak için bir seçenektir.</span><span class="sxs-lookup"><span data-stu-id="fbf38-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="fbf38-119">Ararken filtreleyerek daha hızlı arama yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbf38-119">You can filter as you search, to allow for faster searches.</span></span>

### <a name="all-vendor-invoices-list-page"></a><span data-ttu-id="fbf38-120">Tüm satıcı faturaları liste sayfası</span><span class="sxs-lookup"><span data-stu-id="fbf38-120">All vendor invoices list page</span></span>

<span data-ttu-id="fbf38-121">Tüm deftere nakledilmiş ve nakledilmemiş satıcı faturalarını **Satıcı işbirliği faturaları** listesi sayfasında görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbf38-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="fbf38-122">Faturaların ödeme durumunu görüntülemek için bu liste sayfasını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbf38-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="fbf38-123">Ödeme durumları Nakledilmedi, Ödenmedi, Kısmen ödendi ve Tamamen ödendi durumlarını içerir.</span><span class="sxs-lookup"><span data-stu-id="fbf38-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="fbf38-124">Satınalma siparişinden yeni fatura oluşturma</span><span class="sxs-lookup"><span data-stu-id="fbf38-124">Creating a new invoice from a purchase order</span></span>

<span data-ttu-id="fbf38-125">**Satıcı iş birliği faturalama** çalışma alanındaki **Yeni** eylemini seçerek yeni bir satıcı faturası oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbf38-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="fbf38-126">Satınalma sipariş numarası ve fatura numarası satıcı tarafından sağlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fbf38-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="fbf38-127">Varsayılan olarak, satıcının satınalma emrinden alınan tüm satırlar yeni faturada görünür.</span><span class="sxs-lookup"><span data-stu-id="fbf38-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="fbf38-128">Miktar ve maliyet bilgileri satıcı faturasını iş akışına göndermeden önce düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="fbf38-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="fbf38-129">Göndermeden önce bir faturaya dosya, not, görüntü ve URL ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbf38-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>

<span data-ttu-id="fbf38-130">Daha fazla bilgi için bkz. [Harici satıcılarla satıcı işbirliği](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span><span class="sxs-lookup"><span data-stu-id="fbf38-130">For more information, see [Vendor collaboration with external vendors](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
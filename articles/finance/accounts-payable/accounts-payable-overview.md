---
title: Borç hesaplarını yapılandırmaya genel bakış
description: Bu makalede, Borç hesapları için temel ve isteğe bağlı işlevleri ayarlamada kullanacağınız sayfalar açıklanmaktadır. Ayrıca, Borç hesaplarını ayarlamaya başlamadan önce tamamlamanız gereken kurulum adımları da açıklanmaktadır.
author: abruer
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable, DeliveryReason, DeliveryTerms, DestinationCode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eed11cbe73ede71cabf83655fc1d37b1a979a4c
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830295"
---
# <a name="configure-accounts-payable-overview"></a><span data-ttu-id="e6b78-104">Borç hesaplarını yapılandırmaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="e6b78-104">Configure Accounts payable overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6b78-105">Bu makalede, Borç hesapları için temel ve isteğe bağlı işlevleri ayarlamada kullanacağınız sayfalar açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e6b78-105">This article describes the pages that you use to set up basic and optional functionality for Accounts payable.</span></span> <span data-ttu-id="e6b78-106">Ayrıca, Borç hesaplarını ayarlamaya başlamadan önce tamamlamanız gereken kurulum adımları da açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e6b78-106">It also describes setup steps that you must complete before you start to set up Accounts payable.</span></span>

<a name="prerequisites-for-accounts-payable-setup"></a><span data-ttu-id="e6b78-107">Borç hesapları kurulumu için ön gereksinimler</span><span class="sxs-lookup"><span data-stu-id="e6b78-107">Prerequisites for Accounts payable setup</span></span>
----------------------------------------

<span data-ttu-id="e6b78-108">Borç hesaplarını ayarlamadan önce aşağıdaki kurulumu tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="e6b78-108">Before you can set up Accounts payable, you must complete the following setup:</span></span>

-   <span data-ttu-id="e6b78-109">Genel muhasebe hesabında:</span><span class="sxs-lookup"><span data-stu-id="e6b78-109">In General ledger:</span></span>
    -   <span data-ttu-id="e6b78-110">Ödeme Günlükleri'ni kullanmayı planlıyorsanız, ödeme günlükleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-110">If you plan to use payment journals, set up payment journals.</span></span>
    -   <span data-ttu-id="e6b78-111">Döviz kuru ayarlamalarını çalıştırmayı planlıyorsanız, Para birimleri sayfasında para birimi kodlarını, Döviz kurları türleri sayfasında döviz kuru türlerini ve Para birimi döviz kuru sayfasında, para birimi döviz kurlarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-111">If you plan to run exchange rate adjustments, set up currency codes on the Currencies page, set up exchange rate types on the Exchange rate types page, and set up currency exchange rates on the Currency exchange rates page.</span></span>
-   <span data-ttu-id="e6b78-112">Nakit ve banka yönetimi bölümünde, ödeme yöntemleriyle kullanılacak banka hesaplarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-112">In Cash and bank management, set up bank accounts to use with methods of payment.</span></span>

## <a name="setup-pages-for-accounts-payable"></a><span data-ttu-id="e6b78-113">Borç hesapları için kurulum sayfaları</span><span class="sxs-lookup"><span data-stu-id="e6b78-113">Setup pages for Accounts payable</span></span>

<span data-ttu-id="e6b78-114">Her tüzel kişilik için temel Borç hesapları işlevlerini ayarlamak üzere aşağıdaki sayfaları kullanın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-114">Use the following pages to set up the basic functionality of Accounts payable for each legal entity.</span></span> <span data-ttu-id="e6b78-115">Sayfalar önerilen kurulum sırasıyla listelenmiştir.</span><span class="sxs-lookup"><span data-stu-id="e6b78-115">The pages are listed in the recommended order of setup.</span></span> <span data-ttu-id="e6b78-116">Kurulum işlemini kolaylaştırmak için, oluşturduğunuz ilk kayıtlardan şablonları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e6b78-116">To make the setup process easier, you can create templates from the first records that you create.</span></span> <span data-ttu-id="e6b78-117">Bir şablonda, değerler genellikle kuruluşun belirli bir satıcı tipi için uygulamak istediği özellikleri yansıtan değerleri içerir.</span><span class="sxs-lookup"><span data-stu-id="e6b78-117">In a template, values are typically entered in many fields to reflect the features that the organization wants to implement for a particular type of vendor.</span></span>
1.  <span data-ttu-id="e6b78-118">Satış siparişlerine, satınalma siparişlerine, müşterilere ve satıcılara atadığınız ve fatura vade tarihlerini belirleyen ödeme koşullarını, Ödeme koşulları sayfasında tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-118">On the Terms of payment page, define the terms of payment that you assign to sales orders, purchase orders, customers, and vendors, and that determine invoice due dates.</span></span> <span data-ttu-id="e6b78-119">Daha fazla bilgi için bkz. [Satıcı ödeme ücretlerini tanımlama](tasks/define-vendor-payment-fees.md).</span><span class="sxs-lookup"><span data-stu-id="e6b78-119">For more information, see [Define vendor payment fees](tasks/define-vendor-payment-fees.md).</span></span>
2.  <span data-ttu-id="e6b78-120">Ödeme yöntemleri - Satıcılar sayfa üzerinde, kuruluşun satıcılarına nasıl ödeme yaptığı hakkındaki bilgileri oluşturun ve sürdürün.</span><span class="sxs-lookup"><span data-stu-id="e6b78-120">On the Methods of payment - vendors page, create and maintain information about how the organization pays its vendors.</span></span>
3.  <span data-ttu-id="e6b78-121">Deftere nakletme, kapatma ve ödeme, raporlama ve tahmin yürütme için önemli parametreleri paylaşan satıcı gruplarını, Satıcı grupları sayfasında oluşturun ve sürdürün.</span><span class="sxs-lookup"><span data-stu-id="e6b78-121">On the Vendor groups page, create and maintain groups of vendors that share important parameters for posting, settlement and payment, reporting, and forecasting.</span></span>
4.  <span data-ttu-id="e6b78-122">Satıcı deftere nakil profilleri sayfasında, satıcı hareketlerinin genel muhasebeye nasıl nakledildiğini tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-122">On the Vendor posting profiles page, define how vendor transactions are posted to the general ledger.</span></span>
5.  <span data-ttu-id="e6b78-123">Daha özel bir ayar belirtilmediğinde uygulanacak varsayılan değerleri, çeşitli tiplerde işlevler için parametreleri ve Borç hesapları için çeşitli numara sıralarını Borç hesapları parametreleri sayfasında ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-123">On the Accounts payable parameters page, set up default settings that are applied if a more specific setting isn't specified, parameters for various kinds of functionality, and the various number sequences for Accounts payable.</span></span>
6.  <span data-ttu-id="e6b78-124">Satıcılarla ilgili olan, satıcılardan gelen girişleri izlemek ve satıcılara ödeme akışları için nedenler girmek için kuruluşun kullandığı çeşitli belgelerin biçimini Form kurulumu sayfasında tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-124">On the Form setup page, define the format of various documents that are related to vendors, and that the organization uses to keep track of receipts from vendors and enter reasons for the flow of payments to vendors.</span></span>
7.  <span data-ttu-id="e6b78-125">Satıcılar sayfasında, satıcı hesapları ve ayrıca kuruluşunuzun satış vergilerini bildirdiği vergi dairelerini oluşturun ve sürüdün.</span><span class="sxs-lookup"><span data-stu-id="e6b78-125">On the Vendors page, create and maintain vendor accounts, and also the tax authorities that your organization reports sales taxes to.</span></span>

## <a name="optional-setup-pages-for-accounts-payable"></a><span data-ttu-id="e6b78-126">Borç hesapları için isteğe bağlı kurulum sayfaları</span><span class="sxs-lookup"><span data-stu-id="e6b78-126">Optional setup pages for Accounts payable</span></span>
<span data-ttu-id="e6b78-127">Temel işlevselliğe ek olarak, Borç hesapları ayarlayabileceğiniz başka işlevlere de sahiptir.</span><span class="sxs-lookup"><span data-stu-id="e6b78-127">In addition to the basic functionality, Accounts payable has other functionality that you can set up.</span></span>

<span data-ttu-id="e6b78-128">İşleve göre ek kurulum sayfaları düzenlenir.</span><span class="sxs-lookup"><span data-stu-id="e6b78-128">The additional setup pages are organized by functionality.</span></span>

<span data-ttu-id="e6b78-129">**İlkeler**</span><span class="sxs-lookup"><span data-stu-id="e6b78-129">**Policies**</span></span>
-   <span data-ttu-id="e6b78-130">Satıcı Fatura ilkesi sayfasında satıcı fatura ilkelerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-130">On the Vendor invoice policy page, set up vendor invoice policies.</span></span>

<span data-ttu-id="e6b78-131">**Fatura eşleştirme**</span><span class="sxs-lookup"><span data-stu-id="e6b78-131">**Invoice matching**</span></span>

-   <span data-ttu-id="e6b78-132">Fatura toplamları farkları sayfasında, fatura toplamları için fakları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-132">On the Invoice totals tolerances page, set up tolerances for invoice totals.</span></span>
-   <span data-ttu-id="e6b78-133">Eşleşme ilkesi sayfasında iki yönlü ve üç yollu eşleştirme ilkeleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-133">On the Matching policy page, set up two-way and three-way matching policies.</span></span>
-   <span data-ttu-id="e6b78-134">Fiyat farkları sayfasında birim fiyatları için farkları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-134">On the Price tolerances page, set up tolerances for unit prices.</span></span>
-   <span data-ttu-id="e6b78-135">Madde fiyatı farkı grupları sayfasında madde fiyatları için fark grupları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-135">On the Item price tolerance groups page, set up tolerance groups for item prices.</span></span>
-   <span data-ttu-id="e6b78-136">Satıcı fiyatı farkı grupları sayfasında satıcı fiyatları için fark grupları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-136">On the Vendor price tolerance groups page, set up  tolerance groups for vendor prices.</span></span>
-   <span data-ttu-id="e6b78-137">Gider farkları sayfasında giderler için farkları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-137">On the Charges tolerances page, set up tolerances for charges.</span></span>

<span data-ttu-id="e6b78-138">**İş Akışı**</span><span class="sxs-lookup"><span data-stu-id="e6b78-138">**Workflow**</span></span>

-   <span data-ttu-id="e6b78-139">Borç hesapları iş akışı sayfasında, Satınalma talepleri ve günlük onayları için iş akışı yapılandırmaları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-139">On the Accounts payable workflows page, set up workflow configurations for journal approvals and purchase requisitions.</span></span>

<span data-ttu-id="e6b78-140">**Nedenler**</span><span class="sxs-lookup"><span data-stu-id="e6b78-140">**Reasons**</span></span>

-   <span data-ttu-id="e6b78-141">Satıcı nedenleri sayfasında neden kodlarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-141">On the Vendor reasons page, set up reason codes.</span></span>

<span data-ttu-id="e6b78-142">**Masraflar**</span><span class="sxs-lookup"><span data-stu-id="e6b78-142">**Charges**</span></span>

-   <span data-ttu-id="e6b78-143">Gider kodu sayfasında kullanılan satınalma siparişlerindeki giderleri için kodlar ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-143">On the Charges code page, set up codes for the charges that are used in purchase orders.</span></span>
-   <span data-ttu-id="e6b78-144">Satıcı giderleri grubu üzerinde sayfa oluşturun ve satıcılar için masraf gruplarını güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="e6b78-144">On the Vendor charges group page, create and maintain charges groups for vendors.</span></span>
-   <span data-ttu-id="e6b78-145">Madde giderini grupları sayfasında, maddeler için giderler grupları oluşturun ve sürdürün.</span><span class="sxs-lookup"><span data-stu-id="e6b78-145">On the Item charge groups page, create and maintain charges groups for items.</span></span>
-   <span data-ttu-id="e6b78-146">Otomatik masraflar sayfasında, siparişlere otomatik olarak atanan giderleri tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-146">On the Auto charges page, define the charges that are automatically assigned to orders.</span></span>

<span data-ttu-id="e6b78-147">**Tamamlayıcı maddeler**</span><span class="sxs-lookup"><span data-stu-id="e6b78-147">**Supplementary items**</span></span>

-   <span data-ttu-id="e6b78-148">Tamamlayıcı madde grupları üzerinde- Satıcı sayfasında, satıcılar için tamamlayıcı madde grupları oluşturun ve sürdürün.</span><span class="sxs-lookup"><span data-stu-id="e6b78-148">On the Supplementary item groups - Vendor page, create and maintain supplementary item groups for vendors.</span></span>
-   <span data-ttu-id="e6b78-149">Tamamlayıcı madde grupları üzerinde-Stok sayfasında, maddeler için tamamlayıcı madde grupları oluşturun ve sürdürün.</span><span class="sxs-lookup"><span data-stu-id="e6b78-149">On the Supplementary item groups - Inventory page, create and maintain supplementary item groups for items.</span></span>

<span data-ttu-id="e6b78-150">**Dağıtım**</span><span class="sxs-lookup"><span data-stu-id="e6b78-150">**Distribution**</span></span>

-   <span data-ttu-id="e6b78-151">Teslimat koşulları sayfasında , satıcıdan müşteriye bir madde naklinin koşullarını oluşturun ve sürdürün.</span><span class="sxs-lookup"><span data-stu-id="e6b78-151">On the Terms of delivery page, create and maintain the conditions for an item's transfer from seller to buyer.</span></span>
-   <span data-ttu-id="e6b78-152">Teslimat modları sayfasında, bir sipariş satıcıdan alıcıya teslim edildiğinde, kullanılacak taşıma yöntemlerini oluşturun ve yönetin.</span><span class="sxs-lookup"><span data-stu-id="e6b78-152">On the Modes of delivery page, create and maintain the methods of transport that are used when an order is delivered from the seller to the buyer.</span></span>
-   <span data-ttu-id="e6b78-153">Hedef kodları sayfasında, teslimat hedefleri için tanımlayıcılar ve tarifler oluşturun ve sürdürün.</span><span class="sxs-lookup"><span data-stu-id="e6b78-153">On the Destination codes page, create and maintain identifiers and descriptions for delivery destinations.</span></span>

<span data-ttu-id="e6b78-154">**Formlar**</span><span class="sxs-lookup"><span data-stu-id="e6b78-154">**Forms**</span></span>

-   <span data-ttu-id="e6b78-155">Form notlarısayfasında, çeşitli sayfalarda görüntülenecek standar metni oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e6b78-155">On the Form notes page, create the standard text that appears on various pages.</span></span>
-   <span data-ttu-id="e6b78-156">Form sıralaması parametreleri sayfasında, talepler, giriş listeleri, sevk irsaliyeleri ve faturalar için bir sıralama düzeni ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-156">On the Form sorting parameters page, set up the sorting order for requisitions, receipt lists, packing slips, and invoices.</span></span>
-   <span data-ttu-id="e6b78-157">Yazdırma yönetimi kurulumu sayfasında, sayfaların orjinali ve kopyası için baskı yönetim bilgisini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-157">On the Print management setup page, set up print management information for originals and copies of pages.</span></span>

<span data-ttu-id="e6b78-158">**Ödemeler**</span><span class="sxs-lookup"><span data-stu-id="e6b78-158">**Payments**</span></span>

-   <span data-ttu-id="e6b78-159">Nakit iskontosu sayfasında, nakit iskontoları edinmek için şartları ayarlayın ve yönetin.</span><span class="sxs-lookup"><span data-stu-id="e6b78-159">On the Cash discounts page, set up and manage the terms for obtaining cash discounts.</span></span> <span data-ttu-id="e6b78-160">Nakit iskonto kodları satıcılara bağlıdır ve satınalma siparişlerine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="e6b78-160">The cash discount codes are linked to vendors and are applied to purchase orders.</span></span>
-   <span data-ttu-id="e6b78-161">Ödeme planları sayfasında, satıcılara yapılacak taksit ödemelerini yönetmek için kullanılan ödeme planlarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-161">On the Payment schedules page, set up the payment schedules that are used to manage installment payments to vendors.</span></span>
-   <span data-ttu-id="e6b78-162">Ödeme günleri sayfasında, vade tarihlerini belirlemede kullanılacak ödeme günlerini tanımlayın ve ayın veya haftanın bir günlerini ödeme günleri olarak belirleyin.</span><span class="sxs-lookup"><span data-stu-id="e6b78-162">On the Payment days page, define the payment days that are used to calculate due dates, and specify payment days for a specific day of the week or month.</span></span>
-   <span data-ttu-id="e6b78-163">Ödeme masrafları sayfasında, satıcılar ile ilişkili ödeme masraflarını oluşturun ve sürdürün.</span><span class="sxs-lookup"><span data-stu-id="e6b78-163">On the Payment fee page, create and maintain the payment fees that are associated with vendors.</span></span>
-   <span data-ttu-id="e6b78-164">Ödeme talimatı sayfasında, ödeme talimatları oluşturun ve sürdürün.</span><span class="sxs-lookup"><span data-stu-id="e6b78-164">On the Payment instruction page, create and maintain payment instructions.</span></span>

<span data-ttu-id="e6b78-165">**İstatistikler**</span><span class="sxs-lookup"><span data-stu-id="e6b78-165">**Statistics**</span></span>

-   <span data-ttu-id="e6b78-166">Yaşlandırma dönemi tanımları sayfasında, satıcı hesaplarının vade dağılımını analiz etmede kullanılacak, kullanıcı tarafından tanımlanan aralıkları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-166">On the Aging period definitions page, set up user-defined intervals that are used to analyze the maturity distribution of vendor accounts.</span></span>
-   <span data-ttu-id="e6b78-167">İş kolu sayfasında, satıcılara atanan iş kolu (LOB) kodlarını oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e6b78-167">On the Line of business page, create the line of business (LOB) codes that are assigned to vendors.</span></span>

<span data-ttu-id="e6b78-168">**Vergi 1099**</span><span class="sxs-lookup"><span data-stu-id="e6b78-168">**Tax 1099**</span></span>

-   <span data-ttu-id="e6b78-169">**1099 alanları** sayfasında, en güncel gereksinimlerine göre ABD İç Gelir Servisi'ne (IRS) bildirilecek minimum tutarları onaylayın ve güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="e6b78-169">On the **1099 fields** page, verify and update the minimum amounts that must be reported to the Internal Revenue Service (IRS), based on the latest IRS requirements.</span></span>

## <a name="optional-setup-for-other-modules"></a><span data-ttu-id="e6b78-170">**Diğer modüller için isteğe bağlı kurulum**</span><span class="sxs-lookup"><span data-stu-id="e6b78-170">**Optional setup for other modules**</span></span>
<span data-ttu-id="e6b78-171">**Kuruluş yönetimi**</span><span class="sxs-lookup"><span data-stu-id="e6b78-171">**Organization administration**</span></span>

-   <span data-ttu-id="e6b78-172">Numara serileri sayfasında, fatura numaraları için numara serisi grupları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-172">On the Number sequences page, set up number sequence groups for invoice numbers.</span></span>
-   <span data-ttu-id="e6b78-173">Aşağıdaki sayfalarda adres bilgilerini ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="e6b78-173">On the following pages, set up address information:</span></span>
    -   <span data-ttu-id="e6b78-174">Adres kurulumu</span><span class="sxs-lookup"><span data-stu-id="e6b78-174">Address setup</span></span>
    -   <span data-ttu-id="e6b78-175">NAF kodları</span><span class="sxs-lookup"><span data-stu-id="e6b78-175">NAF codes</span></span>
    -   <span data-ttu-id="e6b78-176">Posta kodlarını içe aktar</span><span class="sxs-lookup"><span data-stu-id="e6b78-176">Import ZIP/postal codes</span></span>

<span data-ttu-id="e6b78-177">**Genel muhasebe**</span><span class="sxs-lookup"><span data-stu-id="e6b78-177">**General ledger**</span></span>

-   <span data-ttu-id="e6b78-178">Finansal boyutlar sayfasında, finansal boyutları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-178">On the Financial dimensions page, set up financial dimensions.</span></span>
-   <span data-ttu-id="e6b78-179">Aşağıdaki sayfalarda, vergi bilgilerini ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="e6b78-179">On the following pages, set up tax information:</span></span>
    -   <span data-ttu-id="e6b78-180">Satış vergisi kodları</span><span class="sxs-lookup"><span data-stu-id="e6b78-180">Sales tax codes</span></span>
    -   <span data-ttu-id="e6b78-181">Satış vergisi grupları</span><span class="sxs-lookup"><span data-stu-id="e6b78-181">Sales tax groups</span></span>
    -   <span data-ttu-id="e6b78-182">Madde satış vergisi grupları</span><span class="sxs-lookup"><span data-stu-id="e6b78-182">Item sales tax groups</span></span>
    -   <span data-ttu-id="e6b78-183">Hesap grubu</span><span class="sxs-lookup"><span data-stu-id="e6b78-183">Account group</span></span>
    -   <span data-ttu-id="e6b78-184">Satış vergisi muafiyet kodları</span><span class="sxs-lookup"><span data-stu-id="e6b78-184">Sales tax exempt codes</span></span>
    -   <span data-ttu-id="e6b78-185">Satış vergi daireleri</span><span class="sxs-lookup"><span data-stu-id="e6b78-185">Sales tax jurisdictions</span></span>
    -   <span data-ttu-id="e6b78-186">Satış vergisi makamları</span><span class="sxs-lookup"><span data-stu-id="e6b78-186">Sales tax authorities</span></span>
    -   <span data-ttu-id="e6b78-187">Satış vergisi kapatma dönemleri</span><span class="sxs-lookup"><span data-stu-id="e6b78-187">Sales tax settlement periods</span></span>

<span data-ttu-id="e6b78-188">**Nakit ve banka yönetimi**</span><span class="sxs-lookup"><span data-stu-id="e6b78-188">**Cash and bank management**</span></span>

-   <span data-ttu-id="e6b78-189">Ödeme amaçları kodları sayfasında, Merkezi Banka amaç kodunu ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e6b78-189">On the Payment purpose codes page, set up the Central Bank purpose code.</span></span>






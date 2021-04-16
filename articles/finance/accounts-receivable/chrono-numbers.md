---
title: Belgeleri ve fişleri kronolojik olarak numaralandırma
description: Bu konu, uygulanabilir belgeler ve ilgili fişler için kronolojik numaraların nasıl ayarlanacağını ve kullanılacağını açıklamaktadır.
author: ikond
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: fe533052b0e5b04a7d27b954ba644761c631d6d7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838873"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a><span data-ttu-id="5b10c-103">Belgeleri ve fişleri kronolojik olarak numaralandırma</span><span class="sxs-lookup"><span data-stu-id="5b10c-103">Numbering documents and vouchers chronologically</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="5b10c-104">Bazı ülke/bölgelerde, belgeleri ve ilgili fişleri kronolojik sırada numaralandırmak için yasal bir gereksinim vardır.</span><span class="sxs-lookup"><span data-stu-id="5b10c-104">In some countries, there is a legal requirement to number documents and related vouchers in chronological order.</span></span> <span data-ttu-id="5b10c-105">Kronoloji, dönemler tarafından desteklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="5b10c-105">The chronology must be supported by periods.</span></span> <span data-ttu-id="5b10c-106">Önceki dönemlere ait tüm numaralar sonraki dönemlere ait olan numaralardan küçük olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5b10c-106">All of the numbers that belong to earlier periods must be less than the numbers that belong to later periods.</span></span> <span data-ttu-id="5b10c-107">Bu gereksinimi karşılamak için kronolojik numaralandırma işlevi uygulanmıştır.</span><span class="sxs-lookup"><span data-stu-id="5b10c-107">To meet this requirement, chronological numbering functionality has been implemented.</span></span> <span data-ttu-id="5b10c-108">Bu konu, uygulanabilir belgeler ve ilgili fişler için kronolojik numaraların nasıl yapılandırılacağı ve kullanılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="5b10c-108">This topic explains how to configure and use chronological numbers for applicable documents and related vouchers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5b10c-109">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="5b10c-109">Prerequisites</span></span>

<span data-ttu-id="5b10c-110">Özellik yönetimi çalışma alanında aşağıdaki **Kronolojik numaralandırma** özelliğini açın.</span><span class="sxs-lookup"><span data-stu-id="5b10c-110">In the Feature management workspace, turn on the **Chronological numbering** feature.</span></span> <span data-ttu-id="5b10c-111">Daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5b10c-111">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="configure-chronological-numbering"></a><span data-ttu-id="5b10c-112">Kronolojik numaralandırmayı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="5b10c-112">Configure chronological numbering</span></span>

<span data-ttu-id="5b10c-113">Kronolojik numaralandırma aşağıdaki belgeleri etkiler.</span><span class="sxs-lookup"><span data-stu-id="5b10c-113">Chronological numbering affects the following documents.</span></span>

<span data-ttu-id="5b10c-114">**Alacak hesapları**</span><span class="sxs-lookup"><span data-stu-id="5b10c-114">**Accounts receivable**</span></span>
- <span data-ttu-id="5b10c-115">Müşteri faturası</span><span class="sxs-lookup"><span data-stu-id="5b10c-115">Customer invoice</span></span>
- <span data-ttu-id="5b10c-116">Müşteri faturası fişi</span><span class="sxs-lookup"><span data-stu-id="5b10c-116">Customer invoice voucher</span></span>
- <span data-ttu-id="5b10c-117">Satış alacak dekontu</span><span class="sxs-lookup"><span data-stu-id="5b10c-117">Sales credit note</span></span>
- <span data-ttu-id="5b10c-118">Satış alacak dekontu fişi</span><span class="sxs-lookup"><span data-stu-id="5b10c-118">Sales credit note voucher</span></span>
- <span data-ttu-id="5b10c-119">Dekont / Serbest metin faturası</span><span class="sxs-lookup"><span data-stu-id="5b10c-119">Free text invoice</span></span>
- <span data-ttu-id="5b10c-120">Dekont / Serbest metin faturası fişi</span><span class="sxs-lookup"><span data-stu-id="5b10c-120">Free text invoice voucher</span></span>
- <span data-ttu-id="5b10c-121">Serbest metinli alacak dekontu</span><span class="sxs-lookup"><span data-stu-id="5b10c-121">Free text credit note</span></span>
- <span data-ttu-id="5b10c-122">Serbest metinli alacak dekontu fişi</span><span class="sxs-lookup"><span data-stu-id="5b10c-122">Free text credit note voucher</span></span>
- <span data-ttu-id="5b10c-123">Sevk irsaliyesi</span><span class="sxs-lookup"><span data-stu-id="5b10c-123">Packing slip</span></span>
- <span data-ttu-id="5b10c-124">Sevk irsaliyesi fişi</span><span class="sxs-lookup"><span data-stu-id="5b10c-124">Packing slip voucher</span></span>
- <span data-ttu-id="5b10c-125">Sevk irsaliyesi düzeltme fişi</span><span class="sxs-lookup"><span data-stu-id="5b10c-125">Packing slip correction voucher</span></span>
- <span data-ttu-id="5b10c-126">Vade farkı dekontu fişi</span><span class="sxs-lookup"><span data-stu-id="5b10c-126">Interest note voucher</span></span>
- <span data-ttu-id="5b10c-127">Tahsilat mektubu fişi</span><span class="sxs-lookup"><span data-stu-id="5b10c-127">Collection letter voucher</span></span>

<span data-ttu-id="5b10c-128">**Borç hesapları**</span><span class="sxs-lookup"><span data-stu-id="5b10c-128">**Accounts payable**</span></span>
- <span data-ttu-id="5b10c-129">Fatura fişi</span><span class="sxs-lookup"><span data-stu-id="5b10c-129">Invoice voucher</span></span>
- <span data-ttu-id="5b10c-130">Alacak dekontu fişi</span><span class="sxs-lookup"><span data-stu-id="5b10c-130">Credit note voucher</span></span>
- <span data-ttu-id="5b10c-131">Ürün giriş fişi</span><span class="sxs-lookup"><span data-stu-id="5b10c-131">Product receipt voucher</span></span>

<span data-ttu-id="5b10c-132">**Proje yönetimi**</span><span class="sxs-lookup"><span data-stu-id="5b10c-132">**Project management**</span></span>
- <span data-ttu-id="5b10c-133">Fatura</span><span class="sxs-lookup"><span data-stu-id="5b10c-133">Invoice</span></span>
- <span data-ttu-id="5b10c-134">Fatura fişi</span><span class="sxs-lookup"><span data-stu-id="5b10c-134">Invoice voucher</span></span>
- <span data-ttu-id="5b10c-135">Alacak dekontu</span><span class="sxs-lookup"><span data-stu-id="5b10c-135">Credit note</span></span>
- <span data-ttu-id="5b10c-136">Alacak dekontu fişi</span><span class="sxs-lookup"><span data-stu-id="5b10c-136">Credit note voucher</span></span> 

### <a name="define-number-sequences"></a><span data-ttu-id="5b10c-137">Numara serileri tanımlama</span><span class="sxs-lookup"><span data-stu-id="5b10c-137">Define number sequences</span></span>

<span data-ttu-id="5b10c-138">Numara serilerini tanımlamak için **Kuruluş yönetimi** > **Numara serileri** > **Numara serileri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="5b10c-138">To define number sequences, go to **Organization administration** > **Number sequences** > **Number sequences**.</span></span> <span data-ttu-id="5b10c-139">Gerekli belgeler için etkilenen dönemleri kapsamak için gereken sayıda numara serisi tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5b10c-139">You can define as many number sequences as required to cover the affected periods for required documents.</span></span> 

<span data-ttu-id="5b10c-140">Her numara serisi için bir şirket belirtin.</span><span class="sxs-lookup"><span data-stu-id="5b10c-140">Specify a company for each number sequence.</span></span> <span data-ttu-id="5b10c-141">Numara serilerinin segmentleri, dönemler için kronolojik sıra sağlayacak şekilde tanımlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5b10c-141">The segments of the number sequences must be defined so that they provide chronological order for periods.</span></span> <span data-ttu-id="5b10c-142">Örneğin, segment adları belirli bir dönemi tanımlayan özel bir önek içerebilir.</span><span class="sxs-lookup"><span data-stu-id="5b10c-142">For example, the segment names can contain a special prefix that identifies a specific period.</span></span>

![Numara serisi kurulumu](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a><span data-ttu-id="5b10c-144">Numara serisi gruplarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="5b10c-144">Configure number sequence groups</span></span>

<span data-ttu-id="5b10c-145">Numara serisi gruplarını konfigüre etmek için **Alacak hesapları** > **Kurulum** > **Alacak hesapları parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="5b10c-145">To configure number sequence groups, go to **Accounts receivable** > **Setup** > **Accounts receivable parameters**.</span></span> <span data-ttu-id="5b10c-146">**Numara serileri** sekmesinde, etkilenen dönemleri kapsamak için gereken sayıda numara serisi grubu tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="5b10c-146">On the **Number sequences** tab, define as many number sequences groups as required to cover the affected periods.</span></span> 

<span data-ttu-id="5b10c-147">Her grup için, **Referans** bölümünde desteklenen belge referanslarından birini seçin ve **Numara serisi kodu** alanında, daha önce ilgili dönem için oluşturulan bir numara serisine referans verin.</span><span class="sxs-lookup"><span data-stu-id="5b10c-147">For each group, in the **Reference** section, select one of the supported document references, and in the **Number sequence code** field, refer to a number sequence that was previously created for the related period.</span></span>

![Numara serisi grubu kurulumu](media/chrono-num-sequence-group.jpg)

<span data-ttu-id="5b10c-149">Benzer şekilde, **Borç hesaplarında** ve **Proje yönetimi ve muhasebe** modüllerinde numara serileri gruplarını yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="5b10c-149">Similarly, configure number sequence groups in **Accounts payable** and **Project management and accounting** modules.</span></span>

### <a name="configure-number-sequence-groups-chronology"></a><span data-ttu-id="5b10c-150">Numara serisi grupları kronolojisini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="5b10c-150">Configure number sequence groups chronology</span></span>

<span data-ttu-id="5b10c-151">Numara serisi grupları kronolojisini yapılandırmak için **Kuruluş yönetimi** > **Numara serileri** > **Kronolojik numara serisi grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="5b10c-151">To configure number sequence groups chronology, go to **Organization administration** > **Number sequences** > **Chronological number sequence groups**.</span></span> <span data-ttu-id="5b10c-152">Numara serisi grupları için uygulanabilirlik koşullarını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="5b10c-152">Define the applicability conditions for number sequence groups.</span></span>

![Kronolojik numaralar kurulumu](media/chrono-num-sequence-group-period.jpg)

| <span data-ttu-id="5b10c-154">Alan</span><span class="sxs-lookup"><span data-stu-id="5b10c-154">Field</span></span>            | <span data-ttu-id="5b10c-155">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b10c-155">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b10c-156">Yürürlüğe giriş</span><span class="sxs-lookup"><span data-stu-id="5b10c-156">Effective</span></span>  | <span data-ttu-id="5b10c-157">Numara serisi grubunun geçerlilik başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="5b10c-157">The start date of number sequence group applicability.</span></span> |
| <span data-ttu-id="5b10c-158">Bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="5b10c-158">Expiration</span></span>      | <span data-ttu-id="5b10c-159">Numara serisi grubunun geçerlilik bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="5b10c-159">The end date of number sequence group applicability.</span></span> <span data-ttu-id="5b10c-160">Bitiş tarihi uygulanmamışsa, **Asla** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="5b10c-160">If no end date is applied, select **Never**.</span></span> |
| <span data-ttu-id="5b10c-161">Numara serisi grubu</span><span class="sxs-lookup"><span data-stu-id="5b10c-161">Number sequence group</span></span> | <span data-ttu-id="5b10c-162">Dönem içinde belge numaraları oluşturmak için kullanılacak numara serisi grubu.</span><span class="sxs-lookup"><span data-stu-id="5b10c-162">Number sequence group that will be used to generate document numbers during the period.</span></span> |
| <span data-ttu-id="5b10c-163">Özgün numara serisi grubu</span><span class="sxs-lookup"><span data-stu-id="5b10c-163">Original number sequence group</span></span> | <span data-ttu-id="5b10c-164">Bu numara serisi grubu kodu, belgelerin zaten belirli bir *kalıcı* numara serisi grubu için atanmış olduğu durumlarda ek filtre uygulama amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5b10c-164">This number sequence group code is used for additional filtering for the cases when documents already have a specific *permanent* number sequence group assigned.</span></span> <span data-ttu-id="5b10c-165">Boş değer belirli bir değer olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="5b10c-165">An empty value is considered a specific value.</span></span> <span data-ttu-id="5b10c-166">Geçici olarak atanan bir grubu dikkate almanız gerekiyorsa bu kurulum için **Varsayılan** seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5b10c-166">If you need to ignore a preliminary assigned group, use the **Default** option for this setup.</span></span> |
| <span data-ttu-id="5b10c-167">Varsayılan</span><span class="sxs-lookup"><span data-stu-id="5b10c-167">Default</span></span> | <span data-ttu-id="5b10c-168">Açıksa sistem, geçici atanan belge numara serisi grubunu yoksayar ve yalnızca dönem başlangıç ve bitiş tarihlerini geçerlilik analizi için kullanır.</span><span class="sxs-lookup"><span data-stu-id="5b10c-168">If turned on, the system ignores the preliminary assigned document number sequence group and uses only the periods start and end dates for applicability analysis.</span></span> <span data-ttu-id="5b10c-169">Kapalıysa, sistem, seçim için **Geçerlilik** + **Sona Erme** + **Orijinal numara serisi grubu** tam kombinasyonunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="5b10c-169">If turned off, the system uses the full combination **Effective** + **Expiration** + **Original number sequence group** for selection.</span></span> |

## <a name="document-posting"></a><span data-ttu-id="5b10c-170">Belge deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="5b10c-170">Document posting</span></span>
<span data-ttu-id="5b10c-171">Bir belgeyi deftere naklettiğinizde, belgenin deftere nakil tarihi temel alınarak ilgili numara serisi grubu belgeye atanır ve sonra algılanan numara serisine göre bir belge numarası oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5b10c-171">When you post a document, the appropriate number sequence group is assigned to the document, based on document's posting date, and then used to generate a document number based on the detected number sequence.</span></span> <span data-ttu-id="5b10c-172">Sistem, numara serisi grubu atamasıyla ilgili bir ileti sağlar.</span><span class="sxs-lookup"><span data-stu-id="5b10c-172">The system provides a message regarding the number sequence group assignment.</span></span>

![Belge numarası](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> <span data-ttu-id="5b10c-174">Bazı ülke/bölgelerde belge numaralandırması için önceden uygulanmış belirli bir mantık vardır.</span><span class="sxs-lookup"><span data-stu-id="5b10c-174">For some countries, there is a specific logic already implemented for document numbering.</span></span> <span data-ttu-id="5b10c-175">Bu durumda, ülkeye özel mantık, **Kronolojik numaralandırma** özelliğini geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="5b10c-175">In this case, country-specific logic will override the **Chronological numbering** feature.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

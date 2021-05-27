---
title: Hindistan Kaynakta Kesilen Vergi'ye (TDS) genel bakış
description: Bu konu, Hindistan Kaynakta Kesilen Vergi (TDS) hakkında ayrıntılı bilgiler sağlar. TDS belgeleri, bu özelliğin işlevselliğini kapsamaktadır.
author: kailiang
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 28ee843036e11bd37b97a065ce53d2eb860c79d9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023671"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a><span data-ttu-id="7b6ef-104">Hindistan Kaynakta Kesilen Vergi'ye (TDS) genel bakış</span><span class="sxs-lookup"><span data-stu-id="7b6ef-104">Indian Tax Deducted at Source (TDS) overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b6ef-105">Bu konu, Hindistan Kaynakta Kesilen Vergi (TDS) hakkında ayrıntılı bilgiler sağlar.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-105">This topic provides detailed information about Indian Tax Deducted at Source (TDS).</span></span>

<span data-ttu-id="7b6ef-106">TDS belgeleri, bu özelliğin işlevselliğini kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-106">The TDS documentation covers the functionality of this capability.</span></span> <span data-ttu-id="7b6ef-107">Ayrıca, TDS için temel kurulum yapma, hareketlerde TDS hesaplama, TDS kapatma işlecini tamamlama, TDS sertifika numaralarını kaydetme ve TDS sorguları, TDS deyimleri ve TDS sertifikaları oluşturma gibi konuları açıklar.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-107">It also explains how to do the basic setup for TDS, calculate TDS on transactions, complete the TDS settlement process, record TDS certificate numbers, and generate TDS inquiries, TDS statements, and TDS certificates.</span></span> <span data-ttu-id="7b6ef-108">Belgeler, aşağıdaki konuları içerir:</span><span class="sxs-lookup"><span data-stu-id="7b6ef-108">The documentation includes the following topics:</span></span>

- [<span data-ttu-id="7b6ef-109">TDS için temel kurulum</span><span class="sxs-lookup"><span data-stu-id="7b6ef-109">Basic setup for TDS</span></span>](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [<span data-ttu-id="7b6ef-110">TDS hesaplaması için kullanılan formül tasarımcısı ve eşik sınırı işlevi</span><span class="sxs-lookup"><span data-stu-id="7b6ef-110">Formula designer and threshold limit functionality used for TDS calculation</span></span>](apac-ind-TDS-Formula-designer.md)
- [<span data-ttu-id="7b6ef-111">Faturalardaki, ödemelerde, senetlerde ve şirketlerarası hareketlerde TDS hesaplanması</span><span class="sxs-lookup"><span data-stu-id="7b6ef-111">Calculation of TDS on invoices, payments, promissory notes, and intercompany transactions</span></span>](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [<span data-ttu-id="7b6ef-112">Dönemsel TDS kapatma işlemi ve TDS tutarlarının TDS yetkili satıcılarına kapatılması</span><span class="sxs-lookup"><span data-stu-id="7b6ef-112">Periodic TDS settlement process and settlement of TDS amounts to TDS authority vendors</span></span>](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [<span data-ttu-id="7b6ef-113">TDS sertifika numaraları ve tarihlerini kaydetme ve güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="7b6ef-113">Recording and updating TDS certificate numbers and dates</span></span>](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a><span data-ttu-id="7b6ef-114">TDS'ye giriş</span><span class="sxs-lookup"><span data-stu-id="7b6ef-114">Introduction to TDS</span></span>

<span data-ttu-id="7b6ef-115">1961 tarihli Gelir Vergisi Kanunu'na göre vergiler, hizmeti alan kişi tarafından avans ödemesi veya alacağın muhasebesi (hangisi önce gerçekleşirse) sırasında kaynakta kesilir.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-115">Per the Income tax Act, 1961, income tax is deducted at the source by the receiver of the service at the time of advance payment or accounting of credit, whichever occurs first.</span></span> <span data-ttu-id="7b6ef-116">Ödemeyi yapan kişi, vergi tutarını düşmeli ve yalnızca net bakiyeyi servis sağlayıcısına ödemelidir.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-116">The person who makes the payment must deduct the tax amount and pay only the net balance to the provider of the service.</span></span> <span data-ttu-id="7b6ef-117">TDS, devlet tarafından belirtilen hizmetlere uygulanır ve devletin bir dönem için belirttiği oranlar kullanılarak kesilir.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-117">TDS is applied on services that the government specifies, and the tax is deducted by using the rates that the government specifies for a period.</span></span> <span data-ttu-id="7b6ef-118">Kesinti oranı, ödemeyi alan veya servisi sağlayan varlığın durumuna bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-118">The rate of deduction is based on the status of the entity that receives the payment or provides the service.</span></span> <span data-ttu-id="7b6ef-119">Durumlar arasında şunlar yer alır: **Bağımsız**, **Hindu Bölünmemiş Aile** (**HUF**), **Şirket**, **Firma**, **Kişiler İştirakı** (**AOP**) **Kişiler Kuruluşu** (**BOI**) ve **Yerel makamlar**.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-119">Statuses include **Individual**, **Hindu Undivided Family** (**HUF**), **Company**, **Firm**, **Association of Persons** (**AOP**), **Body of Individuals** (**BOI**), and **Local authority**.</span></span>

<span data-ttu-id="7b6ef-120">Aşağıdaki bölümlerde, Hindistan Hükümeti tarafından belirtildiği şekilde, TDS'nin uygulandığı hizmetler listesi verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-120">The following sections list the services that TDS is applied on, as specified by the Government of India.</span></span>

<span data-ttu-id="7b6ef-121">**Yerleşik olanlar**</span><span class="sxs-lookup"><span data-stu-id="7b6ef-121">**Residents**</span></span>

- <span data-ttu-id="7b6ef-122">Maaşlardan edilen gelir (Bölüm 192 altında)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-122">Income from salaries (Under section 192)</span></span>
- <span data-ttu-id="7b6ef-123">Menkul kıymet faizlerinden edilen gelir (Bölüm 193 altında)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-123">Income from interest on securities (Under section 193)</span></span>
- <span data-ttu-id="7b6ef-124">Temettülerden edilen gelir (Bölüm 194 altında)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-124">Income from dividend (Under section 194)</span></span>
- <span data-ttu-id="7b6ef-125">Faizden edilen gelir (Bölüm 194A altında)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-125">Income from interest (Under section 194A)</span></span>
- <span data-ttu-id="7b6ef-126">Şans oyunları veya bilmecelerden edilen gelir (Bölüm 194B altında)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-126">Income from lotteries or puzzles (Under section 194B)</span></span>
- <span data-ttu-id="7b6ef-127">At yarışı vb. oyunlardan edilen gelir (Bölüm 194BB altında)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-127">Winning from horse races etc. (Under section 194BB)</span></span>
- <span data-ttu-id="7b6ef-128">Yükleniciler ve alt yükleniciler (Bölüm 194C altında)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-128">Contractors and sub-contractors (Under section 194C)</span></span>
- <span data-ttu-id="7b6ef-129">Sigorta komisyonu (Bölüm 194D altında)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-129">Insurance commission (Under section 194D)</span></span>
- <span data-ttu-id="7b6ef-130">Ulusal tasarruf şeması altında yer alan depozitodan edilen gelir (Bölüm 194EE altında)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-130">Income from deposit under national saving scheme (Under section 194EE)</span></span>
- <span data-ttu-id="7b6ef-131">Yatırım fonu veya UTI'den edilen gelir (Bölüm 194F altında)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-131">Income from mutual fund or UTI (Under section 194F)</span></span>
- <span data-ttu-id="7b6ef-132">Satış veya şans oyunlarında Komisyon, Karşılık, Ödül vb. (Bölüm 194G altında)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-132">Commission, Remuneration, Prize etc., on sale or lottery (Under section 194G)</span></span>
- <span data-ttu-id="7b6ef-133">Komisyon veya aracılık ödemesi (Bölüm 194H altında)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-133">Payment of Commission or brokerage (Under section 194H)</span></span>
- <span data-ttu-id="7b6ef-134">Kira (Bölüm 194I altında)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-134">Rent (Under section 194I)</span></span>
- <span data-ttu-id="7b6ef-135">Profesyonel hizmet (Bölüm 194J altında)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-135">Professional service (Under section 194J)</span></span>
- <span data-ttu-id="7b6ef-136">Birimlerden edilen gelir (Bölüm 194K altında)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-136">Income from Units (Under section 194K)</span></span>
- <span data-ttu-id="7b6ef-137">Belirli gayrimenkul malın edinmesiyle ilgili ücret ödemesi (Bölüm 194LA altında)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-137">Payment of compensation on acquisition of certain immovable property (Under section 194LA)</span></span>

<span data-ttu-id="7b6ef-138">**Yerleşik olmayanlar**</span><span class="sxs-lookup"><span data-stu-id="7b6ef-138">**Non-residents**</span></span>

- <span data-ttu-id="7b6ef-139">Yerleşik olmayan sporculara veya spor birliklerine ödemeler (Bölüm 194E altında)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-139">Payments to Non-resident sportsmen or sports association (Under section 194E)</span></span>
- <span data-ttu-id="7b6ef-140">Diğer toplamlar (Bölüm 195 altında)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-140">Other sums (Under section 195)</span></span>
- <span data-ttu-id="7b6ef-141">Yerleşik olmayan birimlerden edilen gelir (Bölüm 196A altında)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-141">Income in respect of units of non-residents (Under section 196A)</span></span>

    - <span data-ttu-id="7b6ef-142">Yabancı para birimi tahvilleri veya Hint şirketi hisselerinden edilen gelir (Bölüm 196C altında)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-142">Income from foreign currency bonds or shares of Indian Company (Under section 196C)</span></span>
    - <span data-ttu-id="7b6ef-143">Menkul değerlerin yabancı kurumsal yatırımlarından edilen gelir (Bölüm 196D altında)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-143">Incomes of foreign institutional investors from securities (Under section 196D)</span></span>
    - <span data-ttu-id="7b6ef-144">Doğrudan gelirler altındaki maaş ve diğer tüm pozitif gelirler (Bölüm 192)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-144">Salary and all other positive incomes under any head on income (Section 192)</span></span>
    - <span data-ttu-id="7b6ef-145">Menkul kıymetlerin faizi (Bölüm 193)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-145">Interest on securities (Section 193)</span></span>
    - <span data-ttu-id="7b6ef-146">Menkul kıymet faizleri dışındaki faizler (Bölüm 194A)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-146">Interest other than interest on securities (Section 194A)</span></span>
    - <span data-ttu-id="7b6ef-147">Yükleniciler ve alt yüklenicilere ödemeler (Bölüm 194C)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-147">Payments to contractors and sub-contractors (Section 194C)</span></span>
    - <span data-ttu-id="7b6ef-148">Şans oyunları veya bilmecelerden kazanılanlar (Bölüm 194B)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-148">Winnings from Lottery or crossword puzzles (Section 194B)</span></span>
    - <span data-ttu-id="7b6ef-149">At yarışı oyunlardan kazançlar (Bölüm 194BB)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-149">Winnings from horse races (Section 194BB)</span></span>
    - <span data-ttu-id="7b6ef-150">Sigorta işinin tedariği için tüm ödemeleri kapsayan Sigorta Komisyonu (Bölüm 194D)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-150">Insurance Commission covering all payments for procuring Insurance business (Section 194D)</span></span>
    - <span data-ttu-id="7b6ef-151">Şirket olmayan yerleşik olmayanlara veya yabancı bir şirkete menkul kıymet faizi dışında ödenecek faizler (Bölüm 195)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-151">Any interest other than interest on securities payable to non-residents not being a company or to a foreign company (Section 195)</span></span>
    - <span data-ttu-id="7b6ef-152">Yerleşik olmayan sporculara (spor birliği veya kuruluşu dahil) ödeme.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-152">Payment to non-resident sportsman including athlete or sports association or institution.</span></span> <span data-ttu-id="7b6ef-153">Yerleşik olmayan sporcular söz konusu olduğunda Hint gazeteleri, dergileri ve benzeri yerlerde yayınlanması için oyun/sporlarla ilgili reklam ve yazı ödemeleri.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-153">In case of non-resident sportsman, payments in respect of advertisements as well as articles on any game/sports in India in newspapers, magazines, and so.</span></span> <span data-ttu-id="7b6ef-154">dahil edilir (Bölüm 194E)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-154">is included (Section 194E)</span></span>
    - <span data-ttu-id="7b6ef-155">NSS \[Ulusal Tasarruf Şeması \] altında depozitolarla ilgili ödeme (Bölüm 194EE)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-155">Payment in respect of deposits under NSS \[National Savings Scheme\] (Section 194EE)</span></span>
    - <span data-ttu-id="7b6ef-156">Yatırım Fonu veya UTI tarafından Birimlerin tekrar satınalımıyla ilgili ödeme (Bölüm 194F)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-156">Payment on account of repurchase of Units by Mutual Fund or UTI (Section 194F)</span></span>
    - <span data-ttu-id="7b6ef-157">Komisyon veya aracılık ödemesi (Bölüm 194H)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-157">Payment for Commission or brokerage (Section 194H)</span></span>
    - <span data-ttu-id="7b6ef-158">Kira ödemesi (Bölüm 194I)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-158">Payment of rent (Section 194I)</span></span>
    - <span data-ttu-id="7b6ef-159">Profesyonel veya teknik servisler için ödenen ücretler (Bölüm 194J)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-159">Payment of fees for professional or technical services (Section 194J)</span></span>
    - <span data-ttu-id="7b6ef-160">İlgili biletlerin karşılığı veya ödülleri dahil olmak üzere Şans oyunları biletlerinin Stokçularına, dağıtımcılarına, alıcılarına ve satıcılarına komisyon (Bölüm 194G)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-160">Commission to Stockiest, distributors, buyers and sellers of Lottery tickets including remuneration or prize on such tickets (Section 194G)</span></span>
    - <span data-ttu-id="7b6ef-161">Yabancı para birimi cinsinden satın alınan Birimlerden edilen gelir ve yabancı para birimi cinsinden satın alınan bu tür Birimlerin transferinden kaynaklanan uzun vadeli sermaye kazancı (Bölüm 196B)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-161">Income from Units purchased in foreign currency or long-term capital gain arising from the transfer of such Units purchased in foreign currency (Section 196B)</span></span>
    - <span data-ttu-id="7b6ef-162">Tahviller ve hisselerdeki faiz veya temettülerle ilgili olarak yerleşik olmayanlara ödenen tüm gelirler (Bölüm 196C)</span><span class="sxs-lookup"><span data-stu-id="7b6ef-162">Payment of any income to non-residents in respect of interest or dividend on bonds and shares (Section 196C)</span></span>

<span data-ttu-id="7b6ef-163">TDS; satınalmalar, satış, satış iadeleri, kredi notları, sabit kıymet alımları, peşinatlar, avans ödemeleri, senetler, çalışma vergisi ve şirketlerarası hareketler üzerinde hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-163">TDS is calculated on purchases, sales, sales returns, credit notes, fixed asset acquisitions, prepayments, advance payments, promissory notes, works tax, and intercompany transactions.</span></span>

> [!NOTE]
> <span data-ttu-id="7b6ef-164">Geçerli Hindistan vergi senaryosunda, TDS satış hareketlerinde hesaplanmaz.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-164">In the current Indian tax scenario, TDS isn't calculated on sales transactions.</span></span> <span data-ttu-id="7b6ef-165">Ancak sistem, özellikle şirketlerarası hareketler için satış hareketlerinde de TDS düşürülebilirlerinin hesaplanması için bir provizyon içerir.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-165">However, the system includes a provision to calculate TDS recoverable on sales transactions, especially for intercompany transactions.</span></span>

<span data-ttu-id="7b6ef-166">TDS hesaplaması her zaman, TDS bileşeni için tanımlanan eşik ve istisna eşiğini dikkate alır.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-166">The calculation of TDS always considers the threshold and the exception threshold that are defined for the TDS component.</span></span>

<span data-ttu-id="7b6ef-167">Dönemsel TDS kapatma işlemi çalıştırılmalıdır ve TDS ödemeleri, TDS yetkili satıcılarına kapatılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-167">The periodic TDS settlement process must be run, and the TDS payments must be settled to TDS authority vendors.</span></span>

<span data-ttu-id="7b6ef-168">Satıcılardan veya müşterilerden alınan TDS sertifikalarının sertifika numaraları ve tarihleri kaydedilebilir ve güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-168">The certificate numbers and dates for TDS certificates that are received from vendors or customers can be recorded and updated.</span></span> <span data-ttu-id="7b6ef-169">Ek olarak, Form 26Q ve Form 27Q üç aylık ekstreleri ve TDS ile ilgili Form 16A Finance'de oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-169">Additionally, Form 26Q and Form 27Q quarterly statements, and the Form 16A certificate for TDS, can be generated in Finance.</span></span>

## <a name="setting-up-and-working-with-tds"></a><span data-ttu-id="7b6ef-170">TDS'yi kurma ve TDS'yle çalışma</span><span class="sxs-lookup"><span data-stu-id="7b6ef-170">Setting up and working with TDS</span></span>

<span data-ttu-id="7b6ef-171">TDS kurulumu ve TDS'yle çalışma sürecine genel bakış:</span><span class="sxs-lookup"><span data-stu-id="7b6ef-171">Here is an overview of the process for setting up and working with TDS:</span></span>

1. <span data-ttu-id="7b6ef-172">**TDS kurulumu:**</span><span class="sxs-lookup"><span data-stu-id="7b6ef-172">**TDS setup:**</span></span>

    - <span data-ttu-id="7b6ef-173">Parametre kurulumu:</span><span class="sxs-lookup"><span data-stu-id="7b6ef-173">Parameter setup:</span></span>

        - <span data-ttu-id="7b6ef-174">Genel muhasebe parametrelerinde, TDS ile ilgili parametreleri etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-174">In General ledger parameters, activate parameters that are related to TDS.</span></span>
        - <span data-ttu-id="7b6ef-175">Genel muhasebe parametrelerinde, stopaj vergisi ödemelerinin numara sırasını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-175">In General ledger parameters, set up the number sequence for withholding tax payments.</span></span>
        - <span data-ttu-id="7b6ef-176">Borç hesapları ve Alacak hesaplarında parametreleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-176">Set up parameters in Accounts payable and Accounts receivable.</span></span>

    - <span data-ttu-id="7b6ef-177">Temel kurulum:</span><span class="sxs-lookup"><span data-stu-id="7b6ef-177">Basic setup:</span></span>

        - <span data-ttu-id="7b6ef-178">Bir şirket, müşteriler ve satıcılar için TDS kayıt numaralarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-178">Set up TDS registration numbers for a company, customers, and vendors.</span></span>
        - <span data-ttu-id="7b6ef-179">TDS bileşeni gruplarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-179">Set up TDS component groups.</span></span>
        - <span data-ttu-id="7b6ef-180">TDS bileşenlerini ayarlayın, bunlara TDS bileşen gruplarını iliştirin ve bunlar için eşiği ve istisna eşiğini tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-180">Set up TDS components, attach TDS component groups to them, and define the threshold and exception threshold for them.</span></span>
        - <span data-ttu-id="7b6ef-181">TDS yetkililerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-181">Set up TDS authorities.</span></span>
        - <span data-ttu-id="7b6ef-182">TDS kapatma dönemlerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-182">Set up TDS settlement periods.</span></span>
        - <span data-ttu-id="7b6ef-183">TDS vergi kodlarını ayarlayın ve bunlara TDS bileşenlerini iliştirin.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-183">Set up TDS tax codes, and attach TDS components to them.</span></span>
        - <span data-ttu-id="7b6ef-184">TDS vergi gruplarını ayarlayın ve bunlara TDS vergi kodlarını iliştirin.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-184">Set up TDS tax groups, and attach TDS tax codes to them.</span></span>
        - <span data-ttu-id="7b6ef-185">Formül tasarımcısında, TDS grubu için TDS hesaplamasını yapmak üzere bir formül tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-185">In the formula designer, define a formula to calculate TDS for a TDS group.</span></span>
        - <span data-ttu-id="7b6ef-186">TDS imtiyaz sertifikası numaralarını kaydedin.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-186">Record TDS concession certificate numbers.</span></span>

    - <span data-ttu-id="7b6ef-187">Genel muhasebe hesapları ve şirket kurulumu:</span><span class="sxs-lookup"><span data-stu-id="7b6ef-187">Ledger accounts and company setup:</span></span>

        - <span data-ttu-id="7b6ef-188">TDS alacak ve borç genel muhasebe hesapları kurma:</span><span class="sxs-lookup"><span data-stu-id="7b6ef-188">Set up TDS payable and receivable ledger accounts.</span></span>
        - <span data-ttu-id="7b6ef-189">Şirket için bir Vergi Kesintisi ve Tahsilat Hesap Numarası (TAN) ile bir kesinti türü kategorisi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-189">Set up a Tax Deduction and Collection Account Number (TAN) and a deductor type category for the company.</span></span>

    - <span data-ttu-id="7b6ef-190">Diğer kurulum:</span><span class="sxs-lookup"><span data-stu-id="7b6ef-190">Other setup:</span></span>

        - <span data-ttu-id="7b6ef-191">TDS tahsisatını içeren bir ödeme planı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-191">Set up a payment schedule that includes TDS allocation.</span></span>
        - <span data-ttu-id="7b6ef-192">TDS yetkilisine yapılacak ödemeler için bir ödeme ücreti türü ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-192">Set up a payment fee type for payments to the TDS authority.</span></span>
        - <span data-ttu-id="7b6ef-193">Satıcı ve müşteriler için TDS grupları, kalıcı hesap numaraları (PAN'lar) ve için TAN'lar ile ilgili bilgileri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-193">Set up information about TDS groups, permanent account numbers (PANs), and TANs for vendors and customers.</span></span>

2. <span data-ttu-id="7b6ef-194">**Hareketlerde TDS hesaplaması:**</span><span class="sxs-lookup"><span data-stu-id="7b6ef-194">**Calculation of TDS in transactions:**</span></span>

    - <span data-ttu-id="7b6ef-195">Faturalar ve ödemeler</span><span class="sxs-lookup"><span data-stu-id="7b6ef-195">Invoices and payments</span></span>
    - <span data-ttu-id="7b6ef-196">Senetler</span><span class="sxs-lookup"><span data-stu-id="7b6ef-196">Promissory notes</span></span>
    - <span data-ttu-id="7b6ef-197">Avans ödemeleri</span><span class="sxs-lookup"><span data-stu-id="7b6ef-197">Advance payments</span></span>
    - <span data-ttu-id="7b6ef-198">Ön ödemeler</span><span class="sxs-lookup"><span data-stu-id="7b6ef-198">Prepayments</span></span>

3. <span data-ttu-id="7b6ef-199">**TDS kapanışı.**</span><span class="sxs-lookup"><span data-stu-id="7b6ef-199">**TDS settlement:**</span></span>

    - <span data-ttu-id="7b6ef-200">Dönemsel TDS kapatma işlemi</span><span class="sxs-lookup"><span data-stu-id="7b6ef-200">Periodic TDS settlement process</span></span>
    - <span data-ttu-id="7b6ef-201">TDS yetkili satıcılarına TDS ödemelerinin kapatılması ve TDS irsaliyesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7b6ef-201">Settlement of TDS payments to TDS authority vendors and generation of TDS challan</span></span>

4. <span data-ttu-id="7b6ef-202">**TDS sorguları, deyimleri ve sertifikaları:**</span><span class="sxs-lookup"><span data-stu-id="7b6ef-202">**TDS inquiries, statements, and certificate:**</span></span>

    - <span data-ttu-id="7b6ef-203">TDS sertifika numaraları ve tarihlerini kaydedin ve güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-203">Record and update TDS certificate numbers and dates.</span></span>
    - <span data-ttu-id="7b6ef-204">TDS sorgusu ve deftere nakledilmiş TDS sorgusu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-204">Generate a TDS inquiry and a posted TDS inquiry.</span></span>
    - <span data-ttu-id="7b6ef-205">Form 27A, Form 26q ve Form 27Q TDS ve e-TDS üç aylık ekstreler oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-205">Generate Form 27A, Form 26Q, and Form 27Q TDS and e-TDS quarterly statements.</span></span>
    - <span data-ttu-id="7b6ef-206">Form 16A TDS sertifikası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7b6ef-206">Generate a Form 16A TDS certificate.</span></span>

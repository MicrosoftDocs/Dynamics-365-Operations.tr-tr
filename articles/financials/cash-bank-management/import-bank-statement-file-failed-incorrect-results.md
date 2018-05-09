---
title: "Banka ekstresi dosya alma sorunlarını giderme"
description: "Bankadan gelen banka ekstresi dosyasının, Microsoft Dynamics 365 for Finance and Operations tarafından desteklenen düzenle eşleşmesi önemlidir. Banka ekstreleri için sıkı standartlar bulunduğundan çoğu tümleştirme doğru şekilde çalışacaktır. Ancak, bazen ekstre dosyası alınamayabilir veya hatalı sonuçlara sahip olabilir. Genellikle, bu sorunlar banka ekstresi dosyasındaki küçük farklılıklar nedeniyle ortaya çıkar. Bu makale, bu farklılıkları gidermeyi ve sorunların nasıl çözüleceğini açıklar."
author: twheeloc
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4796a440bec7c5c0e77a57beccb9379bd2978df6
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="c31d8-107">Banka ekstresi dosya alma sorunlarını giderme</span><span class="sxs-lookup"><span data-stu-id="c31d8-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c31d8-108">Bankadan gelen banka ekstresi dosyasının, Microsoft Dynamics 365 for Finance and Operations tarafından desteklenen düzenle eşleşmesi önemlidir.</span><span class="sxs-lookup"><span data-stu-id="c31d8-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 for Finance and Operations supports.</span></span> <span data-ttu-id="c31d8-109">Banka ekstreleri için sıkı standartlar bulunduğundan çoğu tümleştirme doğru şekilde çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="c31d8-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="c31d8-110">Ancak, bazen ekstre dosyası alınamayabilir veya hatalı sonuçlara sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="c31d8-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="c31d8-111">Genellikle, bu sorunlar banka ekstresi dosyasındaki küçük farklılıklar nedeniyle ortaya çıkar.</span><span class="sxs-lookup"><span data-stu-id="c31d8-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="c31d8-112">Bu makale, bu farklılıkları gidermeyi ve sorunların nasıl çözüleceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="c31d8-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="c31d8-113">Hata nedir?</span><span class="sxs-lookup"><span data-stu-id="c31d8-113">What is the error?</span></span>
------------------

<span data-ttu-id="c31d8-114">Bir banka ekstresi doyasını içe aktarmaya çalıştıktan sonra, hatayı bulmak için Veri yönetimi iş geçmişine ve yürütme ayrıntılarına gidin.</span><span class="sxs-lookup"><span data-stu-id="c31d8-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="c31d8-115">Hata, ekstre, bilanço ya da ekstre satırına yönlendirerek yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="c31d8-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="c31d8-116">Ancak soruna neden olan alan veya öğeyi tanımlamanıza yardımcı olmaya yeterli olacak bilgi vermesi olası değildir.</span><span class="sxs-lookup"><span data-stu-id="c31d8-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="c31d8-117">Farklar nelerdir?</span><span class="sxs-lookup"><span data-stu-id="c31d8-117">What are the differences?</span></span>
<span data-ttu-id="c31d8-118">Banka dosya düzeni tanımını, Finance and Operations içe aktarma tanımıyla kıyaslayın ve alanlar ve öğelerdeki farklılıkları not edin.</span><span class="sxs-lookup"><span data-stu-id="c31d8-118">Compare the bank file layout definition to the Finance and Operations import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="c31d8-119">Banka ekstreleri dosyasını ilgili örnek Finance and Operations dosyasıyla karşılaştırın.</span><span class="sxs-lookup"><span data-stu-id="c31d8-119">Compare the bank statement file to the related sample Finance and Operations file.</span></span> <span data-ttu-id="c31d8-120">ISO20022 dosyalarında farkları görmek kolaydır.</span><span class="sxs-lookup"><span data-stu-id="c31d8-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="transformations"></a><span data-ttu-id="c31d8-121">Dönüşümler</span><span class="sxs-lookup"><span data-stu-id="c31d8-121">Transformations</span></span>
<span data-ttu-id="c31d8-122">Genellikle, bu değişiklikler üç dönüşümden birinde yapılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c31d8-122">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="c31d8-123">Her bir dönüşüm belirli bir standart için yazılır.</span><span class="sxs-lookup"><span data-stu-id="c31d8-123">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="c31d8-124">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="c31d8-124">Resource name</span></span>                                         | <span data-ttu-id="c31d8-125">Dosya adı</span><span class="sxs-lookup"><span data-stu-id="c31d8-125">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="c31d8-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="c31d8-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="c31d8-127">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="c31d8-127">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="c31d8-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="c31d8-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="c31d8-129">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="c31d8-129">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="c31d8-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="c31d8-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="c31d8-131">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="c31d8-131">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="c31d8-132">Hata ayıklama dönüştürmeleri</span><span class="sxs-lookup"><span data-stu-id="c31d8-132">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="c31d8-133">BAI2 ve MT940 dosyalarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="c31d8-133">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="c31d8-134">BAI2 ve MT940 dosyaları metin tabanlı dosyalardır ve Genişletilebilir Stil Sayfası Dil Dönüşümleri (XSLT) hata ayıklamayı etkinleştirmek için bir düzeltme gerektirir.</span><span class="sxs-lookup"><span data-stu-id="c31d8-134">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="c31d8-135">Program bu ayarlamayı bir dosya içe aktarıldığında yapar.</span><span class="sxs-lookup"><span data-stu-id="c31d8-135">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="c31d8-136">Bir XML dosyası oluşturun ve aşağıdaki metni içine kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="c31d8-136">Create an XML file, and copy the following text into it.</span></span>

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  <span data-ttu-id="c31d8-137">Banka ekstresi dosyasının içeriğini kopyalayın ve bunları XML dosyasına yapıştırarak **PASTESTATEMENTFILEHERE**'ın yerine geçmesini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="c31d8-137">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="c31d8-138">XSLT hata ayıklama</span><span class="sxs-lookup"><span data-stu-id="c31d8-138">Debug the XSLT</span></span>

<span data-ttu-id="c31d8-139">Daha fazla bilgi için <https://msdn.microsoft.com/en-us/library/ms255605.aspx> konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="c31d8-139">For more information, see <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="c31d8-140">Microsoft Visual Studio'yu Başlatın.</span><span class="sxs-lookup"><span data-stu-id="c31d8-140">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="c31d8-141">Bir konsol uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c31d8-141">Create a console application.</span></span>
3.  <span data-ttu-id="c31d8-142">Uygun XSLT'yi açın.</span><span class="sxs-lookup"><span data-stu-id="c31d8-142">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="c31d8-143">XLST'yi ve özellikleri sayfasını tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c31d8-143">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="c31d8-144">Girişi, banka ekstresi dosyasının konumuna ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c31d8-144">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="c31d8-145">Çıktı için bir konum ve dosya adı tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="c31d8-145">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="c31d8-146">Gerekli kesme noktalarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c31d8-146">Set the required break points.</span></span>
8.  <span data-ttu-id="c31d8-147">Menüde **XML** &gt; **XSLT Hata Ayıklamayı Başlat**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c31d8-147">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="c31d8-148">XSLT çıktısını biçimlendirin</span><span class="sxs-lookup"><span data-stu-id="c31d8-148">Format the XSLT output</span></span>

<span data-ttu-id="c31d8-149">Dönüşüm yürütüldüğünde, Visual Studio'da görüntüleyebileceğiniz bir çıktı dosyası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c31d8-149">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="c31d8-150">Çıktı dosyasını hızlı şekilde biçimlendirmek için Ctrl+A, Ctrl+K, and Ctrl+D kullanın.</span><span class="sxs-lookup"><span data-stu-id="c31d8-150">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="c31d8-151">Dönüştürmeyi ayarlayın</span><span class="sxs-lookup"><span data-stu-id="c31d8-151">Adjust the transformation</span></span>

<span data-ttu-id="c31d8-152">Banka ekstresi dosyasında uygun bir alan veya öğeyi almak için dönüştürmeyi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c31d8-152">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="c31d8-153">Sonra bu alanı veya öğeyi uygun Finance and Operations öğesine eşleyin.</span><span class="sxs-lookup"><span data-stu-id="c31d8-153">Then map that field or element to the appropriate Finance and Operations element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="c31d8-154">Borç/Alacak göstergesi</span><span class="sxs-lookup"><span data-stu-id="c31d8-154">Debit/credit indicator</span></span>

<span data-ttu-id="c31d8-155">Bazı durumlarda, borçlar alacak olarak ve alacaklar borç olarak içeri aktarılmış olabilir.</span><span class="sxs-lookup"><span data-stu-id="c31d8-155">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="c31d8-156">Bu sorunu gidermek için uygun XSLT'yi değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c31d8-156">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="c31d8-157">Banka Ekstrelerini birden çok bankadan geliyorsa, bunların tümünün aynı borç/alacak yaklaşımını kullandığından veya ayrı dönüşümleri oluşturduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="c31d8-157">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="c31d8-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator şablonu</span><span class="sxs-lookup"><span data-stu-id="c31d8-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="c31d8-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit şablonu</span><span class="sxs-lookup"><span data-stu-id="c31d8-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="c31d8-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator şablonu</span><span class="sxs-lookup"><span data-stu-id="c31d8-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="c31d8-161">Banka ekstresi biçimleri ve teknik düzenlerine örnekler</span><span class="sxs-lookup"><span data-stu-id="c31d8-161">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="c31d8-162">Aşağıdaki tablo gelişmiş banka mutabakatı içe alma dosyaları ve üç ilgili banka ekstresi örnek dosyalarının teknik düzen tanımlarını örnek olarak verir.</span><span class="sxs-lookup"><span data-stu-id="c31d8-162">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="c31d8-163">Örnek dosyaları ve teknik düzenleri buradan indirebilirsiniz: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="c31d8-163">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="c31d8-164">Teknik düzen tanımı</span><span class="sxs-lookup"><span data-stu-id="c31d8-164">Technical layout definition</span></span>                             | <span data-ttu-id="c31d8-165">Banka ekstresi örnek dosya</span><span class="sxs-lookup"><span data-stu-id="c31d8-165">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="c31d8-166">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="c31d8-166">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="c31d8-167">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="c31d8-167">MT940StatementExample</span></span>                |
| <span data-ttu-id="c31d8-168">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="c31d8-168">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="c31d8-169">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="c31d8-169">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="c31d8-170">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="c31d8-170">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="c31d8-171">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="c31d8-171">BAI2StatementExample</span></span>                 |







---
title: Banka ekstresi dosya alma sorunlarını giderme
description: Bankadan gelen banka ekstresi dosyasının, Microsoft Dynamics 365 Finance tarafından desteklenen düzenle eşleşmesi önemlidir. Banka ekstreleri için sıkı standartlar bulunduğundan çoğu tümleştirme doğru şekilde çalışacaktır. Ancak, bazen ekstre dosyası alınamayabilir veya hatalı sonuçlara sahip olabilir. Genellikle, bu sorunlar banka ekstresi dosyasındaki küçük farklılıklar nedeniyle ortaya çıkar. Bu makale, bu farklılıkları gidermeyi ve sorunların nasıl çözüleceğini açıklar.
author: panolte
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac82a269e8f7773c58517ef017576c82c52039cb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253975"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="ed7a6-107">Banka ekstresi dosya alma sorunlarını giderme</span><span class="sxs-lookup"><span data-stu-id="ed7a6-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed7a6-108">Bankadan gelen banka ekstresi dosyasının, Microsoft Dynamics 365 Finance tarafından desteklenen düzenle eşleşmesi önemlidir.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="ed7a6-109">Banka ekstreleri için sıkı standartlar bulunduğundan çoğu tümleştirme doğru şekilde çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="ed7a6-110">Ancak, bazen ekstre dosyası alınamayabilir veya hatalı sonuçlara sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="ed7a6-111">Genellikle, bu sorunlar banka ekstresi dosyasındaki küçük farklılıklar nedeniyle ortaya çıkar.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="ed7a6-112">Bu makale, bu farklılıkları gidermeyi ve sorunların nasıl çözüleceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="ed7a6-113">Hata nedir?</span><span class="sxs-lookup"><span data-stu-id="ed7a6-113">What is the error?</span></span>
------------------

<span data-ttu-id="ed7a6-114">Bir banka ekstresi doyasını içe aktarmaya çalıştıktan sonra, hatayı bulmak için Veri yönetimi iş geçmişine ve yürütme ayrıntılarına gidin.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="ed7a6-115">Hata, ekstre, bilanço ya da ekstre satırına yönlendirerek yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="ed7a6-116">Ancak soruna neden olan alan veya öğeyi tanımlamanıza yardımcı olmaya yeterli olacak bilgi vermesi olası değildir.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="ed7a6-117">Farklar nelerdir?</span><span class="sxs-lookup"><span data-stu-id="ed7a6-117">What are the differences?</span></span>
<span data-ttu-id="ed7a6-118">Banka dosya düzeni tanımını, Finance içe aktarma tanımıyla kıyaslayın ve alanlar ve öğelerdeki farklılıkları not edin.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-118">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="ed7a6-119">Banka ekstreleri dosyasını ilgili örnek Finance dosyasıyla karşılaştırın.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-119">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="ed7a6-120">ISO20022 dosyalarında farkları görmek kolaydır.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="ed7a6-121">İçe aktarılan banka ekstrelerindeki saat dilimi farklılıkları</span><span class="sxs-lookup"><span data-stu-id="ed7a6-121">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="ed7a6-122">İçe aktarma dosyasındaki tarih-saat değerleri, Finance and Operations'da gösterilen tarih-saat değerlerinden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-122">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="ed7a6-123">Bu tutarsızlığı önlemek için **Veri kaynaklarını yapılandır** sayfasına bir saat dilimi tercihi girin.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-123">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="ed7a6-124">Bir saat dilimi tercihi hakkında daha fazla bilgi için bkz. [Gelişmiş banka mutabakatı içe aktarma işlemi](set-up-advanced-bank-reconciliation-import-process.md).</span><span class="sxs-lookup"><span data-stu-id="ed7a6-124">See [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md) for more information about entering a time zone preference.</span></span>

## <a name="transformations"></a><span data-ttu-id="ed7a6-125">Dönüşümler</span><span class="sxs-lookup"><span data-stu-id="ed7a6-125">Transformations</span></span>
<span data-ttu-id="ed7a6-126">Genellikle, bu değişiklikler üç dönüşümden birinde yapılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-126">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="ed7a6-127">Her bir dönüşüm belirli bir standart için yazılır.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-127">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="ed7a6-128">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="ed7a6-128">Resource name</span></span>                                         | <span data-ttu-id="ed7a6-129">Dosya adı</span><span class="sxs-lookup"><span data-stu-id="ed7a6-129">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="ed7a6-130">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="ed7a6-130">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="ed7a6-131">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="ed7a6-131">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="ed7a6-132">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="ed7a6-132">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="ed7a6-133">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="ed7a6-133">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="ed7a6-134">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="ed7a6-134">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="ed7a6-135">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="ed7a6-135">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="ed7a6-136">Hata ayıklama dönüştürmeleri</span><span class="sxs-lookup"><span data-stu-id="ed7a6-136">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="ed7a6-137">BAI2 ve MT940 dosyalarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="ed7a6-137">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="ed7a6-138">BAI2 ve MT940 dosyaları metin tabanlı dosyalardır ve Genişletilebilir Stil Sayfası Dil Dönüşümleri (XSLT) hata ayıklamayı etkinleştirmek için bir düzeltme gerektirir.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-138">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="ed7a6-139">Program bu ayarlamayı bir dosya içe aktarıldığında yapar.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-139">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="ed7a6-140">Bir XML dosyası oluşturun ve aşağıdaki metni içine kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-140">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="ed7a6-141">Banka ekstresi dosyasının içeriğini kopyalayın ve bunları XML dosyasına yapıştırarak **PASTESTATEMENTFILEHERE**'ın yerine geçmesini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-141">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="ed7a6-142">XSLT hata ayıklama</span><span class="sxs-lookup"><span data-stu-id="ed7a6-142">Debug the XSLT</span></span>

<span data-ttu-id="ed7a6-143">Daha fazla bilgi için <https://msdn.microsoft.com/library/ms255605.aspx> konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-143">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="ed7a6-144">Microsoft Visual Studio'ya başlayın.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-144">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="ed7a6-145">Bir konsol uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-145">Create a console application.</span></span>
3.  <span data-ttu-id="ed7a6-146">Uygun XSLT'yi açın.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-146">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="ed7a6-147">XLST'yi ve özellikleri sayfasını tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-147">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="ed7a6-148">Girişi, banka ekstresi dosyasının konumuna ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-148">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="ed7a6-149">Çıktı için bir konum ve dosya adı tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-149">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="ed7a6-150">Gerekli kesme noktalarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-150">Set the required break points.</span></span>
8.  <span data-ttu-id="ed7a6-151">Menüde **XML** &gt; **XSLT Hata Ayıklamayı Başlat**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-151">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="ed7a6-152">XSLT çıktısını biçimlendirin</span><span class="sxs-lookup"><span data-stu-id="ed7a6-152">Format the XSLT output</span></span>

<span data-ttu-id="ed7a6-153">Dönüşüm yürütüldüğünde, Visual Studio'da görüntüleyebileceğiniz bir çıktı dosyası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-153">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="ed7a6-154">Çıktı dosyasını hızlı şekilde biçimlendirmek için Ctrl+A, Ctrl+K, and Ctrl+D kullanın.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-154">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="ed7a6-155">Dönüştürmeyi ayarlayın</span><span class="sxs-lookup"><span data-stu-id="ed7a6-155">Adjust the transformation</span></span>

<span data-ttu-id="ed7a6-156">Banka ekstresi dosyasında uygun bir alan veya öğeyi almak için dönüştürmeyi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-156">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="ed7a6-157">Sonra bu alanı veya öğeyi uygun Finance öğesine eşleyin.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-157">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="ed7a6-158">Borç/Alacak göstergesi</span><span class="sxs-lookup"><span data-stu-id="ed7a6-158">Debit/credit indicator</span></span>

<span data-ttu-id="ed7a6-159">Bazı durumlarda, borçlar alacak olarak ve alacaklar borç olarak içeri aktarılmış olabilir.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-159">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="ed7a6-160">Bu sorunu gidermek için uygun XSLT'yi değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-160">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="ed7a6-161">Banka Ekstrelerini birden çok bankadan geliyorsa, bunların tümünün aynı borç/alacak yaklaşımını kullandığından veya ayrı dönüşümleri oluşturduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-161">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="ed7a6-162">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator şablonu</span><span class="sxs-lookup"><span data-stu-id="ed7a6-162">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="ed7a6-163">ISO20022XML-to-Reconcilation.xslt GetCreditDebit şablonu</span><span class="sxs-lookup"><span data-stu-id="ed7a6-163">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="ed7a6-164">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator şablonu</span><span class="sxs-lookup"><span data-stu-id="ed7a6-164">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="ed7a6-165">Banka ekstresi biçimleri ve teknik düzenlerine örnekler</span><span class="sxs-lookup"><span data-stu-id="ed7a6-165">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="ed7a6-166">Aşağıdaki tablo gelişmiş banka mutabakatı içe alma dosyaları ve üç ilgili banka ekstresi örnek dosyalarının teknik düzen tanımlarını örnek olarak verir.</span><span class="sxs-lookup"><span data-stu-id="ed7a6-166">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="ed7a6-167">Örnek dosyaları ve teknik düzenleri buradan indirebilirsiniz: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="ed7a6-167">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="ed7a6-168">Teknik düzen tanımı</span><span class="sxs-lookup"><span data-stu-id="ed7a6-168">Technical layout definition</span></span>                             | <span data-ttu-id="ed7a6-169">Banka ekstresi örnek dosya</span><span class="sxs-lookup"><span data-stu-id="ed7a6-169">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="ed7a6-170">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="ed7a6-170">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="ed7a6-171">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="ed7a6-171">MT940StatementExample</span></span>                |
| <span data-ttu-id="ed7a6-172">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="ed7a6-172">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="ed7a6-173">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="ed7a6-173">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="ed7a6-174">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="ed7a6-174">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="ed7a6-175">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="ed7a6-175">BAI2StatementExample</span></span>                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
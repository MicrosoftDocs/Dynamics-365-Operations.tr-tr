---
title: Banka ekstresi dosya alma sorunlarını giderme
description: Bankadan gelen banka ekstresi dosyasının, Microsoft Dynamics 365 Finance tarafından desteklenen düzenle eşleşmesi önemlidir. Banka ekstreleri için sıkı standartlar bulunduğundan çoğu tümleştirme doğru şekilde çalışacaktır. Ancak, bazen ekstre dosyası alınamayabilir veya hatalı sonuçlara sahip olabilir. Genellikle, bu sorunlar banka ekstresi dosyasındaki küçük farklılıklar nedeniyle ortaya çıkar. Bu makale, bu farklılıkları gidermeyi ve sorunların nasıl çözüleceğini açıklar.
author: panolte
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: f0e01881a6b68526479d27014d49a718069cffc9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815896"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="0d4ac-107">Banka ekstresi dosya alma sorunlarını giderme</span><span class="sxs-lookup"><span data-stu-id="0d4ac-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d4ac-108">Bankadan gelen banka ekstresi dosyasının, Microsoft Dynamics 365 Finance tarafından desteklenen düzenle eşleşmesi önemlidir.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-108">It's important that the bank statement file from the bank matches the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="0d4ac-109">Banka ekstreleri için sıkı standartlar bulunduğundan çoğu tümleştirme doğru şekilde çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="0d4ac-110">Ancak, bazen ekstre dosyası alınamayabilir veya hatalı sonuçlara sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="0d4ac-111">Genellikle, bu sorunlar banka ekstresi dosyasındaki küçük farklılıklar nedeniyle ortaya çıkar.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="0d4ac-112">Bu makale, bu farklılıkları gidermeyi ve sorunların nasıl çözüleceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="0d4ac-113">Hata nedir?</span><span class="sxs-lookup"><span data-stu-id="0d4ac-113">What is the error?</span></span>
------------------

<span data-ttu-id="0d4ac-114">Bir banka ekstresi doyasını içe aktarmaya çalıştıktan sonra, hatayı bulmak için Veri yönetimi iş geçmişine ve yürütme ayrıntılarına gidin.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="0d4ac-115">Hata, ekstre, bilanço ya da ekstre satırına yönlendirerek yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="0d4ac-116">Ancak soruna neden olan alan veya öğeyi tanımlamanıza yardımcı olmaya yeterli olacak bilgi vermesi olası değildir.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

> [!NOTE]
> <span data-ttu-id="0d4ac-117">İçe aktarılan Banka ekstreleri yalnızca bir seferde tek bir nokta ile örtüşebilir.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-117">Imported bank statements can overlap only for single a point in time.</span></span>  <span data-ttu-id="0d4ac-118">Örneğin, bir ekstrenin bitiş tarihi 1 Ocak 2021 12:00 ÖÖ ise sonraki ekstrenin başlangıç tarihi 1 Ocak 2021 12:00 ÖÖ olabilir.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-118">For example, if a statement ends at 12:00 AM on January 1, 2021, then beginning date for the next statement can be 12:00 AM on Jarnuary 1, 2021 12:00:00 AM.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="0d4ac-119">Farklar nelerdir?</span><span class="sxs-lookup"><span data-stu-id="0d4ac-119">What are the differences?</span></span>
<span data-ttu-id="0d4ac-120">Banka dosya düzeni tanımını, Finance içe aktarma tanımıyla kıyaslayın ve alanlar ve öğelerdeki farklılıkları not edin.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-120">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="0d4ac-121">Banka ekstreleri dosyasını ilgili örnek Finance dosyasıyla karşılaştırın.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-121">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="0d4ac-122">ISO20022 dosyalarında farkları görmek kolaydır.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-122">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="0d4ac-123">İçe aktarılan banka ekstrelerindeki saat dilimi farklılıkları</span><span class="sxs-lookup"><span data-stu-id="0d4ac-123">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="0d4ac-124">İçe aktarma dosyasındaki tarih-saat değerleri, Finance and Operations'da gösterilen tarih-saat değerlerinden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-124">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="0d4ac-125">Bu tutarsızlığı önlemek için **Veri kaynaklarını yapılandır** sayfasına bir saat dilimi tercihi girin.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-125">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="0d4ac-126">Bir saat dilimi tercihi girme hakkında daha fazla bilgi için bkz. [Gelişmiş banka mutabakatı içe aktarma işlemi](set-up-advanced-bank-reconciliation-import-process.md).</span><span class="sxs-lookup"><span data-stu-id="0d4ac-126">For more information about entering a time zone preference, see [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md).</span></span>

## <a name="transformations"></a><span data-ttu-id="0d4ac-127">Dönüşümler</span><span class="sxs-lookup"><span data-stu-id="0d4ac-127">Transformations</span></span>
<span data-ttu-id="0d4ac-128">Genellikle, bu değişiklikler üç dönüşümden birinde yapılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-128">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="0d4ac-129">Her bir dönüşüm belirli bir standart için yazılır.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-129">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="0d4ac-130">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="0d4ac-130">Resource name</span></span>                                         | <span data-ttu-id="0d4ac-131">Dosya adı</span><span class="sxs-lookup"><span data-stu-id="0d4ac-131">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="0d4ac-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="0d4ac-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="0d4ac-133">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="0d4ac-133">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="0d4ac-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="0d4ac-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="0d4ac-135">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="0d4ac-135">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="0d4ac-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="0d4ac-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="0d4ac-137">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="0d4ac-137">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="0d4ac-138">Hata ayıklama dönüştürmeleri</span><span class="sxs-lookup"><span data-stu-id="0d4ac-138">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="0d4ac-139">BAI2 ve MT940 dosyalarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="0d4ac-139">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="0d4ac-140">BAI2 ve MT940 dosyaları metin tabanlı dosyalardır ve Genişletilebilir Stil Sayfası Dil Dönüşümleri (XSLT) hata ayıklamayı etkinleştirmek için bir düzeltme gerektirir.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-140">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="0d4ac-141">Program bu ayarlamayı bir dosya içe aktarıldığında yapar.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-141">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="0d4ac-142">Bir XML dosyası oluşturun ve aşağıdaki metni içine kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-142">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="0d4ac-143">Banka ekstresi dosyasının içeriğini kopyalayın ve bunları XML dosyasına yapıştırarak **PASTESTATEMENTFILEHERE**'ın yerine geçmesini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-143">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="0d4ac-144">XSLT hata ayıklama</span><span class="sxs-lookup"><span data-stu-id="0d4ac-144">Debug the XSLT</span></span>

<span data-ttu-id="0d4ac-145">Daha fazla bilgi için <https://msdn.microsoft.com/library/ms255605.aspx> konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-145">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="0d4ac-146">Microsoft Visual Studio'ya başlayın.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-146">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="0d4ac-147">Bir konsol uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-147">Create a console application.</span></span>
3.  <span data-ttu-id="0d4ac-148">Uygun XSLT'yi açın.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-148">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="0d4ac-149">XLST'yi ve özellikleri sayfasını tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-149">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="0d4ac-150">Girişi, banka ekstresi dosyasının konumuna ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-150">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="0d4ac-151">Çıktı için bir konum ve dosya adı tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-151">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="0d4ac-152">Gerekli kesme noktalarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-152">Set the required break points.</span></span>
8.  <span data-ttu-id="0d4ac-153">Menüde **XML** &gt; **XSLT Hata Ayıklamayı Başlat**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-153">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="0d4ac-154">XSLT çıktısını biçimlendirin</span><span class="sxs-lookup"><span data-stu-id="0d4ac-154">Format the XSLT output</span></span>

<span data-ttu-id="0d4ac-155">Dönüşüm yürütüldüğünde, Visual Studio'da görüntüleyebileceğiniz bir çıktı dosyası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-155">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="0d4ac-156">Çıktı dosyasını hızlı şekilde biçimlendirmek için Ctrl+A, Ctrl+K, and Ctrl+D kullanın.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-156">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="0d4ac-157">Dönüştürmeyi ayarlayın</span><span class="sxs-lookup"><span data-stu-id="0d4ac-157">Adjust the transformation</span></span>

<span data-ttu-id="0d4ac-158">Banka ekstresi dosyasında uygun bir alan veya öğeyi almak için dönüştürmeyi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-158">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="0d4ac-159">Sonra bu alanı veya öğeyi uygun Finance öğesine eşleyin.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-159">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="0d4ac-160">Borç/Alacak göstergesi</span><span class="sxs-lookup"><span data-stu-id="0d4ac-160">Debit/credit indicator</span></span>

<span data-ttu-id="0d4ac-161">Bazı durumlarda, borçlar alacak olarak ve alacaklar borç olarak içeri aktarılmış olabilir.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-161">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="0d4ac-162">Bu sorunu gidermek için uygun XSLT'yi değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-162">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="0d4ac-163">Banka Ekstrelerini birden çok bankadan geliyorsa, bunların tümünün aynı borç/alacak yaklaşımını kullandığından veya ayrı dönüşümleri oluşturduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-163">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="0d4ac-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator şablonu</span><span class="sxs-lookup"><span data-stu-id="0d4ac-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="0d4ac-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit şablonu</span><span class="sxs-lookup"><span data-stu-id="0d4ac-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="0d4ac-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator şablonu</span><span class="sxs-lookup"><span data-stu-id="0d4ac-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="0d4ac-167">Banka ekstresi biçimleri ve teknik düzenlerine örnekler</span><span class="sxs-lookup"><span data-stu-id="0d4ac-167">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="0d4ac-168">Aşağıdaki tablo gelişmiş banka mutabakatı içe alma dosyaları ve üç ilgili banka ekstresi örnek dosyalarının teknik düzen tanımlarını örnek olarak verir.</span><span class="sxs-lookup"><span data-stu-id="0d4ac-168">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="0d4ac-169">Örnek dosyaları ve teknik düzenleri buradan indirebilirsiniz: [İçe aktarma dosyası örnekleri](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span><span class="sxs-lookup"><span data-stu-id="0d4ac-169">You can download the example files and technical layouts here: [Import file examples](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span></span>  

| <span data-ttu-id="0d4ac-170">Teknik düzen tanımı</span><span class="sxs-lookup"><span data-stu-id="0d4ac-170">Technical layout definition</span></span>                             | <span data-ttu-id="0d4ac-171">Banka ekstresi örnek dosya</span><span class="sxs-lookup"><span data-stu-id="0d4ac-171">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="0d4ac-172">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="0d4ac-172">DynamicsAXMT940Layout</span></span>                                   | [<span data-ttu-id="0d4ac-173">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="0d4ac-173">MT940StatementExample</span></span>](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| <span data-ttu-id="0d4ac-174">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="0d4ac-174">DynamicsAXISO20022Layout</span></span>                                | [<span data-ttu-id="0d4ac-175">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="0d4ac-175">ISO20022StatementExample</span></span>](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| <span data-ttu-id="0d4ac-176">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="0d4ac-176">DynamicsAXBAI2Layout</span></span>                                    | [<span data-ttu-id="0d4ac-177">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="0d4ac-177">BAI2StatementExample</span></span>](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

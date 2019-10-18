---
title: Pozitif ödeme dosyaları ayarlama ve oluşturma
description: Bu konu pozitif ödemenin nasıl kurulacağı ve pozitif ödeme dosyalarının nasıl oluşturulacağı açıklanmıştır.
author: abruer
manager: AnnBe
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 600e3279536857dbb804ef420572fad42fe72311
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189534"
---
# <a name="set-up-and-generate-positive-pay-files"></a><span data-ttu-id="eded7-103">Pozitif ödeme dosyaları ayarlama ve oluşturma</span><span class="sxs-lookup"><span data-stu-id="eded7-103">Set up and generate positive pay files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eded7-104">Bu konu pozitif ödemenin nasıl kurulacağı ve pozitif ödeme dosyalarının nasıl oluşturulacağı açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="eded7-104">This topic explains how to set up positive pay and generate positive pay files.</span></span> 

<span data-ttu-id="eded7-105">Bankaya sunulan çeklerin bir elektronik listesini oluşturmak için pozitif ödeme kurun.</span><span class="sxs-lookup"><span data-stu-id="eded7-105">Set up positive pay to generate an electronic list of checks that is provided to the bank.</span></span> <span data-ttu-id="eded7-106">Ardından, bankaya bir çek sunulduğunda, banka bunu çek listesiyle karşılaştırır.</span><span class="sxs-lookup"><span data-stu-id="eded7-106">Then, when a check is presented to the bank, the bank compares it with the list of checks.</span></span> <span data-ttu-id="eded7-107">Çek, çek listesindeki bir çekle uyuşuyorsa banka çeki serbest bırakır.</span><span class="sxs-lookup"><span data-stu-id="eded7-107">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="eded7-108">Çek, listedeki bir çekle uyuşmuyorsa banka, çeki gözden geçirmek için tutar.</span><span class="sxs-lookup"><span data-stu-id="eded7-108">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

## <a name="security-for-positive-pay-files"></a><span data-ttu-id="eded7-109">Pozitif ödeme dosyaları için güvenlik</span><span class="sxs-lookup"><span data-stu-id="eded7-109">Security for positive pay files</span></span>
<span data-ttu-id="eded7-110">Pozitif ödeme dosyaları, alacaklar ve çek tutarları hakkında hassas bilgiler içermektedir.</span><span class="sxs-lookup"><span data-stu-id="eded7-110">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="eded7-111">Bu nedenle, banka tarafından alınana kadar dosyaların oluşturulduğu süreden itibaren uygun güvenlik önlemlerini uyguladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="eded7-111">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="eded7-112">Pozitif ödeme dosyaları, web tarayıcınız tarafından belirtilen konuma indirilir.</span><span class="sxs-lookup"><span data-stu-id="eded7-112">Positive pay files are downloaded to the location that is specified by your web browser.</span></span> <span data-ttu-id="eded7-113">Pozitif ödeme dosyaları hassas bilgiler içerebileceğinden, Microsoft Dynamics 365 Finance'te bu bilgilerin oluşturulması ve görüntülenmesinin yalnızca yetkili kullanıcılarla sınırlandırılması önemlidir.</span><span class="sxs-lookup"><span data-stu-id="eded7-113">Because positive pay files can contain sensitive information, it's important that only authorized users have access to generate and view this information in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="eded7-114">Gerekli olan ayrıcalıkları belirlerken aşağıdaki tabloyu kullanın.</span><span class="sxs-lookup"><span data-stu-id="eded7-114">Use the following table to help you determine the privileges that are required.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eded7-115">Görev</span><span class="sxs-lookup"><span data-stu-id="eded7-115">Task</span></span></th>
<th><span data-ttu-id="eded7-116">Ayrıcalık</span><span class="sxs-lookup"><span data-stu-id="eded7-116">Privilege</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eded7-117"><strong>Banka hesapları</strong> liste sayfasından veya <strong>Banka hesapları</strong> sayfasından pozitif ödeme dosyaları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="eded7-117">Generate positive pay files from the <strong>Bank accounts</strong> list page or the <strong>Bank accounts</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="eded7-118"><strong>Pozitif banka ödeme bilgilerini koru</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="eded7-118"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="eded7-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="eded7-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eded7-120">Birden çok tüzel kişilik ve banka hesabı için pozitif ödeme dosyalarını <strong>Bir pozitif ödeme dosyası oluştur</strong> sayfasından oluşturun.</span><span class="sxs-lookup"><span data-stu-id="eded7-120">Generate positive pay files for multiple legal entities and bank accounts from the <strong>Generate a positive pay file</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="eded7-121"><strong>Pozitif banka ödeme bilgilerini koru</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="eded7-121"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="eded7-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="eded7-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eded7-123">Pozitif ödeme dosyalarını <strong>Pozitif ödeme dosyası özeti</strong> sayfasında görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="eded7-123">View positive pay files on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="eded7-124"><strong>Birden çok tüzel kişilik için banka pozitif ödeme bilgilerini görüntüle</strong> (BankPositivePayView)</span><span class="sxs-lookup"><span data-stu-id="eded7-124"><strong>View bank positive pay information for multiple legal entities</strong> (BankPositivePayView)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eded7-125">Bir banka pozitif ödeme dosyasını <strong>Pozitif ödeme dosyası özeti</strong> sayfasında onaylayın.</span><span class="sxs-lookup"><span data-stu-id="eded7-125">Confirm a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="eded7-126"><strong>Pozitif ödeme dosyasını onayla</strong> (BankPositivePayConfirm)</span><span class="sxs-lookup"><span data-stu-id="eded7-126"><strong>Confirm positive payment file</strong> (BankPositivePayConfirm)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eded7-127">Bir banka pozitif ödeme dosyasını <strong>Pozitif ödeme dosyası özeti</strong> sayfasında geri çağırın.</span><span class="sxs-lookup"><span data-stu-id="eded7-127">Recall a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="eded7-128"><strong>Pozitif ödeme dosyasını geri çağır</strong> (BankPositivePayRecall)</span><span class="sxs-lookup"><span data-stu-id="eded7-128"><strong>Recall positive pay file</strong> (BankPositivePayRecall)</span></span></td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a><span data-ttu-id="eded7-129">Bir pozitif ödeme biçimi kurma</span><span class="sxs-lookup"><span data-stu-id="eded7-129">Set up a positive pay format</span></span>
<span data-ttu-id="eded7-130">Pozitif ödeme dosyaları veri varlıkları kullanılarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="eded7-130">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="eded7-131">Bir pozitif ödeme dosyası oluşturmadan önce, çek bilgilerinin banka ile iletişim kurabilecek bir biçime çevrilmesi için kullanılacak bir dönüştürme girişi biçimi oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="eded7-131">Before you can generate a positive pay file, you must set up a transformation input format that will be used to translate the check information into a format that can communicate with the bank.</span></span> <span data-ttu-id="eded7-132">**Pozitif ödeme biçimi** sayfasında, bir dosya biçimi tanımlayıcısı ve bir açıklama oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eded7-132">On the **Positive pay format** page, you can create a file format identifier and a description.</span></span> <span data-ttu-id="eded7-133">Dönüştürme girişi biçimi mutlaka XML tipinde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="eded7-133">The transformation input format must be of the XML type.</span></span> <span data-ttu-id="eded7-134">İlgili biçim, kullanmakta olduğunuz dönüşüm dosyasına bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="eded7-134">The specific format depends on the transformation file that you're using.</span></span> <span data-ttu-id="eded7-135">Örneğin, verilen örnek Genişletilebilir Stil Sayfası Dil Dönüşümleri (XSLT) dosyası **XML Öğesi** biçimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="eded7-135">For example, the sample Extensible Stylesheet Language Transformations (XSLT) file that is provided uses the **XML-Element** format.</span></span> <span data-ttu-id="eded7-136">Bankanızın talep ettiği biçim için dönüşüm dosyasının konumunu belirlemek için **Dönüşüm için kullanılan dosyayı yükle** eylemini kullanın.</span><span class="sxs-lookup"><span data-stu-id="eded7-136">Use the **Upload file used for transformation** action to specify the location of the transform file for the format that your bank requires.</span></span>

## <a name="example-xslt-file-for-positive-pay-file"></a><span data-ttu-id="eded7-137">Örnek: Pozitif ödeme dosyası için XSLT dosyası</span><span class="sxs-lookup"><span data-stu-id="eded7-137">Example: XSLT file for positive pay file</span></span>
    <xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:msxsl="urn:schemas-microsoft-com:xslt" exclude-result-prefixes="msxsl xslthelper" xmlns="urn:iso:std:iso:20022:tech:xsd:pain.001.001.02" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xslthelper="http://schemas.microsoft.com/BizTalk/2003/xslthelper">
      <xsl:output method="xml" omit-xml-declaration="no" version="1.0" encoding="utf-8"/>
      <xsl:template match="/">
        <xsl:value-of select="'
    '" />
        <Document>
          <xsl:value-of select="'
    '" />
          <!--Header Begin-->
          <xsl:value-of select='string("Vendor ID,Vendor Name,Voided,Document Type,Check Date,Check Number,Check Amount,Checkbook ID,Vendor Class ID,Posted Date")'/>
          <xsl:value-of select="'
    '" />
          <!--Header End-->
          <xsl:for-each select="Document/BANKPOSITIVEPAYEXPORTENTITY">
            <!--Cheque Detail begin-->
            <xsl:value-of select='RECIPIENTACCOUNTNUM/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='BANKNEGINSTRECIPIENTNAME/text()'/>
            <xsl:value-of select="','" />
            <xsl:choose>
              <xsl:when test='CHEQUESTATUS/text()=normalize-space("Void") or CHEQUESTATUS/text()=normalize-space("Rejected") or CHEQUESTATUS/text()=normalize-space("Cancelled")'>
                <xsl:value-of select='string("Yes")'/>
              </xsl:when>
              <xsl:when test='CHEQUESTATUS/text()=normalize-space("Payment")'>
                <xsl:value-of select='string("No")'/>
              </xsl:when>
              <xsl:otherwise>
                <xsl:value-of select='string(" ")'/>
              </xsl:otherwise>
            </xsl:choose>
            <xsl:value-of select="','" />
            <xsl:value-of select='string("Payment")'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='TRANSDATE/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='CHEQUENUM/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='AMOUNTCUR/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='string("BOA-#1812")'/>
            <xsl:value-of select="','" />
            <xsl:choose>
              <xsl:when test='RECIPIENTTYPE/text()=normalize-space("Vend")'>
                <xsl:value-of select='VENDGROUP/text()'/>
              </xsl:when>
              <xsl:otherwise>
                <xsl:value-of select='CUSTGROUP/text()'/>
              </xsl:otherwise>
            </xsl:choose>
            <xsl:value-of select="','" />
            <xsl:value-of select='TRANSDATE/text()'/>
            <xsl:value-of select="'
    '" />
          </xsl:for-each>
        </Document>
      </xsl:template>
    </xsl:stylesheet>

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a><span data-ttu-id="eded7-138">Pozitif ödeme biçimini bir banka hesabına atama</span><span class="sxs-lookup"><span data-stu-id="eded7-138">Assign the positive pay format to a bank account</span></span>
<span data-ttu-id="eded7-139">Pozitif ödeme bilgisi oluşturmak istediğiniz her bir banka hesabı için, önceki bölümde tanımladığınız pozitif ödeme biçimini atamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="eded7-139">For each bank account that you want to generate positive pay information for, you must assign the positive pay format that you specified in the previous section.</span></span> <span data-ttu-id="eded7-140">**Banka hesaplarını** sayfasında, banka hesabına karşılık gelen pozitif ödeme biçimini seçin.</span><span class="sxs-lookup"><span data-stu-id="eded7-140">On the **Bank accounts** page, select the positive pay format that corresponds to the bank account.</span></span> <span data-ttu-id="eded7-141">**Pozitif ödeme başlangıç tarihi** alanında, pozitif ödeme dosyaları oluşturmak için başlangıç tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="eded7-141">In the **Positive pay start date** field, enter the first date to generate positive pay files.</span></span> <span data-ttu-id="eded7-142">Bu alana bir tarih girmeniz önemlidir.</span><span class="sxs-lookup"><span data-stu-id="eded7-142">It's important that you enter a date in this field.</span></span> <span data-ttu-id="eded7-143">Aksi takdirde, oluşturacağınız ilk pozitif ödeme dosyası bu banka hesabı için o ana kadar oluşturulan tüm çekleri içerir.</span><span class="sxs-lookup"><span data-stu-id="eded7-143">Otherwise, the first positive pay file that you generate will include all checks that have ever been created for this bank account.</span></span>

## <a name="assign-a-number-sequence-for-positive-pay-files"></a><span data-ttu-id="eded7-144">Pozitif ödeme dosyaları için bir numara serisi atama</span><span class="sxs-lookup"><span data-stu-id="eded7-144">Assign a number sequence for positive pay files</span></span>
<span data-ttu-id="eded7-145">Her bir pozitif ödeme dosyası mutlaka kendine özel bir numaraya sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="eded7-145">Each positive pay file must have a unique number.</span></span> <span data-ttu-id="eded7-146">Pozitif ödeme dosyaları için bir numara serisi oluşturmak için **Nakit ve banka yönetimi parametreleri** sayfasındaki **Numara serileri** sekmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="eded7-146">Use the **Number sequences** tab on the **Cash and bank management parameters** page to create a number sequence for positive pay files.</span></span>

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a><span data-ttu-id="eded7-147">Bir tekli banka hesabı için bir pozitif ödeme dosyası oluşturma</span><span class="sxs-lookup"><span data-stu-id="eded7-147">Generate a positive pay file for a single bank account</span></span>
<span data-ttu-id="eded7-148">Tek bir tüzel kişilik ve tek bir banka hesabı için bir pozitif ödeme dosyası oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eded7-148">You can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="eded7-149">Pozitif ödeme dosyalarının aynı anda birden fazla tüzel kişilik ve banka hesabı için nasıl oluşturulacağı hakkında daha fazla bilgi için bir sonraki bölüme bakın.</span><span class="sxs-lookup"><span data-stu-id="eded7-149">For information about how to generate positive pay files for multiple legal entities and bank accounts at the same time, see the next section.</span></span> <span data-ttu-id="eded7-150">Tek bir tüzel kişilik ve tek bir banka hesabı için bir pozitif ödeme dosyası oluşturmak **Banka hesapları** sayfasından **Bir pozitif ödeme dosyası oluştur** iletişim kutusunu açın.</span><span class="sxs-lookup"><span data-stu-id="eded7-150">To generate a positive pay file for a single legal entity and a single bank account, open the **Generate a positive pay file** dialog box from the **Bank accounts** page.</span></span> <span data-ttu-id="eded7-151">**Sonlandırma tarihi** alanında, pozitif ödeme dosyasına eklenecek son çek tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="eded7-151">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="eded7-152">Bu kontrol tarihinin sonuna kadar bir pozitif ödeme dosyasına dahil edilmemiş tüm çekler dosyaya dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="eded7-152">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a><span data-ttu-id="eded7-153">Birden fazla banka hesabı için bir pozitif ödeme dosyası oluşturma</span><span class="sxs-lookup"><span data-stu-id="eded7-153">Generate a positive pay file for multiple bank accounts</span></span>
<span data-ttu-id="eded7-154">Birden fazla banka hesabı için bir pozitif ödeme dosyası oluşturmak için **Bir pozitif ödeme dosyası oluştur** periyodik görevini kullanın.</span><span class="sxs-lookup"><span data-stu-id="eded7-154">To generate a positive pay file for multiple bank accounts, use the **Generate a positive pay file** periodic task.</span></span> <span data-ttu-id="eded7-155">Dosya için pozitif ödeme biçimini seçin ve dosyanın tüm tüzel kişilikler için mi, yoksa seçilen bir tüzel kişilik için mi oluşturulacağını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="eded7-155">Select the positive pay format for the file, and specify whether to generate the file for all legal entities or for a selected legal entity.</span></span> <span data-ttu-id="eded7-156">Ayrıca, belirtilen pozitif ödeme biçimini kullanan tüm banka hesapları veya seçilen bir banka hesabı için pozitif ödeme dosyası oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eded7-156">You can also generate the positive pay file for all bank accounts that use the specified positive pay format or for a selected bank account.</span></span> <span data-ttu-id="eded7-157">**Sonlandırma tarihi** alanında, pozitif ödeme dosyasına eklenecek son çek tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="eded7-157">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="eded7-158">Bu kontrol tarihinin sonuna kadar bir pozitif ödeme dosyasına dahil edilmemiş tüm çekler dosyaya dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="eded7-158">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="view-the-results-of-positive-pay-file-generation"></a><span data-ttu-id="eded7-159">Pozitif ödeme dosyası oluşturma sonuçlarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="eded7-159">View the results of positive pay file generation</span></span>
<span data-ttu-id="eded7-160">Pozitif ödeme dosyası oluşturulduktan sonra sonuçları **Pozitif ödeme dosyası özeti** sayfasında görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eded7-160">After the positive pay file is generated, you can view the results on the **Positive pay file summary** page.</span></span> <span data-ttu-id="eded7-161">Her bir çekin ayrıntılarını görüntülemek için **Pozitif ödeme dosyası** ayrıntıları sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="eded7-161">To view the details of the individual checks, use the **Positive pay file** details page.</span></span>

## <a name="confirm-a-positive-pay-file"></a><span data-ttu-id="eded7-162">Bir pozitif ödeme dosyasını onaylama</span><span class="sxs-lookup"><span data-stu-id="eded7-162">Confirm a positive pay file</span></span>
<span data-ttu-id="eded7-163">Bir pozitif ödeme dosyasında listelenen çekler ödendikten sonra bankanızdan bir onay numarası alırsınız.</span><span class="sxs-lookup"><span data-stu-id="eded7-163">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="eded7-164">Pozitif ödeme dosyasını onaylayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eded7-164">You can then confirm the positive pay file.</span></span> <span data-ttu-id="eded7-165">**Pozitif ödeme dosyası özeti** sayfasında, durumu **Oluşturuldu** olan bir pozitif ödeme dosyası seçin ve ardından **Onay gir** eylemini seçin.</span><span class="sxs-lookup"><span data-stu-id="eded7-165">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Enter confirmation** action.</span></span> <span data-ttu-id="eded7-166">Bir pozitif ödeme dosyasını onayladığınızda, bankadan aldığınız onay numarası kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="eded7-166">When you confirm a positive pay file, the confirmation number that you received from the bank is recorded.</span></span>

## <a name="recall-a-positive-pay-file"></a><span data-ttu-id="eded7-167">Bir pozitif ödeme dosyasını geri çağırma</span><span class="sxs-lookup"><span data-stu-id="eded7-167">Recall a positive pay file</span></span>
<span data-ttu-id="eded7-168">Bir pozitif ödeme dosyasını değiştirmeniz gerekiyorsa, bunu geri çağırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eded7-168">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="eded7-169">**Pozitif ödeme dosyası özeti** sayfasında, durumu **Oluşturuldu** olan bir pozitif ödeme dosyası seçin ve ardından **Geri çağır** eylemini seçin.</span><span class="sxs-lookup"><span data-stu-id="eded7-169">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Recall** action.</span></span> <span data-ttu-id="eded7-170">Pozitif ödeme dosyasındaki her bir çek için, çekin bir pozitif ödeme dosyasına dahil edilip edilmeyeceğini gösteren alan sıfırlanır.</span><span class="sxs-lookup"><span data-stu-id="eded7-170">For each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span> <span data-ttu-id="eded7-171">Geri çağrılan çeki içeren, yeni bir pozitif ödeme dosyası oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eded7-171">You can then create a new positive pay file that includes the check that was recalled.</span></span>




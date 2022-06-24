---
title: Pozitif ödeme dosyaları kurma ve oluşturma
description: Bu makalede pozitif ödemenin nasıl kurulacağı ve pozitif ödeme dosyalarının nasıl oluşturulacağı açıklanmıştır.
author: panolte
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: kfend
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 6b3cff1029b02aaabef2ea9795ab9912f20f1129
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871434"
---
# <a name="set-up-and-generate-positive-pay-files"></a>Pozitif ödeme dosyaları kurma ve oluşturma

[!include [banner](../includes/banner.md)]

Bu makalede pozitif ödemenin nasıl kurulacağı ve pozitif ödeme dosyalarının nasıl oluşturulacağı açıklanmıştır. 

Bankaya sunulan çeklerin bir elektronik listesini oluşturmak için pozitif ödeme kurun. Ardından, bankaya bir çek sunulduğunda, banka bunu çek listesiyle karşılaştırır. Çek, çek listesindeki bir çekle uyuşuyorsa banka çeki serbest bırakır. Çek, listedeki bir çekle uyuşmuyorsa banka, çeki gözden geçirmek için tutar.

## <a name="security-for-positive-pay-files"></a>Pozitif ödeme dosyaları için güvenlik
Pozitif ödeme dosyaları, alacaklar ve çek tutarları hakkında hassas bilgiler içermektedir. Bu nedenle, banka tarafından alınana kadar dosyaların oluşturulduğu süreden itibaren uygun güvenlik önlemlerini uyguladığınızdan emin olun. Pozitif ödeme dosyaları, web tarayıcınız tarafından belirtilen konuma indirilir. Pozitif ödeme dosyaları hassas bilgiler içerebileceğinden, Microsoft Dynamics 365 Finance'te bu bilgilerin oluşturulması ve görüntülenmesinin yalnızca yetkili kullanıcılarla sınırlandırılması önemlidir. Gerekli olan ayrıcalıkları belirlerken aşağıdaki tabloyu kullanın.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Görev</th>
<th>Ayrıcalık</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Banka hesapları</strong> liste sayfasından veya <strong>Banka hesapları</strong> sayfasından pozitif ödeme dosyaları oluşturun.</td>
<td><ul>
<li><strong>Pozitif banka ödeme bilgilerini koru</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="even">
<td>Birden çok tüzel kişilik ve banka hesabı için pozitif ödeme dosyalarını <strong>Bir pozitif ödeme dosyası oluştur</strong> sayfasından oluşturun.</td>
<td><ul>
<li><strong>Pozitif banka ödeme bilgilerini koru</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Pozitif ödeme dosyalarını <strong>Pozitif ödeme dosyası özeti</strong> sayfasında görüntüleyin.</td>
<td><strong>Birden çok tüzel kişilik için banka pozitif ödeme bilgilerini görüntüle</strong> (BankPositivePayView)</td>
</tr>
<tr class="even">
<td>Bir banka pozitif ödeme dosyasını <strong>Pozitif ödeme dosyası özeti</strong> sayfasında onaylayın.</td>
<td><strong>Pozitif ödeme dosyasını onayla</strong> (BankPositivePayConfirm)</td>
</tr>
<tr class="odd">
<td>Bir banka pozitif ödeme dosyasını <strong>Pozitif ödeme dosyası özeti</strong> sayfasında geri çağırın.</td>
<td><strong>Pozitif ödeme dosyasını geri çağır</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a>Bir pozitif ödeme biçimi kurma
Pozitif ödeme dosyaları veri varlıkları kullanılarak oluşturulur. Bir pozitif ödeme dosyası oluşturmadan önce, çek bilgilerinin banka ile iletişim kurabilecek bir biçime çevrilmesi için kullanılacak bir dönüştürme girişi biçimi oluşturmanız gerekir. **Pozitif ödeme biçimi** sayfasında, bir dosya biçimi tanımlayıcısı ve bir açıklama oluşturabilirsiniz. Dönüştürme girişi biçimi mutlaka XML tipinde olmalıdır. İlgili biçim, kullanmakta olduğunuz dönüşüm dosyasına bağlıdır. Örneğin, verilen örnek Genişletilebilir Stil Sayfası Dil Dönüşümleri (XSLT) dosyası **XML Öğesi** biçimini kullanır. Bankanızın talep ettiği biçim için dönüşüm dosyasının konumunu belirlemek için **Dönüşüm için kullanılan dosyayı yükle** eylemini kullanın.

## <a name="example-xslt-file-for-positive-pay-file"></a>Örnek: Pozitif ödeme dosyası için XSLT dosyası

```xml
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
```

> [!NOTE]
> XSLT'deki XML adları, XML içindeki düğümlerin büyük-küçük harf durumuyla eşleşmelidir. XSLT ve XML dosyaları büyük/küçük harf duyarlıdır. 

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a>Pozitif ödeme biçimini bir banka hesabına atama
Pozitif ödeme bilgisi oluşturmak istediğiniz her bir banka hesabı için, önceki bölümde tanımladığınız pozitif ödeme biçimini atamanız gerekir. **Banka hesaplarını** sayfasında, banka hesabına karşılık gelen pozitif ödeme biçimini seçin. **Pozitif ödeme başlangıç tarihi** alanında, pozitif ödeme dosyaları oluşturmak için başlangıç tarihini girin. Bu alana bir tarih girmeniz önemlidir. Aksi takdirde, oluşturacağınız ilk pozitif ödeme dosyası bu banka hesabı için o ana kadar oluşturulan tüm çekleri içerir.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Pozitif ödeme dosyaları için bir numara serisi atama
Her bir pozitif ödeme dosyası mutlaka kendine özel bir numaraya sahip olmalıdır. Pozitif ödeme dosyaları için bir numara serisi oluşturmak için **Nakit ve banka yönetimi parametreleri** sayfasındaki **Numara serileri** sekmesini kullanın.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Bir tekli banka hesabı için bir pozitif ödeme dosyası oluşturma
Tek bir tüzel kişilik ve tek bir banka hesabı için bir pozitif ödeme dosyası oluşturabilirsiniz. Pozitif ödeme dosyalarının aynı anda birden fazla tüzel kişilik ve banka hesabı için nasıl oluşturulacağı hakkında daha fazla bilgi için bir sonraki bölüme bakın. Tek bir tüzel kişilik ve tek bir banka hesabı için bir pozitif ödeme dosyası oluşturmak **Banka hesapları** sayfasından **Bir pozitif ödeme dosyası oluştur** iletişim kutusunu açın. **Sonlandırma tarihi** alanında, pozitif ödeme dosyasına eklenecek son çek tarihini girin. Bu kontrol tarihinin sonuna kadar bir pozitif ödeme dosyasına dahil edilmemiş tüm çekler dosyaya dahil edilir.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Birden fazla banka hesabı için bir pozitif ödeme dosyası oluşturma
Birden fazla banka hesabı için bir pozitif ödeme dosyası oluşturmak için **Bir pozitif ödeme dosyası oluştur** periyodik görevini kullanın. Dosya için pozitif ödeme biçimini seçin ve dosyanın tüm tüzel kişilikler için mi, yoksa seçilen bir tüzel kişilik için mi oluşturulacağını belirleyin. Ayrıca, belirtilen pozitif ödeme biçimini kullanan tüm banka hesapları veya seçilen bir banka hesabı için pozitif ödeme dosyası oluşturabilirsiniz. **Sonlandırma tarihi** alanında, pozitif ödeme dosyasına eklenecek son çek tarihini girin. Bu kontrol tarihinin sonuna kadar bir pozitif ödeme dosyasına dahil edilmemiş tüm çekler dosyaya dahil edilir.

## <a name="view-the-results-of-positive-pay-file-generation"></a>Pozitif ödeme dosyası oluşturma sonuçlarını görüntüleme
Pozitif ödeme dosyası oluşturulduktan sonra sonuçları **Pozitif ödeme dosyası özeti** sayfasında görüntüleyebilirsiniz. Her bir çekin ayrıntılarını görüntülemek için **Pozitif ödeme dosyası** ayrıntıları sayfasını kullanın.

## <a name="confirm-a-positive-pay-file"></a>Bir pozitif ödeme dosyasını onaylama
Bir pozitif ödeme dosyasında listelenen çekler ödendikten sonra bankanızdan bir onay numarası alırsınız. Pozitif ödeme dosyasını onaylayabilirsiniz. **Pozitif ödeme dosyası özeti** sayfasında, durumu **Oluşturuldu** olan bir pozitif ödeme dosyası seçin ve ardından **Onay gir** eylemini seçin. Bir pozitif ödeme dosyasını onayladığınızda, bankadan aldığınız onay numarası kaydedilir.

## <a name="recall-a-positive-pay-file"></a>Bir pozitif ödeme dosyasını geri çağırma
Bir pozitif ödeme dosyasını değiştirmeniz gerekiyorsa, bunu geri çağırabilirsiniz. **Pozitif ödeme dosyası özeti** sayfasında, durumu **Oluşturuldu** olan bir pozitif ödeme dosyası seçin ve ardından **Geri çağır** eylemini seçin. Pozitif ödeme dosyasındaki her bir çek için, çekin bir pozitif ödeme dosyasına dahil edilip edilmeyeceğini gösteren alan sıfırlanır. Geri çağrılan çeki içeren, yeni bir pozitif ödeme dosyası oluşturabilirsiniz.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

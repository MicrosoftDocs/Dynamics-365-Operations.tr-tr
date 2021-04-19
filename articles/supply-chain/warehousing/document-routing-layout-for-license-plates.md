---
title: Plaka etiketleri için belge yönlendirme düzeni
description: Bu konu, etiketlere değer yazdırmak için biçimlendirme yöntemlerinin nasıl kullanılacağını açıklar.
author: perlynne
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: faf54fec2885f868c66987a7b481559d0c5615d0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838286"
---
# <a name="document-routing-layout-for-license-plate-labels"></a><span data-ttu-id="d4b95-103">Plaka etiketleri için belge yönlendirme düzeni</span><span class="sxs-lookup"><span data-stu-id="d4b95-103">Document routing layout for license plate labels</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d4b95-104">Belge yönlendirme düzeni, plaka etiketlerinin düzenini ve bunlar üzerine yazdırılan verileri tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d4b95-104">The document routing layout defines the layout of license plate labels, and the data that is printed on them.</span></span> <span data-ttu-id="d4b95-105">Mobil cihaz menü öğelerini ve iş şablonlarını ayarlarken, yazdırma tetikleme noktalarını yapılandırırsınız.</span><span class="sxs-lookup"><span data-stu-id="d4b95-105">You configure the printing trigger points when you set up mobile device menu items and work templates.</span></span>

<span data-ttu-id="d4b95-106">Tipik bir senaryoda, ambar teslim alma görevlileri, teslim alma alanına gelen paletlerin içeriklerini kaydettikten hemen sonra plaka etiketlerini yazdırır.</span><span class="sxs-lookup"><span data-stu-id="d4b95-106">In a typical scenario, warehouse receiving clerks print license plate labels immediately after they record the contents of pallets that arrive in the receiving area.</span></span> <span data-ttu-id="d4b95-107">Fiziksel etiketler paletlere uygulanır.</span><span class="sxs-lookup"><span data-stu-id="d4b95-107">The physical labels are applied to the pallets.</span></span> <span data-ttu-id="d4b95-108">Bunlar daha sonra, sonraki yerine koyma işlemi ve gelecekteki giden malzeme çekme işlemlerinin bir parçası olarak doğrulama için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d4b95-108">They can then be used for validation as part of the put-away process that follows and future outbound picking operations.</span></span>

<span data-ttu-id="d4b95-109">Yazdırma cihazının gönderilen metni yorumlayabilmesi koşuluyla, çok karmaşık Etiketler yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d4b95-109">You can print highly complex labels, provided that the printing device can interpret the text that is sent to it.</span></span> <span data-ttu-id="d4b95-110">Örneğin, barkod içeren bir Zebra Programlama Dili (ZPL) düzeni aşağıdaki örneğe benzeyebilir.</span><span class="sxs-lookup"><span data-stu-id="d4b95-110">For example, a Zebra Programming Language (ZPL) layout that includes a bar code might resemble the following example.</span></span>

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

<span data-ttu-id="d4b95-111">Etiket yazdırma işleminin bir parçası olarak bu örnekteki `$LicensePlateId$` metni bir veri değeriyle değiştirilecektir.</span><span class="sxs-lookup"><span data-stu-id="d4b95-111">As part of the label printing process, the text `$LicensePlateId$` in this example will be replaced with a data value.</span></span>

<span data-ttu-id="d4b95-112">Yazdırılacak değerleri görmek için **Ambar yönetimi \> Sorgular ve raporlar \>Plaka etiketleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="d4b95-112">To see the values that will be printed, go to **Warehouse management \> Inquiries and reports \> License plate labels**.</span></span>

<span data-ttu-id="d4b95-113">Birçok yaygın kullanılan etiket oluşturma aracı, etiket düzenine ilişkin metni biçimlendirmenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="d4b95-113">Several widely available label generation tools can help you format the text for the label layout.</span></span> <span data-ttu-id="d4b95-114">Bu araçların çoğu `$FieldName$` biçimini destekler.</span><span class="sxs-lookup"><span data-stu-id="d4b95-114">Many of these tools support the `$FieldName$` format.</span></span> <span data-ttu-id="d4b95-115">Ek olarak, Microsoft Dynamics 365 Supply Chain Management, belge yönlendirme düzenine için alan eşlemesinin bir parçası olarak özel biçimlendirme mantığı kullanır.</span><span class="sxs-lookup"><span data-stu-id="d4b95-115">In addition, Microsoft Dynamics 365 Supply Chain Management uses special formatting logic as part of the field mapping for the document routing layout.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="d4b95-116">Sisteminiz için bu özelliği etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="d4b95-116">Turn on this feature for your system</span></span>

<span data-ttu-id="d4b95-117">Sisteminiz bu konuda açıklanan özellikleri zaten içermiyorsa [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ne gidin ve *Gelişmiş plaka etiketi düzenleri* özelliğini açın.</span><span class="sxs-lookup"><span data-stu-id="d4b95-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Enhanced license plate label layouts* feature.</span></span>

## <a name="custom-number-formats"></a><span data-ttu-id="d4b95-118">Özel sayı biçimleri</span><span class="sxs-lookup"><span data-stu-id="d4b95-118">Custom number formats</span></span>

<span data-ttu-id="d4b95-119">Aşağıdaki biçime sahip kodlar kullanarak yazdırılan sayısal alan değerlerinin biçimlendirmesini özelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d4b95-119">You can customize the formatting of numerical field values that are printed by using codes that have the following format.</span></span>

```dos
$FieldName:FormatString$
```

<span data-ttu-id="d4b95-120">Bu biçim için bir açıklama aşağıda verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="d4b95-120">Here is an explanation of this format:</span></span>

- <span data-ttu-id="d4b95-121">`FieldName` veri alanının adıdır (örneğin, **Miktar**).</span><span class="sxs-lookup"><span data-stu-id="d4b95-121">`FieldName` is the name of the data field (such as **Qty**).</span></span>
- <span data-ttu-id="d4b95-122">`FormatString` verilerin nasıl yazdırılması gerektiğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d4b95-122">`FormatString` defines how the data must be printed.</span></span>

<span data-ttu-id="d4b95-123">Aşağıdaki örneklerde iş miktarı (**Miktar**) alanının nasıl özelleştirilebileceği gösterilmektedir:</span><span class="sxs-lookup"><span data-stu-id="d4b95-123">The following examples show how you can customize the work quantity (**Qty**) field:</span></span>

- <span data-ttu-id="d4b95-124">Her zaman dört basamağı göstermek için (sıfırları yer tutucular olarak kullanarak), `$Qty:0000$` kullanın.</span><span class="sxs-lookup"><span data-stu-id="d4b95-124">To always show four digits (by using zeros as placeholders), use `$Qty:0000$`.</span></span> <span data-ttu-id="d4b95-125">Örneğin, miktar 10 ise, etiket "0010" olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="d4b95-125">For example, if the quantity is 10, the label will show "0010."</span></span>
- <span data-ttu-id="d4b95-126">Her zaman iki ondalık basamak göstermek için `$Qty:0.00$` kullanın.</span><span class="sxs-lookup"><span data-stu-id="d4b95-126">To always show two decimal places, use `$Qty:0.00$`.</span></span> <span data-ttu-id="d4b95-127">Örneğin, miktar 10 ise, etiket "10,00" olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="d4b95-127">For example, if the quantity is 10, the label will show "10.00."</span></span>

<span data-ttu-id="d4b95-128">Kullanılabilir sayı biçimi dizelerinin tam listesi için bkz. [Özel sayı biçimlendirme dizeleri](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span><span class="sxs-lookup"><span data-stu-id="d4b95-128">For a complete list of the available number format strings, see [Custom numeric format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="custom-string-formats"></a><span data-ttu-id="d4b95-129">Özel dize biçimleri</span><span class="sxs-lookup"><span data-stu-id="d4b95-129">Custom string formats</span></span>

<span data-ttu-id="d4b95-130">Aşağıdaki alan ve biçim kodunu kullanarak bir dizenin ilk karakterlerini kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d4b95-130">You can remove the first characters of a string by using the following field and format code.</span></span>

```dos
$FieldName:#..$
```

<span data-ttu-id="d4b95-131">Burada, `#` atlanacak karakter sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4b95-131">Here, `#` specifies the number of characters to skip.</span></span> <span data-ttu-id="d4b95-132">Örneğin, ilk iki karakteri içermeyen bir Seri Sevkiyat Konteyner Kodu (SSCC) plaka numarası yazdırmak için `$LicensePlateId:2..$` kullanın.</span><span class="sxs-lookup"><span data-stu-id="d4b95-132">For example, to print a Serial Shipping Container Code (SSCC) license plate number that doesn't include the first two characters, use `$LicensePlateId:2..$`.</span></span> <span data-ttu-id="d4b95-133">Bu durumda, lisans plaka numarası 0011111111111222221 "11111111111222221" olarak yazdırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="d4b95-133">In this case, the license plate number 0011111111111222221 will be printed as "11111111111222221."</span></span>

## <a name="custom-datetime-formats"></a><span data-ttu-id="d4b95-134">Özel tarih/saat biçimleri</span><span class="sxs-lookup"><span data-stu-id="d4b95-134">Custom date/time formats</span></span>

<span data-ttu-id="d4b95-135">Aşağıdaki örnek, tarihleri yazdırmak için kullanılan biçimi nasıl denetleyebileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="d4b95-135">The following example shows how you can control the format that is used to print dates.</span></span>

```dos
$PrintedDate:dd-MM-yyyy$
```

<span data-ttu-id="d4b95-136">Bu örnekte, 30 Nisan 2020 tarihi "30-04-2020" olarak yazdırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="d4b95-136">In this example, the date April 30, 2020, will be printed as "30-04-2020."</span></span>

<span data-ttu-id="d4b95-137">Kullanılabilir tarih/saat biçimlerinin tam listesi için bkz. [Özel tarih ve saat biçimlendirme dizeleri](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="d4b95-137">For a complete list of the available date/time formats, see [Custom date and time format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="print-individual-lines-from-multiline-data"></a><span data-ttu-id="d4b95-138">Çok satırlı verilerden ayrı ayrı satırlar yazdırma</span><span class="sxs-lookup"><span data-stu-id="d4b95-138">Print individual lines from multiline data</span></span>

<span data-ttu-id="d4b95-139">Bir veri alanı birden çok satır içeriyorsa (yani, satır sonları ile ayrılmış satırlar), aşağıdaki biçimi kullanarak tek bir satırı yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d4b95-139">If a data field contains multiple lines (that is, lines that are separated by line breaks), you can print an individual line by using the following format.</span></span>

```dos
$FieldName[#]$
```

<span data-ttu-id="d4b95-140">Burada, `#` yazdırmak istediğiniz satır numarasıdır.</span><span class="sxs-lookup"><span data-stu-id="d4b95-140">Here, `#` is the line number that you want to print.</span></span> <span data-ttu-id="d4b95-141">(İlk satır için 1 kullanın.)</span><span class="sxs-lookup"><span data-stu-id="d4b95-141">(Use 1 for the first line.)</span></span>

<span data-ttu-id="d4b95-142">Örneğin, sisteminizde aşağıdaki çok satırlı adresi depolayan `AdditionalAddress` bir alan vardır:</span><span class="sxs-lookup"><span data-stu-id="d4b95-142">For example, your system has an `AdditionalAddress` field that stores the following multiline address:</span></span>

<span data-ttu-id="d4b95-143">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="d4b95-143">Contoso Inc.</span></span>  
<span data-ttu-id="d4b95-144">123 Cadde Adı</span><span class="sxs-lookup"><span data-stu-id="d4b95-144">123 Street Name</span></span>  
<span data-ttu-id="d4b95-145">Bir Şehir, Bir Eyalet</span><span class="sxs-lookup"><span data-stu-id="d4b95-145">Some City, Some State</span></span>

<span data-ttu-id="d4b95-146">Aşağıdaki kodları kullanarak, bir seferde bir satır olmak üzere bu adresi yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d4b95-146">You can print this address, one line at a time, by using the following codes.</span></span>

| <span data-ttu-id="d4b95-147">Kod</span><span class="sxs-lookup"><span data-stu-id="d4b95-147">Code</span></span> | <span data-ttu-id="d4b95-148">Yazdırılan metin</span><span class="sxs-lookup"><span data-stu-id="d4b95-148">Text that is printed</span></span> |
|---|---|
| `$AdditionalAddress[1]$` | <span data-ttu-id="d4b95-149">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="d4b95-149">Contoso Inc.</span></span> |
| `$AdditionalAddress[2]$` | <span data-ttu-id="d4b95-150">123 Cadde Adı</span><span class="sxs-lookup"><span data-stu-id="d4b95-150">123 Street Name</span></span> |
| `$AdditionalAddress[3]$` | <span data-ttu-id="d4b95-151">Bir Şehir, Bir Eyalet</span><span class="sxs-lookup"><span data-stu-id="d4b95-151">Some City, Some State</span></span> |

## <a name="print-and-format-from-a-display-method"></a><span data-ttu-id="d4b95-152">Bir görüntüleme yönteminden yazdırma ve biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="d4b95-152">Print and format from a display method</span></span>

<span data-ttu-id="d4b95-153">Aşağıdaki biçimi kullanarak bir görüntüleme yönteminden yazdırma yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d4b95-153">You can print from a display method by using the following format.</span></span>

```dos
$DisplayMethod()$
```

<span data-ttu-id="d4b95-154">Bu biçimi, bu konunun önceki kısımlarında açıklanan diğer türlerle birleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d4b95-154">You can combine this format with other types that were described earlier in this topic.</span></span> <span data-ttu-id="d4b95-155">Örneğin, `DisplayListOfItemsNumbers()` bir görüntüleme yönteminiz var ve bu yöntemin ilk öğe numarasını yazdırmak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="d4b95-155">For example, you have a display method that is named `DisplayListOfItemsNumbers()`, and you want to print the first item number of this method.</span></span> <span data-ttu-id="d4b95-156">Bu durumda, aşağıdaki kodu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d4b95-156">In this case, you can use the following code.</span></span>

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a><span data-ttu-id="d4b95-157">Etiketlerin nasıl yazdırılacağı hakkında daha fazla bilgi</span><span class="sxs-lookup"><span data-stu-id="d4b95-157">More information about how to print labels</span></span>

<span data-ttu-id="d4b95-158">Etiketlerin nasıl ayarlanacağı ve yazdırılacağı hakkında daha fazla bilgi için bkz. [Plaka etiketi yazdırmayı etkinleştirme](tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="d4b95-158">For more information about how to set up and print labels, see [Enable license plate label printing](tasks/license-plate-label-printing.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
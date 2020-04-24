---
title: Plaka etiketleri için belge yönlendirme düzeni
description: Bu konu, etiketlere değer yazdırmak için biçimlendirme yöntemlerinin nasıl kullanılacağını açıklar.
author: perlynne
manager: tfehr
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 62d4301f9dbe301c2a2573102d911a8d0ec58eb0
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261383"
---
# <a name="document-routing-layout-for-license-plate-labels"></a><span data-ttu-id="23153-103">Plaka etiketleri için belge yönlendirme düzeni</span><span class="sxs-lookup"><span data-stu-id="23153-103">Document routing layout for license plate labels</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23153-104">Belge yönlendirme düzeni, plaka etiketlerinin düzenini ve bunlar üzerine yazdırılan verileri tanımlar.</span><span class="sxs-lookup"><span data-stu-id="23153-104">The document routing layout defines the layout of license plate labels, and the data that is printed on them.</span></span> <span data-ttu-id="23153-105">Mobil cihaz menü öğelerini ve iş şablonlarını ayarlarken, yazdırma tetikleme noktalarını yapılandırırsınız.</span><span class="sxs-lookup"><span data-stu-id="23153-105">You configure the printing trigger points when you set up mobile device menu items and work templates.</span></span>

<span data-ttu-id="23153-106">Tipik bir senaryoda, ambar teslim alma görevlileri, teslim alma alanına gelen paletlerin içeriklerini kaydettikten hemen sonra plaka etiketlerini yazdırır.</span><span class="sxs-lookup"><span data-stu-id="23153-106">In a typical scenario, warehouse receiving clerks print license plate labels immediately after they record the contents of pallets that arrive in the receiving area.</span></span> <span data-ttu-id="23153-107">Fiziksel etiketler paletlere uygulanır.</span><span class="sxs-lookup"><span data-stu-id="23153-107">The physical labels are applied to the pallets.</span></span> <span data-ttu-id="23153-108">Bunlar daha sonra, sonraki yerine koyma işlemi ve gelecekteki giden malzeme çekme işlemlerinin bir parçası olarak doğrulama için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="23153-108">They can then be used for validation as part of the put-away process that follows and future outbound picking operations.</span></span>

<span data-ttu-id="23153-109">Yazdırma cihazının gönderilen metni yorumlayabilmesi koşuluyla, çok karmaşık Etiketler yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="23153-109">You can print highly complex labels, provided that the printing device can interpret the text that is sent to it.</span></span> <span data-ttu-id="23153-110">Örneğin, barkod içeren bir Zebra Programlama Dili (ZPL) düzeni aşağıdaki örneğe benzeyebilir.</span><span class="sxs-lookup"><span data-stu-id="23153-110">For example, a Zebra Programming Language (ZPL) layout that includes a bar code might resemble the following example.</span></span>

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

<span data-ttu-id="23153-111">Etiket yazdırma işleminin bir parçası olarak bu örnekteki `$LicensePlateId$` metni bir veri değeriyle değiştirilecektir.</span><span class="sxs-lookup"><span data-stu-id="23153-111">As part of the label printing process, the text `$LicensePlateId$` in this example will be replaced with a data value.</span></span>

<span data-ttu-id="23153-112">Yazdırılacak değerleri görmek için **Ambar yönetimi \> Sorgular ve raporlar \>Plaka etiketleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="23153-112">To see the values that will be printed, go to **Warehouse management \> Inquiries and reports \> License plate labels**.</span></span>

<span data-ttu-id="23153-113">Birçok yaygın kullanılan etiket oluşturma aracı, etiket düzenine ilişkin metni biçimlendirmenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="23153-113">Several widely available label generation tools can help you format the text for the label layout.</span></span> <span data-ttu-id="23153-114">Bu araçların çoğu `$FieldName$` biçimini destekler.</span><span class="sxs-lookup"><span data-stu-id="23153-114">Many of these tools support the `$FieldName$` format.</span></span> <span data-ttu-id="23153-115">Ek olarak, Microsoft Dynamics 365 Supply Chain Management, belge yönlendirme düzenine için alan eşlemesinin bir parçası olarak özel biçimlendirme mantığı kullanır.</span><span class="sxs-lookup"><span data-stu-id="23153-115">In addition, Microsoft Dynamics 365 Supply Chain Management uses special formatting logic as part of the field mapping for the document routing layout.</span></span>

## <a name="custom-number-formats"></a><span data-ttu-id="23153-116">Özel sayı biçimleri</span><span class="sxs-lookup"><span data-stu-id="23153-116">Custom number formats</span></span>

<span data-ttu-id="23153-117">Aşağıdaki biçime sahip kodlar kullanarak yazdırılan sayısal alan değerlerinin biçimlendirmesini özelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="23153-117">You can customize the formatting of numerical field values that are printed by using codes that have the following format.</span></span>

```dos
$FieldName:FormatString$
```

<span data-ttu-id="23153-118">Bu biçim için bir açıklama aşağıda verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="23153-118">Here is an explanation of this format:</span></span>

- <span data-ttu-id="23153-119">`FieldName` veri alanının adıdır (örneğin, **Miktar**).</span><span class="sxs-lookup"><span data-stu-id="23153-119">`FieldName` is the name of the data field (such as **Qty**).</span></span>
- <span data-ttu-id="23153-120">`FormatString` verilerin nasıl yazdırılması gerektiğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="23153-120">`FormatString` defines how the data must be printed.</span></span>

<span data-ttu-id="23153-121">Aşağıdaki örneklerde iş miktarı (**Miktar**) alanının nasıl özelleştirilebileceği gösterilmektedir:</span><span class="sxs-lookup"><span data-stu-id="23153-121">The following examples show how you can customize the work quantity (**Qty**) field:</span></span>

- <span data-ttu-id="23153-122">Her zaman dört basamağı göstermek için (sıfırları yer tutucular olarak kullanarak), `$Qty:0000$` kullanın.</span><span class="sxs-lookup"><span data-stu-id="23153-122">To always show four digits (by using zeros as placeholders), use `$Qty:0000$`.</span></span> <span data-ttu-id="23153-123">Örneğin, miktar 10 ise, etiket "0010" olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="23153-123">For example, if the quantity is 10, the label will show "0010."</span></span>
- <span data-ttu-id="23153-124">Her zaman iki ondalık basamak göstermek için `$Qty:0.00$` kullanın.</span><span class="sxs-lookup"><span data-stu-id="23153-124">To always show two decimal places, use `$Qty:0.00$`.</span></span> <span data-ttu-id="23153-125">Örneğin, miktar 10 ise, etiket "10,00" olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="23153-125">For example, if the quantity is 10, the label will show "10.00."</span></span>

<span data-ttu-id="23153-126">Kullanılabilir sayı biçimi dizelerinin tam listesi için bkz. [Özel sayı biçimlendirme dizeleri](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span><span class="sxs-lookup"><span data-stu-id="23153-126">For a complete list of the available number format strings, see [Custom numeric format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="custom-string-formats"></a><span data-ttu-id="23153-127">Özel dize biçimleri</span><span class="sxs-lookup"><span data-stu-id="23153-127">Custom string formats</span></span>

<span data-ttu-id="23153-128">Aşağıdaki alan ve biçim kodunu kullanarak bir dizenin ilk karakterlerini kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="23153-128">You can remove the first characters of a string by using the following field and format code.</span></span>

```dos
$FieldName:#..$
```

<span data-ttu-id="23153-129">Burada, `#` atlanacak karakter sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="23153-129">Here, `#` specifies the number of characters to skip.</span></span> <span data-ttu-id="23153-130">Örneğin, ilk iki karakteri içermeyen bir Seri Sevkiyat Konteyner Kodu (SSCC) plaka numarası yazdırmak için `$LicensePlateId:2..$` kullanın.</span><span class="sxs-lookup"><span data-stu-id="23153-130">For example, to print a Serial Shipping Container Code (SSCC) license plate number that doesn't include the first two characters, use `$LicensePlateId:2..$`.</span></span> <span data-ttu-id="23153-131">Bu durumda, lisans plaka numarası 0011111111111222221 "11111111111222221" olarak yazdırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="23153-131">In this case, the license plate number 0011111111111222221 will be printed as "11111111111222221."</span></span>

## <a name="custom-datetime-formats"></a><span data-ttu-id="23153-132">Özel tarih/saat biçimleri</span><span class="sxs-lookup"><span data-stu-id="23153-132">Custom date/time formats</span></span>

<span data-ttu-id="23153-133">Aşağıdaki örnek, tarihleri yazdırmak için kullanılan biçimi nasıl denetleyebileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="23153-133">The following example shows how you can control the format that is used to print dates.</span></span>

```dos
$PrintedDate:dd-MM-yyyy$
```

<span data-ttu-id="23153-134">Bu örnekte, 30 Nisan 2020 tarihi "30-04-2020" olarak yazdırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="23153-134">In this example, the date April 30, 2020, will be printed as "30-04-2020."</span></span>

<span data-ttu-id="23153-135">Kullanılabilir tarih/saat biçimlerinin tam listesi için bkz. [Özel tarih ve saat biçimlendirme dizeleri](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="23153-135">For a complete list of the available date/time formats, see [Custom date and time format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="print-individual-lines-from-multiline-data"></a><span data-ttu-id="23153-136">Çok satırlı verilerden ayrı ayrı satırlar yazdırma</span><span class="sxs-lookup"><span data-stu-id="23153-136">Print individual lines from multiline data</span></span>

<span data-ttu-id="23153-137">Bir veri alanı birden çok satır içeriyorsa (yani, satır sonları ile ayrılmış satırlar), aşağıdaki biçimi kullanarak tek bir satırı yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="23153-137">If a data field contains multiple lines (that is, lines that are separated by line breaks), you can print an individual line by using the following format.</span></span>

```dos
$FieldName[#]$
```

<span data-ttu-id="23153-138">Burada, `#` yazdırmak istediğiniz satır numarasıdır.</span><span class="sxs-lookup"><span data-stu-id="23153-138">Here, `#` is the line number that you want to print.</span></span> <span data-ttu-id="23153-139">(İlk satır için 1 kullanın.)</span><span class="sxs-lookup"><span data-stu-id="23153-139">(Use 1 for the first line.)</span></span>

<span data-ttu-id="23153-140">Örneğin, sisteminizde aşağıdaki çok satırlı adresi depolayan `AdditionalAddress` bir alan vardır:</span><span class="sxs-lookup"><span data-stu-id="23153-140">For example, your system has an `AdditionalAddress` field that stores the following multiline address:</span></span>

<span data-ttu-id="23153-141">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="23153-141">Contoso Inc.</span></span>  
<span data-ttu-id="23153-142">123 Cadde Adı</span><span class="sxs-lookup"><span data-stu-id="23153-142">123 Street Name</span></span>  
<span data-ttu-id="23153-143">Bir Şehir, Bir Eyalet</span><span class="sxs-lookup"><span data-stu-id="23153-143">Some City, Some State</span></span>

<span data-ttu-id="23153-144">Aşağıdaki kodları kullanarak, bir seferde bir satır olmak üzere bu adresi yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="23153-144">You can print this address, one line at a time, by using the following codes.</span></span>

| <span data-ttu-id="23153-145">Kod</span><span class="sxs-lookup"><span data-stu-id="23153-145">Code</span></span> | <span data-ttu-id="23153-146">Yazdırılan metin</span><span class="sxs-lookup"><span data-stu-id="23153-146">Text that is printed</span></span> |
|---|---|
| `$AdditionalAddress[1]$` | <span data-ttu-id="23153-147">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="23153-147">Contoso Inc.</span></span> |
| `$AdditionalAddress[2]$` | <span data-ttu-id="23153-148">123 Cadde Adı</span><span class="sxs-lookup"><span data-stu-id="23153-148">123 Street Name</span></span> |
| `$AdditionalAddress[3]$` | <span data-ttu-id="23153-149">Bir Şehir, Bir Eyalet</span><span class="sxs-lookup"><span data-stu-id="23153-149">Some City, Some State</span></span> |

## <a name="print-and-format-from-a-display-method"></a><span data-ttu-id="23153-150">Bir görüntüleme yönteminden yazdırma ve biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="23153-150">Print and format from a display method</span></span>

<span data-ttu-id="23153-151">Aşağıdaki biçimi kullanarak bir görüntüleme yönteminden yazdırma yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="23153-151">You can print from a display method by using the following format.</span></span>

```dos
$DisplayMethod()$
```

<span data-ttu-id="23153-152">Bu biçimi, bu konunun önceki kısımlarında açıklanan diğer türlerle birleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="23153-152">You can combine this format with other types that were described earlier in this topic.</span></span> <span data-ttu-id="23153-153">Örneğin, `DisplayListOfItemsNumbers()` bir görüntüleme yönteminiz var ve bu yöntemin ilk öğe numarasını yazdırmak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="23153-153">For example, you have a display method that is named `DisplayListOfItemsNumbers()`, and you want to print the first item number of this method.</span></span> <span data-ttu-id="23153-154">Bu durumda, aşağıdaki kodu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="23153-154">In this case, you can use the following code.</span></span>

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a><span data-ttu-id="23153-155">Etiketlerin nasıl yazdırılacağı hakkında daha fazla bilgi</span><span class="sxs-lookup"><span data-stu-id="23153-155">More information about how to print labels</span></span>

<span data-ttu-id="23153-156">Etiketlerin nasıl ayarlanacağı ve yazdırılacağı hakkında daha fazla bilgi için bkz. [Plaka etiketi yazdırmayı etkinleştirme](tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="23153-156">For more information about how to set up and print labels, see [Enable license plate label printing](tasks/license-plate-label-printing.md).</span></span>

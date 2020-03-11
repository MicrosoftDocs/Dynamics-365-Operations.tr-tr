---
title: FORMAT ER işlevi
description: Bu konu, FORMAT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ae688ef6b24f8d90c0354c8c6449adba1588bfa
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041090"
---
# <span data-ttu-id="ce632-103"><a name="FORMAT">FORMAT ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="ce632-103"><a name="FORMAT">FORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce632-104">`FORMAT` işlevi, belirtilen dizeyi, tüm **%N** oluşumlarını *N*'ci bağımsız değişken ile değiştirerek biçimlendirdikten sonra *Dize* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="ce632-104">The `FORMAT` function returns the specified string as a *String* value after it has been formatted by substituting any occurrences of **%N** with the *N*th argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce632-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="ce632-105">Syntax</span></span>

```vb
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a><span data-ttu-id="ce632-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="ce632-106">Arguments</span></span>

<span data-ttu-id="ce632-107">`string`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="ce632-107">`string`: *String*</span></span>

<span data-ttu-id="ce632-108">Biçimlendirilecek *Dize* veri türünün veri kaynağına yönelik referans.</span><span class="sxs-lookup"><span data-stu-id="ce632-108">A reference to a data source of the *String* type that must be formatted.</span></span> <span data-ttu-id="ce632-109">Bu bağımsız değişken gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ce632-109">This argument is required.</span></span>

<span data-ttu-id="ce632-110">`argument 1`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="ce632-110">`argument 1`: *String*</span></span>

<span data-ttu-id="ce632-111">**%1** oluşumlarını değiştirmek için kullanılan ilk bağımsız değişken.</span><span class="sxs-lookup"><span data-stu-id="ce632-111">The first argument, which is used to replace occurrences of **%1**.</span></span> <span data-ttu-id="ce632-112">Bu bağımsız değişken gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ce632-112">This argument is required.</span></span>

<span data-ttu-id="ce632-113">`argument N`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="ce632-113">`argument N`: *String*</span></span>

<span data-ttu-id="ce632-114">**%2**, **%3** vb. oluşumlarını değiştirmek için kullanılan *N*'ci bağımsız değişken.</span><span class="sxs-lookup"><span data-stu-id="ce632-114">The *N*th argument, which is used to replace occurrences of **%2**, **%3**, and so on.</span></span> <span data-ttu-id="ce632-115">Bu ek bağımsız değişkenler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ce632-115">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="ce632-116">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="ce632-116">Return values</span></span>

<span data-ttu-id="ce632-117">*Dize*</span><span class="sxs-lookup"><span data-stu-id="ce632-117">*String*</span></span>

<span data-ttu-id="ce632-118">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="ce632-118">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ce632-119">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="ce632-119">Usage notes</span></span>

<span data-ttu-id="ce632-120">Bir parametre için bir bağımsız değişken sağlanmamışsa, parametre izede **"%N"** olarak döndürülür.</span><span class="sxs-lookup"><span data-stu-id="ce632-120">If an argument isn't provided for a parameter, the parameter is returned as **"%N"** in the string.</span></span> <span data-ttu-id="ce632-121">*Gerçek* türün değerleri için, varsayılan dize dönüşümü iki ondalık basamakla sınırlıdır.</span><span class="sxs-lookup"><span data-stu-id="ce632-121">For values of the *Real* type, the default string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="ce632-122">Örnek</span><span class="sxs-lookup"><span data-stu-id="ce632-122">Example</span></span>

<span data-ttu-id="ce632-123">Aşağıdaki çizimde, **ÖdemeModeli** veri kaynağı **müşteri** bileşenini kullanarak müşteri kayıtları listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ce632-123">In the following illustration, the **PaymentModel** data source returns a list of customer records by using the **Customer** component.</span></span> <span data-ttu-id="ce632-124">Bu, **İşlemTarihi** alanını kullanarak işlem tarihi değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ce632-124">It returns the processing date value by using the **ProcessingDate** field.</span></span>

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

<span data-ttu-id="ce632-125">Seçilen müşteriler için elektronik dosya oluşturmak üzere tasarlanmış elektronik raporlama (ER) biçiminde veri kaynağı olarak **PaymentModel** seçilir ve işlem akışını denetler.</span><span class="sxs-lookup"><span data-stu-id="ce632-125">In the Electronic reporting (ER) format that is designed to generate an electronic file for selected customers, **PaymentModel** is selected as a data source, and it controls the process flow.</span></span> <span data-ttu-id="ce632-126">Seçilmiş bir müşteri raporun işlendiği tarihte durdurulmuşsa, kullanıcıyı bilgilendirmek için bir özel durum oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ce632-126">If a selected customer is stopped for the date when the report is processed, an exception is thrown to notify the user.</span></span> <span data-ttu-id="ce632-127">Bu tür bir işleme denetimi için tasarlanmış formül aşağıdaki kaynakları kullanabilir:</span><span class="sxs-lookup"><span data-stu-id="ce632-127">The formula that is designed for this type of processing control can use the following resources:</span></span>

- <span data-ttu-id="ce632-128">Aşağıdaki metine sahip SYS70894 etiketi:</span><span class="sxs-lookup"><span data-stu-id="ce632-128">Label SYS70894, which has the following text:</span></span>

    - <span data-ttu-id="ce632-129">**TR-TR dili için:** "Yazdırılacak hiçbir şey yok"</span><span class="sxs-lookup"><span data-stu-id="ce632-129">**For the EN-US language:** "Nothing to print"</span></span>
    - <span data-ttu-id="ce632-130">**DE dili için** "Nichts zu drucken"</span><span class="sxs-lookup"><span data-stu-id="ce632-130">**For the DE language:** "Nichts zu drucken"</span></span>

- <span data-ttu-id="ce632-131">Aşağıdaki metine sahip SYS18389 etiketi:</span><span class="sxs-lookup"><span data-stu-id="ce632-131">Label SYS18389, which has the following text:</span></span>

    - <span data-ttu-id="ce632-132">**TR-TR dili için:** "Müşteri %1 şunun için durduruldu: %2."</span><span class="sxs-lookup"><span data-stu-id="ce632-132">**For the EN-US language:** "Customer %1 is stopped for %2."</span></span>
    - <span data-ttu-id="ce632-133">**DE dili için:** "Debitor '%1' wird für %2 gesperrt."</span><span class="sxs-lookup"><span data-stu-id="ce632-133">**For the DE language:** "Debitor '%1' wird für %2 gesperrt."</span></span>

<span data-ttu-id="ce632-134">Tasarlanabilen ifade şudur:</span><span class="sxs-lookup"><span data-stu-id="ce632-134">Here is the expression that can be designed.</span></span>

```vb
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

<span data-ttu-id="ce632-135">Rapor **Litware Retail** müşterisi için Aralık 17, 2015 tarihinde **EN-US** kültüründe ve **EN-US** dilinde işlenmişse bu formül son kullanıcıya özel durum iletisi olarak sunulabilecek aşağıdaki metni içerir:</span><span class="sxs-lookup"><span data-stu-id="ce632-135">If a report is processed for the **Litware Retail** customer on December 17, 2015, in the **EN-US** culture and the **EN-US** language, this formula returns the following text, which can be presented to the user as an exception message:</span></span>

<span data-ttu-id="ce632-136">*Yazdırılacak birşey yok. Müşteri Litware perakende 17/12/2015 için durduruldu.*</span><span class="sxs-lookup"><span data-stu-id="ce632-136">*Nothing to print. Customer Litware Retail is stopped for 12/17/2015.*</span></span>

<span data-ttu-id="ce632-137">Aynı rapor **Litware Retail** müşterisi için Aralık 17, 2015 tarihinde **DE** kültürü ve **DE** dilinde işlenmişse, formül başka bir tarih biçimini kullanan aşağıdaki metni döndürür:</span><span class="sxs-lookup"><span data-stu-id="ce632-137">If the same report is processed for the **Litware Retail** customer on December 17, 2015, in the **DE** culture and the **DE** language, the formula returns the following text, which uses a different date format:</span></span>

<span data-ttu-id="ce632-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span><span class="sxs-lookup"><span data-stu-id="ce632-138">*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*</span></span>

>[!NOTE]
> <span data-ttu-id="ce632-139">Aşağıdaki sözdizimi, etiketler için ER formüllerinde kullanılır:</span><span class="sxs-lookup"><span data-stu-id="ce632-139">The following syntax is applied in ER formulas for labels:</span></span>
>
> - <span data-ttu-id="ce632-140">**Microsoft Dynamics 365 Finance uygulamasındaki kaynaklardan etiketler için**: **\@X** (burada **X**, Uygulama Nesne Ağacı (AOT) etiket kimliğidir).</span><span class="sxs-lookup"><span data-stu-id="ce632-140">**For labels from resources in the Microsoft Dynamics 365 Finance app:** **\@X**, where **X** is the label ID in the Application Object Tree (AOT)</span></span>
> - <span data-ttu-id="ce632-141">**ER yapılandırmaları içinde bulunan etiketler için:** **@"GER_LABEL:X"**, burada **X**, ER yapılandırma etiket kimliğidir.</span><span class="sxs-lookup"><span data-stu-id="ce632-141">**For labels that reside in ER configurations:** **@"GER_LABEL:X"**, where **X** is the label ID in the ER configuration</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ce632-142">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ce632-142">Additional resources</span></span>

[<span data-ttu-id="ce632-143">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="ce632-143">Text functions</span></span>](er-functions-category-text.md)

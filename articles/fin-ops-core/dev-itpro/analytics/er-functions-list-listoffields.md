---
title: LISTOFFIELDS ER işlevi
description: Bu konu, LISTOFFIELDS Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d8d9f41d6ee5256f560c83486c95ecd47f5b081
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686524"
---
# <a name="listoffields-er-function"></a><span data-ttu-id="9b47d-103">LISTOFFIELDS ER işlevi</span><span class="sxs-lookup"><span data-stu-id="9b47d-103">LISTOFFIELDS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b47d-104">`LISTOFFIELDS` işlev, *numaralandırmanın* veya *konteyner (kayıt)* türünün belirtilen bağımsız değişkeninin yapısına göre oluşturulan bir *kayıt listesi* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="9b47d-104">The `LISTOFFIELDS` function returns a *Record list* value that is created based on the structure of the specified argument of the *Enumeration* or *Container (record)* type.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="9b47d-105">Sözdizimi 1</span><span class="sxs-lookup"><span data-stu-id="9b47d-105">Syntax 1</span></span>

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a><span data-ttu-id="9b47d-106">Sözdizimi 2</span><span class="sxs-lookup"><span data-stu-id="9b47d-106">Syntax 2</span></span>

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a><span data-ttu-id="9b47d-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="9b47d-107">Arguments</span></span>

<span data-ttu-id="9b47d-108">`path`: Veri kaynağı referansı</span><span class="sxs-lookup"><span data-stu-id="9b47d-108">`path`: Data source reference</span></span>

<span data-ttu-id="9b47d-109">Aşağıdaki veri tiplerinden birinin veri kaynağının geçerli referans yolu:</span><span class="sxs-lookup"><span data-stu-id="9b47d-109">The valid reference path of a data source of one of the following data types:</span></span>

- <span data-ttu-id="9b47d-110">Model numaralandırma</span><span class="sxs-lookup"><span data-stu-id="9b47d-110">Model enumeration</span></span>
- <span data-ttu-id="9b47d-111">Biçim numaralandırma</span><span class="sxs-lookup"><span data-stu-id="9b47d-111">Format enumeration</span></span>
- <span data-ttu-id="9b47d-112">Uygulama numaralandırma</span><span class="sxs-lookup"><span data-stu-id="9b47d-112">Application enumeration</span></span>
- <span data-ttu-id="9b47d-113">Konteyner (kayıt)</span><span class="sxs-lookup"><span data-stu-id="9b47d-113">Container (record)</span></span>

<span data-ttu-id="9b47d-114">`language`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="9b47d-114">`language`: *String*</span></span>

<span data-ttu-id="9b47d-115">Bir dil kodunu temsil eden metin.</span><span class="sxs-lookup"><span data-stu-id="9b47d-115">Text that represents a language code.</span></span>

## <a name="return-values"></a><span data-ttu-id="9b47d-116">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="9b47d-116">Return values</span></span>

<span data-ttu-id="9b47d-117">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="9b47d-117">*Record list*</span></span>

<span data-ttu-id="9b47d-118">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="9b47d-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9b47d-119">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="9b47d-119">Usage notes</span></span>

<span data-ttu-id="9b47d-120">Oluşturulan liste aşağıdaki alanlara sahip kayıtları içerir:</span><span class="sxs-lookup"><span data-stu-id="9b47d-120">The list that is created consists of records that have the following fields:</span></span>

- <span data-ttu-id="9b47d-121">**Ad** (*Dize* veri türü)</span><span class="sxs-lookup"><span data-stu-id="9b47d-121">**Name** (*String* data type)</span></span>
- <span data-ttu-id="9b47d-122">**Etiket** (*Dize* veri türü)</span><span class="sxs-lookup"><span data-stu-id="9b47d-122">**Label** (*String* data type)</span></span>
- <span data-ttu-id="9b47d-123">**Açıklama** (*Dize* veri türü)</span><span class="sxs-lookup"><span data-stu-id="9b47d-123">**Description** (*String* data type)</span></span>
- <span data-ttu-id="9b47d-124">**Çevrildi** (*Boole* veri türü)</span><span class="sxs-lookup"><span data-stu-id="9b47d-124">**IsTranslated** (*Boolean* data type)</span></span>

<span data-ttu-id="9b47d-125">`path` bağımsız değişken *konteyner (kayıt)* türünün bir veri kaynağına başvuruyorsa, başvurulan konteyner kaydının her alanı için, oluşturulan listeye yeni bir kayıt eklenir.</span><span class="sxs-lookup"><span data-stu-id="9b47d-125">If the `path` argument refers to a data source of the *Container (Record)* type, for every field of the referenced container record, a new record is added to the list that is created.</span></span> <span data-ttu-id="9b47d-126">Oluşturulan her kayıt için, **Ad** alanı, geçerli kaydın oluşturulduğu Başvurulmuş konteyner kaydı alanının adını döndürür.</span><span class="sxs-lookup"><span data-stu-id="9b47d-126">For every record that is created, the **Name** field returns the name of the field of the referenced container record that the current record was created for.</span></span>

<span data-ttu-id="9b47d-127">`path` bağımsız değişken *Numaralandırma* türlerinden birinin bir veri kaynağına başvuruyorsa, başvurulan numaralandırmanın her numaralandırma değeri için, oluşturulan listeye yeni bir kayıt eklenir.</span><span class="sxs-lookup"><span data-stu-id="9b47d-127">If the `path` argument refers to a data source of one of the *Enumeration* types, for every enumeration value of the referenced enumeration, a new record is added to the list that is created.</span></span> <span data-ttu-id="9b47d-128">Oluşturulan her kayıt için, **ad** alanı geçerli kaydın oluşturulduğu Başvurulmuş numaralandırmanın değerini döndürür, **Açıklama** alanı ilgili numaralandırmanın açıklamasını döndürür ve **Etiket** alanı o numaralandırmanın etiketini döndürür.</span><span class="sxs-lookup"><span data-stu-id="9b47d-128">For every record that is created, the **Name** field returns the value of the referenced enumeration that the current record was created for, the **Description** field returns the description of that enumeration, and the **Label** field returns the label of that enumeration.</span></span>

<span data-ttu-id="9b47d-129">Çalışma zamanında, sözdizimi 1 kullanıldığında, **Etiket** ve **Açıklama** alanları, çalışmakta olan elektronik raporlama (ER) biçiminin dil ayarlarını temel alan değerler döndürmelidir.</span><span class="sxs-lookup"><span data-stu-id="9b47d-129">At runtime, when syntax 1 is used, the **Label** and **Description** fields must return values that are based on the language settings of the Electronic reporting (ER) format that is running:</span></span>

- <span data-ttu-id="9b47d-130">İstenen dile ait Etiketler ve açıklamalar varsa, **etiket** ve **Açıklama** alanları o dile dayalı olarak değerleri verir ve **Çevrilmiş** alan **doğru** döner.</span><span class="sxs-lookup"><span data-stu-id="9b47d-130">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="9b47d-131">İstenen dile ait Etiketler ve açıklamalar yoksa, **etiket** ve **Açıklama** alanları varsayılan **TR-TR** diline dayalı olarak değerleri verir ve **Çevrilmiş** alan **Yanlış** döner.</span><span class="sxs-lookup"><span data-stu-id="9b47d-131">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the default **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

<span data-ttu-id="9b47d-132">Çalışma zamanında, sözdizimi 2 kullanıldığında, **Etiket** ve **Açıklama** alanları, sözde işlevin ikinci bağımsız değişkeni olarak tanımlanan dil ayarlarını temel alan değerler döndürmelidir.</span><span class="sxs-lookup"><span data-stu-id="9b47d-132">At runtime, when syntax 2 is used, the **Label** and **Description** fields must return values that are based on the language that is defined as the second argument of the called function:</span></span>

- <span data-ttu-id="9b47d-133">İstenen dile ait Etiketler ve açıklamalar varsa, **etiket** ve **Açıklama** alanları o dile dayalı olarak değerleri verir ve **Çevrilmiş** alan **doğru** döner.</span><span class="sxs-lookup"><span data-stu-id="9b47d-133">If the labels and descriptions for the requested language are available, the **Label** and **Description** fields return values that are based on that language, and the **IsTranslated** field returns **True**.</span></span>
- <span data-ttu-id="9b47d-134">İstenen dile ait Etiketler ve açıklamalar yoksa, **etiket** ve **Açıklama** alanları **TR-TR** diline dayalı olarak değerleri verir ve **Çevrilmiş** alan **Yanlış** döner.</span><span class="sxs-lookup"><span data-stu-id="9b47d-134">If the labels and descriptions for the requested language aren't available, the **Label** and **Description** fields return values that are based on the **EN-US** language, and the **IsTranslated** field returns **False**.</span></span>

## <a name="example-1"></a><span data-ttu-id="9b47d-135">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9b47d-135">Example 1</span></span>

<span data-ttu-id="9b47d-136">Aşağıdaki örnekte, bir ER veri modelinde oluşturulan numaralandırma gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="9b47d-136">In the following illustration, an enumeration is introduced in an ER data model.</span></span>

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

<span data-ttu-id="9b47d-137">Aşağıdaki örnek ayrıntıları göstermektedir:</span><span class="sxs-lookup"><span data-stu-id="9b47d-137">The following illustration shows these details:</span></span>

- <span data-ttu-id="9b47d-138">Veri kaynağı olarak bir rapora eklenen model numaralandırma.</span><span class="sxs-lookup"><span data-stu-id="9b47d-138">The model enumeration is inserted into a report as a data source.</span></span>
- <span data-ttu-id="9b47d-139">Bir ER ifadesi `LISTOFFIELDS` işlevi parametresi olarak bir model numaralandırma kullanır.</span><span class="sxs-lookup"><span data-stu-id="9b47d-139">An ER expression uses the model enumeration as a parameter of the `LISTOFFIELDS` function.</span></span>
- <span data-ttu-id="9b47d-140">Oluşturulan ER ifadesini kullanarak bir rapora eklenen *kayıt listesi* türünün veri kaynağı.</span><span class="sxs-lookup"><span data-stu-id="9b47d-140">A data source of the *Record list* type is inserted into a report by using the ER expression that is created.</span></span>

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

<span data-ttu-id="9b47d-141">Aşağıdaki örnek `LISTOFFIELDS` işlevi kullanılarak oluşturulan ve *kayıt listesi* türündeki veri kaynağına bağlı olan ER biçim öğelerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9b47d-141">The following example shows the ER format elements that are bound to the data source of the *Record list* type that was created by using the `LISTOFFIELDS` function.</span></span>

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

<span data-ttu-id="9b47d-142">Aşağıdaki örnekte tasarlanan biçim çalıştırıldığında elde edilen sonuç gösterilir.</span><span class="sxs-lookup"><span data-stu-id="9b47d-142">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> <span data-ttu-id="9b47d-143">Ana **DOSYA** ve **KLASÖR** biçim öğelerinin dil ayarlarına uygun olarak, etiketler ve açıklamalar için çevrilen metin ER biçiminin çıktısına girilir.</span><span class="sxs-lookup"><span data-stu-id="9b47d-143">Based on the language settings of the parent **FILE** and **FOLDER** format elements, translated text for labels and descriptions is entered in the output of the ER format.</span></span>

## <a name="example-2"></a><span data-ttu-id="9b47d-144">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9b47d-144">Example 2</span></span>

<span data-ttu-id="9b47d-145">Örneğin, **enumType** veri modeli numaralandırması için **enumType\_de** ve **enumType\_deCH** veri kaynaklarını yapılandırmak üzere *Hesaplanan alan* veri kaynağı türünü kullanırsınız:</span><span class="sxs-lookup"><span data-stu-id="9b47d-145">You use the *Calculated field* data source type to configure **enumType\_de** and **enumType\_deCH** data sources for the **enumType** data model enumeration:</span></span>

- <span data-ttu-id="9b47d-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span><span class="sxs-lookup"><span data-stu-id="9b47d-146">**enumType\_de** = `LISTOFFIELDS (enumType, "de")`</span></span>
- <span data-ttu-id="9b47d-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span><span class="sxs-lookup"><span data-stu-id="9b47d-147">**enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`</span></span>

<span data-ttu-id="9b47d-148">Bu durumda, bu çevirinin kullanılabilir olması durumunda, numaralandırma değeri etiketiki İsviçre Almancası dilinde almak için aşağıdaki ifadeyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9b47d-148">In this case, you can use the following expression to get the label of the enumeration value in Swiss German, if that translation is available.</span></span> <span data-ttu-id="9b47d-149">İsviçre Almanca çeviri kullanılamıyorsa, Almanca etiketi olur.</span><span class="sxs-lookup"><span data-stu-id="9b47d-149">If the Swiss German translation isn't available, the label is in German.</span></span>

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a><span data-ttu-id="9b47d-150">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="9b47d-150">Additional resources</span></span>

[<span data-ttu-id="9b47d-151">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="9b47d-151">List functions</span></span>](er-functions-category-list.md)

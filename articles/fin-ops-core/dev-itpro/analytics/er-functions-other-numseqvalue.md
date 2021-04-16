---
title: NUMSEQVALUE ER işlevi
description: Bu konu, NUMSEQVALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: c3351360d0c1afca9f828ba4fc935096ddfd67f2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744015"
---
# <a name="numseqvalue-er-function"></a><span data-ttu-id="fef3d-103">NUMSEQVALUE ER işlevi</span><span class="sxs-lookup"><span data-stu-id="fef3d-103">NUMSEQVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fef3d-104">`NUMSEQVALUE` işlev, belirtilen numara serisi, kapsam ve kapsam kimliğine dayalı olarak bir numara serisinin yeni oluşturulan değerini gösteren bir *dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="fef3d-104">The `NUMSEQVALUE` function returns a *String* value that represents the new generated value of a number sequence, based on the specified number sequence, scope, and scope ID.</span></span> <span data-ttu-id="fef3d-105">Kapsam kimliği, Elektronik raporlama (ER) biçiminin altında çalıştırıldığı içerikle sağlanan şirket koduna eşittir.</span><span class="sxs-lookup"><span data-stu-id="fef3d-105">The scope ID equals the company code that is supplied by the context that the Electronic reporting (ER) format is run under.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="fef3d-106">Sözdizimi 1</span><span class="sxs-lookup"><span data-stu-id="fef3d-106">Syntax 1</span></span>

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a><span data-ttu-id="fef3d-107">Sözdizimi 2</span><span class="sxs-lookup"><span data-stu-id="fef3d-107">Syntax 2</span></span>

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a><span data-ttu-id="fef3d-108">Sözdizimi 3</span><span class="sxs-lookup"><span data-stu-id="fef3d-108">Syntax 3</span></span>

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a><span data-ttu-id="fef3d-109">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="fef3d-109">Arguments</span></span>

<span data-ttu-id="fef3d-110">`number sequence code`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="fef3d-110">`number sequence code`: *String*</span></span>

<span data-ttu-id="fef3d-111">Yeni bir değerin gerekli olduğu numara serisinin kodunu temsil eden bir metin değeri.</span><span class="sxs-lookup"><span data-stu-id="fef3d-111">A text value that represents the code of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="fef3d-112">`number sequence record ID`: *Int64*</span><span class="sxs-lookup"><span data-stu-id="fef3d-112">`number sequence record ID`: *Int64*</span></span>

<span data-ttu-id="fef3d-113">NumberSequenceTable tablosundaki bir kaydın, yeni bir değerin gerekli olduğu numara SERISININ tanımını içeren kayıt kodunu temsil eden bir *Int64* değeri.</span><span class="sxs-lookup"><span data-stu-id="fef3d-113">An *Int64* value that represents the record ID of a record in the NumberSequenceTable table that contains the definition of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="fef3d-114">`scope type`: *Numaralandırma değeri*</span><span class="sxs-lookup"><span data-stu-id="fef3d-114">`scope type`: *Enum value*</span></span>

<span data-ttu-id="fef3d-115">Yeni bir değerin gerekli olduğu numara serisinin kapsamını tanımlayan **ERExpressionNumberSequenceScopeType** sabit listesinin numaralandırma değeri.</span><span class="sxs-lookup"><span data-stu-id="fef3d-115">An enumeration value of the **ERExpressionNumberSequenceScopeType** enumeration that defines the scope of the number sequence that a new value is required in.</span></span> <span data-ttu-id="fef3d-116">Kullanılabilir kapsam türleri **paylaşılıyor**, **hukuk varlığı** ve **şirket.**</span><span class="sxs-lookup"><span data-stu-id="fef3d-116">The available scope types are **Shared**, **Legal entity**, and **Company**.</span></span>

<span data-ttu-id="fef3d-117">`scope ID`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="fef3d-117">`scope ID`: *String*</span></span>

<span data-ttu-id="fef3d-118">Belirtilen kapsam türüne göre kapsamı tanımlayan *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="fef3d-118">A *String* value that identifies the scope, based on the specified scope type.</span></span>

## <a name="return-values"></a><span data-ttu-id="fef3d-119">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="fef3d-119">Return values</span></span>

<span data-ttu-id="fef3d-120">*Dize*</span><span class="sxs-lookup"><span data-stu-id="fef3d-120">*String*</span></span>

<span data-ttu-id="fef3d-121">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="fef3d-121">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fef3d-122">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="fef3d-122">Usage notes</span></span>

<span data-ttu-id="fef3d-123">**Paylaşılan** kapsam türü için, kapsam kimliği olarak boş bir dize belirtin.</span><span class="sxs-lookup"><span data-stu-id="fef3d-123">For the **Shared** scope type, specify an empty string as the scope ID.</span></span>

<span data-ttu-id="fef3d-124">**Şirket** ve **Tüzel kişilik** kapsam türleri için, kapsam kimliği olarak şirket kodu belirtin.</span><span class="sxs-lookup"><span data-stu-id="fef3d-124">For the **Company** and **Legal entity** scope types, specify the company code as the scope ID.</span></span> <span data-ttu-id="fef3d-125">Bu tür kapsam türleri, kapsam kimliği olarak boş bir dize belirtirseniz geçerli şirket kodu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fef3d-125">If you specify an empty string as the scope ID for these scope types, the current company code is used.</span></span>

<span data-ttu-id="fef3d-126">Sözdizimi 1 kullanıldığında, numara serisi **Şirket** kapsam türü için istenir ve şirket kodu, er biçiminin altında çalıştırıldığı içerikle sağlanır.</span><span class="sxs-lookup"><span data-stu-id="fef3d-126">When syntax 1 is used, the number sequence is requested for the **Company** scope type, and the company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-1"></a><span data-ttu-id="fef3d-127">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fef3d-127">Example 1</span></span>

<span data-ttu-id="fef3d-128">ER biçiminizde *Kullanıcı giriş parametresi* türünün **AskNumSeq** veri kaynağını tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="fef3d-128">In your ER format, you define the **AskNumSeq** data source of the *User input parameter* type.</span></span> <span data-ttu-id="fef3d-129">Bu veri kaynağı **Açıklama** genişletilmiş veri türü (EDT) anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="fef3d-129">This data source refers to the **Description** extended data type (EDT).</span></span> <span data-ttu-id="fef3d-130">Daha sonra, *hesaplanmış alan* türünün **NumSeq** veri kaynağını tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="fef3d-130">Next, you define the **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="fef3d-131">Bu veri kaynağı `NUMSEQVALUE (AskNumSeq)` ifadesini içeriyor.</span><span class="sxs-lookup"><span data-stu-id="fef3d-131">This data source contains the expression `NUMSEQVALUE (AskNumSeq)`.</span></span> <span data-ttu-id="fef3d-132">**Numseq** veri kaynağı çağrıldığında, iletişim kutusuna kodunu girerek çalışma zamanında belirtilen yeni üretilen değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="fef3d-132">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that was specified at runtime by entering its code in the dialog box.</span></span> <span data-ttu-id="fef3d-133">Numara serisi **Şirket** kapsam türü için istendi.</span><span class="sxs-lookup"><span data-stu-id="fef3d-133">The number sequence is requested for the **Company** scope type.</span></span> <span data-ttu-id="fef3d-134">ER biçiminin altında çalıştırıldığı içerikle sağlanan şirket kodudur.</span><span class="sxs-lookup"><span data-stu-id="fef3d-134">The company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-2"></a><span data-ttu-id="fef3d-135">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="fef3d-135">Example 2</span></span>

<span data-ttu-id="fef3d-136">Model eşlemenizde aşağıdaki veri kaynaklarını tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="fef3d-136">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="fef3d-137">*Tablo* türünün **LedgerParms** veri kaynağı.</span><span class="sxs-lookup"><span data-stu-id="fef3d-137">The **LedgerParms** data source of the *Table* type.</span></span> <span data-ttu-id="fef3d-138">Bu veri kaynağı LedgerParameters tablosuna başvurur.</span><span class="sxs-lookup"><span data-stu-id="fef3d-138">This data source refers to the LedgerParameters table.</span></span>
- <span data-ttu-id="fef3d-139">**NumSeq** veri kaynağına *hesaplanan alan* ekleyin.</span><span class="sxs-lookup"><span data-stu-id="fef3d-139">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="fef3d-140">Bu veri kaynağı `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)` ifadesini içeriyor.</span><span class="sxs-lookup"><span data-stu-id="fef3d-140">This data source contains the expression `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span></span>

<span data-ttu-id="fef3d-141">**NumSeq** veri kaynağı çağrıldığında ER biçimi altında çalışan içerik sağlayan bir şirket için Genel muhasebe parametrelerinde yapılandırılmış Gene1 numara serisinin yeni oluşturulan değeri geri döner.</span><span class="sxs-lookup"><span data-stu-id="fef3d-141">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that has been configured in the General ledger parameters for the company that supplies the context that the ER format is run under.</span></span> <span data-ttu-id="fef3d-142">Bu numara serisi benzersiz biçimde günlükleri tanıtır ve hareketleri birbirine bağlayan toplu iş numarası görevi görür.</span><span class="sxs-lookup"><span data-stu-id="fef3d-142">This number sequence uniquely identifies journals and acts as a batch number that links the transactions together.</span></span>

## <a name="example-3"></a><span data-ttu-id="fef3d-143">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="fef3d-143">Example 3</span></span>

<span data-ttu-id="fef3d-144">Model eşlemenizde aşağıdaki veri kaynaklarını tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="fef3d-144">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="fef3d-145">Microsoft Dynamics 365 Finance *numaralandırma* türünün **enumscope** veri kaynağı.</span><span class="sxs-lookup"><span data-stu-id="fef3d-145">The **enumScope** data source of the Microsoft Dynamics 365 Finance *enumeration* type.</span></span> <span data-ttu-id="fef3d-146">Bu veri kaynağı **ERExpressionNumberSequenceScopeType** numaralandırması anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="fef3d-146">This data source refers to the **ERExpressionNumberSequenceScopeType** enumeration.</span></span>
- <span data-ttu-id="fef3d-147">**NumSeq** veri kaynağına *hesaplanan alan* ekleyin.</span><span class="sxs-lookup"><span data-stu-id="fef3d-147">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="fef3d-148">Bu veri kaynağı `NUMSEQVALUE ("Gene_1", enumScope.Company, "")` ifadesini içeriyor.</span><span class="sxs-lookup"><span data-stu-id="fef3d-148">This data source contains the expression `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span></span>

<span data-ttu-id="fef3d-149">**NumSeq** veri kaynağı çağrıldığında ER biçimi altında çalışan içerik sağlayan bir şirket için yapılandırılmış **Gene\_1** numara serisinin yeni oluşturulan değeri geri döner.</span><span class="sxs-lookup"><span data-stu-id="fef3d-149">When the **NumSeq** data source is called, it returns the new generated value of the **Gene\_1** number sequence that has been configured for the company that supplies the context that the ER format is run under.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fef3d-150">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="fef3d-150">Additional resources</span></span>

[<span data-ttu-id="fef3d-151">Diğer (belirli iş etki alanı) işlevleri</span><span class="sxs-lookup"><span data-stu-id="fef3d-151">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
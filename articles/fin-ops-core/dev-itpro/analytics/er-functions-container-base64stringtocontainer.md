---
title: Base64StringToContainer ER işlevi
description: Bu konu, Base64StringToContainer Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 0e92ae41a3e0f03cb14d4791ab768f096f2a0523
ms.sourcegitcommit: e8a46e127d70986539c138b27a641bff6f6874d0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/15/2020
ms.locfileid: "4739119"
---
# <a name="base64stringtocontainer-er-function"></a><span data-ttu-id="66b98-103">Base64StringToContainer ER işlevi</span><span class="sxs-lookup"><span data-stu-id="66b98-103">Base64StringToContainer ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66b98-104">`BASE64STRINGTOCONTAINER` [işlevi](er-formula-language.md#functions), belirtilen *Dize* veri türündeki girişi *[Konteyner](er-functions-category-container.md)* türünde bir veri öğesine dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="66b98-104">The `BASE64STRINGTOCONTAINER` [function](er-formula-language.md#functions) converts the specified input of the *String* type to a data item of the *[Container](er-functions-category-container.md)* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="66b98-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="66b98-105">Syntax</span></span>

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a><span data-ttu-id="66b98-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="66b98-106">Arguments</span></span>

<span data-ttu-id="66b98-107">`input`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="66b98-107">`input`: *String*</span></span>

<span data-ttu-id="66b98-108">*Dize* türünün veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="66b98-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="66b98-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="66b98-109">Return values</span></span>

<span data-ttu-id="66b98-110">*Konteyner*</span><span class="sxs-lookup"><span data-stu-id="66b98-110">*Container*</span></span>

<span data-ttu-id="66b98-111">Sonuçta elde edilen ikili büyük nesne (BLOB) biçimindeki ikili değer.</span><span class="sxs-lookup"><span data-stu-id="66b98-111">The resulting binary value in binary large object (BLOB) format.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="66b98-112">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="66b98-112">Usage notes</span></span>

<span data-ttu-id="66b98-113">Giriş dizesi doğru bir Base64 ikili değerden metne kodlama şeması grubu sağlamazsa Parametre geçerli değil özel durumu oluşur.</span><span class="sxs-lookup"><span data-stu-id="66b98-113">The "Parameter is not valid" exception is thrown if the input string doesn't provide a correct Base64 group of binary-to-text encoding schemes.</span></span>

## <a name="example"></a><span data-ttu-id="66b98-114">Örnek</span><span class="sxs-lookup"><span data-stu-id="66b98-114">Example</span></span>

<span data-ttu-id="66b98-115">Model eşlemenizde aşağıdaki veri kaynaklarını tanımlayın:</span><span class="sxs-lookup"><span data-stu-id="66b98-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="66b98-116">**DocuTypeGroup** uygulama numaralandırmasına başvuran *Dynamics 365 for Operations / Numaralandırma* türündeki kök **DocuTypeGroupEnum** veri kaynağı</span><span class="sxs-lookup"><span data-stu-id="66b98-116">The root **DocuTypeGroupEnum** data source of the *Dynamics 365 for Operations / Enumeration* type that refers to the **DocuTypeGroup** application enumeration</span></span>
- <span data-ttu-id="66b98-117">**CustTable** uygulama tablosuna başvuran *Dynamics 365 for Operations / Tablo kayıtları* türünün kök **Müşteri** veri kaynağı</span><span class="sxs-lookup"><span data-stu-id="66b98-117">The root **Customer** data source of the *Dynamics 365 for Operations / Table records* type that refers to the **CustTable** application table</span></span>
- <span data-ttu-id="66b98-118">Aşağıdaki şekilde yapılandırılan *Hesaplanmış alan* türünün **\#Ortam** veri kaynağı:</span><span class="sxs-lookup"><span data-stu-id="66b98-118">The **\#Media** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="66b98-119">**Müşteri** veri kaynağının alt veri kaynağı olarak eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="66b98-119">It's added as a child data source of the **Customer** data source.</span></span>
    - <span data-ttu-id="66b98-120">`WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)` ifadesini içerir.</span><span class="sxs-lookup"><span data-stu-id="66b98-120">It contains the expression `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span></span>

- <span data-ttu-id="66b98-121">Aşağıdaki şekilde yapılandırılan *Hesaplanmış alan* türünün **\#MediaAsBase64String** veri kaynağı:</span><span class="sxs-lookup"><span data-stu-id="66b98-121">The **\#MediaAsBase64String** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="66b98-122">**Customer.'\#Media'** veri kaynağının alt veri kaynağı olarak eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="66b98-122">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="66b98-123">`Customer.'#Media'.'getFileContentAsBase64String()'` ifadesini içerir.</span><span class="sxs-lookup"><span data-stu-id="66b98-123">It contains the expression `Customer.'#Media'.'getFileContentAsBase64String()'`.</span></span>

- <span data-ttu-id="66b98-124">Aşağıdaki şekilde yapılandırılan *Hesaplanmış alan* türünün **\#BlobFomBase64** veri kaynağı:</span><span class="sxs-lookup"><span data-stu-id="66b98-124">The **\#BlobFomBase64** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="66b98-125">**Customer.'\#Media'** veri kaynağının alt veri kaynağı olarak eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="66b98-125">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="66b98-126">`Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'` ifadesini içerir.</span><span class="sxs-lookup"><span data-stu-id="66b98-126">It contains the expression `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span></span>

<span data-ttu-id="66b98-127">Bu örnekte, **\#MediaAsBase64String** veri kaynağı, geçerli ortam ekinin ikili içeriğini Base64 ikili değerden metne kodlama şeması grubunu temsil eden bir metin olarak kodlar.</span><span class="sxs-lookup"><span data-stu-id="66b98-127">In this example, the **\#MediaAsBase64String** data source encodes the binary content of the current media attachment as text that represents a Base64 group of binary-to-text encoding schemes.</span></span> <span data-ttu-id="66b98-128">**\#BlobFomBase64** veri kaynağı Base64 dizesinin kodunu çözer ve BLOB biçiminde bir ikili değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="66b98-128">The **\#BlobFomBase64** data source decodes the Base64 string and returns a binary value in BLOB format.</span></span>

![ER Model eşleme tasarımcı sayfasındaki örnek veri kaynakları](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a><span data-ttu-id="66b98-130">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="66b98-130">Additional resources</span></span>

[<span data-ttu-id="66b98-131">Konteyner işlevleri</span><span class="sxs-lookup"><span data-stu-id="66b98-131">Container functions</span></span>](er-functions-category-container.md)

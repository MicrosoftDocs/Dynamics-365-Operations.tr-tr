---
title: QRCODE ER işlevi
description: Bu konu, QRCODE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: bac0910d213ee05a2a7a7b218a6714d4f935be16
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916764"
---
# <span data-ttu-id="6dcd5-103"><a name="QRCODE">QRCODE ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="6dcd5-103"><a name="QRCODE">QRCODE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6dcd5-104">Bu `QRCODE` işlev, belirtilen dizgi için hızlı yanıt kodu (QR kodu) görüntüsünü ikili biçimde gösteren bir *konteyner* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="6dcd5-104">The `QRCODE` function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dcd5-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="6dcd5-105">Syntax</span></span>

```
QRCODE (text)
```

## <a name="arguments"></a><span data-ttu-id="6dcd5-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="6dcd5-106">Arguments</span></span>

<span data-ttu-id="6dcd5-107">`text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="6dcd5-107">`text`: *String*</span></span>

<span data-ttu-id="6dcd5-108">Orijinal metni temsil eden bir *dize* değeri.</span><span class="sxs-lookup"><span data-stu-id="6dcd5-108">A *String* value that represents the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="6dcd5-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="6dcd5-109">Return values</span></span>

<span data-ttu-id="6dcd5-110">*Kapsayıcı*</span><span class="sxs-lookup"><span data-stu-id="6dcd5-110">*Container*</span></span>

<span data-ttu-id="6dcd5-111">Sonuçta elde edilen ikili akış.</span><span class="sxs-lookup"><span data-stu-id="6dcd5-111">The resulting binary stream.</span></span>

## <a name="example"></a><span data-ttu-id="6dcd5-112">Örnek</span><span class="sxs-lookup"><span data-stu-id="6dcd5-112">Example</span></span>

<span data-ttu-id="6dcd5-113">Bir elektronik raporlama (ER) biçimini, önceden tanımlanmış bir şablonu kullanarak bir giden belgeyi Microsoft Office biçiminde (Excel çalışma kitapları veya Word belgeleri) oluşturmak için yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6dcd5-113">You can configure an Electronic reporting (ER) format to generate an outbound document in Microsoft Office format (Excel workbooks or Word documents) by using a predefined template.</span></span> <span data-ttu-id="6dcd5-114">Bu şablon bir QR kodu görüntüsü için yer tutucu olarak bir **resim** nesnesi (Excel çalışma kitabı) veya bir **resim içeriği denetimi** (Word belgesi) içeriyor olabilir.</span><span class="sxs-lookup"><span data-stu-id="6dcd5-114">This template may contain a **Picture** object (Excel workbook) or a **Picture Content Control** (Word document) as a placeholder for a QR code image.</span></span> <span data-ttu-id="6dcd5-115">Yapılandırılan ER'ye bu yer tutucuyu doldurmak için kullanılacak bir **hücre** öğesi biçimini yapılandırılmış bir şekilde eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6dcd5-115">You need to add to the configured ER format a **Cell** element that will be used to fill this placeholder in.</span></span> <span data-ttu-id="6dcd5-116">Bir QR kodunda depolanacak bilgileri belirtmek için, bu **hücre** öğesi için bir bağlama tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="6dcd5-116">To specify what information will be stored in a QR code, you need to define a binding for this **Cell** element.</span></span> <span data-ttu-id="6dcd5-117">Örneğin, bu bağlamayı aşağıdaki ifadeyi içerecek biçimde yapılandırabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="6dcd5-117">For example, you can configure such binding as containing the following expression:</span></span>

```
QRCODE (model.ListOfShelfLabels.LabelText)`
```

<span data-ttu-id="6dcd5-118">Yapılandırılmış ER biçimini çalıştırdığınızda, modelin **LabelText** alanının metin değerini Bir QR kod görüntüsü oluşturmak için **model.ListOfShelfLabels** veri kaynağı kullanılacak.</span><span class="sxs-lookup"><span data-stu-id="6dcd5-118">When you run the configured ER format, the text value of the **LabelText** field of the **model.ListOfShelfLabels** data source will be used to generate a QR code image.</span></span> <span data-ttu-id="6dcd5-119">Bu resim, belge şablonundaki bir QR kodu görüntü yer tutucusunun giden bir belge oluşturmak amacıyla kullanılarak değiştirilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="6dcd5-119">This image will replace a QR code image placeholder in the document template using to generate an outbound document.</span></span> <span data-ttu-id="6dcd5-120">Oluşturulan belgenin bu görüntüsü tarandığında, **model.ListOfShelfLabels** veri kaynağının **LabelText** alanından alınan metni döndürür.</span><span class="sxs-lookup"><span data-stu-id="6dcd5-120">When this image of the generated document is scanned, it returns the text that was taken from the **LabelText** field of the **model.ListOfShelfLabels** data source.</span></span> <span data-ttu-id="6dcd5-121">Daha fazla bilgi için [Er kullanarak oluşturduğunuz belgelere resimler ve şekiller katıştırma](electronic-reporting-embed-images-shapes.md)</span><span class="sxs-lookup"><span data-stu-id="6dcd5-121">For more information, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6dcd5-122">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="6dcd5-122">Additional resources</span></span>

[<span data-ttu-id="6dcd5-123">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="6dcd5-123">Text functions</span></span>](er-functions-category-text.md)

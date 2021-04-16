---
title: ALLITEMS ER işlevi
description: Bu konu, ALLITEMS Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 5ddcf989bdfd1d1f5d0a412a2ffefe0e3037ca79
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746735"
---
# <a name="allitems-er-function"></a><span data-ttu-id="ec985-103">ALLITEMS ER işlevi</span><span class="sxs-lookup"><span data-stu-id="ec985-103">ALLITEMS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec985-104">`ALLITEMS` işlevi, bellek içi seçim olarak çalışır ve belirtilen yolla eşleşen tüm öğeleri temsil eden kayıtların listesi olarak yeni bir düzleştirilmiş *kayıt listesi* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="ec985-104">The `ALLITEMS` function runs as an in-memory selection and returns a new flattened *Record list* value as a list of records that represents all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec985-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="ec985-105">Syntax</span></span>

```vb
ALLITEMS (path)
```

## <a name="arguments"></a><span data-ttu-id="ec985-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="ec985-106">Arguments</span></span>

<span data-ttu-id="ec985-107">`path`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="ec985-107">`path`: *Record list*</span></span>

<span data-ttu-id="ec985-108">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="ec985-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="ec985-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="ec985-109">Return values</span></span>

<span data-ttu-id="ec985-110">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="ec985-110">*Record list*</span></span>

<span data-ttu-id="ec985-111">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="ec985-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ec985-112">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="ec985-112">Usage notes</span></span>

<span data-ttu-id="ec985-113">Yol, *kayıt listesi* veri türünün veri kaynağı öğesine geçerli veri kaynağı yolu olarak tanımlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ec985-113">The path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="ec985-114">Dize yolu ve tarih gibi veri öğeleri, elektronik raporlama (ER) ifade oluşturucuda tasarım zamanında hata vermelidir.</span><span class="sxs-lookup"><span data-stu-id="ec985-114">Data elements such as the path string and date should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="ec985-115">Büyük miktarda veri içerebilen işlem veri kaynakları için bu işlevi kullanmanızı önermeyiz.</span><span class="sxs-lookup"><span data-stu-id="ec985-115">We don't recommend that you use this function for transactional data sources that might contain a large volume of data.</span></span> <span data-ttu-id="ec985-116">Bunun yerine, [ALLTEMSQUERY](er-functions-list-allitemsquery.md) işlevini kullanmayı düşünebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec985-116">Instead, consider using the [ALLTEMSQUERY](er-functions-list-allitemsquery.md) function.</span></span>

## <a name="example-1"></a><span data-ttu-id="ec985-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ec985-117">Example 1</span></span>

<span data-ttu-id="ec985-118">`SPLIT("abcdef" , 2)` veri kaynağı **DS** olarak girerseniz, ifade `COUNT( ALLITEMS (DS))` **3** döndürür.</span><span class="sxs-lookup"><span data-stu-id="ec985-118">If you enter `SPLIT("abcdef" , 2)` as data source **DS**, the expression `COUNT( ALLITEMS (DS))` returns **3**.</span></span>

## <a name="example-2"></a><span data-ttu-id="ec985-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ec985-119">Example 2</span></span>

<span data-ttu-id="ec985-120">VendTable uygulama tablosuna başvuran *kayıt listesi* veri türünün veri kaynağına **Vend** değerini girerseniz `ALLITEMS (Vend.'<Relations'.ContactPerson)` ifadesi, **ContactPerson** yapısına sahip bir kayıt listesi döndürür ve **ContactPerson.ContactForParty == VendTable.Party** ilişkisi kullanılarak erişilebilen tüm irtibat kişilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="ec985-120">If you enter **Vend** as the data source of the *Record list* data type that refers to the VendTable application table, the expression `ALLITEMS (Vend.'<Relations'.ContactPerson)` returns a flattened list of records that has the **ContactPerson** table structure and contains all contact persons that can be accessed by using the **ContactPerson.ContactForParty == VendTable.Party** relation, and that is available for all vendors from the referenced vendor table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ec985-121">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ec985-121">Additional resources</span></span>

[<span data-ttu-id="ec985-122">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="ec985-122">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
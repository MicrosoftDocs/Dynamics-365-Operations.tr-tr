---
title: Mali boyutları tanımlama
description: Bu görev kılavuzu, varlığa dayalı bir mali boyutun ve özel bir mali boyutun nasıl ekleneceğini gösterir.
author: aprilolson
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6fbe739eec0cfa1e7b0276872640bd4f82be3ef7
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138348"
---
# <a name="define-financial-dimensions"></a><span data-ttu-id="a8476-103">Mali boyutları tanımlama</span><span class="sxs-lookup"><span data-stu-id="a8476-103">Define financial dimensions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a8476-104">Bu görev kılavuzu, varlığa dayalı bir mali boyutun ve özel bir mali boyutun nasıl ekleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8476-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="a8476-105">Kılavuz, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a8476-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="a8476-106">Bir varlığa dayalı mali boyut oluştur</span><span class="sxs-lookup"><span data-stu-id="a8476-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="a8476-107">**Gezinti bölmesi > Modüller > Genel muhasebe > Hesap planı > Boyutlar > Mali boyutlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="a8476-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Dimensions > Financial dimensions**.</span></span>
2. <span data-ttu-id="a8476-108">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a8476-108">Click **New**.</span></span>
3. <span data-ttu-id="a8476-109">**Kullanıcı değerleri formu** alanında, mali boyuta temel oluşturacak sistem tanımlı bir varlık seçin.</span><span class="sxs-lookup"><span data-stu-id="a8476-109">In the **User values form** field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="a8476-110">**Boyut adı** alanında, mali boyutu tanımlamak için bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a8476-110">In the **Dimension name** field, type a value to describe the financial dimension.</span></span> <span data-ttu-id="a8476-111">Ad, sistem tanımlı varlıktan farklı olabilir ancak boşluk veya özel karakterler içeremez.</span><span class="sxs-lookup"><span data-stu-id="a8476-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>
5. <span data-ttu-id="a8476-112">**Etkinleştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a8476-112">Click **Activate**.</span></span> <span data-ttu-id="a8476-113">Mali boyut etkinleştirmesi tabloyu mali boyut adıyla güncelleştirir ve silinen boyutları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a8476-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="a8476-114">Mali boyutu etkinleştirmeden önce boyut değerleri girebilirsiniz ancak mali boyut etkinleştirilene kadar kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="a8476-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="a8476-115">Etkinleştirme iletisinde **Kapat** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a8476-115">Click **Close** on the activation message.</span></span>
7. <span data-ttu-id="a8476-116">**Etkinleştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a8476-116">Click **Activate**.</span></span> <span data-ttu-id="a8476-117">Boyut etkinleştirmesi, toplu iş tarafından belirli bir tarih ve saatte çalışacak şekilde zamanlanabilir.</span><span class="sxs-lookup"><span data-stu-id="a8476-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="a8476-118">**Eylem bölmesinde** **Boyut değerleri** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a8476-118">On **Action pane**, click **Dimension values**.</span></span> <span data-ttu-id="a8476-119">Bazı boyut değerleri şirkete özgüdür.</span><span class="sxs-lookup"><span data-stu-id="a8476-119">Some dimension values are company specific.</span></span> <span data-ttu-id="a8476-120">Şirket adı boyut değerleri listesinde gösteriliyorsa, şirkete özgü olup olmadığını doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8476-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="a8476-121">Bir özel mali boyut oluştur</span><span class="sxs-lookup"><span data-stu-id="a8476-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="a8476-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a8476-122">Close the page.</span></span>
2. <span data-ttu-id="a8476-123">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a8476-123">Click **New**.</span></span>
3. <span data-ttu-id="a8476-124">**Şuradan alınan değerleri kullan** alanında, **Özel boyut** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a8476-124">In the **Use values from** field, select **Custom dimension**.</span></span>
4. <span data-ttu-id="a8476-125">**Boyut adı** alanında, mali boyutu tanımlamak için bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a8476-125">In the **Dimension name** field, type a value to describe the financial dimension.</span></span>
    - <span data-ttu-id="a8476-126">Ad, boşluk veya özel karakter içeremez.</span><span class="sxs-lookup"><span data-stu-id="a8476-126">The name cannot contain spaces or special characters.</span></span>  
    - <span data-ttu-id="a8476-127">Boyut değerleri için girebileceğiniz bilgi miktarını ve türünü sınırlamak üzere bir hesap maskesi de belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8476-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    - <span data-ttu-id="a8476-128">Harf veya tire gibi her boyut değeri için aynı kalan karakterler girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8476-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="a8476-129">Her boyut değeri oluşturulduğunda değişen harfler ve sayılar için yer tutucu olarak sayı işaretleri (#) ve 've' işareti (&) de girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8476-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="a8476-130">Bir sayının yer tutucusu olarak sayı işareti (#) ve bir harfin yer tutucusu olarak "ve" işareti (&) kullanın.</span><span class="sxs-lookup"><span data-stu-id="a8476-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="a8476-131">Örnek: Boyutu CC harfleri ve üç sayıyla sınırlamak için CC-### biçim maskesini girin.</span><span class="sxs-lookup"><span data-stu-id="a8476-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="a8476-132">**Etkinleştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a8476-132">Click **Activate**.</span></span> <span data-ttu-id="a8476-133">Mali boyut etkinleştirmesi tabloyu mali boyut adıyla güncelleştirir ve silinen boyutları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a8476-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="a8476-134">Mali boyutu etkinleştirmeden önce boyut değerleri girebilirsiniz ancak mali boyut etkinleştirilene kadar kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="a8476-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>     
6. <span data-ttu-id="a8476-135">**Etkinleştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a8476-135">Click **Activate**.</span></span> <span data-ttu-id="a8476-136">Boyut etkinleştirmesi, toplu iş tarafından belirli bir tarih ve saatte çalışacak şekilde zamanlanabilir.</span><span class="sxs-lookup"><span data-stu-id="a8476-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>      
7. <span data-ttu-id="a8476-137">**Eylem bölmesinde** **Boyut değerleri** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a8476-137">On **Action pane**, click **Dimension values**.</span></span>
8. <span data-ttu-id="a8476-138">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a8476-138">Click **New**.</span></span>
9. <span data-ttu-id="a8476-139">**Boyut değeri** alanında, mali boyut değerinizi tanımlamak için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="a8476-139">In the **Dimension value** field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="a8476-140">**Açıklama** alanına, mali boyut değerinizi tanımlayan bir açıklama yazın.</span><span class="sxs-lookup"><span data-stu-id="a8476-140">In the **Description** field, type a description that describes your financial dimension value.</span></span>


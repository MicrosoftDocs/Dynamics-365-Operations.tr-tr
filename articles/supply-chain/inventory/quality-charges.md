---
title: Uygunsuzluk işlemleri giderleri
description: Bu konu, uyumsuzlukla ilgili işlemlerle kullanılabilecek kalite masraflarının nasıl oluşturulacağını açıklamaktadır.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 382890232bff47a885840af1eb7e91d27bb46cae
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022312"
---
# <a name="charges-for-nonconformance-operations"></a><span data-ttu-id="825be-103">Uygunsuzluk işlemleri giderleri</span><span class="sxs-lookup"><span data-stu-id="825be-103">Charges for nonconformance operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="825be-104">Bu konu, uyumsuzlukla ilgili işlemlerle kullanılabilecek kalite masraflarının nasıl oluşturulacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="825be-104">This topic describes how to create quality charges that can be used with operations for a nonconformance.</span></span>

<span data-ttu-id="825be-105">**Kalite giderleri** sayfasını, uygunsuzluklar ile ilgili işlemlerine eklenebilecek giderlerin türlerini tanımlamak için kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="825be-105">You use the **Quality charges** page to define the types of charges that can be added to operations for a nonconformance.</span></span> <span data-ttu-id="825be-106">Giderler, uygunsuz ürünlerle ilgili olarak müşteriye borçlu olduğunuz ücretler veya giderlerle ilgili ayrıntıları izlemenize veya bir satıcının aldığınız uygunsuz ürünler için size olan borcuyla ilgili ayrıntıları izlemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="825be-106">Charges let you track details about fees or charges that you owe to a customer for nonconforming products, or that a vendor owes to you for nonconforming products that you received.</span></span> <span data-ttu-id="825be-107">Ayrıca giderleri, harici satıcılar veya servisler için gereken maliyetleri izlemek için de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="825be-107">You might also use charges to track costs that are required for external vendors or services to perform an operation.</span></span>

## <a name="examples-of-quality-charges"></a><span data-ttu-id="825be-108">Kalite gideri örnekleri</span><span class="sxs-lookup"><span data-stu-id="825be-108">Examples of quality charges</span></span>

<span data-ttu-id="825be-109">Bir üretim şirketi için çalışırsınız.</span><span class="sxs-lookup"><span data-stu-id="825be-109">You work for a manufacturing company.</span></span> <span data-ttu-id="825be-110">Şirketinizin birkaç satıcıyla sözleşmesi vardır.</span><span class="sxs-lookup"><span data-stu-id="825be-110">Your company has contracts with several vendors.</span></span> <span data-ttu-id="825be-111">Bu sözleşmeler, maddelere ait zamanında sevkiyat, zararlar ve ürün kalitesiyle ilgili standartların ana hatlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="825be-111">Those contracts outline standards for on-time shipment, damages, and product quality for items.</span></span> <span data-ttu-id="825be-112">Benzer şekilde, müşterilerinizin bazıları iadeler, zararlarla ve ürün kalitesiyle ilgili olarak şirketinizle sözleşmeleri vardır.</span><span class="sxs-lookup"><span data-stu-id="825be-112">Likewise, several of your customers have agreements with your company about returns, damages, and product quality.</span></span>

<span data-ttu-id="825be-113">Her bir koşul için bir ücret yapısı belirlenir ve sözleşmede belirlenir.</span><span class="sxs-lookup"><span data-stu-id="825be-113">A fee structure is defined for each circumstance and specified in the contract.</span></span> <span data-ttu-id="825be-114">*Zararlar*, *Geç sevkiyat* ve *Kalite* gibi çeşitli türde giderleri ana hatlarıyla ortaya koymak için kalite ücretlerini yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="825be-114">You can configure quality charges to outline the various types of charges, such as *Damages*, *Late shipment*, and *Quality*.</span></span> <span data-ttu-id="825be-115">Daha sonra, uygunsuzluk oluşturduğunuzda bir veya daha fazla işlem eklersiniz.</span><span class="sxs-lookup"><span data-stu-id="825be-115">Then, when you create a nonconformance, you add one or more operations.</span></span> <span data-ttu-id="825be-116">Her işlem için, ücretler hakkındaki ayrıntıları tanımlamak üzere **Giderler**'i seçersiniz.</span><span class="sxs-lookup"><span data-stu-id="825be-116">For each operation, you select **Charges** to define the details about the fees.</span></span>

## <a name="create-a-quality-charge"></a><span data-ttu-id="825be-117">Kalite gideri oluşturma</span><span class="sxs-lookup"><span data-stu-id="825be-117">Create a quality charge</span></span>

1. <span data-ttu-id="825be-118">**Stok yönetimi \> Kurulum \> Kalite yönetimi \> Kalite giderleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="825be-118">Go to **Inventory management \> Setup \> Quality management \> Quality charges**.</span></span>
1. <span data-ttu-id="825be-119">Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="825be-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="825be-120">Ardından yeni satırda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="825be-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="825be-121">**Gider kodu** – Kalite gideri için benzersiz bir kod ya da ad girin.</span><span class="sxs-lookup"><span data-stu-id="825be-121">**Charges code** – Enter a unique ID or name for the quality charge.</span></span>
    - <span data-ttu-id="825be-122">**Açıklama** – Kalite giderinin detaylı bir açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="825be-122">**Description** – Enter a detailed description of the quality charge.</span></span>

1. <span data-ttu-id="825be-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="825be-123">Close the page.</span></span>

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a><span data-ttu-id="825be-124">Uygunsuzluk için işlem kalite gideri ekleme</span><span class="sxs-lookup"><span data-stu-id="825be-124">Add a quality charge to an operation for a nonconformance</span></span>

<span data-ttu-id="825be-125">Uygunsuzluklara işlem ekleme ve bunlara ücret uygulama hakkında ayrıntılar için bkz. [Uygunsuzluklar için işlemler](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="825be-125">For details about how to add operations to a nonconformance and apply charges to them, see [Operations for nonconformances](quality-operations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="825be-126">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="825be-126">Additional resources</span></span>

- [<span data-ttu-id="825be-127">Kalite yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="825be-127">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="825be-128">Kalite ve uygunsuzluk yönetimini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="825be-128">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="825be-129">Uygunsuzlukları onaylamaktan sorumlu çalışanlar</span><span class="sxs-lookup"><span data-stu-id="825be-129">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="825be-130">Uygunsuzluklar için karantina bölgeleri</span><span class="sxs-lookup"><span data-stu-id="825be-130">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="825be-131">Uygunsuzluklar için tanılama türleri</span><span class="sxs-lookup"><span data-stu-id="825be-131">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="825be-132">Uygunsuzluklar için kalite masrafları</span><span class="sxs-lookup"><span data-stu-id="825be-132">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="825be-133">Uygunsuzluklar için işlemler</span><span class="sxs-lookup"><span data-stu-id="825be-133">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="825be-134">Ambar işlemleri için kalite yönetimi</span><span class="sxs-lookup"><span data-stu-id="825be-134">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

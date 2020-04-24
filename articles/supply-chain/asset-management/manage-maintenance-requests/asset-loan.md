---
title: Ödünç varlıklar
description: Bu konuda Varlık Yönetimi'nde ödünç varlık kaydetme işlemi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 07472188051aea7084142cc417c6d725462cf4f9
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205265"
---
# <a name="asset-loans"></a><span data-ttu-id="a900d-103">Ödünç varlıklar</span><span class="sxs-lookup"><span data-stu-id="a900d-103">Asset loans</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a900d-104">Şirketiniz, dahili konumlardan veya müşterilerden onarım veya bakım işleri için varlıklar alırsa ve varlıkları bu konumlara veya müşterilere geçici olarak ödünç veriyorsanız varlık yönetimi ödünç varlıklarını izleyebilir.</span><span class="sxs-lookup"><span data-stu-id="a900d-104">If your company receives assets for repair or maintenance jobs from either internal locations or customers, and if you temporarily loan assets to those locations or customers, Asset Management can track the asset loans.</span></span>

## <a name="register-asset-loans-on-a-maintenance-request"></a><span data-ttu-id="a900d-105">Bir bakım talebine ödünç varlık kaydetme</span><span class="sxs-lookup"><span data-stu-id="a900d-105">Register asset loans on a maintenance request</span></span>

1. <span data-ttu-id="a900d-106">**Varlık yönetimi** \> **Ortak** \> **Bakım talepleri** \> **Tüm bakım talepleri** ya da **Etkin bakım talepleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="a900d-106">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="a900d-107">Bir ödünç varlığa kaydedilecek bakım talebini seçin ve ardından **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a900d-107">Select the maintenance request to register an asset loan on, and then select **Edit**.</span></span>
3. <span data-ttu-id="a900d-108">**İstek** sayfasında **Ödünç varlığı gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a900d-108">On the **Request** page, select **Send loan asset**.</span></span>
4. <span data-ttu-id="a900d-109">Varlığı seçin ve beklenen dönüş tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="a900d-109">Select the asset, and enter the expected return date.</span></span>
5. <span data-ttu-id="a900d-110">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a900d-110">Select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="a900d-111">Bir ödünç varlığı yalnızca aynı varlık türünün bir varlığı kullanılabilir olduğunda gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a900d-111">You can send a loan asset only if an asset of the same asset type is available.</span></span>
> - <span data-ttu-id="a900d-112">Ödünç verilen varlığın **Depoda** gibi bir ödünç varlık olarak kullanılmasını sağlayan bir varlığın yaşam döngüsü durumuna sahip olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a900d-112">The asset that you loan must have an asset lifecycle state that allows it to be used as a loan asset, such as **InStorage**.</span></span> <span data-ttu-id="a900d-113">Ödünç varlık kaydedildiğinde, varlığın varlık yaşam döngüsü durumu otomatik olarak, örneğin **Ödünç Verildi** olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="a900d-113">When the asset loan is registered, the asset lifecycle state of the asset is automatically updated to, for example, **OnLoan**.</span></span>

<span data-ttu-id="a900d-114">Diğer yerlere veya müşterilere ödünç vermiş olduğunuz tüm varlıkların listesini görüntülemek için **Varlık yönetimi** \> **Ortak** \> **Ödünç varlık** \> **Tüm ödünç varlıklar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a900d-114">To view a list of all the assets that you've loaned to other locations or customers, select **Asset management** \> **Common** \> **Asset loan** \> **All asset loans**.</span></span> <span data-ttu-id="a900d-115">Bir varlık için **Sona erdi** kutusu seçiliyse varlık şirketiniz için iade edilmiş olarak kalır.</span><span class="sxs-lookup"><span data-stu-id="a900d-115">If the **Ended** check box is selected for an asset, the asset has been registered as returned to your company.</span></span>

![Bakım Taleplerini Yönetme](media/06-manage-maintenance-requests.png)

<span data-ttu-id="a900d-117">**Etkin ödünç varlıklar** sayfasında henüz şirketinize iade edilmeyen tüm ödünç varlıkların listesini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a900d-117">On the **Active asset loans** page, you can view a list of all the loan assets that haven't yet been returned to your company.</span></span>

## <a name="register-loan-assets-as-returned"></a><span data-ttu-id="a900d-118">İade edilen ödünç varlıkları kaydedin</span><span class="sxs-lookup"><span data-stu-id="a900d-118">Register loan assets as returned</span></span>

1. <span data-ttu-id="a900d-119">**Varlık yönetimi** \> **Ortak** \> **Ödünç varlık** \> **Etkin ödünç varlıklar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a900d-119">Select **Asset management** \> **Common** \> **Asset loan** \> **Active asset loans**.</span></span>
2. <span data-ttu-id="a900d-120">İade edilen olarak kaydetmek için ödünç varlık'ı seçin ve sonra **Ödünç varlığı iade edin**'i seçin..</span><span class="sxs-lookup"><span data-stu-id="a900d-120">Select the asset loan to register as returned, and then select **Return asset loan**.</span></span>
3. <span data-ttu-id="a900d-121">**İade edildi** alanında tarihi ve saati girin.</span><span class="sxs-lookup"><span data-stu-id="a900d-121">In the **Returned** field, enter the date and time.</span></span>
4. <span data-ttu-id="a900d-122">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a900d-122">Select **OK**.</span></span>
5. <span data-ttu-id="a900d-123">**Etkin ödünç varlıklar** listesi sayfasını yenileyin ve ödünç varlığın artık listede görünüp görünmediğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="a900d-123">Refresh the **Active asset loans** list page, and notice that the asset loan no longer appears in the list.</span></span>

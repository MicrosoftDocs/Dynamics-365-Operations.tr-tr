---
title: Kıymet ve kıymet türlerinde garantiler
description: Bu konu, Varlık Yönetimi'nde kıymet garantilerinin ve kıymet türlerinin nasıl ayarlanacağını açıklar.
author: josaw1
manager: tfehr
ms.date: 08/30/2019
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
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 75de9a51560dcd8fea7998425fee14a27e891972
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439437"
---
# <a name="warranties-on-assets-and-asset-types"></a><span data-ttu-id="db80a-103">Kıymet ve kıymet türlerinde garantiler</span><span class="sxs-lookup"><span data-stu-id="db80a-103">Warranties on assets and asset types</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="db80a-104">Bu konu, Varlık Yönetimi'nde kıymet garantilerinin ve kıymet türlerinin nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="db80a-104">This topic explains how to set up warranties on assets and asset types in Asset Management.</span></span>

## <a name="set-up-a-warranty-on-an-asset-type"></a><span data-ttu-id="db80a-105">Kıymet türünde garanti ayarlayın</span><span class="sxs-lookup"><span data-stu-id="db80a-105">Set up a warranty on an asset type</span></span>

1. <span data-ttu-id="db80a-106">**Varlık yönetimi** \> **Kurulum** \> **Varlık türleri** \> **Varlık türleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="db80a-106">Select **Asset management** \> **Setup** \> **Asset types** \> **Asset types**.</span></span>
2. <span data-ttu-id="db80a-107">Sol bölmede, satıcı garanti sözleşmesini iliştirmek için sabit kıymet türünü seçin ve **Kıymet türü varsayılanları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="db80a-107">In the left pane, select the asset type to attach a vendor warranty agreement to, and then select **Asset type defaults**.</span></span>
3. <span data-ttu-id="db80a-108">**Genel** hızlı sekmesinde, **Satıcı garantisi** alanında, sözleşmeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="db80a-108">On the **General** FastTab, in the **Vendor warranty** field, select the agreement.</span></span>

## <a name="set-up-a-warranty-on-an-asset"></a><span data-ttu-id="db80a-109">Kıymette garanti ayarlayın</span><span class="sxs-lookup"><span data-stu-id="db80a-109">Set up a warranty on an asset</span></span>

1. <span data-ttu-id="db80a-110">**Kıymet yönetimi** \> **Ortak** \> **Kıymetler** \> **Tüm kıymetler** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="db80a-110">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="db80a-111">Kıymeti seçin ve **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="db80a-111">Select the asset, and then select **Edit**.</span></span>
3. <span data-ttu-id="db80a-112">**Satıcı** hızlı sekmesinde, **Satıcı garantisi** bölümünde, **Garanti** alanında, garanti sözleşmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="db80a-112">On the **Vendor** FastTab, in the **Vendor warranty** section, in the **Warranty** field, select the warranty agreement.</span></span>
4. <span data-ttu-id="db80a-113">**Garanti başlangıcı** ve **Garanti sonu** alanlarında, başlangıç ve bitiş tarihlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="db80a-113">In the **Warranty start** and **Warranty end** fields, select the start and end dates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="db80a-114">Bir iş emrinin **Garanti başlangıcı** alanında bir tarih seçilirse garanti o tarihteki iş emri için geçerli olur.</span><span class="sxs-lookup"><span data-stu-id="db80a-114">If a date is selected in the **Warranty start** field on a work order, the warranty becomes valid for the work order on that date.</span></span> <span data-ttu-id="db80a-115">Bir iş emri oluşturduğunuzda, **Garanti başlangıcı** alanı otomatik olarak oluşturma tarihine göre ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="db80a-115">When you create a work order, the **Warranty start** field is automatically set to the date of creation.</span></span> <span data-ttu-id="db80a-116">Ancak, tarihi, örneğin garanti anlaşmasının başlangıç tarihine karşılık gelecek şekilde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="db80a-116">However, you can change the date so that it corresponds to, for example, the start date of a warranty agreement.</span></span>
    >
    > ![İş emri sayfası](media/02-warranty.png)

> [!NOTE]
> <span data-ttu-id="db80a-118">Satıcı garantisinin kapsadığı bir kıymet için çalışma emri oluşturduğunuzda, iş emrinde garanti dönemi içinde beklenen başlangıç tarihi varsa garanti sözleşmesiyle ilgili bir bildirim alırsınız.</span><span class="sxs-lookup"><span data-stu-id="db80a-118">When you create a work order for an asset that is covered by a vendor warranty, if the work order has an expected start date during the warranty period, you receive a notification about the warranty agreement.</span></span> <span data-ttu-id="db80a-119">Böylece, gereksinim duyduğunuz şekilde iş emrini iptal edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="db80a-119">You can then cancel the work order, as you require.</span></span>

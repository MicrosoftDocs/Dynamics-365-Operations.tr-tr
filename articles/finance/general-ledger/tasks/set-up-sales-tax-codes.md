---
title: Satış vergisi kodlarını ayarlama
description: Bu konuda, Dynamics 365 Finance'da satış vergisi kodlarının nasıl ayarlanacağı açıklanmaktadır.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6c7208fa65905fcc902d9c08b5b90178745e76d4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815056"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="74d62-103">Satış vergisi kodlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="74d62-103">Set up sales tax codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="74d62-104">Bu konuda, satış vergisi kodlarının nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="74d62-104">This topic explains how to set up sales tax codes.</span></span> <span data-ttu-id="74d62-105">Tüzel kişiliğin hesaplamak, tahsil etmek ve vergi dairelerine ödemekle yükümlü olduğu her dolaylı vergi ve harç için satış vergisi kodları oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="74d62-105">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="74d62-106">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="74d62-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="74d62-107">**Gezinme bölmesi > Vergi > Dolaylı vergiler > Satış vergisi > Satış vergisi kodları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="74d62-107">Go to **Navigation pane > Tax > Indirect taxes > Sales tax > Sales tax codes**.</span></span>
2. <span data-ttu-id="74d62-108">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="74d62-108">Select **New**.</span></span>
3. <span data-ttu-id="74d62-109">**Satış vergisi kodu** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="74d62-109">In the **Sales tax code** field, type a value.</span></span>
4. <span data-ttu-id="74d62-110">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="74d62-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="74d62-111">Bu satış vergisinin hangi vergi dairesine, hangi aralıklarda bildirilip ödenmesi gerektiğini belirtmek üzere açılır listeyi açarak bir **Kapatma dönemi** seçin.</span><span class="sxs-lookup"><span data-stu-id="74d62-111">Select a **Settlement period** by opening the pull-down list to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="74d62-112">Satış vergisinin genel muhasebeye nakledileceği ana hesapları belirtmek için bir **Genel muhasebe deftere nakil grubu** seçin.</span><span class="sxs-lookup"><span data-stu-id="74d62-112">Select a **Ledger posting group** to specify the main accounts to post sales tax to the general ledger.</span></span>
7. <span data-ttu-id="74d62-113">**Hesaplama** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="74d62-113">Expand the **Calculation** FastTab.</span></span> <span data-ttu-id="74d62-114">Burada, satış vergisi tutarlarının nasıl hesaplanacağını denetleyen birden çok alan vardır.</span><span class="sxs-lookup"><span data-stu-id="74d62-114">This includes multiple fields that control how sales tax amounts will be calculated.</span></span> <span data-ttu-id="74d62-115">Bu alanları gerektiği gibi doldurun.</span><span class="sxs-lookup"><span data-stu-id="74d62-115">Fill these fields out as needed.</span></span>  
8. <span data-ttu-id="74d62-116">Arabirimin üst kısmındaki **Eylem Bölmesinde**, **Satış vergisi kodunu** seçin.</span><span class="sxs-lookup"><span data-stu-id="74d62-116">On the **Action Pane** at the top of the interface, select **Sales tax code**.</span></span>
9. <span data-ttu-id="74d62-117">**Değerler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="74d62-117">Select **Values**.</span></span>
10. <span data-ttu-id="74d62-118">Bu vergi kodunun değerini **değer** sütununa girin.</span><span class="sxs-lookup"><span data-stu-id="74d62-118">Enter the value for this tax code in the **value** column.</span></span>
    - <span data-ttu-id="74d62-119">**Hesaplama** hızlı sekmesindeki Kaynak alanında Birim başına tutar seçiliyse, değer, hareketteki miktarla çarpılarak satış vergisi tutarı hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="74d62-119">On the **Calculation** FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="74d62-120">Vergi kodu birim tabanlı bir vergi değilse, değer, satış vergisi tutarını hesaplamak için bu vergi kodunun Kaynağına uygulanan yüzdedir.</span><span class="sxs-lookup"><span data-stu-id="74d62-120">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
11. <span data-ttu-id="74d62-121">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="74d62-121">Select **Save**.</span></span>
12. <span data-ttu-id="74d62-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="74d62-122">Close the page.</span></span>
13. <span data-ttu-id="74d62-123">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="74d62-123">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
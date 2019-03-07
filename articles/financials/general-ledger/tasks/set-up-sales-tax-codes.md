---
title: Satış vergisi kodlarını ayarla
description: Tüzel kişiliğin hesaplamak, tahsil etmek ve vergi dairelerine ödemekle yükümlü olduğu her dolaylı vergi ve harç için satış vergisi kodları oluşturulur.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f29442c2ef2e3d0008a74298fda218e4cbd93f8e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "349182"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="dbf83-103">Satış vergisi kodlarını ayarla</span><span class="sxs-lookup"><span data-stu-id="dbf83-103">Set up sales tax codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dbf83-104">Tüzel kişiliğin hesaplamak, tahsil etmek ve vergi dairelerine ödemekle yükümlü olduğu her dolaylı vergi ve harç için satış vergisi kodları oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="dbf83-104">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="dbf83-105">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="dbf83-105">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="dbf83-106">Vergi > Dolaylı vergiler > Satış vergisi > Satış vergisi kodları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="dbf83-106">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="dbf83-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dbf83-107">Click New.</span></span>
3. <span data-ttu-id="dbf83-108">Satış vergisi kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="dbf83-108">In the Sales tax code field, type a value.</span></span>
4. <span data-ttu-id="dbf83-109">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="dbf83-109">In the Name field, type a value.</span></span>
5. <span data-ttu-id="dbf83-110">Bu satış vergisinin hangi vergi dairesine, hangi aralıklarda bildirilip ödenmesi gerektiğini belirtmek üzere bir Kapatma dönemi seçin.</span><span class="sxs-lookup"><span data-stu-id="dbf83-110">Select a Settlement period to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="dbf83-111">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dbf83-111">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="dbf83-112">Satış vergisinin genel muhasebeye nakledileceği ana hesapları belirtmek için bir Genel muhasebe deftere nakil grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="dbf83-112">Select a Ledger posting group to specify the main accounts to post sales tax to the general ledger.</span></span>
8. <span data-ttu-id="dbf83-113">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="dbf83-113">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="dbf83-114">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dbf83-114">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="dbf83-115">Hesaplama hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="dbf83-115">Expand the Calculation FastTab.</span></span>
    * <span data-ttu-id="dbf83-116">Hesaplama hızlı sekmesinde, satış vergisi tutarlarının nasıl hesaplanacağını denetleyen birden çok alan vardır.</span><span class="sxs-lookup"><span data-stu-id="dbf83-116">The Calculation FastTab has multiple fields that control how sales tax amounts will be calculated.</span></span>  
11. <span data-ttu-id="dbf83-117">Eylem Bölmesinde, Satış vergisi kodu'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dbf83-117">On the Action Pane, click Sales tax code.</span></span>
12. <span data-ttu-id="dbf83-118">Değerler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dbf83-118">Click Values.</span></span>
13. <span data-ttu-id="dbf83-119">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="dbf83-119">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="dbf83-120">Bu vergi kodunun değerini girin.</span><span class="sxs-lookup"><span data-stu-id="dbf83-120">Enter the value for this tax code.</span></span>
    * <span data-ttu-id="dbf83-121">Hesaplama hızlı sekmesindeki Kaynak alanında Birim başına tutar seçiliyse, değer, hareketteki miktarla çarpılarak satış vergisi tutarı hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="dbf83-121">On the Calculation FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="dbf83-122">Vergi kodu birim tabanlı bir vergi değilse, değer, satış vergisi tutarını hesaplamak için bu vergi kodunun Kaynağına uygulanan yüzdedir.</span><span class="sxs-lookup"><span data-stu-id="dbf83-122">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
15. <span data-ttu-id="dbf83-123">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dbf83-123">Click Save.</span></span>
16. <span data-ttu-id="dbf83-124">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="dbf83-124">Close the page.</span></span>
17. <span data-ttu-id="dbf83-125">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dbf83-125">Click Save.</span></span>


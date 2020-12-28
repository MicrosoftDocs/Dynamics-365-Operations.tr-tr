---
title: Veri girişini kolaylaştırmak için bir kayıt şablonu oluşturma
description: Bu konu, sıklıkla kullanılan alan değerlerinin her yeni kayıt için açık olarak girilmesi gerekmeden bir kayıt şablonunun nasıl oluşturulacağını gösterir.
author: margoc
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68d3c7dd2f042617a7e2fcc8bee05fae6a82bde9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685230"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="e5871-103">Veri girişini kolaylaştırmak için bir kayıt şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="e5871-103">Create a record template to facilitate data entry</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e5871-104">Bu konu, sıklıkla kullanılan alan değerlerinin her yeni kayıt için açık olarak girilmesi gerekmeden bir kayıt şablonunun nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e5871-104">This topic demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="e5871-105">Bu yordamda, sabit kıymetlerinize eklenmesi gereken yeni dizüstü bilgisayarlar için yeni bir kayıt oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="e5871-105">In this procedure, you'll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="e5871-106">Bu yordamda, USMF örnek şirketi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e5871-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="e5871-107">Gezinti bölmesinde **Modüller > Sabit kıymetler > Sabit kıymetler > Sabit kıymetler günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e5871-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="e5871-108">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e5871-108">Select **New**.</span></span>
3. <span data-ttu-id="e5871-109">**Sabit kıymet grubu** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="e5871-109">In the **Fixed asset group** field, enter or select a value.</span></span>
4. <span data-ttu-id="e5871-110">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="e5871-110">In the **Name** field, type a value.</span></span> <span data-ttu-id="e5871-111">Örneğin, **Şirket lideri dizüstü bilgisayarı** yazın.</span><span class="sxs-lookup"><span data-stu-id="e5871-111">For example, enter **Corporate lead laptop**.</span></span>  
5. <span data-ttu-id="e5871-112">**Arama adı** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="e5871-112">In the **Search name** field, type a value.</span></span> <span data-ttu-id="e5871-113">Örneğin, **dizüstü bilgisayar** yazın.</span><span class="sxs-lookup"><span data-stu-id="e5871-113">For example, enter **laptop**.</span></span>  
6. <span data-ttu-id="e5871-114">**Teknik bilgi** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="e5871-114">Expand the **Technical information** section.</span></span>
7. <span data-ttu-id="e5871-115">**Yapım** bölümünde, **Model** ve **Model yılı** alanlarına değerleri yazın.</span><span class="sxs-lookup"><span data-stu-id="e5871-115">In the **Make**, **Model**, and **Model year** fields, type values.</span></span>
8. <span data-ttu-id="e5871-116">Eylem Bölmesinde, **Seçenekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e5871-116">On the Action Pane, select **Options**.</span></span>
9. <span data-ttu-id="e5871-117">**Kayıt bilgisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e5871-117">Select **Record info**.</span></span>
10. <span data-ttu-id="e5871-118">**Kullanıcı şablonu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="e5871-118">Select **User template**.</span></span>
11. <span data-ttu-id="e5871-119">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="e5871-119">In the **Name** field, type a value.</span></span>
12. <span data-ttu-id="e5871-120">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="e5871-120">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="e5871-121">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e5871-121">Select **OK**.</span></span>
14. <span data-ttu-id="e5871-122">**Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e5871-122">Select **Close**.</span></span>


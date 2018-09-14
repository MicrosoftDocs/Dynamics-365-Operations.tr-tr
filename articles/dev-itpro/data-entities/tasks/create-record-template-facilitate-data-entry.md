--- 
title: "Veri girişini kolaylaştırmak için bir kayıt şablonu oluşturma"
description: "Bu yordam, sıklıkla kullanılan alan değerlerinin her yeni kayıt için açık olarak girilmesi gerekmeden bir kayıt şablonunun nasıl oluşturulacağını gösterir."
author: margoc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 36d14c386322adab0cc0ba9b7b47c874aefbe519
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="37c3d-103">Veri girişini kolaylaştırmak için bir kayıt şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="37c3d-103">Create a record template to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="37c3d-104">Bu yordam, sıklıkla kullanılan alan değerlerinin her yeni kayıt için açık olarak girilmesi gerekmeden bir kayıt şablonunun nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="37c3d-104">This procedure demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="37c3d-105">Bu yordamda, sabit kıymetlerinize eklenmesi gereken yeni dizüstü bilgisayarlar için yeni bir kayıt oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="37c3d-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="37c3d-106">Bu yordamda, USMF örnek şirketi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="37c3d-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="37c3d-107">Sabit kıymetler > Sabit kıymetler > Sabit kıymetler menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="37c3d-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="37c3d-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="37c3d-108">Click New.</span></span>
3. <span data-ttu-id="37c3d-109">Sabit kıymet grubu alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="37c3d-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="37c3d-110">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="37c3d-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="37c3d-111">Örneğin, "Şirket lideri dizüstü bilgisayarı" yazın.</span><span class="sxs-lookup"><span data-stu-id="37c3d-111">For example, enter 'Corporate lead laptop'.</span></span>  
5. <span data-ttu-id="37c3d-112">Arama adı alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="37c3d-112">In the Search name field, type a value.</span></span>
    * <span data-ttu-id="37c3d-113">Örneğin, "dizüstü bilgisayar" yazın.</span><span class="sxs-lookup"><span data-stu-id="37c3d-113">For example, enter 'laptop.'</span></span>  
6. <span data-ttu-id="37c3d-114">Teknik bilgi bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="37c3d-114">Expand the Technical information section.</span></span>
7. <span data-ttu-id="37c3d-115">Marka alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="37c3d-115">In the Make field, type a value.</span></span>
8. <span data-ttu-id="37c3d-116">Model alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="37c3d-116">In the Model field, type a value.</span></span>
9. <span data-ttu-id="37c3d-117">Model yılı alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="37c3d-117">In the Model year field, type a value.</span></span>
10. <span data-ttu-id="37c3d-118">Eylem Bölmesinde, Seçenekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="37c3d-118">On the Action Pane, click Options.</span></span>
11. <span data-ttu-id="37c3d-119">Kayıt bilgileri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="37c3d-119">Click Record info.</span></span>
12. <span data-ttu-id="37c3d-120">Kullanıcı şablonu'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="37c3d-120">Click User template.</span></span>
13. <span data-ttu-id="37c3d-121">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="37c3d-121">In the Name field, type a value.</span></span>
    * <span data-ttu-id="37c3d-122">Örneğin, "Şirket dizüstü bilgisayarı" yazın.</span><span class="sxs-lookup"><span data-stu-id="37c3d-122">For example, enter 'Corporate laptop.'</span></span>  
14. <span data-ttu-id="37c3d-123">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="37c3d-123">In the Description field, type a value.</span></span>
    * <span data-ttu-id="37c3d-124">Örneğin, "Şirket dizüstü bilgisayarı" yazın.</span><span class="sxs-lookup"><span data-stu-id="37c3d-124">For example, enter 'Corporate laptop'.</span></span>  
15. <span data-ttu-id="37c3d-125">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="37c3d-125">Click OK.</span></span>
16. <span data-ttu-id="37c3d-126">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="37c3d-126">Click Close.</span></span>



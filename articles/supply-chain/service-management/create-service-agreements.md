---
title: Servis anlaşmaları oluşturma
description: Bu başlık, Servis yönetimi ve Proje yönetimi ile muhasebe modüllerinde servis sözleşmeleri oluşturmak için özelliklerin nasıl kullanılacağını açıklar.
author: ShylaThompson
manager: tfehr
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ef5ca8cc9c80581b9f7ef69bd8c4403d3d0296e8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965990"
---
# <a name="create-service-agreements"></a><span data-ttu-id="12b5b-103">Servis anlaşmaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="12b5b-103">Create service agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12b5b-104">Bu başlık, Servis yönetimi ve Proje yönetimi ile muhasebe modüllerinde servis sözleşmeleri oluşturmak için özelliklerin nasıl kullanılacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="12b5b-104">This topic describes how to use features in the Service management and the Project management and accounting modules to create service agreements.</span></span>

## <a name="create-a-service-agreement-from-service-management"></a><span data-ttu-id="12b5b-105">Servis yönetiminden servis sözleşmesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="12b5b-105">Create a service agreement from Service management</span></span>

1. <span data-ttu-id="12b5b-106">**Servis yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="12b5b-106">Navigate to **Service management**.</span></span>
2. <span data-ttu-id="12b5b-107">Sayfa başlığında yeni bir servis sözleşmesi oluşturmak için **Servis sözleşmeleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="12b5b-107">Click **Service agreements** to create a new service agreement line in the page header.</span></span> 
3. <span data-ttu-id="12b5b-108">**Yeni**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="12b5b-108">Click **New**.</span></span> <span data-ttu-id="12b5b-109">Açıklama girin, **Proje Kodu** alanındaki bir projeye yönelik bir referans seçin ve servis sözleşmesi için geri kalan alanları ve satırları doldurun.</span><span class="sxs-lookup"><span data-stu-id="12b5b-109">Enter a description, select a reference to a project in the **Project ID** field, and fill in the rest of the fields and lines for the service agreement.</span></span> <span data-ttu-id="12b5b-110">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="12b5b-110">Click **Save**.</span></span>
4. <span data-ttu-id="12b5b-111">Servis sözleşmesi için servis nesnesi ilişkileri veya servis görevi ilişkileri oluşturmak için **İlişkiler** sekmesinde, **Servis nesneleri**'ni veya **Servis görevleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="12b5b-111">On the **Relations** tab, select **Service objects** or **Service tasks** to create service object relations or service task relations for the service agreement.</span></span> <span data-ttu-id="12b5b-112">Kendilerine ait ilişkiler oluşturduğunuz servis nesneleri ve görevleri servis anlaşmasının satırlarına iliştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="12b5b-112">The service objects and tasks that you have created relations for can be attached on the lines of the service agreement.</span></span>
5. <span data-ttu-id="12b5b-113">Sayfanın alt yarısında, satırları bir servis şablonundan ya da başka bir servis sözleşmesinden kopyalayarak veya servis sözleşmesi satırlarını el ile oluşturarak servis sözleşmesi satırları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="12b5b-113">In the lower half of the page, create service agreement lines by copying lines from a service template, another service agreement, or manually creating the service-agreement lines.</span></span>

> [!NOTE]
> <span data-ttu-id="12b5b-114">Satırları servis sözleşmesine başka bir servis sözleşmesinden kopyalarsanız, servis nesnesi ve servis görevi ilişkilerini kopyalamayı isteyip istemediğinizi gösterebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12b5b-114">If you copy lines into the service agreement from another service agreement, you can indicate whether you also want to copy service object and service task relations.</span></span> <span data-ttu-id="12b5b-115">Bu ilişkileri kopyalarsanız, bunlar servis anlaşmasındaki mevcut ilişkilere eklenecektir.</span><span class="sxs-lookup"><span data-stu-id="12b5b-115">If you copy these relations, they are added to any existing relations on the service agreement.</span></span> <span data-ttu-id="12b5b-116">Servis anlaşması satırlarını bir servis şablonundan kopyalarsanız, servis nesnesi ve servis görevi ilişkileri otomatik olarak yeni servis anlaşması satırlarına servis nesnesi ilişkileri ve servis görevi ilişkileri olarak kopyalanacaktır.</span><span class="sxs-lookup"><span data-stu-id="12b5b-116">If you copy service-agreement lines from a service template, the service-object and service-task relations are automatically copied as service-object relations and service-task relations on the new service-agreement lines.</span></span>

## <a name="create-service-agreement-lines-manually"></a><span data-ttu-id="12b5b-117">Servis sözleşmesi satırlarını el ile oluşturma</span><span class="sxs-lookup"><span data-stu-id="12b5b-117">Create service agreement lines manually</span></span>

1. <span data-ttu-id="12b5b-118">**Service sözleşmeleri** sayfasından satır kılavuzundaki bir servis sözleşmesini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="12b5b-118">From the **Service agreements** page, add a service agreement line in the lines grid.</span></span> 
2. <span data-ttu-id="12b5b-119">Servis sözleşmesi satırı için uygun bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="12b5b-119">Enter the appropriate information for the service agreement line.</span></span> 
3. <span data-ttu-id="12b5b-120">Satırı kaydetmek için **CTRL+S** tuşlarına basın ve ardından sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="12b5b-120">Press **CTRL+S** to save the line, and then close the page.</span></span>

## <a name="create-a-service-agreement-from-project"></a><span data-ttu-id="12b5b-121">Proje'den bir servis anlaşması oluşturma</span><span class="sxs-lookup"><span data-stu-id="12b5b-121">Create a service agreement from Project</span></span>

1. <span data-ttu-id="12b5b-122">**Proje yönetimi ve muhasebe**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="12b5b-122">Click **Project management and accounting**.</span></span>
2. <span data-ttu-id="12b5b-123">**Tüm projeler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="12b5b-123">Click **All projects**.</span></span>
3. <span data-ttu-id="12b5b-124">Listeden projeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="12b5b-124">Select the project from the list.</span></span>
4. <span data-ttu-id="12b5b-125">**Eylem Bölmesi**'nde **Yönet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="12b5b-125">On the **Action Pane**, click **Manage**.</span></span> <span data-ttu-id="12b5b-126">**Yeni** Eylem grubunda **Servis**'e tıklayın ve **Servis sözleşmesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="12b5b-126">In the **New** Action group, click **Service** and select **Service agreement**.</span></span>
5. <span data-ttu-id="12b5b-127">Proje referansını girmek için bu konuda daha önce açıklandığı gibi **Servis sözleşmesi oluşturma** başlıklı bölümdeki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="12b5b-127">Follow the steps in the section titled **Create a service agreement** as described earlier in this topic to enter the project reference.</span></span>


## <a name="related-topics"></a><span data-ttu-id="12b5b-128">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="12b5b-128">Related topics</span></span>

[<span data-ttu-id="12b5b-129">Servis sözleşmeleri geliştirme ve oluşturmaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="12b5b-129">Develop and establish service agreements overview</span></span>](service-agreements.md)



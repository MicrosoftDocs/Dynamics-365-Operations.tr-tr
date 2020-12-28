---
title: Satıcı tasarımları arasında geçiş yapma
description: Bu konu Finance and Operations uygulamaları ile Dataverse arasında satıcı verisi tümleştirmesi arasında geçiş yapmayı açıklar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 731efd3ae841960f3a2c0b9be210c5c68ac835f5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685521"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="4f7a9-103">Satıcı tasarımları arasında geçiş yapma</span><span class="sxs-lookup"><span data-stu-id="4f7a9-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="4f7a9-104">Satıcı veri akışı</span><span class="sxs-lookup"><span data-stu-id="4f7a9-104">Vendor data flow</span></span> 

<span data-ttu-id="4f7a9-105">**Organizasyon** türünün satıcılarını depolamak için **firma** varlığını ve **kişi** türündeki satıcıları depolamak için ilgili **kişi** varlığını kullanmayı seçerseniz, aşağıdaki iş akışlarını konfigüre edin.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="4f7a9-106">Aksi takdirde, bu yapılandırmaya gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="4f7a9-107">Organizasyon türündeki satıcılar için genişletilmiş satıcı tasarımını kullan</span><span class="sxs-lookup"><span data-stu-id="4f7a9-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="4f7a9-108">**Dynamics365FinanceExtended** çözüm paketi aşağıdaki iş akışı işlem şablonlarını içerir.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="4f7a9-109">Her şablon için bir iş akışı oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="4f7a9-110">Hesaplar Tablosunda Satıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="4f7a9-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="4f7a9-111">Satıcılar Tablosunda Satıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="4f7a9-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="4f7a9-112">Hesaplar Tablosunda Satıcıları Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="4f7a9-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="4f7a9-113">Satıcılar Tablosunda Satıcıları Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="4f7a9-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="4f7a9-114">İş akışı işlem şablonlarını kullanarak yeni iş akışı işlemleri oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="4f7a9-115">**Satıcı** varlığı için bir iş akışı işlemi oluşturun ve **Hesaplar Tablosunda Satıcılar Oluşturma** iş akışı işlemi şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="4f7a9-116">Daha sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-116">Then select **OK**.</span></span> <span data-ttu-id="4f7a9-117">Bu iş akışı **Hesap** varlığı için satıcı oluşturma senaryosunu işler.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![Hesaplar Tablosunda Satıcılar Oluşturma iş akışı işlemi](media/create_process.png)

2. <span data-ttu-id="4f7a9-119">**Satıcı** varlığı için bir iş akışı işlemi oluşturun ve **Hesaplar Tablosunda Satıcıları Güncelleştirme** iş akışı işlemi şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="4f7a9-120">Daha sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-120">Then select **OK**.</span></span> <span data-ttu-id="4f7a9-121">Bu iş akışı **Hesap** varlığı için satıcı güncelleştirme senaryosunu işler.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="4f7a9-122">**Hesap** varlığı için bir iş akışı işlemi oluşturun ve **Satıcılar Tablosunda Satıcılar Oluşturma** iş akışı işlemi şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="4f7a9-123">**Hesap** varlığı için bir iş akışı işlemi oluşturun ve **Satıcılar Tablosunda Satıcıları Güncelleştirme** iş akışı işlemi şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="4f7a9-124">İş akışlarını gereksinimlerinize göre gerçek zamanlı iş akışları veya arka plan iş akışları olarak yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="4f7a9-125">Bir iş akışını arka plan iş akışı olarak konfigüre etmek için, **bir arka plan iş akışına dönüştür** ü seçin.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Arka plan iş akışına dönüştürme düğmesi](media/background_workflow.png)

6. <span data-ttu-id="4f7a9-127">**Kuruluş** türünde satıcılarla ilgili bilgileri depolamak üzere **Hesap** varlığını kullanmaya başlamak için **Hesap** ve **Satıcı** tablolarına yönelik olarak oluşturduğunuz iş akışlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="4f7a9-128">Kişi türündeki satıcılar için genişletilmiş satıcı tasarımını kullan</span><span class="sxs-lookup"><span data-stu-id="4f7a9-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="4f7a9-129">**Dynamics365FinanceExtended** çözüm paketi aşağıdaki iş akışı işlem şablonlarını içerir.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="4f7a9-130">Her şablon için bir iş akışı oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="4f7a9-131">Satıcılar Tablosunda Kişi türünde Satıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="4f7a9-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="4f7a9-132">İlgili Kişiler Tablosunda Kişi türünde Satıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="4f7a9-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="4f7a9-133">İlgili Kişiler Tablosunda Kişi türünde Satıcıları Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="4f7a9-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="4f7a9-134">Satıcılar Tablosunda Kişi türünde Satıcıları Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="4f7a9-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="4f7a9-135">İş akışı işlem şablonlarını kullanarak yeni iş akışı işlemleri oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="4f7a9-136">**Satıcı** varlığı için yeni bir iş akışı işlemi oluşturun ve **İlgili Kişiler Tablosunda Kişi türünde Satıcılar oluşturma** iş akışı işlemi şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="4f7a9-137">Daha sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-137">Then select **OK**.</span></span> <span data-ttu-id="4f7a9-138">Bu iş akışı **İlgili kişi** varlığı için satıcı oluşturma senaryosunu işler.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="4f7a9-139">**Satıcı** varlığı için yeni bir iş akışı işlemi oluşturun ve **İlgili Kişiler Tablosunda Kişi türünde Satıcıları güncelleştirme** iş akışı işlemi şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="4f7a9-140">Daha sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-140">Then select **OK**.</span></span> <span data-ttu-id="4f7a9-141">Bu iş akışı **İlgili kişi** varlığı için satıcı güncelleştirme senaryosunu işler.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="4f7a9-142">**İlgili Kişi** varlığı için bir iş akışı işlemi oluşturun ve **Satıcılar Tablosunda Kişi türünde Satıcılar oluşturma** şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="4f7a9-143">**İlgili Kişi** varlığı için bir iş akışı işlemi oluşturun ve **Satıcılar Tablosunda Kişi türünde Satıcıları güncelleştirme** şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="4f7a9-144">İş akışlarını gereksinimlerinize göre gerçek zamanlı iş akışları veya arka plan iş akışları olarak yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="4f7a9-145">Bir iş akışını arka plan iş akışı olarak konfigüre etmek için, **bir arka plan iş akışına dönüştür** ü seçin.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="4f7a9-146">**Kişi** türünde satıcılarla ilgili bilgileri depolamak üzere **İlgili Kişi** varlığını kullanmaya başlamak için **İlgili Kişi** ve **Satıcı** tablolarına yönelik olarak oluşturduğunuz iş akışlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="4f7a9-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>

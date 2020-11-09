---
title: Satıcı tasarımları arasında geçiş yapma
description: Bu konu Finance and Operations uygulamaları ile Common Data Service arasında satıcı verisi tümleştirmesi arasında geçiş yapmayı açıklar.
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
ms.openlocfilehash: 0ecc401706911f8b92146b95bb6415185df8b451
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997564"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="e5f31-103">Satıcı tasarımları arasında geçiş yapma</span><span class="sxs-lookup"><span data-stu-id="e5f31-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="e5f31-104">Satıcı veri akışı</span><span class="sxs-lookup"><span data-stu-id="e5f31-104">Vendor data flow</span></span> 

<span data-ttu-id="e5f31-105">**Organizasyon** türünün satıcılarını depolamak için **firma** varlığını ve **kişi** türündeki satıcıları depolamak için ilgili **kişi** varlığını kullanmayı seçerseniz, aşağıdaki iş akışlarını konfigüre edin.</span><span class="sxs-lookup"><span data-stu-id="e5f31-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="e5f31-106">Aksi takdirde, bu yapılandırmaya gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="e5f31-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="e5f31-107">Organizasyon türündeki satıcılar için genişletilmiş satıcı tasarımını kullan</span><span class="sxs-lookup"><span data-stu-id="e5f31-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="e5f31-108">**Dynamics365FinanceExtended** çözüm paketi aşağıdaki iş akışı işlem şablonlarını içerir.</span><span class="sxs-lookup"><span data-stu-id="e5f31-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="e5f31-109">Her şablon için bir iş akışı oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="e5f31-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="e5f31-110">Hesap Varlığında Satıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="e5f31-110">Create Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="e5f31-111">Satıcılar varlığında satıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="e5f31-111">Create Vendors in Vendors Entity</span></span>
+ <span data-ttu-id="e5f31-112">Hesap Varlığında Satıcılar güncelleme</span><span class="sxs-lookup"><span data-stu-id="e5f31-112">Update Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="e5f31-113">Satıcılar varlığında satıcılar güncelleme</span><span class="sxs-lookup"><span data-stu-id="e5f31-113">Update Vendors in Vendors Entity</span></span>

<span data-ttu-id="e5f31-114">İş akışı işlem şablonlarını kullanarak yeni iş akışı işlemleri oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e5f31-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="e5f31-115">**Hesap Varlığında Satıcılar Oluşturma** iş akışı işlemi şablonunu kullanarak **Satıcı** varlığı için yeni bir iş akışı işlemi oluşturun ve Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5f31-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="e5f31-116">Daha sonra **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e5f31-116">Then select **OK**.</span></span> <span data-ttu-id="e5f31-117">Bu iş akışı **Hesap** varlığı için satıcı oluşturma senaryosunu işler.</span><span class="sxs-lookup"><span data-stu-id="e5f31-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![Hesap Varlığında Satıcılar iş akışı süreci oluşturma](media/create_process.png)

2. <span data-ttu-id="e5f31-119">**Hesap Varlığında Satıcılar Güncelleme** iş akışı işlemi şablonunu kullanarak **Satıcı** varlığı için yeni bir iş akışı işlemi oluşturun ve Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5f31-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="e5f31-120">Daha sonra **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e5f31-120">Then select **OK**.</span></span> <span data-ttu-id="e5f31-121">Bu iş akışı **Hesap** varlığı için satıcı güncelleştirme senaryosunu işler.</span><span class="sxs-lookup"><span data-stu-id="e5f31-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="e5f31-122">**Satıcılar Varlığında Satıcılar Oluşturma** iş akışı işlemi şablonunu kullanarak **Firma** varlığı için yeni bir iş akışı işlemi oluşturun ve Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5f31-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Entity** workflow process template.</span></span>
4. <span data-ttu-id="e5f31-123">**Satıcılar Varlığında Satıcılar Güncelleme** iş akışı işlemi şablonunu kullanarak **Firma** varlığı için yeni bir iş akışı işlemi oluşturun ve Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5f31-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Entity** workflow process template.</span></span>
5. <span data-ttu-id="e5f31-124">İş akışlarını gereksinimlerinize göre gerçek zamanlı iş akışları veya arka plan iş akışları olarak yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5f31-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="e5f31-125">Bir iş akışını arka plan iş akışı olarak konfigüre etmek için, **bir arka plan iş akışına dönüştür** ü seçin.</span><span class="sxs-lookup"><span data-stu-id="e5f31-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Arka plan iş akışına dönüştürme düğmesi](media/background_workflow.png)

6. <span data-ttu-id="e5f31-127">**Kuruluş** türünün satıcı bilgilerini depolamak için **Firma** varlığını kullanmaya başlamak için **Firma** ve **Satıcı** varlıklarında oluşturduğunuz iş akışlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="e5f31-127">Activate the workflows that you created for the **Account** and **Vendor** entities to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="e5f31-128">Kişi türündeki satıcılar için genişletilmiş satıcı tasarımını kullan</span><span class="sxs-lookup"><span data-stu-id="e5f31-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="e5f31-129">**Dynamics365FinanceExtended** çözüm paketi aşağıdaki iş akışı işlem şablonlarını içerir.</span><span class="sxs-lookup"><span data-stu-id="e5f31-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="e5f31-130">Her şablon için bir iş akışı oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="e5f31-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="e5f31-131">Satıcı varlığındaki kişi türünden satıcılar oluştur</span><span class="sxs-lookup"><span data-stu-id="e5f31-131">Create Vendors of type Person in Vendors Entity</span></span>
+ <span data-ttu-id="e5f31-132">İlgili kişiler varlığındaki kişi türünden satıcılar oluştur</span><span class="sxs-lookup"><span data-stu-id="e5f31-132">Create Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="e5f31-133">İlgili kişiler varlığındaki kişi türünden satıcılar güncelle</span><span class="sxs-lookup"><span data-stu-id="e5f31-133">Update Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="e5f31-134">Satıcı varlığındaki kişi türünden satıcılar güncelle</span><span class="sxs-lookup"><span data-stu-id="e5f31-134">Update Vendors of type Person in Vendors Entity</span></span>

<span data-ttu-id="e5f31-135">İş akışı işlem şablonlarını kullanarak yeni iş akışı işlemleri oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e5f31-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="e5f31-136">**İlgili kişiler varlığındaki kişi türünden satıcılar oluştur** iş akışı işlemi şablonunu kullanarak **Satıcı** varlığı için yeni bir iş akışı işlemi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e5f31-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="e5f31-137">Daha sonra **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e5f31-137">Then select **OK**.</span></span> <span data-ttu-id="e5f31-138">Bu iş akışı **İlgili kişi** varlığı için satıcı oluşturma senaryosunu işler.</span><span class="sxs-lookup"><span data-stu-id="e5f31-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="e5f31-139">**İlgili kişiler varlığındaki kişi türünden satıcılar güncelle** iş akışı işlemi şablonunu kullanarak **Satıcı** varlığı için yeni bir iş akışı işlemi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e5f31-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="e5f31-140">Daha sonra **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e5f31-140">Then select **OK**.</span></span> <span data-ttu-id="e5f31-141">Bu iş akışı **İlgili kişi** varlığı için satıcı güncelleştirme senaryosunu işler.</span><span class="sxs-lookup"><span data-stu-id="e5f31-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="e5f31-142">**Satıcı varlığındaki kişi türünden satıcılar oluştur** iş akışı işlemi şablonunu kullanarak **İlgili kişi** varlığı için yeni bir iş akışı işlemi oluşturun ve Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5f31-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Entity** template.</span></span>
4. <span data-ttu-id="e5f31-143">**Satıcı varlığındaki kişi türünden satıcılar güncelle** iş akışı işlemi şablonunu kullanarak **İlgili kişi** varlığı için yeni bir iş akışı işlemi oluşturun ve Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5f31-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Entity** template.</span></span>
5. <span data-ttu-id="e5f31-144">İş akışlarını gereksinimlerinize göre gerçek zamanlı iş akışları veya arka plan iş akışları olarak yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5f31-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="e5f31-145">Bir iş akışını arka plan iş akışı olarak konfigüre etmek için, **bir arka plan iş akışına dönüştür** ü seçin.</span><span class="sxs-lookup"><span data-stu-id="e5f31-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="e5f31-146">**Kişi** türünün satıcı bilgilerini depolamak için **İlgili kişi** varlığını kullanmaya başlamak için **İlgili kişi** ve **Satıcı** varlıklarında oluşturduğunuz iş akışlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="e5f31-146">Activate the workflows that you created on the **Contact** and **Vendor** entities to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>

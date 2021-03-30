---
title: Kira içe aktarma çerçevesi üzerinden kiraları yönetme
description: Bu konu, aynı anda birden fazla kiralamayı düzeltmek için kiralama içe aktarma çerçevesinin nasıl kullanılacağını açıklar.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 90727e8624c8edb7cd9458089dd9d6dfaad67a7f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207243"
---
# <a name="manage-leases-through-the-lease-import-framework"></a><span data-ttu-id="418f7-103">Kira içe aktarma çerçevesi üzerinden kiraları yönetme</span><span class="sxs-lookup"><span data-stu-id="418f7-103">Manage leases through the Lease import framework</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="418f7-104">Bu konu, tek adımda birden fazla kiralamayı düzeltmek için kiralama içe aktarma çerçevesinin nasıl kullanılacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="418f7-104">This topic explains how to use the Lease import framework to adjust multiple leases in one step.</span></span> <span data-ttu-id="418f7-105">Bu özelliği kullanarak zamandan tasarruf edebilir ve insan hatası olasılığını azaltarak daha doğru düzeltmeler yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="418f7-105">By using this capability, you can save time, and you can also ensure more accurate adjustments by reducing the chance of human error.</span></span> <span data-ttu-id="418f7-106">Ek olarak, bu özellik Microsoft Dynamics 365 Finance'i dış veri varlıklarıyla bağlayarak verilerin etkili şekilde karşıya yüklenmesini sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="418f7-106">Additionally, this capability can connect Microsoft Dynamics 365 Finance with external data entities to efficiently upload data.</span></span>

<span data-ttu-id="418f7-107">Aşağıdaki veri varlıkları dış sistemlerle Varlık kiralamayı tümleştirmek için kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="418f7-107">The following data entities can be used to integrate Asset leasing with external systems:</span></span>

- <span data-ttu-id="418f7-108">Kiralama hazırlığı</span><span class="sxs-lookup"><span data-stu-id="418f7-108">Lease staging</span></span>
- <span data-ttu-id="418f7-109">Ödeme sözleşmesi hazırlığı</span><span class="sxs-lookup"><span data-stu-id="418f7-109">Payment contract staging</span></span>
- <span data-ttu-id="418f7-110">Yürütme sözleşmesi hazırlığı</span><span class="sxs-lookup"><span data-stu-id="418f7-110">Executory contract staging</span></span>

<span data-ttu-id="418f7-111">Bir kiralamayı düzeltmek, mali olmayan bilgileri güncelleştirmek ve yeni kiralamalar eklemek için içeri aktarma işlemini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="418f7-111">You can use the import process to adjust a lease, update non-financial information, or add new leases.</span></span> <span data-ttu-id="418f7-112">Kiralama verilerini içe aktarmadan önce görüntüleyebilir ve düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="418f7-112">You can view and edit the leasing data before you import it.</span></span>

<span data-ttu-id="418f7-113">Sistem, kira içe aktarma paketi aracılığıyla aşağıdaki üç işlemi çalıştırabilir.</span><span class="sxs-lookup"><span data-stu-id="418f7-113">The system can run the following three processes through the lease import suite.</span></span>

| <span data-ttu-id="418f7-114">İşlem türü</span><span class="sxs-lookup"><span data-stu-id="418f7-114">Process type</span></span>  | <span data-ttu-id="418f7-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="418f7-115">Description</span></span> |
|---------------|-------------|
| <span data-ttu-id="418f7-116">Kayıt ekleme</span><span class="sxs-lookup"><span data-stu-id="418f7-116">Add record</span></span>    | <span data-ttu-id="418f7-117">Bu işlem türüne sahip olan geçirilmiş kiralamalar sistemde kira oluşturur.</span><span class="sxs-lookup"><span data-stu-id="418f7-117">Migrated leases that have this process type create a lease in the system.</span></span> <span data-ttu-id="418f7-118">Ödeme planı el ile onaylanmalı ve ilk kabul günlük girişi geçiş sonrasında el ile deftere nakledilmelidir.</span><span class="sxs-lookup"><span data-stu-id="418f7-118">The payment schedule must be manually confirmed, and the initial recognition journal entry must be manually posted after the migration.</span></span> |
| <span data-ttu-id="418f7-119">Kaydı güncelleştir</span><span class="sxs-lookup"><span data-stu-id="418f7-119">Update record</span></span> | <span data-ttu-id="418f7-120">Bu işlem türüne sahip olan geçirilmiş kiralamalar, zaten sistemde bulunan bir kiralama için alan değerlerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="418f7-120">Migrated leases that have this process type update field values for a lease that is already in the system.</span></span> <span data-ttu-id="418f7-121">Yalnızca **Alanları güncelleştir seçimi** sayfasında seçilen alanlar güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="418f7-121">Only the fields that have been selected on the **Update fields selection** page are updated.</span></span> <span data-ttu-id="418f7-122">Bu işlem türü kiralamayı düzeltmediğinden, **Alanları güncelleştir seçimi** sayfasında mali olmayan alanları seçmeniz önerilir.</span><span class="sxs-lookup"><span data-stu-id="418f7-122">We recommended that you select non-financial fields on the **Update fields selection** page, because this process type doesn't adjust the lease.</span></span> |
| <span data-ttu-id="418f7-123">Kaydı düzelt</span><span class="sxs-lookup"><span data-stu-id="418f7-123">Adjust record</span></span> | <span data-ttu-id="418f7-124">Bu işlem türüne sahip olan geçirilmiş kiralamalar kiralamayı düzeltir.</span><span class="sxs-lookup"><span data-stu-id="418f7-124">Migrated leases that have this process type adjust the lease.</span></span> <span data-ttu-id="418f7-125">Bu düzeltme, kiralamada mali kiralama değişikliğine neden olur.</span><span class="sxs-lookup"><span data-stu-id="418f7-125">This adjustment causes a financial lease modification of the lease.</span></span> <span data-ttu-id="418f7-126">Kiralama işlendikten sonra sistem, kira içe aktarma paketindeki yeni verileri kullanarak yeni bir ödeme planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="418f7-126">After the lease is processed, the system creates a new payment schedule by using the new data from the lease import suite.</span></span> <span data-ttu-id="418f7-127">Sistem ödeme planını onaylamıyor veya düzeltme günlüğü girişini deftere nakletmiyor.</span><span class="sxs-lookup"><span data-stu-id="418f7-127">The system doesn't confirm the payment schedule or post the adjustment journal entry.</span></span> |

<span data-ttu-id="418f7-128">**Veri yönetimi** çalışma alanı üzerinden bilgi karşıya yüklendikten sonra, **Üst bilgiyi içeri aktar** sayfasını açın (**Varlık kiralama \> Kiralama içeri aktarma çerçevesi \> Üst bilgiyi içeri aktar**).</span><span class="sxs-lookup"><span data-stu-id="418f7-128">After information is uploaded through the **Data management** workspace, open the **Import header** page (**Asset leasing \> Lease import framework \> Import header**).</span></span> <span data-ttu-id="418f7-129">Bu sayfa, daha önce listelenen üç veri varlığının tüm içe aktarımlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="418f7-129">This page lists all imports of the three data entities that were listed earlier.</span></span>

<span data-ttu-id="418f7-130">İşlem çalıştırılmadan önce kiralama hazırlama verilerini görüntülemek için **Hazırlama verileri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="418f7-130">To view the lease staging data before processing is run, select **Staging data**.</span></span>

<span data-ttu-id="418f7-131">Karşılaştırma işlevi, içeri aktarmakta olduğunuz bir kaydı sisteminizde zaten olan ilgili kayıtla karşılaştırmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="418f7-131">The compare function lets you compare a record that you're importing with the corresponding record that's already in your system.</span></span> <span data-ttu-id="418f7-132">Tek bir kiralama kaydını karşılaştırmak için, bir kiralama seçin ve **Karşılaştır** ı seçin.</span><span class="sxs-lookup"><span data-stu-id="418f7-132">To compare an individual lease record, select a lease, and then select **Compare**.</span></span> <span data-ttu-id="418f7-133">Kiralama kayıtlarını geçirmeden önce bir **Farklar** raporu oluşturmak için bu adımı tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="418f7-133">You should complete this step to generate a **Differences** report before you migrate the lease records.</span></span> <span data-ttu-id="418f7-134">Karşılaştırma işlevi, hazırlama verileri içindeki değerleri, o anda sistemde bulunan kiralamaların değerleriyle karşılaştırır.</span><span class="sxs-lookup"><span data-stu-id="418f7-134">The Compare functionality compares the values in the staging data to the values for leases that are currently in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="418f7-135">Karşılaştırma işlevi, **Kayıt ekleme** işlem türüne sahip kiralamalarla karşılaştırılacak bir öğe olmadığından bunlar için çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="418f7-135">The Compare functionality doesn't work for leases that have the **Add record** process type, because there is nothing to compare against that lease.</span></span>
>
> <span data-ttu-id="418f7-136">Aynı anda birden fazla kiralamayı karşılaştırmak için **Varlık kiralama \> Kiralama içeri aktarma çerçevesi \> Periyodik \> Karşılaştır** bölümüne gidin ve **Karşılaştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="418f7-136">To compare multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Compare**, and select **Compare**.</span></span>

<span data-ttu-id="418f7-137">Her bir varlık için, şu anda sistemdekiler ve hazırlama tablolarındakiler arasındaki farkları görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="418f7-137">For each entity, you can view the differences between what is currently in the system and what is in the staging tables.</span></span> <span data-ttu-id="418f7-138">Hazırlama tablolarındaki her bir varlık için **Farklılıkları göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="418f7-138">For each entity in the staging tables, select **See differences**.</span></span> <span data-ttu-id="418f7-139">Açılan iletişim kutusunda geçerli değer ve önerilen hazırlama değeri gösterilir.</span><span class="sxs-lookup"><span data-stu-id="418f7-139">The dialog box that appears shows the current value and the proposed staging value.</span></span>

<span data-ttu-id="418f7-140">**Yeni Değer** sütununda değiştirerek ve ardından **Hazırlamayı güncelleştir**'i seçerek hazırlama değerini de değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="418f7-140">You can also update the staging value by changing it in the **New Value** column and then selecting **Update staging**.</span></span>

<span data-ttu-id="418f7-141">Tüm kayıtların hata vermeden sisteme getirilmesini sağlamak için kiralamaları doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="418f7-141">You can validate leases to ensure that the records can be brought into the system without introducing errors.</span></span> <span data-ttu-id="418f7-142">Kiralama kaydı geçirilmeden önce, sistem kaydın başarıyla içeri aktarıldığından emin olmak için birkaç doğrulama çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="418f7-142">Before a lease record is migrated, the system runs several validations to ensure that the record will be successfully imported.</span></span> <span data-ttu-id="418f7-143">Tek bir kirayı doğrulamak için **Doğrula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="418f7-143">To validate an individual lease, select **Validate**.</span></span>

> [!NOTE]
> <span data-ttu-id="418f7-144">Aynı anda birden fazla kiralamayı doğrulamak için **Varlık kiralama \> Kiralama içeri aktarma çerçevesi \> Periyodik \> Doğrula** bölümüne gidin ve **Karşılaştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="418f7-144">To validate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Validate**, and select **Compare**.</span></span>

<span data-ttu-id="418f7-145">Tek bir kirayı işlemek için **Üst bilgiyi içeri aktar** sayfasında **Kiralama kayıtlarını geçir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="418f7-145">To process an individual lease, select **Migrate lease records** on the **Import header** page.</span></span> <span data-ttu-id="418f7-146">Bir kiralama geçirildiğinde sistem, **İşlem türü** alanında belirtilen işlemi gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="418f7-146">When a lease is migrated, the system performs the action that is specified in the **Process type** field.</span></span>

> [!NOTE]
> <span data-ttu-id="418f7-147">Aynı anda birden fazla kiralamayı doğrulamak için **Varlık kiralama \> Kiralama içeri aktarma çerçevesi \> Periyodik \> Doğrula** bölümüne gidin ve **Karşılaştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="418f7-147">To validate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Validate**, and select **Compare**.</span></span>

<span data-ttu-id="418f7-148">Kiralamalar karşılaştırıldıktan sonra, içeri aktarma kimliğine dahil edilen her kiralama için farkları görüntülemek amacıyla bir rapor çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="418f7-148">After the leases are compared, you can run a report to view the differences for each lease that is included in the import ID.</span></span> <span data-ttu-id="418f7-149">Raporu bir kiralama için çalıştırmak istiyorsanız hazırlama verilerinde bu kiralamayı seçin ve ardından **Karşılaştır ve raporu görüntüle \> Farklar raporu** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="418f7-149">To run the report for one lease, select that lease in the staging data, and then select **Compare and view report \> Differences report**.</span></span>

> [!NOTE]
> <span data-ttu-id="418f7-150">Aynı anda birden fazla kiralamayı doğrulamak için **Varlık kiralama \> Sorgular ve raporlar \> Farklar raporu** bölümüne gidin ve **Karşılaştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="418f7-150">To validate multiple leases at the same time, go to **Asset leasing \> Inquiries and reports \> Differences report**, and select **Compare**.</span></span>

## <a name="set-up-update-fields"></a><span data-ttu-id="418f7-151">Güncelleştirme alanlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="418f7-151">Set up update fields</span></span>

<span data-ttu-id="418f7-152">Kiralama içeri aktarma çerçevesini, kiraları güncelleştirmek için kullanıyorsanız ve işlem türü **Kaydı güncelleştir** ise, güncelleştirilecek belirli alanları seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="418f7-152">If you're using the Lease import framework to update leases, and the process type is **Update record**, you can select specific fields to update.</span></span>

1. <span data-ttu-id="418f7-153">**Varlık Kiralama \> Kiralama içeri aktarma çerçevesi \> Kurulum \> Alanı güncelleştir seçimi** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="418f7-153">Go to **Asset leasing \> Lease import framework \> Setup \> Update field selection**.</span></span>
2. <span data-ttu-id="418f7-154">Görüntülenen sayfada güncelleştirilecek alanları seçin ve sonra bunları **Seçili alanlar** listesine taşımak için yeşil oku seçin.</span><span class="sxs-lookup"><span data-stu-id="418f7-154">On the page that appears, select the fields to update, and then select the green arrow to move them to the **Selected fields** list.</span></span> <span data-ttu-id="418f7-155">Yalnızca **Seçili alanlar** listesindeki alanlar kira içeri aktarma paketi kullanılarak güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="418f7-155">Only fields in the **Selected fields** list can be updated by using the lease import suite.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
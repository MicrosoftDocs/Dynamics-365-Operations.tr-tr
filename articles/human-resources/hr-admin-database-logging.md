---
title: Veritabanı günlüğü yapılandırma ve yönetme
description: Veritabanı günlükleri ile Dynamics 365 Human Resources'taki tablo ve alanlardaki değişiklikleri izleyebilirsiniz.
author: Darinkramer
manager: AnnBe
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3dc4658a0a13af95978c66f5aab882902f754a2d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420936"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="21d6f-103">Veritabanı günlüğü yapılandırma ve yönetme</span><span class="sxs-lookup"><span data-stu-id="21d6f-103">Configure and manage database logging</span></span>

<span data-ttu-id="21d6f-104">Veritabanı günlükleri ile Dynamics 365 Human Resources'taki tablo ve alanlardaki değişiklikleri izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="21d6f-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="21d6f-105">Bu konuda, aşağıdakilerin nasıl yapılacağı açıklanmaktadır:</span><span class="sxs-lookup"><span data-stu-id="21d6f-105">This topic describes how to:</span></span>

- <span data-ttu-id="21d6f-106">Veritabanı günlükleri için güvenlik ve performansı yönetme</span><span class="sxs-lookup"><span data-stu-id="21d6f-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="21d6f-107">Veritabanı günlüğe kayıt ayarla</span><span class="sxs-lookup"><span data-stu-id="21d6f-107">Set up database logging</span></span>
- <span data-ttu-id="21d6f-108">Veritabanı günlüklerini temizleme</span><span class="sxs-lookup"><span data-stu-id="21d6f-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="21d6f-109">Veritabanı günlüklerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="21d6f-109">Overview of database logging</span></span>

<span data-ttu-id="21d6f-110">Veritabanı günlükleri Microsoft Dynamics 365 Human Resources'taki tablo ve alanlarda yapılan belirli değişiklikleri izler.</span><span class="sxs-lookup"><span data-stu-id="21d6f-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="21d6f-111">Bu değişiklikler ekleme, güncelleştirme veya silmeyi içerir.</span><span class="sxs-lookup"><span data-stu-id="21d6f-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="21d6f-112">Veritabanı günlükleri, veritabanı günlüğü tablosundaki tablo veya alanlardaki değişikliklerin kaydını depolar.</span><span class="sxs-lookup"><span data-stu-id="21d6f-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="21d6f-113">Veritabanı günlüğünün iş için kullanımı şunları içerir:</span><span class="sxs-lookup"><span data-stu-id="21d6f-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="21d6f-114">Hassas bilgiler içeren belirli tablolardaki değişikliklerin denetim kaydını oluşturmak.</span><span class="sxs-lookup"><span data-stu-id="21d6f-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="21d6f-115">Tek hareketleri izlemek.</span><span class="sxs-lookup"><span data-stu-id="21d6f-115">Tracking single transactions.</span></span> <span data-ttu-id="21d6f-116">Veritabanı günlükleri toplu işlemlerde çalışan otomatik hareketleri izlemek için tasarlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="21d6f-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="21d6f-117">Veritabanı günlükleri için güvenlik</span><span class="sxs-lookup"><span data-stu-id="21d6f-117">Security for database logging</span></span>

<span data-ttu-id="21d6f-118">Veritabanı günlükleri hassas veriler içerebilir.</span><span class="sxs-lookup"><span data-stu-id="21d6f-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="21d6f-119">Erişimi yalnızca günlük verisine erişmesi gereken güvenlik rollerini içerecek şekilde sınırlayın.</span><span class="sxs-lookup"><span data-stu-id="21d6f-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="21d6f-120">Veritabanı günlüğü ve performansı</span><span class="sxs-lookup"><span data-stu-id="21d6f-120">Database logging and performance</span></span>

<span data-ttu-id="21d6f-121">İş açısından bakıldığında çok değerli olmasına karşın, veritabanı günlükleri kaynak kullanımı ve yönetimi açısından pahalı olabilir.</span><span class="sxs-lookup"><span data-stu-id="21d6f-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="21d6f-122">Veritabanı günlüğünün performans etkileri şunları içerir:</span><span class="sxs-lookup"><span data-stu-id="21d6f-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="21d6f-123">Veritabanı günlüğü tablosu hızlı bir şekilde büyüyebilir ve veritabanı boyutunun artmasına neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="21d6f-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="21d6f-124">Büyüme, korumak istediğiniz günlüğe kaydedilmiş veri miktarına bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="21d6f-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="21d6f-125">Varsayılan olarak, veritabanı günlüğü tablosu yalnızca 30 günlük verilerini korur.</span><span class="sxs-lookup"><span data-stu-id="21d6f-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="21d6f-126">Veritabanı günlükleri uzun süre çalışan veri içe aktarma işlemleri gibi uzun süren otomatikleştirilmiş işlemleri olumsuz etkileyebilir.</span><span class="sxs-lookup"><span data-stu-id="21d6f-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="21d6f-127">Önerilen yöntemler</span><span class="sxs-lookup"><span data-stu-id="21d6f-127">Best practices</span></span>

<span data-ttu-id="21d6f-128">Performansı artırmak için, tabloların tamamı yerine günlüğe kaydedilecek belirli alanları seçerek günlük girişlerini sınırlayın.</span><span class="sxs-lookup"><span data-stu-id="21d6f-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="21d6f-129">Genel performansın sürdürülmesine yardımcı olmak için, veritabanı günlüğü kaydı 20 tabloyla sınırlıdır.</span><span class="sxs-lookup"><span data-stu-id="21d6f-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="21d6f-130">Tek tek alanlar için yalnızca güncelleştirmeler günlüğe kaydedilebilir.</span><span class="sxs-lookup"><span data-stu-id="21d6f-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="21d6f-131">Veritabanı günlüğe kayıt ayarla</span><span class="sxs-lookup"><span data-stu-id="21d6f-131">Set up database logging</span></span>

<span data-ttu-id="21d6f-132">Veritabanı günlüğü kaydını ayarlamak için **Veritabanı değişikliklerini günlüğe kaydetme** sihirbazını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="21d6f-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="21d6f-133">Sihirbaz, tablolar veya alanların günlüğe kaydedilmesini ayarlamak için esnek bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="21d6f-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="21d6f-134">**Sistem yönetimi > Bağlantılar > Veritabanı > Veritabanı günlükleri kurulumu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="21d6f-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="21d6f-135">**Veri tabanı değişikliklerini günlüğe kaydetme** sihirbazında **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="21d6f-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="21d6f-136">Sihirbazı tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="21d6f-136">Complete the wizard.</span></span>

## <a name="clean-up-database-logs"></a><span data-ttu-id="21d6f-137">Veritabanı günlüklerini temizleme</span><span class="sxs-lookup"><span data-stu-id="21d6f-137">Clean up database logs</span></span>

<span data-ttu-id="21d6f-138">Veritabanı günlüklerinin tümünü veya bir bölümünü aşağıdaki seçenekleri kullanarak silebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="21d6f-138">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="21d6f-139">Belirli bir tabloya ait tüm günlükleri seçin.</span><span class="sxs-lookup"><span data-stu-id="21d6f-139">Select all logs for a particular table.</span></span>
- <span data-ttu-id="21d6f-140">Belirli veritabanı günlüğü türlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="21d6f-140">Select specific types of database log.</span></span>
- <span data-ttu-id="21d6f-141">Günlüğün oluşturulduğu tarih ve saati seçin.</span><span class="sxs-lookup"><span data-stu-id="21d6f-141">Select a date and time that a log was created.</span></span>

<span data-ttu-id="21d6f-142">Veritabanı günlüğü temizleme işlemi ayarlamak için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="21d6f-142">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="21d6f-143">**Sistem yönetimi > Bağlantılar > Veritabanı > Veritabanı günlükleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="21d6f-143">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="21d6f-144">**Günlüğü temizle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="21d6f-144">Select **Clean up log**.</span></span>

2. <span data-ttu-id="21d6f-145">Aşağıdaki seçeneklerden birini girerek, günlükleri silmek üzere seçebileceğiniz bir yöntem seçin:</span><span class="sxs-lookup"><span data-stu-id="21d6f-145">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="21d6f-146">Tablo ID</span><span class="sxs-lookup"><span data-stu-id="21d6f-146">Table ID</span></span>
   - <span data-ttu-id="21d6f-147">Günlük türü</span><span class="sxs-lookup"><span data-stu-id="21d6f-147">Type of log</span></span>
   - <span data-ttu-id="21d6f-148">Oluşturma tarihi ve saati</span><span class="sxs-lookup"><span data-stu-id="21d6f-148">Created date and time</span></span>

3. <span data-ttu-id="21d6f-149">Günlük temizleme görevinin ne zaman çalıştırılacağını belirlemek için **Veritabanı günlüklerini temizleme** sekmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="21d6f-149">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="21d6f-150">Varsayılan olarak, veritabanı günlükleri 30 gün süreyle kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="21d6f-150">By default, database logs are available for 30 days.</span></span>

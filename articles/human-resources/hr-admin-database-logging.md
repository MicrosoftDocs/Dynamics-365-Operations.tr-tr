---
title: Veritabanı günlüğü yapılandırma ve yönetme
description: Veritabanı günlükleri ile Dynamics 365 Human Resources'taki tablo ve alanlardaki değişiklikleri izleyebilirsiniz.
author: andreabichsel
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d22ff9f3ce68c81f37840342c795d7d162eb027b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801347"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="e340a-103">Veritabanı günlüğü yapılandırma ve yönetme</span><span class="sxs-lookup"><span data-stu-id="e340a-103">Configure and manage database logging</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e340a-104">Veritabanı günlükleri ile Dynamics 365 Human Resources'taki tablo ve alanlardaki değişiklikleri izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e340a-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="e340a-105">Bu konuda, aşağıdakilerin nasıl yapılacağı açıklanmaktadır:</span><span class="sxs-lookup"><span data-stu-id="e340a-105">This topic describes how to:</span></span>

- <span data-ttu-id="e340a-106">Veritabanı günlükleri için güvenlik ve performansı yönetme</span><span class="sxs-lookup"><span data-stu-id="e340a-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="e340a-107">Veritabanı günlüğe kayıt ayarla</span><span class="sxs-lookup"><span data-stu-id="e340a-107">Set up database logging</span></span>
- <span data-ttu-id="e340a-108">Veritabanı günlüklerini temizleme</span><span class="sxs-lookup"><span data-stu-id="e340a-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="e340a-109">Veritabanı günlüklerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="e340a-109">Overview of database logging</span></span>

<span data-ttu-id="e340a-110">Veritabanı günlükleri Microsoft Dynamics 365 Human Resources'taki tablo ve alanlarda yapılan belirli değişiklikleri izler.</span><span class="sxs-lookup"><span data-stu-id="e340a-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="e340a-111">Bu değişiklikler ekleme, güncelleştirme veya silmeyi içerir.</span><span class="sxs-lookup"><span data-stu-id="e340a-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="e340a-112">Veritabanı günlükleri, veritabanı günlüğü tablosundaki tablo veya alanlardaki değişikliklerin kaydını depolar.</span><span class="sxs-lookup"><span data-stu-id="e340a-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="e340a-113">Veritabanı günlüğünün iş için kullanımı şunları içerir:</span><span class="sxs-lookup"><span data-stu-id="e340a-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="e340a-114">Hassas bilgiler içeren belirli tablolardaki değişikliklerin denetim kaydını oluşturmak.</span><span class="sxs-lookup"><span data-stu-id="e340a-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="e340a-115">Tek hareketleri izlemek.</span><span class="sxs-lookup"><span data-stu-id="e340a-115">Tracking single transactions.</span></span> <span data-ttu-id="e340a-116">Veritabanı günlükleri toplu işlemlerde çalışan otomatik hareketleri izlemek için tasarlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="e340a-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="e340a-117">Veritabanı günlükleri için güvenlik</span><span class="sxs-lookup"><span data-stu-id="e340a-117">Security for database logging</span></span>

<span data-ttu-id="e340a-118">Veritabanı günlükleri hassas veriler içerebilir.</span><span class="sxs-lookup"><span data-stu-id="e340a-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="e340a-119">Erişimi yalnızca günlük verisine erişmesi gereken güvenlik rollerini içerecek şekilde sınırlayın.</span><span class="sxs-lookup"><span data-stu-id="e340a-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="e340a-120">Veritabanı günlüğü ve performansı</span><span class="sxs-lookup"><span data-stu-id="e340a-120">Database logging and performance</span></span>

<span data-ttu-id="e340a-121">İş açısından bakıldığında çok değerli olmasına karşın, veritabanı günlükleri kaynak kullanımı ve yönetimi açısından pahalı olabilir.</span><span class="sxs-lookup"><span data-stu-id="e340a-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="e340a-122">Veritabanı günlüğünün performans etkileri şunları içerir:</span><span class="sxs-lookup"><span data-stu-id="e340a-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="e340a-123">Veritabanı günlüğü tablosu hızlı bir şekilde büyüyebilir ve veritabanı boyutunun artmasına neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="e340a-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="e340a-124">Büyüme, korumak istediğiniz günlüğe kaydedilmiş veri miktarına bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e340a-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="e340a-125">Varsayılan olarak, veritabanı günlüğü tablosu yalnızca 30 günlük verilerini korur.</span><span class="sxs-lookup"><span data-stu-id="e340a-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="e340a-126">Veritabanı günlükleri uzun süre çalışan veri içe aktarma işlemleri gibi uzun süren otomatikleştirilmiş işlemleri olumsuz etkileyebilir.</span><span class="sxs-lookup"><span data-stu-id="e340a-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="e340a-127">Önerilen yöntemler</span><span class="sxs-lookup"><span data-stu-id="e340a-127">Best practices</span></span>

<span data-ttu-id="e340a-128">Performansı artırmak için, tabloların tamamı yerine günlüğe kaydedilecek belirli alanları seçerek günlük girişlerini sınırlayın.</span><span class="sxs-lookup"><span data-stu-id="e340a-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="e340a-129">Genel performansın sürdürülmesine yardımcı olmak için, veritabanı günlüğü kaydı 20 tabloyla sınırlıdır.</span><span class="sxs-lookup"><span data-stu-id="e340a-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="e340a-130">Tek tek alanlar için yalnızca güncelleştirmeler günlüğe kaydedilebilir.</span><span class="sxs-lookup"><span data-stu-id="e340a-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="e340a-131">Veritabanı günlüğe kayıt ayarla</span><span class="sxs-lookup"><span data-stu-id="e340a-131">Set up database logging</span></span>

<span data-ttu-id="e340a-132">Veritabanı günlüğü kaydını ayarlamak için **Veritabanı değişikliklerini günlüğe kaydetme** sihirbazını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e340a-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="e340a-133">Sihirbaz, tablolar veya alanların günlüğe kaydedilmesini ayarlamak için esnek bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="e340a-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="e340a-134">**Sistem yönetimi > Bağlantılar > Veritabanı > Veritabanı günlükleri kurulumu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="e340a-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="e340a-135">**Veri tabanı değişikliklerini günlüğe kaydetme** sihirbazında **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e340a-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="e340a-136">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e340a-136">Select **Next**.</span></span> 
3. <span data-ttu-id="e340a-137">Sihirbazın **tablolar ve alanlar** sayfasında, veritabanı günlüğünü etkinleştirmek istediğiniz tablo ve alanları seçin ve **ileri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e340a-137">On the **Tables and fields** page of the wizard, select the the tables and fields on which you want to enable database logging, and select **Next**.</span></span>

   > [!Note]
   > <span data-ttu-id="e340a-138">Human Resources veritabanındaki tüm tablolarda Veritabanı günlükleri kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="e340a-138">Database logging is not available on all tables in the Human Resources database.</span></span> <span data-ttu-id="e340a-139">Listenin altındaki **tüm tabloları göster** seçilmesi veritabanı günlüğünün bulunduğu tüm veritabanı tablolarını göstermek için tablo ve alanların listesini genişletir, ancak bu, veritabanı tablolarının tam listesinin bir alt kümesi olacaktır.</span><span class="sxs-lookup"><span data-stu-id="e340a-139">Selecting **Show all tables** below the list expands the list of tables and fields to show all database tables for which database logging is available, but this will be a subset of the full list of database tables.</span></span>

4. <span data-ttu-id="e340a-140">Sihirbazın **değişiklik türleri** sayfasında, tabloların ve alanların her biri için değişiklikleri izlemek istediğiniz veri işlemlerini seçin ve **ileri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e340a-140">On the **Types of change** page of the wizard, select the data operations for which you want to track changes for each of the tables and fields, and select **Next**.</span></span> <span data-ttu-id="e340a-141">Günlüğe kaydetmek için mevcut olan veri işlemlerinin açıklaması için aşağıdaki tabloya bakın.</span><span class="sxs-lookup"><span data-stu-id="e340a-141">See the table below for a description of the data operations that are available for logging.</span></span>
5. <span data-ttu-id="e340a-142">**Sonlandır** sayfasında yapılacak değişiklikleri gözden geçirin ve **Sonlandır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e340a-142">On the **Finish** page, review the changes that will be made, and select **Finish**.</span></span>

| <span data-ttu-id="e340a-143">Operasyon</span><span class="sxs-lookup"><span data-stu-id="e340a-143">Operation</span></span> | <span data-ttu-id="e340a-144">Tanım</span><span class="sxs-lookup"><span data-stu-id="e340a-144">Description</span></span> |
| -- | -- |
| <span data-ttu-id="e340a-145">Yeni hareketleri izle</span><span class="sxs-lookup"><span data-stu-id="e340a-145">Track new transactions</span></span> | <span data-ttu-id="e340a-146">Tabloda oluşturulan yeni kayıtlar için bir günlük oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e340a-146">Create a log for new records that are created in the table.</span></span> |
| <span data-ttu-id="e340a-147">Güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e340a-147">Update</span></span> | <span data-ttu-id="e340a-148">Tablo kayıtlarında yapılan güncelleştirmeler veya tablodaki seçili alanlara yapılan güncelleştirmeler için bir günlük oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e340a-148">Create a log for updates to table records, or updates to individually selected fields in the table.</span></span> <span data-ttu-id="e340a-149">Tablo için güncelleştirmeleri günlüğe kaydetmeyi seçerseniz, tabloda herhangi bir kaydın herhangi bir alanı üzerinde her güncelleştirme yapıldığında bir günlük kaydı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e340a-149">If you select to log updates for the table, then a log record is created each time an update is made to any field of any record on the table.</span></span> <span data-ttu-id="e340a-150">Belirli alanların güncelleştirmelerini günlüğe kaydetmeyi seçerseniz, yalnızca tablo kayıtlarının bu alanlarında güncelleştirmeler yapıldığında bir günlük kaydı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e340a-150">If you select to log updates for specific fields, then a log record is created only when updates are made to those fields of table records.</span></span> |
| <span data-ttu-id="e340a-151">Delete</span><span class="sxs-lookup"><span data-stu-id="e340a-151">Delete</span></span> | <span data-ttu-id="e340a-152">Tablodan silinen kayıtlar için bir günlük oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e340a-152">Create a log for records deleted from the table.</span></span> |
| <span data-ttu-id="e340a-153">Yeniden adlandırma anahtarı</span><span class="sxs-lookup"><span data-stu-id="e340a-153">Rename key</span></span> | <span data-ttu-id="e340a-154">Bir tablo anahtarı yeniden adlandırıldığında, bir günlük kaydı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e340a-154">Create a log record when a table key is renamed.</span></span> |


## <a name="clean-up-database-logs"></a><span data-ttu-id="e340a-155">Veritabanı günlüklerini temizleme</span><span class="sxs-lookup"><span data-stu-id="e340a-155">Clean up database logs</span></span>

<span data-ttu-id="e340a-156">Veritabanı günlüklerinin tümünü veya bir bölümünü aşağıdaki seçenekleri kullanarak silebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="e340a-156">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="e340a-157">Belirli bir tabloya ait tüm günlükleri seçin.</span><span class="sxs-lookup"><span data-stu-id="e340a-157">Select all logs for a particular table.</span></span>
- <span data-ttu-id="e340a-158">Belirli veritabanı günlüğü türlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="e340a-158">Select specific types of database log.</span></span>
- <span data-ttu-id="e340a-159">Günlüğün oluşturulduğu tarih ve saati seçin.</span><span class="sxs-lookup"><span data-stu-id="e340a-159">Select a date and time that a log was created.</span></span>

<span data-ttu-id="e340a-160">Veritabanı günlüğü temizleme işlemi ayarlamak için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="e340a-160">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="e340a-161">**Sistem yönetimi > Bağlantılar > Veritabanı > Veritabanı günlükleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e340a-161">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="e340a-162">**Günlüğü temizle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e340a-162">Select **Clean up log**.</span></span>

2. <span data-ttu-id="e340a-163">Aşağıdaki seçeneklerden birini girerek, günlükleri silmek üzere seçebileceğiniz bir yöntem seçin:</span><span class="sxs-lookup"><span data-stu-id="e340a-163">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="e340a-164">Tablo ID</span><span class="sxs-lookup"><span data-stu-id="e340a-164">Table ID</span></span>
   - <span data-ttu-id="e340a-165">Günlük türü</span><span class="sxs-lookup"><span data-stu-id="e340a-165">Type of log</span></span>
   - <span data-ttu-id="e340a-166">Oluşturma tarihi ve saati</span><span class="sxs-lookup"><span data-stu-id="e340a-166">Created date and time</span></span>

3. <span data-ttu-id="e340a-167">Günlük temizleme görevinin ne zaman çalıştırılacağını belirlemek için **Veritabanı günlüklerini temizleme** sekmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e340a-167">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="e340a-168">Varsayılan olarak, veritabanı günlükleri 30 gün süreyle kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e340a-168">By default, database logs are available for 30 days.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

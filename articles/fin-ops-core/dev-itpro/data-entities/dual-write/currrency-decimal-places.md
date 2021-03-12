---
title: Çift yazma için para birimi veri türü geçişi
description: Bu konu, çift yazmanın para birimi için desteklediği ondalık basamak sayısının nasıl değiştirileceğini açıklamaktadır.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 04/06/2020
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
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 5d39bf28dba951a1483412d967c8c6fc6dbcc610
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744387"
---
# <a name="currency-data-type-migration-for-dual-write"></a><span data-ttu-id="ea477-103">Çift yazma için para birimi veri türü geçişi</span><span class="sxs-lookup"><span data-stu-id="ea477-103">Currency data-type migration for dual-write</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ea477-104">Para birimi değerleri için desteklenen ondalık basamak sayısını en fazla 10'a artırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea477-104">You can increase the number of decimal places that are supported for currency values to a maximum of 10.</span></span> <span data-ttu-id="ea477-105">Varsayılan sınır dört ondalık haneye sahiptir.</span><span class="sxs-lookup"><span data-stu-id="ea477-105">The default limit is four decimal places.</span></span> <span data-ttu-id="ea477-106">Ondalık basamakların sayısını artırarak, verileri eşitlemek için çift yazma kullandığınızda veri kaybını engelleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea477-106">By increasing the number of decimal places, you help prevent data loss when you use dual-write to sync data.</span></span> <span data-ttu-id="ea477-107">Ondalık basamak sayısında artış kabul edilerek yapılan bir değişikliktir.</span><span class="sxs-lookup"><span data-stu-id="ea477-107">The increase in the number of decimal places is an opt-in change.</span></span> <span data-ttu-id="ea477-108">Bunu uygulamak için, Microsoft'tan yardım istemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ea477-108">To implement it, you must request assistance from Microsoft.</span></span>

<span data-ttu-id="ea477-109">Ondalık basamak sayısının değiştirilmesi işleminde iki adım vardır:</span><span class="sxs-lookup"><span data-stu-id="ea477-109">The process of changing the number of decimal places has two steps:</span></span>

1. <span data-ttu-id="ea477-110">Microsoft'tan geçiş talep edin.</span><span class="sxs-lookup"><span data-stu-id="ea477-110">Request migration from Microsoft.</span></span>
2. <span data-ttu-id="ea477-111">Dataverse'ta ondalık basamak sayısını değiştirin.</span><span class="sxs-lookup"><span data-stu-id="ea477-111">Change the number of decimal places in Dataverse.</span></span>

<span data-ttu-id="ea477-112">Finance and Operations uygulaması ve Dataverse'ın para birimi değerlerinde aynı sayıda ondalık basamak desteklemesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="ea477-112">The Finance and Operations app and Dataverse must support the same number of decimal places in currency values.</span></span> <span data-ttu-id="ea477-113">Aksi takdirde, bu bilgiler uygulamalar arasında eşitlendiğinde veri kaybı ortaya çıkabilir.</span><span class="sxs-lookup"><span data-stu-id="ea477-113">Otherwise, data loss can occur when this information is synced between apps.</span></span> <span data-ttu-id="ea477-114">Geçiş işlemi para birimi ve döviz kuru değerlerinin depolanma biçimini yeniden yapılandırır, ancak hiçbir veriyi değiştirmez.</span><span class="sxs-lookup"><span data-stu-id="ea477-114">The migration process reconfigures the way that currency and exchange rate values are stored, but it doesn't change any data.</span></span> <span data-ttu-id="ea477-115">Geçiş tamamlandıktan sonra, para birimi kodları ve fiyatlandırma için ondalık basamak sayısı artırılabilir ve kullanıcıların girdiği ve görüntülediği verilerde daha fazla ondalık duyarlığı olabilir.</span><span class="sxs-lookup"><span data-stu-id="ea477-115">After the migration is completed, the number of decimal places for currency codes and pricing can be increased, and the data that users enter and view can have more decimal precision.</span></span>

<span data-ttu-id="ea477-116">Geçiş isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ea477-116">Migration is optional.</span></span> <span data-ttu-id="ea477-117">Daha fazla ondalık basamak desteğinden avantaj sağlayabilecekseniz, geçiş yapmayı düşünmeniz önerilir.</span><span class="sxs-lookup"><span data-stu-id="ea477-117">If you might benefit from support for more decimal places, we recommend that you consider migration.</span></span> <span data-ttu-id="ea477-118">Dörtten fazla ondalık basamak içeren değerlerin gerekli olmadığı kuruluşların geçiş yapması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="ea477-118">Organizations that don't require values that have more than four decimal places don't have to migrate.</span></span>

## <a name="requesting-migration-from-microsoft"></a><span data-ttu-id="ea477-119">Microsoft'tan geçiş talep etme</span><span class="sxs-lookup"><span data-stu-id="ea477-119">Requesting migration from Microsoft</span></span>

<span data-ttu-id="ea477-120">Dataverse'teki mevcut para birimi sütunları için depolama, dörtten fazla ondalık basamak destekleyemez.</span><span class="sxs-lookup"><span data-stu-id="ea477-120">Storage for existing currency columns in Dataverse can't support more than four decimal places.</span></span> <span data-ttu-id="ea477-121">Bu nedenle, geçiş işlemi sırasında, para birimi değerleri veritabanındaki yeni dahili sütunlara kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="ea477-121">Therefore, during the migration process, currency values are copied to new internal columns in the database.</span></span> <span data-ttu-id="ea477-122">Bu işlem, tüm veriler geçirilene kadar sürekli olarak gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="ea477-122">This process occurs continuously until all data has been migrated.</span></span> <span data-ttu-id="ea477-123">Dahili olarak, geçişin sonunda yeni depolama türleri eski depolama türlerinin yerini alır, ancak veri değerleri değiştirilmez.</span><span class="sxs-lookup"><span data-stu-id="ea477-123">Internally, at the end of migration, the new storage types replace the old storage types, but the data values are unchanged.</span></span> <span data-ttu-id="ea477-124">Böylece para birimi sütunları en fazla 10 ondalık basamağı destekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="ea477-124">The currency columns can then support up to 10 decimal places.</span></span> <span data-ttu-id="ea477-125">Geçiş işlemi sırasında Dataverse kesinti olmadan kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ea477-125">During the migration process, Dataverse can continue to be used without interruption.</span></span>

<span data-ttu-id="ea477-126">Aynı zamanda, döviz kurları, geçerli 10 limiti yerine 12'ye kadar ondalık basamağı destekleyecek şekilde değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="ea477-126">At the same time, exchange rates are modified so that they support up to 12 decimal places instead of the current limit of 10.</span></span> <span data-ttu-id="ea477-127">Bu değişiklik, ondalık basamak sayısının hem Finance and Operations hem de Dataverse'te aynı olmasını sağlamak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ea477-127">This change is required so that the number of decimal places is the same in both the Finance and Operations app and Dataverse.</span></span>

<span data-ttu-id="ea477-128">Geçiş hiçbir veriyi değiştirmez.</span><span class="sxs-lookup"><span data-stu-id="ea477-128">Migration doesn't change any data.</span></span> <span data-ttu-id="ea477-129">Para birimi ve döviz kuru sütunları dönüştürüldükten sonra, yöneticiler her hareket para birimi ve fiyatlandırma için ondalık basamak sayısını belirterek sistemi, para birimi sütunları için en çok 10 ondalık basamak kullanacak şekilde yapılandırabilir.</span><span class="sxs-lookup"><span data-stu-id="ea477-129">After the currency and exchange rate columns are converted, admins can configure the system to use up to 10 decimal places for currency columns by specifying the number of decimal places for each transaction currency and for pricing.</span></span>

### <a name="request-a-migration"></a><span data-ttu-id="ea477-130">Geçiş talep etme</span><span class="sxs-lookup"><span data-stu-id="ea477-130">Request a migration</span></span>

<span data-ttu-id="ea477-131">Bu özelliği kullanılabilir hale getirmek için, **CDSExpandDecimal@microsoft.com** adresine aşağıdaki bilgileri ekleyerek e-posta gönderin:</span><span class="sxs-lookup"><span data-stu-id="ea477-131">To make this feature available, email **CDSExpandDecimal@microsoft.com**, and include the following information:</span></span>

+ <span data-ttu-id="ea477-132">**Konu:** \<organizationID\> için genişletilmiş ondalık desteği etkinleştirme isteği</span><span class="sxs-lookup"><span data-stu-id="ea477-132">**Subject:** Request to enable expanded decimal support for \<organizationID\></span></span>
+ <span data-ttu-id="ea477-133">**Gövde:** \<organizationID\> kuruluşum için genişletilmiş ondalık desteğini etkinleştirmek istiyorum.</span><span class="sxs-lookup"><span data-stu-id="ea477-133">**Body:** I would like to enable expanded decimal support for my org \<organizationID\>.</span></span>

<span data-ttu-id="ea477-134">Bir Microsoft temsilcisi, sonraki adımlar için iki ile üç iş günü içinde sizinle iletişim kuracaktır.</span><span class="sxs-lookup"><span data-stu-id="ea477-134">A Microsoft representative will contact you within two to three business days for the next steps.</span></span>

<span data-ttu-id="ea477-135">Bir geçiş istediğinizde, aşağıdaki ayrıntılara sahip olmanız ve bunları uygun şekilde planlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="ea477-135">When you request a migration, you should be aware of the following details and plan for them accordingly:</span></span>

+ <span data-ttu-id="ea477-136">Verileri geçirmek için gereken süre sistemdeki veri miktarına bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ea477-136">The time that is required to migrate the data depends the amount of data in the system.</span></span> <span data-ttu-id="ea477-137">Büyük veritabanlarının geçiş işlemi birkaç gün sürebilir.</span><span class="sxs-lookup"><span data-stu-id="ea477-137">Migration of large databases can take several days.</span></span>
+ <span data-ttu-id="ea477-138">Veritabanı boyutu, geçiş işlemi çalışırken geçici olarak artar, çünkü dizinler için ek alan gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ea477-138">The size of the database temporarily increases while the migration is running, because additional space is needed for indexes.</span></span> <span data-ttu-id="ea477-139">Geçiş tamamlandığında, ek alanın büyük bir çoğunluğu serbest kalır.</span><span class="sxs-lookup"><span data-stu-id="ea477-139">Most of the additional space is freed when the migration is completed.</span></span>
+ <span data-ttu-id="ea477-140">Geçiş işlemi sırasında, geçişin tamamlanmasını engelleyen hatalar oluşursa, sistem Microsoft Desteği'ne uyarıları gönderir ve Destek personeli müdahale edebilir.</span><span class="sxs-lookup"><span data-stu-id="ea477-140">During the migration process, if errors occur that prevent the migration from being completed, the system raise alerts to Microsoft Support, so that Support staff can intervene.</span></span> <span data-ttu-id="ea477-141">Ancak, geçiş sırasında hatalar oluşsa bile, Dataverse olağan kullanım için tamamen kullanılabilir durumda kalır.</span><span class="sxs-lookup"><span data-stu-id="ea477-141">However, even if errors occur during the migration, Dataverse remains fully available for regular use.</span></span>
+ <span data-ttu-id="ea477-142">Geçiş işlemi geri alınamaz.</span><span class="sxs-lookup"><span data-stu-id="ea477-142">The migration process isn't reversible.</span></span>

## <a name="changing-the-number-of-decimal-places"></a><span data-ttu-id="ea477-143">Ondalık basamak sayısının değiştirilmesi</span><span class="sxs-lookup"><span data-stu-id="ea477-143">Changing the number of decimal places</span></span>

<span data-ttu-id="ea477-144">Geçiş tamamlandıktan sonra, Dataverse daha fazla ondalık basamak içeren sayıları depolayabilir.</span><span class="sxs-lookup"><span data-stu-id="ea477-144">After the migration is completed, Dataverse can store numbers that have more decimal places.</span></span> <span data-ttu-id="ea477-145">Yöneticiler, belirli para birimi kodları ve fiyatlandırma için kaç ondalık basamak kullanılacağını seçebilirler.</span><span class="sxs-lookup"><span data-stu-id="ea477-145">Admins can choose how many decimal places are used for specific currency codes and for pricing.</span></span> <span data-ttu-id="ea477-146">Microsoft Power Apps, Power BI, ve Power Automate kullanıcıları daha sonra daha fazla ondalık basamak içeren sayıları görüntüleyebilir ve kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="ea477-146">Users of Microsoft Power Apps, Power BI, and Power Automate can then view and use numbers that have more decimal places.</span></span>

<span data-ttu-id="ea477-147">Bu değişikliği yapmak için Power Apps'te aşağıdaki ayarları güncelleştirmeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="ea477-147">To make this change, you must update the following settings in Power Apps:</span></span>

+ <span data-ttu-id="ea477-148">**Sistem Ayarları: Fiyatlandırma için para birimi duyarlığı** - **Sistem genelinde fiyatlandırma için kullanılan para birimi duyarlığını ayarla** sütunu **Fiyatlandırma Duyarlılığı** seçildiğinde, para biriminin kuruluş için nasıl davranacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="ea477-148">**System Settings: Currency precision for pricing** – The **Set the currency precision that is used for pricing throughout the system** column defines how the currency will behave for the organization when **Pricing Precision** is selected.</span></span>
+ <span data-ttu-id="ea477-149">**İş Yönetimi: Para birimleri** - **Para Birimi Duyarlığı** sütunu, belirli bir para birimi için özel bir ondalık basamak sayısı belirlemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="ea477-149">**Business Management: Currencies** – The **Currency Precision** column lets you specify a custom number of decimal places for a specific currency.</span></span> <span data-ttu-id="ea477-150">Kuruluş genelinde ayara geri dönüş vardır.</span><span class="sxs-lookup"><span data-stu-id="ea477-150">There is a fallback to the organization-wide setting.</span></span>

<span data-ttu-id="ea477-151">Bazı kısıtlamalar bulunur:</span><span class="sxs-lookup"><span data-stu-id="ea477-151">There are some limitations:</span></span>

+ <span data-ttu-id="ea477-152">Bir tablo üzerinde para birimi sütununu yapılandıramazsınız.</span><span class="sxs-lookup"><span data-stu-id="ea477-152">You can't configure the currency column on a table.</span></span>
+ <span data-ttu-id="ea477-153">Yalnızca **Fiyatlandırma** ve **Hareket Para Birimi** düzeylerinde dörtten fazla ondalık basamak belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea477-153">You can specify more than four decimal places only at the **Pricing** and **Transaction Currency** levels.</span></span>

### <a name="system-settings-currency-precision-for-pricing"></a><span data-ttu-id="ea477-154">Sistem Ayarları: Fiyatlandırma için para birimi duyarlığı</span><span class="sxs-lookup"><span data-stu-id="ea477-154">System Settings: Currency precision for pricing</span></span>

<span data-ttu-id="ea477-155">Geçiş tamamlandıktan sonra, yöneticiler para birimi duyarlığını ayarlayabilir.</span><span class="sxs-lookup"><span data-stu-id="ea477-155">After migration is completed, admins can set the currency precision.</span></span> <span data-ttu-id="ea477-156">**Ayarlar \> Yönetim**'e gidin ve **Sistem Ayarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="ea477-156">Go to **Settings \> Administration**, and select **System Settings**.</span></span> <span data-ttu-id="ea477-157">Daha sonra, **Genel** sekmesinde, **Tüm sistemde fiyatlandırma için kullanılan para birimi duyarlığını ayarlayın** sütunundaki değeri aşağıda gösterildiği şekilde değiştirin.</span><span class="sxs-lookup"><span data-stu-id="ea477-157">Then, on the **General** tab, change the value of the **Set the currency precision that is used for pricing throughout the system** column, as shown in the following illustration.</span></span>

![Para birimi sistem ayarları](media/currency-system-settings.png)

### <a name="business-management-currencies"></a><span data-ttu-id="ea477-159">İş Yönetimi: Para Birimleri</span><span class="sxs-lookup"><span data-stu-id="ea477-159">Business Management: Currencies</span></span>

<span data-ttu-id="ea477-160">Belirli bir para birimi için para birimi duyarlığının fiyatlandırma için kullanılan para birimi duyarlığından farklı olmasını istiyorsanız, bunu değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea477-160">If you require that the currency precision for a specific currency differ from the currency precision that is used for pricing, you can change it.</span></span> <span data-ttu-id="ea477-161">**Ayarlar \> İş Yönetimi**'ne gidin **Para birimleri**'ni ve ardından değiştirilecek para birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="ea477-161">Go to **Settings \> Business Management**, select **Currencies**, and select the currency to change.</span></span> <span data-ttu-id="ea477-162">Sonra, aşağıdaki çizimde gösterildiği gibi, **Para Birimi Duyarlığı** sütununu istediğiniz ondalık basamak sayısına ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ea477-162">Then set the **Currency Precision** column to the number of decimal places that you want, as shown in the following illustration.</span></span>

![Belirli bir yerel ayarın para birimi ayarları](media/specific-currency.png)

### <a name="tables-currency-column"></a><span data-ttu-id="ea477-164">tablolar: Para birimi sütunu</span><span class="sxs-lookup"><span data-stu-id="ea477-164">tables: Currency column</span></span>

<span data-ttu-id="ea477-165">Belirli para birimi sütunları için yapılandırılabilecek ondalık basamak sayısı dört ile sınırlıdır.</span><span class="sxs-lookup"><span data-stu-id="ea477-165">The number of decimal places that can be configured for specific currency columns is limited to four.</span></span>

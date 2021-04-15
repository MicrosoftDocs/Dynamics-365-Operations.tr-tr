---
title: Örnek kopyala
description: Microsoft Dynamics 365 Human Resources veritabanını bir korumalı alan ortamına kopyalamak için Microsoft Dynamics Lifecycle Services'i (LCS) kullanabilirsiniz.
author: andreabichsel
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6cb8050980b9b54480d09a59379430cd229ff141
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801107"
---
# <a name="copy-an-instance"></a><span data-ttu-id="ae7c9-103">Örnek kopyala</span><span class="sxs-lookup"><span data-stu-id="ae7c9-103">Copy an instance</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ae7c9-104">Microsoft Dynamics 365 Human Resources veritabanını bir korumalı alan ortamına kopyalamak için Microsoft Dynamics Lifecycle Services'i (LCS) kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="ae7c9-105">Başka bir korumalı alan ortamınız varsa veritabanını bu ortamdan hedeflenen korumalı alan ortamına da kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="ae7c9-106">Örneği kopyalamak için aşağıdaki ipuçlarını göz önünde bulundurun:</span><span class="sxs-lookup"><span data-stu-id="ae7c9-106">To copy an instance, keep the following tips in mind:</span></span>

- <span data-ttu-id="ae7c9-107">Üzerine yazmak istediğiniz İnsan Kaynakları örneği bir korumalı alan ortamı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="ae7c9-108">Kopyalama kaynağı ve hedef ortamlar aynı bölgede olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-108">The environments you're copying from and to must be in the same region.</span></span> <span data-ttu-id="ae7c9-109">Bölgeler arasında kopyalama yapamazsınız.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-109">You can't copy across regions.</span></span>

- <span data-ttu-id="ae7c9-110">Örneği kopyaladıktan sonra oturum açmak için hedef ortamda bir yönetici olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="ae7c9-111">İnsan Kaynakları veritabanını kopyaladığınızda, bir Microsoft Power Apps ortamda bulunan öğeleri (uygulamalar veya veriler) kopyalamayın.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft Power Apps environment.</span></span> <span data-ttu-id="ae7c9-112">Bir Power Apps ortamdaki öğelerin nasıl kopyalanacağı hakkında bilgi için, bkz. [Ortam kopyalama](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="ae7c9-112">For information about how to copy elements in a Power Apps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="ae7c9-113">Üzerine yazmak istediğiniz Power Apps ortamı bir korumalı alan ortamı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-113">The Power Apps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="ae7c9-114">Power Apps üretim ortamını korumalı alan ortamına dönüştürmek için genel bir kiracı yöneticisi olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-114">You must be a global tenant admin to change a Power Apps production environment to a sandbox environment.</span></span> <span data-ttu-id="ae7c9-115">Power Apps ortamın değiştirilmesi hakkında daha fazla bilgi için, bkz. [Örneği değiştirme](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="ae7c9-115">For more information about changing a Power Apps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

- <span data-ttu-id="ae7c9-116">Örneği korumalı alan ortamınıza kopyalayıp sandbox ortamınızı Dataverse ile birleştirmek isterseniz Dataverse tablolarına özel alanları yeniden uygulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-116">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Dataverse, you must reapply custom fields to Dataverse tables.</span></span> <span data-ttu-id="ae7c9-117">[Özel alanları Dataverse'e uygulama](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-117">See [Apply custom fields to Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="ae7c9-118">İnsan Kaynakları veritabanını kopyalama etkileri</span><span class="sxs-lookup"><span data-stu-id="ae7c9-118">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="ae7c9-119">Bir İnsan Kaynakları veritabanını kopyaladığınızda aşağıdaki olaylar oluşur:</span><span class="sxs-lookup"><span data-stu-id="ae7c9-119">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="ae7c9-120">Kopyalama işlemi hedef ortamdaki varolan veritabanını siler.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-120">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="ae7c9-121">Kopyalama işlemi tamamlandıktan sonra, varolan veritabanını kurtaramazsınız.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-121">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="ae7c9-122">Kopyalama işlemi tamamlanana kadar hedef ortam kullanılamayacak.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-122">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="ae7c9-123">Microsoft Azure Blob depolama birimindeki belgeler bir ortamdan diğerine kopyalanmaz.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-123">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="ae7c9-124">Bunun sonucunda, ekli tüm belge ve şablonlar kopyalanmaz ve kaynak ortamda kalır.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-124">As a result, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="ae7c9-125">Yönetici kullanıcı dışındaki tüm kullanıcı hesapları ve iç hizmet kullanıcıları devre dışı bırakılacak.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-125">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="ae7c9-126">Yönetici kullanıcı, diğer kullanıcılar sisteme geri dönmeden önce verileri silebilir veya karartırabilir.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-126">The Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="ae7c9-127">Yönetici kullanıcının, belirli hizmetlere veya URL'lere tümleştirme son noktalarına yeniden bağlanması gibi gerekli yapılandırma değişikliklerini yapması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-127">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="ae7c9-128">İnsan Kaynakları veritabanını Kopyala</span><span class="sxs-lookup"><span data-stu-id="ae7c9-128">Copy the Human Resources database</span></span>

<span data-ttu-id="ae7c9-129">Bu görevi tamamlamak için, önce bir örneği kopyalayın ve sonra Power Apps ortamınızı kopyalamak için Microsoft Power Platform Yönetim Merkezi'ne oturum açın.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-129">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your Power Apps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="ae7c9-130">Bir örneği kopyaladığınızda, hedef örnekte veritabanı silinir.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-130">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="ae7c9-131">Hedef örneği bu işlem sırasında kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-131">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="ae7c9-132">LCS'de oturum açın ve kopyalamak istediğiniz örneği içeren LCS projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-132">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="ae7c9-133">LCS projenizde **İnsan Kaynakları Uygulama Yöneticisi** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-133">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="ae7c9-134">Kopyalanacak örneği seçin ve sonra **Kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-134">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="ae7c9-135">**Örneği kopyala** görev bölmesinde, üzerine yazılacak örneği seçin ve sonra **Kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-135">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="ae7c9-136">**Kopyalama durumu** alanı değerinin **tamamlandı** olarak güncelleştirilmesini bekleyin.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-136">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="ae7c9-137">Üzerine yazılacak örneği Seç</span><span class="sxs-lookup"><span data-stu-id="ae7c9-137">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="ae7c9-138">**Power Platform**'u seçin ve Microsoft Power Platform Yönetim Merkezi'nde oturum açın.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-138">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="ae7c9-139">Power Platform öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-139">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="ae7c9-140">Kopyalanacak Power Apps ortamını seçin ve sonra **Kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-140">Select the Power Apps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="ae7c9-141">Kopyalama işlemi tamamlandığında, hedef örneğe oturum açın ve Dataverse tümleştirmeyi etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-141">When the copy process is completed, sign in to the target instance, and enable Dataverse integration.</span></span> <span data-ttu-id="ae7c9-142">Daha fazla bilgi ve talimatlar için bkz. [Dataverse entegrasyonunu yapılandırma](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="ae7c9-142">For more information and instructions, see [Configure Dataverse integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="ae7c9-143">Veri öğeleri ve durumlar</span><span class="sxs-lookup"><span data-stu-id="ae7c9-143">Data elements and statuses</span></span>

<span data-ttu-id="ae7c9-144">Bir İnsan Kaynakları örneğini kopyaladığınızda aşağıdaki veri öğeleri kopyalanmaz:</span><span class="sxs-lookup"><span data-stu-id="ae7c9-144">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="ae7c9-145">**LogisticsElectronicAddress** tablosundaki e-posta adresleri</span><span class="sxs-lookup"><span data-stu-id="ae7c9-145">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="ae7c9-146">**BatchJobHistory**, **BatchHistory** ve **BatchConstraintHistory** tablolarındaki toplu iş geçmişi</span><span class="sxs-lookup"><span data-stu-id="ae7c9-146">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="ae7c9-147">**SysEmailSMTPPassword** tablosundaki Basit Posta Aktarım Protokolü (SMTP) parolası</span><span class="sxs-lookup"><span data-stu-id="ae7c9-147">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="ae7c9-148">**SysEmailParameters** tablosundaki SMTP geçiş sunucusu</span><span class="sxs-lookup"><span data-stu-id="ae7c9-148">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="ae7c9-149">**PrintMgmtSettings** ve **PrintMgmtDocInstance** tablolarındaki yazdırma yönetimi ayarlar</span><span class="sxs-lookup"><span data-stu-id="ae7c9-149">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="ae7c9-150">**SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** ve **BatchServerGroup** tablolarındaki ortama özel kayıtlar</span><span class="sxs-lookup"><span data-stu-id="ae7c9-150">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="ae7c9-151">DocuValue tablosundaki Belge ekleri.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-151">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="ae7c9-152">Bu ekler, kaynak ortamda üzerine yazılmış tüm Microsoft Office şablonları içerir</span><span class="sxs-lookup"><span data-stu-id="ae7c9-152">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="ae7c9-153">**PersonnelIntegrationConfiguration** tablosundaki bağlantı dizesi</span><span class="sxs-lookup"><span data-stu-id="ae7c9-153">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="ae7c9-154">Ortama özel oldukları için bu öğelerden bazıları kopyalanmaz.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-154">Some of these elements aren't copied because they're environment-specific.</span></span> <span data-ttu-id="ae7c9-155">**BatchServerConfig** ve **SysCorpNetPrinters** kayıtlarını örnekler içerir.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-155">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="ae7c9-156">Destek biletlerinin hacmi nedeniyle diğer öğeler kopyalanmıyor.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-156">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="ae7c9-157">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="ae7c9-157">For example:</span></span>

- <span data-ttu-id="ae7c9-158">SMTP, kullanıcı kabul test (korumalı alan) ortamında hala etkin olduğundan yinelenen e-postalar gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-158">Duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment.</span></span>

- <span data-ttu-id="ae7c9-159">Toplu işler hala etkin olduğundan geçersiz tümleştirme iletileri gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-159">Invalid integration messages might be sent because batch jobs are still enabled.</span></span>

- <span data-ttu-id="ae7c9-160">Yöneticiler yenileme sonrası temizleme eylemlerini gerçekleştiremeden kullanıcılar etkinleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-160">Users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="ae7c9-161">Bir örneği kopyaladığınızda aşağıdaki durumlar da değişir:</span><span class="sxs-lookup"><span data-stu-id="ae7c9-161">Also, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="ae7c9-162">Yönetici dışındaki tüm kullanıcılar **devre dışı** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-162">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="ae7c9-163">Bazı sistem işleri hariç, tüm toplu işler **stopaj** olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-163">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="ae7c9-164">Ortam yöneticisi</span><span class="sxs-lookup"><span data-stu-id="ae7c9-164">Environment admin</span></span>

<span data-ttu-id="ae7c9-165">Yöneticiler dahil olmak üzere hedef korumalı alan ortamındaki tüm kullanıcılar yerine kaynak ortam kullanıcıları tarafından değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-165">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="ae7c9-166">Bir kurulumu kopyalamadan önce, kaynak ortamda bir yönetici olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-166">Before you copy an instance, be sure that you're an Administrator in the source environment.</span></span> <span data-ttu-id="ae7c9-167">Değilseniz kopyalama işlemi tamamlandıktan sonra hedef korumalı alan ortamında oturum açamazsınız.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-167">If you aren't, you can't sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="ae7c9-168">Hedef korumalı alan ortamındaki yönetici olmayan tüm kullanıcılar, korumalı alan ortamında istenmeyen oturum açma yapılmasını engelleyecek şekilde devre dışı bırakılmıştır.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-168">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="ae7c9-169">Yöneticiler gerektiğinde kullanıcıları yeniden değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-169">Administrators can reenable users if needed.</span></span>

## <a name="apply-custom-fields-to-dataverse"></a><span data-ttu-id="ae7c9-170">Özel alanları Dataverse'e uygulama</span><span class="sxs-lookup"><span data-stu-id="ae7c9-170">Apply custom fields to Dataverse</span></span>

<span data-ttu-id="ae7c9-171">Örneği korumalı alan ortamınıza kopyalayıp sandbox ortamınızı Dataverse ile birleştirmek isterseniz Dataverse tablolarına özel alanları yeniden uygulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-171">If you copy an instance into your sandbox environment and want to integrate your sandbox environment with Dataverse, you must reapply custom fields to Dataverse tables.</span></span>

<span data-ttu-id="ae7c9-172">Dataverse tablolarına gösterilen her özel alan için aşağıdaki adımları uygulayın:</span><span class="sxs-lookup"><span data-stu-id="ae7c9-172">For each custom field that's exposed on Dataverse tables, do the following steps:</span></span>

1. <span data-ttu-id="ae7c9-173">Özel alana gidip **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-173">Go to the custom field and select **Edit**.</span></span>

2. <span data-ttu-id="ae7c9-174">Özel alanın etkin olduğu her cdm_\* varlığı için **Etkin** alanının seçimini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-174">Unselect the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

3. <span data-ttu-id="ae7c9-175">**Değişiklikleri Uygula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-175">Select **Apply Changes**.</span></span>

4. <span data-ttu-id="ae7c9-176">Yeniden **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-176">Select **Edit** again.</span></span>

5. <span data-ttu-id="ae7c9-177">Özel alanın etkin olduğu her cdm_\* varlığı için **Etkin** alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-177">Select the **Enabled** field for each cdm_\* entity that the custom field is enabled on.</span></span>

6. <span data-ttu-id="ae7c9-178">Yeniden **Değişiklikleri Uygula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-178">Select **Apply Changes** again.</span></span>

<span data-ttu-id="ae7c9-179">Seçimi kaldırma, değişiklikleri uygulama, yeniden seçme ve değişiklikleri yeniden uygulama, şemanın Dataverse'i güncelleştirerek özel alanları eklemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-179">The process of unselecting, applying changes, reselecting, and reapplying changes prompts the schema to update in Dataverse to include the custom fields.</span></span>

<span data-ttu-id="ae7c9-180">Özel alanlar hakkında daha fazla bilgi için bkz. [Özel alanlar oluşturma ve bunlarla çalışma](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span><span class="sxs-lookup"><span data-stu-id="ae7c9-180">For more information about custom fields, see [Create and work with custom fields](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/user-defined-fields).</span></span>

## <a name="see-also"></a><span data-ttu-id="ae7c9-181">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="ae7c9-181">See also</span></span>

[<span data-ttu-id="ae7c9-182">Human Resources'ı hazırlama</span><span class="sxs-lookup"><span data-stu-id="ae7c9-182">Provision Human Resources</span></span>](hr-admin-setup-provision.md)</br>
[<span data-ttu-id="ae7c9-183">Örneği kaldırma</span><span class="sxs-lookup"><span data-stu-id="ae7c9-183">Remove an instance</span></span>](hr-admin-setup-remove-instance.md)</br>
[<span data-ttu-id="ae7c9-184">Güncelleştirme işlemi</span><span class="sxs-lookup"><span data-stu-id="ae7c9-184">Update process</span></span>](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
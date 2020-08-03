---
title: Örnek kopyala
description: Microsoft Dynamics 365 Human Resources veritabanını bir korumalı alan ortamına kopyalamak için Microsoft Dynamics Lifecycle Services'i (LCS) kullanabilirsiniz.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: b14baf49517f5d606038af20366944788b22eba2
ms.sourcegitcommit: 1ec931f8fe86bde27f6def36ea214a2a05fb22f6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/13/2020
ms.locfileid: "3554337"
---
# <a name="copy-an-instance"></a><span data-ttu-id="225e1-103">Örnek kopyala</span><span class="sxs-lookup"><span data-stu-id="225e1-103">Copy an instance</span></span>

<span data-ttu-id="225e1-104">Microsoft Dynamics 365 Human Resources veritabanını bir korumalı alan ortamına kopyalamak için Microsoft Dynamics Lifecycle Services'i (LCS) kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="225e1-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="225e1-105">Başka bir korumalı alan ortamınız varsa veritabanını bu ortamdan hedeflenen korumalı alan ortamına da kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="225e1-105">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="225e1-106">Bir örneği kopyalamak için, aşağıdakileri yapmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="225e1-106">To copy an instance, you need to ensure the following:</span></span>

- <span data-ttu-id="225e1-107">Üzerine yazmak istediğiniz İnsan Kaynakları örneği bir korumalı alan ortamı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="225e1-107">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="225e1-108">Kopyalama kaynağı ve hedef ortamlar aynı bölgede olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="225e1-108">The environments you are copying from and to must be in the same region.</span></span> <span data-ttu-id="225e1-109">Bölgeler arasında kopyalama yapamazsınız.</span><span class="sxs-lookup"><span data-stu-id="225e1-109">You can't copy across regions.</span></span>

- <span data-ttu-id="225e1-110">Örneği kopyaladıktan sonra oturum açmak için hedef ortamda bir yönetici olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="225e1-110">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="225e1-111">İnsan Kaynakları veritabanını kopyaladığınızda, bir Microsoft PowerApps ortamda bulunan öğeleri (uygulamalar veya veriler) kopyalamayın.</span><span class="sxs-lookup"><span data-stu-id="225e1-111">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft PowerApps environment.</span></span> <span data-ttu-id="225e1-112">Bir PowerApps ortamdaki öğelerin nasıl kopyalanacağı hakkında bilgi için, bkz. [Ortam kopyalama](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="225e1-112">For information about how to copy elements in a PowerApps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="225e1-113">Üzerine yazmak istediğiniz PowerApps ortamı bir korumalı alan ortamı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="225e1-113">The PowerApps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="225e1-114">PowerApps üretim ortamını korumalı alan ortamına dönüştürmek için genel bir kiracı yöneticisi olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="225e1-114">You must be a global tenant admin to change a PowerApps production environment to a sandbox environment.</span></span> <span data-ttu-id="225e1-115">PowerApps ortamın değiştirilmesi hakkında daha fazla bilgi için, bkz. [Örneği değiştirme](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="225e1-115">For more information about changing a PowerApps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="225e1-116">İnsan Kaynakları veritabanını kopyalama etkileri</span><span class="sxs-lookup"><span data-stu-id="225e1-116">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="225e1-117">Bir İnsan Kaynakları veritabanını kopyaladığınızda aşağıdaki olaylar oluşur:</span><span class="sxs-lookup"><span data-stu-id="225e1-117">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="225e1-118">Kopyalama işlemi hedef ortamdaki varolan veritabanını siler.</span><span class="sxs-lookup"><span data-stu-id="225e1-118">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="225e1-119">Kopyalama işlemi tamamlandıktan sonra, varolan veritabanını kurtaramazsınız.</span><span class="sxs-lookup"><span data-stu-id="225e1-119">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="225e1-120">Kopyalama işlemi tamamlanana kadar hedef ortam kullanılamayacak.</span><span class="sxs-lookup"><span data-stu-id="225e1-120">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="225e1-121">Microsoft Azure Blob depolama birimindeki belgeler bir ortamdan diğerine kopyalanmaz.</span><span class="sxs-lookup"><span data-stu-id="225e1-121">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="225e1-122">Bu nedenle, ekli tüm belge ve şablonlar kopyalanmayacak ve kaynak ortamda kalır.</span><span class="sxs-lookup"><span data-stu-id="225e1-122">Therefore, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="225e1-123">Yönetici kullanıcı dışındaki tüm kullanıcı hesapları ve iç hizmet kullanıcıları devre dışı bırakılacak.</span><span class="sxs-lookup"><span data-stu-id="225e1-123">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="225e1-124">Bu nedenle, Yönetici kullanıcısı, diğer kullanıcıların sisteme geri dönebilmesi için verileri silebilir veya karartırabilir.</span><span class="sxs-lookup"><span data-stu-id="225e1-124">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="225e1-125">Yönetici kullanıcının, belirli hizmetlere veya URL'lere tümleştirme son noktalarına yeniden bağlanması gibi gerekli yapılandırma değişikliklerini yapması gerekir.</span><span class="sxs-lookup"><span data-stu-id="225e1-125">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="225e1-126">İnsan Kaynakları veritabanını Kopyala</span><span class="sxs-lookup"><span data-stu-id="225e1-126">Copy the Human Resources database</span></span>

<span data-ttu-id="225e1-127">Bu görevi tamamlamak için, önce bir örneği kopyalayın ve sonra PowerApps ortamınızı kopyalamak için Microsoft Power Platform Yönetim Merkezi'ne oturum açın.</span><span class="sxs-lookup"><span data-stu-id="225e1-127">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your PowerApps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="225e1-128">Bir örneği kopyaladığınızda, hedef örnekte veritabanı silinir.</span><span class="sxs-lookup"><span data-stu-id="225e1-128">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="225e1-129">Hedef örneği bu işlem sırasında kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="225e1-129">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="225e1-130">LCS'de oturum açın ve kopyalamak istediğiniz örneği içeren LCS projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="225e1-130">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="225e1-131">LCS projenizde **İnsan Kaynakları Uygulama Yöneticisi** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="225e1-131">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="225e1-132">Kopyalanacak örneği seçin ve sonra **Kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="225e1-132">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="225e1-133">**Örneği kopyala** görev bölmesinde, üzerine yazılacak örneği seçin ve sonra **Kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="225e1-133">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="225e1-134">**Kopyalama durumu** alanı değerinin **tamamlandı** olarak güncelleştirilmesini bekleyin.</span><span class="sxs-lookup"><span data-stu-id="225e1-134">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="225e1-135">Üzerine yazılacak örneği Seç</span><span class="sxs-lookup"><span data-stu-id="225e1-135">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="225e1-136">**Power Platform**'u seçin ve Microsoft Power Platform Yönetim Merkezi'nde oturum açın.</span><span class="sxs-lookup"><span data-stu-id="225e1-136">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="225e1-137">Power Platform öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="225e1-137">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="225e1-138">Kopyalanacak PowerApps ortamını seçin ve sonra **Kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="225e1-138">Select the PowerApps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="225e1-139">Kopyalama işlemi tamamlandığında, hedef örneğe oturum açın ve Common Data Service tümleştirmeyi etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="225e1-139">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="225e1-140">Daha fazla bilgi ve talimatlar için bkz. [Common Data Service entegrasyonunu yapılandırma](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="225e1-140">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="225e1-141">Veri öğeleri ve durumlar</span><span class="sxs-lookup"><span data-stu-id="225e1-141">Data elements and statuses</span></span>

<span data-ttu-id="225e1-142">Bir İnsan Kaynakları örneğini kopyaladığınızda aşağıdaki veri öğeleri kopyalanmaz:</span><span class="sxs-lookup"><span data-stu-id="225e1-142">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="225e1-143">**LogisticsElectronicAddress** tablosundaki e-posta adresleri</span><span class="sxs-lookup"><span data-stu-id="225e1-143">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="225e1-144">**BatchJobHistory**, **BatchHistory** ve **BatchConstraintHistory** tablolarındaki toplu iş geçmişi</span><span class="sxs-lookup"><span data-stu-id="225e1-144">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="225e1-145">**SysEmailSMTPPassword** tablosundaki Basit Posta Aktarım Protokolü (SMTP) parolası</span><span class="sxs-lookup"><span data-stu-id="225e1-145">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="225e1-146">**SysEmailParameters** tablosundaki SMTP geçiş sunucusu</span><span class="sxs-lookup"><span data-stu-id="225e1-146">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="225e1-147">**PrintMgmtSettings** ve **PrintMgmtDocInstance** tablolarındaki yazdırma yönetimi ayarlar</span><span class="sxs-lookup"><span data-stu-id="225e1-147">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="225e1-148">**SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** ve **BatchServerGroup** tablolarındaki ortama özel kayıtlar</span><span class="sxs-lookup"><span data-stu-id="225e1-148">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="225e1-149">DocuValue tablosundaki Belge ekleri.</span><span class="sxs-lookup"><span data-stu-id="225e1-149">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="225e1-150">Bu ekler, kaynak ortamda üzerine yazılmış tüm Microsoft Office şablonları içerir</span><span class="sxs-lookup"><span data-stu-id="225e1-150">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="225e1-151">**PersonnelIntegrationConfiguration** tablosundaki bağlantı dizesi</span><span class="sxs-lookup"><span data-stu-id="225e1-151">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="225e1-152">Ortama özel oldukları için bu öğelerden bazıları kopyalanmıyor.</span><span class="sxs-lookup"><span data-stu-id="225e1-152">Some of these elements aren't copied because they are environment-specific.</span></span> <span data-ttu-id="225e1-153">**BatchServerConfig** ve **SysCorpNetPrinters** kayıtlarını örnekler içerir.</span><span class="sxs-lookup"><span data-stu-id="225e1-153">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="225e1-154">Destek biletlerinin hacmi nedeniyle diğer öğeler kopyalanmıyor.</span><span class="sxs-lookup"><span data-stu-id="225e1-154">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="225e1-155">Örneğin, SMTP kullanıcı kabul testi (korumalı alan) ortamında hala etkin olduğu için, yinelenen e-postalar gönderilebilir, toplu işler hala etkin olduğundan geçersiz tümleştirme iletileri gönderilebilir ve yöneticilerin yenileme sonrası temizleme eylemleri gerçekleştirebilmesi için kullanıcılar etkinleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="225e1-155">For example, duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="225e1-156">Ayrıca, bir örneği kopyaladığınızda aşağıdaki durumlar da değişecektir:</span><span class="sxs-lookup"><span data-stu-id="225e1-156">In addition, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="225e1-157">Yönetici dışındaki tüm kullanıcılar **devre dışı** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="225e1-157">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="225e1-158">Bazı sistem işleri hariç, tüm toplu işler **stopaj** olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="225e1-158">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="225e1-159">Ortam yöneticisi</span><span class="sxs-lookup"><span data-stu-id="225e1-159">Environment admin</span></span>

<span data-ttu-id="225e1-160">Yöneticiler dahil olmak üzere hedef korumalı alan ortamındaki tüm kullanıcılar yerine kaynak ortam kullanıcıları tarafından değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="225e1-160">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="225e1-161">Bir kurulumu kopyalamadan önce, kaynak ortamda bir yönetici olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="225e1-161">Before you copy an instance, be sure that you're an Administrator in the source environment.</span></span> <span data-ttu-id="225e1-162">Değilseniz, kopyalama işlemi tamamlandıktan sonra hedef sanal alanı ortamında oturum açamazsınız.</span><span class="sxs-lookup"><span data-stu-id="225e1-162">If you aren't, you won't be able to sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="225e1-163">Hedef korumalı alan ortamındaki yönetici olmayan tüm kullanıcılar, korumalı alan ortamında istenmeyen oturum açma yapılmasını engelleyecek şekilde devre dışı bırakılmıştır.</span><span class="sxs-lookup"><span data-stu-id="225e1-163">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="225e1-164">Yöneticiler gerektiğinde kullanıcıları yeniden değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="225e1-164">Administrators can reenable users if needed.</span></span>

---
title: Örnek kopyala
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0bbe325edb65cad0c1912e0a6ade559e5675dc58
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010816"
---
# <a name="copy-an-instance"></a><span data-ttu-id="1d432-102">Örnek kopyala</span><span class="sxs-lookup"><span data-stu-id="1d432-102">Copy an instance</span></span>

<span data-ttu-id="1d432-103">Microsoft Dynamics 365 Human Resources veritabanını bir korumalı alan ortamına kopyalamak için Microsoft Dynamics Lifecycle Services'i (LCS) kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d432-103">You can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Human Resources database to a sandbox environment.</span></span> <span data-ttu-id="1d432-104">Başka bir korumalı alan ortamınız varsa veritabanını bu ortamdan hedeflenen korumalı alan ortamına da kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d432-104">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span>

<span data-ttu-id="1d432-105">Bir örneği kopyalamak için, aşağıdakileri yapmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="1d432-105">To copy an instance, you need to ensure the following:</span></span>

- <span data-ttu-id="1d432-106">Üzerine yazmak istediğiniz İnsan Kaynakları örneği bir korumalı alan ortamı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1d432-106">The Human Resources instance you want to overwrite must be a sandbox environment.</span></span>

- <span data-ttu-id="1d432-107">Kopyalama kaynağı ve hedef ortamlar aynı bölgede olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1d432-107">The environments you are copying from and to must be in the same region.</span></span> <span data-ttu-id="1d432-108">Bölgeler arasında kopyalama yapamazsınız.</span><span class="sxs-lookup"><span data-stu-id="1d432-108">You can't copy across regions.</span></span>

- <span data-ttu-id="1d432-109">Örneği kopyaladıktan sonra oturum açmak için hedef ortamda bir yönetici olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1d432-109">You must be an Administrator in the target environment so you can sign into it after copying the instance.</span></span>

- <span data-ttu-id="1d432-110">İnsan Kaynakları veritabanını kopyaladığınızda, bir Microsoft PowerApps ortamda bulunan öğeleri (uygulamalar veya veriler) kopyalamayın.</span><span class="sxs-lookup"><span data-stu-id="1d432-110">When you copy the Human Resources database, you don't copy the elements (apps or data) that are contained in a Microsoft PowerApps environment.</span></span> <span data-ttu-id="1d432-111">Bir PowerApps ortamdaki öğelerin nasıl kopyalanacağı hakkında bilgi için, bkz. [Ortam kopyalama](https://docs.microsoft.com/power-platform/admin/copy-environment).</span><span class="sxs-lookup"><span data-stu-id="1d432-111">For information about how to copy elements in a PowerApps environment, see [Copy an environment](https://docs.microsoft.com/power-platform/admin/copy-environment).</span></span> <span data-ttu-id="1d432-112">Üzerine yazmak istediğiniz PowerApps ortamı bir korumalı alan ortamı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1d432-112">The PowerApps environment you want to overwrite must be a sandbox environment.</span></span> <span data-ttu-id="1d432-113">PowerApps üretim ortamını korumalı alan ortamına dönüştürmek için genel bir kiracı yöneticisi olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1d432-113">You must be a global tenant admin to change a PowerApps production environment to a sandbox environment.</span></span> <span data-ttu-id="1d432-114">PowerApps ortamın değiştirilmesi hakkında daha fazla bilgi için, bkz. [Örneği değiştirme](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span><span class="sxs-lookup"><span data-stu-id="1d432-114">For more information about changing a PowerApps environment, see [Switch an instance](https://docs.microsoft.com/dynamics365/admin/switch-instance).</span></span>

## <a name="effects-of-copying-a-human-resources-database"></a><span data-ttu-id="1d432-115">İnsan Kaynakları veritabanını kopyalama etkileri</span><span class="sxs-lookup"><span data-stu-id="1d432-115">Effects of copying a Human Resources database</span></span>

<span data-ttu-id="1d432-116">Bir İnsan Kaynakları veritabanını kopyaladığınızda aşağıdaki olaylar oluşur:</span><span class="sxs-lookup"><span data-stu-id="1d432-116">The following events occur when you copy a Human Resources database:</span></span>

- <span data-ttu-id="1d432-117">Kopyalama işlemi hedef ortamdaki varolan veritabanını siler.</span><span class="sxs-lookup"><span data-stu-id="1d432-117">The copy process erases the existing database in the target environment.</span></span> <span data-ttu-id="1d432-118">Kopyalama işlemi tamamlandıktan sonra, varolan veritabanını kurtaramazsınız.</span><span class="sxs-lookup"><span data-stu-id="1d432-118">After the copy process is completed, you can't recover the existing database.</span></span>

- <span data-ttu-id="1d432-119">Kopyalama işlemi tamamlanana kadar hedef ortam kullanılamayacak.</span><span class="sxs-lookup"><span data-stu-id="1d432-119">The target environment will be unavailable until the copy process is completed.</span></span>

- <span data-ttu-id="1d432-120">Microsoft Azure Blob depolama birimindeki belgeler bir ortamdan diğerine kopyalanmaz.</span><span class="sxs-lookup"><span data-stu-id="1d432-120">Documents in Microsoft Azure Blob storage aren't copied from one environment to another.</span></span> <span data-ttu-id="1d432-121">Bu nedenle, ekli tüm belge ve şablonlar kopyalanmayacak ve kaynak ortamda kalır.</span><span class="sxs-lookup"><span data-stu-id="1d432-121">Therefore, any documents and templates that are attached won't be copied and will remain in the source environment.</span></span>

- <span data-ttu-id="1d432-122">Yönetici kullanıcı dışındaki tüm kullanıcı hesapları ve iç hizmet kullanıcıları devre dışı bırakılacak.</span><span class="sxs-lookup"><span data-stu-id="1d432-122">All users except the Admin user and other internal service user accounts will be unavailable.</span></span> <span data-ttu-id="1d432-123">Bu nedenle, Yönetici kullanıcısı, diğer kullanıcıların sisteme geri dönebilmesi için verileri silebilir veya karartırabilir.</span><span class="sxs-lookup"><span data-stu-id="1d432-123">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

- <span data-ttu-id="1d432-124">Yönetici kullanıcının, belirli hizmetlere veya URL'lere tümleştirme son noktalarına yeniden bağlanması gibi gerekli yapılandırma değişikliklerini yapması gerekir.</span><span class="sxs-lookup"><span data-stu-id="1d432-124">The Admin user must make required configuration changes, such as reconnecting integration endpoints to specific services or URLs.</span></span>

## <a name="copy-the-human-resources-database"></a><span data-ttu-id="1d432-125">İnsan Kaynakları veritabanını Kopyala</span><span class="sxs-lookup"><span data-stu-id="1d432-125">Copy the Human Resources database</span></span>

<span data-ttu-id="1d432-126">Bu görevi tamamlamak için, önce bir örneği kopyalayın ve sonra PowerApps ortamınızı kopyalamak için Microsoft Power Platform Yönetim Merkezi'ne oturum açın.</span><span class="sxs-lookup"><span data-stu-id="1d432-126">To complete this task, you first copy an instance, and then sign in to the Microsoft Power Platform Admin Center to copy your PowerApps environment.</span></span>

> [!WARNING]
> <span data-ttu-id="1d432-127">Bir örneği kopyaladığınızda, hedef örnekte veritabanı silinir.</span><span class="sxs-lookup"><span data-stu-id="1d432-127">When you copy an instance, the database is erased in the target instance.</span></span> <span data-ttu-id="1d432-128">Hedef örneği bu işlem sırasında kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="1d432-128">The target instance is unavailable during this process.</span></span>

1. <span data-ttu-id="1d432-129">LCS'de oturum açın ve kopyalamak istediğiniz örneği içeren LCS projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1d432-129">Sign in to LCS, and select the LCS project that contains the instance that you want to copy.</span></span>

2. <span data-ttu-id="1d432-130">LCS projenizde **İnsan Kaynakları Uygulama Yöneticisi** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="1d432-130">In your LCS project, select the **Human Resources App Management** tile.</span></span>

3. <span data-ttu-id="1d432-131">Kopyalanacak örneği seçin ve sonra **Kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="1d432-131">Select the instance to copy, and then select **Copy**.</span></span>

4. <span data-ttu-id="1d432-132">**Örneği kopyala** görev bölmesinde, üzerine yazılacak örneği seçin ve sonra **Kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="1d432-132">In the **Copy an instance** task pane, select the instance to overwrite, and then select **Copy**.</span></span> <span data-ttu-id="1d432-133">**Kopyalama durumu** alanı değerinin **tamamlandı** olarak güncelleştirilmesini bekleyin.</span><span class="sxs-lookup"><span data-stu-id="1d432-133">Wait for the value of the **Copy status** field to be updated to **Completed**.</span></span>

   ![[<span data-ttu-id="1d432-134">Üzerine yazılacak örneği Seç</span><span class="sxs-lookup"><span data-stu-id="1d432-134">Select instance to overwrite</span></span>](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. <span data-ttu-id="1d432-135">**Power Platform**'u seçin ve Microsoft Power Platform Yönetim Merkezi'nde oturum açın.</span><span class="sxs-lookup"><span data-stu-id="1d432-135">Select **Power Platform**, and sign in to the Microsoft Power Platform Admin Center.</span></span>

   ![[<span data-ttu-id="1d432-136">Power Platform öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1d432-136">Select Power Platform</span></span>](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. <span data-ttu-id="1d432-137">Kopyalanacak PowerApps ortamını seçin ve sonra **Kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="1d432-137">Select the PowerApps environment to copy, and then select **Copy**.</span></span>

7. <span data-ttu-id="1d432-138">Kopyalama işlemi tamamlandığında, hedef örneğe oturum açın ve Common Data Service tümleştirmeyi etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="1d432-138">When the copy process is completed, sign in to the target instance, and enable Common Data Service integration.</span></span> <span data-ttu-id="1d432-139">Daha fazla bilgi ve talimatlar için bkz. [Common Data Service entegrasyonunu yapılandırma](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span><span class="sxs-lookup"><span data-stu-id="1d432-139">For more information and instructions, see [Configure Common Data Service integration](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).</span></span>

## <a name="data-elements-and-statuses"></a><span data-ttu-id="1d432-140">Veri öğeleri ve durumlar</span><span class="sxs-lookup"><span data-stu-id="1d432-140">Data elements and statuses</span></span>

<span data-ttu-id="1d432-141">Bir İnsan Kaynakları örneğini kopyaladığınızda aşağıdaki veri öğeleri kopyalanmaz:</span><span class="sxs-lookup"><span data-stu-id="1d432-141">The following data elements aren't copied when you copy a Human Resources instance:</span></span>

- <span data-ttu-id="1d432-142">**LogisticsElectronicAddress** tablosundaki e-posta adresleri</span><span class="sxs-lookup"><span data-stu-id="1d432-142">Email addresses in the **LogisticsElectronicAddress** table</span></span>

- <span data-ttu-id="1d432-143">**BatchJobHistory**, **BatchHistory** ve **BatchConstraintHistory** tablolarındaki toplu iş geçmişi</span><span class="sxs-lookup"><span data-stu-id="1d432-143">The batch job history in the **BatchJobHistory**, **BatchHistory**, and **BatchConstraintHistory** tables</span></span>

- <span data-ttu-id="1d432-144">**SysEmailSMTPPassword** tablosundaki Basit Posta Aktarım Protokolü (SMTP) parolası</span><span class="sxs-lookup"><span data-stu-id="1d432-144">The Simple Mail Transfer Protocol (SMTP) password in the **SysEmailSMTPPassword** table</span></span>

- <span data-ttu-id="1d432-145">**SysEmailParameters** tablosundaki SMTP geçiş sunucusu</span><span class="sxs-lookup"><span data-stu-id="1d432-145">The SMTP Relay server in the **SysEmailParameters** table</span></span>

- <span data-ttu-id="1d432-146">**PrintMgmtSettings** ve **PrintMgmtDocInstance** tablolarındaki yazdırma yönetimi ayarlar</span><span class="sxs-lookup"><span data-stu-id="1d432-146">Print Management settings in the **PrintMgmtSettings** and **PrintMgmtDocInstance** tables</span></span>

- <span data-ttu-id="1d432-147">**SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** ve **BatchServerGroup** tablolarındaki ortama özel kayıtlar</span><span class="sxs-lookup"><span data-stu-id="1d432-147">Environment-specific records in the **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, and **BatchServerGroup** tables</span></span>

- <span data-ttu-id="1d432-148">DocuValue tablosundaki Belge ekleri.</span><span class="sxs-lookup"><span data-stu-id="1d432-148">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="1d432-149">Bu ekler, kaynak ortamda üzerine yazılmış tüm Microsoft Office şablonları içerir</span><span class="sxs-lookup"><span data-stu-id="1d432-149">These attachments include any Microsoft Office templates that were overwritten in the source environment</span></span>

- <span data-ttu-id="1d432-150">**PersonnelIntegrationConfiguration** tablosundaki bağlantı dizesi</span><span class="sxs-lookup"><span data-stu-id="1d432-150">The connection string in the **PersonnelIntegrationConfiguration** table</span></span>

<span data-ttu-id="1d432-151">Ortama özel oldukları için bu öğelerden bazıları kopyalanmıyor.</span><span class="sxs-lookup"><span data-stu-id="1d432-151">Some of these elements aren't copied because they are environment-specific.</span></span> <span data-ttu-id="1d432-152">**BatchServerConfig** ve **SysCorpNetPrinters** kayıtlarını örnekler içerir.</span><span class="sxs-lookup"><span data-stu-id="1d432-152">Examples include **BatchServerConfig** and **SysCorpNetPrinters** records.</span></span> <span data-ttu-id="1d432-153">Destek biletlerinin hacmi nedeniyle diğer öğeler kopyalanmıyor.</span><span class="sxs-lookup"><span data-stu-id="1d432-153">Other elements aren't copied because of the volume of support tickets.</span></span> <span data-ttu-id="1d432-154">Örneğin, SMTP kullanıcı kabul testi (korumalı alan) ortamında hala etkin olduğu için, yinelenen e-postalar gönderilebilir, toplu işler hala etkin olduğundan geçersiz tümleştirme iletileri gönderilebilir ve yöneticilerin yenileme sonrası temizleme eylemleri gerçekleştirebilmesi için kullanıcılar etkinleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="1d432-154">For example, duplicate emails might be sent because SMTP is still enabled in the user acceptance testing (sandbox) environment, invalid integration messages might be sent because batch jobs are still enabled, and users might be enabled before admins can perform post-refresh cleanup actions.</span></span>

<span data-ttu-id="1d432-155">Ayrıca, bir örneği kopyaladığınızda aşağıdaki durumlar da değişecektir:</span><span class="sxs-lookup"><span data-stu-id="1d432-155">In addition, the following statuses change when you copy an instance:</span></span>

- <span data-ttu-id="1d432-156">Yönetici dışındaki tüm kullanıcılar **devre dışı** olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="1d432-156">All users except Admin are set to **Disabled**.</span></span>

- <span data-ttu-id="1d432-157">Bazı sistem işleri hariç, tüm toplu işler **stopaj** olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="1d432-157">All batch jobs, except for some system jobs, are set to **Withhold**.</span></span>

## <a name="environment-admin"></a><span data-ttu-id="1d432-158">Ortam yöneticisi</span><span class="sxs-lookup"><span data-stu-id="1d432-158">Environment admin</span></span>

<span data-ttu-id="1d432-159">Yöneticiler dahil olmak üzere hedef korumalı alan ortamındaki tüm kullanıcılar yerine kaynak ortam kullanıcıları tarafından değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="1d432-159">All users in the target sandbox environment, including Administrators, are replaced by the users of the source environment.</span></span> <span data-ttu-id="1d432-160">Bir örneği kopyalamadan önce, hedef ortamda bir yönetici olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="1d432-160">Before you copy an instance, be sure that you're an Administrator in the target environment.</span></span> <span data-ttu-id="1d432-161">Değilseniz, kopyalama işlemi tamamlandıktan sonra hedef sanal alanı ortamında oturum açamazsınız.</span><span class="sxs-lookup"><span data-stu-id="1d432-161">If you aren't, you won't be able to sign in to the target sandbox environment after the copy has completed.</span></span>

<span data-ttu-id="1d432-162">Hedef korumalı alan ortamındaki yönetici olmayan tüm kullanıcılar, korumalı alan ortamında istenmeyen oturum açma yapılmasını engelleyecek şekilde devre dışı bırakılmıştır.</span><span class="sxs-lookup"><span data-stu-id="1d432-162">All non-Administrator users in the target sandbox environment are disabled to prevent unwanted sign-ins in the sandbox environment.</span></span> <span data-ttu-id="1d432-163">Yöneticiler gerektiğinde kullanıcıları yeniden değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="1d432-163">Administrators can reenable users if needed.</span></span>

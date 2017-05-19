---
title: "Bir veritabanını geri yükledikten sonra mali raporlama veri reyonunu sıfırlama"
description: "Bu konu Microsoft Dynamics 365 for Operations veritabanını geri yüklendikten sonra mali raporlama veri reyonunun nasıl sıfırlanacağını açıklar."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: d4ce390c62cbfb1f693410b004aa296c0ed75eb2
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Bir veritabanını geri yükledikten sonra mali raporlama veri reyonunu sıfırlama

[!include[banner](../includes/banner.md)]


Bu konu Microsoft Dynamics 365 for Operations veritabanını geri yüklendikten sonra mali raporlama veri reyonunun nasıl sıfırlanacağını açıklar. 

Dynamics 365 for Operations veritabanınızı bir yedeklemeden geri yüklemenizi veya veritabanını başka bir ortamdan kopyalamanızı gerektirecek birçok senaryo vardır. Bu durum söz konusu olduğunda, mali raporlama veri reyonunun geri yüklenen Dynamics 365 for Operations veritabanını düzgün şekilde kullanmasını sağlamak için gerekli olan adımları da izlemeniz gerekir. Mali raporlama veri reyonunu Dynamics 365 for Operations veritabanı geri yüklemesi dışında bi rnedenle sıfırlama konusundaki sorularınız için bkz. [Yönetim Raporlayıcısı veri reyonunu sıfırlama](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/). Bu işlemdeki adımların Dynamics 365 for Operation Mayıs 2016 sürümü (Uygulama yapısı 7.0.1265.23014 ve mali raporlama yapısı 7.0.10000.4) ve daha yeni sürümler için desteklendiğini unutmayın. Dynamics 365 for Operations'ın önceki bir sürümüne sahipseniz, yardım için Destek ekibimize başvurun.

## <a name="export-report-definitions"></a>Rapor tanımlarını dışa aktarma
İlk olarak, Rapor Tasarımcısı'nda bulunan rapor tasarımlarını aşağıdaki adımları uygulayarak dışa aktarın:

1.  Rapor Tasarımcısında, **Şirket** &gt; **Yapı Taşı Grupları**'na gidin.
2.  Dışa aktarılacak yapı taşı grubunu seçin ve **Dışa Aktar**'a tıklayın. **Not:** Dynamics 365 for Operations için yalnızca bir yapı taşı grubu desteklenir, **Varsayılan**.
3.  Dışa aktarılacak rapor tanımlarını seçin:
    -   Tüm rapor tanımlarını ve ilgili yapı taşlarını dışa aktarmak için **Tümünü Seç** öğesini tıklayın.
    -   Belirli raporları, satırları, sütunları, ağaçları veya boyut kümelerini dışa aktarmak için ilgili sekmeye tıklayın ve ardından dışa aktarılacak maddeleri seçin. Bir sekmede birden fazla madde seçmek için CTRL tuşunu basılı tutun. Dışa aktarılacak raporları seçtiğinizde ilişkili satırlar, sütunlar, ağaçlar ve boyut kümeleri seçilir.

4.  **Dışa Aktar**'a tıklayın.
5.  Bir dosya adı girin ve dışarı aktarılan rapor tanımlarını kaydetmek için istediğiniz güvenli bir konumu seçin.
6.  **Kaydet**'e tıklayın.

Dosya güvenli bir konuma kopyalanabilir veya yüklenebilir; bu dosyanın daha sonra farklı bir ortama aktarılmasını sağlar. Microsoft Azure depolama hesabı kullanma hakkındaki bilgileri [>AzCopy Komut Satırı Yardımcı Programı ile veri transferi](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy) bölümünde bulabilirsiniz. 
> [!NOTE]
> Microsoft, Dynamics 365 for Operations sözleşmenizin bir parçası olarak bir depolama hesabı sağlamaz. Bir depolama hesabı satın almanız veya ayrı bir Azure aboneliğine ait bir depolama hesabını kullanmanız gerekir. 
> [!WARNING]
> Azure Sanal Makineler'de D sürücüsünün davranışını dikkate alın. Dışa aktarılan yapı taşı gruplarınızı burada kalıcı olarak saklamayın. Geçici sürücüler hakkında daha fazla bilgi için bkz. [Microsoft Azure Sanal Makinelerindeki geçici sürücüyü anlama](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Hizmetleri durdurma
Ortamdaki tüm bilgisayarlara bağlanmak ve services.msc'yi kullanarak aşağıdaki Windows hizmetlerini durdurmak için Uzak Masaüstü'nü kullanın:

-   World wide web publishing service (tüm AOS bilgisayarlarda)
-   Microsoft Dynamics 365 for Operations Toplu İŞ Yönetmini Hizmeti (yalnızca özel olmayan AOS bilgisayarlarda)
-   Management Reporter 2012 İşlem Hizmeti (yalnızca BI bilgisayarlarda)

Bu hizmetlerin Dynamics 365 for Operations veritabanına açık bağlantıları olacaktır.

## <a name="reset"></a>Sıfırla
#### <a name="locate-the-latest-dataupgradezip-package"></a>Son DataUpgrade.zip paketini bulma

[DataUpgrade.zip komut dosyasını indirme](..\migration-upgrade\upgrade-data-to-latest-update.md) konusundaki yönergeleri kullanarak en son DataUpgrade.zip paketini bulun. Yönergeler veri yükseltme paketinin ortamınız için doğru sürümünü nasıl bulacağınızı açıklar.

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>Dynamics 365 for Operations veritabanı için komut dosyalarını çalıştırma

Aşağıdaki komut dosyalarını Dynamics 365 for Operations veritabanı için çalıştırın (finansal raporlama veritabanı için değil).

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Bu komut dosyaları kullanıcıların, rollerin ve değişiklik izleme ayarlarının doğru olmasını sağlar.

#### <a name="execute-powershell-command-to-reset-database"></a>Veritabanını sıfırlamak için PowerShell komutunu çalıştırma

Dynamics 365 for Operations ve mali raporlama tümleştirmesini sıfırlamak için doğrudan AOS bilgisayarındaki aşağıdaki komutu çalıştırın:

1.  Windows PowerShell'i Yönetici olarak açın.
2.  Execute: F:
3.  Execute: cd F:\\MRApplicationService\\MRInstallDirectory
4.  Execute: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1
5.  Execute: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”
    -   Onaylamak için "Y" girmeniz istenir.

Parametre açıklaması:

-   Neden - için geçerli değerler şunlardır: SERVICING, BADDATA, OTHER
-   - ReasonDetail parametresi serbest metindir.
-   Neden ve reasonDetail telemetri/ortam izlemede kaydedilecektir.

## <a name="start-services"></a>Hizmetleri başlatma
Daha önce durdurduğunuz hizmetleri yeniden başlatmak için services.msc'yi kullanın:

-   World wide web publishing service (tüm AOS bilgisayarlarda)
-   Microsoft Dynamics 365 for Operations Toplu İŞ Yönetmini Hizmeti (yalnızca özel olmayan AOS bilgisayarlarda)
-   Management Reporter 2012 İşlem Hizmeti (yalnızca BI bilgisayarlarda)

## <a name="import-report-definitions"></a>Rapor tanımlarını içe aktarma
Rapor Tasarımcısı'ndan rapor tanımlarınızı dışa aktarma sırasında oluşturulan dosyayı kullanarak içe aktarın:

1.  Rapor Tasarımcısında, **Şirket** &gt; **Yapı Taşı Grupları**'na gidin.
2.  Dışa aktarılacak yapı taşı grubunu seçin ve **Dışa Aktar**'a tıklayın. 
    > [!NOTE]
    > Dynamics 365 for Operations için yalnızca bir yapı taşı grubu desteklenir, **Varsayılan**.
3.  **Varsayılan** yapı bloğunu seçin ve **İçe Aktar**'a tıklayın.
4.  Dışa aktarılan rapor tanımlarını içeren dosyayı seçin **Aç**'a tıklayın.
5.  İçe Aktar iletişim kutusunda, içe aktarılacak rapor tanımlarını seçin:
    -   Rapor tanımlarının ve destekleyici yapı taşlarının tümünü içe aktarmak için **Tümünü Seç** öğesine tıklayın.
    -   Belirli raporları, satırları, sütunları, ağaçları veya boyut kümelerini içe aktarmak için, içe aktarılacak raporları, satırları, sütunları, ağaçları veya boyut kümelerini seçin.

6.  **İçe aktar**'a tıklayın.






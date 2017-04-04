---
title: "Bir veritabanını geri yükledikten sonra mali raporlama veri merkezini Sıfırla"
description: "Bu konu Microsoft Dynamics 365 işlemleri veritabanı geri yüklendikten sonra mali raporlama veri merkezini sıfırlamak nasıl açıklar."
author: twheeloc
manager: AnnBe
ms.date: 2016-12-08 16 - 20 - 13
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
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 3967cbb869fbb23d5d7716f619e4c22b4a273921
ms.lasthandoff: 03/29/2017


---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Bir veritabanını geri yükledikten sonra mali raporlama veri merkezini Sıfırla

Bu konu Microsoft Dynamics 365 işlemleri veritabanı geri yüklendikten sonra mali raporlama veri merkezini sıfırlamak nasıl açıklar. 

Burada, Dynamics 365 işlemleri veritabanı için bir yedek kopyasından geri yükleyin veya veritabanını başka bir ortamdan kopyalamak gerekebilir birkaç senaryo vardır. Bu durumda, aynı zamanda işlemleri için veritabanı geri yüklenen Dynamics 365, finansal raporlama veri merkezini doğru kullanıyor olmak için uygun olan adımları izleyin gerekir. Finansal raporlama veri merkezini Dynamics 365 veritabanı işlemleri için geri dışında bir nedenle sıfırlama hakkında sorularınız varsa, bakın [Management Reporter veri merkezini sıfırlama](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) daha fazla bilgi için. Bu işlemdeki adımlar için operasyon için Dynamics 365 desteklenmediğine dikkat edin Mayıs 2016 release (App yapı 7.0.1265.23014 ve finansal raporlama yapı 7.0.10000.4) ve daha yeni sürümleri. Lütfen Dynamics 365 işlemleri için önceki bir sürümü varsa, Yardım için destek ekibimize başvurun.

## <a name="export-report-definitions"></a>Rapor tanımlarını dışa aktar
İlk olarak, aşağıdaki adımları kullanarak Rapor Tasarımcısı'nda bulunan rapor tasarımları verin:

1.  Rapor Tasarımcısı'nda Git **şirket**&gt;**yapıtaşı grupları**.
2.  Dışa aktar öğesini tıklatıp yapı taşı grubu seçin **ver**. **Not:** işlemleri için Dynamics 365 için yalnızca bir yapı taşı grubu desteklenir, **varsayılan**.
3.  Verilecek rapor tanımını seçin:
    -   Tüm rapor tanımlarını ve ilgili yapı taşlarını dışa aktarmak için **Tümünü Seç** öğesini tıklayın.
    -   Belirli raporları, satırları, sütunları, ağaçları veya boyut kümelerini dışa aktarmak için ilgili sekmeye tıklayın ve ardından dışa aktarılacak maddeleri seçin. Bir sekmede birden fazla madde seçmek için CTRL tuşunu basılı tutun. Rapor vermek için seçtiğinizde, ilişkili satırlar, sütunlar, ağaçları ve boyut kümeleri seçilir.

4.  ' I **ver**.
5.  Bir dosya adı girin ve güvenli bir yerde verilen rapor tanımlarını kaydetmek istediğiniz yeri seçin.
6.  Click **Save**.

Dosya kopyalanır veya, başka bir zamanda farklı bir ortama aktarılacak sağlayan güvenli bir konuma karşıya. Microsoft Azure depolama hesabı hakkında bilgi bulunabilir [Transfer AzCopy komut satırı yardımcı programı ile veri](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). **Not:** Microsoft olmayan sağlar depolama hesabı, Dynamics 365 bir parçası olarak işlemleri anlaşması için. Depolama hesabı satın veya ayrı bir Azure abonelik depolama hesabından kullanın. **Önemli:** D sürücüsüne Azure sanal makineler üzerinde'nın davranışını dikkate alın. Burada verilen yapı taşı gruplarınızı kalıcı olarak tutma. Geçici sürücüler hakkında daha fazla bilgi için bkz: [geçici sürücü üzerinde Windows Azure sanal makineleri anlama](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Hizmetleri durdurma
Services.msc kullanarak aşağıdaki Windows Hizmetleri durdurmak ve ortamdaki tüm bilgisayarlara bağlanmak için Uzak Masaüstü'nü kullanın:

-   World wide web publishing service (tüm bilgisayarlarda AOS)
-   Microsoft Dynamics 365 işlemleri toplu Yönetimi hizmeti için (yalnızca özel olmayan AOS bilgisayarları)
-   Management Reporter 2012 işlem hizmeti (yalnızca BI bilgisayarlarda)

Bu hizmetler veritabanı işlemleri için Dynamics 365 açık bağlantıları olacaktır.

## <a name="reset"></a>Sıfırla
#### <a name="locate-the-latest-dataupgradezip-package"></a>Son DataUpgrade.zip paketi bulun

Bulunan yönergeleri kullanarak son DataUpgrade.zip paketi bulun [DataUpgrade.zip komut dosyası karşıdan](..\migration-upgrade\upgrade-data-to-latest-update.md). Veri yükseltme paketini ortamınız için doğru sürümünü bulma yönergeleri açıklanmaktadır.

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>Dynamics 365 karşı operasyonlar veritabanı komut dosyalarını yürütme

Karşı Dynamics 365 (değil karşı finansal raporlama veritabanı) veritabanı işlemleri için aşağıdaki komut dosyasını çalıştırın.

-   DataUpgrade.zip\\AosService\\komut dosyaları\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\komut dosyaları\\GrantAzViewChangeTracking.sql

Bu komut dosyaları, kullanıcılar, roller ve değişiklik izleme ayarları doğru olduğundan emin olun.

#### <a name="execute-powershell-command-to-reset-database"></a>Veritabanı sıfırlamak için PowerShell komut yürütme

Dynamics 365 işlemleri ve mali raporlama bütünleşmesi sıfırlamak için doğrudan AOS bilgisayarındaki, aşağıdaki komutu yürütün:

1.  Windows PowerShell'i yönetici olarak açın.
2.  Yürütme: F:
3.  Yürütün: cd F:\\MRApplicationService\\MRInstallDirectory
4.  Yürütme: Import-Module. \\Server\\MRDeploy\\MRDeploy.psd1
5.  Yürütme: Reset-DatamartIntegration-neden diğer - ReasonDetail "&lt;sıfırlamak için benim neden&gt;"
    -   Onaylamak için "Y" girmeniz istenir.

Parametre açıklaması:

-   Neden - için geçerli değerler şunlardır: bakımı, BADDATA, OTHER.
-   Serbest metin - ReasonDetail parametresidir.
-   Telemetry/ortam izleme nedeni ve reasonDetail kaydedilir.

## <a name="start-services"></a>Hizmetleri başlatma
Services.msc, daha önce durdurduğu hizmetleri yeniden başlatmak için kullanın:

-   World wide web publishing service (tüm bilgisayarlarda AOS)
-   Microsoft Dynamics 365 işlemleri toplu Yönetimi hizmeti için (yalnızca özel olmayan AOS bilgisayarları)
-   Management Reporter 2012 işlem hizmeti (yalnızca BI bilgisayarlarda)

## <a name="import-report-definitions"></a>Rapor tanımlarını içe aktarma
Rapor Tasarımcısı'ndan rapor tasarımlarınızı alma, verme işlemi sırasında oluşturulan dosyayı kullanıyor:

1.  Rapor Tasarımcısı'nda Git **şirket**&gt;**yapıtaşı grupları**.
2.  Dışa aktar öğesini tıklatıp yapı taşı grubu seçin **ver**. **Not:** işlemleri için Dynamics 365 için yalnızca bir yapı taşı grubu desteklenir, **varsayılan**.
3.  Seçin **varsayılan** oluşturma bloğu ve click **alma**.
4.  Verilen rapor tanımlarını içeren dosyayı seçin ve'ı **açık**.
5.  İçe Aktar iletişim kutusunda, içe aktarılacak rapor tanımlarını seçin:
    -   Rapor tanımlarının ve destekleyici yapı taşlarının tümünü içe aktarmak için **Tümünü Seç** öğesine tıklayın.
    -   Belirli raporları, satırları, sütunları, ağaçları veya boyut kümelerini içe aktarmak için, içe aktarılacak raporları, satırları, sütunları, ağaçları veya boyut kümelerini seçin.

6.  Click **Import**.




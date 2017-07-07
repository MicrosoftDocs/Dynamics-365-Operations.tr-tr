---
title: "Korumalı alan ortamında veri yükseltme"
description: "Bu konu, korumalı alan ortamında AX 2012'den Dynamics 365 for Finance and Operations'a veri yükseltmesi yapma işlemini açıklar."
author: tariqbell
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations, UnifiedOperations, Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 7140bf740f37a5eb970a5103750a7095d12a33cc
ms.contentlocale: tr-tr
ms.lasthandoff: 06/15/2017

---

# <a name="data-upgrade-in-a-sandbox-environment"></a>Korumalı alan ortamında veri yükseltme

[!include[banner](../includes/banner.md)]

[!include[upgrade banner](../includes/upgrade-banner.md)]

Bu görevin sonucunda korumalı alan ortamında kullanabileceğiniz yükseltilmiş bir veritabanı elde edersiniz. Korumalı alan ortamı, iş kullanıcılarının ve işlev ekibi üyelerinin uygulama işlevlerini değerlendirebileceği bir ortamdır. Bu işlev özelleştirmeleri ve Microsoft Dynamics AX 2012'den alınan verileri içerir.

Paylaşılan korumalı alan ortamında çalıştırmadan önce veri yükseltme işlemini geliştirme ortamında çalıştırmanızı öneririz çünkü bu yaklaşım başarılı bir yükseltme işlemi için gerekli olan süreyi azaltmaya yardımcı olacaktır. Daha fazla bilgi için bkz. [Bir geliştirme ortamında veri yükseltme](prepare-data-upgrade.md)

## <a name="overview-of-the-sandbox-data-upgrade-process"></a>Korumalı alan veri yükseltme işlemine genel bakış

Korumalı alan ortamında veri yükseltme işlemine başlamadan önce verileri geliştirme ortamında [Bir geliştirme ortamında veri yükseltme](prepare-data-upgrade.md) konusunda açıklandığı şekilde yükseltmiş olmanız gerekir. İki işlem birbirine çok benzer. Ana fark korumalı alan ortamının veri depolama için Microsoft Azure SQL Veritabanı, geliştirme ortamının ise Microsoft SQL Server kullanmasıdır. Veritabanı katmanındaki bu teknik fark korumalı alan ortamındaki veri yükseltme yordamını biraz değiştirmeniz gerekir çünkü AX 2012 veritabanı örneğinden yapılan bir yedekleme yalnızca SQL Veritabanına geri yüklenebilir.

![Korumalı alan veri yükseltme işlemi](./media/data-upgrade-sandbox.png)

Yükseltme sırasındaki üst düzey adımlar şunlardır.

1. AX 2012 veritabanının bir kopyasını oluşturun. Dışa aktarılan kopyada bazı nesneleri silmeniz gerekeceğinden bir kopya almanızı öneririz.
2. SQLPackage.exe adlı ücretsiz SQL Server aracını kullanarak kopyalanan veritabanını bacpac dosyasına aktarın. Bu araç, SQL Veritabanına aktarılabilecek özel bir veritabanı yedekleme türü sunar.
3. Azure depolamaya bacpac dosyasını yükleyin.
4. Korumalı alan ortamındaki Uygulama Nesne Sunucusu (AOS) makinesine bacpac dosyasını indirin ve SQLPackage.exe kullanarak bunu içe aktarın. SQL veritabanı kullanıcılarını sıfırlamak için içe aktarılan veritabanına karşı bir kod çalıştırmalısınız.
5. İçe aktarılan veritabanına karşı veri yükseltme işlemi çalıştırmak için MajorVersionDataUpgrade.zip paketini çalıştırın.

## <a name="create-a-copy-of-the-ax-2012-database"></a>AX 2012 veritabanının bir kopyasını oluşturma

Bazı nesneleri veritabanından silmek zorunda olduğunuz için yükselttiğiniz AX 2012 veritabanının bir kopyasını oluşturmanız gerekir. Bu nesneler Microsoft Windows kimlik doğrulaması kullanıcılarını içerir. Bu değişiklikler değiştirilmiş veritabanını AX 2012 için kullanılamaz hale getirir. Bu adım sırasında veritabanının bir kopyasını oluşturun ve bu nesneleri silin.

Bu adım veritabanı yöneticisi (DBA) veya benzer bilgi ve deneyime sahip bir kişi tarafından yapılmalıdır.

Veritabanının kopyasını oluşturmak için özgün veritabanının bir yedeğini alın ve yeni bir adla geri yükleyin. Her iki veritabanı için yeterli alan bulunduğundan emin olun. Kopyayı farklı bir sunucuda oluşturabilirsiniz. Veritabanını çalıştıran SQL Server kurulumunun sürümü önemli değildir.

Veritabanı kopyası oluşturan bir kod örneğini burada bulabilirsiniz. Bu örneği kendi veritabanı adlarınızı gösterecek şekilde değiştirmelisiniz.

    BACKUP DATABASE [AxDB] TO  DISK = N'D:\Backups\axdb_copyForUpgrade.bak' WITH NOFORMAT, NOINIT,  
    NAME = N'AxDB_copyForUpgrade-Full Database Backup', SKIP, NOREWIND, NOUNLOAD, COMPRESSION,  STATS = 10
    GO

    RESTORE DATABASE [AxDB_copyForUpgrade] FROM  DISK = N'D:\Backups\axdb_copyForUpgrade.bak'   WITH  FILE = 1,  
    MOVE N'AXDBBuild_Data' TO N'F:\MSSQL_DATA\AxDB_copyForUpgrade.mdf',  
    MOVE N'AXDBBuild_Log' TO N'G:\MSSQL_LOGS\AxDB_CopyForUpgrade.ldf',  
    NOUNLOAD,  STATS = 5

Kopya oluşturulduktan sonra, kopyaya karşı aşağıdaki Transact-SQL (T-SQL) komut dosyasını çalıştırın.
YAPILACAK İŞ 

### <a name="export-the-copied-database-to-a-bacpac-file"></a>Kopyalanan veritabanını bir bacpac dosyasına aktarın

SQLPackage.exe aracını kullanarak kopyalanan veritabanını bacpac dosyasına aktarın. Bu adım DBA veya eşdeğer bilgisi olan bir ekip üyesi tarafından yapılmalıdır.

Bu adıma başlamadan önce SQL Server Management Studio'nun en son sürümünü yüklemeniz çok önemlidir. Management Studio'nun önceki sürümlerinde SQLPackage olmasına karşın, en son sürümünü yüklemediğiniz sürece bu adım için doğru şekilde çalışmaz.

Dışa aktarma kullanıma sunmadan önceki kesinti süresi sırasında yeniden yapılmak zorunda olduğundan bu adım önemlidir. Burada bazı ipuçları verilmiştir:

- Bacpac işlemi çok ı/O ve yoğun CPU kullanımı gerektirir. Bu nedenle, dışa aktarmayı güçlü bir makinede çalıştırın.
- SQLPackage veritabanını barındıran makinede yerel olarak çalıştırılmalıdır. Bu işlem de ağı yoğun kullandığından SQLPackage veritabanını veritabanı makinesine bağlayacağınız yerel bir dizüstü bilgisayardan gerçekleştirmeyin.

Daha sonra yönetici olarak bir **Komut İstemi** penceresi açın ve aşağıdaki komutları çalıştırın.

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:export /ssn:localhost /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=1200 /p:VerifyFullTextDocumentTypesSupported=false

Parametrelerle ilgili açıklama aşağıda verilmiştir:

- **ssn** (kaynak sunucu adı) – Dışarıdan aktarmanın alınacağı SQL Server'ın adı. İşlemlerimizde bu parametrenin daima **localhost** olarak ayarlanması gerekir.
- **sdn** (kaynak veritabanı adı) – Dışa aktarılacak veritabanı adı.
- **tf** (hedef dosya) - Dışa aktarmanın yapılacağı dosyasının yolu ve adı. Klasör zaten var olmalıdır, ancak dosya işlem tarafından oluşturulur.
- **/p:CommandTimeout** – Her bir sorgu zaman aşımı değeri. Bu parametre daha büyük tabloların zaman aşımına uğramadan dışa aktarılmasını sağlar.

### <a name="upload-the-bacpac-file-to-azure-storage"></a>Azure depolamaya bacpac dosyasını yükleme

Azure depolamaya bacpac dosyanızı yükleyin. UsingStorageExplorer.docx YAPILAK İŞLER'e bakın

### <a name="import-the-bacpac-file-into-sql-database"></a>bacpac dosyasını SQL Veritabanına aktarın

Bu adım sırasında, dışa aktarılan bacpac dosyasını korumalı alan ortamınızın kullandığı SQL Veritabanı kurulumuna aktaracaksınız. Öncelik korumalı alan AOS makinenize Management Studio'nun en son sürümünü yüklemeniz gerekir. Daha sonra SQLPackage.exe aracını kullanarak dosyayı içe aktarın.

Bu görevleri doğrudan korumalı alan ortamınızın AOS makinesinden gerçekleştirirsiniz çünkü SQL Veritabanı kurulumlarına erişimi kısıtlayan güvelik duvarı kuralları bulunur. Bununla birlikte, AOS makinesini kullanarak erişebilirsiniz.

Dışa aktarma adımı söz konusu olduğunda, içe aktarma işlemini başlatmadan önce Management Studio'nun en son sürümüne sahip olmanız gerekir. Eski bir sürümü varsa, bu adım çalışmayacaktır.

Performans nedeniyle, bacpac dosyasını AOS makinesindeki D sürücüsüne koymanızı öneririz. Azure sanal makinelerde (VM), D sürücüsü genel olarak diğer mevcut disklerden daha yüksek performansa sahip bir fiziksel disktir..

Yönetici olarak bir **Komut İstemi** penceresi açın ve aşağıdaki komutları çalıştırın.

    cd C:\Program Files (x86)\Microsoft SQL Server\130\DAC\bin\

    SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:<azure sql database server name>.database.windows.net /tu:sqladmin /tp:<password from LCS> /tdn:<New database name> /p:CommandTimeout=1200 /p:DatabaseEdition=Premium /p:DatabaseServiceObjective=P1

Parametrelerle ilgili açıklama aşağıda verilmiştir:

- **tsn** (hedef sunucu adı) – İçe aktarılacak SQL Azure sunucusunun adı. Ad LCS'de bulunabilir. Son ek olarak **. database.windows.net** ekleyin.
- **tdn** (hedef veritabanı adı) – İçe aktarılacak veritabanı adı. Veritabanın zaten bulunması gerekmez. Alma işlemi veritabanını oluşturur.
- **sf** (kaynak dosya) - İçeri aktarım için verilerin alınacağı dosyanın yolu ve adı.
- **tp** (hedef parola) – Hedef SQL Veritabanı kurulumu için SQL parolası.
- **tu** (hedef kullanıcı) – Hedef SQL Veritabanı kurulumu için SQL kullanıcı adı. **sqladmin** kullanmanızı öneririz. Bu kullanıcı için parolayı LCS projenizden elde edebilirsiniz.
- **/p:CommandTimeout** – Her bir sorgu zaman aşımı değeri. Bu parametre daha büyük tabloların zaman aşımına uğramadan dışa aktarılmasını sağlar.
- **/p:DatabaseServiceObjective** – Oluşturulan veritabanının hizmet katmanı düzeyi. Varolan veritabanı için değeri Management Studio'yu kullanarak kontrol edebilirsiniz. Veritabanını sağ tıklayın ve sonra **Özellikler**'i seçin.

Komutları çalıştırdıktan sonra aşağıdaki uyarıyı alırsınız. Uyarıyı güvenli bir şekilde yok sayabilirsiniz.

![Korumalı alan hatası](./media/sandbox-2.png)
 
### <a name="run-the-majorversiondataupgradezip-package"></a>MajorVersionDataUpgrade.zip paketini çalıştırma

Veri yükseltme dağıtılabilir paketini [Geliştirme, tanıtım veya korumalı alan ortamlarındaki verileri yükseltme](upgrade-data-to-latest-update.md) bölümünde açıklandığı şekilde çalıştırın.

### <a name="upgrade-a-copy-of-the-database-in-a-development-environment"></a>Bir geliştirme ortamında veritabanının kopyasını yükseltme

Aynı veritabanını geliştirme ortamında yükseltmek yararlı olabilir. Veritabanının geliştirme ortamları için kullanılabilir bir kopyası varsa, yükseltilen korumalı alan ortamında bulunan hataları incelemek çok daha kolay olacaktır.


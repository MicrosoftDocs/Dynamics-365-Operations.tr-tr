---
title: ER şablonlarının yedekleme depolaması
description: Bu konu, şablonların kurtarılması için Elektronik Raporlama (ER) yedekleme depolamasının nasıl kullanılacağını açıklar.
author: NickSelin
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-13
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5dad101ffe56c9266c0d81ede8be1f72b684a8fb
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771433"
---
# <a name="backup-storage-of-er-templates"></a>ER şablonlarının yedekleme depolaması

[!include [banner](../includes/banner.md)]

[Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md) iş kullanıcılarının giden belgelerin biçimini çeşitli ülkelerin/bölgelerin yasal gereksinimlerine uygun şekilde yapılandırmasına olanak tanır. Yapılandırılan ER biçimleri Microsoft Excel çalışma kitapları, Microsoft Word belgeleri veya PDF belgeleri gibi çeşitli biçimlerde giden belgeler oluşturmak için önceden tanımlanmış şablonları kullanılabilir. Şablonlar, oluşturulan belgeler için yapılandırılan veri akışının gerektirdiği verilerle doldurulur.

Yapılandırılan her biçim, bir ER çözümünün parçası olarak yayımlanabilir. Her ER çözümü, Finance and Operations'ın bir örneğinden dışa aktarılabilir ve başka bir örneğin içine aktarılabilir.

ER çerçevesi, geçerli Finance and Operations kurulumu için gerekli şablonları korumak amacıyla [Belge yönetimini yapılandırma](../../fin-ops/organization-administration/configure-document-management.md) özelliğini kullanır. ER çerçevesinin ayarlarına bağlı olarak, Microsoft Azure Blob depolama veya Microsoft SharePoint klasörü, şablonların fiziksel birincil depolama konumu olarak seçilebilir. (Daha fazla bilgi için bkz. [Elektronik raporlama (ER) çerçevesini yapılandırma](electronic-reporting-er-configure-parameters.md).) DocuValue tablosu her şablon için tek bir kayıt içerir. Her kayıtta, **AccessInformation** alanı yapılandırılmış depolama konumunda bulunan bir şablon dosyasının yolunu depolar.

Finance and Operations örneklerinizi yönetirken, geçerli örneği başka bir konuma geçirmeye karar verebilirsiniz. Örneğin, üretim örneğinizi yeni bir korumalı alan ortamına geçirebilirsiniz. ER çerçevesini Blob depolamada şablon depolamak üzere yapılandırırsanız, yeni korumalı alan ortamındaki DocuValue tablosu, üretim ortamındaki Blob depolama örneğine başvurur. Ancak, geçiş işlemi Blob depolamadaki yapıların geçirilmesini desteklemediğinden, bu örneğe korumalı alan ortamından erişilemez. Bu nedenle, iş belgeleri oluşturmak için şablon kullanan bir ER biçimini çalıştırmaya çalışırsanız bir özel durum oluşur ve eksik şablon hakkında bilgilendirilirsiniz. Ayrıca, şablonu içeren ER biçimi yapılandırmasını silmek ve yeniden içe aktarmak için ER temizleme aracını da kullanabilirsiniz. Birden fazla ER biçimi yapılandırmanız olabileceğinden bu işlem uzun sürebilir.

ER şablonlarının Yedek depolaması şablonlarının iş belgeleri oluşturmak üzere daima kullanılabilir olmasını sağlamanıza yardımcı olabilir.

> [!NOTE]
> Bu özellik yalnızca, ER şablonları için fiziksel depolama konumu olarak Blob deposu seçildiğinde kullanılabilir.

Bu özellik için, geçerli ortamdaki yeni bir ER biçimi yapılandırmasının her şablonu, aşağıdaki olaylar gerçekleştiğinde otomatik olarak şablonların (ERDocuDatabaseStorage veritabanı tablosu) yedek depolama konumuna kaydedilir:

- Şablon içeren yeni bir ER biçimi yapılandırmasını içe aktardığınızda.
- Şablon içeren bir ER biçimi yapılandırmasının taslak sürümünü tamamladığınızda.

Şablonların yedek kopyaları, uygulama veritabanının bir parçası olarak yeni Finance and Operations örneğine geçirilir.

Örneğin, ödeme önerisi ve denetim raporları dahil olmak üzere satıcı ödemelerini işlemek amacıyla giden belgelerin oluşturulması için bir ER biçimi şablonu gerekliyse, ancak gerekli şablon birincil depolama konumunda bulunamazsa, aşağıdaki olaylar gerçekleşir:

- Şablon yedek depolama konumunda kullanılabilir durumdaysa, otomatik olarak yedek depolama konumundan alınır, birincil depolama konumuna geri yüklenir ve geçerli yürütme için kullanılır.
- **Elektronik raporlama geliştiricisi** veya **Sistem Yöneticisi** rolüne atanan her kullanıcı, İşlem merkezi aracılığıyla eksik şablon sorunu hakkında bilgilendirilir. Beliren ileti, **Toplu işte bozuk şablonları geri yükleme yordamını otomatik olarak çalıştır** parametresinin değerine bağlıdır:

    - Bu parametre **Kapalı** olarak ayarlanırsa, ileti diğer ER yapılandırma şablonları ile ilgili benzer sorunları otomatik olarak düzeltmek için toplu işlemi çalıştırmanızı önerir. Bu ileti, toplu işlemi başlatmak için kullanabileceğiniz bir bağlantı içerir.
    - Bu parametre **Açık** olarak ayarlandığında, ileti eksik bir şablon sorununun bulunduğu ve yeni **Bozuk şablonları dahili veritabamı yedeklemesinden geri yükle** toplu işinin otomatik olarak planlandığını bildirir. Bu toplu işlem, diğer şablonlardaki benzer sorunları otomatik olarak düzeltir.

**Toplu işte bozuk şablonları geri yükleme yordamını otomatik olarak çalıştır** parametresini ayarlamak için aşağıdaki adımları uygulayın:

1. Finance and Operations içinde, **Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırma sayfaları**'nı açın.
2. **Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.
3. **Kullanıcı parametreleri** iletişim kutusunda, **Toplu işte bozuk şablonları geri yükleme yordamını otomatik olarak çalıştır** parametresi için gereken değeri ayarlayın.

> [!NOTE]
> Bu parametre, uygulama kullanıcısı ve kaydedilmiş şirkete özel olarak tanımlanır.

![ER konfigürasyon sayfası](./media/GER-BackupTemplates-1.png)

Aşağıdaki örnekte **Toplu işte bozuk şablonları geri yükleme yordamını otomatik olarak çalıştır** parametresi **Açık** olarak ayarlandığında beliren ileti gösterilmektedir.

![Satıcı ödeme günlüğü sayfası](./media/GER-BackupTemplates-2.png)

Aşağıdaki örnekte , **Toplu iş** sayfasındaki **Bozuk şablonları dahili veritabamı yedeklemesinden geri yükle** toplu işi gösterilmektedir.

![Toplu iş sayfası](./media/GER-BackupTemplates-3.png)

Tamamlanan **Bozuk şablonları dahili veritabanı yedeklemesinden geri yükle** toplu işlemininin yürütme günlüğü yedek depolama konumundan birincil depolama konumuna geri yüklenmiş şablonlar hakkında bilgi içerir.

![Toplu iş geçmişi sayfası](./media/GER-BackupTemplates-4.png)

Varsayılan olarak, ER biçim yapılandırmalarında şablonların yedek kopyalarının otomatik oluşturulması işlemi etkindir. Şablonların yedek kopyalarını yapmayı durdurmak, **Şablonun yedek kopyalarını yapmayı durdur** seçeneğini **Elektronik raporlama parametreleri** sayfasının **Ekler** sekmesinde **Evet** olarak ayarlayın. Bu sayfayı **Elektronik raporlama** çalışma alanından açabilirsiniz.

**Şablonların yedek kopyalarını yapmayı durdur** seçeneğini **Evet** olarak ayarlasanız ve şablonların önceden yapılan yedek kopyalarını saklamak istemiyorsanız, **Elektronik raporlama parametreleri** sayfasında **Yedek depolamayı temizle** seçeneğini seçin.

Ortamınızı Finance and Operations 10.0.5 (2019 Ekim) sürümüne yükselttiyseniz ve çalıştırılabilir ER biçimi yapılandırmalarını içeren yeni bir ortama geçiş yapmak istiyorsanız, geçiş işlemi gerçekleşmeden önce **Elektronik raporlama parametreleri** sayfasında **Yedek depolamayı doldur** seçeneğini seçin. Bu düğme, tüm kullanılabilir şablonların yedek kopyalarını oluşturma işlemini başlatır, böylece şablonlar ER yedekleme depolaması alanında depolanabilir.

![Elektronik raporlama parametreleri sayfası](./media/GER-BackupTemplates-5.png)

## <a name="supported-deployments"></a>Desteklenen dağıtımlar

Finance and Operations 10.0.5 sürümünde, ER şablonlarını yedekleme depolama alanı özelliği yalnızca bulut dağıtımlarında kullanılabilir.

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)

[Elektronik raporlama (ER) altyapısını yapılandırma](electronic-reporting-er-configure-parameters.md)

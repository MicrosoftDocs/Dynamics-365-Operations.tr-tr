---
title: Dataverse tümleştirmesini yapılandırma
description: Microsoft Dataverse ve Dynamics 365 Human Resources arasındaki tümleştirmeyi açabilir veya kapatabilirsiniz. Ayrıca eşitleme ayrıntılarını görüntüleyebilir, izleme verilerini temizleyebilir ve iki ortam arasındaki veri sorunlarını gidermeye yardımcı olmak için bir tabloyu yeniden işleyebilirsiniz.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bf406a954f5bb8b49627b58a901d0721cdad407b
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890040"
---
# <a name="configure-dataverse-integration"></a>Dataverse tümleştirmesini yapılandırma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dataverse ve Dynamics 365 Human Resources arasındaki tümleştirmeyi açabilir veya kapatabilirsiniz. Eşitleme ayrıntılarını görüntüleyebilir, izleme verilerini temizleyebilir ve iki ortam arasındaki veri sorunlarını gidermeye yardımcı olmak için bir tabloyu yeniden işleyebilirsiniz.

> [!NOTE]
> Dataverse (önceden Common Data Service) ve terminoloji güncelleştirmeleri hakkında daha fazla bilgi için bkz. [Microsoft Dataverse nedir?](/powerapps/maker/data-platform/data-platform-intro)

Tümleştirmeyi kapattığınızda, kullanıcılar Human Resource veya Dataverse'te değişiklikler yapabilir ancak bu değişiklikler iki ortam arasında eşitlenmez.

Varsayılan olarak, Human Resources ve Dataverse arasındaki tümleştirme kapalıdır.

Aşağıdaki durumlarda tümleştirmeyi kapatmak isteyebilirsiniz:

- Verileri, Veri Yönetimi Çerçevesi aracılığıyla dolduruyorsunuzdur ve doğru bir duruma getirmek için verileri birçok defa içe aktarmanız gerekiyordur.

- Human Resources veya Dataverse'te verilerle ilgili sorunlar vardır. Tümleştirmeyi kapatırsanız, bir kaydı bir ortamda silip, diğerinde bırakabilirsiniz. Tümleştirmeyi yeniden açtığınız zaman, silme işlemi yapılmayan ortamdaki kayıt, silindiği ortama yeniden eşitlenir. **Dataverse tümleştirmesi - kaçırılan istek eşitleme** toplu işinin bir sonraki çalıştırılışında eşitleme başlar.

> [!WARNING]
> Veri tümleştirmeyi kapattığınızda, her iki ortamda aynı kaydı düzenlemediğinizden emin olun. Tümleştirmeyi yeniden açtığınızda, son düzenlediğiniz kayıt eşitlenir. Bu nedenle, her iki ortamda da kayıtta aynı değişiklikleri yapmadıysanız, veri kaybı oluşabilir.

## <a name="access-the-dataverse-integration-page"></a>Dataverse tümleştirme sayfasına erişim

1. Dataverse ile tümleştirme için ayarları görüntülemek veya yapılandırmak istediğiniz Human Resources kurulumunda **Sistem yönetimi** kutucuğunu seçin.

    [![Sistem yönetimi kutucuğu](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. **Bağlantılar** sekmesini seçin.

    [![Bağlantılar sekmesi](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. **Tümleştirmeler** altında, **Dataverse yapılandırması**'nı seçin.

    [![Dataverse yapılandırması bağlantısı](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a>Human Resources ve Dataverse arasında tümleştirmeyi açma veya kapatma

- Tümleştirmeyi etkinleştirmek için **Microsoft Dataverse tümleştirme** sayfasında **Dataverse tümleştirmesini etkinleştir** seçeneğini **Evet** olarak ayarlayın.

    > [!NOTE]
    > Tümleştirmeyi açarsanız, **Dataverse tümleştirmesi - kaçırılan istek eşitleme** toplu işinin bir sonraki çalıştırılışında veriler eşitlenir. Toplu iş tamamlandıktan sonra tüm veriler kullanılabilir hale gelecektir.

- Tümleştirmeyi kapatmak için, seçeneği **Hayır** olarak ayarlayın.

[![Dataverse tümleştirmesini açma veya kapatma](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)

> [!WARNING]
> Veri taşıma görevleri gerçekleştirirken Dataverse tümleştirmesini kapatmanız önerilir. Büyük veri yüklemeleri, performansı önemli ölçüde etkileyebilir. Örneğin, 2000 çalışan karşıya yüklemek, tümleştirme etkinleştirildiğinde birkaç saat sürebilir ve devre dışı bırakıldığında bir saatten az olabilir. Bu örnekte verilen sayılar yalnızca gösterim amaçlıdır. Kayıtları içe aktarmak için gereken tam süre birçok etkene göre büyük ölçüde değişebilir.

## <a name="view-data-integration-details"></a>Veri tümleştirme ayrıntılarını görüntüleme

**Microsoft Dataverse tümleştirmesi** sayfasının **Yönetim** hızlı sekmesinde, satırların Human Resources ile Dataverse arasında nasıl bağlandığını görebilirsiniz.

- Tablonun satırlarını görüntülemek için **Dataverse tablosu** alanında tabloyu seçin. Kılavuz, seçilen tablo ile bağlı tüm satırları gösterir.

> [!NOTE]
> Tüm Dataverse tabloları şu anda listelenmiyor. Kılavuzda yalnızca özel alanların kullanımını destekleyen tablolar görünür. Human Resources'nın sürekli sürümleri aracılığıyla yeni tablolar kullanılabilir hale gelir.

Kılavuz aşağıdaki alanları içerir:

- **Dataverse tablo** – Dataverse'teki tablonun adı.
- **Dataverse tablo başvurusu** – Bir kaydı tanımlamak için Dataverse kullanan tanımlayıcı. Bu değer Human Resources'taki bir **Kayıt kodu** değerinin eşdeğeridir. Dataverse tablosunu Microsoft Excel'de açtığınızda tanımlayıcıyı bulabilirsiniz.
- **Human Resources varlık adı** – Verileri Dataverse'e en son eşitleyen Human Resources varlığı. Varlık ya Dataverse öneki veya başka bir önek taşımalıdır.
- **Human Resources başvurusu** – Human Resources'taki kayıtla ilişkili **Kayıt kodu** değeri.
- **Dataverse'ten silindi** – Satırın Dataverse'ten silinip silinmediğini gösteren değer.

> [!NOTE]
> Human Resources'daki kayıtlar, Dataverse'teki satırlara karşılık gelir.

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a>Human Resources kaydının ilişkisini Dataverse satırından kaldırma

Human Resources ve Dataverse arasındaki veri eşitleme sırasında sorunlarla karşılaşırsanız, izlemeyi temizleyerek ve izleme tablosunun yeniden eşitlenmesine izin vererek bu sorunları çözebilirsiniz. İlişkilendirmeyi kaldırır ve sonra satırı Dataverse'te değiştirir veya silerseniz, değişiklikler Human Resources ile eşitlenmez. Human Resources'da değişiklik yaparsanız, yeni bir izleme kaydı oluşturulur ve satır Dataverse'te güncelleştirilir.

- Human Resources kaydının ve Dataverse satırının ilişkisini kaldırmak için **Dataverse tablosu** alanında tabloyu seçin ve ardından **İzleme bilgilerini temizle**'yi seçin.

[![İzleme bilgilerini temizleme](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)

İzlemeyi temizledikten sonra tabloda tam eşitleme çalıştırmak için sonraki yordama bakın.

## <a name="sync-a-table-between-human-resources-and-dataverse"></a>Human Resources ile Dataverse arasında tablo eşitleme

Bu yordamı şu durumlarda kullanın:

- Dataverse'taki değişikliklerin Human Resources'ta görünmesi çok uzun zaman aldığında.

- İzlemeyi temizledikten sonra izleme tablosunu yenilemeniz gerekir.

Human Resources ile Dataverse arasında bir tablonun tam eşitlemesini çalıştırmak için:

1. **Dataverse tablosu** alanında tabloyu seçin.

2. **Şimdi eşitle**'yi seçin.

[![Tam eşitleme çalıştırma](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)

## <a name="see-also"></a>Ayrıca bkz.

[Dataverse tabloları](hr-developer-entities.md)<br>
[Dataverse sanal tablolarını yapılandırma](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Human Resources sanal tablolarıyla ilgili SSS](hr-admin-virtual-entity-faq.md)<br>
[Microsoft Dataverse nedir?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Terminoloji güncelleştirmeleri](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
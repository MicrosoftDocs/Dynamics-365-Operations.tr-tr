---
title: Common Data Service tümleştirmesini yapılandırma
description: Common Data Service ve bir Microsoft Dynamics 365 Human Resources kurulumu arasında tümleştirmeyi açabilir veya kapatabilirsiniz. Ayrıca, eşitleme ayrıntılarını görüntüleyebilir, izleme verilerini temizleyebilir ve iki ortam arasındaki veri sorunlarının giderilmesine yardımcı olarak bir varlığı yeniden eşitleyebilirsiniz.
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
ms.openlocfilehash: 042daf3fdf7a906086af726472da050467d217e3
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010836"
---
# <a name="configure-common-data-service-integration"></a>Common Data Service tümleştirmesini yapılandırma

Common Data Service ve bir Microsoft Dynamics 365 Human Resources kurulumu arasında tümleştirmeyi açabilir veya kapatabilirsiniz. Ayrıca, eşitleme ayrıntılarını görüntüleyebilir, izleme verilerini temizleyebilir ve iki ortam arasındaki veri sorunlarının giderilmesine yardımcı olarak bir varlığı yeniden eşitleyebilirsiniz.

Tümleştirmeyi kapattığınızda, kullanıcılar Human Resource veya Common Data Service'te değişiklikler yapabilir ancak bu değişiklikler iki ortam arasında eşitlenmez.

Varsayılan olarak, Human Resources ile Common Data Service arasındaki tümleştirme, ortamlardaki tanıtım verilerinin varlığına bağlı olarak açık veya kapalıdır:

- Tanıtım verileri içermeyen yeni ortamlar için **Kapalı**
- Tanıtım verileri içeren yeni ortamlar için **Açık**

Tanıtım verileri içeren yeni ortamlar, verileri alınca eşitlemeye başlayacaktır.

Aşağıdaki durumlarda tümleştirmeyi kapatmak isteyebilirsiniz:

- Verileri, Veri Yönetimi Çerçevesi aracılığıyla dolduruyorsunuzdur ve doğru bir duruma getirmek için verileri birçok defa içe aktarmanız gerekiyordur.

- Human Resources veya Common Data Service'te verilerle ilgili sorunlar vardır. Tümleştirmeyi kapatırsanız, bir kaydı bir ortamda silip, diğerinde bırakabilirsiniz. Tümleştirmeyi yeniden açtığınız zaman, silme işlemi yapılmayan ortamdaki kayıt, silindiği ortama yeniden eşitlenir. **Common Data Service tümleştirmesi - kaçırılan istek eşitleme** toplu işinin bir sonraki çalıştırılışında eşitleme başlar.

> [!WARNING]
> Veri tümleştirmeyi kapattığınızda, her iki ortamda aynı kaydı düzenlemediğinizden emin olun. Tümleştirmeyi yeniden açtığınızda, son düzenlediğiniz kayıt eşitlenir. Bu nedenle, her iki ortamda da kayıtta aynı değişiklikleri yapmadıysanız, veri kaybı oluşabilir.

## <a name="access-the-common-data-service-integration-page"></a>Common Data Service tümleştirme sayfasına erişim

1. Common Data Service ile tümleştirme için ayarları görüntülemek veya yapılandırmak istediğiniz Human Resources kurulumunda **Sistem yönetimi** kutucuğunu seçin.

    [![Sistem yönetimi kutucuğu](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. **Bağlantılar** sekmesini seçin.

    [![Bağlantılar sekmesi](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. **Tümleştirmeler** altında, **Common Data Service yapılandırması**'nı seçin.

    [![Common Data Service yapılandırması bağlantısı](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a>Human Resources ve Common Data Service arasında tümleştirmeyi açma veya kapatma

- Tümleştirmeyi açmak için, **Common Data Service'e tümleştirmeyi etkinleştir** seçeneğini **Evet** olarak ayarlayın.

    > [!NOTE]
    > Tümleştirmeyi açarsanız, **Common Data Service tümleştirmesi - kaçırılan istek eşitleme** toplu işinin bir sonraki çalıştırılışında veriler eşitlenir. Toplu iş tamamlandıktan sonra tüm veriler kullanılabilir hale gelecektir.

- Tümleştirmeyi kapatmak için, seçeneği **Hayır** olarak ayarlayın.

[![Common Data Service tümleştirmesini açma veya kapatma](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)

## <a name="view-data-integration-details"></a>Veri tümleştirme ayrıntılarını görüntüleme

**Common Data Service tümleştirmesi** sayfasının **Yönetim** hızlı sekmesinde, kayıtların Human Resources ve Common Data Service arasında birbirlerine nasıl bağlandığını görebilirsiniz.

- Bir varlığın kayıtlarını görüntülemek için, **CDS varlığının adı** alanında varlığı seçin. Kılavuz, seçilen varlıkla bağlantılı tüm kayıtları gösterir.

[![Bir varlığın kayıtlarını görüntüleme](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)

> [!NOTE]
> Şu anda tüm Common Data Service varlıkları listede değildir. Yalnızca özel alanların kullanımını destekleyen varlıklar kılavuzda görünür. Human Resources'ın devam eden sürümleriyle yeni varlıklar sunuluyor.

Kılavuz aşağıdaki alanları içerir:

- **CDS varlığının adı** – Common Data Service'teki varlığın adı.
- **CD varlığı başvurusu** – Common Data Service'in bir kaydı belirlemek için kullandığı tanımlayıcı. Bu değer Human Resources'taki bir**Kayıt kodu** değerinin eşdeğeridir. Common Data Service varlığını Microsoft Excel'de açtığınız zaman tanımlayıcıyı bulabilirsiniz.
- **Human Resources varlığının adı** – Verileri Common Data Service'e en son eşitlenen varlık. Varlık ya Common Data Service öneki veya başka bir önek taşımalıdır.
- **Human Resources başvurusu** – Human Resources'taki kayıtla ilişkili **Kayıt kodu** değeri.
- **CDS'den silindi** – Kaydın Common Data Service'ten silinip silinmediğini gösteren bir değer.

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a>Human Resources'taki bir kaydın ilişkilendirmesini Common Data Service'tan kaldırma

Human Resources ve Common Data Service arasındaki veri eşitleme sırasında sorunlarla karşılaşırsanız, izlemeyi temizleyerek ve izleme tablosunun yeniden eşitlenmesine izin vererek bu sorunları çözebilirsiniz. İlişkilendirmeyi kaldırır ve Common Data Service'te bir kaydı değiştirir veya silerseniz, değişiklikler Human Resources'a eşitlenmez. Human Resources'ta değişiklikler yaparsanız yeni bir izleme kaydı oluşturulur ve kayıt Common Data Service'te güncelleştirilir.

- Human Resources ve Common Data Service arasında bir kaydın ilişkilendirmesini kaldırmak için, **CDS varlığının adı** alanında varlığı ve ardından **İzleme bilgilerini temizle**'yi seçin.

[![İzleme bilgilerini temizleme](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)

İzlemeyi temizledikten sonra varlıkta bir tam eşitleme çalıştırmak için, sonraki yordama bakın.

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a>Varlığı Human Resources ve Common Data Service arasında eşitleme

Common Data Service'teki değişikliklerin Human Resources'ta görünmesi çok uzun sürüyorsa veya izlemeyi temizledikten sonra izleme tablosunu yenilemeniz gerekiyorsa bu yordamı kullanın.

- Human Resources ve Common Data Service arasında bir varlık üzerinde tam eşitleme çalıştırmak için **CDS varlığının adı** alanında varlığı seçin ve **Şimdi eşitle**'yi seçin.

[![Tam eşitleme çalıştırma](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)



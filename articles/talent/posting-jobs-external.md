---
title: Attract'tan harici kariyer sitelerine iş yayımlama
description: Bu konuda Dynamics 365 Talent - Attract'i kullanarak harici işe alım sitelerinde nasıl ilan verilebileceği açıklanmaktadır
author: pganapmsft
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 2c822a1f799144bb9240fc0cbdeb6c5441e278af
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551415"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a>Attract'tan harici kariyer sitelerine iş yayımlama

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Talent: Attract, işlerinizi doğrudan Attract'ten Broadbean'e nakletmenize izin vererek gereksinim duyduğunuz yetenekleri elde etmenize yardımcı olur. [Bir iş oluşturduktan](./creating-jobs-attract.md) sonra, işinizi Broadbean'deki olası tüm iş adayları önüne koymak için bir düğmeye tıklamanız yeterlidir.

Projelerin Broadbean için deftere nakli uygun bir Broadbean lisansı gerektirir. Broadbean çeşitli ürün ve planlar sunar. Broadbean lisanslama ve fiyatlandırma hakkında daha fazla bilgi için [Broadbean'e başvurun](https://www.broadbean.com/contact-us/).

Attract ile Broadbean tümleştirmeyi konfigüre etme hakkında daha fazla bilgiye gereksinim duyan bir yöneticiniz varsa, [Harici iş panoları için ayar girme](./attract-admin-job-board-settings.md) bölümüne bakın.

## <a name="post-jobs-to-broadbean"></a>Broadbean'de iş ilanları yayınlama

Broadbean açıldıktan sonra, işe alımcılar ve yöneticiler buraya iş ilanı gönderebilirler. İş için bir başvur URL'sine sahip olmanız gerekir.

1. Attract içinde, Broadbean'e nakletmek istediğiniz işi açın.
2. **İlanlar** bölmesinde, Broadbean'e karşılık gelen **Şimdi İlan Ver** düğmesini seçin.
3. Broadbean penceresindeki talimatları izleyin.

Attract aşağıdaki bilgileri Broadbean'e aktarır:

- Talep Kodu
- İş unvanı
- İş açıklaması
- İş konumu
- Başvur URL'si
- İşe alan bilgileri

Broadbean ilan vermeyi başarıyla tamamladıktan sonra, Attract içindeki **İlanlar** bölümü, Broadbean durumunu **İlan verildi** olarak gösterir.

> [!NOTE]
> - Broadbean **Endüstri** alanına ihtiyaç duyar. Şu anda bu alan varsayılan olarak **BT** olarak ayarlanmıştır. Ancak, Broadbean iş ilanı verme sayfasında değeri doğru endüstriye değiştirebilirsiniz.
> - Broadbean'in iş ilanınızı seçtiğiniz tüm ilan panolarına göndermesi biraz zaman alır. Bu nedenle, Attract iş için bir durum güncelleştirmesi sağlamasından önce kısa bir gecikme olabilir.

### <a name="view-a-broadbean-job-posting"></a>Bir Broadbean iş ilanına göz atın

Bir işi Broadbean'e aktardıktan sonra, Attract içinden görüntüleyebilirsiniz.

1. Attract içinde, Broadbean'de görüntülemek istediğiniz işi açın.
2. **İlanlar** sekmesinde, Broadbeana'e karşılık gelen üç nokta düğmesini seçin (**...**) ve sonra **Görüntüle**'yi seçin.

Broadbean iş ilanı yeni pencerede görüntülenir.

### <a name="update-a-broadbean-job-posting"></a>Bir Broadbean iş ilanını güncelleştirin

Bir Broadbean işini iki şekilde güncelleştirebilirsiniz.

1. Attract içinde, güncelleştirmek istediğiniz işi açın.
2. **İlanlar** bölmesinde, Broadbean'e karşılık gelen **İlanı Güncelleştir** düğmesini seçin.
3. Broadbean penceresinde ilanı düzenleyin.

veya

1. Attract içinde, Broadbean'de görüntülemek istediğiniz işi açın.
2. **İlanlar** bölümünde, Broadbeana'e karşılık gelen üç nokta düğmesini seçin (**...**) ve sonra **Görüntüle**'yi seçin.
3. Broadbean penceresinde, iş ayrıntılarını düzenleyin ve işi yeniden ilan edin. Attract içindeki iş ayrıntıları değiştirilmez.

### <a name="remove-a-broadbean-job-posting"></a>Bir Broadbean iş ilanını kaldırın

Bir iş ilanını Broadbean'den ihtiyaç duyduğunuzda kaldırabilirsiniz.

1. Attract içinde, kaldırmak istediğiniz işi açın.
2. **İlanlar** bölümünde, Broadbeana'e karşılık gelen üç nokta düğmesini seçin (**...**) ve sonra **İlanı Kaldır**'ı seçin.

Broadbean işi kaldırdıktan sonra, Attract içindeki Broadbean öğesi bir **Şimdi İlan Ver** düğmesine sahip olur. Bu düğmenin varlığı, işin kaldırıldığını ve yeniden ilan verilebileceğini gösterir.

### <a name="troubleshoot-job-posting-to-broadbean"></a>Broadbean'e iş nakil sorunlarını gider

Bir işi Broadbean'e ilan vermekte zorluk çekiyorsanız şu adımları deneyin.

1. Attract içine girmiş olduğunuz Broadbean kimlik bilgilerinin doğru ve geçerli olduğunu doğrulayın.
2. Kimlik bilgileri geçerli ve doğruysa, [Broadbean destek](https://www.broadbean.com/resources/support/) ile iletişime geçin.
3. Sorun devam ederse, [Microsoft destek](./talent-support.md) ile iletişime geçin.

## <a name="see-also"></a>Ayrıca bkz.

[İşler oluşturma](./creating-jobs-attract.md)

[Harici iş panoları için ayarları girin](./attract-admin-job-board-settings.md)

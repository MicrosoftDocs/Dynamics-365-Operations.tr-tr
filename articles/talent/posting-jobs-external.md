---
title: Attract'tan harici kariyer sitelerinde iş ilanları yayınlama
description: Bu kon, harici işe alma sitelerine Dynamics 365 for Talent - Attract kullanarak ilan vermeyi açıklar
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
ms.openlocfilehash: 9c27d1810a89ed7d7a7745e41c5f118dbdfe5dda
ms.sourcegitcommit: cadce85ca3004d53caf6bc49147a524c1bfd421f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/16/2019
ms.locfileid: "1590494"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a>Attract'tan harici kariyer sitelerinde iş ilanları yayınlama

[!include [banner](../includes/banner.md)]

Açık pozisyonlarınızı olabildiğince fazla kalifiye adayın önüne sunmak istersiniz. Broadbean gibi işe alma siteleri bu hedefinizi gerçekleştirmeye yardımcı olur. Microsoft Dynamics 365 Talent: Attract, şimdi Broadbean'e iş ilanları vermenize olanak sağlar ve Microsoft düzenli olarak bu alanda yeni olanaklar sağlar.

## <a name="post-jobs-to-broadbean"></a>Broadbean'e iş ilanları vermek

Broadbean'e iş ilanları verebilmeden önce, Broadbean tümleştirmesini yapılandırmanız gerekir.

> [!NOTE]
> - Harici sitelere iş ilanı verebilmek için [Kapsamlı işe alma eklentisine](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) sahip olmanız gerekir.
> - Attract üzerinden Broadbean'a iş göndermek için bir Broadbean aboneliğine sahip olmanız gerekir.
> - Bu özellik şu anda önizlemededir. Denemek isterseniz, [Attract yönetici ayarlarında açmanız gerekir](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).

### <a name="configure-broadbean-integration"></a>Broadbean tümleştirmesini yapılandırın

1. Attract'e bir yönetici olarak oturum açın.
2. **Ayarlar** düğmesini (çark simgesi) sayfanın sağ üst köşesinde seçin ve sonra **Yönetici merkezini** seçin.
3. **İş panosu ayarları** sekmesinde, **Broadbean tümleştirmesini etkinleştir** bölmesinde, tümleştirmeyi açın.
4. Broadbean ile iletişime geçin ve **Kullanıcı adı, İstemci Kimliği, Şifreleme Belirteci** içerisine bilgilerinizi girin.

> [!WARNING]
> Broadbean kimlik bilgileriniz hassas ve gizlidir. Bu nedenle, bunları dikkatli bir biçimde depolayın ve paylaşın. Attract içinde Yönetici rolüne sahip herkes bu kimlik bilgilerini görebilir.

> [!NOTE]
> Microsoft ve Attract, bu değerleri oluşturmak ve saklanmakta söz sahibi değildir. Attract için bunları güncel tutmak ve kimlik bilgileriniz içeren herhangi bir sorunu Broadbean ile işbirliği yaparak çözmek sizin sorumluluğunuzdur.

### <a name="post-a-job-to-broadbean"></a>Broadbean'e bir iş ilanı vermek

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
2. **İlanlar** bölümünde, Broadbeana'e karşılık gelen üç nokta düğmesini seçin (**...**) ve sonra **Görüntüle**'yi seçin.

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

### <a name="troubleshoot-the-broadbean-integration"></a>Broadbean tümleştirmesi ile ilgili sorunları giderme

Bir işi Broadbean'e ilan vermekte zorluk çekiyorsanız şu adımları deneyin.

1. Attract içine girmiş olduğunuz Broadbean kimlik bilgilerinin doğru ve geçerli olduğunu doğrulayın.
2. Kimlik bilgileri geçerli ve doğruysa, [Broadbean destek](https://www.broadbean.com/resources/support/) ile iletişime geçin.
3. Sorun devam ederse, [Microsoft destek](./talent-support.md) ile iletişime geçin.

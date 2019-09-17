---
title: Dynamics 365 for Talent - Onboard kullanarak işe alım süreci kılavuzu oluşturma ve gönderme
description: Bu konu, yeni işe alım kılavuzu oluşturmak üzere Microsoft Dynamics 365 for Talent - Onboard uygulamasının nasıl kullanılacağını açıklamaktadır. Bu görev, insan sermaye yönetimi (HCM) için işe alma stratejisindeki temel bir ilk adımdır.
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: de5d584e3b7edba2751aa0c83b0465df2c3e4f7d
ms.sourcegitcommit: 9f762fa89c5b432667aa156c22d679a7f601952d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/08/2019
ms.locfileid: "1731682"
---
# <a name="create-and-send-an-onboarding-guide-by-using-dynamics-365-for-talent-onboard"></a>Dynamics 365 for Talent: Onboard kullanarak işe alım süreci kılavuzu oluşturma ve gönderme

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 for Talent: Onbord, yerleşik kendi oluşturduğunuz şablonlardan, bir galerideki şablonlardan veya sıfırdan iş alım kılavuzları oluşturmanıza olanak sağlar.

Bir ekleme kılavuzu oluşturduktan sonra, bunu yeni bir işe alıma gönderebilirsiniz. Alternatif olarak, Onboard uygulamasından yüklediğiniz bir Microsoft Excel dosyada belirttiğiniz birden çok yeni işe alınana gönderebilirsiniz.

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-a-single-new-hire"></a>Şablondan ekleme kılavuzu oluşturma ve bunu tek bir yeni işe alınana gönderme

1. Sol menüde **Şablonlar**'ı seçin.
2. Yeni işe alma için ekleme kılavuzu olarak ayarlamak istediğiniz şablonu **Şablonlarım** altında seçin.
3. Şablonu istediğiniz gibi düzenleyin. Ayrılırken çalışmanızı düzenli olarak kaydedin.
4. Şablonu düzenlemeyi bitirdiğinizde **Kılavuz oluştur**'u seçin.

    [![Şablondan işe alım kılavuzu oluşturma](./media/onboard-create-guide.png)](./media/onboard-create-guide.png)

5. **Kılavuz Oluştur** penceresinde, **Kimin için işe alım süreci gerçekleştiriyorsunuz?** altında yeni işe alma adını veya e-posta adresini girin. Yeni işe alma henüz sistemde değilse, **Şimdi ekle**'yi seçin ve çalışanın bilgilerini girin.

    ![[İşe Alım Kılavuzu ile ilgili bilgileri girme](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

6. **Ne zaman başlar**ın altında, bir başlangıç tarihi seçin.
7. Ekleme kılavuzunun belirli bir tarihteki yeni işe alma için otomatik olarak gönderilmesi gerekiyorsa, **otomatik gönderme tarihi planla**seçeneğinin açık olduğundan emin olun ve sonra otomatik gönderme tarihini seçin. Kılavuzu hemen göndermek için, **otomatik gönderme tarihi planla** seçeneğini kapatın.
8. **Tamam**'ı seçin.
9. İşe alım kılavuzunu düzenlemeyi bitirdiğinizde, sağ üst köşedeki **gönder**'i seçin. Ardından şu adımlardan birini izleyin:

    - Yeni işe alınana işe alım kılavuzu için bir bağlantı göndermek için, **bağlantı kopyala**'yı seçin ve sonra **Kopyala**'yı seçin.
    - Göndermeden önce işe alım kılavuzunun e-postasını özelleştirmek için, **Göndermeden önce e-postayı özelleştir**'i seçin, **İleri**'yi seçin, istediğiniz gibi e-postayı özelleştirin ve sonra **Gönder**'i seçin.
    - E-postayı özelleştirmeden göndermek için **İleri**'yi seçin ve sonra **Gönder**'i seçin.

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-multiple-new-hires"></a>Şablondan ekleme kılavuzu oluşturma ve bunu birden çok yeni işe alınana gönderme

Onboard, birden çok yeni işe alınana aynı anda işe alım kılavuzu göndermenize olanak sağlar.

1. Sol menüde **Şablonlar**'ı seçin.
2. Yeni işe alma için ekleme kılavuzu olarak ayarlamak istediğiniz şablonu **Şablonlarım** altında seçin.
3. Şablonu istediğiniz gibi düzenleyin. Ayrılırken çalışmanızı düzenli olarak kaydedin.
4. Şablonu düzenlemeyi bitirdiğinizde **Kılavuz oluştur**'u seçin.
5. **Kılavuz Oluştur** penceresinde, **aynı anda birden fazla kişinin işe alımı gerekli**yi seçin.

    [![Birden çok yeni işe alım için işe alma kılavuzu oluşturuluyor](./media/onboard-send-guide-multiple-people.png)](./media/onboard-send-guide-multiple-people.png)

6. **Yeni işe alma şablonu**seçin.
7. .Xlsx dosyası indirildikten sonra, **aç**'ı seçin, çalışanların bilgilerini Excel çalışma kitabına girin ve çalışma kitabını kaydedin.

    [![Birden çok yeni alım için işe alma kılavuzu göndermek için Excel şablonu indiriliyor](./media/onboard-send-guide-download-spreadsheet.png)](./media/onboard-send-guide-download-spreadsheet.png)

    > [!NOTE]
    > Çalışma kitabını düzenlemeden önce Excel'de **düzenlemeyi etkinleştir**'i seçmelisiniz.
    > 
    > [![Düzenlemeyi etkinleştirme](./media/onboard-send-guide-enable-editing.png)](./media/onboard-send-guide-enable-editing.png)

8. Excel çalışma kitabını **Birden çok kılavuz oluştur** penceresinde belirlenen alana sürükleyin veya bilgisayarınızdaki dosyaya gözatmak için o alandaki herhangi bir yeri tıklatın.

    [![Düzenlenen çalışma kitabını sürükleme](./media/onboard-send-guide-drag-spreadsheet.png)](./media/onboard-send-guide-drag-spreadsheet.png)

9. İşe alım kılavuzunu düzenlemeyi bitirdiğinizde, sağ üst köşedeki **gönder**'i seçin. Ardından şu adımlardan birini izleyin:

    - Yeni işe alınana işe alım kılavuzu için bir bağlantı göndermek için, **bağlantı kopyala**'yı seçin ve sonra **Kopyala**'yı seçin.
    - Göndermeden önce işe alım kılavuzunun e-postasını özelleştirmek için, **Göndermeden önce e-postayı özelleştir**'i seçin, **İleri**'yi seçin, istediğiniz gibi e-postayı özelleştirin ve sonra **Gönder**'i seçin.
    - E-postayı özelleştirmeden göndermek için **İleri**'yi seçin ve sonra **Gönder**'i seçin.

## <a name="create-a-guide-without-using-a-template"></a>Şablon kullanmadan kılavuz oluştur

Bir şablondan her zaman bir kılavuz oluşturmak zorunda değilsiniz. İsterseniz, bunun yerine bir kılavuzu baştan yapabilirsiniz.

1. Sol menüde **kılavuzlar**'ı seçin ve sonra **Ekle** düğmesini (artı işareti \[**+**\]) seçin.
2. **Kılavuz Oluştur** penceresinde, **Kimin için işe alım süreci gerçekleştiriyorsunuz?** altında yeni işe alma adını veya e-posta adresini girin. Yeni işe alma henüz sistemde değilse, **Şimdi ekle**'yi seçin ve çalışanın bilgilerini girin.

    ![[İşe Alım Kılavuzu ile ilgili bilgileri girme](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

3. **Ne zaman başlar**ın altında, bir başlangıç tarihi seçin.
4. Ekleme kılavuzunun belirli bir tarihteki yeni işe alma için otomatik olarak gönderilmesi gerekiyorsa, **otomatik gönderme tarihi planla**seçeneğinin açık olduğundan emin olun ve sonra otomatik gönderme tarihini seçin. Kılavuzu hemen göndermek için, **otomatik gönderme tarihi planla** seçeneğini kapatın.
5. **Tamam**'ı seçin.

## <a name="save-a-guide-as-a-template"></a>Kılavuzu şablon olarak kaydet

İşe alım kılavuzunu şablon olarak kaydedebilirsiniz. Bu şekilde, daha sonra daha fazla işe alım kılavuzu oluşturmanız gerektiğinde zamandan tasarruf edebilirsiniz.

1. Sol menüde **Kılavuzlar**'ı seçin.
2. **Diğer** düğmesini (üç nokta \[**...**\]) şablon oluşturmak istediğiniz kılavuz için, **şablon olarak kaydet**'i seçin.

    ![[Ekleme kılavuzunu şablon olarak kaydetme](./media/onboard-save-guide-as-template.png)](./media/onboard-save-guide-as-template.png)

3. **Yeni şablon olarak kaydet** penceresinde, yeni şablonunuz için bir ad girin ve sonra **Kaydet**'i seçin.

## <a name="next-steps"></a>Sonraki adımlar

- [İşe alım kılavuzları ve şablonları düzenleme](./onboard-edit-guides-templates.md)
- [İçeriği diğer katkıda bulunanlarla paylaşın](./onboard-share-template.md)
- [Görevlerin ve işe alınan çalışanların durumunu görüntüleme](./onboard-view-status.md)
- [Onboard'da işe alma ekipleri oluşturun](./onboard-create-team.md)

### <a name="see-also"></a>Ayrıca bkz.

- [Onboard uygulamasını deneyin veya satın alın](https://dynamics.microsoft.com/talent/onboard/)
- [Yenilikler](./whats-new.md)
- [Sürüm notları](https://docs.microsoft.com/business-applications-release-notes/index)
- [Destek alma](./talent-support.md)

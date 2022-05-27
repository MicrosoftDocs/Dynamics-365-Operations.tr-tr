---
title: Kişisel bilgileri düzenle
description: Bu makalede, Personel ve Yönetici self servisindeki kişisel bilgilerin nasıl düzenleneceği açıklanmaktadır.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d7e78873d0995334ac80ac22e8058b7fe0bc31ac
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686150"
---
# <a name="edit-personal-information"></a>Kişisel bilgileri düzenle


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Kişisel bilgilerinizi Dynamics 365 Human Resources uygulamasındaki **Personel self servisi** çalışma alanında düzenleyebilirsiniz.

Düzenleyebileceğiniz kişisel bilgiler şunları içerir:

- Adresler
- İlgili kişi ayrıntıları
- Kişisel ilgili kişiler
- Kimlik numaraları
- Ödeme yöntemi
- İnsan Kaynakları'nda kullanılan görüntü

>[!NOTE]
>İlgili kişi bilgileri gibi belirli türde kişisel bilgileri düzenleyemeyebilirsiniz. Daha fazla bilgi için bkz. [Kişisel bilgileri düzenlemeyi kısıtlama](hr-employee-self-service-restrict-editing.md).

**Genel adres defteri parametreleri** sayfasında ayarlanan parametreler, hangi rollerin kişisel bilgilerinizi görebileceğini belirler.

1. İnsan Kaynakları, **çalışan Self servis**'ı seçin.

2. **Kişisel ayrıntıları düzenle** seçin.

3. Adresinizi değiştirmek için **adresler** sekmesini seçin. yaptığınız değişiklikler, **personel yönetimi** çalışma alanında HR için görünür.

    - Yeni bir adres eklemek için **Ekle**'ye tıklayın.
    - Varolan bir adresi düzenlemek için, adresi seçin ve **Düzenle** seçin.
    - Haritayı görüntülemek için **Harita**'yı seçin.
    - Bir kişi eklemek veya kaldırmak için, **diğer Seçenekler** seçeneğini belirleyin ve sonra **Gelişmiş**'i seçin. İlgili **kişi bilgileri** altında, gerekli alanları **Ekle** veya **Kaldır** ve Düzenle 'yi seçin.
    - Saat diliminizi ve konumunuzu ayarlamak için **daha fazla seçenek** belirleyip **Gelişmiş**'i seçin. **Genel** altında, alanları gerektiği gibi düzenleyin.

4. İlgili kişi ayrıntılarını değiştirmek için **ilgili kişi ayrıntıları** sekmesini seçin. Telefon, e-posta ve sosyal medya bağlantıları gibi farklı türlerde iletişim bilgileri sağlayabilirsiniz. İlgili kişi ayrıntısını birincil olarak ayarlayabilirsiniz, ancak yalnızca her türden birini birincil olarak ayarlayabilirsiniz.

    - Yeni bir iletişim bilgisi eklemek için **Ekle**'ye tıklayın. Alanları gerektiği gibi düzenleyin.
    - Varolan bir iletişim bilgisini düzenlemek için, öğeyi seçin ve **Düzenle** seçin. Alanları gerektiği gibi düzenleyin.
    - İlgili kişi ayrıntısını özel olarak ayarlamak için, maddeyi seçin, **Gelişmiş**'i seçin ve sonra **özel** geçişi **Evet** olarak ayarlayın. **Tamam**'ı seçin.
      >[!NOTE]
      >Yöneticiniz ortamınızda **(Önizleme) Çalışanların belirli amaçlar için adres ve kişi bilgilerini eklemesini veya düzenlemesini kısıtlama** özelliğini etkinleştirdiyse **Gelişmiş** düğmesi kullanılamaz. Daha fazla bilgi için bkz. [Kişisel bilgileri düzenlemeyi kısıtlama](hr-employee-self-service-restrict-editing.md).
  
5. Özel kişilerinizi değiştirmek için, **kişisel kişiler** sekmesini seçin. Acil durumda ulaşılacak ilgili kişiler, lehdarlar ve Etkilenenleri belirleyebilirsiniz. İlgili kişi, kişi veya organizasyon olabilir. **Sosyal haklar yönetimi** özelliği, kişisel iletişim bilgilerini kullanır. Daha fazla bilgi için bkz. [Kişisel iletişim uygunluk seçeneklerini yapılandırma](hr-benefits-setup-contact-eligibility-options.md).

6. Sosyal Güvenlik Numarası gibi kimlik numaralarınızı değiştirmek için **kimlik numaraları** sekmesini seçin. Kuruluşunuz bir onay iş akışı ayarlayacaksa değişiklikler onay işlemi ile geçebilir.

    - Kimlik numarası eklemek için **Yeni**'yi seçin. Gerekli alanları doldurun ve **Kaydet**'i seçin.
    - Bir numarayı düzenlemek için **Düzenle** seçin. Gerekli alanları düzenleyin ve **Kaydet**'i seçin.

7. Ödeme yapmak istediğiniz yöntemleri değiştirmek için **Ödeme bilgilerim** sekmesini seçin. Bu sekme yalnızca **Human Resources parametreleri** sayfasında ödeme yöntemleri etkinleştirilmişse kullanılabilir. HR **banka taslağını**, **nakit**, **çek**, **elektronik ödeme** veya **diğerini** etkinleştirebilir. HR ayrıca elektronik ödeme doğrulamasını (ABD maaş için kullanılır), banka hesabı ve rota numarası doğrulamasını da devre dışı bırakabilir.

8. Profiliniz için İnsan Kaynakları görüntülenen resmi değiştirmek için, **görüntü** sekmesini seçin. Organizasyonunuzun ayarlarına bağlı olarak, resimler onay için yönlendirilebilir.

    - Resim karşıya yüklemek için **yeni resim yükle**'yi seçin.
    - Görüntüyü kaldırmak için, görüntüyü seçin ve **Kaldır**'ı seçin.



[!INCLUDE[footer-include](../includes/footer-banner.md)]

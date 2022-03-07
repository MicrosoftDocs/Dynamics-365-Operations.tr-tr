---
title: Satıcı faturalarını içeri aktarmak için elektronik faturalama hizmetini kullanma
description: Bu konuda, Elektronik Faturalama hizmetini kullanarak satıcı faturalarını içeri aktarma hakkında bilgi sağlanmaktadır.
author: gionoder
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 434bf1f6a5a727a71592493b85ab166cbeff2f0980c2c968c99973a03f4dc660
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751264"
---
# <a name="use-the-electronic-invoicing-service-to-import-vendor-invoices"></a>Satıcı faturalarını içeri aktarmak için elektronik faturalama hizmetini kullanma

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Bu konuda, Elektronik Faturalama hizmetini kullanarak satıcı faturalarını içeri aktarmaya başlamanıza yardımcı olacak bilgiler sağlanmaktadır. Bu, satıcılardan elektronik satıcı faturaları almak için izlemeniz gereken Regulatory Configuration Services (RCS), Dynamics 365 Finance ve Dynamics 365 Supply Chain Management'taki yapılandırma adımları üzerinden size yol gösterir.

## <a name="set-up-vendor-invoice-import-in-rcs"></a>RCS'de satıcı faturasını içeri aktarmayı ayarlama
RCS'de satıcı faturasını içeri aktarmayı ayarlamak için şu adımları izleyin:

1. [Genel olarak kullanılabilir Elektronik faturalama özellikleri](e-invoicing-configuration-rcs.md#generally-available-features) listesine başvurun.
2. Elektronik faturalama özelliğini seçip içeri aktarın. Daha fazla bilgi için bkz. [Microsoft yapılandırma sağlayıcısından Elektronik faturalama özelliğini içeri aktarma](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider).
3. Kuruluşunuz için Elektronik faturalama özelliği oluşturun. Daha fazla bilgi için bkz. [Kuruluş sağlayıcınız altında Elektronik faturalama özelliği oluşturma](e-invoicing-get-started.md#create-an-electronic-invoicing-feature-under-your-organization-provider).

## <a name="configure-an-email-account-channel"></a>E-posta hesabı kanalı yapılandırma

Oluşturduğunuz Elektronik faturalama özelliği e-posta ile alınan ekli dosyalardan elektronik satıcı faturalarını içeri aktarıyorsa bir e-posta hesabı kanalı yapılandırın.

1. RCS'de, oluşturduğunuz Elektronik faturalama özelliğini seçin. **Taslak** durumunda olan sürümü seçtiğinizden emin olun.
2. **Kurulumlar** sekmesinde, ızgarada bir özellik kurulumu seçin ve ardından **Düzenle** seçeneğini belirleyin.
3. **Veri kanalı** sekmesinde **Parametreler** alan grubunda **Sunucu adresi**'ni seçin ve e-posta hesabı sağlayıcısını girin.
4. **Sunucu bağlantı noktası**'nı seçin ve e-posta hesabı sağlayıcısı tarafından kullanılan bağlantı noktasını girin.
5. **Kullanıcı adı gizli anahtarı**'nı seçin ve e-posta kullanıcı hesabının kimliğini içeren Anahtar kasası gizli anahtarının adını girin.
6. **Kullanıcı parolası gizli anahtarı**'nı seçin ve e-posta kullanıcı hesabının parolasını içeren Anahtar kasası gizli anahtarının adını girin.
7. **Konu filtresi**'ni seçin. İçeri aktarılacak elektronik satıcı faturasını içeren e-postayı tanımlamak için varsayılan e-posta konusunu içeren dizeyi inceleyip güncelleştirin.
8. **Uygulanabilirlik kuralları** sekmesinde, gerekirse ölçütü inceleyip güncelleştirin. Daha fazla bilgi için bkz. [Uygulanabilirlik kuralları](e-invoicing-configuration-rcs.md#applicability-rules).
9. **Kaydet**'i seçip sayfayı kapatın.

### <a name="configure-a-microsoft-sharepoint-channel"></a>Microsoft SharePoint kanalı yapılandırma

Elektronik faturalama özelliği SharePoint klasörlerinde bulunan dosyalardan elektronik satıcı faturalarını içeri aktarıyorsa bir Microsoft SharePoint kanalı yapılandırın.

1. RCS'de, oluşturduğunuz Elektronik faturalama özelliğini seçin. **Taslak** durumunda olan **Sürüm**'ü seçtiğinizden emin olun.
2. **Kurulumlar** sekmesinde, ızgarada bir Özellik kurulumu seçin ve ardından **Düzenle** seçeneğini belirleyin.
3. **Veri kanalı** sekmesinde **Parametreler** alan grubunda **SharePoint adresi**'ni seçin ve SharePoint URL'sini girin.
4. **Sunucu bağlantı noktası**'nı seçin ve e-posta hesabı sağlayıcısı tarafından kullanılan bağlantı noktasını girin.
5. **Uygulama Kimliği**'ni seçin ve SharePoint istemcisinin kimliğini içeren Anahtar kasası gizli anahtarının adını girin.
6. **Uygulama gizli anahtarı**'nı seçin ve SharePoint istemcisinin parolasını içeren Anahtar kasası gizli anahtarının adını girin.
7. **Dosya filtresi**'ni seçin. İçeri aktarılacak elektronik satıcı faturasını içeren dosyaları filtrelemek için maskeyi inceleyip güncelleştirin.
8. **Uygulanabilirlik kuralları** sekmesinde, gerekirse ölçütü inceleyip güncelleştirin. Daha fazla bilgi için bkz. [Uygulanabilirlik kuralları](e-invoicing-configuration-rcs.md#applicability-rules).
9. **Kaydet**'i seçip sayfayı kapatın

### <a name="deploy-an-electronic-invoicing-feature"></a>Elektronik faturalama özelliği dağıtma

Elektronik faturalama özelliğini dağıtmak için bkz. [Elektronik faturalama özelliğini Servis ortamına dağıtma](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment).

## <a name="set-up-vendor-invoice-import-in-finance-and-supply-chain-management"></a>Finance ve Supply Chain Management'ta satıcı faturasını içeri aktarmayı ayarlama
Farklı satıcı faturasını içeri aktarma türlerini ayarlamak için aşağıdaki iki bölümde yer alan adımları tamamlayın.

### <a name="import-vendor-invoices-from-email"></a>E-postadaki satıcı faturalarını içeri aktarma

1. Finance veya Supply Chain Management ortamınızda oturum açın ve doğru tüzel kişilikte olduğunuzu doğrulayın.
2. **Kuruluş yönetimi** > **Kurulum** > **Elektronik belge parametreleri** bölümüne gidin.
3. **Özellikler** sekmesinde, **NF-e Federal - Brezilya elektronik faturası**'nın seçili olduğundan emin olun.
4. **Harici kanallar** sekmesinde, **Kanallar** alan grubunda **Ekle**'yi seçin.
5. **Kanal** alanında, **NFe** (RCS'de Elektronik faturalama özelliği için veri kanalının yapılandırmasında verilen kanalın adı) öğesini girin.
6. **Açıklama** alanına bir açıklama girin. **Şirket** alanında, tüzel kişiliği seçin.
7. **Belge bağlamı** alanında, **Mali belge bağlamı - Müşteri faturası bağlam modeli**'ni seçin.
8. **Kaynakları içeri aktar** alan grubunda, **Ekle**'yi seçin.
9. **Ad** alanında, **XmlFile** (RCS'de Elektronik faturalama özelliği için veri kanalının yapılandırmasında verilen **Ek filtresi**'nin adı) öğesini girin.
10. **Açıklama** alanında, bir açıklama girin ve **Veri varlığı adı** alanında, **Alınan NF-e XML belgeleri**'ni seçin.
11. **Model eşleme** alanında, **NF-e postası içeri aktarma – NF-e e-postası içeri aktarma (BR)** seçeneğini belirleyin ve ardından **Kaydet**'i seçin.
12. **Elektronik belge** sekmesinde, **Elektronik raporlama** alan grubunda **Ekle**'yi seçin ve **Tablo adı** alanında, **Alınan NF-e XML belgesi**'ni seçin.
13. **Belge bağlamı** alanında, **Mali belge bağlamını sorgula - Müşteri faturası bağlamı**'nı seçin.
14. **Elektronik belge modeli eşlemesi** alanında, **Eşlemeyi sorgula – Mali belge eşlemesi**'ni seçin.
15. **Yanıt türlerini** seçin ve ardından **yeni**'yi seçin.
16. **Yanıt türü** alanında, **Yanıt**'ı girin. **Gönderim durumu** alanında, **Planlandı**'yı girin.
17. **Model eşleme** alanında, **Yanıt iletisinden model eşlemesi - Yanıt iletisi içeri aktarma biçimi**'ni seçin.
18. **Kaydet**'i seçip sayfayı kapatın.

### <a name="import-peppol-electronic-vendor-invoices"></a>PEPPOL elektronik satıcı faturalarını içeri aktarma

1. **Elektronik raporlama** çalışma alanına gidin ve **Raporlama yapılandırmaları**'nı seçin.
2. **Müşteri faturası bağlam modeli**'ni seçin ve türetilmiş bir yapılandırma oluşturun.
3. **Taslak** sürümünde, **Tasarımcı**'yı seçin.
4. **Veri modeli** ağacında, **Müşteri faturası**'nı seçin ve ardından **Modeli veri kaynağına eşle** seçeneğini belirleyin.
5. **Tanımlar** ağacında, **CustomerInvoice** öğesini ve ardından **Tasarımcı**'yı seçin.
6. **Veri kaynakları** ağacında, **Bağlam\_Kanal**'ı seçin. **Değer** alanında, **PEPPOL**'u seçin. Bu, RCS'de Elektronik faturalama özelliği için veri kanalının yapılandırmasında verilen kanalın adıdır. 
7. **Kaydet**'i seçip sayfayı kapatın.
8. Sayfayı kapatın.
9. **Müşteri faturası bağlam modeli**'ni seçin ve **Sürümler** hızlı sekmesinde, **Durumu Değiştir** > **Tamamlandı**'yı seçin.
10. **Kuruluş yönetimi** > **Kurulum** > **Elektronik belge parametreleri**'ne gidin ve **Özellikler** sekmesinde, **PEPPOL Genel elektronik faturaları**'nın seçili olduğundan emin olun. 
11. **Harici kanallar** sekmesinde, **Kanallar** alan grubunda **Ekle**'yi seçin.
12. **Kanal** alanında, **PEPPOL**'u girin. **Açıklama** alanına bir açıklama girin.
13. **Şirket** alanında, tüzel kişiliği seçin. **Belge bağlamı** alanında, **Müşteri faturası bağlamı - Müşteri faturası bağlam modeli**'ni seçin.
14. **Kaydet**'i seçip sayfayı kapatın.


## <a name="receive-electronic-invoices"></a>Elektronik faturalar alma
Elektronik faturaları almak için şu adımları izleyin:

1. **Kuruluş yönetimi** > **Periyodik** > **Elektronik belgeler** > **Elektronik belgeleri al**'a gidin.
2. **Tamam**'ı seçip sayfayı kapatın.

## <a name="view-receive-logs-for-electronic-invoices"></a>Elektronik faturalar için alma günlüklerini görüntüleme

Elektronik faturalar için alma günlüklerini görüntülemek üzere **Kuruluş yönetimi** > **Periyodik** > **Elektronik belgeler** > **Elektronik belge alma günlüğü**'ne gidin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

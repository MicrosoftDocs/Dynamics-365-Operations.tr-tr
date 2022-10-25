---
title: Invoice Capture çözümünü yapılandırma
description: Bu makalede, Invoice Capture çözümünün nasıl yapılandırılacağı anlatılmaktadır.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: e297dafc930368f14f2e68213ce4153ba792ef4d
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691243"
---
# <a name="configure-the-invoice-capture-solution"></a>Invoice Capture çözümünü yapılandırma

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Invoice Capture çözümü yüklendikten sonra, ortamı yapılandırmanız gerekir. İşlem, aşağıdaki temel adımlardan oluşur:

1. **Gerekli:** Microsoft Dynamics 365 Finance'tan tüzel varlıkları eşitleyin. Bu adım, organizasyon yapısını Microsoft Power Platform'da ayarlamak için kullanılır.
2. **Gerekli:** Fatura görüntülerinin içe aktarılması için kanalları yapılandırın. Çözüm aşağıdaki kanalları destekler:

    - Office 365 Outlook (varsayılan)
    - Outlook.com
    - OneDrive
    - SharePoint

3. **İsteğe bağlı:** Optik karakter tanıma (OCR) servisi için ek konfigürasyon gruplarını tanımlayın.
4. **İsteğe bağlı:** Tüzel kişi, satıcı hesabı, öğe ve tedarik türü için eşleme kurallarını tanımlayın.

Bu makale, işlemin gerekli iki adımına odaklanır. Yapılandırma grupları hakkında daha fazla bilgi için bkz. [Invoice Capture çözümü yapılandırma grupları](invoice-capture-config-group.md). Eşleme kuralları hakkında daha fazla bilgi için bkz. [Invoice Capture çözümü eşleme kuralları](invoice-capture-mapping-rules.md).

## <a name="manage-legal-entities"></a>Tüzel kişilikleri yönetme

Finance, yasal yetkililerle kayıt yoluyla tanımlanan kuruluşlar olarak tüzel kişilikleri tanımlar. İş faaliyetleri, ayrı tüzel kişiliklerde gerçekleştirilir ve kaydedilir. Microsoft Power Platform'da iş birimleri, güvenlik rolleri ve kullanıcılar, rol tabanlı güvenlik modeline uygun bir şekilde birbirine bağlanır.

İş birimleri, veri erişimini denetlemek için güvenlik rolleriyle birlikte kullanılır. Kullanıcılar yalnızca işlerini yapmak için ihtiyaç duydukları bilgileri görürler. Invoice Capture çözümü, Finance içindeki mevcut tüzel kişiliklerden temel bilgileri yükleyebileceğiniz ve manuel olarak oluşturulan varlıkları yönetebileceğiniz bir konfigürasyon alanı sağlar. Tüzel kişilikler, satıcı faturalarında ve güvenlik kontrolünde kullanılır.

Bir tüzel kişilik oluşturulduğunda ve liste görünümünde gösterildiğinde, aynı ada sahip varsayılan bir iş birimi otomatik olarak oluşturulur. Ekibe **AP memuru** güvenlik rolü verilir. Tüzel kişilikler içe aktarıldığında, Finance'taki temel master veriler içe aktarılır. Mevcut olmayan öğeler, tüzel kişilik tarafından tanımlanır ve Invoice Capture çözümüne eklenir. Varsayılan yapılandırma grubu yeni tüzel kişiliklere atanır.

### <a name="sync-legal-entities"></a>Tüzel kişilikleri eşitleme

Tüzel kişilikleri doğrudan ekleyemezsiniz. Ancak tüzel kişilikleri Finance'tan eşitleyebilirsiniz. Tüzel kişilikleri eşitlemek için bu adımları izleyin.

1. **Kurulum \> Sistem kurulumu \> Tüzel kişilikleri yönetme** bölümüne gidin.
2. **Tüzel kişilikleri eşitle**'yi seçin ve ardından onay diyalog kutusunda **Tamam**'ı seçin.

Eşitleme tamamlandıktan sonra, yeni tüzel kişiliklerin numarası gösterilir. Yeni tüzel kişilikler, liste görünümünde gösterilir. Varsayılan yapılandırma grubu yeni tüzel kişiliklere atanır.

## <a name="configure-invoice-import-channels"></a>Fatura içe aktarma kanalları yapılandırma

Satıcılar, faturaları farklı kanallardan (e-posta, dosya çalışma alanı veya fatura portalı) farklı formatlarda (kağıt veya resim) gönderir. Invoice Capture çözümü, farklı kanalları ve formatları işleyebilir. Aşağıdaki türler desteklenir:

- Office 365 Outlook
- Outlook.com
- SharePoint
- OneDrive

Belirli bir hesap için kanal oluşturulduğunda, gelen kutusundaki veya alandaki gelen e-postaları veya dosyaları izlemek için önceden tanımlanmış bir şablona sahip otomatik bir akış oluşturur. Geçerli bir faturaya sahip tüm dosyalar tanınabilir ve Borç hesapları (AP) memuru tarafından işlenmeyi beklemek üzere fatura alanına gönderilebilir. Ek, PDF veya resim formatında olmalıdır. Faturalar, kanal yapılandırmasına göre Invoice Capture çözümüne yüklenebilir.

### <a name="create-a-channel"></a>Bir kanal oluşturma

Ek çözüm paketini içe aktardıysanız (Dynamics 365 Invoice Capture – Yükleme Araçları) Office 365 Outlook için varsayılan bağlantı kullanıma hazırdır. Farklı e-posta hesapları veya diğer kanal türleri için daha fazla bağlantı oluşturmak istiyorsanız bkz. [Kanallar için ek bağlantı oluşturma](invoice-capture-advanced-settings.md#create-additional-connections-for-channels).

Bir kanal oluşturmak için şu adımları izleyin.

1. **Kurulum \> Sistem kurulumu \> Yapılandırma kanalları** bölümüne gidin.
2. **Yeni**'yi seçin.
3. Aşağıdaki alanları ayarlayın:

    - Kanal adı
    - Açıklama
    - Tip
    - Bağlantı

Yalnızca aşağıdaki ölçütlere uyan e-postalar veya dosyalar çözüme aktarılabilir.

| Tip               | Yapılandırma  | Daha fazla bilgi |
|--------------------|----------------|------------------|
| Office 365 Outlook | Klasör         | E-posta klasörü kök dizinin altında olmalıdır. Varsayılan olarak Gelen Kutusu klasörü kullanılır. Bir alt klasör desteklenmez. |
|                    | Konu filtresi | (İsteğe bağlı) Konuya dahil edilmesi gereken bir alt dize. |
|                    | Kaynak           | (İsteğe bağlı) Gönderenin veya gönderenlerin e-postası adresi. Birden fazla adres belirtirseniz ayırıcı olarak noktalı virgül (;) kullanın. |
| SharePoint         | Site adresi   | Site adresinin URL'si. |
|                    | Klasör         | Site adresindeki klasör. |

### <a name="activate-the-channel"></a>Kanalı etkinleştirme

Akış kaydedildiğinde, alanlar kanalın durumunu ve oluşturulduğu saati gösterir. Başlangıçta, **Durum** alanı **Etkin değil** olarak ayarlanır. **Durum açıklaması** alanı, kanalın başlatıldığını ve etkinleştirilmeye hazır olduğunu gösterir.

Kanalı etkinleştirmek için **Etkinleştir** öğesini seçin. **Durum** ve **Durum açıklaması** alanları güncelleştirilir.

Bir kanal gerekmiyorsa bunu devre dışı bırakabilirsiniz. Kanalı devre dışı bırakmak için **Devre dışı bırak**'ı seçin. **Durum** ve **Durum açıklaması** alanları güncelleştirilir.

### <a name="manage-flows-in-flow-management"></a>Akışları akış yönetiminde yönetme

**Yapılandırma kanalları** sayfasında veya akış yönetiminde bir kanal görüntüleyebilirsiniz.

Daha fazla ayrıntı görüntülemek için **Yönetici sistemi \> Varsayılan çözümü \> Bulut akışları** bölümüne gidin ve hedef akışı seçin. Gösterilen ayrıntılar arasında bağlı bağlantılar, sahipler ve çalıştırma geçmişleri yer alır.

Durumu eşitlemek için kanalın durumunun akışın durumuyla eşleştiğini onaylamak için **Denetle**'yi seçin.

Özel durum işlemenin bazı durumları **Durum açıklaması** alanında gösterilir:

- **Kayıp Dataverse bağlantısı** – Geçerli kullanıcı en az bir **Microsoft Dataverse** bağlantı başvurusu oluşturmadı.
- **Bulunamadı** – Kanala bağlı olan akış, akış yönetiminde silindi. Yeni bir kanal oluşturmak için kanalın yeniden kaydedilmesi gerekir.
- **Akış yönetiminde devre dışı bırakıldı** – Akış, akış yönetiminde devre dışı bırakıldı ve kanalın durumu akışın durumundan farklı.
- **Akış yönetiminde etkinleştirildi** – Akış, akış yönetiminde etkinleştirildi ve kanalın durumu akışın durumundan farklı.
- **Beklenmeyen bir hata oluştu** – Kullanıcı, sitenin bir "iletişim sitesi" olduğunu ve klasörün "Belge kitaplığı" olduğunu onaylaması gerekir.

---
title: Invoice Capture çözümü yapılandırma grupları
description: Bu makalede, Invoice Capture çözümünde yapılandırma grupları hakkında genel bilgi sağlanmaktadır.
author: sunfzam
ms.date: 09/28/2022
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
ms.openlocfilehash: cfe5ae35b4f87a350d944b30a49251081766ad27
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691247"
---
# <a name="invoice-capture-solution-configuration-groups"></a>Invoice Capture çözümü yapılandırma grupları

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Kullanıcılar, yapılandırma gruplarını kullanarak fatura alanlarının listesini ve tüzel kişiliklerin manuel inceleme ayarını yönetebilir. Kullanıcılar, gruplardaki farklı tüzel kişilikler için fatura yapılandırmaları ayarlayabilir. Aynı yapılandırma grubundaki tüm tüzel kişilikler aynı fatura alanlarını ve manuel inceleme ayarını kullanır.

## <a name="manage-configuration-groups"></a>Konfigürasyon gruplarını yönet

Uygulamayı kullanarak yapılandırma gruplarını yönetmek için **Kurulum** alanına gidin ve ardından **Sistem kurulumu \> Yapılandırma grupları bileşenini tanımla**'yı seçin.

**Yapılandırma gruplarını tanımla** sayfasında, ana sekme tanımlanmış yapılandırma gruplarının listesini gösterir. Ayrıca varsayılan bir yapılandırma grubu da gösterir. Her yapılandırma grubu için aşağıdaki eylemler kullanılabilir:

- **Yapılandırma grubu kopyalama** – Mevcut bir grubu çoğaltarak yeni bir yapılandırma grubu oluşturabilirsiniz. Yeni grup, **Grup adı** ve **Grup açıklaması** dışındaki tüm alanlar için orijinal grupla aynı değerlere sahiptir. Yapılandırma grubu yinelendikten sonra **Tamam**'ı seçin.
- **Yapılandırma gruplarını sil** – Bir yapılandırma grubunu silmek için, grubu seçin ve ardından **Sil**'i seçin.

    > [!NOTE]
    > Varsayılan yapılandırma grubu silinemez.

- **Yapılandırma grubunun kimliğini düzenle** – Yapılandırma grubunun kimliğini düzenlemek için, **Grup kimliği** alanını seçin ve değeri güncelleştirin. Grup kimliği, boşluk ve özel karakterler içermemeli ve 20 karakteri aşmamalıdır.

    > [!NOTE]
    > **Grup kimliği** alanının değeri yalnızca bir kez güncelleştirilebilir.

- **Yapılandırma grubunun açıklamasını düzenle** – Yapılandırma grubunun açıklamasını düzenlemek için, **Açıklama** alanını seçin ve değeri güncelleştirin.
- **Manuel inceleme ayarını değiştir** – Kullanıcılar bir faturanın manuel olarak incelenip incelenmeyeceğine karar verebilir. Manuel inceleme ayarını değiştirmek için **Manuel inceleme gerekli** seçeneğini belirleyin. Aşağıdaki seçenekler bulunur:

    - **Daima manuel incele** – Yapılandırma grubundaki faturalar her zaman manuel inceleme gerektiriyorsa bu seçeneği belirleyin.
    - **Hatalar ve uyarılar için** – Hata iletileri veya uyarı iletilerini içeren faturalar manuel incelenmesi gerekiyorsa bu seçeneği belirleyin.
    - **Hatalar için** – Hata iletileri içeren faturalar manuel incelenmesi gerekiyorsa bu seçeneği belirleyin.

- **Güvenilirlik puanı ayarını değiştir** – Güvenilirlik puanı, Invoice Capture çözümünün tanınan fatura verilerinin doğruluğunu raporlamak için sağladığı meta verilerdir. Skor arttıkça, tanınan veriler de o kadar kesin olabilir. Yapılandırma, kullanıcıların güvenilirlik puanını temel alarak manuel incelemenin ne zaman gerekli olduğunu tanımlamasına olanak tanır. Kullanıcılar faturaların güvenilirlik puanı eşiğini değiştirebilir. Güvenirlik puanı ayarını güncelleştirmek için **Güvenilirlik puanı** alanını seçin ve değeri güncelleştirin.

    Güvenilirlik puanları için iki uyarı türü vardır:

    - **Uyarı** – Uyarı eşiğinin üzerinde güvenilirlik puanlarına sahip fatura alanları doğru olarak kabul edilir. Uyarı eşiğinin hata eşiğinden büyük ve 100'den küçük olması gerekir.
    - **Hata** – Hata eşiğinin altında güvenilirlik puanlarına sahip fatura alanları başarısız olarak kabul edilir. Hata iletileri kullanıcıya gösterilir. Hata eşiğinin 0'dan (sıfır) büyük ve uyarı eşiğinden küçük olması gerekir. Uyarı eşiği ve hata eşiği arasında güvenilirlik puanlarına sahip fatura alanları için uyarı iletileri gösterilir.

- **Fatura alanlarını yönet** – Kullanıcılar, yan yana görüntüleyicide gösterilen fatura alanları listesini yönetebilir. **Fatura alanı yönetimi** sekmesinde, dişli simgesini seçin, eklenecek fatura alanlarını seçin ve ardından **Kaydet**'i seçin. Seçilen alanlar listeye eklenir. Listeden bir fatura alanını kaldırmak için, alanda **Kaldır**'ı seçin.

### <a name="manage-file-filters-optional"></a>Dosya filtrelerini yönetme (isteğe bağlı)

Dosya filtrelerini yönetme, kullanıcıların gelen fatura dosyaları için ek filtreler tanımlamasına olanak tanır. Filtre ölçütüne uymayan dosyalar alınır ve **Alınan dosyalar** listesinde görünür, ancak dosya doğrulama hataları gösterir. Bu davranış, kanalda tanımlanan filtreler için olan davranıştan farklıdır. Bu filtreler için kriterleri karşılamayan dosyalar hiç alınmaz. Kullanıcılar gelen dosyaları inceleyebilir ve her dosyanın geçerli olmayan bir fatura olup olmadığına karar verebilir ve dosyayı eski haline getirebilir ya da tanıma ve yakalanan faturalara dahil etmek için manuel olarak dahil edilebilir.

Invoice Capture çözümü yüklendiğinde, varsayılan bir dosya filtresi tanımlanır. Bu dosya filtresi geneldir. Farklı filtre ayarları istiyorsanız varsayılan filtreyi güncelleştirebilirsiniz. Bir alan zorunlu ise **Gerekli**'yi seçin. 

### <a name="accepted-file-size"></a>Kabul edilen dosya boyutu

Kabul edilen dosya boyutunu seçebilirsiniz.

> [!NOTE]
> 20.480 kilobayttan (KB) büyük dosyalar desteklenmez.

### <a name="supported-file-types"></a>Desteklenen dosya türleri

Şu anda aşağıdaki dosya türleri desteklenir:

- PDF
- PNG
- JPG
- JPEG
- TIF
- TIFF

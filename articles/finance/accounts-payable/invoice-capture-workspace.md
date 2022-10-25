---
title: Invoice Capture çözümü çalışma alanı
description: Bu makalede, Invoice Capture çözümü çalışma alanı hakkında bilgi sağlanmaktadır.
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
ms.openlocfilehash: 4f3af7abf94542437be6132344d6bb7ffaf33d07
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691244"
---
# <a name="invoice-capture-solution-workspace"></a>Invoice Capture çözümü çalışma alanı

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="side-by-side-viewer-for-the-invoice-capture-solution"></a>Invoice Capture çözümü için yan yana görüntüleyici

Sisteme fatura girmek genellikle zaman alan ve hatalara açık bir işlemdir, çünkü memurların doğru bilgileri toplamak için birden fazla ek dosyada ve pencerede gezinmesi gerekir. Yan yana belge görüntüleyicisi, bir işlemi daha kolay, daha etkili ve daha doğru hale getirerek faturalar üzerinde çalışırken deneyiminizi geliştirmenize yardımcı olur.

Yan yana belge görüntüleyicisi kullanıcıların orijinal belgeyi ve faturayı aynı pencerede yan yana açmasını sağlar. Fatura sayfası orijinal fatura belgesinden gelen bilgilerle doldurulur. Görüntüleyici, fatura sayfası alanları ve orijinal fatura belgesi arasındaki bağlantıyı oluşturur. Görüntüleyici ayrıca kullanıcıların fatura sayfasında bulunan hataları bulmasına yardımcı olur.

### <a name="open-the-side-by-side-viewer"></a>Yan yana görüntüleyiciyi açma

Microsoft Dynamics 365 Finance'da, özet sayfasındaki listeden veya fatura listesi sayfasından yan yana görüntüleyiciyi açabilirsiniz. Ayrıca, bir kayda çift dokunarak (veya çift tıklayarak) veya fatura numarasını seçerek de açabilirsiniz.

### <a name="using-the-side-by-side-viewer"></a>Yan yana görüntüleyici kullanma

#### <a name="manually-review-an-invoice"></a>Bir faturayı manuel inceleme

İçe aktarılan bir fatura belgesi, hatalar veya uyarılar nedeniyle manuel inceleme gerektirebilir. Yan yana görüntüleyicide, belge üst bilgisi **İçe aktarıldı** durumunu gösterir ve mevcut sürüm **Orijinal Sürüm** olur.

Faturayı incelemeye başlamak için **İncelemeyi başlat**'ı seçin. Tüm alanlar düzenlenebilir hale gelir. **Durum** alanı **İncelemede** olarak güncelleştirilir ve **Mevcut sürüm** alanı **Değiştirilmiş sürüm** olarak güncelleştirilir.

#### <a name="view-and-work-with-messages"></a>İletileri görüntüleme ve iletilerle çalışma

Kullanıcılar, inceleme işlemini ileti bölmesinden başlatmalıdır. Hata iletileri kırmızı bir X ile, uyarı iletileri bir üçgen ile, bilgi iletileri ise bir daire ile gösterilir. Güvenilirlik puanıyla ilgili iletiler, yapılandırma grubu tarafından belirlenen eşiğe bağlı olarak uyarı veya hata olarak sınıflandırılabilir. Daha fazla bilgi için bkz [Invoice Capture çözümü yapılandırma grupları](invoice-capture-config-group.md).

Uyarı ve hata iletileri, ileti bölmesinden, fatura başlığından veya fatura satırlarından yok sayılabilir. Bir ileti göz ardı edildikten sonra artık hata veya uyarı olarak görülmez ve fatura doğrulaması başarısız olmaz.

- İleti bölmesindeki iletileri yok saymak için **Yoksay**'ı seçin. Yoksayılan bir iletiyi sıfırlamak için yeniden **Yoksay**'ı seçin. Bunun türü, daha sonra hata veya bilgi uyarısından değiştirilir.
- Fatura üst bilgisinden veya fatura satırından iletileri sıfırlamak için alanda **Yoksay**'ı seçin. İleti sembolü kaybolur. Ancak ileti, ileti bölmesinden sıfırlanırsa yeniden görüntülenir.

Fatura üst bilgisi alanlarıyla ilişkili iletiler için, ileti bölmesinde iletiyi seçtiğinizde, imleç üst bilgi bölümünde karşılık gelen ilgili alana taşınır.

#### <a name="proofread-and-edit-fields"></a>Alanları düzeltme ve düzenleme

Bir alanın değeri orijinal faturadan optik karakter tanıma (OCR) yoluyla okunursa alan üzerinde bir sembol belirir. Sembolü seçerseniz belge görüntüleyici, fatura verilerini doğrulamanıza yardımcı olmak için alan değerinin okunduğu yeri yakınlaştırır ve vurgular.

Belge görüntüleyiciyi orijinal büyütme oranına sıfırlamak için bu adımlardan birini izleyin:

- Daha önce seçtiğiniz sembolün aynısını seçin.
- Belge görüntüleyicinin sağ üst köşesindeki düğmeyi seçin.

Alanları, gerektiği şekilde düzenleyin. İmleç bir alandan ayrıldığında düzenlemeler otomatik olarak kaydedilir. Bir alanın sağında yer alan sembol, o alanın manuel olarak güncelleştirildiğini gösterir. Sayfa yenilendiğinde sembol kaldırılır.

#### <a name="check-an-invoice-to-get-up-to-date-messages"></a>Güncel iletiler edinmek için faturayı denetleme

Bir alanı düzenlediğinizde, alan değeri güncelleştirilir, ancak yeni doğrulama iletileri oluşturulmaz. Güncel doğrulama iletileri edinmek için **Denetle**'yi seçin. İleti bölmesindeki, fatura başlığındaki ve fatura satırlarındaki iletiler güncelleştirilir.

#### <a name="complete-the-review"></a>İncelemeyi tamamlama

İncelemeyi tamamlamak için **İncelemeyi tamamla**'yı seçin. Faturalar doğrulanır. Herhangi bir hata bulunursa belgenin durumu **İncelemede** kalır ve bir ileti çubuğu görüntülenir. İleti bölmesi ve fatura üst bilgisi ve satırlarındaki tüm iletiler, başarısız doğrulamanın nedenleri hakkında bilgi sağlamak için otomatik olarak güncelleştirilir.

Tüm durdurma hataları düzeltildikten sonra inceleme tamamlanabilir. Belge durumu **İncelendi** olarak güncelleştirilir ve alanlar artık düzenlenemez. **İncelemeyi başlat**'ı tekrar seçerek incelemeyi yeniden başlatabilirsiniz.

#### <a name="generate-a-pending-vendor-invoice-in-finance"></a>Finance'ta bekleyen bir satıcı faturası oluşturma

Fatura belgesini bağlı Finance ortamına göndermek için **Oluştur**'u seçin. Fatura oluşturma başarısız olursa ileti çubuğunda bir hata iletisi görüntülenir.

#### <a name="void-an-invoice"></a>Bir faturayı hükümsüz kılma

Bir faturayı hükümsüz kılmak için **Hükümsüz kıl**'ı seçin. Hükümsüz faturalar incelenemez ve **Manuel incelenmesi gereken faturalar** listesinde gösterilmez.

### <a name="validation-logic"></a>Doğrulama mantığı

Yan yana görüntüleyicideki bazı anahtar alanlar, fatura hazırlama verilerinde yer almaz ancak Finance'ta bekleyen faturalar oluşturmak için gereklidir. Bu alanlar, geçerli fatura hazırlama verilerinin ve Finance'tan ana verilerin birleşiminden türetilir.

**Tüzel Kişilik**, **Satıcı Hesabı** ve **Öğe Numarası**'ndan türetilmesi gereken alanlar. Bunların aşağıdaki sırada türetilmesi gerekir. Bir alanın türetilmesi başarısız olursa işlem durur.

1. **Yasal varlık**: İlk olarak Tüzel kişilik türetilir. Tüzel kişilik için etkin bir eşleme kuralı bulunursa tüzel kişilik şirket adı ve şirket adresi temel alınarak türetilir.
2. **Satıcı hesabı**: Ardından, satıcı hesabı aktif bir eşleme kuralına ve türetilen tüzel kişilik ile satıcı adı ve satıcı adresinin bir kombinasyonuna dayalı olarak türetilir.
3. **Öğe numarası**: Son olarak, öğe adı aşağıdaki üç bilgi türüne dayalı olarak hazırlamadan türetilir:

    - Yapılandırılmış bir eşleme kuralı
    - Türetilen tüzel kişilik
    - Türetilen satıcı hesabı

Doğrulama çalıştırmak için yan yana görüntüleyicide **Denetim** öğesini seçin. Şu anda, doğrulama aşağıdaki denetimleri gerçekleştirir:

- **Zorunlu denetim**: Bu denetim yan yana görüntüleyici için zorunlu alanları doğrular. Kullanıcılar, **Yapılandırma ayarı** sayfasında hangi alanların zorunlu olması gerektiğini seçebilir.
- **Güvenilirlik puanı**: Kullanıcılar güvenilirlik puanı için uyarı eşiğini ve hata eşiğini ayarlayabilir. Bu denetim, OCR'den alınan ve bu eşiklerin altında kalan güvenilirlik puanına odaklanır. Doğrulama sonucuna bağlı olarak hata veya uyarı iletileri gösterilir.
- **Tüzel kişilik**: Bu denetim, yasal bir varlığın Finance'ta olduğunu doğrular. Yasal varlık Finance ortamında mevcut değilse doğrulama işlemi başarısız olur.

Yan yana görüntüleyici ilk kez kullanıldığında ve kullanıcı **Denetim**'i seçtiğinde, türetme ve doğrulama işlemleri çalıştırılır. Faturalar doğru ise kullanıcı, **İncelemeyi tamamla** öğesini seçtiğinde doğrulama işlemi çalıştırılır. Ayrıca kullanıcı, **Satıcı faturası oluştur** öğesini seçtiğinde de çalıştırılır.

Türetme işlemi, doğrulama işleminden önce gerçekleşir ve tüm uyarılar ve hatalar doğrulama işleminden gelir. Uyarılar ve hatalar Finance'ta günlüğe kaydedilir.

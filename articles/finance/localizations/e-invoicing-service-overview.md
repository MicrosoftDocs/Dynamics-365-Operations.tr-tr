---
title: Elektronik faturalama eklentisine genel bakış
description: Bu konu, Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management uygulamalarında elektronik faturalama eklentisi hakkında bilgi sağlar.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ffd48e173b66cc6d2571e666d5452a5eff05176c
ms.sourcegitcommit: f860ac2b18f6bbbfc4a46b497baec2477105b116
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/19/2020
ms.locfileid: "4448990"
---
# <a name="electronic-invoicing-add-on-overview"></a>Elektronik faturalama eklentisine genel bakış

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management için Elektronik faturalama eklentisi elektronik fatura belgelerinin yapılandırılabilir şekilde işlenmesini ve yapılandırılabilir belge alış verişi sağlayan aşırı ölçeklenebilir bir çoklu kiracı hizmetidir. İşlem ve tümleştirme kuralları tümüyle yapılandırılabilir ve bu mantık Finance ve Supply Chain Management dışında çalıştırılır. Servis esas olarak şirketten kamuya senaryolarındaki e-fatura işlemlerinde hedeflenmiştir, ancak başka amaçlar için özel olarak yapılandırılabilir.

Elektronik faturalama eklentisi aşağıdaki hedeflere ulaşmanıza yardımcı olabilir:

- Ülkeye/bölgeye özel gereksinimlerin hızlı ve kolay şekilde benimseme
- Elektronik faturalama eklenti çözümünün standartlaştırılmış uygulamaları
- Belge geçmişinin gelişmiş izlenebilirliği
- Daha kısa uygulama döngüsü
- Düşülen toplam sahip olma maliyeti (TCO)
- Kod değişiklikleri gerekmeyen yapılandırmalar kolayca ayarlanabilir
- Basitleştirilmiş yapılandırma paketi
- E-fatura belgelerinin işlenmesinde yerleşik dışa aktarma, içe aktarma ve tümleştirme, kolay genişletilebilirlik
- Şirketler arasında aynı dışa aktarma, içe aktarma ve tümleştirme yapılandırmasının kolay yeniden kullanımı

Elektronik faturalama eklentisini kullanmak için, Microsoft Dynamics Lifecycle Services (LCS) içindeki projenizden yüklemeniz gerekir. Daha sonra, Finance veya Supply Chain Management uygulamalarıyla tümleştirmeyi açmak için kurulum yordamını izleyin. Daha fazla bilgi için bkz. [Elektronik faturalama eklentisini kullanmaya başlangıç](e-invoicing-get-started.md).

## <a name="availability"></a>Kullanılabilirlik

Başlangıçta, Elektronik faturalama eklentisi bir önizleme programıyla seçili müşteriler tarafından kullanılabilir. Daha sonra, önizleme daha geniş bir müşteri kitlesine açılacaktır. Son olarak, servis genel kullanıma açık olacaktır. Ülkeye/bölgeye özel gereksinimleri karşılayan işlevler, sürümün farklı aşamalarında sınırlı olduğundan, her zaman desteklenen ülkeye/bölgeye özel çözümlerin kapsam ve kapsamını vurgulayan en güncel belgeleri denetlemeniz gerekir.

Elektronik faturalama eklentisi aşağıdaki Azure coğrafyalarında dağıtıldı:

- Amerika Birleşik Devletleri
- Avrupa

> [!NOTE]
> Elektronik faturalama eklentisi şirket içi dağıtımları desteklemiyor.

## <a name="extended-configurability"></a>Genişletilmiş yapılandırılabilirlik

Elektronik faturalama eklentisi, belirtilen taraflara elektronik belge oluşturmanız ve göndermeniz gereken senaryolarda kullanılabilir. Özel olarak, alınan verilere dayalı olarak, yapılandırılabilir bir işlem eylemi çalıştırmak için tasarlanmıştır. Finance ve Supply Chain Management uygulamalarında kullanılabilen yapılandırılabilirlik seçenekleri belge dönüşümüyle sınırlıdır. Hizmet, içinde kullanılabilen yapılandırılabilir tümleştirmeler ekleyerek bu seçenekleri genişletir. Ayrıca, önceden kullanılabilen elektronik fatura işlevleri de dahil olmak üzere, Brazilian Nota fiscal eletrônica (NF-e), Mexican Comprobante Fiscal Digital por Internet (CFDI) veya diğer Batı Avrupa Universal Business Language (UBL)/Pan-European Public Procurement OnLine (PEPPOL) işlevleri gibi, dışa aktarma ve içe aktarma yapılandırmaları ve harici Web hizmetleriyle tümleştirmeleri kullanacaktır.

## <a name="feature-highlights"></a>Özellikle ilgili önemli noktalar

- Finance ve Supply Chain Management uygulamalarıyla yerleşik tümleştirme
- Tüm ülkeler veya bölgeler için e-fatura sürecini yapılandırılması ve izlenmesiyle ilgili tutarlı kullanıcı deneyimi
- Yeni ülke veya bölgelerde, elektronik faturalama eklenti çözümlerinin daha hızlı, kolay ve ucuz olarak benimsenmesi
- Hizmetin Regulatory Configuration Service (RCS) ve Genelleştirme özelliği kurulumu aracılığıyla yapılandırılması
- İş verilerinin, RCS 'de tanımlanan yapılandırmaları kullanarak çoklu e-fatura biçimlerine (XML, JavaScript nesne gösterimi \[JSON\], TXT ve virgülle ayrılmış değerler \[CSV\]) biçimlerine dönüştürülmesi:

    - E-fatura dönüştürmesi için yapılandırma özelliğinin kullanılamadığı ülkeler veya bölgeler için kullanılabilen elektronik raporlama biçimleri

- Dijital imzalar aracılığıyla sertifika işleme dahil olmak üzere, e-faturaların harici Web hizmetlerine yapılandırılabilir gönderimi:

    - Yerleşik, kolayca genişletilebilir ve çeşitli ülkelerde ek içerikle yapılandırılabilir tümleştirme

    > [!NOTE]
    > Şu anda sınırlı sayıda doğrudan gönderimler desteklenmektedir. Daha fazla bilgi için bu konunun önceki kısımlarında yer alan [Kullanılabilirlik](#availability) bölümüne bakın. Destek ileride genişletilecektir.

- Yapılandırılabilir özel durum iletisi işleme dahil olmak üzere Web hizmetlerinden yanıtların işlenmesi
- Elektronik imza desteği (örneğin, XMLDSIG imza algoritması kullanılarak)
- E-fatura iletilerinin toplu olarak işlenmesi

## <a name="architecture-and-data-flow"></a>Mimari ve veri akışı

Elektronik faturalama eklentisi LCS'den yüklendiğinde ve gerekli kurulum tüm gerekli uygulamalarda tamamlanırsa, güvenli bir bağlantı kurulur. Hizmet şu anda Amerika Birleşik Devletleri ve Avrupa'da bulunan veri merkezlerinde bulunmaktadır. Bu nedenle, hizmet konumu ilgili Finance veya Supply Chain Management örneğinin konumundan farklı olabilir. Elektronik faturalama eklentisinin kurulumunu tamamladıktan ve tümleştirmeyi açıktan sonra, bir e-faturanın her gönderilmesinde belirli bir belgeyle ilgili ana veriler ve işlem verileri Elektronik faturalama eklentisine gönderilir.

> [!NOTE]
> Elektronik faturanızda veya herhangi bir belgede kişisel veriler varsa, bu özelliği kullanmanın, Genel Veri Koruma Yönetmeliği (GDPR) ve kişisel verilerin aktarılmasıyla ilgili diğer düzenlemeleri karşıladığını doğrulayın.

### <a name="high-level-description-of-the-data-flow"></a>Veri akışının üst düzey açıklaması

1. İstemci hizmete kurallı bir iş belgesi gönderir.
2. Hizmet, istemciden alınan bağlam bilgilerine göre uygulanabilir işlem akışını seçer.
3. Hizmet işlem eylemlerini çalıştırır. Bu eylemler, iş belgesini elektronik bir faturaya dönüştürmek, elektronik bir imza uygulamak ve belgeyi harici bir Web servisine göndermek olabilir.
4. Alınan ve işlenen tüm belgeler müşterinin Azure Blob depolama alanında depolanır.
5. İşlenmek üzere kullanılan tüm kiracı gizli anahtarları ve sertifikaları müşterinin Azure anahtar kasasında depolanır.
6. Hizmet, gönderilen iş belgesinin işlem durumu hakkında istemciye isteğe bağlı bilgiler sağlar.
7. İstemci tamamlanan işleme yürütme hakkında bilgi alır ve tüm günlük bilgilerini kullanılabilir yapar. Ayrıca, akış işlemi sırasında oluşturulan veya alınan belgeyi kullanılabilir yapar.

Aşağıdaki şekil, Elektronik faturalama eklentisi ile arasındaki veri akışının nasıl olduğunu gösterir.

![Elektronik faturalama eklentisinde veri akışı](media/e-invoicing-service-data-flow-diagram-overview.png)

## <a name="privacy-notice"></a>Gizlilik bildirimi
Elektronik faturalandırmanın etkinleştirilmesi ve kullanılması, kuruluş vergi kayıt kodunu içeren sınırlı verilerin gönderilmesini gerektirebilir. Bu, devlete ait Web servisi ile tümleştirme için gerekli önceden tanımlanmış biçimlerde vergi dairesine elektronik fatura göndermek amacıyla vergi dairesi tarafından yetkilendirilen üçüncü taraf kuruluşlarına iletilecektir. Bu harici sistemlerden alınan verilerin bu Dynamics 365 çevrimiçi hizmetine aktarılması [gizlilik bildirimimize](https://go.microsoft.com/fwlink/?LinkId=512132) tabidir. Daha fazla bilgi için, lütfen ülkeye özel özellik belgelerindeki Gizlilik bildirimi bölümlerine bakın.

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik faturalama eklentisini kullanmaya başlangıç](e-invoicing-get-started.md)
- [Brezilya için Elektronik faturalama eklentisini kullanmaya başlangıç](e-invoicing-bra-get-started.md)
- [Meksika için Elektronik faturalama eklentisini kullanmaya başlangıç](e-invoicing-mex-get-started.md)
- [İtalya için Elektronik faturalama eklentisini kullanmaya başlangıç](e-invoicing-ita-get-started.md)
- [Elektronik faturalamayı eklentisini kurma](e-invoicing-setup.md)

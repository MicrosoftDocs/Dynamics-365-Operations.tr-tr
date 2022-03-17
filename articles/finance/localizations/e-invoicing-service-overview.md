---
title: Elektronik faturalamaya genel bakış
description: Bu konu, Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management uygulamalarında elektronik faturalama hakkında genel bakış sağlar.
author: gionoder
ms.date: 01/21/2022
ms.topic: overview
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
ms.openlocfilehash: 23a98706bc2ab0abc2c72e9f20d8e8fbff56b2b9
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371466"
---
# <a name="electronic-invoicing-overview"></a>Elektronik faturalamaya genel bakış

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management için Elektronik faturalama elektronik faturalarının yapılandırılabilir şekilde işlenmesini ve yapılandırılabilir elektronik belge alış verişi sağlayan aşırı ölçeklenebilir bir çoklu kiracı hizmetidir. İşlem ve tümleştirme kuralları tümüyle yapılandırılabilir ve bu mantık Finance ve Supply Chain Management dışında çalıştırılır. Servis esas olarak işletmeler arası senaryolarda elektronik fatura belgelerinin işlenmesini hedeflemektedir. Ancak, farklı türlerde belgeler için işletmeler arası senaryolar gibi diğer amaçlar için özel konfigüre edilebilir.

Elektronik faturalama aşağıdaki hedeflere ulaşmanıza yardımcı olabilir:

- Ülkeye/bölgeye özel gereksinimlerin hızlı ve kolay şekilde benimseme
- Elektronik faturalama çözümünün standartlaştırılmış uygulamaları
- Belge geçmişinin gelişmiş izlenebilirliği
- Daha kısa uygulama döngüsü
- Düşülen toplam sahip olma maliyeti (TCO)
- Kod değişiklikleri gerekmeyen yapılandırmalar kolayca ayarlanabilir
- Basitleştirilmiş yapılandırma paketi
- Elektronik fatura belgelerinin işlenmesinde yerleşik dışa aktarma, içe aktarma ve tümleştirme, kolay genişletilebilirlik
- Şirketler arasında aynı dışarı aktarma, içeri aktarma ve tümleştirme yapılandırmasının kolay yeniden kullanımı

## <a name="service-availability"></a>Hizmet kullanılabilirliği

Şimdilik Elektronik faturalama işlevi Finance ve Supply Chain Management müşterileri için kullanılabilir. Daha fazla bilgi için, uygulamanızın lisans hüküm ve koşullarını gözden geçirin.

Ülkeye/bölgeye özel gereksinimleri karşılayan işlevler, sürümün farklı aşamalarında sınırlı olduğundan, her zaman desteklenen ülkeye/bölgeye özel çözümlerin kapsam ve kapsamını vurgulayan en güncel belgeleri denetlemeniz gerekir.

Elektronik faturalama aşağıdaki Azure coğrafyalarında dağıtıldı:

- Amerika Birleşik Devletleri
- Avrupa
- Asya

> [!NOTE]
> Elektronik faturalama şirket içi dağıtımları desteklemiyor.

## <a name="feature-highlights"></a>Özellikle ilgili önemli noktalar

- Finance ve Supply Chain Management uygulamalarıyla yerleşik tümleştirme
- Tüm ülkeler veya bölgeler için elektronik fatura sürecini yapılandırılması ve izlenmesiyle ilgili tutarlı kullanıcı deneyimi
- Yeni ülke veya bölgelerde, elektronik faturalama çözümlerinin daha hızlı, kolay ve ucuz olarak benimsenmesi
- Hizmetin Regulatory Configuration Service (RCS) kurulumu ve Genelleştirme özellikleri aracılığıyla yapılandırılması
- İş verilerinin, RCS 'de tanımlanan yapılandırmaları kullanarak çoklu elektronik fatura biçimlerine (XML, JavaScript nesne gösterimi \[JSON\], TXT ve virgülle ayrılmış değerler \[CSV\]) biçimlerine dönüştürülmesi:

    - Elektronik fatura dönüştürmesi için yapılandırma özelliğinin kullanılamadığı ülkeler veya bölgeler için kullanılabilen elektronik raporlama (ER) biçimleri

- Dijital imzalar aracılığıyla sertifika işleme dahil olmak üzere, elektronik faturaların harici Web hizmetlerine yapılandırılabilir gönderimi:

    - Yerleşik, kolayca genişletilebilir ve çeşitli ülkelerde ve bölgelerde ek içerikle yapılandırılabilir tümleştirme

- Yapılandırılabilir özel durum iletilerini işleme dahil olmak üzere Web hizmetlerinden yanıtların işlenmesi
- Elektronik imza desteği (örneğin, XMLDSig imza algoritması kullanın elektronik imzalar)
- E-postalara belge gönderme ve bunları SharePoint'te depolama yeteneği
- Elektronik fatura iletilerinin toplu olarak işlenmesi
- Gelen belgelerin konfigüre edilebilir dönüştürmesi ve Finance ve Supply Chain Management'ta bu belgelerin işlenmesi
- E-posta ve SharePoint gibi kanallardan gelen belgeleri alma özelliği

## <a name="privacy-notice"></a>Gizlilik bildirimi

Elektronik fatura özelliğini etkinleştirmek ve kullanmak, sınırlı verilerin gönderilmesini gerektirebilir. Bu verilere kuruluşun vergi kayıt kodu dahildir. Bu veriler, devlete ait Web servisi ile tümleştirme için gerekli önceden tanımlanmış biçimlerde vergi dairesine elektronik fatura göndermek amacıyla vergi dairesi tarafından yetkilendirilen üçüncü taraf kuruluşlarına iletilecektir. Bu harici sistemlerden alınan verilerin bu Dynamics 365 çevrimiçi hizmetine aktarılması [gizlilik bildirimimize](https://go.microsoft.com/fwlink/?LinkId=512132) tabidir. Daha fazla bilgi için ülkeye/bölgeye özel özellik belgelerindeki "Gizlilik bildirimi" bölümüne bakın.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

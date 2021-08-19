---
title: Belgeleri ve fişleri kronolojik olarak numaralandırma
description: Bu konu, uygulanabilir belgeler ve ilgili fişler için kronolojik numaraların nasıl ayarlanacağını ve kullanılacağını açıklamaktadır.
author: ikond
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ced09fb4be49dbfd10dac9f9ece86372d38e854460c7ca6cd72922c64ac7cce4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724147"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a>Belgeleri ve fişleri kronolojik olarak numaralandırma

[!include [banner](../includes/banner.md)]


Bazı ülke/bölgelerde, belgeleri ve ilgili fişleri kronolojik sırada numaralandırmak için yasal bir gereksinim vardır. Kronoloji, dönemler tarafından desteklenmelidir. Önceki dönemlere ait tüm numaralar sonraki dönemlere ait olan numaralardan küçük olmalıdır. Bu gereksinimi karşılamak için kronolojik numaralandırma işlevi uygulanmıştır. Bu konu, uygulanabilir belgeler ve ilgili fişler için kronolojik numaraların nasıl yapılandırılacağı ve kullanılacağını açıklamaktadır.

## <a name="prerequisites"></a>Önkoşullar

Özellik yönetimi çalışma alanında aşağıdaki **Kronolojik numaralandırma** özelliğini açın. Daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="configure-chronological-numbering"></a>Kronolojik numaralandırmayı yapılandırma

Kronolojik numaralandırma aşağıdaki belgeleri etkiler.

**Alacak hesapları**
- Müşteri faturası
- Müşteri faturası fişi
- Satış alacak dekontu
- Satış alacak dekontu fişi
- Dekont / Serbest metin faturası
- Dekont / Serbest metin faturası fişi
- Serbest metinli alacak dekontu
- Serbest metinli alacak dekontu fişi
- Sevk irsaliyesi
- Sevk irsaliyesi fişi
- Sevk irsaliyesi düzeltme fişi
- Vade farkı dekontu fişi
- Tahsilat mektubu fişi

**Borç hesapları**
- Fatura fişi
- Alacak dekontu fişi
- Ürün giriş fişi

**Proje yönetimi**
- Fatura
- Fatura fişi
- Alacak dekontu
- Alacak dekontu fişi 

### <a name="define-number-sequences"></a>Numara serileri tanımlama

Numara serilerini tanımlamak için **Kuruluş yönetimi** > **Numara serileri** > **Numara serileri**'ne gidin. Gerekli belgeler için etkilenen dönemleri kapsamak için gereken sayıda numara serisi tanımlayabilirsiniz. 

Her numara serisi için bir şirket belirtin. Numara serilerinin segmentleri, dönemler için kronolojik sıra sağlayacak şekilde tanımlanmalıdır. Örneğin, segment adları belirli bir dönemi tanımlayan özel bir önek içerebilir.

![Numara serisi kurulumu.](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a>Numara serisi gruplarını yapılandırma

Numara serisi gruplarını konfigüre etmek için **Alacak hesapları** > **Kurulum** > **Alacak hesapları parametreleri**'ne gidin. **Numara serileri** sekmesinde, etkilenen dönemleri kapsamak için gereken sayıda numara serisi grubu tanımlayın. 

Her grup için, **Referans** bölümünde desteklenen belge referanslarından birini seçin ve **Numara serisi kodu** alanında, daha önce ilgili dönem için oluşturulan bir numara serisine referans verin.

![Numara serisi grubu kurulumu.](media/chrono-num-sequence-group.jpg)

Benzer şekilde, **Borç hesaplarında** ve **Proje yönetimi ve muhasebe** modüllerinde numara serileri gruplarını yapılandırın.

### <a name="configure-number-sequence-groups-chronology"></a>Numara serisi grupları kronolojisini yapılandırma

Numara serisi grupları kronolojisini yapılandırmak için **Kuruluş yönetimi** > **Numara serileri** > **Kronolojik numara serisi grupları**'na gidin. Numara serisi grupları için uygulanabilirlik koşullarını tanımlayın.

![Kronolojik numaralar kurulumu.](media/chrono-num-sequence-group-period.jpg)

| Alan            | Tanım                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Yürürlüğe giriş  | Numara serisi grubunun geçerlilik başlangıç tarihi. |
| Bitiş tarihi      | Numara serisi grubunun geçerlilik bitiş tarihi. Bitiş tarihi uygulanmamışsa, **Asla** seçeneğini belirleyin. |
| Numara serisi grubu | Dönem içinde belge numaraları oluşturmak için kullanılacak numara serisi grubu. |
| Özgün numara serisi grubu | Bu numara serisi grubu kodu, belgelerin zaten belirli bir *kalıcı* numara serisi grubu için atanmış olduğu durumlarda ek filtre uygulama amacıyla kullanılır. Boş değer belirli bir değer olarak kabul edilir. Geçici olarak atanan bir grubu dikkate almanız gerekiyorsa bu kurulum için **Varsayılan** seçeneğini kullanın. |
| Varsayılan | Açıksa sistem, geçici atanan belge numara serisi grubunu yoksayar ve yalnızca dönem başlangıç ve bitiş tarihlerini geçerlilik analizi için kullanır. Kapalıysa, sistem, seçim için **Geçerlilik** + **Sona Erme** + **Orijinal numara serisi grubu** tam kombinasyonunu kullanır. |

## <a name="document-posting"></a>Belge deftere nakletme
Bir belgeyi deftere naklettiğinizde, belgenin deftere nakil tarihi temel alınarak ilgili numara serisi grubu belgeye atanır ve sonra algılanan numara serisine göre bir belge numarası oluşturmak için kullanılır. Sistem, numara serisi grubu atamasıyla ilgili bir ileti sağlar.

![Belge numarası.](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> Bazı ülke/bölgelerde belge numaralandırması için önceden uygulanmış belirli bir mantık vardır. Bu durumda, ülkeye özel mantık, **Kronolojik numaralandırma** özelliğini geçersiz kılar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

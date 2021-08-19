---
title: Kullanım yönetimi panosu
description: Bu konu, Elektronik Faturalama hizmetinin kullanımını izlemek ve uyumlu kalmak için Kullanım yönetimi panosunun nasıl kullanılacağını açıklar.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 35b50c8cb5c6ef72f466a4fb10c7af0e53afc3db5d1ef9e2b23d6049e24a70c3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776486"
---
# <a name="usage-management-dashboard"></a>Kullanım yönetimi panosu

[!include [banner](../includes/banner.md)]

**Kullanım Yönetimi** panosu, Elektronik Faturalama servisinin kullanımını izlemenize yardımcı olur ve bu nedenle kuruluşunuzun aylık kullanım açısından uyumlu kalmasını sağlar. Uyumluluk, gönderme biriminin hesaplanmasıyla ve elde edilen birim ile kullanılan birim arasındaki sapmaları belirlemek için alınan gönderilerle karşılaştırarak belirlenir.

Pano, aşağıdaki göstergeleri içerir:

- Lisans uyumluluğu amaçları için tüketimi izlemek amacıyla kullanabileceğiniz bir maliyet göstergesi:

    - Aylık kullanım (dışarı aktarma)

- Elektronik Faturalama hizmetinin kullanımını yönetim amaçlarını izlemek için kullanabileceğiniz üç operasyon göstergesi:

    - Özelliğe göre kullanım
    - Ortama göre kullanım
    - Aylık kullanım (içeri aktarma)

## <a name="measurement-scope"></a>Ölçüm kapsamı

- Ölçü birimi: 

    **Kullanım yönetimi** panosu, iş belgelerinin ve içe aktarılan elektronik faturaların gönderimini sayar.

- Kuruluş: 

    Sayım, Microsoft Dynamics 365 Finance veya Dynamics 365 Supply Chain Management'taki örneklerin sayısından veya Elektronik Faturalama hizmetinin etkinleştirildiği tüzel kişilik sayısından bağımsız olarak, kuruluşunuzun kiracı kimliğine göre özetlenir.


## <a name="indicator-usage-per-month-export"></a>Gösterge: Aylık kullanım (dışa aktar)

Bu gösterge, kuruluşunuzun tanımlı bir dönemde kestiği elektronik faturalar hakkında ayrıntılı bilgi sağlar.

### <a name="scope"></a>Kapsam
- Bu iş belgelerinin içerdiği satır sayısına bakmaksızın, Finance ve Supply Chain Management'tan Elektronik Faturalama hizmetine gönderilen iş belgelerinin sayısı.
- Elektronik Faturalama servisi tarafından başarıyla işlenen gönderilen iş belgelerinin sayısı. Özellik kurulumunda tanımlanan eylemlerin akışı tamamlandığında, bir belge başarıyla işlenmiş olarak kabul edilir.

> [!NOTE]
> Bir elektronik fatura harici bir web servisine gönderildiğinde, sayım işlemi web hizmeti işlemenin sonuçlarından (kabul edildi, reddedildi veya şema doğrulama hatası) bağımsız olur. Web servisi, Elektronik Faturalama servisinin isteğini alıp yanıtlamışsa gönderim geçerli bir sayım olarak kabul edilir.

- **Özel durum:** Finance ve Supply Chain Management'tan Elektronik Faturalama hizmetine yeniden gönderme yapıldığında iş belgeleri sayılmaz (örneğin elektronik faturanın durumunu değiştirmek için aynı iş belgesi yeniden giriş işlemi yapılması gerektiği senaryolarda). Örneğin, Brezilya elektronik faturasının (mali belge) gönderilmesi geçerli olarak sayılır, ancak bunun iptal isteği sayılmaz.


### <a name="calculation"></a>Hesaplama

Bakiye hesabı aşağıdaki gibi hesaplanır:

Bakiye = Ücretsiz + Satın alınan – Kullanılan

Where:

- Ücretsiz:
  
    Müşterinin ayda gönderebileceği, ücretsiz iş belgeleri hacmi. Elektronik Faturalama servisine gönderilebilecek 100 iş belgesi paketini içerir. Ücretsiz hacim birikimli değildir ve kalan bakiye bir sonraki döneme aktarılmaz.
  
- Satın alınan:
  
    Elektronik Faturalama servisine gönderilebilecek 1,000 iş belgesi paketi. Kuruluşunuz için aylık olarak bu paketin edinilmiş olması gerekir. Satın alınan hacim birikimli değildir ve kalan bakiye bir sonraki döneme aktarılmaz.
  
- Kullanılan: 

    Tanımlanan ölçütlere göre, Elektronik Faturalama servisine gönderilen iş belgesi sayısı.
   
> [!IMPORTANT]
> Organizasyonunuz, ücretsiz 100 gönderilik aylık hacmini aşmayı planlıyorsa, Elektronik Faturalama hizmeti için Microsoft lisans ilkesiyle uyumlu kalmasını sağlamak için zirve hacmi satın alın.
>
> Şu anda, satın alınan birimin, çoklu 1.000'lik gönderim paketi olarak alım tarihine göre el ile girilmesi gerekir.

## <a name="indicator-usage-by-feature"></a>Gösterge: Özelliğe göre kullanım

Bu gösterge, tanımlanan bir dönemde elektronik faturaların gönderilmesi için elektronik faturalama özelliklerinin kullanımını gösterir.

- Hesaplama:
  
    Kullanılan = İş belgelerinin Elektronik Faturalama hizmetine gönderilmesi sırasında her bir elektronik faturalama özelliğinin kaç kez kullanıldığı.

## <a name="indicator-usage-by-environment"></a>Gösterge: Ortama göre kullanım

Bu gösterge, tanımlanan bir dönem içindeki elektronik faturalama servis ortamlarının kullanımını gösterir.

- Hesaplama:
    
    Kullanılan = İş belgelerinin Elektronik Faturalama hizmetine gönderilmesi sırasında her bir elektronik faturalama servis ortamının kaç kez kullanıldığı.

## <a name="indicator-usage-per-month-import"></a>Gösterge: Aylık kullanım (içe aktar)

Bu gösterge, tanımlı bir dönemde Elektronik Faturalama servisi tarafından Finance ve Supply Chain Management'a göre elektronik faturaların içe aktarılma hacmini gösterir.

- Kapsam:

    Finance ve Supply Chain Management'a aktarılan elektronik faturalar, bu elektronik faturaların içerdiği satır sayısından bağımsızdır.

- Hesaplama:

    Alınan = Finance ve Supply Chain Management'a aktarılan elektronik faturaların sayısı.

## <a name="functions"></a>İşlevler
### <a name="purchase"></a>Satınalma

**Aylık kullanım (dışa aktar)** sekmesinde, alınan gönderimler tutarını el ile kaydetmek için **Satın al** öğesini seçin.

Belirli bir tarih için, **Yeni**'yi seçin ve bu tarihte elde edilen **Paketler** sayısını girin.

**Miktar** aşağıdaki şekilde hesaplanır:

Miktar = Paket * 1.000

Hesaplanan **Miktar**, **Ay başına gösterge (dışa aktar)** göstergesindeki **Satın alınan** değerini yansıtır.

### <a name="update"></a>Güncelleştirme

Eylem bölmesinde, hesaplamayı yenilemek ve sayfada ve grafikte gösterilen verileri güncelleştirmek için **Güncelleştir**'i seçin.

### <a name="reset-history-data"></a>Geçmiş verilerini sıfırla

Eylem bölmesinde, göstergelerin hesaplandığı veritabanını yenilemek için **Geçmiş verileri sıfırla**'yı seçin.




> [!NOTE]
> **Kullanım yönetimi** panosu, parasal tutarları göstermez. Bunun yerine, yalnızca sayılan gönderimlerin ve içe aktarılan belgelerin hacmini gösterir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

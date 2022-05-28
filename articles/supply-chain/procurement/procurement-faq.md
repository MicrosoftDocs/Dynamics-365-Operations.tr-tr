---
title: Tedarik ile ilgili SSS
description: Bu konuda, Supply Chain Management'ın tedarik işlevleri hakkında sık sorulan soruların (SSS) yanıtları sağlanmaktadır
author: GalynaFedorova
ms.date: 05/31/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 718108447dcb5cec488b7fa626feb551808e8dd8
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669362"
---
# <a name="procurement-faq"></a>Tedarik ile ilgili SSS

[!include [banner](../includes/banner.md)]

Bu konuda, Supply Chain Management'ın tedarik işlevleri hakkında sık sorulan soruların (SSS) yanıtları sağlanmaktadır.

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>Yalnızca oluşturduğum satınalma siparişlerini görüntüleyebilir miyim?

Bu işlev şu anda kullanılamıyor.

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>Bir satınalma siparişindeki stok rezerve edebilir ve kayıtlı stokla hareket oluşturabilir miyim?

### <a name="issue-description"></a>Sorun açıklaması

Malzemeler bir satınalma siparişi üzerinde *Kayıtlı* durumda olsa bile, yine de stoku rezerve edebilirsiniz. Başka bir deyişle, kayıtlı stok için hareketler oluşturabilirsiniz.

### <a name="reproduce-the-issue"></a>Sorunu yeniden oluşturma

Aşağıdaki yordamda, bu sorunu yeniden oluşturmanın bir yolu gösterilmektedir.

1. Bir satınalma siparişi oluşturmak.
2. Satınalma siparişi satırını kaydedin.
3. Kayıtlı stok için rezervasyon veya hareket üretebildiğinize dikkat edin.

### <a name="issue-resolution"></a>Sorunun çözümü

Bu davranış tasarımdan kaynaklanır. Bu, kayıtlı malzemelerin ambar veya stoka fiziksel olarak ulaşmış olması ve bu nedenle rezervasyon için kullanılabilir durumda olması beklenir.

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>Bir satınalma siparişini iptal eden kullanıcıyı bulabilir miyim?

Bu bilgiler yalnızca satınalma siparişi değişiklik yönetimine tabi olduğunda izlenir. Değişiklik yönetimini kullanıyorsanız, değişikliği kimlerin göndermiş olduğunu (iptal) ve kimin onayladığını görebilirsiniz.

## <a name="why-cant-i-link-a-purchase-agreement-to-an-existing-purchase-order"></a>Neden satınalma sözleşmesini mevcut bir satınalma siparişine bağlayamıyorum?

Satınalma siparişi oluşturulduğunda bir satınalma siparişinin bir satınalma sözleşmesi ile ilişkilendirilmesi gerekir. Aksi takdirde, satınalma siparişi satırları satınalma sözleşmesi satırlarıyla ilişkilendirilemez.

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>"El ile veya harici belge ile girilen fiyatları ve indirimleri güncelleştir" iletisinin görünmesine neden olan denetimler nelerdir?

Sevkiyat tarihini değiştirdiğinizde, "El ile veya harici belge ile girilen fiyatları ve indirimleri güncelleştir" şeklinde bir ileti alabilirsiniz. Bu iletiyi alırsınız; çünkü sevkiyat tarihi değiştirilirse farklı bir ticaret veya satış sözleşmesi tetiklenebilir ve bir fiyat değişikliğine neden olabilir. Sevkiyat tarihinde yapılan bir değişiklik ambar zamanlamalarını ve diğer ilgili bilgileri de etkileyebilir.

İleti, herhangi bir tarih veya başka parametre değiştiğinde tetiklenir. İletinin amacı, bu değişikliklerden dolayı oluşabilecek fiyat değişikliklerinin farkında olduğunuzdan emin olmak içindir.

Bu ileti ticari sözleşme değerlendirme (TAE) istemidir. Tam açıklama için bkz. [Ticari sözleşme değerlendirme ilkeleri](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).

## <a name="why-cant-i-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>Neden kategori tabanlı maddeler içeren bir satınalma siparişi satırı için birden fazla faturayı deftere nakledemiyorum?

Faturaları deftere nakletmek istiyorsanız miktar değeri zorunludur. Bu nedenle, bir satırın tam miktarı yalnızca kısmi bir tutar için faturalanmışsa, kalan tutarı başka bir faturada faturalayamazsınız.

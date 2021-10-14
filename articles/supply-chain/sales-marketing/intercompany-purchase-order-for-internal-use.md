---
title: Dahili kullanım için bir şirketlerarası satın alma siparişi oluşturma ve faturalama
description: Bu konuda, dahili kullanım için şirketlerarası satın alma siparişinin nasıl oluşturulacağı ve faturalanacağı açıklanmaktadır
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 88a14ff962c5cf0cd1cff24b16cc7a62e9e1c8ce
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548584"
---
# <a name="create-and-invoice-an-intercompany-purchase-order-for-internal-use"></a>Dahili kullanım için bir şirketlerarası satın alma siparişi oluşturma ve faturalama

[!include [banner](../../includes/banner.md)]

Şirketlerarası satıcı için şirketlerarası satın alma siparişi oluşturabilirsiniz. Bu, şirketlerarası satıcıda otomatik olarak bir şirketlerarası satış siparişi oluşturur.

![Şirketlerarası dahili satın alma süreci](media/intercompanypurchaseprocess.png)

## <a name="create-an-intercompany-purchase-order-and-a-corresponding-intercompany-sales-order"></a>Şirketlerarası satın alma siparişi ve buna karşılık gelen bir şirketlerarası satış siparişi oluşturma

Bu adımları, resimde gösterildiği gibi tüzel kişilik AAA'da gerçekleştirin.

1. **Borç hesapları** \> **Satın alma siparişleri** \> **Tüm satın alma siparişleri**'ni seçin.
1. **Tüm satın alma siparişleri** liste sayfasında, şirketlerarası satıcı için bir satın alma siparişi oluşturun. Alan değerleri satıcı hesabından satın alma siparişine kopyalanır.

    Şirketlerarası bir satıcıyla çalıştığınız için satıcıya karşılık gelen tüzel kişilikte bir şirketlerarası satış siparişi oluşturulur. Şirketlerarası satış siparişi numarası, şirketlerarası satın alma siparişi numarası ile aynı olabilir ve tüzel kişiliğin kimliğini içerebilir. Kullanılan numara yapısı **Şirketlerarası** sayfasındaki **Satış siparişi numaralandırma** alanındaki seçime bağlıdır. Örneğin, tüzel kişilik AAA'da 00029\_064 numaralı bir satın alma siparişi oluşturursanız tüzel kişilik BBB'deki satış siparişi numarası AAA00029\_64'tür.

    Bir bilgi iletisinde, şirketlerarası satınalma siparişinin ve şirketlerarası satış siparişinin oluşturulduğu bildirilir. İleti, sizi bilgilendirmek kamacıyla şirketlerarası satış siparişi numarasını içerir.

1. Satın alma siparişine satır maddeleri ekleyin. Karşılık gelen satır maddeleri, şirketlerarası satış siparişine otomatik olarak eklenir. Diğer tüzel kişilikte bir madde mevcut değilse bir ileti görüntülenir ve maddeyi satın alma siparişine ekleyemezsiniz. Bu sorunu gidermek için diğer tüzel kişiliğe geçin ve ürünü bu tüzel kişilikte serbest bırakın. Madde, o tüzel kişilikteki satış siparişlerine eklenebilir durumda olacaktır. Ardından, satın alma siparişinin tüzel kişiliğine geri dönün ve satır maddeleri eklemeye devam edin.
1. Satın alma siparişi için bilgileri girmeyi tamamladığınızda girişlerinizi onaylayın.

## <a name="process-the-intercompany-packing-slip-and-customer-invoice"></a>Şirketlerarası sevk irsaliyesini ve müşteri faturasını işleme

Bu adımları, resimde gösterildiği gibi tüzel kişilik BBB'de gerçekleştirin.

1. **Alacak hesapları \> Satış siparişi \> Tüm satış siparişleri**'sayfasına gidin.
1. **Tüm satış siparişleri** liste sayfasında, şirketlerarası satış siparişini seçin.
1. Eylem Bölmesi'nde **Çek ve paketle** sekmesini seçin ve ardından **Sevk irsaliyesi**'ni seçin.
1. **Deftere nakletme** onay kutusunu seçin.
1. **Tamam**'ı seçin. Sevk irsaliyesi, tüzel kişilik BBB'ye kaydedilir.
1. **Tüm satış siparişleri** liste sayfasında, şirketlerarası satış siparişini seçin.
1. Eylem Bölmesi'nde **Fatura** ve ardından **Fatura** sekmesini seçin.
1. **Deftere nakletme** onay kutusunu seçin.
1. **Tamam**'ı seçin.

    Şirketlerarası satış siparişi için müşteri faturası, tüzel kişilik BBB'ye kaydedilir.

## <a name="process-the-intercompany-product-receipt-and-vendor-invoice"></a>Şirketlerarası ürün girişini ve satıcı faturasını işleme

Bu adımları, resimde gösterildiği gibi tüzel kişilik AAA'da gerçekleştirin.

1. **Borç hesapları \> Satın alma siparişleri \> Tüm satınalma siparişleri**'ne gidin.
1. **Tüm satın alma siparişleri** liste sayfasında şirketlerarası satın alma siparişini seçin.
1. Eylem Bölmesi'nde **Teslim al**'ı ve ardından **Ürün girişi**'ni seçin. Ürün girişi oluşturulur. Ürün giriş numarası, şirketlerarası sevk irsaliyesi numarası ile aynıdır.
1. **Deftere nakletme** onay kutusunu seçin.
1. **Tamam**'ı seçin.
1. **Tüm satın alma siparişleri** liste sayfasında şirketlerarası satın alma siparişini seçin.
1. Eylem Bölmesi'nde **Fatura**'yı ve ardından **Fatura**'yı seçin. Satıcı faturası oluşturulur. Satıcı fatura numarası, şirketlerarası müşteri fatura numarası ile aynıdır.
1. Satıcı faturası girişini tamamlayın ve ardından deftere nakledin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

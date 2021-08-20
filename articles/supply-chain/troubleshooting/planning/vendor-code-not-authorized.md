---
title: Satıcı kodu belirli bir ürün ve tarih için yetkilendirilmemiş
description: Planlı siparişi kesinleştirmeyi veya satınalma siparişine satır eklemeyi denediğinizde, satıcı kodunun bir ürün ve tarih için yetkilendirilmemiş olduğunu belirten bir hata iletisi alırsınız.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 67cb054a648eac2b9a0e89b5e6a645af3c6142ad25237adb7afbd28f96c7e2eb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777731"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a>Satıcı kodu belirli bir ürün ve tarih için yetkilendirilmemiş

Hata kodu: SYP4881415

## <a name="symptoms"></a>Belirtiler

Planlı siparişi kesinleştirmeye veya bir satınalma siparişine satır eklemeye çalıştığınızda, aşağıdaki hata iletisini alırsınız:

> %1 satıcı kodu %3 konumundaki %2 için yetkili değil.

## <a name="cause"></a>Nedeni

Bu hata, **Onaylanan satıcı denetimi yöntemi** alanı belirtilen ürün için *Yalnızca uyarı* veya *İzin verilmiyor* olarak ayarlandığı ve satıcı o ürünü tedarik yetkisine sahip olmadığı için oluşur.

## <a name="resolution"></a>Çözüm

Bu sorunu gidermek için, ilgili ürünün satıcı denetimini devre dışı bırakın ya da satıcıyı onaylayın.

Bir ürünün satıcı denetimini devre dışı bırakmak için aşağıdaki adımları izleyin.

1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. İlgili ürünü açın.
1. **Satınalma** hızlı sekmesinde, **Onaylanmış satıcı denetimi yöntemi** alanını *Yalnızca uyarı* veya *İzin verilmiyor* dışında bir değere ayarlayın.

Ürün için satıcıyı onaylamak üzere şu adımları izleyin.

1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. İlgili maddeyi açın.
1. Eylem Bölmesi'nde, **Satın al** sekmesindeki **Onaylanan satıcı** grubunda **Ayar**'ı seçin.
1. **Onaylanan satıcı** liste sayfasında ızgaraya satır eklemeyin ve ardından aşağıdaki değerleri ayarlayın:

    - **Satıcı**: Geçerli ürün için onaylanacak satıcıyı seçin.
    - **Geçerlilik tarihi**: Satıcının onaylandığı ilk tarihi seçin.
    - **Sona erme tarihi**: Satıcının onaylandığı son tarihi seçin.

Daha fazla bilgi için bkz. [Belirli ürünler için satıcıları onaylama](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).

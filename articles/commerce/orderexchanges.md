---
title: Bir iade emrinde bir değişiklik yapılandırma ve işleme
description: Bu konuda, Dynamics 365 Commerce için bir iadede bir değişikliğin nasıl yapılandırılacağı açıklanmaktadır.
author: josaw1
ms.date: 07/28/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 488f6fb5af6451bc462566a9714054b49eb1a80b8264528778797f6a39647764
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758348"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a>Bir iade emrinde bir değişiklik yapılandırma ve işleme

[!include [banner](includes/banner.md)]

Dynamics 365 Commerce uygulamasının önceki sürümlerinde, müşteri siparişlerine göre iadeler Genel Merkez'deki iade emri belgesi kullanılarak işlenmiştir. Ancak iade emri belgesi yalnızca iade edilen ürünleri işlemek için kullanılabilir. İade edilen ürünler, iade emri satırlarında bir eksi miktarla belirtilir. Bunun aksine, satışlar ise artı bir miktarla gösterilir. Ancak iade emri belgesi artı miktarları desteklemez. Bu kısıtlama nedeniyle, uygulamanın önceki sürümleri ürün değişikliklerinin iade emri belgesi kullanılarak yapıldığı senaryoları desteklememiştir.

Ancak, değişikliklerin iade emirlerinde yapıldığı senaryoları desteklemek için işlevler eklenmiştir. Commerce artık bu tür hareketleri işlemek için iade emri belgesi yerine satış siparişi belgesini kullanmaktadır.

## <a name="configure-commerce-to-support-exchanges-on-return-orders"></a>Commerce uygulamasını iade emirlerinde değişiklikleri destekleyecek şekilde yapılandırma

> [!NOTE]
> Commerce sürüm 10.0.20 ve sonraki sürümlerde, "POS'ta birleşik iade işleme deneyimi" olarak adlandırılan yeni bir özellik mevcuttur. Bu özelliği etkinleştirirseniz aşağıdaki kurulum adımları gerekmez. **İadeleri satış siparişleri olarak işle** kalıcı olarak yapılandırılmış bir ayar haline gelir ve bunu değiştiremezsiniz.

Sistemi iade emirlerinde değişiklikleri destekleyecek şekilde yapılandırmak için (**POS'ta birleşik iade işleme deneyimi** özelliği etkin değilse) şu adımları izleyin.

1. **Retail ve Commerce \> Genel merkez ayarı \> Parametreler \> Commerce parametreleri**'ne gidin. **Müşteri siparişleri** hızlı sekmesinde, **İade emirlerine satış siparişleri olarak işlem yap** seçeneğini **Evet** olarak ayarlayın.
2. **Genel yapılandırma dağıtım planı** işini (**1110**) çalıştırın.

## <a name="make-an-exchange"></a>Değişiklik yapma

Sistem önceki bölümde açıklandığı gibi yapılandırıldıktan sonra, satış noktası (POS) kullanıcısının uygulamanın önceki sürümlerinde olduğu gibi bir iadeye işlem yapmak için yine bir satış siparişi veya satış faturası seçmesi gerekir. Ancak iade maddeler sepete eklendikten sonra, kullanıcı yeni satış satırlarını sepete ekleyebilir.

Kullanıcı, bu yeni satış satırları için bir müşteri sipariş satırını işlemek amacıyla gerekli olan tüm öznitelikleri tanımlamalıdır. Bu öznitelikler, teslimat yöntemini ve karşılama konumunu içerir. Hareket için yapılması gereken ödeme iade emri satırları ile satış siparişi satırlarının net değeri olacaktır. Hareketin ödemesi yapıldıktan sonra, iade emri Genel Merkez'de satış siparişi belgesi olarak deftere nakledilir ve sistem, iade satırlarını derhal faturalandırır.

Sepet için çeşitli tutarlara yönelik daha iyi bir görüş sağlamak üzere, sepete üç yeni tutar alanı eklenmiştir. Bu yeni alanların POS kullanıcı arabiriminde kullanılabilmesini sağlamak için ekran tasarımcısını kullanabilirsiniz.

- **Uygulanan havale**: Kullanıcı bir müşteri siparişi teslim alma hareketi gerçekleştirdiğinde bir işlemde uygulanan havale tutarı. Havale geçersiz kılma işlemi yoksa ve yüzde 10 havale yapılandırıldıysa bu alandaki tutar müşteri siparişinin toplam tutarının yüzde 90'ıdır.
- **Gerçekleşen tutar**: Müşteri siparişi oluşturulduğunda veya düzenlendiğinde ya da bir müşteri siparişi değişikliği sırasında teslimat şeklinin **Gerçekleştirme** olarak ayarlandığı satırların toplam tutarı. Bu alandaki tutar, vergileri ve masrafları içerir.
- **İade tutarı**: Müşteri siparişi değişikliği sırasında eksi miktarlar içeren satırların toplam tutarı. Bu alandaki tutar, vergileri ve masrafları içerir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

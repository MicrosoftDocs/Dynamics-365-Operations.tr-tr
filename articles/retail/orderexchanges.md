---
title: "Bir iade emrinde bir değişiklik yapılandırma ve işleme"
description: "Bu konuda, Microsoft Dynamics 365 for Retail için bir iadede bir değişikliğin nasıl yapılandırılacağı açıklanmaktadır."
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 3331b984693c58c6ee8c49b98ed7d3a8df5b79ff
ms.openlocfilehash: 45b628376a483d3d639e5c018dd93570ed8ce7af
ms.contentlocale: tr-tr
ms.lasthandoff: 12/04/2018

---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a>Bir iade emrinde bir değişiklik yapılandırma ve işleme

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 for Retail'ın önceki sürümlerinde, müşteri siparişlerine göre iadeler Retail Headquarters'daki iade emri belgesi kullanılarak işlenmiştir. Ancak, iade emri belgesi yalnızca iade edilen ürünleri işlemek için kullanılabilir. İade edilen ürünler, iade emri satırlarında bir eksi miktarla belirtilir. Bunun aksine, satışlar ise artı bir miktarla gösterilir. Ancak, iade emri belgesi artı miktarları desteklemez. Bu kısıtlama nedeniyle, Retail'ın önceki sürümleri ürün değişikliklerinin iade emri belgesi kullanılarak yapıldığı senaryoları desteklememiştir.

Ancak, değişikliklerin iade emirlerinde yapıldığı senaryoları desteklemek için işlevler eklenmiştir. Retail artık bu tür hareketleri işlemek için iade emri belgesi yerine satış siparişi belgesini kullanmaktadır.

## <a name="configure-retail-to-support-exchanges-on-return-orders"></a>Retail'ı iade emirlerinde değişiklikleri destekleyecek şekilde yapılandırma

Sistemi, iade emirlerinde değişiklikleri destekleyecek şekilde yapılandırmak için bu adımları izleyin.

1. **Retail \> Headquarters ayarı \> Parametreler \> Retail parametreleri**'ne gidin. **Müşteri siparişleri** hızlı sekmesinde, **İade emirlerine satış siparişleri olarak işlem yap** seçeneğini **Evet** olarak ayarlayın.
2. **Genel yapılandırma dağıtım planı** işini (**1110**) çalıştırın.

## <a name="make-an-exchange"></a>Değişiklik yapma

Sistem önceki bölümde açıklandığı gibi yapılandırıldıktan sonra, satış noktası (POS) kullanıcısının Retail'ın önceki sürümlerinde olduğu gibi bir iadeye işlem yapmak için yine bir satış siparişi veya satış faturası seçmesi gerekir. Ancak iade maddeler sepete eklendikten sonra, kullanıcı yeni satış satırlarını sepete ekleyebilir.

Kullanıcı, bu yeni satış satırları için bir müşteri sipariş satırını işlemek amacıyla gerekli olan tüm öznitelikleri tanımlamalıdır. Bu öznitelikler, teslimat yöntemini ve karşılama konumunu içerir. Hareket için yapılması gereken ödeme iade emri satırları ile satış siparişi satırlarının net değeri olacaktır. Hareketin ödemesi yapıldıktan sonra, iade emri Retail Headquarters'da satış siparişi belgesi olarak kaydedilir ve sistem, iade satırlarını derhal faturalandırır.

Sepet için çeşitli tutarlara yönelik daha iyi bir görüş sağlamak üzere, sepete üç yeni tutar alanı eklenmiştir. Bu yeni alanların POS kullanıcı arabiriminde kullanılabilmesini sağlamak için ekran tasarımcısını kullanabilirsiniz.

- **Uygulanan havale**: Kullanıcı bir müşteri siparişi teslim alma hareketi gerçekleştirdiğinde bir işlemde uygulanan havale tutarı. Havale geçersiz kılma işlemi yoksa ve yüzde 10 havale yapılandırıldıysa bu alandaki tutar müşteri siparişinin toplam tutarının yüzde 90'ıdır.
- **Gerçekleşen tutar**: Müşteri siparişi oluşturulduğunda veya düzenlendiğinde ya da bir müşteri siparişi değişikliği sırasında teslimat şeklinin **Gerçekleştirme** olarak ayarlandığı satırların toplam tutarı. Bu alandaki tutar, vergileri ve masrafları içerir.
- **İade tutarı**: Müşteri siparişi değişikliği sırasında eksi miktarlar içeren satırların toplam tutarı. Bu alandaki tutar, vergileri ve masrafları içerir.


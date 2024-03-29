---
title: Standart maliyetleri imalat dışı bir ortamda güncelleme
description: Bu makalede, imalat dışı bir ortamda standart maliyetlerin güncellenmesine yönelik yönergeler sağlanmıştır.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 548955f544842ea5f60fd2d800c8c11cb459ee4c
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679093"
---
# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a>Standart maliyetleri imalat dışı bir ortamda güncelleme

[!include [banner](../includes/banner.md)]

Bu makalede, imalat dışı bir ortamda standart maliyetlerin güncellenmesine yönelik yönergeler sağlanmıştır.

Aşağıdaki yönergelerde, standart maliyeti iki sürümlü bir yaklaşım kullanarak güncellediğiniz varsayılmaktadır. Bu yaklaşımda bir maliyet sürümü orijinal olarak donmuş dönem için tanımlanmış olan standart maliyetleri, ikinci maliyetlendirme sürümü ise artımlı güncellemeleri içerir. Her güncelleme, ikinci maliyetlendirme sürümüne alınmış bir maliyet kaydı olarak girilir ve nihayetinden etkinleştirilir. Bir alternatif, orijinal olarak tanımlanmış olan standart maliyetler kümesini kullanan tek sürümlü yaklaşımdır. İki sürümlü yaklaşım ikinci bir maliyetlendirme sürümü tanımlamanızı gerektirir. Bu maliyetlendirme sürümünü tanımlamaya yönelik yönergeler şunlardır:

-   Bir **Standart maliyetler** maliyetlendirme türü atayın.
-   Maliyetlendirme sürümünün içeriklerini belirtmek için **2016-UPDATES** gibi anlamlı bir tanımlayıcı atayın.
-   İçeriklerin maliyet kayıtlarını içerdiğinden emin olun.
-   Maliyet kayıtlarının tüm tesisler için girilmesine izin verin. Bir tesis belirtirseniz, maliyet kayıtları yalnızca o tesis için girilebilir.
-   Geri dönüş ilkesini **Hiç** olarak belirtin. Geri dönül ilkesi yalnızca mamul maddelere yönelik maliyet hesaplamaları için geçerlidir.

Yeni maddeler için standart maliyetleri düzeltmek, ayarlamak veya güncellemek üzere aşağıdaki adımları izleyin.

1.  Maliyet verilerinin ikinci maliyetlendirme sürümüne girilebilmesini sağlamak için **Maliyetlendirme sürümü** **ayarlar** sayfasını kullanın. İsteğe bağlı olarak, bekleyen maliyetlerin etkinleştirilmesini önleyin, böylelikle etkinleştirme bekleyen maliyetler tamamen ve doğru şekilde tanımlandıktan sonra mümkün olacaktır. Ayrıca isteğe bağlı olarak **Başlangıç tarihi** alanına bir tarih de girebilirsiniz. Genel bir yönerge olarak, artımlı güncellemelere izin vermek istediğinizde tarih kullanın. Alternatif olarak **Başlangıç tarihi** alanını maliyetlendirme sürümü için boş bırakın ve ardından her bir maliyet kaydı için **Başlangıç tarihi** alanına bir tarih girin.
2.  Güncellemeleri ikinci maliyetlendirme sürümüne alınmış madde maliyet kayıtları olarak girmek için **Madde fiyatı** sayfasını kullanın.
3.  İkinci maliyetlendirme sürümüne alınmış madde maliyet kayıtlarının tam ve doğruluğunu doğrulamak için **Madde fiyatları** raporunu kullanın.
4.  İkinci maliyetlendirme sürümüne alınmış bekleyen maliyet kayıtlarının etkinleştirilmesine izin vermek için engelleme bayrağını değiştirmek üzere **Maliyetlendirme sürüm bakımı** sayfasını kullanın.
5.  İkinci maliyetlendirme sürümüne alınmış tüm bekleyen madde maliyet kayıtlarını etkinleştirmek için **Etkin fiyatlar** sayfasını (**Maliyetlendirme sürüm bakımı** sayfasından açabilirsiniz) kullanın. Tek tek maddelere yönelik bekleyen maliyet kayıtlarını **Madde fiyatı** sayfasında **Bekleyen fiyatı etkinleştir** düğmesine tıklayarak da etkinleştirebilirsiniz.
6.  Ek veri bakımını önlemek için, **Maliyetlendirme sürümü ayarları** sayfasını kullanarak ikinci maliyetlendirme sürümüne alınmış engelleme bayraklarını değiştirin. Durdurma ilkeleri yeni bekleyen maliyetler girilmesini ve bekleyen maliyetlerin etkinleştirilmesini önler.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
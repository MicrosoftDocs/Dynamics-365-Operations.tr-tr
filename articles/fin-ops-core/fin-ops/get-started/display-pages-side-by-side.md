---
title: Yeni pencerede aç özelliğini kullanarak sayfaları yan yana gösterme
description: Bu makale, sayfaları nasıl yan yana görüntüleyebileceğinizi açıklar.
author: aneesmsft
manager: AnnBe
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35ade352edf31fe895a9b9118a8ad7d5fe6c0bde
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798415"
---
# <a name="show-pages-side-by-side-using-the-open-in-new-window-feature"></a>Yeni pencerede aç özelliğini kullanarak sayfaları yan yana gösterme

[!include [banner](../includes/banner.md)]

Bu makalede, sayfaları nasıl yan yana görüntüleyebileceğiniz açıklanmaktadır.

Görevleri hızlı bir şekilde tamamlamak için birden fazla sayfayı yan yana görüntülemek isteyebilirsiniz. Örneğin, birden fazla günlükteki satırları doğrulamak veya girmek isteyebilirsiniz. Genellikle, doğrulamak veya birden fazla günşüğe satır girkmek için günlüklerin bir listesinin görüntülendiği sayfa ve belirli bir günlüğün satırlarının görüntülendiği sayfa arasında gidip gelmek zorunda kalırsınız. Ancak, **Yeni pencerede aç** özelliği, bu sayfaları yan yana görüntüleyerek görevlerinizi hızlı bir şekilde gerçekleştirebilmenizi sağlar.

Yukarıda örnekten devam: satırları görüntülerken **Yeni pencerede aç** simgesine tıklayabilirsiniz.

[![Yeni pencerede aç simgesine tıklayın.](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)

**Yeni pencerede aç** simgesine tıklamak satırlar sayfasını yeni bir açılır tarayıcıda açar ve ardından orijinal tarayıcıyı günlüklerin listesinin görüntülendiği geçmiş sayfasına geri döndürür. Bunun ardından her iki sayfayı yan yana görüntüleyebilirsiniz. Günlüğü görüntüledikten sonra, günlük listesi sayfasındaki seçili günlüğü değiştirebilirsiniz; açılan penceredeki satırlar sayfası, yeni seçilen günlüğün satırlarını otomatik olarak görüntüler.

[![Sayfaları yan yana görüntüleyebilirsiniz.](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)

Bu sayfaların arka planındaki veriler arasında var olan ilişkiler sayesinde bağlantıyı dinamik etkinleştirme ve yenileme gerçekleşir. Sistem veriler arasındaki ilişkiyi bilmiyorsa, açılır pencere, kaynağı olan penceredeki değişikliğe yanıt olarak otomatik yenilenmez.

Bazı sayfalarda Kılavuz görünümü, Başlık görünümü ve Ayrıntı görünümü gibi birden çok görünüm vardır. **Yeni pencerede aç** simgesi, tüm sayfanın yeni bir tarayıcı penceresinde açılmasına neden olur. Bu nedenle, **Yeni pencerede aç** özelliğini kullanarak aynı sayfanın iki görünümünü yan yana tutamazsınız. Bu sayfaların hemen hemen hepsinde, kayıtlar arasında geçiş yapmak ve benzer bir deneyim elde etmek için kullanabileceğiniz bir gezinti listesi vardır.

**Yeni pencerede aç** özelliğini kullanabilmeniz için, sitenin URL'sinden açılır pencerelere izin vermek için tarayıcınızın açılır pencere engelleyicisini yapılandırmanız gerekir. Örneğin "\*. dynamics.com"dan açılır pencerelere izin verebilirsiniz.

**Yeni pencerede aç** özelliği yalnızca pencerede birden fazla sayfa açık olduğu zaman kullanılabilir. Ayrıca, açılır pencere, artık sayfada açık sayfa kalmadığı zaman (yani penceredeki son sayfayı kapattığınızda) otomatik olarak kapanır. Uygulamada başka bir alana gittiğinizde sistem de açık sayfaları kapatır. Bu nedenle, açık açılır pencereleriniz varsa ve uygulamada başka bir alana giderseniz, sistem bu pencerelerdeki sayfaları kapatacağından açılır pencereler otomatik olarak kapatılır.

Açılır pencerelerin üst çubuğunda, sayfanın salt okunur olarak açıldığı şirket hakkında bilgiler görüntülenir. Açılır pencereler de ana tarayıcı penceresine bağlıdır. Ana pencere kapatılır veya yenilenirse, açık tüm açılır pencereler salt okunur duruma geçer. Bu durum gerçekleşirse bu pencerelerde bilgileri görüntülemeye devam edebilirsiniz ancak onlarla etkileşime giremezsiniz.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
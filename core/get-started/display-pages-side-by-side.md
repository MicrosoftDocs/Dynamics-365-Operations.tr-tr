---
title: "Yeni Pencerede Aç simgesini kullanarak sayfaları yan yana görüntüleme"
description: "Bu makale, Microsoft Dynamics 365 for Finance and Operations'da sayfaların yan yana nasıl görüntüleneceğini açıklar."
author: aneesmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: aad98247692bdbaf5b8023b393b5e33260dd0b1a
ms.contentlocale: tr-tr
ms.lasthandoff: 06/13/2017

---

# <a name="display-pages-side-by-side-using-the-open-in-new-window-icon"></a>Yeni Pencerede Aç simgesini kullanarak sayfaları yan yana görüntüleme

[!include[banner](../includes/banner.md)]


Bu makale, Microsoft Dynamics 365 for Finance and Operations'da sayfaların yan yana nasıl görüntüleneceğini açıklar.

Microsoft Dynamics 365 for Finance and Operations görevleri verimli bir şekilde gerçekleştirmenize yardımcı olur. Bazı durumlarda, görevleri hızlı bir şekilde tamamlamak için birden fazla sayfayı yan yana görüntülemek isteyebilirsiniz. Örneğin, birden fazla günlükteki satırları doğrulamak veya girmek isteyebilirsiniz. Genellikle bunu yapmak için günlüklerin bir listesinin görüntülendiği sayfa ve belirli bir günlüğün satırlarının görüntülendiği sayfa arasında gidip gelmek zorunda kalırsınız. Ancak, **Yeni pencerede aç** özelliği, bu sayfaları yan yana görüntüleyerek görevlerinizi hızlı bir şekilde gerçekleştirebilmenizi sağlar. Yukarıda örnekten devam: satırları görüntülerken **Yeni pencerede aç** simgesine tıklayabilirsiniz. [![yeni-pencerede-ac-simgesi](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png) **Yeni pencerede aç** simgesine tıklanınca, satırlar sayfası yeni açılan bir tarayıcı penceresinde görüntülenir ve ardından, günlükler listesinin görüntülendiği sayfaya geri döner. Bunun ardından her iki sayfayı yan yana görüntüleyebilirsiniz. Günlük görüntülemeyi tamamladığınızda, günlük listesi sayfasındaki seçili günlüğü değiştirebilirsiniz; açılan penceredeki satırlar sayfası, yeni seçilen günlüğün satırlarını otomatik olarak görüntüler. [![sayfalari-yan-yana-goster](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)Bu sayfaların arka planındaki veriler arasında var olan ilişkiler sayesinde bağlantıyı dinamik etkinleştirme ve yenileme gerçekleşir. Sistem veriler arasındaki ilişkiyi bilmiyorsa, açılır pencere, kaynağı olan penceredeki değişikliğe yanıt olarak otomatik yenilenmez. Bazı sayfalarda Kılavuz görünümü, Başlık görünümü ve Ayrıntı görünümü gibi birden çok görünüm vardır. **Yeni pencerede aç** simgesi, tüm sayfanın yeni bir tarayıcı penceresinde açılmasına neden olur. Bu nedenle, **Yeni pencerede aç** özelliğini kullanarak aynı sayfanın iki görünümünü yan yana tutamazsınız. Ancak, bu sayfaların hemen hemen hepsinde, kayıtlar arasında geçiş yapmak ve benzer bir deneyim elde etmek için kullanabileceğiniz bir gezinti listesi vardır. **Yeni pencerede aç** özelliğini kullanabilmeniz için, Finance and Operations sitesinin URL'sinden açılır pencerelere izin vermek için tarayıcınızın açılır pencere engelleyicisini yapılandırmanız gerekir. Örneğin "\*. dynamics.com"dan açılır pencerelere izin verebilirsiniz. **Yeni pencerede aç** özelliği yalnızca pencerede birden fazla sayfa açık olduğu zaman kullanılabilir. Ayrıca, açılır pencere, artık sayfada açık sayfa kalmadığı zaman (yani penceredeki son sayfa kapatıldığında) otomatik olarak kapanır. Ayrıca uygulamada başka bir alana gittiğinizde Finance and Operations açık sayfaları da kapatır. Bu nedenle, açık açılır pencereleriniz varsa ve uygulamada başka bir alana giderseniz, bu pencerelerdeki sayfalar sistem tarafından kapatılacağı için, açılır pencereler otomatik olarak kapanır. Açılır pencerelerin üst çubuğunda, sayfanın salt okunur olarak açıldığı şirket hakkında bilgiler görüntülenir. Açılır pencereler de ana Finance and Operations tarayıcı penceresine bağlıdır. Ana pencere kapatılır veya yenilenirse, açık tüm açılır pencereler salt okunur duruma geçer. Bu, bu pencerelerde bilgileri yalnızca görüntüleyebileceğiniz, ancak onlarla etkileşime giremeyeceğiniz anlamına gelir.





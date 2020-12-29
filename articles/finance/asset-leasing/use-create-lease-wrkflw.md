---
title: Kira onayı iş akışları kullanma
description: Bu konu, varlık kiralamalarını onaylamak için iş akışlarının nasıl kullanılacağını ve iş akışlarının durumunu ve geçmişini nasıl izleyeceğinizi açıklamaktadır.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1805e1f87ee70a1f35d9105b8f7ad6c95861efcc
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4449028"
---
# <a name="use-lease-approval-workflows"></a>Kira onayı iş akışları kullanma

[!include [banner](../includes/banner.md)]

Bu konu, varlık kiralamalarını onaylamak için iş akışlarının nasıl kullanılacağını ve iş akışlarının durumunu ve geçmişini nasıl izleyeceğinizi açıklamaktadır. İş akışları, standart bir onay adımları kümesi sağlayarak ve sürecin her adımını onaylayan belirli kullanıcıları atayarak kiralama onayları yönetiminin tutarlı olmasına yardımcı olur. Onaylayan kullanıcı, bir kiralamayı onaylayabilir, reddedebilir, bir değişiklik isteyebilir veya bunu onay için başka bir kullanıcıya atayabilir. İş akışları, durum ve geçmişlerini izlemenize olanak tanıyarak onay işlemine dair daha fazla görünürlük de sunar. Ek olarak, belirli onaylayanlara atanan görevleri ve onayları listeleyen merkezi bir çalışma listesi görebilirsiniz.

Bu yordamı kullanmadan önce, en azından bir kiralama onayı iş akışının oluşturulduğundan emin olun. İş akışı yoksa oluşturun. İş akışının nasıl ayarlanacağı hakkında bilgi için bkz. [Kiralama onayı iş akışlarını ayarlama](set-up-lease-wrkflw.md).

1. Kiralamayı onaya gönderin. Kiralama için **Defter ayrıntıları** sayfasında, **İş akışı**'nı seçin ve ardından **Gönder**'i seçin.
2. Görüntülenen iletişim kutusunda açıklama ekleyebilirsiniz. Atanan onaylayan kiralamayla birlikte bu yorumu da görür. Yorum girme işlemini tamamladığınızda **Gönder**'i seçin. Kiralama, iş akışı sistemine gönderilir ve onaylayan kişi bunu onay için alır.
3. Onay için atanmış olan kiralamaları görüntülemek için **Modüller \> Ortak \> İş öğeleri \> Bana atanan iş öğeleri** bölümüne gidin.
4. **Bana atanan iş öğeleri** sayfasında, görüntülemek istediğiniz kiralamaya ait **Kiralama Kimliği** bağlantısını seçin. Gösterilen sayfa, erişim izniniz olan kiralama defterlerine ve kiralama ayrıntılarına bağlıdır.
5. Kirayı görüntülemeyi bitirdiğinizde, **İş akışı**'nı seçin ve hangi eylemin gerçekleştirilmesi gerektiğine karar verin. Seçenekler arasında **Onayla**, **Reddedildi**, **Değişiklik iste**, **Temsilci ata** ve **İptal edildi** yer alır. Seçili kiralama için onay geçmişini görüntülemek üzere **Geçmişi görüntüle**'yi de seçebilirsiniz.
6. Bir eylem seçtikten sonra, eylemi açıklayan bir yorum girin. Yorumu girmeyi bitirdiğinizde, listeden **Onaylandı** eylemi seçin.
7. Onay eylemlerini görüntülemek için **Kiralama özeti** sayfasındaki **Kiralama ayrıntıları** sayfasına dönün ve **İş Akışı \> Görüntüleme geçmişi**'ni seçin.

    İş akışı etkinliklerini **İş akışı geçmişi** sayfasında görüntüleyebilirsiniz. Bu sayfa, belirli bir kiralama üzerinde gerçekleştirilen iş akışı adımlarını gösterir. Atanan iş öğelerinin durumunu görmek için **İş öğeleri** alanını da kullanabilirsiniz.

8. Bir iş akışını durdurmak için **İş akışı geçmişi** sayfasında **Yakala**'yı seçin. Görüntülenen iletişim kutusunda yorum girin ve **Tamam**'ı seçin.
9. Bir iş akışını devre dışı bırakmak veya önceden oluşturulmuş bir iş akışını etkinleştirmek için **Varlık kiralama \> Kurulum \> Kiralama iş akışı** bölümüne gidin. Ardından, **Kiralama iş akışı** sayfasında **İş akışı \> Sürümler**'i seçin. Geçerli bir iş akışını devre dışı bırakmak için kiralama sürümü iletişim kutusunda etkin kirayı seçin ve ardından **Devre dışı bırak**'ı seçin. Varolan bir iş akışını etkin hale getirmek için iş akışını seçin ve sonra **Etkin yap**'ı seçin.

---
title: (ER) Yapılandırmaları RCS'den içe aktarma
description: Bu konu, bir kullanıcının bir ER yapılandırmasının yeni sürümünü RCS'den nasıl içe aktarılacağı hakkında bilgi sağlar.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c458cf815837fb7e4688c4c0443b7962cac403a5
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/04/2019
ms.locfileid: "1727018"
---
# <a name="er-import-configurations-from-rcs"></a>(ER) Yapılandırmaları RCS'den içe aktarma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, yeni bir Elektronik Raporlama (ER) sürümü oluşturabilir. ve bunu Microsoft Regulatory Configuration Services (RCS)'den içe aktarabilir. Bu örnekte, bir RCS örneğinde yapılandırılan ER yapılandırmasının sürümünü seçersiniz ve bunu örnek şirket, Litw, Inc. için geçerli Finance and Operations örneğine içe aktarmanız gerekir. Bu adımlar herhangi bir şirket içinde gerçekleştirilerek, ER yapılandırmaları şirketler arasında paylaşıldığından gerçekleştirilebilir. Bu adımları tamamlamak için öncelikle [Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md). adımlarını tamamlamanız gerekir. Bu adımları tamamlamak için **Tamamlanmış** veya **Paylaşılan** durumda en az bir er yapılandırması içeren bir RCS örneğine de erişiminiz olmalıdır.

1. **Organizasyon yönetimi** > **Çalışma alanları** > **Elektronik raporlama**'ya gidin. 
2. Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve **Etkin** olarak işaretlemiş olduğundan emin olun. Bu konudaki yapılandırma sağlayıcısını göremiyorsanız [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md) prosedüründeki adımları tamamlayın. 
3. Şirketiniz için sağlanmış bir RCS ortamınız yoksa **Regulatory services - Yapılandırma** dış bağlantısını tıklatın ve RCS ortamını sağlamak için yönergeleri izleyin. 
4. **Elektronik raporlama parametreleri**'ne tıklayın. 
5. **RCS** sekmesine tıklayın. 
6. Şirketiniz için RCS ortamı zaten sağlanmış ise ona erişmek için sayfa URL'lerinde sunulanları kullanın. 
7. Sayfayı kapatın. 

## <a name="register-a-new-er-repository"></a>Yeni bir ER havuzu kaydedin. 
1. Listede, seçili satırı işaretleyin. 
2. Litware, Inc. sağlayıcısı seçin. 
3. Depolar'a tıklayın. 
4. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın. 
5. Yapılandırma havuz türü alanında RCS'yi girin. 
6. Havuz oluştur'a tıklayın. 
7. RCS ortamı görüntüleme adı alanına bir değer girin veya seçin. 
8. İstenilen RCS örneğini seçin. Bunlardan birkaç tane olabilir. 
9. Tamam'a tıklayın. 

## <a name="import-er-configurations-from-rcs-based-repository"></a>RCS tabanlı depodan ER yapılandırmalarını içe aktarın
1. **Filtreleri göster**'e tıklayın. 
2. **Name** alanındaki "RCS" değeri filtresine **ile başlar** filtre işlecini kullanarak bir filtre girin. 
3. Seçili havuzu açtığınızda, **Regulatory Configuration Services'a bağlan** sayfasında,**Regulatory Configuration Services'e bağlanmak için buraya tıklayın** bağlantısına tıklayın. 
4. **Aç**'a tıklayın. 
5. **Kapat**'a tıklayın. 
6. İstenen ER yapılandırması sürümünü seçin ve bunu geçerli Finance and Operations örneğine getirmek için **İçe aktar**'a tıklayın.


---
title: (ER) Yapılandırmaları RCS'den içe aktarma
description: Bu makalede, bir kullanıcının bir ER yapılandırmasının yeni sürümünü RCS'den nasıl içe aktaracağı hakkında bilgiler sağlanmaktadır.
author: kfend
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ''
ms.openlocfilehash: 55e7a3ae23b708acecb5ac219b885f43b4c7aa0a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290049"
---
# <a name="er-import-configurations-from-rcs"></a>(ER) Yapılandırmaları RCS'den içe aktarma

[!include [banner](../../includes/banner.md)]

Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, yeni bir Elektronik Raporlama (ER) sürümü oluşturabilir. ve bunu Microsoft Regulatory Configuration Services (RCS)'den içe aktarabilir. Bu örnekte, bir RCS örneğinde yapılandırılan ER yapılandırmasının sürümünü seçersiniz ve bunu örnek şirket, Litw, Inc. için geçerli örneğe aktarmanız gerekir. Bu adımlar herhangi bir şirket içinde gerçekleştirilerek, ER yapılandırmaları şirketler arasında paylaşıldığından gerçekleştirilebilir. Bu adımları tamamlamak için öncelikle [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md) makalesindeki adımları tamamlamanız gerekir. Bu adımları tamamlamak için **Tamamlanmış** veya **Paylaşılan** durumda en az bir er yapılandırması içeren bir RCS örneğine de erişiminiz olmalıdır.

1. **Organizasyon yönetimi** > **Çalışma alanları** > **Elektronik raporlama**'ya gidin. 
2. Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve **Etkin** olarak işaretlemiş olduğundan emin olun. Bu yapılandırma sağlayıcısını göremiyorsanız [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md) makalesindeki adımları tamamlayın. 
3. Şirketiniz için sağlanmış bir RCS ortamınız yoksa **Regulatory services - Yapılandırma** dış bağlantısını seçin ve RCS ortamını sağlamak için yönergeleri izleyin. 
4. **Elektronik raporlama parametreleri**'ni seçin. 
5. **RCS** sekmesini seçin. 
6. Şirketiniz için RCS ortamı zaten sağlanmış ise ona erişmek için sayfa URL'lerinde sunulanları kullanın. 
7. Sayfayı kapatın. 

## <a name="register-a-new-er-repository"></a>Yeni bir ER havuzu kaydedin. 
1. Listede, seçili satırı işaretleyin. 
2. Litware, Inc. sağlayıcısı seçin. 
3. Depolar'ı seçin. 
4. Açılır iletişim kutusunu açmak için Ekle öğesini seçin. 
5. Yapılandırma havuz türü alanında RCS'yi girin. 
6. Depo oluştur'u seçin. 
7. RCS ortamı görüntüleme adı alanına bir değer girin veya seçin. 
8. İstenilen RCS örneğini seçin. Bunlardan birkaç tanesine sahip olabilirsiniz. 
9. Tamam'ı seçin. 

## <a name="import-er-configurations-from-rcs-based-repository"></a>RCS tabanlı depodan ER yapılandırmalarını içeri aktarma
1. **Filtreleri göster**'i seçin. 
2. **Name** alanındaki "RCS" değeri filtresine **ile başlar** filtre işlecini kullanarak bir filtre girin. 
3. Seçili depoyu açtığınızda, **Regulatory Configuration Services'a bağlan** sayfasında,**Regulatory Configuration Services'a bağlanmak için burayı seçin** bağlantısını seçin. 
4. **Aç**'ı seçin. 
5. **Kapat**'ı seçin. 
6. İstenen ER yapılandırması sürümünü seçin ve bunu geçerli kuruluma getirmek için **İçeri aktar**'ı seçin.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

---
title: RCS genel deposunda yapılandırmaları sona erdirme
description: Bu makalede, RCS genel deposundaki yapılandırmalara nasıl son verileceği açıklanmaktadır.
author: gionoder
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace
ms.openlocfilehash: b0605f56058e3c93ea088ee8386ba26c4ce2b65a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272351"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a>RCS genel deposunda yapılandırmaları sona erdirme

[!include [banner](../includes/banner.md)]

Bu makalede, RCS genel deposundaki yapılandırmaya nasıl son verileceği açıklanmaktadır. Daha önce, gerekli olmayan yapılandırmalar yalnızca silinebiliyordu. Ancak şimdi, sunulan bir yapılandırmayı RCS genel deposunda **Sona erdirildi** olarak işaretleyebilirsiniz. Bu işlevle şunları da yapabilirsiniz: 
 
 - Bir yapılandırmanın sona erdirilmesi planlanıyorsa ön bildirim sağlama.
 - Eskisiyle değiştirilen yapılandırmayla ilgili ayrıntılar ekleme.
 - Kullanıcıya, belirli bir yapılandırmanın ne zaman sona erdirileceğiyle ilgili bilgi vermek için bir **Son desteklenme tarihi** ayarlayın.

Bir yapılandırma sürümünü sona erdirdiğinizde aşağıdaki isteğe bağlı bilgileri belirtebilirsiniz:

  - **Yedek yapılandırma**
  - **Yedek yapılandırma sürümü**
  - **Serbest metin notu**: Belge bağlantıları veya referanslar sağlamak için bu alanı kullanın
  - **Son desteklenme tarihi**: Bu alan, geçerli yapılandırmanın/sürümün destekleneceği son tarihi sağlar. Bu tarih el ile güncelleştirilmelidir.
  
Yapılandırmayı sona erdirmek için aşağıdaki adımları tamamlayın. 

1. **Tüm sürümleri** **Evet**'e ayarlayarak aynı ayarlara sahip tüm sürümleri ya da tek bir sürümü tek bir işlemle sona erdirmek istediğinizi seçin. 
2. **Sona erdir** parametresini **Evet** olarak ayarlayın.
3. Yapılandırmaları sona erdirmek için **Tamam**'ı seçin. Değişiklikleri kaydettiğinizde, **Sona erdirilen tarih** alanı doldurulacaktır.

![Yapılandırmayı sona erdirme bilgileri.](media/Discontinue-details-2.png)
  
Yapılandırmayı istediğiniz zaman **paylaşılan** olarak geri döndürebilir veya sona erdirme bilgilerini ayarlayabilirsiniz. Bir yapılandırmayı paylaştırırsanız, ileride yapılacak sona erdirme için planlarınızı belirtecek şekilde **desteklendiği son tarih** ve sona erdirmeyle ilgili tüm diğer bilgileri belirtin.

Yapılandırmanın sona erdirilmesinden önce, planlı bir sona erdirme hakkında bilgi paylaşmak istiyorsanız, kullanıcı yedek yapılandırmayla ilgili tüm alanları önceden doldurabilir ancak **Sona erdir** parametresini **Hayır** olarak ayarlar.

> [!NOTE]
> Sona erdirme, yapılandırmayla yapılan işlemleri sınırlamaz. Yapılandırmaları almaya, çalıştırmaya veya türetmeye devam edebilirsiniz; bu alanlar bilgi amaçlıdır.

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a>Finance, 10.0.14 sürümünden itibaren bu bilgilerin görüntülenmesini destekler

Dynamics 365 Finance, 10.0.14 sürümünden itibaren son verme bilgilerinin görüntülenmesini destekler. **Genel depo** sayfasında, sona erdirmeyle ilgili güncel bilgileri görüntüleyebilirsiniz. Varsayılan olarak, sona erdirilen yapılandırmalar filtrelenir.
  
**İçe aktarılan yapılandırmalar** (ERSolutionTable) sayfası, içe aktarıldıklarında zaten sona erdirilmiş olan yapılandırmaları gösterir. İçe aktarma işleminden sonra sona erdirilen yapılandırmalar için **içe aktarma yapılandırmaları güncelleştirmeleri** işi çalıştırılarak sona erdirme bilgileri eşitlenebilir.



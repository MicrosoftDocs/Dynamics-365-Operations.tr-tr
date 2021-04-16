---
title: ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 1 - Biçim oluşturma)
description: Bu konuda, önceden oluşturulmuş metin çıktısının verilerine dayalı olarak sayma ve toplama işlemi yapmak üzere Elektronik raporlama biçiminin nasıl yapılandırılacağı açıklanmaktadır. (1. Bölüm)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f1db144b2bfafa72abeaa92c6b21de717e4acbf
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749057"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a>ER Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma (Bölüm 1 - Biçim oluşturma)

[!include [banner](../../includes/banner.md)]

Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) biçimini zaten oluşturulmuş metin çıktısının verilerine bağlı olarak nasıl sayacağını ve toplayacağını açıklar. Bu adımlar tüm şirketlerde gerçekleştirilebilir.

Bu adımları tamamlamak için öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.

Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Microsoft tarafından sağlanan yapılandırma listesine erişim alma
1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
    * "Litware, Inc." emin olun sağlayıcısının kullanılabilir ve etkin olarak işaretlendiğinden emin olun.  
2. "Litware, Inc." seçin. sağlayıcısını seçin.
3. Depolar'a tıklayın.
    * "Operasyon kaynakları" türünün bir havuzu zaten varsa geçerli alt görevin kalan adımlarını atlayın.  
4. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
5. Yapılandırma havuzu türü alanına "Operasyon kaynakları" yazın.
6. Havuz oluştur'a tıklayın.
7. Tamam'a tıklayın.

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a>Microsoft tarafından sağlanan Intrastat yapılandırmalarını alma
1. Aç'a tıklayın.
2. Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini seçin.
3. İçe aktar'ı tıklatın.
    * Seçili yapılandırmanın 1.1 sürümü için İthalat'a tıklayın.  
4. Evet'i tıklatın.
5. Sayfayı kapatın.
6. Sayfayı kapatın.
7. Raporlama konfigürasyonları'na tıklayın.
8. Ağaçta, "Intrastat modeli" öğesini genişletin.
9. Ağaçta, "Intrastat modeli\Intrastat (DE)" öğesini seçin.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
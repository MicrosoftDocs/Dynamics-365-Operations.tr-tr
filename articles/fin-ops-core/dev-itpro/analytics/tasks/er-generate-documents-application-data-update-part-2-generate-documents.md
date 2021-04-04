---
title: Uygulama verileri içeren belgeler oluşturmak için yapılandırmalar tasarlama
description: Bu konuda, elektronik belge oluşturmak için Elektronik raporlama (ER) yapılandırmalarının nasıl tasarlanacağı açıklanmaktadır. (1. Bölüm - Yapılandırma içe aktarma).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 217eca9bd1502d4327857720fb2d32a3ec3508ef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563186"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a>Uygulama verileri içeren belgeler oluşturmak için yapılandırmalar tasarlama

[!include [banner](../../includes/banner.md)]

Bu yordamdaki adımları tamamlamak için ilk önce ER Uygulama veri güncelleştirmesi ile belgeler oluştur (Bölüm 1: Yapılandırmaları içe aktar) yordamını tamamlamalısınız.



Bu yordamdaki adımlar bir Elektronik raporlama (ER) yapılandırmasının, bir elektronik belge oluşturmak için nasıl kullanılacağını açıklar. Bu yordamda, örnek şirket Litware Inc. için oluşturulmuş ER içe aktarılan biçim yapılandırmasını çalıştırırsınız.



Bu yordam, sistem yöneticisi veya elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar için oluşturulmuştur. Bu adımlar DEMF veri kümesi kullanılarak tamamlanabilir. 



Başlamadan önce, DEMF şirketi için ülke bağlamını DEU'dan (Almanya) BEL'e (Belçika) çevirin. Tüzel varlık DEMF'in birincil adresindeki ülke kodunu güncelleştirmek için Kuruluş yönetimi > Kuruluşlar > Tüzel kişilikler seçeneğini tıklatın. Uygulamanızı yeniden başlatın.


## <a name="run-imported-er-format"></a>İçe aktarılan ER biçimini çalıştır
1. Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.
2. Ağaçta, 'Intrastat (model)' öğesini genişletin.
3. Ağaçta, 'Intrastat (model)\Intrastat (biçim)' öğesini seçin.
4. Çalıştır öğesine tıklayın.
    * Intrstat raporunu oluşturmak için ER biçim yapılandırmasının taslak sürümünü çalıştırın.  
5. Dosya adı gir alanında, 'intrastat.xml' yazın.
    * Dosyanın adını belirtin.  
6. Tamam'a tıklayın.
    * Oluşturulan XML dosyasını gözden geçirin.  
7. Sayfayı kapatın.
8. Vergi > Bildirimler > Dış ticaret > Intrastat öğesine gidin.
    * Oluşturulan elektronik belgeye dahil edilen Intrastat hareketlerini görüntülemek için bu formu açın.  
9. Intrastat arşivini tıklat.
    * Çalıştırılan ER biçimi uygulama veri güncelleştirmesi için herhangi bir ayar içermediğinden, tamamlanan Intrasta raporunun ayrıntıları arşivlenmez.  
10. Sayfayı kapatın.
11. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
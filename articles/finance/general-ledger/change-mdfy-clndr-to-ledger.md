---
title: Genel muhasebe takvimini değiştirme veya yeniden atama
description: Bu konuda, genel muhasebeye atanmış olan takvimin nasıl değiştirileceği ve yeni bir takvimin genel muhasebeye nasıl atanacağı açıklanmaktadır.
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 16000243bc8aa76b04ac56dfb8bfbab7cd644eb3120cc68493ff066598f6cf85
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758089"
---
# <a name="change-or-reassign-a-ledger-calendar"></a>Genel muhasebe takvimini değiştirme veya yeniden atama

[!include [banner](../includes/banner.md)]

Bu konuda, genel muhasebeye atanmış olan takvimin nasıl değiştirileceği ve yeni bir takvimin genel muhasebeye nasıl atanacağı açıklanmaktadır.

## <a name="issue"></a>Sorun

Zaman zaman şirketlerin genel muhasebeye atanan mevcut takvimi değiştirmesi veya yeni bir takvim ataması gerekir.

## <a name="resolution"></a>Çözüm

Genel muhasebe takvimini değiştirmeye veya yeniden atamaya yönelik iki senaryo vardır. İlk senaryo, önceden genel muhasebeye atanmış mevcut bir takvimi değiştirmeyi kapsar. İkinci senaryo yeni bir takvim oluşturmayı ve bunu genel muhasebeye atamayı kapsar. Her iki değişiklik de işlemler genel muhasebeye nakledildikten sonra bile herhangi bir zamanda yapılabilir.

### <a name="change-an-existing-fiscal-calendar"></a>Mevcut mali takvimi değiştirme

Genel muhasebenize atanan mevcut bir takvimi değiştirmek için **Genel muhasebe \>Genel muhasebe kurulumu \> Muhasebe**'ye gidin ve **Genel muhasebe takvimleri** sayfasını açmak için mali takvimin bağlantısını seçin.

Takvimde yapılabilecek değişikliklerle ilgili sınırlar vardır. Örneğin, bir yıldaki *dönemlerin* başlangıç ve bitiş tarihlerini değiştirebilirsiniz ancak takvimdeki bir *yılın* başlangıç ve bitiş tarihlerini değiştiremezsiniz.

Bir yıldaki dönemleri değiştirmek için uygun takvimi ve yılı seçin. İlk olarak, mevcut çalışma dönemlerinin bir kısmını veya tamamını silmek için **Dönemi sil** düğmesini kullanın. İlki dışında tüm çalışma dönemleri silinebilir. Ardından, sonraki dönem için uygun bir başlangıç tarihi girerek kalan dönemi veya dönemleri yeni dönemlere bölmek için **Dönemi böl** düğmesini kullanın.

Takvimdeki dönemleri değiştirdikten sonra takvimin atandığı her tüzel kişilikte (şirkette) **Genel muhasebe dönemlerini yeniden hesapla** işlemini çalıştırmanız gerekir. Hiçbir uyarı iletisi size bu adımı tamamlamanızı hatırlatmasa da Genel muhasebede deftere nakledilmiş işlemlere atanan dönemi güncelleştirmek için yeniden hesaplama işlemi gerekir. Yeniden hesaplama işlemini çalıştırmak için her şirkette **Genel muhasebe kurulumu** sayfasında **Genel muhasebe dönemlerini yeniden hesapla**'yı seçin.

Yeniden hesaplama işlemi çalıştırılmazsa bir mizandaki veya mali tablolardaki işlem bakiyeleri dönemlere yanlış şekilde eklenebilir. Bu durumda, yeniden hesaplama işlemini çalıştırarak istediğiniz zaman bakiyeleri düzeltebilirsiniz.

### <a name="assign-a-new-fiscal-calendar"></a>Yeni bir mali takvim atama

Yeni bir mali takvim atamak için **Genel muhasebe \> Genel muhasebe kurulumu \> Muhasebe**'ye gidin ve **Düzenle**'yi seçerek **Genel muhasebe** sayfasını düzenleme moduna getirin. Ardından **Mali takvim** alanında, yeni bir mali takvim seçin.

Genel muhasebe için mali takvimi değiştirdikten sonra **Genel muhasebe dönemlerini yeniden hesapla** işlemini çalıştırmanız gerekir. Genel muhasebeye yeni bir mali takvim atadığınızda bir ileti size bu adımı tamamlamanız gerektiğini anımsatır. İleti, yeniden hesaplama işleminin isteğe bağlı olduğunu belirtiyor gibi görünse de böyle bir durum yoktur. Genel muhasebede deftere nakledilmiş işlemlere atanan dönemi güncelleştirmek için gereklidir. Yeniden hesaplama işlemini çalıştırmak için **Genel muhasebe kurulumu** sayfasında **Genel muhasebe dönemlerini yeniden hesapla**'yı seçin.

Yeniden hesaplama işlemi çalıştırılmazsa bir mizandaki veya mali tablolardaki işlem bakiyeleri dönemlere yanlış şekilde eklenebilir. Bu durumda, yeniden hesaplama işlemini çalıştırarak istediğiniz zaman bakiyeleri düzeltebilirsiniz.

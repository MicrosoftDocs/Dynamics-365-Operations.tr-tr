---
title: Uygulama verileri içeren belgeler oluşturma
description: Bu yordamdaki adımları tamamlamak için ilk önce "ER Uygulama veri güncelleştirmesi ile belgeler oluştur (Bölüm 4 - Biçimi değiştir)" yordamını tamamlamalısınız.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a2643c85e64373e30aab16be686c50cd224490fe
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684487"
---
# <a name="generate-documents-that-have-application-data"></a>Uygulama verileri içeren belgeler oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordamdaki adımları tamamlamak için ilk önce "ER Uygulama veri güncelleştirmesi ile belgeler oluştur (Bölüm 4 - Biçimi değiştir)" yordamını tamamlamalısınız.



Bu yordamdaki adımlar bir Elektronik raporlama (ER) yapılandırmasının, bir elektronik belge oluşturmak ve uygulama verisini güncelleştirmek için nasıl kullanılacağını açıklar. Bu yordamda, Intrastat raporunu oluşturmak ve raporlama işleminin arşivleme ayrıntıları için uygulama verisini güncelleştirmek amacıyla ER biçim yapılandırmasını çalıştırırsınız.



Bu yordam, sistem yöneticisi veya elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar için oluşturulmuştur. Bu adımlar DEMF veri kümesi kullanılarak tamamlanabilir. Başlamadan önce DEMF şirketin ülke bağlamının BEL (Belçika) olduğunu doğrulayın.


## <a name="set-up-foreign-trade-parameters"></a>Dış ticaret parametreleri ayarla
1. Vergi > Kurulum > Dış Ticaret > Dış Ticaret parametreleri'ne gidin.
2. Numara serileri sekmesini tıklatın.

    Instrastat raporlama işlemlerinin arşivleme ayrıntıları, oluşturduğumuz her arşivin kaydını tanımlamamız gerekir. Bunun için özel bir numara serisinin yapılandırılmış olması gerekir.  

3. 'Intrastat arşiv kodu' referansını seçin.
4. Numara serisi kodu alanında, bir değer girin.

    'Numara sırası kodu' alanında, 'Fore_2' değerini girin ya da seçin.  

5. Numara serisi kodunu ResolveChanges.
6. Kaydet'i tıklatın.
7. Sayfayı kapatın.

## <a name="run-modified-er-format"></a>Değiştirilen ER biçimini çalıştırın
1. Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.
2. Ağaçta, 'Intrastat (model)' öğesini genişletin.
3. Ağaçta, 'Intrastat (model)\Intrastat (biçim)' öğesini seçin.
4. Çalıştır'a tıklayın.
5. Dosya adı gir alanında, 'intrastat2.xml' yazın.
6. Tamam'a tıklayın.

## <a name="review-er-format-executions-results"></a>ER biçimi yürütmesine ait sonuçları gözden geçirin
Oluşturulan XML dosyasını gözden geçirin.  
1. Sayfayı kapatın.
2. Vergi > Bildirimler > Dış ticaret > Intrastat öğesine gidin.

    Oluşturulan elektronik belgeye dahil edilmiş olan Intrastat hareketlerini görüntülemek için bunları içeren formu açın.  

3. Intrastat arşivini tıklat.

    Çalıştırılan ER biçimi uygulama veri güncelleştirmesi için herhangi bir ayarı şimdi içerdiğinden, tamamlanan Intrastat raporlamasının ayrıntıları arşivlenmiştir. Bu formda oluşturulan arşivin başlık kaydını görebilirsiniz.  

4. Ayrıntılar seçeneğini tıklatın.

    Bu formda oluşturulan arşivin ayrıntılarını görebilirsiniz.  

5. Sayfayı kapatın.
6. Sayfayı kapatın.
7. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
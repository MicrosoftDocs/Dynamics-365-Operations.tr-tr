---
title: Katıştırılmış resimlere sahip Office biçiminde raporlar oluşturma
description: Bu makalede, Excel ve Word'de eklenmiş resimler içeren elektronik belgeler oluşturmak için Elektronik raporlama (ER) yapılandırmalarının nasıl tasarlanacağı gösterilmektedir.
author: NickSelin
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e728c6e55eca7bcb541a019d1fc9af00b5ad2081
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855630"
---
# <a name="generate-reports-in-office-format-that-have-embedded-images"></a>Katıştırılmış resimlere sahip Office biçiminde raporlar oluşturma

[!include [banner](../../includes/banner.md)]

Aşağıdaki adımlar 'Sistem yöneticisi' veya 'Elektronik raporlama geliştiricisi' rolündeki bir kullanıcının, MS office biçimlerinde (Excel ve Word) katıştırılmış resimler içeren elektronik belgeler oluşturmak için Elektronik raporlama (ER) yapılandırmalarını nasıl tasarlayabileceklerini açıklar.

Bu örnekte, 'Litware, Inc.' örnek şirketi için oluşturulmuş ER yapılandırmalarını kullanacaksınız.  Bu adımları tamamlamak için öncelikle "ER Katıştırılmış resimler barındıran MS Office biçimlerinde raporlar hazırla (Bölüm 2: Yapılandırmaları gözden geçir)" görev kılavuzundaki adımları tamamlayın. Bu adımlar 'USMF' şirketinde gerçekleştirilebilir.


## <a name="run-format-with-initial-model-mapping"></a>Biçimi ilk model eşleme ile çalıştırın
1. Nakit ve banka yönetimi > Banka hesapları > Banka hesapları öğesine gidin.
2. Banka hesabı alanında "USMF OPER" değeriyle filtre uygulamak için Hızlı Filtre'yi kullanın.
3. Eylem Bölmesinde Kurulum'a tıklayın.
4. Denetle'yi tıklatın.
5. Testi yazdır'a tıklayın.
    * Test amacıyla biçimi çalıştırın.  
6. Ciro edilebilir çek biçimi alanında Evet'i işaretleyin.
7. Tamam'a tıklayın.
    * Oluşturulan sonucu inceleyin. Raporda hem şirket logosu hem de yetkili kişinin imzası görünür. İmza resmi seçilen banka hesabıyla ilişkilendirilmiş çek düzeni kaydının "Kapsayıcı" veri türü alanından alınır.  
8. Kopyalar bölümünü genişletin.
9. Düzenle öğesine tıklayın.
10. Filigran alanında 'Filigranı Geçersiz olarak yazdır' girin.
    * Bir Excel şekli öğesinde belge oluştururken filigranı göstermek için filigran biçim ayarını değiştirin.  
11. Testi yazdır'a tıklayın.
12. Tamam'a tıklayın.
    * Oluşturulan sonucu inceleyin. Filigran, oluşturulan raporda seçim seçeneğine uygun olarak gösterilir.  
13. Sayfayı kapatın.
14. Eylem Bölmesinde, Ödemeleri yönet'e tıklayın.
15. Çekler'i tıklatın.
16. Filtreleri göster'e tıklayın.
17. Aşağıdaki filtreleri uygulayın: "Çek numarası" alanında "şunlardan biri" filtre işlecini kullanarak "381", "385", "389" filtre değerini girin.
18. Listede, tüm satırları işaretleyin.
19. Çek kopyasını yazdır'ı tıklatın.
    * Seçilen çekleri yeniden yazdırmak için biçimi çalıştırın.  
    * Oluşturulan sonucu inceleyin. Seçili çekler yeniden yazdırılır. Şirket logosu ve etiketleri yazdırılmaz çünkü önceden yazdırılmış formda mevcutturlar.  

## <a name="modify-the-mapping-of-the-imported-data-model"></a>İçe aktarılan veri modelinin eşlemesini değiştirin
1. Sayfayı kapatın.
2. Sayfayı kapatın.
3. Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.
4. Ağaçta, 'Çekler için model' öğesini seçin.
5. Tasarımcı'yı tıklatın.
6. Modeli veri kaynağına eşle'yi tıklayın.
7. Tasarımcı'ya tıklayın.
    * Seçilen banka hesabıyla ilişkilendirilmiş çek düzeni kaydına eklenmiş olan dosyadan imza resmi almak için veri modelinin imza öğesi bağlamasını değiştireceğiz.  
8. Ayrıntıları göster'i kapatın.
9. Ağaçta, 'düzen' metnini genişletin.
10. Ağaçta, 'düzen\imza' öğesini genişletin.
11. Ağaçta 'düzen\imza\resim = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp' seçeneğini belirleyin.
12. Ağaçta, 'chequesaccount' öğesini genişletin veya daraltın.
13. Ağaç altından 'chequesaccount\<İlişkiler' seçeneğini genişletin.
14. Ağaçta 'chequesaccount\<İlişkiler\BankChequeLayout' seçeneğini genişletin.
15. Ağaçta 'chequesaccount\<İlişkiler\BankChequeLayout\<İlişkiler' seçeneğini genişletin.
16. Ağaçta 'chequesaccount\<İlişkiler\BankChequeLayout\<İlişkiler\<Belgeler' seçeneğini genişletin.
17. Ağaçta 'chequesaccount\<İlişkiler\BankChequeLayout\<İlişkiler\Belgeler\<getFileContentAsContainer()' seçeneğini belirleyin.
18. Bağla'ya tıklayın.
19. Kaydet'e tıklayın.
20. Sayfayı kapatın.
21. Sayfayı kapatın.
22. Sayfayı kapatın.
23. Sayfayı kapatın.

## <a name="run-format-using-the-adjusted-model-mapping"></a>Ayarlanan model eşlemesini kullanarak biçimi çalıştırın
1. Nakit ve banka yönetimi > Banka hesapları > Banka hesapları öğesine gidin.
2. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, Banka hesabı alanında 'USMF OPER' değerini girerek filtreleme yapın.
3. Eylem Bölmesinde Kurulum'a tıklayın.
4. Denetle'yi tıklatın.
5. Testi yazdır'a tıklayın.
6. Tamam'a tıklayın.
    * Oluşturulan sonucu inceleyin. Belge Yönetimi ekinden alınan resim, yetkili kişinin imzası olarak gösterilir.  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a>MS Word belgesini içe aktarılan biçimde bir şablon olarak kullanın
1. Sayfayı kapatın.
2. Sayfayı kapatın.
3. Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.
4. Ağaçta, 'Çekler için model' öğesini genişletin.
5. Ağaçta 'Çekler için model\Çek yazdırma biçimi' seçin.
6. Tasarımcı'yı tıklatın.
7. Ekler'e tıklayın.
8. Sil'i tıklatın.
9. Evet'i tıklatın.
10. Yeni'ye tıklayın.
11. Dosya'ya tıklayın.
    * Gözat'ı tıklatın ve önceden indirilen 'Çek şablonu Word.docx' dosyasını seçin.  
12. Sayfayı kapatın.
13. Şablon alanına bir değer girin veya seçin.
14. Kaydet'e tıklayın.
15. Sayfayı kapatın.
16. Düzenle öğesine tıklayın.
17. Taslak Çalıştır alanında Evet'e tıklayın.
18. Sayfayı kapatın.
19. Nakit ve banka yönetimi > Banka hesapları > Banka hesapları öğesine gidin.
20. Banka hesabı alanında "USMF OPER" değeriyle filtre uygulamak için Hızlı Filtre'yi kullanın.
21. Denetle'yi tıklatın.
22. Testi yazdır'a tıklayın.
23. Tamam'a tıklayın.
    * Oluşturulan sonucu inceleyin. Çıktı; şirket logosunu, yetkili kişinin imzasını ve seçili filigran metinini gösteren ekli resimler içeren bir Word belgesi olarak oluştulur.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
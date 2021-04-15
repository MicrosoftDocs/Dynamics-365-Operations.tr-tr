---
title: ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 5 - Biçimi değiştirme ve çalıştırma)
description: Bu konuda, ER çıktılarında Belge Yönetimi dosyaları (ekler) kullanmak üzere Elektronik raporlama (ER) biçiminin nasıl yapılandırılacağı açıklanmaktadır. (5. Bölüm)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f954b76a09bf7c5edd4c608d400318fbd9386778
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749105"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a>ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 5 - Biçimi değiştirme ve çalıştırma)

[!include [banner](../../includes/banner.md)]

Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar. Bu adımlar DEMF şirketinde gerçekleştirilebilir.

Bu adımları tamamlamak için öncelikle "ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 4: Biçimi çalıştırma)" yordamındaki adımları tamamlamalısınız.

Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a>Ekleri oluşturulan iletilere ikili biçimde doldurmak için biçimi değiştirin
1. Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.
2. Ağaçta "Müşteri fatura modeli" seçeneğini genişletin.
3. Ağaçta, "Müşteri faturası modeli\Müşteri faturası modeli (özel)"i genişletin.
4. Ağaçta, "Müşteri faturası modeli\Müşteri faturası modeli (özel)\Elektronik fatura örnek iletisi"ni seçin.
5. Tasarımcı'yı tıklatın.
    * UNICODE kodlaması kullanarak XML dosyası olarak oluşturulan çıktıda fatura iletisini doldurun.  
6. İletişim kutusunu açmak için Kök ekle'yi tıklatın.
7. Ağaçta seçin 'Common\File'.
8. Ad alanında, "Xml iletisi" yazın.
    * Xml iletisi  
9. Kodlama alanına 'UTF-8' yazın.
    * UTF-8  
10. Tamam'a tıklayın.
    * Oluşturulan çıktıyı sıkıştırılmış bir dosya olarak yapılandırın.  
11. İletişim kutusunu açmak için Kök ekle'yi tıklatın.
12. Ağaçta, "Ortak\Klasör"ü seçin.
13. Ad alanına "Zip çıktısı" yazın.
    * Zip çıktısı  
14. Tamam'a tıklayın.
15. Ağaçta, "Zip çıktısı" öğesini seçin.
    * Oluşturulan sıkıştırılmış dosyaya ekleri orijinal adları ve uzantıları ile dosyalar olarak ekleyin.  
16. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
17. Ağaçta seçin 'Common\File'.
18. Ad alanına "Ekli dosya" yazın.
    * Ekli dosya  
19. Tamam'a tıklayın.
20. Ağaçta, "Zip çıktısı\Ekli dosya" öğesini seçin.
21. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
22. Ağaçta, "Metin\Base64" seçeneğini işaretleyin.
23. Tamam'a tıklayın.

## <a name="map-new-format-elements-to-data-model"></a>Veri modeline yeni biçim öğeleri eşleme
1. Eşleme sekmesini tıklatın.
2. Ağaçta, 'model'i genişletin.
3. Ağaçta, "model\Fatura ekleri" seçeneğini genişletin.
4. Ağaçta, "Zip çıktısı\Ekli dosya\Base64" öğesini seçin.
5. Ağaçta, "model\Fatura ekleri\Dosya içeriği" seçeneğini işaretleyin.
6. Bağla'ya tıklayın.
7. Ağaçta, "Zip çıktısı\Ekli dosya" öğesini seçin.
8. Dosya adını düzenle'ye tıklayın.
9. Ağaçta, 'model'i genişletin.
10. Ağaçta, "model\Fatura ekleri" seçeneğini genişletin.
11. Ağaçta "model\Fatura ekleri\Dosya adı" seçeneğini işaretleyin.
12. Veri kaynağı ekle'ye tıklayın.
13. Kaydet'e tıklayın.
14. Sayfayı kapatın.
15. Ağaçta, "model\Fatura ekleri" seçeneğini işaretleyin.
16. Bağla'ya tıklayın.
17. Kaydet'e tıklayın.
18. Sayfayı kapatın.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Seçili fatura için tasarlanan raporu çalıştırın
1. Çalıştır öğesine tıklayın.
2. Eklenecek kayıtlar () bölümünü genişletin.
3. Filtre'ye tıklayın.
4. Müşteri fatura günlüğü satırını ve Satış siparişi alanını seçin.
5. Ölçütler alanında "Satış siparişi" alanına 000148 no.lu sipariş numarasını yazın.
    * 000148  
6. Tamam'a tıklayın.
7. Tamam'a tıklayın.
    * Ortaya çıkan sonucu inceleyin. XML biçimindeki fatura iletisine ek olarak her bir ek için tek bir dosya oluşturulduğunu unutmayın. Ek dosyaları ikili biçimde sıkıştırılmış çıktı ile doldurulur.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
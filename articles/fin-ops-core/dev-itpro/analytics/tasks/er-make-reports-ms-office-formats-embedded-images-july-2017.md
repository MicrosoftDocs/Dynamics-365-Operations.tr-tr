---
title: Katıştırılmış resimlere sahip Office biçiminde rapor oluşturmak için yapılandırmalar tasarlama
description: Bu konuda, katıştırılmış resimler içeren Excel ve Word biçimlerinde elektronik belgeler oluşturan yapılandırmaların nasıl tasarlanacağı açıklanmaktadır.
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
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
ms.openlocfilehash: b60ed6b07851c44ceb4b8f313bc65f04b802e646
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093682"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>Katıştırılmış resimlere sahip Office biçiminde rapor oluşturmak için yapılandırmalar tasarlama

[!include [banner](../../includes/banner.md)]

Bu yordamdaki adımları tamamlamak için öncelikle "ER Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamını tamamlayın. Bu yordam, katıştırılmış resimler içeren Microsoft Excel veya Word belgeleri oluşturmak üzere Elektronik raporlama (ER) yapılandırmalarının nasıl tasarlanacağını gösterir. Bu yordamda, Litware, Inc. adlı örnek şirket için gerekli ER yapılandırmalarını oluşturacaksınız. Bu adımlar USMF veri kümesi kullanılarak tamamlanabilir. Bu yordam, sistem yöneticisi veya elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar için oluşturulmuştur. Başlamadan önce [ER kullanılarak oluşturduğunuz iş belgelerine görüntü ve şekil katıştırma](../electronic-reporting-embed-images-shapes.md) Yardım konusunda listelenen dosyaları indirin ve kaydedin. Bu dosyalar şunlardır: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.

## <a name="verify-prerequisites"></a>Ön koşulları doğrulama  
 1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.  
 2. Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve etkin olarak işaretlemiş olduğundan emin olun. Bu yapılandırma sağlayıcısını göremiyorsanız "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlayın.   
 3. Raporlama konfigürasyonları'na tıklayın.  
 
## <a name="add-a-new-er-model-configuration"></a>Yeni bir ER model yapılandırması ekleme  
 1. Yeni bir model oluşturmak yerine, daha önce kaydetmiş olduğunuz ER modeli yapılandırma dosyasını (Model for cheques.xml) yükleyebilirsiniz. Bu dosya ödeme çekleri için örnek veri modelini ve veri modelinin Dynamics 365 for Operations uygulamasındaki veri bileşenleriyle eşleşmesini içerir.   
 2. Sürümler hızlı sekmesinde, Değiştir'e tıklayın.   
 3. XML dosyasından yükle'ye tıklayın.  
 4. Gözat'a tıklayın ve sonra Model for cheques.xml dosyasını seçin.   
 5. Tamam'a tıklayın.  
 6. Yüklenen model resimler içeren Excel ve Word biçiminde belgeler oluşturmak için veri kaynağı olarak kullanılır.  

## <a name="add-a-new-er-format-configuration"></a>Yeni bir ER biçim yapılandırması ekleme  
 1. Yeni bir biçim oluşturmak yerine, daha önce kaydetmiş olduğunuz ER biçimi yapılandırma dosyasını (Cheques printing format.xml) yükleyebilirsiniz. Bu dosya, önceden yazdırılan formu ve bu biçimin 'Çekler için model' veri modelindeki eşlemesini kullanan çekleri yazdırmaya yönelik biçim için örnek düzeni içerir.   
 2. Değiştir seçeneğine tıklayın.  
 3. XML dosyasından yükle'ye tıklayın.  
 4. Gözat'a tıklayın ve Çek yazdırma biçimi.xml dosyasını seçin.   
 5. Tamam'a tıklayın.  
 6. Ağaçta, 'Çekler için model' öğesini genişletin.  
 7. Ağaçta 'Çekler için model\Çek yazdırma biçimi' seçin.  
 8. Yüklenen biçim resimler içeren Excel ve Word biçiminde belgeler oluşturmak için kullanılır.   

## <a name="configure-er-user-parameters"></a>ER kullanıcı parametrelerini yapılandırma  
 1. Eylem Bölmesi'nde, Yapılandırmalar'a tıklayın.  
 2. Kullanıcı parametreleri'ne tıklayın.  
 3. Çalıştırma ayarları alanında Evet'i seçin.  
  Seçilen biçimin tamamlanmış sürümü yerine taslak sürümünü başlatmak için 'Taslak çalıştır' bayrağını etkinleştirin.  
 4. Tamam'a tıklayın.  

## <a name="configure-cash--bank-management-parameters"></a>Nakit ve banka yönetimi parametrelerini yapılandırma  
 1. Nakit ve banka yönetimi > Banka hesapları > Banka hesapları öğesine gidin.  
 2. Banka hesabı alanında "USMF OPER" değeriyle filtre uygulamak için Hızlı Filtre'yi kullanın.  
 3. Eylem Bölmesinde Kurulum'a tıklayın.  
 4. Denetle'yi tıklatın.  
 5. Kurulum bölümünü genişletin.  
 6. Düzenle öğesine tıklayın.  
 7. Şirket logosu alanından Evet'i seçin.  
 8. Şirket logosuna tıklayın.  
 9. Değiştir seçeneğine tıklayın.  
 10. Gözat'a tıklayın ve daha önce indirdiğiniz Şirket logosu.png dosyasını seçin.   
 11. Kaydet'e tıklayın.  
 12. Sayfayı kapatın.  
 13. İmza bölümünü genişletin.  
 14. İlk imzayı yazdır alanında Evet'i seçin.  
 15. Değiştir seçeneğine tıklayın.  
 16. Gözat'a tıklayın ve daha önce indirdiğiniz İmza görüntüsü.png dosyasını seçin.   
 17. Kopyalar bölümünü genişletin.  
 18. Filigran alanında, bir seçenek seçin.  
 19. Genel elektronik Dışa aktarma biçimi alanında Evet'i seçin.  
 20. 'Çek yazdırma formu' yapılandırmasını seçin.  
 21. Seçilen ER biçimi artık çekleri yazdırmak için kullanılır.  
 22. İliştir'e tıklayın.  
 23. Yeni'ye tıklayın.  
 24. Dosya'ya tıklayın.  
 25. Gözat'a tıklayın ve daha önce indirdiğiniz İmza görüntüsü 2.png dosyasını seçin.   
 26. Sayfayı kapatın.  
 27. Sayfayı kapatın.  
 28. Sayfayı kapatın.  
 29. Nakit ve Banka yönetimi > Kurulum > Nakit ve Banka yönetim parametreleri.  
 30. Etkin olmayan banka hesaplarında açık provizyon oluşturmaya izin ver: alanında Evet'i seçin.  
 31. Kaydet'e tıklayın.  
 32. Sayfayı kapatın.  

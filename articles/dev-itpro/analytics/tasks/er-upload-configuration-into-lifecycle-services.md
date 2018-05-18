--- 
title: "Elektronik raporlama (ER) için Lifecycle Services'a bir yapılandırmayı yükleme"
description: "Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, yeni bir Elektronik Raporlama (ER) oluşturabilir. ve bunu Microsoft Lifecycle Services (LCS)'ye yükleyebilir."
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3d9c2192bac8477e9c9376aab3e3b561da777569
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---
# <a name="upload-a-configuration-into-lifecycle-services-for-electronic-reporting-er"></a>Elektronik raporlama (ER) için Lifecycle Services'a bir yapılandırmayı yükleme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, yeni bir Elektronik Raporlama (ER) oluşturabilir. ve bunu Microsoft Lifecycle Services (LCS)'ye yükleyebilir.

Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma oluşturacak ve bunu LCS'ye yükleyeceksiniz. Bu adımlar, ER yapılandırmaları şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir. Bu adımları tamamlamak için, öncelikle "Bir yapılandırma sağlayıcı oluşturun ve etkin olarak işaretleyin" yordamındaki adımları tamamlamanız gerekir. Bu adımları tamamlamak için LCS erişimi de gereklidir.

1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
2. 'Litware, Inc.'ı seçin. ve etkin olarak ayarlayın.
3. Yapılandırmalar'a tıklayın.

## <a name="create-a-new-data-model-configuration"></a>Yeni bir veri modeli yapılandırması oluşturun
1. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
    * Elektronik belgeler için bir örnek veri modeli içeren bir yapılandırma oluşturacaksınız. Bu veri modeli yapılandırması daha sonra LCS'ye yüklenecektir.  
2. İsim alanında 'Örnek model yapılandırması' yazın.
    * Örnek model yapılandırması  
3. Açıklama alanına, 'Örnek model yapılandırması' yazın.
    * Örnek model yapılandırması  
4. Konfigürasyon oluştur'u tıklatın.
5. Model tasarımcısı'na tıklayın.
6. Yeni'ye tıklayın.
7. İsim alanına 'Giriş noktası' yazın.
    * Giriş noktası  
8. Ekle öğesini tıklatın.
9. Kaydet'e tıklayın.
10. Sayfayı kapatın.
11. Durumu değiştir öğesine tıklayın.
12. Tamamla öğesine tıklayın.
13. Tamam'a tıklayın.

## <a name="register-a-new--repository"></a>Yeni bir havuz kaydedin
1. Sayfayı kapatın.
2. Depolar'a tıklayın.
    * Bu, Litware, Inc. için havuzların listesini açmanızı sağlayacaktır. yapılandırma sağlayıcısı.  
3. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
    * Bu, yeni bir havuz eklemenize olanak sağlar.  
4. Yapılandırma havuz türü alanında LCS'yi seçin.
5. Havuz oluştur'a tıklayın.
6. Proje alanında bir değer girin veya seçin.
    * İstenilen LCS projesini seçin. Projeye erişiminiz olmalıdır.  
7. Tamam'a tıklayın.
    * Yeni bir havuz girişini tamamlayın.  
8. Listede, seçili satırı işaretleyin.
    * LCS havuz kaydını seçin.  
    * Mevcut sağlayıcı tarafından işaretlenen kayıtlı bir havuzun, yani sadece bu sağlayıcının sahip olduğu yapılandırmaların bu havuzda kullanılabileceğini ve bunun doğrultusunda, seçili LCS projesine karşıya yüklenebileceğini unutmayın.  
9. Aç'a tıklayın.
    * ER yapılandırmalarının listesini görüntülemek için havuzu açın. Bu proje ER yapılandırmaları paylaşımı için henüz kullanılmamışsa, bu boş olacaktır.  
10. Sayfayı kapatın.
11. Sayfayı kapatın.

## <a name="upload-configuration-into-lcs"></a>Yapılandırmayı LCS'ye karşıya yükleyin
1. Yapılandırmalar'a tıklayın.
2. Ağaçta seçin 'Örnek model yapılandırması' seçeneğini işaretleyin.
    * Tamamlanmış olan oluşturulan bir yapılandırmayı seçin.  
3. Listede, istenen kaydı bulun ve seçin.
    * 'Tamamlandı' durumuna sahip seçili konfigürasyona sahip sürümü seçin.  
4. Durumu değiştir öğesine tıklayın.
5. Paylaş'ı tıklatın.
    * LCS'de yayımlandığında yapılandırma durumu 'Tamamlandı' seçeneğinden 'Paylaşıldı' seçeneğine değişecektir.  
6. Tamam'a tıklayın.
7. Listede, istenen kaydı bulun ve seçin.
    * 'Paylaşıldı' durumuna sahip yapılandırma sürümünü seçin.  
    * Seçili sürümün durumunun 'Paylaşılan'dan 'Tamamlandı'ya değiştiğini unutmayın.  
8. Sayfayı kapatın.
9. Depolar'a tıklayın.
    * Bu, Litware, Inc. için havuzların listesini açmanızı sağlayacaktır. yapılandırma sağlayıcısı.  
10. Aç'a tıklayın.
    * LCS deposunu seçin ve açın.  
    * Not: Seçili yapılandırma, LCS projesinin seçili bir varlığı olarak gösterilir.  
    * https://lcs.dynamics.com kullanarak LCS'yi açın. Daha önce havuz kaydı için kullanılan bir proje açın, bu projenin 'Varlık kütüphanesini' açın ve 'Kural Yöneticisi yapılandırma' kıymet türünün içeriğini genişletin – karşıya yüklenen ER yapılandırma kullanılabilir olacaktır. Not: Bu LCS projesine erişim sağlayıcısının erişimi varsa, karşıya yüklenen LCS yapılandırmasını başka bir Microsoft Dynamics 365 for Finance and Operations örneğine alınabilir.  



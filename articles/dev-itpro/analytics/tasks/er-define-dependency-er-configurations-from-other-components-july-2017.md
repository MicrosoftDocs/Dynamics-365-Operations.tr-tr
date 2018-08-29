--- 
title: "ER yapılandırmalarının diğer bileşenlere bağımlılığını tanımlama"
description: "Bu adımları tamamlamak için önce ER Model eşleme yapılandırmalarını yönet görev kılavuzundaki adımları tamamlamalı ve Microsoft Dynamics Lifecycle Services (LCS) üzerinde erişim sahibi olmanız gerekir."
author: NickSelin
manager: AnnBe
ms.date: 06/23/2017
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 18eb8de7c851e5477d93a00f744fe56929c43ca2
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---
# <a name="define-the-dependency-of-er-configurations-on-other-components"></a>ER yapılandırmalarının diğer bileşenlere bağımlılığını tanımlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu adımları tamamlamak için önce ER Model eşleme yapılandırmalarını yönet görev kılavuzundaki adımları tamamlamalı ve Microsoft Dynamics Lifecycle Services (LCS) üzerinde erişim sahibi olmanız gerekir.

Bu yordam, bir Elektronik raporlama (ER) yapılandırmasının nasıl tasarlanacağını ve diğer yazılım bileşenlerine olan bağımlılıklarını nasıl belirtileceğini gösterir; bu sayede yapılandırmanı belirli bir Microsoft Dynamics 365 for Finance and Operations sürümüne doğru şekilde indirildiğinden emin olmaya yardımcı olabilirsiniz. Bu örnekte, Litware, Inc. adlı örnek şirket için gerekli ER yapılandırmalarını oluşturacaksınız. 

Bu yordam Sistem yöneticisi veya Elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar içindir. Adımlar, ER yapılandırmaları şirketler arasında paylaşıldığı için herhangi bir şirkette gerçekleştirilebilir. 

1. Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.
    * Yapılandırmalar ağacının 'Örnek veri modeli' yapılandırmasını ve alt öğelerini içerdiğinden emin olun. Aksi takdirde, görev kılavuzundaki, ER Model eşleme yapılandırmalarını yönet üzerindeki adımları tamamlayın ve bu kılavuzu yeniden başlatın.   

## <a name="define-the-dependency-of-er-configurations-from-other-components"></a>Diğer bileşenlerden ER yapılandırmalarının bağımlılığını tanımla
1. Ağaçta 'Örnek veri modeli' seçeneğini genişletin.
2. Ağaçta, 'Örnek veri modeli\Örnek eşleme' seçeneğini belirleyin.
    * 'Örnek eşleme' model eşleme yapılandırmasının taslak sürümünü seçtik. Şimdi bunun diğer yazılım bileşenleriyle bağımlılığını tanımlayacağız. Bu adım, bu yapılandırmasının sürümünü bir ER havuzundan indirilmesini ve bu sürümün daha fazla kullanımını denetlemek için bir önkoşuldur.   
3. Önkoşullar bölümünü genişletin.
    * Uygulama 'önkoşulları' grubunun bu aşamada otomatik olarak eklenmiş olduğunu unutmayın. Bu grup, veri modeli yapılandırmasını referans alan bileşenin önkoşulunu içerir ve Uygulama bayrağı açıktır. Bu bayrak 'Örnek eşleme' modeli eşleme yapılandırmasının, veri modeli, 'Örnek veri modelinin' veri modelinin uygulaması olarak kabul edildiği anlamına gelir. Bu bileşen, ER'yi 'Örnek eşleme' eşleme yapılandırmasını bir ER havuzundan, 'Örnek veri modeli' model yapılandırması indirildiğinde indirmeye zorlayacaktır.   
4. Düzenle öğesine tıklayın.
    * Bir yazılım bileşeninden bir yapılandırma sürümüne geçerli sürümün tek bir bağımlılığı, bileşenin türünü ve bileşen sürümü ya da bileşen sürümlerinin aralığını tanımlayarak belirtilebilir.  
    * İstenen bağımlılıklar birlikte gruplandırılabilir. 'Tümü' gruplama türü seçildiğinde, bu grubun bağımlılık koşulu bu grup ve alt gruptan her bir bağımlılık koşulu yerine getirildiğinde yerine getirilmiş sayılır. 'Biri' gruplama türü seçildiğinde, bu grubun bağımlılık koşulu bu grup ve alt gruptan en az bir bağımlılık koşulu yerine getirildiğinde yerine getirilmiş sayılır.   
5. Yeni'ye tıklayın.
6. Ürün önkoşul bileşenini seçin.
7. Microsoft Dynamics 365 for Operations sürüm (1611) seçin.
8. Sürüm alanına '[7.1.1541.3036,8)' yazın.
    * (7.1.1541.3036,8)  
    * Girdiğiniz bağımlılıklar bu yapılandırma herhangi bir ER havuzundan indirildiğinde değerlendirilecektir. Bu yapılandırma sürümü ER havuzundan, 'Örnek veri modeli' yapılandırmasının 1. sürümü halihazırda yerinde olduğunda veya önceden indirildiğinde indirilecektir. Önceden indirilirse, sürümünün 7.1.1541.3036 veya sonrası olan ancak sürüm 8'i geçmeyen Finance and Operations içerisinde tamamlanması gerekir.   
9. Kaydet'e tıklayın.
10. Sayfayı kapatın.
11. Durumu değiştir öğesine tıklayın.
12. Tamamla öğesine tıklayın.
13. Tamam'a tıklayın.
14. Ağaçta, 'Örnek veri modeli\Örnek eşleme (alternatif)' seçeneğini belirleyin.
15. Düzenle öğesine tıklayın.
16. Yeni'ye tıklayın.
17. Ürün önkoşul bileşenini seçin.
18. Microsoft Dynamics AX 7.0 RTW'yi seçin.
19. Sürüm alanına '[7.0.1265.3015,7.1)' yazın.
    * (7.0.1265.3015,7.1)  
    * Bağımlılıklar bir yapılandırma herhangi bir ER havuzundan indirildiğinde değerlendirilecektir. Bu yapılandırma sürümü ER havuzundan, 'Örnek veri modeli' yapılandırmasının 1. sürümü halihazırda yerinde olduğunda veya önceden indirildiğinde indirilecektir. Önceden indirilirse, sürümünün 7.0.1265.3015 veya sonrası olan ancak küçük sürüm 1'i geçmeyen Microsoft Dynamics 365 for Finance and Operations, Enterprise edition içerisinde tamamlanması gerekir.   
20. Kaydet'e tıklayın.
21. Sayfayı kapatın.
22. Durumu değiştir öğesine tıklayın.
23. Tamamla öğesine tıklayın.
24. Tamam'a tıklayın.

## <a name="configure-the-er-repository"></a>ER havuzunu yapılandırın
1. Sayfayı kapatın.
2. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
    * Geçerli ER sağlayıcısı Litware, Inc. için ER havuzlarının listesini açın.  
3. Listede, seçili satırı işaretleyin.
4. Depolar'a tıklayın.
5. Filtreleri göster'e tıklayın.
6. "İçerir" filtre işlecini kullanarak "Tür adı" alanına bir "LCS" filtre değeri girin.
    * LCS havuzu geçerli ER sağlayıcı için zaten kayıtlı ise, bu alt görevin kalan adımlarını atlayabilirsiniz. LCS havuzu zaten kayıtlı değilse, kalan adımları tamamlayın.   
7. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
8. Yapılandırma havuz türü alanında LCS'yi girin.
9. Havuz oluştur'a tıklayın.
10. Proje alanında bir değer girin veya seçin.
    * 'Proje' alanının aramasından arzu edilen LCS proje aramasını seçin.  
11. Tamam'a tıklayın.
12. Sayfayı kapatın.

## <a name="upload-configurations-to-lcs"></a>Yapılandırmaları LCS'ye karşıya yükleyin
1. Raporlama konfigürasyonları'na tıklayın.
2. Ağaçta 'Örnek veri modeli' seçeneğini belirleyin.
3. Bu yapılandırmanın tamamlanan sürümünü seçin.
4. Durumu değiştir öğesine tıklayın.
5. Paylaş'ı tıklatın.
6. Tamam'a tıklayın.
    * Bu model yapılandırmasının Sürüm 1'i, LCS'ye, önceden yapılandırılmış ER havuzunun LCS projesini kullanarak karşıya yüklenmiştir.   
7. Ağaçta 'Örnek veri modeli' seçeneğini genişletin.
8. Ağaçta, 'Örnek veri modeli\Örnek eşleme' seçeneğini belirleyin.
9. Bu yapılandırmanın tamamlanan sürümünü seçin.
10. Durumu değiştir öğesine tıklayın.
11. Paylaş'ı tıklatın.
12. Tamam'a tıklayın.
    * Bu model eşleme yapılandırmasının Sürüm 1.1'i, LCS'ye, önceden yapılandırılmış ER havuzunun LCS projesini kullanarak karşıya yüklenmiştir.   
13. Ağaçta, 'Örnek veri modeli\Örnek eşleme (alternatif)' seçeneğini belirleyin.
14. Bu yapılandırmanın tamamlanan sürümünü seçin.
15. Durumu değiştir öğesine tıklayın.
16. Paylaş'ı tıklatın.
17. Tamam'a tıklayın.
    * Bu model eşleme yapılandırmasının Sürüm 1.1'i, LCS'ye, önceden yapılandırılmış ER havuzunun LCS projesini kullanarak karşıya yüklenmiştir.   

## <a name="evaluate-er-configuration-dependencies"></a>ER yapılandırma bağımlılıklarını değerlendirin
    * Oluşturulan yapılandırmaları sistemden sileceğiz ve onları LCS havuzundan yeniden indireceğiz.  
1. Ağaçta, 'Örnek veri modeli\Örnek eşleme' seçeneğini belirleyin.
2. Sil'i tıklatın.
3. Evet'i tıklatın.
4. Ağaçta, 'Örnek veri modeli\Örnek eşleme (alternatif)' seçeneğini belirleyin.
5. Sil'i tıklatın.
6. Evet'i tıklatın.
7. Ağaçta, 'Örnek veri modeli\Örnek biçim' seçeneğini belirleyin.
8. Sil'i tıklatın.
9. Evet'i tıklatın.
10. Ağaçta 'Örnek veri modeli' seçeneğini belirleyin.
11. Sil'i tıklatın.
12. Evet'i tıklatın.
13. Sayfayı kapatın.
    * Geçerli ER sağlayıcısı Litware, Inc. için ER havuzlarının listesini açın.  
14. Depolar'a tıklayın.
15. Filtreleri göster'e tıklayın.
16. "İçerir" filtre işlecini kullanarak "Tür adı" alanına bir "LCS" filtre değeri girin.
17. Aç'a tıklayın.
18. Ağaçta 'Örnek veri modeli' seçeneğini belirleyin.
    * Geçerli havuz için ER yapılandırmalarının her sürümü için önceden belirlenmiş önkoşulların yerine getirilip getirilmediğini gösteren bir değerlendirme görüntüleyebileceğinizi unutmayın. Bu değerlendirmeyi görüntülemek Önkoşulları denetle'yi tıklatın.   
19. Ön koşulları kontrol et'i tıklatın.
20. İçe aktar'ı tıklatın.
21. Evet'i tıklatın.
22. Sayfayı kapatın.
23. Sayfayı kapatın.
24. Sayfayı kapatın.
25. Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.
26. Ağaçta 'Örnek veri modeli' seçeneğini genişletin.
    * Model 'Örnek eşleşme' eşleme yapılandırmasının, seçilen veri modeli yapılandırması ile birlikte indirildiğini unutmayın. İki dosya birlikte indirilmiştir çünkü 'Örnek eşleşme', seçilen veri modelini uyguluyor olarak tanımlanmıştır ve Finance and Operations için uygulanabilirdir. 'Örnek eşleşme (alternatif)' yapılandırması, gerekli uygulama sürümü yerine getirilmediği için indirilmemiştir.   
    * Dynamics 365 for Finance and Operations, Enterprise edition'a oturum açar, aynı sağlayıcıya kaydolur, aynı LCS projesine erişir ve aynı veri modeli yapılandırmasını indirirseniz, 'Örnek eşleme (alternatif)' yapılandırması indirilir ve 'Örnek eşleme' yapılandırması atlanır.  



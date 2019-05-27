---
title: ER Biçiminizi, o biçimin yeni bir temel sürümünü benimseyerek yükseltin.
description: Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcının, bir Elektronik raporlama (ER) biçim yapılandırmasını nasıl sürdürebileceğini gösterir.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 040505f567b9db1a5987e4ada38d46f919440c96
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544461"
---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a>ER Biçiminizi, o biçimin yeni bir temel sürümünü benimseyerek yükseltin.

[!include [task guide banner](../../includes/task-guide-banner.md)]

Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcının, bir Elektronik raporlama (ER) biçim yapılandırmasını nasıl sürdürebileceğini gösterir. Bu yordam, bir yapılandırma sağlayıcısından (CP) alınan biçime dayalı olarak bir biçimin özel bir sürümünün nasıl oluşturulabileceğini açıklar. Ayrıca, bu biçimin yeni bir temel sürümünün nasıl benimseneceğini de açıklar.



Bu adımları tamamlamak için önce "yapılandırma sağlayıcı oluşturmak ve etkin olarak işaretleme" ve "Kullanım biçimi ödemeler için elektronik belgeleri oluşturmak için oluşturulan" yordamlarındaki adımları tamamlamanız gerekir. Bu adımlar GBSI şirketinde gerçekleştirilebilir.


## <a name="select-format-configuration-for-customization"></a>Özelleştirme için yapılandırma biçimi seçin
1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
    * Bu örnekte örnek şirket Litware, Inc. (http://www.litware.com) belirli bir ülke için elektronik ödemeleri destekleyen bir biçim yapılandırma sağlayıcısı görevi görecektir.    Örnek şirket Proseware, Inc. (http://www.proseware.com) Litware, Inc. tarafından sağlanan biçim yapılandırmasının tüketicisi görevi görecektir. Proseware, Inc. bu ülkenin belirli bölgelerdeki biçimleri kullanır.  
2. Raporlama konfigürasyonları'na tıklayın.
3. Filtreleri göster'e tıklayın.
4. Şu filtreleri uygulayın: "ile başlar" filtre işlecini kullanarak "Ad" alanında "BACS (Birleşik Krallık hayali)" için bir filtre değeri girin
    * BACS (UK hayali)  
    * Seçili biçim yapılandırması BACS'nin (Birleşik Krallık hayali) sahibi, sağlayıcı Litware, Inc.'dir.  
5. Filtreleri göster'e tıklayın.
6. Listede, istenen kaydı bulun ve seçin.
    * Tamamlandı durumunda olan biçim sürümü, Proseware, Inc. özelleştirme için.  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a>Elektronik belgenin özel bir biçim için yeni bir konfigürasyonunu oluşturma
    * Proseware, Inc. BACS (UK hayali) yapılandırmasının, hizmet aboneliklerine uygun olarak Litware, Inc.'den ödeme belgeleri oluşturmak için gerekli biçimi içeren, alınan sürüm 1.1. Proseware, Inc. kendi ülkesi için bunu bir standart olarak kullanmak istiyor fakat çeşitli bölgesel gereklilikleri desteklemek için bazı özelleştirmeler gereklidir. Proseware, Inc. ayrıca, özelleştirilmiş bir biçimden Litware Inc. tarafından (yeni ülke gereksinimlerini destekleyen) gelen yeni sürüme hızlı bir biçimde geçiş yapmak için yükseltme kabiliyetini de tutmak istiyor ve bu yükseltmeyi en düşük maliyetle gerçekleştirmek istiyor.  Bunu yapmak için Proseware, Inc'nin Litware, Inc. yapılandırması BACS'yi (Birleşik Krallık hayali) taban olarak kullanan bir yapılandırma oluşturması gerekir.  
1. Sayfayı kapatın.
2. Etkin bir sağlayıcı yapmak için Proseware, Inc.'i seçin.
3. Etkin olarak ayarla'ya tıklayın.
4. Raporlama konfigürasyonları'na tıklayın.
5. Ağaçta, 'Ödemeler (Basitleştirilmiş model)' genişletin.
6. Ağaçta 'Payments (simplified model)\BACS (UK fictitious)' seçin.
    * Litware, Inc.'den BACS (Birleşik Krallık hayali) yapılandırmasını seçin.     Proseware, Inc. sürüm 1.1'i özel sürümün tabanı olarak kullanacaktır.  
7. İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.
    * Bu, özel bir ödeme biçimi için yeni bir yapılandırma oluşturmanızı sağlar.  
8. Yeni alanında, 'İsimden Türet: BACS (UK hayali), Litware, Inc.' girin.
    * Özel sürümü oluşturma için temel olarak BACS (UK hayali) kullanımını onaylamak için Türet seçeneğini belirleyin.  
9. İsim alanına, 'BACS (UK hayali özel)' yazın.
    * BACS (Birleşik Krallık, hayali özel)  
10. Açıklama alanına, "BACS satıcı ödemesi (Birleşik Krallık özel)" yazın.
    * BACS satıcı ödemesi (Birleşik Krallık, hayali özel)  
    * Etkin yapılandırma sağlayıcısı (Proseware, Inc.) otomatik olarak buraya girilir. Bu sağlayıcının, bu yapılandırmayı sürdürmesi mümkün olacaktır. Diğer sağlayıcılar bu yapılandırmayı kullanabilir, ancak onu sürdüremezler.  
11. Konfigürasyon oluştur'u tıklatın.

## <a name="customize-your-format-for-the-electronic-document"></a>Elektronik belge için biçiminizi özelleştirme
1. Tasarımcı'yı tıklatın.
2. Genişlet/daralt'a tıklayın.
3. Genişlet/daralt'a tıklayın.
4. Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Banka" öğesini seçin.
5. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
6. Ağaçta seçin 'XML\Element'.
7. İsim alanına 'IBAN' yazın.
    * IBAN  
8. Tamam'a tıklayın.
9. Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Banka\IBAN" öğesini seçin.
10. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
11. Ağaçta seçin 'Text\String'.
12. Tamam'a tıklayın.
13. Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Ad\Dize" öğesini seçin.
14. Maksimum uzunluk alanında 60 girin.
15. Eşleme sekmesini tıklatın.
16. Ağaçta, 'model'i genişletin.
17. Ağaçta genişletin 'model\Payments'.
18. Ağaçta genişletin 'model\Payments\Creditor'.
19. Ağaçta genişletin 'model\Payments\Creditor\Account'.
20. Ağaçta, "model\Ödemeler\Alacaklı\Hesap\IBAN" öğesini seçin.
21. Ağaçta, "Xml\İleti\Ödemeler\Madde =  model.Payments\Satıcı\Banka\IBAN\Dize" öğesini seçin.
22. Bağla'ya tıklayın.
23. Kaydet'e tıklayın.

## <a name="validate-the-customized-format"></a>Özelleştirilmiş biçimi doğrulama
1. Doğrula'ya tıklayın.
    * Tüm bağlamaların sorunsuz olduğundan emin olmak için özelleştirilmiş biçimi düzeninin ve veri eşlemesi değişikliklerini doğrulayın.  
2. Sayfayı kapatın.

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a>Özel biçim yapılandırmasının geçerli sürümünün durumunu değiştirme
    * Ödeme belgesi oluşturulmasında kullanılabilir duruma getirmek için tasarlanan biçim yapılandırmasının durumunu Taslak'tan Tamamlandı'ya değiştirin.  
1. Durumu değiştir öğesine tıklayın.
    * Seçili yapılandırmanın geçerli sürümünün Taslak durumunda olduğunu unutmayın.  
2. Tamamla öğesine tıklayın.
3. Açıklama alanına bir değer girin.
4. Tamam'a tıklayın.
5. Listede, istenen kaydı bulun ve seçin.
    * Oluşturulan yapılandırmanın tamamlanmış sürüm 1.1.1 olarak kaydedildiğini unutmayın. Bu, BACS (Birleşik Krallık, hayali özel) biçiminin, Ödemeler (basitleştirilmiş model) veri modelinin 1. sürümüne dayalı olan BACS (Birleşik Krallık hayali) biçiminin 1. sürümüne dayalı olduğu anlamına gelmektedir.  

## <a name="test-the-customized-format-to-generate-payment-files"></a>Ödeme dosyaları oluşturmak için özelleştirilmiş biçimi test et
    * Paralel Dynamics 365 for Finance and Operations, Enterprise edition oturumunda "Ödemeler için elektronik belgeleri oluşturmak için oluşturulan biçimi kullan" yordamındaki adımları tamamlayın. Elektronik Ödeme yöntemi parametrelerinde BACS (UK hayali özel) biçimi seçin. Oluşturulan ödeme dosyasında son sunulan XML düğümünün, bölgesel gereksinimleri uygun IBAN kodu sunma içerdiğinden emin olun.  

## <a name="update-the-existing-country-specific-configuration"></a>Ülkeye özgü varolan yapılandırmayı güncelleştirmek
    * Litware, Inc. BACS (UK hayali) yapılandırmasını güncelleştirmek ve elektronik belge biçimini yönetmek için yeni ülke gereksinimleri benimsemesi gerekir. Daha sonra, bu yeni sürümünde Proseware, Inc. dahil olmak üzere hizmet aboneleri için sunulan bu yapılandırma içine alınacaktır.  
    * Gerçek servis sağlama ile ilgili işlemlerde, her yeni BACS (UK hayali) sürümü Proseware, Inc. tarafından Litware, Inc.'nin yapılandırmalarının LCS havuzundan alınabilir. Bu yordamda biz bu servis sağlayıcı adına BACS (UK hayali) güncelleştirmenin benzetimini yapacağız.  
1. Sayfayı kapatın.
2. Litware, inc. sağlayıcısı seçin.
3. Etkin olarak ayarla'ya tıklayın.
4. Raporlama konfigürasyonları'na tıklayın.
5. Ağaçta, 'Ödemeler (Basitleştirilmiş model)' genişletin.
6. Ağaçta 'Payments (simplified model)\BACS (UK fictitious)' seçin.
    * Taslak sürümü Litware, Inc. şirketine aittir. sağlayıcı BACS (UK hayali), ülkeye özgü yeni gereksinimlerini desteklemek için değişiklikleri getirmek üzere seçilir.  

## <a name="localize-the-base-format-of-the-electronic-document"></a>Elektronik belge temel biçimini yerelleştirme.
    * Ülkeye özel yeni gereksinimlerin Litware, Inc. tarafından destekleneceğini varsayalım:  - Her ödeme hareketi için alacaklı banka SWIFT kodu için bir değer.  - Oluşturma dosyasında satıcının adı için 100 karakter metin uzunluğu sınırı.  
    * Yeni ülkeye özgü gereksinimler  
    * Gerekli değişiklikleri tanıtmak için istenen yapılandırmanın taslak sürümünü seçin.  
1. Tasarımcı'yı tıklatın.
2. Genişlet/daralt'a tıklayın.
3. Genişlet/daralt'a tıklayın.
4. Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Banka" öğesini seçin.
5. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
6. Ağaçta seçin 'XML\Element'.
7. İsim alanına 'SWIFT' yazın.
    * SWIFT  
8. Tamam'a tıklayın.
9. Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Banka\SWIFT" öğesini seçin.
10. Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.
11. Ağaçta seçin 'Text\String'.
12. Tamam'a tıklayın.
13. Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Ad\Dize" öğesini seçin.
14. Maksimum uzunluk alanında 100 girin.
15. Eşleme sekmesini tıklatın.
16. Ağaçta, 'model'i genişletin.
17. Ağaçta genişletin 'model\Payments'.
18. Ağaçta genişletin 'model\Payments\Creditor'.
19. Ağaçta genişletin 'model\Payments\Creditor\Agent'.
20. Ağaçta, "model\Ödemeler\Alacaklı\Temsilci\SWIFT" öğesini seçin.
21. Ağaçta, "Xml\İleti\Ödemeler\Madde =  model.Payments\Satıcı\Banka\SWIFT\Dize" öğesini seçin.
22. Bağla'ya tıklayın.
23. Kaydet'e tıklayın.

## <a name="validate-the-localized-format"></a>Yerelleştirilmiş biçimi doğrulama
1. Doğrula'ya tıklayın.
2. Sayfayı kapatın.

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a>Temel biçim yapılandırmasının geçerli sürümünün durumunu değiştirin
    * Güncelleştirilen temel biçim yapılandırmasının durumunu, ödeme belgeleri ve bundan türetilen biçim yapılandırmalarının oluşturulmasında kullanılabilmesi için, Taslak'tan Tamamlandı'ya değiştirin.  
1. Durumu değiştir öğesine tıklayın.
    * Seçili yapılandırmanın geçerli sürümünün Taslak durumunda olduğunu unutmayın.  
2. Tamamla öğesine tıklayın.
3. Açıklama alanına bir değer girin.
4. Tamam'a tıklayın.
5. Listede, istenen kaydı bulun ve seçin.

## <a name="change-the-base-version-for-the-custom-format-configuration"></a>Özel biçim yapılandırması için temel sürümü değiştir
    * Proseware, Inc.'nin BACS (UK hayali) yapılandırmasının yeni sürümü 1.2'nin yakın zaman önce duyurulan ülkeye özgü gereksinimleri uygun elektronik ödeme belgeleri oluşturmak kullanılabilir olduğunu bilgisi verilir. Proseware, Inc. bu ülke için bir standart olarak bunu kullanmaya başlamak istiyor.  Proseware, Inc'nin bunu yapmak için temel yapılandırma sürümünü, BACS (UK hayali özel) özel yapılandırma sürümü için değiştirmesi gerekiyor. BACS (UK hayali) 1.1 sürümü yerine yeni sürüm 1.2 kullanın.  
1. Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.
2. Etkin olarak işaretlemek için Proseware, Inc. sağlayıcısını seçin.
3. Etkin olarak ayarla'ya tıklayın.
4. Raporlama konfigürasyonları'na tıklayın.
5. Ağaçta, 'Ödemeler (Basitleştirilmiş model)' genişletin.
6. Ağaçta 'Payments (simplified model)\BACS (UK fictitious)' genişletin.
7. Ağaçta 'Payments (simplified model)\BACS (UK fictitious)\BACS (UK fictitious custom)' seçin.
    * Proseware, Inc. şirketine ait olan BACS (Birleşik Krallık, hayali özel) yapılandırmasını seçin.  
    * Gerekli değişiklikleri tanıtmak için seçili yapılandırmanın taslak sürümünü kullanın.  
8. Rebase'yi tıklatın.
    * Yapılandırmayı güncelleştirmek için yeni bir temel olarak uygulanması için yeni sürüm 1.2'yi temel yapılandırma olarak seçin.  
9. Tamam'a tıklayın.
    * Otomatik olarak birleştirilemeyen bazı biçim değişikliklerini temsil eden, yeni temel sürüm ile özel sürümün birleştirilmesi sırasında bazı çakışmaların ortaya çıktığını göz önünde tutun.  

## <a name="resolve-rebase-conflicts"></a>Rebase çakışmalarını çözümle
1. Tasarımcı'yı tıklatın.
    * Satıcının adı metin uzunluğu sınırına yapılan değişikliğin otomatik olarak çözümlenme uygulanamadığını göz önünde bulundurun. Bu nedenle, bu çakışmalar listesinde görüntülenir. Her Güncelleştirme türü çakışma için, aşağıdaki seçenekler mevcuttur:  - Önceki taban sürüm değerini (bu durumda 0 olan) getirmek için, daha önceki bir taban değeri uygula (ızgaranın üstündeki düğme).  - Yeni temel sürüm değerini (bu durumda 100) getirmek için temel bir değer uygula. (ızgara üzerindeki düğme).  - Kendi (özel) değerinizi tutun (bizim durumumuzda 60).  Satıcı adı uzunluğu için bir ülkeye özgü temel sınır olan 100 karakter limitini uygulamak için Uygula'yı tıklatın.  
    * Proseware, Inc. şirketinin ve Litware, Inc.'in yönetim biçiminde ilgili bileşenlerin otomatik olarak birleştirildiği, IBAN ve SWIFT kodları kullanarak bu biçim için özel ve yerel sürümlerinin olduğunu unutmayın.  
2. Taban değeri uygula'yı tıklatın.
    * Satıcı adlarına ülkeye özgü temel sınır olan 100 karakter limitini uygulamak için Uygula'yı tıklatın.  
3. Kaydet'e tıklayın.
    * Biçimi kaydetmek, çözümlenen çakışmaları çakışmalar listesinden kaldırır.  
4. Sayfayı kapatın.

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a>Özel biçim yapılandırmasının geçerli sürümünün durumunu değiştirin
1. Durumu değiştir öğesine tıklayın.
    * Güncelleştirilen, özel biçim yapılandırmasının durumunu Taslak'tan, Tamamlandı'ya değiştirin. Bu, ödeme belgeleri oluşturmak için biçim yapılandırmasını kullanılabilir hale getirir. Seçili yapılandırmanın geçerli sürümünün Taslak durumunda olduğunu unutmayın.  
2. Tamamla öğesine tıklayın.
3. Açıklama alanına bir değer girin.
4. Tamam'a tıklayın.
    * Oluşturulan yapılandırmanın tamamlanmış sürüm 1.2.2: taban BACS (UK hayali özel) biçiminin 2. sürümü, yani temel BACS (UK hayali) biçiminin 2. sürümüne dayalı, bu da Ödemeler (basitleştirilmiş model) veri modelinin 1. sürümüne dayalı olan sürüm olduğunu unutmayın.  

## <a name="test-the-customized-format-for-payment-files-generation"></a>Ödeme dosyaları oluşturması için özelleştirilmiş biçimi test et
    * Paralel Dynamics 365 for Finance and Operations, Enterprise edition oturumunda "Ödemeler için elektronik belgeleri oluşturmak için oluşturulan biçimi kullan" yordamındaki adımları tamamlayın. Elektronik Ödeme yöntemi parametrelerinde oluşturulan 'BACS (UK hayali özel)' biçimi seçin. Oluşturulan ödeme dosyasında Proseware, Inc. tarafından son sunulan XML düğümünün, bölgesel gereksinimleri uygun IBAN hesap kodu sunma içerdiğinden emin olun. Dosya ayrıca Litware, Inc. tarafından yakın zaman önce sunulan XML düğün sunum SWIFT banka kodunu ülke gereksinimlerine göre içermelidir.  


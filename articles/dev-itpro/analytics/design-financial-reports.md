---
title: "Mali raporları görüntüleme ve tasarlama"
description: "Bu makale, Microsoft Dynamics 365 for Finance and Operations için mali raporları görüntüleme ve oluşturma konusunda size yol gösteren alıştırmalar sağlar."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 10814
ms.assetid: cd5f6483-c09b-4c2d-9336-d22eb6ab6e4f
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b49cfe39732a450e4723419c50d8bcc3d64b7ec9
ms.openlocfilehash: d1fbcefd80f1c48fafbbcb6315406856eaae68a0
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="view-and-design-financial-reports"></a>Mali raporları görüntüleme ve tasarlama

[!include[banner](../includes/banner.md)]


Bu makale, Microsoft Dynamics 365 for Finance and Operations için mali raporları görüntüleme ve oluşturma konusunda size yol gösteren alıştırmalar sağlar. Mali raporlama, Finance and Operations içerisinde bulunan görüntüleme deneyimlerinden ve mali raporları oluşturmanızı ve düzenlemenizi sağlayan tek tıkla rapor tasarlayıcısından oluşur.  

<a name="exercise-1-generate-and-explore-a-default-financial-report"></a>Alıştırma 1: Bir varsayılan mali rapor oluşturma ve keşfetme
-----------------------------------------------------------

Bu alıştırma için mevcut bir varsayılan raporu oluşturacak ve keşfedeceksiniz. Bu rapor tüm hesapları içerir ve ayrıca hesaplar için hesap özelliklerini (özniteliklerini) içerir. Hareket bilgilerini ayrıntılı şekilde inceleyecek, boyut boyut filtreleri uygulayacak ve rapordaki para birimini değiştireceksiniz. İlk olarak, finansal raporlama için boyutların görüntülenme satırını güncelleştireceğiz. Bu işlem boyutların, mali raporların tasarlanması ve görüntülenmesi satırında nasıl görüntüleneceğini seçmenize izin verir.

1.  Genel muhasebedeki **Hesap Planı Boyutları** altındaki **Uygulamaları entegre etmek için mali boyut yapılandırma** öğesine gelin.
2.  Boyutları şu satırda olacak şekilde taşıyın:
    1.  Ana Hesap
    2.  İş Birimi
    3.  Maliyet Merkezi
    4.  Departman

    Not: Diğer boyutlar halihazırda bulundukları satırda kalabilir.
3.  Boyut yapılandırmasını kaydedin. Ardından, bir rapor oluşturacağız ve rapordaki verileri inceleyeceğiz.
4.  Genel muhasebede **Sorgular ve raporlar** altındaki **Mali raporlar** öğesine gelin.
5.  **GM Ayrıntısı – Varsayılan** adlı rapor satırını seçin.
6.  **Düzenle** öğesini seçin. Not: Tek tıklamayla rapor tasarımcısını indirmeniz ve oturum açmanız istenecektir. Oturum açmak için bilgilerinizi girin.
7.  Taban yılı 2012 olarak değiştirin ve **Oluştur** öğesini seçin. Bir rapor, rapor tasarımcısından oluşturulduktan sonra, yeni bir tarayıcı sekmesinde açılacaktır. Raporu yeni bir tarayıcıs sekmesine keşfedebilir veya ilk tarayıcı sekmenize gidebilir ve rapor buradan, **Mali raporlar** listesini seçerek açabilirsiniz.
8.  Açılan raporda, raporun hesap bilgilerini ayrıntılı şekilde incelemek için tutarlardan birini seçin.
9.  Hesap bilgilerine geldikten sonra verileri içeren bir hesap seçin **rapor hareket düzeyini** ayrıntılı şekilde inceleyin. Rapor hareket düzeyinde bu raporun tasarımına dahil edilen özellikleri (öznitelikleri) görebilirsiniz. Harekete ve hesaba bağlı olarak, özniteliklerden bazıları veya tümü görüntülenebilir.
10. Rapor hareket düzeyini kapatın.
11. Aynı veya farklı bir hesap seçin ve **fiş hareketlerini açın.** Fiş hareketleri seçilen hesabın dönemine, yılına ve hesap + boyut kombinasyonuna göre filtrelenir. Fiş hareketlerinden, hareket hakkındaki diğer bilgileri de keşfetmeyi seçebilirsiniz.
12. Fiş hareketlerini kapatın. Bir finansal rapor içinde, farklı bir dönem veya yıl için veya farklı öznitelikler ve boyutlar uygulayarak verileri görüntülemeyi seçebilirsiniz. Bu işlem **Rapor Seçenekleri** kullanılarak gerçekleştirilir.
13. **Rapor Seçenekleri** öğesini seçin.
14. **Bir boyut filtresi ekle** öğesini ve **İş Birimi** öğesini seçin.
15. Alana 001 yazın ve **Tamam** öğesini seçin. Raporda sadece 001 İş Birimi ile ilgili verileri görüntüler. Bu, raporun kişiselleştirilmiş bir görünümüdür ve başkalarının görüntülemesi için kullanılamaz.
16. Filtrelenen raporu kapatın. Mali raporlar, Finance and Operations'a eklenmiş olan herhangi bir para biriminde görüntülenebilir.
17. **Para birimini** öğesini seçin ve ardından **EUR** seçimini yapın. Rapor şimdi Euro cinsinde görüntüler. Bu rapor tasarıma dahil edilen tüm para birimi kodları veya para birimi simgeleri artık uygulanan para biriminde görüntülenmeye başlar. Bir para birimi için para birimi simgesi tanımlanmamışsa para birimi simgesi görüntülenmez.
18. **GL Ayrıntıları** raporunu kapatın.
19. **Rapor Tasarımcısını** kapatın.

## <a name="exercise-2-add-additional-account-properties-to-a-report-design"></a>Alıştırma 2: Bir rapor tasarımına ek hesap özellikleri ekleyin.
Bu alıştırmada mevcut bir varsayılan raporu değiştireceksiniz. Hem satır tanımını tüm hesapları içine alacak şekilde güncelleştirecek hem de sütun tanımını hesap özniteliklerini içine alacak şekilde güncelleştireceksiniz. Güncelleştirmeler tamamlandıktan sonra yeni oluşturulan raporu oluşturacak ve raporu keşfedeceksiniz. Mali raporlar listesinden başlayacağız.

1.  Genel muhasebede Sorgular ve raporlar altındaki **Mali raporlar** öğesine gelin.
2.  **Özet Mizan – Varsayılan** adlı rapor satırını seçin.
3.  **Düzenle** öğesini seçin. **Özet Mizan – Varsayılan**, rapor tasarımcısında açılacaktır.
4.  **Dosya** ve ardından **Farklı Kaydet** seçimlerini yapın ve Rapor Öznitelikler İçeren Ayrıntılı Mizan adın verin. Not: Rapor tasarımcısında ne zaman yeni bir rapor oluşturulsa Finance and Operations'ta mali raporlar listesi güncelleştirilir.
5.  Rapor tanımından, **Mizan – Varsayılan satır tanımını** açmak için satır tanım simgesini seçin.
6.  Satır tanımını **Özniteliklere Sahip Ayrıntılı Mizan** olarak farklı kaydedin
7.  İmleç, satır 50'deyken **Düzenle** ve ardından **Boyutlardan Satır Ekle** seçimlerini yapın. Boyutlardan satır eklenmesi, satır tanımınıza hangi boyutların dahil edileceğini seçmenize izin verir.  Bu alıştırma için, Ana Hesabı kullanarak satır tanımı oluşturacağız.
8.  **Ana Hesabın** tüm işaretleri içerdiğinden emin olun ve **Tamam** seçimini yapın. Satır tanımı şimdi tüzel kişilik USMF için ana hesapların tümünü içermektedir.
9.  Satır 11110'a gelin ve satır 11110'u silin.
10. Satır 11080'da **--- (Altı çizili tutarlar)** öğesini silin.
11. Satır 11140'ta B sütununa **Tüm hesapların toplamını** yazın.
12. C sütununda açılır listeden **TOT** seçimini yapın.
13. D sütununa **50:11080** yazın.
14. Satır tanımını **kaydedin**. Satır tanımı şimdi tüm hesapların yanı sıra hesaplarının tümünün birlikte eklenmesi için bir toplam satırı içermektedir. Ardından, sütun tanımını ek hesap özniteliklerini içine alacak şekilde güncelleştireceğiz.
15. **Özniteliklere Sahip Ayrıntılı Mizan** rapor tanımından **Özet Mizan – Varsayılan** sütun tanımını açmak üzere sütun tanımı simgesini seçin.
16. Sütun tanımını **Özniteliklere Sahip Ayrıntılı Mizan** olarak farklı kaydedin. Sütun tanımı mali veri sütunlarını, bir açıklama sütunu ve hesaplama sütunları içerir. Hesaplar hakkında ilave ayrıntılar sağlamak üzere sütun tanımına öznitelik sütunları ekleyeceğiz.
17. Aşağıdaki öznitelikler, sütun tanımına eklenecektir:
    -   Günlük Numarası
    -   Günlük Tanımı
    -   Hareket Tarihi
    -   Oluşturan
    -   Son değiştiren

18. I sütununda sütun türü olarak **ATTR** seçimini yapın. Ardından, öznitelik kategorisi olarak **Günlük Numarası** seçimini yapın.
19. Kalan öznitelikler için sütun eklemeye devam edin.
20. **Başlık 2** satırında eklenen yeni sütunların her biri için tanımlar ekleyin.
21. Sütun tanımını kaydedin. Şimdi satır tanımı ve sütun tanımı güncellenmiştir, şimdi bunları rapor tanımına eklememiz gerekiyor.
22. **Özniteliklere Sahip Ayrıntılı Mizan** rapor tanımından, hem satır tanımı hem sütun tanımı için Özniteliklere Sahip Özet Mizan seçimini yapın.
23. Taban yılını **2012** olarak değiştirin.
24. Rapor tanımını **kaydedin** ve **oluşturun**. Rapor oluşturma işlemi tamamlandıktan ve rapor açıldıktan sonra raporu ilk alıştırmada olduğu gibi inceleyebilirsiniz. Farklı özniteliklerin nasıl görüntülendiğini görmek için farklı hesapları ayrıntılı şekilde inceleyin.
25. **Özniteliklere Sahip Ayrıntılı Mizan** raporunu kapatın.
26. **Rapor Tasarımcısını** kapatın.

## <a name="exercise-3-create-a-multidimensional-report-using-a-reporting-tree"></a>Alıştırma 3: Bir raporlama ağacı kullanarak bir çok boyutlu rapor oluşturma
Bu alıştırma için mevcut bir varsayılan raporu değiştireceksiniz. Bir raporlama ağacı oluşturacak ve bir Maliyet Merkezi/Bölgesel Gelir Beyanı oluşturmak üzere bunu bir rapor tanımına ekleyeceksiniz. Güncelleştirmeler tamamlandıktan sonra Maliyet Merkezini/Bölgesel Gelir Beyanını oluşturacak ve raporlama ağacını kullanarak raporu inceleyeceksiniz. Mali raporlar listesinden başlayacağız.

1.  Genel muhasebede Sorgular ve raporlar altındaki **Mali raporlar** öğesine gelin.
2.  **Gelir Beyanı – Varsayılan** adlı rapor satırını seçin
3.  **Düzenle** öğesini seçin. **Gelir Beyanı – Varsayılan**, rapor tasarımcısında açılacaktır.
4.  **Dosya** menüsünde, **Yeni** seçimini yapın ve ardından **Raporlama Ağacı Tanımı** öğesini tıklayın
5.  **Düzenle** menüsünde **Boyutlardan Raporlama Birimleri Ekle** öğesini tıklayın...
6.  **Maliyet Merkezi** dışındaki tüm boyutların onay kutularını temizleyin.
7.  Maliyet Merkezi boyutu için **Boyuttan** alanını tıklayın, **007** girin ve ardından Sekme tuşuna basın. **Boyuta** alanına **018** girin.
8.  Ortaya çıkan ağacı **Bölüme Göre Maliyet Merkezi** adıyla **Kaydedin.** Şimdi raporlama ağacı oluşturuldu, bundan sonra raporlama ağacını Pazarlama, Operasyonlar ve Perakende olmak üzere üç yeni birleşik birimi içine alacak şekilde değiştireceğiz.
9.  **Pencere** menüsünde **Bölüme Göre Maliyet Merkezleri** öğesini tıklayın. (Raporlama ağacı kapatılmışsa gezinti panosunda Raporlama Ağacı Tanımlarından seçin.)
10. İki numaralı birim **Ticaret Fuarları** öğesini ve ardından **Raporlama Birimi Ekle** simgesini tıklayın.
11. Boş satırdaki varlık sütununu çift tıklatın ve **USMF** öğesini seçin.
12. B ve C sütunlarına **Pazarlama** yazın.
13. Beş numaralı birim **Hizmet Operasyonları** öğesini tıklayın ve ardından sağ tıklayın. **Raporlama Birim Ekle** öğesini seçin.
14. 11. adımı yineleyin.
15. B ve C sütunlarına **Operasyonlar** yazın.
16. On iki numaralı birimi **Satış Yeri** öğesini tıklayın ve ardından sağ tıklatın. **Raporlama Birimi Ekle** öğesini seçin.
17. 11. adımı yineleyin.
18. B ve C sütunlarına **Perakende** yazın. Pazarlama, Operasyonlar ve Perakende birimlerinin mevcut birleşik birimlerle aynı düzeyde görüntülendiğine dikkat edin. Yeni birimler bir sonraki adımda düzenlenecektir. Raporlama birimleri, yükselt ve indir sağ tıklama seçenekleriyle veya sürükle ve bırak yöntemiyle düzenlenir.
19. Üç numaralı birim **Ticaret Fuarları** öğesinin aktif olduğunu doğrulayın ve sağ tıklayın.
20. **Raporlama Birimini İndir** öğesini seçin. Birimin şimdi **Pazarlama** biriminin alt birimi olarak görüntülendiğine dikkat edin.
21. Dört numaralı birim **Pazarlama** **Kampanya** öğesini tıklayın ve sağ tıklayın.
22. **Raporlama Birimini İndir** öğesini seçin.
23. Grafik ekranından **Hizmet Operasyonları** düğmesini tıklayın. Farenin sol düğmesini basılı tutarak birimi sürükleyerek **Operasyonlar** üzerine bırakın. Üniteyi Operasyonlar grubuna bırakmak için sol fare düğmesini bırakın. **Üretim, Kalite Kontrol, Lojistik, Satın Alma ve Yönetim** için aynı adımları tekrarlayın.
24. İndirerek veya sürükleyip bırakarak **Satış Yeri**, **Süpermarket**, **Alışveriş Merkezi** ve **Çevrimiçi** alt birimlerini **Perakende** altında oluşturun.
25. Ortaya çıkan yeniden organizasyonu kaydedin. Şimdi raporlama ağacını oluşturduk ve düzenledik; artık rapor tanımına eklenebilir.
26. **Pencere** menüsünde rapor tanımını açmak için **Gelir Beyanı – Varsayılan** öğesini seçin.
27. **Ağaç türü** açılır okunu tıklayın ve **Raporlama ağacı** seçimini yapın.
28. Ağaç açılır okunu tıklayın ve **Bölüme Göre Maliyet Merkezleri** seçimini yapın.
29. Taban yılını **2012** olarak değiştirin, değişiklikleri **kaydedin** ve rapor **oluşturun**. Raporun oluşturulması tamamlandığında ve rapor açıldığında raporu inceleyebilirsiniz.
30. **Raporlama Ağacı** açılır menüsünü seçerek raporlama birimlerini görüntüleyin. Alternatif olarak, raporlama ağacının tüm birimlerin tüm bakiyelerini görmek için raporun bir satırını ayrıntılı şekilde inceleyebilirsiniz.
31. **Gelir Beyanı – Varsayılan** öğesini kapatın.
32. **Rapor Tasarımcısını** kapatın.

## <a name="exercise-4-create-a-consolidated-report-using-an-organization-hierarchy"></a>Alıştırma 4: Bir organizasyon hiyerarşisi kullanarak konsolide rapor oluşturma
Bu alıştırma için mevcut bir varsayılan raporu değiştireceksiniz. Bir Konsolide Gelir Beyanı ve Bilanço üretmek için rapor tanımına bir organizasyon hiyerarşisi ekleyeceğiz. Güncelleştirmeler tamamlandıktan sonra konsolide rapor oluşturacak ve raporlama ağacını kullanarak raporu inceleyeceksiniz. Mali raporlar listesinden başlayacağız.

1.  Genel muhasebede Sorgular ve raporlar altındaki **Mali raporlar** öğesine gelin.
2.  **Bilanço ve Gelir Beyanı Yan Yana – Varsayılan** adlı rapor satırını seçin
3.  **Düzenle** öğesini seçin. **Bilanço ve Gelir Beyanı Yan Yana – Varsayılan**, rapor tasarlayıcıda açılacaktır.
4.  **Dosya** &gt; **Farklı Kaydet** seçimlerini yapın ve rapora **Konsolide Bilanço ve Gelir Beyannamesi Yan Yana** adını verin.
5.  Taban yılını 2012 olarak değiştirin.
6.  Ağaç türü açılır okunu tıklayın ve **Organizasyon Hiyerarşileri** seçimini yapın.
7.  Ağaç açılır okunu tıklayın ve **Contoso Holdings** seçimini yapın.
8.  Değişiklikleri kaydedin ve raporu oluşturun. İstenirse, tüm raporlama birimlerini seçin. Raporun oluşturulması tamamlandığında ve rapor açıldığında raporu inceleyebilirsiniz.
9.  **Rapor Seçenekleri** öğesini seçin.
10. **Bir boyut filtresi ekle** öğesini ve **Departman** öğesini seçin.
11. Alana **022** yazın ve **Tamam** seçimini yapın.
12. Filtrelenen raporu kapatın.
13. Raporlama Ağaç **ı** açılır menüsünü seçerek raporlama birimlerini görüntüleyin. Alternatif olarak, raporlama ağacının tüm birimlerin tüm bakiyelerini görmek için raporun bir satırını ayrıntılı şekilde inceleyebilirsiniz.
14. **Konsolide Bilanço ve Gelir Beyanı Yan Yana** öğesini kapatın.
15. **Rapor Tasarımcısını** kapatın.

## <a name="exercise-5-create-a-sidebyside-departmental-report"></a>Alıştırma 5: Yan yana bir departman raporu oluşturma
Bu alıştırmada yeni bir rapor oluşturacaksınız. Bu rapor, yan yana bir departman gelir beyanıdır. Mevcut bir sıra tanımını kullanın, ancak farklı olarak, boyut filtrelerini kullanan yeni bir rapor tanımı ve yeni bir sütun tanımı oluşturun. Mali raporlar listesinden başlayacağız.

1.  Genel muhasebede Sorgular ve raporlar altındaki **Mali raporlar** öğesine gelin.
2.  **Yeni** öğesini seçin. Rapor tasarımcısı bir boş rapor tanımını açar. İlk göreviniz sütun tanımı oluşturmaktır.
3.  Sırasıyla **Dosya**, **Yeni** ve **Sütun Tanımı** düğmelerini tıklayarak yeni bir sütun tanımı oluşturun.
4.  **Sütun A**'da sütun türünü **DESC** olarak seçin.
5.  **Sütun B**'de sütun türünü **FD** olarak seçin.
6.  **Boyut Filtresi** alanını çift tıklayın.
7.  **Boyut** penceresinde, **Departman** sütununu çift tıklayın.
8.  İletişim penceresinin Bireysel veya aralık bölümünde, departmanların bir listesini görüntülemek için **Başlangıç** alanından **elips** öğesini tıklayın.
9.  Departman **022**, **Satış ve Pazarlama** seçimini yapın ve ardından **Tamam** öğesini tıklayın.
10. Departman 23-25 için 5 ile 8. adımlar arasındaki işlemleri tekrarlayın.
11. Her bir FD sütununun **Başlık 2** satırında, şu departman tanımlarını yazın:
    -   Sütun B – Satış ve Pazarlama
    -   Sütun C – Operasyonlar
    -   Sütun D – Finans
    -   Sütun E - IT

12. Sütun tanımını Yan Yana Departmanlar olarak kaydedin. Mevcut bir satır tanımını kullandığımız için, rapor tanımı şimdi yeni oluşturulan sütun tanımını ve mevcut satır tanımını kullanacak şekilde değiştirilebilir.
13. **Pencere** menüsünde rapor tanımını açmak için **Yeni Rapor Tanımı** öğesini seçin.
14. Satır tanımını **Gelir Beyanı – Varsayılan** olarak ve sütun tanımını **Yan Yana Departmanlar** olarak seçin.
15. Rapor tanımını **Yan Yana Departman Gelir Beyanı** olarak kaydedin.
16. Taban yılını **2012** olarak değiştirin.
17. Ayrıntı düzeyini **Finans, Hesap ve Hareket** olarak değiştirin.
18. Değişikliklerinizi **Kaydedin** ve **Oluştur** öğesini seçin. Raporun oluşturulması tamamlandıktan ve rapor açıldıktan sonra raporu inceleyebilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar
[Mali raporlama](../../financials/general-ledger/financial-reporting-getting-started.md) 
[Mali raporları görüntüle](../../financials/general-ledger/view-financial-reports.md) 
[Dynamics Mali Raporlama Blogu](http://blogs.msdn.com/b/dynamics_financial_reporting/)





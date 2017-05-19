---
title: "Retail Modern POS için resimleri ayarlama ve yönetme"
description: "Bu makalede, Retail Modern POS&quot;ta (MPOS) görüntülenen çeşitli varlıklar için resimlerin ayarlanmasını ve yönetilmesini sağlayan adımlar açıklanmaktadır."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 52851
ms.assetid: 5c21385e-64e0-4091-98fa-6a662eb33010
ms.search.region: global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: e144b05ec516d297c3cf81081936d306b9cb9026
ms.contentlocale: tr-tr
ms.lasthandoff: 04/26/2017


---

# <a name="set-up-and-manage-images-for-retail-modern-pos"></a>Retail Modern POS için resimleri ayarlama ve yönetme

[!include[banner](includes/banner.md)]


Bu makalede, Retail Modern POS'ta (MPOS) görüntülenen çeşitli varlıklar için resimlerin ayarlanmasını ve yönetilmesini sağlayan adımlar açıklanmaktadır.

<a name="setting-up-the-media-base-url-and-defining-media-templates-to-configure-the-format-for-image-urls"></a>Ortam temel URL'yi ayarlama ve resim URL'lerini biçimini yapılandırmak için ortam şablonları tanımlama
-------------------------------------------------------------------------------------------------

Perakende Modern POS (MPOS) içinde görünen resimlerin Microsoft Dynamics 365 for Operations - Perakende dışında harici olarak barındırılması gerekir. Genellikle, bunlar bir içerik yönetim sistemi, içerik iletici ağ (CDN) veya media server içinde barındırılır. MPOS sonra getirir ve resimleri ürünler ve katalogla gibi uygun varlıklar için hedef URL'ye erişerek görüntüler. Dışarıda barındırılan bu görüntüleri getirmek için MPOS görüntüler için doğru URL biçimi gerektirir. Görüntüler için gerekli URL biçimini kanal profilinde **ortam temel URL**değerini ayarlayarak ve her varlık için **medya şablon tanımla**işlevselliği kullanarak yapılandırabilirsiniz. Varlıkların alt kümesi için standart URL biçimi **Excel'de Düzenle** işlevini kullanarak üzerine yazabilirsiniz. **Önemli not:** Dynamics 365 for Operations'ın geçerli sürümünde, artık URL biçimini **Resim** MPOS için XML özniteliği kullanarak **varsayılan** varlıklar için öznitelik grubunda ayarlayamazsınız. Microsoft Dynamics AX 2012 R3'ü biliyorsanız ve Dynamics 365 for Operations'ın geçerli sürümünü kullanıyorsanız, görüntüleri belirlemek için her zaman yeni **Medya şablonu tanımla** işlevini kullandığınızdan emin olun **görüntü** özniteliğini **varsayılan** ürünleri de dahil olmak üzere herhangi bir varlık için öznitelik grubunda kullanmayın veya değiştirmeyin. Görüntüler için doğrudan **varsayılan**öznitelik grubunda yaptığınız değişiklikler yansıtılmaz. Gelecekteki bir sürümde bu seçenek devre dışı bırakılacak. Aşağıdaki yordamlarda, görüntüler için katalog varlığı için örnek olarak ayarlanmıştır. Bu yordamlar, doğru görüntü hedef yolunun ortak bir yol kullanan tüm katalog resimler için örtülü olarak ayarlandığını garanti olmasına yardımcı olur. Örneğin, dışarıdan, media server veya CDN ayarladıysanız ve görüntüleri belirli bir mağazanın MPOS içinde görünmesini istiyorsanız, **medya şablon tanımla** işlevselliği MPOS'nin görüntü arama ve alma yolunu ayarlamanıza yardımcı olur. **Not:** bu demo verileri Örneği için, perakende sunucusuna ortam sunucusu dağıtılır. Ancak, bunu Dynamics 365 for Operations dışında herhangi bir yerde sağlayabilirsiniz.

### <a name="set-up-the-media-base-url-for-a-channel"></a>Bir kanal için ortam temel URL'yi ayarlama

1.  Dynamics 365 for Operations HQ portal'ı açın.
2.  **Perakende ve ticaret** &gt; **Kanal kurulumu** &gt; **Kanal profilleri**'ne tıklayın. [![kanal-profili1](./media/channel-profile1.png)](./media/channel-profile1.png)
3.  Mağazanızın MPOS için kullandığı kanal profilinde **ortam temel URL** alanını media Server'ınızın veya CDN temel URL ile güncelleştirin. Temel URL farklı varlıkların tüm resim klasörleri tarafından paylaşılan URL'nin ilk parçasıdır.[![kanal-profili2](./media/channel-profile2.png)](./media/channel-profile2.png)

### <a name="define-the-media-template-for-an-entity"></a>Bir varlık için ortam şablonu tanımlama

1.  **Perakende ve ticaret** &gt; **Katalog Yönetimi** &gt; **Katalog resimleri**'ne tıklayın.
2.  **katalog resimleri** sayfasında eylem bölmesinde **medya şablon tanımla**'ya tıklayın. **medya şablon tanımla** iletişim kutusunda **varlık** alanında, **katalog** varsayılan olarak seçili olmalıdır.
3.  **medya yolu** hızlı sekmesinde, görüntü konumu kalan yolunu girin. Medya yolunu **LanguageID** değişken olarak destekler. Demo verileri için örneğin, medya sunucunuz için medya temel URL altındaki tüm katalog görüntüleri için bir **katalog** klasörü oluşturabilirsiniz (https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer). Sonra her dil için bir klasörünüz olabilir, en-US, fr-FR gibi ve her klasörün altında uygun görüntüleri kopyalayın. Çeşitli diller için farklı resimler yoksa **LanguageID** değişkenini klasör yapısında atlayabilir ve katalog görüntüleri içeren kataloglar klasörüne doğrudan işaret edebilirsiniz. **Not:** Dynamics AX geçerli sürümü katalog, ürün ve kategori varlıklar için **{LanguageId}** belirtecini destekler. ( **{LanguageID}** belirteci müşteri ve Çalışan varlıkları için Microsoft Dynamics AX 6.x'den bu yana etkili varolan standarda göre desteklenmez.)
4.  Görüntüler için dosya adı biçimi için katalog adı sabit kodlanmış hale getirilir ve değiştirilemez. Bu nedenle, MPOS bunları düzgün işleme sağlanmasına yardımcı olmak için uygun katalog adları olacak şekilde resimlerinizi yeniden adlandırın.
5.  **dosya uzantısı** alanında, sahip olduğunuz görüntülerin türüne bağlı olarak beklenen dosya adı uzantısı seçin. Örneğin, demo verileri için katalog resimler .jpg uzantısı olarak ayarlanır. (Resim adları Katalog adları sahip olacak biçimde de yeniden adlandırılır.)
6.  **Tamam**'a tıklayın.
7.  Resimler için ortam şablonunun doğru kaydedildiğini doğrulamak için **katalog resimleri** sayfasında, **medya şablonu tanımla**'yı yeniden tıklayın. Şablonu **medya şablon tanımla** iletişim kutusunu kapatmadan doğrulamak için **Excel için Resim URL'leri oluştur** hızlı sekmesini kullanabilirsiniz. Resim URL'si görünümünü denetleyin ve URL yukarıda belirtilen şablon standardıyla uyumlu olduğunu doğrulayın. **medya şablonu tanımla** iletişim kutusunda bu ortak URL yolunu kullanan tüm katalog görüntüleri için görüntü yolu artık örtülü olarak ayarlanmıştır. Bu URL yolu üzerine yazılmadığı sürece tüm katalog görüntüleri için geçerlidir. Kanal profilde tanımladığınız ortam temel URL'den görüntü yolunun ilk bölümü alınır. Yolun geri kalan bölümü medya şablonda tanımlanan yoldan alınır. Görüntü konumu tam URL'sini sağlamak üzere iki bölümden birleşir. Örneğin, demo verileri kataloğunda Fabrikam Temel katalog adı verilir. Bu nedenle, katalog adı ve şablonunda yapılandırılmış .jpg dosya adı uzantısı kullanır, böylece görüntü adı Fabrikam Bankası Catalog.jpg olması gerekir. Bu durumda, birleştirme sonrasında URL https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam Bankası Catalog.jpg olacaktır.
8.  MPOS görüntülere erişmek için bir şablon kullanabilecek şekilde kanal veritabanına yeni şablon itmek için Eşitleme işleri çalıştırın.
9.  Kanal tarafında katalog görüntülerde medya şablonunu güncelleştirmek için **Perakende BT** &gt; **Dağıtım planı**'nda **Katalog İşi 1150**'yi çalıştırdığınızdan emin olun.[![katalog1](./media/catalog1.png)](./media/catalog1.png)

## <a name="previewing-an-image-from-the-entity-level"></a>Varlık düzeyinde Görüntü Önizleme
1.  HQ'da varlık öğesi sayfasından medya şablondan türetilen resim URL'si kullanan resmi önizleyebilirsiniz. Bu örnek için uygun kataloğa gidin ve ardından Eylem Bölmesinde **Ortam** &gt; **Görüntüler**'e tıklayın. Farklı kanal profilleri olabilecek farklı mağazalar seçmek için açılır listeyi kullanın.
2.  örtülü medya şablonu Düzenlemek veya kaldırmak için **tanımla medya şablon** için iletişim kutusu **katalog resimleri** sayfası için geri dönmelisiniz.
3.  **Ekle** ve **Kaldır** düğmelerini örtülü bir şablonu temel alan ve belirli bir görüntü için kullanılan yolu el ile değiştirmek için kullanabilirsiniz. Daha fazla bilgi için bu makalenin ilerisindeki "varlık öğeleri için ortam şablon üzerine yazma" bölümüne bakın.
4.  Resmi önizlemeyi bitirdikten ve gereken değişiklikleri yaptıktan sonra uygun mağaza için MPOS örneğini başlatın ve katalog resimlerinin gösterilip gösterilmediğine bakın.[![katalog4](./media/catalog4.png)](./media/catalog4.png)

**Not:** , desteklenen tüm beş varlık için aynı yordamı kullanabilirsiniz: çalışan, müşteri, katalog, kategori ve ürün. "Katalog ürünleri" (katalog düzeyinde ayarlanmış ürünler) ve "Kanal Ürünleri" (kanal düzeyinde ayarlanmış ürünler) ürün varlığı için ayarlanan ortam şablonu kullanır. Ürünler ortam şablonu için ürün başına gösterilecek ürün görüntü sayısını seçebilirsiniz. Belirli bir ürün için varsayılan resim de ayarlayabilirsiniz. Bu şekilde, MPOS boş görüntüleri önleyebilir ve hangi resmin ürün öğesi için varsayılan görüntü olarak kullanıldığını denetlemeye yardımcı olabilirsiniz. Aşağıdaki örnekte, her ürünün beş görüntüsü vardır ve ilk resmi varsayılan görüntüsü olarak ayarlanır. Varyant ürünleri ana ürünlerle aynı şekilde davranılır. Görüntü dosyasının dosya adı, ürün numarasına dayanmalıdır. Dosya adı oluşturulurken bazı karakterler de kaçar. Bu nedenle, **Excel için Resim URL'leri oluştur** bölümü kullanarak dosya adını doğrulamak iyidir. [![ürünler](./media/prods.png)](./media/prods.png)  

## <a name="synchronization-jobs-to-send-a-media-template-to-the-channel-side"></a>Kanal tarafına medya şablon göndermek için Eşitleme işleri
Desteklenen beş varlığın tümü için (Çalışan, Müşteri, Katalog, Kategori ve Ürünler), resim ayarlamak için **Ortam şablonunu tanımla** iletişim penceresini ne zaman güncelleştirirseniz **Perakende BT** &gt; **Dağıtım planı**'ndan Katalog işi'ni (1150) çalıştırdığınızdan emin olun. Bu işi kanala eşitlenmiş ve MPOS tarafından kullanılan güncelleştirilmiş medya şablonu etkinleştirir. Aşağıdaki değişiklikleri yaptıktan sonra katalog işini (1150) çalıştır:

-   Katalog resim ortamı şablonunu **Katalog resimleri** &gt; **Medya şablonu tanımla**'dan güncelleştirirsiniz.
-   Çalışan resmi ortam şablonunu **Çalışan resimleri** &gt; **Ortam şablonu tanımla**'dan güncelleştirirsiniz.
-   Müşteri resmi ortam şablonunu **Müşteri resmi** &gt; **Ortam şablonu tanımla**'dan güncelleştirirsiniz.
-   Ürün resmi ortam şablonunu **Ürün resimleri** &gt; **Ortam şablonu tanımla**'dan güncelleştirirsiniz.
-   Kategori resim ortam şablonunu **Kategori resimleri** &gt; **Ortam şablonu tanımla**'dan güncelleştirirsiniz. Ayrıca kanal yayımlamanız gerekir.

## <a name="overwriting-the-media-template-for-entity-items"></a>Varlık öğeleri için ortam şablonu üzerine yazma
Önceki kısımda öğrendiğiniz gibi belirli bir varlık için ortam şablonu tek bir ortak yol destekler. Bu yol, yapılandırılmış ortam temel URL ve tanımlanan ortam yoluna dayanır. Ancak, çoğu durumda, bir satıcı bir varlık öğe alt kümesi için farklı kaynaklardan gelen görüntüleri kullanabilmek ister. Örneğin, bir mağaza bir katalog görüntü kümesi için kendi kendine barındırılan ortam sunucusu kullanır ancak başka bir küme için CDN URL'ler kullanır. Varlık düzeyinde varlık görüntüler için bir ortam şablonu esas alan resim URL'leri üzerine yazmak için Excel'de Düzenle ve **Önizleme** sayfasında el ile düzenlemek işlevini kullanabilirsiniz.

### <a name="overwrite-by-using-edit-in-excel"></a>Excel'de Düzenle'yi kullanarak üzerine yaz

1.  **Perakende ve ticaret** &gt; **Katalog Yönetimi** &gt; **Katalog resimleri**'ne tıklayın.
2.  **katalog resimleri** sayfasında **medya şablon tanımla**'ya tıklayın. **medya şablon tanımla** iletişim kutusunda **varlık** alanında, **katalog** seçili olmalıdır.
3.  **medya yolu** hızlı sekmesi üzerinde, görüntü konumuna dikkat edin.
4.  **Excel için Resim URL'leri oluştur** hızlı sekmesinde **Oluştur**'a tıklayın. **Önemli:** ortam şablonu değiştiğinde Excel'de Düzenle işlevini kullanmadan önce **Oluştur**'a tıklamanız gerekir. [![excel1](./media/excel1.jpg)](./media/excel1.jpg) Şimdi, son kaydedilmiş ortam şablonuna göre oluşturulan resim URL'lerinin önizlemesini görüyorsunuz. [![excel2](./media/excel2.png)](./media/excel2.png) **Not:** Excel kullanımı için oluşturulan URL'ler tanımlanan ortam şablonunun yolunu ve kurallarını kullanır. Bu kurallar, dosya adları için kuralları içerir. Dynamics AX dışında fiziksel görüntüleri ayarladıysanız ve daha önce tanımladığınız medya şablondan türetilen URL'lerden görüntüleri alınabilmesi beklenir. Bu türetilmiş URL'ler Excel'de düzenle işlevlerini kullanarak geçersiz kılabilirsiniz.
5.  **Excel'de düzenle**'ye tıklayın.
6.  Microsoft Excel çalışma sayfasını açtıktan sonra **düzenleme etkinleştir**'i ne zaman istenirse tıklayın.
7.  İstendiğinde, sağ bölmede **bu eklentiye güven**'e tıklayın ve eklenti yükleme tamamlamasını bekleyin. [![Bu eklentiye güven](./media/excel4.jpg)](./media/excel4.jpg)
8.  Oturum açmanız istendiğinde, HQ için oturum açmak amacıyla kullandığınız kimlik bilgilerini girin. [![Oturum açma komutu](./media/excel5.png)](./media/excel5.png)
9.  Oturum açtıktan sonra çeşitli katalog girdileri için resim URL'leri listesini görmek mümkün olacaktır.
10. Çeşitli varlık öğeler için resim URL'leri düzenleyin, ekleyin ve kaldırın.
11. Ürünler dışındaki tüm varlıklar için resim URL'leri üzerine yazabilirsiniz. Varolan resim URL'sini, resmin yeni hedef URL'sini kullanacak şekilde değiştirin ve dosya adını resim dosyası için yeni dosya adıyla güncelleştirin. Dosya adının kaydın benzersiz sağlanmasına yardımcı olmak için benzersiz olması gerekir. [![Excel'de resim URL'leri üzerine yaz](./media/excel6.jpg)](./media/excel6.jpg) **Not:** Excel'de düzenle işlevini veya varlık madde sayfasını kullanarak Ürünlerin varlıkları için resim URL'lerinin üzerine yazdığınız zaman, MPOS tüm ortam şablonu resim URL'lerini üzerine yazılan resim URL'leriyle birlikte her zaman gösterir.
12. Değişiklik yapmayı bitirdikten sonra **Excel'de Yayımla** tıklayarak yeni bir açık ilişki girişi oluşturun.
13. HQ'ya geri dönün ve **Tamam**'a tıklayın.
14. Varlık için uygun eşitleme işleri çalıştırın ve varlık sayfasında veya MPOS'de önizlemeyi denetleyin.

#### <a name="creating-new-records"></a>Yeni kayıtlar oluşturma

Excel'de yeni kayıtlar oluşturabilirsiniz. Ancak, doğru bilgileri sağlamaya özen gösterin. Örneğin, yeni bir katalog girişi oluşturmak için katalog kimliği ve Katalog adı doğru yazıldığından ve benzersiz bir dosya adı sağladığınızdan emin olun. Benzersiz bir dosya adı çok önemlidir, çünkü Excel kayıtlarında benzersizliği yayın sırasında doğrulanır. İlk ayrıntıları için yeni bir kayıt oluşturmak istediğiniz kataloğu kopyalayın ve kaydı kopyalayın. Bilgilerin geri kalanı aynı olacağı için yalnızca dosya adı ve URL güncelleştirmeniz gerekir. Ürün varlık öğeleri için yeni kayıtlar oluşturmak için aynı temel yordamı kullanın. Excel çalışma sayfasından yeni bir kayıt oluşturmak istediğiniz ürün için varolan bir kaydı kopyalayın ve ardından resim URL'si ve dosya adını değiştirin. Dosya adının benzersiz olduğundan emin olun.

#### <a name="deleting-an-existing-record"></a>Varolan bir kaydın silinmesi

Sadece üzerine yazılan resim URL'si kayıtları silinebilir. Resim silindikten ve eşitleme tamamlandıktan sonra görüntüyü artık **Önizleme** sayfası veya MPOS'de görünmez. Ortam şablonundan türetilen görüntü URL kayıtları silinemez, çünkü bu kayıtlar her zaman her seferinde ortam şablonundan türetilir.

### <a name="overwrite-from-the-entity-level-preview-page"></a>Varlık düzeyinde üzerine yaz Önizleme sayfası

Ürünleri dışındaki tüm varlıklar için **Önizleme** sayfasında varlık öğesi düzeyinde belirli bir varlık öğesi için görüntü URL'si üzerine yazabilirsiniz. Ürünler için "Katalog ürünleri" varlık sayfasını kullanabilirsiniz. Bu örnek, bir katalog görüntü üzerine nasıl yazıldığını gösterir.

1.  **Kataloglar** &gt; **Ortam** &gt; **Resimler**'e tıklayın ve güncelleştirilecek katalog resmini seçin.
2.  **Ekle**'ye tıklayın ve ortam şablon URL'si üzerine yazılacak resim URL'si girin.
3.  Katalog için bu görüntünün MPOS'da gösterilmesini istiyorsanız, varsayılan görüntü olarak ayarlayabilirsiniz.
4.  **Tamam** düğmesine tıklayın. Resim URL'si için bu katalog görüntü güncelleştirilir ve önizlemesi gösterilir. [![önizleme3](./media/preview3.png)](./media/preview3.png)
5.  Üzerindeki yazılan tüm üzerine resim URL'leri için Görüntü Önizlemesini **katalog resimleri** galeri sayfasında görebilirsiniz.

**[![önizleme-4](./media/preview-4.png)](./media/preview-4.png)Not:** Şu anda galeri ortam şablonu resim URL'leri için resim önizlemelerini göstermiyor. Kullanıcının açıkça bir URL üzerinden bu sayfaya sağlıyorsa, katalog, çalışan, müşteri ve kategori varlıklar için hangi resmin varsayılan olduğunu belirtmenizi öneririz, çünkü perakende sunucusu istemcileri Katalog, müşteri, çalışan ve kategori başına yalnızca bir resim gösterir. Kullanıcı varsayılan görüntü belirtmiyorsa, sistem varsayılan resmi belirler ve perakende hizmet arayıcısına (MPOS veya ticaret) gönderir.

### <a name="overwrite-the-image-url-for-catalog-product-images-from-the-preview-page"></a>Önizleme sayfasında katalog ürün resimleri için resim URL'si üzerine yazma

Önizleme sayfasında katalog ürün resimleri için resim URL'si üzerine yazmak için **Önizleme** sayfasını kullanmanız gerekir. Excel'de Düzenle işlevini kullanamazsınız.

1.  Ürün Kataloğu düzeyinde görüntüleri üzerine yazmak için bir katalog seçin ve ardından resmin üzerine yazılacak ürünü seçin.
2.  **Öznitelikler**'e tıklayın.
3.  Sonraki sayfada **Görüntü**'yü seçin ve sonra **Düzenle**'ye tıklayın. **Önizleme** sayfası kaydırıcı bir iletişim kutusu olarak açılır.
4.  **Ekle**'ye tıklayın ve resim URL'si üzerine yeni bir URL yazın.
5.  **Tamam** düğmesine tıklayın. Şimdi yeni resmin önizlemesini görebilir ve varsayılan resim olarak ayarlayabilirsiniz.

**[![kat3](./media/cat3.png)](./media/cat3.png)Not:** Kategori resim ilişkilendirme sonrasında kanalı yayımlamanız ve değişikliklerin kanal veritabanına yayımlanmasının sağlanmasına yardımcı olmak için Kanal işini çalıştırmanız gerekir.

## <a name="setting-up-images-to-appear-in-offline-mode-for-mpos"></a>MPOS için Çevrimdışı modunda görünür görüntüleri ayarlama
MPOS (Perakende sunucu veya ağ bağlantısı yok ve hareketler bir yerel çevrimdışı veritabanında depolandığında) (MPOS perakende sunucusuna bağlı olduğunda) Çevrimiçi modda veya çevrimdışı modda çalıştırabilirsiniz. MPOS çevrimdışı modda çalıştığında, perakende sunucu bağlantısı kesildiği için bu görüntüleri perakende sunucudan görüntülemek için harici görüntü sunucudan alamaz. Ancak, MPOS çevrimdışı modda çalıştığında görüntülenir, böylece görüntülerini ayarlayabilirsiniz.

### <a name="set-up-product-images-to-appear-in-offline-mode-for-mpos"></a>MPOS için Çevrimdışı modunda görünür ürün görüntüleri ayarlama

Çevrimdışı modda kullanılması gereken ürün resimleri gerekli fiziksel görüntü temel ürün yansımasına yükleyerek ayarlanabilir.

1.  **Ürün bilgileri yönetimi** &gt; **Ürünler** &gt; **Ürünler**'e tıklayın.
2.  Çevrimdışı bir yansıma için ayarlamak istediğiniz ürünü seçin.
3.  **düzenle**'ye tıklayın ve sonra sağ bölmeyi görüntülemek için sağ köşedeki oka tıklayın.
4.  **ürün resmi** hızlı sekmesinde **görüntü Değiştir**'e tıklayın ve seçilen ürün çevrimdışı modda kullanılmak üzere fiziksel resim yükleyin.
5.  Sayfayı kaydet ve kapatın
6.  MPOS çevrimiçi modunda çalışırken, HQ'da verileri çevrimdışı veritabanında en az bir kez gönderildiğinden emin olmak için katalog işlemini çalıştırın.
7.  MPOS çevrimdışı moduna geçirin. HQ belirli ürün için karşıya görüntü görmelisiniz. [![çevrimdışı1](./media/offline1.png)](./media/offline1.png)

 

### <a name="set-up-catalog-category-employee-and-customer-images-to-appear-in-offline-mode-for-mpos"></a>Katalog, kategori, çalışan ve müşteri görüntüleri Çevrimdışı modda MPOS için görünmesini Ayarla

Çevrimdışı modda kullanılması gereken katalog, kategori, çalışan ve müşteri görüntüleri gerekli görüntünün hedef bağlantı galeriye eklenerek ve seçilen varlık için varsayılan resim olarak görüntü ayarı ayarlanabilir.

1.  Kataloğa gidin ve Eylem Bölmesinde **Ortam** &gt; **Resimler**'e tıklayın.
2.  "**Varlık düzeyinde üzerine yaz Önizleme sayfası**" bölümündeki adımları takip ederek harici görüntü URL'si ekleyin.
3.  Kılavuzda listelenen görüntü karşısındaki onay kutusunu seçerek bu görüntüyü katalog için varsayılan resim olarak işaretleyin.
4.  Katalog işini çalıştırın. Bu görüntü şimdi MPOS'de o katalog için çevrimdışı görüntü olarak kullanılacaktır.
5.  Kategori, çalışan ve müşteri gibi diğer varlıklar için benzer bir işlem izleyin.

[![çevrimdışı2](./media/offline2.png)](./media/offline2.png)    





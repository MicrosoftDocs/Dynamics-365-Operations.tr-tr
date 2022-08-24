---
title: Modern POS (MPOS) için resimleri ayarlama ve yönetme
description: Bu makale, Modern POS (MPOS) içinde görüntülenen çeşitli varlıklar için görüntülerin ayarlanmasını ve yönetilmesini sağlayan adımlar açıklanmaktadır.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 52851
ms.assetid: 5c21385e-64e0-4091-98fa-6a662eb33010
ms.search.industry: Retail
ms.search.form: RetailChannelProfile, RetailMediaGallery, RetailImages,
ms.openlocfilehash: f282c163ef5a74283231492e499201c6d4619115
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287524"
---
# <a name="set-up-and-manage-images-for-modern-pos-mpos"></a>Modern POS (MPOS) için resimleri ayarlama ve yönetme

[!include [banner](includes/banner.md)]

Bu makale, Modern POS (MPOS) içinde görüntülenen çeşitli varlıklar için görüntülerin ayarlanmasını ve yönetilmesini sağlayan adımlar açıklanmaktadır.

## <a name="setting-up-the-media-base-url-and-defining-media-templates-to-configure-the-format-for-image-urls"></a>Ortam temel URL'yi ayarlama ve resim URL'lerini biçimini yapılandırmak için ortam şablonları tanımlama

Modern POS (MPOS) içinde görüntülenen resimlerin harici olarak, Commerce dışında barındırılması gerekir. Genellikle, bunlar bir içerik yönetim sistemi, içerik iletici ağ (CDN) veya media server içinde barındırılır. MPOS sonra getirir ve resimleri ürünler ve katalogla gibi uygun varlıklar için hedef URL'ye erişerek görüntüler. Dışarıda barındırılan bu görüntüleri getirmek için MPOS görüntüler için doğru URL biçimi gerektirir. Görüntüler için gerekli URL biçimini kanal profilinde **ortam temel URL** değerini ayarlayarak ve her varlık için **medya şablon tanımla** işlevselliği kullanarak yapılandırabilirsiniz. Varlıkların alt kümesi için standart URL biçimi **Excel'de Düzenle** işlevini kullanarak üzerine yazabilirsiniz.

> [!IMPORTANT]
> Commerce'in geçerli sürümünde, artık varlıklar için **Varsayılan** öznitelik grubundaki MPOS için **Resim** özniteliği XML'ini kullanarak URL biçimini ayarlayamazsınız. Microsoft Dynamics AX 2012 R3 ile aşina iseniz ve Commerce geçerli sürümünü kullanıyorsanız, görüntüleri belirlemek için her zaman yeni **Medya şablonu tanımla** işlevini kullandığınızdan emin olun. **görüntü** özniteliğini **varsayılan** ürünleri de dahil olmak üzere herhangi bir varlık için öznitelik grubunda kullanmayın veya değiştirmeyin. Görüntüler için doğrudan **varsayılan** öznitelik grubunda yaptığınız değişiklikler yansıtılmaz. Gelecekteki bir sürümde bu seçenek devre dışı bırakılacak.

Aşağıdaki yordamlarda, görüntüler için katalog varlığı için örnek olarak ayarlanmıştır. Bu yordamlar, doğru görüntü hedef yolunun ortak bir yol kullanan tüm katalog resimler için örtülü olarak ayarlandığını garanti olmasına yardımcı olur. Örneğin, dışarıdan, media server veya CDN ayarladıysanız ve görüntüleri belirli bir mağazanın MPOS içinde görünmesini istiyorsanız, **medya şablon tanımla** işlevselliği MPOS'nin görüntü arama ve alma yolunu ayarlamanıza yardımcı olur.

> [!NOTE]
> Bu demo verileri Örneği için, Commerce Scale Unit ortam sunucusu dağıtılır. Ancak, herhangi bir yerde Commerce dışında sağlayabilirsiniz.

### <a name="set-up-the-media-base-url-for-a-channel"></a>Bir kanal için ortam temel URL'yi ayarlama

1. Commerce HQ portalını açın.
2. **perakende ve ticaret** &gt; **kanal Kurulumu** &gt; **kanal profilleri** tıklayın.

    [![Gezinme.](./media/channel-profile1.png)](./media/channel-profile1.png)

3. Mağazanızın MPOS için kullandığı kanal profilinde **ortam temel URL** alanını media Server'ınızın veya CDN temel URL ile güncelleştirin. Temel URL farklı varlıkların tüm görüntü klasörleri tarafından paylaşılan URL'nin ilk parçasıdır.

    [![Kanal profilleri sayfası.](./media/channel-profile2.png)](./media/channel-profile2.png)

### <a name="define-the-media-template-for-an-entity"></a>Bir varlık için ortam şablonu tanımlama

1. **perakende ve ticaret** &gt; **Katalog Yönetimi** &gt; **katalog resimleri**'ne tıklayın.
2. **katalog resimleri** sayfasında eylem bölmesinde **medya şablon tanımla**'ya tıklayın. **medya şablon tanımla** iletişim kutusunda **varlık** alanında, **katalog** varsayılan olarak seçili olmalıdır.
3. **medya yolu** hızlı sekmesinde, görüntü konumu kalan yolunu girin. Medya yolunu **LanguageID** değişken olarak destekler. Örneğin demo verilerinde medya sunucunuz için medya temel URL'si altındaki tüm katalog resimlerine ait bir **Kataloglar** klasörü oluşturabilirsiniz (`https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer`). Sonra her dil için bir klasörünüz olabilir, en-US, fr-FR gibi ve her klasörün altında uygun görüntüleri kopyalayın. Çeşitli diller için farklı resimler yoksa **LanguageID** değişkenini klasör yapısında atlayabilir ve katalog görüntüleri içeren kataloglar klasörüne doğrudan işaret edebilirsiniz.

    > [!NOTE]
    > Commerce'in geçerli sürümü Katalog, Ürün ve Kategori varlıkları için **{LanguageId}** belirtecini destekliyor. ( **{LanguageID}** belirteci müşteri ve Çalışan varlıkları için Microsoft Dynamics AX 6.x'den bu yana etkili varolan standarda göre desteklenmez.)

4. Görüntüler için dosya adı biçimi için katalog adı sabit kodlanmış hale getirilir ve değiştirilemez. Bu nedenle, MPOS bunları düzgün işleme sağlanmasına yardımcı olmak için uygun katalog adları olacak şekilde resimlerinizi yeniden adlandırın.
5. **dosya uzantısı** alanında, sahip olduğunuz görüntülerin türüne bağlı olarak beklenen dosya adı uzantısı seçin. Örneğin, demo verileri için katalog resimler .jpg uzantısı olarak ayarlanır. (Resim adları Katalog adları sahip olacak biçimde de yeniden adlandırılır.)
6. **Tamam**'a tıklayın.
7. Resimler için ortam şablonunun doğru kaydedildiğini doğrulamak için **katalog resimleri** sayfasında, **medya şablonu tanımla**'yı yeniden tıklayın. Şablonu **medya şablon tanımla** iletişim kutusunu kapatmadan doğrulamak için **Excel için Resim URL'leri oluştur** hızlı sekmesini kullanabilirsiniz. Resim URL'si görünümünü denetleyin ve URL yukarıda belirtilen şablon standardıyla uyumlu olduğunu doğrulayın. **medya şablonu tanımla** iletişim kutusunda bu ortak URL yolunu kullanan tüm katalog görüntüleri için görüntü yolu artık örtülü olarak ayarlanmıştır. Bu URL yolu üzerine yazılmadığı sürece tüm katalog görüntüleri için geçerlidir. Kanal profilde tanımladığınız ortam temel URL'den görüntü yolunun ilk bölümü alınır. Yolun geri kalan bölümü medya şablonda tanımlanan yoldan alınır. Görüntü konumu tam URL'sini sağlamak üzere iki bölümden birleşir. Örneğin, demo verileri kataloğunda Fabrikam Temel katalog adı verilir. Bu nedenle, katalog adı ve şablonunda yapılandırılmış .jpg dosya adı uzantısı kullanır, böylece görüntü adı Fabrikam Bankası Catalog.jpg olması gerekir. Bu durumda birleştirmeden sonra URL `https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam Base Catalog.jpg` olarak değişir.
8. MPOS görüntülere erişmek için bir şablon kullanabilecek şekilde kanal veritabanına yeni şablon itmek için Eşitleme işleri çalıştırın.
9. Kanal tarafında katalog görüntülerde medya şablonunu güncelleştirmek için **Retail ve Commerce BT** &gt; **Dağıtım zamanlaması**'nda **Katalog İşi 1150** çalıştırdığınızdan emin olun.

    [![Ortam şablonu tanımla iletişim kutusu.](./media/catalog1.png)](./media/catalog1.png)

## <a name="previewing-an-image-from-the-entity-level"></a>Varlık düzeyinde Görüntü Önizleme

1. HQ'da varlık öğesi sayfasından medya şablondan türetilen resim URL'si kullanan resmi önizleyebilirsiniz. Bu örnek için uygun kataloğa gidin ve ardından Eylem Bölmesinde **Ortam** &gt; **Görüntüler**'e tıklayın. Farklı kanal profilleri olabilecek farklı mağazalar seçmek için açılır listeyi kullanın.
2. örtülü medya şablonu Düzenlemek veya kaldırmak için **tanımla medya şablon** için iletişim kutusu **katalog resimleri** sayfası için geri dönmelisiniz.
3. **Ekle** ve **Kaldır** düğmelerini örtülü bir şablonu temel alan ve belirli bir görüntü için kullanılan yolu el ile değiştirmek için kullanabilirsiniz. Daha fazla bilgi için bu makalenin ilerisindeki [Varlık öğeleri için ortam şablon üzerine yazma](#overwriting-the-media-template-for-entity-items) bölümüne bakın.
4. görüntüyü önizleme ve gereken değişiklikleri yaptıktan sonra uygun mağaza için MPOS örneğini başlatın ve Katalog görüntülerinin gösterilip gösterilmediğine bakın.

    [![Resimler iletişim kutusu.](./media/catalog4.png)](./media/catalog4.png)

> [!NOTE]
> Desteklenen tüm beş varlık için aynı yordamı kullanabilirsiniz: çalışan, müşteri, katalog, kategori ve ürün. "Katalog ürünleri" (katalog düzeyinde ayarlanmış ürünler) ve "Kanal Ürünleri" (kanal düzeyinde ayarlanmış ürünler) ürün varlığı için ayarlanan ortam şablonu kullanır. Ürünler ortam şablonu için ürün başına gösterilecek ürün görüntü sayısını seçebilirsiniz. Belirli bir ürün için varsayılan resim de ayarlayabilirsiniz. Bu şekilde, MPOS boş görüntüleri önleyebilir ve hangi resmin ürün öğesi için varsayılan görüntü olarak kullanıldığını denetlemeye yardımcı olabilirsiniz. Aşağıdaki örnekte, her ürünün beş görüntüsü vardır ve ilk resmi varsayılan görüntüsü olarak ayarlanır. Varyant ürünleri ana ürünlerle aynı şekilde davranılır. Görüntü dosyasının dosya adı, ürün numarasına dayanmalıdır. Dosya adı oluşturulurken bazı karakterler de kaçar. Bu nedenle, **Excel için Resim URL'leri oluştur** bölümü kullanarak dosya adını doğrulamak iyidir. Bu makalenin sonraki bölümünde bulunan [Excel'de Düzenle'yi kullanarak üzerine yazma](#overwrite-by-using-edit-in-excel) konusuna bakın.

## <a name="synchronization-jobs-to-send-a-media-template-to-the-channel-side"></a>Kanal tarafına medya şablon göndermek için Eşitleme işleri

Desteklenen beş varlığın tümü için (Çalışan, Müşteri, Katalog, Kategori ve Ürünler), resim ayarlamak için **Ortam şablonunu tanımla** iletişim penceresini ne zaman güncelleştirirseniz **Retail ve Commerce BT** &gt; **Dağıtım planı**'ndan Katalog işi'ni (1150) çalıştırdığınızdan emin olun. Bu işi kanala eşitlenmiş ve MPOS tarafından kullanılan güncelleştirilmiş medya şablonu etkinleştirir. Aşağıdaki değişiklikleri yaptıktan sonra katalog işini (1150) çalıştır:

- Katalog resim ortamı şablonunu **Katalog resimleri** &gt; **Medya şablonu tanımla**'dan güncelleştirirsiniz.
- Çalışan resmi ortam şablonunu **Çalışan resimleri** &gt; **Ortam şablonu tanımla**'dan güncelleştirirsiniz.
- Müşteri resmi ortam şablonunu **Müşteri resmi** &gt; **Ortam şablonu tanımla**'dan güncelleştirirsiniz.
- Ürün resmi ortam şablonunu **Ürün resimleri** &gt; **Ortam şablonu tanımla**'dan güncelleştirirsiniz.
- Kategori resim ortam şablonunu **Kategori resimleri** &gt; **Ortam şablonu tanımla**'dan güncelleştirirsiniz. Ayrıca kanal yayımlamanız gerekir.

## <a name="overwriting-the-media-template-for-entity-items"></a>Varlık öğeleri için ortam şablonu üzerine yazma

Önceki kısımda öğrendiğiniz gibi belirli bir varlık için ortam şablonu tek bir ortak yol destekler. Bu yol, yapılandırılmış ortam temel URL ve tanımlanan ortam yoluna dayanır. Ancak, çoğu durumda, bir satıcı bir varlık öğe alt kümesi için farklı kaynaklardan gelen görüntüleri kullanabilmek ister. Örneğin, bir mağaza bir katalog görüntü kümesi için kendi kendine barındırılan ortam sunucusu kullanır ancak başka bir küme için CDN URL'ler kullanır. Varlık düzeyinde varlık görüntüler için bir ortam şablonu esas alan resim URL'leri üzerine yazmak için Excel'de Düzenle ve **Önizleme** sayfasında el ile düzenlemek işlevini kullanabilirsiniz.

### <a name="overwrite-by-using-edit-in-excel"></a>Excel'de Düzenle'yi kullanarak üzerine yaz

1. **perakende ve ticaret** &gt; **Katalog Yönetimi** &gt; **katalog resimleri**'ne tıklayın.
2. **katalog resimleri** sayfasında **medya şablon tanımla**'ya tıklayın. **medya şablon tanımla** iletişim kutusunda **varlık** alanında, **katalog** seçili olmalıdır.
3. **medya yolu** hızlı sekmesi üzerinde, görüntü konumuna dikkat edin.
4. **Excel için Resim URL'leri oluştur** hızlı sekmesinde **Oluştur**'a tıklayın.

    > [!IMPORTANT]
    > Ortam şablonu değiştiğinde Excel'de Düzenle işlevini kullanmadan önce **Oluştur**'a tıklamanız gerekir.

    Şimdi, son kaydedilmiş ortam şablonuna göre oluşturulan resim URL'lerinin önizlemesini görürsünüz.

    [![Oluştur seçildikten sonra Excel için Resim URL'leri oluştur hızlı sekmesi.](./media/excel2.png)](./media/excel2.png)

    > [!NOTE]
    > Excel kullanımı için oluşturulan URL'ler tanımlanan medya şablonunun yolunu ve kurallarını kullanır. Bu kurallar, dosya adları için kuralları içerir. Fiziksel görüntüleri Commerce dışında ayarlamış olmanız ve daha önce tanımladığınız medya şablonundan türetilen URL'lerden görüntülerin alınabilmesi beklenir. Bu türetilmiş URL'ler Excel'de düzenle işlevlerini kullanarak geçersiz kılabilirsiniz.

5. **Excel'de düzenle**'ye tıklayın.
6. Microsoft Excel çalışma sayfasını açtıktan sonra **Düzenleme etkinleştir**'i ne zaman istenirse tıklayın.
7. İstendiğinde, sağ bölmede **bu eklentiye güven**'e tıklayın ve eklenti yükleme tamamlamasını bekleyin.

    [![Bu eklentiye güven.](./media/excel4.jpg)](./media/excel4.jpg)

8. Oturum açmanız istendiğinde, HQ için oturum açmak amacıyla kullandığınız kimlik bilgilerini girin.

    [![Oturum açma komutu.](./media/excel5.png)](./media/excel5.png)

9. Oturum açtıktan sonra çeşitli katalog girdileri için resim URL'leri listesini görmek mümkün olacaktır.
10. Çeşitli varlık öğeler için resim URL'leri düzenleyin, ekleyin ve kaldırın.
11. Ürünler dışındaki tüm varlıklar için resim URL'leri üzerine yazabilirsiniz. Varolan resim URL'sini, resmin yeni hedef URL'sini kullanacak şekilde değiştirin ve dosya adını resim dosyası için yeni dosya adıyla güncelleştirin. Dosya adının kaydın benzersiz sağlanmasına yardımcı olmak için benzersiz olması gerekir.

    [![Excel'de resim URL'leri üzerine yazma.](./media/excel6.jpg)](./media/excel6.jpg)

    > [!NOTE]
    > Excel işlevlerini veya varlık madde sayfa düzenleme kullanarak Ürün varlıkları için resim URL'lerinin üzerine yazdığınızda, MPOS her zaman üzerine yazılan resim URL'leri ile birlikte tüm medya şablon görüntü URL'lerini gösterir.

12. Değişiklik yapmayı bitirdikten sonra **Excel'de Yayımla** tıklayarak yeni bir açık ilişki girişi oluşturun.
13. HQ'ya geri dönün ve **Tamam**'a tıklayın.
14. Varlık için uygun eşitleme işleri çalıştırın ve varlık sayfasında veya MPOS'de önizlemeyi denetleyin.

#### <a name="creating-new-records"></a>Yeni kayıtlar oluşturma

Excel'de yeni kayıtlar oluşturabilirsiniz. Ancak, doğru bilgileri sağlamaya özen gösterin. Örneğin, yeni bir katalog girişi oluşturmak için katalog kimliği ve Katalog adı doğru yazıldığından ve benzersiz bir dosya adı sağladığınızdan emin olun. Benzersiz bir dosya adı çok önemlidir, çünkü Excel kayıtlarında benzersizliği yayın sırasında doğrulanır. İlk ayrıntıları için yeni bir kayıt oluşturmak istediğiniz kataloğu kopyalayın ve kaydı kopyalayın. Bilgilerin geri kalanı aynı olacağı için yalnızca dosya adı ve URL güncelleştirmeniz gerekir. Ürün varlık öğeleri için yeni kayıtlar oluşturmak için aynı temel yordamı kullanın. Excel çalışma sayfasından yeni bir kayıt oluşturmak istediğiniz ürün için varolan bir kaydı kopyalayın ve ardından resim URL'si ve dosya adını değiştirin. Dosya adının benzersiz olduğundan emin olun.

#### <a name="deleting-an-existing-record"></a>Varolan bir kaydın silinmesi

Sadece üzerine yazılan resim URL'si kayıtları silinebilir. Resim silindikten ve eşitleme tamamlandıktan sonra görüntüyü artık **Önizleme** sayfası veya MPOS'de görünmez. Ortam şablonundan türetilen görüntü URL kayıtları silinemez, çünkü bu kayıtlar her zaman her seferinde ortam şablonundan türetilir.

### <a name="overwrite-from-the-entity-level-preview-page"></a>Varlık düzeyinde üzerine yaz Önizleme sayfası

Ürünleri dışındaki tüm varlıklar için **Önizleme** sayfasında varlık öğesi düzeyinde belirli bir varlık öğesi için görüntü URL'si üzerine yazabilirsiniz. Ürünler için "Katalog ürünleri" varlık sayfasını kullanabilirsiniz. Bu örnek, bir katalog görüntü üzerine nasıl yazıldığını gösterir.

1. **Kataloglar** &gt; **Ortam** &gt; **Resimler**'e tıklayın ve güncelleştirilecek katalog resmini seçin.
2. **Ekle**'ye tıklayın ve ortam şablon URL'si üzerine yazılacak resim URL'si girin.
3. Katalog için bu görüntünün MPOS'da gösterilmesini istiyorsanız, varsayılan görüntü olarak ayarlayabilirsiniz.
4. **Tamam** düğmesine tıklayın. Resim URL'si için bu katalog görüntü güncelleştirilir ve önizlemesi gösterilir.

    [![Yeni görüntü iletişim kutusunda güncelleştirilen URL.](./media/preview3.png)](./media/preview3.png)

5. Üzerindeki yazılan tüm üzerine resim URL'leri için Görüntü Önizlemesini **katalog resimleri** galeri sayfasında görebilirsiniz.

    [![Katalog görüntü galerisi sayfası.](./media/preview-4.png)](./media/preview-4.png)

> [!NOTE]
> Galeri şablon görüntü URL Görüntü Önizlemeleri ortam şu anda göstermiyor. Kullanıcının açıkça bir URL üzerinden bu sayfaya sağlıyorsa, katalog, çalışan, müşteri ve kategori varlıklar için hangi resmin varsayılan olduğunu belirtmenizi öneririz, çünkü Commerce Scale Unit istemcileri Katalog, müşteri, çalışan ve kategori başına yalnızca bir resim gösterir. Kullanıcı varsayılan görüntü belirtmiyorsa, sistem varsayılan resmi belirler ve Commerce hizmet arayıcısına (MPOS veya ticaret) gönderir.

### <a name="overwrite-the-image-url-for-catalog-product-images-from-the-preview-page"></a>Önizleme sayfasında katalog ürün resimleri için resim URL'si üzerine yazma

Önizleme sayfasında katalog ürün resimleri için resim URL'si üzerine yazmak için **Önizleme** sayfasını kullanmanız gerekir. Excel'de Düzenle işlevini kullanamazsınız.

1. Ürün Kataloğu düzeyinde görüntüleri üzerine yazmak için bir katalog seçin ve ardından resmin üzerine yazılacak ürünü seçin.
2. **Öznitelikler**'e tıklayın.
3. Sonraki sayfada **Görüntü**'yü seçin ve sonra **Düzenle**'ye tıklayın. **Önizleme** sayfası kaydırıcı bir iletişim kutusu olarak açılır.
4. **Ekle**'ye tıklayın ve resim URL'si üzerine yeni bir URL yazın.
5. **Tamam** düğmesine tıklayın. Şimdi yeni resmin önizlemesini görebilir ve varsayılan resim olarak ayarlayabilirsiniz.

    [![Yeni görüntü iletişim kutusunda görüntü önizleme.](./media/cat3.png)](./media/cat3.png)

> [!NOTE]
> Kategori görüntü ilişkilendirme sonrasında kanal yayımlamanız ve değişiklikleri kanal veritabanına yayımlanan sağlanmasına yardımcı sağlamak için Kanal işini çalıştırmanız gerekir.

## <a name="setting-up-images-to-appear-in-offline-mode-for-mpos"></a>MPOS için Çevrimdışı modunda görünür görüntüleri ayarlama

MPOS (Commerce Scale Unit veya ağ bağlantısı yok ve hareketler bir yerel çevrimdışı veritabanında depolandığında) (MPOS Commerce Scale Unit bağlı olduğunda) Çevrimiçi modda veya çevrimdışı modda çalıştırabilirsiniz. MPOS çevrimdışı modda çalıştığında, bağlantısı kesildiği için bu görüntüleri Commerce Scale Unit'den görüntülemek için harici görüntü sunucudan alamaz. Ancak, MPOS çevrimdışı modda çalıştığında görüntülenir, böylece görüntülerini ayarlayabilirsiniz.

### <a name="set-up-product-images-to-appear-in-offline-mode-for-mpos"></a>MPOS için Çevrimdışı modunda görünür ürün görüntüleri ayarlama

Çevrimdışı modda kullanılması gereken ürün resimleri gerekli fiziksel görüntü temel ürün yansımasına yükleyerek ayarlanabilir.

1. **Ürün bilgileri yönetimi** &gt; **Ürünler** &gt; **Ürünler**'e tıklayın.
2. Çevrimdışı bir yansıma için ayarlamak istediğiniz ürünü seçin.
3. **düzenle**'ye tıklayın ve sonra sağ bölmeyi görüntülemek için sağ köşedeki oka tıklayın.
4. **ürün resmi** hızlı sekmesinde **görüntü Değiştir**'e tıklayın ve seçilen ürün çevrimdışı modda kullanılmak üzere fiziksel resim yükleyin.
5. Sayfayı kaydet ve kapatın
6. MPOS çevrimiçi modunda çalışırken, HQ'da verileri çevrimdışı veritabanında en az bir kez gönderildiğinden emin olmak için katalog işlemini çalıştırın.
7. MPOS çevrimdışı moduna geçirin. HQ belirli ürün için karşıya görüntü görmelisiniz.

    [![Çevrimdışı modda ürün resmi.](./media/offline1.png)](./media/offline1.png)

### <a name="set-up-catalog-category-employee-and-customer-images-to-appear-in-offline-mode-for-mpos"></a>Katalog, kategori, çalışan ve müşteri görüntüleri Çevrimdışı modda MPOS için görünmesini Ayarla

Çevrimdışı modda kullanılması gereken katalog, kategori, çalışan ve müşteri görüntüleri gerekli görüntünün hedef bağlantı galeriye eklenerek ve seçilen varlık için varsayılan resim olarak görüntü ayarı ayarlanabilir.

1. Kataloğa gidin ve Eylem Bölmesinde **Ortam** &gt; **Resimler**'e tıklayın.
2. [Varlık düzeyinde üzerine yaz Önizleme sayfası](#overwrite-from-the-entity-level-preview-page) bölümündeki adımları takip ederek harici görüntü URL'si ekleyin.
3. Kılavuzda listelenen görüntü karşısındaki onay kutusunu seçerek bu görüntüyü katalog için varsayılan resim olarak işaretleyin.
4. Katalog işini çalıştırın. Bu görüntü şimdi MPOS'de o katalog için çevrimdışı görüntü olarak kullanılacaktır.
5. Kategori, çalışan ve müşteri gibi diğer varlıklar için benzer bir işlem izleyin.

    [![Çevrimdışı görüntü.](./media/offline2.png)](./media/offline2.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

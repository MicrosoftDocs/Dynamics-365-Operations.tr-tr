---
title: İş belgesi yönetiminde Microsoft Office stili kullanıcı arabirimi (video içerir)
description: Bu konu, Elektronik raporlama (ER) çerçevesinin İş belgesi yönetimi özelliğindeki yeni kullanıcı arabiriminin nasıl kullanılacağı hakkında bilgi vermektedir.
author: v-anamir
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e33830e2147d92ad5ee53ad11da55a50613b8ef9
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8074753"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>İş belgesi yönetiminde Microsoft Office stili kullanıcı arabirimi

[!include [banner](../includes/banner.md)]

İş belgesi yönetimi iş kullanıcılarının Microsoft Office 365 hizmeti veya uygun Microsoft Office masaüstü uygulamasını kullanarak iş belgesi şablonlarını düzenlemesini sağlar. Düzenlemeler tasarım değişiklikleri veya yeni dağıtımlar içerebilir ya da kullanıcılar kaynak kodunu değiştirmeden ek veri eklemek için yer tutucular ekleyebilirler. İş belgesi yönetimiyle nasıl çalışılacağı hakkında daha fazla bilgi için bkz. [İş belgesi yönetimine genel bakış](er-business-document-management.md).

Yeni kullanıcı arabirimi (UI) daha net ve kullanımı daha rahat. **İşletme belgesi** alanında, yalnızca geçerli [etkin](tasks/er-configuration-provider-mark-it-active-2016-11.md) [sağlayıcının](general-electronic-reporting.md#Provider) sahip olduğu ve geçerli Dynamics 365 Finance örneğinde bulunan şablonlar gösterilir. Önceki kullanıcı arabiriminde, **Şablon** sekmesi herhangi bir sağlayıcı için kullanılabilen tüm şablonları listeliyordu. Aynı role sahip herhangi bir kullanıcı tarafından oluşturulan ve düzenlenen tüm şablonları da gösteriyordu.

**İşletme belgesi yönetimi** çalışma alanındaki **Yeni belge** düğmesini, başka bir sağlayıcı tarafından sağlanan ve geçerli Finance örneğinde bulunan [Elektronik raporlama (ER)](general-electronic-reporting.md) biçim [yapılandırmasında](general-electronic-reporting.md#Configuration) şablon oluşturmak ve düzenlemek veya Excel çalışma kitabından yeni bir şablon yüklemek için kullanabilirsiniz. Ayrıca, sürüm 10.0.25 ve sonraki sürümlerde, [Genel depoda](general-electronic-reporting.md#Repository) depolanan ER biçimli yapılandırmada şablon oluşturmak ve düzenlemek için **Yeni belge** düğmesini kullanabilirsiniz.

Bu konudaki örneklerde, etkin sağlayıcı Contoso'dur ve bunu Microsoft tarafından sağlanan bir şablonu temel alan bir şablon oluşturmak için kullanırsınız. Alternatif olarak, kendi şablonunuzu Excel biçiminde karşıya yükleyerek bir şablon oluşturabilirsiniz.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWAVQg]

[İşletme belgesi yönetimini kullanarak yeni bir işletme belgesi oluşturma](https://youtu.be/gAIYl-mM_pw) videosu (yukarıda gösterilen) YouTube'daki [Finans ve Operasyon oynatma listesine](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) eklenmiştir.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>İş belgesi yönetiminde yeni belge kullanıcı arabirimini kullanıma açma

İş belgesi yönetiminde yeni belge kullanıcı arabirimini kullanmaya başlamak için,**Özellik yönetimi** çalışma alanındaki **İş belgesi yönetimi için Office benzeri arabirim deneyimi** özelliğini açmanız gerekir.

Bu özelliği tüm tüzel kişilikler için açmak üzere bu adımları izleyin.

1. **Özellik yönetimi** çalışma alanında, **Tümü** sekmesinde, listeden **İş belgesi yönetimi için Office benzeri arabirim deneyimi**'ni seçin.
2. Seçili özelliği açmak için **Şimdi etkinleştir**'i seçin.
3. Yeni özelliğe erişmek için sayfayı yenileyin.

## <a name="add-or-activate-a-provider"></a>Sağlayıcı ekleme veya etkinleştirme

Bir iş belgesinin her şablonu, belirli bir yapılandırma sağlayıcısına ait olarak işaretlenmiş bir ER biçimi yapılandırmasında depolanır. Yeni bir şablon oluşturduğunuzda, şablonu tutmak için yeni bir ER biçimi yapılandırması oluşturulur. Bu nedenle, bu yapılandırma için bir sağlayıcı tanımlanmalıdır. Bu amaçla ER çerçevesinin etkin sağlayıcısı kullanılır. ER'de sağlayıcı yoksa, bir sağlayıcı oluşturabilirsiniz. *Etkin* sağlayıcı yoksa, varolan sağlayıcılardan birini etkinleştirebilirsiniz. Sağlayıcı eklemek veya etkinleştirmek için bir iletişim kutusu gerektiğinde açılır, ancak yeni bir şablon eklemeye başlarsınız.

### <a name="add-a-new-provider"></a>Yeni sağlayıcı ekle

Yeni sağlayıcı oluşturmak için **Yapılandırma sağlayıcısı** iletişim kutusunda şu adımları izleyin:

1.  **Yapılandırma sağlayıcısını seçin** sekmesinde, **Ad** alanına yeni sağlayıcı adını girin.
2.  **Internet adresi** alanına, yeni sağlayıcının internet adresini (URL) girin. 
3.  **Tamam**'ı seçin.

    ![İşletme Belgesi Yönetimi'nde yeni bir sağlayıcı oluşturma.](./media/bdm_create_provider.png)

Eklenen sağlayıcı otomatik olarak etkinleştirilir.

### <a name="activate-a-provider"></a>Sağlayıcıyı etkinleştirme

Bir sağlayıcıyı etkinleştirmek için **Yapılandırma sağlayıcısı** iletişim kutusunda şu adımları izleyin:

1.  **Yapılandırma sağlayıcısını seçin** sekmesinde, **Yapılandırma sağlayıcısı** alanında sağlayıcıyı seçin.
2.  **Tamam**'ı seçin.

    ![İşletme Belgesi Yönetimi'nde bir sağlayıcıyı etkinleştirme.](./media/bdm_choose_provider.png)

Seçili sağlayıcı etkinleştirilir.

> [!NOTE]
> Her İşletme belgesi yönetimi şablonu, sağlayıcıyı yapılandırma yazarı olarak adlandıran bir ER biçim yapılandırmasında bulunur. Bu nedenle, her şablon için etkin bir sağlayıcı gereklidir.

## <a name="edit-a-template-that-is-owned-by-another-provider"></a>Başka bir sağlayıcının sahip olduğu şablonu düzenleme

Bu örnek, başka bir sağlayıcı tarafından sağlanan ve geçerli Finance örneğinde bulunan ER biçim yapılandırmasında şablon oluşturmak ve düzenlemek için **İşletme belgesi yönetimi** çalışma alanında **Yeni belge** düğmesinin nasıl kullanılacağını gösterir. Bu örnekte, etkin sağlayıcı, Microsoft tarafından sağlanan ER biçimi yapılandırmasını kullanan Contoso'dur. **Yeni belge**'yi seçtikten sonra, **Yeni şablon oluştur** sayfasındaki **Seç** sekmesi, geçerli sağlayıcının ve diğer sağlayıcıların sahip olduğu geçerli Finance örneğinin tüm şablonlarını gösterir. Bir şablon seçerek açın. Daha sonra şablonun yeni bir düzenlenebilir kopyasını oluşturabilirsiniz. Düzenlenen şablon, otomatik olarak oluşturulan yeni bir ER biçimi yapılandırmasında depolanır.

1. **İş belgesi yönetimi** çalışma alanında **Yeni belge**'yi seçin.

    ![İş belgesi yönetimi çalışma alanı.](./media/BDM_overview_new_template1.png)

2. **Yeni şablon oluştur** sayfasında, **Seç** sekmesinde, şablon olarak kullanılacak belgeyi seçin ve sonra **Belge oluştur**'u seçin.

    ![İş belgeleri iletişim kutusu.](./media/BDM_overview_new_template2.png)

3. Yeni iletişim kutusunda, **Başlık** alanında, başlığı gerektiği gibi değiştirin. Başlık metni, otomatik olarak oluşturulan yeni ER biçimi yapılandırmasını adlandırmak için kullanılır. Bu yapılandırmanın taslak sürümü (**Müşteri FTI raporu (GER) kopyası**) düzenlenen şablonu içerir ve bu ER biçimini geçerli kullanıcı için çalıştırmak üzere kullanılır. Temel ER biçimi yapılandırmasındaki özgün şablon, diğer kullanıcıların tümü için bu ER biçimini çalıştırmada kullanılacaktır.
4. **Ad** alanında, düzenlenebilir şablonun otomatik olarak oluşturulacak ilk revizyonunun adını değiştirin.
5. **Yorum** alanında, düzenlenebilir şablonun otomatik olarak oluşturulacak revizyonuna için yorumları güncelleştirin.
6. Düzenleme işleminin başlangıcını onaylamak için **Tamam**'ı seçin.

    ![Belge oluşturma iletişim kutusu.](./media/BDM_overview_new_template3.png)

## <a name="upload-a-template-that-uses-an-existing-excel-workbook"></a>Varolan Excel çalışma kitabını kullanan şablonu yükleme

Bu örnek, kullanılabilir Excel çalışma kitabına dayalı olarak ER biçimli bir yapılandırmada şablon oluşturmak ve düzenlemek için **İşletme belgesi yönetimi** çalışma alanında **Yeni belge** düğmesinin nasıl kullanılacağını gösterir. Bu örnekte, etkin sağlayıcı Contoso'dur ve Microsoft tarafından sağlanan ER [veri modeli](er-overview-components.md#data-model-component) ve ER [model eşlemesi](er-overview-components.md#model-mapping-component) yapılandırmalarını kullanırsınız. **Yeni belge**'yi seçtikten sonra, **Yeni şablon oluştur** sayfasında **Yükle** sekmesini seçin. Burada, Excel çalışma kitabı yüklemesinin ayrıntılarını belirtebilirsiniz. Excel çalışma kitabını yükledikten sonra, düzenleme için açılan bir işletme belgesi şablonuna dönüştürülür. Düzenlenen şablon, otomatik olarak oluşturulan yeni bir ER biçimi yapılandırmasında depolanır.

Bir şablonu karşıya yüklemeden önce gerekli bilgileri sağlamak için aşağıdaki adımları izleyin.

1. **İş belgesi yönetimi** çalışma alanında **Yeni belge**'yi seçin.
2. **Yeni şablon oluştur** sayfasında, **Yükle** sekmesindeki **Şablon** sekmesinde şablon olarak kullanmak istediğiniz Excel dosyasını bulmak ve seçmek için **Gözat**'ı seçin. **Şablon** bölümünde, **Başlık** ve **Açıklama** alanları otomatik olarak doldurulur. Bunlar otomatik olarak oluşturulan yeni ER biçimi yapılandırmasının adını ve açıklamasını belirtir. Bu alanları istediğiniz şekilde düzenleyebilirsiniz.
3. **Belge Türü** bölümünde, **Ad** alanında iş belgesinin türünü belirtin. Bu değer, doğru veri kaynağını (ER model konfigürasyonu) aramak için kullanılacaktır.

    ![Şablon oluştur sayfasının Yükle sekmesindeki Şablon sekmesi.](./media/BDM_overview_new_UI_import_21.jpg)

4. **Veri kaynağı** sekmesinde, **Filtre** hızlı sekmesinde **Filtreyi uygula**'yı seçin. **Veri kaynağı** bölümünde, **Ad** alanı otomatik olarak doldurulur veya el ile bir değer seçebilirsiniz. Uygun veri kaynağı adını ad, açıklama, ülke/bölge kodu ve iş belgesi türü ile aramak için filtre kullanabilirsiniz.

    ![Yeni şablon oluştur sayfasının Yükle sekmesindeki veri kaynağı sekmesi.](./media/BDM_overview_new_UI_import_31.jpg)

    > [!NOTE]
    > **Filtre** hızlı sekmesi, doğru veri kaynağını (ER model konfigürasyonu) aramak için kullanılır. Karşıya yüklediğiniz belge için en uygun veri kaynağını bulmak üzere tüm filtre alanlarını düzenleyebilirsiniz.
    > 
    > **Filtre** hızlı sekmesindeki koşullar **VEYA** koşulları olarak kullanılır.

5. **Eşleme** sekmesinde **Otomatik algıla**'yı seçin. **Kök tanımı** alanı otomatik olarak doldurulur veya el ile bir değer seçebilirsiniz. Bu sekme, şablondan ve modelden gelen öğelerin bitiş eşlemesini gösterir.

    ![Yeni şablon oluştur sayfasının Yükle sekmesindeki Eşleme sekmesi.](./media/BDM_overview_new_UI_import_41.jpg)

    > [!NOTE]
    > **Şablon yapısı** bölümündeki eşleme, kullanıcının dilindeki ve şablondaki hücre adındaki etiket veya açıklamaların tam eşleşmesini kullanır.

6. Bir şablon oluşturmak ve düzenleme işlemini başlatmak istediğinizi onaylamak için **Belge oluştur** seçeneğini belirleyin.

Daha fazla bilgi için bkz. [İş belgesi yönetimine genel bakış](er-business-document-management.md).

## <a name="upload-a-template-from-the-global-repository"></a>Genel depoya bir şablon yükleme

Bu örnek, Microsoft tarafından sağlanan genel depoda bulunan ER biçim yapılandırmasında şablon oluşturmak ve düzenlemek için **İşletme belgesi yönetimi** çalışma alanında **Yeni belge** düğmesinin nasıl kullanılacağını gösterir. Bu örnekte, etkin sağlayıcı, Microsoft tarafından sağlanan ER biçimi yapılandırmasını kullanan Contoso'dur. **Yeni belge**'yi seçtikten sonra, **Yeni şablon oluştur** sayfasındaki **Genel depodan içeri aktar** sekmesi, Genel depoda depolanan ancak geçerli Finance örneğinde olmayan tüm işletme belgesi şablonlarını gösterir. Bir şablon seçtikten sonra, şablon, yeni bir düzenlenebilir kopya oluşturmak için Genel depodan geçerli Finance örneğine içeri aktarılır. Düzenlenen şablon, otomatik olarak oluşturulan yeni bir ER biçimi yapılandırmasında depolanır.

1. **İş belgesi yönetimi** çalışma alanında **Yeni belge**'yi seçin.
2. **Yeni şablon oluştur** sayfasında, **Genel depodan içeri aktar** sekmesinde, şablon olarak kullanılacak belgeyi seçin ve sonra **Belge oluştur**'u seçin.

    ![Yeni şablon oluştur sayfasındaki Genel depodan içeri aktar sekmesi.](./media/BDM_overview_new_template22.png)

3. İleti kutusunda, seçili belgeyi Global depodan geçerli Finance örneğine içeri aktarmak istediğinizi onaylamak için **Evet**'i seçin. Yetkilendirme istenirse ekrandaki yönergeleri izleyin.
4. Yeni iletişim kutusunda, **Başlık** alanında, başlığı gerektiği gibi değiştirin. Başlık metni, otomatik olarak oluşturulan yeni ER biçimi yapılandırmasını adlandırmak için kullanılır. Bu yapılandırmanın taslak sürümü (**Tahsilat mektubu notu (Excel) metni**) düzenlenmiş şablonu içerir ve geçerli kullanıcı için bu ER biçimini çalıştırmak amacıyla kullanılır. Temel ER biçimi yapılandırmasındaki özgün şablon, diğer kullanıcıların tümü için bu ER biçimini çalıştırmada kullanılacaktır.
5. **Ad** alanında, düzenlenebilir şablonun otomatik olarak oluşturulacak ilk revizyonunun adını değiştirin.
6. **Yorum** alanında, düzenlenebilir şablonun otomatik olarak oluşturulacak revizyonuna için yorumları güncelleştirin.
7. Düzenleme işleminin başlangıcını onaylamak için **Tamam**'ı seçin.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

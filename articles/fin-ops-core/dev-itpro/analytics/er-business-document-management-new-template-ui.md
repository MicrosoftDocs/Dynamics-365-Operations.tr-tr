---
title: İş belgesi yönetiminde Microsoft Office stili kullanıcı arabirimi
description: Bu konu, Elektronik raporlama (ER) çerçevesinin İş belgesi yönetimi özelliğindeki yeni kullanıcı arabiriminin nasıl kullanılacağı hakkında bilgi vermektedir.
author: v-anamir
ms.date: 04/12/2021
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
ms.openlocfilehash: 4d4c256b2384f14fd8439c4a9263860f504113de369142d0913a2538f1f0939f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737963"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>İş belgesi yönetiminde Microsoft Office stili kullanıcı arabirimi

[!include [banner](../includes/banner.md)]

İş belgesi yönetimi iş kullanıcılarının Microsoft 365 hizmeti veya uygun Microsoft Office masaüstü uygulamasını kullanarak iş belgesi şablonlarını düzenlemesini sağlar. Düzenlemeler tasarım değişiklikleri veya yeni dağıtımlar içerebilir ya da kullanıcılar kaynak kodunu değiştirmeden ek veri eklemek için yer tutucular ekleyebilirler. İş belgesi yönetimiyle nasıl çalışılacağı hakkında daha fazla bilgi için bkz. [İş belgesi yönetimine genel bakış](er-business-document-management.md).

Yeni kullanıcı arabirimi (UI) daha net ve kullanımı daha rahat. **İş belgesi** alanı, yalnızca, geçerli sağlayıcı için kullanılabilen şablonları gösterir. Önceki kullanıcı arabiriminde, **Şablon** sekmesi sağlayıcılar için kullanılabilir olan tüm şablonları listeliyordu. Aynı role sahip herhangi bir kullanıcı tarafından oluşturulan ve düzenlenen tüm şablonları da gösteriyordu.

**Yeni belge** düğmesini, başka bir sağlayıcı tarafından sağlanan bir Elektronik raporlama (ER) biçimi yapılandırmasında şablon oluşturmak ve düzenlemek için kullanabilirsiniz. Bu konudaki örnekte sağlayıcı Microsoft'tur. Alternatif olarak, kendi şablonunuzu Excel biçiminde karşıya yükleyerek bir şablon oluşturabilirsiniz.


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

[İş belgesi yönetimi kullanarak yeni iş belgesi oluşturma](https://youtu.be/gAIYl-mM_pw) videosu (yukarıda gösterilir) YouTube'daki [Finance and Operations oynatma listesine](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) eklenmiştir.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>İş belgesi yönetiminde yeni belge kullanıcı arabirimini kullanıma açma

İş belgesi yönetiminde yeni belge kullanıcı arabirimini kullanmaya başlamak için,**Özellik yönetimi** çalışma alanındaki **İş belgesi yönetimi için Office benzeri arabirim deneyimi** özelliğini açmanız gerekir.

Bu özelliği tüm tüzel kişilikler için açmak üzere bu adımları izleyin.

1. **Özellik yönetimi** çalışma alanında, **Tümü** sekmesinde, listeden **İş belgesi yönetimi için Office benzeri arabirim deneyimi**'ni seçin.
2. Seçili özelliği açmak için **Şimdi etkinleştir**'i seçin.
3. Yeni özelliğe erişmek için sayfayı yenileyin.

## <a name="edit-templates-that-are-owned-by-other-providers"></a>Sahibi diğer sağlayıcılar olan düzenleme şablonları

1. **İş belgesi yönetimi** çalışma alanında **Yeni belge**'yi seçin.

    ![İş belgesi yönetimi çalışma alanı.](./media/BDM_overview_new_template1.png)

2. **Seç** sekmesinde, şablon olarak kullanılacak belgeyi ve ardından **Belge oluştur**'u seçin.

    ![İş belgeleri iletişim kutusu.](./media/BDM_overview_new_template2.png)

3. Yeni iletişim kutusunda, **Başlık** alanında, başlığı gerektiği gibi değiştirin. Başlık metni, otomatik olarak oluşturulan yeni ER biçimi yapılandırmasını adlandırmak için kullanılır. Bu yapılandırmanın taslak sürümü (**Müşteri FTI raporu (GER) kopyası**) düzenlenen şablonu içerir ve bu ER biçimini geçerli kullanıcı için çalıştırmak üzere kullanılır. Temel ER biçimi yapılandırmasındaki özgün şablon, diğer kullanıcıların tümü için bu ER biçimini çalıştırmada kullanılacaktır.
4. **Ad** alanında, düzenlenebilir şablonun otomatik olarak oluşturulacak ilk revizyonunun adını değiştirin.
5. **Yorum** alanında, düzenlenebilir şablonun otomatik olarak oluşturulacak revizyonuna için yorumları güncelleştirin.
6. Düzenleme işleminin başlangıcını onaylamak için **Tamam**'ı seçin.

    ![Belge oluşturma iletişim kutusu.](./media/BDM_overview_new_template3.png)

**Yeni belge** düğmesi, kullanıcıların başka bir sağlayıcı tarafından sağlanan bir ER biçimi yapılandırmasında şablon oluşturmak ve düzenlemek için kullanılır. Bu örnekte sağlayıcı Microsoft'tur. **Yeni belge**'yi seçtiğiniz zaman, sahibi geçerli ve diğer sağlayıcılar olan tüm şablonları görüntüleyebilirsiniz. Siz şablonu seçtikten sonra şablon düzenleme için açılır. Düzenlenen şablon daha sonra otomatik olarak oluşturulan yeni bir ER biçim yapılandırması içinde depolanır.

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a>Varolan Excel biçimini kullanan bir şablonu karşıya yükleme
Bir şablonu karşıya yüklemeden önce gerekli bilgileri sağlamak için aşağıdaki adımları izleyin.

1. **İş belgesi yönetimi** çalışma alanında **Yeni belge**'yi seçin.

    ![İş belgesi yönetimi çalışma alanı.](./media/BDM_overview_new_template1.png)
    
2. **Yeni şablon oluştur** sayfasında, **Yükle** sekmesindeki **Şablon** sekmesinde şablon olarak kullanmak istediğiniz Excel dosyasını bulmak ve seçmek için **Gözat**'ı seçin. **Şablon** bölümünde, **Başlık** ve **Açıklama** alanları otomatik olarak doldurulur. Bunlar otomatik olarak oluşturulan yeni ER biçimi yapılandırmasının adını ve açıklamasını belirtir. Bu alanları istediğiniz şekilde düzenleyebilirsiniz.
3. **Belge Türü** bölümünde, **Ad** alanında iş belgesinin türünü belirtin. Bu değer, doğru veri kaynağını (ER model konfigürasyonu) aramak için kullanılacaktır.

    ![Şablon sekmesi.](./media/BDM_overview_new_UI_import_21.jpg)

4. **Veri kaynağı** sekmesinde, **Filtre** hızlı sekmesinde **Filtreyi uygula**'yı seçin. **Veri kaynağı** bölümünde, **Ad** alanı otomatik olarak doldurulur veya el ile bir değer seçebilirsiniz. Uygun veri kaynağı adını ad, açıklama, ülke/bölge kodu ve iş belgesi türü ile aramak için filtre kullanabilirsiniz.

    ![Veri kaynağı sekmesi.](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > **Filtre** hızlı sekmesi, doğru veri kaynağını (ER model konfigürasyonu) aramak için kullanılır. Karşıya yüklediğiniz belge için en uygun veri kaynağını bulmak üzere tüm filtre alanlarını düzenleyebilirsiniz.
    > 
    > **Filtre** hızlı sekmesindeki koşullar **VEYA** koşulları olarak kullanılır.
    
5. **Eşleme** sekmesinde **Otomatik algıla**'yı seçin. **Kök tanımı** alanı otomatik olarak doldurulur veya el ile bir değer seçebilirsiniz. Bu sekme, şablondan ve modelden gelen öğelerin bitiş eşlemesini gösterir.

    ![Eşleme sekmesi.](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > **Şablon yapısı** bölümündeki eşleme, kullanıcının dilindeki ve şablondaki hücre adındaki etiket veya açıklamaların tam eşleşmesini kullanır.

6. Bir şablon oluşturmak ve düzenleme işlemini başlatmak istediğinizi onaylamak için **Belge oluştur** seçeneğini belirleyin.

Daha fazla bilgi için bkz. [İş belgesi yönetimine genel bakış](er-business-document-management.md).

Elektronik raporlamada bir sağlayıcı yoksa, oluşturabilirsiniz. Etkin sağlayıcı yoksa, etkinleştirmeyi seçebilirsiniz.

- Sağlayıcı oluşturmak için, **Ad** alanında sağlayıcının adını değiştirin, **İnternet adresi** alanında yeni sağlayıcının internet adresini güncelleştirin ve onaylamak için **Tamam**'ı seçin.

    ![BDM'de yeni sağlayıcı oluşturma.](./media/bdm_create_provider.png)
    
- Mevcut sağlayıcıyı etkinleştirmek için **Yapılandırma sağlayıcısı** alanında sağlayıcının adını seçin ve ardından sağlayıcıyı etkin olarak ayarlamak için **Tamam**'ı seçin.

    ![BDM'de sağlayıcıyı etkinleştirme.](./media/bdm_choose_provider.png)

> [!NOTE]
> Her BDM şablonu yapılandırmanın yazarı olarak sağlayıcıya başvurur. Bu nedenle şablon için etkin bir sağlayıcı gereklidir.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

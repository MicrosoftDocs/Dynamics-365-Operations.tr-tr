---
title: İş belgesi yönetimine genel bakış
description: Bu konu, ER çerçevesinin iş belge yönetimi özelliğinin nasıl kullanılacağı hakkında bilgi sağlar.
author: NickSelin
manager: AnnBe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERSecurityAccessEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e657ffbad88aeb9fd238112954f5555496ac329
ms.sourcegitcommit: fcc4596eeadac5dfe9a3242afa49b9b1c0c96575
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/15/2020
ms.locfileid: "4740968"
---
# <a name="business-document-management-overview"></a>İş belgesi yönetimine genel bakış

[!include [banner](../includes/banner.md)]

[Elektronik raporlama (ER)](general-electronic-reporting.md) çerçevesi kullanan iş kullanıcıları toplam belgelerin biçimini çeşitli ülkelerin/bölgelerin yasal gereksinimlerine uygun şekilde yapılandırmanıza olanak tanır. Kullanıcılar, oluşturulan belgelere hangi uygulama verilerinin yerleştirileceğini belirtmek için veri akışını da tanımlayabilir. ER çerçevesi, önceden tanımlanmış şablonları kullanarak Microsoft Office (Excel çalışma kitapları veya Word belgeleri) giden belgeleri biçimler. Şablon, gerekli belgelerin oluşturulması sırasında veri akışına uygun olarak, gerekli verilerle doldurulur. Konfigüre edilen her biçim, belirli giden belgeler oluşturmak üzere bir ER çözümünün parçası olarak yayımlanabilir. Bu, farklı giden belgeler oluşturmak için kullanabileceğiniz şablonlar içerebilen bir ER biçim yapılandırması ile temsil edilir. İş kullanıcıları gerekli iş belgelerini yönetmek için bu çerçeveyi kullanabilir.

**İş belgesi yönetimi** ER çerçevesinin üzerine kurulmuştur ve iş kullanıcılarının Microsoft 365 servisini veya uygun Microsoft Office masaüstü uygulamasını kullanarak iş belgesi şablonlarını düzenlemesini sağlar. Belgelerde yapılan düzenlemeler, iş belge tasarımlarının değiştirilmesini ve kaynak kodu değişiklikleri ve Yeni dağıtımlar olmaksızın ek veriler için yer tutucular eklemeyi içerir. İş belgelerinin şablonlarını güncelleştirmek için ER çerçevesi gerekli bilgisine sahip değildir.

> [!NOTE]
> Iş belgesi yönetiminin sipariş, fatura vb. gibi iş belgelerini üretmek için kullanılan şablonları değiştirmenize olanak verdiğini unutmayın. Bir şablon değiştirildiğinde ve yeni bir sürümü yayımlanmışsa, bu sürüm gerekli iş belgelerini oluşturmak için kullanılır. İş belgesi yönetimi, zaten oluşturulmuş iş belgelerini değiştirmek için kullanılamaz.

## <a name="supported-deployments"></a>Desteklenen dağıtımlar

Şu anda, Iş belgesi yönetimi özelliği yalnızca bulut dağıtımları için geçerlidir. Bu özellik şirket içi dağıtımınız için önemliyse, [Fikirler](https://experience.dynamics.com/ideas/) sitesine geri bildirim vererek bize bildirin.

## <a name="supported-microsoft-office-applications"></a>Desteklenen Microsoft Office uygulamaları

Masaüstü uygulamaları kullanarak Microsoft Office şablonları Excel veya Word biçimlerinde düzenlemek üzere iş belge yönetimini kullanmak için Microsoft Office 2010 veya daha ileri bir sürümü yüklemiş olmanız gerekir. Bu, bulut ve şirket içi dağıtımlarda desteklenir.

Microsoft 365 uygulamalarını kullanarak şablonları Excel veya Word biçimlerinde düzenlemek üzere iş belge yönetimini kullanmak için web aboneliği için Microsoft 365 Office sahibi olmanız gerekir. Bu, bulut dağıtımında desteklenir.

## <a name="business-document-availability"></a>İş belgesi uygunluğu

2019 Ekim sürümü için planlanan tüm raporların tam listesi için bkz. [ Word ve Excel'de yapılandırılabilir iş belgeleri raporlaması](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details).

2020 Ekim sürümü için planlanan tüm raporların tam listesi için bkz. [Yapılandırılabilir iş belgeleri - Word şablonları](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-finance/configurable-business-documents-word-templates).

Gelecekteki sürümlerde daha fazla rapor kullanılabilir olacak. Ek raporlarla ilgili özel bildirimler ayrı olarak gönderilecektir. Şu anda kullanılabilir raporların listesini nasıl inceleyebileceğinizi öğrenmek için aşağıdaki [Yapılandırılabilir iş belgelerini desteklemek için Finance'te yayınlanan ER yapılandırmalarının listesi](#list-of-configurations-cbd) bölümüne bakın.

Bu özellik hakkında daha fazla bilgi edinmek için bu konudaki örneği tamamlayın.

## <a name="configure-er-parameters"></a>ER parametrelerini yapılandırma

İş belgesi yönetimi ER çerçevesinin üzerine oluşturulduğundan, İş belge yönetimiyle çalışmaya başlamak için ER parametrelerini konfigüre etmelisiniz. Bunu yapmak için ER parametrelerini [Elektronik raporlama (ER) çerçevesini yapılandırma](electronic-reporting-er-configure-parameters.md)'da açıklandığı şekilde ayarlamanız gerekir. Ayrıca, [Yapılandırma sağlayıcıları oluştur ve bunları ektin olarak işaretle](tasks/er-configuration-provider-mark-it-active-2016-11.md)'de gösterildiği gibi yeni bir yapılandırma sağlayıcısı eklemeniz gerekir.

![ER Çalışma Alanı](./media/BDM-Overview-ERSetting.png)

## <a name="import-er-solutions"></a>ER çözümlerini çe aktar

Bu prosedürde verilen örnekte, örnek ER yapılandırmaları kullanılmıştır. İş belgesi yönetimi kullanılarak düzenlenebilen iş belgesi şablonlarını içeren ER yapılandırmalarını geçerli Dynamics 365 Finance kurulumunuzda içe aktarmanız gerekir. Bu prosedürü tamamlamak için aşağıdaki dosyaları indirin ve ardından yerel olarak depolayın.

**Örnek ER müşteri faturalama çözümü**

| Dosya                                      | İçerik |
|-------------------------------------------|---------|
| Customer invoicing model.version.2.xml    | [ER verisi modeli yapılandırması](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Customer FTI report (GER).version.2.3.xml | [Serbest metin fatura ER biçim yapılandırması](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

**Örnek ER ödeme çekleri çözümü**

| Dosya                                     | İçerik |
|------------------------------------------|---------|
| Model for cheques.version.10.xml         | [ER verisi modeli yapılandırması](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Cheques printing format.version.10.9.xml | [Ödeme çeki ER biçim yapılandırması](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

**Örnek ER dış ticaret çözümü**

| Dosya                             | İçerik |
|----------------------------------|---------|
| Intrastat model.version.1.xml    | [ER verisi modeli yapılandırması](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Intrastat report.version.1.9.xml | [Intrastat kontrol raporu ER biçim yapılandırması](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

Her bir dosyayı içe aktarmak için aşağıdaki yordamı kullanın. İlgili ER *biçimi* yapılandırmasını içe aktarmadan önce, yukarıdaki tablolardaki her bir er çözümünün ER *veri modeli* yapılandırmasını içe aktarın.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar** sayfasını açın.
2. Sayfanın üstündeki **Döviz**'i seçin.
3. **XML dosyasından yükle**'yi seçin.
4. Gerekli XML dosyasını yüklemek için **Gözat**'ı seçin.
5. Yapılandırmanın içe aktarma işlemini onaylamak için **Tamam**'ı seçin.

![Yapılandırmayı içeri aktarmayı onaylayan ER yapılandırmaları sayfası](./media/BDM-Overview-ERSolutions.png)

Alternatif olarak, resmi olarak yayımlanan ER biçimi yapılandırmalarını Microsoft Dynamics Lifecycle Service (LCS) uygulamasından içe aktarabilirsiniz. Örneğin, bu prosedürü tamamlamak için **Serbest metin faturası (Excel)** ER biçimi yapılandırmasının en son sürümünü içe aktarabilirsiniz. İlgili ER veri modeli ve ER model eşleme yapılandırmaları otomatik olarak içe aktarılır.

![LCS paylaşılan varlık kitaplığı içerik sayfası](./media/BDM-Overview-SharedAssetLibrary.png)

ER yapılandırmalarının içe aktarılması hakkında daha fazla bilgi içi bkz: [ER yapılandırması yaşam döngüsünü yönetme](general-electronic-reporting-manage-configuration-lifecycle.md).

## <a name="enable-business-document-management"></a>İş belgesi yönetimini etkinleştirme

Iş belge yönetimini başlatmak için **Özellik Yönetimi** çalışma alanını açmanız ve **İş belge yönetimi** özelliğini etkinleştirmeniz gerekir.

Tüm yasal varlıklar için iş belgesi yönetim işlevlerini etkinleştirmek üzere aşağıdaki yordamı kullanın.

1. **Özellik yönetimi** çalışma alanını açın.
2. **Yeni** sekmesinde, listeden **İş belge yönetimi** özelliğini seçin.
3. Seçili özelliği açmak için **Şimdi etkinleştir**'i seçin.
4. Yeni özelliğe erişmek için sayfayı yenileyin.

> [!NOTE]
> İş belgesi yönetimi'nde yeni belge kullanıcı arabiriminin kullanılması hakkında daha fazla bilgi için bkz. [İş belgesi yönetimi'nde yeni belge kullanıcı arabirimi](er-business-document-management-new-template-ui.md).

![Özellik yönetimi çalışma alanı](./media/BDM-Overview-FMEnabling.png)

Yeni özellikleri etkinleştirme hakkında daha fazla bilgi için [Özellik yönetimine genel bakış](../../fin-ops/get-started/feature-management/feature-management-overview.md)'a bakın.

## <a name="configure-parameters"></a>Parametrelerini yapılandırma

Iş belgesi yönetimi için temel parametreleri ayarlamak üzere aşağıdaki bölümlerdeki bilgileri kullanın.

### <a name="prerequisites-for-parameter-setup"></a>Parametre kurulumu için Önkoşullar

Iş belge yönetimini kurmadan önce, gerekli belge türünü belge yönetim çerçevesi olarak ayarlamanız gerekir. Bu belge türü, ER raporları için şablon olarak kullanılan Office biçimlerindeki (Excel ve Word) belgelerin geçici bir depolanmasını belirtmek için kullanılır. Geçici depolama şablonu Office Masaüstü uygulamaları kullanılarak düzenlenebilir.

Bu belge türü için aşağıdaki öznitelik değerleri seçilmelidir.

| Öznitelik adı | Öznitelik değeri |
|----------------|-----------------|
| Sınıf          | Dosya iliştir     |
| Grup          | Dosya            |
| Konum       | SharePoint      |

Gerekli belge yönetimi parametrelerinin ve belge türlerinin nasıl ayarlanacağı hakkında bilgi için bkz: [Belge yönetimini yapılandır](../../fin-ops/organization-administration/configure-document-management.md).

![Belge yönetimi belge türünü ayarla](./media/BDM-Overview-DMSetting.png)

### <a name="set-up-parameters"></a><a name="SetupBdmParameters"></a>Parametreleri ayarlayın

Temel İş belgesi yönetim parametreleri **İş belgesi parametreleri** sayfasında ayarlanabilir. Yalnızca belirli kullanıcılar sayfaya erişebilir. Bunların arasında yer alanlar:

- **Sistem Yöneticisi** rolüne atanan kullanıcılar.
- Vergi gerçekleştirmek üzere konfigüre edilen herhangi bir role atanan kullanıcılar **Iş belgesi yönetimi parametrelerinin bakımı** (AOT adı **ERBDMaintainParameters**).

Tüm tüzel kişilikler için temel parametreleri ayarlamak üzere aşağıdaki yordamı kullanın.

1. **İş belgesi parametreleri** sayfasına erişimi olan bir kullanıcı olarak oturum açın.
2. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **İş belgesi yönetimi** \> **İş belgesi yönetimi parametreleri**'ne gidin.
3. **İş belgesi parametreleri** sayfasında, **Ekler** sekmesinde, **SharePoint belge türü** alanında, şablonları ofis formatlarında geçici olarak depolamak için kullanılacak belge tipini tanımlayan Office Masaüstü uygulamaları kullanılarak düzenlenir. 

> [!NOTE]
> Yalnızca bir SharePoint yerleşim kullanılarak konfigüre edilen belge türleri bu parametre için kullanılabilir.

![Iş belgesi yönetim parametrelerinin kurulumu](./media/BDM-Overview-BDMSetting.png)

Seçili belge türü şirkete özgüdür ve seçilen belge türü konfigüre edilen şirketteki İş Belge yönetiminde kullanıcının çalıştığı zaman kullanılır. Kullanıcı, başka bir şirkette İş belgesi yönetimi ile çalışırken, bu şirket için yapılandırılmadıysa, seçilen aynı belge türü kullanılacaktır. Bir belge türü konfigüre edildiğinde, **SharePoint belge türü** alanında seçilen yerine kullanılacak.

> [!NOTE]
> **SharePoint belge türü** parametresi, Microsoft Excel veya Word kullanarak düzenlenebilen şablonlar için geçici depolama yeri olarak bir SharePoint klasörü tanımlar. Bu Office masaüstü uygulamalarını şablon düzenleme amacıyla kullanmayı planlıyorsanız bu parametreyi ayarlamanız gerekir. Daha fazla bilgi için bkz. [Office masaüstü uygulamasında şablon düzenleme](#EditInOfficeDesktopApp). Şablonu yalnızca Microsoft 365'teki işlevleri kullanarak değiştirmeyi planlıyorsanız bu parametreyi boş bırakabilirsiniz. Daha fazla bilgi için bkz. [Microsoft 365'te şablon düzenleme](#EditInOffice365).

## <a name="configure-access-permissions"></a>Erişim izinlerini yapılandır

Varsayılan olarak, İş belgesi yönetimi izinlerine erişim özelliği etkin olmadığında, İş belge yönetimi çalışma alanına erişimi olan her Kullanıcı, tüm ER çözüm şablonlarını görür. İş belgesi yönetimi çalışma alanı yalnızca, ER biçim yapılandırmalarında bulunan ve bir **İş belgesi türü** etiketi tarafından işaretlenen şablonları gösterir.

![İş belgesi türü etiketi olan ER yapılandırmaları sayfası](./media/BDM-Overview-ERFormatTags.png)

İş belgesi yönetimi çalışma alanında bulunan şablonların listesi, erişim izinleri yapılandırılarak kısıtlanabilir. Farklı iş etki alanları (işlevsel alanlar) için iş belgeleri oluşturmak amacıyla farklı şablonlar kullanıldığında ve İş belge yönetimi çalışma alanında düzenleme yapmak üzere belirli kullanıcıların farklı şablonlara erişmesine izin vermek istiyorsanız, bu durum önemli olabilir.

İş belgesi yönetimi erişim izinleri, erişim izinlerinin **Yapılandırıcısı üzerinde ayarlanabilir**. Yalnızca aşağıdaki kullanıcılar sayfaya erişebilir:

- **Sistem Yöneticisi** rolüne atanan kullanıcılar.
- Söz konusu görevi gerçekleştirmek üzere konfigüre edilen başka herhangi bir role atanan kullanıcılar için **iş belgesi şablonlarına erişim izinleri konfigüre edin** (AOT adı **ERBDTemplatesSecurity**).

Tüm yasal varlıklar için iş belgesi yönetim izinlerini kurmak üzere aşağıdaki yordamı kullanın.

1. **Erişim izinleri yapılandırıcısı** sayfasına erişimi olan bir kullanıcı olarak oturum açın.
2. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **İş belgesi yönetimi** \> **Erişim izinlerini yönet**'e gidin.

    İş belgesi yönetimi için erişim izinlerinin kullanımının etkin olmadığını bildiren bir uyarıların bildirimine dikkat edin.

    ![Iş belgesi yönetimi erişim izinleri sayfası](./media/BDM-Overview-TemplatesAccess1.png)

    Bu ayarla, **İş belgesi şablonlarını yönet** (AOT adı **ERBDManageTemplates**) görevini gerçekleştirecek bir güvenlik rolüne atanan her Kullanıcı, iş belge yönetimini açabilir ve kullanılabilir tüm şablonları düzenleyebilir.

    Aşağıdaki grafik, **Alacak hesapları memuru** rolüne atanan kullanıcılar için İş belgesi yönetimi çalışma alanında neler mevcut olduğunu göstermektedir. Geçerli erişim izinleri ayarıyla, Kullanıcı, faturalama, mevzuat raporlaması ve ödemeler dahil farklı işlevsel alanlardaki iş belgesi şablonlarını düzenleyebilir.

    ![Alacak hesapları memuru için İş belgesi yönetimi çalışma alanı sayfası](./media/BDM-Overview-TemplatesForAlice1.png)

3. **Erişim izinleri yapılandırıcısı** sayfasında, **Erişim izinleri ayarı**'nıseçin.
4. **Şablonları düzenlemek için erişim izinleri ayarları** iletişim kutusunda, **Yapılandırılan erişim izinlerini uygula** seçeneğini etkinleştirin.
5. Iş belgesi yönetimi erişim izinlerinin etkinleştirildiğini onaylamak için **Tamam**'ı seçin.

    ![İş belgesi yönetimi erişimi izinleri onaylama](./media/BDM-Overview-TemplatesAccess2.png)

6. İlgili iş belge yönetimi şablonlarına erişim izinlerinin konfigüre edildiği yeni bir iş rolü girmek için **Ekle**'yi seçin.
7. **Güvenlik rolleri** iletişim kutusunda, **Alacak hesapları memuru** rolünü seçin ve sonra rol seçimini onaylamak için **Tamam**'ı seçin.
8. **Yapılandırma etiketleri başına erişim izinleri** sekmesinde, **Yeni**'yi seçin.
9. **Etiket türü** alanında, **İşlevsel alan**'ı seçin ve **Kimlik** alanında **Faturalama**'yı seçin.
10. Seçili rol için yapılandırılmış erişim izinlerini depolamak üzere **Kaydet**'i seçin.

    Geçerli ayar, **Alacak hesaplarına atanan memurlar** için bir rol ve gümrük vergisi gerçekleştirmekle ilgili, **İş belgesi şablonlarını yönetme** (AOT adı **ERBDManageTemplates**), ER biçimi **İşlevsel alan** etiketine ilişkin **Faturalama** değeri olan yapılandırma şablonları iş belgesi yönetimi çalışma alanında düzenleme için kullanılabilir olacaktır.

11. **İlgili bilgi** bölmesini geçerli sayfanın sağ tarafından değiştirin. **İlgili bilgiler** bölmesi, alacak **Hesaplar Yardım memuru** rolüne atanan kullanıcılar için hangi er yapılandırma şablonları kullanılabilir olacağını da içerecek şekilde, yapılandırılan erişim izinlerinin nasıl uygulanacağını gösterir.

    ![Erişim izinleri yapılandırıcısı sayfasındaki ilgili bilgiler bölmesi](./media/BDM-Overview-TemplatesAccess3.png)

12. **Yapılandırma etiketleri başına erişim izinleri** sekmesinde, **Ekle** seçeneğini seçin.
13. **Yapılandırma Seç** iletişim kutusunda, **Intrastat raporu** ER biçim yapılandırmasını işaretleyin.
14. Seçili yapılandırmaların girişini onaylamak için **Tamam**'ı, sonra da seçili rol için yapılandırılan erişim izinlerini depolamak üzere **Kaydet**'i seçin.

Geçerli ayar, **Alacak hesaplarına atanan memurlar** için bir rol ve gümrük vergisi gerçekleştirmekle ilgili, **İş belgesi şablonlarını yönetme** (AOT adı **ERBDManageTemplates**), aşağıdaki şablonlar çalışma alanında düzenleme için kullanılabilir olacaktır.

- **İşlevsel alan** etiketi için **Faturalama** değerine sahip şablonlar.
- **Yapılandırma başına erişim izinleri** sekmesi üzerinde listelenen ER biçim yapılandırmalarına ait şablonlar (bu örnekte **Yasal raporlama** etki alanının **Intrastat raporu** biçimi yapılandırmasındaki şablonlar).

![Erişim izinleri yapılandırıcısı sayfasındaki erişim izinleri hızlı sekmeleri](./media/BDM-Overview-TemplatesAccess4.png)

Aşağıdaki grafik, **Alacak hesapları memuru** rolüne atanan kullanıcılar için İş belgesi yönetimi çalışma alanında neler mevcut olduğunu göstermektedir. Geçerli Iş belge yönetimi erişim izinleri ayarıyla, Kullanıcı **faturalama** etki alanından ve **Intrastat raporu** ER biçim yapılandırmasındaki iş belgesi şablonlarını düzenleyebilir. **Ödemeler** etki alanındaki şablonlara **alacak hesapları memuru** rolü için erişilemez.

![İş belgesi yönetimi çalışma alanı sayfasında iş belgesi şablonlarını düzenleme](./media/BDM-Overview-TemplatesForAlice2.png)

> [!NOTE]
> **Yapılandırma etiketleri başına erişim izinleri** bir ER biçimi yapılandırmasının benzersiz kimlik kodu kullanılarak depolanır. Bu, bunlara başvuran bir ER yapılandırması silindiğinde bu kuralların silinmeyeceği anlamına gelir. Silinen yapılandırmaları bu örneğe geri aktardığınızda, bu kurallar bunlara yeniden başvuracaktır. Silinen yapılandırmalar tekrar içe aktarıldıktan sonra kuralları yeniden ayarlamaya gerek yoktur.

## <a name="use-business-document-management-to-edit-templates"></a>Şablonları düzenlemek için İş belge yönetimi'ni kullan

İş kullanıcıları iş belgesi şablonlarına İş belgesi yönetimi çalışma alanında düzenleme yapmak için erişebilir. Iş belgesi yönetimi çalışma alanı'na yalnızca aşağıdaki kullanıcılar erişebilir:

- **Sistem Yöneticisi** rolüne atanan kullanıcılar.
- Vergi gerçekleştirmek üzere konfigüre edilen herhangi bir role atanan kullanıcılar **Iş belgesi yönetimi şablonlarını yönet** (AOT adı **ERBDManageTemplates**).

İş belge yönetimi çalışma alanındaki serbest metin faturası şablonlarını düzenlemek için aşağıdaki yordamı kullanın. Bu yordamı gerçekleştirmeden önce, bu konudaki önceki yordamların tümünü tamamlamış olmalısınız.

1. İş belgesi yönetimi çalışma alanına erişimi olan bir kullanıcı olarak oturum açın.
2. İş belgesi yönetimi çalışma alanı sayfasını açın.

**Özellik yönetimi** çalışma alanında **İş belgeleri yönetimi için Office benzeri kullanıcı arabirimi deneyimi** özelliği devre dışı bırakıldığında, **İş belgesi yönetimi** çalışma alanındaki ana kılavuz aşağıdaki şablonları gösterir:

- ER yapılandırma sağlayıcınızın sahibi olduğu şablonlar (**Elektronik raporlama** çalışma alanında etkin olarak işaretlenmiş geçerli sağlayıcı). Bu şablonlardan birini seçtikten sonra, başlatmak veya düzenlemeye devam etmek için **Şablonu düzenle**'yi seçebilirsiniz.
- Sahibi başka ER yapılandırması sağlayıcıları olan şablonlar. Bu şablonlardan birini seçtikten sonra, ER yapılandırma sağlayıcınızın sahibi olduğu şablonun bir kopyasını oluşturmak için **Yeni belge**'yi seçebilir ve bu kopyayı düzenlemeye başlayabilirsiniz.

![İş belgesi yönetimi çalışma alanı sayfasında şablon listeleri](./media/BDM-Overview-EditingTemplate1.png)

**Şablon** sekmesi seçili şablonun içeriğini gösterir. Seçili şablonun ayrıntılarını ve bu şablonun içinde bulunduğu er biçim yapılandırmasının ayrıntılarını gözden geçirmek için **Ayrıntılar** sekmesini seçin. Tüm şablonların **Yayımlanmış** durumu olduğuna ve **Düzeltme** sütununda hiçbir ayrıntı içermediğini unutmayın. Bu, bu şablonların şu anda düzenlenmediği anlamına gelir.

**İş belgeleri yönetimi için Office benzeri kullanıcı arabirimi deneyimi** özelliği **Özellik yönetimi** çalışma alanında etkin olduğunda, **İş belgesi yönetimi** çalışmal alanındaki ana kılavuz ER yapılandırması sağlayıcınızın sahibi olduğu şablonları gösterir (**Elektronik raporlama** çalışma alanında etkin olarak işaretlenmiş olan geçerli sağlayıcı). Bu şablonlardan birini seçtikten sonra, başlatmak veya düzenlemeye devam etmek için **Şablonu düzenle**'yi seçebilirsiniz.

Başka ER yapılandırması sağlayıcılarının sahibi olduğu şablonlarla çalışmak için, ER sağlayıcınızın sahibi olduğu bir şablon kopyası oluşturmak için **Yeni belge**'yi seçin. Daha sonra kopyayı düzenlemeye başlayabilirsiniz. Daha fazla bilgi için bkz. [İş belgesi yönetiminde yeni belge kullanıcı arabirimi](er-business-document-management-new-template-ui.md).

### <a name="initiate-editing-templates-owned-by-your-configuration-provider"></a>Yapılandırma sağlayıcınız tarafından sahip olan düzenleme şablonlarını başlatın

1. İş belgesi yönetimi çalışma alanında, listedeki **Çek yazdırma biçim** şablonunu seçin.
2. **Ayrıntılar** sekmesini seçin.

![İş belgesi yönetimi çalışma alanı sayfası, Ayrıntılar sekmesi](./media/BDM-Overview-EditingTemplate2.png)

Seçili şablon için **Şablonu Düzenle** şablonu seçeneği kullanılabilir. Bu seçenek, etkin ER yapılandırma sağlayıcısı (Bu örnekte, **Litware, Inc.**) tarafından sahip olan ER biçim yapılandırması içindeki bir şablon için her zaman kullanılabilir. **Şablonu düzenle** seçildiğinde, temel ER biçim yapılandırmasının taslak sürümünden var olan şablon düzenlenebilir olacaktır.

### <a name="initiate-editing-templates-owned-by-other-providers"></a>Diğer sağlayıcılar tarafından sahip olan düzenleme şablonlarını başlatın

1. İş belgesi yönetimi çalışma alanında, şablon olarak kullanmak istediğiniz belgeyi seçin.

    ![İş belgesi yönetimi çalışma alanı sayfasında belge seçme](./media/BDM-Overview-EditingTemplate3.png)

2. **Yeni belge**'yi seçin ve gerekirse, **Başlık** alanında, düzenlenebilir şablonun başlığını değiştirin. Metin, otomatik olarak oluşturulan ER biçimi yapılandırmasını adlandırmak için kullanılacaktır. Düzenlenen şablonu içerecek şekilde bu yapılandırmanın taslak sürümünün (**Müşteri FTI raporu (GER) kopyası**) bu ER biçimini otomatik olarak geçerli kullanıcı için çalışacak şekilde işaretleneceğini göz önünde bulundurun. Aynı zamanda, temel ER biçimi yapılandırmasındaki değiştirilmemiş özgün şablon, başka bir kullanıcının bu ER biçimini çalıştırmak için kullanılacaktır.
3. **Ad** alanında, düzenlenebilir şablonun otomatik olarak oluşturulacak ilk revizyonunun adını değiştirin.
4. **Yorum** alanında, düzenlenebilir şablonun otomatik olarak oluşturulan revizyonuna ilişkin yorumu değiştirin.
5. Düzenleme işleminin başlangıcını onaylamak için **Tamam**'ı seçin.

![Yeni şablon oluşturmak için düzenleme işleminin başlangıcını onaylama](./media/BDM-Overview-EditingTemplate4.png)

**Yeni belge** seçeneği, geçerli veya başka bir sağlayıcı tarafından (bu örnekte Microsoft) sağlanan ER biçimi yapılandırmasındaki revizyonu olmayan bir şablonda her zaman kullanılabilir. Düzenlenen şablon daha sonra otomatik olarak oluşturulan yeni bir ER biçim yapılandırması içinde depolanır.

### <a name="start-editing-a-template"></a>Şablonu düzenlemeye başla

1. Seçili şablondan **Belgeyi düzenle**'yi seçin.
2. **Ad** alanında, düzenlenebilir şablonun otomatik olarak oluşturulacak ilk revizyonunun adını değiştirin.
3. **Yorum** alanında, düzenlenebilir şablonun otomatik olarak oluşturulan revizyonuna ilişkin değişikliği değiştirin.

    ![İş belgesi yönetimi çalışma alanı sayfasında şablon düzenleme](./media/BDM-Overview-EditingTemplate5.png)

4. Düzenleme işleminin başlangıcını onaylamak için **Tamam**'ı seçin.

**BDM şablon düzenleyici** sayfası açılır. Seçili şablon, Microsoft 365 kullanılarak çevrimiçi düzenleme için uygun olacak.

![İş belge yönetimi şablon düzenleme sayfası](./media/BDM-Overview-EditingLayout1.png)

### <a name="edit-a-template-in-microsoft-365"></a><a name="EditInOffice365"></a>Microsoft 365'te şablon düzenleme

Microsoft 365 kullanarak şablonda değişiklik yapabilirsiniz. Örneğin, Office Online'da, alanın yazı tipini, şablon başlığında **Normal**'den **Kalın**'a değiştirin. Bu değişiklikler, birincil şablonun depolama alanında (varsayılan olarak, Azure Blob depolaması) depolanan düzenlenebilir şablonda otomatik olarak depolanır. Bu, ER çerçevesi için yapılandırılmıştır.

![İş belgesi yönetimi şablon düzenleyicisi sayfasındaki şablon üst bilgisinde yazı tipini kalın olarak değiştirme](./media/BDM-Overview-EditingLayout2.png)

### <a name="edit-a-template-in-the-office-desktop-application"></a><a name="EditInOfficeDesktopApp"></a>Office masaüstü uygulamasında şablon düzenle

> [!NOTE]
> Bu işlev yalnızca **SharePoint belge türü** parametresi doğru olarak yapılandırıldığında kullanılabilir. Daha fazla bilgi için bkz. [Parametreleri yapılandırma](#SetupBdmParameters).

1. **Office Masaüstü uygulaması**'nın (Bu örnekte Excel) işlevini kullanarak şablonu değiştirmek için masaüstü uygulamasında aç seçeneğini seçin. Düzenlenebilir şablon, kalıcı depolama alanından İş belgesi yönetimi parametrelerinde konfigüre edilen geçici depolama alanına bir SharePoint klasör olarak kopyalanır.
2. Şablonu, Office Desktop Excel uygulamasındaki geçici dosya depolama alanından açmak istediğinizi onaylayın.

    ![Masaüstü Excel uygulamasında açılan şablon](./media/BDM-Overview-EditingLayout3.png)

3. Şablonu değiştirin. Örneğin, şablon başlığındaki alanların yazı tipini, rengi **Siyah** ila **Mavi** arasında güncelleyerek değiştirin.

    ![Masaüstü Excel uygulamasını kullanarak şablon üst bilgisinde yazı tipi rengini değiştirme](./media/BDM-Overview-EditingLayout4.png)

4. Şablon değişikliklerini geçici depoda depolamak için Excel masaüstü uygulamasında **Kaydet**'i seçin.

    ![Masaüstü Excel uygulamasını kullanarak İş belgesi yönetimi şablon düzenleyicisi sayfasında değişiklikleri kaydetme](./media/BDM-Overview-EditingLayout5.png)

5. Excel masaüstü uygulamasını kapatın.
6. Geçici şablon depolama alanını kalıcı şablon depolama ile eşitlemek için **Kaydedilmiş kopyayı eşitle**'yi seçin.

> [!NOTE]
> Geçici dosya depolama alanındaki düzenlenebilir şablonun kopyası yalnızca geçerli şablon düzenlemenin oturumu için depolanır. **BDM Şablon Düzenleyicisi** sayfasını kapatarak bu oturumu bitirdiğinizde, bu kopya silinir. Şablonu geçici dosya depolama alanında ayarladıysanız ve **Kaydedilmiş kopyayı eşitle**'yi seçmediyseniz, **BDM Şablon Düzenleyicisi** sayfasını kapatmaya çalıştığınızda, tanıtılan değişiklikleri depolamak isteyip istemediğinizi soran bir ileti alırsınız. Şablonda yaptığınız değişiklikleri kalıcı dosya konumunda kaydetmek istiyorsanız **Evet**'i seçin.

### <a name="validate-a-template"></a>Bir şablon doğrula

1. **BDM şablon düzenleyicisi** sayfasında, değiştirilen şablonu arka plandaki er biçim yapılandırmasıyla doğrulamak için **Sorunları denetle**'yi seçin. Şablonu temel ER biçimi yapılandırmasındaki biçimin yapısıyla hizalamak için (varsa) önerileri uygulayın.
2. Düzenlenebilir şablonla hizalanması gereken temel ER biçimi yapılandırmasındaki biçimin geçerli yapısını görüntülemek için **Biçimi göster**'i seçin. 
3. Bölmeyi kapatmak için **Biçimi Gizle**'yi seçin.

    ![BDM BDM Şablon Düzenleyicisi sayfası](./media/BDM-Overview-EditingTemplate6.png)

4. **BDM şablon düzenleyici** sayfasını kapatın.

Güncelleştirilen şablon, **Şablon** sekmesinde gösterilir. düzenlenen şablonun durumunun **Taslak** olduğuna ve geçerli düzeltmenin artık boş olmadığına dikkat edin. Bu, bu şablonun düzenleme işleminin başlatıldığı anlamına gelir.

![İş belgesi yönetimi çalışma alanı sayfasında güncellenen şablonu görüntüleme](./media/BDM-Overview-EditingTemplate5.png)

### <a name="test-the-modified-template"></a>Değiştirilmiş şablonu sına 

1. Uygulamada, şirketi **USMF** olarak değiştirin.
2. **Alacak hesapları** \> **Faturalar** \> **Tüm serbest metin faturaları**'na gidin.
3. **FTI-00000002** faturasını seçin ve **Yazdırma yönetimi**'ni seçin.
4. Düzeyi işlenecek faturaların kapsamını belirlemek için **Modül - alacak hesapları** \> **Belgeler** \> **Serbest metin fatura** \> **Özgün belge**'yi seçin.
5. **Rapor biçimi** alanında, **Müşteri FTI raporu (GER)** belirtilen belge düzeyi için ER biçimini seçin.

    ![Yazdırma yönetimi sayfasını yazdır](./media/BDM-Overview-TestRun1.png)

6. Geçerli sayfayı kapatmak için **ESC** tuşuna basın.
7. **Yazdır**'ı seçin ve **Seçili** öğesini belirleyin.
8. Belgeyi karşıdan yükleyin ve Excel masaüstü uygulamasını kullanarak açın.

![Serbest metin faturaları sayfası](./media/BDM-Overview-TestRun2.png)

Değiştirilen şablon, seçili madde için serbest metin faturası raporu oluşturmak amacıyla kullanılır. Bu raporun şablona eklediğiniz değişikliklerden nasıl etkilendiğini analiz etmek için, başka bir uygulama oturumunda şablonu değiştirdikten sonra bu raporu bir uygulama oturumunda çalıştırabilirsiniz.

### <a name="create-an-alternative-template-revision"></a>Alternatif şablon düzeltmesi oluştur

1. **BDM Şablon Düzenleyicisi** sayfasını açın ve **Müşteri FTI raporu (GER) Kopyala** şablonunu seçin.
2. **Düzeltmeler** sekmesinde, **Yeni**'yi seçin.
3. Gerekirse, **Ad** alanında, İkinci revizyon adını değiştirin ve onu o anda etkin olan ilk revizyon üzerinde temellendirin.
4. İhtiyaç halinde **Yorum** alanında, düzenlenebilir şablonun otomatik olarak oluşturulan revizyonuna ilişkin değişikliği değiştirin.

    ![İş belgesi yönetimi çalışma alanı sayfasında şablonda düzeltmeler oluşturma](./media/BDM-Overview-AddRevision.png)

    Şablonunuzun kalıcı şablonun depolama alanında depolanmış yeni bir düzeltmesi oluşturdunuz. Şimdi etkin olarak seçili olan ikinci revizyon şablonunu düzenlemeye devam edebilirsiniz.

5. İlk düzeltmeyi seçin ve sonra etkin **Ayarla**'yı seçin. Şablonun bu düzeltmesine dönmek istediğinizde, başka bir düzeltmeyi etkin olarak seçebilirsiniz.
6. İkinci revizyonu seçin ve **Sil**'i seçin.
7. Seçili revizyonu silmeyi onaylamak için **Tamam**'ı seçin. Etkin olmayan revizyonlar artık gerekli olmadığında silinebilir.

### <a name="delete-a-modified-template"></a>Değiştirilmiş şablonu silme

1. **BDM Şablon Düzenleyicisi** sayfasında **Şablon** sekmesini seçin.
2. **Sil**'i seçin.
3. Silme işlemini onaylamak için **Tamam**'ı seçerseniz, **Müşteri FTI raporu (GER) Kopyala** değiştirilmiş şablonla ER biçimini silinecek. Diğer seçenekleri keşfetmek için **İptal**'i seçin.

### <a name="revoke-changes-of-template"></a>Şablon değişikliklerini iptal et

Şablonu geçerli etkin sağlayıcının sahibi olduğu bir ER biçiminden düzenlediğinizde, bu şablon için tanıtılan değişiklikleri iptal etme seçeneği sunulur.

![İş belgesi yönetimi çalışma alanı sayfasında şablondaki değişiklikleri reddetme](./media/BDM-Overview-RevokeChanges.png)

1. **BDM Şablon Düzenleyicisi** sayfasında **Şablon** sekmesini seçin.
2. **Geri Al** seçeneğini belirleyin.
3. Şablon için tanıtılan değişiklikleri iptal etmek için **Tamam**'ı seçerseniz, değiştirilen şablon orijinal şablonla değiştirilir ve tüm değişiklikler kaldırılır. Şablonda yapılan değişiklikleri iptal ettiğinizde, şablonu silebilirsiniz. Diğer seçenekleri keşfetmek için **İptal**'i seçin.

### <a name="publish-a-modified-template"></a>Değiştirilmiş şablonu yayınlama

1. **BDM Şablon Düzenleyicisi** sayfasında **Şablon** sekmesinde **Yayınla**'yı seçin.
2. Yayımlamayı onaylamak için **Tamam**'ı seçerseniz, türetilmiş **Müşteri FTI raporunun (GER) Kopyala** değiştirilmiş şablonu içeren taslak biçimi tamamlandı olarak işaretlenir. Değiştirilen şablon, diğer kullanıcılar için kullanılabilir duruma gelir. Bu ER biçiminin tamamlanmış sürümleri şablonunuzun yalnızca son etkin düzeltmesini tutacaktır. Diğer düzeltmeler silinecek. Diğer seçenekleri keşfetmek için **İptal**'i seçin.

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

### <a name="i-selected-edit-document-but-instead-of-going-to-the-bdm-template-editor-page-in-finance-i-was-sent-to-the-microsoft-365-webpage"></a>Belgeyi düzenle'yi seçtim ancak Finance'teki BDM şablon düzenleyicisi sayfasına gitmek yerine Microsoft 365 web sayfasına yönlendirildim.

Bu sorun, Microsoft 365'in yeniden yönlendirmesiyle ilgili bilinen bir sorundur. Bu durum, Microsoft 365'te ilk kez oturum açtığınızda yaşanır. Bu sorunu geçici olarak çözmek için tarayıcınızda **Geri**'yi seçerek bir önceki sayfaya geri dönün.

### <a name="i-understand-how-to-edit-a-template-by-using-microsoft-365-in-the-first-application-session-and-how-to-use-the-template-in-the-second-application-session-and-adjust-the-template-to-see-how-my-changes-affect-the-generated-business-document-can-i-use-the-office-desktop-application-in-the-same-way"></a>İlk uygulama oturumunda, bir şablonun Microsoft 365 kullanarak nasıl düzenleneceğini ve değişikliklerin oluşturulan iş belgesini nasıl etkilediğini görmek için ikinci uygulama oturumunda şablonu nasıl kullanacağımı ve şablonu nasıl ayarlayacağımı anlıyorum. Office masaüstü uygulamasını aynı şekilde kullanabilir miyim?

Evet, yapabilirsiniz. İlk uygulama oturumunda, **Masaüstü uygulamasında aç**'ı seçin. Şablonunuz geçici dosya deposunda depolanır ve Office masaüstü uygulaması'nda açılır. Ardından, şablon değişikliklerinizi oluşturulan iş belgesinde önizlemek için aşağıdaki adımları tamamlayın:

1. Office masaüstü uygulamasını kullanarak şablonda değişiklik yapın.
2. Office Masaüstü uygulamasında **Kaydet**'i seçin.
3. İlk uygulama oturumunun **BDM şablon düzenleyicisi** sayfasında, **Depolanan kopyayı Eşitle**'yi seçin.
4. İkinci uygulama oturumunda bu şablon ER biçimini yürütür.

### <a name="when-i-select-open-in-desktop-app-i-receive-the-following-error-message-value-cannot-be-null-parameter-name-externalid-how-do-i-work-around-this-issue"></a>Masaüstü Uygulamasında Aç'ı seçtiğimde şu hata iletisini alıyorum: "Değer null olamaz. Parametre adı: externalId." Bu soruna nasıl çözüm bulabilirim?

Büyük olasılıkla, bu örneği dağıtmak için kullanılan Azure AD etki alanından farklı olan Azure AD etki alanının şu anki uygulama örneğinde oturum açtınız. Office Masaüstü uygulamaları kullanılarak düzenleme için şablonları depolamak amacıyla kullanılan SharePoint hizmeti, aynı etki alanına ait olduğundan SharePoint hizmete erişim için gereken izinlere sahip değildir. Bu sorunu gidermek için, doğru Azure AD etki alanı olan bir kullanıcının kimlik bilgilerini kullanarak geçerli örnekte oturum açın.

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)

[ER OPENXML biçiminde raporlar oluşturmak için yapılandırma tasarlama (Kasım 2016)](tasks/er-design-reports-openxml-2016-11.md)

[Word biçiminde raporlar oluşturmak için ER yapılandırmaları tasarlama](tasks/er-design-configuration-word-2016-11.md)

[Er kullanarak oluşturduğunuz belgelere resimler ve şekiller katıştırma](electronic-reporting-embed-images-shapes.md)

[Power BI'ya veri çekmek için Elektronik raporlamayı (ER) yapılandırma](general-electronic-reporting-report-configuration-get-data-powerbi.md)

## <a name="list-of-er-configurations-that-have-been-released-in-finance-to-support-configurable-business-documents"></a><a name="list-of-configurations-cbd"></a>Yapılandırılabilen iş belgelerini desteklemek için Finance'te yayınlanan ER yapılandırmalarının listesi

Finance için ER yapılandırmalarının [listesi](general-electronic-reporting.md#list-of-configurations) sürekli olarak güncelleştirilmektedir. Şu anda desteklenen ER yapılandırmalarının listesini incelemek için [Genel depo](er-download-configurations-global-repo.md)'yu açın. Yapılandırılabilir iş belgelerini desteklemek için kullanılan ER yapılandırmalarının listesini incelemek için Genel depo'da [filtre uygulayabilirsiniz](https://docs.microsoft.com/dynamics365/finance/localizations/enhanced-filtering-global-repo).

![Yapılandırma deposu sayfasında Genel depo içeriklerini filtreleme](./media/bdm-overview-filterglobalrepo.gif)

Aşağıdaki tabloda yapılandırılabilir iş belgelerini destekleyen ve Aralık 2020'ye kadar Finance'te yayınlanmış olan ER yapılandırmalarının listesi gösterilmektedir.

| Veri modeli yapılandırması    | Biçim yapılandırmaları                           |
|-----------------------------|-------------------------------------------------|
| Konşimento modeli        | Konşimento (Excel)                          |
|                             | Konşimento (Word)                           |
| Kaynak sertifikası modeli | Kaynak sertifikası (Excel)                   |
|                             | Kaynak sertifikası (Word)                    |
| Fatura modeli               | Müşteri Borç Dekontu ve Alacak Dekontu (Excel)          |
|                             | Müşteri Borç Dekontu ve Alacak Dekontu (Word)           |
|                             | Serbest metin faturası (Excel)                       |
|                             | Serbest metin faturası (Excel) (BH)                  |
|                             | Serbest metin faturası (FR) (Excel)                  |
|                             | Serbest metin faturası (LT) (Excel)                  |
|                             | Serbest metin faturası (LV) (Excel)                  |
|                             | Serbest metin faturası (PL) (Excel)                  |
|                             | Serbest metin faturası (CZ) (Excel)                  |
|                             | Serbest metin faturası (EE) (BH)                  |
|                             | Serbest metin faturası (HU) (Excel)                  |
|                             | Serbest metin faturası (TH) (Excel)                  |
|                             | Serbest metin faturası (Word)                        |
|                             | Proje sözleşmesi satır öğeleri (Excel)             |
|                             | Proje sözleşmesi satır öğeleri (CZ) (Excel)        |
|                             | Proje sözleşmesi satır öğeleri (Excel) (BH)        |
|                             | Proje sözleşmesi satır öğeleri (HU) (Excel)        |
|                             | Proje sözleşmesi satır öğeleri (LT) (Excel)        |
|                             | Proje sözleşmesi satır öğeleri (PL) (Excel)        |
|                             | Proje sözleşmesi satır öğeleri (Word)              |
|                             | Proje müşterisini tutmayı serbest bırakma (Excel)      |
|                             | Proje müşterisini tutmayı serbest bırakma (CZ) (Excel) |
|                             | Proje müşterisini tutmayı serbest bırakma (HU) (Excel) |
|                             | Proje müşterisini tutmayı serbest bırakma (LT) (Excel) |
|                             | Proje müşterisini tutmayı serbest bırakma (PL) (Excel) |
|                             | Proje müşterisini tutmayı serbest bırakma (TH) (Excel) |
|                             | Proje müşterisini tutmayı serbest bırakma (Word)       |
|                             | Proje faturası (Excel)                         |
|                             | Proje Faturası (Word)                          |
|                             | Proje faturası (AE) (Excel)                    |
|                             | Proje faturası (CZ) (Excel)                    |
|                             | Proje faturası (Excel) (BH)                    |
|                             | Proje faturası (HU) (Excel)                    |
|                             | Proje faturası (JP) (Excel)                    |
|                             | Proje faturası (LT) (Excel)                    |
|                             | Proje faturası (PL) (Excel)                    |
|                             | Proje faturası (TH) (Excel)                    |
|                             | Proje faturası tam (MY) (Excel)               |
|                             | Proje faturası basit (MY) (Excel)             |
|                             | Proje yönetme faturası (Excel)                  |
|                             | Proje yönetme faturası (CZ) (Excel)             |
|                             | Proje yönetme faturası (Excel) (BH)             |
|                             | Proje yönetme faturası (HU) (Excel)             |
|                             | Proje yönetme faturası (JP) (Excel)             |
|                             | Proje yönetme faturası (LT) (Excel)             |
|                             | Proje yönetme faturası (PL) (Excel)             |
|                             | Proje yönetme faturası (Word)                   |
|                             | Satın alma avans faturası (Excel)                |
|                             | Satın alma avans faturası (Word)                 |
|                             | Satış avans faturası (Excel)                   |
|                             | Satış avans faturası (Word)                    |
|                             | Satış avans faturası (PL) (Excel)              |
|                             | Satış faturası (Excel)                           |
|                             | Satış faturası (Excel) (BH)                      |
|                             | Satış faturası (Excel) (CZ)                      |
|                             | Satış faturası (Excel) (EE)                      |
|                             | Satış faturası (Excel) (FR)                      |
|                             | Satış faturası (Excel) (HU)                      |
|                             | Satış faturası (Excel) (IN)                      |
|                             | Satış faturası (Excel) (LT)                      |
|                             | Satış faturası (Excel) (LV)                      |
|                             | Satış faturası (Excel) (PL)                      |
|                             | Satış faturası (Excel) (TH)                      |
|                             | Satış faturası (Word)                            |
|                             | TMS Ticari Fatura (Excel)                  |
|                             | TMS Ticari Fatura (Word)                   |
|                             | Satıcı faturası belgesi (Excel)                 |
|                             | Satıcı faturası belgesi (CZ) (Excel)            |
|                             | Satıcı faturası belgesi (HU) (Excel)            |
|                             | Satıcı faturası belgesi (IN) (Excel)            |
|                             | Satıcı faturası belgesi (LT) (Excel)            |
|                             | Satıcı faturası belgesi (LV) (Excel)            |
|                             | Satıcı faturası belgesi (MY) (Excel)            |
|                             | Satıcı faturası belgesi (Word)                  |
| Sipariş modeli                 | Sözleşme onayı (Excel)                  |
|                             | Sözleşme onayı (Word)                   |
|                             | Satın alma sözleşmesi onayı (Excel)         |
|                             | Satın alma sözleşmesi onayı (Word)          |
|                             | Satınalma siparişi (Excel)                          |
|                             | Satınalma siparişi (CZ) (Excel)                     |
|                             | Satınalma siparişi sorgusu (CZ) (Excel)             |
|                             | Satınalma siparişi (HU) (Excel)                     |
|                             | Satınalma siparişi sorgusu (HU) (Excel)             |
|                             | Satınalma siparişi (Word)                           |
|                             | Satınalma siparişi sorgusu (Excel)                  |
|                             | Satınalma siparişi sorgusu (Word)                   |
|                             | Satış siparişi onayı (Excel)                |
|                             | Satış siparişi onayı (CZ) (Excel)           |
|                             | Satış siparişi onayı (HU) (Excel)           |
|                             | Satış siparişi onayı (Word)                 |
| Ambalaj listesi modeli          | Konteyner içeriği (Excel)                      |
|                             | Konteyner içeriği (Word)                       |
|                             | Yük listesi (Excel)                               |
|                             | Yük listesi (Word)                                |
|                             | Malzeme çekme listesi (Excel)                            |
|                             | Malzeme çekme listesi (CZ) (Excel)                       |
|                             | Malzeme çekme listesi (Word)                             |
|                             | Üretim malzeme çekme listesi (Excel)                    |
|                             | Üretim malzeme çekme listesi (Word)                     |
|                             | Yük için sevkiyat çekme listesi (Excel)             |
|                             | Yük için sevkiyat çekme listesi (Word)              |
|                             | Sevkiyat için sevkiyat çekme listesi (Excel)         |
|                             | Sevkiyat için sevkiyat çekme listesi (Word)          |
|                             | Dalga için sevkiyat çekme listesi (Excel)             |
|                             | Dalga için sevkiyat çekme listesi (Word)              |
| Ödeme modeli               | Müşteri ödeme ihbarı (Excel)                 |
|                             | Müşteri ödeme ihbarı (Word)                  |
|                             | Satıcı ödeme ihbarı (Excel)                   |
|                             | Satıcı ödeme ihbarı (Word)                    |
| Teklif modeli             | Proje teklifi (Excel)                       |
|                             | Proje teklifi (Word)                        |
|                             | Teklif talebi (Excel)                   |
|                             | Teklif talebi (Kabul Etme) (Excel)          |
|                             | Teklif talebi (Kabul Etme) (Word)           |
|                             | Teklif talebi (Reddetme) (Excel)          |
|                             | Teklif talebi (Reddetme) (Word)           |
|                             | Teklif talebi (İade) (Excel)          |
|                             | Teklif talebi (İade) (Word)           |
|                             | Teklif talebi (Word)                    |
|                             | Satış teklifi (Excel)                         |
|                             | Satış teklifi (CZ) (Excel)                    |
|                             | Satış teklifi (HU) (Excel)                    |
|                             | Satış teklifi (Word)                          |
|                             | Satış teklifi onayı (Excel)            |
|                             | Satış teklifi onayı (Word)             |
| Mutabakat modeli        | Müşteri hesap ekstresi, Harici (Excel)             |
|                             | Müşteri hesap ekstresi, Harici (CN) (Excel)        |
|                             | Müşteri hesap ekstresi, Harici (Word)              |
|                             | Müşteri hesap ekstresi, Fransa (Excel)          |
| Anımsatıcı modeli              | Tahsilat mektubu dekontu (Excel)                  |
|                             | Tahsilat mektubu dekontu (CN) (Excel)             |
|                             | Tahsilat mektubu dekontu (Word)                   |
|                             | Müşteri vade farkı dekontu (Excel)                  |
|                             | Müşteri vade farkı dekontu (Word)                   |
| İrsaliye modeli               | Yük ödemesi (Excel)                             |
|                             | Yük ödemesi (Word)                              |
|                             | Satınalma siparişi sevk irsaliyesi (Excel)             |
|                             | Satınalma siparişi sevk irsaliyesi (CZ) (Excel)        |
|                             | Satınalma siparişi sevk irsaliyesi (Word)              |
|                             | Rota (Excel)                                   |
|                             | Rota (Word)                                    |
|                             | Satış siparişi sevk irsaliyesi (Excel)                |
|                             | Satış siparişi sevk irsaliyesi (CZ) (Excel)           |
|                             | Satış siparişi sevk irsaliyesi (LT) (Excel)           |
|                             | Satış siparişi sevk irsaliyesi (PL) (Excel)           |
|                             | Satış siparişi sevk irsaliyesi (Word)                 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
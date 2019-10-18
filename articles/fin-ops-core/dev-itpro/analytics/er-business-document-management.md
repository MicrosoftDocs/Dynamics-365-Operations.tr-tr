---
title: İş belgesi yönetimine genel bakış
description: Bu konu, ER çerçevesinin iş belge yönetimi özelliğinin nasıl kullanılacağı hakkında bilgi sağlar.
author: NickSelin
manager: AnnBe
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3c84b08ec45dfa7aa9c7b913087a2518bfeedf87
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181577"
---
# <a name="business-document-management-overview"></a>İş belgesi yönetimine genel bakış

[Elektronik raporlama (ER) çerçevesi](general-electronic-reporting.md) kullanan iş kullanıcıları toplam belgelerin biçimini çeşitli ülkelerin/bölgelerin yasal gereksinimlerine uygun şekilde yapılandırmanıza olanak tanır. Kullanıcılar, oluşturulan belgelere hangi uygulama verilerinin yerleştirileceğini belirtmek için veri akışını da tanımlayabilir. ER çerçevesi, önceden tanımlanmış şablonları kullanarak Microsoft Office (Excel çalışma kitapları veya Word belgeleri) giden belgeleri biçimler. Şablon, gerekli belgelerin oluşturulması sırasında veri akışına uygun olarak, gerekli verilerle doldurulur. Konfigüre edilen her biçim, belirli giden belgeler oluşturmak üzere bir ER çözümünün parçası olarak yayımlanabilir. Bu, farklı giden belgeler oluşturmak için kullanabileceğiniz şablonlar içerebilen bir ER biçim konfigürasyonu ile temsil edilir. İş kullanıcıları gerekli iş belgelerini yönetmek için bu çerçeveyi kullanabilir.

**İş belgesi Yönetimi** ER çerçevesinin üzerine kurulmuştur ve iş kullanıcılarının servis veya uygun Microsoft Office 365 Microsoft Office masaüstü uygulamasını kullanarak iş belgesi şablonlarını düzenlemesini sağlar. Belgelerde yapılan düzenlemeler, iş belge tasarımlarının değiştirilmesini ve kaynak kodu değişiklikleri ve Yeni dağıtımlar olmaksızın ek veriler için yer tutucular eklemeyi içerir. İş belgelerinin şablonlarını güncelleştirmek için ER çerçevesi gerekli bilgisine sahip değildir.

> [!NOTE]
> Iş belgesi yönetiminin sipariş, fatura vb. gibi iş belgelerini üretmek için kullanılan şablonları değiştirmenize olanak verdiğini unutmayın. Bir şablon değiştirildiğinde ve yeni bir sürümü yayımlanmışsa, bu sürüm gerekli iş belgelerini oluşturmak için kullanılır. İş belgesi yönetimi, zaten oluşturulmuş iş belgelerini değiştirmek için kullanılamaz.

## <a name="supported-deployments"></a>Desteklenen dağıtımlar

Şu anda, Iş belgesi yönetimi özelliği yalnızca bulut dağıtımları için geçerlidir. Bu özellik şirket içi dağıtımınız için önemliyse, [Fikirler](https://experience.dynamics.com/ideas/) sitesine geri bildirim vererek bize bildirin.

## <a name="supported-microsoft-office-applications"></a>Desteklenen Microsoft Office uygulamaları

Masaüstü uygulamaları kullanarak Microsoft Office şablonları Excel veya Word biçimlerinde düzenlemek üzere iş belge yönetimini kullanmak için Microsoft Office 2010 veya daha ileri bir sürümü yüklemiş olmanız gerekir. Bulut ve şirket içi dağıtımlarda desteklenir.

## <a name="business-document-availability"></a>İş belgesi uygunluğu

Excel tabanlı şablonlarla olan aşağıdaki raporlar, genel önizlemenin yayımlanmasıyla kullanılabilir:

**Alacak hesapları** (Ağustos 2019)

- Satış avans faturası
- Satış siparişi sevk irsaliyesi

**Borç hesaplar** (Ağustos 2019)

- Satınalma Avans Faturası
- Satın alma siparişi
- Satınalma siparişi sevk irsaliyesi

Daha fazla rapor mevcut olacak. Ek raporlarla ilgili özel bildirimler ayrı olarak gönderilecektir. 

2019 Ekim yayımı için planlanan tüm raporların tam listesi, [ Word ve Excel'de konfigüre edilebilir iş belgeleri raporlaması](https://docs.microsoft.com/en-us/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details)' içinde bulunabilir.

# <a name="example-enable-configure-and-use-business-document-management"></a>Örnek: iş belge yönetimini etkinleştirme, konfigüre etme ve kullanma

Bu özellik hakkında daha fazla bilgi edinmek için bu konudaki örneği tamamlayın.

## <a name="configure-er-parameters"></a>ER parametrelerini yapılandırma

İş belgesi yönetimi ER çerçevesinin üzerine oluşturulduğundan, İş belge yönetimiyle çalışmaya başlamak için ER parametrelerini konfigüre etmelisiniz. Bunu yapmak için, [ER çerçevesini konfigüre et](electronic-reporting-er-configure-parameters.md)'te açıklandığı şekilde er parametrelerini ayarlamanız gerekir. Ayrıca, [Konfigürasyon sağlayıcıları oluştur ve bunları ektin olarak işaretle](tasks/er-configuration-provider-mark-it-active-2016-11.md)'de gösterildiği gibi yeni bir konfigürasyon sağlayıcısı eklemeniz gerekir.

![ER Çalışma Alanı](./media/BDM-Overview-ERSetting.png)

## <a name="import-er-solutions"></a>ER çözümlerini çe aktar

İş belgeleri şablonlarını içeren ER konfigürasyonlarını, geçerli örneğe aktarmanız gerekir. Bu yordamı tamamlamak için aşağıdaki dosyaları karşıdan yükleyin ve yerel olarak depolayın.

**Örnek ER müşteri faturalama çözümü**

| **Dosya**                                  | **İçerik**                                |
|-------------------------------------------|--------------------------------------------|
| Customer invoicing model.version.2.xml    | [ER verisi modeli yapılandırması](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Customer FTI report (GER).version.2.3.xml | [Serbest metin fatura ER formu konfigürasyonları](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

**Örnek ER ödeme çekleri çözümü**

| **Dosya**                                  | **İçerik**                                |
|-------------------------------------------|--------------------------------------------|
| Model for cheques.version.10.xml          | [ER verisi modeli yapılandırması](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Cheques printing format.version.10.9.xml  | [Ödeme çeki ER biçimi konfigürasyonu](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

**Örnek ER dış ticaret çözümü**

| **Dosya**                                  | **İçerik**                                |
|-------------------------------------------|--------------------------------------------|
| Intrastat model.version.1.xml             | [ER verisi modeli yapılandırması](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Intrastat report.version.1.9.xml          | [Intrastat kontrol raporu ER biçim konfigürasyonu](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

Her bir dosyayı içe aktarmak için aşağıdaki yordamı kullanın. İlgili ER *biçimi* yapılandırmasını içe aktarmadan önce, yukarıdaki tablolardaki her bir er çözümünün ER *veri modeli* yapılandırmasını içe aktarın.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar** sayfasını açın.
2. Sayfanın üstündeki **Döviz**'i seçin.
3. **XML dosyasından yükle**'yi seçin.
4. Gerekli XML dosyasını yüklemek için **Gözat**'ı seçin.
5. Konfigürasyonun içe aktarma işlemini onaylamak için **Tamam**'ı seçin.

![ER konfigürasyon sayfası](./media/BDM-Overview-ERSolutions.png)

ER konfigürasyonlarının içe aktarılması hakkında daha fazla bilgi içi bkz: [ER konfigürasyonu yaşam döngüsünü yönetme](general-electronic-reporting-manage-configuration-lifecycle.md).

## <a name="enable-business-document-management"></a>İş belgesi yönetimini etkinleştirme

Iş belge yönetimini başlatmak için **Özellik Yönetimi** çalışma alanını açmanız ve **İş belge yönetimi** özelliğini etkinleştirmeniz gerekir.

Tüm yasal varlıklar için iş belgesi yönetim işlevlerini etkinleştirmek üzere aşağıdaki yordamı kullanın.

1. **Özellik yönetimi** çalışma alanını açın.
2. **Yeni** sekmesinde, listeden **İş belge yönetimi** özelliğini seçin.
3. Seçili özelliği açmak için **Şimdi etkinleştir**'i seçin.
4. Yeni özelliğe erişmek için sayfayı yenileyin.

![Özellik yönetimi çalışma alanı](./media/BDM-Overview-FMEnabling.png)

Yeni özellikleri etkinleştirme hakkında daha fazla bilgi için [Özellik yönetimine genel bakış](../../fin-and-ops/get-started/feature-management/feature-management-overview.md)'a bakın.

## <a name="configure-parameters"></a>Parametrelerini yapılandırma

Iş belgesi yönetimi için temel parametreleri ayarlamak üzere aşağıdaki bölümlerdeki bilgileri kullanın.

### <a name="prerequisites-for-parameter-setup"></a>Parametre kurulumu için Önkoşullar
Iş belge yönetimini kurmadan önce, gerekli belge türünü belge yönetim çerçevesi olarak ayarlamanız gerekir. Bu belge türü, ER raporları için şablon olarak kullanılan Office biçimlerindeki (Excel ve Word) belgelerin geçici bir depolanmasını belirtmek için kullanılır. Geçici depolama şablonu Office Masaüstü uygulamaları kullanılarak düzenlenebilir.

Bu belge türü için aşağıdaki öznitelik değerleri seçilmelidir.

| **Öznitelik adı**  | **Öznitelik değeri**   |
|---------------------|-----------------------|
| Sınıf               | Dosya iliştir           |
| Grup               | Dosya                  |
| Konum            | SharePoint            |

Gerekli belge yönetimi parametrelerinin ve belge türlerinin nasıl ayarlanacağı hakkında bilgi için bkz: [Belge yönetimini yapılandır](../../fin-and-ops/organization-administration/configure-document-management.md).

![Belge yönetimi belge türünü ayarla](./media/BDM-Overview-DMSetting.png)

### <a name="set-up-parameters"></a>Parametreleri ayarlayın

Temel İş belgesi yönetim parametreleri **İş belgesi parametreleri** sayfasında ayarlanabilir. Yalnızca belirli kullanıcılar sayfaya erişebilir. Bunların arasında yer alanlar:

- **Sistem Yöneticisi** rolüne atanan kullanıcılar.
- Vergi gerçekleştirmek üzere konfigüre edilen herhangi bir role atanan kullanıcılar **Iş belgesi yönetimi parametrelerinin bakımı** (AOT adı **ERBDMaintainParameters**).

Tüm tüzel kişilikler için temel parametreleri ayarlamak üzere aşağıdaki yordamı kullanın.

1. **İş belgesi parametreleri** sayfasına erişimi olan bir kullanıcı olarak oturum açın.
2. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **İş belgesi yönetimi** \> **İş belgesi yönetimi parametreleri**'ne gidin.
3.  **İş belgesi parametreleri** sayfasında, **Ekler** sekmesinde, **SharePoint belge türü** alanında, şablonları ofis formatlarında geçici olarak depolamak için kullanılacak belge tipini tanımlayan Office Masaüstü uygulamaları kullanılarak düzenlenir. 

> [!NOTE]
> Yalnızca bir SharePoint yerleşim kullanılarak konfigüre edilen belge türleri bu parametre için kullanılabilir.

![Iş belgesi yönetim parametrelerinin kurulumu](./media/BDM-Overview-BDMSetting.png)

Seçili belge türü şirkete özgüdür ve seçilen belge türü konfigüre edilen şirketteki İş Belge yönetiminde kullanıcının çalıştığı zaman kullanılır. Kullanıcı, başka bir şirkette İş belgesi yönetimi ile çalışırken, bu şirket için yapılandırılmadıysa, seçilen aynı belge türü kullanılacaktır. Bir belge türü konfigüre edildiğinde, **SharePoint belge türü** alanında seçilen yerine kullanılacak.

## <a name="configure-access-permissions"></a>Erişim izinlerini yapılandır

Varsayılan olarak, İş belgesi yönetimi izinlerine erişim özelliği etkin olmadığında, İş belge yönetimi çalışma alanına erişimi olan her Kullanıcı, tüm ER çözüm şablonlarını görür. İş belgesi yönetimi çalışma alanı yalnızca, ER biçim konfigürasyonlarında bulunan ve bir **İş belgesi türü** etiketi tarafından işaretlenen şablonları gösterir.

![ER konfigürasyon sayfası](./media/BDM-Overview-ERFormatTags.png)

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

![İş belgesi yönetimi çalışma alanı sayfası](./media/BDM-Overview-TemplatesForAlice1.png)

3. **Erişim izinleri yapılandırıcısı** sayfasında, **Erişim izinleri ayarı**'nıseçin.
4. **Şablonları düzenlemek için erişim izinleri ayarları** iletişim kutusunda, **Yapılandırılan erişim izinlerini uygula** seçeneğini etkinleştirin.
5. Iş belgesi yönetimi erişim izinlerinin etkinleştirildiğini onaylamak için **Tamam**'ı seçin.

![Iş belgesi yönetimi erişim izinleri yapılandırması sayfası](./media/BDM-Overview-TemplatesAccess2.png)

6. İlgili iş belge yönetimi şablonlarına erişim izinlerinin konfigüre edildiği yeni bir iş rolü girmek için **Ekle**'yi seçin.
7. **Güvenlik rolleri** iletişim kutusunda, **Alacak hesapları memuru** rolünü seçin ve sonra rol seçimini onaylamak için **Tamam**'ı seçin.
8. **Konfigürasyon etiketleri başına erişim izinleri** sekmesinde, **Yeni**'yi seçin.
9. **Etiket türü** alanında, **İşlevsel alan**'ı seçin ve **Kimlik** alanında **Faturalama**'yı seçin.
10. Seçili rol için yapılandırılmış erişim izinlerini depolamak üzere **Kaydet**'i seçin.

  Geçerli ayar, **Alacak hesaplarına atanan memurlar** için bir rol ve gümrük vergisi gerçekleştirmekle ilgili, **İş belgesi şablonlarını yönetme** (AOT adı **ERBDManageTemplates**), ER biçimi **İşlevsel alan** etiketine ilişkin **Faturalama** değeri olan konfigürasyon şablonları iş belgesi yönetimi çalışma alanında düzenleme için kullanılabilir olacaktır.

11. **İlgili bilgi** bölmesini geçerli sayfanın sağ tarafından değiştirin. **İlgili bilgiler** bölmesi, alacak **Hesaplar Yardım memuru** rolüne atanan kullanıcılar için hangi er yapılandırma şablonları kullanılabilir olacağını da içerecek şekilde, yapılandırılan erişim izinlerinin nasıl uygulanacağını gösterir.

![Iş belgesi yönetimi erişim izinleri yapılandırması sayfası](./media/BDM-Overview-TemplatesAccess3.png)

12. **Konfigürasyon etiketleri başına erişim izinleri** sekmesinde, **Ekle** seçeneğini seçin.
13. **Konfigürasyon Seç** iletişim kutusunda, **Intrastat raporu** ER biçimi konfigürasyonunu işaretleyin.
14. Seçili konfigürasyonların girişini onaylamak için **Tamam**'ı, sonra da seçili rol için yapılandırılan erişim izinlerini depolamak üzere **Kaydet**'i seçin.

Geçerli ayar, **Alacak hesaplarına atanan memurlar** için bir rol ve gümrük vergisi gerçekleştirmekle ilgili, **İş belgesi şablonlarını yönetme** (AOT adı **ERBDManageTemplates**), aşağıdaki şablonlar çalışma alanında düzenleme için kullanılabilir olacaktır.

- **İşlevsel alan** etiketi için **Faturalama** değerine sahip şablonlar.
- **Konfigürasyon başına erişim izinleri** sekmesi üzerinde listelenen er biçim konfigürasyonlarına ait şablonlar (bu örnekte **Yasal raporlama** etki alanının **Intrastat raporu** biçimi konfigürasyonundaki şablonlar).

![Iş belgesi yönetimi erişim izinleri yapılandırması sayfası](./media/BDM-Overview-TemplatesAccess4.png)

Aşağıdaki grafik, **Alacak hesapları memuru** rolüne atanan kullanıcılar için İş belgesi yönetimi çalışma alanında neler mevcut olduğunu göstermektedir. Geçerli Iş belge yönetimi erişim izinleri ayarıyla, Kullanıcı **faturalama** etki alanından ve **Intrastat raporu** ER konfigürasyonu konfigürasyonundaki iş belgesi şablonlarını düzenleyebilir. **Ödemeler** etki alanındaki şablonlara **alacak hesapları memuru** rolü için erişilemez.

![İş belgesi yönetimi çalışma alanı sayfası](./media/BDM-Overview-TemplatesForAlice2.png)

> [!NOTE]
> **Konfigürasyon etiketleri başına erişim izinleri** bir ER biçimi yapılandırmasının benzersiz kimlik kodu kullanılarak depolanır. Bu, bunlara başvuran bir ER yapılandırması silindiğinde bu kuralların silinmeyeceği anlamına gelir. Silinen yapılandırmaları bu örneğe geri aktardığınızda, bu kurallar bunlara yeniden başvuracaktır. Silinen konfigürasyonlar tekrar içe aktarıldıktan sonra kuralları yeniden ayarlamaya gerek yoktur.

## <a name="use-business-document-management-to-edit-templates"></a>Şablonları düzenlemek için İş belge yönetimi'ni kullan

İş kullanıcıları iş belgesi şablonlarına İş belgesi yönetimi çalışma alanında düzenleme yapmak için erişebilir. Iş belgesi yönetimi çalışma alanı'na yalnızca aşağıdaki kullanıcılar erişebilir:

- **Sistem Yöneticisi** rolüne atanan kullanıcılar.
- Vergi gerçekleştirmek üzere konfigüre edilen herhangi bir role atanan kullanıcılar **Iş belgesi yönetimi şablonlarını yönet** (AOT adı **ERBDManageTemplates**).

İş belge yönetimi çalışma alanındaki serbest metin faturası şablonlarını düzenlemek için aşağıdaki yordamı kullanın. Bu yordamı gerçekleştirmeden önce, bu konudaki önceki yordamların tümünü tamamlamış olmalısınız.

1. İş belgesi yönetimi çalışma alanına erişimi olan bir kullanıcı olarak oturum açın.
2. İş belgesi yönetimi çalışma alanı sayfasını açın.

![İş belgesi yönetimi çalışma alanı sayfası](./media/BDM-Overview-EditingTemplate1.png)

**Şablon** sekmesi seçili şablonun içeriğini gösterir. Seçili şablonun ayrıntılarını ve bu şablonun içinde bulunduğu er biçim yapılandırmasının ayrıntılarını gözden geçirmek için **Ayrıntılar** sekmesini seçin. Tüm şablonların **Yayımlanmış**durumu olduğuna ve **Düzeltme** sütununda hiçbir ayrıntı içermediğini unutmayın. Bu, bu şablonların şu anda düzenlenmediği anlamına gelir.

### <a name="initiate-editing-templates-owned-by-your-configuration-provider"></a>Yapılandırma sağlayıcınız tarafından sahip olan düzenleme şablonlarını başlatın

1. İş belgesi yönetimi çalışma alanında, listedeki **Çek yazdırma biçim** şablonunu seçin.
2. **Ayrıntılar** sekmesini seçin.

![İş belgesi yönetimi çalışma alanı sayfası](./media/BDM-Overview-EditingTemplate2.png)

Seçili şablon için **Şablonu Düzenle** şablonu seçeneği kullanılabilir. Bu seçenek, etkin ER yapılandırma sağlayıcısı (Bu örnekte, **Litware, Inc.**) tarafından sahip olan ER biçimi konfigürasyonu içindeki bir şablon için her zaman kullanılabilir. **Şablonu düzenle** seçildiğinde, temel ER biçim konfigürasyonunun taslak sürümünden varolan şablon düzenlenebilir olacaktır.

### <a name="initiate-editing-templates-owned-by-other-providers"></a>Diğer sağlayıcılar tarafından sahip olan düzenleme şablonlarını başlatın

1. İş belgesi yönetimi çalışma alanında, listedeki **Müşteri FTI raporu (GER)** şablonunu seçin.
2. **Ayrıntılar** sekmesini seçin.

![İş belgesi yönetimi çalışma alanı sayfası](./media/BDM-Overview-EditingTemplate3.png)

Seçili şablon için **Yeni dosya** şablonu seçeneği kullanılabilir. Bu seçenek, başka bir sağlayıcı tarafından sağlanan ER formatındaki bir şablonda her zaman kullanılabilir (Bu örnekte **Microsoft**). **Yeni belge** seçildiğinde, düzenlemek için yeni bir şablon kullanılabilir. Düzenlenen şablon daha sonra otomatik olarak oluşturulan yeni bir ER biçimi konfigürasyonu içinde depolanır.

### <a name="start-editing-a-template"></a>Şablonu düzenlemeye başla

1. Seçili şablondan **Yeni belge**'yi seçin.
2. **Başlık** alanında, gerekirse düzenlenebilir şablonun başlığını değiştirin. Metin, otomatik olarak oluşturulan ER biçimi yapılandırmasını adlandırmak için kullanılacaktır. Düzenlenen şablonu içerecek şekilde bu konfigürasyonun taslak sürümünün (**Müşteri FTI raporu (GER) kopyası**) bu ER biçimini otomatik olarak geçerli kullanıcı için çalışacak şekilde işaretleneceğini göz önünde bulundurun. Aynı zamanda, temel ER biçimi konfigürasyonundaki değiştirilmemiş özgün şablon, başka bir kullanıcının bu ER biçimini çalıştırmak için kullanılacaktır.
3. **Ad** alanında, düzenlenebilir şablonun otomatik olarak oluşturulacak ilk revizyonunun adını değiştirin.
4. **Yorum** alanında, düzenlenebilir şablonun otomatik olarak oluşturulan revizyonuna ilişkin değişikliği değiştirin.

![İş belgesi yönetimi çalışma alanı sayfası](./media/BDM-Overview-EditingTemplate4.png)

5. Düzenleme işleminin başlangıcını onaylamak için **Tamam**'ı seçin.

**BDM şablon düzenleyici** sayfası açılır. Seçili şablon, kullanılarak Office 365 çevrimiçi düzenleme için kullanılabilir olacak.

![İş belgesi yönetimi çalışma alanı sayfası](./media/BDM-Overview-EditingLayout1.png)

### <a name="edit-a-template-in-office-365"></a>Office 365'te şablon düzenle

Office 365 İşlevini kullanarak şablonu değiştirin. Örneğin, Office Online'da, alanın yazı tipini, şablon başlığında **Normal**'den **Kalın**'a değiştirin. Bu değişiklikler, birincil şablonun depolama alanında depolanan düzenlenebilir şablon için (varsayılan olarak, ER çerçevesi için yapılandırılan Azure Blob depolaması) otomatik olarak depolanır.

![İş belge yönetimi şablon düzenleme sayfası](./media/BDM-Overview-EditingLayout2.png)

### <a name="edit-a-template-in-the-office-desktop-application"></a>Office masaüstü uygulamasında şablon düzenle

1. **Office Masaüstü uygulaması**'nın (Bu örnekte Excel) işlevini kullanarak şablonu değiştirmek için masaüstü uygulamasında aç seçeneğini seçin. Düzenlenebilir şablon, kalıcı depolama alanından İş belgesi yönetimi parametrelerinde konfigüre edilen geçici depolama alanına bir SharePoint klasör olarak kopyalanır.
2. Şablonu, Office Desktop Excel uygulamasındaki geçici dosya depolama alanından açmak istediğinizi onaylayın.

![İş belgesi yönetimi çalışma alanı sayfası](./media/BDM-Overview-EditingLayout3.png)

3. Şablonu değiştirin. Örneğin, şablon başlığındaki alanların yazı tipini, rengi **Siyah** ila **Mavi** arasında güncelleyerek değiştirin.

![İş belge yönetimi şablon düzenleme sayfası](./media/BDM-Overview-EditingLayout4.png)

4. Şablon değişikliklerini geçici depoda depolamak için Excel masaüstü uygulamasında **Kaydet**'i seçin.

![İş belge yönetimi şablon düzenleme sayfası](./media/BDM-Overview-EditingLayout5.png)

5. Excel masaüstü uygulamasını kapatın.
6. Geçici şablon depolama alanını kalıcı şablon depolama ile eşitlemek için **Kaydedilmiş kopyayı eşitle**'yi seçin.

> [!NOTE]
> Geçici dosya depolama alanındaki düzenlenebilir şablonun kopyası yalnızca geçerli şablon düzenlemenin oturumu için depolanır. **BDM Şablon Düzenleyicisi** sayfasını kapatarak bu oturumu bitirdiğinizde, bu kopya silinir. Şablonu geçici dosya depolama alanında ayarladıysanız ve **Kaydedilmiş kopyayı eşitle**'yi seçmediyseniz, **BDM Şablon Düzenleyicisi** sayfasını kapatmaya çalıştığınızda, tanıtılan değişiklikleri depolamak isteyip istemediğinizi soran bir ileti alırsınız. Şablonda yaptığınız değişiklikleri kalıcı dosya konumunda kaydetmek istiyorsanız **Evet**'i seçin.

### <a name="validate-a-template"></a>Bir şablon doğrula

1. **BDM şablon düzenleyicisi** sayfasında, değiştirilen şablonu arka plandaki er formatı konfigürasyonuyla doğrulamak için **Sorunları denetle**'yi seçin. Şablonu temel ER formatı konfigürasyonundaki biçimin yapısıyla hizalamak için (varsa) önerileri uygulayın.
2. Düzenlenebilir şablonla hizalanması gereken taban er formatı konfigürasyonundaki biçimin geçerli yapısını görüntülemek için **Biçimi göster**'i seçin. 
3. Bölmeyi kapatmak için **Biçimi Gizle**'yi seçin.

![BDM BDM Şablon Düzenleyicisi sayfası](./media/BDM-Overview-EditingTemplate6.png)

4. **BDM şablon düzenleyici** sayfasını kapatın.

Güncelleştirilen şablon, **Şablon** sekmesinde gösterilir. düzenlenen şablonun durumunun **Taslak** olduğuna ve geçerli düzeltmenin artık boş olmadığına dikkat edin. Bu, bu şablonun düzenleme işleminin başlatıldığı anlamına gelir.

![İş belgesi yönetimi çalışma alanı sayfası](./media/BDM-Overview-EditingTemplate5.png)

### <a name="test-the-modified-template"></a>Değiştirilmiş şablonu sına 

1. Uygulamada, şirketi **USMF** olarak değiştirin.
2. **Alacak hesapları** \> **Faturalar** \> **Tüm serbest metin faturaları**'na gidin.
3. **FTI-00000002** faturasını seçin ve **Yazdırma yönetimi**'ni seçin.
4. Düzeyi işlenecek faturaların kapsamını belirlemek için **Modül - alacak hesapları** \> **Belgeler** \> **Serbest metin fatura** \> **Özgün belge**'yi seçin.
5. **Rapor biçimi** alanında, **Müşteri FTI raporu (GER)** belirtilen belge düzeyi için ER biçimini seçin.

![Yazdırma yönetimi sayfasını yazdır](./media/BDM-Overview-TestRun1.png)

6. Geçerli sayfayı kapatmak için **ESC** tuşuna basın.
7. **Yazdır**'ı seçin ve **Seçili**'ye tıklayın.
8. Belgeyi karşıdan yükleyin ve Excel masaüstü uygulamasını kullanarak açın.

![Serbest metin faturaları sayfası](./media/BDM-Overview-TestRun2.png)

Değiştirilen şablon, seçili madde için serbest metin faturası raporu oluşturmak amacıyla kullanılır. Bu raporun şablona eklediğiniz değişikliklerden nasıl etkilendiğini analiz etmek için, başka bir uygulama oturumunda şablonu değiştirdikten sonra bu raporu bir uygulama oturumunda çalıştırabilirsiniz.

### <a name="create-an-alternative-template-revision"></a>Alternatif şablon düzeltmesi oluştur

1. **BDM Şablon Düzenleyicisi** sayfasını açın ve **Müşteri FTI raporu (GER) Kopyala** şablonunu seçin.
2. **Düzeltmeler** sekmesinde, **Yeni**'yi seçin.
3. Gerekirse, **Ad** alanında, İkinci revizyon adını değiştirin ve onu o anda etkin olan ilk revizyon üzerinde temellendirin.
4. İhtiyaç halinde **Yorum** alanında, düzenlenebilir şablonun otomatik olarak oluşturulan revizyonuna ilişkin değişikliği değiştirin.

![İş belgesi yönetimi çalışma alanı sayfası](./media/BDM-Overview-AddRevision.png)

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

![İş belgesi yönetimi çalışma alanı sayfası](./media/BDM-Overview-RevokeChanges.png)

1. **BDM Şablon Düzenleyicisi** sayfasında **Şablon** sekmesini seçin.
2. **Geri Al**seçeneğini belirleyin.
3. Şablon için tanıtılan değişiklikleri iptal etmek için **Tamam**'ı seçerseniz, değiştirilen şablon orijinal şablonla değiştirilir ve tüm değişiklikler kaldırılır. Şablonda yapılan değişiklikleri iptal ettiğinizde, şablonu silebilirsiniz. Diğer seçenekleri keşfetmek için **İptal**'i seçin.

### <a name="publish-a-modified-template"></a>Değiştirilmiş şablonu yayınlama
1. **BDM Şablon Düzenleyicisi** sayfasında **Şablon** sekmesinde **Yayınla**'yı seçin.
2. Yayımlamayı onaylamak için **Tamam**'ı seçerseniz, türetilmiş **Müşteri FTI raporunun (GER) Kopyala** değiştirilmiş şablonu içeren taslak biçimi tamamlandı olarak işaretlenir. Değiştirilen şablon, diğer kullanıcılar için kullanılabilir duruma gelir. Bu ER biçiminin tamamlanmış sürümleri şablonunuzun yalnızca son etkin düzeltmesini tutacaktır. Diğer düzeltmeler silinecek. Diğer seçenekleri keşfetmek için **İptal**'i seçin.

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

#### <a name="i-selected-new-document-but-instead-of-opening-the-bdm-template-editor-page-in-finance-and-operations-i-have-been-sent-to-the-office-365-web-page"></a>**Yeni belge** seçtim, ancak Finance and Operations'taki **BDM şablon düzenleyici** sayfasını açmak yerine Office 365 Web sayfasına gönderildim.
Bu, Office 365 yeniden yönlendirmede olduğu bilinen bir sorundur. İlk kez Office 365'te oturum açtığınızda bu durum gerçekleşir. Bu soruna geçici bir çözüm bulmak için, tarayıcınızın **Geri** düğmesini seçerek geri dönün.

#### <a name="i-understand-how-to-edit-a-template-by-using-office-365-in-the-first-application-session-and-how-to-use-the-template-in-the-second-application-session-adjusting-the-template-to-see-how-my-changes-affect-the-generated-business-document-can-i-do-this-using-the-office-desktop-application"></a>İlk uygulama oturumunda, bir şablonun Office 365 kullanarak nasıl düzenleneceğini ve değişikliklerin oluşturulan iş belgesini nasıl etkilediğini görmek için şablonu ayarlama ikinci uygulama oturumunda şablonu nasıl kullanacağınızı anladım. Bunu Office masaüstü uygulamasını kullanarak yapabilir miyim?
Evet, yapabilirsiniz. İlk uygulama oturumunda, **Masaüstü uygulamasında aç**'ı seçin. Şablonunuz geçici dosya deposunda depolanır ve Office masaüstü uygulaması'nda açılır. Ardından, şablon değişikliklerinizi oluşturulan iş belgesinde önizlemek için aşağıdaki adımları tamamlayın:

1. Office masaüstü uygulamasını kullanarak şablonda değişiklik yapın.
2. Office Masaüstü uygulamasında **Kaydet**'i seçin.
3. İlk uygulama oturumunun **BDM şablon düzenleyicisi** sayfasında, **Depolanan kopyayı Eşitle**'yi seçin.
4. İkinci uygulama oturumunda bu şablon ER biçimini yürütür.

#### <a name="i-get-the-error-value-cannot-be-null-parameter-name-externalid-when-i-select-open-in-desktop-app-how-do-i-work-around-this"></a>'Değer boş olamaz hatası alıyorum. **Masaüstü uygulamasında aç**'ı seçtiğimde parametre adı: externalId' Bu soruna nasıl çözüm bulabilirim? 
Büyük olasılıkla, bu örneği dağıtmak için kullanılan Azure AD etki alanından farklı olan Azure AD etki alanının şu anki uygulama örneğinde oturum açtınız. Office Masaüstü uygulamaları kullanılarak düzenleme için şablonları depolamak amacıyla kullanılan SharePoint hizmeti, aynı etki alanına ait olduğundan SharePoint hizmete erişim için gereken izinlere sahip değildir. Bu sorunu gidermek için, doğru Azure AD etki alanı olan bir kullanıcının kimlik bilgilerini kullanarak geçerli örnekte oturum açın.

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik raporlamaya genel bakış](general-electronic-reporting.md)

[OPENXML formatında raporların oluşturulması için bir yapılandırma tasarlama](tasks/er-design-reports-openxml-2016-11.md)

[Word biçiminde raporlar oluşturmak için ER yapılandırmaları tasarlama](tasks/er-design-configuration-word-2016-11.md)

[Er kullanarak oluşturduğunuz belgelere resimler ve şekiller katıştırma](electronic-reporting-embed-images-shapes.md)

[Power BI'ya veri çekmek için Elektronik raporlamayı yapılandırma](general-electronic-reporting-report-configuration-get-data-powerbi.md)
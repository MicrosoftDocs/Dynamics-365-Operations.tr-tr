---
title: Elektronik raporlama (ER) genişletilmiş biçim araması
description: Bu konu, gerekli biçim Global havuzda depolandığı zaman, ER biçim aramasında bir ER biçim başvurusunun nasıl ayarlanacağını açıklamaktadır.
author: NickSelin
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: baba699a1b8efc986b4b274b8faf143d24d69e96
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355793"
---
# <a name="allow-users-to-set-up-an-er-format-reference-inquiring-a-format-from-the-global-repository"></a>Kullanıcıların, Global havuzdan bir biçim sorgulayan ER biçimi başvurusu ayarlamalarına izin verme

[!include [banner](../includes/banner.md)]

giden belgelerin [biçimlerini](general-electronic-reporting.md#FormatComponentOutbound) çeşitli ülkelerin/bölgelerin yasal gereksinimlerine uygun şekilde yapılandırmak için [Elektronik raporlama](general-electronic-reporting.md) (ER) çerçevesini kullanabilirsiniz. Ayrıca, giden belgelerin ayrıştırılması için [biçimleri](general-electronic-reporting.md#FormatComponentInbound) yapılandırmak ve uygulama verilerini eklemek ya da güncelleştirmek için bu belgelerdeki bilgileri kullanmak için de ER çerçevesini kullanabilirsiniz. Bu biçimlerin her biri, Dynamics 365 Finance kurulumunuzda, belirli bir iş sürecinin parçası olarak gelen veya giden iş belgelerini işlemek için kullanılabilir.

Genellikle, belirli bir iş sürecinde hangi ER biçiminin kullanılması gerektiğini belirtmeniz gerekir. Bunu yapmak için, iş sürecine özgü parametrelerin bir parçası olarak yapılandırılan bir arama alanında tek bir ER biçimi seçin. Bu arama alanları genellikle ER çerçevesinin uygun API'sını kullanarak uygulanır. Daha fazla bilgi için bkz. [ER çerçevesi API'sı - bir biçim eşleme aramasını görüntülemek için kod](er-apis-app73.md#code-to-display-a-format-mapping-lookup).

Örneğin, [dış ticaret parametreleri](../../../finance/localizations/emea-intrastat.md#set-up-foreign-trade-parameters) yapılandırdığınızda, Intrastat beyannamesini ve Intrastat beyanname denetim raporunu oluşturmak için kullanılacak bireysel ER biçimlerine başvuruları ayarlamanız gerekir. Aşağıdaki ekran görüntüleri, **Dış ticaret parametreleri** sayfasında ER biçimleri arama alanının nasıl göründüğünü gösteriyor.

Geçerli Finance kurulumunda intrastat iş süreciyle ilgili ER biçimleri yoksa bu arama alanı boş olacaktır.

[![Dış ticaret parametreleri sayfası.](./media/ER-ExtLookup-Lookup1.gif)](./media/ER-ExtLookup-Lookup1.gif)

Geçerli Finance kurulumunda Intrastat iş süreciyle ilgili ER biçimleri varsa, bu arama alanı ER biçimlerini sunar.

[![Dış ticaret parametreleri sayfası.](./media/ER-ExtLookup-Lookup2.png)](./media/ER-ExtLookup-Lookup2.png)

Bu arama, yalnızca geçerli Finance kurulumunda zaten içe aktarılmış olan ER biçimlerini sunar. ER çözümlerini geçerli Finance kurulumunda [içe aktarmak için](./tasks/er-import-configuration-lifecycle-services.md), ER biçimlerini içeren ER çözümlerinin [yaşam döngüsünü](general-electronic-reporting-manage-configuration-lifecycle.md) destekleyen ilgili ER çerçevesi işlevini çalıştırmak için izinleriniz olmalıdır.

Finance 10.0.9 sürümünden (Nisan 2020 sürümü) başlayarak, ER çerçevesi API'sı kullanarak uygulanan ER biçim aramasının kullanıcı arabirimi genişletilmiştir. **Biçim yapılandırmasını seç** hızlı sekmesindeki varolan ER biçimlerini yine de seçebilirsiniz. Ayrıca, genişletilmiş arama, belirli ER biçimlerini bulmak için Genel depoda (GR) arama yapmak için yeni bir seçenek sunar. GR'nin tüm ER biçimleri **Global havuzdan içe aktar** hızlı sekmesinde sunulur.

[![Dış ticaret parametreleri sayfası.](./media/ER-ExtLookup-Lookup3.png)](./media/ER-ExtLookup-Lookup3.png)

**Biçim yapılandırmasını seç** hızlı sekmesine benzer şekilde, **Global havuzdan içe aktar** hızlı sekmesi yalnızca bu arama alanında bir ER biçiminin seçildiği iş süreci için uygun olan ER biçimlerini gösterir. Bu örnekte, Intrastat beyannamesinin oluşturulması gösterilmektedir. ER biçimi, şirket ülke içeriğine bağlı olarak kullanıcının oturum açtığı şirket için geçerlidir.

**Global havuzdan içe aktar** hızlı sekmesinde bir ER biçimi seçtiğiniz zaman, seçilen ER biçimi [yapılandırması](general-electronic-reporting.md#Configuration), GR'den geçerli Finance kurulumuna aktarılır.

[![Dış ticaret parametreleri sayfası.](./media/ER-ExtLookup-FormatImport.png)](./media/ER-ExtLookup-FormatImport.png)

Bunun ardından içe aktarma işlemi başarıyla tamamlandıysa, içe aktarılan ER biçimine başvuru bu arama alanında depolanır. GR'ye ilk kez eriştiğinizde, GR depolama alanına erişimi yönetmek için kullanılan [Regulatory Configuration Service](https://aka.ms/rcs)'e (RCS) kaydolmak için verilen bağlantıyı izlemeniz gerekir.

[![Dış ticaret parametreleri sayfası.](./media/ER-ExtLookup-RepoSignUp.png)](./media/ER-ExtLookup-RepoSignUp.png)

Varsayılan olarak, **Global havuzdan içe aktar** hızlı sekmesi, performans iyileştirmeleri için GR içeriğine göre otomatik olarak oluşturulan geçici depolamadan gelen ER biçimlerinin listesini sunar. Bu durum, **Genel havuzdan içe aktar** hızlı sekmesi ilk kez açıldığında olur ve birkaç saniye alabilir.

**Global havuzdan içe aktar** hızlı sekmesinde gerekli ER biçimini görmüyorsanız ancak bu ER biçiminin GR'de depolandığından eminseniz **Eşitle** seçeneğini belirleyin. Bu seçenek, geçici depolama alanını güncelleştirir ve GR'nin geçerli içeriğiyle eşitler.

## <a name="feature-activation"></a>Özellik etkinleştirme

Bu işlevselliğin kullanılabilirliği, **Özellik yönetimi**'ndeki **Global havuzu sorgulamaya izin veren ER biçimi yapılandırmaları için genişletilmiş arama** özelliğiyle kontrol edilir. Varsayılan olarak bu özellik etkindir.

[![Özellik yönetimi sayfası.](./media/ER-ExtLookup-FeatureMngt.png)](./media/ER-ExtLookup-FeatureMngt.png)

## <a name="security-considerations"></a>Güvenlik ile ilgili hususlar

**Yapılandırma havuzlarını koru** (**ERMaintainSolutionRepositories**) ayrıcalığı, **Global havuzdan içe aktar** hızlı sekmesi etkin durumdayken ER biçim aramasını açan kullanıcı için GR'ye erişimi kontrol eder. Kullanıcıların ER biçimi aramalarından GR içeriğine erişmelerine izin vermek için, kullanıcılara, atanmış rol ve sorumluluklarını kullanıp veya doğrudan **ERMaintainSolutionRepositories** ayrıcalığı vererek güvenlik ayarlarını değiştirmeniz gerekir.

Aşağıdaki ekran görüntüsünde, **Muhasebeci** rolüne atanmış kullanıcılara bu ayrıcalığın nasıl verilebileceği gösterilmektedir. Bu rol, kullanıcıların **Dış ticaret parametreleri** sayfasındaki **Dosya biçimi** ve **Rapor biçimi eşleme** alanlarında dış ticaret parametrelerini yapılandırmalarına ve ER biçimlerine başvuruları ayarlamalarına izin verir.

[![Güvenlik yapılandırması sayfası.](./media/ER-ExtLookup-SecuritySetting.png)](./media/ER-ExtLookup-SecuritySetting.png)

## <a name="limitations"></a>Sınırlamalar

ER biçim aramasında GR'ye erişim şu anda yalnızca giden belgeler oluşturmak için kullanılan ER biçimlerinin seçimi için desteklenmektedir.

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

### <a name="why-cant-i-access-the-global-repository-from-the-er-format-lookup"></a>ER biçimi aramadan Global havuza neden erişemiyorum?

**Özellik yönetimi** sayfasında **Global havuzu sorgulamaya izin veren ER biçimi yapılandırmaları için genişletilmiş arama** özelliğini etkinleştirdiyseniz ancak **Global havuzdan içe aktar** hızlı sekmesinde ER biçimlerini göremiyorsanız ve **Eşitle** seçeneği görünür olduğu halde devre dışıysa, kullanıcıya **Yapılandırma havuzlarını koru** (**ERMaintainSolutionRepositories**) ayrıcalığının verildiğinden emin olun. Bu ayrıcalığı almak için sistem yöneticinizle iletişime geçin.

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)
- [Elektronik raporlama (ER) çerçevesi API'sı](er-apis-app73.md)
- [Elektronik raporlama (ER) yapılandırması yaşam döngüsünü yönetme](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
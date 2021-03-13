---
title: Üretim ve ambar yönetimi iş yükleri için bulut ve uç ölçek birimleri
description: Bu konu, üretim ve ambar yönetimi iş yükleri için bulut ve uç ölçek birimleri hakkında bilgi sağlar.
author: cabeln
manager: ''
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 28301cdfb86d00ea6f04e996fe7fb1485e83b2d4
ms.sourcegitcommit: 289e9183d908825f4c8dcf85d9affd4119238d0c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104976"
---
# <a name="cloud-and-edge-scale-units-for-manufacturing-and-warehouse-management-workloads"></a>Üretim ve ambar yönetimi iş yükleri için bulut ve uç ölçek birimleri

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bulut ve uç ölçek birimleri atölye ve ambar yürütme iş yüklerinin farklı ortamlar arasında dağıtılmasını sağlar. Bu işlevsellik, performansın artırılmasına, hizmet kesintilerinin önlenmesine ve çalışma süresini en üst düzeye çıkarılmasına yardımcı olabilir. Aşağıdaki eklentiler tarafından sağlanır:

- Dynamics 365 Supply Chain Management için Bulut Ölçek Birimi Eklentisi
- Dynamics 365 Supply Chain Management için Uç Ölçek Birimi Eklentisi

Üretim ve dağıtım ile çalışan şirketler, önemli iş süreçlerini kesintiye uğramadan ve büyük ölçekte 7/24 çalıştırabilmelidir. Bulut ve uç ölçek birimleri, şirketlerin zaman zaman ağ bağlantısı veya gecikme sorunlarıyla karşılaşsalar bile, görev açısından kritik öneme sahip önemli üretim ve ambar işlemlerini kesintisiz olarak yürütmelerine olanak tanır.

## <a name="public-preview-information"></a>Genel önizleme bilgileri

Önizleme, Dynamics 365 Supply Chain Management ortamınızın bulut tabanlı hub'ı olarak işlev yapan bir ortam ve bulut ölçek birimi olarak işlev yapan bir ortam sağlar.

<!-- You will also be able to use Local Business Data (LBD) to configure an on-premises environment as an edge scale unit for the hub you received as part of the preview program.-->

### <a name="preview-availability"></a>Önizlemenin kullanıma sunulması

Bulut ve uç ölçek birimlerinin önizlemesi, Supply Chain Management'ın mevcut müşterileri için Ekim 2020'de kullanıma sunulmuştur.

[Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) ortamınızdaki dağıtım için Ekim önizleme sürümü 10.0.15/Platform güncelleştirmesi 39'a erişmek için Supply Chain Management için önizleme erken erişim programının (PEAP olarak da bilinir) bir parçası olmalısınız. Zaten daha geniş [Dynamics Insider Program](https://experience.dynamics.com/insider)'ın bir üyesiyseniz PEAP'ye katılabilirsiniz. "Finance & Operations: Önizleme erken erişim programı (PEAP)" adlı programı seçin.

> [!IMPORTANT]
> Supply Chain Management için ölçek birimi özelliği, yalnızca [ Finance and Operations için Bulut + Uç Önizlemesi koşullarını](https://Aka.ms/SCMCnETerms) kabul ederseniz kullanıma sunulur.

### <a name="data-processing-for-the-preview"></a>Önizleme için veri işleme

Genel önizleme sırasında, bazı yönetim hizmetleri yalnızca ABD'de barındırılacaktır. Ancak, özellik genel kullanıma sunulduğunda, bu yönetim hizmetleri Supply Chain Management tarafından desteklenen tüm coğrafyalarda kullanılabilir hale getirilecektir. Bu, ölçek birimi yöneticisi tarafından kullanılan yönetim bilgilerinin aktarılmasını ve depolanmasını etkiler:

- Kiracı adlarınız ve kimlikleriniz
- LCS proje kimlikleriniz
- Oturum açmak için kullanılan yönetici e-posta adresleri
- Hub ve ölçek birimleri için ortam kimlikleri
- İş yükü yapılandırmaları
- Eşleme analizi sayfasında görüntülenen toplanan ölçümler (gecikme ve aktarım hızı gibi)

Önizleme ortamlarınız kapatıldığında, ABD veri merkezlerine aktarılan ve ABD veri merkezlerinde depolanan veriler silinir.

### <a name="sign-up-for-the-preview"></a>Önizleme için kaydolma

Supply Chain Management için bulut ve uç önizlemesine kaydolmak için kuruluşunuzun zaten çevrimiçi bir Supply Chain Management bulut ortamına sahip olması gerekir.

Ölçek birimi özellikleri şu anda genel önizleme sürümündedir. Kaydolduğunuzda, belirli bir kiracı üzerinde bir kullanıcı hesabı kullanmanız gerekir. Ayrıca, o kiracıdaki etkin Dynamics 365 LCS projesi için LCS'de proje sahibi veya ortam yöneticisi olmalısınız.

Önizlemeye kaydolduğunuzda, bir kiracı seçecek ve kayıt adımlarını uygulayacaksınız. Microsoft önizleme kapasitesi ayırdığı anda, size uygun LCS projesine yönelik iki ortam (hub ve ölçek birimi) için hazırlama ayrıntılarını ve promosyon kodlarını içeren bir e-posta göndereceğiz. Daha sonra iki ortamı katman 2 korumalı alan ortamı olarak dağıtabilirsiniz. Bu ortamlar, promosyon kodlarının oluşturulacağı tarihten itibaren 60 gün geçerli olacaktır. Bir sonraki paragrafta açıklanan adım tamamlanana kadar iki ortamı kullanmamalısınız.

İki ortamın promosyon kodları kullanılarak dağıtıldığını Microsoft'tan doğruladıktan sonra, ortamlardan biri hub olarak çalışacak şekilde yapılandırılır ve diğeri ölçek birimi olarak çalışacak şekilde yapılandırılır. Daha sonra ölçek birimlerini yapılandırabilir ve [Ölçek Birimi Yöneticisi portalını](https://aka.ms/SCMSUM) kullanarak seçilen ambar yönetimi ve üretim iş yüklerini dağıtabilirsiniz.

Önizleme ortamları 60 gün sonra otomatik olarak silinir. Ancak, kullanılmadığı görünüyorsa, bunlar daha erken silinebilir. Önizleme ortamlarınız silindikten sonra, yeni bir önizleme dağıtımı için kaydolabilir ve sıraya girebilirsiniz.

Önizlemeye kaydolmak için [Ölçek Birimi Yöneticisi portalına](https://aka.ms/SCMSUM) gidin.

### <a name="limitations-that-apply-during-the-preview-period"></a>Önizleme döneminde uygulanan sınırlamalar

> [!IMPORTANT]
> Bu özellik için önizleme programının ilk aşamasında Microsoft, uç ölçek birimlerine sahip hub'ları değil, yalnızca bulut ölçek birimlerine sahip hub'ları destekler. Uç ölçek birimleri şirket içinde yüklenir ve programın yaklaşan bir aşamasında kullanıma sunulması beklenmektedir.

Bulut ve uç ölçek birimleri bir önizleme özelliği olduğundan, bunlarla ilgili hizmetler şu anda sınırlı ülke ve bölgelerde kullanılabilir. Bulut ve uç ölçek birimlerini etkinleştirerek, bulut ve uç ölçek birimlerinin yapılandırması ve işlenmesiyle ilgili bazı verilerin ABD'de bulunan bir veri merkezinde depolanabileceğini anladığınızı onaylamış olursunuz. Bulut ve uç ölçek birimlerini etkinleştirerek [Finance and Operations için Bulut + Uç Önizlemesi koşullarını](https://Aka.ms/SCMCnETerms) da kabul etmiş olursunuz. Bulut ve uç ölçek birimleri hakkında daha fazla bilgi edinmek için [belgelere](https://aka.ms/scmcne) bakın.

Gizliliğiniz Microsoft için önemlidir. Daha fazla bilgi için [Gizlilik Bildirimimizi](https://aka.ms/privacy) okuyun.

> [!IMPORTANT]
> Ölçek birimlerinde iş yükleri kullanıldığında, genel önizlemedeki bazı iş işlevleri tam olarak desteklenmez. İşlevsel iş yükleri hakkında daha fazla bilgi için bu konunun ilerleyen bölümlerine bakın.

## <a name="scale-units-and-dedicated-workloads"></a>Ölçek birimleri ve özel iş yükleri

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Ölçek birimlerini içeren Dynamics 365":::

Ölçek birimleri, özel işleme kapasitesi ekleyerek merkezi Supply Chain Management hub ortamınızı genişletir. Ölçek birimleri bulutta çalışabilir. Alternatif olarak, yerel tesislerde uçta da çalıştırabilirsiniz. Ölçek birimlerinin hub ortamıyla bağlantısı geçici olarak kesilebilir. Bunlar bağlandıklarında, ölçek birimleri atanan iş yükleri için özel işlemeyi çalıştırmak için gereken tüm bilgileri alır.

:::image type="content" source="media/cloud_edge-previewoptions.png" alt-text="Genel önizlemedeki ölçek birimi seçenekleri":::

Genel önizleme için Ölçek Birimi Yöneticisi portalını kullanarak bulut ölçek biriminde seçili iş yükleriyle bir hub ortamını yapılandırabilirsiniz. Yerel İş Verilerine (LBD) şirket içi ortamda erişimi olan önizleme katılımcıları, LBD ortamını uç ölçek birimi olarak da yapılandırabilir.

İş yükü, hariç tutulup bir ölçek birimine devredilebilen tanımlanmış bir iş işlevselliği kümesidir. Şu anda, önizleme özellikleri iki tür iş yükü sunar:

- Üretim yürütme
- Ambar yönetimi

Ölçek birimi başına her iş yükü türünden birini atayabilirsiniz. 

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Bir ölçek birimindeki özel üretim yürütme iş yükü özellikleri

Üretim yürütmede, bulut ve edge ölçek birimleri, ölçek buluta bağlı olmasalar bile aşağıdaki özellikleri sağlar:

- Makine operatörleri ve üretim katı denetçileri operasyonel üretim planına erişebilirler.
- Makine operatörleri, gizli ve süreç üretim işleri çalıştırarak planı güncel tutabilir.
- Üretim katı denetçisi, çalışma planını ayarlayabilir.
- Çalışanlar, doğru çalışan maaşı hesaplamasını sağlamak için kenardan giriş ve çıkış zamanlarına erişebilirsiniz.

Daha fazla bilgi için [üretim ölçek birimi iş yükü ayrıntıları](cloud-edge-workload-manufacturing.md) bölümüne bakın.

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Bir ölçek birimindeki özel ambar yönetimi iş yükü özellikleri

Ambar yönetiminde, bulut ve uç ölçek birimleri, ölçek buluta bağlı olmasalar bile aşağıdaki özellikleri sağlar:

- Satış siparişleri ve talep stok yenileme için seçili dalga yöntemlerinin işlenmesi etkindir.
- Ambar çalışanları, ambar uygulamasını kullanarak satış ve talep stok yenileme ambar işlerini çalıştırabilir.
- Ambar çalışanları, ambar uygulamasını kullanarak eldeki stokta sorgu çalıştırabilirler.
- Ambar çalışanları ambar uygulamasını kullanarak stok hareketleri oluşturabilir ve çalıştırabilir.
- Ambar çalışanları satın alma siparişlerini kaydedebilir ve ambar uygulamasını kullanarak siparişleri kaydedebilir.

Daha fazla bilgi için [ambar ölçek birimi iş yükü ayrıntıları](cloud-edge-workload-warehousing.md) bölümüne bakın.

## <a name="onboard-scale-units-for-your-supply-chain-management-environment"></a>Supply Chain Management ortamınız için dahili ölçek birimleri

### <a name="deploy-the-preview-for-cloud-and-edge-scale-units"></a>Bulut ve uç ölçek birimleri için önizlemeyi dağıtma

Aşağıdaki resimde, bulut ölçe birimlerine yönelik genel önizleme için kaydolma ve sağlama akışı gösterilmektedir.

:::image type="content" source="media/cloud_edge-previewsignup.png" alt-text="Kayıt adımlarını önizleme":::

### <a name="select-your-lcs-project-tenant-and-the-detailed-preview-process"></a>LCS projesi kiracınızı ve ayrıntılı önizleme işlemini seçin

Genel önizlemede, [Ölçek Birimi Yöneticisi portalı](https://aka.ms/SCMSUM), hesabınızın parçası olduğu ve bir LCS projesinin sahibi veya ortam yöneticisi olduğunuz kiracıların listesini gösterir.

Aradığınız kiracı bu listede yoksa [LCS](https://lcs.dynamics.com/v2)'ye gidin ve bu kiracı için bir ortam yöneticisi veya LCS projesinin proje sahibi olduğunuzdan emin olun. Seçilen kiracının yalnızca  Azure Active Directory(Azure AD) hesaplarının kayıt deneyimini tamamlama yetkisine sahip olduğunu unutmayın.

> [!NOTE]
> LCS'ye değişiklik uyguladıktan sonra, kiracı listesinde değişikliklerin yansıması 30 dakika kadar sürebilir.

Her kiracı için liste, kaydolma durumunu gösterir.

:::image type="content" source="media/cloud_edge-Signup1.png" alt-text="Kiracı için kaydolma seçeneği":::

LCS kiracınızın önizlemeye katılması için **Kaydolmak için buraya tıklayın** bağlantısını seçin. Koşulları kabul etmelisiniz. Ayrıca, Microsoft'un önizleme kayıt işlemiyle ilgili iletişimleri gönderebileceği bir iş e-posta adresi de sağlamanız gerekir.

:::image type="content" source="media/cloud_edge-Signup2.png" alt-text="Kiracı için kayıt gönderme":::

Microsoft, kayıt formunda sağladığınız adrese bir e-posta göndererek isteğinizi gözden geçirecek ve sonraki adımlar hakkında sizi bilgilendirecektir.

Önizleme programına erişim izni aldıktan sonra, LCS projeniz için iki promosyon kodu alırsınız. Artık bu promosyon kodlarını Kullanarak LCS'de iki ortam dağıtabilirsiniz. Ortamlar PEAP 10.0.15 veya sonraki sürümünü kullanmalıdır. Promosyon kodlarını uygulamayı bitirdiğinizde, önizleme özellikleri için ortamları etkinleştirme işini bitirebilmemiz için Microsoft'a bildirin (talimat verildiği şekilde). Microsoft, bu yapılandırma adımı tamamlandığında size bildirecektir.

Artık önizleme ortamınızda ölçek birimlerini ve iş yüklerini yapılandırmaya başlayabilirsiniz.

> [!IMPORTANT]
> Bulut ölçek birimlerini yapılandırdığınızda, [Ölçek Birimi Yöneticisi portalında gerekli tüm adımları yapabilirsiniz](#scale-unit-manager-portal).
<!-- 
> If want to use edge scale units with your preview deployment, you must do all scale unit configuration in the user interface on the hub as described in [Configure the hub environment for use with edge scale units](cloud-edge-edge-scale-units-lbd.md#configure-the-hub-environment). You can't use Scale Unit Manager portal if you include an edge scale unit. -->

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>Ölçek Birim Yöneticisi portalını kullanarak bulut ölçek birimlerini ve iş yüklerini yönetme

[Ölçek Birimi Yöneticisi portalına](https://aka.ms/SCMSUM) gidin ve kiracı hesabınızı kullanarak oturum açın. **Ölçek birimlerini yapılandır** sayfasında, önceden listelenmemişse bir hub ortamı ekleyebilirsiniz. Daha sonra ölçek birimleri ve iş yükleri ile yapılandırmak istediğiniz hub'ı seçebilirsiniz.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Ölçek birimi ve iş yükü yönetimi deneyimi":::

Topolojinizde bulunan bir veya daha fazla ölçek birimini eklemek için **Ölçek birimleri ekle**'yi seçin. Önizlemede, önizleme programının bir parçası olarak aldığınız promosyon kodlarından birinden dağıttığınız bulut ölçek birimini görmeniz gerekir.

<!--  [!IMPORTANT]
> In the public preview, the Scale Unit Manager portal shows the cloud scale unit that you received as part of the preview program. Any edge scale unit that you created based on an LBD configuration can't be managed in the Scale Unit Manager portal yet. For configuration details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md) -->

**Tanımlanan iş yükleri** sekmesinde, ölçek birimlerinizden birine ambar yönetimi veya üretim yürütme iş yükü eklemek için **İş yükü oluştur** düğmesini kullanın. Her iş yükü için iş yükü tarafından sahip olunacak işlemlerin bağlamını belirtmeniz gerekir. Ambar yönetimi iş yükleri için bağlam, belirli bir tesis ve tüzel kişilikteki belirli bir ambardır. Üretim yürütme iş yükleri için bağlam, tüzel kişilikteki belirli bir tesistir.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="İş yükü oluşturma":::

> [!IMPORTANT]
> Önizlemedeki Ölçek Birimi Yöneticisi portalı, ölçek birimlerindeki iş yüklerini kaldırmanıza veya atama yapıldıktan sonra bir ölçek birimini hub'dan atamanıza izin vermez. Bir atamayı kaldırmanız gerekiyorsa önizleme programı yönetimi için ilgili kişiye ulaşın.

<!-- ### Create an edge scale unit using your custom on-premises hardware appliance

In the public preview, you can create on-premises edge scale units on your custom hardware using the LBD environments. For details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md). -->

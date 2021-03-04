---
title: İş belgesi yönetiminde yeni belge kullanıcı arabirimi
description: Bu konu, Elektronik raporlama (ER) çerçevesinin İş belge yönetimi özelliğindeki yeni belge kullanıcı arabiriminin (UI) nasıl kullanılacağı hakkında bilgi vermektedir.
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 2cb6e0da4af07b9b8486bf1e5bda29523cbd08e9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681364"
---
# <a name="new-document-user-interface-in-business-document-management"></a>İş belgesi yönetiminde yeni belge kullanıcı arabirimi

[!include [banner](../includes/banner.md)]

İş belgesi yönetimi iş kullanıcılarının Microsoft 365 hizmeti veya uygun Microsoft Office masaüstü uygulamasını kullanarak iş belgesi şablonlarını düzenlemesini sağlar. Düzenlemeler tasarım değişiklikleri veya yeni dağıtımlar içerebilir ya da kullanıcılar kaynak kodunu değiştirmeden ek veri eklemek için yer tutucular ekleyebilirler. İş belgesi yönetimiyle nasıl çalışılacağı hakkında daha fazla bilgi için bkz. [İş belgesi yönetimine genel bakış](er-business-document-management.md).

Yeni belge kullanıcı arabirimi (UI) daha net ve kullanımı daha rahat. **İş belgesi** alanı, yalnızca, geçerli sağlayıcı için kullanılabilen şablonları gösterir.

**Yeni belge** düğmesi, kullanıcıların başka bir sağlayıcı tarafından sağlanan bir Elektronik raporlama (ER) biçimi yapılandırmasında şablon oluşturmalarına ve düzenlemelerine olanak sağlar. Bu konudaki örnekte sağlayıcı Microsoft'tur.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>İş belgesi yönetiminde yeni belge kullanıcı arabirimini kullanıma açma

İş belgesi yönetiminde yeni belge kullanıcı arabirimini kullanmaya başlamak için,**Özellik yönetimi** çalışma alanındaki **İş belgesi yönetimi için Office benzeri arabirim deneyimi** özelliğini açmanız gerekir.

Bu özelliği tüm tüzel kişilikler için açmak üzere bu adımları izleyin.

1. **Özellik yönetimi** çalışma alanında, **Yeni** sekmesinde, listeden **İş belgesi yönetimi için Office benzeri arabirim deneyimi**'ni seçin.
2. Seçili özelliği açmak için **Şimdi etkinleştir**'i seçin.
3. Yeni özelliğe erişmek için sayfayı yenileyin.

### <a name="edit-templates-that-are-owned-by-other-providers"></a>Sahibi diğer sağlayıcılar olan düzenleme şablonları

1. **İş belgesi yönetimi** çalışma alanında **Yeni belge**'yi seçin.

    ![İş belgesi yönetimi çalışma alanı](./media/BDM_overview_new_template1.png)

2. İletişim kutusunda, şablon olarak kullanılacak belgeyi ve ardından **Belge oluştur**'u seçin.

    ![İş belgeleri iletişim kutusu](./media/BDM_overview_new_template2.png)

3. Yeni iletişim kutusunda, **Başlık** alanında, başlığı gerektiği gibi değiştirin. Başlık metni, otomatik olarak oluşturulan yeni ER biçimi yapılandırmasını adlandırmak için kullanılır. Bu yapılandırmanın taslak sürümü (**Müşteri FTI raporu (GER) kopyası**) düzenlenen şablonu içerir ve bu ER biçimini geçerli kullanıcı için çalıştırmak üzere kullanılır. Temel ER biçimi yapılandırmasındaki özgün şablon, diğer kullanıcıların tümü için bu ER biçimini çalıştırmada kullanılacaktır.
4. **Ad** alanında, düzenlenebilir şablonun otomatik olarak oluşturulacak ilk revizyonunun adını değiştirin.
5. **Yorum** alanında, düzenlenebilir şablonun otomatik olarak oluşturulacak revizyonuna için yorumları güncelleştirin.
6. Düzenleme işleminin başlangıcını onaylamak için **Tamam**'ı seçin.

    ![Belge oluşturma iletişim kutusu](./media/BDM_overview_new_template3.png)

**Yeni belge** düğmesi, kullanıcıların başka bir sağlayıcı tarafından sağlanan bir ER biçimi yapılandırmasında şablon oluşturmak ve düzenlemek için kullanılır. Bu örnekte sağlayıcı Microsoft'tur. **Yeni belge**'yi seçtiğiniz zaman, sahibi geçerli ve diğer sağlayıcılar olan tüm şablonları görüntüleyebilirsiniz. Siz şablonu seçtikten sonra şablon düzenleme için açılır. Düzenlenen şablon daha sonra otomatik olarak oluşturulan yeni bir ER biçim yapılandırması içinde depolanır.

Daha fazla bilgi için bkz. [İş belgesi yönetimine genel bakış](er-business-document-management.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
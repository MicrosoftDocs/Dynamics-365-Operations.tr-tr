---
title: Örneği kaldırma
description: Bu konuda, Microsoft Dynamics 365 Human Resources için bir test sürüşü kaldırma yeni bir üretim ortam işlemi adım adım anlatılmaktadır.
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4256938be70f301d3d7b7663f10addb19725b048
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859647"
---
# <a name="remove-an-instance"></a>Örneği kaldırma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Microsoft Dynamics 365 Human Resources için bir test sürüşünün veya üretim ortamının kaldırılması süreci açıklanmaktadır.

## <a name="remove-a-test-drive-environment"></a>Bir test ortamını kaldırma

İnsan Kaynakları test ortamları 60 günlük süre sonu ilkesi ile sunulur. Ancak, test ortamları sahipleri aşağıdaki adımları uygulayarak denemelerini daha erken sonlandırabilir. 

1. [Power Apps Yönetim Merkezi](https://admin.businessplatform.microsoft.com/)'ne gidin.
2. **Ortamlar**'ı seçin.
3. Test ortamını seçin. Test ortamı adı şuna benzer bir düzene sahiptir: TestDrive - alias@domain
4. **Sil**'i seçin ve kararı onaylayın. 

Var olan test ortamı kaldırılır. Kaldırıldığında, yeni bir test ortamı için kaydolabilirsiniz. 

## <a name="remove-a-production-environment"></a>Bir üretim ortamını kaldırma

Bu konuda, İnsan Kaynaklarını bir Bulut Çözümü Sağlayıcısı (CSP) veya kurumsal mimari (EA) sözleşmesi aracılığıyla aldığınız varsayılır. 

Tek bir İnsan Kaynakları ortamı tek bir Power Apps ortamı içinde "yer aldığından", dikkate alınması gereken iki seçenek vardır. İlk seçenek tüm Power Apps ortamını kaldırmayı, ikinci seçenek yalnızca İnsan Kaynakları'nı kaldırmayı içerir. İlk seçenek, Power Apps ortamını özellikle İnsan Kaynakları sağlamak için oluşturmuş, uygulamaya henüz başlamış veya herhangi bir tümleştirme yapmamış olmanız durumunda tercih edilir. İkinci seçenek Power Apps ve Power Automate'ten alınan zengin verilerle doldurulan bir Power Apps ortamınız olması durumunda uygundur.

> [!Important]
> Power Apps ortamını kaldırmadan önce, İnsan Kaynakları kapsamı dışındaki zengin veri tümleştirmeleri için kullanılmadığından emin olun. Varsayılan Power Apps ortamlarının da kaldırılamayacağını unutmayın. 

İnsan Kaynakları ve ilişkili uygulamalar ve akışlar dahil tüm Power Apps ortamını kaldırmak için:

1. [Power Apps Yönetim Merkezi](https://admin.businessplatform.microsoft.com/)'ne gidin.
2. **Ortamlar**'ı seçin.
3. Kaldırılacak ortamı seçin.
4. **Sil**'i seçin ve kararı onaylayın. 
5. Silme işlemi tamamlanana kadar bekleyin.
6. İnsan Kaynakları'na abone olmak için kullandığınız hesabı kullanarak [Lifecycle Services](https://lcs.dynamics.com/Logon/Index)'da (LCS) oturum açın. 
7. Ortamı içeren İnsan Kaynakları Projesini seçin. 
8. LCS projenizde **İnsan Kaynakları Uygulama Yöneticisi** kutucuğunu seçin. 
9. Kaldırılacak örneği seçin. 
10. **Örneği kaldır**'ı seçin ve ardından kararınızı onaylayın.  

İnsan Kaynakları ortamını mevcut bir Power Apps ortamından kaldırmak için aşağıdaki adımları uygulayın. Bu özellik doğrudan LCS içinden etkinleştirilene kadar, İnsan Kaynakları DevOps ekibine başvurmak ve destek almak geçicidir.

1. Kaldırma isteğini başlatmak için Destek birime başvurun.
2. Destek ekibi İnsan Kaynakları DevOps ekibiyle kaldırma isteğini başlatacaktır. 
3. Ortamın kaldırıldığı hakkında bilgi aldıktan sonra devam edin.
4. İnsan Kaynaklarına abone olmak için kullandığınız hesabı kullanarak LCS'de oturum açın. 
5. Ortamı içeren İnsan Kaynakları Projesini seçin. 
6. LCS projenizde **İnsan Kaynakları Uygulama Yöneticisi** kutucuğunu seçin. 
7. Kaldırmak istediğiniz örneği seçin. Bu örneğin Dağıtım durumu **Silindi** olarak işaretlenmiş olmalıdır.
8. **Örneği kaldır**'ı seçin ve ardından kararınızı onaylayın. 

## <a name="recover-a-soft-deleted-environment"></a>Geçici olarak silinen bir ortamı kurtarma

Human Resources ortamınızın bağlı olduğu Power Apps ortamını yazılımla silerseniz, Lifecycle Services'te İnsan Kaynakları ortamının durumu **Geçici olarak silindi** olur. Bu durumda, kullanıcılar Human Resources'a bağlanamaz.

Ortamı geri yüklemek için:

1. [Power Apps ortamını kurtarma](/power-platform/admin/recover-environment) bölümündeki yönergeleri uygulayın.

2. Human Resources ortamını geri yüklemek için Destek birimine başvurun. Daha fazla bilgi için [Destek alma](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md) bölümüne bakın.

> [!Warning]
> Power Apps ortamları silme işleminden sonra yalnızca yedi gün süreyle kaydedilir. Ortamı yedi gün içinde kurtarmanız gerekir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

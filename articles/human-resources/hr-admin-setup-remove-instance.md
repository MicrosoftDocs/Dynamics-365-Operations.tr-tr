---
title: Örneği kaldırma
description: Bu makalede, Microsoft Dynamics 365 Human Resources için bir test sürüşünün veya üretim ortamının kaldırılması süreci tanımlanmaktadır.
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
ms.openlocfilehash: 0ce676c93e133cc04ad9c49417ed2ca0d6791e93
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178487"
---
# <a name="remove-an-instance"></a>Örneği kaldırma

_**Uygulandığı Öğe** tek başına çalışan altyapıda İnsan Kaynakları_ 

> [!NOTE]
> Temmuz 2022 tarihinden başlayarak tek başına İnsan Kaynakları altyapısında yeni İnsan Kaynakları ortamları sağlanamaz ve burada yeni Microsoft Dynamics Lifecycle Services (LCS) projeleri oluşturulamaz. Müşteriler, İnsan Kaynakları ortamları yalnızca finans ve operasyon altyapısı üzerinden dağıtılabilir. Daha fazla bilgi için bkz. [Finans ve operasyon altyapısında İnsan Kaynakları sağlama](/hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Finans ve operasyon uygulama altyapısı bir ortamın silinmesini destekler. Bir ortamın nasıl silineceği hakkında daha fazla bilgi için bkz. [Bir ortam silme](../fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure.md#delete-an-environment).

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

Tek bir İnsan Kaynakları ortamı tek bir Power Apps ortamı içinde yer aldığından, bir ortamı kaldırırken dikkate alınması gereken iki seçenek vardır. 
- **Tüm Power Apps ortamını kaldırın.** Bu seçenek, Power Apps ortamını özellikle İnsan Kaynakları sağlamak için oluşturulmuş, uygulamaya henüz başlamış veya herhangi bir tümleştirme yapmamış olmanız durumunda tercih edilir.  
- **Yalnızca İnsan Kaynakları'nı kaldırın.** Bu seçenek Microsoft Power Apps ve Power Automate 'içinde kullanılan verilerle doldurulan bir Power Apps ortamı olması durumunda uygundur.


> [!Important]
> Power Apps ortamını kaldırmadan önce, İnsan Kaynakları kapsamı dışındaki veri tümleştirmeleri için kullanılmadığından emin olun. Varsayılan Power Apps ortamlarının da kaldırılamayacağını unutmayın. 

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

Human Resources ortamınızın bağlı olduğu Power Apps ortamını yazılımla silerseniz, LCS'de İnsan Kaynakları ortamının durumu **Geçici olarak silindi** olur. Bu durumda, kullanıcılar Human Resources'a bağlanamaz.

Ortamı geri yüklemek için:

1. [Power Apps ortamını kurtarma](/power-platform/admin/recover-environment) bölümündeki yönergeleri uygulayın.

2. Human Resources ortamını geri yüklemek için Destek birimine başvurun. Daha fazla bilgi için [Destek alma](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md) bölümüne bakın.

> [!Warning]
> Power Apps ortamları silme işleminden sonra yalnızca yedi gün süreyle kaydedilir. Ortamı yedi gün içinde kurtarmanız gerekir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

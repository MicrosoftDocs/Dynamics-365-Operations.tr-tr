---
title: Talent ortamlarını kaldırma
description: Bu konuda, Dynamics 365 Talent için bir test sürüşü kaldırma yeni bir üretim ortam işlemi adım adım anlatılmaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: e752d658388fc6cb6f4b84ac83cb12a71522199b
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898122"
---
# <a name="remove-talent-environments"></a>Talent ortamlarını kaldırma

Bu konuda, Dynamics 365 Talent için bir test sürüşü kaldırma yeni bir üretim ortam işlemi adım adım anlatılmaktadır.

## <a name="removing-a-test-drive-environment"></a>Bir test ortamını kaldırma

Talent test ortamları 60 günlük süre sonu ilkesi ile sunulur. Ancak, test ortamları sahipleri aşağıdaki adımları uygulayarak denemelerini daha erken sonlandırabilir. 

1. [Power Apps Yönetim Merkezi](https://admin.businessplatform.microsoft.com/)'ne gidin.
2. **Ortamlar**'ı seçin.
3. Test ortamını seçin. Test ortamı adı şuna benzer bir düzene sahiptir: TestDrive - alias@domain
4. **Sil**'i seçin ve kararı onaylayın. 

Var olan test ortamı kaldırılır. Kaldırıldığında, yeni bir test ortamı için kaydolabilirsiniz. 

## <a name="removing-a-production-environment"></a>Bir üretim ortamını kaldırma

Bu konuda, Talent'ı bir Bulut Çözümü Sağlayıcısı (CSP) veya kurumsal mimari (EA) sözleşmesi aracılığıyla aldığınız varsayılır. 

Tek bir Talent ortamı tek bir Power Apps ortamı içinde "yer aldığından", dikkate alınması gereken iki seçenek vardır. İlk seçenek tüm Power Apps ortamını kaldırmayı, ikinci seçenek yalnızca Talent'ı kaldırmayı içerir. İlk seçenek, Power Apps ortamını özellikle Talent sağlamak için oluşturmuş, uygulamaya henüz başlamış veya herhangi bir tümleştirme yapmamış olmanız durumunda tercih edilir. İkinci seçenek Power Apps ve Power Automate'ten alınan zengin verilerle doldurulan bir Power Apps ortamınız olması durumunda uygundur.

> [!Important]
> Power Apps ortamını kaldırmadan önce, Talent kapsamı dışındaki zengin veri tümleştirmeleri için kullanılmadığından emin olun. Varsayılan Power Apps ortamlarının da kaldırılamayacağını unutmayın. 

Talent ve ilişkili uygulamalar ve akışlar dahil tüm Power Apps ortamını kaldırmak için:

1. [Power Apps Yönetim Merkezi](https://admin.businessplatform.microsoft.com/)'ne gidin.
2. **Ortamlar**'ı seçin.
3. Kaldırılacak ortamı seçin.
4. **Sil**'i seçin ve kararı onaylayın. 
5. Silme işlemi tamamlanana kadar bekleyin.
6. Talent'a abone olmak için kullandığınız hesabı kullanarak [Lifecycle Services](https://lcs.dynamics.com/Logon/Index)'da (LCS) oturum açın. 
7. Ortamı içeren Talent Projesini seçin. 
8. LCS projenizde **Talent Uygulama Yöneticisi** kutucuğunu seçin. 
9. Kaldırılacak örneği seçin. 
10. **Örneği kaldır**'ı seçin ve ardından kararınızı onaylayın.  

Talent ortamını mevcut bir Power Apps ortamından kaldırmak için aşağıdaki adımları uygulayın. Bu özellik doğrudan LCS içinden etkinleştirilene kadar, Talent DevOps ekibine başvurmak ve destek almak geçicidir.

1. Kaldırma isteğini başlatmak için Destek birime başvurun.
2. Destek ekibi Talent DevOps ekibiyle kaldırma isteğini başlatacaktır. 
3. Ortamın kaldırıldığı hakkında bilgi aldıktan sonra devam edin.
4.  Talent'a abone olmak için kullandığınız hesabı kullanarak LCS'de oturum açın. 
5. Ortamı içeren Talent projesini seçin. 
6. LCS projenizde **Talent Uygulama Yöneticisi** kutucuğunu seçin. 
7. Kaldırmak istediğiniz örneği seçin. Bu örneğin Dağıtım durumu **Başarısız** olarak işaretlenmiş olmalıdır.
8. **Örneği kaldır**'ı seçin ve ardından kararınızı onaylayın. 


---
title: Örneği kaldır
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5c5f875ad9361c31af4fbe863488b881cdd97a6e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010815"
---
# <a name="remove-an-instance"></a>Örneği kaldır

Bu konuda, Microsoft Dynamics 365 Human Resources için bir test sürüşü kaldırma yeni bir üretim ortam işlemi adım adım anlatılmaktadır.

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
4.  İnsan Kaynaklarına abone olmak için kullandığınız hesabı kullanarak LCS'de oturum açın. 
5. Ortamı içeren İnsan Kaynakları Projesini seçin. 
6. LCS projenizde **İnsan Kaynakları Uygulama Yöneticisi** kutucuğunu seçin. 
7. Kaldırmak istediğiniz örneği seçin. Bu örneğin Dağıtım durumu **Başarısız** olarak işaretlenmiş olmalıdır.
8. **Örneği kaldır**'ı seçin ve ardından kararınızı onaylayın. 

---
title: Satınalma ilkeleri oluşturma
description: Bu prosedür satınalma için iş süreçlerinize uygun olacak şekilde satınalma ilkelerinin nasıl oluşturulacağını gösterir.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3bd4d6f8625c91f2190e994f04cbec4548272f04
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "312911"
---
# <a name="create-purchasing-policies"></a>Satınalma ilkeleri oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu prosedür satınalma için iş süreçlerinize uygun olacak şekilde satınalma ilkelerinin nasıl oluşturulacağını gösterir. Satınalma ilkelerini oluşturmadan önce satın alma ilkesi parametrelerini ayarlamanız gerekir. Bir satınalma ilkesini oluşturmak, değiştirmek ve çıkarmak mümkündür ancak satınalma ilkesini silemezsiniz. Bu prosedür genellikle bir satınalma yöneticisi tarafından gerçekleştirilir. Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.


## <a name="set-up-policy-parameters"></a>İlke parametrelerini ayarlayın
1. Satınalma ilkeleri'ne gidin.
2. Parametreler'e tıklayın.
    * İlke önceliği kuralları kuruluşunuzdaki farklı düzeylere uygulanır. Kuruluş hiyerarşinize göre gösterilen kuruluş birimleri ve Tedarik dahili kontrolü amacına atanan hiyerarşideki düzeyler. Örneğin, kuruluşunuzun yasal varlıkları, maliyet merkezleri, bölgeleri ve departmanları olabilir, ancak yalnızca bazıları Tedarik dahili kontrolünün hiyerarşi amacına sahip olabilir. Varsayılan olarak, kuruluşun Şirket türü kullanılabilir.  
3. İlke kuralı türü parametreleri sekmesine tıklayın.
4. Ağaçta, 'Satınalma ilkesi\ Satınalma talebi kontrol kuralı'nı seçin.
    * İlke düzeyinde ilke çözümü için öncelik sırasını tanımlayın. Ancak, bazı ilke türleri için tek tek ilke kuralı türlerine ilişkin öncelik sırasını geçersiz kılabilirsiniz. Örneğin, satınalma ilkeleri için öncelik sırasını maliyet merkezi, departman, şirket olarak tanımlayabilirsiniz. Katalog ilke kuralı için öncelik sırasını departman, maliyet merkezi, şirket olarak tanımlamak isteyebilirsiniz. Katalog ilke kuralı için öncelik sırasını değiştirebilirsiniz. Bir çalışan talep oluşturduğunda görüntülenecek katalog çalışanın departmanı, sonra maliyet merkezi ve son olarak şirketiyle ilişkili ilkeler tarafından belirlenir.  
    * Birden fazla organizasyon düzeyi listelenmişse Satınalma talebi kontrol kuralı için öncelik sırasını ayarlamak amacıyla Yukarı/Aşağı okları kullanabilirsiniz.  
5. Sayfayı kapatın.

## <a name="create-a-new-policy"></a>Yeni bir ilke oluştur
1. Yeni'ye tıklayın.
2. İsim alanına bir değer yazın.
3. Açıklama alanına bir değer girin.
    * Tek bir satın alma ilkesini yalnızca bir kuruluş hiyerarşisine uygulayabilirsiniz. Örneğin, 'Coğrafi' olarak ve "Bölüm" olarak adlandırılan bir hiyerarşiye sahipseniz her biri için farklı bir satın alma ilkesi vardır.  
    * İlkenin uygulanması gereken bir kuruluş seçin.  
4. Seçilen kuruluşu eklemek için oka tıklayın.
    * Daha fazla kuruluş eklemek için bu işlemi yineleyebilirsiniz.  

## <a name="add-a-policy-rule"></a>İlke kuralı ekleyin
1. İlke kuralı türü listesinde Talep amacı kuralı'nı seçin.
    * Varsayılan talep amacını Tüketim türüne ayarlayan ancak bunun yerine seçilecek Stok yenileme türüne izin veren bir kural oluşturacaksınız.  
2. İlke kuralı oluştur'a tıklayın.
3. El ile geçersiz kılmaya izin ver alanında Evet'i seçin.
4. Kapat’a tıklayın.
    * Şimdi satın alma ilkesi için diğer ilke kurallarını ayarlayabilirsiniz.   İlke kuralı türünün tek bir tedarik ilkesi ile aynı sürede etkin olan çakışan kurallara sahip olamayacağına dikkat edin.  
5. Sayfayı kapatın.
6. Sayfayı kapatın.


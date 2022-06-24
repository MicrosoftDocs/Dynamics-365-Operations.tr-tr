---
title: Satınalma ilkeleri oluşturma
description: Bu makale satınalma için iş süreçlerinize uygun olacak şekilde satınalma ilkelerinin nasıl oluşturulacağını gösterir.
author: GalynaFedorova
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 011705723466d746fa5b23c5499d03a548f133f1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878859"
---
# <a name="create-purchasing-policies"></a>Satınalma ilkeleri oluşturma

[!include [banner](../../includes/banner.md)]

Bu makale satınalma için iş süreçlerinize uygun olacak şekilde satınalma ilkelerinin nasıl oluşturulacağını gösterir. Satınalma ilkelerini oluşturmadan önce satın alma ilkesi parametrelerini ayarlamanız gerekir. Bir satınalma ilkesini oluşturmak, değiştirmek ve çıkarmak mümkündür ancak satınalma ilkesini silemezsiniz. Bu prosedür genellikle bir satınalma yöneticisi tarafından gerçekleştirilir. Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.


## <a name="set-up-policy-parameters"></a>İlke parametrelerini ayarlayın
1. Gezinti bölmesinde **Modüller > Tedarik ve kaynak atama > Ayar > İlkeler > Satınalma ilkeleri**.
2. Eylem Bölmesi'nde, **Parametreler**'i seçin.
- İlke önceliği kuralları kuruluşunuzdaki farklı düzeylere uygulanır. Kuruluş hiyerarşinize göre gösterilen kuruluş birimleri ve Tedarik dahili kontrolü amacına atanan hiyerarşideki düzeyler. Örneğin, kuruluşunuzun yasal varlıkları, maliyet merkezleri, bölgeleri ve departmanları olabilir, ancak yalnızca bazıları Tedarik dahili kontrolünün hiyerarşi amacına sahip olabilir. Varsayılan olarak, kuruluşun Şirket türü kullanılabilir.  
3. **İlke kuralı türü parametreleri** sekmesini seçin.
4. Ağaçta, **Satınalma ilkesi > Satınalma talebi kontrol kuralı**'na gidin.
- İlke düzeyinde ilke çözümü için öncelik sırasını tanımlayın. Ancak, bazı ilke türleri için tek tek ilke kuralı türlerine ilişkin öncelik sırasını geçersiz kılabilirsiniz. Örneğin, satınalma ilkeleri için öncelik sırasını maliyet merkezi, departman, şirket olarak tanımlayabilirsiniz. Katalog ilke kuralı için öncelik sırasını departman, maliyet merkezi, şirket olarak tanımlamak isteyebilirsiniz. Katalog ilke kuralı için öncelik sırasını değiştirebilirsiniz. Bir çalışan talep oluşturduğunda görüntülenecek katalog çalışanın departmanı, sonra maliyet merkezi ve son olarak şirketiyle ilişkili ilkeler tarafından belirlenir.  
- Birden fazla organizasyon düzeyi listelenmişse Satınalma talebi kontrol kuralı için öncelik sırasını ayarlamak amacıyla Yukarı/Aşağı okları kullanabilirsiniz.  
5. Sayfayı kapatın.

## <a name="create-a-new-policy"></a>Yeni bir ilke oluştur
1. **Yeni**'yi seçin.
2. **Ad** alanına bir değer yazın.
3. **Tanım** alanına bir değer girin.
- Tek bir satın alma ilkesini yalnızca bir kuruluş hiyerarşisine uygulayabilirsiniz. Örneğin, 'Coğrafi' olarak ve "Bölüm" olarak adlandırılan bir hiyerarşiye sahipseniz her biri için farklı bir satın alma ilkesi vardır.  
- İlkenin uygulanması gereken bir kuruluş seçin.  
4. Seçilen kuruluşu eklemek için oku seçin.
- Daha fazla kuruluş eklemek için bu işlemi yineleyebilirsiniz.  

## <a name="add-a-policy-rule"></a>İlke kuralı ekleyin
1. **İlke kuralı türü** listesinde **Talep amacı kuralı**'nı seçin.
- Varsayılan talep amacını Tüketim türüne ayarlayan ancak bunun yerine seçilecek Stok yenileme türüne izin veren bir kural oluşturacaksınız.  
2. **İlke kuralı oluştur**'u seçin.
3. **El ile geçersiz kılmaya izin ver** alanında **Evet**'i seçin.
4. **Kapat**'ı seçin.
- Şimdi satın alma ilkesi için diğer ilke kurallarını ayarlayabilirsiniz. İlke kuralı türünün tek bir tedarik ilkesi ile aynı sürede etkin olan çakışan kurallara sahip olamayacağına dikkat edin.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]